---
title : "Cấu hình ECR cho CD"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 8.3 </b> "
---
 
1. Chúng ta truy cập vào [ECR](https://ap-southeast-1.console.aws.amazon.com/ecr/private-registry/repositories?region=ap-southeast-1)

   - Copy **URI** của repo vừa tạo

    ![ECR](/images/8-ECR/3.png)

2. Truy cập vào **CodeCommit**

    - Chọn **Repositories**

    - Truy cập vào repo mà chúng ta đã tạo **aws-ci-cd-codecommit**

    ![ECR](/images/8-ECR/4.png)

3. Truy cập file **scripts** / **pull_docker_image.sh**

    - Chọn **Edit**

    ![ECR](/images/8-ECR/8.png)

    - Thay đổi các **DOCKER_IMAGE** thành **URI** của repo **ECR** của bạn lưu ý phải có tag **:latest**.

    - Thay đổi **region** theo **region** của **ECR**

    ![ECR](/images/8-ECR/9.png)

    - Sau khi thay đổi, điền 1 số thông tin cần thiết

    - **Commit changes**

    ![ECR](/images/8-ECR/7.png)

4. Truy cập file **scripts** / **start_docker_image.sh**

    - Chọn **Edit**

    ![ECR](/images/8-ECR/10.png)

    - Thay đổi các **DOCKER_IMAGE** thành **URI** của repo **ECR** của bạn lưu ý phải có tag **:latest**.

    ![ECR](/images/8-ECR/11.png)

    - Sau khi thay đổi, điền 1 số thông tin cần thiết

    - **Commit changes**

    ![ECR](/images/8-ECR/7.png)








