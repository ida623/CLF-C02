# AWS Certified Cloud Practitioner — Practice Test #3 中英對照

---

## Q1
A multi-national company has its business-critical data stored on a fleet of Amazon EC2 instances, in various countries, configured in region-specific compliance rules. To demonstrate compliance, the company needs to submit historical configurations on a regular basis. Which AWS service is best suited for this requirement?
一家跨國公司將業務關鍵資料儲存在各國的 Amazon EC2 執行個體上，並設定了特定區域的合規規則。為了展示合規性，公司需要定期提交歷史設定。哪個 AWS 服務最適合此需求？

* Amazon Macie
* Amazon GuardDuty
* AWS CloudTrail
* AWS Config

---

## Q2
Which AWS service can be used to automate code deployment to Amazon EC2 instances as well as on-premises instances?
哪個 AWS 服務可用於自動化將程式碼部署至 Amazon EC2 執行個體以及本地執行個體？

* AWS CodePipeline
* AWS CloudFormation
* AWS CodeCommit
* AWS CodeDeploy

---

## Q3
An IT company has a hybrid cloud architecture and it wants to centralize the server logs for its Amazon EC2 instances and on-premises servers. Which of the following is the MOST effective for this use-case?
一家 IT 公司擁有混合雲架構，希望集中管理 Amazon EC2 執行個體和本地伺服器的伺服器日誌。以下哪個最有效？

* Use AWS CloudTrail for the EC2 instance and Amazon CloudWatch Logs for the on-premises servers／使用 AWS CloudTrail 用於 EC2 執行個體，Amazon CloudWatch Logs 用於本地伺服器
* Use Amazon CloudWatch Logs for the EC2 instance and AWS CloudTrail for the on-premises servers／使用 Amazon CloudWatch Logs 用於 EC2 執行個體，AWS CloudTrail 用於本地伺服器
* Use AWS Lambda to send log data from EC2 instance and on-premises servers to Amazon CloudWatch Logs／使用 AWS Lambda 將 EC2 執行個體和本地伺服器的日誌資料傳送至 Amazon CloudWatch Logs
* Use Amazon CloudWatch Logs for both the EC2 instance and the on-premises servers／同時使用 Amazon CloudWatch Logs 用於 EC2 執行個體和本地伺服器

---

## Q4
A financial services enterprise plans to enable Multi-Factor Authentication (MFA) for its employees. For ease of travel, they prefer not to use any physical devices to implement MFA. Which of the below options is best suited for this use case?
一家金融服務企業計劃為其員工啟用 MFA。為了出行方便，他們傾向不使用任何實體裝置來實施 MFA。以下哪個選項最適合此使用案例？

* Hardware Multi-Factor Authentication (MFA) device／硬體多重要素驗證裝置
* U2F security key／U2F 安全金鑰
* Soft Token Multi-Factor Authentication (MFA) device／軟體令牌多重要素驗證裝置
* Virtual Multi-Factor Authentication (MFA) device／虛擬多重要素驗證裝置

---

## Q5
Which of the following AWS services offer block-level storage? (Select two)
以下哪些 AWS 服務提供區塊層級儲存？（選兩項）

* Amazon Simple Storage Service (Amazon S3)
* Amazon Elastic File System (Amazon EFS)
* Amazon Elastic Container Service (Amazon ECS)
* Instance Store／執行個體存放區
* Amazon Elastic Block Store (Amazon EBS)

---

## Q6
Which of the following statements are CORRECT about the AWS Auto Scaling group? (Select two)
以下哪些陳述關於 AWS Auto Scaling 群組是正確的？（選兩項）

* Auto Scaling group scales up and upgrades to a more powerful EC2 instance to match an increase in demand／Auto Scaling 群組向上擴展並升級至更強大的 EC2 執行個體以符合需求增加
* Auto Scaling group scales down and reduces the number of EC2 instances to match a decrease in demand／Auto Scaling 群組向下擴展並減少 EC2 執行個體數量以符合需求減少
* Auto Scaling group scales down and downgrades to a less powerful EC2 instance to match a decrease in demand／Auto Scaling 群組向下擴展並降級至較低效能的 EC2 執行個體以符合需求減少
* Auto Scaling group scales out and adds more number of EC2 instances to match an increase in demand／Auto Scaling 群組向外擴展並增加更多 EC2 執行個體以符合需求增加
* Auto Scaling group scales in and reduces the number of EC2 instances to match a decrease in demand／Auto Scaling 群組向內縮減並減少 EC2 執行個體數量以符合需求減少

---

