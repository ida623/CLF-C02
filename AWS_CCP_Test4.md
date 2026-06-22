# AWS Certified Cloud Practitioner — Practice Test #4 中英對照

---

## Q1
Which AWS service would you use to create a logically isolated section of the AWS Cloud where you can launch AWS resources in your virtual network?
您會使用哪個 AWS 服務來建立 AWS 雲端的邏輯隔離區段，以便在您的虛擬網路中啟動 AWS 資源？

* Virtual Private Network (VPN)／虛擬私有網路
* Network Access Control List (Network ACL)／網路存取控制清單
* Subnet／子網路
* Virtual Private Cloud (VPC)／虛擬私有雲

---

## Q2
An organization maintains a separate Virtual Private Cloud (VPC) for each of its business units. Two units need to privately share data. Which is the most optimal way of privately sharing data between the two VPCs?
一個組織為每個業務單位維護獨立的 VPC。兩個單位需要私下共享資料。在兩個 VPC 之間私下共享資料的最佳方式是什麼？

* VPC Endpoint／VPC 端點
* AWS Direct Connect
* AWS Site-to-Site VPN
* VPC peering connection／VPC 對等連線

---

## Q3
A financial services company wants to ensure that all customer data uploaded on its data lake on Amazon S3 always stays private. Which of the following is the MOST efficient solution to address this compliance requirement?
一家金融服務公司希望確保上傳至 Amazon S3 資料湖的所有客戶資料始終保持私有。以下哪個解決方案最有效率地滿足此合規要求？

* Trigger a Lambda function every time an object is uploaded on S3 to change the object settings to make sure it stays private／每次物件上傳至 S3 時觸發 Lambda 函數變更物件設定以確保其保持私有
* Use Amazon CloudWatch to ensure that all S3 resources stay private／使用 Amazon CloudWatch 確保所有 S3 資源保持私有
* Set up a high-level advisory committee to review the privacy settings of each object uploaded into S3／設立高階顧問委員會審查每個上傳至 S3 的物件隱私設定
* Use Amazon S3 Block Public Access to ensure that all S3 resources stay private／使用 Amazon S3 封鎖公開存取以確保所有 S3 資源保持私有

---

## Q4
Which of the following types are free under the Amazon S3 pricing model? (Select two)
以下哪些類型在 Amazon S3 定價模型下是免費的？（選兩項）

* Data storage fee for objects stored in S3 Standard／儲存在 S3 Standard 中的物件儲存費用
* Data storage fee for objects stored in S3 Glacier／儲存在 S3 Glacier 中的物件儲存費用
* Data transferred out to an EC2 instance in any AWS Region／傳輸至任何 AWS 區域的 EC2 執行個體的資料輸出
* Data transferred in from the internet／從網際網路傳入的資料
* Data transferred out to an EC2 instance when the instance is in the same AWS Region as the S3 bucket／當 EC2 執行個體與 S3 儲存貯體位於同一 AWS 區域時傳輸至該執行個體的資料

---

## Q5
An e-commerce company wants to review the Payment Card Industry (PCI) reports on AWS Cloud. Which AWS resource can be used to address this use-case?
一家電子商務公司希望審查 AWS 雲端上的 PCI 報告。哪個 AWS 資源可以滿足此使用案例？

* AWS Trusted Advisor
* AWS Cost & Usage Report (AWS CUR)
* AWS Secrets Manager
* AWS Artifact

---

## Q6
How is Amazon EC2 different from traditional hosting systems? (Select two)
Amazon EC2 與傳統託管系統有何不同？（選兩項）

* With Amazon EC2, users risk overbuying resources／使用 Amazon EC2，使用者有超購資源的風險
* Amazon EC2 caters more towards groups of users with similar system requirements so that resources are shared and cost is reduced／Amazon EC2 更適合具有相似系統需求的使用者群組，以便共享資源並降低成本
* Amazon EC2 provides a pre-configured instance for a fixed monthly cost／Amazon EC2 以固定月費提供預先設定的執行個體
* With Amazon EC2, developers can launch and terminate the instances anytime they need to／使用 Amazon EC2，開發人員可以隨時啟動和終止執行個體
* Amazon EC2 can scale with changing computing requirements／Amazon EC2 可以隨計算需求的變化進行擴展

---

## Q7
Which AWS service would you choose for a data processing project that needs a schemaless database?
對於需要無結構描述資料庫的資料處理專案，您會選擇哪個 AWS 服務？

