---
title: " Event 2 "
date: 2026-06-06
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---
# Bài thu hoạch: "FCAJ Community Day (6 Tháng 6)"
### Mục Đích Của Sự Kiện
Sự kiện FCAJ Community Day (6 Tháng 6) được tổ chức nhằm chia sẻ các kiến thức công nghệ thực tế, từ containerization, bảo mật ứng dụng, game server trên cloud cho đến AI, GraphRAG và định hướng phát triển nghề nghiệp trong lĩnh vực hệ thống.
Các mục tiêu chính của sự kiện gồm:
* Giúp người tham dự hiểu rõ hơn về Docker và cách đóng gói ứng dụng để triển khai nhất quán giữa các môi trường.
* Giới thiệu cách kết hợp AWS WAF với Machine Learning để phát hiện và phản ứng với các hành vi tấn công bất thường.
* Chia sẻ mô hình triển khai multiplayer game server trên nền tảng cloud.
* Cung cấp phương pháp làm việc nhóm hiệu quả trong môi trường dự án thực tế.
* Giới thiệu hướng tiếp cận GraphRAG sử dụng AWS Neptune để xây dựng Graph Knowledge Base.
* Định hướng lộ trình phát triển nghề nghiệp từ IT Helpdesk lên Senior System Administrator.

### Danh Sách Diễn Giả & Đề Tài
* **Bảo Huỳnh** - Đề tài: Docker - A containerization technology
* **Lê Hoàng Gia Đại** - Đề tài: Combining AWS WAF with Machine Learning for Cyber Attack Detection
* **Nguyễn Quốc Bảo** - Đề tài: Multiplayer in the Cloud: Connecting Godot Clients with AWS
* **Trương Phước** - Đề tài: Cách làm việc nhóm hiệu quả
* **Việt Phát** - Đề tài: AWS Neptune for Building a Graph Knowledge Base for GraphRAG
* **Vinh Trần** - Đề tài: Từ IT Helpdesk lên Senior Sysadmin: Hành trình tự học và Lộ trình dịch chuyển

### Nội Dung Nổi Bật Của Các Bài Tham Luận

#### 1. Docker - A containerization technology - Diễn giả: Bảo Huỳnh
Bài chia sẻ giúp người tham dự hiểu rõ sự khác biệt giữa virtual machine và container. Nếu máy ảo cần một hệ điều hành riêng cho từng môi trường, container lại chia sẻ kernel của hệ điều hành, nhờ đó nhẹ hơn, khởi động nhanh hơn và dễ triển khai hơn.
Diễn giả cũng trình bày các thành phần quan trọng của Docker như Docker Engine, Dockerfile, Docker Image và Docker Container. Ngoài ra, phần Docker Compose giúp mình hiểu cách chạy nhiều dịch vụ như frontend, backend và database trong cùng một môi trường cấu hình.
Nội dung này rất thực tế vì Docker giúp giảm lỗi khác biệt môi trường giữa máy cá nhân, môi trường test và production.

#### 2. Combining AWS WAF with Machine Learning for Cyber Attack Detection - Diễn giả: Lê Hoàng Gia Đại
Phần trình bày tập trung vào bài toán bảo mật ứng dụng web. Diễn giả chỉ ra rằng các hệ thống WAF truyền thống dựa trên rule cố định có thể gặp khó khăn khi đối mặt với các dạng tấn công mới hoặc các hành vi bất thường thay đổi liên tục.
Giải pháp được giới thiệu là kết hợp AWS WAF, Kinesis Data Firehose, Amazon S3, AWS Lambda và mô hình Machine Learning để phân tích log truy cập. Khi phát hiện dấu hiệu bất thường, hệ thống có thể tự động cập nhật danh sách IP cần chặn trên AWS WAF.
Qua nội dung này, mình hiểu thêm cách xây dựng hệ thống bảo mật chủ động thay vì chỉ phản ứng thủ công khi sự cố đã xảy ra.

