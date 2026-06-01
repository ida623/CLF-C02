# AWS Cloud Practitioner【TEST02】

---

## Questions (1–5)

(1) move to a fully managed AWS database
Ans: Amazon Elastic Container Registry (Amazon ECR)

(2) assess its EC2 instances for vulnerabilities
Ans: Amazon Inspector

(3) protect its web application from SQL injection and cross-site scripting
Ans: AWS Web Application Firewall (AWS WAF)

(4) AWS Compute Optimizer delivers recommendations for
Ans: Amazon EC2 instances, Amazon EC2 Auto Scaling groups / Amazon EBS / AWS Lambda functions

(5) global in scope
Ans: Amazon CloudFront / AWS Identity and Access Management (AWS IAM)

---

(1)
中文題目：哪項 AWS 服務用於儲存與管理容器映像（Container Images）？
答案：Amazon Elastic Container Registry，ECR（彈性容器登錄服務）
解析：**Amazon ECR** 是 AWS 的全受管容器映像倉庫，功能類似 Docker Hub，提供：
- 安全儲存、版本管理與部署 Docker 容器映像
- 與 ECS、EKS、Lambda 原生整合
- 支援私有與公有映像倉庫
- 映像漏洞掃描功能
注意：本題原始題幹（move to a fully managed AWS database）與答案（ECR）不符，考試中此題實際考的是「容器映像倉庫」，ECR 負責儲存映像而非資料庫。作答時認準 ECR 對應容器映像管理即可。

(2)
中文題目：哪項 AWS 服務可評估 EC2 執行個體的安全漏洞？
答案：Amazon Inspector
解析：**Amazon Inspector** 是自動化安全評估服務，可針對：
- **EC2 執行個體**：掃描作業系統漏洞（CVE）與網路可達性問題
- **Lambda 函數**：掃描程式碼相依套件漏洞
- **ECR 容器映像**：在推送時自動掃描
Inspector 持續監控，發現漏洞後產生優先排序的安全發現（findings）報告，幫助快速修補。

(3)
中文題目：哪項 AWS 服務可保護 Web 應用程式免受 SQL 注入與跨站腳本（XSS）攻擊？
答案：AWS Web Application Firewall，WAF
解析：**AWS WAF** 運作於第 7 層（應用層），可設定規則過濾惡意 HTTP/HTTPS 請求，防禦：
- **SQL Injection**：惡意 SQL 語法注入資料庫查詢
- **Cross-Site Scripting（XSS）**：注入惡意腳本至網頁
- 惡意 Bot、IP 封鎖、速率限制
WAF 可部署於 CloudFront、ALB、API Gateway、AppSync 前端，是應用層安全的核心工具。

(4)
中文題目：AWS Compute Optimizer 可針對哪些服務提供最佳化建議？
答案：Amazon EC2 執行個體、EC2 Auto Scaling 群組 / Amazon EBS / AWS Lambda 函數
解析：**AWS Compute Optimizer** 利用機器學習分析 CloudWatch 歷史使用數據，針對以下資源提供右型化（right-sizing）建議：
- **EC2 執行個體**：建議更適合的執行個體類型與大小
- **EC2 Auto Scaling 群組**：優化群組配置
- **EBS Volume**：建議適合的 Volume 類型與大小
- **Lambda 函數**：建議最佳記憶體配置
目標是協助識別過度配置或配置不足的資源，達到降本效果。

(5)
中文題目：哪些 AWS 服務屬於全球範圍（global scope），而非區域性（regional）服務？
答案：Amazon CloudFront / AWS Identity and Access Management，IAM
解析：AWS 服務依範圍分類：
- **全球範圍（Global）**：IAM（使用者、角色、政策全球通用）、CloudFront（全球 CDN 邊緣節點）、Route 53、AWS Organizations
- **區域範圍（Regional）**：EC2、S3（雖可跨區域複製，但 bucket 本身屬於特定 Region）、RDS、VPC
- **可用區範圍（AZ-level）**：EBS Volume、子網路（Subnet）
考試常考：IAM 和 CloudFront 是最常考的 Global 服務。

---

## Questions (6–10)

(6) always free to use
Ans: AWS Identity and Access Management (AWS IAM) / AWS Auto Scaling

(7) process every Monday at 2 AM (runtime ~5 minutes)
Ans: AWS Lambda / Amazon EventBridge

(8) helps with global application availability and performance
Ans: AWS Global Accelerator

(9) AWS Shared Responsibility Model — responsibility of the customer
Ans: Managing patches of the guest OS on Amazon EC2

(10) designated Technical Account Manager (TAM)
Ans: AWS Enterprise Support

---

(6)
中文題目：哪些 AWS 服務永遠免費使用（always free）？
答案：AWS IAM / AWS Auto Scaling
解析：AWS 免費方案分為三類：永久免費（Always Free）、12 個月免費、試用免費。**永久免費**的服務包含：
- **AWS IAM**：建立使用者、群組、角色、政策，完全免費
- **AWS Auto Scaling**：Auto Scaling 服務本身免費，只需支付底層 EC2 等資源費用
- 其他永久免費服務：AWS CloudFormation（範本本身免費）、VPC（基本功能免費）、CloudWatch（基本監控免費）

(7)
中文題目：需要每週一凌晨 2 點執行一次、執行時間約 5 分鐘的排程任務，應使用哪些 AWS 服務？
答案：AWS Lambda / Amazon EventBridge
解析：這是典型的**排程任務（Scheduled Job）**架構：
- **Amazon EventBridge**：設定 Cron 排程規則（每週一 02:00），自動觸發目標服務
- **AWS Lambda**：執行實際業務邏輯，無伺服器、按需啟動，5 分鐘以內的任務完全適合（Lambda 最長 15 分鐘）
兩者搭配是 AWS 上實現排程任務的最佳實踐，無需維運任何伺服器。

