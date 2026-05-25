# AWS Certified Cloud Practitioner — Practice Test #6
# AWS 雲端從業人員認證 — 練習測驗 #6 中英對照

---

## Q1
**A company provides you with a completed product that is run and managed by the company itself. As a customer, you only use the product without worrying about maintaining or managing the product. Which cloud computing model does this kind of product belong to?**

一家公司提供給你一個由該公司自行運行和管理的完整產品。作為客戶，你只需使用該產品，無需擔心維護或管理。這種產品屬於哪種雲端運算模型？

- Product as a Service (Paas)／產品即服務
- Infrastructure as a Service (IaaS)／基礎設施即服務
- Platform as a Service (PaaS)／平台即服務
- ✅ **Software as a Service (SaaS) ／軟體即服務**

---

## Q2
**As part of a flexible pricing model, AWS offers two types of Savings Plans. Which of the following are the Savings Plans from AWS?**

作為彈性定價模型的一部分，AWS 提供兩種 Savings Plans。以下哪項是 AWS 的 Savings Plans？

- Compute Savings Plans, Storage Savings Plans／運算節省計畫、儲存節省計畫
- Reserved Instances (RI) Savings Plans, EC2 Instance Savings Plans／預留執行個體節省計畫、EC2 執行個體節省計畫
- Instance Savings Plans, Storage Savings Plans／執行個體節省計畫、儲存節省計畫
- ✅ **Compute Savings Plans, EC2 Instance Savings Plans／運算節省計畫、EC2 執行個體節省計畫**

---

## Q3
**A company is looking for ways to make its desktop applications available to the employees from browsers on their devices/laptops. Which AWS service will help achieve this requirement without having to procure servers or maintain infrastructure?**

一家公司希望讓員工能透過裝置/筆電的瀏覽器存取桌面應用程式。哪項 AWS 服務可在無需採購伺服器或維護基礎設施的情況下實現此需求？

- Amazon WorkSpaces
- AWS Outposts
- AWS Snowball
- ✅ **Amazon AppStream 2.0**

---

## Q4
**Which of the following points have to be considered when choosing an AWS Region for a service? (Select two)**

選擇 AWS 區域時，需考慮以下哪些因素？（選兩項）

- The AWS Region with high availability index should be considered for your business／應選擇高可用性指數的 AWS 區域
- The AWS Region should have 5G networks／AWS 區域應具備 5G 網路
- The AWS Region chosen should have all its AZs within 100 Kms radius／所選區域的所有 AZ 應在 100 公里半徑內
- ✅ **Compliance and Data Residency guidelines of the AWS Region should match your business requirements／AWS 區域的合規及資料駐留規定應符合業務需求**
- ✅ **AWS Region chosen should be geographically closer to the user base／所選 AWS 區域應在地理位置上靠近使用者群**

---

## Q5
**A company is planning to move their traditional CRM application running on MySQL to an AWS database service. Which database service is the right fit for this requirement?**

一家公司計畫將其運行在 MySQL 上的傳統 CRM 應用程式遷移至 AWS 資料庫服務。哪項資料庫服務最適合此需求？

- Amazon DynamoDB
- Amazon ElastiCache
- Amazon Neptune
- ✅ **Amazon Aurora**

---

## Q6
**A team manager needs data about the changes that have taken place for AWS resources in his account during the past two weeks. Which AWS service can help get this data?**

一位團隊經理需要了解其帳戶中 AWS 資源在過去兩週內所發生的變更資料。哪項 AWS 服務可提供此資料？

- Amazon CloudWatch
- AWS CloudTrail
- Amazon Inspector
- ✅ **AWS Config**

---

## Q7
**Which of the following services/tools offers a user-friendly graphical user interface to manage AWS Snowball devices without a need for command-line interface or REST APIs?**

以下哪項服務/工具提供友善的圖形使用者介面，無需命令列或 REST API 即可管理 AWS Snowball 裝置？

- AppStream 2.0
- AWS Config
- AWS Transfer Family
- ✅ **AWS OpsHub**

---

## Q8
**An e-commerce company needs to generate custom reports and graphs every week for analyzing the product sales data. The company is looking at a tool/service that will help them analyze this data using interactive dashboards with minimal effort. The dashboards also need to be accessible from any device. Which AWS tool/service will you recommend for this use-case?**

一家電商公司每週需要生成自訂報表和圖表來分析產品銷售資料，希望以最少的工作量透過互動式儀表板分析資料，且儀表板需可從任何裝置存取。你推薦哪項 AWS 工具/服務？

- Amazon SageMaker
- Amazon Athena
- AWS Glue
- ✅ **Amazon QuickSight**

---

## Q9
**A company is looking at real-time processing of streaming big data for their ad-tech platform. Which of the following AWS services is the right choice for this requirement?**

一家公司希望對其廣告技術平台的串流大數據進行即時處理。以下哪項 AWS 服務最適合此需求？

