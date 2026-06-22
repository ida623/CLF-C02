# AWS 填空練習｜新手白話版

這份是從 `AWS填空練習.md` 重新整理出來的版本。寫法會刻意白話一點，假設你還不熟 AWS、雲端、伺服器、網路這些詞。

使用方式很簡單：

1. 先看每題的白話提示，猜 `___` 裡面是哪個 AWS 名詞。
2. 猜完再展開「答案」。
3. 如果答錯，不用硬背，先想「這個服務是在解決什麼問題」。

---

## 1. 雲端運算模型

這一章先分清楚「你自己要管多少東西」。雲端服務越高階，AWS 幫你管越多；越底層，你能控制越多，但也要自己負責更多。

1. `___`：你直接使用現成軟體，例如線上信箱或 CRM。伺服器、系統、更新都不用你管。
2. `___`：AWS 幫你準備好開發和部署平台，你主要負責寫程式、放程式。
3. `___`：AWS 提供虛擬伺服器、硬碟、網路等底層資源，你要自己安裝和管理系統。
4. `___`：公司同時使用自己的機房和 AWS 雲端，兩邊一起合作。
5. `___`：所有資源都跑在雲端供應商的環境裡，不放在公司自己的機房。
6. `___`：雲端環境只給單一公司自己使用，通常放在公司自己的資料中心。

<details>
<summary>答案</summary>

1. SaaS（Software as a Service／軟體即服務）
2. PaaS（Platform as a Service／平台即服務）
3. IaaS（Infrastructure as a Service／基礎設施即服務）
4. Hybrid Cloud（混合雲）
5. Public Cloud（公有雲）
6. Private Cloud（私有雲）

</details>

---

## 2. 雲端優勢與基本概念

這一章是在學「為什麼大家要用雲端」。核心想法是：快、彈性、可靠、能省錢，也比較容易自動化。

1. `___`：需要新資源時可以很快取得，不用等買機器、拉線、進機房。
2. `___`：流量多就自動加資源，流量少就縮回來，避免浪費錢。
3. `___`：系統可以隨著需求變大而變大，例如使用者變多也能撐住。
4. `___`：系統能穩定運作，不容易因為小故障就整個壞掉。
5. `___`：服務盡量保持可用，就算某個資料中心出問題，使用者也不容易感覺到。
6. `___`：很多客戶一起使用 AWS，AWS 的規模很大，所以能把單位成本壓低。
7. `___`：增加更多台機器來分擔工作。
8. `___`：把同一台機器升級成更強，例如更多 CPU 或記憶體。
9. `___`：系統元件不要綁太死，彼此用 API 或訊息溝通，壞一個不容易拖垮全部。
10. `___`：用程式碼建立和管理雲端資源，而不是每次都靠人工點選。
11. `___`：算總成本時，不只算伺服器價格，也要算電力、冷卻、人力、機房維護等。

<details>
<summary>答案</summary>

1. Agility（敏捷性）
2. Elasticity（彈性）
3. Scalability（可擴展性）
4. Reliability（可靠性）
5. High Availability（高可用性）
6. Economies of Scale（規模經濟）
7. Horizontal Scaling（水平擴展／向外擴展）
8. Vertical Scaling（垂直擴展／向上擴展）
9. Loose Coupling（鬆耦合）
10. Infrastructure as Code（IaC，基礎設施即程式碼）
11. Total Cost of Ownership（TCO，總持有成本）

</details>

---

## 3. 定價與成本管理

這一章是在學「AWS 怎麼收錢，以及怎麼避免花冤枉錢」。考試很常問：哪種工作負載適合哪種付費方式。

1. `___`：你承諾會用一定金額的運算資源，AWS 就給你折扣。
2. `___`：比較彈性的節省方案，可套用到 EC2、Fargate、Lambda 等運算服務。
3. `___`：針對特定 EC2 類型與區域承諾用量，折扣通常更好，但彈性較低。
4. `___`：先承諾使用 EC2 一年或三年，換取很大的折扣，而且不會被 AWS 中斷。
5. `___`：保留期間內可以換機型或作業系統，比較有彈性。
6. `___`：折扣高但變更彈性較低，適合需求很固定的 EC2。
7. `___`：使用 AWS 暫時沒人用的閒置容量，很便宜，但 AWS 需要時會收回。
8. `___`：用多少付多少，不用預先承諾，適合短期或需求不固定的工作。
9. `___`：整台實體伺服器只給你用，常用在需要自帶授權的軟體。
10. `___`：跑在專用硬體上，但不指定固定是哪一台實體主機。
11. `___`：EC2 主機上的本機暫存磁碟，速度快，但 EC2 結束後資料可能消失。
12. `___`：用圖表看 AWS 花費，也能預測未來費用。
13. `___`：設定預算上限，快超過或已超過時通知你。
14. `___`：最詳細的 AWS 費用和用量報告，通常會放到 S3。
15. `___`：幫資源貼標籤，之後可以看哪個部門、專案花了多少錢。
16. `___`：還沒建立資源前，先估算大概會花多少錢。
17. `___`：分析你的 EC2、EBS、Lambda 等資源，建議要不要調小、調大或換規格。
18. `___`：把多個 AWS 帳戶的帳單合在一起，也可以共享部分折扣。
19. `___`：AWS 給你的抵用金，可用來折抵符合條件的費用。

