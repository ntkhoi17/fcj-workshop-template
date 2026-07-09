---
title: "Bản đề xuất"
date: 2026-07-09
weight: 2
chapter: false
pre: " <b> 2. </b> "
---


### 1. Tóm tắt dự án
Dự án Document Management System (DMS) được xây dựng nhằm tạo ra một hệ thống quản lý tài liệu nội bộ an toàn, dễ mở rộng và tối ưu chi phí trên nền tảng AWS Serverless.
Hệ thống cho phép người dùng đăng nhập, tải lên tài liệu, quản lý phiên bản, chia sẻ tài liệu theo quyền hạn và theo dõi lịch sử thao tác. DMS sử dụng các dịch vụ AWS như Amazon Cognito, API Gateway, Lambda, S3, DynamoDB, EventBridge, GuardDuty, CloudFront, CloudWatch và SNS.

### 2. Tuyên bố vấn đề
Việc lưu trữ và chia sẻ tài liệu nội bộ theo cách truyền thống thường gặp nhiều hạn chế như khó quản lý phiên bản, thiếu phân quyền chi tiết, khó kiểm tra lịch sử thao tác và tiềm ẩn nguy cơ rò rỉ dữ liệu.
Giải pháp đề xuất là xây dựng hệ thống quản lý tài liệu theo kiến trúc 100% Serverless, trong đó file được upload trực tiếp lên Amazon S3 bằng Presigned URL, được kiểm tra malware trước khi lưu chính thức và toàn bộ metadata được quản lý bằng DynamoDB.

### 3. Kiến trúc giải pháp
Hệ thống hoạt động theo luồng chính:
* Người dùng truy cập hệ thống qua **Amazon CloudFront**.
* Frontend được lưu trữ trong **Amazon S3 FrontendBucket**.
* Người dùng đăng nhập bằng **Amazon Cognito** và nhận **JWT token**.
* Frontend gọi API thông qua **Amazon API Gateway**.
* **API Gateway** xác thực **JWT** bằng **Cognito Authorizer**.
* **Core API Lambdas** xử lý các API chính như thông tin người dùng, danh sách tài liệu và chi tiết tài liệu.
* **Intent Lambdas** tạo Presigned URL cho upload/download.
* Người dùng upload file trực tiếp lên **Amazon S3 QuarantineBucket**.
* **Amazon GuardDuty** quét malware cho file upload.
* **Amazon EventBridge** kích hoạt **Upload Processor Function**.
* **Upload Processor** đọc kết quả quét, cập nhật trạng thái vào **DynamoDB** và chuyển file an toàn sang **DocumentsBucket**.
* **CloudWatch** ghi log và kích hoạt cảnh báo qua **SNS** khi có lỗi hoặc bất thường.

### 4. Triển khai kỹ thuật
* **Frontend:** React SPA, phân phối qua Amazon CloudFront.
* **Backend:** AWS Lambda sử dụng Node.js 22 để xử lý nghiệp vụ.
* **API:** Amazon API Gateway tích hợp Cognito Authorizer.
* **Lưu trữ:** Amazon S3 gồm FrontendBucket, QuarantineBucket và DocumentsBucket.
* **Cơ sở dữ liệu:** Amazon DynamoDB lưu metadata, version, sharing và audit log.
* **Bảo mật:** Cognito phân quyền người dùng, S3 Private Bucket, Presigned URL, IAM Least Privilege và GuardDuty Malware Protection.
* **Giám sát:** CloudWatch Logs, X-Ray tracing và SNS Alerts.
* **Triển khai hạ tầng:** AWS CDK theo mô hình Infrastructure as Code.

### 5. Lộ trình triển khai
* **Tuần 9:** Phân tích yêu cầu, thiết kế kiến trúc và chuẩn bị môi trường.
* **Tuần 10:** Triển khai hạ tầng DMS bằng AWS CDK.
* **Tuần 11:** Cấu hình backend, tạo user admin, kiểm thử API và xác minh luồng upload tài liệu.
* **Tuần 12:** Kiểm tra bảo mật, giám sát, dọn dẹp tài nguyên và tổng kết dự án.

### 6. Ước tính ngân sách
Do sử dụng kiến trúc Serverless, hệ thống hoạt động theo mô hình (pay-as-you-go), chỉ phát sinh chi phí theo mức sử dụng thực tế. Trong môi trường thử nghiệm, chi phí thấp nhờ AWS Free Tier.
* **AWS Lambda:** ~0.00 USD (nằm trong mức miễn phí 1 triệu request/tháng).
* **Amazon S3:** ~0.15 USD cho lưu trữ và băng thông ra ngoài.
* **DynamoDB:** ~0.00 USD (mức miễn phí 25GB lưu trữ).
* **API Gateway & Cognito:** Miễn phí với lưu lượng người dùng nội bộ nhỏ.
* **Tổng ngân sách dự kiến:** Dưới 1 USD/tháng cho môi trường thử nghiệm và khoảng dưới 10 USD/tháng cho môi trường thực tế quy mô vừa.

### 7. Đánh giá rủi ro và dự phòng
* **Rủi ro rò rỉ dữ liệu:** Khắc phục bằng S3 Private Bucket, Block Public Access, Presigned URL có thời hạn và phân quyền bằng Cognito.
* **Rủi ro upload file độc hại:** Khắc phục bằng QuarantineBucket và GuardDuty Malware Protection.
* **Rủi ro nghẽn cổ chai khi upload file lớn:** Khắc phục bằng cách upload trực tiếp lên S3 thay vì gửi file qua API Gateway.
* **Rủi ro phát sinh chi phí:** Khắc phục bằng CloudWatch Alarm, SNS cảnh báo và cleanup tài nguyên sau khi hoàn thành.

### 8. Kết quả kỳ vọng
Dự án kỳ vọng hoàn thiện một hệ thống quản lý tài liệu nội bộ an toàn, có phân quyền, có quản lý phiên bản, có audit log và có khả năng kiểm tra file trước khi lưu trữ chính thức.
Thông qua dự án, nhóm có thể vận dụng kiến thức AWS Serverless vào một bài toán thực tế, đồng thời rèn luyện kỹ năng thiết kế, triển khai, kiểm thử, bảo mật và giám sát hệ thống cloud-native.