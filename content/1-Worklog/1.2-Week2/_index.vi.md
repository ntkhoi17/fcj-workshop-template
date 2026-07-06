---
title: "Worklog Tuần 2"
date: 27-04-2026
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---


### Mục tiêu tuần 2:

* Tìm hiểu các giải pháp tối ưu chi phí, quản lý tài nguyên và kiểm soát quyền truy cập trên AWS thông qua Amazon Lightsail, Tag, Resource Groups và IAM Policy theo Resource Tag.
* Nắm được cách tự động mở rộng quy mô ứng dụng, cân bằng tải và giám sát hệ thống bằng Amazon EC2 Auto Scaling, Elastic Load Balancer, Amazon CloudWatch và Grafana.
* Làm quen với các công cụ vận hành và tự động hóa trên AWS như AWS CLI, AWS Lambda, CloudWatch Dashboard và tích hợp thông báo qua Slack.
* Tìm hiểu các mô hình kết nối DNS hybrid, dịch chuyển máy chủ ảo và dịch chuyển cơ sở dữ liệu bằng Route 53 Resolver, VM Import/Export, AWS DMS và AWS Schema Conversion Tool.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2   | - Tìm hiểu Tối ưu chi phí tính toán với Amazon Lightsail<br>- Tìm hiểu cách Quản lý tài nguyên theo nhóm bằng Tag và Resource Groups<br>- **Thực hành:**<br>&emsp; + Triển khai Lightsail Database<br>&emsp; + Triển khai WordPress Instance trên Lightsail<br>&emsp; + Cấu hình Networking cho Lightsail Instance<br>&emsp; + Gán Tag cho tài nguyên AWS<br>&emsp; + Lọc tài nguyên theo Tag<br>&emsp; + Tạo Resource Group để quản lý tài nguyên theo nhóm | 27/04/2026   | 27/04/2026      | <https://000045.awsstudygroup.com/vi/> <br><br> <https://000027.awsstudygroup.com/vi/> |
| 3   | - Tìm hiểu Tự động mở rộng quy mô ứng dụng với Amazon EC2 Auto Scaling<br>- Tìm hiểu Quản lý truy cập dịch vụ EC2 bằng Tag thông qua IAM<br>- **Thực hành:**<br>&emsp; + Chuẩn bị hạ tầng mạng cho ứng dụng<br>&emsp; + Tạo Launch Template<br>&emsp; + Tạo Target Group và Elastic Load Balancer<br>&emsp; + Tạo Auto Scaling Group<br>&emsp; + Kiểm thử Manual Scaling, Scheduled Scaling và Dynamic Scaling<br>&emsp; + Tạo IAM Policy kiểm soát quyền EC2 dựa trên Resource Tag<br>&emsp; + Kiểm tra chính sách truy cập EC2 theo điều kiện Tag | 28/04/2026   | 28/04/2026      | <https://000006.awsstudygroup.com/vi/> <br><br> <https://000028.awsstudygroup.com/vi/> |
| 4   | - Tìm hiểu Tạo bảng theo dõi hệ thống với Amazon CloudWatch<br>- Tìm hiểu Tạo bảng theo dõi hệ thống với Amazon CloudWatch và Grafana<br>- Tìm hiểu Bật tắt máy chủ tự động và nhắn tin qua Slack với AWS Lambda<br>- **Thực hành:**<br>&emsp; + Xem và phân tích CloudWatch Metrics<br>&emsp; + Tìm kiếm và phân tích CloudWatch Logs<br>&emsp; + Tạo CloudWatch Alarm<br>&emsp; + Tạo CloudWatch Dashboard<br>&emsp; + Cài đặt Grafana trên EC2 Instance<br>&emsp; + Kết nối Grafana để theo dõi tài nguyên AWS<br>&emsp; + Tạo Lambda Function tự động Start/Stop EC2 Instance<br>&emsp; + Cấu hình Incoming Webhook Slack để nhận thông báo | 29/04/2026   | 29/04/2026      | <https://000008.awsstudygroup.com/vi/> <br><br> <https://000029.awsstudygroup.com/vi/> <br><br> <https://000022.awsstudygroup.com/vi/> |
| 5   | - Tìm hiểu Thiết lập hệ thống DNS Hybrid tích hợp giữa môi trường Local và Amazon VPC với Amazon Route 53 Resolver<br>- Tìm hiểu Sử dụng AWS CLI trên Amazon EC2 Windows/Ubuntu<br>- **Thực hành:**<br>&emsp; + Tạo Key Pair<br>&emsp; + Khởi tạo CloudFormation Template<br>&emsp; + Cấu hình Security Group<br>&emsp; + Kết nối đến Remote Desktop Gateway<br>&emsp; + Triển khai Microsoft Active Directory<br>&emsp; + Tạo Route 53 Outbound Endpoint<br>&emsp; + Tạo Route 53 Resolver Rules<br>&emsp; + Tạo Route 53 Inbound Endpoint<br>&emsp; + Cài đặt và cấu hình AWS CLI<br>&emsp; + Kiểm tra tài nguyên AWS thông qua CLI | 30/04/2026   | 30/04/2026      | <https://000010.awsstudygroup.com/vi/> <br><br> <https://000011.awsstudygroup.com/vi/> |
| 6   | - Tìm hiểu Dịch chuyển máy chủ ảo với AWS VM Import/Export<br>- Tìm hiểu Dịch chuyển cơ sở dữ liệu với AWS Database Migration Service và AWS Schema Conversion Tool<br>- **Thực hành:**<br>&emsp; + Chuẩn bị máy ảo từ môi trường On-premise<br>&emsp; + Export máy ảo từ môi trường ảo hóa<br>&emsp; + Tải máy ảo lên Amazon S3<br>&emsp; + Import máy ảo vào AWS<br>&emsp; + Triển khai EC2 Instance từ AMI đã import<br>&emsp; + Cài đặt AWS Schema Conversion Tool<br>&emsp; + Kết nối đến cơ sở dữ liệu nguồn<br>&emsp; + Chuyển đổi lược đồ cơ sở dữ liệu<br>&emsp; + Tạo DMS Replication Instance<br>&emsp; + Tạo Source Endpoint và Target Endpoint<br>&emsp; + Tạo DMS Migration Task và kiểm tra dữ liệu sau khi di chuyển | 01/05/2026   | 01/05/2026      | <https://000014.awsstudygroup.com/vi/> <br><br> <https://000043.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 2:

#### 1. Tìm hiểu Amazon Lightsail
* Hiểu được Amazon Lightsail là dịch vụ hỗ trợ triển khai nhanh các ứng dụng phổ biến với mô hình cấu hình đơn giản.
* Nắm được cách triển khai các ứng dụng mã nguồn mở trên Lightsail như WordPress, PrestaShop và Akaunting.
* Hiểu cách Lightsail hỗ trợ triển khai ứng dụng, cơ sở dữ liệu, networking, snapshot và cảnh báo trong cùng một môi trường quản lý.
* Biết cách sử dụng Lightsail để tối ưu chi phí cho các hệ thống nhỏ hoặc các ứng dụng cần triển khai nhanh.
* **Thực hành triển khai tài nguyên trên Amazon Lightsail:**
  * Tạo Lightsail Database.
  * Tạo WordPress Instance.
  * Cấu hình Ubuntu cho Instance.
  * Cấu hình Networking cho ứng dụng.
  * Cấu hình WordPress trên Lightsail.
  * Tìm hiểu cách tạo Snapshot để sao lưu tài nguyên.
  * Tìm hiểu cách chuyển sang Instance lớn hơn khi ứng dụng cần mở rộng.

#### 2. Tìm hiểu Tag và Resource Groups
* Hiểu Tag là nhãn metadata được gán cho tài nguyên AWS.
* Nắm được cấu trúc Tag gồm Key và Value.
* Hiểu cách phân loại tài nguyên theo mục đích sử dụng, môi trường, chủ sở hữu hoặc nhóm triển khai.
* Hiểu vai trò của AWS Resource Groups trong việc gom nhóm và quản lý nhiều tài nguyên cùng lúc.
* **Thực hành quản lý tài nguyên bằng Tag:**
  * Tạo EC2 Instance có gắn Tag.
  * Thêm và xóa Tag trên tài nguyên.
  * Lọc tài nguyên theo Tag trên AWS Console.
  * Sử dụng AWS CLI để thao tác với Tag.
  * Tạo Resource Group dựa trên Tag để quản lý tài nguyên theo nhóm.

#### 3. Tìm hiểu Amazon EC2 Auto Scaling
* Hiểu vai trò của Auto Scaling Group trong việc tự động tăng hoặc giảm số lượng EC2 Instance theo nhu cầu truy cập.
* Nắm được lợi ích của Auto Scaling Group trong việc tăng tính sẵn sàng, tối ưu chi phí và giảm thao tác quản trị thủ công.
* Hiểu cách Auto Scaling Group kết hợp với Elastic Load Balancer để phân phối yêu cầu đến nhiều Instance.
* Tìm hiểu các hình thức mở rộng như Manual Scaling, Scheduled Scaling, Dynamic Scaling và Predictive Scaling.
* **Thực hành triển khai ứng dụng với Auto Scaling Group:**
  * Chuẩn bị hạ tầng mạng cho ứng dụng.
  * Khởi tạo EC2 Instance và Database Instance với Amazon RDS.
  * Cài đặt dữ liệu cho Database.
  * Triển khai máy chủ web.
  * Tạo Launch Template.
  * Tạo Target Group.
  * Tạo Elastic Load Balancer.
  * Tạo Auto Scaling Group.
  * Kiểm thử khả năng phân phối tải và mở rộng tài nguyên.

