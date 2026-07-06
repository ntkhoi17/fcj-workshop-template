---
title: "Worklog Tuần 8"
date: 08-06-2026
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---


### Mục tiêu tuần 8:

* Tìm hiểu kiến trúc hướng sự kiện trên AWS thông qua Amazon SNS và Amazon SQS, bao gồm mô hình Pub/Sub, Message Filtering và Advanced Message Filtering.
* Thực hành các mô hình chia sẻ dữ liệu và xây dựng hệ thống sẵn sàng cao bằng Amazon EBS Multi-Attach, NVMe Reservation, MySQL HA Cluster và Windows Failover Cluster.
* Làm quen với việc giám sát hạ tầng mạng bằng VPC Flow Logs và phân tích lưu lượng mạng thông qua Amazon CloudWatch Logs.
* Tìm hiểu cách ủy quyền truy cập Billing Console và quản trị chi phí, sử dụng tài nguyên bằng IAM Policy theo Region, EC2 Family, Instance Size và EBS Volume Type.
* Nắm được cách quản lý thông tin xác thực an toàn bằng AWS Secrets Manager khi tích hợp với Amazon RDS và AWS Fargate.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2   | - Tìm hiểu Xây dựng kiến trúc Event-driven với Amazon SNS và Amazon SQS<br>- Tìm hiểu Giám sát hạ tầng mạng với VPC Flow Logs<br>- **Thực hành:**<br>&emsp; + Chuẩn bị hạ tầng cho kiến trúc Event-driven và cài đặt Event Generator<br>&emsp; + Tạo SQS Queue OrdersQueue và đăng ký vào SNS Topic Orders<br>&emsp; + Tạo SQS Queue Orders-EU và cấu hình Subscription Filter Policy (location = eu-west)<br>&emsp; + Tạo SQS Queue Orders-RL và cấu hình Advanced Filter Policy theo số lượng đơn hàng<br>&emsp; + Khởi tạo môi trường mạng, tạo và kích hoạt VPC Flow Logs đẩy về CloudWatch Logs | 08/06/2026   | 08/06/2026      | <https://000077.awsstudygroup.com/vi/> <br><br> <https://000074.awsstudygroup.com/vi/> |
| 3   | - Tìm hiểu Chia sẻ dữ liệu lưu trữ với Amazon EBS Multi-Attach và NVMe Reservation<br>- **Thực hành:**<br>&emsp; + Tạo Prod VPC, Test VPC và khởi chạy các EC2 Instance tương ứng<br>&emsp; + Tạo EBS Volume (io2) hỗ trợ Multi-Attach và gắn vào nhiều máy chủ đồng thời<br>&emsp; + Cài đặt PostgreSQL, tạo dữ liệu mẫu, thực hiện backup/restore database<br>&emsp; + Cấu hình NVMe Reservation kiểm soát truy cập trên hai môi trường Prod/Test<br>&emsp; + Kiểm tra các báo cáo Reservation Register và Reservation Report | 09/06/2026   | 09/06/2026      | <https://100000.awsstudygroup.com/vi/> |
| 4   | - Tìm hiểu Tính sẵn sàng cao cho cơ sở dữ liệu với EBS Multi-Attach và AWS Systems Manager<br>- **Thực hành:**<br>&emsp; + Thiết lập dải mạng VPC riêng cho cụm MySQL HA Cluster và phân quyền IAM cho SSM<br>&emsp; + Khởi chạy các EC2 Instances, tạo EBS dùng chung và cấu hình Logical Volume Management (LVM)<br>&emsp; + Cài đặt MySQL và cấu hình định tuyến qua Internal Network Load Balancer (NLB)<br>&emsp; + Deploy WordPress kết nối MySQL qua NLB; tạo Systems Manager Runbook & Response Plan<br>&emsp; + Cấu hình CloudWatch Alarm và thực hiện kiểm thử kịch bản Fail-over tự động | 10/06/2026   | 10/06/2026      | <https://100001.awsstudygroup.com/vi/> |
| 5   | - Tìm hiểu Cụm chịu lỗi Windows Server trên AWS<br>- **Thực hành:**<br>&emsp; + Xây dựng hạ tầng mạng VPC/Subnet và khởi tạo dịch vụ AWS Managed Microsoft Active Directory<br>&emsp; + Khởi chạy cụm Windows EC2 Instances và liên kết (Join) các node vào Domain hệ thống<br>&emsp; + Tạo EBS Volume hỗ trợ Multi-Attach để làm phân vùng lưu trữ chia sẻ chung<br>&emsp; + Cài đặt Windows Feature Failover Clustering, khởi chạy Cluster Validation Wizard<br>&emsp; + Tạo Windows Failover Cluster hoàn chỉnh, phân tầng cấu hình Network và Storage | 11/06/2026   | 11/06/2026      | <https://100002.awsstudygroup.com/vi/> |
| 6   | - Tìm hiểu Ủy quyền truy cập Console thanh toán<br>- Tìm hiểu Quản lý chi phí và sử dụng tài nguyên bằng IAM<br>- Tìm hiểu Quản lý thông tin xác thực với AWS Secrets Manager<br>- **Thực hành:**<br>&emsp; + Tạo IAM User Group, kích hoạt và gán Policy kiểm soát phân quyền xem Billing Console<br>&emsp; + Viết Custom IAM Policy giới hạn nghiêm ngặt theo Region, EC2 Family, Instance Size và EBS Type<br>&emsp; + Khởi tạo môi trường Secrets Manager đồng bộ hóa với hệ thống VPC, EC2, RDS và ECS Fargate<br>&emsp; + Lưu trữ RDS credentials bảo mật, cấu hình xoay vòng mật khẩu tự động (Secret Rotation) | 12/06/2026   | 12/06/2026      | <https://000075.awsstudygroup.com/vi/> <br><br> <https://000064.awsstudygroup.com/vi/> <br><br> <https://000096.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 8:

