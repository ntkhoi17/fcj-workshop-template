---
title: "Worklog Tuần 1"
date: 20-04-2026
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---


### Mục tiêu tuần 1:

* Tìm hiểu các kiến thức nền tảng về AWS Cloud, chính sách AWS Free Tier 2025 và các công cụ hỗ trợ quản lý chi phí trong quá trình sử dụng dịch vụ AWS.
* Nắm được cơ chế quản lý định danh, phân quyền truy cập và cấp quyền cho dịch vụ AWS thông qua AWS IAM và IAM Role.
* Làm quen với môi trường phát triển AWS Cloud9 và các dịch vụ hạ tầng cơ bản gồm Amazon VPC, Amazon EC2, Amazon S3 và Amazon RDS.
* Thực hành triển khai các tài nguyên AWS cơ bản nhằm xây dựng nền tảng cho các bài thực hành và dự án ở những tuần tiếp theo.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2   | - Tìm hiểu AWS Free Tier 2025<br>- Tìm hiểu cách Quản lý chi phí với AWS Budget<br>- Tìm hiểu quy trình gửi Yêu cầu Hỗ trợ từ AWS Support | 20/04/2026   | 20/04/2026      | <https://000001.awsstudygroup.com/vi/> <br><br> <https://000007.awsstudygroup.com/vi/> <br><br> <https://000009.awsstudygroup.com/vi/> |
| 3   | - Tìm hiểu Quản trị quyền truy cập với AWS Identity and Access Management (AWS IAM)<br>- Tìm hiểu cách Cấp quyền cho ứng dụng truy cập dịch vụ AWS thông qua IAM Role<br>- **Thực hành:**<br>&emsp; + Tạo IAM User và IAM Group<br>&emsp; + Cấu hình IAM Policy<br>&emsp; + Gán IAM Role cho dịch vụ AWS | 21/04/2026   | 21/04/2026      | <https://000002.awsstudygroup.com/vi/> <br><br> <https://000048.awsstudygroup.com/vi/> |
| 4   | - Tìm hiểu cách sử dụng Cloud IDE trên trình duyệt với AWS Cloud9<br>- Tìm hiểu dịch vụ Hosting Static Website với Amazon S3<br>- **Thực hành:**<br>&emsp; + Khởi tạo môi trường AWS Cloud9<br>&emsp; + Tạo S3 Bucket<br>&emsp; + Upload mã nguồn website<br>&emsp; + Cấu hình Static Website Hosting | 22/04/2026   | 22/04/2026      | <https://000049.awsstudygroup.com/vi/> <br><br> <https://000057.awsstudygroup.com/vi/> |
| 5   | - Tìm hiểu Triển khai hạ tầng mạng với Amazon Virtual Private Cloud (Amazon VPC):<br>&emsp; + CIDR Block<br>&emsp; + Public Subnet và Private Subnet<br>&emsp; + Internet Gateway<br>&emsp; + Route Table<br>- **Thực hành:**<br>&emsp; + Tạo VPC tùy chỉnh<br>&emsp; + Tạo Subnet<br>&emsp; + Cấu hình định tuyến mạng | 23/04/2026   | 23/04/2026      | <https://000003.awsstudygroup.com/vi/> |
| 6   | - Tìm hiểu Amazon Elastic Compute Cloud (Amazon EC2)<br>- Tìm hiểu Amazon Relational Database Service (Amazon RDS)<br>- **Thực hành:**<br>&emsp; + Tạo EC2 Instance<br>&emsp; + Kết nối EC2 thông qua SSH<br>&emsp; + Tạo RDS MySQL Instance<br>&emsp; + Cấu hình Security Group kết nối EC2 và RDS | 24/04/2026   | 24/04/2026      | <https://000004.awsstudygroup.com/vi/> <br><br> <https://000005.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 1:

#### 1. Tìm hiểu AWS Free Tier 2025
* Hiểu các chương trình sử dụng miễn phí của AWS gồm Always Free, 12 Months Free và Trial.
* Nắm được giới hạn sử dụng miễn phí của một số dịch vụ phổ biến trên AWS.
* Biết cách theo dõi mức sử dụng tài nguyên nhằm hạn chế phát sinh chi phí ngoài dự kiến.

