---
title: "Configure ECR for CD"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: "<b>8.3 </b>"
---

1. We navigate to [ECR](https://ap-southeast-1.console.aws.amazon.com/ecr/private-registry/repositories?region=ap-southeast-1)

   - Copy the **URI** of the repository you just created

    ![ECR](/aws-fcj-workshop-001/8-ECR/3.png)

2. Access **CodeCommit**

    - Select **Repositories**

    - Access the repository we created **aws-ci-cd-codecommit**

    ![ECR](/aws-fcj-workshop-001/8-ECR/4.png)

3. Access the **scripts** / **pull_docker_image.sh** file

    - Choose **Edit**

    ![ECR](/aws-fcj-workshop-001/8-ECR/8.png)

    - Replace **DOCKER_IMAGE** with the **URI** of your **ECR** repository make sure it has the **:latest** tag.

    - Replace **region** with the **region** of your **ECR**

    ![ECR](/aws-fcj-workshop-001/8-ECR/9.png)

    - After making the changes, provide necessary information

    - **Commit changes**

    ![ECR](/aws-fcj-workshop-001/8-ECR/7.png)

4. Access the **scripts** / **start_docker_image.sh** file

    - Choose **Edit**

    ![ECR](/aws-fcj-workshop-001/8-ECR/10.png)

    - Replace **DOCKER_IMAGE** with the **URI** of your **ECR** repository make sure it has the **:latest** tag.

    ![ECR](/aws-fcj-workshop-001/8-ECR/11.png)

    - After making the changes, provide necessary information

    - **Commit changes**

    ![ECR](/aws-fcj-workshop-001/8-ECR/7.png)
