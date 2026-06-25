# AWS 名詞生活化理解

整理來源：[AWS填空練習_白話文版.md](AWS填空練習_白話文版.md)。

這份筆記把 AWS 名詞先翻成生活場景來理解。先不用急著背英文，先記住「它像生活中的什麼東西」和「它在幫你解決什麼問題」。

---

## 1. 雲端運算模型

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| SaaS | 直接去餐廳吃飯 | 你只負責使用成品，伺服器、更新、維護都由服務商處理。 |
| PaaS | 租一個已配好廚具的廚房 | 平台已準備好，你主要負責放程式和管理自己的應用。 |
| IaaS | 租一間空廚房和水電瓦斯 | AWS 給你伺服器、硬碟、網路等基礎，你自己安裝和管理。 |
| Hybrid Cloud | 公司一半自己煮，一半叫外送 | 本地機房和 AWS 雲端一起使用。 |
| Public Cloud | 大家共用大型商場裡的服務 | 資源在 AWS 這種公有雲供應商裡，不在自己公司機房。 |
| Private Cloud | 公司自己的專用會所 | 雲端環境只給單一組織使用，控制權較高。 |

---

## 2. 雲端優勢與基本概念

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| Agility | 想買東西打開 App 馬上下單 | 需要資源時很快取得，不必等採購和架機器。 |
| Elasticity | 尖峰時加開收銀台，沒人時關掉 | 流量多自動加資源，流量少自動縮回。 |
| Scalability | 小店能擴成連鎖店 | 系統可以隨使用者變多而變大。 |
| Reliability | 車子不容易壞，壞了也能修回來 | 系統穩定，故障後能恢復。 |
| High Availability | 便利商店 24 小時營業 | 服務盡量不中斷，使用者一直能用。 |
| Economies of Scale | 大賣場大量進貨比較便宜 | AWS 規模大，所以單位成本可以壓低。 |
| Horizontal Scaling | 多開幾個櫃台 | 增加更多台機器一起分擔工作。 |
| Vertical Scaling | 把一個櫃台換成超強櫃台 | 升級單台機器，例如更多 CPU 或記憶體。 |
| Loose Coupling | 各部門用表單交接，不綁在一起 | 系統元件不要互相卡死，壞一個不容易拖垮全部。 |
| Infrastructure as Code | 用食譜自動做出同一道菜 | 用程式碼建立資源，避免每次靠人工點選。 |
| Total Cost of Ownership | 買車不只看車價，還要算油錢保養 | 算總成本時，也要算人力、機房、電力、維護等。 |

---

## 3. 定價與成本管理

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| Savings Plans | 辦健身房長約換折扣 | 承諾一定用量或花費，AWS 給折扣。 |
| Compute Savings Plans | 一張比較通用的運動場館會員卡 | 彈性高，可套用到 EC2、Fargate、Lambda 等運算服務。 |
| EC2 Instance Savings Plans | 指定某家分店的會員卡 | 折扣較好，但限制在特定 EC2 家族和區域。 |
| EC2 Reserved Instance | 預訂一年或三年的固定座位 | 承諾使用 EC2 換折扣，不會被 AWS 中斷。 |
| Convertible RI | 可換座位類型的長約票 | 保留期間可調整一些屬性，彈性較高。 |
| Standard RI | 折扣最大但不能隨便換的長約票 | 適合需求很固定的 EC2。 |
| EC2 Spot Instance | 撿餐廳快打烊的特價餐 | 很便宜，但 AWS 需要容量時可能收回。 |
| EC2 On-Demand Instance | 需要時才買單次票 | 用多少付多少，適合短期或需求不固定。 |
| EC2 Dedicated Host | 整棟房子只租給你 | 整台實體伺服器專用，常用於授權或合規需求。 |
| EC2 Dedicated Instance | 住在專用樓層，但不指定哪間房 | 跑在專用硬體上，但不指定固定主機。 |
| EC2 Instance Store | 飯店房間桌上的便條紙 | 速度快但暫時，EC2 結束後資料可能消失。 |
| AWS Cost Explorer | 家庭記帳圖表 | 用圖表看 AWS 花費並預測未來費用。 |
| AWS Budgets | 每月花費提醒 | 設預算，快超過時通知你。 |
| AWS Cost and Usage Report | 最詳細的消費明細發票 | 記錄最完整的成本和用量，常放到 S3。 |
| AWS Cost Allocation Tags | 幫每筆支出貼部門標籤 | 用標籤看哪個專案或部門花了多少錢。 |
| AWS Pricing Calculator | 買東西前先試算購物車 | 建資源前先估算費用。 |
| AWS Compute Optimizer | 幫你看衣服尺寸合不合 | 分析資源是否太大、太小或該換規格。 |
| Consolidated Billing | 全家帳單合併付款 | 多個 AWS 帳戶合併帳單，也可能共享折扣。 |
| AWS Credits | 抵用券 | 可折抵符合條件的 AWS 費用。 |