#### 1. Kiến trúc hướng sự kiện Event-driven (Amazon SNS & Amazon SQS)
* Hiểu sâu kiến trúc bóc tách liên kết (Decoupled Architecture) hướng sự kiện, tối ưu hóa khả năng mở rộng độc lập giữa bên phát sinh thông điệp (Publisher) và bên tiêu thụ dữ liệu (Consumer).
* **Lọc tin nhắn nâng cao (Message Filtering):** Làm chủ cơ chế điều hướng thông minh của Amazon SNS thông qua Subscription Filter Policy (lọc theo thuộc tính chuỗi như `location = eu-west`) và Advanced Filter Policy (lọc theo điều kiện toán học số học như `quantity >= 100`), giúp cắt giảm toàn bộ logic sàng lọc dữ liệu dư thừa tại tầng ứng dụng nhận tin.

#### 2. Giám sát hạ tầng mạng toàn diện với VPC Flow Logs
* Nắm chắc phương pháp thu thập và kiểm toán toàn bộ luồng lưu lượng mã IP (Inbound/Outbound traffic) đi qua các Elastic Network Interface (ENI) trong phân vùng mạng VPC.
* **Thực hành quản trị an ninh mạng:** Kích hoạt thành công VPC Flow Logs đẩy luồng dữ liệu tập trung về Amazon CloudWatch Logs, bóc tách chính xác trạng thái ACCEPT/REJECT của các gói tin để phát hiện các lỗ hổng hoặc quy tắc Security Group/Network ACL đang cấu hình sai lệch.