- Amazon Redshift
- Amazon Simple Queue Service (Amazon SQS)
- Amazon EMR
- ✅ **Amazon Kinesis Data Streams**

---

## Q10
**Which AWS service is used to store and commit code privately and also offer features for version control?**

哪項 AWS 服務用於私密地儲存和提交程式碼，並提供版本控制功能？

- AWS CodePipeline
- AWS CodeBuild
- AWS CodeStar
- ✅ **AWS CodeCommit**

---

## Q11
**Which of the following statements are true about AWS Regions and Availability Zones (AZ)? (Select two)**

以下哪些關於 AWS 區域和可用區（AZ）的陳述是正確的？（選兩項）

- AWS calls each group of logical data centers as AWS Regions／AWS 將每組邏輯資料中心稱為 AWS 區域
- Traffic between AZs is not encrypted by default, but can be configured／AZ 之間的流量預設未加密，但可設定
- An AZ is a physical location where AWS clusters the data centers／AZ 是 AWS 集群資料中心的實體位置
- ✅ **Each AWS Region consists of multiple, isolated, and physically separate AZs within a geographic area／每個 AWS 區域由地理區域內多個隔離且實體分開的 AZ 組成**
- ✅ **All traffic between Availability Zones (AZ) is encrypted／所有 AZ 之間的流量均已加密**

---

## Q12
**Which of the following data sources are used by Amazon Detective to analyze events and identify potential security issues?**

Amazon Detective 使用以下哪些資料來源來分析事件並識別潛在安全問題？

- Amazon CloudWatch Logs, Amazon VPC Flow Logs and Amazon GuardDuty findings
- Amazon CloudWatch Logs, AWS CloudTrail logs and Amazon S3 Access Logs
- Amazon CloudWatch Logs, AWS CloudTrail logs and Amazon Inspector logs
- ✅ **AWS CloudTrail logs, Amazon VPC Flow Logs, and Amazon GuardDuty findings／AWS CloudTrail 日誌、Amazon VPC 流量日誌和 Amazon GuardDuty 調查結果**

---

## Q13
**Which of the following statements are correct regarding the AWS Shared Responsibility Model? (Select two)**

以下哪些關於 AWS 共同責任模型的陳述是正確的？（選兩項）

- For abstracted services such as Amazon S3, AWS operates encryption options and appropriate permissions for accessing S3 resources／對於 S3 等抽象化服務，AWS 負責加密選項及存取 S3 資源的適當權限
- AWS maintains the configuration of its infrastructure devices and is responsible for configuring the guest operating systems, databases, and applications／AWS 負責設定訪客作業系統、資料庫和應用程式
- Amazon EC2 is categorized as IaaS and hence AWS will perform all of the necessary security configuration and management tasks／EC2 屬於 IaaS，因此 AWS 負責所有安全設定和管理工作
- ✅ **AWS trains AWS employees, but a customer must train their own employees／AWS 訓練 AWS 員工，但客戶必須訓練自己的員工**
- ✅ **AWS is responsible for patching and fixing flaws within the infrastructure, but customers are responsible for patching their guest OS and applications／AWS 負責修補基礎設施缺陷，但客戶負責修補其訪客作業系統和應用程式**

---

## Q14
**Which of the below services are encrypted by default and need no user intervention to enable encryption?**

以下哪些服務預設已加密，無需使用者介入即可啟用加密？

- Amazon CloudWatch logs, Application Load Balancer (ALB), Amazon S3 Glacier
- AWS Storage Gateway, Application Load Balancer (ALB), Amazon CloudFront
- AWS Organizations, Amazon EC2, AWS CloudTrail Logs
- ✅ **AWS CloudTrail Logs, Amazon S3 Glacier, AWS Storage Gateway**

---

## Q15
**An e-commerce company has its on-premises data storage on an NFS file system that is accessed in parallel by multiple applications. Which storage service should the company use to move their files to AWS Cloud seamlessly if the application is hosted on Amazon EC2 instances?**

一家電商公司的本地資料儲存在 NFS 檔案系統上，可被多個應用程式並行存取。若應用程式託管於 EC2，應使用哪項儲存服務將檔案無縫遷移至 AWS 雲端？

- Amazon Elastic Block Store (Amazon EBS)
- Amazon Simple Storage Service (Amazon S3)
- AWS Storage Gateway
- ✅ **Amazon Elastic File System (Amazon EFS)**

---

## Q16
**A university provides access to AWS services for its students to submit their research data for analysis. The university is looking at the most cost-effective approach for recovering from disasters and it can tolerate data loss of a few hours. Which disaster recovery strategy is well-suited for this use case?**

一所大學為學生提供 AWS 服務存取以提交研究資料進行分析，正在尋找最具成本效益的災難復原方案，且可承受數小時的資料損失。哪種災難復原策略最適合此使用案例？

- Warm standby strategy／暖備策略
- Multi-site active/active strategy／多站點主動/主動策略
- Pilot light strategy／導引燈策略
- ✅ **Backup and restore strategy／備份與還原策略**

