# AWS Cloud Practitioner【TEST06】

---

## Questions (1–5)

(1) A company provides you with a completed product that is run and managed by the company itself
Ans: Software as a Service (SaaS)

(2) flexible pricing model — AWS offers two types of Savings Plans
Ans: Compute Savings Plans / EC2 Instance Savings Plans

(3) make its desktop applications available from browsers on devices/laptops without procuring servers or maintaining infrastructure
Ans: Amazon AppStream 2.0

(4) be considered when choosing an AWS Region
Ans: Compliance and Data Residency guidelines should match your business requirements / AWS Region chosen should be geographically closer to the user base

(5) moving its CRM application running on MySQL to an AWS database service
Ans: Amazon Aurora

---

(1)
中文題目：某公司提供你一個已完成的產品，由該公司自行運作與管理，這屬於哪種雲端服務模型？
答案：Software as a Service，SaaS（軟體即服務）
解析：雲端服務三大模型：
- **IaaS（基礎設施即服務）**：提供虛擬化基礎設施，客戶管理 OS 以上層級，如 Amazon EC2
- **PaaS（平台即服務）**：提供應用程式執行平台，客戶只需部署程式碼，如 Elastic Beanstalk
- **SaaS（軟體即服務）**：**完整的軟體產品由服務提供商運作與管理**，使用者只需使用功能，無需管理任何基礎設施，如 Gmail、Salesforce、Amazon Rekognition
題目關鍵字「completed product + run and managed by the company itself」完全對應 SaaS 定義。

(2)
中文題目：AWS 彈性定價模型提供哪兩種 Savings Plans 類型？
答案：Compute Savings Plans / EC2 Instance Savings Plans
解析：**AWS Savings Plans** 是承諾使用量換取折扣的彈性方案，分為三種：
- **Compute Savings Plans**：最靈活，適用於 EC2（任何執行個體系列、大小、Region、OS）、AWS Fargate、Lambda，折扣最高 66%
- **EC2 Instance Savings Plans**：僅適用於特定 Region 與執行個體系列的 EC2，折扣最高 72%（比 Compute SP 更高），但靈活性較低
- **SageMaker Savings Plans**：適用於 Amazon SageMaker
考試常考：Compute SP 最靈活但折扣稍低；EC2 Instance SP 折扣最高但限制最多。

(3)
中文題目：哪項 AWS 服務可讓企業的桌面應用程式從瀏覽器在裝置或筆電上存取，且無需採購伺服器或維護基礎設施？
答案：Amazon AppStream 2.0
解析：**Amazon AppStream 2.0** 是全受管的應用程式串流服務：
- 將桌面應用程式在 AWS 雲端執行，透過瀏覽器串流至任何裝置
- 使用者無需在本地安裝軟體，只需瀏覽器即可存取
- 企業無需管理底層伺服器或基礎設施
- 適合：設計軟體（AutoCAD）、工程工具、教育訓練應用、需要高效能 GPU 的應用
與 **Amazon WorkSpaces** 差異：WorkSpaces 提供完整虛擬桌面（VDI）；AppStream 2.0 只串流特定應用程式。

(4)
中文題目：選擇 AWS Region 時應考量哪些因素？
答案：
- 合規與資料主權要求應符合業務需求
- 選擇的 AWS Region 應在地理位置上靠近使用者群
解析：**選擇 AWS Region 的四大考量因素**：
- **Compliance & Data Residency（合規與資料主權）**：某些法規（GDPR、LGPD）要求資料必須儲存在特定地理範圍內，必須選擇符合要求的 Region
- **Proximity to Users（靠近使用者）**：選擇地理位置靠近主要使用者群的 Region，降低網路延遲，提升使用體驗
- **Service Availability（服務可用性）**：並非所有服務在所有 Region 都可用
- **Pricing（定價）**：不同 Region 的定價不同

(5)
中文題目：企業想將 MySQL 上的 CRM 應用程式遷移至 AWS 資料庫服務，應選擇哪項服務？
答案：Amazon Aurora
解析：**Amazon Aurora** 是 AWS 的高效能受管關聯式資料庫，具備兩大重要特性：
- **MySQL 相容**：完全相容 MySQL，CRM 應用程式無需修改程式碼即可遷移
- **高效能**：吞吐量比標準 MySQL 高出最多 5 倍，並提供自動容錯、自動擴縮儲存（最高 128TB）
- **全受管**：AWS 負責備份、修補、Multi-AZ 高可用性
與 **RDS for MySQL** 差異：Aurora 效能更高、儲存架構更先進，但費用略高；若追求最大相容性且成本敏感，也可選 RDS MySQL。

---

## Questions (6–10)

(6) needs data about configuration changes for AWS resources during the past two weeks
Ans: AWS Config

(7) offers a graphical user interface to manage AWS Snowball devices without needing CLI
Ans: AWS OpsHub

(8) needs to generate custom reports and interactive dashboards for analyzing product sales data, accessible from any device
Ans: Amazon QuickSight

(9) needs real-time processing of streaming big data for their ad-tech platform
Ans: Amazon Kinesis Data Streams

(10) used to store and commit code privately and offers features for version control
Ans: AWS CodeCommit

---

(6)
中文題目：哪項 AWS 服務可提供過去兩週內帳戶中 AWS 資源組態變更的資料？
答案：AWS Config
解析：**AWS Config** 持續記錄 AWS 資源的組態狀態與變更歷史：
- 提供資源組態的**時間軸（Configuration Timeline）**，可回溯查詢任意時間點的資源狀態
- 記錄「什麼資源在什麼時間被誰變更為何種組態」
- 預設保留組態歷史記錄，方便合規稽核與問題排查
與 **CloudTrail** 差異：CloudTrail 記錄「誰執行了哪個 API 操作」（操作層級）；Config 記錄「資源組態本身的狀態如何變化」（資源狀態層級），兩者互補。

(7)
中文題目：哪項 AWS 工具提供圖形化使用者介面，讓使用者無需命令列即可管理 AWS Snowball 裝置？
答案：AWS OpsHub
解析：**AWS OpsHub** 是 Snow 家族裝置的圖形化管理工具：
- 安裝於本地電腦，提供直覺的 GUI 介面
- 管理 Snowball Edge 與 Snowcone 裝置（解鎖裝置、傳輸資料、啟動 EC2 執行個體）
- 無需熟悉命令列介面（CLI），降低使用門檻
- 適合非技術人員或需要快速操作的現場部署場景
在 OpsHub 推出前，管理 Snowball 裝置需透過 CLI，OpsHub 大幅簡化了操作流程。

(8)
中文題目：哪項 AWS 服務可針對產品銷售資料生成自訂報告與互動式儀表板，且可從任何裝置存取？
答案：Amazon QuickSight
解析：**Amazon QuickSight** 是 AWS 的雲端商業智慧（BI）服務：
- 建立互動式圖表、儀表板與自訂報告
- **跨裝置存取**：透過瀏覽器在電腦、平板、手機皆可存取
- 支援多種資料來源：S3、Redshift、RDS、Athena、Salesforce 等
- **SPICE 引擎**：超快速平行記憶體計算引擎，提供毫秒級查詢回應
- 按使用量計費（Reader/Author 授權），無需管理伺服器
是 AWS 生態系中取代傳統 BI 工具（Tableau、Power BI）的雲端原生選擇。

