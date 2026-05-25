# AWS 雲端從業人員認證 — 專有名詞解析清單

---

## 雲端運算模型

**SaaS（Software as a Service／軟體即服務）**：由供應商完整運行和管理的軟體產品，客戶直接使用，無需維護底層基礎設施。
`來源：Q1`

**PaaS（Platform as a Service／平台即服務）**：提供開發與部署應用程式的平台環境，客戶管理應用程式，無需管理底層作業系統或硬體。
`來源：Q1`

**IaaS（Infrastructure as a Service／基礎設施即服務）**：提供虛擬化的運算、儲存與網路資源，客戶自行管理作業系統以上的所有層級。
`來源：Q1、Q20`

---

## 定價與成本管理

**Savings Plans**：AWS 提供的彈性定價模型，承諾一定使用量以換取折扣，分為 Compute Savings Plans 和 EC2 Instance Savings Plans 兩種。
`來源：Q2`

**Compute Savings Plans**：適用於任何 EC2 執行個體、Fargate 及 Lambda 的彈性節省計畫，不限機型或區域。
`來源：Q2`

**EC2 Instance Savings Plans**：針對特定 EC2 執行個體系列和區域的節省計畫，折扣比 Compute Savings Plans 更高。
`來源：Q2`

**AWS Cost Explorer**：視覺化分析 AWS 歷史支出並可預測未來 12 個月費用的工具。
`來源：Q36`

**AWS Budgets**：設定費用或用量預算並在超標時發出警報的服務。
`來源：Q22`

**AWS Cost and Usage Report（CUR）**：提供最詳細 AWS 費用明細的報告服務。
`來源：Q22`

**AWS Cost Allocation Tags（成本分配標籤）**：為 AWS 資源加上標籤，用於將費用細分至各部門或專案的機制。
`來源：Q22`

**AWS Pricing Calculator**：在實際部署前預估 AWS 服務費用的免費線上計算工具。
`來源：Q36`

---

## 運算服務

**Amazon EC2（Elastic Compute Cloud）**：提供可調整大小的虛擬伺服器（執行個體）的核心運算服務。
`來源：Q20、Q45`

**Amazon EC2 Image Builder**：自動化建立、維護和更新 EC2 AMI 及容器映像的服務。
`來源：Q32`

**Amazon EC2 AMI（Amazon Machine Image）**：包含作業系統及軟體設定的 EC2 執行個體啟動模板。
`來源：Q32`

**AWS Lambda**：無伺服器運算服務，只需上傳程式碼即可執行，無需管理伺服器。
`來源：Q51、Q57`

**AWS Elastic Beanstalk**：自動處理部署、容量佈建、負載平衡與自動擴展的應用程式平台，使用者只需上傳程式碼。
`來源：Q26、Q50、Q52`

**AWS Fargate**：用於容器的無伺服器運算引擎，無需管理底層伺服器即可執行容器。
`來源：Q30`

**Amazon Lightsail**：提供簡單、低成本的虛擬私有伺服器、資料庫與網路的入門級雲端服務。
`來源：Q30`

**AWS Auto Scaling**：根據需求自動調整 AWS 資源數量的服務，為免費功能。
`來源：Q50`

**Auto Scaling Group（ASG）**：管理一組 EC2 執行個體自動擴展與縮減的邏輯群組。
`來源：Q26、Q46`

**Predictive Scaling（預測性擴展）**：根據歷史週期性負載模式預先調整資源數量的 ASG 擴展方式。
`來源：Q46`

---

## EC2 執行個體類型

**Memory Optimized（記憶體最佳化）**：適用於需要大量記憶體的工作負載，如記憶體快取、大型資料庫。
`來源：Q45`

**Compute Optimized（運算最佳化）**：適用於需要高運算效能的工作負載，如批次處理、高效能運算。
`來源：Q45`

**Storage Optimized（儲存最佳化）**：適用於需要高速、大量本機儲存存取的工作負載。
`來源：Q45`