---

## Q17
**An organization in the US plans to launch a new product line and needs additional IT infrastructure to support the workload. They want a solution that enables rapid deployment of resources and minimizes setup time. Which advantages of cloud computing can help the organization achieve this goal? (Select two)**

美國一家機構計畫推出新產品線，需要額外的 IT 基礎設施來支援工作負載，並希望快速部署資源並最小化設定時間。哪些雲端運算優勢可幫助實現此目標？（選兩項）

- Benefit from massive economies of scale／受益於大規模經濟效益
- Trade fixed expense for variable expense／將固定費用轉為可變費用
- Go global in minutes／幾分鐘內實現全球化
- ✅ **Enable automatic scaling of resources based on demand／根據需求自動擴展資源**
- ✅ **Increase speed and agility／提升速度和敏捷性**

---

## Q18
**Which of the following are the security best practices suggested by AWS for IAM? (Select two)**

以下哪些是 AWS 針對 IAM 建議的安全最佳實務？（選兩項）

- Do not change passwords and access keys once created／密碼和存取金鑰一旦建立就不要更改
- Share your AWS account root user credentials only if absolutely necessary／僅在絕對必要時共享根使用者憑證
- Enable MFA on your root user account to give root access to multiple users without sharing credentials／啟用 MFA 讓多個使用者無需共享憑證即可獲得根存取權限
- ✅ **Do not share security credentials between accounts, use IAM roles instead／不要在帳戶之間共享安全憑證，改用 IAM 角色**
- ✅ **When you create IAM policies, grant the least privileges required to perform a task／建立 IAM 政策時，授予執行任務所需的最少權限**

---

## Q19
**Which feature of the AWS Cloud refers to right-sizing the resources?**

AWS 雲端的哪項特性是指對資源進行合理調整（right-sizing）？

- Resiliency／韌性
- Reliability／可靠性
- Horizontal scaling／水平擴展
- ✅ **Elasticity／彈性**

---

## Q20
**Per the AWS Shared Responsibility Model, management of which of the following AWS services is the responsibility of the customer?**

根據 AWS 共同責任模型，以下哪項 AWS 服務的管理是客戶的責任？

- Amazon DynamoDB
- AWS Elastic Beanstalk
- Amazon Simple Storage Service (Amazon S3)
- ✅ **Amazon Elastic Compute Cloud (Amazon EC2)**

---

## Q21
**As part of log analysis, you have realized that one or more AWS-owned IP addresses are being used for port scanning your on-premises server. Which service/team should you connect to resolve this issue?**

在日誌分析過程中，你發現一個或多個 AWS 擁有的 IP 位址正在對你的本地伺服器進行連接埠掃描。你應聯繫哪個服務/團隊來解決此問題？

- Reach out to Werner Vogels, the CTO of Amazon／聯繫 Amazon CTO Werner Vogels
- Use AWS Trusted Advisor to log a complaint／使用 AWS Trusted Advisor 提出投訴
- Contact AWS Support／聯繫 AWS Support
- ✅ **Contact AWS Abuse team／聯繫 AWS 濫用團隊**

---

## Q22
**An organization is looking to break down its AWS spending so that each department and project can be accurately charged for the resources they consume. Which AWS feature or service is the best fit for this use-case?**

一家機構希望細分其 AWS 支出，以便每個部門和專案能夠準確地為其消耗的資源計費。哪項 AWS 功能或服務最適合此使用案例？

- AWS Cost and Usage Report (CUR)
- AWS Marketplace
- AWS Budgets
- ✅ **AWS cost allocation tags／AWS 成本分配標籤**

---

## Q23
**A company wants to establish a private, dedicated connection between AWS and its on-premises data center. Which AWS service is the right choice for this requirement?**

一家公司希望在 AWS 和其本地資料中心之間建立私有的專用連接。哪項 AWS 服務是正確選擇？

- Amazon CloudFront
- AWS Site-to-Site VPN
- Amazon API Gateway
- ✅ **AWS Direct Connect**

---

## Q24
**Which of the following is the least effort way to encrypt data for AWS services only in your AWS account using AWS KMS?**

使用 AWS KMS 為 AWS 帳戶中的 AWS 服務加密資料，以下哪種方式最省力？

- Create your own customer managed keys (CMKs) in AWS KMS／在 AWS KMS 中建立自己的客戶管理金鑰
- Use AWS owned CMK in the service you wish to use encryption／在要使用加密的服務中使用 AWS 擁有的 CMK
- Use AWS KMS APIs to encrypt data within your own application by using the AWS Encryption SDK／使用 AWS 加密 SDK 透過 KMS API 在應用程式中加密資料
- ✅ **Use AWS managed master keys that are automatically created in your account for each service／使用為每項服務自動在帳戶中建立的 AWS 受管主金鑰**

---

## Q25
**An e-learning company wants to build a knowledge graph by leveraging a fully managed database. Which of the following is the best fit for this requirement?**

