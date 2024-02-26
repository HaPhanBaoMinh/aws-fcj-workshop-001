---
title : "Kiểm tra kết nối SSH tới EC2"
date :  "`r Sys.Date()`" 
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

1. Quay trở lại trang chủ và hãy chắc chắn rằng **Instance state**  của bạn đã ở trạng thái **Running**

    ![EC2](/images/4-EC2/9.png)

2. Tiến hành kết nối **SSH** tới EC2 Instance

    - Chọn EC2 vừa tạo

    - Chọn **Connect**

    - Ở màn hình **Connect to instance** chúng ta chọn **SSH client**

    ![EC2](/images/4-EC2/10.png)

    ![EC2](/images/4-EC2/11.png)

3. Mở cửa sổ **Terminal** và tiến hành kết nối

    - Hãy di chuyển tới folder chứa file **key pair** mà chúng ta đã tạo

            chmod 400 <key-pair-name.pem>

    - Tiến hành kết nối

            ssh -i "mac-key.pem" ec2-user@ec2-13-215-154-122.ap-southeast-1.compute.amazonaws.com

    Các bạn có thể lấy thông tin kết nối ở trang **Connect to instance** 

    ![EC2](/images/4-EC2/12.png)

4. Kết nối thành công

    ![EC2](/images/4-EC2/13.png)