<details>
<summary>答案</summary>

1. Savings Plans（節省方案）
2. Compute Savings Plans（運算節省方案）
3. EC2 Instance Savings Plans（EC2 執行個體節省方案）
4. EC2 Reserved Instance（RI，保留執行個體）
5. Convertible RI（可轉換保留執行個體）
6. Standard RI（標準保留執行個體）
7. EC2 Spot Instance（Spot 執行個體）
8. EC2 On-Demand Instance（隨需執行個體）
9. EC2 Dedicated Host（專用主機）
10. EC2 Dedicated Instance（專用執行個體）
11. EC2 Instance Store（執行個體存放區）
12. AWS Cost Explorer（成本探索器）
13. AWS Budgets（預算警示）
14. AWS Cost and Usage Report（CUR，成本與用量報告）
15. AWS Cost Allocation Tags（成本分配標籤）
16. AWS Pricing Calculator（定價計算機）
17. AWS Compute Optimizer（運算資源最佳化工具）
18. Consolidated Billing（合併計費）
19. AWS Credits（AWS 信用額度）

</details>

---

## 4. 運算服務

運算服務可以先想成「在哪裡跑程式」。有些像租一台電腦，有些像你只丟程式碼，AWS 自己幫你跑。

1. `___`：AWS 上最基本的虛擬伺服器服務，你可以像管理一台電腦一樣管理它。
2. `___`：幫你自動建立和更新 EC2 映像檔或容器映像檔。
3. `___`：EC2 開機用的範本，裡面包含作業系統和預先裝好的軟體。
4. `___`：EC2 第一次開機時自動執行的腳本，例如自動安裝套件。
5. `___`：EC2 自己的資訊，例如它的 IP、映像檔 ID、所在位置等。
6. `___`：不用自己管理 SSH 金鑰，也能安全連到 EC2 的工具。
7. `___`：你只上傳程式碼，AWS 在需要時幫你執行，不用管理伺服器。
8. `___`：把程式丟上去後，AWS 幫你處理部署、擴展、負載平衡等雜事。
9. `___`：跑容器時不用自己管理底層 EC2 伺服器的運算引擎。
10. `___`：AWS 的容器管理服務，用來執行和管理 Docker 容器。
11. `___`：存放 Docker 容器映像檔的倉庫。
12. `___`：簡化版雲端主機服務，適合 WordPress、小網站、簡單資料庫。
13. `___`：根據需求自動增加或減少 AWS 資源。
14. `___`：管理一群 EC2，設定最少幾台、最多幾台、平常想維持幾台。
15. `___`：根據過去流量規律，提前幫你擴充資源。
16. `___`：適合跑大量批次工作，例如一次處理很多檔案或大量運算任務。
17. `___`：把使用者流量平均分給多台伺服器或多個目標。
18. `___`：看 HTTP/HTTPS 內容來分流，常用在網站和 API。
19. `___`：看 TCP/UDP 連線來分流，適合低延遲、高效能網路需求。
20. `___`：提供固定入口 IP，並用 AWS 全球網路把使用者導到較近、較快的端點。

<details>
<summary>答案</summary>

1. Amazon EC2（Elastic Compute Cloud，彈性運算雲端）
2. Amazon EC2 Image Builder（EC2 映像檔建置服務）
3. Amazon Machine Image（AMI，Amazon 機器映像檔）
4. EC2 User Data（使用者資料）
5. EC2 Instance Metadata（執行個體中繼資料）
6. EC2 Instance Connect（EC2 執行個體連線）
7. AWS Lambda（無伺服器函數運算）
8. AWS Elastic Beanstalk（彈性應用程式部署平台）
9. AWS Fargate（無伺服器容器運算引擎）
10. Amazon ECS（Elastic Container Service，彈性容器服務）
11. Amazon ECR（Elastic Container Registry，彈性容器映像檔倉庫）
12. Amazon Lightsail（輕量級雲端主機服務）
13. AWS Auto Scaling（自動擴展）
14. Auto Scaling Group（ASG，自動擴展群組）
15. Predictive Scaling（預測性擴展）
16. AWS Batch（批次運算）
17. AWS Elastic Load Balancing（ELB，彈性負載平衡）
18. Application Load Balancer（ALB，應用程式負載平衡器）
19. Network Load Balancer（NLB，網路負載平衡器）
20. AWS Global Accelerator（全球加速器）

</details>

---

## 5. EC2 執行個體類型

EC2 類型可以想成不同規格的電腦：有的記憶體大，有的 CPU 強，有的磁碟快，有的有 GPU。

