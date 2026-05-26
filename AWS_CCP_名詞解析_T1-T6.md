# AWS 雲端從業人員認證 — 專有名詞解析清單（T1–T6 全套）

---

## 雲端運算模型

**SaaS（Software as a Service／軟體即服務）**：由供應商完整運行和管理的軟體產品，客戶直接使用，無需維護底層基礎設施。
`T1Q54、T2Q14、T3Q57、T5Q64、T6Q1`

**PaaS（Platform as a Service／平台即服務）**：提供開發與部署應用程式的平台環境，客戶管理應用程式，無需管理底層作業系統或硬體。
`T5Q63、T5Q64、T6Q1`

**IaaS（Infrastructure as a Service／基礎設施即服務）**：提供虛擬化的運算、儲存與網路資源，客戶自行管理作業系統以上的所有層級。
`T1Q54、T6Q1、T6Q20`

**Hybrid Cloud（混合雲）**：將本地資料中心與 AWS 雲端結合使用的部署模型，適用於有合規或資料主權需求的場景。
`T2Q60、T5Q9`

**Public Cloud（公有雲）**：完全在雲端供應商基礎設施上執行的部署模型。
`T5Q9`

**Private Cloud（私有雲）**：在企業自有資料中心內部署的雲端環境。
`T5Q9`

---

## 雲端運算優勢與概念

**Agility（敏捷性）**：雲端可快速取用新技術資源、快速迭代和部署的特性。
`T1Q22、T3Q41、T4Q41`

**Elasticity（彈性）**：根據實際需求動態擴展或縮減資源的雲端特性，即「right-sizing」。
`T2Q36、T6Q19`

**Scalability（可擴展性）**：系統能夠隨需求增長而擴大容量的能力。
`T1Q22`

**Reliability（可靠性）**：系統在預期條件下持續正確執行的能力。
`T1Q22`

**High Availability（高可用性）**：透過多 AZ 或多區域部署確保服務持續可用，即使部分元件故障也不中斷。
`T2Q21、T3Q12、T3Q49`

**Economies of Scale（規模經濟）**：AWS 因聚合數十萬客戶使用量，得以提供更低的隨用隨付價格。
`T1Q26、T4Q41`

**Horizontal Scaling（水平擴展／向外擴展）**：透過新增更多執行個體來擴展容量，而非升級現有機器規格。
`T2Q19、T3Q6`

**Vertical Scaling（垂直擴展／向上擴展）**：透過提升現有機器的 CPU/RAM 規格來擴展容量。
`T5Q62`

**Loose Coupling（鬆耦合）**：應用程式元件間相互獨立、透過訊息或 API 通訊的架構最佳實務。
`T4Q15`

**Infrastructure as Code（IaC）**：以程式碼定義和管理基礎設施，提升一致性與自動化，屬於卓越營運支柱建議。
`T3Q34`

**Total Cost of Ownership（TCO）**：評估從本地遷移至雲端的完整成本，包含伺服器管理、電力、冷卻等。
`T5Q14`

---

## 定價與成本管理

**Savings Plans**：AWS 提供的彈性定價模型，承諾一定使用量以換取折扣，分為 Compute Savings Plans 和 EC2 Instance Savings Plans 兩種。
`T6Q2`

**Compute Savings Plans**：適用於任何 EC2 執行個體、Fargate 及 Lambda 的彈性節省計畫，不限機型或區域。
`T6Q2`

**EC2 Instance Savings Plans**：針對特定 EC2 執行個體系列和區域的節省計畫，折扣比 Compute Savings Plans 更高。
`T6Q2`

**EC2 Reserved Instance（RI，保留執行個體）**：承諾 1 年或 3 年使用量以換取大幅折扣（最高 72%）的 EC2 定價方式，不會被中斷，有全額/部分/無預付三種付款選項。
`T1Q8、T1Q30、T3Q28、T5Q23、T5Q24`

**Convertible RI（可轉換保留執行個體）**：可在保留期間變更執行個體屬性（機型、作業系統等）的保留執行個體類型，適合工作負載會變動的場景。
`T5Q23`

**Standard RI（標準保留執行個體）**：折扣最高但彈性最低、不可轉換屬性的保留執行個體類型。
`T5Q23`

**EC2 Spot Instance（Spot 執行個體）**：使用 AWS 閒置容量、可節省最高 90% 費用但可能被中斷的執行個體，適合可容忍中斷的彈性工作負載。
`T1Q42、T3Q7、T4Q36`

**EC2 On-Demand Instance（隨需執行個體）**：按秒計費、無長期承諾、不會被中斷，適合短期、突發或不可預測的工作負載。
`T2Q54、T4Q49`

**EC2 Dedicated Host（專用主機）**：提供獨立實體伺服器供單一客戶使用，支援攜帶自有授權（BYOL），適合伺服器綁定軟體授權。
`T1Q48`

**EC2 Dedicated Instance（專用執行個體）**：在專用硬體上執行但不保證固定實體主機，介於一般執行個體與 Dedicated Host 之間。
`T1Q48`

**EC2 Instance Store（執行個體存放區）**：實體主機上的暫存高速本機磁碟，執行個體終止後資料消失，適合快取等暫時性工作負載。
`T1Q40、T3Q5、T3Q45`

**AWS Cost Explorer**：視覺化分析 AWS 歷史支出並可預測未來 12 個月費用的工具，也可識別未充分使用的資源。
`T1Q29、T3Q60、T4Q51、T5Q43、T6Q36`

**AWS Budgets**：設定費用、用量或 RI 使用率預算，並在超標時發出警報的服務。
`T1Q28、T2Q58、T3Q40、T4Q42、T6Q22`

**AWS Cost and Usage Report（CUR）**：提供最詳細 AWS 費用明細（可細至小時級）的報告服務，輸出至 S3。
`T3Q33、T5Q58、T6Q22`

