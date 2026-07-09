---
title: "Worklog Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---



### Mục tiêu tuần 11:

* Cấu hình người dùng quản trị đầu tiên trên Amazon Cognito và kiểm thử toàn diện cơ chế xác thực JWT.
* Kiểm thử hiệu năng và tính đúng đắn của các endpoint backend quan trọng như **/me**, **/upload-intents**, **/documents** cùng các API liên quan đến tài liệu.
* Xác minh luồng upload tài liệu end-to-end từ frontend/API đến QuarantineBucket, cơ chế quét của GuardDuty, kho lưu trữ DocumentsBucket và Database DynamoDB.
* Khởi chạy React frontend trên môi trường local và kiểm thử các cấu phần giao diện cốt lõi: đăng nhập, tải tài liệu, chia sẻ, quản lý người dùng, audit log và analytics.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2   | - Tạo người dùng Admin đầu tiên trong Amazon Cognito<br>- Tìm hiểu luồng xác thực **USER_PASSWORD_AUTH**<br>- **Thực hành:**<br>&emsp; + Tạo user **admin@yourcompany.com** trong Cognito User Pool qua AWS Console<br>&emsp; + Thiết lập mật khẩu tạm thời (Temporary Password) cho user quản trị<br>&emsp; + Thêm user vào nhóm đặc quyền tối cao SYSTEM_ADMIN<br>&emsp; + Nghiên cứu cấu trúc câu lệnh khởi tạo user bằng AWS CLI<br>&emsp; + Thực hiện cuộc gọi xác thực đến Cognito, trích xuất chuỗi **AccessToken** | 29/06/2026   | 29/06/2026      |  |
| 3   | - Kiểm thử endpoint **/me** và các bộ API metadata cơ bản của tài khoản<br>- **Thực hành:**<br>&emsp; + Thực hiện cuộc gọi (Request) tới endpoint **/me** đính kèm Bearer Token<br>&emsp; + Kiểm tra cấu trúc dữ liệu trả về gồm: **userId**, **email**, **name** và **groups**<br>&emsp; + Xác minh API Gateway giải mã và chứng thực JWT token thành công<br>&emsp; + Truy vết log thực thi trong CloudWatch Logs của Lambda **me**<br>&emsp; + Phân tích, ghi nhận các mã lỗi hệ thống khi token sai hoặc hết hạn | 30/06/2026   | 30/06/2026      |  |
| 4   | - Kiểm thử tích hợp luồng upload tài liệu bảo mật sử dụng Presigned URL<br>- **Thực hành:**<br>&emsp; + Gọi API **/upload-intents** lấy dữ liệu **uploadIntentId** và Presigned PUT URL<br>&emsp; + Tiến hành upload trực tiếp file **report.pdf** lên S3 QuarantineBucket qua URL<br>&emsp; + Giám sát tiến trình GuardDuty Malware Protection tự động kích hoạt quét file<br>&emsp; + Kiểm tra nhãn tag an ninh trên S3, xác minh file sạch được đẩy sang DocumentsBucket<br>&emsp; + Rà soát DynamoDB kiểm tra bản ghi và trạng thái READY của tài liệu | 01/07/2026   | 01/07/2026      |  |
| 5   | - Kiểm thử hệ thống API liệt kê danh mục tài liệu và các tính năng tương tác core<br>- **Thực hành:**<br>&emsp; + Thực thi cuộc gọi API **/documents** bằng AccessToken để trích xuất danh sách file<br>&emsp; + Đối chiếu thông tin **documentId**, **filename**, **versionNumber** với DynamoDB<br>&emsp; + Kiểm thử API lấy chi tiết tài liệu và API trích xuất audit events của file<br>&emsp; + Gọi Intent Lambda sinh Presigned Download URL để kiểm tra tải file bảo mật | 02/07/2026   | 02/07/2026      |  |
| 6   | - Khởi chạy frontend React trên môi trường local và kiểm thử tương tác giao diện<br>- **Thực hành:**<br>&emsp; + Cài đặt gói thư viện phụ thuộc bằng npm trong thư mục frontend<br>&emsp; + Khởi chạy ứng dụng web local (Vite Server) thông qua lệnh **npm run dev**<br>&emsp; + Ánh xạ các thông số **UserPoolId**, **UserPoolClientId** và **ApiUrl** từ CDK Outputs<br>&emsp; + Kiểm thử các tính năng: Đăng nhập Admin, tải/download file, chia sẻ quyền truy cập, duyệt phòng ban, tra cứu audit log và hiển thị dashboard phân tích | 03/07/2026   | 03/07/2026      |  |

