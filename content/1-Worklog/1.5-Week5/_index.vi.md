---
title: "Worklog Tuần 5"
date: 18-05-2026
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---


### Mục tiêu tuần 5:

* Tìm hiểu các phương pháp lựa chọn kích thước máy chủ phù hợp, trực quan hóa chi phí và phân tích chi phí sử dụng nâng cao trên AWS.
* Nắm được quy trình chuyển đổi ứng dụng Monolith TravelBuddy sang kiến trúc Microservices thông qua Elastic Beanstalk, CodeStar, CodePipeline, Lambda và API Gateway.
* Thực hành cơ cấu lại dữ liệu và quy trình làm việc bằng Amazon DynamoDB, AWS Lambda, AWS Step Functions và các workflow serverless.
* Tìm hiểu các mô hình truyền tin và xử lý sự kiện giữa các microservices bằng Amazon SQS, Amazon SNS, Amazon Kinesis và MQTT.
* Làm quen với việc xây dựng Single Page Application có xác thực bằng Amazon Cognito và trải nghiệm các dịch vụ AI trên AWS như Amazon Polly, Amazon Rekognition và Amazon Lex.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2   | - Tìm hiểu Lựa chọn kích thước máy chủ phù hợp với Amazon EC2 Resource Optimization<br>- Tìm hiểu Trực quan hóa Chi phí sử dụng trên AWS<br>- Tìm hiểu Phân tích chi phí sử dụng nâng cao với AWS Glue và Amazon Athena<br>- **Thực hành:**<br>&emsp; + Làm quen với Amazon CloudWatch<br>&emsp; + Tạo IAM Role để sử dụng với Amazon CloudWatch Agent<br>&emsp; + Gắn CloudWatch IAM Role với EC2 Instance<br>&emsp; + Cài đặt CloudWatch Agent<br>&emsp; + Cập nhật Amazon EC2 Resource Optimization<br>&emsp; + Xem đề xuất tối ưu kích thước EC2 bằng AWS Compute Optimizer<br>&emsp; + Xem chi phí và mức sử dụng theo dịch vụ<br>&emsp; + Xem chi phí và mức sử dụng theo tài khoản<br>&emsp; + Xem phạm vi của Savings Plans và Reserved Instance<br>&emsp; + Tạo báo cáo EC2 tùy chỉnh<br>&emsp; + Phân tích chi phí bằng AWS Cost Explorer<br>&emsp; + Chuẩn bị cơ sở dữ liệu cho phân tích chi phí<br>&emsp; + Xây dựng cơ sở dữ liệu với AWS Glue<br>&emsp; + Truy vấn dữ liệu chi phí bằng Amazon Athena | 18/05/2026   | 18/05/2026      | <https://000032.awsstudygroup.com/vi/> <br><br> <https://000034.awsstudygroup.com/vi/> <br><br> <https://000040.awsstudygroup.com/vi/> |
| 3   | - Tìm hiểu Dịch chuyển ứng dụng Monolith<br>- Tìm hiểu Tự động phát hành ứng dụng<br>- **Thực hành:**<br>&emsp; + Tạo Key Pair<br>&emsp; + Tạo CloudFormation Stack phục vụ môi trường TravelBuddy<br>&emsp; + Kết nối Windows Instance<br>&emsp; + Cài đặt Database<br>&emsp; + Tải Project TravelBuddy<br>&emsp; + Kiểm tra ứng dụng cục bộ bằng Eclipse IDE<br>&emsp; + Triển khai ứng dụng Monolith lên AWS Elastic Beanstalk<br>&emsp; + Cập nhật ứng dụng và truy vấn API bằng Eclipse IDE<br>&emsp; + Chuẩn bị môi trường phát hành tự động<br>&emsp; + Thiết lập AWS CodeStar Project<br>&emsp; + Kết nối Eclipse IDE với AWS CodeCommit<br>&emsp; + Thay thế ứng dụng mẫu<br>&emsp; + Triển khai thông qua Pipeline<br>&emsp; + Xác định lỗi trong quá trình triển khai<br>&emsp; + Tạo EC2 Windows Instance<br>&emsp; + Tạo CodeDeploy Application và Deployment Group<br>&emsp; + Tạo S3 Bucket lưu gói triển khai<br>&emsp; + Triển khai Windows Service bằng AWS CodeDeploy | 19/05/2026   | 19/05/2026      | <https://000050.awsstudygroup.com/vi/> <br><br> <https://000051.awsstudygroup.com/vi/> |
| 4   | - Tìm hiểu Tạo một Microservice<br>- Tìm hiểu Cơ cấu lại dữ liệu và quy trình làm việc<br>- **Thực hành:**<br>&emsp; + Chuẩn bị môi trường và cấu hình Eclipse IDE<br>&emsp; + Tạo và kiểm tra AWS Lambda Function tại môi trường cục bộ<br>&emsp; + Tải Lambda Function lên AWS Lambda<br>&emsp; + Cấu hình S3 Trigger để gọi Lambda khi có file được upload<br>&emsp; + Cập nhật Lambda để tạo thumbnail cho file image/jpeg<br>&emsp; + Xóa các file không phải hình ảnh<br>&emsp; + Tạo gói triển khai và tự động hóa bằng AWS CLI<br>&emsp; + Triển khai Lambda ImageManager<br>&emsp; + Tự động hóa Serverless Microservice bằng AWS SAM và CloudFormation<br>&emsp; + Tạo nhánh mới và triển khai lại thông qua CI/CD Pipeline<br>&emsp; + Tạo DynamoDB Table<br>&emsp; + Thêm Global Secondary Index<br>&emsp; + Tự động hóa Microservice<br>&emsp; + Tạo API cho Microservice<br>&emsp; + Cập nhật IAM Policy và triển khai thông qua Pipeline<br>&emsp; + Tạo Workflow với AWS Step Functions<br>&emsp; + Tạo Lambda Microservice cho Calculator Workflow<br>&emsp; + Mở rộng Calculation Workflow | 20/05/2026   | 20/04/2026      | <https://000052.awsstudygroup.com/vi/> <br><br> <https://000053.awsstudygroup.com/vi/> |
| 5   | - Tìm hiểu Microservice Messaging và Eventing<br>- Tìm hiểu Tạo và chứng thực Single Page Application (SPA)<br>- **Thực hành:**<br>&emsp; + Chuẩn bị môi trường và cấu hình AWS CLI<br>&emsp; + Triển khai Web trên Amazon S3<br>&emsp; + Thực hành SQS Publisher tới SQS Subscriber<br>&emsp; + Thực hành SQS Publisher tới nhiều SQS Subscriber<br>&emsp; + Thực hành SQS Publisher tới SQS Subscriber với FIFO Queue<br>&emsp; + Thực hành SNS Publisher tới nhiều SQS Subscribers<br>&emsp; + Thực hành Kinesis Publisher tới SQS Subscriber<br>&emsp; + Thực hành MQTT Publisher tới MQTT Subscriber<br>&emsp; + Tạo Kinesis Producer<br>&emsp; + Gửi bản ghi vào Kinesis<br>&emsp; + Kiểm tra dữ liệu trong Elasticsearch<br>&emsp; + Khám phá Kibana để xem dữ liệu<br>&emsp; + Tạo DynamoDB Table cho SPA<br>&emsp; + Xây dựng và triển khai Serverless Microservice thủ công<br>&emsp; + Tạo và cung cấp API với Amazon API Gateway<br>&emsp; + Triển khai API với CodeStar và CI/CD<br>&emsp; + Thiết lập trang SPA<br>&emsp; + Tạo Client để sử dụng API<br>&emsp; + Thêm xác thực vào SPA bằng Amazon Cognito User Pools<br>&emsp; + Thiết lập xác thực cho Microservice<br>&emsp; + Đăng ký và đăng nhập người dùng<br>&emsp; + Theo dõi hiệu năng ứng dụng với AWS X-Ray | 21/05/2026   | 21/05/2026      | <https://000054.awsstudygroup.com/vi/> <br><br> <https://000055.awsstudygroup.com/vi/> |
| 6   | - Tìm hiểu Trải nghiệm các dịch vụ AI trên AWS<br>- Tổng hợp chuỗi nội dung chuyển đổi Monolith sang Microservices<br>- **Thực hành:**<br>&emsp; + Chuẩn bị môi trường sử dụng Amazon Polly<br>&emsp; + Khám phá Amazon Polly & Tạo speech/speech marks bằng AWS CLI & Java SDK<br>&emsp; + Chuẩn bị môi trường sử dụng Amazon Rekognition<br>&emsp; + Phát hiện đối tượng & Nhận diện khuôn mặt bằng Amazon Rekognition<br>&emsp; + Thử nghiệm ứng dụng tìm người<br>&emsp; + Triển khai ứng dụng TravelBuddy tích hợp Amazon Lex<br>&emsp; + Tạo & Nâng cấp Lex Chat Bot cho TravelBuddy<br>&emsp; + Tạo Lambda Handler cho Lex Bot & Cập nhật kết nối dịch vụ<br>&emsp; + Phát hành Lex Chat Bot & Tổng hợp kiến trúc toàn hệ thống | 22/05/2026   | 22/05/2026      | <https://000056.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 5:

#### 1. Tìm hiểu Amazon EC2 Resource Optimization
* Hiểu được mục tiêu tối ưu hóa hạ tầng (Right-sizing) nhằm lựa chọn kích thước EC2 phù hợp, tránh lãng phí tài nguyên và cắt giảm chi phí vận hành.
* Nắm vững cơ chế cài đặt CloudWatch Agent để thu thập thêm các chỉ số hệ thống chuyên sâu (chỉ số Memory/RAM) vốn không có sẵn ở mức giám sát cơ bản.
* **Thực hành tối ưu hạ tầng:** Cấu hình IAM Role gắn kết vào EC2, triển khai Agent thành công và khai thác các đề xuất tối ưu hóa tài nguyên thông minh từ công cụ AWS Compute Optimizer.

#### 2. Phân tích chi phí với AWS Cost Explorer
* Làm chủ giao diện trực quan hóa chi phí để theo dõi và bóc tách dữ liệu chi tiêu chi tiết theo từng dịch vụ, theo tài khoản thành viên hoặc theo dòng sản phẩm.
* Nắm được phương pháp phân tích sâu về phạm vi bao phủ cũng như hiệu quả tận dụng của các gói Savings Plans và Reserved Instance (RI).
* Xây dựng thành công các bộ báo cáo EC2 tùy chỉnh để theo dõi độ co giãn, phát hiện các điểm bất thường về chi phí và hiểu rõ cấu trúc tính phí truyền dữ liệu (Data Transfer) trong các kiến trúc Cloud phổ biến.

