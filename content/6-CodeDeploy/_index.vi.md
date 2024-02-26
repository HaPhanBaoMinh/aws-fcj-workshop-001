---
title : "CodeDeploy"
date :  "`r Sys.Date()`" 
weight : 6
chapter : false
pre : " <b> 6. </b> "
---

#### AWS CodeDeploy

#### Tự động hóa việc triển khai mã để duy trì thời gian hoạt động của ứng dụng

![CodeDeploy](/images/6-CodeDeploy/0.webp)

![CodeDeploy](/images/Intro/3.png)

- Tự động hóa và triển khai nhất quán các ứng dụng trên nhiều môi trường phát triển, kiểm thử và sản xuất của bạn.

- Theo dõi tình trạng của nhóm ứng dụng và tự động khôi phục các bản cập nhật khi cần.

- Khởi chạy và theo dõi trạng thái của các bản triển khai ứng dụng thông qua Bảng điều khiển quản lý AWS hoặc Giao diện dòng lệnh (CLI) AWS.

- Sử dụng lại mã thiết lập bạn hiện có và tích hợp với quy trình phát hành phần mềm hiện tại hay chuỗi công cụ phân phối liên tục.

#### Use cases

- **Tự động hóa việc triển khai để loại bỏ thao tác thủ công**: Lặp lại quy trình triển khai ứng dụng trên hàng loạt các nhóm hoặc phiên bản khác nhau bằng cách sử dụng mô hình cài đặt dựa trên tệp và lệnh.

- **Triển khai đến nhiều máy chủ**: Quản lý hoạt động triển khai đến hàng nghìn máy chủ bằng chức năng giám sát và chuyển lưu lượng nâng cao.

- **Sử dụng các kỹ thuật triển khai nâng cao**: Hỗ trợ nhiều phương thức triển khai, bao gồm tại chỗ, canary và triển khai lục/lam.

- **Giám sát tình trạng và trở về phiên bản trước**: Cấu hình các cảnh báo có chức năng trở về phiên bản trước và dừng quy trình triển khai ứng dụng đang diễn ra.