### Kết quả đạt được tuần 11:

#### 1. Khởi tạo và thiết lập tài khoản quản trị tối cao đầu tiên
* Thấu hiểu triết lý an ninh hệ thống: Việc tắt tính năng tự đăng ký tự do (Self-signup) là bắt buộc đối với hệ thống quản trị dữ liệu doanh nghiệp nhằm ngăn chặn triệt để nguy cơ thâm nhập trái phép.
* Thực hiện tạo lập thành công tài khoản quản trị gốc **admin@yourcompany.com** trong Cognito User Pool, cấu hình mật khẩu tạm thời và gán định danh trực tiếp vào nhóm đặc quyền **SYSTEM_ADMIN** phục vụ cho toàn bộ tiến trình kiểm thử end-to-end.

#### 2. Nghiên cứu cơ chế xác thực Token-Based với Amazon Cognito
* Làm chủ luồng xác thực **USER_PASSWORD_AUTH** để chứng thực tài khoản mật mã trực tiếp với dịch vụ định danh của AWS.
* Trích xuất thành công chuỗi mã hóa bảo mật **AccessToken** từ kết quả phản hồi của Cognito, hiểu rõ vai trò của JWT (JSON Web Token) đóng vai trò làm mã thông báo Bearer Token đính kèm trong Header để vượt qua lớp lá chắn Cognito Authorizer trên API Gateway.

#### 3. Xác minh tính toàn vẹn của Endpoint API **/me**
* Thực hiện gọi thành công API **/me**, xác nhận API Gateway chặn lọc, giải mã token chính xác và chuyển tiếp ngữ cảnh định danh (User Context) xuống cho tầng tính toán xử lý.
* Kiểm tra cấu trúc dữ liệu JSON trả về, đảm bảo hiển thị tường minh các trường thông tin: **userId**, **email**, **name** và kiểm tra khớp chuỗi phân quyền nhóm **SYSTEM_ADMIN** tại thời điểm runtime.

#### 4. Khai thác CloudWatch Logs phục vụ Troubleshooting API
* Định vị chính xác Log Group chuyên biệt của Lambda Function trên bảng quản trị CloudWatch.
* Đọc hiểu, phân tích sâu các dòng log sinh ra theo thời gian thực (Runtime Logs) khi frontend thực hiện cuộc gọi API, làm chủ kỹ năng rà soát và xử lý các lỗi hệ thống thường gặp như thiếu Token (401 Unauthorized), Token sai cấu trúc hoặc Token quá hạn truy cập (Expired Token).

#### 5. Kiểm thử chuỗi luồng xử lý Upload Intent độc lập
* Gửi thành công yêu cầu khởi tạo ý định tải tệp tin (Upload Intent) thông qua phương thức **POST** tới endpoint **/upload-intents** kèm các tham số file (**filename**, **contentType**, **size**).
* Trích xuất thành công dữ liệu phản hồi từ Backend Lambda bao gồm một chuỗi khóa định danh **uploadIntentId** tạm thời và một đường dẫn liên kết nâng cao **Presigned PUT URL** có cấu hình thời gian hết hạn nghiêm ngặt.

#### 6. Thử nghiệm cơ chế truyền tải tệp tin bảo mật tốc độ cao
* Thực hiện truyền tải trực tiếp tệp tin dữ liệu **report.pdf** từ Client lên hạ tầng đám mây S3 bằng đường dẫn Presigned PUT URL.
* Xác nhận luồng đi của tệp tin lớn chạy độc lập, hoàn toàn không đi xuyên qua cổng API Gateway hay tầng tính toán Lambda, chứng minh tính ưu việt của kiến trúc trong việc tối ưu hóa băng thông hạ tầng mạng và loại bỏ hoàn toàn rào cản giới hạn kích thước payload (10MB) của API Gateway.