(8)
中文題目：哪項 AWS 服務可提升全球應用程式的可用性與效能？
答案：AWS Global Accelerator
解析：**AWS Global Accelerator** 透過 AWS 全球骨幹網路路由流量，提供：
- 固定兩個靜態 Anycast IP 位址，無需更改 DNS
- 自動將流量路由至最近、最健康的 AWS 端點（跨 Region）
- 降低延遲、提升可用性（自動故障轉移）
與 CloudFront 差異：CloudFront 是 CDN，快取靜態內容；Global Accelerator 優化動態流量路由，不做內容快取。

(9)
中文題目：在 AWS 共同責任模型中，以下哪項是客戶的責任？
答案：管理 Amazon EC2 上 Guest OS 的修補（patching）
解析：EC2 是 IaaS 服務，責任劃分如下：
- **AWS 負責**：實體主機硬體、Hypervisor、底層基礎設施
- **客戶負責**：**Guest OS 的安裝、設定、修補與更新**、應用程式、資料、Security Group 規則
這與 RDS 等 Managed Service 不同——RDS 的 OS 修補由 AWS 自動處理，客戶無需介入。

(10)
中文題目：哪個 AWS Support 方案提供專屬技術客戶經理（TAM）？
答案：AWS Enterprise Support
解析：**AWS Enterprise Support** 是最高等級的支援方案，獨有功能包含：
- **Technical Account Manager（TAM）**：專屬技術顧問，主動協助架構審查、規劃、最佳化
- 15 分鐘回應時間（關鍵業務中斷）
- Infrastructure Event Management（基礎設施事件管理）
- Well-Architected Reviews
Business Support 雖提供 24/7 支援，但不包含專屬 TAM。

---

## Questions (11–15)

(11) per-second billing and access to the underlying OS
Ans: Amazon EC2

(12) gives a personalized view of AWS service health
Ans: AWS Health — Your Account Health Dashboard

(13) storage accessible across different AZs
Ans: Amazon Elastic File System (Amazon EFS)

(14) the Software as a Service (SaaS) model example
Ans: Amazon Rekognition

(15) AWS Shared Responsibility Model — responsibility of AWS
Ans: Edge Location Management（邊緣節點管理）

---

(11)
中文題目：哪項 AWS 服務支援按秒計費，且客戶可存取底層作業系統？
答案：Amazon EC2
解析：**Amazon EC2** 是 IaaS 服務，兩大特性：
- **按秒計費**：Linux 執行個體按秒計費（最低 60 秒），Windows 按小時計費
- **OS 存取**：客戶可完全控制 Guest OS（SSH/RDP 登入），安裝軟體、修改設定
這與 Lambda、Fargate 等無伺服器服務不同——無伺服器服務不提供 OS 存取，也不按秒計費（Lambda 按毫秒）。

(12)
中文題目：哪項 AWS 服務可提供針對你帳戶的個人化 AWS 服務健康狀態視圖？
答案：AWS Health — Your Account Health Dashboard（帳戶健康儀表板）
解析：AWS Health 分為兩種儀表板：
- **Service Health Dashboard**：顯示所有 AWS 服務在所有 Region 的通用狀態（公開）
- **Your Account Health Dashboard（帳戶健康儀表板）**：顯示**影響你帳戶**的特定事件、維護通知與建議行動（個人化）
題目關鍵字「personalized view（個人化視圖）」對應 Account Health Dashboard。

(13)
中文題目：哪項 AWS 儲存服務可跨不同可用區（AZ）存取？
答案：Amazon Elastic File System，EFS
解析：**Amazon EFS** 是跨 AZ 的共享檔案儲存，可同時被多個 AZ 的 EC2 執行個體掛載。比較：
- **EBS**：綁定單一 AZ，只能掛載同 AZ 的 EC2
- **EFS**：跨多個 AZ，自動多 AZ 冗餘儲存
- **S3**：物件儲存，Region 層級，無 AZ 限制，但非傳統檔案系統語義
需要跨 AZ 共享存取且使用標準檔案系統介面，選 EFS。

(14)
中文題目：哪項 AWS 服務是軟體即服務（SaaS）模型的範例？
答案：Amazon Rekognition
解析：雲端服務模型：
- **IaaS**：EC2（提供虛擬基礎設施）
- **PaaS**：Elastic Beanstalk（提供執行平台）
- **SaaS**：**Amazon Rekognition**（完整的影像與視訊分析服務，客戶只需呼叫 API，無需管理任何基礎設施或平台）
Rekognition 提供臉部辨識、物件偵測、文字辨識等功能，是典型的 SaaS——功能即服務，開箱即用。

(15)
中文題目：在 AWS 共同責任模型中，哪項屬於 AWS 的責任？
答案：Edge Location Management（邊緣節點管理）
解析：AWS 負責所有底層實體基礎設施的管理，包含：
- 全球資料中心、Region、AZ 的實體設施
- **Edge Location（邊緣節點）**：CloudFront、Route 53 等服務使用的全球邊緣節點，由 AWS 全權管理與維護
客戶只需設定要分發的內容與規則，邊緣節點的硬體、網路、維護皆由 AWS 負責。

---

## Questions (16–20)

(16) use a hardware device for data encryption
Ans: AWS CloudHSM

(17) connect your on-premises network with AWS Cloud
Ans: AWS Direct Connect / AWS Virtual Private Network (VPN)

(18) Access Key ID and Secret Access Key are associated with which IAM entity
Ans: IAM User

(19) Horizontal Scalability (Elasticity) examples
Ans: Elastic Load Balancing (ELB) / Read Replicas in Amazon RDS

(20) INCORRECT statement about AWS Auto Scaling
Ans: "You can automatically deploy AWS Shield when a DDoS attack is detected"

---

(16)
中文題目：哪項 AWS 服務使用硬體裝置進行資料加密？
答案：AWS CloudHSM（雲端硬體安全模組）
解析：**AWS CloudHSM** 提供 FIPS 140-2 Level 3 認證的**專用硬體安全模組（HSM）**，用於：
- 生成、儲存與管理加密金鑰
- 執行加密運算（對稱/非對稱加密）
- 滿足嚴格的合規要求（金融、醫療）
與 KMS 差異：**KMS** 是軟體管理的多租戶金鑰管理服務；**CloudHSM** 提供客戶專屬的實體硬體，金鑰完全由客戶掌控，AWS 無法存取。