**AWS Cost Allocation Tags（成本分配標籤）**：為 AWS 資源加上標籤，用於將費用細分至各部門或專案的機制，需分別啟動 AWS 生成與使用者自訂標籤。
`T3Q62、T5Q65、T6Q22`

**AWS Pricing Calculator**：在實際部署前預估 AWS 服務費用的免費線上工具，也可用於比較本地與雲端成本。
`T1Q46、T4Q54、T6Q36`

**AWS Compute Optimizer**：透過機器學習分析工作負載，推薦最佳 EC2、EBS、Lambda 等資源配置以降低成本並提升效能。
`T1Q29、T2Q4`

**Consolidated Billing（合併計費）**：AWS Organizations 功能，將多個帳戶的費用匯總，並可共享保留執行個體折扣及批量折扣。
`T2Q63、T4Q28、T4Q47`

**AWS Credits（AWS 信用額度）**：AWS 提供的折抵金，優先套用到到期日最近、適用服務範圍最窄的信用額度。
`T1Q32`

---

## 運算服務

**Amazon EC2（Elastic Compute Cloud）**：提供可調整大小的虛擬伺服器（執行個體）的核心 IaaS 運算服務，支援按秒計費。
`T1Q53、T2Q11、T4Q6、T6Q20`

**Amazon EC2 Image Builder**：自動化建立、維護和更新 EC2 AMI 及容器映像的服務，減少手動維護映像的時間。
`T6Q32`

**Amazon Machine Image（AMI）**：包含作業系統及軟體設定的 EC2 執行個體啟動模板，必須與 EC2 執行個體位於相同區域。
`T3Q11、T3Q52、T5Q49、T6Q32`

**EC2 User Data（使用者資料）**：在 EC2 執行個體啟動時自動執行的啟動程序腳本（bootstrap script）。
`T4Q59`

**EC2 Instance Metadata（執行個體中繼資料）**：可從執行個體內部存取的執行個體資訊（如 IP、AMI ID 等）。
`T4Q59`

**EC2 Instance Connect**：透過瀏覽器或 CLI 安全連線至 EC2 執行個體的工具，無需開啟額外連接埠或使用公用 IP。
`T4Q48`

**AWS Lambda**：無伺服器運算服務，只需上傳程式碼即可執行，按請求數和執行時間計費，無需管理任何伺服器。
`T2Q24、T3Q39、T3Q43、T4Q30、T5Q57、T6Q57`

**AWS Elastic Beanstalk**：自動處理部署、容量佈建、負載平衡與 Auto Scaling 的應用程式平台（PaaS），使用者只需上傳程式碼，本身免費。
`T2Q46、T3Q36（ECS）、T5Q63、T6Q26、T6Q50、T6Q52`

**AWS Fargate**：用於容器的無伺服器運算引擎，使用 ECS 或 EKS 時無需管理底層 EC2 伺服器。
`T2Q56、T4Q18、T4Q23`

**Amazon ECS（Elastic Container Service）**：用於在 AWS 上執行、停止和管理 Docker 容器的全受管容器編排服務。
`T3Q36`

**Amazon ECR（Elastic Container Registry）**：用於儲存、管理和部署 Docker 容器映像的全受管容器映像倉庫。
`T2Q1`

**Amazon Lightsail**：提供簡單、低成本的虛擬私有伺服器、資料庫與網路的入門級雲端服務，適合 WordPress 等簡單應用。
`T5Q36、T6Q30`

**AWS Auto Scaling**：根據需求自動調整 AWS 資源數量（向外擴展/向內縮減）的服務，本身免費使用。
`T2Q20、T2Q27、T3Q6、T4Q60、T6Q50`

**Auto Scaling Group（ASG）**：管理一組 EC2 執行個體自動擴展與縮減的邏輯群組，可設定最小、最大和期望執行個體數量。
`T6Q26、T6Q46`

**Predictive Scaling（預測性擴展）**：根據歷史週期性負載模式（如每週固定時段）預先調整資源數量的 ASG 擴展方式。
`T6Q46`

**AWS Batch**：在 AWS 上以具成本效益的方式執行大規模批次運算工作負載的全受管服務。
`T5Q46`

**AWS Elastic Load Balancing（ELB）**：自動將傳入流量分配至多個目標（EC2、容器、Lambda）的負載平衡服務，提供高可用性與容錯能力。
`T1Q7、T2Q19、T5Q52`

**Application Load Balancer（ALB）**：ELB 的一種，在第 7 層（HTTP/HTTPS）進行流量路由，最適合 Web 應用程式。
`T4Q33`

**Network Load Balancer（NLB）**：ELB 的一種，在第 4 層（TCP/UDP）進行流量路由，適合需要超低延遲的場景。
`T4Q33`

**AWS Global Accelerator**：使用 AWS 全球網路骨幹將流量導向最近端點，提供靜態 IP 位址作為應用程式固定入口，適合非 HTTP 使用案例。
`T2Q8、T4Q10`

---

## EC2 執行個體類型

**Memory Optimized（記憶體最佳化）**：適用於需要大量記憶體的工作負載，如記憶體快取、大型資料庫。
`T6Q45`

**Compute Optimized（運算最佳化）**：適用於需要高運算效能的工作負載，如批次處理、高效能科學運算。
`T6Q45`

**Storage Optimized（儲存最佳化）**：適用於需要高速、大量本機儲存存取的工作負載，如資料倉儲。
`T6Q45`

**Accelerated Computing（加速運算）**：配備 GPU 或 FPGA，適用於機器學習推論、圖形渲染等工作負載。
`T6Q45`

---

## 儲存服務

**Amazon S3（Simple Storage Service）**：物件儲存服務，以扁平鍵值結構儲存任意類型的檔案，具高耐久性（11 個 9），出站流量收費、入站免費。
`T1Q18、T2Q50、T4Q8、T6Q15`