一家電子學習公司希望利用全受管資料庫建立知識圖譜。以下哪項最適合此需求？

- Amazon Relational Database Service (Amazon RDS)
- Amazon DynamoDB
- Amazon DocumentDB
- ✅ **Amazon Neptune**

---

## Q26
**Which of the following statements are correct regarding the health monitoring and reporting capabilities supported by AWS Elastic Beanstalk? (Select two)**

以下哪些關於 AWS Elastic Beanstalk 支援的健康監控和報告功能的陳述是正確的？（選兩項）

- AWS Elastic Beanstalk provides only basic health reporting system; Combined with ELB, they provide advanced health check features／Elastic Beanstalk 僅提供基本健康報告系統，與 ELB 結合才提供進階健康檢查功能
- The basic health reporting system does not use health checks performed by ELB／基本健康報告系統不使用 ELB 執行的健康檢查
- In a single instance environment, Elastic Beanstalk determines the instance's health by monitoring the ELB health settings／在單一執行個體環境中，Elastic Beanstalk 透過監控 ELB 健康設定來確定執行個體健康狀況
- ✅ **The Elastic Beanstalk health monitoring can determine that the environment's Auto Scaling group is available and has a minimum of at least one instance／Elastic Beanstalk 健康監控可確定環境的 Auto Scaling 群組可用且至少有一個執行個體**
- ✅ **With basic health reporting, the Elastic Beanstalk service does not publish any metrics to Amazon CloudWatch／使用基本健康報告時，Elastic Beanstalk 不會將任何指標發布至 Amazon CloudWatch**

---

## Q27
**As a Cloud Practitioner, which of the following credentials would you recommend for signing in to the AWS Management Console to meet security best practices? (Select two)**

作為雲端從業人員，你會推薦使用以下哪些憑證登入 AWS 管理主控台以符合安全最佳實務？（選兩項）

- Access Key ID／存取金鑰 ID
- X.509 certificate／X.509 憑證
- Secret Access Key／秘密存取金鑰
- ✅ **IAM Username and password／IAM 使用者名稱和密碼**
- ✅ **Multi Factor Authentication (MFA)／多重要素驗證**

---

## Q28
**Which of the following statements are correct regarding the AWS Support Plans? (Select two)**

以下哪些關於 AWS 支援計畫的陳述是正確的？（選兩項）

- AWS Concierge service is available for the AWS Business Support and AWS Enterprise Support plans／AWS Concierge 服務適用於商業和企業支援計畫
- Infrastructure Event Management is included for free for Business and Enterprise Support plans and can be extended to Developer Support plan for an additional fee／基礎設施事件管理免費包含在商業和企業支援計畫中，可付費延伸至開發人員支援計畫
- Contextual guidance based on customer use-case, is available only for the AWS Enterprise support plan／基於客戶使用案例的情境指導僅適用於企業支援計畫
- ✅ **Both Basic and AWS Developer Support plans have access to the core Trusted Advisor checks only／基本和開發人員支援計畫僅能存取核心 Trusted Advisor 檢查**
- ✅ **A designated Technical Account Manager is available only for AWS Enterprise Support plan／指定技術客戶經理僅適用於 AWS 企業支援計畫**

---

## Q29
**A manufacturing company is looking at a service that can offer AWS infrastructure, AWS services, APIs, and tools to its on-premises data center for running low latency applications. Which of the following service/tool is the best fit for the given requirement?**

一家製造公司希望在其本地資料中心提供 AWS 基礎設施、服務、API 和工具，以運行低延遲應用程式。哪項服務/工具最適合此需求？

- AWS Wavelength
- AWS Snow Family
- AWS Local Zones
- ✅ **AWS Outposts**

---

## Q30
**A blogging company is looking at an easy to use solution to host WordPress blogs. The company needs a cost-effective, readily available solution without the need to manage the configurations for servers or the databases. Which AWS service will help you achieve this functionality?**

一家部落格公司希望找到一個易於使用的解決方案來託管 WordPress 部落格，需要一個具成本效益、隨時可用的解決方案，且無需管理伺服器或資料庫設定。哪項 AWS 服務可實現此功能？

- AWS Fargate
- Amazon Elastic Compute Cloud (EC2) with Amazon S3 for storage
- Host the application directly on Amazon S3
- ✅ **Amazon Lightsail**

---

## Q31
**A healthcare company wants to implement a continuous replication based disaster recovery mechanism and provide fast, reliable recovery of physical, virtual, and cloud-based servers into AWS Cloud. Which of the following represents the best-fit solution for this use case?**

一家醫療公司希望實施基於持續複製的災難復原機制，並提供將實體、虛擬和雲端伺服器快速可靠地恢復到 AWS 雲端的能力。哪項解決方案最適合此使用案例？

- AWS Storage Gateway
- AWS Snowball Edge
- CloudCover Disaster Recovery
- ✅ **CloudEndure Disaster Recovery**