(17)
中文題目：哪些 AWS 服務可將本地端（on-premises）網路連接至 AWS Cloud？
答案：AWS Direct Connect / AWS Virtual Private Network，VPN
解析：兩種混合雲連線方式比較：
- **AWS Direct Connect**：實體專線，穩定低延遲，不經過公共網路，適合大量資料傳輸，建置時間較長（數週）
- **AWS VPN（Site-to-Site VPN）**：透過公共網際網路建立加密通道（IPSec），部署快速（數分鐘），費用較低，但受網路品質影響
兩者可同時使用：Direct Connect 為主要連線，VPN 作為備援，實現高可用混合雲架構。

(18)
中文題目：Access Key ID 與 Secret Access Key 屬於哪種 IAM 實體？
答案：IAM User（IAM 使用者）
解析：**Access Key** 是 IAM 使用者的程式化存取憑證，用於 AWS CLI、SDK 或 API 呼叫：
- **Access Key ID**：公開識別碼（類似帳號）
- **Secret Access Key**：私密金鑰（類似密碼，僅建立時顯示一次）
IAM Role 不使用 Access Key，而是透過 STS 取得臨時安全憑證。最佳實踐：EC2 或 Lambda 上應使用 IAM Role，避免在程式碼或設定檔中硬寫 Access Key。

(19)
中文題目：哪些 AWS 服務展現了水平擴展（Horizontal Scalability / Elasticity）的特性？
答案：Elastic Load Balancing，ELB / Amazon RDS Read Replicas（讀取複本）
解析：
- **水平擴展（Scale Out）**：增加更多執行個體數量來分散負載，而非升級單一機器規格
- **ELB**：將流量分散到多個 EC2 執行個體，支援水平擴展架構
- **RDS Read Replicas**：新增多個唯讀複本分散讀取負載，是資料庫水平擴展的典型做法
垂直擴展（Scale Up）則是升級單一執行個體規格（如從 t3.medium 升至 t3.large）。

(20)
中文題目：關於 AWS Auto Scaling，哪個敘述是**錯誤的**？
答案：「偵測到 DDoS 攻擊時可自動部署 AWS Shield」——此為錯誤說法
解析：**AWS Auto Scaling** 的職責是根據負載自動調整運算資源數量（如 EC2 執行個體），與安全防護無關。AWS Shield 的部署方式：
- **Shield Standard**：自動為所有客戶啟用，無需任何操作
- **Shield Advanced**：需手動訂閱並設定保護的資源
兩者皆非由 Auto Scaling 觸發部署，Auto Scaling 無法偵測或回應 DDoS 事件。

---

## Questions (21–25)

(21) Multi-AZ deployment provides which benefit
Ans: High Availability（高可用性）

(22) NOT supported by Amazon Rekognition
Ans: Quickly resize photos to create thumbnails

(23) build solutions on AWS Cloud
Ans: AWS Service Catalog / AWS Partner Network (APN)

(24) statements are true about AWS Lambda
Ans: AWS Lambda lets you run code without provisioning or managing servers / You pay only for the compute time you consume

(25) provision resources to run big data workloads on Hadoop clusters
Ans: Amazon EMR

---

(21)
中文題目：RDS Multi-AZ 部署提供哪項主要優勢？
答案：High Availability（高可用性）
解析：**RDS Multi-AZ** 在不同 AZ 維護一個同步的備用副本（Standby Replica）：
- 主要執行個體故障時自動容錯移轉（Failover），通常在 1-2 分鐘內完成
- 端點（Endpoint DNS）不變，應用程式無需修改
- 主要目的是**高可用性（HA）**，而非效能提升
注意：Multi-AZ 的 Standby 不提供讀取服務，若要分散讀取負載，需使用 **Read Replicas**。

(22)
中文題目：哪項功能**不是** Amazon Rekognition 支援的？
答案：快速調整照片大小以建立縮圖（Resize photos to create thumbnails）
解析：**Amazon Rekognition** 是 AI 視覺分析服務，支援：
- 臉部偵測、辨識與比較
- 物件與場景標記（Object Detection）
- 文字辨識（OCR）
- 不安全內容偵測（Content Moderation）
- 名人辨識、情緒分析
**圖片縮放**是影像處理（Image Processing）功能，Rekognition 不提供此類操作，應使用 **AWS Lambda + Pillow/Sharp** 或 **Amazon S3 + CloudFront** 等方案處理縮圖需求。

(23)
中文題目：哪些 AWS 資源可協助企業在 AWS Cloud 上建立解決方案？
答案：AWS Service Catalog / AWS Partner Network，APN
解析：
- **AWS Service Catalog**：IT 管理者可建立預先核准的產品目錄（CloudFormation 範本），讓終端使用者自助部署符合規範的 AWS 資源，確保治理與合規
- **AWS Partner Network（APN）**：AWS 認證的合作夥伴生態系，包含顧問夥伴（協助遷移與架構）與技術夥伴（提供 AWS 上的軟體解決方案）
兩者皆是協助企業在 AWS 建構解決方案的重要資源。

(24)
中文題目：關於 AWS Lambda 的正確描述為何？
答案：
- Lambda 讓你執行程式碼，無需佈建或管理伺服器
- 你只需為實際使用的運算時間付費
解析：**AWS Lambda** 核心特性：
- **無伺服器**：完全無需管理底層基礎設施
- **事件驅動**：由觸發器（S3、API Gateway、EventBridge 等）啟動
- **按需計費**：按請求次數與執行持續時間（毫秒）計費，閒置時不產生費用
- **自動擴縮**：可同時處理數千個並行請求
Lambda 是實現微服務、事件處理、排程任務的核心無伺服器服務。

