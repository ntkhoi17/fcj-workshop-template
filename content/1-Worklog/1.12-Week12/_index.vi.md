---
title: "Worklog Tuần 12"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---


### Mục tiêu tuần 12:

* Hoàn thiện phần cấu hình bảo mật chuyên sâu và thiết lập hệ thống giám sát cho dự án DMS thông qua các lớp IAM Least Privilege, S3 Private Bucket, Presigned URL, GuardDuty, Cognito, CloudWatch, X-Ray và SNS.
* Kiểm tra và đánh giá thực tế năng lực của các lớp bảo vệ dữ liệu, quyền hạn truy cập, phân quyền theo nhóm người dùng và tính an toàn của luồng xử lý tệp tin.
* Thực hiện giải phóng, dọn dẹp toàn bộ tài nguyên hạ tầng AWS bằng câu lệnh CDK Destroy nhằm tối ưu chi phí và tránh phát sinh hóa đơn ngoài ý muốn.
* Tổng kết toàn diện kết quả triển khai dự án cuối khóa DMS, đúc kết các bài học kinh nghiệm và kiểm tra chi phí chu kỳ thanh toán tại AWS Billing & Cost Explorer.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2   | - Tìm hiểu IAM Least Privilege và bảo mật quyền truy cập trong hệ thống DMS<br>- Tìm hiểu bảo mật Amazon S3 bằng Private Bucket và Presigned URL<br>- **Thực hành:**<br>&emsp; + Kiểm tra và xác thực cấu hình IAM Role độc lập cho từng Lambda Function<br>&emsp; + Rà soát quyền **dynamodb:Query** cho Lambda **documents** và quyền **PutItem**/**s3:PutObject** cho Lambda **upload-intents**<br>&emsp; + Xác minh quyền **GetItem**/**s3:GetObject** cho Lambda **download-intents** và quyền quản trị Cognito cho Lambda **admin-users**<br>&emsp; + Kiểm toán Block All Public Access trên cả 3 S3 buckets và kiểm tra thời hạn link | 06/07/2026   | 06/07/2026      |  |
| 3   | - Tìm hiểu GuardDuty Malware Protection và Cognito Role-based Access Control<br>- **Thực hành:**<br>&emsp; + Kiểm tra trạng thái Malware Protection Plan và danh sách Protected Buckets trên GuardDuty<br>&emsp; + Truy vết nhãn tag kết quả scan thực tế trên S3 object trong QuarantineBucket<br>&emsp; + Xác minh logic hàm **process-upload** chỉ xử lý các file mang nhãn **CLEAN**<br>&emsp; + Kiểm thử phân cấp đặc quyền runtime trên Frontend tương ứng với các JWT Claims của 3 nhóm: EMPLOYEE, DEPARTMENT_ADMIN, SYSTEM_ADMIN | 07/07/2026   | 07/07/2026      |  |
| 4   | - Tìm hiểu CloudWatch Logs, CloudWatch Insights, X-Ray tracing và SNS Alerts<br>- **Thực hành:**<br>&emsp; + Phân tích structured logs của hệ thống bên trong các CloudWatch Log Groups<br>&emsp; + Sử dụng CloudWatch Logs Insights thực thi truy vấn log nâng cao bằng bộ lọc<br>&emsp; + Xác minh bản ghi audit log tự động sinh ra khi người dùng thao tác tệp tin<br>&emsp; + Kiểm tra bản đồ Trace X-Ray và xác thực trạng thái Confirmed của SNS Topic | 08/07/2026   | 08/07/2026      |  |
| 5   | - Khởi chạy tiến trình gỡ bỏ, dọn dẹp (Cleanup) hạ tầng tài nguyên hệ thống trên AWS<br>- **Thực hành:**<br>&emsp; + Di chuyển vào thư mục **aws/infrastructure** tại local terminal<br>&emsp; + Thực thi câu lệnh phá hủy hạ tầng tự động: **npx cdk destroy -c environment=dev**<br>&emsp; + Giám sát luồng gỡ bỏ cấu hình stack **DmsStack-dev** trên giao diện dòng lệnh<br>&emsp; + Đăng nhập Console kiểm tra chéo trạng thái xóa sạch của S3, DynamoDB, Lambda, Cognito, API Gateway, EventBridge và CloudFront Distribution | 09/07/2026   | 09/07/2026      |  |
| 6   | - Tổng kết đánh giá dự án DMS và kiểm toán chi phí hóa đơn chu kỳ thanh toán<br>- **Thực hành:**<br>&emsp; + Truy cập AWS Billing và Cost Explorer để kiểm tra biến động chi phí sau cleanup<br>&emsp; + Tổng hợp hệ thống các dịch vụ AWS, danh sách tính năng và các lớp bảo mật đã áp dụng<br>&emsp; + Ghi nhận toàn bộ luồng kiến trúc xử lý tệp tin Serverless đầu cuối an toàn<br>&emsp; + Đúc kết bài học kinh nghiệm thiết kế kiến trúc và hoàn thiện tập tài liệu báo cáo | 10/07/2026   | 10/07/2026      |  |