* Amazon Aurora
* Amazon Relational Database Service (Amazon RDS)
* Amazon RedShift
* Amazon DynamoDB

---

## Q8
Which of the following statements are true regarding Amazon S3? (Select two)
以下哪些陳述關於 Amazon S3 是正確的？（選兩項）

* Amazon S3 is a block storage service designed for a broad range of workloads／Amazon S3 是專為各種工作負載設計的區塊儲存服務
* You can install databases on Amazon S3／您可以在 Amazon S3 上安裝資料庫
* Amazon S3 is a fully managed, elastic file system storage service used as database backup／Amazon S3 是用作資料庫備份的全受管彈性檔案系統儲存服務
* Amazon S3 stores data in a flat non-hierarchical structure／Amazon S3 以扁平的非階層式結構儲存資料
* Amazon S3 is a key value based object storage service／Amazon S3 是基於鍵值的物件儲存服務

---

## Q9
Which of the following describes an Availability Zone (AZ) in the AWS Cloud?
以下哪項描述了 AWS 雲端中的可用區域（AZ）？

* One or more data centers in multiple locations／多個位置中的一個或多個資料中心
* One or more server racks in multiple locations／多個位置中的一個或多個伺服器機架
* One or more server racks in the same location／同一位置中的一個或多個伺服器機架
* One or more data centers in the same location／同一位置中的一個或多個資料中心

---

## Q10
Which of the following statements are CORRECT regarding AWS Global Accelerator? (Select two)
以下哪些陳述關於 AWS Global Accelerator 是正確的？（選兩項）

* AWS Global Accelerator can be used to host static websites／AWS Global Accelerator 可用於託管靜態網站
* AWS Global Accelerator cannot be configured with an Elastic Load Balancer (ELB)／AWS Global Accelerator 無法與 ELB 配合設定
* AWS Global Accelerator uses edge locations different from Amazon CloudFront edge locations／AWS Global Accelerator 使用與 Amazon CloudFront 不同的邊緣位置
* AWS Global Accelerator provides static IP addresses that act as a fixed entry point to your applications／AWS Global Accelerator 提供靜態 IP 位址作為應用程式的固定進入點
* AWS Global Accelerator is a good fit for non-HTTP use cases／AWS Global Accelerator 非常適合非 HTTP 使用案例

---

## Q11
Which of the following are benefits of the AWS Web Application Firewall (AWS WAF)? (Select two)
以下哪些是 AWS WAF 的優點？（選兩項）

* AWS WAF offers dedicated support from the DDoS Response Team (DRT) and advanced reporting／AWS WAF 提供來自 DDoS 響應團隊的專屬支援和進階報告
* AWS WAF offers protection against all known infrastructure (Layer 3 and 4) attacks／AWS WAF 提供針對所有已知基礎設施（第 3 和第 4 層）攻擊的保護
* AWS WAF lets you monitor HTTP and HTTPS requests forwarded to Amazon Route 53／AWS WAF 可讓您監控轉發至 Amazon Route 53 的 HTTP 和 HTTPS 請求
* AWS WAF can block all requests except the ones that you allow／AWS WAF 可以封鎖除您允許的請求之外的所有請求
* AWS WAF can check for the presence of SQL code that is likely to be malicious (known as SQL injection)／AWS WAF 可以檢查可能是惡意的 SQL 程式碼（即 SQL 注入）

---

## Q12
The DevOps team at an IT company wants to centrally manage its servers on AWS Cloud as well as on-premise data center so that it can collect software inventory, run commands, configure and patch servers at scale. Which AWS service would you recommend?
一家 IT 公司的 DevOps 團隊希望集中管理 AWS 雲端及本地資料中心的伺服器，以便大規模收集軟體庫存、執行命令、設定和修補伺服器。您會推薦哪個 AWS 服務？

* AWS Config
* AWS Service Catalog
* AWS CloudFormation
* AWS Systems Manager

---

## Q13
Which AWS services can be used together to send alerts whenever the AWS account root user signs in? (Select two)
哪些 AWS 服務可以結合使用，在 AWS 帳戶根使用者登入時發送警報？（選兩項）

* AWS Step Functions
* Amazon Simple Queue Service (Amazon SQS)
* AWS Lambda
* Amazon CloudWatch
* Amazon Simple Notification Service (Amazon SNS)

---