(25)
中文題目：哪項 AWS 服務可用於在 Hadoop 叢集上執行大數據工作負載？
答案：Amazon EMR（彈性 MapReduce）
解析：**Amazon EMR** 是 AWS 的受管大數據平台，支援：
- **Hadoop**、Spark、Hive、HBase、Flink、Presto 等開源框架
- 自動佈建與擴縮叢集（可使用 Spot Instance 大幅降低成本）
- 適合 ETL、機器學習、資料轉換、日誌分析等大規模資料處理
客戶只需提交工作，EMR 負責叢集管理，大幅降低營運負擔。

---

## Questions (26–30)

(26) find, buy, and immediately start using software solutions
Ans: AWS Marketplace

(27) helps you scale resources to match supply with demand
Ans: AWS Auto Scaling

(28) help you review workloads against AWS best practices
Ans: AWS Trusted Advisor

(29) correct statement about RDS Multi-AZ with one standby
Ans: Amazon RDS Multi-AZ enhances database availability

(30) monitor EC2 CPU utilization and send an email if it exceeds 80%
Ans: Amazon CloudWatch / Amazon Simple Notification Service (SNS)

---

(26)
中文題目：哪項 AWS 平台可讓你尋找、購買並立即開始使用軟體解決方案？
答案：AWS Marketplace
解析：**AWS Marketplace** 是數位軟體商城，提供：
- 數千款來自第三方 ISV 的軟體產品（AMI、SaaS、容器、CloudFormation 範本）
- 支援多種計費模式：BYOL、按小時、按月、合約
- 一鍵部署，費用直接合併至 AWS 帳單
- 分類包含：安全性、機器學習、DevOps、資料庫、網路等
與 AWS Service Catalog 差異：Marketplace 是外部軟體商城；Service Catalog 是企業內部核准產品目錄。

(27)
中文題目：哪項 AWS 服務可協助依據需求自動調整資源規模？
答案：AWS Auto Scaling
解析：**AWS Auto Scaling** 根據定義的政策自動增減資源數量：
- **動態擴展**：依 CloudWatch 指標（如 CPU 使用率）觸發
- **預測性擴展**：使用機器學習預測流量並提前擴展
- **排程擴展**：依時間排程調整
支援服務：EC2 Auto Scaling 群組、ECS、DynamoDB、Aurora 等，確保資源供需平衡，避免浪費或效能不足。

(28)
中文題目：哪項 AWS 服務可協助你對照 AWS 最佳實踐審查工作負載？
答案：AWS Trusted Advisor
解析：**AWS Trusted Advisor** 提供即時最佳化建議，涵蓋五大類別：
- **成本優化**：識別閒置或未充分利用的資源
- **效能**：提升服務速度與回應能力
- **安全性**：識別安全設定漏洞
- **容錯**：提升高可用性與備援能力
- **服務限制**：監控接近上限的配額
Business/Enterprise 方案可解鎖全部 100+ 項檢查。

(29)
中文題目：關於部署一個含單一備用副本的 RDS Multi-AZ，正確的描述為何？
答案：Amazon RDS Multi-AZ 可增強資料庫可用性
解析：**RDS Multi-AZ** 的核心價值是**高可用性（High Availability）**：
- 同步複寫至另一 AZ 的 Standby 副本
- 主要副本故障時自動切換，無需人工介入
- 端點不變，應用程式透明切換
常見誤解：Standby 副本不接受讀取請求，不能提升讀取效能；若要讀取擴展，需另建 Read Replicas。

(30)
中文題目：如何監控 EC2 CPU 使用率，並在超過 80% 時發送電子郵件通知？
答案：Amazon CloudWatch / Amazon Simple Notification Service，SNS
解析：標準監控告警架構：
1. **Amazon CloudWatch**：收集 EC2 的 CPU 使用率指標，設定警報閾值（80%）
2. **CloudWatch Alarm**：當指標超過閾值時觸發動作
3. **Amazon SNS**：接收 CloudWatch 警報，將通知發送至訂閱的電子郵件地址
此架構是 AWS 上最常見的監控通知模式，三個元件各司其職，協同完成告警流程。

---

## Questions (31–35)

(31) deliver consistent low-latency gameplay to nearby users
Ans: AWS Local Zones

(32) pillars mentioned in the AWS Well-Architected Framework
Ans: Reliability（可靠性）/ Cost Optimization（成本優化）

(33) essential for implementing security of resources in AWS Cloud
Ans: AWS Identity and Access Management (IAM)

(34) fully managed, flexible, scalable file storage with low latency for Windows-based applications
Ans: Amazon FSx for Windows File Server

(35) will help accelerate your business outcomes — CAF phase
Ans: Envision（願景規劃）

---

(31)
中文題目：哪項 AWS 服務可為附近使用者提供穩定低延遲的遊戲體驗？
答案：AWS Local Zones
解析：**AWS Local Zones** 是 AWS 基礎設施的延伸，將運算、儲存、資料庫等服務部署至更靠近終端使用者的地理位置：
- 提供個位數毫秒（single-digit millisecond）延遲
- 適合即時遊戲、媒體串流、即時分析、AR/VR 等對延遲敏感的應用
- 與父 Region 連接，可存取完整 AWS 服務
與 Wavelength 差異：Wavelength 部署於電信商 5G 網路邊緣；Local Zones 部署於主要都會區。

(32)
中文題目：AWS Well-Architected Framework 包含哪些支柱？
答案：Reliability（可靠性）/ Cost Optimization（成本優化）
解析：**AWS Well-Architected Framework** 共有六大支柱：
1. **Operational Excellence**（卓越營運）：自動化、持續改進
2. **Security**（安全性）：保護資料與系統
3. **Reliability**（可靠性）：從故障中恢復、按需擴展
4. **Performance Efficiency**（效能效率）：有效利用資源
5. **Cost Optimization**（成本優化）：避免不必要支出
6. **Sustainability**（永續性）：降低環境影響（2021年新增）
本題選項為 Reliability 與 Cost Optimization，均為六大支柱中的一部分。

