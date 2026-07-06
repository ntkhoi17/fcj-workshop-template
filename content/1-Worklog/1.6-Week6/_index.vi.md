---
title: "Worklog Tuần 6"
date: 25-05-2026
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---


### Mục tiêu tuần 6:

* Tìm hiểu cách điều phối quy trình xử lý serverless bằng AWS Step Functions thông qua State Machine, Task State, Choice State, Parallel State và cơ chế xử lý lỗi.
* Thực hành xây dựng ứng dụng serverless sử dụng AWS Lambda, Amazon S3, Amazon DynamoDB, Amazon API Gateway và Frontend web.
* Nắm được cách triển khai ứng dụng serverless bằng AWS Serverless Application Model (SAM) và tự động hóa triển khai bằng AWS CodePipeline.
* Tìm hiểu cơ chế xác thực người dùng bằng Amazon Cognito và thiết lập website tĩnh có bảo mật SSL bằng Amazon S3, Amazon Route 53, AWS Certificate Manager và Amazon CloudFront.
* Làm quen với hệ thống xử lý đơn hàng bất đồng bộ bằng Amazon SQS, Amazon SNS và giám sát ứng dụng Lambda bằng Amazon CloudWatch, CloudWatch Alarm cùng AWS X-Ray.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2   | - Tìm hiểu Bắt đầu với AWS Step Functions<br>- **Thực hành:**<br>&emsp; + Tìm hiểu Service Orchestration và lĩnh vực kinh doanh của workflow mẫu<br>&emsp; + Tạo Cloud9 Instance phục vụ môi trường thực hành<br>&emsp; + Tạo các dịch vụ mẫu bằng AWS Lambda<br>&emsp; + Kiểm tra Account Application và Data Checking<br>&emsp; + Khởi tạo State Machine bằng AWS Step Functions<br>&emsp; + Tạo workflow sử dụng Task State<br>&emsp; + Cập nhật Permission trong SAM Template<br>&emsp; + Xử lý State Input và State Output<br>&emsp; + Cấu hình Choice State để rẽ nhánh workflow<br>&emsp; + Cải tiến workflow với cơ chế kích hoạt và tạm dừng<br>&emsp; + Thêm retry và catch để xử lý lỗi<br>&emsp; + Cấu hình Parallel State để xử lý song song | 25/05/2026   | 25/05/2026      | <https://000047.awsstudygroup.com/vi/> |
| 3   | - Tìm hiểu Serverless - Lambda tương tác với S3 và DynamoDB<br>- Tìm hiểu Serverless - Hướng dẫn viết Frontend gọi API Gateway<br>- **Thực hành:**<br>&emsp; + Tìm hiểu kiến trúc Serverless gồm Lambda, S3, DynamoDB và API Gateway<br>&emsp; + Tạo Lambda Function xử lý ảnh & Cấu hình trigger tự động từ S3 Bucket<br>&emsp; + Tạo IAM Policy cho Lambda Function & Kiểm tra khi có file upload lên S3<br>&emsp; + Tạo bảng DynamoDB với Partition Key và Sort Key<br>&emsp; + Tạo Lambda Function ghi dữ liệu vào DynamoDB & Triển khai Frontend web<br>&emsp; + Tạo Lambda Function đọc/xóa dữ liệu & Thiết lập API Gateway, API Method<br>&emsp; + Cài đặt, kích hoạt CORS & Kiểm tra gọi API bằng Postman và Frontend | 26/05/2026   | 26/05/2026      | <https://000078.awsstudygroup.com/vi/> <br><br> <https://000079.awsstudygroup.com/vi/> |
| 4   | - Tìm hiểu Serverless - Triển khai ứng dụng trên SAM<br>- Tìm hiểu Serverless - Xác thực với Amazon Cognito<br>- **Thực hành:**<br>&emsp; + Chuẩn bị môi trường triển khai ứng dụng serverless bằng AWS SAM<br>&emsp; + Triển khai Frontend web, tạo bảng DynamoDB và cụm Lambda xử lý dữ liệu<br>&emsp; + Cấu hình API Gateway bằng SAM (Tạo GET API, POST API và DELETE API)<br>&emsp; + Tạo Amazon Cognito User Pool quản lý định danh người dùng<br>&emsp; + Tích hợp xác thực Cognito vào API Gateway và Lambda Function Backend<br>&emsp; + Kiểm tra chức năng Đăng ký, Đăng nhập và Xác thực trên giao diện Frontend | 27/05/2026   | 27/05/2026      | <https://000080.awsstudygroup.com/vi/> <br><br> <https://000081.awsstudygroup.com/vi/> |
| 5   | - Tìm hiểu Serverless - Thiết lập trang website static có SSL trên S3<br>- Tìm hiểu Serverless - Xử lý đơn hàng với SQS và SNS<br>- **Thực hành:**<br>&emsp; + Chuẩn bị môi trường website tĩnh trên S3, cấu hình domain Route 53<br>&emsp; + Khởi tạo yêu cầu chứng chỉ SSL/TLS bằng AWS Certificate Manager (ACM)<br>&emsp; + Cấu hình Amazon CloudFront Distribution phân phối trang web qua HTTPS<br>&emsp; + Khởi tạo kiến trúc xử lý đơn hàng: Tạo SQS Queue, SNS Topic, OrdersTable<br>&emsp; + Deploy cụm Lambda: checkout_order, order_management, handle_order, delete_order<br>&emsp; + Kiểm tra luồng Checkout, gửi tin qua SNS và ghi dữ liệu DynamoDB | 28/05/2026   | 28/05/2026      | <https://000082.awsstudygroup.com/vi/> <br><br> <https://000083.awsstudygroup.com/vi/> |
| 6   | - Tìm hiểu Serverless - CI/CD với AWS CodePipeline<br>- Tìm hiểu Serverless - Giám sát Lambda với CloudWatch và X-Ray<br>- **Thực hành:**<br>&emsp; + Khởi tạo Git Repository cho SAM Project & Thiết lập SAM Pipeline CI/CD<br>&emsp; + Cấu hình CodeBuild đóng gói ứng dụng, chuẩn bị CloudFormation Template<br>&emsp; + Thiết lập và chạy tự động Pipeline cho cả hai thành phần Backend & Frontend<br>&emsp; + Đồng bộ mã nguồn tự động build, deploy folder Frontend lên S3 Bucket web<br>&emsp; + Thực hành gỡ lỗi Lambda bằng Logs, cấu hình Custom Metrics & CloudWatch Alarm<br>&emsp; + Tích hợp AWS X-Ray theo dõi Trace của API, phân tích độ trễ và lỗi hệ thống | 29/05/2026   | 29/05/2026      | <https://000084.awsstudygroup.com/vi/> <br><br> <https://000085.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 6:

#### 1. Điều phối ứng dụng với AWS Step Functions
* Hiểu rõ vai trò của AWS Step Functions đóng vai trò làm trung tâm điều phối dịch vụ (Service Orchestration), giúp liên kết nhiều thành phần độc lập thành quy trình nghiệp vụ (workflow) thống nhất.
* Nắm chắc tư duy xây dựng State Machine, làm chủ cơ chế truyền nhận dữ liệu thông qua cấu trúc xử lý State Input và State Output.
* **Thực hành thiết lập Workflow phức hợp:** Triển khai không gian Cloud9 viết ứng dụng mẫu, vận hành cấu hình thành công các thành phần: Task State gọi hàm Lambda xử lý, Choice State rẽ nhánh điều kiện logic, Parallel State thực thi song song đa nhiệm, và bật cơ chế Pause/Resume dựa trên token/callback để xử lý các luồng phê duyệt từ con người.
* **Tối ưu hóa khả năng chịu lỗi:** Cấu hình trực tiếp tính năng `Retry` tự động thử lại khi có lỗi tạm thời và `Catch` để bắt biệt lệ, chuyển tiếp luồng xử lý lỗi an toàn.

#### 2. Kiến trúc ứng dụng Serverless cốt lõi (Lambda, S3, DynamoDB, API Gateway)
* Thấu hiểu sâu sắc nguyên lý vận hành của một kiến trúc Serverless tiêu chuẩn: Tối ưu chi phí theo mức độ sử dụng (Pay-as-you-go), tự động co giãn không giới hạn và triệt tiêu gánh nặng quản trị hạ tầng.
* **Thực hành xây dựng hệ thống thu thập & xử lý ảnh:**
  * Cấu hình S3 PutObject Event tự động kích hoạt hàm Lambda Function xử lý hình ảnh, tích hợp Lambda Layers để tối ưu kích thước mã nguồn khi xử lý resize ảnh.
  * Thiết kế bảng dữ liệu Amazon DynamoDB chuẩn hóa dải khóa Partition Key và Sort Key, phân quyền IAM Policy bảo mật và thực thi mã nguồn CRUD dữ liệu qua bộ SDK.
  * Khởi tạo cổng Amazon API Gateway kết nối an toàn với Backend Lambda, cấu hình các API Method, kích hoạt CORS (Cross-Origin Resource Sharing) để Frontend web trên trình duyệt gọi API thành công qua Postman và môi trường thực tế.

