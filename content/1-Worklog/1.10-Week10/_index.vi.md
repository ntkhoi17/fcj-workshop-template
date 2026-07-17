---
title: "Worklog Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---


### Mục tiêu tuần 10:

* Làm quen với việc triển khai hạ tầng dự án DMS bằng AWS CDK.
* Triển khai lần lượt các thành phần định danh, lưu trữ, cơ sở dữ liệu, API và xử lý sự kiện.
* Cấu hình bảo mật, giám sát và phân phối giao diện cho hệ thống.
* Kiểm tra kết quả triển khai và các thông số đầu ra của CDK Stack.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Chuẩn bị môi trường triển khai AWS CDK<br>- Tìm hiểu cấu trúc mã nguồn hạ tầng DMS<br>- **Thực hành:**<br>&emsp; + Clone Repository và cài đặt dependencies<br>&emsp; + Tạo file `.env` từ `.env.example`<br>&emsp; + Kiểm tra biến môi trường cảnh báo<br>&emsp; + Build mã nguồn Lambda TypeScript<br>&emsp; + Kiểm tra thư mục đầu ra `dist`<br>&emsp; + Thực hiện CDK Bootstrap | 22/06/2026 | 22/06/2026 |  |
| 3 | - Triển khai lớp Identity, Storage và Database<br>- **Thực hành:**<br>&emsp; + Tạo Amazon Cognito User Pool và App Client<br>&emsp; + Tạo các nhóm người dùng của hệ thống<br>&emsp; + Tạo FrontendBucket, QuarantineBucket và DocumentsBucket<br>&emsp; + Bật Block Public Access và cấu hình CORS cần thiết<br>&emsp; + Tạo bảng Amazon DynamoDB<br>&emsp; + Cấu hình TTL, PITR và các chỉ mục cần thiết | 23/06/2026 | 23/06/2026 |  |
| 4 | - Triển khai lớp Compute và API<br>- **Thực hành:**<br>&emsp; + Kiểm tra mã nguồn các Lambda Function chính<br>&emsp; + Triển khai Lambda xử lý người dùng và tài liệu<br>&emsp; + Triển khai Lambda tạo Upload/Download Intent<br>&emsp; + Triển khai Upload Processor Function<br>&emsp; + Tạo Amazon API Gateway<br>&emsp; + Tích hợp Cognito Authorizer với các API Route | 24/06/2026 | 24/06/2026 |  |
| 5 | - Triển khai lớp Security, Event và Monitoring<br>- **Thực hành:**<br>&emsp; + Cấu hình GuardDuty Malware Protection cho QuarantineBucket<br>&emsp; + Tạo EventBridge Rule nhận kết quả quét file<br>&emsp; + Kết nối EventBridge với Upload Processor Function<br>&emsp; + Tạo CloudFront Distribution cho FrontendBucket<br>&emsp; + Cấu hình Origin Access Control<br>&emsp; + Tạo CloudWatch Log Groups và SNS Topic cảnh báo | 25/06/2026 | 25/06/2026 |  |
| 6 | - Triển khai và kiểm tra toàn bộ hạ tầng DMS<br>- **Thực hành:**<br>&emsp; + Chạy lệnh `cdk synth` để kiểm tra Template<br>&emsp; + Xem thay đổi bằng `cdk diff`<br>&emsp; + Triển khai CDK Stack lên môi trường `dev`<br>&emsp; + Theo dõi trạng thái CloudFormation Stack<br>&emsp; + Ghi nhận UserPoolId, UserPoolClientId, ApiUrl và CloudFrontUrl<br>&emsp; + Kiểm tra các tài nguyên trên AWS Console<br>&emsp; + Ghi nhận và xử lý các lỗi triển khai cơ bản | 26/06/2026 | 26/06/2026 |  |

### Kết quả đạt được tuần 10:

* Chuẩn bị được môi trường triển khai dự án bằng AWS CDK.
* Hiểu vai trò của các lệnh:
  * `cdk bootstrap`
  * `cdk synth`
  * `cdk diff`
  * `cdk deploy`
* Build được mã nguồn Lambda và kiểm tra thư mục đầu ra trước khi triển khai.
* Triển khai được Amazon Cognito User Pool, App Client và các nhóm người dùng:
  * EMPLOYEE
  * DEPARTMENT_ADMIN
  * SYSTEM_ADMIN
* Tạo được ba S3 Bucket phục vụ:
  * Lưu giao diện Frontend.
  * Cách ly file mới upload.
  * Lưu tài liệu đã được kiểm tra an toàn.
* Cấu hình Block Public Access và CORS phù hợp cho các Bucket.
* Tạo được bảng DynamoDB sử dụng mô hình Single-table Design.
* Cấu hình được TTL, Point-in-Time Recovery và các chỉ mục phục vụ truy vấn.
* Triển khai được các Lambda Function chính của hệ thống DMS.
* Tạo được API Gateway và tích hợp Cognito Authorizer.
* Hiểu luồng tạo Presigned URL cho thao tác upload và download tài liệu.
* Cấu hình được GuardDuty Malware Protection cho QuarantineBucket.
* Tạo được EventBridge Rule để chuyển kết quả quét đến Upload Processor Function.
* Hiểu cách Upload Processor cập nhật trạng thái:
  * `READY`
  * `REJECTED`
  * `FAILED`
* Tạo được CloudFront Distribution kết nối với FrontendBucket thông qua Origin Access Control.
* Cấu hình được CloudWatch Logs và SNS Topic phục vụ giám sát, cảnh báo.
* Triển khai được CloudFormation Stack cho môi trường phát triển.
* Ghi nhận được các CDK Outputs quan trọng để cấu hình Backend và Frontend.
* Kiểm tra được trạng thái của các tài nguyên sau khi triển khai trên AWS Console.