## Q7
A research group wants to provision an Amazon EC2 instance for a flexible application that can be interrupted. Which of the following would you recommend as the MOST cost-optimal option?
一個研究群組希望為可被中斷的彈性應用程式佈建 Amazon EC2 執行個體。以下哪個是最具成本效益的選項？

* On-Demand Instance／隨需執行個體
* Dedicated Host／專用主機
* Reserved Instance (RI)／保留執行個體
* Spot Instance／Spot 執行個體

---

## Q8
Which Amazon Route 53 routing policy would you use when you want to route your traffic in an active-passive configuration?
當您想以主動-被動設定路由流量時，您會使用哪個 Amazon Route 53 路由政策？

* Weighted routing／加權路由
* Latency-based routing／延遲型路由
* Simple routing／簡單路由
* Failover routing／容錯移轉路由

---

## Q9
Which AWS service protects your AWS account by monitoring malicious activity and detecting threats?
哪個 AWS 服務透過監控惡意活動和偵測威脅來保護您的 AWS 帳戶？

* Amazon CloudWatch
* AWS Trusted Advisor
* AWS CloudTrail
* Amazon GuardDuty

---

## Q10
As a Cloud Practitioner, which Amazon S3 storage class would you recommend for data archival?
作為 Cloud Practitioner，您會推薦哪個 Amazon S3 儲存類別用於資料封存？

* Amazon S3 Standard
* Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)
* Amazon S3 Intelligent-Tiering
* Amazon S3 Glacier Flexible Retrieval

---

## Q11
Which of the following AWS entities provides the information required to launch an Amazon EC2 instance?
以下哪個 AWS 實體提供啟動 Amazon EC2 執行個體所需的資訊？

* Amazon Elastic Block Store (Amazon EBS)
* AWS Lambda
* Amazon Elastic File System (Amazon EFS)
* Amazon Machine Image (AMI)

---

## Q12
Which of the following improves the availability for a fleet of Amazon EC2 instances?
以下哪項可提升 Amazon EC2 執行個體群的可用性？

* Deploy the EC2 instances in the same AZ across two different AWS Regions／在兩個不同 AWS 區域的同一 AZ 中部署 EC2 執行個體
* Deploy the EC2 instances in the same AZ of an AWS Region／在 AWS 區域的同一 AZ 中部署 EC2 執行個體
* Deploy the EC2 instances across different AWS Regions of the same AZ／在同一 AZ 的不同 AWS 區域中部署 EC2 執行個體
* Deploy the EC2 instances across different Availability Zones (AZ) in the same AWS Region／在同一 AWS 區域的不同可用區域（AZ）中部署 EC2 執行個體

---

## Q13
An enterprise is developing a roadmap for its cloud adoption journey and wants to ensure its IT investments align with business objectives and deliver measurable value. Which perspective of the AWS Cloud Adoption Framework (CAF) addresses the strategy management capability?
一家企業正在制定雲端採用之旅的路線圖，並希望確保其 IT 投資與業務目標保持一致並創造可衡量的價值。AWS CAF 的哪個觀點涉及策略管理能力？

* Operations Perspective／營運觀點
* Platform Perspective／平台觀點
* Governance Perspective／治理觀點
* Business Perspective／業務觀點

---

## Q14
Which of the following AWS services specialize in data migration from on-premises to AWS Cloud? (Select two)
以下哪些 AWS 服務專門用於從本地到 AWS 雲端的資料遷移？（選兩項）

* AWS Direct Connect
* AWS Transit Gateway
* AWS Site-to-Site VPN
* AWS Snowball
* AWS Database Migration Service (AWS DMS)

---

## Q15
A development team is looking for a forum where the most frequent questions and requests from AWS customers are listed along with AWS provided solutions. Which AWS forum/service can be used for troubleshooting an issue or checking for a solution?
一個開發團隊正在尋找一個論壇，其中列出了 AWS 客戶最常見的問題和請求以及 AWS 提供的解決方案。哪個 AWS 論壇/服務可用於疑難排解或查找解決方案？

* AWS Support Center
* AWS Health Dashboard - service health
* AWS Marketplace
* AWS Knowledge Center

---

## Q16
A financial services company must meet compliance requirements that mandate storing multiple copies of data in geographically distant locations. Which of the following represents the MOST resource-efficient solution?
一家金融服務公司必須符合要求在地理位置遙遠的地點儲存多個資料副本的合規要求。以下哪個代表最有效率的解決方案？