(33)
中文題目：哪項 AWS 服務是實施 AWS Cloud 資源安全性的核心？
答案：AWS Identity and Access Management，IAM
解析：**AWS IAM** 是 AWS 安全架構的基礎，提供：
- **身份驗證（Authentication）**：確認使用者是誰
- **授權（Authorization）**：控制使用者能做什麼（Policy）
- 管理使用者、群組、角色、服務帳號
- 支援最小權限原則（Least Privilege）
- 與所有 AWS 服務整合
沒有 IAM，就無法實施任何細粒度的存取控制，是 AWS 安全的第一道防線。

(34)
中文題目：哪項 AWS 服務為 Windows 應用程式提供完全受管、靈活、可擴展且低延遲的檔案儲存？
答案：Amazon FSx for Windows File Server
解析：**Amazon FSx for Windows File Server** 提供：
- 原生支援 **SMB 協定**與 Windows NTFS 檔案系統
- 與 Active Directory 整合，支援 Windows 驗證
- 適合 Windows 應用程式、主目錄、企業工作負載
- 完全受管，AWS 負責硬體、OS、備份
與 EFS 差異：EFS 使用 NFS 協定，主要供 Linux 使用；FSx for Windows 使用 SMB，專為 Windows 設計。

(35)
中文題目：哪個 AWS Cloud Adoption Framework（CAF）階段專注於加速業務成果？
答案：Envision（願景規劃）
解析：**AWS CAF** 將雲端轉型旅程分為四個階段：
1. **Envision（願景）**：識別並優先排序轉型機會，將雲端目標與業務成果連結，建立轉型路線圖
2. **Align（對齊）**：識別各視角的能力缺口，制定行動計劃
3. **Launch（啟動）**：交付試行專案，展示業務價值
4. **Scale（擴展）**：將成功案例擴展至全組織
題目關鍵字「accelerate business outcomes（加速業務成果）」對應 **Envision** 階段的核心目標。

---

## Questions (36–40)

(36) acquire resources as you need and release when no longer needed
Ans: Elasticity（彈性）

(37) Operations Perspective of the AWS Cloud Adoption Framework includes
Ans: Performance and capacity management（效能與容量管理）

(38) block users from certain geographies from accessing content
Ans: AWS Web Application Firewall (AWS WAF)

(39) AWS pricing policy for data transfer charges into or out of an AWS Region
Ans: Only outbound data transfer is charged（僅對外傳輸收費）

(40) correct statements about the AWS root user account
Ans: Highly recommended to enable MFA for root user / Root user credentials are the email and password used to create the AWS account

---

(36)
中文題目：按需取得資源並在不需要時釋放，這對應雲端的哪項特性？
答案：Elasticity（彈性）
解析：**Elasticity（彈性）** 是雲端的核心特性之一，指系統能夠：
- 依據需求**自動增加**資源（Scale Out）
- 需求降低時**自動釋放**資源（Scale In）
- 精確匹配供需，避免過度配置或資源不足
與 Agility 差異：Agility 強調快速取得資源的速度；Elasticity 強調動態調整資源規模以匹配需求。AWS Auto Scaling 是實現 Elasticity 的核心服務。

(37)
中文題目：AWS CAF 營運視角（Operations Perspective）包含哪些能力？
答案：效能與容量管理（Performance and capacity management）
解析：**AWS CAF Operations Perspective** 關注如何確保業務持續運作，核心能力包含：
- **效能與容量管理**：確保系統效能符合業務需求
- 事件管理（Event Management）
- 問題與事故管理（Incident Management）
- 變更與發布管理
- 持續性管理（可用性與災難復原）
營運視角的主要利害關係人：IT 營運經理、Site Reliability Engineer（SRE）。

(38)
中文題目：哪項 AWS 服務可封鎖特定地理位置的使用者存取內容？
答案：AWS Web Application Firewall，WAF
解析：**AWS WAF** 支援**地理位置匹配條件（Geo Match）**，可依使用者 IP 的地理位置封鎖或允許特定國家/地區的流量。除地理封鎖外，WAF 也支援：
- IP 黑白名單
- HTTP Header/Body 規則
- 速率限制（Rate Limiting）
部署於 CloudFront、ALB、API Gateway 前端，有效控制內容存取範圍。

(39)
中文題目：AWS 對進出 Region 的資料傳輸如何收費？
答案：只有**對外（Outbound）**資料傳輸收費
解析：AWS 資料傳輸費用原則：
- **傳入 AWS（Inbound）**：**免費**（從網際網路傳入 AWS）
- **傳出 AWS（Outbound）**：**收費**（從 AWS 傳出至網際網路）
- **同 Region 內，AZ 之間**：少量費用
- **跨 Region**：收費（雙向）
- **同 AZ 內**：免費
此設計鼓勵資料流入 AWS，對外傳輸才產生費用。

(40)
中文題目：關於 AWS Root 使用者帳戶，哪些描述是正確的？
答案：
- 強烈建議為 Root 帳戶啟用 MFA
- Root 使用者的登入憑證是建立 AWS 帳戶時使用的電子郵件地址與密碼
解析：**AWS Root User** 最佳實踐：
- Root 帳戶擁有帳戶的**最高權限**，不受 IAM Policy 限制
- **立即啟用 MFA**（多因素驗證），防止帳戶被盜用
- 日常操作應使用具有適當權限的 IAM 使用者，不直接使用 Root
- Root 帳戶專用任務：變更帳戶設定、關閉帳戶、恢復 IAM 管理員存取等少數操作

---

## Questions (41–45)

(41) track the history of configuration changes on AWS resources
Ans: AWS Config

(42) be used to access and manage all AWS services
Ans: AWS Management Console / AWS Command Line Interface (AWS CLI) / AWS Software Development Kit (SDK)

(43) 24x7 phone-based technical support — MOST cost-effective
Ans: AWS Business Support

(44) thumbnails that are rarely used but need to be immediately accessible — most cost-effective S3 storage
Ans: Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)

(45) LEAST operational overhead for any scale
Ans: Amazon DynamoDB

---

