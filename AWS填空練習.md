# AWS 雲端從業人員認證 — 填空練習（T1–T6 全套）

---

## 雲端運算模型

1. `___`：由供應商完整運行和管理的軟體產品，客戶直接使用，無需維護底層基礎設施。
2. `___`：提供開發與部署應用程式的平台環境，客戶管理應用程式，無需管理底層作業系統或硬體。
3. `___`：提供虛擬化的運算、儲存與網路資源，客戶自行管理作業系統以上的所有層級。
4. `___`：將本地資料中心與 AWS 雲端結合使用的部署模型，適用於有合規或資料主權需求的場景。
5. `___`：完全在雲端供應商基礎設施上執行的部署模型。
6. `___`：在企業自有資料中心內部署的雲端環境。

<details>
<summary>✅ 答案</summary>

1. SaaS（Software as a Service／軟體即服務）
2. PaaS（Platform as a Service／平台即服務）
3. IaaS（Infrastructure as a Service／基礎設施即服務）
4. Hybrid Cloud（混合雲）
5. Public Cloud（公有雲）
6. Private Cloud（私有雲）

</details>

---

## 雲端運算優勢與概念

1. `___`：雲端可快速取用新技術資源、快速迭代和部署的特性。
2. `___`：根據實際需求動態擴展或縮減資源的雲端特性，即「right-sizing」。
3. `___`：系統能夠隨需求增長而擴大容量的能力。
4. `___`：系統在預期條件下持續正確執行的能力。
5. `___`：透過多 AZ 或多區域部署確保服務持續可用，即使部分元件故障也不中斷。
6. `___`：AWS 因聚合數十萬客戶使用量，得以提供更低的隨用隨付價格。
7. `___`：透過新增更多執行個體來擴展容量，而非升級現有機器規格。
8. `___`：透過提升現有機器的 CPU/RAM 規格來擴展容量。
9. `___`：應用程式元件間相互獨立、透過訊息或 API 通訊的架構最佳實務。
10. `___`：以程式碼定義和管理基礎設施，提升一致性與自動化，屬於卓越營運支柱建議。
11. `___`：評估從本地遷移至雲端的完整成本，包含伺服器管理、電力、冷卻等。

<details>
<summary>✅ 答案</summary>

1. Agility（敏捷性）
2. Elasticity（彈性）
3. Scalability（可擴展性）
4. Reliability（可靠性）
5. High Availability（高可用性）
6. Economies of Scale（規模經濟）
7. Horizontal Scaling（水平擴展／向外擴展）
8. Vertical Scaling（垂直擴展／向上擴展）
9. Loose Coupling（鬆耦合）
10. Infrastructure as Code（IaC）
11. Total Cost of Ownership（TCO）

</details>

---

## 定價與成本管理

1. `___`：AWS 提供的彈性定價模型，承諾一定使用量以換取折扣，分為兩種子類型。
2. `___`：適用於任何 EC2 執行個體、Fargate 及 Lambda 的彈性節省計畫，不限機型或區域。
3. `___`：針對特定 EC2 執行個體系列和區域的節省計畫，折扣比前者更高。
4. `___`：承諾 1 年或 3 年使用量以換取大幅折扣（最高 72%）的 EC2 定價方式，不會被中斷。
5. `___`：可在保留期間變更執行個體屬性（機型、作業系統等）的保留執行個體類型。
6. `___`：折扣最高但彈性最低、不可轉換屬性的保留執行個體類型。
7. `___`：使用 AWS 閒置容量、可節省最高 90% 費用但可能被中斷的執行個體，適合彈性工作負載。
8. `___`：按秒計費、無長期承諾、不會被中斷，適合短期、突發或不可預測的工作負載。
9. `___`：提供獨立實體伺服器供單一客戶使用，支援攜帶自有授權（BYOL）。
10. `___`：在專用硬體上執行但不保證固定實體主機，介於一般執行個體與 Dedicated Host 之間。
11. `___`：實體主機上的暫存高速本機磁碟，執行個體終止後資料消失，適合快取等暫時性工作負載。
12. `___`：視覺化分析 AWS 歷史支出並可預測未來 12 個月費用的工具，也可識別未充分使用的資源。
13. `___`：設定費用、用量或 RI 使用率預算，並在超標時發出警報的服務。
14. `___`：提供最詳細 AWS 費用明細（可細至小時級）的報告服務，輸出至 S3。
15. `___`：為 AWS 資源加上標籤，用於將費用細分至各部門或專案的機制。
16. `___`：在實際部署前預估 AWS 服務費用的免費線上工具，也可用於比較本地與雲端成本。
17. `___`：透過機器學習分析工作負載，推薦最佳 EC2、EBS、Lambda 等資源配置以降低成本並提升效能。
18. `___`：AWS Organizations 功能，將多個帳戶的費用匯總，並可共享保留執行個體折扣及批量折扣。
19. `___`：AWS 提供的折抵金，優先套用到到期日最近、適用服務範圍最窄的項目。