(9)
中文題目：哪項 AWS 服務可滿足廣告技術平台的即時串流大數據處理需求？
答案：Amazon Kinesis Data Streams
解析：**Amazon Kinesis Data Streams** 是即時資料串流服務：
- 即時收集、處理與分析**串流資料**（每秒數 GB 規模）
- 資料保留最長 7 天（預設 24 小時），支援多個消費者同時讀取
- 適合廣告點擊流（Ad Click Stream）分析、即時競價（Real-Time Bidding）、日誌監控、IoT 資料
Kinesis 家族比較：
- **Kinesis Data Streams**：即時串流資料擷取，需自行管理消費者邏輯
- **Kinesis Data Firehose**：全受管，自動載入至 S3/Redshift/Elasticsearch，無需寫消費者程式碼
- **Kinesis Data Analytics**：對串流資料執行 SQL 分析

(10)
中文題目：哪項 AWS 服務用於私下儲存與提交程式碼，並提供版本控制功能？
答案：AWS CodeCommit
解析：**AWS CodeCommit** 是 AWS 的全受管 Git 原始碼版本控制服務：
- 私有 Git 儲存庫，程式碼儲存於 AWS，安全加密
- 與 AWS IAM 整合，提供細粒度的存取控制
- 支援標準 Git 工作流程（branch、merge、pull request）
- 與 CodeBuild、CodeDeploy、CodePipeline 整合，構建完整 CI/CD 流水線
注意：2024年7月 AWS 宣布 CodeCommit 停止接受新客戶，現有客戶仍可使用，但新專案建議考慮 GitHub、GitLab 等替代方案。

---

## Questions (11–15)

(11) true about AWS Regions and Availability Zones (AZ)
Ans: Each AWS Region consists of multiple, isolated, and physically separate AZs / All traffic between AZs is encrypted

(12) used by Amazon Detective to analyze events and identify potential security issues
Ans: AWS CloudTrail logs / Amazon VPC Flow Logs / Amazon GuardDuty findings

(13) true about AWS Shared Responsibility Model
Ans: AWS trains AWS employees, but customers must train their own employees / AWS patches infrastructure, but customers patch their guest OS and applications

(14) are encrypted by default and need no user intervention
Ans: AWS CloudTrail Logs / Amazon S3 Glacier / AWS Storage Gateway

(15) on-premises NFS file system accessed in parallel by multiple applications — moving to AWS
Ans: Amazon Elastic File System (Amazon EFS)

---

(11)
中文題目：關於 AWS Region 與可用區（AZ），哪些描述是正確的？
答案：
- 每個 AWS Region 由多個、隔離的、實體分離的 AZ 組成
- 所有 AZ 之間的流量皆經過加密
解析：**AWS 基礎設施架構重點**：
- **多個 AZ**：每個 Region 最少 3 個 AZ（目前多數 Region 有 3-6 個）
- **實體隔離**：不同 AZ 有獨立的電力、冷卻、網路，防止單點故障波及多個 AZ
- **AZ 間流量加密**：AWS 在 AZ 之間的私有網路流量上使用加密，確保資料傳輸安全
- AZ 之間距離足夠遠（防災），但夠近（低延遲，通常 < 2ms）以支援同步複寫

(12)
中文題目：Amazon Detective 使用哪些資料來源分析事件並識別潛在安全問題？
答案：AWS CloudTrail logs / Amazon VPC Flow Logs / Amazon GuardDuty findings
解析：**Amazon Detective** 是安全調查服務，自動收集並分析以下資料來源：
- **AWS CloudTrail logs**：API 呼叫記錄，追蹤使用者與資源的操作行為
- **Amazon VPC Flow Logs**：網路流量記錄，分析異常連線模式
- **Amazon GuardDuty findings**：威脅偵測結果，作為調查起點
Detective 使用機器學習與圖形分析，將這三種資料來源整合，提供視覺化的安全事件時間軸與關聯圖，協助資安團隊快速進行根本原因分析（Root Cause Analysis）。

(13)
中文題目：關於 AWS 共同責任模型，哪些描述是正確的？
答案：
- AWS 訓練 AWS 員工，但客戶必須自行訓練其員工
- AWS 負責修補基礎設施，但客戶負責修補其 Guest OS 與應用程式
解析：**人員訓練的責任劃分**：
- **AWS 側**：負責訓練 AWS 資料中心、網路、硬體的操作人員
- **客戶側**：負責訓練自己的開發人員、系統管理員、資安人員使用 AWS 服務
**修補（Patching）責任劃分**：
- **AWS 負責**：實體硬體韌體、Hypervisor、受管服務（RDS、Lambda）的底層 OS
- **客戶負責**：EC2 上的 Guest OS 更新修補、自行部署的應用程式修補

(14)
中文題目：哪些 AWS 服務預設即啟用加密，且無需使用者介入？
答案：AWS CloudTrail Logs / Amazon S3 Glacier / AWS Storage Gateway
解析：**預設加密的 AWS 服務**：
- **AWS CloudTrail Logs**：日誌檔案自動使用 SSE-S3 加密儲存於 S3
- **Amazon S3 Glacier**：所有儲存於 Glacier 的封存資料預設使用 AES-256 加密
- **AWS Storage Gateway**：傳輸至 AWS 的資料使用 SSL/TLS 加密，儲存時自動加密
- **Amazon S3**（2023年後）：所有新上傳物件預設 SSE-S3 加密
以上服務皆無需手動啟用加密，開箱即受保護。

(15)
中文題目：本地端使用 NFS 檔案系統，可被多個應用程式平行存取，遷移至 AWS 應選擇哪項服務？
答案：Amazon Elastic File System，Amazon EFS
解析：本題的關鍵需求對應分析：
- **NFS 協定**：EFS 原生支援 NFS v4.1/v4.0 協定，完全相容現有 NFS 客戶端
- **多個應用程式平行存取**：EFS 支援數千個 EC2 執行個體同時掛載並並行讀寫
- **跨 AZ 可用**：EFS 自動跨多個 AZ 冗餘儲存，高可用性
遷移時，本地 NFS 應用程式幾乎無需修改即可切換至 EFS，是 NFS 工作負載遷移 AWS 的最佳路徑。

---

## Questions (16–20)

(16) for research and can tolerate data loss of a few hours
Ans: Backup and restore strategy（備份與還原策略）

(17) wants rapid deployment and minimal setup time — which cloud computing advantages
Ans: Increase speed and agility / Enable automatic scaling of resources based on demand

(18) security best practices suggested by AWS for IAM
Ans: Do not share security credentials between accounts, use IAM roles instead / When creating IAM policies, grant the least privileges required to perform a task

(19) feature of AWS Cloud that refers to right-sizing the resources
Ans: Elasticity（彈性）

(20) AWS Shared Responsibility Model — which AWS service is the responsibility of the customer
Ans: Amazon Elastic Compute Cloud (Amazon EC2)

---

(16)
中文題目：企業用於研究且可容忍數小時資料遺失，應選擇哪種災難復原策略？
答案：Backup and restore strategy（備份與還原策略）
解析：AWS 四種 DR 策略的 RTO/RPO 比較（由慢到快）：
- **Backup & Restore**：定期備份資料，災難時從備份重建，**RTO/RPO 最長（數小時）**，成本最低
- **Pilot Light**：核心服務持續運行，災難時快速擴展，RTO 數十分鐘
- **Warm Standby**：縮小規模環境持續運行，RTO 數分鐘
- **Multi-Site Active-Active**：完整雙環境，RTO 接近零，成本最高
題目關鍵字「tolerate data loss of a few hours（可容忍數小時資料遺失）」對應最高 RPO 的 **Backup & Restore** 策略，也是成本最低的選擇，符合研究環境的需求。

