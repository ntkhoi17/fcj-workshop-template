---
title: "Worklog Tuần 3"
date: 04-05-2026
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---


### Mục tiêu tuần 3:

* Tìm hiểu cách quản lý dịch vụ, vận hành máy chủ và tự động hóa tác vụ trên AWS thông qua AWS Systems Manager, Patch Manager, Run Command và Session Manager.
* Nắm được cách khởi tạo hạ tầng dưới dạng mã bằng AWS CloudFormation, bao gồm template cơ bản, stack, tài nguyên tùy chỉnh và kiểm tra thay đổi hạ tầng.
* Tìm hiểu các cơ chế quản lý định danh và giới hạn quyền truy cập nâng cao bằng AWS IAM Identity Center, IAM Permission Boundary và IAM Role Condition.
* Làm quen với các dịch vụ bảo mật, mã hóa và bảo vệ ứng dụng như AWS Security Hub, AWS WAF, AWS KMS và AWS Backup.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2   | - Tìm hiểu Quản lý dịch vụ và tự động hóa tác vụ sử dụng AWS Systems Manager<br>- Tìm hiểu làm việc với AWS Systems Manager - Session Manager<br>- **Thực hành:**<br>&emsp; + Tạo VPC và Subnet phục vụ môi trường Systems Manager<br>&emsp; + Tạo Public Windows EC2 Instance<br>&emsp; + Tạo và gán IAM Role cho EC2 Instance<br>&emsp; + Kiểm tra Managed Nodes trong Fleet Manager<br>&emsp; + Sử dụng Patch Manager để scan và cài đặt bản vá<br>&emsp; + Sử dụng Run Command để chạy lệnh trên nhiều máy chủ<br>&emsp; + Kết nối Public EC2 và Private EC2 bằng Session Manager<br>&emsp; + Cấu hình lưu session logs vào Amazon S3<br>&emsp; + Thực hành Port Forwarding để truy cập Private Windows Instance | 04/05/2026   | 04/05/2026      | <https://000031.awsstudygroup.com/vi/> <br><br> <https://000058.awsstudygroup.com/vi/> |
| 3   | - Tìm hiểu Khởi tạo hạ tầng dưới dạng Code với AWS CloudFormation<br>- **Thực hành:**<br>&emsp; + Tạo IAM User và IAM Role phục vụ CloudFormation<br>&emsp; + Tạo Workspace để viết template<br>&emsp; + Tạo CloudFormation Template cơ bản<br>&emsp; + Kiểm tra template trước khi triển khai<br>&emsp; + Khởi chạy CloudFormation Stack bằng AWS CLI<br>&emsp; + Tìm hiểu CloudFormation nâng cao<br>&emsp; + Tạo Lambda Function làm tài nguyên tùy chỉnh<br>&emsp; + Tìm hiểu Mapping, StackSets và Drift Detection | 05/05/2026   | 05/05/2026      | <https://000037.awsstudygroup.com/vi/> |
| 4   | - Tìm hiểu Thiết lập Single Sign-On cho Organization bằng AWS IAM Identity Center<br>- Tìm hiểu Giới hạn Quyền của User với IAM Permission Boundary<br>- Tìm hiểu Giới hạn chuyển Role theo Condition<br>- **Thực hành:**<br>&emsp; + Tạo AWS Account trong AWS Organizations<br>&emsp; + Tạo User và Group trong IAM Identity Center<br>&emsp; + Tạo Permission Set và gán quyền truy cập theo Group<br>&emsp; + Kiểm tra quyền truy cập qua AWS Access Portal<br>&emsp; + Cấu hình AWS CLI sử dụng IAM Identity Center<br>&emsp; + Tạo Permission Set có điều kiện truy cập theo thời gian<br>&emsp; + Tạo Policy giới hạn quyền tối đa bằng Permission Boundary<br>&emsp; + Tạo IAM User bị giới hạn quyền theo Region<br>&emsp; + Kiểm tra quyền EC2 ở Region được phép và Region bị giới hạn<br>&emsp; + Tạo IAM Group, IAM User và Admin IAM Role<br>&emsp; + Cấu hình Switch Role<br>&emsp; + Giới hạn Assume Role theo địa chỉ IP và thời gian | 06/05/2026   | 06/05/2026      | <https://000012.awsstudygroup.com/vi/> <br><br> <https://000030.awsstudygroup.com/vi/> <br><br> <https://000044.awsstudygroup.com/vi/> |
| 5   | - Tìm hiểu Kiểm tra đánh giá tiêu chuẩn bảo mật với AWS Security Hub<br>- Tìm hiểu Bảo mật Ứng dụng và API với Web Application Firewall (AWS WAF)<br>- **Thực hành:**<br>&emsp; + Tìm hiểu các tiêu chuẩn AWS Foundational Security Best Practices, CIS AWS Foundations Benchmark và PCI DSS<br>&emsp; + Kích hoạt AWS Security Hub CSPM<br>&emsp; + Kích hoạt AWS Config phục vụ quá trình đánh giá tuân thủ<br>&emsp; + Xem Security Score theo từng bộ tiêu chuẩn<br>&emsp; + Kiểm tra các phát hiện và rủi ro bảo mật<br>&emsp; + Tạo S3 Bucket phục vụ lab AWS WAF<br>&emsp; + Triển khai ứng dụng mẫu<br>&emsp; + Tạo Web ACL với Managed Rules<br>&emsp; + Tạo Custom Rule và Custom Rule nâng cao<br>&emsp; + Kiểm thử Rule mới<br>&emsp; + Cấu hình ghi nhật ký request | 07/05/2026   | 07/05/2026      | <https://000018.awsstudygroup.com/vi/> <br><br> <https://000026.awsstudygroup.com/vi/> |
| 6   | - Tìm hiểu Quản lý Khóa với dịch vụ AWS Key Management Service (AWS KMS)<br>- Tìm hiểu Triển khai kế hoạch sao lưu hệ thống với AWS Backup<br>- **Thực hành:**<br>&emsp; + Tạo Policy và Role phục vụ AWS KMS<br>&emsp; + Tạo Group và User để kiểm tra quyền truy cập dữ liệu mã hóa<br>&emsp; + Tạo Customer Managed Key trên AWS KMS<br>&emsp; + Cấu hình Key Administrator và Key Usage Permission<br>&emsp; + Tạo S3 Bucket và upload dữ liệu lên S3<br>&emsp; + Mã hóa dữ liệu S3 bằng AWS KMS<br>&emsp; + Tạo AWS CloudTrail để ghi nhận hoạt động trong tài khoản<br>&emsp; + Tạo Amazon Athena để truy vấn log lưu trên S3<br>&emsp; + Kiểm thử quyền truy cập dữ liệu mã hóa<br>&emsp; + Tạo Presigned URL để chia sẻ dữ liệu trong thời gian giới hạn<br>&emsp; + Tạo Backup Plan cho hệ thống<br>&emsp; + Tạo Backup Vault và Backup Rule<br>&emsp; + Gán tài nguyên vào Backup Plan bằng Tag<br>&emsp; + Thiết lập thông báo backup qua Amazon SNS<br>&emsp; + Kiểm tra hoạt động sao lưu và khôi phục dữ liệu | 08/05/2026   | 08/05/2026      | <https://000033.awsstudygroup.com/vi/> <br><br> <https://000013.awsstudygroup.com/vi/> |