1. `___`：適合很吃記憶體的工作，例如大型資料庫或快取。
2. `___`：適合很吃 CPU 的工作，例如大量計算、批次處理。
3. `___`：適合需要很快本機硬碟的工作，例如資料倉儲或大量讀寫。
4. `___`：有 GPU 或 FPGA，適合機器學習、影像處理、3D 渲染。

<details>
<summary>答案</summary>

1. Memory Optimized（記憶體最佳化）
2. Compute Optimized（運算最佳化）
3. Storage Optimized（儲存最佳化）
4. Accelerated Computing（加速運算）

</details>

---

## 6. 儲存服務

儲存可以先分成三種：放檔案、放硬碟、放共享資料夾。S3 像大型雲端檔案櫃，EBS 像接在 EC2 上的硬碟，EFS/FSx 像多人共用資料夾。

1. `___`：AWS 的物件儲存服務，適合放圖片、影片、備份、日誌等檔案。
2. `___`：S3 預設常用儲存類別，適合常常讀取的資料。
3. `___`：AWS 會觀察資料使用情況，自動把資料放到較省錢的儲存層。
4. `___`：資料不常讀，但需要時要能很快取回。
5. `___`：資料只存在單一可用區，較便宜，適合可重新產生的資料。
6. `___`：便宜的封存儲存，取回可能要幾分鐘到幾小時。
7. `___`：更便宜、更長期的封存儲存，適合多年保存且很少取回的資料。
8. `___`：防止 S3 檔案不小心被公開給全世界看的保護設定。
9. `___`：保留同一個 S3 物件的不同版本，避免誤刪或覆蓋救不回來。
10. `___`：設定規則，讓 S3 檔案到一定時間後自動轉到便宜儲存層或刪除。
11. `___`：把 S3 物件自動複製到同區域或不同區域。
12. `___`：透過 CloudFront 邊緣節點，加快遠端使用者上傳到 S3 的速度。
13. `___`：記錄誰對 S3 bucket 做了哪些存取請求。
14. `___`：接給 EC2 使用的雲端硬碟，資料可以持久保存。
15. `___`：多台 EC2 可以一起掛載使用的 Linux NFS 共享檔案系統。
16. `___`：給 Windows 應用使用的全受管 SMB 檔案伺服器。
17. `___`：高效能檔案系統，常用在機器學習、高效能運算。
18. `___`：把公司機房的儲存和 AWS 雲端儲存接起來的混合雲服務。
19. `___`：EBS 的備份，可以用來還原硬碟或搬到其他可用區。
20. `___`：幫你把本地資料快速同步或搬到 AWS 儲存服務。

<details>
<summary>答案</summary>

1. Amazon S3（Simple Storage Service，簡單儲存服務）
2. Amazon S3 Standard（S3 標準）
3. Amazon S3 Intelligent-Tiering（智慧型分層）
4. Amazon S3 Standard-IA（Infrequent Access，不頻繁存取）
5. Amazon S3 One Zone-IA（單一可用區不頻繁存取）
6. Amazon S3 Glacier Flexible Retrieval（Glacier 彈性取回）
7. Amazon S3 Glacier Deep Archive（Glacier 深度封存）
8. Amazon S3 Block Public Access（封鎖公開存取）
9. Amazon S3 Versioning（版本控制）
10. Amazon S3 Lifecycle Configuration（生命週期設定）
11. Amazon S3 Replication（S3 複寫）
12. Amazon S3 Transfer Acceleration（S3TA，傳輸加速）
13. Amazon S3 Access Logs（S3 存取日誌）
14. Amazon EBS（Elastic Block Store，彈性區塊存放區）
15. Amazon EFS（Elastic File System，彈性檔案系統）
16. Amazon FSx for Windows File Server（適用於 Windows 的受管檔案伺服器）
17. Amazon FSx for Lustre（適用於 Lustre 的高效能檔案系統）
18. AWS Storage Gateway（儲存閘道）
19. Amazon EBS Snapshots（EBS 快照）
20. AWS DataSync（資料同步服務）

</details>

---

## 7. 資料庫服務

資料庫服務是在處理「資料要怎麼存、怎麼查、怎麼擴展」。考試常考關聯式、NoSQL、快取、資料倉儲的差異。

1. `___`：AWS 幫你管理關聯式資料庫，例如 MySQL、PostgreSQL、SQL Server。
2. `___`：RDS 在另一個可用區放備援資料庫，主資料庫壞掉時可自動切過去。
3. `___`：RDS 的唯讀副本，用來分擔查詢壓力。
4. `___`：AWS 自家的高效能關聯式資料庫，相容 MySQL 和 PostgreSQL。
5. `___`：AWS 的 NoSQL 資料庫，適合大量快速讀寫的鍵值或文件資料。
6. `___`：DynamoDB 的跨區域資料表，讓多個區域都能讀寫。
7. `___`：DynamoDB 的快取加速器，讓熱門資料讀取更快。
8. `___`：記憶體快取服務，可用 Redis 或 Memcached，常用來減少資料庫壓力。
9. `___`：圖形資料庫，適合處理人與人、物件與物件之間的關係。
10. `___`：相容 MongoDB 的文件資料庫。
11. `___`：資料倉儲服務，適合大量資料分析和商業報表。
12. `___`：把資料庫從本地或其他地方搬到 AWS 的遷移工具。