**Amazon S3 Standard**：適用於頻繁存取資料的標準儲存類別，無最低儲存期限費用限制。
`T4Q19、T6Q44`

**Amazon S3 Intelligent-Tiering**：自動根據存取模式在不同儲存層間移動資料以節省成本，適合隨機或不可預測的存取模式，無資料取得費用。
`T4Q50、T6Q44`

**Amazon S3 Standard-IA（Infrequent Access）**：適用於不常存取但需要快速取回的資料，有最低儲存期限（30 天）及資料取得費用。
`T1Q65、T6Q44`

**Amazon S3 One Zone-IA**：只儲存於單一 AZ 的低成本不頻繁存取儲存類別，可用性最低，適合可輕易重建的資料（如縮圖）。
`T2Q44、T3Q35、T5Q38`

**Amazon S3 Glacier Flexible Retrieval**：低成本封存儲存，資料取回時間從數分鐘到數小時，適合資料封存備份。
`T3Q10`

**Amazon S3 Glacier Deep Archive**：S3 最低成本的儲存類別，適合需長達 10 年以上合規保留的資料，取回時間最長。
`T3Q61、T6Q54`

**Amazon S3 Block Public Access（封鎖公開存取）**：帳戶或儲存貯體層級的設定，確保 S3 資料不會意外公開，是保護資料的最有效方式。
`T4Q3`

**Amazon S3 Versioning（版本控制）**：保留物件的所有版本，防止意外刪除或覆寫，是 S3 資料保護的最佳方式。
`T3Q47`

**Amazon S3 Lifecycle Configuration（生命週期設定）**：定義規則自動在 S3 儲存類別間轉換物件或過期刪除物件，以節省成本。
`T4Q26、T5Q37`

**Amazon S3 Replication（S3 複寫）**：自動跨帳戶或跨區域複製 S3 物件（含中繼資料），分為 SRR（同區域）和 CRR（跨區域）。
`T3Q16、T4Q63`

**Amazon S3 Transfer Acceleration（S3TA）**：透過 CloudFront 邊緣節點加速從遠端位置上傳至 S3 的傳輸速度。
`T4Q25`

**Amazon S3 Access Logs（S3 存取日誌）**：記錄對 S3 儲存貯體發出的所有請求，用於稽核和分析存取行為。
`T5Q57`

**Amazon EBS（Elastic Block Store）**：為 EC2 執行個體提供持久性區塊儲存磁碟區，只能掛載至同一 AZ 的單一執行個體，快照以增量方式儲存於 S3。
`T2Q23、T3Q5、T3Q46、T5Q4、T6Q15`

**Amazon EFS（Elastic File System）**：可由多個 EC2 執行個體跨 AZ、跨 VPC、跨區域同時掛載的全受管 NFS 檔案系統，預設支援高可用性。
`T2Q13、T2Q23、T3Q21、T3Q29、T3Q49、T4Q52、T6Q15`

**Amazon FSx for Windows File Server**：提供 Windows 原生 SMB 協定的全受管檔案儲存服務，適合 Windows 應用程式。
`T2Q34`

**Amazon FSx for Lustre**：高效能並行檔案系統，適用於機器學習和高效能運算（HPC）工作負載。
`T2Q34`

**AWS Storage Gateway**：連接本地環境與 AWS 雲端儲存的混合雲儲存服務，支援 File、Volume 和 Tape 三種閘道類型，預設加密。
`T2Q62、T6Q14`

**Amazon S3 EBS Snapshots（EBS 快照）**：EBS 磁碟區的時間點備份，以增量方式儲存於 S3，可用於跨 AZ 複製資料。
`T3Q46、T5Q17`

**AWS DataSync**：自動化、加速本地系統與 AWS 儲存服務（S3、EFS）之間的線上資料傳輸，支援增量備份。
`T5Q6`

---

## 資料庫服務

**Amazon RDS（Relational Database Service）**：全受管關聯式資料庫服務，AWS 負責修補底層作業系統，客戶負責資料庫加密等設定。
`T1Q25、T2Q29、T2Q47、T4Q20、T4Q62、T6Q5`

**Amazon RDS Multi-AZ（多可用區部署）**：主資料庫同步複寫至待機執行個體，AZ 故障時自動容錯移轉，同一端點無需手動干預，主要提升可用性。
`T1Q41、T2Q29`

**Amazon RDS Read Replica（讀取副本）**：非同步複製的唯讀資料庫副本，主要用於提升讀取擴展性，也可在主區域故障時提升韌性。
`T2Q19、T3Q48`

**Amazon Aurora**：AWS 自研的高效能關聯式資料庫，相容 MySQL 與 PostgreSQL，AWS 自動修補底層 OS，適合 CRM 等企業應用。
`T1Q15、T6Q5`

**Amazon DynamoDB**：全受管的 NoSQL 鍵值與文件資料庫，提供毫秒級效能、彈性結構描述，預設支援高可用性。
`T2Q45、T2Q48、T3Q49、T4Q7、T6Q41`

**Amazon DynamoDB Global Tables（全球資料表）**：DynamoDB 的多區域主動-主動複製功能，適合需跨區域高可用的應用程式。
`T1Q63`

**Amazon DynamoDB Accelerator（DAX）**：DynamoDB 的記憶體快取層，可將讀取效能提升至微秒級，解決讀取密集型瓶頸。
`T6Q43`

**Amazon ElastiCache**：全受管的記憶體快取服務，支援 Redis 與 Memcached，用於降低資料庫讀取負載、減少應用程式延遲。
`T5Q42、T6Q43`

**Amazon Neptune**：全受管的圖形資料庫服務（NoSQL），適合建立知識圖譜、社交網路等高度關聯性資料應用。
`T6Q25、T6Q41`

**Amazon DocumentDB**：相容 MongoDB 的全受管文件資料庫服務（NoSQL），支援靈活結構描述。
`T6Q41`