(41)
中文題目：哪項 AWS 服務可追蹤 AWS 資源的組態變更歷史？
答案：AWS Config
解析：**AWS Config** 是組態管理與合規服務，提供：
- 持續記錄 AWS 資源的組態快照與變更歷史
- 評估資源組態是否符合自訂規則（Config Rules）
- 產生組態時間軸，可追溯「資源在某時間點的狀態為何」
與 CloudTrail 差異：**CloudTrail** 記錄「誰做了什麼 API 操作」；**AWS Config** 記錄「資源組態是什麼狀態及如何變化」，兩者互補。

(42)
中文題目：哪些方式可存取與管理所有 AWS 服務？
答案：AWS Management Console / AWS CLI / AWS SDK
解析：AWS 提供三大存取介面：
- **AWS Management Console**：網頁圖形介面，適合視覺化操作與學習
- **AWS CLI（Command Line Interface）**：命令列工具，適合腳本自動化與批次操作
- **AWS SDK（Software Development Kit）**：各程式語言的函式庫，適合應用程式整合（Python Boto3、Node.js、Java 等）
三者皆呼叫相同的底層 AWS API，選擇取決於使用場景與偏好。

(43)
中文題目：哪個 AWS Support 方案提供 24/7 電話技術支援，且最符合成本效益？
答案：AWS Business Support
解析：Support 方案電話支援比較：
- **Basic**：無技術支援
- **Developer**：僅 Email 支援（工作時間）
- **Business**：**24/7 電話、Email、Chat 技術支援**，回應時間最快 1 小時（生產系統中斷）
- **Enterprise**：同 Business，另加 TAM，但費用更高
題目要求「24/7 電話支援 + 最符合成本效益」，**Business** 是提供此功能的最低成本方案。

(44)
中文題目：照片分享 App 需要儲存極少存取的縮圖，但需要立即可存取，哪種 S3 儲存類別最符合成本效益？
答案：Amazon S3 One Zone-Infrequent Access，S3 One Zone-IA
解析：S3 低頻存取類別比較：
- **S3 Standard-IA**：跨多 AZ 冗餘，立即存取，成本較 Standard 低
- **S3 One Zone-IA**：僅儲存在**單一 AZ**，比 Standard-IA 再便宜約 20%，同樣提供毫秒級存取
縮圖是可重新生成的衍生資料（非原始資料），即使單一 AZ 故障導致資料遺失也可重新產生，因此選用 **One Zone-IA** 最符合成本效益。

(45)
中文題目：哪項 AWS 資料庫服務在任何規模下的營運負擔最低？
答案：Amazon DynamoDB
解析：**Amazon DynamoDB** 是完全受管的 NoSQL 資料庫，特點：
- **零伺服器管理**：無需佈建、修補、擴展資料庫伺服器
- **自動擴縮**：依流量自動調整讀寫容量
- **Serverless 選項**：DynamoDB On-Demand 模式，完全按需計費
- 個位數毫秒延遲，可處理每秒數百萬筆請求
相比 RDS（需管理執行個體大小、多 AZ、備份），DynamoDB 的營運負擔極低，是無伺服器架構的首選資料庫。

---

## Questions (46–50)

(46) upload PHP code but still wants access to the underlying OS
Ans: AWS Elastic Beanstalk

(47) Shared Responsibility Model — customer responsibility for Amazon RDS
Ans: Database encryption

(48) flexible schema and supports document data models
Ans: Amazon DynamoDB

(49) secure shell access to EC2 without opening new ports or using public IPs
Ans: AWS Systems Manager Session Manager

(50) correct statement regarding AWS Storage services
Ans: S3 is object-based, EBS is block-based, EFS is file-based storage

---

(46)
中文題目：企業想上傳 PHP 程式碼並讓 AWS 自動處理部署，但仍需存取底層 OS，應使用哪項服務？
答案：AWS Elastic Beanstalk
解析：**AWS Elastic Beanstalk** 是 PaaS 平台，特點：
- 自動處理部署、容量配置、負載平衡、Auto Scaling、健康監控
- 支援多種語言：PHP、Python、Java、Node.js、.NET、Ruby 等
- **保留底層 EC2 存取權**：客戶仍可 SSH 登入 EC2，存取與自訂 OS 環境
這與 Lambda（完全無伺服器，無 OS 存取）不同。Elastic Beanstalk 兼顧部署便利性與底層控制權。

(47)
中文題目：在 AWS 共同責任模型中，Amazon RDS 的哪些事項屬於客戶的責任？
答案：資料庫加密（Database encryption）
解析：RDS 責任劃分：
- **AWS 負責**：底層硬體、OS 修補、資料庫引擎安裝與更新、實體安全
- **客戶負責**：**資料庫加密設定**（選擇是否啟用 RDS 加密、管理 KMS 金鑰）、資料庫使用者與權限管理、安全群組規則、備份保留政策
雖然 AWS 提供加密功能，但**是否啟用與金鑰管理**是客戶的責任。

(48)
中文題目：哪項 AWS 資料庫服務支援彈性結構（flexible schema）與文件資料模型？
答案：Amazon DynamoDB
解析：**Amazon DynamoDB** 是 NoSQL 資料庫，支援：
- **彈性結構（Flexible Schema）**：每筆資料項目（Item）可擁有不同屬性，無需預先定義固定結構
- **資料模型**：鍵值（Key-Value）與文件（Document）模型，支援 JSON 格式資料
- 與傳統關聯式資料庫（RDS）不同，不需要固定的資料表結構（Schema），適合資料格式多變的應用場景。

(49)
中文題目：哪項 AWS 服務可提供安全的 Shell 存取 EC2 執行個體，且無需開放新連接埠或使用公有 IP？
答案：AWS Systems Manager Session Manager
解析：**AWS Systems Manager Session Manager** 提供安全的瀏覽器或 CLI 型 Shell 存取：
- **無需開放 SSH Port 22 或 RDP Port 3389**
- **無需公有 IP 位址或跳板機（Bastion Host）**
- 所有工作階段日誌自動記錄至 CloudTrail 與 S3
- 透過 IAM 政策控制存取權限
大幅降低攻擊面，是取代傳統 SSH 跳板機的安全最佳實踐。