---

## Q32
**A company is looking at a service/tool to automate and minimize the time spent on keeping the server images up-to-date. These server images are used by Amazon EC2 instances as well as the on-premises systems. Which AWS service will help achieve the company's need?**

一家公司希望自動化並最小化保持伺服器映像更新所花費的時間，這些伺服器映像供 EC2 執行個體和本地系統使用。哪項 AWS 服務可滿足此需求？

- Amazon EC2 Amazon Machine Image (AMI)
- AWS CloudFormation templates
- AWS Systems Manager (SSM)
- ✅ **Amazon EC2 Image Builder**

---

## Q33
**AWS Support offers five support plans for its customers. Which of the following features are covered as part of the AWS Basic Support Plan? (Select two)**

AWS Support 為客戶提供五種支援計畫。以下哪些功能包含在 AWS 基本支援計畫中？（選兩項）

- Infrastructure event management／基礎設施事件管理
- Use-case guidance／使用案例指導
- Client-side diagnostic tools／客戶端診斷工具
- ✅ **One-on-one responses to account and billing questions／一對一回答帳戶和帳單問題**
- ✅ **Service health checks／服務健康檢查**

---

## Q34
**Which of the following statements are correct regarding the AWS Control Tower and Service Control Policies? (Select two)**

以下哪些關於 AWS Control Tower 和服務控制政策（SCP）的陳述是正確的？（選兩項）

- SCPs, by default, affect all the users in the AWS Organization. They have to be configured to effect only the member accounts, if needed／SCP 預設影響 AWS 組織中的所有使用者，需設定才能僅影響成員帳戶
- SCPs can help grant permissions to the accounts in your organization／SCP 可以幫助授予組織中帳戶的權限
- AWS Control Tower helps you deploy a multi-account AWS environment and operate it with day-to-day reminders and recommendations／AWS Control Tower 幫助部署多帳戶環境並以每日提醒和建議來運作
- ✅ **AWS Control Tower is an AWS native service providing a pre-defined set of blueprints and guardrails to help customers implement a landing zone for new AWS accounts／AWS Control Tower 是 AWS 原生服務，提供預定義的藍圖和護欄，幫助客戶為新 AWS 帳戶實施登陸區**
- ✅ **Service Control Policies (SCPs) are a type of organization policy that you can use to manage permissions in your organization／SCP 是一種組織政策，可用於管理組織中的權限**

---

## Q35
**Which AWS service allows you to connect any number of IoT devices to the cloud without requiring you to provision or manage servers?**

哪項 AWS 服務允許你將任意數量的 IoT 裝置連接到雲端，而無需佈建或管理伺服器？

- AWS Control Tower
- Amazon Connect
- AWS IoT Gateway
- ✅ **AWS IoT Core**

---

## Q36
**Which tool/service will help you get a forecast of your spending for the next 12 months?**

哪項工具/服務可幫助你獲得未來 12 個月支出的預測？

- AWS Pricing Calculator
- AWS Marketplace
- Consolidated Billing of AWS Organizations
- ✅ **AWS Cost Explorer**

---

## Q37
**Which of the following AWS services is delivered globally rather than regionally?**

以下哪項 AWS 服務是全球性交付而非區域性交付？

- AWS Snowball
- Amazon Elastic File System (Amazon EFS)
- Amazon Simple Storage Service (Amazon S3) buckets
- ✅ **Amazon WorkSpaces**

---

## Q38
**Which of the following AWS services can be used to continuously monitor both malicious activities as well as unauthorized behavior to protect your AWS accounts and workloads?**

以下哪項 AWS 服務可用於持續監控惡意活動和未授權行為，以保護你的 AWS 帳戶和工作負載？

- Amazon Inspector
- AWS Security Hub
- Amazon Detective
- ✅ **Amazon GuardDuty**

---

## Q39
**A gaming company needs compute and storage services close to edge locations in order to ensure ultra-low latency for end-users and devices that connect through mobile networks. Which AWS service is the best fit for this requirement?**

一家遊戲公司需要靠近邊緣位置的運算和儲存服務，以確保透過行動網路連接的終端使用者和裝置的超低延遲。哪項 AWS 服務最適合此需求？

- AWS Snowball Edge
- AWS Snowball
- AWS Outposts
- ✅ **AWS Wavelength**

---

## Q40
**Which pillar of AWS Well-Architected Framework focuses on using IT and computing resources efficiently, while considering the right resource types and sizes based on workload requirements?**

AWS Well-Architected Framework 的哪個支柱著重於有效率地使用 IT 和運算資源，同時根據工作負載需求考慮正確的資源類型和大小？

- Cost Optimization Pillar／成本最佳化支柱
- Reliability Pillar／可靠性支柱
- Operational Excellence Pillar／卓越營運支柱
- ✅ **Performance Efficiency Pillar／效能效率支柱**

---

## Q41
**Which of the following are NoSQL database services from AWS? (Select two)**