**Amazon Redshift**：用於大規模 PB 級資料倉儲與 OLAP（線上分析處理）的全受管服務。
`T1Q14、T3Q32、T6Q9`

**Amazon MemoryDB for Redis**：相容 Redis 的持久性記憶體資料庫服務。
（見 ElastiCache）

**AWS Database Migration Service（DMS）**：協助將資料庫從本地或其他雲端遷移至 AWS 的服務。
`T3Q14`

---

## 網路服務

**Amazon VPC（Virtual Private Cloud）**：在 AWS 雲端中建立邏輯隔離私有網路的服務，跨越一個區域內的所有 AZ，子網路只跨一個 AZ。
`T2Q55、T4Q1、T5Q39、T6Q56`

**Subnet（子網路）**：VPC 內依 AZ 劃分的網路區段，只存在於單一 AZ 中。
`T2Q55、T4Q44`

**Internet Gateway（網際網路閘道）**：允許 VPC 內資源與公共網際網路通訊的 VPC 元件。
`T4Q44`

**NAT Gateway（NAT 閘道）**：由 AWS 全受管的網路位址轉換服務，允許私有子網路中的執行個體存取網際網路，但不允許外部發起連線。
`T1Q36`

**Security Group（安全群組）**：作為虛擬防火牆在執行個體層級控制入站與出站流量，有狀態（stateful）、只能設定允許規則、支援 CIDR 表示法。
`T2Q57、T3Q54、T4Q1、T6Q47、T6Q60、T6Q61`

**Network ACL（網路存取控制清單）**：在子網路層級控制進出流量的無狀態（stateless）防火牆，包含有編號的規則清單（按遞增順序評估），可設定允許和拒絕規則，支援 CIDR 表示法。
`T1Q36、T2Q57、T3Q54、T5Q1、T6Q60`

**VPC Peering Connection（VPC 對等連線）**：兩個 VPC 之間的私有直接連線，適用於同組織內少數 VPC 間的資料共享。
`T4Q2`

**AWS Transit Gateway**：將多個 VPC 和本地網路連接至單一中樞閘道的網路路由服務，適合大規模多 VPC 架構。
`T1Q11、T3Q50、T4Q14`

**VPC Endpoint（VPC 端點）**：讓 VPC 私密連接至 AWS 服務而不經過公開網際網路，分為 Gateway Endpoint（S3、DynamoDB）和 Interface Endpoint（其他服務）。
`T1Q17、T3Q27、T4Q46`

**AWS PrivateLink**：讓 VPC 私密存取 AWS 服務或其他 VPC 服務的介面端點技術，不需要 IGW 或 NAT。
`T1Q11、T6Q56`

**AWS Direct Connect**：在企業本地資料中心與 AWS 之間建立私有、專用實體網路連線，提供高頻寬與穩定延遲。
`T1Q31、T2Q17、T3Q53（非答案）、T4Q14、T5Q53、T6Q23`

**AWS Site-to-Site VPN**：透過公共網際網路在本地網路與 AWS VPC 之間建立加密 IPSec 隧道連線，由虛擬私有閘道（VGW）和客戶閘道（CGW）組成。
`T2Q17、T3Q38、T5Q8、T6Q23`

**Virtual Private Gateway（VGW，虛擬私有閘道）**：Site-to-Site VPN 在 AWS 端的元件。
`T3Q38`

**Customer Gateway（CGW，客戶閘道）**：Site-to-Site VPN 在客戶本地端的元件，由客戶自行設定。
`T3Q38、T5Q8`

**Amazon Route 53**：AWS 提供的高可用性 DNS 服務，提供網域註冊、健康檢查、多種路由政策。
`T5Q22`

**Route 53 Simple Routing（簡單路由）**：將流量導向單一資源的最基本路由政策。
`T4Q21`

**Route 53 Weighted Routing（加權路由）**：依照設定的權重比例將流量分配至多個資源，可控制各資源接收的流量比例。
`T1Q2`

**Route 53 Latency-based Routing（延遲型路由）**：將請求路由至提供最低延遲 AWS 端點的路由政策，改善使用者效能。
`T2Q51`

**Route 53 Failover Routing（容錯移轉路由）**：主動-被動設定，主要資源故障時自動切換至備援資源的路由政策。
`T3Q8`

**Amazon CloudFront**：全球 CDN（內容傳遞網路）服務，將內容快取至全球 Edge Location 邊緣節點以降低延遲、提升靜態網站效能。
`T3Q55、T6Q23`

**Amazon API Gateway**：用於建立、發布、維護和監控 RESTful 及 WebSocket API 的全受管服務，可呼叫 Lambda 建立無伺服器應用程式前端。
`T6Q51、T6Q59`

**AWS Elastic Load Balancing（ELB）**：參見運算服務區段。
`T1Q7`

---

## 邊緣與混合雲服務

**AWS Outposts**：將 AWS 基礎設施、服務、API 和工具延伸至客戶本地資料中心的全受管機架式設備，適合低延遲或資料駐留需求。
`T6Q29`

**AWS Wavelength**：將 AWS 運算與儲存服務部署至電信業者 5G 網路邊緣，讓行動裝置使用者獲得超低延遲。
`T6Q39`

**AWS Local Zones**：將 AWS 服務延伸至靠近特定大城市的地點，提供個位數毫秒延遲，適合媒體製作、遊戲等場景。
`T2Q31`

**AWS Snow Family（Snow 系列）**：用於大量資料離線遷移至 AWS 或在邊緣位置執行運算的實體裝置系列。
`T3Q14、T3Q64`

**AWS Snowball**：PB 級資料離線傳輸至 AWS 的實體儲存裝置，適合頻寬有限的遠端位置資料遷移。
`T3Q64`

**AWS Snowball Edge**：具備邊緣運算能力的 Snowball 裝置，可在本地進行資料處理後再傳至 AWS。
`T6Q31`