(17)
中文題目：企業想要快速部署與最短設定時間，這對應雲端運算的哪些優勢？
答案：提升速度與敏捷性（Increase speed and agility）/ 依需求自動擴展資源
解析：
- **Increase Speed and Agility（速度與敏捷性）**：雲端資源幾分鐘內即可取得，相較傳統 IT 採購（數週至數月），大幅縮短從構想到部署的時間，「rapid deployment + minimal setup time」直接對應此優勢
- **Automatic Scaling（自動擴展）**：Auto Scaling 依需求自動增減資源，無需手動預置，進一步減少設定與管理負擔
兩者共同體現雲端在部署速度與資源彈性方面的核心優勢。

(18)
中文題目：AWS 針對 IAM 建議的安全最佳實踐為何？
答案：
- 不在帳戶間共享安全憑證，改用 IAM Role
- 建立 IAM Policy 時，只授予執行任務所需的最低權限
解析：**IAM 核心安全原則**：
- **不共享憑證**：每個使用者應有獨立的 IAM 帳號，共享憑證無法追蹤操作歸屬，且一旦洩露影響範圍更大；跨服務或跨帳號存取應使用 **IAM Role**（臨時憑證）
- **最小權限原則（Least Privilege）**：只授予完成特定任務所需的最低權限集合，降低憑證洩露或誤操作的影響範圍
其他 IAM 最佳實踐：啟用 MFA、定期輪換憑證、不使用 Root 帳戶日常操作

(19)
中文題目：AWS Cloud 的哪項特性指的是為資源進行右型化（right-sizing）？
答案：Elasticity（彈性）
解析：**Elasticity（彈性）** 在 AWS 語境中的雙重含義：
- **動態擴縮**：依據需求自動增減資源（Scale Out / Scale In）
- **Right-Sizing（右型化）**：為工作負載選擇並動態調整最適合的資源規格，避免過度配置（浪費）或配置不足（效能不佳）
彈性讓企業隨時能精確匹配工作負載所需的資源量，既不多付費也不犧牲效能，是雲端相較傳統固定容量 IT 的核心差異。

(20)
中文題目：在 AWS 共同責任模型中，哪項 AWS 服務的安全主要由客戶負責？
答案：Amazon Elastic Compute Cloud，Amazon EC2
解析：**EC2 是典型的客戶高責任服務（IaaS）**：
- **AWS 負責**：實體主機硬體、Hypervisor、底層網路基礎設施、資料中心實體安全
- **客戶負責**：Guest OS 安裝、修補與更新、應用程式安全、資料加密、Security Group 與 NACL 設定、IAM 存取控制
相比之下，**Amazon S3、Lambda、RDS** 等受管服務的 AWS 責任範圍更大（負責底層 OS 與平台），客戶只需管理應用層。EC2 是客戶責任最重的 AWS 服務之一。

---

## Questions (21–25)

(21) realized that AWS-owned IP addresses are being used for port scanning your on-premises server
Ans: Contact AWS Abuse Team

(22) break down AWS spending so each department and project can be accurately charged
Ans: AWS cost allocation tags

(23) establish a private, dedicated connection between AWS and its on-premises data center
Ans: AWS Direct Connect

(24) least effort way to encrypt data for AWS services only in your account using AWS KMS
Ans: Use AWS managed master keys that are automatically created in your account for each service

(25) wants to build a knowledge graph by leveraging a fully managed database
Ans: Amazon Neptune

---

(21)
中文題目：企業發現 AWS 擁有的 IP 位址正被用於對其本地端伺服器進行連接埠掃描，應如何處理？
答案：聯絡 AWS Abuse Team（AWS 濫用回報團隊）
解析：**AWS Abuse Team** 專門處理 AWS 資源被濫用的情況：
- 回報途徑：透過 AWS 官網的 Report Amazon AWS Abuse 表單，或寄信至 abuse@amazonaws.com
- 處理範圍：來自 AWS IP 的 DDoS 攻擊、連接埠掃描（Port Scanning）、垃圾郵件、惡意軟體散佈
- AWS 會調查並對違規帳戶採取措施
注意：若是自己的 AWS 帳戶遭入侵被用於攻擊，應同時聯絡 AWS Support 進行帳戶安全事件回應，並立即輪換所有憑證。

(22)
中文題目：如何分解 AWS 支出，讓每個部門與專案都能準確計費？
答案：AWS cost allocation tags（AWS 成本分配標籤）
解析：**Cost Allocation Tags** 是 AWS 成本追蹤的核心工具：
- 為每個 AWS 資源加上標籤（如 Department: Engineering、Project: Phoenix）
- 在 **AWS Billing Console** 啟用成本分配標籤
- 之後在 **Cost Explorer** 與 **Cost & Usage Report** 可依標籤分組，查看各部門、各專案的精確費用
- 支援 AWS 產生的標籤（如 aws:createdBy）與使用者自訂標籤
最佳實踐：制定全組織統一的標籤命名規範，並使用 AWS Config Rules 強制執行標籤合規，確保所有資源都有正確標籤。

(23)
中文題目：哪項 AWS 服務可在 AWS 與本地端資料中心之間建立私有、專用的連線？
答案：AWS Direct Connect
解析：**AWS Direct Connect** 的核心特性：
- **私有（Private）**：不經過公共網際網路，流量在專用實體線路上傳輸
- **專用（Dedicated）**：企業獨享的實體光纖連線，不與其他客戶共享頻寬
- 提供穩定低延遲、固定頻寬（1/10/100 Gbps 可選）
- 滿足對網路品質要求嚴格的場景：大量資料傳輸、即時應用、法規要求不走公網
與 **Site-to-Site VPN** 差異：VPN 透過公網加密傳輸，設定快但穩定性受公網影響；Direct Connect 實體專線，穩定但建置時間較長（數週）。

(24)
中文題目：使用 AWS KMS 為帳戶內的 AWS 服務加密資料，哪種方式最省力？
答案：使用 AWS 為每項服務自動在帳戶中建立的 AWS 受管主金鑰（AWS Managed Master Keys）
解析：**AWS KMS 金鑰類型**比較：
- **AWS Owned Keys（AWS 擁有金鑰）**：完全由 AWS 管理，客戶不可見，多服務共用，免費
- **AWS Managed Keys（AWS 受管金鑰）**：AWS 在客戶帳戶中為每項服務自動建立（如 aws/s3、aws/rds），客戶可查看但不能直接管理，**使用最省力，幾乎零設定**，免費
- **Customer Managed Keys（CMK，客戶自管金鑰）**：客戶完全控制（建立、輪換、刪除、設定 Policy），彈性最高，但需自行管理，每月每個金鑰 $1
題目強調「least effort（最省力）」對應 **AWS Managed Keys**。

