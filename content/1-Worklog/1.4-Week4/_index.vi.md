---
title: "Worklog Tuần 4"
date: 11-05-2026
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---



### Mục tiêu tuần 4:

* Tìm hiểu các mô hình kết nối mạng nâng cao trên AWS thông qua VPC Peering và AWS Transit Gateway.
* Thực hành triển khai ứng dụng container bằng Docker, Amazon ECR, Amazon ECS, Application Load Balancer và ECS Service.
* Nắm được quy trình triển khai ứng dụng tự động với CI/CD Pipeline thông qua GitLab, GitHub Actions, AWS CodeBuild, AWS CodeDeploy và AWS CodePipeline.
* Làm quen với các dịch vụ lưu trữ và phân tích dữ liệu trên AWS như File Storage Gateway, Amazon FSx for Windows File Server và Data Lake.
* Tìm hiểu các phương pháp tối ưu chi phí dài hạn cho EC2 và RDS thông qua Savings Plans, Reserved Instance và Reserved DB Instance.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2   | - Tìm hiểu Liên kết các Virtual Private Cloud với VPC Peering<br>- Tìm hiểu Quản lý tập trung các kết nối với AWS Transit Gateway<br>- **Thực hành:**<br>&emsp; + Khởi tạo CloudFormation Template<br>&emsp; + Tạo Security Group<br>&emsp; + Tạo EC2 Instance trong các VPC<br>&emsp; + Cập nhật Network ACL<br>&emsp; + Tạo kết nối VPC Peering giữa hai VPC<br>&emsp; + Cập nhật Route Table cho kết nối Peering<br>&emsp; + Kích hoạt Cross-Peer DNS<br>&emsp; + Tạo Key Pair phục vụ lab Transit Gateway<br>&emsp; + Tạo Transit Gateway<br>&emsp; + Tạo Transit Gateway Attachments<br>&emsp; + Tạo Transit Gateway Route Tables<br>&emsp; + Thêm Transit Gateway Routes vào VPC Route Tables | 11/05/2026   | 11/05/2026      | <https://000019.awsstudygroup.com/vi/> <br><br> <https://000020.awsstudygroup.com/vi/> |
| 3   | - Tìm hiểu Triển khai ứng dụng với Docker<br>- Tìm hiểu Triển khai ứng dụng lên Amazon Elastic Container Service (Amazon ECS)<br>- **Thực hành:**<br>&emsp; + Cài đặt Dependencies để chạy ứng dụng ở môi trường Local<br>&emsp; + Triển khai và kiểm tra ứng dụng ở máy cục bộ<br>&emsp; + Cấu hình VPC và Security Group<br>&emsp; + Tạo IAM Role để truy cập Amazon ECR<br>&emsp; + Đăng nhập Docker Hub<br>&emsp; + Tạo DB Subnet Group và khởi chạy RDS Instance<br>&emsp; + Cấu hình EC2 Instance và cài đặt thư viện cần thiết<br>&emsp; + Triển khai ứng dụng bằng Docker Image<br>&emsp; + Triển khai ứng dụng bằng Docker Compose<br>&emsp; + Push Docker Image lên Amazon ECR hoặc Docker Hub<br>&emsp; + Cấu hình hạ tầng ECS<br>&emsp; + Tạo ECS Cluster<br>&emsp; + Tạo ECS Task Definition cho Backend và Frontend<br>&emsp; + Cấu hình Application Load Balancer<br>&emsp; + Tạo ECS Service và kiểm tra kết quả triển khai | 12/05/2026   | 12/05/2026      | <https://000015.awsstudygroup.com/vi/> <br><br> <https://000016.awsstudygroup.com/vi/> |
| 4   | - Tìm hiểu Triển khai ứng dụng với AWS CodePipeline<br>- Tìm hiểu Tự động hóa Triển khai Ứng dụng AWS CodePipeline<br>- **Thực hành:**<br>&emsp; + Fork và chỉnh sửa Repository<br>&emsp; + Cài đặt và đăng ký GitLab Runner<br>&emsp; + Cấu hình quyền và IAM Role<br>&emsp; + Thêm biến môi trường và chạy Pipeline<br>&emsp; + Triển khai CI/CD với GitHub Actions<br>&emsp; + Tạo Access Key và Secret Key phục vụ pipeline<br>&emsp; + Thiết lập GitHub cho CodeBuild<br>&emsp; + Tạo CodeBuild Frontend và CodeBuild Backend<br>&emsp; + Tạo tag và kiểm tra kết quả build<br>&emsp; + Theo dõi ứng dụng bằng Container Insights trên CloudWatch<br>&emsp; + Định tuyến logs với FireLens và Amazon S3<br>&emsp; + Chuẩn bị hạ tầng triển khai ứng dụng lên EC2<br>&emsp; + Tạo S3 Bucket lưu artifact<br>&emsp; + Tạo Git Credential và Git Connection<br>&emsp; + Tạo Service Role và Instance Profile<br>&emsp; + Cài đặt CodeDeploy Agent<br>&emsp; + Tạo CodeCommit Repository<br>&emsp; + Tạo CodeBuild Project<br>&emsp; + Tạo CodeDeploy Application<br>&emsp; + Tạo CodePipeline hoàn chỉnh và kiểm tra quá trình triển khai | 13/05/2026   | 13/05/2026      | <https://000017.awsstudygroup.com/vi/> <br><br> <https://000023.awsstudygroup.com/vi/> |
| 5   | - Tìm hiểu Lưu trữ dữ liệu không giới hạn trên AWS với File Storage Gateway<br>- Tìm hiểu Triển khai Kho lưu trữ chung cho Windows sử dụng Amazon FSx<br>- **Thực hành:**<br>&emsp; + Tạo S3 Bucket phục vụ File Storage Gateway<br>&emsp; + Tạo EC2 Instance cho Storage Gateway<br>&emsp; + Tạo Storage Gateway<br>&emsp; + Tạo File Shares<br>&emsp; + Kết nối File Shares từ máy On-premise<br>&emsp; + Tạo môi trường thực hành FSx<br>&emsp; + Tạo SSD Multi-AZ File System<br>&emsp; + Tạo HDD Multi-AZ File System<br>&emsp; + Ánh xạ File Share mặc định<br>&emsp; + Tạo File mới trên File Share<br>&emsp; + Kiểm tra hiệu năng lưu trữ<br>&emsp; + Giám sát hiệu năng FSx<br>&emsp; + Kích hoạt chống dữ liệu trùng lặp<br>&emsp; + Kích hoạt Shadow Copies<br>&emsp; + Quản lý Session người dùng và tệp đang mở<br>&emsp; + Kích hoạt hạn ngạch bộ nhớ người dùng<br>&emsp; + Kích hoạt chia sẻ truy cập liên tục<br>&emsp; + Mở rộng thông lượng và dung lượng lưu trữ | 14/05/2026   | 14/05/2026      | <https://000024.awsstudygroup.com/vi/> <br><br> <https://000025.awsstudygroup.com/vi/> |
| 6   | - Tìm hiểu Xây dựng Data Lake trên AWS<br>- Tìm hiểu Tối ưu chi phí với Savings Plans, Reserved Instance và Reserved DB Instance<br>- **Thực hành:**<br>&emsp; + Tạo IAM Role cho Data Lake<br>&emsp; + Tạo Policy phục vụ thu thập và xử lý dữ liệu<br>&emsp; + Tạo S3 Bucket lưu trữ dữ liệu<br>&emsp; + Tạo Delivery Stream để thu thập dữ liệu<br>&emsp; + Tạo dữ liệu mẫu<br>&emsp; + Tạo Glue Crawler<br>&emsp; + Kiểm tra Data Catalog<br>&emsp; + Chuyển đổi dữ liệu<br>&emsp; + Phân tích dữ liệu bằng Amazon Athena<br>&emsp; + Trực quan hóa dữ liệu bằng Amazon QuickSight<br>&emsp; + Tìm hiểu các loại Savings Plans<br>&emsp; + Xem Savings Plans Recommendation<br>&emsp; + Tìm hiểu quy trình mua Savings Plans<br>&emsp; + Tìm hiểu Reserved Instance và Reserved DB Instance cho Amazon RDS | 15/05/2026   | 15/05/2026      | <https://000035.awsstudygroup.com/vi/> <br><br> <https://000042.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 4:

#### 1. Tìm hiểu VPC Peering
* Hiểu VPC Peering là kết nối mạng độc lập giữa hai VPC cho phép định tuyến traffic an toàn bằng địa chỉ private IPv4 hoặc IPv6 mà không cần qua Internet công cộng.
* Nắm được cách cấu hình bảng định tuyến (Route Table) để liên thông tài nguyên giữa dải mạng VPC mặc định và VPC tùy chỉnh.
* **Thực hành cấu hình định tuyến nâng cao:** Triển khai hạ tầng qua CloudFormation, cập nhật Network ACL (Stateless Firewall cấp subnet) phân biệt với Security Group (Stateful Firewall cấp tài nguyên), và kích hoạt thành công Cross-Peer DNS để đồng bộ phân giải tên miền private giữa 2 đầu VPC.

#### 2. Tìm hiểu AWS Transit Gateway
* Hiểu vai trò của Transit Gateway đóng vai trò như một Cloud Router trung tâm (Hub-and-Spoke) giúp quản lý tập trung và đơn giản hóa kiến trúc kết nối khi số lượng VPC và mạng On-premises tăng quy mô lớn.
* **Thực hành xây dựng kiến trúc mạng tập trung:** Khởi tạo Transit Gateway, thiết lập các kết nối thành phần Transit Gateway Attachments tương ứng với từng VPC, cấu hình Transit Gateway Route Tables độc lập và ánh xạ Route phù hợp giúp tối ưu hóa luồng đi dữ liệu.