#### 3. Phân tích chi phí nâng cao với AWS Glue và Amazon Athena
* Hiểu phương pháp xây dựng một nền tảng phân tích báo cáo chi phí (Cost and Usage Report - CUR) quy mô lớn.
* **Thực hành xử lý dữ liệu lớn:** Sử dụng AWS Glue để quét cấu trúc dữ liệu, tự động xây dựng cơ sở dữ liệu và Data Catalog tập trung; tích hợp dịch vụ Amazon Athena để thực thi các câu lệnh truy vấn SQL trực tiếp trên kho log, phục vụ công tác bóc tách Cost Allocation theo Tags và Usage.

#### 4. Dịch chuyển ứng dụng Monolith (Mạch DevAx TravelBuddy)
* Hiểu rõ cấu trúc và các điểm hạn chế của kiến trúc ứng dụng Monolith TravelBuddy (JSP/Java Servlet chạy trên nền Database tập trung).
* **Thực hành dịch chuyển hạ tầng:** Triển khai hạ tầng qua CloudFormation Stack, cấu hình cài đặt Database, build thử nghiệm mã nguồn cục bộ qua Eclipse IDE và thực hiện deploy ứng dụng Monolith lên môi trường AWS Elastic Beanstalk để kiểm thử kết quả gọi API.