<details>
<summary>✅ 答案</summary>

1. Savings Plans
2. Compute Savings Plans
3. EC2 Instance Savings Plans
4. EC2 Reserved Instance（RI，保留執行個體）
5. Convertible RI（可轉換保留執行個體）
6. Standard RI（標準保留執行個體）
7. EC2 Spot Instance（Spot 執行個體）
8. EC2 On-Demand Instance（隨需執行個體）
9. EC2 Dedicated Host（專用主機）
10. EC2 Dedicated Instance（專用執行個體）
11. EC2 Instance Store（執行個體存放區）
12. AWS Cost Explorer
13. AWS Budgets
14. AWS Cost and Usage Report（CUR）
15. AWS Cost Allocation Tags（成本分配標籤）
16. AWS Pricing Calculator
17. AWS Compute Optimizer
18. Consolidated Billing（合併計費）
19. AWS Credits（AWS 信用額度）

</details>

---

## 運算服務

1. `___`：提供可調整大小的虛擬伺服器（執行個體）的核心 IaaS 運算服務，支援按秒計費。
2. `___`：自動化建立、維護和更新 EC2 AMI 及容器映像的服務。
3. `___`：包含作業系統及軟體設定的 EC2 執行個體啟動模板，必須與執行個體位於相同區域。
4. `___`：在 EC2 執行個體啟動時自動執行的啟動程序腳本。
5. `___`：可從執行個體內部存取的執行個體資訊（如 IP、AMI ID 等）。
6. `___`：透過瀏覽器或 CLI 安全連線至 EC2 執行個體的工具，無需開啟額外連接埠或使用公用 IP。
7. `___`：無伺服器運算服務，只需上傳程式碼即可執行，按請求數和執行時間計費。
8. `___`：自動處理部署、容量佈建、負載平衡與 Auto Scaling 的應用程式平台（PaaS），本身免費。
9. `___`：用於容器的無伺服器運算引擎，使用 ECS 或 EKS 時無需管理底層 EC2 伺服器。
10. `___`：用於在 AWS 上執行、停止和管理 Docker 容器的全受管容器編排服務。
11. `___`：用於儲存、管理和部署 Docker 容器映像的全受管容器映像倉庫。
12. `___`：提供簡單、低成本的虛擬私有伺服器、資料庫與網路的入門級雲端服務，適合 WordPress 等簡單應用。
13. `___`：根據需求自動調整 AWS 資源數量（向外擴展/向內縮減）的服務，本身免費使用。
14. `___`：管理一組 EC2 執行個體自動擴展與縮減的邏輯群組，可設定最小、最大和期望執行個體數量。
15. `___`：根據歷史週期性負載模式預先調整資源數量的 ASG 擴展方式。
16. `___`：在 AWS 上以具成本效益的方式執行大規模批次運算工作負載的全受管服務。
17. `___`：自動將傳入流量分配至多個目標（EC2、容器、Lambda）的負載平衡服務。
18. `___`：ELB 的一種，在第 7 層（HTTP/HTTPS）進行流量路由，最適合 Web 應用程式。
19. `___`：ELB 的一種，在第 4 層（TCP/UDP）進行流量路由，適合需要超低延遲的場景。
20. `___`：使用 AWS 全球網路骨幹將流量導向最近端點，提供靜態 IP 位址作為應用程式固定入口。

<details>
<summary>✅ 答案</summary>

1. Amazon EC2（Elastic Compute Cloud）
2. Amazon EC2 Image Builder
3. Amazon Machine Image（AMI）
4. EC2 User Data（使用者資料）
5. EC2 Instance Metadata（執行個體中繼資料）
6. EC2 Instance Connect
7. AWS Lambda
8. AWS Elastic Beanstalk
9. AWS Fargate
10. Amazon ECS（Elastic Container Service）
11. Amazon ECR（Elastic Container Registry）
12. Amazon Lightsail
13. AWS Auto Scaling
14. Auto Scaling Group（ASG）
15. Predictive Scaling（預測性擴展）
16. AWS Batch
17. AWS Elastic Load Balancing（ELB）
18. Application Load Balancer（ALB）
19. Network Load Balancer（NLB）
20. AWS Global Accelerator

</details>

---

## EC2 執行個體類型

1. `___`：適用於需要大量記憶體的工作負載，如記憶體快取、大型資料庫。
2. `___`：適用於需要高運算效能的工作負載，如批次處理、高效能科學運算。
3. `___`：適用於需要高速、大量本機儲存存取的工作負載，如資料倉儲。
4. `___`：配備 GPU 或 FPGA，適用於機器學習推論、圖形渲染等工作負載。

<details>
<summary>✅ 答案</summary>

1. Memory Optimized（記憶體最佳化）
2. Compute Optimized（運算最佳化）
3. Storage Optimized（儲存最佳化）
4. Accelerated Computing（加速運算）