**Accelerated Computing（加速運算）**：配備 GPU 或 FPGA，適用於機器學習、圖形渲染等工作負載。
`來源：Q45`

---

## 儲存服務

**Amazon S3（Simple Storage Service）**：物件儲存服務，可儲存任意類型的檔案，具高耐久性與擴展性。
`來源：Q15、Q44、Q49`

**Amazon S3 Standard**：適用於頻繁存取資料的標準儲存類別。
`來源：Q44`

**Amazon S3 Intelligent-Tiering**：自動根據存取模式在不同儲存層間移動資料以節省成本，適合隨機存取模式。
`來源：Q44`

**Amazon S3 Standard-IA（Infrequent Access）**：適用於不常存取但需要快速取回的資料。
`來源：Q44、Q54`

**Amazon S3 Glacier Flexible Retrieval**：低成本封存儲存，資料取回時間從數分鐘到數小時不等。
`來源：Q54`

**Amazon S3 Glacier Deep Archive**：S3 最低成本的儲存類別，適合需長達 10 年以上合規保留的資料。
`來源：Q14、Q54`

**Amazon EBS（Elastic Block Store）**：為 EC2 執行個體提供持久性區塊儲存磁碟區的服務。
`來源：Q15`

**Amazon EFS（Elastic File System）**：可由多個 EC2 執行個體同時掛載的全受管 NFS 網路檔案系統。
`來源：Q15`

**AWS Storage Gateway**：連接本地環境與 AWS 雲端儲存的混合雲儲存服務，預設加密。
`來源：Q14、Q15`

---

## 資料庫服務

**Amazon RDS（Relational Database Service）**：全受管關聯式資料庫服務，支援 MySQL、PostgreSQL 等引擎。
`來源：Q5、Q25、Q41`

**Amazon Aurora**：AWS 自研的高效能關聯式資料庫，相容 MySQL 與 PostgreSQL，適合企業級 CRM 等應用。
`來源：Q5`

**Amazon DynamoDB**：全受管的 NoSQL 鍵值與文件資料庫，提供毫秒級效能。
`來源：Q25、Q41、Q43`

**Amazon DynamoDB Accelerator（DAX）**：DynamoDB 的記憶體快取層，可將讀取效能提升至微秒級。
`來源：Q43`

**Amazon ElastiCache**：全受管的記憶體快取服務，支援 Redis 與 Memcached。
`來源：Q5、Q43`

**Amazon Neptune**：全受管的圖形資料庫服務，適合建立知識圖譜、社交網路等關係型資料應用。
`來源：Q5、Q25、Q41`

**Amazon DocumentDB**：相容 MongoDB 的全受管文件資料庫服務（NoSQL）。
`來源：Q25、Q41`

**Amazon Redshift**：用於大規模資料倉儲與分析的全受管服務。
`來源：Q9`

---

## 網路服務

**Amazon VPC（Virtual Private Cloud）**：在 AWS 雲端中建立邏輯隔離私有網路的服務。
`來源：Q56`

**Security Group（安全群組）**：作為虛擬防火牆，控制 EC2 執行個體的入站與出站流量，支援 CIDR 表示法。
`來源：Q47、Q60、Q61`

**Network ACL（網路存取控制清單）**：在子網路層級控制進出流量的防火牆規則，支援 CIDR 表示法。
`來源：Q60、Q61`

**AWS Direct Connect**：在企業本地資料中心與 AWS 之間建立私有、專用實體網路連線的服務。
`來源：Q23`

**AWS Site-to-Site VPN**：透過公共網際網路在本地網路與 AWS VPC 之間建立加密隧道連線。
`來源：Q23`

**Amazon Route 53**：AWS 提供的可擴展 DNS 網域名稱系統服務。
`來源：Q56`

**Amazon CloudFront**：全球 CDN（內容傳遞網路）服務，將內容快取至邊緣節點以降低延遲。
`來源：Q23、Q59`