#### 4. Tìm hiểu quản lý truy cập EC2 bằng Resource Tag thông qua IAM
* Hiểu cách dùng Resource Tag để kiểm soát quyền truy cập vào EC2.
* Nắm được cách áp dụng nguyên tắc đặc quyền tối thiểu trong IAM Policy.
* Tìm hiểu cách tạo IAM Policy có điều kiện dựa trên Tag.
* Hiểu cách IAM Role được sử dụng để cấp quyền có kiểm soát cho nhóm người dùng nhất định.
* **Thực hành kiểm soát quyền EC2 bằng IAM và Tag:**
  * Tạo IAM User phục vụ kiểm thử.
  * Tạo IAM Policy có điều kiện.
  * Tạo IAM Role.
  * Thực hiện chuyển Role để kiểm tra quyền.
  * Kiểm tra quyền truy cập EC2 ở các Region khác nhau.
  * Kiểm tra việc tạo EC2 Instance khi có và không có Tag thỏa điều kiện.
  * Kiểm tra việc chỉnh sửa Resource Tag trên EC2 Instance.

#### 5. Tìm hiểu Amazon CloudWatch
* Hiểu CloudWatch là dịch vụ giám sát và quản lý dữ liệu vận hành cho tài nguyên AWS, ứng dụng hybrid và ứng dụng on-premises.
* Nắm được vai trò của Metrics, Logs, Alarms và Dashboards trong quá trình theo dõi hệ thống.
* Hiểu cách CloudWatch hỗ trợ phân tích hiệu năng, tự động hóa phản hồi sự cố và giảm thời gian xử lý lỗi.
* Tìm hiểu khả năng lưu trữ dữ liệu Metrics, phân tích Logs và tạo cảnh báo theo ngưỡng tùy chỉnh.
* **Thực hành giám sát hệ thống với CloudWatch:**
  * Xem các Metrics của tài nguyên AWS.
  * Thực hiện tìm kiếm Metrics.
  * Thực hiện phép toán trên Metrics.
  * Tạo Dynamic Labels.
  * Làm việc với CloudWatch Logs.
  * Sử dụng CloudWatch Logs Insights.
  * Tạo Metric Filter.
  * Tạo CloudWatch Alarm.
  * Tạo CloudWatch Dashboard để trực quan hóa trạng thái hệ thống.

#### 6. Tìm hiểu Grafana trên AWS
* Hiểu Grafana là công cụ mã nguồn mở dùng để trực quan hóa dữ liệu giám sát.
* Nắm được cách Grafana hỗ trợ tạo biểu đồ, truy vấn dữ liệu, cảnh báo và theo dõi chỉ số hệ thống.
* Hiểu cách Grafana có thể kết hợp với dữ liệu giám sát từ AWS để xây dựng dashboard trực quan.
* Biết vai trò của Grafana trong việc theo dõi hoạt động ứng dụng và hạ tầng.
* **Thực hành triển khai Grafana:**
  * Tạo VPC and Subnet phục vụ môi trường thực hành.
  * Tạo Security Group.
  * Tạo EC2 Instance.
  * Tạo IAM User.
  * Tạo IAM Role.
  * Gán IAM Role cho EC2 Instance.
  * Cài đặt Grafana trên Linux EC2 Instance.
  * Theo dõi tài nguyên AWS thông qua Grafana Dashboard.

#### 7. Tìm hiểu tối ưu chi phí EC2 với AWS Lambda
* Hiểu cách sử dụng Lambda Function để tự động bật và tắt EC2 Instance.
* Nắm được trường hợp áp dụng cho các máy chủ chỉ cần hoạt động trong một số khung giờ nhất định.
* Hiểu cách kết hợp Tag, IAM Role, Lambda và Slack để tự động hóa vận hành.
* Biết cách giảm chi phí bằng cách tắt máy chủ khi không cần sử dụng.
* **Thực hành tự động bật tắt EC2 và gửi thông báo Slack:**
  * Tạo VPC.
  * Tạo Security Group.
  * Tạo EC2 Instance.
  * Cấu hình Incoming Webhook Slack.
  * Tạo Tag cho Instance.
  * Tạo Role cho Lambda.
  * Tạo Lambda Function dừng EC2 Instance.
  * Tạo Lambda Function khởi động EC2 Instance.
  * Kiểm tra kết quả và thông báo gửi về Slack.