#### 5. Tự động phát hành ứng dụng (CI/CD với CodeStar & CodeDeploy)
* Hiểu cách tự động hóa quy trình cập nhật mã nguồn cho ứng dụng Monolith.
* **Thực hành thiết lập CI/CD:** Khởi tạo dự án AWS CodeStar kết nối chuỗi công cụ Git CodeCommit, CodeBuild và CodePipeline giúp đồng bộ tự động mã nguồn từ Eclipse lên Elastic Beanstalk; đồng thời thực hành cấu hình CodeDeploy Application chạy Agent để tự động hóa triển khai các Windows Service lên máy chủ EC2 an toàn qua S3 Artifact.

#### 6. Tách một phần Monolith thành AWS Lambda Microservice
* Nắm được tư duy phân tách kiến trúc, cô lập các tính năng xử lý nặng từ Monolith chuyển dịch sang mô hình Serverless Microservice hướng sự kiện.
* **Thực hành lập trình Serverless:** Viết mã nguồn Lambda Function trên Eclipse IDE, cấu hình S3 PutObject Trigger để tự động kích hoạt xử lý tệp tin khi có sự kiện upload, thực hiện logic tự động tạo ảnh thu nhỏ (thumbnail) cho định dạng `image/jpeg` và lọc bỏ các tệp tin sai định dạng một cách tự động.

#### 7. Tự động hóa quản lý Serverless với AWS SAM (Serverless Application Model)
* Hiểu cách sử dụng AWS SAM làm framework mã nguồn mở để định nghĩa và quản lý hạ tầng không máy chủ dưới dạng mã (IaC).
* **Thực hành CI/CD cho Lambda:** Sử dụng công cụ dòng lệnh AWS CLI đóng gói mã nguồn, viết template mô tả tài nguyên (Lambda, S3 Trigger, Bucket) và thực hiện cấu hình CodeStar tự động phát hành ứng dụng lại thông qua nhánh code mới.

#### 8. Cơ cấu lại dữ liệu (Refactor sang NoSQL với Amazon DynamoDB)
* Thấu hiểu triết lý thiết kế cơ sở dữ liệu phân tán khi chuyển đổi từ Monolith sang Microservices theo mô hình Polyglot Persistence (lựa chọn kho lưu trữ tối ưu theo mô hình truy cập dữ liệu).
* **Thực hành thiết kế NoSQL:** Khởi tạo bảng dữ liệu trên Amazon DynamoDB, cấu hình tối ưu hóa truy vấn nâng cao bằng Global Secondary Index (GSI) để tăng tốc độ quét dữ liệu Trip Sector và cập nhật API Gateway / IAM Policy thông qua Pipeline phát hành tự động.

#### 9. Điều phối chuỗi Workflow với AWS Step Functions
* Hiểu được tầm quan trọng của dịch vụ Step Functions trong việc thiết kế và quản lý các trạng thái hoạt động (State Machine) để điều phối chuỗi xử lý phức tạp của nhiều microservices.
* **Thực hành xây dựng Workflow:** Thiết kế luồng xử lý Calculator Workflow tự động liên kết và gọi liên tiếp các hàm Lambda Microservice xử lý logic, nâng cao tính trực quan và khả năng chịu lỗi cho kiến trúc Serverless.