**AWS PrivateLink**：讓 VPC 私密存取 AWS 服務或其他 VPC 服務而不經過公開網路的服務。
`來源：Q56`

**Amazon API Gateway**：用於建立、發布、維護和監控 RESTful 及 WebSocket API 的全受管服務。
`來源：Q51、Q59`

---

## 邊緣與混合雲服務

**AWS Outposts**：將 AWS 基礎設施、服務和 API 延伸至客戶本地資料中心的全受管服務。
`來源：Q3、Q29`

**AWS Wavelength**：將 AWS 運算與儲存服務部署至電信業者 5G 網路邊緣，實現超低延遲應用。
`來源：Q29、Q39`

**AWS Local Zones**：將 AWS 服務延伸至靠近特定大城市的地點，降低延遲。
`來源：Q29`

**AWS Snow Family**：用於大量資料離線遷移至 AWS 的實體裝置系列（包含 Snowball、Snowball Edge 等）。
`來源：Q3、Q7`

**AWS Snowball**：用於 PB 級資料傳輸的實體儲存裝置。
`來源：Q3、Q7`

**AWS Snowball Edge**：具備運算能力的 Snowball 裝置，可在邊緣位置進行資料處理。
`來源：Q31、Q39`

---

## 安全與身份服務

**AWS IAM（Identity and Access Management）**：管理 AWS 使用者、群組、角色與存取權限的服務。
`來源：Q18、Q27`

**MFA（Multi-Factor Authentication／多重要素驗證）**：在密碼之外額外要求第二驗證因素以保護帳戶安全。
`來源：Q18、Q27`

**AWS KMS（Key Management Service）**：建立和管理加密金鑰的全受管服務。
`來源：Q24`

**AWS Managed Master Keys（AWS 受管主金鑰）**：AWS 自動為每項服務建立與管理的加密金鑰，最省力的加密方式。
`來源：Q24`

**Customer Managed Keys（CMK，客戶管理金鑰）**：由客戶自行在 KMS 中建立和管理的加密金鑰。
`來源：Q24`

**Amazon GuardDuty**：持續監控 AWS 帳戶和工作負載中惡意活動與未授權行為的威脅偵測服務。
`來源：Q12、Q38`

**Amazon Inspector**：自動評估 EC2 執行個體和容器應用程式安全漏洞的服務。
`來源：Q6、Q38、Q47`

**Amazon Detective**：利用 CloudTrail、VPC Flow Logs 和 GuardDuty 資料自動分析安全事件根本原因的服務。
`來源：Q12、Q38`

**AWS Security Hub**：集中彙整和管理多項 AWS 安全服務警報的安全態勢管理服務。
`來源：Q38`

**AWS WAF（Web Application Firewall）**：保護 Web 應用程式免受常見網路攻擊的防火牆，可部署於 CloudFront、ALB、API Gateway 和 AppSync。
`來源：Q59`

**AWS Firewall Manager**：集中管理跨帳戶和應用程式的 WAF 規則及安全政策的服務。
`來源：Q56`

**AWS Abuse Team（濫用團隊）**：負責處理 AWS 資源被用於惡意行為（如連接埠掃描）投訴的專責團隊。
`來源：Q21`

**Service Control Policies（SCP，服務控制政策）**：在 AWS Organizations 中限制成員帳戶權限的組織政策。
`來源：Q34`

---

## 監控與管理服務

**Amazon CloudWatch**：監控 AWS 資源指標、日誌和事件，並設定警報的服務。
`來源：Q6、Q26`

**AWS CloudTrail**：記錄所有 AWS 帳戶 API 呼叫與使用者操作的稽核日誌服務，預設記錄管理事件。
`來源：Q6、Q47、Q63`

**AWS CloudTrail Insights**：分析 CloudTrail 管理事件，偵測異常 API 活動並發出警報的功能。
`來源：Q55`

**AWS Config**：持續追蹤 AWS 資源設定變更歷史並評估合規性的服務。
`來源：Q6`