#### 3. Chia sẻ lưu trữ High-Availability với Amazon EBS Multi-Attach & NVMe Reservation
* Thấu hiểu năng lực đặc biệt của dòng ổ đĩa cao cấp Amazon EBS io2 cho phép liên kết đồng thời vào nhiều máy chủ ảo EC2 trong cùng một phân vùng Availability Zone (AZ).
* **Kiểm soát tính toàn vẹn dữ liệu:** Vận hành thành công cơ chế NVMe Reservation (`Reservation Register` và `Reservation Report`) để điều phối, phân định quyền ghi/đọc ổ đĩa dùng chung giữa hai môi trường Production và Test chạy cơ sở dữ liệu PostgreSQL, ngăn chặn triệt để hiện tượng xung đột dữ liệu (Data Corruption).

#### 4. Xây dựng cụm MySQL HA Cluster tích hợp AWS Systems Manager
* Triển khai hoàn chỉnh kiến trúc cơ sở dữ liệu MySQL Cluster có tính sẵn sàng cao (High Availability) trên nền tảng ổ đĩa chia sẻ EBS Multi-Attach kết hợp giải pháp quản lý phân vùng LVM (Logical Volume Management).
* **Tự động hóa khắc phục sự cố (Auto Fail-over):** Cấu hình cổng Internal Network Load Balancer (NLB) làm đại diện kết nối cho ứng dụng WordPress, xây dựng kịch bản xử lý tự động Systems Manager Runbook kết hợp Incident Manager Response Plan và CloudWatch Alarm, giúp hệ thống tự động phát hiện máy chủ chính gặp sự cố và lập tức chuyển giao vai trò sang máy chủ dự phòng mượt mà (Zero-downtime).

#### 5. Triển khai hạ tầng doanh nghiệp Windows Failover Cluster
* Làm chủ quy trình xây dựng hệ thống chịu lỗi Windows Server phân tán quy mô lớn trực tiếp trên môi trường điện toán đám mây AWS.
* **Đồng bộ hóa hạ tầng Microsoft:** Khởi tạo thành công trục quản lý định danh tập trung AWS Managed Microsoft Active Directory, cấu hình kết nối mạng cho các Windows EC2 cụm node, vượt qua các bài kiểm tra nghiêm ngặt của Cluster Validation Wizard để thiết lập thành công cụm Windows Failover Cluster dùng chung phân vùng lưu trữ EBS Multi-Attach io2.

#### 6. Hoạch định quản trị chi phí doanh nghiệp (Cost Governance) thông qua IAM Policies
* Nắm vững bộ best practices kiểm soát tài chính và phân bổ tài nguyên an toàn cho doanh nghiệp đa phòng ban.
* **Kiểm soát đặc quyền tài nguyên:** Thực hiện ủy quyền an toàn quyền truy cập Billing Console từ tài khoản Root sang cho IAM User Group; thiết kế hệ thống Custom IAM Policy nâng cao nhằm khóa chặn và giới hạn quyền hạn khởi tạo hạ tầng của nhân sự dựa theo các điều kiện ràng buộc khắt khe bao gồm: Chỉ định dải Region được phép, loại trừ nhóm chip máy chủ (EC2 Family), kích thước cấu hình (Instance Size) và phân loại ổ đĩa cứng (EBS Volume Type) nhằm tối ưu hóa chi tiêu ngân sách.

#### 7. Quản lý thông tin mật cao cấp bằng AWS Secrets Manager
* Triệt tiêu hoàn toàn rủi ro rò rỉ mã nguồn do thói quen hard-code thông tin bảo mật (username/password) trực tiếp vào mã nguồn phần mềm.
* **Thực hành bảo mật thông tin nhạy cảm:** Cấu hình Secrets Manager lưu trữ mã hóa dữ liệu credentials của Amazon RDS, thiết lập tính năng tự động xoay vòng mật khẩu định kỳ an toàn (Secret Rotation) thông qua AWS Lambda Handler, tích hợp kết nối bảo mật cho tầng container phi máy chủ AWS Fargate lấy thông tin xác thực động (Dynamic Credentials) trực tiếp từ API Secrets Manager qua mạng nội bộ VPC Endpoint.