* Use S3 same-region replication (S3 SRR) to replicate data between distant AWS Regions／使用 S3 同區域複寫在遙遠的 AWS 區域之間複寫資料
* For every new object, trigger an AWS Lambda function to write data into a bucket in another AWS Region／對每個新物件觸發 AWS Lambda 函數將資料寫入另一個 AWS 區域的儲存貯體
* Run a daily job on an EC2 instance to copy objects into another Region／在 EC2 執行個體上執行每日作業以將物件複製到另一個區域
* Use S3 cross-region replication (S3 CRR) to replicate data between distant AWS Regions／使用 S3 跨區域複寫在遙遠的 AWS 區域之間複寫資料

---

## Q17
Which of the following AWS services are regional in scope? (Select two)
以下哪些 AWS 服務的範圍是區域性的？（選兩項）

* AWS Identity and Access Management (AWS IAM)
* AWS Web Application Firewall (AWS WAF)
* Amazon CloudFront
* Amazon Rekognition
* AWS Lambda

---

## Q18
A leading research firm needs to access information available in old patents and documents (such as PDFs, Text Files, Word documents, etc) present in its huge knowledge base. Which of the following is the correct service to address this requirement?
一家領先的研究公司需要存取其龐大知識庫中舊專利和文件（如 PDF、文字檔案、Word 文件等）中的資訊。哪個服務適合解決此需求？

* Amazon Comprehend
* Amazon Lex
* Amazon Personalize
* Amazon Kendra

---

## Q19
Under the AWS Shared Responsibility Model, which of the following is the responsibility of a customer regarding AWS Lambda?
根據 AWS 共同責任模型，以下哪項是客戶對 AWS Lambda 的責任？

* Maintain all runtime environments for AWS Lambda functions／維護 AWS Lambda 函數的所有執行環境
* Configure networking infrastructure for the AWS Lambda functions／為 AWS Lambda 函數設定網路基礎設施
* Patch underlying OS for the AWS Lambda function infrastructure／修補 AWS Lambda 函數基礎設施的底層作業系統
* Maintain versions of an AWS Lambda function／維護 AWS Lambda 函數的版本

---

## Q20
Which of the following AWS services have data encryption automatically enabled? (Select two)
以下哪些 AWS 服務預設自動啟用資料加密？（選兩項）

* Amazon Redshift
* Amazon Elastic File System (Amazon EFS)
* Amazon Elastic Block Store (Amazon EBS)
* AWS Storage Gateway
* Amazon Simple Storage Service (Amazon S3)

---

## Q21
Which of the following statements is correct regarding the Amazon Elastic File System (Amazon EFS) storage service?
以下哪項陳述關於 Amazon EFS 儲存服務是正確的？

* EC2 instances can access files on an Amazon EFS file system only in one Availability Zone (AZ)／EC2 執行個體只能在一個 AZ 中存取 Amazon EFS 檔案系統的檔案
* EC2 instances can access files on an Amazon EFS file system across many AZs and VPCs but not across Regions／EC2 執行個體可以跨多個 AZ 和 VPC 存取 Amazon EFS 檔案系統的檔案，但不能跨區域
* EC2 instances can access files on an Amazon EFS file system across many AZs but not across VPCs and Regions／EC2 執行個體可以跨多個 AZ 存取 Amazon EFS 檔案系統的檔案，但不能跨 VPC 和區域
* EC2 instances can access files on an Amazon EFS file system across many Availability Zones (AZ), Regions and VPCs／EC2 執行個體可以跨多個 AZ、區域和 VPC 存取 Amazon EFS 檔案系統的檔案

---

## Q22
A cyber-security agency uses AWS Cloud and wants to carry out security assessments on its own AWS infrastructure without any prior approval from AWS. Which of the following describes/facilitates this practice?
一家網路安全機構使用 AWS 雲端，希望在無需事先獲得 AWS 批准的情況下對其自己的 AWS 基礎設施進行安全評估。以下哪項描述/促進了此實踐？

* AWS Secrets Manager
* Network Stress Testing／網路壓力測試
* Amazon Inspector
* Penetration Testing／滲透測試

---

## Q23
Which of the following is a part of the AWS Global Infrastructure?
以下哪項是 AWS 全球基礎設施的一部分？

* Virtual Private Network (VPN)／虛擬私有網路
* Virtual Private Cloud (VPC)／虛擬私有雲
* Subnet／子網路
* AWS Region／AWS 區域

---

## Q24
An IT company has deployed a static website on Amazon S3, but the website is still inaccessible. Which of the following solutions would you suggest to address this issue?
一家 IT 公司在 Amazon S3 上部署了靜態網站，但網站仍無法存取。您建議哪個解決方案來解決此問題？

