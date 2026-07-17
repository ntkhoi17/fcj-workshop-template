---
title: "Worklog Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---


### Mục tiêu tuần 11:

* Tạo tài khoản quản trị và kiểm tra cơ chế xác thực bằng Amazon Cognito.
* Kiểm thử các API cơ bản của hệ thống DMS bằng JWT Token.
* Xác minh luồng upload tài liệu bằng Presigned URL và quá trình xử lý file sau khi quét.
* Kiểm tra API liệt kê, xem chi tiết và tải xuống tài liệu.
* Khởi chạy giao diện React trên môi trường local và thực hiện kiểm thử chức năng cơ bản.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tạo tài khoản quản trị trong Amazon Cognito<br>- Tìm hiểu luồng xác thực người dùng<br>- **Thực hành:**<br>&emsp; + Tạo người dùng quản trị trong User Pool<br>&emsp; + Thiết lập mật khẩu cho người dùng<br>&emsp; + Thêm người dùng vào nhóm SYSTEM_ADMIN<br>&emsp; + Đăng nhập và lấy JWT Token<br>&emsp; + Kiểm tra thông tin nhóm trong Token | 29/06/2026 | 29/06/2026 |  |
| 3 | - Kiểm thử API thông tin người dùng<br>- Tìm hiểu cách API Gateway xác thực JWT Token<br>- **Thực hành:**<br>&emsp; + Gọi endpoint `/me` bằng Bearer Token<br>&emsp; + Kiểm tra userId, email và groups<br>&emsp; + Kiểm thử trường hợp thiếu hoặc sai Token<br>&emsp; + Theo dõi Lambda Logs trên CloudWatch<br>&emsp; + Ghi nhận các mã lỗi cơ bản | 30/06/2026 | 30/06/2026 |  |
| 4 | - Kiểm thử luồng tạo Upload Intent<br>- Kiểm thử upload file bằng Presigned URL<br>- **Thực hành:**<br>&emsp; + Gọi API `/upload-intents`<br>&emsp; + Ghi nhận uploadIntentId và Presigned PUT URL<br>&emsp; + Upload một file PDF mẫu lên QuarantineBucket<br>&emsp; + Kiểm tra file trong Amazon S3<br>&emsp; + Theo dõi trạng thái Upload Intent trong DynamoDB | 01/07/2026 | 01/07/2026 |  |
| 5 | - Kiểm tra kết quả quét và xử lý tài liệu<br>- Kiểm thử các API quản lý tài liệu<br>- **Thực hành:**<br>&emsp; + Theo dõi kết quả GuardDuty Malware Protection<br>&emsp; + Kiểm tra EventBridge và Upload Processor Logs<br>&emsp; + Xác minh file sạch trong DocumentsBucket<br>&emsp; + Kiểm tra trạng thái `READY` trong DynamoDB<br>&emsp; + Gọi API `/documents` và API chi tiết tài liệu<br>&emsp; + Tạo Presigned GET URL và tải file kiểm thử | 02/07/2026 | 02/07/2026 |  |
| 6 | - Khởi chạy React Frontend trên môi trường local<br>- Thực hiện kiểm thử giao diện cơ bản<br>- **Thực hành:**<br>&emsp; + Cài đặt các thư viện bằng npm<br>&emsp; + Cấu hình UserPoolId, UserPoolClientId và ApiUrl<br>&emsp; + Khởi chạy ứng dụng bằng `npm run dev`<br>&emsp; + Kiểm thử chức năng đăng nhập<br>&emsp; + Kiểm thử danh sách, upload và download tài liệu<br>&emsp; + Ghi nhận lỗi giao diện và lỗi kết nối API | 03/07/2026 | 03/07/2026 |  |

### Kết quả đạt được tuần 11:

* Tạo được tài khoản quản trị trong Amazon Cognito.
* Thêm người dùng vào nhóm SYSTEM_ADMIN.
* Đăng nhập và lấy được JWT Token phục vụ kiểm thử API.
* Hiểu cách API Gateway sử dụng Cognito Authorizer để xác thực request.
* Gọi được endpoint `/me` và kiểm tra các thông tin:
  * userId
  * email
  * groups
* Nhận biết được một số lỗi xác thực cơ bản:
  * Thiếu Token
  * Token không hợp lệ
  * Token hết hạn
* Biết cách sử dụng CloudWatch Logs để theo dõi quá trình thực thi Lambda.
* Gọi được API tạo Upload Intent.
* Nhận được uploadIntentId và Presigned PUT URL.
* Upload được file trực tiếp lên QuarantineBucket.
* Theo dõi được trạng thái tài liệu trong Amazon S3 và DynamoDB.
* Hiểu luồng xử lý sau khi GuardDuty hoàn thành quét file.
* Kiểm tra được hoạt động của EventBridge và Upload Processor Function.
* Xác minh được file sạch được chuyển sang DocumentsBucket.
* Kiểm tra được trạng thái `READY` và thông tin phiên bản trong DynamoDB.
* Gọi được API liệt kê và xem chi tiết tài liệu.
* Tạo được Presigned GET URL và tải file từ DocumentsBucket.
* Cấu hình và khởi chạy được React Frontend trên môi trường local.
* Kiểm thử được các chức năng cơ bản:
  * Đăng nhập
  * Xem danh sách tài liệu
  * Upload tài liệu
  * Download tài liệu
* Ghi nhận được các lỗi cơ bản để tiếp tục khắc phục và hoàn thiện hệ thống.