---

## 4. 運算服務

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| Amazon EC2 | 租一台雲端電腦 | 最基本的虛擬伺服器，你像管電腦一樣管理它。 |
| Amazon EC2 Image Builder | 自動做標準化電腦範本的工廠 | 幫你建立和更新 EC2 或容器映像檔。 |
| Amazon Machine Image | 裝好系統的電腦複製模板 | EC2 開機用的範本，包含作業系統和軟體。 |
| EC2 User Data | 新電腦第一次開機自動執行的待辦清單 | EC2 第一次啟動時跑的初始化腳本。 |
| EC2 Instance Metadata | 電腦自己的身分證 | EC2 自己的 IP、ID、所在位置等資訊。 |
| EC2 Instance Connect | 臨時安全開門鑰匙 | 不必長期管理 SSH 金鑰，也能連到 EC2。 |
| AWS Lambda | 叫外送員幫你跑一次任務 | 只放程式碼，有事件時 AWS 幫你執行，不用管伺服器。 |
| AWS Elastic Beanstalk | 交給店長幫你開店 | 你放程式，AWS 幫你處理部署、擴展、負載平衡。 |
| AWS Fargate | 只帶便當盒，不用管廚房 | 跑容器但不用管理底層 EC2。 |
| Amazon ECS | 貨櫃調度中心 | 管理和執行 Docker 容器。 |
| Amazon ECR | 貨櫃倉庫 | 存放 Docker 容器映像檔。 |
| Amazon Lightsail | 套餐式小主機 | 適合 WordPress、小網站、簡單資料庫。 |
| AWS Auto Scaling | 自動加減人手 | 依需求自動增加或減少資源。 |
| Auto Scaling Group | 排班表設定最少和最多員工 | 管一群 EC2，設定最少、最多、期望台數。 |
| Predictive Scaling | 依過去尖峰先排更多員工 | 根據歷史流量，提前擴充資源。 |
| AWS Batch | 大量文件集中處理中心 | 適合大量批次工作，例如處理很多檔案。 |
| AWS Elastic Load Balancing | 餐廳門口的帶位人員 | 把流量分給多台伺服器或目標。 |
| Application Load Balancer | 會看點餐內容的帶位人員 | 依 HTTP/HTTPS 內容分流，常用於網站和 API。 |
| Network Load Balancer | 只看車道和速度的交通指揮 | 依 TCP/UDP 連線分流，適合低延遲需求。 |
| AWS Global Accelerator | 全球快速通道入口 | 提供固定入口 IP，用 AWS 全球網路導到較快端點。 |

---

## 5. EC2 執行個體類型

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| Memory Optimized | 超大桌面的辦公桌 | 適合很吃記憶體的工作，例如大型資料庫或快取。 |
| Compute Optimized | 很會算數的計算機 | 適合大量 CPU 計算和批次處理。 |
| Storage Optimized | 超快倉庫輸送帶 | 適合大量磁碟讀寫，例如資料倉儲。 |
| Accelerated Computing | 裝渦輪的工作站 | 有 GPU 或 FPGA，適合機器學習、影像處理、3D 渲染。 |

