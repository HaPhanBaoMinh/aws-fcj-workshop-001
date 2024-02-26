---
title : "CodePipeline"
date : "`r Sys.Date()`"
weight : 7
chapter : false
pre : " <b> 7. </b> "
---

#### AWS CodePipeline

#### Tự động hóa các quy trình phân phối liên tục để cung cấp các bản cập nhật nhanh chóng và ổn định

![CodePipeline](/images/7-CodePipeline/0.jpeg)

![CodePipeline](/images/Intro/4.jpg)

- Lập mô hình quy trình phát hành phần mềm của bạn và giảm thiểu công sức thiết lập hoặc cung cấp máy chủ.

- Xác định các giai đoạn trong quy trình phát hành phần mềm của bạn bằng Bảng điều khiển quản lý AWS hoặc Giao diện dòng lệnh (CLI) AWS.

- Nhanh chóng phát hành các tính năng mới, lặp lại dựa trên phản hồi và phát hiện lỗi bằng cách kiểm thử mỗi khi mã thay đổi.

- Điều chỉnh cho phù hợp với nhu cầu của bạn bằng cách sử dụng các plugin của riêng bạn hoặc các plugin tích hợp sẵn trong bất kỳ bước nào của quá trình phát hành.

#### Use cases

- **Xác định cấu trúc quy trình của bạn**: Cập nhật các quy trình hiện có và cung cấp mẫu để tạo ra những quy trình mới với một tài liệu JSON khai báo.

- **Nhận thông báo cho các sự kiện**: Giám sát các sự kiện tác động đến quy trình của bạn bằng Dịch vụ thông báo đơn giản (SNS) của Amazon với chức năng cung cấp tin nhắn trạng thái và liên kết đến nguồn sự kiện.

- **Kiểm soát và cấp quyền truy cập**: Quản lý những cá nhân có thể thay đổi và kiểm soát quy trình làm việc phát hành của bạn với Quản lý danh tính và truy cập (IAM) trong AWS.

- **Tích hợp hệ thống tùy chỉnh của riêng bạn**: Đăng ký một hành động tùy chỉnh và liên kết máy chủ vào quy trình của bạn bằng cách tích hợp tác tử nguồn mở CodePipeline với các máy chủ của bạn.