### Kết quả đạt được tuần 12:

#### 1. Thấu hiểu và áp dụng nguyên tắc đặc quyền tối thiểu IAM Least Privilege
* Phân tích sâu tầm quan trọng của việc cấp phát IAM Role độc lập cho từng hàm Lambda nghiệp vụ riêng biệt thay vì sử dụng một siêu Role chung (Wildcard Master Role) cho toàn bộ Backend, giúp thu hẹp bề mặt tấn công khi có sự cố bảo mật.
* **Kiểm toán chính sách đặc quyền Lambda:** * Xác nhận Lambda **documents** chỉ mang duy nhất quyền đọc dữ liệu thông qua hành động **dynamodb:Query**.
  * Xác nhận Lambda **upload-intents** chỉ sở hữu quyền **dynamodb:PutItem** ghi nhận ý định tải file và quyền **s3:PutObject** trên vùng cách ly.
  * Xác nhận Lambda **download-intents** cô lập trong phạm vi **dynamodb:GetItem** và tạo liên kết **s3:GetObject** từ kho tệp chính thức.
  * Xác nhận Lambda **admin-users** sở hữu riêng quyền gọi API quản trị nhân sự trên thư mục Cognito.
  * Xác nhận Lambda **process-upload** nắm giữ đặc quyền chuyển vùng dữ liệu (đọc từ Quarantine, ghi sang Documents và cập nhật DynamoDB).

#### 2. Kiểm soát an toàn kho lưu trữ S3 và cơ chế Presigned URL
* Xác thực cấu hình bảo mật nghiêm ngặt trên toàn bộ 3 S3 Bucket (**FrontendBucket**, **QuarantineBucket**, **DocumentsBucket**), đảm bảo tính năng **Block All Public Access** hoạt động 100%, triệt tiêu hoàn toàn khả năng dò đoán hoặc truy cập URL trực tiếp từ bên ngoài Internet.
* Chứng minh tính đúng đắn của cơ chế Presigned URL (phân biệt rõ PUT URL cho tải lên và GET URL cho tải xuống) đóng vai trò cấp đặc quyền truy cập tạm thời an toàn, tự động hết hạn chính xác theo cấu hình mốc thời gian mạt định của hệ thống.

#### 3. Thử nghiệm hệ thống phòng vệ mã độc thông minh với GuardDuty
* Rà soát bảng điều khiển GuardDuty Console, xác nhận tính năng **Malware Protection Plan** đã giám sát chuẩn xác phạm vi các vùng lưu trữ được chỉ định (**Protected Buckets**).
* Xác minh luồng rà soát mã độc thời gian thực: Khi frontend tải tệp tin lên, GuardDuty tự động can thiệp đánh giá và gán nhãn tag an ninh tương ứng trực tiếp lên S3 Object (**CLEAN** cho tệp sạch và **THREAT_FOUND** cho tệp nhiễm độc).
* Kiểm chứng tính an toàn tuyệt đối của logic hậu kiểm dịch: Hàm **process-upload** thực hiện đọc nhãn tag thành công, lập tức gỡ bỏ và xóa sạch các tệp có nhãn nguy hiểm, chỉ cho phép các tệp sạch di chuyển vào kho lưu trữ cốt lõi.

#### 4. Phân cấp đặc quyền người dùng với Cognito Role-Based Access Control
* Xác minh tính năng phân tầng bảo mật tại thời điểm runtime dựa trên cấu trúc các nhóm quyền (Group Claims) tích hợp sẵn trong bộ mã xác thực JWT token của Amazon Cognito:
  * Nhóm **EMPLOYEE**: Chỉ có quyền cơ bản để tải lên, liệt kê và tải xuống các tệp tin do chính mình sở hữu.
  * Nhóm **DEPARTMENT_ADMIN**: Nắm giữ đặc quyền quản lý, điều phối và thiết lập liên kết chia sẻ tài liệu trong phạm vi ranh giới phòng ban.
  * Nhóm **SYSTEM_ADMIN**: Sở hữu đặc quyền tối cao, có khả năng quản trị danh sách người dùng, giám sát biểu đồ hệ thống và truy cập kho tài liệu tập trung.