#### 3. Phát triển Serverless nâng cao với AWS SAM (Serverless Application Model)
* Làm chủ framework AWS SAM trong việc chuẩn hóa, khai báo hạ tầng không máy chủ dưới dạng mã (IaC) thông qua tệp cấu hình YAML gọn nhẹ.
* **Thực hành hiện thực hóa hạ tầng:** Tái cấu trúc toàn bộ ứng dụng thủ công trước đó sang mã nguồn SAM, định nghĩa trọn gói API Gateway (GET/POST/DELETE), cụm chức năng Lambda và bảng DynamoDB, giúp quá trình biên dịch tự động chuyển đổi sang AWS CloudFormation chính xác.

#### 4. Quản lý định danh người dùng tập trung bằng Amazon Cognito
* Phân biệt rõ ràng chức năng hệ thống giữa User Pool (Thư mục lưu trữ tài khoản, phục vụ đăng ký/đăng nhập/xác thực mã OTP) và Identity Pool (Cung cấp thông tin quyền hạn tạm thời của AWS IAM để người dùng truy cập trực tiếp tài nguyên AWS).
* **Thực hành tích hợp an ninh:** Khởi tạo Cognito User Pool, liên kết bộ chứng thực (Authorizer) vào API Gateway và kiểm thử thành công các luồng nghiệp vụ bảo mật (Đăng ký, Đăng nhập, Xác thực Token) trực tiếp trên giao diện Frontend.

#### 5. Thiết lập trang Website Static có SSL thông qua mạng lưới phân phối CloudFront
* Hiểu giải pháp bảo vệ dữ liệu truyền tải trên Internet bằng HTTPS kết hợp cơ chế phân giải tên miền và tối ưu hóa bộ nhớ đệm (Caching).
* **Thực hành triển khai hệ thống mạng bảo mật:** Tạo Hosted Zone trên Amazon Route 53 quản lý domain, phát hành chứng chỉ an toàn SSL/TLS miễn phí qua AWS Certificate Manager (ACM), cấu hình thiết lập mạng lưới Amazon CloudFront Distribution để phân phối website tĩnh từ S3 Bucket ra toàn cầu với độ trễ thấp và bảo mật tối đa.

#### 6. Xử lý đơn hàng bất đồng bộ bằng Amazon SQS và Amazon SNS
* Nắm chắc nguyên lý kiến trúc hướng sự kiện (Event-driven Architecture), bóc tách độ phụ thuộc (decoupling) giữa khâu đặt hàng và khâu xử lý dữ liệu phía sau để nâng cao tính ổn định của hệ thống.
* **Thực hành luồng đặt hàng Serverless:** Khởi tạo hàng đợi Amazon SQS kết hợp bộ phân tán tin nhắn Amazon SNS Topic, lập trình chuỗi Lambda (`checkout_order`, `order_management`, `handle_order`, `delete_order`), mô phỏng luồng đưa đơn hàng vào Queue, đẩy thông báo qua SNS, cập nhật dữ liệu vào OrdersTable trên DynamoDB và xóa tin nhắn khỏi hàng đợi khi hoàn tất xử lý.

#### 7. Tự động hóa phát hành Serverless bằng AWS CodePipeline
* Thấu hiểu tư duy DevOps áp dụng cho Serverless giúp loại bỏ thao tác thủ công, giảm thiểu rủi ro khi cập nhật phiên bản phần mềm.
* **Thực hành xây dựng Pipeline CI/CD tự động:** Thiết lập Git Repository, cấu hình dự án CodeBuild tự động biên dịch ứng dụng SAM Project, thiết lập hoàn chỉnh hai luồng CodePipeline độc lập: Luồng Backend (Tự động cập nhật CloudFormation Stack khi đổi code Lambda/API) và luồng Frontend (Tự động build mã nguồn giao diện và đồng bộ đẩy thẳng dữ liệu lên S3 Web Hosting).

#### 8. Giám sát chuyên sâu hệ thống Serverless bằng CloudWatch và AWS X-Ray
* Hiểu tầm quan trọng của công tác kiểm toán, đo lường hiệu năng hiển thị (Observability) trong các hệ thống phân tán Serverless.
* **Thực hành quản trị vận hành:** * Sử dụng CloudWatch Logs để phân tích sâu log thực thi, tra cứu lỗi sự cố (troubleshooting) của Lambda.
  * Thiết lập cấu hình Custom Metrics đo đạc chỉ số doanh nghiệp và cài đặt CloudWatch Alarm để chủ động gửi cảnh báo khi hệ thống vượt ngưỡng cho phép.
  * Kích hoạt AWS X-Ray Trace thu thập bản đồ dịch vụ (Service Map), giúp theo dõi chi tiết đường đi của từng request, bóc tách chính xác độ trễ và điểm nghẽn hiệu năng giữa API Gateway và các hàm Lambda Function.