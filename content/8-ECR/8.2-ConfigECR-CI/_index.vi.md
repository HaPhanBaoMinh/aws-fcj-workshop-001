---
title : "Cấu hình ECR cho CI"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 8.2 </b> "
---
 
1. Chúng ta truy cập vào [ECR](https://ap-southeast-1.console.aws.amazon.com/ecr/private-registry/repositories?region=ap-southeast-1)

   - Copy **URI** của repo vừa tạo

    ![ECR](/images/8-ECR/3.png)

2. Truy cập vào **CodeCommit**

    - Chọn **Repositories**

    - Truy cập vào repo mà chúng ta đã tạo **aws-ci-cd-codecommit**

    ![ECR](/images/8-ECR/4.png)

    - Truy cập file **buildspec.yml**

    ![ECR](/images/8-ECR/5.png)

    - Chọn **Edit** 

    - Thay đổi các **<ECR_REPOSITORY_URI>** thành **URI** của repo **ECR**

    - Thay đổi các **<region>** thành **ap-southeast-1**

    ![ECR](/images/8-ECR/6.png)

    - Sau khi thay đổi, điền 1 số thông tin cần thiết

    - **Commit changes**

    ![ECR](/images/8-ECR/7.png)