## Q14
A multi-national organization wants to connect its on-premises data center with different VPCs for better collaboration. Which AWS services can be combined to build the MOST efficient solution? (Select two)
一家跨國組織希望將其本地資料中心與不同的 VPC 連接以促進協作。哪些 AWS 服務可以結合使用以建立最有效率的解決方案？（選兩項）

* VPC peering connection／VPC 對等連線
* AWS Storage Gateway
* Internet Gateway／網際網路閘道
* AWS Direct Connect
* AWS Transit Gateway

---

## Q15
Which of the following is the best practice for application architecture on AWS Cloud?
以下哪項是 AWS 雲端應用程式架構的最佳實務？

* Use synchronous communication between components／在元件之間使用同步通訊
* Build tightly coupled components／建立緊耦合元件
* Build monolithic applications／建立單體式應用程式
* Build loosely coupled components／建立鬆耦合元件

---

## Q16
AWS Shield Advanced provides expanded DDoS attack protection for web applications running on which of the following resources? (Select two)
AWS Shield Advanced 為在以下哪些資源上執行的 Web 應用程式提供擴展的 DDoS 攻擊防護？（選兩項）

* Amazon Simple Storage Service (Amazon S3)
* AWS Elastic Beanstalk
* AWS Identity and Access Management (AWS IAM)
* Amazon Elastic Compute Cloud (Amazon EC2)
* Amazon CloudFront

---

## Q17
An e-commerce company has migrated its IT infrastructure from the on-premises data center to AWS Cloud. Which of the following costs is the company responsible for?
一家電子商務公司已將其 IT 基礎設施從本地資料中心遷移至 AWS 雲端。以下哪項成本由公司負責？

* Costs for hardware infrastructure on AWS Cloud／AWS 雲端上的硬體基礎設施成本
* AWS Data Center physical security costs／AWS 資料中心實體安全成本
* Costs for powering servers on AWS Cloud／AWS 雲端上伺服器的電力成本
* Application software license costs／應用程式軟體授權成本

---

## Q18
Which of the following are the serverless computing services offered by AWS? (Select two)
以下哪些是 AWS 提供的無伺服器運算服務？（選兩項）

* Amazon Elastic Compute Cloud (Amazon EC2)
* Amazon Lightsail
* AWS Elastic Beanstalk
* AWS Fargate
* AWS Lambda

---

## Q19
Which of the following Amazon S3 storage classes has NO constraint of a minimum storage duration charge for objects?
以下哪個 Amazon S3 儲存類別對物件沒有最低儲存期限費用的限制？

* Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)
* Amazon S3 Standard-Infrequent Access (S3 Standard-IA)
* Amazon S3 Glacier Flexible Retrieval
* Amazon S3 Standard

---

## Q20
Which of the following is correct regarding the Amazon RDS service?
以下哪項關於 Amazon RDS 服務的陳述是正確的？

* You can use read replicas for improved read performance only and multi-AZ deployment for disaster recovery only／您只能使用讀取副本提升讀取效能，只能使用多 AZ 部署進行災難恢復
* You can use both read replicas and multi-AZ deployment having single standby for improved read performance／您可以同時使用讀取副本和具有單一待機的多 AZ 部署來提升讀取效能
* You can use read replicas for disaster recovery only and multi-AZ deployment for improved read performance only／您只能使用讀取副本進行災難恢復，只能使用多 AZ 部署提升讀取效能
* You can use both read replicas and multi-AZ deployment for disaster recovery／您可以同時使用讀取副本和多 AZ 部署進行災難恢復

---

## Q21
Which Amazon Route 53 routing policy would you use to route traffic to a single resource such as a web server for your website?
您會使用哪個 Amazon Route 53 路由政策將流量路由至單一資源（例如您網站的 Web 伺服器）？

* Latency-based routing／延遲型路由
* Failover routing／容錯移轉路由
* Weighted routing／加權路由
* Simple routing／簡單路由

---

## Q22
Which of the following is available across all AWS Support plans?
以下哪項在所有 AWS Support 方案中都可用？

* Third-Party Software Support／第三方軟體支援
* Full set of AWS Trusted Advisor best practice checks／完整的 AWS Trusted Advisor 最佳實務檢查
* Enhanced Technical Support with unlimited cases and unlimited contacts／具有無限案例和無限聯絡人的增強技術支援
* AWS Health Dashboard – Your account health／AWS Health Dashboard – 您的帳戶健康狀態

---

## Q23
Which of the following is a container service of AWS?
以下哪個是 AWS 的容器服務？

* Amazon Simple Notification Service (Amazon SNS)
* AWS Elastic Beanstalk
* Amazon SageMaker
* AWS Fargate