---

## 6. 儲存服務

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| Amazon S3 | 超大型雲端置物櫃 | 放圖片、影片、備份、日誌等物件檔案。 |
| Amazon S3 Standard | 最常用、隨手可拿的櫃位 | 適合常常讀取的資料。 |
| Amazon S3 Intelligent-Tiering | 會自動幫你換便宜櫃位的管理員 | AWS 依使用情況自動調整儲存層。 |
| Amazon S3 Standard-IA | 放不常拿但要拿時要快的櫃位 | 適合不常讀但需要快速取回的資料。 |
| Amazon S3 One Zone-IA | 只放在單一倉庫的便宜櫃位 | 較便宜，適合可重新產生的資料。 |
| Amazon S3 Glacier Flexible Retrieval | 冷凍倉庫 | 封存資料，取回可能要幾分鐘到幾小時。 |
| Amazon S3 Glacier Deep Archive | 地下深層保險庫 | 超長期保存，很少取回，成本更低。 |
| Amazon S3 Block Public Access | 置物櫃的公開鎖 | 防止 S3 檔案不小心公開給所有人。 |
| Amazon S3 Versioning | 文件歷史版本 | 保留物件不同版本，避免誤刪或覆蓋救不回來。 |
| Amazon S3 Lifecycle Configuration | 自動整理櫃子的規則 | 到時間自動轉便宜儲存層或刪除。 |
| Amazon S3 Replication | 自動影印一份放別處 | 把 S3 物件複製到同區域或不同區域。 |
| Amazon S3 Transfer Acceleration | 加速快遞通道 | 透過邊緣節點加快遠端上傳到 S3。 |
| Amazon S3 Access Logs | 置物櫃出入紀錄 | 記錄誰對 S3 bucket 做了哪些請求。 |
| Amazon EBS | 接在雲端電腦上的硬碟 | 給 EC2 使用的雲端硬碟，資料可持久保存。 |
| Amazon EFS | 大家共用的網路資料夾 | 多台 EC2 可一起掛載的 Linux 共享檔案系統。 |
| Amazon FSx for Windows File Server | 公司 Windows 共用資料夾 | 適合 Windows 應用和 SMB 檔案共享。 |
| Amazon FSx for Lustre | 高速專業檔案跑道 | 適合機器學習、高效能運算、大量檔案處理。 |
| AWS Storage Gateway | 本地倉庫和雲端倉庫的中轉門 | 把公司機房儲存和 AWS 儲存接起來。 |
| Amazon EBS Snapshots | 硬碟拍照備份 | EBS 的備份，可還原或搬到其他可用區。 |
| AWS DataSync | 搬家公司的同步搬運服務 | 快速同步或搬遷本地資料到 AWS 儲存服務。 |

---

## 7. 資料庫服務

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| Amazon RDS | 請專人管理 Excel 資料庫系統 | AWS 代管 MySQL、PostgreSQL、SQL Server 等關聯式資料庫。 |
| Amazon RDS Multi-AZ | 重要店面有備援分店 | 主資料庫壞掉時，可自動切到另一個可用區。 |
| Amazon RDS Read Replica | 多開查詢櫃台 | 用唯讀副本分擔查詢壓力。 |
| Amazon Aurora | AWS 自家升級版關聯式資料庫 | 相容 MySQL 和 PostgreSQL，效能和雲端整合較強。 |
| Amazon DynamoDB | 超快的號碼牌查資料櫃 | NoSQL 資料庫，適合大量快速讀寫鍵值或文件資料。 |
| Amazon DynamoDB Global Tables | 多國分店都能同步改資料 | 跨區域資料表，讓多個區域都能讀寫。 |
| Amazon DynamoDB Accelerator | 熱門資料的快速取餐台 | DynamoDB 快取，讓常讀資料更快。 |
| Amazon ElastiCache | 把常用資料放在桌上 | 記憶體快取，減少資料庫壓力。 |
| Amazon Neptune | 人際關係圖譜 | 圖形資料庫，適合處理人和物件之間的關係。 |
| Amazon DocumentDB | 文件型資料櫃 | 相容 MongoDB 的文件資料庫。 |
| Amazon Redshift | 大型商業報表分析中心 | 資料倉儲，適合大量資料分析和 BI 報表。 |
| AWS Database Migration Service | 資料庫搬家公司 | 把資料庫從本地或其他地方搬到 AWS。 |