**AWS OpsHub**：提供圖形介面管理 AWS Snow 系列裝置的工具，無需命令列或 REST API。
`T6Q7`

---

## 安全與身份服務

**AWS IAM（Identity and Access Management）**：管理 AWS 使用者、群組、角色與存取權限的全球性服務，本身免費。
`T2Q5、T2Q6、T2Q18、T2Q33、T3Q31、T4Q35、T5Q31`

**IAM User（IAM 使用者）**：代表與 AWS 互動的人員或應用程式的 IAM 實體，Access Key ID 和 Secret Access Key 與 IAM 使用者綁定。
`T2Q18`

**IAM Role（IAM 角色）**：可被 AWS 服務或使用者臨時承擔的身份，是讓 EC2 執行個體存取 DynamoDB 等服務的推薦方式。
`T4Q53`

**IAM Policy（IAM 政策）**：以 JSON 定義的權限文件，必要元素為 Effect 和 Action，應遵循最小權限原則。
`T3Q44`

**IAM Credentials Report（IAM 憑證報告）**：列出帳戶中所有 IAM 使用者及其密碼、存取金鑰、MFA 裝置等狀態的報告。
`T4Q43`

**IAM Access Advisor（IAM 存取顧問）**：顯示 IAM 使用者實際存取各服務的時間，協助審查並縮減過多權限。
`T5Q44`

**MFA（Multi-Factor Authentication／多重要素驗證）**：在密碼之外額外要求第二驗證因素，強烈建議為根使用者帳戶啟用。
`T2Q40、T3Q4、T3Q31、T4Q35、T4Q61、T6Q27`

**Virtual MFA Device（虛擬 MFA 裝置）**：使用智慧型手機 Authenticator App 實現 MFA，無需攜帶實體裝置。
`T3Q4、T4Q27`

**U2F Security Key（U2F 安全金鑰）**：插入 USB 連接埠的實體安全金鑰，用於 AWS MFA 驗證。
`T4Q27`

**Hardware MFA Device（硬體 MFA 裝置）**：產生一次性密碼的實體 Token 裝置。
`T3Q4`

**Access Key ID & Secret Access Key（存取金鑰）**：與 IAM 使用者綁定，用於程式化存取 AWS API、CLI 和 SDK 的憑證。
`T1Q39、T2Q18`

**AWS IAM Identity Center（前身 AWS SSO）**：集中管理多個 AWS 帳戶的存取，並支援單一登入（SSO）。
`T5Q27`

**Amazon Cognito**：為 Web 和行動應用程式提供使用者註冊、登入和存取控制的服務。
`T5Q15`

**AWS Security Token Service（AWS STS）**：為受信任使用者提供臨時、有限權限安全憑證的服務。
`T5Q40`

**AWS KMS（Key Management Service）**：建立和管理加密金鑰的全受管服務，支援 AWS 受管金鑰、客戶受管金鑰等多種類型。
`T1Q4、T6Q24`

**Customer Managed Key（CMK，客戶受管金鑰）**：由客戶自行在 KMS 中建立和管理的加密金鑰，提供最高控制度。
`T1Q4、T6Q24`

**AWS Managed Key（AWS 受管金鑰）**：AWS 自動為每項服務在客戶帳戶中建立與管理的加密金鑰，最省力的加密方式。
`T6Q24`

**AWS CloudHSM**：使用硬體安全模組（HSM）在雲端執行加密操作的服務，滿足需要硬體裝置加密的法規要求。
`T2Q16、T5Q5`

**AWS Secrets Manager**：安全儲存、管理和自動輪換資料庫密碼、API 金鑰等機密資訊的服務。
`T1Q4（選項）`

**Amazon GuardDuty**：持續分析 CloudTrail、VPC Flow Logs、DNS 日誌，偵測 AWS 帳戶和工作負載中惡意活動與威脅的服務。
`T3Q9、T5Q11、T6Q38`

**Amazon Inspector**：自動評估 EC2 執行個體和容器應用程式安全漏洞與偏離最佳實務的服務，不追蹤設定變更。
`T1Q38、T2Q2、T5Q10、T6Q38`

**Amazon Macie**：使用機器學習自動發現和保護 Amazon S3 中敏感資料（如個人識別資訊 PII）的全受管服務。
`T1Q20、T5Q18`

**Amazon Detective**：利用 CloudTrail 日誌、VPC Flow Logs 和 GuardDuty 調查結果，自動分析安全事件根本原因的服務。
`T6Q12、T6Q38`

**AWS Security Hub**：集中彙整和管理多項 AWS 安全服務警報，提供統一安全態勢視圖的服務。
`T6Q38`

**AWS Shield Standard**：預設為所有 AWS 客戶免費啟用的基本 DDoS 防護服務。
`T1Q35、T2Q65、T3Q58`

**AWS Shield Advanced**：付費的進階 DDoS 防護服務，保護 EC2、CloudFront、Route 53、ELB、Global Accelerator 等，並提供費用保護和 DRT 支援。
`T1Q12、T3Q42、T4Q16`

**AWS WAF（Web Application Firewall）**：在第 7 層（應用層）保護 Web 應用程式免受 SQL 注入、XSS 等攻擊，可部署於 CloudFront、ALB、API Gateway 和 AppSync。
`T2Q3、T2Q38、T2Q65、T4Q11、T5Q32、T6Q59`

**AWS Artifact**：提供 AWS 安全和合規報告（如 HIPAA、PCI、SOC）以及合規相關文件的自助服務入口。
`T1Q50、T4Q5`

**AWS Acceptable Use Policy（可接受使用政策）**：描述 AWS 服務禁止使用行為的政策文件。
`T2Q59`

**Penetration Testing（滲透測試）**：客戶無需事先取得 AWS 批准即可對自己的 AWS 基礎設施進行安全評估的實踐。
`T3Q22`

**VPC Flow Logs（VPC 流量日誌）**：捕獲 VPC 中網路介面進出流量資訊的日誌，用於安全分析和故障排除。
`T6Q12`