---

## Q24
Which AWS service can help you analyze your infrastructure to identify unattached or underutilized Amazon EBS Elastic Volumes?
哪個 AWS 服務可以幫助您分析基礎設施，以識別未附加或未充分使用的 Amazon EBS 彈性磁碟區？

* Amazon Inspector
* Amazon CloudWatch
* AWS Config
* AWS Trusted Advisor

---

## Q25
A media company uploads its media files to a centralized Amazon S3 bucket from geographically dispersed locations. Which solution can the company use to optimize transfer speeds?
一家媒體公司從地理位置分散的地點將媒體檔案上傳至集中的 Amazon S3 儲存貯體。公司可以使用哪個解決方案來優化傳輸速度？

* Amazon CloudFront
* AWS Global Accelerator
* AWS Direct Connect
* Amazon S3 Transfer Acceleration (S3TA)

---

## Q26
Which of the following AWS services offers Lifecycle configuration for cost-optimal storage?
以下哪個 AWS 服務提供生命週期設定以實現成本最佳化儲存？

* Amazon Elastic Block Store (Amazon EBS)
* Amazon EC2 Instance Store
* AWS Storage Gateway
* Amazon Simple Storage Service (Amazon S3)

---

## Q27
Which of the following AWS authentication mechanisms supports an AWS MFA device that you can plug into a USB port on your computer?
以下哪個 AWS 驗證機制支援可插入電腦 USB 連接埠的 AWS MFA 裝置？

* Hardware Multi-Factor Authentication (MFA) device／硬體多重要素驗證裝置
* Virtual Multi-Factor Authentication (MFA) device／虛擬多重要素驗證裝置
* SMS text message-based Multi-Factor Authentication (MFA)／基於簡訊的多重要素驗證
* U2F security key／U2F 安全金鑰

---

## Q28
Bob and Susan each have an AWS account in AWS Organizations. Susan has five Reserved Instances (RIs) and Bob has none. During one hour, Susan uses three instances and Bob uses six, for a total of nine. Which of the following statements are correct about consolidated billing? (Select two)
Bob 和 Susan 各自在 AWS Organizations 中擁有一個 AWS 帳戶。Susan 有五個保留執行個體，Bob 沒有。在某一小時內，Susan 使用三個執行個體，Bob 使用六個，共九個。以下哪些陳述關於合併計費是正確的？（選兩項）

* AWS bills three instances as Reserved Instances, and the remaining six instances as regular instances／AWS 將三個執行個體計為保留執行個體，其餘六個計為一般執行個體
* Bob receives the cost-benefit from Susan's RI only if he launches his instances in the same AWS Region where Susan purchased her RIs／Bob 僅在與 Susan 購買 RI 的同一 AWS 區域啟動執行個體時才能獲得成本優惠
* Bob does not receive any cost-benefit since he hasn't purchased any RI／Bob 未購買任何 RI 因此不會獲得任何成本優惠
* Bob receives the cost-benefit from Susan's RIs only if he launches his instances in the same Availability Zone (AZ) where Susan purchased her RIs／Bob 僅在與 Susan 購買 RI 的同一可用區域啟動執行個體時才能獲得成本優惠
* AWS bills five instances as Reserved Instances, and the remaining four instances as regular instances／AWS 將五個執行個體計為保留執行個體，其餘四個計為一般執行個體

---

## Q29
Which AWS service will help you deploy application code automatically to an Amazon EC2 instance?
哪個 AWS 服務可以幫助您將應用程式程式碼自動部署至 Amazon EC2 執行個體？

* AWS CloudFormation
* AWS Elastic Beanstalk
* AWS CodeBuild
* AWS CodeDeploy

---

## Q30
Which of the following scenarios can be handled by AWS Lambda? (Select two)
以下哪些情境可以由 AWS Lambda 處理？（選兩項）

* You can install Container Services on AWS Lambda／您可以在 AWS Lambda 上安裝容器服務
* AWS Lambda can be used to store sensitive environment variables／AWS Lambda 可用於儲存敏感環境變數
* You can install low latency databases on AWS Lambda／您可以在 AWS Lambda 上安裝低延遲資料庫
* AWS Lambda can be used for preprocessing of data before it is stored in Amazon S3 buckets／AWS Lambda 可用於在資料儲存至 Amazon S3 儲存貯體之前進行預處理
* AWS Lambda can be used to execute code in response to events such as updates to DynamoDB tables／AWS Lambda 可用於回應事件（如 DynamoDB 資料表更新）來執行程式碼