#### 3. Multiplayer in the Cloud: Connecting Godot Clients with AWS - Diễn giả: Nguyễn Quốc Bảo
Bài tham luận giới thiệu cách triển khai game nhiều người chơi trên cloud. Nội dung tập trung vào các vấn đề quan trọng như độ trễ, đồng bộ trạng thái giữa các người chơi và cách duy trì kết nối thời gian thực giữa game client và server.
Diễn giả trình bày cách sử dụng Godot Engine để kết nối với server thông qua các giao thức như UDP, TCP hoặc WebSocket. Đồng thời, bài chia sẻ cũng đề cập đến việc triển khai dedicated game server bằng các dịch vụ AWS như Amazon GameLift, Amazon ECS hoặc AWS App Runner.
Phần demo giúp mình hình dung rõ hơn cách một hành động từ client được gửi lên server và đồng bộ lại cho các client khác.

#### 4. Cách làm việc nhóm hiệu quả - Diễn giả: Trương Phước
Nội dung này tập trung vào các yếu tố giúp một nhóm làm việc hiệu quả hơn, bao gồm mục tiêu chung rõ ràng, giao tiếp minh bạch, sự tin tưởng và phân chia trách nhiệm hợp lý.
Diễn giả chia sẻ cách áp dụng Agile/Scrum trong dự án, bao gồm các hoạt động như Daily Standup, Sprint Planning và Retrospective. Bên cạnh đó, các công cụ như Jira, Trello, Slack, Discord, Git và GitHub cũng được đề cập như những công cụ hỗ trợ quan trọng trong quá trình phối hợp nhóm.
Điểm mình rút ra là làm việc nhóm không chỉ là chia task, mà còn cần giao tiếp đúng cách, phản hồi mang tính xây dựng và xử lý mâu thuẫn một cách tích cực.

#### 5. AWS Neptune for Building a Graph Knowledge Base for GraphRAG - Diễn giả: Việt Phát
Bài trình bày giới thiệu hạn chế của RAG truyền thống khi chỉ dựa vào vector database. Với những câu hỏi cần suy luận nhiều bước hoặc có nhiều mối quan hệ giữa các thực thể, RAG truyền thống có thể chưa đủ hiệu quả.
Giải pháp GraphRAG kết hợp tìm kiếm ngữ nghĩa với cơ sở dữ liệu đồ thị. AWS Neptune được sử dụng để lưu trữ các thực thể và mối quan hệ dưới dạng Graph Knowledge Base. Thông qua các ngôn ngữ truy vấn như Gremlin hoặc openCypher, hệ thống có thể truy xuất ngữ cảnh phong phú hơn.
Nội dung này giúp mình hiểu rằng việc tổ chức tri thức đúng cách có thể cải thiện đáng kể chất lượng câu trả lời của các hệ thống AI.

#### 6. Từ IT Helpdesk lên Senior Sysadmin - Diễn giả: Vinh Trần
Phần chia sẻ này mang tính định hướng nghề nghiệp rất thực tế. Diễn giả phân tích sự khác biệt giữa IT Helpdesk và System Administrator. Nếu Helpdesk chủ yếu xử lý sự cố người dùng, Sysadmin cần có tư duy quản trị, tự động hóa, thiết kế và tối ưu hạ tầng.
Lộ trình được gợi ý bao gồm các nhóm kỹ năng như mạng máy tính, hệ điều hành Linux/Windows Server, scripting với Bash, PowerShell hoặc Python, cloud computing và Infrastructure as Code bằng Terraform.
Diễn giả cũng nhấn mạnh tầm quan trọng của việc tự xây dựng Home Lab để thực hành và tích lũy kinh nghiệm thực tế.

### Những Gì Học Được