**AWS Abuse Team（濫用團隊）**：負責處理 AWS 資源被用於惡意行為（如連接埠掃描、DDoS）投訴的專責團隊。
`T1Q43、T6Q21`

---

## 監控與管理服務

**Amazon CloudWatch**：監控 AWS 資源指標、日誌和事件，設定警報（如 CPU 超過 80% 發送 SNS 通知）的服務，帳單指標資料儲存於 us-east-1。
`T2Q30、T3Q3、T3Q65、T4Q13、T4Q40、T5Q56、T6Q26`

**AWS CloudTrail**：記錄所有 AWS 帳戶 API 呼叫與使用者操作的稽核日誌服務，預設記錄管理事件，日誌預設加密。
`T1Q3、T3Q1（非答案）、T6Q47、T6Q63`

**AWS CloudTrail Insights**：分析 CloudTrail 管理事件，自動偵測異常 API 活動（如異常資源佈建）並發出警報的功能。
`T6Q55`

**AWS Config**：持續追蹤 AWS 資源設定變更歷史並評估合規性的服務，適合提交歷史設定給稽核單位。
`T2Q41、T3Q1、T5Q34、T6Q6`

**AWS Trusted Advisor**：依據 AWS 最佳實務，針對成本、效能、安全、容錯與服務限制提供建議的工具；Basic/Developer 方案只能存取核心檢查。
`T1Q24、T2Q28、T3Q60、T3Q63、T4Q24、T4Q56、T5Q45`

**AWS Well-Architected Tool**：透過回答問卷來審查工作負載並與 AWS 架構最佳實務比較的免費工具。
`T6Q58`

**AWS Systems Manager（SSM）**：集中管理 EC2 和本地伺服器（收集軟體庫存、執行命令、修補伺服器）的運維自動化服務。
`T4Q12、T5Q61`

**AWS Systems Manager Session Manager**：提供安全的瀏覽器 Shell 存取 EC2 執行個體，無需開啟 SSH 連接埠或使用公用 IP。
`T2Q49`

**AWS Health Dashboard – Service Health**：發布所有 AWS 服務在所有區域的一般狀態和可用性資訊的儀表板，可訂閱 RSS feed。
`T2Q52、T5Q26`

**AWS Health Dashboard – Your Account Health**：提供特定帳戶中 AWS 資源受影響事件的個人化視圖，在所有支援方案中均可使用。
`T2Q12、T3Q26、T4Q22`

**AWS X-Ray**：分析和偵錯分散式微服務和無伺服器應用程式效能問題的追蹤服務。
`T1Q60`

**AWS CloudFormation**：以 JSON 或 YAML 範本定義和自動化佈建 AWS 基礎設施的 IaC（基礎設施即程式碼）服務。
`T4Q45`

**AWS Cloud Development Kit（AWS CDK）**：使用 Python、JavaScript 等常見程式語言定義雲端基礎設施的開發框架，最終生成 CloudFormation 範本。
`T5Q28`

**AWS Knowledge Center**：提供 AWS 客戶最常見問題和解答的知識庫論壇。
`T3Q15`

---

## 開發者工具

**AWS CodeCommit**：私有的 Git 程式碼儲存庫服務，提供版本控制功能。
`T6Q10`

**AWS CodeBuild**：全受管的持續整合服務，負責編譯程式碼和執行測試。
`T6Q10`

**AWS CodeDeploy**：自動化將應用程式程式碼部署至 EC2 執行個體及本地執行個體的服務。
`T3Q2、T4Q29`

**AWS CodePipeline**：自動化軟體發布流程（原始碼→建置→測試→部署）的持續交付服務。
`T6Q10`

**AWS CodeStar**：快速開發、建置和部署 AWS 應用程式的整合開發專案管理服務。
`T6Q10`

**AWS CodeArtifact**：全受管的套件儲存庫服務，整合 Maven、npm、Gradle 等套件管理工具，維護應用程式相依性。
`T6Q64`

**Amazon CodeGuru**：使用機器學習自動化程式碼審查、識別程式碼缺陷並提供改善建議的服務。
`T5Q30`

**AWS Software Development Kit（SDK）**：提供程式語言特定 API 以程式化存取 AWS 服務的工具套件。
`T1Q56、T2Q42`

**AWS CLI（Command Line Interface）**：透過命令列介面管理 AWS 服務的工具。
`T2Q42`

**AWS Management Console（管理主控台）**：透過 Web 瀏覽器管理 AWS 服務的圖形介面。
`T2Q42`

**AWS Device Farm**：提供真實行動裝置和瀏覽器的測試服務，可跨不同韌體和 OS 版本進行測試。
`T4Q64`

**AWS Fault Injection Simulator（AWS FIS）**：用於實施混沌工程、注入故障以測試應用程式韌性的服務。
`T5Q19`

---

## 分析與 AI/ML 服務

**Amazon Kinesis Data Streams**：即時擷取和處理串流大數據的服務，適合廣告技術等即時分析場景。
`T6Q9、T6Q51`

**Amazon EMR（Elastic MapReduce）**：用於在 Hadoop/Spark 叢集上執行大數據工作負載的受管服務。
`T2Q25、T6Q9`

**Amazon Athena**：直接對 S3 資料使用標準 SQL 進行互動式查詢的無伺服器分析服務。
`T2Q61、T6Q8`

**Amazon QuickSight**：建立互動式商業智慧儀表板的全受管 BI 服務，可從任何裝置存取。
`T6Q8`

**AWS Glue**：全受管的無伺服器 ETL（Extract, Transform, Load）資料整合服務，用於準備分析用資料。
`T5Q20、T6Q8`

**Amazon SageMaker**：提供完整機器學習工作流程（建置、訓練、部署模型）的全受管平台。
`T5Q60、T6Q8`