(25)
中文題目：哪項 AWS 服務可讓企業利用全受管資料庫建立知識圖譜（knowledge graph）？
答案：Amazon Neptune
解析：**Amazon Neptune** 是 AWS 的全受管圖形資料庫服務：
- 專為**高度連接的資料**設計，如社交網路、知識圖譜、推薦引擎、詐欺偵測
- 支援兩種圖形查詢語言：**Apache TinkerPop Gremlin**（屬性圖）和 **W3C SPARQL**（RDF 語義圖）
- **知識圖譜（Knowledge Graph）**：將實體（Entity）與關係（Relationship）以圖形結構表示，如 Google 的知識圖譜
- 完全受管，自動跨 AZ 複寫，6 份資料副本，高可用性

---

## Questions (26–30)

(26) correct regarding AWS Elastic Beanstalk health monitoring
Ans: Health monitoring can determine that the Auto Scaling group is available and has at least one instance / With basic health reporting, Elastic Beanstalk does not publish any metrics to Amazon CloudWatch

(27) recommend for signing in to the AWS Management Console to meet security best practices
Ans: IAM Username and password / Multi Factor Authentication (MFA)

(28) correct regarding AWS Support Plans
Ans: A designated TAM is available only for AWS Enterprise Support plan / Both Basic and Developer plans have access to core Trusted Advisor checks only

(29) needs AWS infrastructure, services, APIs, and tools in its on-premises data center for running low latency applications
Ans: AWS Outposts

(30) needs an easy solution to host WordPress blogs without managing servers or databases
Ans: Amazon Lightsail

---

(26)
中文題目：關於 AWS Elastic Beanstalk 健康監控，哪些描述是正確的？
答案：
- Beanstalk 健康監控可判斷環境的 Auto Scaling 群組是否可用且至少有一個執行個體
- 基本健康回報模式下，Beanstalk 不會發布任何指標至 Amazon CloudWatch
解析：**Elastic Beanstalk 健康監控**分為兩種模式：
- **Basic Health Reporting（基本健康回報）**：檢查 Auto Scaling 群組與 ELB 的基本狀態（是否有執行個體在運行），**不發布自訂指標至 CloudWatch**，僅在 Beanstalk Console 顯示顏色狀態（Green/Yellow/Red）
- **Enhanced Health Reporting（增強健康回報）**：提供更詳細的執行個體與應用程式健康指標，**會發布至 CloudWatch**，需額外費用
Basic 模式的限制是無法設定 CloudWatch 警示，需升級至 Enhanced 模式。

(27)
中文題目：登入 AWS Management Console 時，哪些做法符合安全最佳實踐？
答案：IAM 使用者名稱與密碼 / 多因素驗證（MFA）
解析：**AWS Console 登入安全最佳實踐**：
- **使用 IAM 使用者**（而非 Root 帳戶）：每人一個 IAM 帳戶，有獨立的使用者名稱與密碼，操作可追溯
- **啟用 MFA（Multi-Factor Authentication）**：在密碼之外加入第二層驗證（Authenticator App、硬體金鑰），即使密碼洩露也能防止未授權存取
兩者搭配是 Console 存取的安全基準。進階建議：使用 **AWS IAM Identity Center（SSO）** 集中管理多帳戶的 Console 存取。

(28)
中文題目：關於 AWS Support 方案，哪些描述是正確的？
答案：
- 專屬 TAM 僅在 AWS Enterprise Support 方案中提供
- Basic 與 Developer 方案只能存取核心 Trusted Advisor 檢查
解析：**AWS Support 方案重要差異**：
- **TAM（Technical Account Manager）**：只有 **Enterprise Support** 提供專屬 TAM（Enterprise On-Ramp 提供共享 TAM 存取），Business 方案不包含
- **Trusted Advisor 存取**：
  - **Basic / Developer**：僅 7 項核心安全與服務限制檢查
  - **Business / Enterprise**：全部 100+ 項檢查（涵蓋成本優化、效能、安全、容錯、服務限制）
這兩點是考試高頻考題，務必記住。

(29)
中文題目：哪項 AWS 服務可讓企業在自有本地端資料中心使用 AWS 基礎設施、服務、API 與工具，以執行低延遲應用程式？
答案：AWS Outposts
解析：**AWS Outposts** 將 AWS 基礎設施延伸至客戶的本地端資料中心：
- AWS 實際運送並安裝 **Outposts 機架或伺服器**至客戶場所
- 客戶可在本地使用 AWS 原生服務（EC2、EBS、RDS、ECS 等）
- 使用與 AWS Cloud 相同的 API、工具與控制台，真正混合一致性
- 適合：個位數毫秒延遲需求、資料主權要求、無法傳送至雲端的資料處理
與 **Local Zones** 差異：Local Zones 是 AWS 在都市部署的基礎設施延伸（仍在 AWS 管理的資料中心）；Outposts 將設備實際放入客戶場所。

(30)
中文題目：哪項 AWS 服務提供最簡單的方式託管 WordPress 部落格，且無需管理伺服器或資料庫？
答案：Amazon Lightsail
解析：**Amazon Lightsail** 是 AWS 的輕量雲端服務，特別適合個人網站與小型應用：
- 提供 **WordPress 一鍵部署**範本，幾分鐘內即可上線
- 包含運算、SSD 儲存、資料傳輸、DNS 管理的捆綁固定月費方案
- 無需管理底層伺服器、資料庫、負載平衡器等複雜設定
- 與完整 AWS EC2 + RDS 架構相比，設定複雜度大幅降低
題目關鍵字「easy solution + WordPress + without managing servers or databases」完全對應 Lightsail 的定位。

---

## Questions (31–35)

(31) healthcare company wants continuous replication based disaster recovery and fast recovery
Ans: CloudEndure Disaster Recovery

(32) wants to automate keeping server images up-to-date for both EC2 instances and on-premises systems
Ans: Amazon EC2 Image Builder

(33) covered as part of the AWS Basic Support Plan
Ans: One-on-one responses to account and billing questions / Service health checks

(34) correct regarding AWS Control Tower and Service Control Policies (SCPs)
Ans: AWS Control Tower provides pre-defined blueprints and guardrails for a landing zone / SCPs are a type of organization policy used to manage permissions in your organization

(35) allows you to connect any number of IoT devices to the cloud without provisioning or managing servers
Ans: AWS IoT Core

---

(31)
中文題目：醫療公司需要基於持續複寫的災難復原方案並能快速恢復，應使用哪項服務？
答案：CloudEndure Disaster Recovery
解析：**CloudEndure Disaster Recovery**（現已整合為 **AWS Elastic Disaster Recovery**）的核心特性：
- **持續複寫（Continuous Replication）**：將本地端或雲端伺服器的資料持續同步至 AWS，RPO（復原點目標）可達**秒級**
- **快速恢復（Fast Recovery）**：RTO（復原時間目標）通常在**數分鐘**內
- 自動在 AWS 維護一個低成本的暫存環境（Staging Area），災難時快速啟動完整規模的複本
- 適合需要最低 RPO/RTO 的關鍵業務系統，如醫療、金融
與 Backup & Restore 差異：後者 RPO 為數小時；CloudEndure 可達秒級，是最高等級的 DR 保護。