---

## Q31
Which pillar of AWS Well-Architected Framework is responsible for making sure that you select the right resource types and sizes based on your workload requirements?
AWS Well-Architected Framework 的哪個支柱負責確保根據工作負載需求選擇正確的資源類型和大小？

* Operational Excellence／卓越營運
* Cost Optimization／成本優化
* Reliability／可靠性
* Performance Efficiency／效能效率

---

## Q32
A digital media company wants to convert English language subtitles into Spanish language subtitles. Which AWS service would you recommend?
一家數位媒體公司希望將英文字幕轉換為西班牙文字幕。您會推薦哪個 AWS 服務？

* Amazon Polly
* Amazon Rekognition
* Amazon Transcribe
* Amazon Translate

---

## Q33
Which of the following is best-suited for load-balancing HTTP and HTTPS traffic?
以下哪個最適合用於 HTTP 和 HTTPS 流量的負載平衡？

* AWS Auto Scaling
* Network Load Balancer／網路負載平衡器
* System Load Balancer
* Application Load Balancer／應用程式負載平衡器

---

## Q34
As per the AWS Shared Responsibility Model, which of the following is a responsibility of AWS from a security and compliance point of view?
根據 AWS 共同責任模型，以下哪項是 AWS 從安全和合規角度的責任？

* Patching guest OS and applications／修補客體作業系統和應用程式
* Service and Communications Protection／服務和通訊保護
* Identity and Access Management／身分和存取管理
* Patching networking infrastructure／修補網路基礎設施

---

## Q35
According to the AWS Shared Responsibility Model, which of the following are responsibilities of the customer for AWS IAM? (Select two)
根據 AWS 共同責任模型，以下哪些是客戶對 AWS IAM 的責任？（選兩項）

* Manage global network security infrastructure／管理全球網路安全基礎設施
* Compliance validation for the underlying software infrastructure／底層軟體基礎設施的合規驗證
* Configuration and vulnerability analysis for the underlying software infrastructure／底層軟體基礎設施的設定和漏洞分析
* Analyze user access patterns and review AWS IAM permissions／分析使用者存取模式並審查 AWS IAM 權限
* Enable multi-factor authentication (MFA) on all accounts／在所有帳戶上啟用多重要素驗證（MFA）

---

## Q36
Amazon EC2 Spot instances are a best-fit for which of the following scenarios?
Amazon EC2 Spot 執行個體最適合以下哪種情境？

* To run scheduled jobs (jobs that run at the same time every day)／執行排程作業（每天在相同時間執行的作業）
* To install cost-effective Amazon RDS database／安裝具成本效益的 Amazon RDS 資料庫
* To run batch processes for critical workloads／執行關鍵工作負載的批次處理
* To run any containerized workload with Amazon ECS that can be interrupted／執行任何可被中斷的 Amazon ECS 容器化工作負載

---

## Q37
The DevOps team at a Big Data consultancy has set up Amazon EC2 instances across two AWS Regions. Which of the following characterizes this application architecture?
一家大數據諮詢公司的 DevOps 團隊在兩個 AWS 區域設定了 Amazon EC2 執行個體。以下哪項描述了此應用程式架構的特點？

* Deploying the application across two AWS Regions improves security／跨兩個 AWS 區域部署應用程式可提升安全性
* Deploying the application across two AWS Regions improves agility／跨兩個 AWS 區域部署應用程式可提升敏捷性
* Deploying the application across two AWS Regions improves scalability／跨兩個 AWS 區域部署應用程式可提升可擴展性
* Deploying the application across two AWS Regions improves availability／跨兩個 AWS 區域部署應用程式可提升可用性

---

## Q38
A cargo shipping company runs CRM applications that need to be accessible 24*7 but can be managed on fewer instances during a disaster for some time. Which disaster recovery strategy is well-suited and cost-effective?
一家貨運公司執行需要全天候存取的 CRM 應用程式，但在災難期間可以暫時在較少的執行個體上管理。哪種災難恢復策略既適合又具成本效益？

* Multi-site active-active strategy／多站點主動-主動策略
* Pilot Light strategy／試點燈策略
* Backup & Restore strategy／備份與還原策略
* Warm Standby strategy／暖待機策略

---

## Q39
AWS Marketplace facilitates which of the following use-cases? (Select two)
AWS Marketplace 促進以下哪些使用案例？（選兩項）

