---
title : "Kiểm tra thành quả"
date :  "`r Sys.Date()`" 
weight : 9
chapter : false
pre : " <b> 9. </b> "
---

1. Chúng ta truy cập vào **CodeCommit**

    ![Test](/images/9-Test/1.png)

2. Ở màn hình **aws-ci-cd-pipeline**

    - Chọn **Release change** 

    - Chọn **Release**

    ![Test](/images/9-Test/2.png)

3. Chờ đợi thành quả

    - Theo dõi từng bước

    ![Test](/images/9-Test/3.png)

4. Sau khi tất cả các bước thành công, chúng ta quay lại **EC2** và truy cập vào **Public IPv4 address**

    - Các bạn hãy chắc chắn rằng mình truy cập bằng **http**

    ![Test](/images/9-Test/4.png)

5. Kết quả

    ![Test](/images/9-Test/5.png)

6. Chúng ta hãy thử thay đổi code trong phần **CodePipeline** để quá trình CI/CD tự hoạt động

    - Truy cập **aws-ci-cd-codecommit / views / index.pug**

    - Chúng ta hãy thử thay đổi nội dung của thẻ **h1**

    - Sau đó tiến thành điền thông tin và **Commit**

    ![Test](/images/9-Test/6.png)

    ![Test](/images/9-Test/7.png)

7. Khi sau khi **Commit** khi quay lại **CodePipeline** chúng ta có thể thấy trạng thái đã tahy đổi thành **In progress**

    ![Test](/images/9-Test/8.png)

8. Khi tất cả step đã thành công thì quay lại truy cập vào **Public IPv4 address** của **EC2**

    ![Test](/images/9-Test/9.png)



