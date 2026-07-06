---
title: "Worklog Tuần 7"
date: 01-06-2026
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---


### Mục tiêu tuần 7:

* Tìm hiểu cách xây dựng API GraphQL cho ứng dụng serverless bằng AWS AppSync và kết nối dữ liệu với Amazon DynamoDB Resolver.
* Thực hành triển khai ứng dụng container đơn giản trên Amazon Lightsail Container, bao gồm triển khai public image và image tự build.
* Củng cố kiến thức xây dựng Data Lake trên AWS thông qua Amazon S3, AWS Glue, Amazon Athena, Amazon QuickSight và các bước xử lý dữ liệu thực tế.
* Làm quen với các dịch vụ phân tích dữ liệu trên AWS như Amazon Kinesis, AWS Glue, Amazon EMR, Amazon Athena, Amazon QuickSight, AWS Lambda và Amazon Redshift.
* Tìm hiểu các nội dung bảo mật và quản trị truy cập nâng cao với Amazon Cognito Cross Sites và AWS Firewall Manager.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2   | - Tìm hiểu Serverless - Giới thiệu AWS AppSync<br>- Tìm hiểu Bắt đầu với Amazon Lightsail Container<br>- **Thực hành:**<br>&emsp; + Tìm hiểu AWS AppSync và mô hình GraphQL API<br>&emsp; + Tạo DynamoDB Resolver trong AppSync và thực hành các thao tác dữ liệu (Ghi, Đọc, Cập nhật, Xóa, Quét, Truy vấn)<br>&emsp; + Tạo đối tượng phức tạp trong AppSync để mở rộng mô hình dữ liệu<br>&emsp; + Tạo Container Service trên Lightsail & Triển khai Public Image<br>&emsp; + Cấu hình AWS CLI, cài đặt Docker trên Ubuntu để build và push Container Image | 01/06/2026   | 01/06/2026      | <https://000086.awsstudygroup.com/vi/> <br><br> <https://000046.awsstudygroup.com/vi/> |
| 3   | - Tìm hiểu Xây dựng Data Lake trên AWS<br>- Tìm hiểu Xây dựng Datalake với dữ liệu của bạn<br>- **Thực hành:**<br>&emsp; + Tạo IAM Role/Policy, S3 Bucket và Kinesis Firehose Delivery Stream tạo dữ liệu mẫu<br>&emsp; + Tạo Glue Crawler, chuyển đổi dữ liệu, truy vấn bằng Athena và vẽ biểu đồ QuickSight<br>&emsp; + Khởi tạo Cloud9, download dataset, kiểm tra Encoding và đẩy lên S3<br>&emsp; + Dùng AWS Glue DataBrew thực hiện Data Profiling, Clean và Transform dữ liệu<br>&emsp; + Cấu hình ETL chuyển đổi định dạng sang Parquet và kiểm tra Schema | 02/06/2026   | 02/06/2026      | <https://000035.awsstudygroup.com/vi/> <br><br> <https://000070.awsstudygroup.com/vi/> |
| 4   | - Tìm hiểu Các dịch vụ phân tích dữ liệu trên AWS<br>- Tìm hiểu Bắt đầu với Amazon QuickSight<br>- **Thực hành:**<br>&emsp; + Khởi tạo Kinesis Firehose tiếp nhận và xử lý Dummy Data<br>&emsp; + Tạo Glue Crawler và transform dữ liệu với Glue Interactive Sessions / Glue Studio<br>&emsp; + Triển khai cụm Amazon EMR xử lý dữ liệu lớn bằng Apache Spark<br>&emsp; + Phân tích dữ liệu trực tiếp bằng Athena và Kinesis Data Analytics<br>&emsp; + Tạo Analysis trên QuickSight: Vẽ biểu đồ đường, hình tròn, Pivot Table và tạo KPI | 03/06/2026   | 03/06/2026      | <https://000072.awsstudygroup.com/vi/> <br><br> <https://000073.awsstudygroup.com/vi/> |
| 5   | - Tìm hiểu cải tiến Dashboard và tạo Dashboard tương tác trên Amazon QuickSight<br>- Tìm hiểu Triển khai AWS Cognito Cross Sites<br>- **Thực hành:**<br>&emsp; + Định dạng giao diện Dashboard QuickSight, tạo thêm cấu trúc bảng chi tiết dữ liệu<br>&emsp; + Thiết lập tính năng tương tác nâng cao: Cài đặt Filter, Filter Actions và Navigation Actions<br>&emsp; + Phân tích cơ chế hoạt động phối hợp giữa Cognito User Pool và Identity Pool<br>&emsp; + Triển khai cấu hình Cognito Cross Sites và kiểm tra luồng xác thực/ủy quyền | 04/06/2026   | 04/06/2026      | <https://000073.awsstudygroup.com/vi/> <br><br> <https://000141.awsstudygroup.com/vi/> |
| 6   | - Tìm hiểu Quản trị bảo mật với AWS Firewall Manager <br>- **Thực hành:**<br>&emsp; + Nghiên cứu vai trò Security Groups, vai trò AWS Config và AWS Organizations<br>&emsp; + Tích hợp AWS Resource Access Manager kết nối hạ tầng đa tài khoản<br>&emsp; + Thiết lập chính sách kiểm soát Security Groups tập trung với Firewall Manager<br>&emsp; + Chạy tác vụ Audit phát hiện cấu hình sai quy tắc, giới hạn mở cổng RDP/SSH bừa bãi<br>&emsp; + Nghiệm thu và dọn dẹp tài nguyên hệ thống | 05/06/2026   | 05/06/2026      | <https://000097.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 7:

#### 1. Xây dựng API GraphQL với AWS AppSync
* Hiểu sâu kiến thức cốt lõi về mô hình thiết kế API dạng GraphQL so với REST API truyền thống, tối ưu hóa việc truy xuất dữ liệu chỉ trong một truy vấn duy nhất.
* **Thực hành cấu hình Resolver:** Tạo lập thành công kết nối GraphQL API xuống nguồn dữ liệu NoSQL thông qua Amazon DynamoDB Resolver; thực thi mượt mà các phương thức truy xuất: Thêm mới (Create), Đọc (Read), Cập nhật (Update), Xóa (Delete), Quét toàn bảng (Scan) và lọc nâng cao (Query), đồng thời định nghĩa thành công các đối tượng dữ liệu phức tạp.

#### 2. Triển khai Container tinh gọn trên Amazon Lightsail
* Thấu hiểu giải pháp đóng gói và vận hành container của Amazon Lightsail nhằm đơn giản hóa tối đa quy trình quản lý hạ tầng phần cứng phía dưới so với ECS/EKS.
* **Thực hành điều phối Container:** Khởi tạo cấu hình mạng và Deploy thành công một ứng dụng web từ Public Docker Image; đồng thời thực hành kết nối môi trường máy chủ ảo qua CLI để tự biên dịch (build) một Custom Image riêng biệt, tiến hành push (đẩy) trực tiếp lên kho lưu trữ và phát hành phiên bản ứng dụng mới.

#### 3. Xây dựng và chuẩn hóa Data Lake nâng cao
* Làm chủ trọn vẹn quy trình xây dựng kho dữ liệu lớn Data Lake trên nền tảng lưu trữ trung tâm Amazon S3 từ khâu thu thập cho đến trực quan hóa báo cáo.
* **Thực hành xử lý và dọn dẹp dữ liệu (ETL):** Vận hành môi trường mã nguồn Cloud9 để xử lý tập dữ liệu thô (Dataset), kiểm tra Encoding, sử dụng AWS Glue DataBrew thực hiện trích xuất hồ sơ dữ liệu (Data Profiling), thiết lập quy trình Clean/Transform và biên dịch chuyển đổi toàn bộ định dạng tệp sang chuẩn Parquet (dạng lưu trữ cột - Columnar Storage) giúp tăng tốc độ truy vấn SQL trên Amazon Athena và cập nhật chính xác Schema trong Data Catalog.

