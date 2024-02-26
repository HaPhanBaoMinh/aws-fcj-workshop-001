---
title: "Create Deployment Group"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: "<b>6.3 </b>"
---

1. Access **aws-ci-cd-codedeploy** in **CodeDeploy** that we created earlier.

    - Click **Create deployment group**.

    ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/4.png)

2. In the **Create deployment group** screen:

    - Enter **Deployment group name** as **```aws-ci-cd-deploy-group```**.

    ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/5.png)

    - Under **Service role**, select **CodeDeployServiceRole**.

    ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/6.png)

    - For **Deployment type**, choose **In-place**.

    ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/7.png)

    - Under **Environment configuration**:

        - Choose **Amazon EC2 instances**.

        - **Name**: **aws-ci-cd-ec2** This is the name of the EC2 instance we created.

    ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/8.png)

    - For **Agent configuration with AWS Systems Manager**:

        - Select **Never** for **Install AWS CodeDeploy Agent**. We have already installed the CodeDeploy Agent and do not need updates at this time.

    ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/9.png)

    - Under **Deployment settings**:

        - Choose **CodeDeployDefault.AllAtOnce**.

    ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/10.png)

    - For **Load balancer**:

        - Uncheck **Enable load balancing**.

    ![CodeDeploy](/aws-fcj-workshop-001/6-CodeDeploy/11.png)

    - Click **Create deployment group**.