</details>

---

## 儲存服務

1. `___`：物件儲存服務，以扁平鍵值結構儲存任意類型的檔案，具高耐久性（11 個 9），出站流量收費、入站免費。
2. `___`：適用於頻繁存取資料的標準儲存類別，無最低儲存期限費用限制。
3. `___`：自動根據存取模式在不同儲存層間移動資料以節省成本，適合隨機或不可預測的存取模式。
4. `___`：適用於不常存取但需要快速取回的資料，有最低儲存期限（30 天）及資料取得費用。
5. `___`：只儲存於單一 AZ 的低成本不頻繁存取儲存類別，適合可輕易重建的資料（如縮圖）。
6. `___`：低成本封存儲存，資料取回時間從數分鐘到數小時，適合資料封存備份。
7. `___`：S3 最低成本的儲存類別，適合需長達 10 年以上合規保留的資料，取回時間最長。
8. `___`：帳戶或儲存貯體層級的設定，確保 S3 資料不會意外公開。
9. `___`：保留物件的所有版本，防止意外刪除或覆寫，是 S3 資料保護的最佳方式。
10. `___`：定義規則自動在 S3 儲存類別間轉換物件或過期刪除物件，以節省成本。
11. `___`：自動跨帳戶或跨區域複製 S3 物件（含中繼資料），分為 SRR（同區域）和 CRR（跨區域）。
12. `___`：透過 CloudFront 邊緣節點加速從遠端位置上傳至 S3 的傳輸速度。
13. `___`：記錄對 S3 儲存貯體發出的所有請求，用於稽核和分析存取行為。
14. `___`：為 EC2 執行個體提供持久性區塊儲存磁碟區，只能掛載至同一 AZ 的單一執行個體。
15. `___`：可由多個 EC2 執行個體跨 AZ、跨 VPC、跨區域同時掛載的全受管 NFS 檔案系統。
16. `___`：提供 Windows 原生 SMB 協定的全受管檔案儲存服務，適合 Windows 應用程式。
17. `___`：高效能並行檔案系統，適用於機器學習和高效能運算（HPC）工作負載。
18. `___`：連接本地環境與 AWS 雲端儲存的混合雲儲存服務，支援 File、Volume 和 Tape 三種閘道類型。
19. `___`：EBS 磁碟區的時間點備份，以增量方式儲存於 S3，可用於跨 AZ 複製資料。
20. `___`：自動化、加速本地系統與 AWS 儲存服務（S3、EFS）之間的線上資料傳輸，支援增量備份。

<details>
<summary>✅ 答案</summary>

1. Amazon S3（Simple Storage Service）
2. Amazon S3 Standard
3. Amazon S3 Intelligent-Tiering
4. Amazon S3 Standard-IA（Infrequent Access）
5. Amazon S3 One Zone-IA
6. Amazon S3 Glacier Flexible Retrieval
7. Amazon S3 Glacier Deep Archive
8. Amazon S3 Block Public Access（封鎖公開存取）
9. Amazon S3 Versioning（版本控制）
10. Amazon S3 Lifecycle Configuration（生命週期設定）
11. Amazon S3 Replication（S3 複寫）
12. Amazon S3 Transfer Acceleration（S3TA）
13. Amazon S3 Access Logs（S3 存取日誌）
14. Amazon EBS（Elastic Block Store）
15. Amazon EFS（Elastic File System）
16. Amazon FSx for Windows File Server
17. Amazon FSx for Lustre
18. AWS Storage Gateway
19. Amazon EBS Snapshots（EBS 快照）
20. AWS DataSync

</details>

---

## 資料庫服務

1. `___`：全受管關聯式資料庫服務，AWS 負責修補底層作業系統，客戶負責資料庫加密等設定。
2. `___`：主資料庫同步複寫至待機執行個體，AZ 故障時自動容錯移轉，主要提升可用性。
3. `___`：非同步複製的唯讀資料庫副本，主要用於提升讀取擴展性。
4. `___`：AWS 自研的高效能關聯式資料庫，相容 MySQL 與 PostgreSQL，適合 CRM 等企業應用。
5. `___`：全受管的 NoSQL 鍵值與文件資料庫，提供毫秒級效能、彈性結構描述，預設支援高可用性。
6. `___`：DynamoDB 的多區域主動-主動複製功能，適合需跨區域高可用的應用程式。
7. `___`：DynamoDB 的記憶體快取層，可將讀取效能提升至微秒級，解決讀取密集型瓶頸。
8. `___`：全受管的記憶體快取服務，支援 Redis 與 Memcached，用於降低資料庫讀取負載。
9. `___`：全受管的圖形資料庫服務（NoSQL），適合建立知識圖譜、社交網路等高度關聯性資料應用。
10. `___`：相容 MongoDB 的全受管文件資料庫服務（NoSQL），支援靈活結構描述。
11. `___`：用於大規模 PB 級資料倉儲與 OLAP（線上分析處理）的全受管服務。
12. `___`：協助將資料庫從本地或其他雲端遷移至 AWS 的服務。