**Amazon Forecast**：基於機器學習的時間序列預測服務，如預測網站流量、銷售量等。
`T6Q53`

**Amazon Rekognition**：提供影像和影片分析（物件識別、人臉辨識、文字偵測等）的 AI 服務，屬於 SaaS 型服務，不支援快速縮圖調整。
`T2Q14、T2Q22、T3Q17、T3Q51`

**Amazon Transcribe**：將語音自動轉換為文字的 AI 服務，用於語音輸入分析。
`T1Q27、T6Q49`

**Amazon Polly**：將文字轉換為自然語音的 AI 服務，用於語音輸出。
`T1Q27`

**Amazon Translate**：提供神經機器翻譯的 AI 服務，可轉換不同語言的文字內容。
`T4Q32`

**Amazon Comprehend**：用於自然語言處理（NLP）的 AI 服務，可分析文字情感、擷取實體與關鍵字。
`T6Q49`

**Amazon Lex**：使用自然語言理解（NLU）建立聊天機器人和語音介面的 AI 服務（Alexa 底層技術）。
`T5Q21`

**Amazon Kendra**：使用機器學習的智慧企業搜尋服務，可從 PDF、Word 等文件中擷取答案。
`T3Q18`

**Amazon Personalize**：根據使用者歷史資料提供個人化推薦（如電影、產品推薦）的 AI 服務。
`T5Q16`

**Amazon Elastic Transcoder**：將 S3 媒體檔案轉換為適合行動裝置等各種格式播放的媒體轉碼服務。
`T6Q49`

**Amazon OpenSearch Service**：用於日誌分析、全文搜尋和即時應用程式監控的分散式搜尋服務。
`T1Q7（選項）`

---

## 應用程式整合

**Amazon SQS（Simple Queue Service）**：全受管的訊息佇列服務，用於解耦應用程式元件並確保訊息不遺失，適合系統間非同步通訊。
`T1Q21、T2Q30（選項）、T5Q13、T6Q62`

**Amazon SNS（Simple Notification Service）**：全受管的發布/訂閱訊息通知服務，可向多個訂閱者（Email、SQS、Lambda）發送通知。
`T1Q21、T2Q30、T4Q13、T6Q62`

**Amazon MQ**：全受管的訊息代理服務，相容 Apache ActiveMQ 和 RabbitMQ，適合遷移現有本地訊息代理功能。
`T2Q64`

**Amazon EventBridge**：無伺服器事件匯流排服務，可根據排程或事件觸發 Lambda 等服務。
`T2Q7`

**AWS Step Functions**：用於編排多個 Lambda 函數和 AWS 服務的無伺服器工作流程服務。
`T2Q7（選項）`

**Amazon AppStream 2.0**：將桌面應用程式串流至瀏覽器的服務，無需採購或管理伺服器。
`T6Q3`

**AWS IoT Core**：讓任意數量的 IoT 裝置安全連接至雲端的全受管服務，無需佈建伺服器。
`T6Q35`

**Amazon Connect**：雲端基礎的客服中心服務，提供語音和聊天支援。
`T6Q35（選項）`

**Amazon Pinpoint**：向使用者發送推播通知、Email、SMS 的行銷訊息傳遞服務。
`T1Q60（選項）`

---

## 架構與治理框架

**AWS Well-Architected Framework**：AWS 官方提供的六大支柱雲端架構最佳實務框架（卓越營運、安全性、可靠性、效能效率、成本優化、永續性）。
`T2Q32、T6Q40`

**Operational Excellence Pillar（卓越營運支柱）**：著重自動化、頻繁小型可回復變更、預測故障、維護 IaC 的支柱。
`T3Q34、T5Q7`

**Security Pillar（安全性支柱）**：著重使用 KMS 加密資料、啟用追蹤能力的支柱。
`T5Q33`

**Reliability Pillar（可靠性支柱）**：著重水平擴展（scale out）實現容錯，而非垂直擴展（scale up）的支柱。
`T1Q44`

**Performance Efficiency Pillar（效能效率支柱）**：著重根據工作負載需求選擇正確資源類型與大小（right-sizing）的支柱。
`T4Q31、T6Q40`

**Cost Optimization Pillar（成本優化支柱）**：著重降低不必要支出、選擇正確定價模型的支柱。
`T2Q32`

**AWS Cloud Adoption Framework（AWS CAF）**：指導組織雲端採用旅程的框架，包含業務、人員、治理、平台、安全、營運六大觀點。
`T1Q47、T2Q35、T2Q37、T3Q13、T4Q57`

**Business Perspective（業務觀點）**：CAF 中確保 IT 投資與業務目標對齊的觀點，涵蓋策略管理能力。
`T3Q13、T4Q57`

**Platform Perspective（平台觀點）**：CAF 中由 CTO 和工程師主導的觀點，負責建立雲端平台。
`T1Q59`

**Operations Perspective（營運觀點）**：CAF 中負責效能、容量管理的觀點。
`T2Q37`

**AWS Migration Strategies（遷移策略 6R）**：雲端遷移的六種策略：Rehost（直接搬移）、Replatform（重新平台化）、Refactor（重構）、Repurchase（重新購買）、Retain（保留）、Retire（淘汰）。
`T1Q25、T5Q48`

**Rehost（重新託管／Lift and Shift）**：不修改程式碼直接將應用程式搬移至 AWS，遷移速度最快。
`T5Q48`

**Replatform（重新平台化）**：進行少量最佳化（如改用 RDS 托管資料庫）但不變更核心架構。
`T1Q25`

**AWS Control Tower**：提供預定義藍圖和護欄，協助客戶快速建立符合最佳實務的多帳戶 AWS 登陸區（Landing Zone）的原生服務。
`T6Q34`

**AWS Organizations**：集中管理和治理多個 AWS 帳戶的服務，支援統一帳單、SCP 和批量折扣共享，帳戶移除前必須能獨立運作。
`T1Q9、T2Q63、T4Q47`