(32)
中文題目：哪項 AWS 服務可自動化維護 EC2 執行個體與本地端系統的伺服器映像更新？
答案：Amazon EC2 Image Builder
解析：**Amazon EC2 Image Builder** 是自動化映像（AMI）建立與維護服務：
- 定義映像建立流程（安裝軟體、套用修補、安全設定）
- **自動排程**：定期重新建立包含最新 OS 修補與軟體版本的映像
- **支援 EC2 AMI 與 VMware 映像**：可輸出至 EC2 或本地端 VMware 環境
- 內建安全掃描（整合 Amazon Inspector），確保映像無已知漏洞
- 完全免費（只需支付建立映像過程中使用的 EC2 費用）
解決了手動維護映像更新繁瑣、易遺漏修補的痛點。

(33)
中文題目：哪些項目包含在 AWS Basic Support 方案中？
答案：帳戶與帳單問題的一對一回應 / 服務健康檢查
解析：**AWS Basic Support**（所有帳戶預設免費）包含：
- **帳戶與帳單問題（Account & Billing Questions）**：可透過 AWS Support Center 提交，獲得人工一對一回應
- **服務健康檢查（Service Health Checks）**：存取 AWS Health Dashboard 查看服務狀態
- AWS 文件、白皮書、最佳實踐指南
- AWS re:Post（社群論壇）
- 核心 Trusted Advisor 檢查（7 項）
**不包含**：技術支援（需 Developer 以上）、CloudWatch Alarm 協助、Architecture Review

(34)
中文題目：關於 AWS Control Tower 與服務控制政策（SCP），哪些描述是正確的？
答案：
- AWS Control Tower 提供預定義的藍圖與護欄，為新 AWS 帳戶實作落地區（Landing Zone）
- SCP 是一種組織政策，可用於管理組織內的權限
解析：
- **AWS Control Tower**：多帳戶環境的自動化設定服務，提供「Landing Zone」——一套已套用最佳實踐的多帳戶架構，包含：預定義的 OU 結構、帳戶出廠設定、安全護欄（Guardrails）
- **SCP（Service Control Policies）**：AWS Organizations 的政策類型，設定組織單位（OU）或帳戶的**最大可用權限**邊界，即使帳戶內 IAM 管理員也無法超越 SCP 限制
兩者常搭配使用：Control Tower 管理帳戶架構，SCP 提供跨帳戶的一致性權限控制。

(35)
中文題目：哪項 AWS 服務可讓你連接任意數量的 IoT 裝置至雲端，且無需佈建或管理伺服器？
答案：AWS IoT Core
解析：**AWS IoT Core** 是全受管的 IoT 訊息代理與裝置管理服務：
- 無需管理任何伺服器或基礎設施，按訊息量計費
- 支援數十億個裝置同時連接，高度可擴展
- 支援 MQTT、HTTP、WebSocket 等 IoT 標準協定
- 裝置影子（Device Shadow）：維護裝置的最後已知狀態，即使裝置離線也能查詢
- 與 Lambda、Kinesis、S3、DynamoDB 等服務整合，實現完整的 IoT 資料處理流程

---

## Questions (36–40)

(36) help you get a forecast of your spending for the next 12 months
Ans: AWS Cost Explorer

(37) delivered globally rather than regionally
Ans: Amazon WorkSpaces

(38) can continuously monitor both malicious activities and unauthorized behavior to protect AWS accounts and workloads
Ans: Amazon GuardDuty

(39) needs compute and storage services close to edge locations in 5G mobile networks
Ans: AWS Wavelength

(40) focuses on using IT and computing resources efficiently and selecting the right resource types and sizes
Ans: Performance Efficiency Pillar

---

(36)
中文題目：哪項 AWS 服務可協助預測未來 12 個月的支出？
答案：AWS Cost Explorer
解析：**AWS Cost Explorer** 的費用預測功能：
- 基於過去 12 個月的使用量歷史，使用機器學習模型**預測未來最多 12 個月**的費用
- 提供信賴區間（Confidence Interval），顯示預測的高低範圍
- 可依服務、Region、使用類型等維度篩選預測
- 協助企業提前規劃預算，識別費用異常趨勢
題目關鍵字「forecast + next 12 months」直接對應 Cost Explorer 的預測功能。

(37)
中文題目：哪項 AWS 服務以全球（而非區域性）方式交付？
答案：Amazon WorkSpaces
解析：**Amazon WorkSpaces** 是 AWS 的虛擬桌面基礎設施（VDI）服務：
- 在全球多個 AWS Region 提供虛擬 Windows/Linux 桌面
- 使用者從任何地點、任何裝置透過 WorkSpaces 用戶端存取虛擬桌面
- 以**全球服務**方式設計，WorkSpaces 可部署在靠近使用者的 Region，統一管理
- 適合遠端辦公、跨國員工、承包商需要安全存取企業環境的場景
與 AppStream 2.0 差異：WorkSpaces 提供完整虛擬桌面環境；AppStream 只串流特定應用程式。

(38)
中文題目：哪項 AWS 服務可持續監控惡意活動與未授權行為，以保護 AWS 帳戶與工作負載？
答案：Amazon GuardDuty
解析：**Amazon GuardDuty** 的「持續監控」特性：
- **24/7 持續分析**：不間斷地分析 CloudTrail、VPC Flow Logs、DNS 日誌、S3 資料事件
- **機器學習**：建立基準行為模式，自動偵測偏差（異常 API 呼叫、可疑網路連線）
- **威脅情報**：整合 AWS 與第三方的已知惡意 IP 與網域黑名單
- 完全受管，無需部署 Agent 或管理基礎設施
- 發現威脅時自動產生 Findings，可觸發 EventBridge → Lambda 自動回應

(39)
中文題目：哪項 AWS 服務可在 5G 行動網路的邊緣節點提供靠近的運算與儲存服務？
答案：AWS Wavelength
解析：**AWS Wavelength** 將 AWS 運算與儲存服務嵌入電信商的 5G 網路基礎設施：
- 應用程式流量不需離開電信商網路即可到達 AWS 運算資源
- 實現**個位數毫秒延遲**，適合 5G 超低延遲應用
- 適用場景：即時遊戲、AR/VR、智慧車輛、工業自動化、即時影像分析
與 **Local Zones** 差異：Local Zones 部署於都市，延伸 AWS 至使用者附近；Wavelength 嵌入電信商 5G 基站，針對行動裝置提供極低延遲。

(40)
中文題目：AWS Well-Architected Framework 的哪個支柱關注有效利用 IT 與運算資源，並選擇正確的資源類型與大小？
答案：Performance Efficiency Pillar（效能效率支柱）
解析：**Performance Efficiency 支柱**的核心設計原則：
- **選擇正確資源類型與大小（Right-Sizing）**：依工作負載特性選擇最適合的 EC2 類型、資料庫引擎、儲存類別
- **使用受管服務**：利用 AWS 受管服務減少管理負擔，將精力集中於應用程式優化
- **Go Global in Minutes**：利用 AWS 全球基礎設施快速在多個 Region 部署，降低使用者延遲
- **持續演進**：隨技術進步更新架構，採用新服務與功能
題目關鍵字「efficiently + right resource types and sizes」精確對應 Performance Efficiency。

---

## Questions (41–45)

(41) are NoSQL database services from AWS
Ans: Amazon DocumentDB / Amazon Neptune

(42) needs automated reference deployments to speed up deploying financial solutions on AWS
Ans: AWS Partner Solutions (formerly Quick Starts)

(43) DynamoDB-based weather application experiences high read requests during holidays
Ans: Amazon DynamoDB Accelerator (DAX)