<details>
<summary>答案</summary>

1. Amazon RDS（Relational Database Service，關聯式資料庫服務）
2. Amazon RDS Multi-AZ（多可用區部署）
3. Amazon RDS Read Replica（讀取副本）
4. Amazon Aurora（AWS 自家高效能關聯式資料庫）
5. Amazon DynamoDB（NoSQL 資料庫）
6. Amazon DynamoDB Global Tables（全球資料表）
7. Amazon DynamoDB Accelerator（DAX，DynamoDB 加速器）
8. Amazon ElastiCache（記憶體快取服務）
9. Amazon Neptune（圖形資料庫）
10. Amazon DocumentDB（文件資料庫，相容 MongoDB）
11. Amazon Redshift（資料倉儲服務）
12. AWS Database Migration Service（DMS，資料庫遷移服務）

</details>

---

## 8. 網路服務

網路題目可以先想成「誰可以連到誰、流量要怎麼走」。VPC 是你的雲端私人網路，其他服務都是在幫它連內部、連外部或保護流量。

1. `___`：在 AWS 裡建立自己的私人網路空間。
2. `___`：VPC 裡更小的網路區塊，每個都屬於某一個可用區。
3. `___`：讓 VPC 裡的資源可以連到公開網際網路。
4. `___`：讓私有子網路裡的機器可以連出去上網，但外面不能主動連進來。
5. `___`：綁在 EC2 等資源上的虛擬防火牆，只要允許回應流量就會自動放行。
6. `___`：套在子網路上的防火牆，需要分別管理進站和出站規則。
7. `___`：把兩個 VPC 私下接起來，讓它們像同一個內網一樣溝通。
8. `___`：多個 VPC 和本地網路太多時，用一個中心點統一連接。
9. `___`：讓 VPC 內的資源私下連到 AWS 服務，不必走公開網際網路。
10. `___`：透過私有連線提供或使用服務，常用於私下存取 AWS 或第三方服務。
11. `___`：公司機房和 AWS 之間的專線，比一般 VPN 更穩定。
12. `___`：透過網際網路建立加密通道，把公司網路接到 AWS。
13. `___`：Site-to-Site VPN 在 AWS 這一端的閘道。
14. `___`：Site-to-Site VPN 在公司機房這一端的閘道或設備。
15. `___`：AWS 的 DNS 服務，可做網域解析、健康檢查和路由。
16. `___`：最單純的 DNS 路由，把流量導到指定目標。
17. `___`：依比例分配流量，例如 80% 到新版、20% 到舊版。
18. `___`：把使用者導向延遲最低的區域或端點。
19. `___`：主站壞掉時，自動把流量切到備援站。
20. `___`：AWS 的 CDN，把內容快取到全球邊緣節點，讓使用者更快拿到內容。
21. `___`：用來建立和管理 API 的服務，例如 REST API 或 WebSocket API。

<details>
<summary>答案</summary>

1. Amazon VPC（Virtual Private Cloud，虛擬私有雲端）
2. Subnet（子網路）
3. Internet Gateway（網際網路閘道）
4. NAT Gateway（NAT 閘道）
5. Security Group（安全群組）
6. Network ACL（網路存取控制清單）
7. VPC Peering Connection（VPC 對等連線）
8. AWS Transit Gateway（傳輸閘道）
9. VPC Endpoint（VPC 端點）
10. AWS PrivateLink（私有鏈結）
11. AWS Direct Connect（直接專線連接）
12. AWS Site-to-Site VPN（站對站 VPN）
13. Virtual Private Gateway（VGW，虛擬私有閘道）
14. Customer Gateway（CGW，客戶閘道）
15. Amazon Route 53（DNS 與路由服務）
16. Route 53 Simple Routing（簡單路由）
17. Route 53 Weighted Routing（加權路由）
18. Route 53 Latency-based Routing（延遲型路由）
19. Route 53 Failover Routing（容錯移轉路由）
20. Amazon CloudFront（內容傳遞網路 CDN）
21. Amazon API Gateway（API 閘道）

</details>

---

## 9. 邊緣與混合雲服務

這一章是在學「AWS 不只在大型區域，也能靠近使用者或放到客戶現場」。重點是降低延遲、搬大量資料、或支援本地需求。

1. `___`：把 AWS 的硬體和服務放到客戶自己的機房裡。
2. `___`：把 AWS 放到 5G 電信網路邊緣，讓手機或低延遲應用更快。
3. `___`：AWS 在大城市附近設的小型延伸區域，讓使用者延遲更低。
4. `___`：AWS 用來離線搬大量資料或在邊緣運算的一整個裝置系列。
5. `___`：把大量資料裝進實體設備，再寄送到 AWS 匯入。
6. `___`：除了搬資料，也能在本地先做一些運算處理的 Snow 裝置。
7. `___`：用圖形介面管理 Snow 裝置，不必只靠命令列。

