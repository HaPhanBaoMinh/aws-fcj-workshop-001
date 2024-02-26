---
title : "CodeBuild"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---

#### AWS CodeBuild

#### Xây dựng và kiểm thử mã với khả năng điều chỉnh quy mô tự động

![CodeCommit](/images/3-CodeBuild/0.png)

![CodeCommit](/images/Intro/2.png)

- Tránh phải thiết lập, quản lý hoặc vá lỗi cho các máy chủ xây dựng riêng của bạn.

- Tự động điều chỉnh quy mô dung lượng để các bản dựng mất thời gian chờ trong hàng đợi khi chạy.

- Chỉ cần thanh toán cho số phút dựng bạn sử dụng.

- Sử dụng môi trường xây dựng được đóng gói sẵn hoặc của riêng bạn, cũng như mã hóa tạo tác bằng các khóa của riêng bạn.

#### Use cases

- **Tự động hóa quy trình tích hợp liên tục và phân phối liên tục (CI/CD)**: Tạo một quy trình phát hành phần mềm hoàn toàn tự động, khuyến khích thay đổi mã thông qua nhiều môi trường triển khai.

- **Loại bỏ tính phức tạp của việc quản lý các máy chủ xây dựng**: Chạy các tác vụ xây dựng Jenkins hiện có của bạn trên CodeBuild để không cần phải cấu hình và quản lý các nút xây dựng Jenkins.

- **Xây dựng mã nguồn được lưu trữ trên GitHub**: Tự động triển khai các bản dựng phần mềm bằng cách sử dụng kho lưu trữ GitHub sẵn có và đăng tải kết quả lên GitHub.