#### 4. Khai phá các dịch vụ Analytics quy mô lớn trên AWS
* Nắm chắc tư duy kiến trúc và sơ đồ dòng chảy dữ liệu (tiếp nhận -> lưu trữ -> xử lý -> phân tích -> tiêu thụ) trong hệ sinh thái Big Data của AWS.
* **Thực hành vận hành chuỗi Analytics pipeline:** Kết nối Amazon Kinesis Firehose thu thập dữ liệu luồng trực tiếp, ứng dụng công cụ AWS Glue Interactive Sessions và Glue Studio để tạo bộ lọc dữ liệu tự động, triển khai cụm máy chủ Amazon EMR (Elastic MapReduce) để xử lý tính toán tập dữ liệu lớn bằng Apache Spark, kết hợp tích hợp Amazon Kinesis Data Analytics phân tích dữ liệu trực tiếp và nghiên cứu mô hình lưu trữ kho dữ liệu Data Warehouse trên Amazon Redshift.

#### 5. Thiết lập và tối ưu hóa hệ thống Dashboard trực quan Amazon QuickSight
* Hiểu rõ các thành phần cấu trúc cốt lõi của giải pháp Business Intelligence (BI) trên Cloud bao gồm: Data Source, Dataset, Analysis, Visual và Dashboard.
* **Thực hành xây dựng hệ thống báo cáo BI:** Cấu hình phân quyền kết nối và chỉnh sửa Dataset, trực quan hóa trạng thái hệ thống bằng cụm biểu đồ đa dạng (Biểu đồ đường xu hướng, biểu đồ tròn phân phối, Pivot Table và khối hiển thị KPI/Insights).
* **Thiết lập Dashboard tương tác:** Hoàn thiện giao diện báo cáo chuyên nghiệp thông qua việc cấu hình bộ lọc Filter dữ liệu động, thiết lập cơ chế chuyển hướng thông minh Navigation Actions và Filter Actions trước khi phát hành (Publish) phiên bản Dashboard hoàn chỉnh chia sẻ cho người dùng doanh nghiệp.

#### 6. Đồng bộ hệ thống bảo mật xác thực danh tính với Cognito Cross Sites
* Làm chủ giải pháp quản lý danh tính đa nền tảng, thiết lập cơ chế chứng thực an toàn OAuth 2.0 phục vụ Single Sign-On (SSO).
* **Thực hành tích hợp bảo mật liên kết:** Phối hợp chặt chẽ tính năng của Cognito User Pool (máy chủ xác thực người dùng) và Cognito Identity Pool (cấp quyền truy cập tài nguyên AWS dựa trên thuộc tính/vai trò), hiện thực hóa thành công mã nguồn phân tích luồng Token JWT để kiểm soát an ninh nghiêm ngặt trực tiếp trên giao diện Client.

#### 7. Quản trị chính sách an ninh tập trung bằng AWS Firewall Manager
* Thấu hiểu sâu sắc tư duy quản trị an toàn thông tin quy mô doanh nghiệp lớn (Enterprise Security) khi vận hành môi trường đa tài khoản liên kết chặt chẽ thông qua AWS Organizations và AWS Config.
* **Thực hành cấu hình kiểm toán tập trung:** Tích hợp tính năng AWS Resource Access Manager để chia sẻ tài nguyên an toàn, khởi tạo các chính sách (Policies) bảo mật quản lý tập trung hệ thống Security Groups từ Firewall Manager, thực thi tác vụ kiểm toán tự động (Audit) để kịp thời phát hiện và khóa chặn các Security Groups vi phạm quy tắc an toàn thông tin (mở cổng SSH 22 hoặc RDP 3389 công khai ra Internet), triệt tiêu tối đa rủi ro cấu hình sai hệ thống cấu trúc mạng vòng ngoài.