<details>
<summary>答案</summary>

1. AWS Outposts（本地部署 AWS 服務）
2. AWS Wavelength（5G 邊緣運算）
3. AWS Local Zones（本地延伸區域）
4. AWS Snow Family（Snow 系列）
5. AWS Snowball（資料實體搬運設備）
6. AWS Snowball Edge（具運算能力的資料搬運設備）
7. AWS OpsHub（Snow 裝置圖形管理工具）

</details>

---

## 10. 安全與身份服務

這一章很重要。先記住一句話：安全不是只有 AWS 負責，你也要管好帳號、權限、加密、日誌和防護。

1. `___`：管理誰可以登入 AWS、誰可以做哪些事的服務。
2. `___`：代表一個人或一個應用程式的 AWS 身分。
3. `___`：臨時被使用的身分，常用來讓 EC2 安全存取其他 AWS 服務。
4. `___`：用 JSON 寫的權限規則，定義允許或拒絕哪些動作。
5. `___`：列出 IAM 使用者密碼、金鑰、MFA 等狀態的報告。
6. `___`：查看某個 IAM 身分最近用過哪些服務，方便移除多餘權限。
7. `___`：除了密碼之外，再加一層驗證，例如手機驗證碼。
8. `___`：用手機驗證器 App 產生 MFA 驗證碼。
9. `___`：插在 USB 或裝置上的實體安全金鑰。
10. `___`：會產生一次性驗證碼的實體 MFA 裝置。
11. `___`：程式、CLI 或 SDK 用來呼叫 AWS API 的一組金鑰。
12. `___`：集中管理多個 AWS 帳戶的登入，也就是 AWS 的單一登入服務。
13. `___`：幫網站或 App 處理使用者註冊、登入和身分驗證。
14. `___`：提供短時間有效的臨時安全憑證。
15. `___`：管理加密金鑰的服務，常用來加密資料。
16. `___`：由你自己建立和管理的 KMS 金鑰。
17. `___`：AWS 幫你建立和管理的 KMS 金鑰，操作最省事。
18. `___`：提供雲端硬體安全模組，適合法規要求很高的加密需求。
19. `___`：安全保存密碼、API Key、資料庫密碼，並可自動輪換。
20. `___`：分析帳戶和網路日誌，偵測可疑或惡意活動。
21. `___`：檢查 EC2、容器等工作負載是否有弱點或安全問題。
22. `___`：自動找出 S3 裡的敏感資料，例如身分證號、信用卡號、個資。
23. `___`：協助調查安全事件，找出事件從哪裡開始、怎麼發生。
24. `___`：集中整理多個 AWS 安全服務的警報和安全狀態。
25. `___`：AWS 免費提供的基本 DDoS 防護。
26. `___`：付費進階 DDoS 防護，包含專家支援與成本保護。
27. `___`：保護網站免於常見 Web 攻擊，例如 SQL Injection、XSS。
28. `___`：下載 AWS 合規報告和安全文件的入口。
29. `___`：記錄 VPC 網路流量，用於安全分析和除錯。
30. `___`：處理 AWS 資源被用來攻擊、掃描或濫用的通報團隊。

<details>
<summary>答案</summary>

1. AWS IAM（Identity and Access Management，身份與存取管理）
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
12. AWS IAM Identity Center（前身 AWS SSO，AWS 單一登入服務）
13. Amazon Cognito（使用者身份驗證服務）
14. AWS Security Token Service（AWS STS，安全臨時憑證服務）
15. AWS KMS（Key Management Service，金鑰管理服務）
16. Customer Managed Key（CMK，客戶受管金鑰）
17. AWS Managed Key（AWS 受管金鑰）
18. AWS CloudHSM（雲端硬體安全模組）
19. AWS Secrets Manager（密碼與機密管理）
20. Amazon GuardDuty（威脅偵測服務）
21. Amazon Inspector（安全弱點評估）
22. Amazon Macie（敏感資料自動探索）
23. Amazon Detective（安全事件調查）
24. AWS Security Hub（安全狀態集中管理）
25. AWS Shield Standard（標準 DDoS 防護）
26. AWS Shield Advanced（進階 DDoS 防護）
27. AWS WAF（Web Application Firewall，網頁應用防火牆）
28. AWS Artifact（合規報告下載入口）
29. VPC Flow Logs（VPC 流量日誌）
30. AWS Abuse Team（濫用團隊）

</details>

---

## 11. 監控與管理服務

這一章是在學「出事前怎麼知道、出事後怎麼查」。監控看狀態，日誌查發生過什麼，管理工具幫你自動化維護。