---

## 8. 網路服務

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| Amazon VPC | 自己在雲端蓋的一個園區 | AWS 裡自己的私人網路空間。 |
| Subnet | 園區裡分區的街區 | VPC 裡更小的網路區塊。 |
| Internet Gateway | 園區的大門通向外面馬路 | 讓 VPC 公開資源能連到網際網路。 |
| NAT Gateway | 只准員工出門，不准外人進門的出口 | 私有子網路可連出去上網，外部不能主動連進來。 |
| Security Group | 房間門口的警衛 | 綁在 EC2 等資源上，控制誰能進出。 |
| Network ACL | 社區大門警衛 | 套在子網路層級，進站出站都要分別管。 |
| VPC Peering Connection | 兩個園區之間的私有小路 | 把兩個 VPC 私下接起來。 |
| AWS Transit Gateway | 大型交通轉運站 | 多個 VPC 和本地網路集中連接。 |
| VPC Endpoint | 園區內直達 AWS 服務的內部通道 | 私下連到 AWS 服務，不必走公開網際網路。 |
| AWS PrivateLink | 私人包廂通道 | 透過私有連線使用 AWS 或第三方服務。 |
| AWS Direct Connect | 公司到 AWS 的專用高速公路 | 專線連接，比一般 VPN 更穩定。 |
| AWS Site-to-Site VPN | 在公路上加密的專用車道 | 透過網際網路建立加密通道連到 AWS。 |
| Virtual Private Gateway | AWS 這邊的 VPN 閘道 | Site-to-Site VPN 在 AWS 端的入口。 |
| Customer Gateway | 公司這邊的 VPN 閘道 | Site-to-Site VPN 在客戶機房端的設備或設定。 |
| Amazon Route 53 | 網路世界的導航和電話簿 | DNS 服務，負責網域解析、健康檢查和路由。 |
| Route 53 Simple Routing | 固定導航到同一個地址 | 最單純的 DNS 路由。 |
| Route 53 Weighted Routing | 80% 客人去 A 店、20% 去 B 店 | 按比例分配流量。 |
| Route 53 Latency-based Routing | 導航到最快到達的分店 | 把使用者導向延遲最低的端點。 |
| Route 53 Failover Routing | 主店關門就導到備援店 | 主站壞掉時切到備援站。 |
| Amazon CloudFront | 全球快取便利店 | CDN，把內容快取到靠近使用者的邊緣節點。 |
| Amazon API Gateway | 餐廳櫃台接單再轉給廚房 | 建立和管理 API，讓前端和後端溝通。 |

---

## 9. 邊緣與混合雲服務

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| AWS Outposts | AWS 把一小套設備搬進你公司 | 在客戶機房裡跑 AWS 硬體和服務。 |
| AWS Wavelength | 把小廚房放到 5G 基地台旁 | 讓 5G 低延遲應用更快。 |
| AWS Local Zones | 在大城市旁開小型分店 | 靠近使用者，降低延遲。 |
| AWS Snow Family | 一系列實體搬運箱 | 用來離線搬大量資料或在邊緣運算。 |
| AWS Snowball | 裝滿資料寄到 AWS 的硬箱子 | 用實體設備搬大量資料。 |
| AWS Snowball Edge | 有小型電腦功能的搬運箱 | 除了搬資料，也能在本地做運算。 |
| AWS OpsHub | Snow 裝置的遙控面板 | 用圖形介面管理 Snow 裝置。 |

