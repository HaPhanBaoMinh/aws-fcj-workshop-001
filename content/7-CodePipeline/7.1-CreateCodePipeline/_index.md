---
title: "Create CodePipeline"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: "<b> 7.1 </b>"
---

#### Create CodePipeline

1. Navigate to **CodePipeline**

    - Click **Pipelines**, then click **Create pipeline**.

    ![CodePipeline](/images/7-CodePipeline/1.png)

2. In the **Create new pipeline** screen:

    - **Step 1: Choose pipeline settings**

    - Set **Pipeline name** to **```aws-ci-cd-pipeline```**.

    - Click **Next**.

    ![CodePipeline](/images/7-CodePipeline/2.png)

    - **Step 2: Add source stage**

    - Choose **AWS CodeCommit** for **Source provider**.

    - Select **aws-ci-cd-codecommit** for **Repository name**, which we created when setting up **CodeCommit**.

    - Choose **main** for **Branch name**.

    - Click **Next**.

    ![CodePipeline](/images/7-CodePipeline/3.png)

    - **Step 3: Add build stage**

    - Choose **AWS CodeBuild** for **Build provider**.

    - Choose **Asia Pacific (Singapore)** for **Region**.

    - Select **aws-ci-cd-codebuild** for **Project name**, which we created when setting up **CodeBuild**.

    - Click **Next**.

    ![CodePipeline](/images/7-CodePipeline/4.png)

    - **Step 4: Add deploy stage**

    - Choose **AWS CodeDeploy** for **Deploy provider**.

    - Choose **Asia Pacific (Singapore)** for **Region**.

    - Select **aws-ci-cd-codedeploy** for **Application name**, which we created when setting up **CodeDeploy**.

    - Select **aws-ci-cd-deploy-group** for **Deployment group**, which we created when setting up the deployment group in **CodeDeploy**.

    - Click **Next**.

    ![CodePipeline](/images/7-CodePipeline/5.png)

    - **Step 5: Review**

    - Click **Create Pipeline**.

    ![CodePipeline](/images/7-CodePipeline/6.png)