1. `___`：看指標、收日誌、設警報，例如 CPU 太高就通知你。
2. `___`：記錄誰在 AWS 帳戶裡做了什麼 API 操作。
3. `___`：發現 CloudTrail 裡異常的 API 活動，例如突然大量刪除資源。
4. `___`：記錄 AWS 資源設定如何變更，並檢查是否符合規範。
5. `___`：根據 AWS 最佳實務給你成本、安全、效能等建議。
6. `___`：透過問卷檢查你的架構是否符合 AWS 最佳實務。
7. `___`：集中管理 EC2 或本地伺服器，例如派送命令、修補、盤點。
8. `___`：不用開 SSH 連接埠，也能透過瀏覽器安全連進 EC2。
9. `___`：查看 AWS 各服務在全球的公開服務狀態。
10. `___`：查看你的帳戶中哪些資源受到 AWS 事件影響。
11. `___`：追蹤微服務或無伺服器應用的請求流程，找出哪裡慢或出錯。
12. `___`：用 JSON 或 YAML 描述 AWS 架構，讓 AWS 自動幫你建立資源。
13. `___`：用 Python、JavaScript 等程式語言寫雲端架構，最後產生 CloudFormation。
14. `___`：AWS 官方常見問題和解答的知識庫。

<details>
<summary>答案</summary>

1. Amazon CloudWatch（雲端監控服務）
2. AWS CloudTrail（API 操作稽核日誌）
3. AWS CloudTrail Insights（CloudTrail 異常活動偵測）
4. AWS Config（資源設定合規管理）
5. AWS Trusted Advisor（可信任顧問）
6. AWS Well-Architected Tool（架構完善評估工具）
7. AWS Systems Manager（SSM，系統管理服務）
8. AWS Systems Manager Session Manager（工作階段管理員）
9. AWS Health Dashboard – Service Health（服務健康狀態儀表板）
10. AWS Health Dashboard – Your Account Health（帳戶健康狀態儀表板）
11. AWS X-Ray（分散式追蹤服務）
12. AWS CloudFormation（基礎設施即程式碼服務）
13. AWS Cloud Development Kit（AWS CDK，雲端開發套件）
14. AWS Knowledge Center（AWS 知識中心）

</details>

---

## 12. 開發者工具

這一章主要是給開發流程用的：放程式碼、建置、測試、部署、用命令管理 AWS。

1. `___`：AWS 的私有 Git 程式碼倉庫服務。
2. `___`：自動編譯程式碼、跑測試、產生建置結果。
3. `___`：把程式自動部署到 EC2 或本地伺服器。
4. `___`：把原始碼、建置、測試、部署串成一條自動化發布流程。
5. `___`：整合開發、建置、部署和專案管理的 AWS 開發服務。
6. `___`：存放軟體套件的服務，可搭配 npm、Maven、Gradle。
7. `___`：用機器學習幫你做程式碼審查、找問題、給建議。
8. `___`：讓程式用特定語言呼叫 AWS 服務的工具包。
9. `___`：用命令列操作 AWS 的工具。
10. `___`：用瀏覽器圖形介面操作 AWS 的地方。
11. `___`：提供真實手機和瀏覽器環境，幫你測試 App 或網站。
12. `___`：故意注入故障，測試系統遇到問題時是否撐得住。

<details>
<summary>答案</summary>

1. AWS CodeCommit（Git 程式碼倉庫服務）
2. AWS CodeBuild（程式碼自動建置服務）
3. AWS CodeDeploy（程式碼自動部署服務）
4. AWS CodePipeline（CI/CD 發布流水線）
5. AWS CodeStar（整合開發服務）
6. AWS CodeArtifact（套件管理服務）
7. Amazon CodeGuru（AI 程式碼審查工具）
8. AWS Software Development Kit（SDK，軟體開發套件）
9. AWS CLI（Command Line Interface，命令列介面）
10. AWS Management Console（管理主控台）
11. AWS Device Farm（裝置測試農場）
12. AWS Fault Injection Simulator（AWS FIS，故障注入模擬器）

</details>

---

## 13. 分析與 AI/ML 服務

這一章分兩塊：分析服務用來處理和查資料，AI/ML 服務用來做預測、辨識、語音、翻譯等智慧功能。

1. `___`：即時收集和處理大量串流資料，例如即時點擊紀錄。
2. `___`：在 AWS 上跑 Hadoop、Spark 這類大數據叢集。
3. `___`：直接用 SQL 查 S3 裡的資料，不用先架資料庫。
4. `___`：做商業智慧報表和互動式儀表板。
5. `___`：整理資料用的 ETL 服務，負責擷取、轉換、載入資料。
6. `___`：從建立、訓練到部署機器學習模型的一站式平台。
7. `___`：做時間序列預測，例如預測銷售量或網站流量。
8. `___`：分析圖片或影片，例如辨識人臉、物體、文字。
9. `___`：把語音轉成文字。
10. `___`：把文字轉成自然語音。
11. `___`：把文字翻譯成其他語言。
12. `___`：理解文字內容，例如情緒分析、關鍵字、實體辨識。
13. `___`：建立聊天機器人或語音對話介面。
14. `___`：企業搜尋服務，可以從文件中找答案。
15. `___`：根據使用者行為做個人化推薦，例如商品或影片推薦。
16. `___`：把媒體檔轉成不同格式，方便不同裝置播放。