---

## 10. 安全與身份服務

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| AWS IAM | 公司門禁和權限系統 | 管誰能登入 AWS、能做哪些事。 |
| IAM User | 一張員工識別證 | 代表一個人或程式的 AWS 身分。 |
| IAM Role | 臨時工作證 | 可被暫時使用的身分，常給 EC2 或跨帳戶使用。 |
| IAM Policy | 門禁規則表 | 用 JSON 定義允許或拒絕哪些動作。 |
| IAM Credentials Report | 員工門禁健康檢查表 | 列出 IAM 使用者密碼、金鑰、MFA 等狀態。 |
| IAM Access Advisor | 看員工最近進過哪些房間 | 查看某身分最近用過哪些服務，方便移除多餘權限。 |
| MFA | 除了鑰匙還要驗指紋 | 多重要素驗證，多一層保護。 |
| Virtual MFA Device | 手機驗證器 App | 用手機產生 MFA 驗證碼。 |
| U2F Security Key | 實體安全鑰匙 | 插 USB 或裝置上的硬體安全金鑰。 |
| Hardware MFA Device | 會跳驗證碼的小令牌 | 實體 MFA 裝置，產生一次性驗證碼。 |
| Access Key ID & Secret Access Key | 程式用的帳號密碼 | CLI 或 SDK 呼叫 AWS API 的金鑰。 |
| AWS IAM Identity Center | 公司單一登入櫃台 | 集中管理多個 AWS 帳戶的登入。 |
| Amazon Cognito | App 會員登入系統 | 幫網站或 App 處理使用者註冊和登入。 |
| AWS Security Token Service | 臨時通行證發放處 | 提供短時間有效的臨時安全憑證。 |
| AWS KMS | 鑰匙管理室 | 管理加密金鑰，用來加密資料。 |
| Customer Managed Key | 你自己管的保險箱鑰匙 | 由客戶建立和管理的 KMS 金鑰。 |
| AWS Managed Key | AWS 幫你管的保險箱鑰匙 | AWS 建立和管理，操作較省事。 |
| AWS CloudHSM | 專用硬體保險箱 | 雲端硬體安全模組，適合法規要求高的加密需求。 |
| AWS Secrets Manager | 密碼保險箱 | 安全保存密碼、API Key，並可自動輪換。 |
| Amazon GuardDuty | 保全巡邏系統 | 偵測帳戶和網路中的可疑活動。 |
| Amazon Inspector | 安全檢查員 | 檢查 EC2、容器等是否有漏洞。 |
| Amazon Macie | 個資掃描員 | 找出 S3 裡的敏感資料。 |
| Amazon Detective | 偵探 | 協助調查安全事件的來龍去脈。 |
| AWS Security Hub | 保全監控總控室 | 集中整理多個安全服務的警報和狀態。 |
| AWS Shield Standard | 基本防撞護盾 | 免費基本 DDoS 防護。 |
| AWS Shield Advanced | 進階防撞護盾加專家 | 付費 DDoS 防護，含專家支援與成本保護。 |
| AWS WAF | 網站門口的檢查站 | 防 SQL Injection、XSS 等 Web 攻擊。 |
| AWS Artifact | 合規文件櫃 | 下載 AWS 合規報告和安全文件。 |
| VPC Flow Logs | 道路監視器紀錄 | 記錄 VPC 網路流量，用於安全分析和除錯。 |
| AWS Abuse Team | 處理濫用通報的客服團隊 | 處理 AWS 資源被用來攻擊、掃描或濫用的通報。 |

---

