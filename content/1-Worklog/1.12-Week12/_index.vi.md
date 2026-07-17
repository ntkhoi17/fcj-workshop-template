---
title: "Worklog Tuần 12"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---


### Mục tiêu tuần 12:

* Rà soát các cấu hình bảo mật chính của hệ thống DMS.
* Kiểm tra cơ chế phân quyền, bảo vệ file và xử lý kết quả quét malware.
* Theo dõi log, chỉ số và cảnh báo của hệ thống.
* Dọn dẹp tài nguyên AWS sau khi hoàn thành kiểm thử.
* Tổng kết dự án và kiểm tra chi phí phát sinh trên tài khoản AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Rà soát IAM Least Privilege<br>- Kiểm tra bảo mật các S3 Bucket<br>- **Thực hành:**<br>&emsp; + Kiểm tra IAM Role của các Lambda Function chính<br>&emsp; + Rà soát quyền truy cập DynamoDB và Amazon S3<br>&emsp; + Kiểm tra Block Public Access trên các Bucket<br>&emsp; + Kiểm tra thời hạn Presigned PUT/GET URL<br>&emsp; + Ghi nhận các quyền cần điều chỉnh | 06/07/2026 | 06/07/2026 |  |
| 3 | - Kiểm tra GuardDuty Malware Protection<br>- Kiểm tra phân quyền người dùng bằng Amazon Cognito<br>- **Thực hành:**<br>&emsp; + Kiểm tra trạng thái Malware Protection Plan<br>&emsp; + Xem kết quả quét và tag trên S3 Object<br>&emsp; + Kiểm tra hoạt động của Upload Processor Function<br>&emsp; + Xác minh file sạch được chuyển sang DocumentsBucket<br>&emsp; + Kiểm thử quyền cơ bản của các nhóm người dùng | 07/07/2026 | 07/07/2026 |  |
| 4 | - Kiểm tra CloudWatch Logs và hệ thống cảnh báo<br>- Làm quen với CloudWatch Logs Insights và AWS X-Ray<br>- **Thực hành:**<br>&emsp; + Xem log của các Lambda Function<br>&emsp; + Lọc một số bản ghi bằng CloudWatch Logs Insights<br>&emsp; + Kiểm tra audit log trong DynamoDB<br>&emsp; + Xem Trace và Service Map cơ bản trên AWS X-Ray<br>&emsp; + Kiểm tra trạng thái đăng ký SNS Email | 08/07/2026 | 08/07/2026 |  |
| 5 | - Dọn dẹp hạ tầng dự án DMS<br>- **Thực hành:**<br>&emsp; + Kiểm tra dữ liệu cần sao lưu trước khi xóa<br>&emsp; + Làm trống các S3 Bucket nếu cần thiết<br>&emsp; + Chạy lệnh `npx cdk destroy -c environment=dev`<br>&emsp; + Theo dõi quá trình xóa CloudFormation Stack<br>&emsp; + Kiểm tra các tài nguyên còn sót trên AWS Console<br>&emsp; + Xóa thủ công tài nguyên chưa được CDK loại bỏ | 09/07/2026 | 09/07/2026 |  |
| 6 | - Tổng kết dự án và kiểm tra chi phí<br>- **Thực hành:**<br>&emsp; + Kiểm tra AWS Billing và Cost Explorer<br>&emsp; + Xem chi phí theo từng dịch vụ đã sử dụng<br>&emsp; + Kiểm tra lại tài nguyên còn hoạt động<br>&emsp; + Tổng hợp kiến trúc và chức năng của hệ thống<br>&emsp; + Ghi nhận khó khăn và bài học kinh nghiệm<br>&emsp; + Hoàn thiện tài liệu báo cáo thực tập | 10/07/2026 | 10/07/2026 |  |

### Kết quả đạt được tuần 12:

* Hiểu vai trò của nguyên tắc Least Privilege trong việc giới hạn quyền cho Lambda Function.
* Rà soát được quyền truy cập cơ bản của các Lambda:
  * Đọc và ghi dữ liệu trong DynamoDB.
  * Upload file vào QuarantineBucket.
  * Đọc file từ DocumentsBucket.
  * Quản lý người dùng trong Amazon Cognito.
* Kiểm tra được Block Public Access trên các S3 Bucket.
* Hiểu sự khác nhau giữa:
  * Presigned PUT URL dùng để upload file.
  * Presigned GET URL dùng để download file.
* Kiểm tra được trạng thái GuardDuty Malware Protection cho QuarantineBucket.
* Theo dõi được tag kết quả quét trên S3 Object.
* Xác minh được Upload Processor chỉ chuyển file an toàn sang DocumentsBucket.
* Kiểm tra được quyền cơ bản của các nhóm:
  * EMPLOYEE
  * DEPARTMENT_ADMIN
  * SYSTEM_ADMIN
* Biết cách xem Lambda Logs trong Amazon CloudWatch.
* Thực hiện được truy vấn log cơ bản bằng CloudWatch Logs Insights.
* Kiểm tra được các audit log phát sinh khi người dùng thao tác với tài liệu.
* Làm quen với Service Map và Trace của AWS X-Ray.
* Kiểm tra được trạng thái đăng ký nhận cảnh báo qua Amazon SNS.
* Thực hiện được quá trình dọn dẹp CloudFormation Stack bằng AWS CDK.
* Biết cách xử lý một số tài nguyên không được xóa tự động:
  * S3 Bucket còn dữ liệu.
  * Log Group được giữ lại.
  * Tài nguyên có Removal Policy.
  * CloudFront Distribution đang trong quá trình vô hiệu hóa.
* Kiểm tra lại các dịch vụ trên AWS Console sau khi chạy CDK Destroy.
* Sử dụng AWS Billing và Cost Explorer để xem chi phí theo từng dịch vụ.
* Tổng hợp được kiến trúc, chức năng và các lớp bảo mật của hệ thống DMS.
* Hoàn thiện phần tổng kết, bài học kinh nghiệm và tài liệu báo cáo thực tập.