<details>
<summary>答案</summary>

1. Amazon Kinesis Data Streams（即時資料串流）
2. Amazon EMR（Elastic MapReduce，彈性 MapReduce 大數據叢集）
3. Amazon Athena（互動式 SQL 查詢）
4. Amazon QuickSight（商業智慧視覺化）
5. AWS Glue（ETL 資料整合服務）
6. Amazon SageMaker（機器學習一站式平台）
7. Amazon Forecast（時間序列預測）
8. Amazon Rekognition（圖像與影片辨識）
9. Amazon Transcribe（語音轉文字）
10. Amazon Polly（文字轉語音）
11. Amazon Translate（語言翻譯）
12. Amazon Comprehend（自然語言理解）
13. Amazon Lex（對話式 AI）
14. Amazon Kendra（企業智慧搜尋）
15. Amazon Personalize（個人化推薦）
16. Amazon Elastic Transcoder（媒體檔案轉碼）

</details>

---

## 14. 應用程式整合

這一章是在學「不同系統之間怎麼溝通」。常見觀念是佇列、通知、事件和工作流程。

1. `___`：訊息排隊服務，讓系統 A 可以先把工作放進佇列，系統 B 之後再慢慢處理。
2. `___`：發布通知給很多訂閱者，例如 Email、SQS、Lambda。
3. `___`：相容 ActiveMQ 和 RabbitMQ 的受管訊息代理服務。
4. `___`：事件匯流排，可以依照事件或排程觸發後續動作。
5. `___`：把多個 Lambda 或 AWS 服務串成流程圖式的工作流程。
6. `___`：把桌面應用程式串流到使用者瀏覽器中執行。
7. `___`：讓大量 IoT 裝置安全連到 AWS。

<details>
<summary>答案</summary>

1. Amazon SQS（Simple Queue Service，簡單佇列服務）
2. Amazon SNS（Simple Notification Service，簡單通知服務）
3. Amazon MQ（受管訊息代理）
4. Amazon EventBridge（事件匯流排）
5. AWS Step Functions（工作流程協調服務）
6. Amazon AppStream 2.0（桌面應用程式串流）
7. AWS IoT Core（IoT 裝置連線服務）

</details>

---

## 15. 架構與治理框架

這一章比較像管理和最佳實務。不是單一技術，而是 AWS 建議你怎麼設計、遷移、管理多帳戶和控管成本。

1. `___`：AWS 的架構最佳實務框架，用六大支柱檢查系統設計。
2. `___`：重點是自動化、可回復的小變更、用程式碼管理營運。
3. `___`：重點是權限、加密、偵測、保護資料和系統。
4. `___`：重點是系統壞掉時仍能恢復，常鼓勵水平擴展和容錯設計。
5. `___`：重點是選對資源類型和大小，不要效能不足也不要過度浪費。
6. `___`：重點是用正確定價模式、刪除閒置資源、降低不必要成本。
7. `___`：協助公司規劃如何採用雲端的框架，包含業務、人員、治理、平台、安全、營運。
8. `___`：CAF 裡和業務目標、商業價值最相關的觀點。
9. `___`：CAF 裡負責雲端平台、架構、工具和技術基礎的觀點。
10. `___`：CAF 裡負責日常運維、監控、容量和服務管理的觀點。
11. `___`：雲端遷移常見六種做法，例如搬過去、稍微改、重寫、淘汰。
12. `___`：幾乎不改系統，直接搬到 AWS，也常叫 Lift and Shift。
13. `___`：稍微調整平台，例如把自管資料庫換成 RDS。
14. `___`：幫你快速建立多帳戶 AWS 環境，並套用基本治理護欄。
15. `___`：集中管理多個 AWS 帳戶、帳單和組織政策。
16. `___`：在 Organizations 裡限制帳戶最大權限的政策。
17. `___`：說明 AWS 負責雲端本身安全，客戶負責雲端中的安全。
18. `___`：AWS 官方提供架構範例和解決方案設計參考的地方。
19. `___`：由 AWS 合作夥伴提供的自動化部署參考方案。
20. `___`：AWS 的軟體商店，可以買 SaaS、AMI、第三方工具。
21. `___`：公司可以建立核准過的 IT 服務清單，讓使用者照規範部署。
22. `___`：貼在 AWS 資源上的鍵值，方便分類、搜尋、計費。
23. `___`：AWS 官方專業服務團隊，協助客戶做遷移和雲端落地。
24. `___`：AWS 合作夥伴網路，包含諮詢與技術合作夥伴。

<details>
<summary>答案</summary>