* Enable Amazon S3 versioning／啟用 Amazon S3 版本控制
* Enable Amazon S3 replication／啟用 Amazon S3 複寫
* Disable Amazon S3 encryption／停用 Amazon S3 加密
* Fix the Amazon S3 bucket policy／修正 Amazon S3 儲存貯體政策

---

## Q25
An e-commerce company uses AWS Cloud and would like to receive separate invoices for development and production environments. Which of the following solutions would you recommend?
一家電子商務公司使用 AWS 雲端，希望收到開發和生產環境的獨立發票。您會推薦以下哪個解決方案？

* Use AWS Cost Explorer to create separate invoices for development and production environments／使用 AWS Cost Explorer 為開發和生產環境建立獨立發票
* Tag all resources as either development or production, then use the tags to create separate invoices／將所有資源標記為開發或生產，然後使用標籤建立獨立發票
* Use AWS Organizations to create separate invoices for development and production environments／使用 AWS Organizations 為開發和生產環境建立獨立發票
* Create separate AWS accounts for development and production environments to receive separate invoices／為開發和生產環境建立獨立的 AWS 帳戶以接收獨立發票

---

## Q26
An AWS hardware failure has impacted one of your Amazon EBS volumes. Which AWS service will alert you of the affected resources and provide a remedial action?
AWS 硬體故障影響了您的一個 Amazon EBS 磁碟區。哪個 AWS 服務會通知您受影響的資源並提供補救措施？

* Amazon GuardDuty
* AWS Trusted Advisor
* AWS Config
* AWS Health Dashboard – Your account health／AWS Health Dashboard – 您的帳戶健康狀態

---

## Q27
Which AWS service will you use to privately connect your VPC to Amazon S3?
您會使用哪個 AWS 服務將您的 VPC 私下連接至 Amazon S3？

* AWS Direct Connect
* Amazon API Gateway
* AWS Transit Gateway
* VPC Endpoint／VPC 端點

---

## Q28
Compared to the on-demand instance prices, what is the highest possible discount offered for reserved instances (RI)?
與隨需執行個體價格相比，保留執行個體（RI）提供的最高折扣是多少？

* 40%
* 90%
* 50%
* 72%

---

## Q29
Which of the following use cases is best suited for Amazon EFS Standard-Infrequent Access (EFS Standard-IA) storage class?
以下哪個使用案例最適合 Amazon EFS Standard-Infrequent Access（EFS Standard-IA）儲存類別？

* Object storage for workloads that need sub-second latency speeds for accessing the data／需要亞秒延遲存取資料的工作負載的物件儲存
* Use as boot volume for highly available Amazon EC2 instances／用作高可用性 Amazon EC2 執行個體的開機磁碟區
* Storing data in a single AWS Availability Zone (AZ)／將資料儲存在單一 AWS 可用區域（AZ）中
* Storing files in an accessible location to satisfy audit requirements／將檔案儲存在可存取的位置以滿足稽核要求

---

## Q30
An IT company would like to move its IT resources from an AWS Region in the US to another AWS Region in Europe. Which of the following represents the correct solution?
一家 IT 公司希望將其 IT 資源從美國的 AWS 區域遷移至歐洲的另一個 AWS 區域。以下哪個代表正確的解決方案？

* Use AWS CloudFormation to move the resources from source AWS Region to destination AWS Region／使用 AWS CloudFormation 將資源從來源 AWS 區域遷移至目標 AWS 區域
* Use AWS Database Migration Service (AWS DMS) to move all resources from source to destination AWS Region／使用 AWS DMS 將所有資源從來源遷移至目標 AWS 區域
* Raise a ticket with AWS Support for this resource migration／向 AWS Support 提交工單以進行此資源遷移
* The company should just start creating new resources in the destination AWS Region and then migrate the relevant data and applications into this new AWS Region／公司應直接在目標 AWS 區域中建立新資源，然後將相關資料和應用程式遷移至此新 AWS 區域

---

## Q31
Which of the following are recommended best practices for AWS IAM service? (Select two)
以下哪些是 AWS IAM 服務的推薦最佳實務？（選兩項）

* Share AWS account root user access keys with other administrators／與其他管理員共享 AWS 帳戶根使用者存取金鑰
* Grant maximum privileges to avoid assigning privileges again／授予最大權限以避免再次分配權限
* Create a minimum number of accounts and share these account credentials among employees／建立最少數量的帳戶並在員工之間共享這些帳戶憑證
* Rotate credentials regularly／定期輪換憑證
* Enable multi-factor authentication (MFA) for all users／為所有使用者啟用多重要素驗證（MFA）

---

