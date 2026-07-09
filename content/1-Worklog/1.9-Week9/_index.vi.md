---
title: "Worklog Tuần 9"
date: 15-06-2026
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---



### Mục tiêu tuần 9:

* Tìm hiểu tổng quan dự án cuối kỳ Document Management System trên nền tảng AWS Serverless.
* Phân tích kiến trúc hệ thống, luồng xử lý upload tài liệu, xác thực người dùng, quét malware và lưu trữ metadata.
* Xác định các dịch vụ AWS cốt lõi được sử dụng trong hệ thống như Cognito, API Gateway, Lambda, S3, DynamoDB, EventBridge, GuardDuty, CloudFront, CloudWatch và SNS.
* Chuẩn bị môi trường phát triển, công cụ triển khai và cấu trúc source code để phục vụ quá trình xây dựng hệ thống ở các tuần tiếp theo.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2   | - Tìm hiểu tổng quan dự án Document Management System trên AWS Serverless<br>- Tìm hiểu bài toán quản lý tài liệu nội bộ trong doanh nghiệp<br>- **Thực hành:**<br>&emsp; + Xác định mục tiêu hệ thống DMS<br>&emsp; + Xác định nhóm người dùng nội bộ<br>&emsp; + Phân tích các chức năng chính như upload, quản lý phiên bản, chia sẻ, audit log và analytics<br>&emsp; + Đọc cấu trúc nội dung workshop dự án cuối kỳ | 15/06/2026   | 15/06/2026      |  |
| 3   | - Tìm hiểu kiến trúc tổng thể của hệ thống DMS<br>- Tìm hiểu vai trò của các dịch vụ AWS Serverless trong hệ thống<br>- **Thực hành:**<br>&emsp; + Phân tích luồng đăng nhập bằng Amazon Cognito<br>&emsp; + Phân tích luồng gọi API qua Amazon API Gateway<br>&emsp; + Phân tích vai trò của AWS Lambda trong xử lý nghiệp vụ<br>&emsp; + Phân tích vai trò của Amazon S3 trong lưu trữ frontend, quarantine file và tài liệu chính thức<br>&emsp; + Phân tích vai trò của Amazon DynamoDB trong lưu metadata, version, share và audit log | 16/06/2026   | 16/06/2026      |  |
| 4   | - Tìm hiểu luồng upload tài liệu bảo mật bằng Presigned URL<br>- Tìm hiểu cơ chế kiểm dịch file trước khi lưu trữ chính thức<br>- **Thực hành:**<br>&emsp; + Phân tích lý do file không upload trực tiếp qua API Gateway<br>&emsp; + Phân tích luồng tạo Presigned PUT URL từ Intent Lambda<br>&emsp; + Phân tích quá trình frontend upload file vào QuarantineBucket<br>&emsp; + Phân tích cơ chế GuardDuty Malware Protection quét file<br>&emsp; + Phân tích EventBridge kích hoạt Upload Processor Function<br>&emsp; + Phân tích quá trình chuyển file sạch sang DocumentsBucket | 17/06/2026   | 17/06/2026      |  |
| 5   | - Tìm hiểu các quyết định thiết kế quan trọng trong hệ thống DMS<br>- Tìm hiểu mô hình phân quyền và thiết kế dữ liệu<br>- **Thực hành:**<br>&emsp; + Phân tích quyết định sử dụng Presigned URL<br>&emsp; + Phân tích quyết định upload qua QuarantineBucket trước khi đưa vào DocumentsBucket<br>&emsp; + Phân tích DynamoDB single-table design<br>&emsp; + Phân tích các entity chính gồm Document, Version, Share, AuditLog, UploadIntent và UserProfile<br>&emsp; + Phân tích audit log dạng append-only<br>&emsp; + Phân tích nguyên tắc IAM tối thiểu quyền cho từng Lambda Function | 18/06/2026   | 18/06/2026      |  |
| 6   | - Chuẩn bị môi trường triển khai dự án DMS<br>- Tìm hiểu cấu trúc repository và các công cụ cần thiết<br>- **Thực hành:**<br>&emsp; + Kiểm tra tài khoản AWS và quyền truy cập cần thiết<br>&emsp; + Kiểm tra AWS CLI và profile triển khai<br>&emsp; + Kiểm tra Node.js, npm, AWS CDK CLI và Git<br>&emsp; + Tìm hiểu lệnh cài đặt AWS CDK CLI & lệnh CDK Bootstrap<br>&emsp; + Tìm hiểu cấu trúc thư mục: aws/functions, aws/infrastructure, frontend, contracts và docs<br>&emsp; + Chuẩn bị biến môi trường cảnh báo DMS_ALERT_EMAIL | 19/06/2026   | 19/06/2026      |  |