<details>
<summary>✅ 答案</summary>

1. Amazon RDS（Relational Database Service）
2. Amazon RDS Multi-AZ（多可用區部署）
3. Amazon RDS Read Replica（讀取副本）
4. Amazon Aurora
5. Amazon DynamoDB
6. Amazon DynamoDB Global Tables（全球資料表）
7. Amazon DynamoDB Accelerator（DAX）
8. Amazon ElastiCache
9. Amazon Neptune
10. Amazon DocumentDB
11. Amazon Redshift
12. AWS Database Migration Service（DMS）

</details>

---

## 網路服務

1. `___`：在 AWS 雲端中建立邏輯隔離私有網路的服務，跨越一個區域內的所有 AZ。
2. `___`：VPC 內依 AZ 劃分的網路區段，只存在於單一 AZ 中。
3. `___`：允許 VPC 內資源與公共網際網路通訊的 VPC 元件。
4. `___`：由 AWS 全受管的網路位址轉換服務，允許私有子網路中的執行個體存取網際網路，但不允許外部發起連線。
5. `___`：作為虛擬防火牆在執行個體層級控制入站與出站流量，有狀態（stateful），只能設定允許規則。
6. `___`：在子網路層級控制進出流量的無狀態（stateless）防火牆，包含有編號的規則清單，可設定允許和拒絕規則。
7. `___`：兩個 VPC 之間的私有直接連線，適用於同組織內少數 VPC 間的資料共享。
8. `___`：將多個 VPC 和本地網路連接至單一中樞閘道的網路路由服務，適合大規模多 VPC 架構。
9. `___`：讓 VPC 私密連接至 AWS 服務而不經過公開網際網路，分為 Gateway Endpoint 和 Interface Endpoint。
10. `___`：讓 VPC 私密存取 AWS 服務或其他 VPC 服務的介面端點技術，不需要 IGW 或 NAT。
11. `___`：在企業本地資料中心與 AWS 之間建立私有、專用實體網路連線，提供高頻寬與穩定延遲。
12. `___`：透過公共網際網路在本地網路與 AWS VPC 之間建立加密 IPSec 隧道連線。
13. `___`：Site-to-Site VPN 在 AWS 端的元件。
14. `___`：Site-to-Site VPN 在客戶本地端的元件，由客戶自行設定。
15. `___`：AWS 提供的高可用性 DNS 服務，提供網域註冊、健康檢查、多種路由政策。
16. `___`：將流量導向單一資源的最基本路由政策。
17. `___`：依照設定的權重比例將流量分配至多個資源的路由政策。
18. `___`：將請求路由至提供最低延遲 AWS 端點的路由政策。
19. `___`：主動-被動設定，主要資源故障時自動切換至備援資源的路由政策。
20. `___`：全球 CDN（內容傳遞網路）服務，將內容快取至全球 Edge Location 以降低延遲。
21. `___`：用於建立、發布、維護和監控 RESTful 及 WebSocket API 的全受管服務。

<details>
<summary>✅ 答案</summary>

1. Amazon VPC（Virtual Private Cloud）
2. Subnet（子網路）
3. Internet Gateway（網際網路閘道）
4. NAT Gateway（NAT 閘道）
5. Security Group（安全群組）
6. Network ACL（網路存取控制清單）
7. VPC Peering Connection（VPC 對等連線）
8. AWS Transit Gateway
9. VPC Endpoint（VPC 端點）
10. AWS PrivateLink
11. AWS Direct Connect
12. AWS Site-to-Site VPN
13. Virtual Private Gateway（VGW，虛擬私有閘道）
14. Customer Gateway（CGW，客戶閘道）
15. Amazon Route 53
16. Route 53 Simple Routing（簡單路由）
17. Route 53 Weighted Routing（加權路由）
18. Route 53 Latency-based Routing（延遲型路由）
19. Route 53 Failover Routing（容錯移轉路由）
20. Amazon CloudFront
21. Amazon API Gateway

</details>

---

## 邊緣與混合雲服務

1. `___`：將 AWS 基礎設施、服務、API 和工具延伸至客戶本地資料中心的全受管機架式設備。
2. `___`：將 AWS 運算與儲存服務部署至電信業者 5G 網路邊緣，讓行動裝置使用者獲得超低延遲。
3. `___`：將 AWS 服務延伸至靠近特定大城市的地點，提供個位數毫秒延遲，適合媒體製作、遊戲等場景。
4. `___`：用於大量資料離線遷移至 AWS 或在邊緣位置執行運算的實體裝置系列。
5. `___`：PB 級資料離線傳輸至 AWS 的實體儲存裝置，適合頻寬有限的遠端位置資料遷移。
6. `___`：具備邊緣運算能力的 Snowball 裝置，可在本地進行資料處理後再傳至 AWS。
7. `___`：提供圖形介面管理 AWS Snow 系列裝置的工具，無需命令列或 REST API。