#### Về Kỹ Thuật & Công Nghệ
* Hiểu rõ hơn về containerization và lý do Docker được sử dụng phổ biến trong triển khai ứng dụng hiện đại.
* Nắm được cách sử dụng Dockerfile và Docker Compose để chuẩn hóa môi trường phát triển.
* Hiểu cách AWS WAF có thể kết hợp với log streaming và Machine Learning để phát hiện tấn công bất thường.
* Có thêm kiến thức về kiến trúc game server trên cloud và các yêu cầu về độ trễ, đồng bộ trạng thái.
* Hiểu được vai trò của AWS Neptune trong việc xây dựng Graph Knowledge Base cho GraphRAG.
* Biết thêm cách GraphRAG hỗ trợ các câu hỏi phức tạp cần suy luận nhiều bước.

#### Về Kỹ Năng Làm Việc Nhóm
* Hiểu hơn về cách tổ chức nhóm theo Agile/Scrum.
* Biết cách sử dụng các công cụ như Jira, Trello và Git để quản lý công việc hiệu quả hơn.
* Nhận thấy giao tiếp rõ ràng và phản hồi tích cực là yếu tố quan trọng khi làm việc nhóm.
* Học được cách nhìn nhận xung đột như một cơ hội để cải thiện thay vì chỉ là vấn đề tiêu cực.

#### Về Định Hướng Phát Triển Bản Thân
* Có thêm cái nhìn thực tế về lộ trình phát triển từ IT Helpdesk đến Senior Sysadmin.
* Biết cần xây dựng nền tảng vững về mạng, hệ điều hành, tự động hóa và cloud.
* Hiểu tầm quan trọng của việc thực hành qua Home Lab và học thông qua dự án thực tế.
* Có thêm động lực để rèn luyện kỹ năng scripting, Linux và Infrastructure as Code.

### Ứng Dụng Vào Công Việc
* **Áp dụng Docker:** Sử dụng Dockerfile và Docker Compose để đóng gói các ứng dụng demo, giúp việc chạy thử và triển khai thuận tiện hơn.
* **Cải thiện bảo mật hệ thống:** Tìm hiểu thêm cách phân tích log và kết hợp AWS WAF với các cơ chế phát hiện bất thường.
* **Tối ưu teamwork:** Áp dụng cách chia task, theo dõi tiến độ và review code rõ ràng hơn khi làm việc nhóm.
* **Nghiên cứu GraphRAG:** Tiếp tục tìm hiểu AWS Neptune và cách biểu diễn dữ liệu dưới dạng graph để hỗ trợ các bài toán AI.
* **Xây dựng lộ trình tự học:** Lên kế hoạch học thêm Linux Administration, Python automation và cloud infrastructure.

### Trải Nghiệm Trong Event
Sự kiện mang lại cho mình nhiều kiến thức đa dạng, từ nền tảng triển khai ứng dụng với Docker, bảo mật với AWS WAF, game server trên cloud cho đến GraphRAG và định hướng nghề nghiệp hệ thống.
Điểm mình ấn tượng là các bài chia sẻ đều gắn với tình huống thực tế. Những khái niệm như Docker Compose, WAF kết hợp Machine Learning hay Graph Knowledge Base không chỉ được giải thích lý thuyết mà còn được liên hệ với các bài toán triển khai cụ thể.
Ngoài kiến thức kỹ thuật, phần chia sẻ về làm việc nhóm và lộ trình nghề nghiệp cũng giúp mình nhìn rõ hơn những kỹ năng cần cải thiện trong thời gian thực tập.

### Bài Học Rút Ra
1. Docker là công cụ quan trọng giúp chuẩn hóa môi trường và giảm lỗi khi triển khai ứng dụng.
2. Bảo mật hiện đại cần kết hợp giữa rule, log, automation và phân tích hành vi.
3. Với các bài toán AI phức tạp, cách tổ chức dữ liệu có vai trò rất quan trọng.
4. Làm việc nhóm hiệu quả cần quy trình, công cụ và giao tiếp rõ ràng.
5. Phát triển nghề nghiệp trong lĩnh vực hệ thống cần sự kiên trì, thực hành đều đặn và lộ trình học tập cụ thể.