#### 7. Giám sát luồng rà soát mã độc tự động thời gian thực của GuardDuty
* Xác minh tính năng GuardDuty Malware Protection tự động kích hoạt lập tức ngay khi tệp tin đổ vào vùng đệm cách ly **QuarantineBucket**.
* Kiểm tra siêu dữ liệu Object Metadata trên Console, xác nhận hệ thống tự động gán nhãn tag đánh giá an ninh chính xác: hiển thị nhãn trạng thái **CLEAN** đối với tệp tin an toàn và gắn nhãn nguy hiểm **THREAT_FOUND** khi mô phỏng tải lên tệp tin dính mã độc thử nghiệm.

#### 8. Kiểm toán tiến trình xử lý hậu kiểm dịch tệp tin (Post-Scan Processing)
* Xác minh luồng sự kiện bất đồng bộ hoạt động chính xác: Sự kiện gán nhãn tag từ GuardDuty kích hoạt trục định tuyến EventBridge gọi trực tiếp hàm xử lý core **Upload Processor Function**.
* Kiểm chứng hàm processor tự động đọc tag, thực hiện di chuyển an toàn file sạch sang kho lưu trữ tập trung **DocumentsBucket**, đồng thời khởi tạo bản ghi metadata, ghi nhận phiên bản (**versionNumber**) và cập nhật trạng thái thực thể thành **READY** trong bảng DynamoDB single-table.

#### 9. Kiểm thử hệ thống API quản lý và phân quyền trích xuất tài liệu
* Gọi thành công API **/documents** bằng AccessToken để kiểm tra năng lực truy vấn dữ liệu của Lambda theo phân tầng bảo mật.
* Xác thực dữ liệu danh mục tệp tin trả về hiển thị chuẩn xác cấu trúc: **documentId**, **filename**, **versionNumber** và mốc thời gian hệ thống **timestamp**, đảm bảo dữ liệu hiển thị đồng bộ 100% với các thực thể lưu trữ thực tế trong bảng DynamoDB.
* Kiểm thử thông suốt hai luồng API phụ trợ cao cấp: API truy xuất chi tiết thuộc tính tài liệu (Document Details) và API kết xuất lịch sử chuỗi sự kiện audit (Document Audit Events).

#### 10. Xác minh quy trình tải xuống bảo mật (Secure Download Flow)
* Thực hiện gọi API yêu cầu tải tệp tin, kích hoạt hàm Lambda **download-intents** kiểm tra phân quyền người dùng và trả về một chuỗi liên kết động **Presigned GET URL** có giới hạn thời gian thực thi ngắn.
* Tiến hành tải tệp tin thành công từ kho lưu trữ kín **DocumentsBucket** thông qua URL vừa nhận, chứng minh kiến trúc bảo vệ dữ liệu an toàn, chặn đứng hoàn toàn nguy cơ truy cập trực tiếp hoặc dò đoán đường link S3 Object từ bên ngoài Internet.

#### 11. Triển khai và cấu hình môi trường Frontend cục bộ
* Thực hiện cài đặt thành công toàn bộ các module thư viện giao diện React SPA thông qua trình quản lý gói npm tại thư mục frontend.
* Kích hoạt máy chủ phát triển cục bộ Vite Server chạy mượt mà thông qua câu lệnh **npm run dev**, khởi chạy giao diện ứng dụng thành công tại cổng port mặc định **http://localhost:5173**.
* Thực hiện liên kết thông suốt hệ thống Front-End với hạ tầng Cloud Backend bằng cách ánh xạ chính xác bộ ba tham số trích xuất từ CDK Outputs bao gồm: **UserPoolId**, **UserPoolClientId** và đường dẫn gốc **ApiUrl**.

#### 12. Kiểm tra toàn diện kịch bản nghiệm thu tính năng hệ thống (End-to-End Testing)
* Sử dụng tài khoản Admin đăng nhập thành công vào giao diện, thực hiện kiểm thử trơn tru, không phát sinh lỗi đối với chuỗi kịch bản tính năng nghiệp vụ thực tế bao gồm:
  * Duyệt danh mục tài liệu, thực hiện tải lên file mới và tải xuống file bảo mật.
  * Thiết lập cấu hình chia sẻ tài liệu (Sharing Link) và thực thi phê duyệt cấp quyền phân phối file.
  * Vận hành không gian quản trị người dùng (User Management) với quyền System Admin và duyệt sơ đồ phòng ban (Department Management) với quyền Department Admin.
  * Tra cứu nhật ký hoạt động hệ thống append-only và trực quan hóa biểu đồ dữ liệu trên Dashboard phân tích hệ thống.