#### 10. Xây dựng Microservice Messaging và Eventing (SQS, SNS, Kinesis, MQTT)
* Làm chủ 4 mô hình truyền tin cốt lõi phục vụ cơ chế giao tiếp bất đồng bộ, giúp giảm thiểu độ phụ thuộc (decoupling) giữa các hệ thống Microservices:
  * **Amazon SQS:** Thực hành truyền tin dạng hàng đợi Point-to-Point (Publisher sang Subscriber) bao gồm cả hàng đợi chuẩn và hàng đợi đảm bảo thứ tự FIFO Queue.
  * **Amazon SNS:** Triển khai mô hình truyền tin dạng Pub/Sub (Phát tán thông điệp từ một Publisher đến nhiều SQS Subscriber đồng thời).
  * **Amazon Kinesis:** Thực hành xử lý luồng dữ liệu (Data Streaming) thời gian thực quy mô lớn thông qua Kinesis Producer.
  * **MQTT:** Thực hành truyền tin gọn nhẹ hướng sự kiện chuẩn IoT.
* **Tích hợp phân tích Log tập trung:** Thiết lập đưa luồng dữ liệu Kinesis đổ vào Elasticsearch và sử dụng công cụ Kibana để trực quan hóa, khám phá dữ liệu logs.

#### 11. Xây dựng Kiến trúc Single Page Application (SPA) trên Cloud
* Hiểu cách tổ chức mô hình frontend tách biệt hoàn toàn với backend API trong các kiến trúc ứng dụng hiện đại.
* **Thực hành deploy Front-End:** Triển khai mã nguồn giao diện trang web tĩnh của ứng dụng SPA chạy trực tiếp trên kho lưu trữ cấu hình bảo mật của Amazon S3 Bucket.

#### 12. Cung cấp Backend API thông qua Amazon API Gateway
* Nắm vững kiến thức về API Gateway đóng vai trò làm cổng bảo mật vòng ngoài đón nhận toàn bộ request từ Client điều hướng vào các Serverless Microservices phía sau.
* **Thực hành cấu hình API:** Khởi tạo DynamoDB Table lưu trữ, xây dựng thủ công các endpoint API và tích hợp triển khai tự động chuỗi API thông qua CodeStar Pipeline.

#### 13. Xác thực bảo mật nâng cao cho SPA bằng Amazon Cognito
* Nắm chắc bộ quy chuẩn an ninh AAA (Authentication, Authorization, Accounting) cho ứng dụng đám mây.
* **Thực hành tích hợp bảo mật:** Cấu hình Amazon Cognito User Pools làm hệ thống quản lý định danh người dùng tập trung, thiết lập xác thực Token-based bảo vệ cho cụm API Gateway Backend, thực hiện kiểm thử quy trình Đăng ký/Đăng nhập người dùng mới và tích hợp dịch vụ AWS X-Ray để theo dõi, phân tích hiệu năng cuộc gọi.

#### 14. Ứng dụng dịch vụ AI chuyên sâu chuyển đổi văn bản (Amazon Polly)
* Hiểu cách thức hoạt động của dịch vụ Trí tuệ nhân tạo Amazon Polly giúp chuyển đổi văn bản thô thành giọng nói tự nhiên chất lượng cao.
* **Thực hành tích hợp Polly:** Sử dụng AWS CLI và Java SDK để trích xuất dữ liệu âm thanh (speech) kết hợp Speech Marks (nhãn đánh dấu mốc thời gian) nhằm đồng bộ chính xác âm thanh với văn bản hoặc hình ảnh chuyển động trong ứng dụng.

#### 15. Khai phá sức mạnh thị giác máy tính và Chatbot (Amazon Rekognition & Lex)
* Nắm rõ năng lực xử lý hình ảnh nâng cao của Amazon Rekognition và giải pháp xây dựng hội thoại thông minh của Amazon Lex.
* **Thực hành triển khai ứng dụng AI hoàn chỉnh:**
  * Sử dụng Rekognition để phát hiện đối tượng, phân tích và nhận diện khuôn mặt phục vụ bài toán tìm kiếm người dùng thực tế.
  * Triển khai hoàn chỉnh Lex Chat Bot tích hợp trực tiếp vào giao diện TravelBuddy, lập trình hàm Lambda Handler xử lý logic hội thoại phía sau và phát hành thành công ứng dụng tương tác bằng ngôn ngữ tự nhiên.