### Kết quả đạt được tuần 9:

#### 1. Tìm hiểu tổng quan dự án Document Management System
* Hiểu DMS là hệ thống quản lý tài liệu nội bộ được xây dựng trên hạ tầng AWS Serverless tối tân.
* Nắm được mục tiêu hệ thống là hỗ trợ upload, lưu trữ, quản lý phiên bản, chia sẻ và theo dõi toàn bộ lịch sử thao tác với tài liệu.
* Hiểu hệ thống được thiết kế đặc thù nhằm phục vụ nhóm người dùng nội bộ trong doanh nghiệp thay vì người dùng công khai bên ngoài.
* Xác định rõ đây là dự án cuối kỳ phức hợp giúp tổng hợp, đúc kết nhiều mảng kiến thức AWS chuyên sâu đã học ở các tuần trước.

#### 2. Xác định các chức năng chính của hệ thống
* Upload tài liệu an toàn.
* Quản lý đa phiên bản (versioning) của tài liệu.
* Liệt kê danh sách tài liệu linh hoạt theo người dùng hoặc theo phòng ban.
* Xem chi tiết thông tin và tải xuống tài liệu bảo mật thông qua Presigned URL.
* Thực hiện chia sẻ hoặc thu hồi nhanh đặc quyền truy cập tài liệu.
* Ghi nhận audit log tập trung (append-only) cho các thao tác hệ thống quan trọng.
* Thống kê trực quan dung lượng lưu trữ và mật độ hoạt động thông qua hệ thống analytics.

#### 3. Tìm hiểu kiến trúc AWS Serverless của DMS
* Hiểu Amazon Cognito đảm nhiệm toàn bộ khâu xác thực người dùng và quản lý phân quyền theo nhóm (Group Memberships).
* Hiểu Amazon API Gateway là điểm tiếp nhận (Endpoint) và điều phối REST API chính của hệ thống.
* Hiểu AWS Lambda đóng vai trò bộ não xử lý các logic nghiệp vụ backend hoàn toàn serverless.
* Hiểu Amazon S3 được dùng đa năng: Lưu trữ mã nguồn tĩnh Frontend, khu vực cách ly kiểm dịch file (Quarantine) và kho tài liệu chính thức (Documents).
* Hiểu Amazon DynamoDB lưu dữ liệu phi cấu trúc: metadata, version, share, audit log và upload intent.
* Hiểu Amazon EventBridge làm trục định tuyến sự kiện phản hồi các trạng thái upload file.
* Hiểu Amazon GuardDuty thực hiện quét mã độc tự động (Malware Protection) cho file ngay khi được tải lên.
* Hiểu Amazon CloudFront làm mạng lưới CDN phân phối giao diện React frontend toàn cầu với độ trễ thấp.
* Hiểu Amazon CloudWatch và Amazon SNS hỗ trợ thu thập logs vận hành, giám sát chỉ số và kích hoạt cảnh báo khẩn cấp.

