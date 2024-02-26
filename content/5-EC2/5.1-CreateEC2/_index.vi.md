---
title : "Tạo EC2"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 5.1 </b> "
---

#### Tạo EC2

1. Chúng ta truy cập vào [EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#Instances:v=3;$case=tags:true%5C,client:false;$regex=tags:false%5C,client:false)

    - Chọn **Launch instances**

    ![EC2](/images/4-EC2/1.png)

2. Mục **Name and tags** của instance chúng ta nhập **```aws-ci-cd-ec2```**

    ![EC2](/images/4-EC2/2.png)

3. Thực hiện chọn **AMI**

    - Chọn **Quick Start**

    - Chọn **Amazon Linux 2**

    - Chọn **AMI**

    ![EC2](/images/4-EC2/3.png)

4. Thực hiện tạo **Key pair**

    - Chọn **Create key pair**

    - **Key pair name** nhập **```aws-ci-cd-ec2-key```** (tên tùy chọn, bạn có thể đặt bất kỳ).

    - **Key pair type**, chọn RSA

    - **Private key file format**, chọn **.pem**

    - Chọn **Create key pair**

    ![EC2](/images/4-EC2/5.png)

    ![EC2](/images/4-EC2/6.png)


5. Thực hiện chọn **Instance type**

    ![EC2](/images/4-EC2/4.png)

6. Mục **Network settings**

    - Chọn **Create security group**

    - Chọn **Allow SSH traffic from** và **Allow HTTP traffic from the internet**

    ![EC2](/images/4-EC2/7.png)

7. Tiến hành **Launch instance**

    ![EC2](/images/4-EC2/8.png)

