---
title: "Install Docker"
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: "<b> 5.4 </b>"
---

Reference documentation [Here](https://www.cyberciti.biz/faq/how-to-install-docker-on-amazon-linux-2/)

1. Install **Docker**:

        sudo yum install docker

    ![EC2](/aws-fcj-workshop-001/4-EC2/18.png)

2. Add **group membership** for **ec2-user** to execute **docker** commands without **sudo**:

        sudo usermod -a -G docker ec2-user 

        id ec2-user

        # Reload a Linux user's group assignments to docker without logout

        newgrp docker

3. Configure Docker to run at **AMI boot time**:

        sudo systemctl enable docker.service

4. Start **Docker**:

        sudo systemctl start docker.service

5. Check the status of **Docker**:

        sudo systemctl status docker.service

    ![EC2](/aws-fcj-workshop-001/4-EC2/19.png)

    If the result looks like this, Docker has been successfully started.