以下哪些是 AWS 的 NoSQL 資料庫服務？（選兩項）

- AWS Storage Gateway
- Amazon Aurora
- Amazon Relational Database Service (Amazon RDS)
- ✅ **Amazon DocumentDB**
- ✅ **Amazon Neptune**

---

## Q42
**A financial consulting company is looking for automated reference deployments, that will speed up the process of deploying its financial solutions on AWS Cloud. The reference deployment should be able to deploy most of the well-known functions of financial services and leave space for customizations, if necessary. Which AWS service will help achieve this requirement?**

一家金融諮詢公司正在尋找自動化的參考部署方案，以加速在 AWS 雲端部署金融解決方案的過程，且需能留有自訂空間。哪項 AWS 服務可滿足此需求？

- Amazon QuickSight
- AWS Elastic Beanstalk
- AWS CloudFormation
- ✅ **AWS Partner Solutions (formerly Quick Starts)／AWS 合作夥伴解決方案（前身為 Quick Starts）**

---

## Q43
**A weather-tracking application is built using Amazon DynamoDB. During holidays and travel seasons, the load is high and the read requests consume most of the database resources, increasing overall application latency. Which feature/service will help resolve this issue?**

一個天氣追蹤應用程式使用 Amazon DynamoDB 建構。在假日和旅遊旺季，負載很高，讀取請求消耗大部分資料庫資源，導致應用程式延遲增加。哪項功能/服務可解決此問題？

- Amazon CloudFront
- Amazon DynamoDB Regulator
- Amazon ElastiCache
- ✅ **Amazon DynamoDB Accelerator (DAX)**

---

## Q44
**A media company uses Amazon S3 for storing all its data. Which storage class should it consider for cost-optimal storage of the data that has random access patterns?**

一家媒體公司使用 Amazon S3 儲存所有資料。對於具有隨機存取模式的資料，應考慮哪種儲存類別以實現最優成本儲存？

- Amazon S3 Standard (S3 Standard)
- Amazon S3 Random Access (S3 Random-Access)
- Amazon S3 Standard-Infrequent Access (S3 Standard-IA)
- ✅ **Amazon S3 Intelligent-Tiering (S3 Intelligent-Tiering)**

---

## Q45
**A company is moving its on-premises application to AWS Cloud. The application uses in-memory caches for running custom workloads. Which Amazon EC2 instance type is the right choice for the given requirement?**

一家公司正在將其本地應用程式遷移至 AWS 雲端，該應用程式使用記憶體快取運行自訂工作負載。哪種 EC2 執行個體類型最適合此需求？

- Accelerated computing instance types／加速運算執行個體類型
- Storage Optimized instance types／儲存最佳化執行個體類型
- Compute Optimized instance types／運算最佳化執行個體類型
- ✅ **Memory Optimized instance types／記憶體最佳化執行個體類型**

---

## Q46
**Which of the following represents the correct scenario where an Auto Scaling group's (ASG) predictive scaling can be effectively used to maintain the required number of AWS resources?**

以下哪種情境最適合使用 Auto Scaling 群組的預測性擴展來維持所需的 AWS 資源數量？

- To help configure a CloudWatch SQS metric for scaling the group based on the value of the metric／幫助設定 CloudWatch SQS 指標以根據指標值擴展群組
- To help configure a scaling policy to keep the average aggregate CPU utilization at 40 percent／幫助設定擴展政策使平均 CPU 使用率保持在 40%
- To manage a fixed number of resources in the Auto Scaling group／管理 Auto Scaling 群組中固定數量的資源
- ✅ **To manage a workload that exhibits recurring load patterns that are specific to the day of the week or the time of day／管理具有週期性負載模式（特定於星期幾或一天中某個時段）的工作負載**

---

## Q47
**A Security Group has been changed in an AWS account and the manager of the account has asked you to find out the details of the user who changed it. As a Cloud Practitioner, which AWS service will you use to fetch the necessary information?**

AWS 帳戶中的安全群組被更改，帳戶管理者要求你找出更改者的詳細資訊。作為雲端從業人員，你會使用哪項 AWS 服務獲取必要資訊？

- Amazon Inspector
- AWS X-Ray
- AWS Trusted Advisor
- ✅ **AWS CloudTrail**

---

## Q48
**As an AWS Cloud Practitioner, you have been tasked to find examples of AWS Cloud solution designs. Which service/feature would you recommend?**

作為 AWS 雲端從業人員，你被要求尋找 AWS 雲端解決方案設計範例。你會推薦哪項服務/功能？

- AWS Trusted Advisor
- APN Consulting Partner
- AWS Marketplace
- ✅ **AWS Architecture Center／AWS 架構中心**

---

## Q49
**A company stores all its media files in Amazon S3 which is accessed by an application hosted on Amazon EC2 instances. The company wants to convert these media files into formats that users can playback on mobile devices. Which AWS service/tool helps you achieve this requirement?**