(44) storing data with random access patterns — which storage class for cost-optimal
Ans: Amazon S3 Intelligent-Tiering

(45) uses in-memory caches for running custom workloads
Ans: Memory Optimized instance types（記憶體優化執行個體類型）

---

(41)
中文題目：哪些是 AWS 提供的 NoSQL 資料庫服務？
答案：Amazon DocumentDB / Amazon Neptune
解析：**AWS NoSQL 資料庫服務**分類：
- **Amazon DynamoDB**：鍵值（Key-Value）與文件（Document）型 NoSQL，最常見
- **Amazon DocumentDB**：文件（Document）型 NoSQL，**相容 MongoDB API**，適合從 MongoDB 遷移
- **Amazon Neptune**：圖形（Graph）型 NoSQL，適合知識圖譜、社交網路
- **Amazon Keyspaces**：寬列（Wide-Column）型 NoSQL，**相容 Apache Cassandra**
- **Amazon ElastiCache**：記憶體（In-Memory）型，Redis/Memcached
對比：**Amazon RDS、Aurora、Redshift** 皆為關聯式（SQL）資料庫，不屬於 NoSQL。

(42)
中文題目：哪項 AWS 資源提供自動化的參考部署，加速在 AWS 上部署金融解決方案？
答案：AWS Partner Solutions（前稱 Quick Starts）
解析：**AWS Partner Solutions（Quick Starts）** 提供：
- 由 AWS 與合作夥伴共同開發的**自動化參考架構**，以 CloudFormation 範本打包
- 針對特定產業（金融、醫療、政府）的合規架構解決方案
- 遵循 AWS 最佳實踐，經過安全與效能驗證
- 幾分鐘內即可部署完整的解決方案架構
金融服務常用的 Quick Starts 包含：PCI DSS 合規架構、HIPAA 合規環境、資料湖解決方案等。

(43)
中文題目：基於 DynamoDB 的天氣應用程式在假日期間面臨大量讀取請求，應使用哪項服務？
答案：Amazon DynamoDB Accelerator，DAX
解析：**Amazon DynamoDB Accelerator（DAX）** 是 DynamoDB 專用的記憶體快取：
- 為 DynamoDB 讀取操作提供**微秒級延遲**（DynamoDB 本身為毫秒級）
- **與 DynamoDB API 完全相容**：應用程式只需將端點從 DynamoDB 改為 DAX，無需修改查詢邏輯
- 自動管理快取失效，確保資料一致性
- 大幅降低高讀取峰值期間的 DynamoDB 讀取容量消耗，節省成本
題目關鍵字「high read requests during holidays（假日高讀取請求）」對應 DAX 的讀取快取加速場景。

(44)
中文題目：儲存具有隨機存取模式的資料，哪種 S3 儲存類別最符合成本效益？
答案：Amazon S3 Intelligent-Tiering
解析：**Amazon S3 Intelligent-Tiering** 的設計目標：
- 專為**存取模式不可預測或會隨時間變化**的資料設計（如隨機存取模式）
- 自動監控每個物件的存取頻率，自動在以下層級間移動：
  - **Frequent Access（頻繁存取）**：費用同 Standard
  - **Infrequent Access（低頻存取）**：費用同 Standard-IA，30 天未存取後移至此層
  - **Archive Instant Access**：90 天未存取後移至此層
- **無取回費用**，移動層級時也不收費
- 小額監控費用（每 1,000 個物件），但免除了手動管理儲存類別的負擔
隨機存取模式無法預測哪些資料頻繁使用，Intelligent-Tiering 自動優化最適合。

(45)
中文題目：哪種 EC2 執行個體類型適合使用記憶體快取執行自訂工作負載？
答案：Memory Optimized instance types（記憶體優化執行個體）
解析：**EC2 執行個體類型**依工作負載特性分類：
- **General Purpose（通用型）**：均衡 CPU/記憶體/網路，如 t3、m6i，適合 Web 伺服器
- **Compute Optimized（運算優化）**：高 CPU/記憶體比，如 c6i，適合 HPC、遊戲
- **Memory Optimized（記憶體優化）**：大量記憶體，如 **r6i、x2idn**，適合**記憶體快取**、記憶體資料庫、即時大數據分析
- **Storage Optimized（儲存優化）**：高 I/O 吞吐量，如 i3、d3，適合 NoSQL 資料庫
- **Accelerated Computing（加速運算）**：GPU/FPGA，如 p4、inf2，適合機器學習
題目關鍵字「in-memory caches（記憶體快取）」直接對應 **Memory Optimized** 執行個體。

---

## Questions (46–50)

(46) scenario can effectively use Auto Scaling group's predictive scaling
Ans: To manage a workload that exhibits recurring load patterns specific to the day of the week or time of day

(47) the manager wants to find out the details of the user who changed it
Ans: AWS CloudTrail

(48) wants to find examples of AWS Cloud solution designs
Ans: AWS Architecture Center

(49) wants to convert media files into formats for mobile device playback
Ans: Amazon Elastic Transcoder

(50) are offered free of cost
Ans: AWS Elastic Beanstalk / AWS Auto Scaling

---

(46)
中文題目：哪種場景最適合使用 Auto Scaling 群組的預測性擴展（Predictive Scaling）？
答案：管理具有週期性負載模式的工作負載，例如特定星期幾或一天中特定時段的規律流量
解析：**Predictive Scaling（預測性擴展）** 的運作原理：
- 使用機器學習分析**歷史負載模式**，預測未來的流量趨勢
- **提前**（而非被動）擴展資源，確保峰值到來時已有足夠容量
- 最適合：**週期性、可預測的負載模式**——如每天上班時間流量高、週末流量低、每月月底結帳高峰
與 **Dynamic Scaling** 差異：Dynamic Scaling 是被動回應（指標超標才擴展）；Predictive Scaling 是主動預測（提前擴展）。

(47)
中文題目：管理者想了解是哪個使用者更改了某項設定的詳細資訊，應使用哪項服務？
答案：AWS CloudTrail
解析：**AWS CloudTrail** 記錄所有 AWS API 呼叫的完整詳情，包含：
- **誰（Who）**：執行操作的 IAM 使用者、角色或服務
- **什麼（What）**：執行的 API 動作（如 ModifyDBInstance、PutBucketPolicy）
- **何時（When）**：操作的精確時間戳記
- **哪裡（Where）**：來源 IP 位址、目標 Resource ARN
題目關鍵字「details of the user who changed it（查詢誰進行了變更）」精確對應 CloudTrail 的操作審計功能，是帳戶操作稽核的唯一完整記錄。

(48)
中文題目：哪項 AWS 資源提供 AWS Cloud 解決方案設計的範例？
答案：AWS Architecture Center（AWS 架構中心）
解析：**AWS Architecture Center** 是 AWS 官方的架構參考資源庫：
- 提供各種工作負載的**參考架構圖**（Reference Architectures）
- 涵蓋產業解決方案（金融、醫療、零售）與技術主題（微服務、資料分析、ML）
- 包含 **AWS Well-Architected Labs**：動手實作最佳實踐
- 架構圖可免費下載，作為設計新系統的起點
與 **AWS Marketplace** 差異：Marketplace 是軟體商城；Architecture Center 是架構設計知識庫。

