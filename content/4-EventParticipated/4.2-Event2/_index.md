---
title: " Event 2 "
date: 2026-06-06
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---
# Summary Report: "FCAJ Community Day (June 6)"
### Purpose of the Event
The FCAJ Community Day (June 6) event was organized to share practical technological knowledge, spanning from containerization, application security, cloud game servers to AI, GraphRAG, and career orientation within the infrastructure domain.
The main objectives of the event included:
* Helping attendees better understand Docker and how to package applications for consistent deployment across environments.
* Introducing how to combine AWS WAF with Machine Learning to detect and respond to anomalous attack behaviors.
* Sharing deployment models for multiplayer game servers on cloud platforms.
* Providing methods for effective teamwork in real-world project environments.
* Introducing the GraphRAG approach utilizing AWS Neptune to construct a Graph Knowledge Base.
* Orienting the career progression path from an IT Helpdesk position to a Senior System Administrator.

### List of Speakers & Topics
* **Bao Huynh** - Topic: Docker - A containerization technology
* **Le Hoang Gia Dai** - Topic: Combining AWS WAF with Machine Learning for Cyber Attack Detection
* **Nguyen Quốc Bao** - Topic: Multiplayer in the Cloud: Connecting Godot Clients with AWS
* **Truong Phuoc** - Topic: Effective Teamwork Methods
* **Viet Phat** - Topic: AWS Neptune for Building a Graph Knowledge Base for GraphRAG
* **Vinh Tran** - Topic: From IT Helpdesk to Senior Sysadmin: A Journey of Self-Learning and Transition Roadmap

### Key Highlights of the Presentations

#### 1. Docker - A containerization technology - Speaker: Bao Huynh
The presentation helped attendees clearly understand the differences between virtual machines and containers. While a virtual machine requires a separate operating system for each environment, a container shares the operating system kernel, making it lighter, faster to boot up, and easier to deploy.
The speaker also presented core components of Docker such as the Docker Engine, Dockerfile, Docker Image, and Docker Container. Additionally, the Docker Compose section helped me understand how to run multiple services like frontends, backends, and databases within the same configuration environment.
This content is highly practical because Docker minimizes environment discrepancy errors between local machines, test environments, and production.

#### 2. Combining AWS WAF with Machine Learning for Cyber Attack Detection - Speaker: Le Hoang Gia Dai
The presentation focused on web application security challenges. The speaker pointed out that traditional WAF systems relying on fixed rules could struggle when facing new attack vectors or continuously changing anomalous behaviors.
The introduced solution is combining AWS WAF, Kinesis Data Firehose, Amazon S3, AWS Lambda, and Machine Learning models to analyze access logs. Upon detecting anomalies, the system can automatically update the IP blocklist on AWS WAF.
Through this topic, I learned more about building proactive security systems instead of merely reacting manually after incidents occur.

#### 3. Multiplayer in the Cloud: Connecting Godot Clients with AWS - Speaker: Nguyen Quoc Bao
The presentation introduced how to deploy multiplayer games on the cloud. The content focused on critical challenges such as latency, state synchronization between players, and maintaining real-time connectivity between game clients and servers.
The speaker presented how to utilize the Godot Engine to connect with servers via protocols like UDP, TCP, or WebSockets. Concurrently, the talk touched upon deploying dedicated game servers using AWS services like Amazon GameLift, Amazon ECS, or AWS App Runner.
The demo portion helped me better visualize how an action from a client is sent to the server and synchronized back to other clients.

#### 4. Effective Teamwork Methods - Speaker: Truong Phuoc
This content focused on factors that help a team work more effectively, including clear common goals, transparent communication, trust, and appropriate division of responsibilities.
The speaker shared how to apply Agile/Scrum in projects, including activities like Daily Standups, Sprint Planning, and Retrospectives. Furthermore, tools like Jira, Trello, Slack, Discord, Git, and GitHub were mentioned as crucial supporting utilities in the team coordination process.
My takeaway is that teamwork is not just about breaking down tasks, but also about communicating properly, providing constructive feedback, and resolving mâu thuẫn in a positive manner.