* Purchase compliance documents from third-party vendors／向第三方供應商購買合規文件
* Buy Amazon EC2 Standard Reserved Instances (RI)／購買 Amazon EC2 標準保留執行個體
* Raise request for purchasing AWS Direct Connect connection／提出購買 AWS Direct Connect 連線的請求
* Sell Software as a Service (SaaS) solutions to AWS customers／向 AWS 客戶銷售 SaaS 解決方案
* AWS customer can buy software bundled into customized AMIs by AWS Marketplace sellers／AWS 客戶可以購買由 AWS Marketplace 賣家捆綁至自訂 AMI 中的軟體

---

## Q40
Which AWS service can be used to set up billing alarms to monitor estimated charges on your AWS account?
哪個 AWS 服務可用於設定帳單警報以監控 AWS 帳戶的預估費用？

* AWS Organizations
* AWS Cost Explorer
* AWS CloudTrail
* Amazon CloudWatch

---

## Q41
Which benefit of Cloud Computing allows AWS to offer lower pay-as-you-go prices as usage from hundreds of thousands of customers is aggregated in the cloud?
雲端運算的哪項優勢使 AWS 能夠在數十萬客戶的使用量聚合到雲端時提供更低的隨用隨付價格？

* Increased speed and agility／提升速度和敏捷性
* Trade capital expense for variable expense／以資本支出換取可變支出
* Go global in minutes／幾分鐘內實現全球化
* Massive economies of scale／大規模規模經濟

---

## Q42
An e-commerce company would like to receive alerts when the Amazon EC2 Reserved Instances (RI) utilization drops below a certain threshold. Which AWS service can be used to address this use-case?
一家電子商務公司希望在 Amazon EC2 保留執行個體（RI）使用率低於某個閾值時收到警報。哪個 AWS 服務可以解決此使用案例？

* AWS Cost Explorer
* AWS Systems Manager
* AWS Trusted Advisor
* AWS Budgets

---

## Q43
Which of the following AWS entities lists all users in your account and the status of their various account aspects such as passwords, access keys, and MFA devices?
以下哪個 AWS 實體列出帳戶中所有使用者及其各種帳戶方面的狀態（如密碼、存取金鑰和 MFA 裝置）？

* AWS Trusted Advisor
* AWS Cost & Usage Report (AWS CUR)
* Amazon Inspector
* Credentials Report／憑證報告

---

## Q44
Which of the following entities are part of an Amazon VPC in the AWS Cloud? (Select two)
以下哪些實體是 AWS 雲端中 Amazon VPC 的一部分？（選兩項）

* AWS Storage Gateway
* Object／物件
* API Gateway
* Subnet／子網路
* Internet Gateway／網際網路閘道

---

## Q45
Which AWS service will you use to provision the same AWS infrastructure across multiple AWS accounts and regions?
您會使用哪個 AWS 服務在多個 AWS 帳戶和區域中佈建相同的 AWS 基礎設施？

* AWS CodeDeploy
* AWS Systems Manager
* AWS Config
* AWS CloudFormation

---

## Q46
Which AWS entity enables you to privately connect your Amazon VPC to an Amazon SQS queue?
哪個 AWS 實體使您能夠將 Amazon VPC 私下連接至 Amazon SQS 佇列？

* AWS Direct Connect
* VPC Gateway Endpoint／VPC 閘道端點
* Internet Gateway／網際網路閘道
* VPC Interface Endpoint／VPC 介面端點

---

## Q47
AWS Organizations provides which of the following benefits? (Select two)
AWS Organizations 提供以下哪些優點？（選兩項）

* Deploy patches on Amazon EC2 instances across the member AWS accounts／在成員 AWS 帳戶的 Amazon EC2 執行個體上部署修補程式
* Provision Amazon EC2 Spot instances across the member AWS accounts／在成員 AWS 帳戶中佈建 Amazon EC2 Spot 執行個體
* Check vulnerabilities on Amazon EC2 instances across the member AWS accounts／檢查成員 AWS 帳戶中 Amazon EC2 執行個體的漏洞
* Volume discounts for Amazon EC2 and Amazon S3 aggregated across the member AWS accounts／跨成員 AWS 帳戶聚合的 Amazon EC2 和 Amazon S3 批量折扣
* Share the reserved Amazon EC2 instances amongst the member AWS accounts／在成員 AWS 帳戶之間共享保留的 Amazon EC2 執行個體

---