## 11. 監控與管理服務

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| Amazon CloudWatch | 儀表板和警報器 | 看指標、收日誌、設警報。 |
| AWS CloudTrail | 操作錄影紀錄 | 記錄誰在 AWS 帳戶裡做了什麼 API 操作。 |
| AWS CloudTrail Insights | 異常行為警報 | 發現 CloudTrail 裡不尋常的 API 活動。 |
| AWS Config | 資源設定變更簿 | 記錄 AWS 資源設定如何變更，並檢查合規。 |
| AWS Trusted Advisor | 雲端健檢顧問 | 根據最佳實務給成本、安全、效能等建議。 |
| AWS Well-Architected Tool | 架構健康問卷 | 用問卷檢查架構是否符合 AWS 最佳實務。 |
| AWS Systems Manager | IT 管理工具箱 | 集中管理 EC2 或本地伺服器，做修補、盤點、命令派送。 |
| AWS Systems Manager Session Manager | 不開門也能進房間的安全通道 | 不用開 SSH 連接埠，也能安全連進 EC2。 |
| AWS Health Dashboard - Service Health | AWS 全世界服務公告板 | 查看 AWS 各服務的公開健康狀態。 |
| AWS Health Dashboard - Your Account Health | 你帳戶專屬事件通知 | 看你的帳戶中哪些資源受到 AWS 事件影響。 |
| AWS X-Ray | 包裹追蹤號碼 | 追蹤請求在微服務間怎麼走，找出哪裡慢或錯。 |
| AWS CloudFormation | 用藍圖蓋房子 | 用 JSON 或 YAML 描述架構，AWS 自動建立資源。 |
| AWS Cloud Development Kit | 用程式語言畫建築藍圖 | 用 Python、JavaScript 等寫雲端架構，最後產生 CloudFormation。 |
| AWS Knowledge Center | AWS 問答知識庫 | 官方常見問題和解答入口。 |

---

## 12. 開發者工具

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| AWS CodeCommit | 程式碼倉庫 | AWS 的私有 Git 程式碼倉庫。 |
| AWS CodeBuild | 自動組裝工廠 | 自動編譯、測試、產生建置結果。 |
| AWS CodeDeploy | 自動送貨上架 | 把程式自動部署到 EC2 或本地伺服器。 |
| AWS CodePipeline | 生產線輸送帶 | 把原始碼、建置、測試、部署串成流程。 |
| AWS CodeStar | 專案開發總管 | 整合開發、建置、部署和專案管理。 |
| AWS CodeArtifact | 套件倉庫 | 存放 npm、Maven、Gradle 等軟體套件。 |
| Amazon CodeGuru | AI 程式碼教練 | 用機器學習做程式碼審查和效能建議。 |
| AWS Software Development Kit | 各語言版 AWS 遙控器 | 讓程式用特定語言呼叫 AWS 服務。 |
| AWS CLI | 命令列遙控器 | 用文字命令操作 AWS。 |
| AWS Management Console | AWS 的網頁控制台 | 用瀏覽器圖形介面操作 AWS。 |
| AWS Device Farm | 真機測試實驗室 | 用真實手機和瀏覽器測試 App 或網站。 |
| AWS Fault Injection Simulator | 故障演練教官 | 故意製造故障，測試系統是否撐得住。 |

---

