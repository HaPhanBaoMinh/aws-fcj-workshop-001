---
title : "Tạo SNS để nhận thông báo - Optional"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 7.3 </b> "
---

#### Tạo SNS để nhận thông báo - Optional

1. Truy cập **SNS**

    - Chọn **Topics**

    - Chọn **Create topic**

    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/13.png)

2. Ở màn hình **Create topic**

    - Type chọn **Standard**

    - Mục **Name** chọn **```AWS-CICD-TOPIC```**

    - **Create topic**

    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/14.png)

3. Truy cập **SNS**

    - Chọn **Subscriptions**

    - Chọn **Create subscription**

    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/15.png)

4. Ở màn hình **Create subscription**

    - Ở **Topic ARN** chọn topic ARN mà chúng ta đã tạo **AWS-CICD-TOPIC**

    - Mục **Protocol** chọn **```Email```**

    - Mục **Endpoint** điền email bạn muốn nhận thông báo

    - **Create subscription**

    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/16.png)

5. Vào gmail để xác nhận

    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/17.png)

6. Gán **notification** cho **Codepipeline**

    - Mục **Notification name** điền **```aws-ci-cd-pipeline-noti```**

    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/18.png)

    - Chọn 1 số sự kiện mà bạn muốn nhận thông báo 
    
    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/19.png)

    - Phần **Targets** chọn SNS mà chúng ta đã tạo

    ![CodePipeline](/aws-fcj-workshop-001/7-CodePipeline/20.png)

    - **Submit**
