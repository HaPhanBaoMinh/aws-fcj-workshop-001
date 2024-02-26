---
title : "Tạo IAM cho CodeDeploy"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 6.1 </b> "
---

1. Chúng ta truy cập vào [IAM](https://us-east-1.console.aws.amazon.com/iam/home?region=ap-southeast-1#/home)

    - Chọn **Roles** sau đó chọn **Create role**

    ![IAM](/sws-fcj-workchop-001j-workshop-001/-workshop-001/6-CodeDeploy/12.png) 

2. Trong giao diện **Create role**

    - Mục **Service or use case** chúng ta tìm kiếm và chọn **CodeDeploy**

    - Chọn **Next**

    ![CodeDeploy](/sws-fcj-workchop-001j-workshop-001/-workshop-001/6-CodeDeploy/13.png)

3. Ở màn hình **Add permissions**

    - Phần **Permissions policies** đã được chọn sẵn

    - Chọn **Next**

4. Tiếp theo chúng ta thêm quyền **AmazonEC2RoleforAWSCodeDeploy** cho  **CodeDeployServiceRole**

    ![CodeDeploy](/sws-fcj-workchop-001j-workshop-001/-workshop-001/6-CodeDeploy/16.png)
    
    ![CodeDeploy](/sws-fcj-workchop-001j-workshop-001/-workshop-001/6-CodeDeploy/17.png)

    ![CodeDeploy](/sws-fcj-workchop-001j-workshop-001/-workshop-001/6-CodeDeploy/18.png)

5. Ở màn hình **Name, review, and create**

    - Điền **Role name** là **```CodeDeployServiceRole```**

    - Chọn **Create role**

    ![CodeDeploy](/sws-fcj-workchop-001j-workshop-001/-workshop-001/6-CodeDeploy/15.png)