(49)
中文題目：哪項 AWS 服務可將媒體檔案轉換為適合行動裝置播放的格式？
答案：Amazon Elastic Transcoder
解析：**Amazon Elastic Transcoder** 是雲端媒體轉碼服務：
- 將存放在 S3 的影片或音訊檔案轉換為多種格式（MP4、HLS、WebM 等）
- 支援行動裝置（iOS、Android）、平板、桌面瀏覽器的最佳播放格式
- 提供預定義的轉碼範本（Presets），無需深入了解編碼技術
- 按輸出分鐘數計費，無需管理轉碼基礎設施
適合 OTT 平台、影音內容分發、使用者上傳影片處理等場景。

(50)
中文題目：哪些 AWS 服務不額外收費（免費）？
答案：AWS Elastic Beanstalk / AWS Auto Scaling
解析：**AWS 永久免費服務（服務本身不收費）**：
- **AWS Elastic Beanstalk**：服務本身免費，只需支付底層 EC2、RDS、ELB 等資源費用
- **AWS Auto Scaling**：Auto Scaling 服務本身免費，只需支付底層 EC2 等資源費用
- **AWS CloudFormation**：範本本身免費，只需支付部署的資源費用
- **AWS IAM**：完全免費
- **Amazon VPC**：基本功能免費（NAT Gateway、VPN 連線等特定功能收費）
這些「協調型服務」本身不收費，費用來自它們所管理的底層資源。

---

## Questions (51–55)

(51) correct regarding Amazon API Gateway
Ans: API Gateway can call an AWS Lambda function to create the front door of a serverless application / API Gateway can be configured to send data directly to Amazon Kinesis Data Stream

(52) true about AWS Elastic Beanstalk
Ans: There is no additional charge for AWS Elastic Beanstalk / You can quickly deploy and manage applications without having to learn about the infrastructure

(53) use-case solved using Amazon Forecast
Ans: Predict the web traffic of a website for the next few weeks

(54) retain data for 10 years to meet compliance — which S3 storage class at minimal cost
Ans: Amazon S3 Glacier Deep Archive

(55) employees are provisioning additional resources via API calls beyond baseline
Ans: AWS CloudTrail Insights

---

(51)
中文題目：關於 Amazon API Gateway，哪些描述是正確的？
答案：
- API Gateway 可呼叫 AWS Lambda 函數，成為無伺服器應用程式的前端入口
- API Gateway 可設定為直接將資料傳送至 Amazon Kinesis Data Stream
解析：**Amazon API Gateway** 是全受管的 API 建立、發布、維護服務：
- **與 Lambda 整合**：API Gateway 接收 HTTP 請求 → 觸發 Lambda 函數處理 → 返回回應，是無伺服器 REST API 的標準架構（**Serverless Front Door**）
- **與 Kinesis 整合**：API Gateway 可設定直接將請求資料轉發至 Kinesis Data Stream，實現 API → 即時串流資料管道，無需 Lambda 中間層
- 支援 REST API、HTTP API、WebSocket API
- 內建功能：節流（Throttling）、API 金鑰管理、請求/回應轉換、快取

(52)
中文題目：關於 AWS Elastic Beanstalk，哪些描述是正確的？
答案：
- AWS Elastic Beanstalk 不額外收費
- 可快速部署與管理應用程式，無需了解基礎設施
解析：**AWS Elastic Beanstalk** 的核心價值：
- **零額外費用**：Beanstalk 服務本身免費，費用來自底層資源（EC2、ELB、RDS、S3）
- **基礎設施抽象**：開發者只需上傳程式碼，Beanstalk 自動處理容量佈建、負載平衡、Auto Scaling、健康監控
- 支援多種平台：Java、Python、PHP、Node.js、Ruby、.NET、Go、Docker
- 保留底層控制權：有需要時仍可直接存取 EC2 進行自訂設定

(53)
中文題目：哪種使用案例可以用 Amazon Forecast 解決？
答案：預測網站未來幾週的流量
解析：**Amazon Forecast** 是全受管的時間序列預測服務：
- 使用與 Amazon.com 相同的機器學習技術
- 適合**時間序列資料的預測**：銷售量預測、庫存需求、能源消耗、**網站流量預測**
- 無需機器學習專業知識，上傳歷史資料即可自動建立預測模型
- 預測準確度通常優於傳統統計方法（ARIMA）
題目關鍵字「predict web traffic + next few weeks」對應 Forecast 的時間序列預測能力，適合需要提前規劃運算容量的場景。

(54)
中文題目：需要將資料保存 10 年以符合合規要求，哪種 S3 儲存類別成本最低？
答案：Amazon S3 Glacier Deep Archive
解析：**S3 Glacier Deep Archive** 的合規封存特性：
- AWS 成本**最低**的儲存類別，適合長達 10 年以上的合規保留
- 資料持久性 **99.999999999%（11 個 9）**
- 取回時間 12-48 小時（合規封存通常不需要即時存取）
- **最低儲存期限 180 天**（計費考量）
- 搭配 **S3 Object Lock（WORM）**可實現合規級別的不可刪除保護
10 年合規封存的三個需求：超低成本 ✓、高持久性 ✓、長期保留 ✓，Deep Archive 完全符合。

(55)
中文題目：員工透過 API 呼叫佈建超出基準的額外資源，應使用哪項服務來識別此異常行為？
答案：AWS CloudTrail Insights
解析：**AWS CloudTrail Insights** 是 CloudTrail 的異常行為偵測功能：
- 自動分析 CloudTrail 的**管理事件（Management Events）**，建立 API 活動基準線
- 偵測**異常的 API 呼叫模式**：如資源佈建速率突然大幅超出正常水準
- 當偵測到異常時，產生 Insights 事件並發送至 CloudTrail、S3、EventBridge
- 適合偵測：異常大量 EC2 啟動、IAM 角色變更激增、安全群組規則大量修改
題目關鍵字「provisioning additional resources beyond baseline（超出基準的資源佈建）」對應 Insights 的異常活動偵測。

---

## Questions (56–60)

(56) will help provision a logically isolated network
Ans: Amazon Virtual Private Cloud (Amazon VPC)

(57) the customer's responsibility when running applications using AWS Lambda
Ans: Writing and maintaining the function code and its dependencies

(58) free tool that helps review workloads and compare them to AWS architectural best practices
Ans: AWS Well-Architected Tool

(59) AWS WAF can be deployed on which services
Ans: Amazon CloudFront / Application Load Balancer / Amazon API Gateway / AWS AppSync

(60) allow CIDR block notation for IP address ranges
Ans: Network Access Control List (Network ACL) / Security Group

---

(56)
中文題目：哪項 AWS 服務可協助佈建邏輯隔離的網路？
答案：Amazon Virtual Private Cloud，Amazon VPC
解析：**Amazon VPC** 是 AWS 網路隔離的基礎：
- 在 AWS Cloud 中建立**邏輯隔離**的虛擬網路空間
- 自訂 IP 位址範圍（CIDR Block）
- 完全控制網路設定：子網路、路由表、Internet Gateway、NAT Gateway
- 資源（EC2、RDS 等）在 VPC 內啟動，與其他 VPC 和公共網際網路隔離
- 可透過 VPC Peering、Transit Gateway、VPN、Direct Connect 選擇性連接其他網路
「邏輯隔離（Logically Isolated）」是 VPC 的核心定義，確保你的 AWS 資源在專屬的虛擬網路環境中運行。

