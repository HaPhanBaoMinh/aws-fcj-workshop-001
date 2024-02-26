---
title : "Cài đặt Docker"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 5.4 </b> "
---

Tài liệu tham khảo [Tại đây](https://www.cyberciti.biz/faq/how-to-install-docker-on-amazon-linux-2/)

1. Cài đặt **Docker**

        sudo yum install docker

    ![EC2](/aws-fcj-workshop-001/-workchop-001j-workshop-001/4-EC2/18.png)

2. Thêm **group membership** cho **ec2-user** để có thể thực hiện các lệnh **docker** mà không cần quyền **sudo**

        sudo usermod -a -G docker ec2-user 

        id ec2-user

        # Reload a Linux user's group assignments to docker w/o logout

        newgrp docker

3. Cấu hình để docker để có thể chạy lúc **AMI boot time**:

        sudo systemctl enable docker.service

4. Tiến hành chạy **Docker**

        sudo systemctl start docker.service

5. Kiểm tra trạng thái **Docker**

        sudo systemctl status docker.service

    ![EC2](/aws-fcj-workshop-001/-workchop-001j-workshop-001/4-EC2/19.png)

    Nếu kết quả như này là đã chạy docker thành công.