## 13. 分析與 AI/ML 服務

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| Amazon Kinesis Data Streams | 即時水流資料管 | 即時收集和處理大量串流資料。 |
| Amazon EMR | 大型資料處理工廠 | 在 AWS 跑 Hadoop、Spark 等大數據叢集。 |
| Amazon Athena | 對 S3 檔案直接問 SQL 問題 | 不用架資料庫，也能用 SQL 查 S3 資料。 |
| Amazon QuickSight | 商業報表看板 | 做 BI 視覺化報表和互動式儀表板。 |
| AWS Glue | 資料清洗和搬運工 | ETL 服務，擷取、轉換、載入資料。 |
| Amazon SageMaker | 機器學習工作室 | 建立、訓練、部署機器學習模型的一站式平台。 |
| Amazon Forecast | 銷售預測師 | 做時間序列預測，例如銷售量或流量。 |
| Amazon Rekognition | 會看圖的眼睛 | 分析圖片或影片，辨識人臉、物體、文字。 |
| Amazon Transcribe | 聽寫員 | 把語音轉成文字。 |
| Amazon Polly | 朗讀員 | 把文字轉成自然語音。 |
| Amazon Translate | 翻譯員 | 把文字翻譯成其他語言。 |
| Amazon Comprehend | 文字理解助手 | 分析情緒、關鍵字、實體等文字內容。 |
| Amazon Lex | 聊天機器人櫃台 | 建立文字或語音對話介面。 |
| Amazon Kendra | 企業內部搜尋員 | 從文件中找答案。 |
| Amazon Personalize | 推薦系統店員 | 根據使用者行為做個人化推薦。 |
| Amazon Elastic Transcoder | 影片格式轉換器 | 把媒體檔轉成不同格式。 |

---

## 14. 應用程式整合

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| Amazon SQS | 排隊號碼牌 | 系統 A 把工作放進佇列，系統 B 之後慢慢處理。 |
| Amazon SNS | 廣播通知喇叭 | 發布通知給 Email、SQS、Lambda 等多個訂閱者。 |
| Amazon MQ | 專業郵局系統 | 受管訊息代理，相容 ActiveMQ 和 RabbitMQ。 |
| Amazon EventBridge | 事件轉運中心 | 依事件或排程觸發後續動作。 |
| AWS Step Functions | 流程圖指揮官 | 把多個 Lambda 或 AWS 服務串成工作流程。 |
| Amazon AppStream 2.0 | 遠端使用桌面軟體 | 把桌面應用串流到使用者瀏覽器。 |
| AWS IoT Core | IoT 裝置總機 | 讓大量 IoT 裝置安全連到 AWS。 |

---

## 15. 架構與治理框架

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| AWS Well-Architected Framework | 建築安全檢查表 | 用六大支柱檢查系統架構是否健康。 |
| Operational Excellence Pillar | 店面營運 SOP | 重點是自動化、可回復的小變更、營運流程。 |
| Security Pillar | 門禁和保全規劃 | 重點是權限、加密、偵測、資料保護。 |
| Reliability Pillar | 備援和故障恢復設計 | 重點是壞了能恢復、服務不中斷。 |
| Performance Efficiency Pillar | 選對工具和尺寸 | 重點是資源類型和大小合適，不過度浪費。 |
| Cost Optimization Pillar | 省錢採購策略 | 重點是正確定價、刪除閒置資源、降低成本。 |
| AWS Cloud Adoption Framework | 公司搬上雲端的總計畫 | 從業務、人員、治理、平台、安全、營運規劃雲端採用。 |
| Business Perspective | 老闆和業務的角度 | 關心商業價值、目標和成果。 |
| Platform Perspective | 工程平台的角度 | 關心雲端平台、架構、工具和技術基礎。 |
| Operations Perspective | 日常維運的角度 | 關心監控、容量、服務管理和日常運作。 |
| AWS Migration Strategies | 搬家方式選單 | 雲端遷移常見做法，例如直接搬、稍微改、重寫。 |
| Rehost | 原封不動搬家 | 幾乎不改系統，直接搬到 AWS，也叫 Lift and Shift。 |
| Replatform | 搬家時順手換家具 | 稍微調整平台，例如自管資料庫改成 RDS。 |
| AWS Control Tower | 多帳戶社區建案樣板 | 快速建立多帳戶 AWS 環境並套用治理護欄。 |
| AWS Organizations | 集團公司總管理處 | 集中管理多個 AWS 帳戶、帳單和組織政策。 |
| Service Control Policies | 集團最高禁令 | 在 Organizations 裡限制帳戶最大權限。 |
| AWS Shared Responsibility Model | 房東和房客責任分工 | AWS 管雲端本身，你管雲端中的資料和設定。 |
| AWS Architecture Center | 建築設計參考資料庫 | AWS 官方架構範例和解決方案參考。 |
| AWS Partner Solutions | 合作夥伴提供的裝修包 | 由 AWS 夥伴提供的自動化部署參考方案。 |
| AWS Marketplace | 雲端軟體商店 | 可以買 SaaS、AMI、第三方工具。 |
| AWS Service Catalog | 公司核准採購清單 | 建立核准的 IT 服務清單，讓使用者照規範部署。 |
| Tags | 資源貼紙 | 幫 AWS 資源分類、搜尋、計費。 |
| AWS Professional Services | AWS 官方顧問團 | 協助客戶做遷移和雲端落地。 |
| AWS Partner Network | AWS 合作夥伴網路 | 包含諮詢與技術合作夥伴。 |