## Q32
Which AWS service can be used for online analytical processing?
哪個 AWS 服務可用於線上分析處理？

* Amazon ElastiCache
* Amazon Relational Database Service (Amazon RDS)
* Amazon DynamoDB
* Amazon Redshift

---

## Q33
A startup has just moved its IT infrastructure to AWS Cloud. The CTO would like to receive detailed reports that break down the startup's AWS costs by the hour in an Amazon S3 bucket. Which AWS service would you recommend?
一家新創公司剛將其 IT 基礎設施遷移至 AWS 雲端。CTO 希望在 Amazon S3 儲存貯體中收到按小時細分 AWS 成本的詳細報告。您會推薦哪個 AWS 服務？

* AWS Cost Explorer
* AWS Pricing Calculator
* AWS Budgets
* AWS Cost & Usage Report (AWS CUR)

---

## Q34
Which pillar of the AWS Well-Architected Framework recommends maintaining infrastructure as code (IaC)?
AWS Well-Architected Framework 的哪個支柱建議將基礎設施作為程式碼（IaC）維護？

* Cost Optimization／成本優化
* Security／安全性
* Performance Efficiency／效能效率
* Operational Excellence／卓越營運

---

## Q35
Which Amazon S3 storage class offers the lowest availability?
哪個 Amazon S3 儲存類別提供最低的可用性？

* Amazon S3 Intelligent-Tiering
* Amazon S3 Standard
* Amazon S3 Glacier Flexible Retrieval
* Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)

---

## Q36
A startup runs its proprietary application on docker containers. Which AWS service would you recommend so that the startup can run containers and still have access to the underlying servers?
一家新創公司在 Docker 容器上執行其專有應用程式。您會推薦哪個 AWS 服務，使新創公司可以執行容器並仍然可以存取底層伺服器？

* Amazon Elastic Container Registry (Amazon ECR)
* AWS Fargate
* AWS Lambda
* Amazon Elastic Container Service (Amazon ECS)

---

## Q37
A global e-commerce platform wants to restrict access to its website from specific countries to comply with regional regulations. Which AWS service is best suited to implement this restriction?
一個全球電子商務平台希望限制特定國家/地區對其網站的存取，以符合地區法規。哪個 AWS 服務最適合實施此限制？

* Amazon Fraud Detector
* AWS Shield
* Amazon Pinpoint
* Amazon WAF

---

## Q38
Which of the following are components of an AWS Site-to-Site VPN? (Select two)
以下哪些是 AWS Site-to-Site VPN 的元件？（選兩項）

* Network Address Translation gateway (NAT gateway)／網路位址轉換閘道
* AWS storage gateway／AWS 儲存閘道
* Internet gateway／網際網路閘道
* Virtual private gateway (VGW)／虛擬私有閘道
* Customer gateway／客戶閘道

---

## Q39
AWS Lambda pricing is based on which of the following criteria? (Select two)
AWS Lambda 定價基於以下哪些標準？（選兩項）

* The number of lines of code for the AWS Lambda function／AWS Lambda 函數的程式碼行數
* The language runtime of the AWS Lambda function／AWS Lambda 函數的語言執行環境
* The size of the deployment package for the AWS Lambda function／AWS Lambda 函數的部署套件大小
* Number of requests for the AWS Lambda function／AWS Lambda 函數的請求數量
* The time it takes for the AWS Lambda function to execute／AWS Lambda 函數執行所需的時間

---

## Q40
Which budget types can be created under AWS Budgets? (Select three)
在 AWS Budgets 下可以建立哪些預算類型？（選三項）

* Software budget／軟體預算
* Resource budget／資源預算
* Hardware budget／硬體預算
* Reservation budget／預留預算
* Usage budget／使用量預算
* Cost budget／成本預算

---

## Q41
Which feature of AWS Cloud offers the ability to innovate faster and rapidly develop, test and launch software applications?
AWS 雲端的哪項功能提供了更快創新以及快速開發、測試和啟動軟體應用程式的能力？

* Cost savings／成本節省
* Ability to deploy globally in minutes／幾分鐘內全球部署的能力
* Elasticity／彈性
* Agility／敏捷性

---

## Q42
Which of the following is correct regarding the AWS Shield Advanced pricing?
以下哪項關於 AWS Shield Advanced 定價的陳述是正確的？

* AWS Shield Advanced is a free service for all AWS Support plans／AWS Shield Advanced 對所有 AWS Support 方案免費
* AWS Shield Advanced is a free service for AWS Business Support plan／AWS Shield Advanced 對 AWS Business Support 方案免費
* AWS Shield Advanced is a free service for AWS Enterprise Support plan／AWS Shield Advanced 對 AWS Enterprise Support 方案免費
* AWS Shield Advanced offers protection against higher fees that could result from a DDoS attack／AWS Shield Advanced 提供針對因 DDoS 攻擊可能導致較高費用的保護