#### 2. Tìm hiểu AWS Budget
* Hiểu cơ chế quản lý và theo dõi chi phí trên AWS.
* Tạo Budget để giám sát mức sử dụng tài nguyên.
* Thiết lập Email Notification để nhận cảnh báo khi chi phí đạt ngưỡng cấu hình.

#### 3. Tìm hiểu AWS Support
* Nắm được các hình thức hỗ trợ do AWS cung cấp.
* Hiểu quy trình tạo và quản lý Support Case.
* Phân biệt các loại yêu cầu hỗ trợ như Account and Billing, Technical Support và Service Limit Increase.

#### 4. Tìm hiểu AWS Identity and Access Management (IAM)
* Hiểu vai trò của IAM User, IAM Group và IAM Policy.
* Nắm được nguyên tắc phân quyền tối thiểu (Least Privilege).
* Hiểu cách kiểm soát quyền truy cập đối với tài nguyên AWS.

#### 5. Thực hành quản lý người dùng và phân quyền
* Tạo IAM User.
* Tạo IAM Group.
* Gán Policy cho User và Group.
* Kiểm tra quyền truy cập sau khi cấu hình phân quyền.

#### 6. Tìm hiểu IAM Role
* Phân biệt IAM User và IAM Role.
* Hiểu cơ chế Trust Policy và Permission Policy.
* Tìm hiểu cách cấp quyền cho dịch vụ AWS mà không cần sử dụng Access Key.

#### 7. Thực hành cấp quyền thông qua IAM Role
* Tạo IAM Role.
* Gán Role cho dịch vụ AWS.
* Kiểm tra khả năng truy cập tài nguyên thông qua Role được cấp.

#### 8. Tìm hiểu AWS Cloud9
* Khởi tạo môi trường phát triển trên nền tảng Cloud.
* Sử dụng trình soạn thảo mã nguồn trực tiếp trên trình duyệt.
* Làm quen với Terminal tích hợp và các công cụ hỗ trợ phát triển.

#### 9. Tìm hiểu Amazon S3 và triển khai Static Website
* Hiểu mô hình lưu trữ Object Storage trên Amazon S3.
* Tạo S3 Bucket và quản lý đối tượng lưu trữ.
* Cấu hình Static Website Hosting.
* Triển khai website tĩnh và truy cập thông qua Website Endpoint.

#### 10. Tìm hiểu Amazon VPC
* Hiểu vai trò của VPC trong việc xây dựng hạ tầng mạng trên AWS.
* Nắm được các thành phần CIDR Block, Subnet, Route Table và Internet Gateway.
* Hiểu sự khác biệt giữa Public Subnet và Private Subnet.

#### 11. Thực hành triển khai hạ tầng mạng
* Tạo VPC tùy chỉnh.
* Tạo Public Subnet.
* Cấu hình Route Table và Internet Gateway.
* Kiểm tra khả năng kết nối mạng trong môi trường AWS.

#### 12. Tìm hiểu Amazon EC2
* Hiểu khái niệm máy chủ ảo trên AWS.
* Tìm hiểu Amazon Machine Image (AMI), Instance Type, Key Pair và Security Group.
* Nắm được quy trình khởi tạo và quản lý EC2 Instance.

#### 13. Thực hành triển khai EC2
* Tạo EC2 Instance.
* Cấu hình Security Group.
* Kết nối máy chủ thông qua SSH.
* Kiểm tra trạng thái hoạt động của Instance.

#### 14. Tìm hiểu Amazon Relational Database Service (Amazon RDS)
* Hiểu mô hình cơ sở dữ liệu được quản lý trên AWS.
* Tìm hiểu các thành phần Database Instance, Database Engine và Endpoint.
* Hiểu cơ chế bảo mật và kiểm soát truy cập cơ sở dữ liệu.

#### 15. Thực hành triển khai Amazon RDS
* Tạo RDS MySQL Instance.
* Cấu hình các thông số cơ bản cho cơ sở dữ liệu.
* Thiết lập Security Group cho phép kết nối.
* Kiểm tra kết nối giữa EC2 Instance và RDS Instance.