1. AWS Well-Architected Framework（AWS 架構完善框架）
2. Operational Excellence Pillar（卓越營運支柱）
3. Security Pillar（安全性支柱）
4. Reliability Pillar（可靠性支柱）
5. Performance Efficiency Pillar（效能效率支柱）
6. Cost Optimization Pillar（成本優化支柱）
7. AWS Cloud Adoption Framework（AWS CAF，雲端採用框架）
8. Business Perspective（業務觀點）
9. Platform Perspective（平台觀點）
10. Operations Perspective（營運觀點）
11. AWS Migration Strategies（遷移策略 6R）
12. Rehost（重新託管／Lift and Shift）
13. Replatform（重新平台化）
14. AWS Control Tower（多帳戶環境自動建置）
15. AWS Organizations（多帳戶組織管理）
16. Service Control Policies（SCP，服務控制政策）
17. AWS Shared Responsibility Model（共同責任模型）
18. AWS Architecture Center（架構中心）
19. AWS Partner Solutions（前身 Quick Starts）
20. AWS Marketplace（AWS 軟體商店）
21. AWS Service Catalog（核准 IT 服務目錄）
22. Tags（標籤）
23. AWS Professional Services（AWS 專業服務）
24. AWS Partner Network（APN，AWS 合作夥伴網路）

</details>

---

## 16. 基礎設施概念

這一章是在學 AWS 全球基礎設施。先記住：Region 最大，裡面有多個 AZ；Edge Location 則靠近使用者，用來加速內容。

1. `___`：AWS 的地理區域，例如東京、新加坡、維吉尼亞。
2. `___`：同一個區域裡彼此分離的資料中心群，用來做高可用。
3. `___`：CloudFront 用來快取內容的全球節點，通常比 Region 更靠近使用者。
4. `___`：雲端虛擬桌面服務，讓使用者遠端使用桌面環境。
5. `___`：透過 SFTP、FTPS、FTP 把檔案傳到 S3 或 EFS。

<details>
<summary>答案</summary>

1. AWS Region（區域）
2. Availability Zone（AZ，可用區）
3. Edge Location（邊緣位置）
4. Amazon WorkSpaces（雲端虛擬桌面）
5. AWS Transfer Family（檔案傳輸服務，支援 SFTP/FTPS/FTP）

</details>

---

## 17. 災難復原

災難復原是在問「大故障發生時，系統多久能恢復、資料最多會少多少」。通常成本越高，恢復越快。

1. `___`：平常只備份資料，災難時再還原，最便宜但恢復最慢。
2. `___`：雲端只保留最小核心系統，災難時再快速補齊其他資源。
3. `___`：雲端平常就跑一套縮小版系統，災難時放大成正式規模。
4. `___`：多個站點同時完整運作，恢復最快但成本最高。

<details>
<summary>答案</summary>

1. Backup and Restore（備份與還原）
2. Pilot Light（導引燈）
3. Warm Standby（暖備）
4. Multi-Site Active/Active（多站點主動/主動）

</details>

---

## 18. AWS 支援計畫

支援方案可以先看成「你能多快、用什麼方式找 AWS 求助」。等級越高，支援越完整，也越貴。

1. `___`：免費支援，主要包含帳戶、帳單、基本健康狀態和少數 Trusted Advisor 檢查。
2. `___`：適合開發測試，有 Email 技術支援，但支援範圍較有限。
3. `___`：適合正式營運工作負載，有 24/7 技術支援和完整 Trusted Advisor 檢查。
4. `___`：介於 Business 和 Enterprise 之間，可取得一組 TAM 團隊支援。
5. `___`：最高等級支援，包含指定 TAM、Concierge、重大活動支援等。
6. `___`：企業支援中的技術顧問，協助你規劃和優化 AWS 使用方式。
7. `___`：企業支援中的帳務和帳戶協助服務。

<details>
<summary>答案</summary>

1. AWS Basic Support（基本支援）
2. AWS Developer Support（開發人員支援）
3. AWS Business Support（商業支援）
4. AWS Enterprise On-Ramp Support（企業入門支援）
5. AWS Enterprise Support（企業支援）
6. Technical Account Manager（TAM，技術客戶經理）
7. AWS Concierge（帳務與帳戶禮賓服務）

</details>

---

## 快速記憶小抄

- 想「租一台雲端電腦」：Amazon EC2
- 想「只跑程式碼，不管伺服器」：AWS Lambda
- 想「放檔案」：Amazon S3
- 想「接在 EC2 上的硬碟」：Amazon EBS
- 想「多人共用資料夾」：Amazon EFS
- 想「關聯式資料庫」：Amazon RDS / Amazon Aurora
- 想「NoSQL 快速資料庫」：Amazon DynamoDB
- 想「自己的雲端私人網路」：Amazon VPC
- 想「管理登入與權限」：AWS IAM
- 想「看監控和警報」：Amazon CloudWatch
- 想「查誰做了什麼操作」：AWS CloudTrail
- 想「估算費用」：AWS Pricing Calculator
- 想「看花費」：AWS Cost Explorer
- 想「設定預算」：AWS Budgets

---

*整理來源：`AWS填空練習.md`。本版本重點是給 AWS 初學者快速理解與考前複習使用。*