(50)
中文題目：關於 AWS 儲存服務，哪個描述是正確的？
答案：S3 是物件儲存、EBS 是區塊儲存、EFS 是檔案儲存
解析：AWS 三大儲存類型對照：

| 服務 | 類型 | 存取方式 | 適用場景 |
|------|------|----------|----------|
| **Amazon S3** | 物件儲存（Object） | HTTP/REST API | 靜態檔案、備份、資料湖 |
| **Amazon EBS** | 區塊儲存（Block） | 掛載至單一 EC2 | 作業系統磁碟、資料庫 |
| **Amazon EFS** | 檔案儲存（File） | NFS，多 EC2 共享 | 共享工作目錄、CMS |

---

## Questions (51–55)

(51) routing requests to the endpoint that provides the fastest experience
Ans: Latency-based routing

(52) publishes up-to-the-minute status of ALL AWS services in ALL Regions
Ans: AWS Health Dashboard — Service Health

(53) the fundamental drivers of cost with AWS Cloud
Ans: Compute, Storage, and Outbound Data Transfer

(54) most cost-effective with no long-term commitment, no upfront payment, and won't be interrupted
Ans: On-Demand Instance

(55) correct statement about AZ scope for VPC and subnet
Ans: VPC spans all AZs in the Region; subnet spans only one AZ

---

(51)
中文題目：哪種 Route 53 路由政策將請求路由至提供最快速體驗的端點？
答案：Latency-based routing（延遲型路由）
解析：**Latency-based routing** 根據使用者到各 AWS Region 的網路延遲選擇最佳端點：
- Route 53 測量使用者到各 Region 的延遲
- 自動將流量路由至**延遲最低**的 Region
- 適合全球部署、需要低延遲的應用（遊戲、串流、API）
與 Geolocation 路由差異：Geolocation 依使用者**地理位置**路由（不保證延遲最低）；Latency-based 依**實際網路延遲**路由。

(52)
中文題目：哪項 AWS 服務發布所有 AWS 服務在所有 Region 的即時狀態資訊？
答案：AWS Health Dashboard — Service Health（服務健康儀表板）
解析：
- **Service Health Dashboard**（service.aws.amazon.com/health）：公開頁面，顯示所有 AWS 服務在所有 Region 的即時與歷史狀態，任何人皆可查看
- **Your Account Health Dashboard**：顯示**影響你帳戶**的特定事件（個人化）
題目關鍵字「ALL AWS services in ALL Regions（所有服務、所有區域）」對應公開的 **Service Health Dashboard**。

(53)
中文題目：AWS Cloud 費用的根本驅動因素為何？
答案：Compute（運算）、Storage（儲存）、Outbound Data Transfer（對外資料傳輸）
解析：AWS 定義三大核心費用驅動因子：
- **Compute（運算）**：EC2、Lambda、ECS 等運算資源的使用時間與規格
- **Storage（儲存）**：S3、EBS、EFS 等儲存的容量與請求次數
- **Outbound Data Transfer（對外資料傳輸）**：從 AWS 傳出至網際網路的流量
注意：資料傳入 AWS 免費；跨 Region 傳輸另計；同 Region 內部分傳輸也有費用。

(54)
中文題目：哪種 EC2 購買方式最符合成本效益，且無長期承諾、無預付費用，並保證不會被中斷？
答案：On-Demand Instance（隨需執行個體）
解析：此題考的是三個條件的交集：
- **無長期承諾（No long-term commitment）**：排除 Reserved Instance（需 1/3 年）
- **無預付費用（No upfront payment）**：排除 All Upfront RI
- **保證不被中斷（Won't be interrupted）**：排除 Spot Instance（可被中斷）
**On-Demand** 完全符合三項條件，按需使用、按小時/秒計費，無任何承諾，且不會被 AWS 中斷。

(55)
中文題目：關於 VPC 與子網路（Subnet）的 AZ 範圍，哪個描述正確？
答案：VPC 跨越 Region 內所有 AZ；Subnet 只跨越單一 AZ
解析：AWS 網路架構範圍：
- **VPC**：**Region 層級**，自動跨越該 Region 內所有 AZ，是整個虛擬網路的邊界
- **Subnet**：**AZ 層級**，每個 Subnet 只存在於單一 AZ 內
- 一個 VPC 可包含多個 Subnet，分布於不同 AZ，實現高可用性架構
最佳實踐：在每個 AZ 各建立一個 Public Subnet 和 Private Subnet，確保跨 AZ 冗餘。

---

## Questions (56–60)

(56) avoiding the operational overhead of scaling, patching, securing, and managing servers
Ans: Amazon ECS — Fargate launch type

(57) correct statement for Security Group vs Network ACL
Ans: Security Group acts as a firewall at the instance level; Network ACL acts at the subnet level

(58) get notified when AWS account charges exceed your budgeted amount
Ans: AWS Budgets

(59) describes prohibited uses of the web services
Ans: AWS Acceptable Use Policy

(60) deploys IT infrastructure in a combination of on-premises and AWS Cloud
Ans: Hybrid deployment（混合部署）

---

(56)
中文題目：哪種 AWS 容器服務可避免擴展、修補、保護與管理伺服器的營運負擔？
答案：Amazon ECS — Fargate launch type（Fargate 啟動類型）
解析：Amazon ECS 有兩種啟動類型：
- **EC2 launch type**：客戶需自行管理 EC2 叢集（OS 修補、擴展、安全）
- **Fargate launch type**：**完全無伺服器**，AWS 負責底層基礎設施的所有管理，客戶只需定義容器規格與任務
題目關鍵字「avoiding operational overhead of scaling, patching, securing servers」精確對應 **Fargate**，客戶只需專注於容器應用程式本身。

(57)
中文題目：關於 Security Group 與 Network ACL 的正確描述為何？
答案：Security Group 在**執行個體（Instance）層級**作為防火牆；Network ACL 在**子網路（Subnet）層級**運作
解析：