**AWS Trusted Advisor**：依據 AWS 最佳實務，針對成本、效能、安全、容錯與服務限制提供建議的工具。
`來源：Q21、Q28、Q33`

**AWS Well-Architected Tool**：透過回答問卷來審查工作負載並與 AWS 架構最佳實務比較的免費工具。
`來源：Q58`

**AWS Systems Manager（SSM）**：集中管理 EC2 和本地伺服器的運維自動化服務。
`來源：Q32`

**AWS OpsHub**：提供圖形介面管理 AWS Snowball 系列裝置的工具，無需命令列。
`來源：Q7`

---

## 開發者工具

**AWS CodeCommit**：私有的 Git 程式碼儲存庫服務，提供版本控制功能。
`來源：Q10`

**AWS CodeBuild**：全受管的持續整合服務，負責編譯程式碼和執行測試。
`來源：Q10、Q64`

**AWS CodePipeline**：自動化軟體發布流程的持續交付服務。
`來源：Q10`

**AWS CodeStar**：快速開發、建置和部署 AWS 應用程式的整合開發專案管理服務。
`來源：Q10、Q64`

**AWS CodeArtifact**：全受管的套件儲存庫服務，整合 Maven、npm、Gradle 等套件管理工具。
`來源：Q64`

---

## 分析與 AI/ML 服務

**Amazon Kinesis Data Streams**：即時擷取和處理串流大數據的服務，適合廣告技術等即時分析場景。
`來源：Q9、Q51`

**Amazon EMR（Elastic MapReduce）**：用於大規模資料處理的受管 Hadoop/Spark 叢集服務。
`來源：Q9`

**Amazon Athena**：直接對 S3 資料使用標準 SQL 進行互動式查詢的無伺服器分析服務。
`來源：Q8`

**Amazon QuickSight**：建立互動式商業智慧儀表板的全受管 BI 服務，可從任何裝置存取。
`來源：Q8`

**AWS Glue**：全受管的 ETL（Extract, Transform, Load）資料整合服務。
`來源：Q8、Q49`

**Amazon SageMaker**：提供完整機器學習工作流程（建置、訓練、部署）的全受管平台。
`來源：Q8、Q53`

**Amazon Forecast**：基於機器學習的時間序列預測服務，如預測網站流量、銷售量等。
`來源：Q53`

**Amazon Elastic Transcoder**：將 S3 媒體檔案轉換為適合行動裝置等各種格式播放的媒體轉碼服務。
`來源：Q49`

**Amazon Transcribe**：將語音自動轉換為文字的 AI 服務。
`來源：Q49`

**Amazon Comprehend**：用於自然語言處理（NLP）的 AI 服務，可分析文字情感與實體。
`來源：Q49`

---

## 應用程式整合

**Amazon SQS（Simple Queue Service）**：全受管的訊息佇列服務，用於解耦應用程式元件並確保訊息不遺失。
`來源：Q9、Q62`

**Amazon SNS（Simple Notification Service）**：全受管的發布/訂閱訊息通知服務。
`來源：Q62`

**Amazon AppStream 2.0**：將桌面應用程式串流至瀏覽器的服務，無需採購或管理伺服器。
`來源：Q3、Q7`

**AWS IoT Core**：讓 IoT 裝置安全連接至雲端的全受管服務，無需佈建伺服器。
`來源：Q35`

**Amazon Connect**：雲端基礎的客服中心服務。
`來源：Q35`

---

## 架構與治理

**AWS Well-Architected Framework**：AWS 官方提供的雲端架構最佳實務框架，包含六大支柱。
`來源：Q40、Q58`

**Performance Efficiency Pillar（效能效率支柱）**：Well-Architected Framework 中著重有效使用運算資源、選擇正確資源類型與大小的支柱。
`來源：Q40`

