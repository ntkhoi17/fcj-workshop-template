---
title: "Worklog Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---



### Mục tiêu tuần 10:

* Triển khai hạ tầng dự án DMS bằng AWS CDK theo mô hình Infrastructure as Code (IaC).
* Tạo các tài nguyên chính gồm Cognito User Pool, S3 Buckets, DynamoDB Table, Lambda Functions, API Gateway, EventBridge, GuardDuty, CloudFront, CloudWatch và SNS.
* Kiểm tra kết quả triển khai trên AWS Console và xác minh các output quan trọng từ CDK.
* Chuẩn bị nền tảng backend để phục vụ kiểm thử API và luồng upload tài liệu ở tuần tiếp theo.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2   | - Chuẩn bị triển khai hạ tầng DMS bằng AWS CDK<br>- **Thực hành:**<br>&emsp; + Clone repository dự án DMS và cài đặt dependencies bằng npm<br>&emsp; + Cấu hình file môi trường **.env** từ **.env.example**<br>&emsp; + Thiết lập biến ngân sách cảnh báo **DMS_ALERT_EMAIL**<br>&emsp; + Biên dịch (Build) Lambda Functions từ TypeScript sang JavaScript<br>&emsp; + Rà soát cấu trúc thư mục đầu ra **dist** sau khi build<br>&emsp; + Thực thi lệnh CDK Bootstrap cho đúng tài khoản và Region đích | 22/06/2026   | 22/06/2026      | |
| 3   | - Tìm hiểu và triển khai các tài nguyên Identity, Storage và Database bằng CDK<br>- **Thực hành:**<br>&emsp; + Định nghĩa và deploy Cognito User Pool **dms-dev** bằng email đăng nhập<br>&emsp; + Tạo lập thủ công các nhóm người dùng: EMPLOYEE, DEPARTMENT_ADMIN, SYSTEM_ADMIN<br>&emsp; + Thiết lập chính sách bảo mật mật khẩu (Password Policy) cho User Pool<br>&emsp; + Tạo cụm 3 buckets S3 độc lập: FrontendBucket, QuarantineBucket, DocumentsBucket<br>&emsp; + Kích hoạt cấu hình Block All Public Access và thiết lập CORS cho QuarantineBucket<br>&emsp; + Khởi tạo bảng DynamoDB **dms-dev** (PAY_PER_REQUEST, PITR, TTL và cụm GSI) | 23/06/2026   | 23/06/2026      |  |
| 4   | - Tìm hiểu và triển khai tầng xử lý Compute, API và trục điều hướng sự kiện Event<br>- **Thực hành:**<br>&emsp; + Khởi tạo cụm chức năng Lambda Backend xử lý API nghiệp vụ (**me**, **documents**, **document-detail**, **document-audit-events**, **upload-intents**, **download-intents**, **document-sharing**, **admin-users**, **analytics**) và hàm core xử lý tệp **process-upload**<br>&emsp; + Định nghĩa API Gateway REST API liên kết Authorizer xác thực mã thông báo Cognito<br>&emsp; + Cấu hình EventBridge bắt sự kiện **ObjectCreated** của QuarantineBucket | 24/06/2026   | 24/06/2026      |  |
| 5   | - Tìm hiểu và triển khai các dịch vụ Security, CDN và hệ thống Monitoring cảnh báo<br>- **Thực hành:**<br>&emsp; + Cấu hình phân quyền IAM Role riêng biệt cho GuardDuty Malware Protection<br>&emsp; + Kích hoạt tính năng tự động quét mã độc và gán nhãn an ninh cho QuarantineBucket<br>&emsp; + Định nghĩa mạng lưới CloudFront Distribution liên kết FrontendBucket qua OAC<br>&emsp; + Thiết lập hệ thống CloudWatch Log Groups cho Lambda và lưu trữ theo mốc dev<br>&emsp; + Khởi tạo SNS Topic cảnh báo lỗi và đăng ký phân phối tin nhắn qua Email | 25/06/2026   | 25/06/2026      |  |
| 6   | - Thực thi Deploy toàn bộ cấu trúc hạ tầng hệ thống và kiểm toán sau triển khai<br>- **Thực hành:**<br>&emsp; + Khởi chạy lệnh deploy tự động: **npx cdk deploy -c environment=dev -c alertEmail=...**<br>&emsp; + Phân tích kết quả CDK Outputs (**UserPoolId**, **UserPoolClientId**, **ApiUrl**, **CloudFrontUrl**)<br>&emsp; + Kiểm định trạng thái hoạt động của CloudFormation Stack **DmsStack-dev**<br>&emsp; + Rà soát thực tế cấu hình các thành phần: DynamoDB, S3, Lambda, API Gateway trên Console | 26/06/2026   | 26/06/2026      |  |

### Kết quả đạt được tuần 10:

#### 1. Chuẩn bị mã nguồn và thiết lập môi trường triển khai dự án
* Khởi tạo thành công không gian làm việc bằng cách clone mã nguồn DMS Project về máy.
* Cài đặt toàn vẹn các thư viện phụ thuộc (dependencies) thông qua trình quản lý gói npm.
* Đồng bộ hóa cấu hình hệ thống bằng cách khởi tạo file môi trường mật **.env** từ mẫu **.env.example**, đồng thời khai báo địa chỉ email quản trị thông qua biến **DMS_ALERT_EMAIL**.
* Thực hiện biên dịch thành công toàn bộ mã nguồn xử lý của Lambda từ ngôn ngữ TypeScript sang JavaScript, đảm bảo thư mục phân phối đầu ra **dist** được tạo lập chính xác và sẵn sàng cho công tác đóng gói hạ tầng.

#### 2. Thực thi quy trình CDK Bootstrap hệ thống
* Hiểu sâu bản chất của lệnh CDK Bootstrap là tạo dựng các tài nguyên nền tảng (như Amazon S3 bucket lưu trữ artifact, các IAM Roles thực thi) nhằm hỗ trợ AWS CloudFormation nhận diện và triển khai ứng dụng.
* Thực hiện khởi chạy thành công tác vụ bootstrap nhắm trúng mã AWS Account và dải Region mục tiêu của dự án, kiểm tra xác thực trạng thái hoàn tất của stack nền **CDKToolkit** trực tiếp trên Console.

#### 3. Thiết kế và triển khai cơ chế quản lý định danh Amazon Cognito
* Định nghĩa và deploy thành công dịch vụ Amazon Cognito User Pool với tên gọi mã hóa theo môi trường **dms-dev**.
* Khóa chặt luồng an ninh bằng cách cấu hình cơ chế đăng nhập bắt buộc qua Email, tắt hoàn toàn tính năng tự đăng ký tự do (Self-signup) để đảm bảo chỉ có tài khoản Quản trị viên tối cao mới được quyền cấp phát thành viên mới.
* Phân tách tổ chức thành công thông qua cụm 3 nhóm đặc quyền cố định: **EMPLOYEE**, **DEPARTMENT_ADMIN**, và **SYSTEM_ADMIN**.
* Áp dụng bộ quy chuẩn chính sách bảo mật mật khẩu phức tạp (Password Policy) kết hợp hoạch định thời gian hết hạn an toàn cho bộ mã thông báo: Access Token, ID Token và Refresh Token.

#### 4. Quy hoạch hệ thống kho lưu trữ Amazon S3 và bảo mật nâng cao
* Triển khai cấu trúc an toàn thông tin bao gồm 3 S3 Bucket đảm nhận các vai trò biệt lập:
  * **FrontendBucket**: Nơi lưu trữ tập trung toàn bộ mã nguồn tĩnh của trang Single Page Application.
  * **QuarantineBucket**: Vùng đệm cách ly cô lập, tiếp nhận tệp tin tải lên ban đầu để phục vụ công tác rà soát.
  * **DocumentsBucket**: Kho lưu trữ chính thức tuyệt mật, nơi chứa các tài liệu đã được phê duyệt an toàn.
* Kích hoạt cơ chế an ninh nghiêm ngặt **Block All Public Access** cho toàn bộ các bucket vừa tạo nhằm ngăn chặn nguy cơ rò rỉ dữ liệu ra Internet.
* Cấu hình chính sách CORS (Cross-Origin Resource Sharing) chi tiết cho **QuarantineBucket** nhằm cấp phép mượt mà cho các cuộc gọi giao thức **PUT** truyền tải file trực tiếp từ trình duyệt của người dùng.

#### 5. Thiết lập bảng cơ sở dữ liệu Single-Table thiết kế Amazon DynamoDB
* Khởi tạo thành công bảng cơ sở dữ liệu NoSQL **dms-dev** áp dụng mô hình single-table design tối ưu chi phí vận hành.
* Kích hoạt chế độ tính phí linh hoạt **PAY_PER_REQUEST** để tự động co giãn theo lưu lượng request thực tế và bật cơ chế mã hóa toàn vẹn dữ liệu bằng AWS Managed Key.
* Nâng cao tính an toàn dữ liệu doanh nghiệp thông qua việc kích hoạt tính năng khôi phục theo mốc thời gian Point-In-Time Recovery (PITR).
* Cấu hình thuộc tính tự động quét rác dữ liệu **expiresAtEpoch** cho tính năng Time to Live (TTL) nhằm dọn sạch các bản ghi ý định tải lên (Upload Intents) đã hết hạn.
* Triển khai hoàn chỉnh hệ thống các chỉ mục phụ toàn cục (Global Secondary Indexes - GSI) phục vụ đa dạng các mẫu truy vấn nghiệp vụ phức tạp của ứng dụng.

