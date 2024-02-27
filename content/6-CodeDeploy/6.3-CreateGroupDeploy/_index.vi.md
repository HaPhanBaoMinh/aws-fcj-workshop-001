---
title : "Tạo Group Deploy"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 6.3 </b> "
---

1. Chúng ta truy cập vào **aws-ci-cd-codedeploy** trong **CodeDeploy** mà chúng ta đã tạo.

    - Chọn **Create deployment group**

    ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/4.png)

2. Màn hình **Create deployment group**

    - Mục **Deployment group name** điền **```aws-ci-cd-deploy-group```**

    ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/5.png)

    - Mục **Service role** chúng ta chọn **CodeDeployServiceRole**

    ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/6.png)

    - Mục **Deployment type** chúng ta chọn chiến thuật deploy **In-place**

        ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/7.png)

    - Mục **Environment configuration**

        - Chọn **Amazon EC2 instances**

        - **Name** : **aws-ci-cd-ec2** Đây là tên của EC2 mà chúng ta đã tạo

        ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/8.png)

    - Mục **Agent configuration with AWS Systems Manager**

        - **Install AWS CodeDeploy Agent** chúng ta chọn **Never**

        - Ở phần này chúng ta đã cài đặt CodeDeploy Agent và không có nhu cầu update

        ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/9.png)

    - Mục **Deployment settings** 

        - Chọn **CodeDeployDefault.AllAtOne**

        ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/10.png)

    - Mục **Load balancer**

        - Uncheck **Enable load balancing**

        ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/11.png)

    - **Create deployment group**