(57)
中文題目：使用 AWS Lambda 執行應用程式時，哪些屬於客戶的責任？
答案：撰寫與維護函數程式碼及其相依套件
解析：**Lambda 的共同責任劃分**：
- **AWS 負責**：底層運算基礎設施、執行環境（Runtime）安裝與修補、OS 維護、函數的自動擴縮、資源佈建
- **客戶負責**：**函數程式碼（Function Code）**本身的邏輯、安全性與正確性；**相依套件（Dependencies）**的管理與版本（如 Python 套件、Node.js 模組）；函數的 IAM 執行角色設定、觸發器設定、記憶體與逾時配置
Lambda 是無伺服器服務，客戶不需管理任何伺服器，但程式碼品質與安全完全是客戶責任。

(58)
中文題目：哪項 AWS 免費工具可協助審查工作負載並與 AWS 架構最佳實踐比較（透過回答一系列問題）？
答案：AWS Well-Architected Tool
解析：**AWS Well-Architected Tool** 的使用方式：
- 在 AWS Console 中選擇要審查的工作負載
- 針對 Well-Architected Framework 六大支柱（卓越營運、安全性、可靠性、效能效率、成本優化、永續性）回答問題
- 工具自動識別高風險項目（HRI）並提供改善建議
- 完全**免費**，無需額外費用
- 可定期執行，追蹤架構成熟度的進步
與 **Trusted Advisor** 差異：Trusted Advisor 自動掃描帳戶資源；Well-Architected Tool 需人工回答問題，提供更深入的架構評估。

(59)
中文題目：AWS WAF 可部署在哪些 AWS 服務上？
答案：Amazon CloudFront / Application Load Balancer / Amazon API Gateway / AWS AppSync
解析：**AWS WAF 支援的部署目標**：
- **Amazon CloudFront**：在全球邊緣節點過濾流量，最靠近使用者
- **Application Load Balancer（ALB）**：Region 層級，保護後端 EC2 與容器
- **Amazon API Gateway**：保護 REST API 端點
- **AWS AppSync**：保護 GraphQL API
WAF 規則在流量到達後端資源之前即進行評估，是第 7 層應用層防護的核心部署模式。每個部署目標需分別設定 WAF Web ACL。

(60)
中文題目：哪些 AWS 服務允許使用 CIDR 區塊表示法指定 IP 位址範圍？
答案：Network Access Control List，Network ACL / Security Group
解析：**CIDR 表示法**在 AWS 網路安全服務中的應用：
- **Security Group**：規則支援 CIDR 表示法（如 10.0.0.0/16）指定允許的 IP 來源或目的地，也支援 Security Group ID 作為來源
- **Network ACL**：規則使用 CIDR 表示法指定 IP 範圍，支援 Allow 與 Deny
兩者皆允許以 CIDR 精確控制特定 IP 範圍的流量存取，差異在於作用層級（Security Group 在執行個體層；NACL 在子網路層）與狀態（SG 有狀態；NACL 無狀態）。

---

## Questions (61–65)

(61) help control the incoming traffic to an Amazon EC2
Ans: Security Group

(62) sends messages to a downstream application when orders are created — wants to decouple without communication loss
Ans: Amazon Simple Queue Service (SQS)

(63) By default, which events are logged by AWS CloudTrail
Ans: Management events（管理事件）

(64) a repository service for maintaining application dependencies via integration with package managers like Maven, Gradle, npm
Ans: AWS CodeArtifact

(65) will help you organize AWS resources and automate tasks on large numbers of resources at a time
Ans: AWS Resource Groups

---

(61)
中文題目：哪項 AWS 服務可協助控制進入 Amazon EC2 執行個體的流量？
答案：Security Group（安全群組）
解析：**Security Group** 是 EC2 的虛擬防火牆：
- 作用在**執行個體（Instance）層級**
- 設定允許哪些**入站（Inbound）**流量的 Port、Protocol 和來源 IP/CIDR
- **有狀態（Stateful）**：允許的入站流量，對應的出站回應自動允許
- 預設：拒絕所有入站流量，允許所有出站流量
- 只有 Allow 規則（沒有 Deny）
題目關鍵字「control the incoming traffic（控制傳入流量）」對應 Security Group 的 Inbound Rules 設定功能。

(62)
中文題目：應用程式在訂單建立時向下游應用程式傳送訊息，企業想在不遺失訊息的情況下解耦此架構，應使用哪項服務？
答案：Amazon Simple Queue Service，SQS
解析：**SQS 解耦架構的核心優勢**：
- **不遺失訊息**：SQS 訊息預設保留最多 4 天（可設定最長 14 天），消費者離線或處理失敗時訊息不會遺失
- **解耦（Decoupling）**：訂單服務（生產者）與下游應用程式（消費者）完全獨立，各自可獨立擴展、部署
- **Dead Letter Queue（DLQ）**：處理失敗的訊息自動移至死信佇列，防止訊息永久遺失
- **可靠傳遞**：SQS 在多個 AZ 冗餘儲存訊息，確保高持久性
題目關鍵字「without communication loss（不遺失訊息）+ decouple」精確對應 SQS 的設計目標。

(63)
中文題目：AWS CloudTrail 預設記錄哪些事件？
答案：Management events（管理事件）
解析：**CloudTrail 事件類型**：
- **Management Events（管理事件）**：AWS 帳戶資源的控制面板操作，如 CreateBucket、RunInstances、CreateUser，**預設啟用記錄，免費**
- **Data Events（資料事件）**：資源內的資料操作，如 S3 物件的 GetObject/PutObject、Lambda 函數執行，**預設不記錄**，需額外設定與付費
- **Insights Events（洞察事件）**：異常 API 活動偵測，**需額外啟用與付費**
考試常考：CloudTrail 預設記錄的是 **Management Events**，Data Events 和 Insights Events 皆非預設。

(64)
中文題目：哪項 AWS 服務是應用程式相依套件的儲存庫服務，可與 Maven、Gradle、npm 等套件管理器整合？
答案：AWS CodeArtifact
解析：**AWS CodeArtifact** 是全受管的軟體套件儲存庫服務：
- 集中儲存、發布與共享應用程式相依套件（Artifacts）
- 支援多種套件格式：**npm**（Node.js）、**Maven/Gradle**（Java）、**PyPI**（Python）、**NuGet**（.NET）
- 與 AWS IAM 整合，提供細粒度的套件存取控制
- 可設定為代理公共儲存庫（npmjs.com、Maven Central），快取套件以提升建置速度
- 適合：企業內部套件管理、私有套件發布、建置流水線的套件依賴管理

(65)
中文題目：哪項 AWS 服務可協助組織 AWS 資源，並同時對大量資源自動化執行任務？
答案：AWS Resource Groups
解析：**AWS Resource Groups** 是 AWS 資源的組織與批量管理工具：
- 依標籤（Tags）或 CloudFormation Stack 將相關資源**邏輯分組**（如將某應用程式的所有資源分為一組）
- **批量執行任務**：透過 AWS Systems Manager 的 Run Command，對整個資源群組同時執行操作（如批量修補、批量設定變更）
- 提供資源群組的統一視圖，方便監控與管理
- 與 AWS Config、CloudWatch、Trusted Advisor 整合，提供群組層級的合規與健康狀態視圖
是大規模資源管理與自動化操作的重要工具。