**AWS Control Tower**：提供預定義藍圖和護欄，協助客戶快速建立符合最佳實務的多帳戶 AWS 環境的原生服務。
`來源：Q34`

**AWS Organizations**：集中管理和治理多個 AWS 帳戶的服務，支援統一帳單與 SCP。
`來源：Q34`

**AWS Shared Responsibility Model（共同責任模型）**：定義 AWS 與客戶各自負責的安全責任範圍，AWS 負責雲端基礎設施安全，客戶負責雲端中的資源安全。
`來源：Q13、Q20、Q57`

**AWS Architecture Center（架構中心）**：提供 AWS 官方雲端解決方案設計範例與參考架構的知識庫。
`來源：Q48`

**AWS Partner Solutions（前身 Quick Starts）**：由 AWS 合作夥伴提供的自動化參考部署，可快速在 AWS 上部署常見解決方案。
`來源：Q42`

**AWS Marketplace**：提供第三方軟體、服務和資料的線上商店，可直接部署至 AWS 環境。
`來源：Q22、Q48`

**AWS Resource Groups（資源群組）**：組織 AWS 資源並支援大量資源批次管理與自動化的功能。
`來源：Q65`

**Tags（標籤）**：附加在 AWS 資源上的鍵值對，用於分類、搜尋與成本分配。
`來源：Q22、Q65`

---

## 基礎設施概念

**AWS Region（區域）**：由多個地理上分離的可用區組成的 AWS 基礎設施地理範圍。
`來源：Q4、Q11`

**Availability Zone（AZ，可用區）**：AWS 區域內一個或多個實體分離的資料中心群，AZ 間流量預設加密。
`來源：Q4、Q11`

**Elasticity（彈性）**：根據實際需求動態擴展或縮減資源的雲端特性，即「right-sizing」。
`來源：Q19`

**Amazon WorkSpaces**：全受管的雲端桌面服務（DaaS），為全球性交付服務。
`來源：Q3、Q37`

**AWS Transfer Family**：將檔案透過 SFTP、FTPS、FTP 協定傳輸至 S3 或 EFS 的全受管服務。
`來源：Q7`

---

## 災難復原

**Backup and Restore（備份與還原）**：成本最低的災難復原策略，RPO/RTO 較長，適合可容忍數小時資料損失的場景。
`來源：Q16`

**Pilot Light（導引燈）**：在雲端維持最小核心系統運行，災難時快速擴展的復原策略。
`來源：Q16`

**Warm Standby（暖備）**：在雲端維持縮小版的完整環境，可快速擴展至正式規模的復原策略。
`來源：Q16`

**Multi-Site Active/Active（多站點主動/主動）**：成本最高但 RTO/RPO 最短的災難復原策略，多個站點同時提供服務。
`來源：Q16`

**CloudEndure Disaster Recovery**：提供持續複製的災難復原服務，可將實體、虛擬和雲端伺服器快速恢復至 AWS。
`來源：Q31`

---

## 支援計畫

**AWS Basic Support（基本支援）**：免費提供，包含帳單問題諮詢、服務健康檢查及核心 Trusted Advisor 檢查。
`來源：Q28、Q33`

**AWS Developer Support（開發人員支援）**：付費計畫，提供技術支援，含核心 Trusted Advisor 檢查。
`來源：Q28`

**AWS Business Support（商業支援）**：提供全套 Trusted Advisor 檢查及 24/7 技術支援的付費計畫。
`來源：Q28`

**AWS Enterprise Support（企業支援）**：最高級支援計畫，包含指定技術客戶經理（TAM）和 AWS Concierge 服務。
`來源：Q28`

**Technical Account Manager（TAM，技術客戶經理）**：僅企業支援計畫提供的專屬 AWS 技術顧問。
`來源：Q28`

**AWS Concierge**：企業支援計畫提供的專屬帳單與帳戶管理顧問服務。
`來源：Q28`

---

*共收錄約 92 個 AWS 專有名詞｜題目來源：Practice Test #6 Q1–Q65*