#### 3. Tìm hiểu triển khai ứng dụng với Docker
* Hiểu phương pháp đóng gói ứng dụng hoàn chỉnh kèm các gói thư viện phụ thuộc (dependencies) vào Docker Image để vận hành nhất quán trên mọi môi trường.
* **Thực hành đóng gói và chạy Docker:** Triển khai kiểm thử source code chạy cục bộ (local), viết file cấu hình để khởi chạy cụm dịch vụ frontend/backend đồng thời qua Docker Compose, cấu hình cơ sở dữ liệu RDS MySQL độc lập và tiến hành push (đẩy) production image an toàn lên kho lưu trữ Amazon ECR.

#### 4. Tìm hiểu Amazon Elastic Container Service (Amazon ECS)
* Nắm chắc cơ chế vận hành của AWS ECS trong việc quản lý vòng đời ứng dụng container hóa thông qua cấu trúc: ECS Cluster, Task Definition (Định nghĩa container), và ECS Service (Quản lý trạng thái thực thi).
* **Thực hành điều phối Container:** Cấu hình hệ thống phân tầng mạng (NAT Gateway, Route Table) an toàn, đăng ký dịch vụ trong Namespace AWS Cloud Map, khởi tạo Cluster chạy trên hạ tầng phi máy chủ AWS Fargate, liên kết Application Load Balancer để tự động điều phối traffic vào các Task ứng dụng ổn định.
* **Nắm rõ chiến lược deployment:** Phân tích quy trình cập nhật ứng dụng dạng Rolling Deployment (cho Frontend) và Blue/Green Deployment (cho Backend) đảm bảo dịch vụ không bị gián đoạn (Zero-downtime).

#### 5. Tìm hiểu giải pháp CI/CD cho ứng dụng Container
* Hiểu tư duy tự động hóa chuỗi quy trình xây dựng (Build), kiểm thử (Test) và triển khai (Deploy) mã nguồn ứng dụng liên tục sử dụng các pipeline công nghệ hiện đại.
* **Thực hành tự động hóa tích hợp:** Cài đặt và đăng ký GitLab Runner tự động kích hoạt pipeline, cấu hình chuỗi tự động hóa GitHub Actions kết nối với AWS CodeBuild để build tự động ứng dụng Frontend/Backend theo tag phát hành code.
* **Giám sát kiến trúc Container:** Kích hoạt tính năng Container Insights trên CloudWatch thu thập hiệu năng chuyên sâu, cấu hình FireLens làm đại lý điều hướng và xuất tập trung logs ứng dụng sang lưu trữ lâu dài tại Amazon S3.