<details>
<summary>✅ 答案</summary>

1. AWS Outposts
2. AWS Wavelength
3. AWS Local Zones
4. AWS Snow Family（Snow 系列）
5. AWS Snowball
6. AWS Snowball Edge
7. AWS OpsHub

</details>

---

## 安全與身份服務

1. `___`：管理 AWS 使用者、群組、角色與存取權限的全球性服務，本身免費。
2. `___`：代表與 AWS 互動的人員或應用程式的 IAM 實體，存取金鑰與此綁定。
3. `___`：可被 AWS 服務或使用者臨時承擔的身份，是讓 EC2 存取 DynamoDB 等服務的推薦方式。
4. `___`：以 JSON 定義的權限文件，必要元素為 Effect 和 Action，應遵循最小權限原則。
5. `___`：列出帳戶中所有 IAM 使用者及其密碼、存取金鑰、MFA 裝置等狀態的報告。
6. `___`：顯示 IAM 使用者實際存取各服務的時間，協助審查並縮減過多權限。
7. `___`：在密碼之外額外要求第二驗證因素，強烈建議為根使用者帳戶啟用。
8. `___`：使用智慧型手機 Authenticator App 實現 MFA，無需攜帶實體裝置。
9. `___`：插入 USB 連接埠的實體安全金鑰，用於 AWS MFA 驗證。
10. `___`：產生一次性密碼的實體 Token 裝置。
11. `___`：與 IAM 使用者綁定，用於程式化存取 AWS API、CLI 和 SDK 的憑證。
12. `___`：集中管理多個 AWS 帳戶的存取，並支援單一登入（SSO）。
13. `___`：為 Web 和行動應用程式提供使用者註冊、登入和存取控制的服務。
14. `___`：為受信任使用者提供臨時、有限權限安全憑證的服務。
15. `___`：建立和管理加密金鑰的全受管服務，支援多種金鑰類型。
16. `___`：由客戶自行在 KMS 中建立和管理的加密金鑰，提供最高控制度。
17. `___`：AWS 自動為每項服務在客戶帳戶中建立與管理的加密金鑰，最省力的加密方式。
18. `___`：使用硬體安全模組（HSM）在雲端執行加密操作的服務，滿足需要硬體裝置加密的法規要求。
19. `___`：安全儲存、管理和自動輪換資料庫密碼、API 金鑰等機密資訊的服務。
20. `___`：持續分析 CloudTrail、VPC Flow Logs、DNS 日誌，偵測 AWS 帳戶和工作負載中惡意活動與威脅的服務。
21. `___`：自動評估 EC2 執行個體和容器應用程式安全漏洞與偏離最佳實務的服務，不追蹤設定變更。
22. `___`：使用機器學習自動發現和保護 Amazon S3 中敏感資料（如個人識別資訊 PII）的全受管服務。
23. `___`：利用 CloudTrail 日誌、VPC Flow Logs 和 GuardDuty 調查結果，自動分析安全事件根本原因的服務。
24. `___`：集中彙整和管理多項 AWS 安全服務警報，提供統一安全態勢視圖的服務。
25. `___`：預設為所有 AWS 客戶免費啟用的基本 DDoS 防護服務。
26. `___`：付費的進階 DDoS 防護服務，保護 EC2、CloudFront、Route 53、ELB 等，並提供費用保護和 DRT 支援。
27. `___`：在第 7 層（應用層）保護 Web 應用程式免受 SQL 注入、XSS 等攻擊的服務。
28. `___`：提供 AWS 安全和合規報告（如 HIPAA、PCI、SOC）以及合規相關文件的自助服務入口。
29. `___`：捕獲 VPC 中網路介面進出流量資訊的日誌，用於安全分析和故障排除。
30. `___`：負責處理 AWS 資源被用於惡意行為（如連接埠掃描、DDoS）投訴的專責團隊。

<details>
<summary>✅ 答案</summary>

1. AWS IAM（Identity and Access Management）
2. IAM User（IAM 使用者）
3. IAM Role（IAM 角色）
4. IAM Policy（IAM 政策）
5. IAM Credentials Report（IAM 憑證報告）
6. IAM Access Advisor（IAM 存取顧問）
7. MFA（Multi-Factor Authentication／多重要素驗證）
8. Virtual MFA Device（虛擬 MFA 裝置）
9. U2F Security Key（U2F 安全金鑰）
10. Hardware MFA Device（硬體 MFA 裝置）
11. Access Key ID & Secret Access Key（存取金鑰）
12. AWS IAM Identity Center（前身 AWS SSO）
13. Amazon Cognito
14. AWS Security Token Service（AWS STS）
15. AWS KMS（Key Management Service）
16. Customer Managed Key（CMK，客戶受管金鑰）
17. AWS Managed Key（AWS 受管金鑰）
18. AWS CloudHSM
19. AWS Secrets Manager
20. Amazon GuardDuty
21. Amazon Inspector
22. Amazon Macie
23. Amazon Detective
24. AWS Security Hub
25. AWS Shield Standard
26. AWS Shield Advanced
27. AWS WAF（Web Application Firewall）
28. AWS Artifact
29. VPC Flow Logs（VPC 流量日誌）
30. AWS Abuse Team（濫用團隊）