## Q48
Which of the following entities can be used to connect to an Amazon EC2 server from a Mac OS, Windows or Linux based computer via a browser-based client?
以下哪個實體可用於透過瀏覽器用戶端從 Mac OS、Windows 或 Linux 電腦連接至 Amazon EC2 伺服器？

* SSH
* AWS Direct Connect
* Putty
* Amazon EC2 Instance Connect

---

## Q49
Which of the following is the MOST cost-effective Amazon EC2 instance purchasing option for short-term, spiky and critical workloads on AWS Cloud?
以下哪個是 AWS 雲端上短期、突發性和關鍵工作負載最具成本效益的 Amazon EC2 執行個體購買選項？

* Reserved Instance (RI)／保留執行個體
* Spot Instance／Spot 執行個體
* Dedicated Host／專用主機
* On-Demand Instance／隨需執行個體

---

## Q50
Which of the following Amazon S3 storage classes do not charge any data retrieval fee? (Select two)
以下哪些 Amazon S3 儲存類別不收取任何資料取得費用？（選兩項）

* Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)
* Amazon S3 Standard-Infrequent Access (S3 Standard-IA)
* Amazon S3 Glacier Flexible Retrieval
* Amazon S3 Intelligent-Tiering
* Amazon S3 Standard

---

## Q51
Which of the following AWS services can be used to forecast your AWS account usage and costs?
以下哪個 AWS 服務可用於預測您的 AWS 帳戶使用量和成本？

* AWS Cost & Usage Report (AWS CUR)
* AWS Pricing Calculator
* AWS Budgets
* AWS Cost Explorer

---

## Q52
Which of the following AWS storage services can be directly used with on-premises systems?
以下哪個 AWS 儲存服務可直接與本地系統搭配使用？

* Amazon EC2 Instance Store
* Amazon Simple Storage Service (Amazon S3)
* Amazon Elastic Block Store (Amazon EBS)
* Amazon Elastic File System (Amazon EFS)

---

## Q53
Which of the following entities should be used for an Amazon EC2 Instance to access a DynamoDB table?
以下哪個實體應用於 Amazon EC2 執行個體存取 DynamoDB 資料表？

* AWS Key Management Service (KMS)
* Amazon Cognito
* AWS IAM user access keys／AWS IAM 使用者存取金鑰
* IAM role／IAM 角色

---

## Q54
A financial services company wants to compare the cost of running their IT infrastructure on-premises vs AWS Cloud. Which AWS service would you recommend?
一家金融服務公司希望比較在本地與 AWS 雲端執行 IT 基礎設施的成本。您會推薦哪個 AWS 服務？

* AWS Cost Explorer
* AWS Trusted Advisor
* AWS Budgets
* AWS Pricing Calculator

---

## Q55
A social media company wants to have the MOST cost-optimal strategy for deploying Amazon EC2 instances. Which of the following options would you recommend? (Select two)
一家社群媒體公司希望制定最具成本效益的 Amazon EC2 執行個體部署策略。您會推薦以下哪些選項？（選兩項）

* Use On-Demand Instances for ad-hoc jobs that can be interrupted／使用隨需執行個體執行可被中斷的臨時作業
* Use On-Demand Instances to run applications with a predictable usage over the next one year／使用隨需執行個體執行未來一年具有可預測使用量的應用程式
* Use Reserved Instances (RI) for ad-hoc jobs that can be interrupted／使用保留執行個體執行可被中斷的臨時作業
* Use Spot Instances for ad-hoc jobs that can be interrupted／使用 Spot 執行個體執行可被中斷的臨時作業
* Use Reserved Instances (RI) to run applications with a predictable usage over the next one year／使用保留執行個體執行未來一年具有可預測使用量的應用程式

---

## Q56
AWS Trusted Advisor can provide alerts on which of the following common security misconfigurations? (Select two)
AWS Trusted Advisor 可以針對以下哪些常見安全設定錯誤提供警報？（選兩項）

* When you don't enable data encryption on Amazon S3 Glacier／當您未在 Amazon S3 Glacier 上啟用資料加密時
* When you don't tag objects in Amazon S3 buckets／當您未在 Amazon S3 儲存貯體中為物件加上標籤時
* When you share IAM user credentials with others／當您與他人共享 IAM 使用者憑證時
* When you don't turn on user activity logging (AWS CloudTrail)／當您未開啟使用者活動日誌記錄（AWS CloudTrail）時
* When you allow public access to Amazon S3 buckets／當您允許公開存取 Amazon S3 儲存貯體時