#### 5. AWS Neptune for Building a Graph Knowledge Base for GraphRAG - Speaker: Viet Phat
The presentation introduced the limitations of traditional RAG when relying solely on vector databases. For queries requiring multi-step reasoning or containing deep relationships between entities, traditional RAG might not be effective enough.
The GraphRAG solution combines semantic search with graph databases. AWS Neptune is utilized to store entities and relationships in the form of a Graph Knowledge Base. Through query languages like Gremlin or openCypher, the system can retrieve a richer context.
This content helped me realize that organizing knowledge properly can significantly improve the answer quality of AI systems.

#### 6. From IT Helpdesk to Senior Sysadmin - Speaker: Vinh Tran
This sharing session provided highly practical career orientation. The speaker analyzed the differences between an IT Helpdesk role and a System Administrator. While a Helpdesk mostly handles end-user incidents, a Sysadmin requires a mindset for governance, automation, design, and infrastructure optimization.
The suggested roadmap included skill groups such as computer networking, Linux/Windows Server operating systems, scripting with Bash, PowerShell, or Python, cloud computing, and Infrastructure as Code using Terraform.
The speaker also emphasized the importance of building a Home Lab to practice and accumulate real-world experience.

### Key Takeaways

#### Regarding Technical Knowledge & New Technologies
* Better understood containerization and the reasons why Docker is widely used in modern application deployment.
* Grasped how to use Dockerfiles and Docker Compose to standardize development environments.
* Understood how AWS WAF can combine with log streaming and Machine Learning to detect anomalous attacks.
* Acquired further knowledge on cloud game server architectures and requirements regarding latency and state synchronization.
* Understood the role of AWS Neptune in building a Graph Knowledge Base for GraphRAG.
* Learned how GraphRAG supports complex queries requiring multi-step reasoning.

#### Regarding Teamwork Skills
* Better understood how to organize teams according to Agile/Scrum.
* Learned how to utilize tools like Jira, Trello, and Git to manage tasks more effectively.
* Recognized that clear communication and positive feedback are crucial elements in teamwork.
* Learned to view conflicts as opportunities for improvement rather than just negative issues.

#### Regarding Personal Development Orientation
* Gained a realistic view of the career progression path from IT Helpdesk to Senior Sysadmin.
* Identified the need to build a solid foundation in networking, operating systems, automation, and cloud.
* Understood the importance of practicing through Home Labs and learning via real-world projects.
* Acquired more motivation to refine skills in scripting, Linux, and Infrastructure as Code.

### Professional Applications
* **Applying Docker:** Use Dockerfiles and Docker Compose to package demo applications, making local execution and deployment more convenient.
* **Improving System Security:** Research further into log analysis and combining AWS WAF with anomaly detection mechanisms.
* **Optimizing Teamwork:** Apply task division, progress tracking, and clear code reviews when working in teams.
* **Researching GraphRAG:** Continue exploring AWS Neptune and data representation in graph formats to support AI use cases.
* **Structuring a Self-Study Roadmap:** Plan to study Linux Administration, Python automation, and cloud infrastructure.

### Overall Event Experience
The event brought me a diverse range of knowledge, from application deployment foundations with Docker, security with AWS WAF, cloud game servers to GraphRAG and infrastructure career orientation.
The point that impressed me was that all presentations were tied to real-world scenarios. Concepts like Docker Compose, WAF combined with Machine Learning, or Graph Knowledge Bases were not just explained theoretically but were linked to specific deployment challenges.
Apart from technical knowledge, the insights on teamwork and career roadmaps also helped me clearly identify skills that need improvement during my internship.

### Lessons Learned
1. Docker is an important tool that standardizes environments and reduces deployment errors.
2. Modern security requires a combination of rules, logs, automation, and behavioral analysis.
3. For complex AI challenges, the way data is organized plays a very important role.
4. Effective teamwork requires workflows, tools, and clear communication.
5. Career development in the infrastructure field demands persistence, regular practice, and a specific learning roadmap.
### Some Photos from the Event
![Event2](../../images/event2.png)