一家公司將所有媒體檔案儲存在 Amazon S3 中，由 EC2 上的應用程式存取。公司希望將這些媒體檔案轉換為使用者可在行動裝置上播放的格式。哪項 AWS 服務/工具可實現此需求？

- Amazon Transcribe
- Amazon Comprehend
- AWS Glue
- ✅ **Amazon Elastic Transcoder**

---

## Q50
**Which of the following AWS services are offered free of cost? (Select two)**

以下哪些 AWS 服務是免費提供的？（選兩項）

- Amazon EC2 Spot Instances／Amazon EC2 Spot 執行個體
- An Elastic IP address, which is chargeable as long as it is associated with an EC2 instance／Elastic IP 位址，只要與 EC2 執行個體關聯就需收費
- Amazon CloudWatch facilitated detailed monitoring of EC2 instances／Amazon CloudWatch 促進的 EC2 執行個體詳細監控
- ✅ **AWS Elastic Beanstalk**
- ✅ **AWS Auto Scaling**

---

## Q51
**Which of the following statements are correct regarding Amazon API Gateway? (Select two)**

以下哪些關於 Amazon API Gateway 的陳述是正確的？（選兩項）

- Amazon API Gateway creates RESTful APIs, Storage Gateway creates WebSocket APIs／API Gateway 建立 RESTful API，Storage Gateway 建立 WebSocket API
- Amazon API Gateway does not yet support API result caching／Amazon API Gateway 尚不支援 API 結果快取
- If an API response is served by the cached data, it is not considered an API call for billing purposes／若 API 回應由快取資料提供，則不計入計費目的的 API 呼叫
- ✅ **Amazon API Gateway can call an AWS Lambda function to create the front door of a serverless application／Amazon API Gateway 可呼叫 Lambda 函數以建立無伺服器應用程式的前門**
- ✅ **API Gateway can be configured to send data directly to Amazon Kinesis Data Stream／API Gateway 可設定為直接將資料傳送至 Amazon Kinesis Data Stream**

---

## Q52
**Which of the following statements are true about AWS Elastic Beanstalk? (Select two)**

以下哪些關於 AWS Elastic Beanstalk 的陳述是正確的？（選兩項）

- AWS Elastic Beanstalk supports web applications built on different languages. But, Elastic Beanstalk cannot be used for deploying non-web applications／Elastic Beanstalk 支援不同語言的 Web 應用程式，但不能用於部署非 Web 應用程式
- AWS Elastic Beanstalk supports Java, .NET, PHP, but does not support Docker web applications／Elastic Beanstalk 支援 Java、.NET、PHP，但不支援 Docker Web 應用程式
- AWS Elastic Beanstalk automates capacity provisioning, load balancing, and application deployment, but auto-scaling functionality cannot be automated／Elastic Beanstalk 自動化容量佈建、負載平衡和應用程式部署，但無法自動化 Auto Scaling
- ✅ **There is no additional charge for AWS Elastic Beanstalk. You pay only for the underlying AWS resources that your application consumes／AWS Elastic Beanstalk 無額外費用，你只需為應用程式消耗的底層 AWS 資源付費**
- ✅ **With AWS Elastic Beanstalk, you can quickly deploy and manage applications in the AWS Cloud without having to learn about the infrastructure that runs those applications／使用 Elastic Beanstalk，你可以快速部署和管理 AWS 雲端中的應用程式，而無需了解運行這些應用程式的基礎設施**

---

## Q53
**Which of the following use-cases can be solved using the Amazon Forecast service?**

以下哪種使用案例可以使用 Amazon Forecast 服務解決？

- To develop and test fully functional machine learning models／開發和測試完整的機器學習模型
- Document search service that can extract answers from text within documents／可從文件中提取答案的文件搜尋服務
- To recommend personalized products for users based on their previous purchases／根據使用者過去的購買記錄推薦個人化產品
- ✅ **Predict the web traffic of a website for the next few weeks／預測網站未來幾週的網路流量**

---

## Q54
**A financial services company needs to retain its data for 10 years to meet compliance norms. Which Amazon S3 storage class is the best fit for this use case considering that the data has to be stored at a minimal cost?**

一家金融服務公司需要將資料保留 10 年以符合合規規範。考慮到資料必須以最低成本儲存，哪種 Amazon S3 儲存類別最適合此使用案例？

- Amazon S3 Glacier Flexible Retrieval
- Amazon S3 Standard-Infrequent Access (S3 Standard-IA)
- Amazon S3 Intelligent-Tiering
- ✅ **Amazon S3 Glacier Deep Archive**

---

## Q55
**A company has defined a baseline that mentions the number of AWS resources to be used for different stages of application testing. However, employees are provisioning additional resources via API calls, resulting in higher testing costs. Which AWS service will help the company raise alarms whenever the baseline resource numbers are crossed?**

一家公司定義了應用程式測試不同階段使用的 AWS 資源基準數量，但員工透過 API 呼叫佈建額外資源，導致測試成本增加。哪項 AWS 服務可在超過基準資源數量時發出警報？

