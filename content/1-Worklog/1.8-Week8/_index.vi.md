---
title: "Worklog Tuần 8"
date: 08-06-2026
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---


### Mục tiêu tuần 8:

* Tìm hiểu kiến trúc hướng sự kiện bằng Amazon SNS và Amazon SQS.
* Làm quen với việc bảo vệ ứng dụng web và API bằng AWS WAF.
* Thực hành mã hóa dữ liệu trên Amazon S3 bằng AWS KMS.
* Củng cố cơ chế xác thực người dùng cho ứng dụng SPA bằng Amazon Cognito.
* Thực hành giám sát ứng dụng serverless bằng Amazon CloudWatch và AWS X-Ray.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu kiến trúc Event-driven<br>- Tìm hiểu Amazon SNS và Amazon SQS<br>- **Thực hành:**<br>&emsp; + Tạo SNS Topic<br>&emsp; + Tạo SQS Queue và Subscription<br>&emsp; + Gửi và nhận thông điệp<br>&emsp; + Cấu hình Filter Policy theo thuộc tính<br>&emsp; + Kiểm tra thông điệp được điều hướng đến từng Queue | 08/06/2026 | 08/06/2026 | <https://000077.awsstudygroup.com/vi/> |
| 3 | - Tìm hiểu AWS Web Application Firewall<br>- Tìm hiểu Web ACL, Managed Rules và Custom Rules<br>- **Thực hành:**<br>&emsp; + Chuẩn bị ứng dụng mẫu<br>&emsp; + Tạo Web ACL<br>&emsp; + Thêm AWS Managed Rules<br>&emsp; + Tạo Custom Rule cơ bản<br>&emsp; + Gửi request để kiểm tra Rule<br>&emsp; + Xem request được cho phép hoặc chặn | 09/06/2026 | 09/06/2026 | <https://000026.awsstudygroup.com/vi/> |
| 4 | - Tìm hiểu AWS Key Management Service<br>- Tìm hiểu Customer Managed Key và Key Policy<br>- **Thực hành cơ bản:**<br>&emsp; + Tạo Customer Managed Key<br>&emsp; + Cấu hình Key Administrator và Key User<br>&emsp; + Tạo S3 Bucket<br>&emsp; + Bật mã hóa S3 bằng AWS KMS<br>&emsp; + Upload và tải dữ liệu mã hóa<br>&emsp; + Kiểm tra quyền truy cập của người dùng | 10/06/2026 | 10/06/2026 | <https://000033.awsstudygroup.com/vi/> |
| 5 | - Tìm hiểu kiến trúc Single Page Application<br>- Tìm hiểu xác thực bằng Amazon Cognito<br>- **Thực hành cơ bản:**<br>&emsp; + Tạo Cognito User Pool<br>&emsp; + Tạo App Client<br>&emsp; + Tạo tài khoản người dùng kiểm thử<br>&emsp; + Tích hợp giao diện đăng ký và đăng nhập<br>&emsp; + Cấu hình Cognito Authorizer cho API Gateway<br>&emsp; + Gọi API bằng JWT Token | 11/06/2026 | 11/06/2026 | <https://000055.awsstudygroup.com/vi/> |
| 6 | - Tìm hiểu giám sát Lambda bằng Amazon CloudWatch<br>- Tìm hiểu Distributed Tracing bằng AWS X-Ray<br>- **Thực hành:**<br>&emsp; + Xem Lambda Logs trên CloudWatch<br>&emsp; + Theo dõi Duration, Errors và Invocations<br>&emsp; + Tạo CloudWatch Alarm cơ bản<br>&emsp; + Kích hoạt Active Tracing cho Lambda<br>&emsp; + Gọi API để tạo dữ liệu Trace<br>&emsp; + Xem Service Map và phân tích độ trễ<br>&emsp; + Dọn dẹp tài nguyên sau thực hành | 12/06/2026 | 12/06/2026 | <https://000085.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 8:

* Hiểu vai trò của kiến trúc Event-driven trong việc giảm sự phụ thuộc giữa các thành phần.
* Phân biệt được chức năng của Amazon SNS và Amazon SQS.
* Tạo được SNS Topic, SQS Queue và Subscription.
* Biết cách sử dụng Filter Policy để điều hướng thông điệp.
* Hiểu vai trò của AWS WAF trong việc bảo vệ ứng dụng web và API.
* Tạo được Web ACL sử dụng Managed Rules và Custom Rule cơ bản.
* Hiểu vai trò của AWS KMS trong việc quản lý khóa mã hóa.
* Tạo được Customer Managed Key và sử dụng để mã hóa dữ liệu trên Amazon S3.
* Phân biệt được quyền quản trị khóa và quyền sử dụng khóa.
* Hiểu cấu trúc cơ bản của một Single Page Application.
* Tạo được Cognito User Pool, App Client và người dùng kiểm thử.
* Tích hợp được Cognito Authorizer với Amazon API Gateway ở mức cơ bản.
* Biết cách sử dụng JWT Token để gọi API được bảo vệ.
* Theo dõi được Lambda Logs và các chỉ số cơ bản trên Amazon CloudWatch.
* Tạo được CloudWatch Alarm để phát hiện lỗi Lambda.
* Sử dụng AWS X-Ray để xem Service Map, Trace và độ trễ của request.