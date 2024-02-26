---
title : "Tạo CodeBuild"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

#### Tạo CodeBuild

1. Chúng ta truy cập vào **CodeBuild**

    Chọn **Build projects** sau đó chọn **Create project**

    ![CodeCBuild](/images/3-CodeBuild/1.png)

2. Trong giao diện **Create build project**

    Nhập **```aws-ci-cd-codebuild```** cho **Project name**.

3. Mục **Source**

    ![CodeCBuild](/images/3-CodeBuild/2.png)

    - Mục **Source provider** là **AWS CodeCommit**

    - Mục **Repository** là **aws-ci-cd-codecommit** - Tên CodeCommit mà chúng ta đã tạo

    - Chọn **Branch**

    - Chọn **main**
 
4. Mục **Environment**

    ![CodeCBuild](/images/3-CodeBuild/3.png)

    - Phần **Service role** chúng ta chọn **New service role** để AWS tạo cho chúng ta 1 service role mới 

5. Mục **Buildspec**

    ![CodeCBuild](/images/3-CodeBuild/4.png)

    - Chúng ta chọn **Use a buildspec file** từ đó **CodeBuild** sẽ đọc file **buildspec.yml** trong **CodeCommit**

6. Mục **Logs**

    ![CodeCBuild](/images/3-CodeBuild/5.png)

    - Chọn **CloudWatch logs - optional**

    - Ở đây **build output** chúng ta đã đẩy lên **ECR** nên không chọn mục **S3**

7. Hoàn thành **build project**

    ![CodeCBuild](/images/3-CodeBuild/6.png)