| 特性 | Security Group | Network ACL |
|------|----------------|-------------|
| 作用層級 | 執行個體（Instance） | 子網路（Subnet） |
| 狀態 | 有狀態（Stateful） | 無狀態（Stateless） |
| 規則類型 | 僅 Allow | Allow 與 Deny |
| 預設行為 | 拒絕所有流量 | 允許所有流量 |

兩者為互補的防火牆機制，建議搭配使用實現縱深防禦。

(58)
中文題目：哪項 AWS 服務可在帳戶費用超過預算時發送通知？
答案：AWS Budgets
解析：**AWS Budgets** 可設定多種類型的預算警示：
- **Cost Budget**：實際或預測費用超出閾值時通知
- **Usage Budget**：使用量超出閾值時通知
- **Reservation Budget**：RI/Savings Plans 使用率過低時通知
通知可透過 Email 或 SNS 主題發送，支援多個警示閾值（如達到 80%、100%、預測超出時各發一次通知）。

(59)
中文題目：哪份 AWS 文件描述 Web 服務的禁止使用行為？
答案：AWS Acceptable Use Policy（AWS 可接受使用政策）
解析：**AWS Acceptable Use Policy（AUP）** 明確列出使用 AWS 服務的禁止行為，包含：
- 傳送未經授權的大量訊息（垃圾郵件）
- 散佈惡意軟體
- 進行安全攻擊或入侵他人系統
- 散佈非法內容
AUP 是所有 AWS 客戶必須遵守的使用條款，違反可能導致帳戶暫停。

(60)
中文題目：企業將 IT 基礎設施部署於本地資料中心與 AWS Cloud 的組合中，這稱為什麼部署模型？
答案：Hybrid deployment（混合部署）
解析：AWS 定義三種部署模型：
- **Cloud（雲端）**：所有資源完全部署於 AWS Cloud
- **On-Premises（本地）**：所有資源部署於本地資料中心（私有雲）
- **Hybrid（混合）**：同時使用本地環境與 AWS Cloud，透過 Direct Connect 或 VPN 連接，適合有合規要求或漸進式遷移需求的企業

---

## Questions (61–65)

(61) wants to do SQL-based analysis with minimum effort
Ans: Amazon Athena

(62) the different Storage Gateway types
Ans: Tape Gateway / File Gateway / Volume Gateway

(63) needs consolidated billing and a single payment method
Ans: AWS Organizations

(64) migrate to AWS Cloud easily without rewriting code
Ans: Amazon MQ

(65) be used to prevent DDoS attacks
Ans: AWS Shield / AWS Web Application Firewall (AWS WAF) / Amazon CloudFront with Amazon Route 53

---

(61)
中文題目：哪項 AWS 服務可讓企業以最少的工作量對資料進行 SQL 分析？
答案：Amazon Athena
解析：**Amazon Athena** 是 Serverless 互動式查詢服務：
- 直接對 **Amazon S3** 中的資料執行標準 SQL 查詢
- 無需載入資料、無需管理伺服器或資料庫
- 支援 CSV、JSON、Parquet、ORC 等多種格式
- 按掃描的資料量計費（每 TB 約 $5）
題目關鍵字「SQL-based analysis + minimum effort」對應 Athena 的核心定位——無伺服器、開箱即查。

(62)
中文題目：AWS Storage Gateway 有哪些類型？
答案：Tape Gateway（磁帶閘道）/ File Gateway（檔案閘道）/ Volume Gateway（磁碟區閘道）
解析：**AWS Storage Gateway** 將本地環境與 AWS 儲存整合，分為三種類型：
- **File Gateway**：透過 NFS/SMB 存取 S3，本地快取最近使用的檔案
- **Volume Gateway**：提供 iSCSI 區塊儲存，資料備份至 S3（Stored 或 Cached 模式）
- **Tape Gateway**：模擬虛擬磁帶機（VTL），將備份寫入 S3 Glacier，取代實體磁帶
三者共同目標：讓本地應用程式無感地使用 AWS 雲端儲存。

(63)
中文題目：企業需要合併帳單與統一付款方式，應使用哪項 AWS 服務？
答案：AWS Organizations
解析：**AWS Organizations** 提供多帳戶管理，核心功能包含：
- **Consolidated Billing（合併帳單）**：所有成員帳戶的費用合併至主帳戶，單一付款方式
- **Volume Discounts**：合併使用量享受更大折扣（如 S3、EC2）
- **RI 與 Savings Plans 共享**：未使用的折扣自動套用至其他帳戶
- 服務控制政策（SCP）：統一管理組織內帳戶的權限範圍

(64)
中文題目：哪項 AWS 服務可協助企業輕鬆遷移至 AWS Cloud，且無需重寫程式碼？
答案：Amazon MQ
解析：**Amazon MQ** 是受管訊息代理（Message Broker）服務，支援 **Apache ActiveMQ** 與 **RabbitMQ**：
- 企業若已使用 ActiveMQ 或 RabbitMQ，可直接遷移至 Amazon MQ，**無需修改應用程式程式碼**
- 使用標準協定：AMQP、MQTT、OpenWire、STOMP
與 SQS/SNS 差異：SQS/SNS 是 AWS 原生訊息服務，需調整程式碼才能整合；Amazon MQ 是針對傳統訊息系統的直接遷移路徑。

(65)
中文題目：哪些 AWS 服務可用於防禦 DDoS 攻擊？
答案：AWS Shield / AWS WAF / Amazon CloudFront with Amazon Route 53
解析：AWS 的多層 DDoS 防禦架構：
- **AWS Shield Standard**：自動防護所有客戶，抵禦第 3/4 層 DDoS 攻擊，免費
- **AWS Shield Advanced**：進階第 7 層防護、DRT 支援、費用保護，付費
- **AWS WAF**：過濾惡意 HTTP 請求，防禦應用層（第 7 層）攻擊，與 Shield Advanced 搭配使用
- **CloudFront + Route 53**：CloudFront 分散流量至邊緣節點，Route 53 提供 Anycast 路由，共同吸收並分散大流量 DDoS 攻擊，降低對源站的衝擊
多服務協同防禦是 AWS DDoS 最佳實踐架構。