</details>

---

## 監控與管理服務

1. `___`：監控 AWS 資源指標、日誌和事件，設定警報的服務，帳單指標資料儲存於 us-east-1。
2. `___`：記錄所有 AWS 帳戶 API 呼叫與使用者操作的稽核日誌服務，預設記錄管理事件，日誌預設加密。
3. `___`：分析 CloudTrail 管理事件，自動偵測異常 API 活動並發出警報的功能。
4. `___`：持續追蹤 AWS 資源設定變更歷史並評估合規性的服務，適合提交歷史設定給稽核單位。
5. `___`：依據 AWS 最佳實務，針對成本、效能、安全、容錯與服務限制提供建議的工具。
6. `___`：透過回答問卷來審查工作負載並與 AWS 架構最佳實務比較的免費工具。
7. `___`：集中管理 EC2 和本地伺服器（收集軟體庫存、執行命令、修補伺服器）的運維自動化服務。
8. `___`：提供安全的瀏覽器 Shell 存取 EC2 執行個體，無需開啟 SSH 連接埠或使用公用 IP。
9. `___`：發布所有 AWS 服務在所有區域的一般狀態和可用性資訊的儀表板，可訂閱 RSS feed。
10. `___`：提供特定帳戶中 AWS 資源受影響事件的個人化視圖，在所有支援方案中均可使用。
11. `___`：分析和偵錯分散式微服務和無伺服器應用程式效能問題的追蹤服務。
12. `___`：以 JSON 或 YAML 範本定義和自動化佈建 AWS 基礎設施的 IaC 服務。
13. `___`：使用 Python、JavaScript 等常見程式語言定義雲端基礎設施的開發框架，最終生成 CloudFormation 範本。
14. `___`：提供 AWS 客戶最常見問題和解答的知識庫論壇。

<details>
<summary>✅ 答案</summary>

1. Amazon CloudWatch
2. AWS CloudTrail
3. AWS CloudTrail Insights
4. AWS Config
5. AWS Trusted Advisor
6. AWS Well-Architected Tool
7. AWS Systems Manager（SSM）
8. AWS Systems Manager Session Manager
9. AWS Health Dashboard – Service Health
10. AWS Health Dashboard – Your Account Health
11. AWS X-Ray
12. AWS CloudFormation
13. AWS Cloud Development Kit（AWS CDK）
14. AWS Knowledge Center

</details>

---

## 開發者工具

1. `___`：私有的 Git 程式碼儲存庫服務，提供版本控制功能。
2. `___`：全受管的持續整合服務，負責編譯程式碼和執行測試。
3. `___`：自動化將應用程式程式碼部署至 EC2 執行個體及本地執行個體的服務。
4. `___`：自動化軟體發布流程（原始碼→建置→測試→部署）的持續交付服務。
5. `___`：快速開發、建置和部署 AWS 應用程式的整合開發專案管理服務。
6. `___`：全受管的套件儲存庫服務，整合 Maven、npm、Gradle 等套件管理工具。
7. `___`：使用機器學習自動化程式碼審查、識別程式碼缺陷並提供改善建議的服務。
8. `___`：提供程式語言特定 API 以程式化存取 AWS 服務的工具套件。
9. `___`：透過命令列介面管理 AWS 服務的工具。
10. `___`：透過 Web 瀏覽器管理 AWS 服務的圖形介面。
11. `___`：提供真實行動裝置和瀏覽器的測試服務，可跨不同韌體和 OS 版本進行測試。
12. `___`：用於實施混沌工程、注入故障以測試應用程式韌性的服務。

<details>
<summary>✅ 答案</summary>

1. AWS CodeCommit
2. AWS CodeBuild
3. AWS CodeDeploy
4. AWS CodePipeline
5. AWS CodeStar
6. AWS CodeArtifact
7. Amazon CodeGuru
8. AWS Software Development Kit（SDK）
9. AWS CLI（Command Line Interface）
10. AWS Management Console（管理主控台）
11. AWS Device Farm
12. AWS Fault Injection Simulator（AWS FIS）

</details>

---

## 分析與 AI/ML 服務