---

## Q43
Which AWS service can be used to execute code triggered by new files being uploaded to Amazon S3?
哪個 AWS 服務可用於執行由新檔案上傳至 Amazon S3 觸發的程式碼？

* Amazon Simple Queue Service (Amazon SQS)
* Amazon Elastic Compute Cloud (Amazon EC2)
* Amazon Elastic Container Service (Amazon ECS)
* AWS Lambda

---

## Q44
AWS IAM policies are written as JSON documents. Which of the following are mandatory elements of an IAM policy?
AWS IAM 政策以 JSON 文件形式撰寫。以下哪些是 IAM 政策的必要元素？

* Effect, Sid
* Action, Condition
* Sid, Principal
* Effect, Action

---

## Q45
A research lab wants to optimize the caching capabilities for its scientific computations application running on Amazon EC2 instances. Which Amazon EC2 storage option is best suited for this use-case?
一個研究實驗室希望優化其在 Amazon EC2 執行個體上執行的科學運算應用程式的快取功能。哪個 Amazon EC2 儲存選項最適合此使用案例？

* Amazon Simple Storage Service (Amazon S3)
* Amazon Elastic Block Store (Amazon EBS)
* Amazon Elastic File System (Amazon EFS)
* Instance Store／執行個體存放區

---

## Q46
A customer is running a comparative study of pricing models of Amazon EFS and Amazon EBS. Which of the following statements are correct regarding this use-case? (Select two)
一位客戶正在對 Amazon EFS 和 Amazon EBS 的定價模型進行比較研究。以下哪些陳述關於此使用案例是正確的？（選兩項）

* Amazon EBS Snapshot storage pricing is based on the amount of space your data consumes in Amazon EBS／Amazon EBS 快照儲存定價基於資料在 Amazon EBS 中佔用的空間量
* With AWS Backup, you pay only for the amount of Amazon EFS backup storage you use in a month, you need not pay for restoring this data／使用 AWS Backup，您只需為每月使用的 Amazon EFS 備份儲存量付費，無需為恢復此資料付費
* Amazon EC2 data transfer charges will apply for all Amazon EBS direct APIs for Snapshots／Amazon EC2 資料傳輸費用將適用於所有 Amazon EBS 快照直接 API
* Amazon EBS Snapshots are stored incrementally, which means you are billed only for the changed blocks stored／Amazon EBS 快照以增量方式儲存，這表示您只需為儲存的已變更區塊付費
* You will pay a fee each time you read from or write data stored on the Amazon EFS - Infrequent Access storage class／每次從 Amazon EFS - Infrequent Access 儲存類別讀取或寫入資料時，您都需要支付費用

---

## Q47
Which of the following is the best way to protect your data from accidental deletion on Amazon S3?
以下哪項是保護 Amazon S3 上資料免遭意外刪除的最佳方式？

* Amazon S3 lifecycle configuration／Amazon S3 生命週期設定
* Amazon S3 storage classes／Amazon S3 儲存類別
* Amazon S3 Transfer Acceleration (Amazon S3TA)
* Amazon S3 Versioning／Amazon S3 版本控制

---

## Q48
What is the primary benefit of deploying an Amazon RDS database in a Read Replica configuration?
在讀取副本設定中部署 Amazon RDS 資料庫的主要優點是什麼？

* Read Replica reduces database usage costs／讀取副本降低資料庫使用成本
* Read Replica protects the database from a regional failure／讀取副本保護資料庫免受區域故障影響
* Read Replica enhances database availability／讀取副本提升資料庫可用性
* Read Replica improves database scalability／讀取副本提升資料庫可擴展性

---

## Q49
Which AWS services/features support High Availability by default? (Select two)
以下哪些 AWS 服務/功能預設支援高可用性？（選兩項）

* Amazon Elastic Block Store (Amazon EBS)
* Subnet／子網路
* Instance Store／執行個體存放區
* Amazon Elastic File System (Amazon EFS)
* Amazon DynamoDB

---

## Q50
An organization maintains separate Amazon VPCs for each of its departments. The organization now wants to connect all VPCs for better departmental collaboration. Which AWS service will help effectively?
一個組織為每個部門維護獨立的 Amazon VPC。組織現在希望連接所有 VPC 以促進部門協作。哪個 AWS 服務可以有效幫助解決此問題？