#### 6. Xây dựng Pipeline triển khai lên EC2 với AWS CodePipeline
* Làm chủ trọn vẹn bộ công cụ DevOps chính hãng của AWS bao gồm: CodeCommit (Quản lý mã nguồn), CodeBuild (Biên dịch/đóng gói), CodeDeploy (Triển khai tự động) và CodePipeline (Quản lý luồng tự động tổng thể).
* **Thực hành thiết lập CI/CD cho EC2:** Khởi tạo S3 Bucket lưu trữ artifact, cấu hình phân quyền Instance Profile cho máy chủ, cài đặt CodeDeploy Agent trên EC2, thiết lập chuỗi Source -> Build -> Deploy tự động thông qua CodePipeline và làm chủ kỹ năng rà soát, xử lý lỗi (troubleshooting) trong quá trình thực thi.

#### 7. Tìm hiểu AWS Storage Gateway
* Hiểu vai trò của dịch vụ File Storage Gateway trong việc tạo cầu nối lưu trữ lai (hybrid storage), cho phép kết nối máy chủ On-premises cục bộ trực tiếp tới không gian lưu trữ không giới hạn của Amazon S3 thông qua các giao thức chia sẻ file tiêu chuẩn.
* **Thực hành cấu hình cổng lưu trữ:** Deploy máy chủ Storage Gateway trên EC2, tạo File Shares tương thích và thực hiện gắn (mount) ổ đĩa về máy cục bộ để kiểm tra mượt mà khả năng đọc/ghi dữ liệu thời gian thực.

#### 8. Tìm hiểu Amazon FSx for Windows File Server
* Nắm vững kiến thức về Amazon FSx giúp cung cấp hệ thống lưu trữ tệp tin hiệu năng cao, quản trị tự động hoàn toàn qua giao thức SMB chuẩn hóa cho môi trường hệ điều hành Windows Server trong doanh nghiệp.
* **Thực hành quản lý lưu trữ nâng cao:** Khởi tạo cụm bộ nhớ SSD và HDD phiên bản dự phòng đa vùng Multi-AZ, thực hiện ánh xạ kết nối dữ liệu, cấu hình kích hoạt các tính năng chuyên sâu: Chống trùng lặp dữ liệu (Data Deduplication) tối ưu dung lượng, bật bản sao bóng Shadow Copies khôi phục dữ liệu, cài đặt hạn ngạch bộ nhớ người dùng (User Quotas) và vận hành mở rộng thông lượng/dung lượng không gián đoạn thông qua AWS CLI.

#### 9. Tìm hiểu Data Lake trên AWS
* Hiểu tư duy thiết kế kho dữ liệu tập trung (Data Lake) trên nền tảng Amazon S3 phục vụ lưu trữ khối lượng lớn dữ liệu thô phi cấu trúc hoặc đã xử lý từ nhiều nguồn khác nhau, sẵn sàng cho công tác phân tích chuyên sâu.
* **Thực hành xây dựng trục xử lý dữ liệu:** Phân quyền IAM Policy xử lý dữ liệu, tạo luồng thu thập dữ liệu tự động với Amazon Kinesis Data Firehose Delivery Stream, cấu hình AWS Glue Crawler tự động quét cấu trúc và cập nhật bảng lưu trữ Data Catalog, thực hiện truy vấn tối ưu bằng ngôn ngữ SQL thông qua Amazon Athena và tích hợp trực quan hóa biểu đồ phân tích sang Amazon QuickSight.

#### 10. Tìm hiểu cơ chế tối ưu chi phí hạ tầng (Savings Plans & Reserved Instance)
* Nắm rõ các phương án quản lý tài chính dài hạn trên Cloud khi doanh nghiệp có nhu cầu sử dụng tài nguyên ổn định nhằm giảm thiểu tối đa chi phí vận hành (lên tới 72%).
* **Phân tích mô hình cam kết:** Phân biệt rõ ràng bản chất giữa Savings Plans (cam kết mức chi tiêu tính theo $/giờ linh hoạt linh động cho Compute/EC2/Fargate) và Reserved Instance / Reserved DB Instance (cam kết thuê máy chủ/cơ sở dữ liệu RDS cố định loại cấu hình theo thời hạn 1 năm hoặc 3 năm).
* **Ứng dụng quản trị tài chính:** Đọc hiểu bảng đề xuất tự động Savings Plans Recommendation từ AWS Billing Console để hoạch định ngân sách đầu tư hạ tầng chính xác cho doanh nghiệp.
