---
title: "Create EC2"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: "<b> 5.1 </b>"
---

#### Create EC2

1. Navigate to [EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#Instances:v=3;$case=tags:true%5C,client:false;$regex=tags:false%5C,client:false) and select **Launch instances**.

    ![EC2](/images/4-EC2/1.png)

2. In the **Name and tags** section of the instance, enter **```aws-ci-cd-ec2```**.

    ![EC2](/images/4-EC2/2.png)

3. Proceed to select an **AMI**:

    - Choose **Quick Start**.

    - Select **Amazon Linux 2**.

    - Choose an **AMI**.

    ![EC2](/images/4-EC2/3.png)

4. Create a **Key pair**:

    - Select **Create key pair**.

    - For **Key pair name**, enter **```aws-ci-cd-ec2-key```** (optional name, you can choose any).

    - For **Key pair type**, select RSA.

    - For **Private key file format**, select **.pem**.

    - Select **Create key pair**.

    ![EC2](/images/4-EC2/5.png)

    ![EC2](/images/4-EC2/6.png)

5. Choose an **Instance type**.

    ![EC2](/images/4-EC2/4.png)

6. **Network settings**:

    - Select **Create security group**.

    - Allow SSH traffic from and Allow HTTP traffic from the internet.

    ![EC2](/images/4-EC2/7.png)

7. Proceed to **Launch instance**.

    ![EC2](/images/4-EC2/8.png)