### Kết quả đạt được tuần 3:

#### 1. Tìm hiểu AWS Systems Manager
* Hiểu vai trò của AWS Systems Manager trong việc quản lý tập trung tài nguyên AWS.
* Nắm được cách Systems Manager hỗ trợ theo dõi hoạt động, thay đổi cấu hình, cảnh báo, compliance và trạng thái phần mềm.
* Hiểu cách gom nhóm tài nguyên để quản lý theo ứng dụng, môi trường production hoặc development.
* Làm quen với Fleet Manager, Managed Nodes, Patch Manager và Run Command.

#### 2. Thực hành quản lý máy chủ bằng AWS Systems Manager
* Tạo VPC và Subnet cho môi trường thực hành.
* Tạo Public Windows EC2 Instance.
* Tạo IAM Role cho EC2 Instance.
* Gán IAM Role để Instance có thể làm việc với Systems Manager.
* Kiểm tra EC2 Instance xuất hiện trong danh sách Managed Nodes.
* Mở terminal session đến các Windows EC2 Instance thông qua Fleet Manager.

#### 3. Tìm hiểu và thực hành Patch Manager
* Hiểu Patch Manager dùng để kiểm tra và cài đặt bản vá cho máy chủ.
* Thực hiện Patch now trên các Windows EC2 Instance.
* Chọn Patch operation là Scan and install.
* Chọn reboot option phù hợp trong quá trình cập nhật.
* Kiểm tra kết quả patch sau khi hoàn tất.

