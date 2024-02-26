---
title : "Source code"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2.2 </b> "
---

#### Chuẩn bị source code

- Các bạn có thể lấy source code [Tại dây](/downloads/source_code.zip)

#### Cấu trúc source code

- Ở đây mình chuẩn bị một server Express.js đơn giản
- Có 2 file mà chúng ta cần chú ý
    - appspec.yml
    - buildspec.yml

![Folder](/images/1-Prepare/4.png)

##### buildspec.yml

![Folder](/images/1-Prepare/5.png)

- **version**

    Định nghĩa phiên bản của buildspec.yml Trong trường hợp này, nó là **0.2**.

- **phases**

    Gồm 3 phần chính **install**, **pre_build**, **build**, **post_build**.

- **install**

    Trong block này, một phiên bản của Node.js (phiên bản mới nhất) được cài đặt bằng runtime-versions.

    Sau đó, Docker daemon được khởi chạy sử dụng lệnh nohup /usr/local/bin/dockerd và timeout 15 giây được đặt để chờ đến khi Docker daemon sẵn sàng.

    Docker daemon được khởi chạy để lắng nghe trên cả UNIX socket (unix:///var/run/docker.sock) và TCP socket (tcp://127.0.0.1:2375).

    Trình điều khiển lưu trữ overlay2 được sử dụng cho Docker daemon.

- **pre_build**

    Trong block này sẽ mô tả những hành động trước khi quá trình build được diễn ra.

    Đăng nhập vào Amazon ECR (Elastic Container Registry) được thực hiện bằng cách sử dụng AWS CLI và lấy mật khẩu bằng **aws ecr get-login-password**

    Tạo biến **$REPOSITORY_URI** được đặt để lưu trữ URI của ECR repository.

    **$COMMIT_HASH** được sử dụng để lấy 7 ký tự đầu tiên của **CODEBUILD_RESOLVED_SOURCE_VERSION** trả về từ **CodeBuild**

    **IMAGE_TAG** được sử dụng làm tag cho Docker image, mặc định là **latest**.

- **build**

    Trong block này sẽ mô tả những hành động để tiến hành build Docker image

    Lệnh **docker build** được sử dụng để xây dựng Docker image từ Dockerfile trong thư mục hiện tại và đặt tag là **$REPOSITORY_URI:latest**.

    Docker image được đặt lại tag với tag là **$REPOSITORY_URI:$IMAGE_TAG**.

- **post_build**

    Trong block này sẽ mô tả những hành động sau khi quá trình build được thực hiện.

    Docker image được đẩy lên Amazon ECR bằng lệnh **docker push**.

    Một tệp **imagedefinitions.json** được tạo ra, chứa định nghĩa của Docker image với tên là "exp-code-pipeline" và imageUri là $REPOSITORY_URI:$IMAGE_TAG.

##### appspec.yml

![Folder](/images/1-Prepare/6.png)

- **version**

    Định nghĩa phiên bản của file cấu hình

- **os**

    Xác định hệ điều hành mà quy trình triển khai này được thiết kế để chạy trên. Trong trường hợp này, quy trình triển khai dự kiến sẽ chạy trên hệ điều hành Linux.

- **files**

    Cung cấp danh sách các tệp cần thiết cho quy trình triển khai.

- **hooks**

    Định nghĩa các hooks (khi chạy) trong quy trình triển khai, chẳng hạn như trước khi cài đặt (BeforeInstall) hoặc khi ứng dụng được khởi động (ApplicationStart).

    **BeforeInstall:**

    - Đây là một hook được gọi trước khi quy trình cài đặt bắt đầu.

    - **pull_docker_image.sh**: Một tập lệnh được thực thi để kéo (pull) Docker image từ một kho lưu trữ Docker.

    - Timeout được đặt là 300 giây (5 phút), và các tập lệnh được thực thi dưới quyền của người dùng **root**.

    **ApplicationStart**

    - Đây là một hook được gọi sau khi quy trình cài đặt hoàn tất và ứng dụng được sẵn sàng để khởi chạy.

    - **start_docker_image.sh**: Một tập lệnh được thực thi để khởi động Docker image đã được kéo (pulled) trước đó.

    - Timeout được đặt là 300 giây (5 phút), và các tập lệnh được thực thi dưới quyền của người dùng root.