#### 4. Phân tích luồng đăng nhập và gọi API
* Người dùng truy cập hệ thống một cách an toàn thông qua liên kết Amazon CloudFront.
* CloudFront phân phối giao diện React frontend từ S3 FrontendBucket về trình duyệt của Client.
* Người dùng thực hiện đăng nhập bằng tài khoản Amazon Cognito và nhận về mã JSON Web Token (JWT).
* Frontend đính kèm JWT token vào header để gửi các request đến Amazon API Gateway.
* API Gateway tiến hành xác thực tính hợp lệ của JWT token thông qua cấu hình Cognito Authorizer.
* Toàn bộ request hợp lệ được chuyển tiếp xuống các hàm Lambda Function tương ứng để xử lý logic runtime.

#### 5. Phân tích luồng upload tài liệu bằng Presigned URL
* Frontend gửi yêu cầu lên API để khởi tạo một ý định tải tệp (Upload Intent).
* Hàm Intent Lambda tiếp nhận và tạo ra một liên kết Presigned PUT URL có thời hạn giới hạn ngắn.
* Tệp tin được Frontend upload trực tiếp từ trình duyệt lên S3 QuarantineBucket thông qua Presigned URL vừa nhận.
* Quá trình truyền file lớn không đi qua API Gateway và Lambda, giúp loại bỏ hoàn toàn giới hạn kích thước payload (10MB) và tiết kiệm tài nguyên tính toán backend.
* QuarantineBucket đóng vai trò làm vùng đệm cô lập tạm thời trước khi tài liệu được phê duyệt đưa vào kho lưu trữ chính thức.

#### 6. Tìm hiểu luồng kiểm dịch file độc hại
* File mới xuất hiện trong QuarantineBucket lập tức kích hoạt tính năng GuardDuty Malware Protection quét mã độc tự động.
* GuardDuty thực hiện gán nhãn (tag) kết quả đánh giá an ninh trực tiếp lên S3 object metadata.
* Tệp tin hoàn toàn an toàn được hệ thống gán trạng thái **CLEAN**.
* Tệp tin phát hiện có nguy cơ độc hại được gán trạng thái **THREAT_FOUND**.
* Trục EventBridge bắt sự kiện gán nhãn, tự động định tuyến thông tin đến hàm Upload Processor Function.
* Upload Processor Function đọc dữ liệu tag an ninh để đưa ra quyết định xử lý tiếp theo phù hợp.

#### 7. Phân tích vai trò của Upload Processor Function
* Đọc tệp tin và bóc tách nhãn kết quả quét độc hại từ khu vực QuarantineBucket.
* Triển khai di chuyển an toàn các file sạch (**CLEAN**) sang kho lưu trữ tập trung DocumentsBucket.
* Tiến hành cập nhật trạng thái hoạt động của tài liệu trực tiếp trong cơ sở dữ liệu DynamoDB.
* Ghi nhận toàn bộ metadata và tạo bản ghi version record tương ứng cho tài liệu mới.
* Đẩy nhật ký xử lý chi tiết vào hệ thống giám sát CloudWatch Logs.
* Đảm bảo tuyệt đối không có bất kỳ tệp tin chưa an toàn hoặc nhiễm độc nào được phép lọt vào kho tài liệu chính thức của doanh nghiệp.

#### 8. Tìm hiểu thiết kế DynamoDB single-table
* Hiểu triết lý thiết kế single-table design: gom toàn bộ các thực thể (entities) nghiệp vụ khác nhau vào lưu trữ chung trong duy nhất một bảng DynamoDB để tối ưu chi phí và giảm số lượng bảng quản trị.
* Xác định rõ cấu trúc định danh cho các entity chính bao gồm: Document, Version, Share, AuditLog, UploadIntent và UserProfile.
* Nắm chắc vai trò cốt lõi của Global Secondary Index (GSI) hỗ trợ thực thi các câu lệnh truy vấn dữ liệu phức tạp theo nhiều chiều chỉ mục khác nhau.
* Hiểu cơ chế Time to Live (TTL) được dùng để hệ thống tự động quét và xóa sạch các bản ghi UploadIntent đã hết hạn, giảm rác dữ liệu.