#### 4. Tìm hiểu và thực hành Run Command
* Hiểu Run Command cho phép chạy lệnh đồng loạt trên nhiều máy chủ.
* Sử dụng document AWS-RunPowerShellScript.
* Chạy lệnh kiểm tra người dùng trên Windows EC2 Instance.
* Chọn nhiều Instance làm target.
* Cấu hình lưu output command vào Amazon S3.
* Kiểm tra kết quả chạy lệnh và lỗi phát sinh nếu có.

#### 5. Tìm hiểu AWS Systems Manager Session Manager
* Hiểu Session Manager hỗ trợ kết nối đến máy chủ EC2 mà không cần mở trực tiếp cổng SSH hoặc RDP ra Internet.
* Nắm được cách kết nối đến Public EC2 Instance và Private EC2 Instance trong VPC.
* Hiểu vai trò của VPC Endpoint trong việc kết nối đến EC2 Private Instance.
* Làm quen với các endpoint ssm, ssmmessages và ec2messages.

#### 6. Thực hành kết nối EC2 bằng Session Manager
* Tạo VPC.
* Tạo Public Subnet và Private Subnet.
* Tạo Security Group.
* Tạo Public Linux EC2 Instance.
* Tạo Private Windows EC2 Instance.
* Tạo IAM Role cho Session Manager.
* Kích hoạt DNS hostnames cho VPC.
* Tạo VPC Endpoint phục vụ kết nối đến Private Instance.
* Kết nối thành công đến EC2 Private Instance thông qua Session Manager.

#### 7. Tìm hiểu quản lý Session Logs & Port Forwarding
* Hiểu Session history chỉ hiển thị lịch sử phiên kết nối nhưng chưa hiển thị chi tiết câu lệnh.
* Nắm được cách lưu trữ session logs vào Amazon S3 và vai trò của S3 Gateway Endpoint trong quá trình ghi log phiên làm việc.
* Hiểu nguyên lý Port Forwarding dùng để chuyển hướng lưu lượng từ máy trạm đến Instance trong Private Subnet.
* **Thực hành chuyển tiếp cổng:** Cấu hình AWS CLI và cài đặt Session Manager Plugin, chạy lệnh với document `AWS-StartPortForwardingSession` để RDP từ Private Windows Instance về localhost thành công.

#### 8. Tìm hiểu AWS CloudFormation
* Hiểu CloudFormation là dịch vụ hỗ trợ mô tả và khởi tạo tài nguyên hạ tầng bằng mã (Infrastructure as Code - IaC).
* Nắm được cách sử dụng template để triển khai tài nguyên AWS tự động, nhất quán giữa nhiều Region hoặc nhiều tài khoản và làm quen với khái niệm Stack, Template, Resource.
* **Thực hành khởi tạo hạ tầng:** Tạo Workspace, tạo và kiểm tra CloudFormation Template cơ bản trước khi khởi chạy Stack bằng AWS CLI.
* **Nghiên cứu tính năng nâng cao:** Tạo Lambda Function làm tài nguyên tùy chỉnh (Custom Resource), tìm hiểu cơ chế Mapping để ánh xạ giá trị, StackSets và cơ chế phát hiện sai lệch hạ tầng Drift Detection.

#### 9. Tìm hiểu AWS IAM Identity Center (AWS Single Sign-On)
* Nắm được cách quản lý định danh và phân quyền tập trung cho nhân viên trong tổ chức thuộc AWS Organizations dựa trên Group Membership và Permission Set.
* **Thực hành thiết lập định danh:** Tạo tài khoản, User, Group và Permission Set trong IAM Identity Center để kiểm tra quyền truy cập thành công qua AWS Access Portal.
* **Tích hợp CLI và Time-based Access Control:** Cấu hình AWS CLI xác thực thông qua trình duyệt bằng lệnh `aws configure sso` và tạo Permission Set sử dụng Inline Policy giới hạn thời gian truy cập tạm thời để giảm rủi ro bảo mật.