- Amazon Detective
- AWS X-Ray
- AWS Config
- ✅ **AWS CloudTrail Insights**

---

## Q56
**Which of the following AWS services will help provision a logically isolated network for your AWS resources?**

以下哪項 AWS 服務可幫助為你的 AWS 資源佈建邏輯隔離的網路？

- AWS PrivateLink
- AWS Firewall Manager
- Amazon Route 53
- ✅ **Amazon Virtual Private Cloud (Amazon VPC)**

---

## Q57
**Which of the following is the responsibility of the customer when running applications using AWS Lambda?**

使用 AWS Lambda 運行應用程式時，以下哪項是客戶的責任？

- Configuring the networking infrastructure for the Lambda service／設定 Lambda 服務的網路基礎設施
- Updating the operating system and runtime environment for Lambda functions／更新 Lambda 函數的作業系統和執行環境
- Managing the physical servers where the Lambda function runs／管理 Lambda 函數運行的實體伺服器
- ✅ **Writing and maintaining the function code and its dependencies／編寫和維護函數程式碼及其相依性**

---

## Q58
**Which free tool helps to review the state of your workloads and compares them to the latest AWS architectural best practices after you have answered a series of questions about your workload?**

哪項免費工具可在你回答一系列關於工作負載的問題後，幫助審查工作負載的狀態並與最新的 AWS 架構最佳實務進行比較？

- AWS Trusted Advisor
- AWS Well-Architected Framework
- AWS Technical Account Manager (TAM)
- ✅ **AWS Well-Architected Tool**

---

## Q59
**AWS Web Application Firewall (AWS WAF) can be deployed on which of the following services?**

AWS WAF 可部署在以下哪些服務上？

- AWS AppSync, Amazon CloudFront, Application Load Balancer, Amazon EC2
- Amazon CloudFront, Amazon EC2, Amazon API Gateway, Application Load Balancer
- Application Load Balancer, Amazon EC2, Amazon API Gateway
- ✅ **Amazon CloudFront, Application Load Balancer, Amazon API Gateway, AWS AppSync**

---

## Q60
**A Cloud Practitioner wants to use CIDR block notation when providing an IP address range. Which of the following AWS network services/utilities allow this feature? (Select two)**

一位雲端從業人員希望在提供 IP 位址範圍時使用 CIDR 區塊表示法。以下哪些 AWS 網路服務/工具支援此功能？（選兩項）

- Amazon Simple Storage Service (Amazon S3)
- AWS Cost Explorer
- AWS Lambda
- ✅ **Network access control list (network ACL)／網路存取控制清單**
- ✅ **Security group／安全群組**

---

## Q61
**Which of the following will help you control the incoming traffic to an Amazon EC2 instance?**

以下哪項可幫助你控制流向 Amazon EC2 執行個體的傳入流量？

- Route Table／路由表
- AWS Resource Group／AWS 資源群組
- Network access control list (network ACL)／網路存取控制清單
- ✅ **Security Group／安全群組**

---

## Q62
**An e-commerce application sends out messages to a downstream application whenever an order is created. The downstream application processes the messages and updates its own systems. Currently, the two applications directly communicate with each other. Which service will you use to decouple this architecture, without any communication loss between the two systems?**

一個電商應用程式在每次建立訂單時向下游應用程式發送消息，下游應用程式處理消息並更新其自身系統。目前兩個應用程式直接通訊。你會使用哪項服務來解耦此架構，且不會造成兩個系統之間的通訊損失？

- Amazon Kinesis Data Streams
- AWS Lambda
- Amazon Simple Notification Service (Amazon SNS)
- ✅ **Amazon Simple Queue Service (SQS)**

---

## Q63
**By default, which of the following events are logged by AWS CloudTrail?**

預設情況下，AWS CloudTrail 記錄以下哪種類型的事件？

- AWS CloudTrail Insights events／CloudTrail Insights 事件
- Data events／資料事件
- Data events and Insights events／資料事件和 Insights 事件
- ✅ **Management events／管理事件**

---

## Q64
**Which of the following is a repository service that helps in maintaining application dependencies via integration with commonly used package managers and build tools like Maven, Gradle, npm, etc?**

以下哪項是透過與 Maven、Gradle、npm 等常用套件管理器和建置工具整合來幫助維護應用程式相依性的儲存庫服務？

- AWS CodeCommit
- AWS CodeBuild
- AWS CodeStar
- ✅ **AWS CodeArtifact**

---

## Q65
**Which feature/functionality will help you organize your AWS resources, manage and automate tasks on large numbers of resources at a time?**

哪項功能可幫助你組織 AWS 資源，並一次管理和自動化大量資源的任務？

- Tags／標籤
- Amazon WorkSpaces
- AWS Organizations
- ✅ **AWS Resource Groups／AWS 資源群組**

---

*共 65 題 | Total: 65 Questions*
