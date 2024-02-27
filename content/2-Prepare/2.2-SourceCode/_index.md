---
title: "Source code"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: "<b>2.2 </b>"
---

#### Source Code Preparation

- You can obtain the source code [Here](/downloads/source_code.zip).

#### Source Code Structure

- Here we prepare a simple Express.js server.
- There are 2 files we need to pay attention to:
  - appspec.yml
  - buildspec.yml

![Folder](/aws-fcj-workshop-001/1-Prepare/4.png)

##### buildspec.yml

![Folder](/aws-fcj-workshop-001/1-Prepare/5.png)

- **version**

    Defines the version of buildspec.yml. In this case, it is **0.2**.

- **phases**

    Consists of 3 main phases: **install**, **pre_build**, **build**, **post_build**.

- **install**

    In this block, a version of Node.js (the latest version) is installed using runtime-versions.

    Then, Docker daemon is started using the command nohup /usr/local/bin/dockerd and a timeout of 15 seconds is set to wait until Docker daemon is ready.

    Docker daemon is started to listen on both UNIX socket (unix:///var/run/docker.sock) and TCP socket (tcp://127.0.0.1:2375).

    Overlay2 storage driver is used for Docker daemon.

- **pre_build**

    In this block, actions before the build process takes place are described.

    Logging in to Amazon ECR (Elastic Container Registry) is done using AWS CLI and getting the password by **aws ecr get-login-password**.

    A variable **$REPOSITORY_URI** is set to store the URI of the ECR repository.

    **$COMMIT_HASH** is used to get the first 7 characters of **CODEBUILD_RESOLVED_SOURCE_VERSION** returned from **CodeBuild**.

    **IMAGE_TAG** is used as a tag for the Docker image, defaulting to **latest**.

- **build**

    In this block, actions to build the Docker image are described.

    The **docker build** command is used to build a Docker image from the Dockerfile in the current directory and tag it as **$REPOSITORY_URI:latest**.

    The Docker image is retagged with the tag **$REPOSITORY_URI:$IMAGE_TAG**.

- **post_build**

    In this block, actions after the build process is done are described.

    The Docker image is pushed to Amazon ECR using the **docker push** command.

    An **imagedefinitions.json** file is generated, containing the definition of the Docker image with the name "exp-code-pipeline" and imageUri as $REPOSITORY_URI:$IMAGE_TAG.

##### appspec.yml

![Folder](/aws-fcj-workshop-001/1-Prepare/6.png)

- **version**

    Defines the version of the configuration file.

- **os**

    Specifies the operating system that this deployment process is designed to run on. In this case, the deployment process is expected to run on Linux.

- **files**

    Provides a list of files necessary for the deployment process.

- **hooks**

    Defines hooks (actions) in the deployment process, such as before installation (BeforeInstall) or when the application is started (ApplicationStart).

    **BeforeInstall:**

  - This is a hook called before the installation process begins.

  - **pull_docker_image.sh**: A script executed to pull a Docker image from a Docker repository.

  - Timeout is set to 300 seconds (5 minutes), and the commands are executed under the **root** user.

    **ApplicationStart**

  - This is a hook called after the installation process completes and the application is ready to start.

  - **start_docker_image.sh**: A script executed to start the previously pulled Docker image.

  - Timeout is set to 300 seconds (5 minutes), and the commands are executed under the **root** user.
