---
title: "Create CodeBuild"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: "<b> 4.1 </b>"
---

#### Create CodeBuild

1. Navigate to **CodeBuild**, select **Build projects**, then choose **Create project**.

    ![CodeCBuild](/images/3-CodeBuild/1.png)

2. In the **Create build project** interface:

    Enter **```aws-ci-cd-codebuild```** for the **Project name**.

3. **Source** Section

    ![CodeCBuild](/images/3-CodeBuild/2.png)

    - **Source provider**: AWS CodeCommit

    - **Repository**: **aws-ci-cd-codecommit** - The name of the CodeCommit repository we created.

    - Choose the **Branch**: **main**

4. **Environment** Section

    ![CodeCBuild](/images/3-CodeBuild/3.png)

    - For **Service role**, select **New service role** to let AWS create a new service role for us.

5. **Buildspec** Section

    ![CodeCBuild](/images/3-CodeBuild/4.png)

    - Select **Use a buildspec file**, so **CodeBuild** will read the **buildspec.yml** file from **CodeCommit**.

6. **Logs** Section

    ![CodeCBuild](/images/3-CodeBuild/5.png)

    - Choose **CloudWatch logs - optional**.

    - Since we pushed the **build output** to **ECR**, we won't select the **S3** option.

7. Complete the **build project**.

    ![CodeCBuild](/images/3-CodeBuild/6.png)