#### 10. Tìm hiểu IAM Permission Boundary & Condition
* Hiểu Permission Boundary là cơ chế giới hạn quyền tối đa của IAM User/Group nhằm ngăn chặn rủi ro leo thang đặc quyền.
* **Thực hành giới hạn quyền:** Tạo Policy giới hạn quản trị EC2 trong Region `ap-southeast-1`, gán quyền admin cho tài khoản thử nghiệm kết hợp Permission Boundary để kiểm tra lỗi truy cập khi tài khoản chuyển sang Region khác.
* **Giới hạn Switch Role:** Tạo chuỗi IAM Group, IAM User và Admin IAM Role nhằm thực hiện cấu hình Switch Role có kèm Condition ràng buộc chặt chẽ theo dải địa chỉ IP và mốc thời gian cụ thể.

#### 11. Tìm hiểu AWS Security Hub
* Hiểu cách Security Hub cung cấp cái nhìn tổng quan về cảnh báo bảo mật, trạng thái tuân thủ và tổng hợp phát hiện rủi ro từ các dịch vụ như GuardDuty, Inspector và Macie.
* Làm quen với các tiêu chuẩn AWS Foundational Security Best Practices, CIS AWS Foundations Benchmark và PCI DSS.
* **Thực hành cấu hình CSPM:** Kích hoạt Security Hub CSPM trên Console, đồng bộ kích hoạt AWS Config phục vụ quá trình đánh giá tự động và kiểm tra chi tiết bảng Security Score của hệ thống.

#### 12. Tìm hiểu AWS Web Application Firewall (AWS WAF)
* Hiểu vai trò của AWS WAF trong việc ngăn chặn các request độc hại tấn công vào ứng dụng web và API thông qua các bộ luật Web ACL, Managed Rules và Custom Rules.
* **Thực hành bảo vệ ứng dụng:** Khởi tạo S3 Bucket, deploy ứng dụng mẫu, thiết lập Web ACL kết hợp các Custom Rule nâng cao và cấu hình ghi nhật ký (logging) request để phục vụ công tác phân tích an ninh.

#### 13. Tìm hiểu AWS Key Management Service (AWS KMS)
* Hiểu cơ chế tạo, xoay vòng tự động và quản lý khóa mã hóa bất đối xứng/đối xứng (Symmetric Customer Managed Key) nhằm bảo vệ dữ liệu ở trạng thái lưu trữ (data-at-rest).
* **Thực hành quản lý khóa:** Phân định rõ quyền giữa Key Administrator và Key Usage Permission, khởi tạo S3 Bucket và thực hiện cấu hình mã hóa toàn vẹn dữ liệu S3 Objects bằng AWS KMS.

#### 14. Ứng dụng AWS CloudTrail, Amazon Athena và Chia sẻ dữ liệu mã hóa
* Nắm được cách CloudTrail ghi lại nhật ký hoạt động API và cách sử dụng Amazon Athena để truy vấn log trực tiếp trên S3 bằng ngôn ngữ SQL.
* **Thực hành kiểm thử an ninh dữ liệu:** Xác thực phân quyền giải mã khóa KMS đối với từng nhóm User và thực hiện tạo Presigned URL để chia sẻ dữ liệu an toàn trong một khoảng thời gian giới hạn được chỉ định.

#### 15. Tìm hiểu AWS Backup
* Hiểu vai trò của AWS Backup trong việc tập trung và tự động hóa chính sách bảo vệ dữ liệu (EBS, RDS, DynamoDB, EFS) đáp ứng các chỉ số mục tiêu khôi phục RTO và RPO.
* **Thực hành lập lịch sao lưu:** Khởi tạo Backup Plan, thiết lập Backup Rule (lịch hằng ngày), tạo Backup Vault, gán tài nguyên bằng thẻ Tag và liên kết Amazon SNS để tự động hóa gửi thông báo trạng thái `BACKUP_JOB_COMPLETED`/`RESTORE_JOB_COMPLETED` qua AWS CLI.
* **Kiểm tra phục hồi:** Tiến hành kiểm thử hoạt động khôi phục dữ liệu từ bản sao lưu để đảm bảo tính sẵn sàng và toàn vẹn của hệ thống khi có sự cố xảy ra.