---

## 16. 基礎設施概念

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| AWS Region | 一個國家或大城市據點 | AWS 的地理區域，例如東京、新加坡。 |
| Availability Zone | 同一城市裡分開的資料中心群 | Region 裡彼此分離的資料中心，用來做高可用。 |
| Edge Location | 離使用者最近的小取貨點 | CloudFront 快取內容的全球節點。 |
| Amazon WorkSpaces | 雲端辦公桌 | 雲端虛擬桌面，讓使用者遠端使用桌面環境。 |
| AWS Transfer Family | 專門收發檔案的櫃台 | 透過 SFTP、FTPS、FTP 把檔案傳到 S3 或 EFS。 |

---

## 17. 災難復原

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| Backup and Restore | 東西先拍照備份，壞了再重買重裝 | 最便宜，但恢復最慢。 |
| Pilot Light | 只留一盞小燈和基本設備 | 雲端只保留最小核心系統，災難時再補齊。 |
| Warm Standby | 備用店面平常半開 | 平常跑縮小版系統，災難時放大成正式規模。 |
| Multi-Site Active/Active | 多家完整分店同時營業 | 恢復最快但成本最高。 |

---

## 18. AWS 支援計畫

| 名詞 | 生活化比喻 | 白話理解 |
|---|---|---|
| AWS Basic Support | 免費客服櫃台 | 免費支援，主要處理帳戶、帳單、基本健康狀態。 |
| AWS Developer Support | 開發者 Email 客服 | 適合開發測試，有 Email 技術支援。 |
| AWS Business Support | 正式營業用 24 小時客服 | 適合正式營運工作負載，有 24/7 技術支援。 |
| AWS Enterprise On-Ramp Support | 企業支援入門套餐 | 介於 Business 和 Enterprise，可取得 TAM 團隊支援。 |
| AWS Enterprise Support | 最高級企業管家服務 | 指定 TAM、Concierge、重大活動支援等。 |
| Technical Account Manager | 技術客戶經理 | 企業支援中的技術顧問，協助規劃和優化 AWS。 |
| AWS Concierge | 帳務禮賓管家 | 協助企業支援中的帳務和帳戶問題。 |

---

## 一句話快速抓感覺

| 想做的事 | 先想到 |
|---|---|
| 租一台雲端電腦 | Amazon EC2 |
| 只跑程式碼，不管伺服器 | AWS Lambda |
| 放檔案、圖片、備份 | Amazon S3 |
| 接在 EC2 上的硬碟 | Amazon EBS |
| 多台 Linux 主機共用資料夾 | Amazon EFS |
| 關聯式資料庫 | Amazon RDS 或 Amazon Aurora |
| NoSQL 快速資料庫 | Amazon DynamoDB |
| 自己的雲端私人網路 | Amazon VPC |
| 管登入和權限 | AWS IAM |
| 看監控和警報 | Amazon CloudWatch |
| 查誰做了什麼操作 | AWS CloudTrail |
| 估算費用 | AWS Pricing Calculator |
| 看花費趨勢 | AWS Cost Explorer |
| 設定預算警示 | AWS Budgets |