1. `___`：即時擷取和處理串流大數據的服務，適合廣告技術等即時分析場景。
2. `___`：用於在 Hadoop/Spark 叢集上執行大數據工作負載的受管服務。
3. `___`：直接對 S3 資料使用標準 SQL 進行互動式查詢的無伺服器分析服務。
4. `___`：建立互動式商業智慧儀表板的全受管 BI 服務，可從任何裝置存取。
5. `___`：全受管的無伺服器 ETL（Extract, Transform, Load）資料整合服務，用於準備分析用資料。
6. `___`：提供完整機器學習工作流程（建置、訓練、部署模型）的全受管平台。
7. `___`：基於機器學習的時間序列預測服務，如預測網站流量、銷售量等。
8. `___`：提供影像和影片分析（物件識別、人臉辨識、文字偵測等）的 AI 服務。
9. `___`：將語音自動轉換為文字的 AI 服務，用於語音輸入分析。
10. `___`：將文字轉換為自然語音的 AI 服務，用於語音輸出。
11. `___`：提供神經機器翻譯的 AI 服務，可轉換不同語言的文字內容。
12. `___`：用於自然語言處理（NLP）的 AI 服務，可分析文字情感、擷取實體與關鍵字。
13. `___`：使用自然語言理解（NLU）建立聊天機器人和語音介面的 AI 服務（Alexa 底層技術）。
14. `___`：使用機器學習的智慧企業搜尋服務，可從 PDF、Word 等文件中擷取答案。
15. `___`：根據使用者歷史資料提供個人化推薦（如電影、產品推薦）的 AI 服務。
16. `___`：將 S3 媒體檔案轉換為適合行動裝置等各種格式播放的媒體轉碼服務。

<details>
<summary>✅ 答案</summary>

1. Amazon Kinesis Data Streams
2. Amazon EMR（Elastic MapReduce）
3. Amazon Athena
4. Amazon QuickSight
5. AWS Glue
6. Amazon SageMaker
7. Amazon Forecast
8. Amazon Rekognition
9. Amazon Transcribe
10. Amazon Polly
11. Amazon Translate
12. Amazon Comprehend
13. Amazon Lex
14. Amazon Kendra
15. Amazon Personalize
16. Amazon Elastic Transcoder

</details>

---

## 應用程式整合

1. `___`：全受管的訊息佇列服務，用於解耦應用程式元件並確保訊息不遺失，適合系統間非同步通訊。
2. `___`：全受管的發布/訂閱訊息通知服務，可向多個訂閱者（Email、SQS、Lambda）發送通知。
3. `___`：全受管的訊息代理服務，相容 Apache ActiveMQ 和 RabbitMQ，適合遷移現有本地訊息代理功能。
4. `___`：無伺服器事件匯流排服務，可根據排程或事件觸發 Lambda 等服務。
5. `___`：用於編排多個 Lambda 函數和 AWS 服務的無伺服器工作流程服務。
6. `___`：將桌面應用程式串流至瀏覽器的服務，無需採購或管理伺服器。
7. `___`：讓任意數量的 IoT 裝置安全連接至雲端的全受管服務，無需佈建伺服器。

<details>
<summary>✅ 答案</summary>

1. Amazon SQS（Simple Queue Service）
2. Amazon SNS（Simple Notification Service）
3. Amazon MQ
4. Amazon EventBridge
5. AWS Step Functions
6. Amazon AppStream 2.0
7. AWS IoT Core

</details>

---

## 架構與治理框架

1. `___`：AWS 官方提供的六大支柱雲端架構最佳實務框架（卓越營運、安全性、可靠性、效能效率、成本優化、永續性）。
2. `___`：著重自動化、頻繁小型可回復變更、預測故障、維護 IaC 的支柱。
3. `___`：著重使用 KMS 加密資料、啟用追蹤能力的支柱。
4. `___`：著重水平擴展（scale out）實現容錯，而非垂直擴展（scale up）的支柱。
5. `___`：著重根據工作負載需求選擇正確資源類型與大小（right-sizing）的支柱。
6. `___`：著重降低不必要支出、選擇正確定價模型的支柱。
7. `___`：指導組織雲端採用旅程的框架，包含業務、人員、治理、平台、安全、營運六大觀點。
8. `___`：CAF 中確保 IT 投資與業務目標對齊的觀點，涵蓋策略管理能力。
9. `___`：CAF 中由 CTO 和工程師主導的觀點，負責建立雲端平台。
10. `___`：CAF 中負責效能、容量管理的觀點。
11. `___`：雲端遷移的六種策略（Rehost、Replatform、Refactor、Repurchase、Retain、Retire）。
12. `___`：不修改程式碼直接將應用程式搬移至 AWS，遷移速度最快。
13. `___`：進行少量最佳化（如改用 RDS 托管資料庫）但不變更核心架構。
14. `___`：提供預定義藍圖和護欄，協助客戶快速建立符合最佳實務的多帳戶 AWS 登陸區（Landing Zone）。
15. `___`：集中管理和治理多個 AWS 帳戶的服務，支援統一帳單、SCP 和批量折扣共享。
16. `___`：在 AWS Organizations 中限制成員帳戶最大可用權限的組織政策，只能限制不能授予。
17. `___`：定義 AWS 與客戶各自負責的安全責任，AWS 負責「雲端本身的安全」，客戶負責「雲端中的安全」。
18. `___`：提供 AWS 官方雲端解決方案設計範例與參考架構的知識庫。
19. `___`：由 AWS 合作夥伴提供的自動化參考部署，可快速在 AWS 上部署常見解決方案。
20. `___`：提供第三方軟體（含 SaaS、自訂 AMI）的線上商店，可直接部署至 AWS 環境。
21. `___`：幫助組織管理和提供已核准 IT 服務目錄的服務，協助識別正確 AWS 服務。
22. `___`：附加在 AWS 資源上的鍵值對，用於分類、搜尋與成本分配。
23. `___`：AWS 官方的專業服務團隊，協助客戶加速雲端遷移和基礎設施建置。
24. `___`：AWS 授權合作夥伴網路，分為技術合作夥伴和諮詢合作夥伴。

