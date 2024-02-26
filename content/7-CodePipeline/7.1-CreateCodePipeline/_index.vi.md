---
title : "Tạo CodePipeline"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 7.1 </b> "
---

#### Tạo CodePipeline

1. Chúng ta truy cập vào **CodePipeline**

    - Chọn **Pipelines** sau đó chọn **Create pipeline**

    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/1.png)

2. Ở màn hình **Create new pipeline**

    - **Step 1: Choose pipeline settings**

    - Mục **Pipeline name** đặt tên **```aws-ci-cd-pipeline```**

    - **Next**

    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/2.png)

    - **Step 2: Add source stage**

    - Mục **Source provider** chọn **AWS CodeCommit**

    - Mục **Repository name** chọn **aws-ci-cd-codecommit** mà chúng ta đã tạo khi tạo **CodeCommit**

    - **Branch name** chọn **main**

    - **Next**

    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/3.png)

    - **Step 3: Add build stage**

    - Mục **Build provider** chọn **AWS CodeBuild**

    - Mục **Region** chọn **Asia Pacific (Singapore)**

    - Mục **Project name** chọn **aws-ci-cd-codebuild** mà chúng ta đã tạo khi tạo **CodeBuild**

    - **Next**

    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/4.png)

    - **Step 4: Add deploy stage**

    - Mục **Deploy provider** chọn **AWS CodeDeploy**

    - Mục **Region** chọn **Asia Pacific (Singapore)**

    - Mục **Application name** chọn **aws-ci-cd-codedeploy** mà chúng ta đã tạo khi tạo **Codedeploy**

    - Mục **Deployment group** chọn **aws-ci-cd-deploy-group** mà chúng ta đã tạo khi tạo **Codedeploy**

    - **Next**

    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/5.png)

    - **Step 5: Review**

    - **Create Pipeline**

    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/6.png)
