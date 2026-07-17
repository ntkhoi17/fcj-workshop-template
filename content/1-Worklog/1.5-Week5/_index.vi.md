---
title: "Worklog Tuần 5"
date: 18-05-2026
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---


### Mục tiêu tuần 5:

* Tìm hiểu cách theo dõi và phân tích chi phí sử dụng trên AWS.
* Nắm được phương pháp lựa chọn kích thước EC2 phù hợp với nhu cầu sử dụng.
* Tìm hiểu kiến trúc Monolith và quy trình triển khai ứng dụng lên AWS Elastic Beanstalk.
* Làm quen với tư duy tách một chức năng từ Monolith thành Serverless Microservice.
* Thực hành AWS Lambda kết hợp với Amazon S3 theo mô hình hướng sự kiện.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu AWS Cost Explorer<br>- Tìm hiểu chi phí theo dịch vụ và tài khoản<br>- Tìm hiểu Savings Plans và Reserved Instance<br>- **Thực hành:**<br>&emsp; + Xem chi phí và mức sử dụng theo dịch vụ<br>&emsp; + Lọc dữ liệu chi phí theo khoảng thời gian<br>&emsp; + Tạo báo cáo chi phí EC2 tùy chỉnh<br>&emsp; + Xem tổng quan chi phí truyền dữ liệu | 18/05/2026 | 18/05/2026 | <https://000034.awsstudygroup.com/vi/> |
| 3 | - Tìm hiểu EC2 Right-Sizing<br>- Tìm hiểu AWS Compute Optimizer<br>- **Thực hành:**<br>&emsp; + Tạo IAM Role cho CloudWatch Agent<br>&emsp; + Gán IAM Role cho EC2 Instance<br>&emsp; + Cài đặt CloudWatch Agent<br>&emsp; + Theo dõi chỉ số CPU và bộ nhớ<br>&emsp; + Xem đề xuất tối ưu kích thước EC2 | 19/05/2026 | 19/05/2026 | <https://000032.awsstudygroup.com/vi/> |
| 4 | - Tìm hiểu kiến trúc ứng dụng Monolith TravelBuddy<br>- Chuẩn bị môi trường thực hành<br>- **Thực hành:**<br>&emsp; + Tạo Key Pair<br>&emsp; + Tạo CloudFormation Stack<br>&emsp; + Kết nối Windows EC2 Instance<br>&emsp; + Cài đặt cơ sở dữ liệu<br>&emsp; + Tải mã nguồn TravelBuddy<br>&emsp; + Kiểm tra ứng dụng bằng Eclipse IDE | 20/05/2026 | 20/05/2026 | <https://000050.awsstudygroup.com/vi/> |
| 5 | - Tìm hiểu AWS Elastic Beanstalk<br>- Tìm hiểu quy trình triển khai ứng dụng Monolith<br>- **Thực hành:**<br>&emsp; + Tạo Elastic Beanstalk Environment<br>&emsp; + Triển khai ứng dụng TravelBuddy<br>&emsp; + Kiểm tra trạng thái môi trường<br>&emsp; + Truy cập ứng dụng sau triển khai<br>&emsp; + Cập nhật một thay đổi nhỏ<br>&emsp; + Kiểm tra API của ứng dụng | 21/05/2026 | 21/05/2026 | <https://000050.awsstudygroup.com/vi/> |
| 6 | - Tìm hiểu Serverless Microservice<br>- Tìm hiểu Lambda kết hợp với S3 Event<br>- **Thực hành cơ bản:**<br>&emsp; + Tạo S3 Bucket<br>&emsp; + Tạo AWS Lambda Function<br>&emsp; + Cấu hình S3 PutObject Trigger<br>&emsp; + Upload file để kích hoạt Lambda<br>&emsp; + Kiểm tra kết quả trong CloudWatch Logs<br>&emsp; + Tìm hiểu logic xử lý file hình ảnh<br>&emsp; + Dọn dẹp tài nguyên sau thực hành | 22/05/2026 | 22/05/2026 | <https://000052.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 5:

* Biết cách sử dụng AWS Cost Explorer để theo dõi chi phí và mức sử dụng.
* Xem được chi phí theo:
  * Dịch vụ AWS
  * Khoảng thời gian
  * Tài khoản
  * Loại tài nguyên
* Hiểu ý nghĩa của Savings Plans và Reserved Instance trong tối ưu chi phí.
* Hiểu khái niệm Right-Sizing đối với Amazon EC2.
* Biết cách sử dụng CloudWatch Agent để thu thập thêm chỉ số hệ thống.
* Làm quen với đề xuất tối ưu tài nguyên từ AWS Compute Optimizer.
* Hiểu đặc điểm và hạn chế cơ bản của kiến trúc Monolith.
* Chuẩn bị được môi trường TravelBuddy bằng CloudFormation.
* Triển khai được ứng dụng Monolith cơ bản lên AWS Elastic Beanstalk.
* Biết cách kiểm tra trạng thái và cập nhật ứng dụng trên Elastic Beanstalk.
* Hiểu tư duy tách một chức năng từ Monolith thành Microservice.
* Tạo được Lambda Function được kích hoạt bởi sự kiện upload file lên Amazon S3.
* Biết cách kiểm tra quá trình thực thi Lambda thông qua CloudWatch Logs.