* AWS Direct Connect
* AWS Site-to-Site VPN
* VPC peering connection／VPC 對等連線
* AWS Transit Gateway

---

## Q51
Which of the following capabilities does Amazon Rekognition provide as a ready-to-use feature?
以下哪些功能是 Amazon Rekognition 提供的即用型功能？

* Resize images quickly／快速調整圖片大小
* Convert images into greyscale／將圖片轉換為灰階
* Human pose detection／人體姿勢偵測
* Identify objects in a photo／識別照片中的物件

---

## Q52
What is the region-specific constraint that the Amazon Machine Image (AMI) must meet so that it can be used for an Amazon EC2 instance?
Amazon Machine Image（AMI）必須滿足哪些特定區域限制才能用於 Amazon EC2 執行個體？

* You can use an AMI from a different region, but it degrades the performance of the EC2 instance／您可以使用不同區域的 AMI，但這會降低 EC2 執行個體的效能
* An AMI is a global entity, so the region is not applicable／AMI 是全球實體，因此區域不適用
* You should use an AMI from the same region, as it improves the performance of the EC2 instance／您應該使用相同區域的 AMI，因為這可提升 EC2 執行個體的效能
* You must use an AMI from the same region as that of the EC2 instance. The region of the AMI has no bearing on the performance of the EC2 instance／您必須使用與 EC2 執行個體相同區域的 AMI。AMI 的區域對 EC2 執行個體的效能沒有影響

---

## Q53
Which AWS service can be used as an in-memory database with high-performance and low latency?
哪個 AWS 服務可用作高效能、低延遲的記憶體內資料庫？

* Amazon DynamoDB
* Amazon Athena
* Amazon Relational Database Service (Amazon RDS)
* Amazon ElastiCache

---

## Q54
Which of the following statements are CORRECT regarding security groups and network access control lists (network ACL)? (Select two)
以下哪些陳述關於安全群組和網路存取控制清單（網路 ACL）是正確的？（選兩項）

* A network ACL is stateful, that is, it automatically allows the return traffic／網路 ACL 是有狀態的，即它自動允許回傳流量
* A security group contains a numbered list of rules and evaluates these rules in the increasing order while deciding whether to allow the traffic／安全群組包含有編號的規則清單，並在決定是否允許流量時按遞增順序評估這些規則
* A security group is stateless, that is, the return traffic must be explicitly allowed／安全群組是無狀態的，即回傳流量必須明確允許
* A network ACL contains a numbered list of rules and evaluates these rules in the increasing order while deciding whether to allow the traffic／網路 ACL 包含有編號的規則清單，並在決定是否允許流量時按遞增順序評估這些規則
* A security group is stateful, that is, it automatically allows the return traffic／安全群組是有狀態的，即它自動允許回傳流量

---

## Q55
A company has a static website hosted on an Amazon S3 bucket in Asia. It wants to drive growth globally. How can it improve the global performance of its static website?
一家公司在亞洲的 Amazon S3 儲存貯體上託管靜態網站，現在希望推動全球增長。如何提升其靜態網站的全球效能？

* Use AWS Web Application Firewall (AWS WAF) to improve the performance of your website／使用 AWS WAF 提升網站效能
* Use AWS CloudFormation to improve the performance of your website／使用 AWS CloudFormation 提升網站效能
* Use Amazon S3 Transfer Acceleration (Amazon S3TA) to improve the performance of your website／使用 Amazon S3TA 提升網站效能
* Use Amazon CloudFront to improve the performance of your website／使用 Amazon CloudFront 提升網站效能

---

## Q56
According to the AWS Shared Responsibility Model, which of the following are the responsibilities of the customer? (Select two)
根據 AWS 共同責任模型，以下哪些是客戶的責任？（選兩項）

* Ensuring AWS employees cannot access customer data／確保 AWS 員工無法存取客戶資料
* Compliance validation of Cloud infrastructure／雲端基礎設施的合規驗證
* AWS Global Network Security／AWS 全球網路安全
* Operating system patches and updates of an Amazon EC2 instance／Amazon EC2 執行個體的作業系統修補程式和更新
* Managing IAM users and roles／管理 IAM 使用者和角色

---

## Q57
Which of the following Cloud Computing models does the 'gmail' service represent?
以下哪個雲端運算模型代表了「gmail」服務？

* Infrastructure as a service (IaaS)／基礎設施即服務
* Platform as a service (PaaS)／平台即服務
* Function as a service (FaaS)／函數即服務
* Software as a service (SaaS)／軟體即服務

---

