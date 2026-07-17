---
title: "Worklog Tuần 2"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Tìm hiểu cách quản lý tài nguyên, tối ưu chi phí và kiểm soát quyền truy cập trên AWS.
* Nắm được cơ chế mở rộng ứng dụng, cân bằng tải và giám sát hệ thống.
* Làm quen với AWS CLI, Lambda, CloudWatch, Grafana và tự động hóa vận hành.
* Tìm hiểu DNS Hybrid và các phương pháp dịch chuyển máy chủ, cơ sở dữ liệu lên AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu Amazon Lightsail<br>- Tìm hiểu Tag và Resource Groups<br>- **Thực hành:**<br>&emsp; + Triển khai WordPress và Database trên Lightsail<br>&emsp; + Cấu hình Networking<br>&emsp; + Gán Tag và tạo Resource Group | 27/04/2026 | 27/04/2026 | <https://000045.awsstudygroup.com/vi/> <br><br> <https://000027.awsstudygroup.com/vi/> |
| 3 | - Tìm hiểu Amazon EC2 Auto Scaling<br>- Tìm hiểu kiểm soát quyền EC2 bằng Resource Tag<br>- **Thực hành:**<br>&emsp; + Tạo Launch Template và Target Group<br>&emsp; + Tạo Elastic Load Balancer và Auto Scaling Group<br>&emsp; + Kiểm thử các hình thức Scaling<br>&emsp; + Tạo IAM Policy theo điều kiện Tag | 28/04/2026 | 28/04/2026 | <https://000006.awsstudygroup.com/vi/> <br><br> <https://000028.awsstudygroup.com/vi/> |
| 4 | - Tìm hiểu Amazon CloudWatch và Grafana<br>- Tìm hiểu tự động bật/tắt EC2 bằng Lambda<br>- **Thực hành:**<br>&emsp; + Phân tích Metrics và Logs<br>&emsp; + Tạo Alarm và Dashboard<br>&emsp; + Cài đặt Grafana trên EC2<br>&emsp; + Tạo Lambda Start/Stop EC2<br>&emsp; + Gửi thông báo qua Slack | 29/04/2026 | 29/04/2026 | <https://000008.awsstudygroup.com/vi/> <br><br> <https://000029.awsstudygroup.com/vi/> <br><br> <https://000022.awsstudygroup.com/vi/> |
| 5 | - Tìm hiểu DNS Hybrid với Route 53 Resolver<br>- Tìm hiểu sử dụng AWS CLI trên EC2 Windows/Ubuntu<br>- **Thực hành:**<br>&emsp; + Triển khai Microsoft Active Directory<br>&emsp; + Tạo Inbound và Outbound Endpoint<br>&emsp; + Tạo Resolver Rules<br>&emsp; + Cài đặt và sử dụng AWS CLI | 30/04/2026 | 30/04/2026 | <https://000010.awsstudygroup.com/vi/> <br><br> <https://000011.awsstudygroup.com/vi/> |
| 6 | - Tìm hiểu AWS VM Import/Export<br>- **Thực hành:**<br>&emsp; + Chuẩn bị máy ảo từ môi trường On-premise<br>&emsp; + Export máy ảo từ môi trường ảo hóa<br>&emsp; + Tải file máy ảo lên Amazon S3<br>&emsp; + Import máy ảo vào AWS<br>&emsp; + Tạo AMI từ máy ảo đã import<br>&emsp; + Triển khai EC2 Instance từ AMI | 01/05/2026 | 01/05/2026 | <https://000014.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 2:

* Triển khai được WordPress và Database trên Amazon Lightsail.
* Biết cách sử dụng Tag và Resource Groups để phân loại, tìm kiếm và quản lý tài nguyên.
* Hiểu cách Auto Scaling Group kết hợp với Elastic Load Balancer để mở rộng ứng dụng và tăng tính sẵn sàng.
* Biết cách tạo IAM Policy kiểm soát quyền truy cập EC2 dựa trên Resource Tag.
* Sử dụng CloudWatch để theo dõi:
  * Metrics
  * Logs
  * Alarms
  * Dashboards
* Cài đặt Grafana trên EC2 và kết nối dữ liệu giám sát từ AWS.
* Tạo Lambda Function tự động bật/tắt EC2 và gửi thông báo qua Slack.
* Hiểu cách Route 53 Resolver hỗ trợ phân giải DNS giữa môi trường Local và Amazon VPC.
* Cài đặt và sử dụng AWS CLI để kiểm tra, tạo và quản lý tài nguyên AWS.
* Hiểu quy trình đưa máy ảo từ môi trường On-premise lên AWS bằng VM Import/Export.
* Biết cách lưu file máy ảo trên Amazon S3, tạo AMI và triển khai EC2 Instance từ máy ảo đã import.