---

## Q57
Which of the following is a perspective of the AWS Cloud Adoption Framework (AWS CAF)?
以下哪項是 AWS 雲端採用框架（AWS CAF）的觀點？

* Product／產品
* Process／流程
* Architecture／架構
* Business／業務

---

## Q58
Which AWS service can be used to host a static website with the LEAST effort?
哪個 AWS 服務可以以最少的工作量託管靜態網站？

* AWS Storage Gateway
* Amazon S3 Glacier
* Amazon Elastic File System (Amazon EFS)
* Amazon Simple Storage Service (Amazon S3)

---

## Q59
Which of the following can you use to run a bootstrap script while launching an Amazon EC2 instance?
以下哪項可讓您在啟動 Amazon EC2 執行個體時執行啟動程序腳本？

* Amazon EC2 instance AMI data／Amazon EC2 執行個體 AMI 資料
* Amazon EC2 instance metadata／Amazon EC2 執行個體中繼資料
* Amazon EC2 instance configuration data／Amazon EC2 執行個體設定資料
* Amazon EC2 instance user data／Amazon EC2 執行個體使用者資料

---

## Q60
Which entity ensures that your application on Amazon EC2 always has the right amount of capacity to handle the current traffic demand?
哪個實體確保您在 Amazon EC2 上的應用程式始終擁有適當的容量來處理當前的流量需求？

* Application Load Balancer／應用程式負載平衡器
* Multi-AZ deployment／多 AZ 部署
* Network Load Balancer／網路負載平衡器
* Amazon EC2 Auto Scaling

---

## Q61
Which of the following are recommended security best practices for the AWS account root user? (Select two)
以下哪些是 AWS 帳戶根使用者的推薦安全最佳實務？（選兩項）

* Keep your AWS account root user access keys in an encrypted file on Amazon S3／將 AWS 帳戶根使用者存取金鑰保存在 Amazon S3 的加密檔案中
* Disable MFA for the root user as it can lock the entire AWS account if the MFA device is lost／停用根使用者的 MFA，因為若 MFA 裝置遺失可能會鎖定整個 AWS 帳戶
* Share AWS account root user access keys with other administrators／與其他管理員共享 AWS 帳戶根使用者存取金鑰
* Enable multi-factor authentication (MFA) for the AWS account root user／為 AWS 帳戶根使用者啟用多重要素驗證（MFA）
* Set up an IAM user with administrator permissions and do not use AWS account root user for administrative tasks／設定具有管理員權限的 IAM 使用者，不要將 AWS 帳戶根使用者用於管理任務

---

## Q62
Reserved Instance (RI) pricing is available for which of the following AWS services? (Select two)
保留執行個體（RI）定價適用於以下哪些 AWS 服務？（選兩項）

* Amazon Simple Storage Service (Amazon S3)
* Amazon CloudFront
* AWS Identity and Access Management (AWS IAM)
* Amazon Elastic Compute Cloud (Amazon EC2)
* Amazon Relational Database Service (Amazon RDS)

---

## Q63
A firm wants to maintain the same data on Amazon S3 between its production account and multiple test accounts, retaining object metadata. Which technique should you choose?
一家公司希望在其生產帳戶和多個測試帳戶之間在 Amazon S3 上維護相同的資料，同時保留物件中繼資料。您應選擇哪種技術？

* Amazon S3 Bucket Policy／Amazon S3 儲存貯體政策
* Amazon S3 Storage Classes／Amazon S3 儲存類別
* Amazon S3 Transfer Acceleration (Amazon S3TA)
* Amazon S3 Replication／Amazon S3 複寫

---

## Q64
The QA team at a company wants a tool/service that can provide access to different mobile devices with variations in firmware and Operating System versions. Which AWS service can address this use case?
一家公司的 QA 團隊需要一個工具/服務，可以存取具有不同韌體和作業系統版本的各種行動裝置。哪個 AWS 服務可以解決此使用案例？

* AWS Elastic Beanstalk
* AWS Mobile Farm
* AWS CodePipeline
* AWS Device Farm

---

## Q65
Which of the following AWS Support plans provide programmatic access to AWS Support Center features to create, manage and close your support cases? (Select two)
以下哪些 AWS Support 方案提供對 AWS Support Center 功能的程式化存取，以建立、管理和關閉支援案例？（選兩項）

* AWS Developer Support
* AWS Basic Support
* AWS Corporate Support
* AWS Enterprise Support
* AWS Business Support