<details>
<summary>✅ 答案</summary>

1. AWS Well-Architected Framework
2. Operational Excellence Pillar（卓越營運支柱）
3. Security Pillar（安全性支柱）
4. Reliability Pillar（可靠性支柱）
5. Performance Efficiency Pillar（效能效率支柱）
6. Cost Optimization Pillar（成本優化支柱）
7. AWS Cloud Adoption Framework（AWS CAF）
8. Business Perspective（業務觀點）
9. Platform Perspective（平台觀點）
10. Operations Perspective（營運觀點）
11. AWS Migration Strategies（遷移策略 6R）
12. Rehost（重新託管／Lift and Shift）
13. Replatform（重新平台化）
14. AWS Control Tower
15. AWS Organizations
16. Service Control Policies（SCP，服務控制政策）
17. AWS Shared Responsibility Model（共同責任模型）
18. AWS Architecture Center（架構中心）
19. AWS Partner Solutions（前身 Quick Starts）
20. AWS Marketplace
21. AWS Service Catalog
22. Tags（標籤）
23. AWS Professional Services
24. AWS Partner Network（APN）

</details>

---

## 基礎設施概念

1. `___`：由多個地理上分離的可用區組成的 AWS 基礎設施地理範圍，每個區域至少包含三個 AZ。
2. `___`：AWS 區域內一個或多個實體分離的資料中心群，是實現高可用性的基本單位。
3. `___`：CloudFront CDN 的快取節點，分佈在全球各大城市，數量遠多於 AWS 區域。
4. `___`：全受管的雲端虛擬桌面服務（DaaS），為全球性交付（非區域性）服務。
5. `___`：將檔案透過 SFTP、FTPS、FTP 協定安全傳輸至 S3 或 EFS 的全受管服務。

<details>
<summary>✅ 答案</summary>

1. AWS Region（區域）
2. Availability Zone（AZ，可用區）
3. Edge Location（邊緣位置）
4. Amazon WorkSpaces
5. AWS Transfer Family

</details>

---

## 災難復原

1. `___`：成本最低的 DR 策略，RPO/RTO 最長（數小時），適合可容忍較長恢復時間的場景。
2. `___`：在雲端維持最小核心系統運行，災難時快速擴展完整環境的 DR 策略，成本次低。
3. `___`：在雲端維持縮小版的完整環境持續運行，災難時快速擴展至正式規模。
4. `___`：成本最高但 RTO/RPO 最短的 DR 策略，多個站點同時提供完整服務。

<details>
<summary>✅ 答案</summary>

1. Backup and Restore（備份與還原）
2. Pilot Light（導引燈）
3. Warm Standby（暖備）
4. Multi-Site Active/Active（多站點主動/主動）

</details>

---

## AWS 支援計畫

1. `___`：免費提供，包含帳戶帳單問題諮詢、服務健康檢查及核心 Trusted Advisor 檢查（7 項）。
2. `___`：付費計畫，含核心 Trusted Advisor 檢查、工作時間 Email 技術支援，無電話支援。
3. `___`：付費計畫，提供全套 Trusted Advisor 檢查、24/7 電話技術支援、第三方軟體互操作指導。
4. `___`：介於商業和企業之間的方案，提供 TAM 池（非指定）存取。
5. `___`：最高級支援計畫，包含指定技術客戶經理（TAM）、AWS Concierge 及 Infrastructure Event Management。
6. `___`：僅企業支援計畫提供的專屬 AWS 技術顧問，協助優化 AWS 環境。
7. `___`：企業支援計畫提供的專屬帳單與帳戶管理顧問服務。

<details>
<summary>✅ 答案</summary>

1. AWS Basic Support（基本支援）
2. AWS Developer Support（開發人員支援）
3. AWS Business Support（商業支援）
4. AWS Enterprise On-Ramp Support
5. AWS Enterprise Support（企業支援）
6. Technical Account Manager（TAM，技術客戶經理）
7. AWS Concierge

</details>

---

*共收錄約 160 個 AWS 專有名詞｜題目來源：Practice Test T1–T6（每套 65 題）*
