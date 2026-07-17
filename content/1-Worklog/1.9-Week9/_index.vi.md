---
title: "Worklog Tuần 9"
date: 15-06-2026
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---


### Mục tiêu tuần 9:

* Tìm hiểu tổng quan dự án Document Management System trên AWS Serverless.
* Phân tích kiến trúc, chức năng và các luồng xử lý chính của hệ thống.
* Tìm hiểu cơ chế xác thực, upload tài liệu, quét malware và lưu trữ dữ liệu.
* Chuẩn bị môi trường phát triển và cấu trúc mã nguồn cho dự án.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu tổng quan dự án Document Management System<br>- Phân tích bài toán quản lý tài liệu nội bộ<br>- **Thực hành:**<br>&emsp; + Xác định mục tiêu của hệ thống<br>&emsp; + Xác định các nhóm người dùng<br>&emsp; + Liệt kê các chức năng chính<br>&emsp; + Xác định phạm vi triển khai dự án | 15/06/2026 | 15/06/2026 |  |
| 3 | - Tìm hiểu kiến trúc tổng thể của hệ thống DMS<br>- Tìm hiểu vai trò của các dịch vụ AWS<br>- **Thực hành:**<br>&emsp; + Phân tích luồng đăng nhập bằng Amazon Cognito<br>&emsp; + Phân tích luồng gọi API qua API Gateway<br>&emsp; + Xác định vai trò của Lambda, S3 và DynamoDB<br>&emsp; + Vẽ sơ đồ kiến trúc tổng thể của hệ thống | 16/06/2026 | 16/06/2026 |  |
| 4 | - Tìm hiểu luồng upload tài liệu bằng Presigned URL<br>- Tìm hiểu quy trình kiểm dịch file<br>- **Thực hành:**<br>&emsp; + Phân tích luồng tạo Presigned PUT URL<br>&emsp; + Phân tích quá trình upload vào QuarantineBucket<br>&emsp; + Tìm hiểu GuardDuty Malware Protection<br>&emsp; + Phân tích EventBridge kích hoạt Upload Processor<br>&emsp; + Phân tích quá trình chuyển file sạch sang DocumentsBucket | 17/06/2026 | 17/06/2026 |  |
| 5 | - Tìm hiểu mô hình phân quyền và thiết kế dữ liệu<br>- Tìm hiểu các quyết định bảo mật của hệ thống<br>- **Thực hành:**<br>&emsp; + Xác định các nhóm EMPLOYEE, DEPARTMENT_ADMIN và SYSTEM_ADMIN<br>&emsp; + Phân tích DynamoDB Single-table Design<br>&emsp; + Xác định các entity chính của hệ thống<br>&emsp; + Phân tích audit log dạng append-only<br>&emsp; + Xác định quyền IAM tối thiểu cho từng Lambda | 18/06/2026 | 18/06/2026 |  |
| 6 | - Chuẩn bị môi trường phát triển dự án<br>- Tìm hiểu cấu trúc Repository<br>- **Thực hành:**<br>&emsp; + Kiểm tra AWS CLI và AWS Profile<br>&emsp; + Kiểm tra Node.js, npm, Git và AWS CDK CLI<br>&emsp; + Tìm hiểu lệnh CDK Bootstrap<br>&emsp; + Tạo cấu trúc thư mục dự án<br>&emsp; + Chuẩn bị biến môi trường cảnh báo<br>&emsp; + Kiểm tra môi trường trước khi triển khai | 19/06/2026 | 19/06/2026 |  |

### Kết quả đạt được tuần 9:

* Hiểu mục tiêu của hệ thống DMS là quản lý tài liệu nội bộ trên nền tảng AWS Serverless.
* Xác định được các chức năng chính:
  * Upload và download tài liệu.
  * Quản lý phiên bản.
  * Chia sẻ và thu hồi quyền truy cập.
  * Ghi nhận audit log.
  * Theo dõi trạng thái tài liệu.
* Hiểu vai trò của các dịch vụ chính:
  * Amazon Cognito
  * Amazon API Gateway
  * AWS Lambda
  * Amazon S3
  * Amazon DynamoDB
  * Amazon EventBridge
  * Amazon GuardDuty
  * Amazon CloudFront
  * Amazon CloudWatch
  * Amazon SNS
* Phân tích được luồng đăng nhập và gọi API bằng JWT Token.
* Hiểu lý do sử dụng Presigned URL để upload và download file.
* Phân tích được quy trình:
  * Upload file vào QuarantineBucket.
  * Quét malware bằng GuardDuty.
  * Nhận sự kiện qua EventBridge.
  * Xử lý kết quả bằng Upload Processor.
  * Chuyển file an toàn sang DocumentsBucket.
* Hiểu mô hình DynamoDB Single-table Design và vai trò của Global Secondary Index.
* Xác định được các entity chính:
  * Document
  * Version
  * Share
  * AuditLog
  * UploadIntent
  * UserProfile
* Hiểu mô hình phân quyền theo các nhóm người dùng trong Amazon Cognito.
* Nắm được nguyên tắc Least Privilege khi cấp quyền cho Lambda Function.
* Hoàn thành sơ đồ kiến trúc tổng thể của hệ thống DMS.
* Chuẩn bị được AWS CLI, Node.js, npm, Git và AWS CDK CLI.
* Hiểu cấu trúc các thư mục `aws/functions`, `aws/infrastructure`, `frontend`, `contracts` và `docs`.
* Hoàn thành bước chuẩn bị trước khi bắt đầu triển khai hạ tầng dự án.