#### 8. Tìm hiểu Route 53 Resolver và mô hình Hybrid DNS
* Hiểu nhu cầu tích hợp DNS giữa môi trường On-premise và Amazon VPC.
* Nắm được vai trò của Amazon Route 53 trong việc phân giải tên miền trên AWS.
* Hiểu các thành phần của Route 53 Resolver gồm Outbound Endpoint, Inbound Endpoint và Resolver Rules.
* Biết cách Route 53 Resolver hỗ trợ chuyển tiếp truy vấn DNS giữa hệ thống Local và AWS.
* **Thực hành thiết lập Hybrid DNS:**
  * Tạo Key Pair.
  * Khởi tạo CloudFormation Template.
  * Cấu hình Security Group.
  * Kết nối đến RDGW.
  * Triển khai Microsoft Active Directory.
  * Tạo Route 53 Outbound Endpoint.
  * Tạo Route 53 Resolver Rules.
  * Tạo Route 53 Inbound Endpoint.
  * Kiểm thử khả năng phân giải DNS giữa môi trường Local và Amazon VPC.

#### 9. Tìm hiểu AWS CLI
* Hiểu AWS Command Line Interface là công cụ dòng lệnh cho phép tương tác với các dịch vụ AWS.
* Nắm được cách AWS CLI hỗ trợ thao tác tương tự AWS Management Console thông qua command-line shell.
* Biết các môi trường có thể sử dụng AWS CLI như Linux Shell, Windows Command Prompt, PowerShell và kết nối từ xa vào EC2.
* Hiểu cách dùng AWS CLI để kiểm tra và quản lý tài nguyên AWS.
* **Thực hành sử dụng AWS CLI:**
  * Cài đặt AWS CLI.
  * Kiểm tra tài nguyên thông qua CLI.
  * Thao tác với Amazon S3 bằng CLI.
  * Thao tác với Amazon SNS bằng CLI.
  * Thao tác với IAM bằng CLI.
  * Thao tác với VPC và Internet Gateway bằng CLI.
  * Tạo EC2 Instance sử dụng AWS CLI.
  * Tìm hiểu các lỗi thường gặp và cách khắc phục khi sử dụng CLI.

#### 10. Tìm hiểu AWS VM Import/Export
* Hiểu VM Import/Export là dịch vụ hỗ trợ import máy ảo từ môi trường ảo hóa vào Amazon EC2 và export máy ảo từ AWS ra môi trường bên ngoài.
* Nắm được các tình huống sử dụng như dịch chuyển ứng dụng từ On-premise lên AWS, sao lưu máy ảo và tạo kho lưu trữ phục hồi sau sự cố.
* Hiểu vai trò của Amazon S3 trong quá trình lưu trữ file máy ảo khi import hoặc export.
* Biết cách triển khai EC2 Instance từ AMI được tạo sau quá trình import.
* **Thực hành dịch chuyển máy chủ ảo:**
  * Chuẩn bị máy ảo từ môi trường ảo hóa.
  * Export máy ảo từ môi trường On-premise.
  * Tải máy ảo lên Amazon S3.
  * Import máy ảo vào AWS.
  * Tạo AMI từ máy ảo đã import.
  * Triển khai EC2 Instance từ AMI.
  * Tìm hiểu quy trình export EC2 Instance hoặc AMI ra môi trường bên ngoài.

#### 11. Tìm hiểu AWS Database Migration Service và Schema Conversion Tool
* Hiểu quá trình chuyển đổi lược đồ cơ sở dữ liệu khi dịch chuyển giữa các hệ quản trị cơ sở dữ liệu khác nhau.
* Nắm được vai trò của AWS Schema Conversion Tool trong việc phân tích và chuyển đổi schema, view, stored procedure và function.
* Hiểu vai trò của AWS DMS trong việc di chuyển dữ liệu từ cơ sở dữ liệu nguồn sang cơ sở dữ liệu đích.
* Biết các loại nguồn và đích dữ liệu có thể sử dụng trong DMS như Oracle, SQL Server, Amazon RDS, Aurora, Amazon S3 và các hệ thống dữ liệu khác.
* **Thực hành dịch chuyển cơ sở dữ liệu:**
  * Đăng nhập vào AWS và chuẩn bị môi trường.
  * Tạo Key Pair.
  * Kết nối EC2 Instance và cài đặt AWS Schema Conversion Tool.
  * Kết nối đến cơ sở dữ liệu nguồn.
  * Cấu hình cơ sở dữ liệu nguồn.
  * Tạo dự án trong Schema Conversion Tool.
  * Chuyển đổi lược đồ cơ sở dữ liệu.
  * Cấu hình cơ sở dữ liệu đích.
  * Tạo DMS Replication Instance.
  * Tạo Source Endpoint và Target Endpoint.
  * Tạo DMS Migration Task.
  * Kiểm tra nội dung dữ liệu ở cơ sở dữ liệu đích.
  * Theo dõi quá trình migration bằng CloudWatch Metrics, Task Logs và Table Statistics.