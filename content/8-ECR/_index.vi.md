---
title : "ECR"
date :  "`r Sys.Date()`" 
weight : 8
chapter : false
pre : " <b> 8. </b> "
---

#### AWS ECR

#### Dễ dàng lưu trữ, chia sẻ và triển khai phần mềm bộ chứa của bạn ở bất cứ nơi nào

![ECR](/aws-fcj-workshop-001/8-ECR/0.jpeg)

![ECR](/aws-fcj-workshop-001/Intro/5.png)

- Đưa images bộ chứa lên Amazon ECR mà không cần cài đặt hoặc mở rộng cơ sở hạ tầng và lấy hình ảnh bằng bất kỳ công cụ quản lý nào.

- Chia sẻ và tải xuống images một cách an toàn qua Giao thức truyền siêu văn bản bảo mật (HTTPS) với tính năng mã hóa tự động và kiểm soát truy cập.

- Truy cập và phân phối images nhanh hơn, giảm thời gian tải xuống và cải thiện tính khả dụng bằng cơ sở hạ tầng ổn định, có quy mô linh hoạt.

#### Use cases

- **Quản lý lỗ hổng phần mềm**: Sử dụng Amazon Inspector - dịch vụ quản lý lỗ hổng được tích hợp chặt chẽ - để đáp ứng các yêu cầu bảo mật về tuân thủ images, từ đó tự động hóa quá trình quét đánh giá lỗ hổng và định tuyến nhãn khắc phục.

- **Hợp lý hóa khối lượng công việc triển khai**: Xuất bản các ứng dụng trong bộ chứa chỉ với một lệnh duy nhất và dễ dàng tích hợp những môi trường tự quản lý của bạn.

- **Quản lý các chính sách về vòng đời của hình ảnh**: Tự động lưu các hình ảnh gần đây nhất và lưu trữ hình ảnh bạn không cần đến. Sử dụng quy tắc và gắn thẻ để nhanh chóng truy cập hình ảnh.

