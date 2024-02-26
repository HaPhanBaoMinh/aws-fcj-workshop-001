---
title : "Cài đặt CodeDeploy Agent"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 5.3 </b> "
---

Tài liệu tham khảo [Tại đây](https://docs.aws.amazon.com/codedeploy/latest/userguide/codedeploy-agent-operations-install-linux.html)

1. Update **yum** và cài đặt các **packages** cần thiết

        sudo yum update

        sudo yum install ruby

        sudo yum install wget

    ![EC2](/aws-fcj-workshop-001/4-EC2/14.png)


2. Di chuyển tới **home directory**

        cd /home/ec2-user

3. Tải **CodeDeploy agent**

        wget https://aws-codedeploy-ap-southeast-1.s3.ap-southeast-1.amazonaws.com/latest/install

    Hiện tại mình đang thực hiện trên region **ap-southeast-1**, nếu các bạn thực hiện trên region khác thì có thể tham khảo link ở đầu page để có được thông tin cài đặt của region đó

    ![EC2](/aws-fcj-workshop-001/4-EC2/15.png)

    Sau khi cài đặt các bạn có thể thấy đã có file **install**


4. Tiến hành cấp quyền và cài đặt file **install**

        chmod +x ./install

        sudo ./install auto

    Cài đặt thành công

    ![EC2](/aws-fcj-workshop-001/4-EC2/16.png)

5. Kiểm tra trạng thái của CodeDeploy Agent

        systemctl status codedeploy-agent

    Như vậy là CodeDeploy Agent đã chạy thành công

    ![EC2](/aws-fcj-workshop-001/4-EC2/17.png)
