---
title : "Create IAM for CodeDeploy"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 6.1 </b> "
---

1. We access [IAM](https://us-east-1.console.aws.amazon.com/iam/home?region=ap-southeast-1#/home)

    - Select **Roles** and then click on **Create role**

    ![IAM](/images/6-CodeDeploy/12.png)

2. In the **Create role** interface

    - In the **Service or use case** section, search for and select **CodeDeploy**

    - Click **Next**

    ![CodeDeploy](/images/6-CodeDeploy/13.png)

3. In the **Add permissions** screen

    - The **Permissions policies** section is preselected

    - Click **Next**

4. Next, we add the **AmazonEC2RoleforAWSCodeDeploy** permission to the **CodeDeployServiceRole**

    ![CodeDeploy](/images/6-CodeDeploy/16.png)

    ![CodeDeploy](/images/6-CodeDeploy/17.png)

    ![CodeDeploy](/images/6-CodeDeploy/18.png)

5. In the **Name, review, and create** screen

    - Enter **Role name** as **```CodeDeployServiceRole```**

    - Click **Create role**

    ![CodeDeploy](/images/6-CodeDeploy/15.png)
