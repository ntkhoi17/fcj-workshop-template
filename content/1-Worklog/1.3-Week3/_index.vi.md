---
title: "Worklog Tuần 3"
date: 04-05-2026
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---


### Mục tiêu tuần 3:

* Tìm hiểu cách quản lý và vận hành máy chủ bằng AWS Systems Manager.
* Thực hành kết nối EC2 an toàn thông qua Session Manager.
* Làm quen với Infrastructure as Code bằng AWS CloudFormation.
* Tìm hiểu các cơ chế giới hạn quyền nâng cao trong AWS IAM.
* Làm quen với AWS Security Hub và AWS Backup.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Tìm hiểu AWS Systems Manager<br>- Tìm hiểu Patch Manager và Run Command<br>- **Thực hành:**<br>&emsp; + Tạo Windows EC2 Instance<br>&emsp; + Tạo và gán IAM Role cho EC2<br>&emsp; + Kiểm tra Managed Node<br>&emsp; + Quét bản vá bằng Patch Manager<br>&emsp; + Chạy lệnh từ xa bằng Run Command | 04/05/2026 | 04/05/2026 | <https://000031.awsstudygroup.com/vi/> |
| 3 | - Tìm hiểu AWS Systems Manager Session Manager<br>- **Thực hành:**<br>&emsp; + Tạo Public Subnet và Private Subnet<br>&emsp; + Tạo Public EC2 và Private EC2<br>&emsp; + Tạo IAM Role cho Session Manager<br>&emsp; + Tạo VPC Endpoint cần thiết<br>&emsp; + Kết nối đến EC2 trong Private Subnet<br>&emsp; + Cấu hình lưu Session Log vào Amazon S3 | 05/05/2026 | 05/05/2026 | <https://000058.awsstudygroup.com/vi/> |
| 4 | - Tìm hiểu Infrastructure as Code với AWS CloudFormation<br>- **Thực hành:**<br>&emsp; + Tạo IAM Role cho CloudFormation<br>&emsp; + Viết CloudFormation Template cơ bản<br>&emsp; + Kiểm tra cú pháp Template<br>&emsp; + Tạo và cập nhật CloudFormation Stack<br>&emsp; + Kiểm tra tài nguyên được triển khai | 06/05/2026 | 06/05/2026 | <https://000037.awsstudygroup.com/vi/> |
| 5 | - Tìm hiểu IAM Permission Boundary<br>- Tìm hiểu IAM Role và Condition<br>- **Thực hành:**<br>&emsp; + Tạo Policy giới hạn quyền tối đa<br>&emsp; + Áp dụng Permission Boundary cho IAM User<br>&emsp; + Kiểm tra quyền tại Region được phép<br>&emsp; + Tạo IAM Role và thực hiện Switch Role<br>&emsp; + Giới hạn Assume Role theo địa chỉ IP hoặc thời gian | 07/05/2026 | 07/05/2026 | <https://000030.awsstudygroup.com/vi/> <br><br> <https://000044.awsstudygroup.com/vi/> |
| 6 | - Tìm hiểu tổng quan về AWS Security Hub<br>- Tìm hiểu AWS Backup<br>- **Thực hành:**<br>&emsp; + Kích hoạt AWS Security Hub<br>&emsp; + Xem Security Score và các phát hiện bảo mật<br>&emsp; + Tạo Backup Vault và Backup Plan<br>&emsp; + Gán tài nguyên vào Backup Plan<br>&emsp; + Cấu hình thông báo bằng Amazon SNS<br>&emsp; + Theo dõi trạng thái Backup Job | 08/05/2026 | 08/05/2026 | <https://000018.awsstudygroup.com/vi/> <br><br> <https://000013.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 3:

* Hiểu vai trò của AWS Systems Manager trong việc quản lý tập trung các máy chủ.
* Biết cách sử dụng Patch Manager để kiểm tra bản vá và Run Command để chạy lệnh từ xa.
* Kết nối được đến EC2 trong Public Subnet và Private Subnet bằng Session Manager.
* Hiểu vai trò của IAM Role và VPC Endpoint khi quản lý Private EC2.
* Biết cách lưu Session Log vào Amazon S3 để theo dõi hoạt động kết nối.
* Hiểu các thành phần cơ bản của AWS CloudFormation:
  * Template
  * Stack
  * Resource
  * Parameter
* Viết và triển khai được CloudFormation Template cơ bản.
* Hiểu cách Permission Boundary giới hạn quyền tối đa của IAM User.
* Biết cách tạo IAM Role và giới hạn Assume Role bằng Condition.
* Làm quen với Security Score và các phát hiện bảo mật trong AWS Security Hub.
* Tạo được Backup Vault, Backup Plan và theo dõi trạng thái sao lưu.
* Biết cách sử dụng Amazon SNS để nhận thông báo về hoạt động backup.