#### 5. Khai thác dữ liệu Log tập trung nâng cao với CloudWatch Insights và X-Ray
* Làm chủ kỹ năng quản trị vận hành thông qua hệ thống log cấu trúc (Structured Logs) được thu thập tự động từ mã nguồn Lambda đổ về CloudWatch Log Groups.
* **Thực hành phân tích chuyên sâu:** Sử dụng công cụ CloudWatch Logs Insights viết câu lệnh truy vấn lọc log theo mốc thời gian (**timestamp**) và nội dung thông điệp (**message**) để bóc tách chính xác các bản ghi audit log append-only (thao tác upload, xem, share, tải xuống), đảm bảo đáp ứng tốt các yêu cầu kiểm toán an ninh doanh nghiệp.
* Xác minh biểu đồ dịch vụ end-to-end thông qua các điểm Trace của AWS X-Ray nhằm đo lường mượt mà độ trễ cuộc gọi API.

#### 6. Đồng bộ hệ thống giám sát và trục cảnh báo an toàn thông tin
* Xác thực trạng thái liên kết thông suốt giữa CloudWatch Alarms và trục phân phối tin nhắn Amazon SNS Topic (**DmsAlertTopic**).
* Kiểm tra hòm thư điện tử của quản trị viên, đảm bảo trạng thái đăng ký nhận tin đạt mức **Confirmed**, sẵn sàng tiếp nhận các thông báo khẩn cấp đẩy về từ hệ thống ngay khi backend phát sinh lỗi vượt ngưỡng (**5XX Error Rate**) hoặc chi phí ước tính tháng vượt định mức.

#### 7. Vận hành quy trình dọn dẹp giải phóng hạ tầng bằng CDK Destroy
* Thực hiện di chuyển vào thư mục hạ tầng **aws/infrastructure** tại local terminal và kích hoạt tiến trình phá hủy hạ tầng tự động thông qua câu lệnh: **npx cdk destroy -c environment=dev**.
* Giám sát toàn bộ luồng gỡ bỏ tài nguyên diễn ra trên màn hình terminal, hiểu sâu sắc best practice dọn dẹp tài nguyên (Resource Cleanup) là bắt buộc sau khi kết thúc dự án hoặc kết thúc quá trình nghiên cứu để chặn đứng hoàn toàn nguy cơ phát sinh chi phí lãng phí trên tài khoản Cloud.

#### 8. Nghiệm thu kết quả gỡ bỏ hạ tầng trên AWS Console
* Đăng nhập chéo vào tài khoản quản trị AWS Web Console, xác thực CloudFormation Stack **DmsStack-dev** đã được xóa bỏ hoàn toàn khỏi hệ thống mà không phát sinh lỗi.
* Xác minh toàn bộ các tài nguyên thành phần đã bị gỡ bỏ sạch sẽ, bao gồm: cả 3 S3 Buckets, bảng DynamoDB **dms-dev**, cụm các hàm Lambda Functions, cấu hình API Gateway REST API, các EventBridge Rules, mạng phân phối CloudFront Distribution, SNS Topic và cấu hình quét của GuardDuty Plan.

#### 9. Kiểm toán chi phí hậu chiến dịch tại AWS Billing
* Khai thác bảng quản trị tài chính AWS Billing và bộ công cụ Cost Explorer để kiểm tra chéo các chỉ số biến động hóa đơn sau khi thực hiện chiến dịch dọn dẹp tài nguyên.
* Rà soát chi tiết chi phí tích lũy của các nhóm dịch vụ S3, DynamoDB, số lượt triệu gọi Lambda, dung lượng log lưu trữ trên CloudWatch Logs và mốc sử dụng GuardDuty, đảm bảo toàn bộ tài nguyên đã dừng tính phí chính xác và ghi nhận các khoản phí nhỏ còn dư lại (nếu có) trong chu kỳ thanh toán hiện hành.

#### 10. Tổng kết đúc kết giá trị dự án cuối khóa DMS
* Tổng kết thành công dự án Document Management System chạy hoàn toàn trên mô hình Serverless tân tiến nhất của AWS. Hệ thống đáp ứng trọn vẹn các bài toán thực tế của doanh nghiệp: Xác thực bảo mật Cognito, quản trị cổng API Gateway, lưu trữ biệt lập an toàn S3 Private Bucket, quét mã độc GuardDuty thời gian thực, điều hướng trục sự kiện EventBridge, thiết kế bảng tối ưu dữ liệu DynamoDB Single-Table và giám sát tập trung CloudWatch/SNS.
* **Đúc kết bài học chuyên môn giá trị:** 
  * Nắm vững kỹ nghệ lập trình, đóng gói và triển khai hạ tầng tự động thông qua mã Code (IaC) với bộ công cụ mạnh mẽ AWS CDK.
  * Làm chủ tư duy bóc tách kiến trúc hệ thống đa tầng phân tầng độc lập (Frontend, API, Compute Logic, Secure Storage, Monitoring).
  * Ứng dụng thành thạo mô hình single-table design để tối ưu hóa hiệu năng truy vấn NoSQL cho các hệ thống có cấu trúc thực thể đa dạng, tích lũy nền tảng tư duy thiết kế hệ thống Cloud bền vững, sẵn sàng cho các dự án quy mô doanh nghiệp trong tương lai.