#### 9. Tìm hiểu mô hình phân quyền người dùng
* Xác định nhóm **EMPLOYEE**: Người dùng thông thường trong tổ chức, có các quyền hạn cơ bản.
* Xác định nhóm **DEPARTMENT_ADMIN**: Người quản lý, có đặc quyền điều phối tài liệu trong phạm vi phòng ban được chỉ định.
* Xác định nhóm **SYSTEM_ADMIN**: Quản trị viên tối cao, có toàn quyền cấu hình và giám sát toàn bộ hệ thống.
* Hiểu thông tin phân nhóm (Group Claims) được Cognito tích hợp trực tiếp vào cấu trúc mã JWT token.
* Hiểu cách hàm Lambda thực hiện bóc tách token để kiểm tra quyền hạn của người dùng tại thời điểm runtime trước khi phê duyệt thực thi nghiệp vụ.

#### 10. Tìm hiểu các quyết định thiết kế bảo mật hệ thống
* Sử dụng Presigned URL cho mọi thao tác upload/download nhằm tối ưu hóa băng thông, tránh truyền file dung lượng lớn qua tầng tính toán backend.
* Thiết lập quy trình bắt buộc: Mọi file tải lên đều phải bị cách ly tại QuarantineBucket để quét mã độc trước khi được công nhận chính thức.
* Bảo vệ tài liệu tải xuống bằng Presigned GET URL sinh động có thời gian hết hạn nghiêm ngặt.
* Thiết kế hệ thống audit log theo mô hình append-only (chỉ thêm mới), ngăn chặn triệt để hành vi chỉnh sửa hoặc xóa bỏ lịch sử vận hành.
* Áp dụng nguyên tắc đặc quyền tối thiểu (Least Privilege Principle) bằng cách cấu hình mỗi Lambda Function sở hữu một IAM Role độc lập với các quyền hạn được thu hẹp nhất có thể.

#### 11. Chuẩn bị môi trường triển khai dự án
* Rà soát các điều kiện tài khoản AWS, xác định danh sách các quyền hạn IAM tối thiểu cần có để khởi tạo các tài nguyên: IAM Role, Lambda, S3, DynamoDB, Cognito, CloudFront, EventBridge, GuardDuty, SNS và CloudWatch.
* Kiểm tra và chuẩn bị sẵn cấu hình AWS CLI kết hợp Profile triển khai tương ứng.
* Thiết lập môi trường lập trình cục bộ: Đảm bảo Node.js phiên bản ổn định từ **20.x** trở lên và trình quản lý gói npm từ phiên bản **10.x** trở lên.
* Thực hiện cài đặt bộ công cụ phát triển hạ tầng AWS CDK CLI phiên bản **2.x** và cài đặt Git phục vụ clone/quản lý mã nguồn.

#### 12. Tìm hiểu cấu trúc kiến trúc Repository dự án
* Thư mục **aws/functions**: Nơi tập trung toàn bộ mã nguồn xử lý logic của các hàm Lambda viết bằng TypeScript.
* Thư mục **aws/infrastructure**: Khu vực chứa mã nguồn định nghĩa và dựng hạ tầng AWS CDK Stack.
* Thư mục **frontend**: Chứa mã nguồn giao diện Single Page Application xây dựng trên nền tảng React và trình đóng gói siêu tốc Vite.
* Thư mục **contracts**: Nơi lưu trữ cấu trúc định nghĩa API chuẩn hóa OpenAPI schemas.
* Thư mục **docs**: Hệ thống tài liệu kỹ thuật, mô hình dữ liệu (data model) và tài liệu ghi nhận các quyết định thiết kế (ADR).
* Ghi nhớ quy tắc đóng gói: Cần phải chạy tiến trình biên dịch TypeScript để đảm bảo thư mục đầu ra **dist** của Lambda luôn tồn tại trước khi tiến hành deploy hạ tầng.
