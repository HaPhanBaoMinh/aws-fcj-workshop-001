---
title: "Create SNS for Notifications - Optional"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 7.3 </b> "
---

#### Create SNS for Notifications - Optional

1. Access **SNS**

    - Select **Topics**

    - Click on **Create topic**

    ![CodePipeline](/images/7-CodePipeline/13.png)

2. In the **Create topic** interface

    - Choose **Standard** for the type

    - In the **Name** field, enter **```AWS-CICD-TOPIC```**

    - Click **Create topic**

    ![CodePipeline](/images/7-CodePipeline/14.png)

3. Access **SNS**

    - Select **Subscriptions**

    - Click on **Create subscription**

    ![CodePipeline](/images/7-CodePipeline/15.png)

4. In the **Create subscription** screen

    - Choose the topic ARN we created **AWS-CICD-TOPIC** in **Topic ARN**

    - For **Protocol**, select **```Email```**

    - In the **Endpoint** field, enter the email address where you want to receive notifications

    - Click **Create subscription**

    ![CodePipeline](/images/7-CodePipeline/16.png)

5. Go to your email to confirm the subscription

    ![CodePipeline](/images/7-CodePipeline/17.png)

6. Assign **notification** to **Codepipeline**

    - In the **Notification name** field, enter **```aws-ci-cd-pipeline-noti```**

    ![CodePipeline](/images/7-CodePipeline/18.png)

    - Select the events for which you want to receive notifications

    ![CodePipeline](/images/7-CodePipeline/19.png)

    - In the **Targets** section, choose the SNS topic we created

    ![CodePipeline](/images/7-CodePipeline/20.png)

    - Click **Submit**
