---
title: "Worklog Tuần 6"
date: 25-05-2026
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---


### Mục tiêu tuần 6:

* Tìm hiểu cách điều phối quy trình serverless bằng AWS Step Functions.
* Thực hành AWS Lambda tương tác với Amazon S3 và Amazon DynamoDB.
* Xây dựng API serverless bằng Amazon API Gateway.
* Làm quen với việc triển khai ứng dụng bằng AWS SAM.
* Tìm hiểu cơ chế xác thực người dùng bằng Amazon Cognito.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu AWS Step Functions và State Machine<br>- Tìm hiểu Task State và Choice State<br>- **Thực hành cơ bản:**<br>&emsp; + Chuẩn bị các Lambda Function mẫu<br>&emsp; + Tạo State Machine<br>&emsp; + Cấu hình Task State gọi Lambda<br>&emsp; + Tạo Choice State để rẽ nhánh<br>&emsp; + Kiểm tra Input và Output của workflow<br>&emsp; + Tìm hiểu Retry và Catch | 25/05/2026 | 25/05/2026 | <https://000047.awsstudygroup.com/vi/> |
| 3 | - Tìm hiểu Lambda tương tác với Amazon S3<br>- Tìm hiểu kiến trúc xử lý ảnh theo sự kiện<br>- **Thực hành:**<br>&emsp; + Tạo S3 Bucket lưu ảnh<br>&emsp; + Tạo IAM Role cho Lambda<br>&emsp; + Tạo Lambda Function xử lý ảnh<br>&emsp; + Cấu hình S3 PutObject Trigger<br>&emsp; + Upload ảnh để kích hoạt Lambda<br>&emsp; + Kiểm tra kết quả trong CloudWatch Logs | 26/05/2026 | 26/05/2026 | <https://000078.awsstudygroup.com/vi/> |
| 4 | - Tìm hiểu Lambda tương tác với DynamoDB<br>- Tìm hiểu Amazon API Gateway và CORS<br>- **Thực hành:**<br>&emsp; + Tạo bảng DynamoDB<br>&emsp; + Tạo Lambda ghi và đọc dữ liệu<br>&emsp; + Tạo API Gateway Resource và Method<br>&emsp; + Tích hợp API Gateway với Lambda<br>&emsp; + Kích hoạt CORS<br>&emsp; + Kiểm tra API bằng Postman | 27/05/2026 | 27/05/2026 | <https://000078.awsstudygroup.com/vi/> <br><br> <https://000079.awsstudygroup.com/vi/> |
| 5 | - Tìm hiểu AWS Serverless Application Model<br>- Tìm hiểu cấu trúc SAM Template<br>- **Thực hành:**<br>&emsp; + Cài đặt và cấu hình AWS SAM CLI<br>&emsp; + Khởi tạo SAM Project<br>&emsp; + Khai báo Lambda và DynamoDB trong Template<br>&emsp; + Chạy SAM Build và Validate<br>&emsp; + Triển khai ứng dụng bằng SAM Deploy<br>&emsp; + Kiểm tra các tài nguyên được tạo | 28/05/2026 | 28/05/2026 | <https://000080.awsstudygroup.com/vi/> |
| 6 | - Tìm hiểu xác thực bằng Amazon Cognito<br>- Phân biệt User Pool và Identity Pool<br>- **Thực hành:**<br>&emsp; + Tạo Amazon Cognito User Pool<br>&emsp; + Tạo App Client<br>&emsp; + Tạo người dùng kiểm thử<br>&emsp; + Tích hợp Cognito Authorizer với API Gateway<br>&emsp; + Kiểm tra đăng ký và đăng nhập<br>&emsp; + Gọi API bằng Access Token<br>&emsp; + Dọn dẹp tài nguyên sau thực hành | 29/05/2026 | 29/05/2026 | <https://000081.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 6:

* Hiểu vai trò của AWS Step Functions trong việc điều phối các dịch vụ serverless.
* Tạo được State Machine cơ bản sử dụng:
  * Task State
  * Choice State
  * State Input và Output
* Hiểu vai trò của Retry và Catch trong xử lý lỗi workflow.
* Tạo được Lambda Function kích hoạt khi có file được upload lên Amazon S3.
* Biết cách sử dụng CloudWatch Logs để kiểm tra quá trình thực thi Lambda.
* Tạo được bảng DynamoDB và Lambda Function đọc, ghi dữ liệu.
* Hiểu các thành phần cơ bản của Amazon API Gateway:
  * Resource
  * Method
  * Integration
  * CORS
* Kiểm tra được API serverless bằng Postman.
* Hiểu vai trò của AWS SAM trong việc triển khai hạ tầng serverless dưới dạng mã.
* Biết cách sử dụng các lệnh:
  * `sam build`
  * `sam validate`
  * `sam deploy`
* Tạo được Amazon Cognito User Pool và App Client.
* Hiểu sự khác nhau giữa User Pool và Identity Pool.
* Tích hợp được Cognito Authorizer với API Gateway ở mức cơ bản.
* Kiểm tra được luồng đăng ký, đăng nhập và gọi API bằng token.