#### 6. Lập trình và phân quyền tầng tính toán AWS Lambda
* Khởi chạy toàn bộ cụm chức năng Lambda xử lý Backend nghiệp vụ, cấu hình đồng bộ chạy trên môi trường Runtime Node.js phiên bản mới và tận dụng kiến trúc vi xử lý ARM64 để tăng tốc độ phản hồi đồng thời tối ưu hóa 34% chi phí tính toán.
* Thiết lập hệ thống phân tách đặc quyền: Cấp phát cho mỗi hàm Lambda một IAM Role vận hành độc lập theo đúng nguyên tắc đặc quyền tối thiểu (Least Privilege Principle), tuyệt đối không dùng chung quyền hạn.
* Kích hoạt tính năng AWS X-Ray Active Tracing xuyên suốt các hàm tính toán nhằm thu thập bản đồ dịch vụ và đo lường độ trễ end-to-end.

#### 7. Triển khai cổng API bảo mật Amazon API Gateway và trục sự kiện EventBridge
* Khởi tạo thành công hệ thống REST API Gateway làm điểm tiếp nhận duy nhất cho toàn bộ các yêu cầu từ tầng ứng dụng Client.
* Tích hợp thành công bộ chứng thực cao cấp **Cognito Authorizer** để API Gateway tự động đánh chặn, giải mã và kiểm tra tính hợp lệ của mã thông báo JWT đính kèm trong Header, khóa chặt mọi route nghiệp vụ nhạy cảm.
* Đồng bộ hóa cấu hình tính năng gửi sự kiện của S3, thiết lập để **QuarantineBucket** tự động bắn tín hiệu sự kiện **ObjectCreated** (tạo tệp mới) sang trục Amazon EventBridge.
* Định nghĩa thành công Rule bắt sự kiện tại phân vùng prefix **quarantine/**, cấu hình chuyển tiếp dữ liệu sự kiện sang cho hàm **process-upload** Lambda làm đích xử lý bất đồng bộ, kèm theo thiết lập hàng đợi Dead Letter Queue (DLQ) dự phòng lỗi.

#### 8. Triển khai GuardDuty Malware Protection quét mã độc tự động
* Khởi tạo IAM Role đặc thù cấp quyền cho dịch vụ an ninh AWS GuardDuty có khả năng tương tác và đọc ghi dữ liệu trên khu vực cách ly.
* Triển khai cấu hình kích hoạt thành công tính năng **Malware Protection Plan** liên kết trực tiếp vào **QuarantineBucket**.
* Thiết lập hệ thống tự động quét mã độc thời gian thực, đảm bảo ngay khi tệp tin đổ vào vùng đệm sẽ lập tức bị rà soát và tự động gắn nhãn tag an ninh tương ứng với hai trạng thái logic: **CLEAN** (Tệp sạch) hoặc **THREAT_FOUND** (Phát hiện mối đe dọa nguy hiểm).

#### 9. Tối ưu phân phối nội dung với CloudFront CDN và thiết lập giám sát CloudWatch / SNS
* Tạo lập mạng lưới Amazon CloudFront Distribution làm lớp lá chắn vòng ngoài phân phối mã nguồn Static SPA từ **FrontendBucket** ra toàn cầu.
* Áp dụng giao thức bảo mật cao cấp Origin Access Control (OAC) để khóa chặt bucket lưu trữ, ép buộc toàn bộ luồng truy cập frontend chỉ được phép đi qua CloudFront CDN.
* Khởi tạo hệ thống CloudWatch Log Groups cho từng hàm Lambda với cấu hình thời hạn lưu trữ log tối ưu cho môi trường phát triển (Dev Environment).
* Thiết lập trục cảnh báo khẩn cấp Amazon SNS Topic kết hợp CloudWatch Alarms gửi email trực tiếp tới hòm thư quản trị viên ngay khi hệ thống backend phát sinh lỗi nghiêm trọng (**5XX Error Rate**) hoặc chi phí sử dụng vượt ngưỡng dự toán ngân sách.

#### 10. Nghiệm thu tổng thể kết quả triển khai hạ tầng
* Chạy hoàn tất chuỗi lệnh triển khai và nhận về kết quả thành công tuyệt đối từ CloudFormation Stack **DmsStack-dev** với trạng thái ghi nhận **CREATE_COMPLETE**.
* Trích xuất chính xác các thông số CDK Outputs quan trọng (**UserPoolId**, **UserPoolClientId**, **ApiUrl**, **CloudFrontUrl**) phục vụ cho giai đoạn cấu hình ứng dụng.
* Thực hiện rà soát chéo (Double-check) trên giao diện AWS Console, xác nhận toàn bộ các tài nguyên Storage (S3), Database (DynamoDB), Identity (Cognito), Compute (Lambda), Security (GuardDuty) và Network (API Gateway/CloudFront) đã hiển thị đầy đủ, thông suốt và sẵn sàng vận hành.