## Q58
As per the AWS Shared Responsibility Model, which of the following security services/utilities falls under the purview of AWS?
根據 AWS 共同責任模型，以下哪些安全服務/工具屬於 AWS 的管轄範圍？

* Security group／安全群組
* AWS Shield Advanced
* AWS Web Application Firewall (AWS WAF)
* AWS Shield Standard

---

## Q59
Which of the following are correct statements regarding the AWS Shared Responsibility Model? (Select two)
以下哪些陳述關於 AWS 共同責任模型是正確的？（選兩項）

* Configuration Management is the responsibility of the customer／設定管理是客戶的責任
* For a service like Amazon EC2 (IaaS), AWS is responsible for maintaining guest operating system／對於 Amazon EC2（IaaS）等服務，AWS 負責維護客體作業系統
* AWS is responsible for training AWS and customer employees on AWS products and services／AWS 負責培訓 AWS 和客戶員工關於 AWS 產品和服務
* For abstracted services like Amazon S3, AWS operates the infrastructure layer, the operating system, and platforms／對於 Amazon S3 等抽象服務，AWS 負責維運基礎設施層、作業系統和平台
* AWS is responsible for Security 'of' the Cloud／AWS 負責雲端的安全性

---

## Q60
An IT company wants to identify all Amazon EC2 instances that are under-utilized. Which AWS services can be used off-the-shelf to address this use-case without needing any manual configurations? (Select two)
一家 IT 公司希望識別所有未充分使用的 Amazon EC2 執行個體。哪些 AWS 服務可以開箱即用地解決此使用案例，無需任何手動設定？（選兩項）

* Amazon CloudWatch
* AWS Cost & Usage Report (AWS CUR)
* AWS Budgets
* AWS Cost Explorer
* AWS Trusted Advisor

---

## Q61
A medical device company is looking for a durable and cost-effective way of storing their historic data. Due to compliance requirements, the data must be stored for 10 years. Which AWS Storage solution will you suggest?
一家醫療設備公司正在尋找儲存其歷史資料的耐用且具成本效益的方式。由於合規要求，資料必須儲存 10 年。您會建議哪個 AWS 儲存解決方案？

* Amazon Elastic File System (Amazon EFS)
* Amazon S3 Glacier Flexible Retrieval
* AWS Storage Gateway
* Amazon S3 Glacier Deep Archive

---

## Q62
Which of the following statements are true about Cost Allocation Tags in AWS Billing? (Select two)
以下哪些陳述關於 AWS 計費中的成本分配標籤是正確的？（選兩項）

* Tags help in organizing resources and are a mandatory configuration item to run reports／標籤有助於組織資源，是執行報告的必要設定項目
* For each resource, each tag key must be unique, but can have multiple values／對於每個資源，每個標籤鍵必須唯一，但可以有多個值
* Only user-defined tags need to be activated before they can appear in Cost Explorer or on a cost allocation report／只有使用者定義的標籤需要在出現在 Cost Explorer 或成本分配報告中之前啟動
* For each resource, each tag key must be unique, and each tag key can have only one value／對於每個資源，每個標籤鍵必須唯一，且每個標籤鍵只能有一個值
* You must activate both AWS generated tags and user-defined tags separately before they can appear in Cost Explorer or on a cost allocation report／您必須分別啟動 AWS 生成的標籤和使用者定義的標籤，才能使其出現在 Cost Explorer 或成本分配報告中

---

## Q63
AWS Trusted Advisor analyzes your AWS environment and provides best practice recommendations for which of the following categories? (Select two)
AWS Trusted Advisor 分析您的 AWS 環境並為以下哪些類別提供最佳實務建議？（選兩項）

* Change Management／變更管理
* Elasticity／彈性
* Documentation／文件
* Service Limits／服務限制
* Cost Optimization／成本優化

---

## Q64
Which AWS service will you use if you have to move large volumes of on-premises data to AWS Cloud from a remote location with limited bandwidth?
如果您必須從頻寬有限的遠端位置將大量本地資料移動至 AWS 雲端，您會使用哪個 AWS 服務？

* AWS Virtual Private Network (VPN)
* AWS Direct Connect
* AWS Transit Gateway
* AWS Snowball

---

## Q65
Amazon CloudWatch billing metric data is stored in which AWS Region?
Amazon CloudWatch 帳單指標資料儲存在哪個 AWS 區域？

* In the AWS Region where the AWS resource is provisioned／在佈建 AWS 資源的 AWS 區域
* In the AWS Region where the AWS account is created／在建立 AWS 帳戶的 AWS 區域
* US West (N. California) - us-west-1
* US East (N. Virginia) - us-east-1
