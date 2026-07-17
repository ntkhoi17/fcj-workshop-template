---
title: "Worklog Tuần 4"
date: 11-05-2026
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---



### Mục tiêu tuần 4:

* Tìm hiểu cách kết nối hai VPC bằng VPC Peering.
* Làm quen với Docker và quy trình đóng gói ứng dụng bằng Container.
* Thực hành lưu trữ Docker Image trên Amazon ECR.
* Tìm hiểu các thành phần cơ bản của Amazon ECS.
* Tìm hiểu các phương án tối ưu chi phí dài hạn cho EC2 và RDS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu VPC Peering<br>- Tìm hiểu Network ACL và Cross-Peer DNS<br>- **Thực hành:**<br>&emsp; + Chuẩn bị hai VPC và EC2 Instance<br>&emsp; + Tạo kết nối VPC Peering<br>&emsp; + Cập nhật Route Table<br>&emsp; + Kiểm tra kết nối giữa hai VPC<br>&emsp; + Kích hoạt Cross-Peer DNS | 11/05/2026 | 11/05/2026 | <https://000019.awsstudygroup.com/vi/> |
| 3 | - Tìm hiểu Docker và Docker Image<br>- Tìm hiểu Docker Container và Docker Compose<br>- **Thực hành:**<br>&emsp; + Cài đặt các công cụ cần thiết<br>&emsp; + Chạy ứng dụng ở môi trường Local<br>&emsp; + Tạo Docker Image<br>&emsp; + Khởi chạy Docker Container<br>&emsp; + Kiểm tra ứng dụng bằng Docker Compose | 12/05/2026 | 12/05/2026 | <https://000015.awsstudygroup.com/vi/> |
| 4 | - Tìm hiểu Amazon Elastic Container Registry<br>- Tìm hiểu cách triển khai Docker trên EC2<br>- **Thực hành:**<br>&emsp; + Tạo Amazon ECR Repository<br>&emsp; + Cấu hình IAM Role cho EC2<br>&emsp; + Tạo EC2 Instance<br>&emsp; + Push Docker Image lên Amazon ECR<br>&emsp; + Pull Image và chạy Container trên EC2 | 13/05/2026 | 13/05/2026 | <https://000015.awsstudygroup.com/vi/> |
| 5 | - Tìm hiểu tổng quan về Amazon ECS<br>- Tìm hiểu ECS Cluster, Task Definition và ECS Service<br>- **Thực hành cơ bản:**<br>&emsp; + Tạo ECS Cluster<br>&emsp; + Tạo Task Definition đơn giản<br>&emsp; + Tạo ECS Service<br>&emsp; + Triển khai Container từ Amazon ECR<br>&emsp; + Kiểm tra trạng thái ECS Task<br>&emsp; + Dọn dẹp tài nguyên sau thực hành | 14/05/2026 | 14/05/2026 | <https://000016.awsstudygroup.com/vi/> |
| 6 | - Tìm hiểu Savings Plans<br>- Tìm hiểu Reserved Instance và Reserved DB Instance<br>- So sánh các mô hình cam kết sử dụng<br>- **Thực hành:**<br>&emsp; + Xem Savings Plans Recommendation<br>&emsp; + Phân tích thời hạn cam kết và phương thức thanh toán<br>&emsp; + So sánh Savings Plans với Reserved Instance<br>&emsp; + Tổng hợp và ôn tập nội dung tuần 4 | 15/05/2026 | 15/05/2026 | <https://000042.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 4:

* Hiểu cách VPC Peering kết nối tài nguyên giữa hai VPC bằng địa chỉ mạng riêng.
* Biết cách cập nhật Route Table và kiểm tra kết nối giữa hai VPC.
* Phân biệt được Security Group và Network ACL.
* Hiểu các khái niệm cơ bản của Docker:
  * Docker Image
  * Docker Container
  * Dockerfile
  * Docker Compose
* Đóng gói và chạy được ứng dụng bằng Docker ở môi trường Local.
* Biết cách tạo Repository và lưu Docker Image trên Amazon ECR.
* Triển khai được Docker Container cơ bản trên Amazon EC2.
* Hiểu các thành phần chính của Amazon ECS:
  * ECS Cluster
  * Task Definition
  * ECS Task
  * ECS Service
* Thực hành triển khai Container cơ bản trên Amazon ECS.
* Hiểu sự khác nhau giữa Savings Plans, Reserved Instance và Reserved DB Instance.
* Biết cách xem Savings Plans Recommendation để tham khảo phương án tối ưu chi phí.
