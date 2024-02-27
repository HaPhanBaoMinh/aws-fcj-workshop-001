---
title : "CodeCommit"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 3 </b> "
---

## AWS CodeCommit

#### Lưu trữ mã nguồn Git riêng tư một cách an toàn và mở rộng, cộng tác trên mã nguồn

![CodeCBuild](/aws-fcj-workshop-001/2-CodeCommit/0.jpeg)

![CodeCommit](/aws-fcj-workshop-001/-workshop-001/Intro/1.png)

- Không cần lưu trữ, bảo trì, sao lưu hoặc điều chỉnh quy mô các máy chủ kiểm soát nguồn của riêng bạn..

- Tùy chỉnh quyền truy cập cho từng người dùng vào kho lưu trữ của bạn với các tệp được mã hóa tự động trong quá trình truyền.

- Đảm bảo kho lưu trữ của bạn có độ sẵn sàng cao và truy cập được với kiến ​​trúc bền bỉ, có khả năng dự phòng và quy mô linh hoạt.

- Duy trì kho lưu trữ của bạn gần với môi trường xây dựng, dàn dựng và sản xuất của bạn trên AWS.

#### Các trường hợp sử dụng

- **Hợp tác trên mã nguồn**: Triển khai các quy trình làm việc bao gồm việc xem xét và phản hồi mã theo mặc định và kiểm soát ai có thể thực hiện thay đổi với các nhánh cụ thể.

- **Sử dụng các công cụ hiện có của bạn**: Tiếp tục sử dụng các phần bổ trợ môi trường phát triển, hệ thống tích hợp liên tục và phân phối liên tục (CI/CD) cũng như máy khách đồ họa mà bạn thích.

- **Nhận thông báo và tập lệnh tùy chỉnh**: Nhận thông báo qua Amazon Simple Notification Service (SNS) cho các sự kiện ảnh hưởng đến kho mã của bạn, và gửi thông báo để tạo webhook HTTP.

- **Tạo tối đa 5.000 kho lưu trữ theo mặc định**: Tạo tối đa 25.000 kho lưu trữ bổ sung theo yêu cầu, cũng như lưu trữ và lập phiên bản bất kỳ loại tệp nào.