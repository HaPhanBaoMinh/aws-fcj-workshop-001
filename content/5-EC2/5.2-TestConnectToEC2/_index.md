---
title: "Check SSH Connection to EC2"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: "<b> 5.2 </b>"
---

1. Go back to the homepage and ensure that your **Instance state** is **Running**.

    ![EC2](/aws-fcj-workshop-001/4-EC2/9.png)

2. Connect via **SSH** to the EC2 Instance:

    - Select the EC2 instance you just created.

    - Choose **Connect**.

    - On the **Connect to instance** screen, select **SSH client**.

    ![EC2](/aws-fcj-workshop-001/4-EC2/10.png)

    ![EC2](/aws-fcj-workshop-001/4-EC2/11.png)

3. Open a **Terminal** window and establish the connection:

    - Navigate to the folder containing the **key pair** file we created.

            chmod 400 <key-pair-name.pem>

    - Proceed with the connection:

            ssh -i "mac-key.pem" ec2-user@ec2-13-215-154-122.ap-southeast-1.compute.amazonaws.com

    You can obtain the connection information from the **Connect to instance** screen.

    ![EC2](/aws-fcj-workshop-001/4-EC2/12.png)

4. Successful connection.

    ![EC2](/aws-fcj-workshop-001/4-EC2/13.png)