**Service Control Policies（SCP，服務控制政策）**：在 AWS Organizations 中限制成員帳戶最大可用權限的組織政策，只能限制不能授予。
`T6Q34`

**AWS Shared Responsibility Model（共同責任模型）**：定義 AWS 與客戶各自負責的安全責任，AWS 負責「雲端本身的安全」（實體、網路、虛擬化），客戶負責「雲端中的安全」（OS、應用程式、資料）。共同責任領域包含設定管理、作業系統設定等。
`T1Q13、T1Q19、T2Q9、T2Q15、T2Q47、T3Q56、T3Q58、T3Q59、T4Q34、T5Q25、T5Q29、T5Q55、T6Q13、T6Q20、T6Q57`

**AWS Architecture Center（架構中心）**：提供 AWS 官方雲端解決方案設計範例與參考架構的知識庫。
`T6Q48`

**AWS Partner Solutions（前身 Quick Starts）**：由 AWS 合作夥伴提供的自動化參考部署，可快速在 AWS 上部署常見解決方案。
`T5Q59、T6Q42`

**AWS Marketplace**：提供第三方軟體（含 SaaS、自訂 AMI）的線上商店，可直接部署至 AWS 環境，也可讓供應商銷售解決方案。
`T2Q26、T4Q39`

**AWS Service Catalog**：幫助組織管理和提供已核准 IT 服務目錄的服務，協助識別正確 AWS 服務。
`T2Q23`

**AWS Resource Groups（資源群組）**：組織 AWS 資源並支援大量資源批次管理與自動化的功能。
`T6Q65`

**Tags（標籤）**：附加在 AWS 資源上的鍵值對，用於分類、搜尋與成本分配，每個鍵對每個資源必須唯一。
`T3Q62、T5Q65、T6Q22`

**AWS Professional Services**：AWS 官方的專業服務團隊，協助客戶加速雲端遷移和基礎設施建置。
`T1Q6`

**AWS Partner Network（APN）**：AWS 授權合作夥伴網路，分為 APN 技術合作夥伴（提供技術產品）和 APN 諮詢合作夥伴（提供遷移建議與服務）。
`T1Q6、T1Q64、T2Q23`

---

## 基礎設施概念

**AWS Region（區域）**：由多個地理上分離的可用區組成的 AWS 基礎設施地理範圍，每個區域至少包含三個 AZ。
`T1Q34、T3Q23、T6Q4、T6Q11`

**Availability Zone（AZ，可用區）**：AWS 區域內一個或多個實體分離的資料中心群，AZ 間流量預設加密，是實現高可用性的基本單位。
`T1Q34、T6Q4、T6Q11`

**Edge Location（邊緣位置）**：CloudFront CDN 的快取節點，分佈在全球各大城市，數量遠多於 AWS 區域。
`T2Q15`

**Amazon WorkSpaces**：全受管的雲端虛擬桌面服務（DaaS），為全球性交付（非區域性）服務。
`T6Q37`

**AWS Transfer Family**：將檔案透過 SFTP、FTPS、FTP 協定安全傳輸至 S3 或 EFS 的全受管服務。
`T6Q7（選項）`

---

## 災難復原

**Backup and Restore（備份與還原）**：成本最低的 DR 策略，RPO/RTO 最長（數小時），適合可容忍較長恢復時間的場景。
`T6Q16`

**Pilot Light（導引燈）**：在雲端維持最小核心系統運行，災難時快速擴展完整環境的 DR 策略，成本次低。
`T6Q16`

**Warm Standby（暖備）**：在雲端維持縮小版的完整環境持續運行，災難時快速擴展至正式規模，適合 24/7 業務但可接受縮減規模的場景。
`T4Q38、T6Q16`

**Multi-Site Active/Active（多站點主動/主動）**：成本最高但 RTO/RPO 最短的 DR 策略，多個站點同時提供完整服務。
`T6Q16`

**CloudEndure Disaster Recovery**：提供持續複製的 DR 服務，可將實體、虛擬和雲端伺服器快速恢復至 AWS。
`T6Q31`

**RDS Multi-AZ vs Read Replica**：Multi-AZ 主要提升可用性（自動容錯移轉）；Read Replica 主要提升讀取擴展性（也可用於 DR）。
`T2Q29、T3Q48、T4Q20`

---

## AWS 支援計畫

**AWS Basic Support（基本支援）**：免費提供，包含帳戶帳單問題諮詢、服務健康檢查及核心 Trusted Advisor 檢查（7 項）。
`T2Q24、T6Q28、T6Q33`

**AWS Developer Support（開發人員支援）**：付費計畫，含核心 Trusted Advisor 檢查、工作時間 Email 技術支援，無電話支援。
`T1Q24、T2Q24、T6Q28`

**AWS Business Support（商業支援）**：付費計畫，提供全套 Trusted Advisor 檢查、24/7 電話技術支援、第三方軟體互操作指導，是最具成本效益的電話支援方案。
`T1Q1、T2Q10（Enterprise）、T2Q43、T5Q3、T6Q28`

**AWS Enterprise On-Ramp Support**：介於商業和企業之間的方案，提供 TAM 池（非指定）存取。
`T1Q1（選項）`

**AWS Enterprise Support（企業支援）**：最高級支援計畫，包含指定技術客戶經理（TAM）、AWS Concierge、Infrastructure Event Management、第三方軟體互操作指導。
`T1Q16、T2Q10、T4Q65、T6Q28`

**Technical Account Manager（TAM，技術客戶經理）**：僅企業支援計畫提供的專屬 AWS 技術顧問，協助優化 AWS 環境。
`T2Q10、T6Q28`

**AWS Concierge**：企業支援計畫提供的專屬帳單與帳戶管理顧問服務。
`T6Q28`

---

*共收錄約 160 個 AWS 專有名詞｜題目來源：Practice Test T1–T6（每套 65 題）*
