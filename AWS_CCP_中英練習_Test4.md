# AWS Cloud Practitioner【TEST04】

---

## Questions (1–5)

(1) create a logically isolated section of the AWS Cloud where you can launch AWS resources in your virtual network
Ans: Virtual Private Cloud (VPC)

(2) Two VPCs need to privately share data between each other
Ans: VPC peering connection

(3) wants to ensure that all customer data on Amazon S3 always stays private
Ans: Use Amazon S3 Block Public Access

(4) are free under the Amazon S3 pricing model
Ans: Data transferred in from the internet / Data transferred out to an EC2 instance in the same AWS Region as the S3 bucket

(5) wants to review Payment Card Industry (PCI) reports on AWS Cloud
Ans: AWS Artifact

---

(1)
中文題目：哪項 AWS 服務可讓你在 AWS Cloud 中建立邏輯隔離的區段，並在其中的虛擬網路啟動 AWS 資源？
答案：Virtual Private Cloud，VPC（虛擬私有雲）
解析：**Amazon VPC** 是 AWS 網路的基礎元件，讓你能夠：
- 在 AWS Cloud 中建立**邏輯隔離**的虛擬網路環境
- 自訂 IP 位址範圍（CIDR Block）、子網路、路由表、網路閘道
- 完全控制進出流量（Security Group、Network ACL）
- 在 VPC 內啟動 EC2、RDS 等 AWS 資源
每個 AWS 帳戶在每個 Region 都有一個預設 VPC，可立即使用。VPC 是所有 AWS 網路架構的起點。

(2)
中文題目：兩個 VPC 需要私下共享資料，應使用哪項 AWS 功能？
答案：VPC Peering Connection（VPC 對等連線）
解析：**VPC Peering** 讓兩個 VPC 之間建立私有網路連線，流量不經過公共網際網路：
- 支援**同帳號、跨帳號、跨 Region** 的 VPC 對等連線
- 對等連線是**非傳遞性（Non-transitive）**：A-B、B-C 對等，A 無法透過 B 到達 C，需另建 A-C 對等
- CIDR Block 不能重疊
- 若需連接多個 VPC，大規模時建議改用 **AWS Transit Gateway**（星型拓撲，避免大量 Peering 管理）

(3)
中文題目：企業想確保 Amazon S3 上的所有客戶資料始終保持私有，應如何設定？
答案：使用 Amazon S3 Block Public Access（S3 封鎖公開存取）
解析：**S3 Block Public Access** 提供帳戶層級或儲存桶層級的公開存取封鎖，包含四項設定：
- 封鎖新的公開 ACL
- 封鎖現有的公開 ACL
- 封鎖新的公開 Bucket Policy
- 封鎖現有的公開 Bucket Policy
即使之後有人誤設公開政策，Block Public Access 也會覆蓋並防止資料外洩。是確保 S3 資料不被公開存取的最強保護機制。

(4)
中文題目：在 Amazon S3 定價模型中，哪些資料傳輸是免費的？
答案：從網際網路傳入 S3 的資料 / 傳出至同一 AWS Region 內 EC2 執行個體的資料
解析：AWS S3 資料傳輸費用規則：
- **傳入 S3（Inbound）**：從網際網路上傳資料至 S3，**免費**
- **同 Region 傳出至 EC2**：S3 傳出至同 Region 的 EC2，**免費**
- **傳出至網際網路（Outbound）**：從 S3 下載資料至公網，**收費**
- **跨 Region 傳輸**：S3 資料複寫或傳送至其他 Region，**收費**
這些規則設計鼓勵資料流入 AWS，並讓同 Region 內的服務溝通不產生額外成本。

(5)
中文題目：企業想在 AWS Cloud 上查閱支付卡產業（PCI）的合規報告，應使用哪項服務？
答案：AWS Artifact
解析：**AWS Artifact** 是 AWS 的合規文件自助下載入口，提供：
- **合規報告**：SOC 1/2/3、PCI DSS、ISO 27001、ISO 27017、HIPAA、FedRAMP 等第三方稽核報告
- **合規協議**：Business Associate Agreement（BAA）等法律協議
- 完全免費，透過 AWS Management Console 存取
題目關鍵字「PCI reports（PCI 合規報告）」直接對應 AWS Artifact 的核心功能，是審查 AWS 合規文件的唯一官方入口。

---

## Questions (6–10)

(6) Amazon EC2 different from traditional hosting systems
Ans: Developers can launch and terminate instances anytime / Amazon EC2 can scale with changing computing requirements

(7) choose for a data processing project that needs a schemaless database
Ans: Amazon DynamoDB

(8) statements are true regarding Amazon S3
Ans: Amazon S3 stores data in a flat non-hierarchical structure / Amazon S3 is a key-value based object storage service

(9) describes an Availability Zone (AZ)
Ans: One or more data centers in the same location

(10) CORRECT regarding AWS Global Accelerator
Ans: AWS Global Accelerator provides static IP addresses that act as a fixed entry point / AWS Global Accelerator is a good fit for non-HTTP use cases

---

(6)
中文題目：Amazon EC2 與傳統託管系統相比有哪些不同？
答案：
- 開發人員可隨時啟動與終止執行個體
- Amazon EC2 可依運算需求變化彈性擴縮
解析：傳統實體主機託管的限制：
- 需要提前採購硬體，週期長（數週至數月）
- 容量固定，無法快速擴縮
- 終止使用仍需支付閒置硬體成本
**EC2 的革命性差異**：
- **隨時啟動/終止**：幾分鐘內即可取得或釋放運算資源
- **彈性擴縮**：依需求自動增減，搭配 Auto Scaling 實現動態調整
- **按需付費**：只為實際使用的時間付費，無閒置成本

(7)
中文題目：資料處理專案需要一個無結構描述（schemaless）的資料庫，應選擇哪項 AWS 服務？
答案：Amazon DynamoDB
解析：**Amazon DynamoDB** 是 NoSQL 資料庫，核心特性：
- **Schemaless（無固定結構）**：每筆資料項目（Item）可擁有不同的屬性，無需預先定義固定的資料表結構
- 支援鍵值（Key-Value）與文件（Document）資料模型
- 自動擴縮，個位數毫秒延遲
相比之下，**Amazon RDS**（MySQL、PostgreSQL 等）是關聯式資料庫，需要預先定義固定的 Schema（資料表結構），無法靈活應對資料格式多變的場景。

(8)
中文題目：關於 Amazon S3，哪些描述是正確的？
答案：
- Amazon S3 以扁平非階層式結構儲存資料
- Amazon S3 是以鍵值為基礎的物件儲存服務
解析：**Amazon S3 的儲存模型**：
- **扁平非階層式（Flat Non-Hierarchical）**：S3 本身不存在真正的資料夾或目錄結構，「資料夾」只是 Key 名稱中包含「/」的視覺化呈現，底層仍是扁平的命名空間
- **鍵值物件儲存（Key-Value Object Storage）**：每個物件由唯一的 Key（物件名稱）識別，Value 為物件內容，搭配 Metadata
這與傳統檔案系統（EFS）的樹狀目錄結構截然不同。

(9)
中文題目：哪個描述最能說明可用區（Availability Zone，AZ）的定義？
答案：位於同一地理位置的一個或多個資料中心
解析：**AWS Availability Zone（AZ）** 的架構：
- 由**一個或多個**實體資料中心組成，但對外呈現為單一 AZ
- 同一 AZ 的資料中心之間透過高速低延遲私有網路連接
- 不同 AZ 之間有足夠的地理距離，確保獨立的電力、冷卻、網路，防止單點故障
- 一個 AWS Region 包含最少 3 個 AZ（通常 3-6 個）
AZ 是 AWS 高可用性架構的核心單位，跨 AZ 部署是容錯的基本策略。

(10)
中文題目：關於 AWS Global Accelerator，哪些描述是正確的？
答案：
- AWS Global Accelerator 提供靜態 IP 位址，作為應用程式的固定入口點
- AWS Global Accelerator 適合非 HTTP 使用案例
解析：**AWS Global Accelerator** 的核心特性：
- **靜態 Anycast IP**：提供兩個固定的全球靜態 IP，流量從最近的 AWS 邊緣節點進入 AWS 骨幹網路，無需更改 DNS
- **非 HTTP 使用案例**：特別適合 TCP/UDP 協定，如遊戲、IoT、VoIP，這些場景無法使用 CloudFront（CDN 主要針對 HTTP/HTTPS）
- **動態路由**：自動將流量路由至最近、最健康的端點，實現全球低延遲與自動故障轉移

---

## Questions (11–15)

(11) are benefits of AWS WAF
Ans: AWS WAF can block all requests except the ones you allow / AWS WAF can check for SQL injection code

(12) centrally manage servers on AWS and on-premises to collect software inventory, run commands, configure and patch servers
Ans: AWS Systems Manager

(13) used together to send alerts whenever the AWS account root user signs in
Ans: Amazon CloudWatch / Amazon Simple Notification Service (Amazon SNS)

(14) connect its on-premises data center with multiple VPCs
Ans: AWS Transit Gateway / AWS Direct Connect

(15) best practice for application architecture on AWS Cloud
Ans: Build loosely coupled components（建立鬆散耦合元件）

---

(11)
中文題目：AWS WAF 提供哪些安全優勢？
答案：
- AWS WAF 可封鎖除你允許以外的所有請求（白名單模式）
- AWS WAF 可檢查 SQL 注入攻擊碼
解析：**AWS WAF** 的核心防護能力：
- **白名單（Allow List）模式**：預設封鎖所有流量，只允許符合規則的請求通過，實現最嚴格的存取控制
- **SQL Injection 防護**：偵測並封鎖嘗試注入惡意 SQL 語法的 HTTP 請求，保護後端資料庫
- **XSS 防護**：跨站腳本攻擊過濾
- **速率限制（Rate Limiting）**：防止 API 濫用與暴力破解
- **IP 封鎖**：依 IP 或 IP 範圍封鎖惡意來源

(12)
中文題目：哪項 AWS 服務可集中管理 AWS 與本地端伺服器，包含收集軟體清單、執行指令、設定與大規模修補？
答案：AWS Systems Manager
解析：**AWS Systems Manager（SSM）** 是混合雲統一管理平台，核心功能：
- **Inventory（清單）**：自動收集 EC2 與本地伺服器的軟體清單、設定資訊
- **Run Command**：遠端執行命令，無需 SSH 或 RDP
- **Patch Manager**：自動化 OS 與應用程式修補，跨 AWS 與本地端
- **Session Manager**：安全的瀏覽器型 Shell 存取，無需開放 Port 22
- **Parameter Store**：安全儲存設定與密鑰
支援 EC2 與透過 SSM Agent 連接的本地端伺服器，實現混合雲統一管理。

(13)
中文題目：哪兩項 AWS 服務可搭配使用，在 AWS 帳戶 Root 使用者登入時發送警示？
答案：Amazon CloudWatch / Amazon Simple Notification Service，SNS
解析：Root 使用者登入警示的實作流程：
1. **AWS CloudTrail** 記錄 Root 使用者的登入 API 事件
2. **Amazon CloudWatch** 設定指標篩選器（Metric Filter），偵測 CloudTrail 日誌中的 Root 登入事件
3. **CloudWatch Alarm** 在事件發生時觸發
4. **Amazon SNS** 接收 CloudWatch 警示，發送 Email 或簡訊通知
此為 AWS 安全最佳實踐的標準告警架構，確保 Root 帳戶的任何使用都能被即時偵測。

(14)
中文題目：企業想將本地端資料中心與多個 VPC 連接，應使用哪些 AWS 服務？
答案：AWS Transit Gateway / AWS Direct Connect
解析：
- **AWS Direct Connect**：提供從本地端資料中心到 AWS 的**實體專線**，穩定低延遲，不經過公共網路
- **AWS Transit Gateway**：作為雲端網路的中央集線器，可同時連接多個 VPC 與 Direct Connect/VPN，讓本地端透過單一連線存取所有 VPC
兩者搭配是連接本地端與多 VPC 的最佳架構：Direct Connect 提供高品質本地-雲端連線，Transit Gateway 管理 VPC 間的路由與互聯。

(15)
中文題目：AWS Cloud 上應用程式架構的最佳實踐為何？
答案：Build loosely coupled components（建立鬆散耦合的元件）
解析：**鬆散耦合（Loose Coupling）** 是 AWS Well-Architected 的核心設計原則：
- 元件之間透過**標準介面**（API、訊息佇列）溝通，而非直接依賴
- 單一元件的故障不會造成整個系統崩潰
- 各元件可以獨立擴展、部署與更新
實現工具：**Amazon SQS**（佇列解耦）、**Amazon SNS**（事件通知）、**API Gateway**（標準 API 介面）
對比緊密耦合（Tight Coupling）：元件直接相互呼叫，任何一個故障都可能導致連鎖失敗。

---

## Questions (16–20)

(16) AWS Shield Advanced provides DDoS protection for
Ans: Amazon EC2 / Amazon CloudFront

(17) costs the company is responsible for
Ans: Application software license costs（應用程式軟體授權費用）

(18) serverless computing services offered by AWS
Ans: AWS Fargate / AWS Lambda

(19) Amazon S3 storage class with NO minimum storage duration charge
Ans: Amazon S3 Standard

(20) correct regarding Amazon RDS
Ans: You can use both read replicas and multi-AZ deployment for disaster recovery

---

(16)
中文題目：AWS Shield Advanced 為哪些 AWS 服務提供 DDoS 防護？
答案：Amazon EC2 / Amazon CloudFront
解析：**AWS Shield Advanced** 提供進階 DDoS 防護的服務範圍包含：
- **Amazon EC2**
- **Amazon CloudFront**
- **Elastic Load Balancing（ELB）**
- **Amazon Route 53**
- **AWS Global Accelerator**
相比 Shield Standard（保護所有 AWS 服務的基本 3/4 層防護），Shield Advanced 針對以上特定服務提供更深入的第 7 層防護、即時攻擊可視化、DDoS 回應團隊（DRT）支援與費用保護。

(17)
中文題目：企業在 AWS 上的應用程式，哪些費用由企業自行負責？
答案：Application software license costs（應用程式軟體授權費用）
解析：共同責任模型的費用對應：
- **AWS 負責的費用**：實體硬體、資料中心維運、網路基礎設施、受管服務的底層運作
- **客戶負責的費用**：**應用程式軟體授權（如 Windows Server、SQL Server、Oracle）**、應用程式開發與維護、資料管理、使用 AWS 服務的費用（EC2、S3 等）
即使在 AWS 上運行，第三方軟體的授權費用仍是客戶的責任，AWS 不負擔客戶選擇使用的商業軟體授權成本。

(18)
中文題目：AWS 提供哪些無伺服器（serverless）運算服務？
答案：AWS Fargate / AWS Lambda
解析：
- **AWS Lambda**：事件驅動的無伺服器函數運算，完全不需管理伺服器，按請求與執行時間計費
- **AWS Fargate**：容器的無伺服器運算引擎，搭配 ECS 或 EKS 使用，無需管理底層 EC2 叢集
兩者皆屬於無伺服器，差異在於：Lambda 執行單一函數（短暫任務）；Fargate 執行容器（更完整的應用程式）。相比之下，EC2 和 ECS EC2 launch type 需要客戶管理底層伺服器。

(19)
中文題目：哪種 Amazon S3 儲存類別沒有最短儲存期限的費用限制？
答案：Amazon S3 Standard
解析：S3 各儲存類別的最短儲存期限（Minimum Storage Duration）：
- **S3 Standard**：**無最短儲存期限**，即使儲存 1 天後刪除也只收 1 天費用
- **S3 Standard-IA**：最短 30 天
- **S3 One Zone-IA**：最短 30 天
- **S3 Glacier Instant / Flexible Retrieval**：最短 90 天
- **S3 Glacier Deep Archive**：最短 180 天
S3 Standard 最靈活，適合需要頻繁存取或無法預測儲存時間的資料。

(20)
中文題目：關於 Amazon RDS，哪個描述是正確的？
答案：可以同時使用 Read Replicas 與 Multi-AZ 部署來進行災難復原
解析：RDS 的兩種機制可**同時搭配使用**：
- **Multi-AZ**：提供高可用性（HA），同步複寫至同 Region 的備用副本，主要故障時自動切換（Failover），用於**災難復原與可用性**
- **Read Replicas**：提供讀取擴展，非同步複寫，可跨 Region 部署，在緊急情況下可將 Read Replica 提升（Promote）為獨立資料庫，也可用於**跨 Region 災難復原**
兩者目的不同但互補，企業可同時啟用以達到最高的可用性與擴展性。

---

## Questions (21–25)

(21) use to route traffic to a single resource
Ans: Simple routing（簡單路由）

(22) is available across all AWS Support plans
Ans: AWS Health Dashboard — Your account health

(23) is a container service of AWS
Ans: AWS Fargate

(24) can identify unattached or underutilized Amazon EBS volumes
Ans: AWS Trusted Advisor

(25) upload files to a centralized S3 bucket from geographically dispersed locations
Ans: Amazon S3 Transfer Acceleration (S3TA)

---

(21)
中文題目：哪種 Route 53 路由政策用於將流量路由至單一資源？
答案：Simple routing（簡單路由）
解析：**Route 53 Simple Routing** 是最基本的路由政策：
- 將 DNS 查詢路由至**單一指定資源**（如一個 EC2 IP 或 S3 端點）
- 不支援健康檢查（Health Check）
- 一個記錄可包含多個 IP 值，Route 53 隨機回傳其中一個（客戶端選擇）
適合單一後端、無冗餘需求的簡單架構。若需要健康檢查或流量分配，應選擇 Failover、Weighted 或 Latency 路由政策。

(22)
中文題目：哪項 AWS 服務在所有 AWS Support 方案中皆可使用？
答案：AWS Health Dashboard — Your Account Health（帳戶健康儀表板）
解析：各 Support 方案的功能差異：
- **Basic（所有帳戶）**：可存取 AWS Health Dashboard — Your Account Health、文件、白皮書、論壇
- **Developer**：加上 Email 技術支援
- **Business**：加上 24/7 電話支援、完整 Trusted Advisor
- **Enterprise**：加上 TAM、Infrastructure Event Management
**AWS Health Dashboard — Your Account Health** 是基本功能，所有方案（包含免費的 Basic）皆可使用，是唯一跨所有方案的健康狀態服務。

(23)
中文題目：哪項 AWS 服務是容器服務？
答案：AWS Fargate
解析：**AWS Fargate** 是無伺服器的容器運算引擎，用於運行 Docker 容器：
- 搭配 **Amazon ECS** 或 **Amazon EKS** 使用
- 無需佈建或管理 EC2 伺服器叢集
- 按實際使用的 vCPU 與記憶體計費
常見容器服務比較：
- **ECS（EC2 launch type）**：客戶管理底層 EC2，有伺服器存取權
- **ECS/EKS（Fargate launch type）**：無伺服器容器，AWS 管理底層
- **Amazon ECR**：容器映像倉庫（不執行容器）

(24)
中文題目：哪項 AWS 服務可識別未附加或使用率過低的 Amazon EBS Volume？
答案：AWS Trusted Advisor
解析：**AWS Trusted Advisor** 在「成本優化」類別中提供 EBS 相關建議：
- **未附加的 EBS Volume**：識別已建立但未掛載至任何 EC2 的 Volume（持續產生儲存費用但未使用）
- **低使用率的 EBS Volume**：識別讀寫 I/O 極低的 Volume，可能可以降階或刪除
Business/Enterprise 方案可存取完整的 Trusted Advisor 檢查，Basic/Developer 方案只能看到部分核心檢查。

(25)
中文題目：企業需要從地理位置分散的多個地點上傳檔案至集中的 S3 儲存桶，應使用哪項服務？
答案：Amazon S3 Transfer Acceleration，S3TA
解析：**Amazon S3 Transfer Acceleration** 利用 CloudFront 的全球邊緣節點加速長距離 S3 上傳：
- 使用者上傳至**最近的 CloudFront 邊緣節點**
- 資料透過 **AWS 優化的全球骨幹網路**高速傳輸至目標 S3 儲存桶
- 對比直接上傳：避免跨越多個公網躍點帶來的延遲與不穩定
- 費用：在標準 S3 費用外額外收取加速傳輸費用
適合全球分散使用者上傳大量資料至同一個 S3 儲存桶的場景。

---

## Questions (26–30)

(26) offers Lifecycle configuration for cost-optimal storage
Ans: Amazon Simple Storage Service (Amazon S3)

(27) can plug into a USB port on your computer
Ans: U2F security key

(28) correct about consolidated billing
Ans: AWS bills five instances as Reserved Instances, remaining four as regular instances / Bob receives cost-benefit from Susan's RIs only if he launches in the same AZ

(29) help you deploy application code automatically to an Amazon EC2 instance
Ans: AWS CodeDeploy

(30) use cases handled by AWS Lambda
Ans: AWS Lambda can be used for preprocessing data before storing in S3 / AWS Lambda can execute code in response to events such as updates to DynamoDB tables

---

(26)
中文題目：哪項 AWS 服務提供生命週期設定（Lifecycle Configuration）以實現最佳成本儲存？
答案：Amazon Simple Storage Service，Amazon S3
解析：**S3 Lifecycle Configuration** 可自動依時間將物件轉換至更低成本的儲存類別或自動刪除：
- **轉換動作（Transition Actions）**：如 30 天後移至 S3 Standard-IA，90 天後移至 S3 Glacier
- **到期動作（Expiration Actions）**：在指定天數後自動刪除物件或版本
典型的成本優化生命週期策略：S3 Standard → S3 Standard-IA → S3 Glacier Flexible Retrieval → S3 Glacier Deep Archive → 自動刪除，隨資料老化逐步降低儲存成本，無需人工介入。

(27)
中文題目：哪種 MFA 裝置可插入電腦的 USB 埠使用？
答案：U2F Security Key（U2F 安全金鑰）
解析：AWS 支援的 MFA 類型比較：
- **Virtual MFA**：手機 App（Google Authenticator），無需實體裝置
- **U2F Security Key**：實體 USB/NFC 安全金鑰（如 YubiKey），**插入 USB 埠**按觸即可驗證，符合 FIDO U2F 標準
- **Hardware MFA device**：專用硬體金鑰卡（如 Gemalto Token），顯示動態數字驗證碼
- **FIDO2 Passkey**：最新標準，支援生物辨識
題目關鍵字「plug into a USB port（插入 USB 埠）」直接對應 U2F Security Key。

(28)
中文題目：關於 AWS 合併帳單（Consolidated Billing），哪些描述是正確的？
答案：
- AWS 將五個執行個體計為 Reserved Instances，剩餘四個以一般費率計費
- Bob 只有在與 Susan 購買 RI 的**相同 AZ** 中啟動執行個體，才能享受 RI 的費用優惠
解析：**Consolidated Billing RI 共享規則**：
- 組織內若有成員購買了 RI 但未完全使用，**剩餘的 RI 折扣可自動套用至其他成員帳戶的相符執行個體**
- **Standard RI**：折扣只套用至**相同 AZ**內啟動的執行個體（AZ-specific）
- **Regional RI**：折扣套用至整個 Region，更靈活
例：Susan 購買 5 個 RI，Bob 在相同 AZ 啟動 9 個執行個體 → 5 個享 RI 折扣，4 個以 On-Demand 計費。

(29)
中文題目：哪項 AWS 服務可協助自動將應用程式程式碼部署至 Amazon EC2 執行個體？
答案：AWS CodeDeploy
解析：**AWS CodeDeploy** 是全受管的自動化部署服務：
- 支援部署至 **EC2 執行個體**、**On-Premises 伺服器**、**Lambda 函數**、**ECS 服務**
- 提供多種部署策略：In-Place（原地更新）、Blue/Green（藍綠部署）
- 最小化部署期間的停機時間
- 與 CodePipeline、GitHub、Bitbucket 整合，實現 CI/CD 流水線
是 AWS Developer Tools 系列（CodeCommit、CodeBuild、CodeDeploy、CodePipeline）中專責部署的服務。

(30)
中文題目：哪些使用案例可由 AWS Lambda 處理？
答案：
- Lambda 可用於在資料儲存至 S3 之前進行預處理
- Lambda 可在 DynamoDB 資料表更新等事件觸發時執行程式碼
解析：**AWS Lambda 事件驅動架構的典型應用**：
- **S3 資料預處理**：圖片上傳 S3 時觸發 Lambda 進行壓縮、格式轉換、中繼資料提取後再儲存
- **DynamoDB Streams 觸發**：資料表的增刪改操作觸發 Lambda 進行下游通知、資料同步、稽核日誌
Lambda 支援數十種 AWS 服務作為觸發器（Event Source），是事件驅動架構的核心元件。

---

## Questions (31–35)

(31) selecting the right resource types and sizes based on workload requirements
Ans: Performance Efficiency（效能效率）

(32) convert English language subtitles into Spanish
Ans: Amazon Translate

(33) for load-balancing HTTP and HTTPS traffic
Ans: Application Load Balancer（應用程式負載平衡器）

(34) Shared Responsibility Model — responsibility of AWS
Ans: Patching networking infrastructure（修補網路基礎設施）

(35) customer responsibilities for AWS IAM in the Shared Responsibility Model
Ans: Analyze user access patterns and review AWS IAM permissions / Enable MFA on all accounts

---

(31)
中文題目：AWS Well-Architected Framework 的哪個支柱關注根據工作負載需求選擇正確的資源類型與大小？
答案：Performance Efficiency（效能效率）
解析：**Performance Efficiency 支柱**的核心設計原則：
- **選擇正確的資源類型與大小（Right-Sizing）**：根據工作負載特性選擇最合適的 EC2 類型、資料庫引擎、儲存類別
- 隨技術演進持續更新架構，採用新服務與功能
- 使用 CloudWatch 監控效能指標，做出有依據的調整決策
- **AWS Compute Optimizer** 是此支柱的核心工具，提供 Right-Sizing 建議
Right-Sizing 是 Performance Efficiency 而非 Cost Optimization 的主要考量——先確保效能符合需求，再優化成本。

(32)
中文題目：哪項 AWS 服務可將英文字幕轉換為西班牙文？
答案：Amazon Translate
解析：**Amazon Translate** 是神經機器翻譯（Neural Machine Translation）服務：
- 支援 75+ 種語言之間的高品質翻譯
- 透過 API 即時翻譯文字內容
- 適用於字幕翻譯、網站本地化、客服多語言支援
與其他語言服務比較：
- **Amazon Transcribe**：語音轉文字（Speech to Text）
- **Amazon Polly**：文字轉語音（Text to Speech）
- **Amazon Translate**：文字語言翻譯（Translation）
- **Amazon Comprehend**：自然語言理解（情感分析、實體識別）

(33)
中文題目：哪種負載平衡器適合 HTTP 與 HTTPS 流量的負載平衡？
答案：Application Load Balancer，ALB（應用程式負載平衡器）
解析：AWS 提供三種負載平衡器：
- **ALB（Application Load Balancer）**：**第 7 層（應用層）**，專為 HTTP/HTTPS 設計，支援路徑路由、主機路由、標頭路由，適合微服務與容器架構
- **NLB（Network Load Balancer）**：第 4 層（傳輸層），超高效能 TCP/UDP，適合低延遲、高吞吐量場景
- **CLB（Classic Load Balancer）**：舊世代，支援第 4/7 層，已逐漸淘汰
題目關鍵字「HTTP and HTTPS traffic」明確對應 ALB。

(34)
中文題目：在 AWS 共同責任模型中，哪項屬於 AWS 的責任？
答案：修補網路基礎設施（Patching networking infrastructure）
解析：**AWS 負責（Security OF the Cloud）**的項目：
- 實體資料中心的網路設備（路由器、交換器、防火牆）的安裝、維護與**修補**
- AWS 骨幹網路基礎設施的安全性
- Hypervisor 修補
- 受管服務（RDS、Lambda 等）底層 OS 的修補
客戶負責的是：Guest OS（EC2 上）的修補、應用程式層的安全設定。網路基礎設施屬於 AWS 管理的底層硬體，完全由 AWS 負責修補。

(35)
中文題目：在 AWS 共同責任模型中，哪些是客戶對 AWS IAM 的責任？
答案：分析使用者存取模式並審查 IAM 權限 / 為所有帳戶啟用 MFA
解析：**IAM 的共同責任劃分**：
- **AWS 負責**：IAM 服務本身的可用性、底層基礎設施安全
- **客戶負責**：
  - **定期審查 IAM 權限**：確保使用者與角色遵循最小權限原則，移除不必要的存取
  - **分析存取模式**：使用 IAM Access Analyzer、Credential Report 識別過度授權
  - **啟用 MFA**：為所有 IAM 使用者（尤其是具有高權限的帳戶）啟用多因素驗證
IAM 的設定與管理完全屬於客戶責任範疇。

---

## Questions (36–40)

(36) EC2 Spot Instances are a best-fit for
Ans: Running containerized workloads with Amazon ECS that can be interrupted

(37) set up EC2 instances across two AWS Regions
Ans: Deploying across two AWS Regions improves availability

(38) in a disaster, they can run on fewer instances for some time
Ans: Warm Standby strategy

(39) AWS Marketplace facilitates which use-cases
Ans: Sell Software as a Service (SaaS) solutions to AWS customers / AWS customers can buy software bundled into customized AMIs by Marketplace sellers

(40) used to set up billing alarms to monitor estimated charges on your AWS account
Ans: Amazon CloudWatch

---

(36)
中文題目：EC2 Spot Instance 最適合哪種使用場景？
答案：使用 Amazon ECS 執行可以被中斷的容器化工作負載
解析：**Spot Instance 的適用原則**：適合**可容忍中斷**的工作負載，以換取最高 90% 的折扣：
- ECS 容器化的批次處理任務（資料分析、影像渲染）
- CI/CD 測試工作
- 機器學習訓練任務
- 大數據處理（EMR）
**不適合**：需要持續運行的生產資料庫、有狀態應用、關鍵業務服務
ECS 與 Spot 的結合透過 ECS 的任務重新排程機制，在 Spot 被回收時自動將任務遷移至其他執行個體，降低中斷影響。

(37)
中文題目：將 EC2 執行個體部署在兩個 AWS Region 中，這帶來哪項主要優勢？
答案：跨兩個 AWS Region 部署可提升**可用性（Availability）**
解析：跨 Region 部署的優勢：
- **高可用性**：若一個 Region 發生重大故障（自然災害、區域性中斷），另一個 Region 可繼續提供服務
- **災難復原（DR）**：實現最高等級的業務持續性（RTO/RPO 最低）
- **全球覆蓋**：降低不同地理位置使用者的存取延遲
搭配 **Route 53 Failover 路由**或 **Global Accelerator**，可實現跨 Region 的自動故障轉移。

(38)
中文題目：在災難發生時，企業可以在一段時間內以較少的執行個體運作，這是哪種災難復原策略？
答案：Warm Standby（暖備援）策略
解析：AWS 定義四種災難復原策略（由慢到快、由便宜到昂貴）：
1. **Backup & Restore**：備份資料，災難時重建環境，RTO/RPO 最長，成本最低
2. **Pilot Light**：僅保持核心服務（如資料庫）在備援 Region 運行，災難時快速擴展
3. **Warm Standby**：備援環境以**縮小規模**持續運行，災難時擴展至完整規模，**可在較少執行個體下運作一段時間**
4. **Multi-Site Active-Active**：兩個 Region 同時承載完整流量，RTO/RPO 最短，成本最高

(39)
中文題目：AWS Marketplace 支援哪些使用案例？
答案：
- 向 AWS 客戶銷售 SaaS 解決方案
- AWS 客戶可購買 Marketplace 賣家打包的自訂 AMI 軟體
解析：**AWS Marketplace** 作為數位軟體商城，支援：
- **ISV（獨立軟體廠商）視角**：可在 Marketplace 上架並銷售 SaaS 產品、AMI、容器映像、CloudFormation 範本
- **AWS 客戶視角**：可購買預先設定好軟體的**自訂 AMI**（一鍵啟動即包含所需軟體）、訂閱 SaaS 服務（費用合併至 AWS 帳單）
這讓軟體採購與部署更快速，且費用統一透過 AWS 帳單結算。

(40)
中文題目：哪項 AWS 服務可設定帳單警示（Billing Alarm）以監控 AWS 帳戶的預估費用？
答案：Amazon CloudWatch
解析：**AWS 帳單警示**的設定方式：
1. 在 **AWS Billing Console** 啟用「接收帳單警示（Receive Billing Alerts）」
2. 切換至 **us-east-1（N. Virginia）** Region（帳單指標僅儲存於此）
3. 在 **Amazon CloudWatch** 建立以 `EstimatedCharges` 為指標的警示
4. 設定閾值（如超過 $100），觸發 **SNS** 通知
注意：現在 AWS 也提供 **AWS Budgets** 作為更靈活的預算管理工具，但帳單警示的原始實作機制是 CloudWatch。

---

## Questions (41–45)

(41) allows AWS to offer lower pay-as-you-go prices
Ans: Massive economies of scale（大規模經濟效益）

(42) receive alerts when EC2 Reserved Instances utilization drops below a threshold
Ans: AWS Budgets

(43) status of credentials including passwords, access keys, and MFA devices
Ans: Credentials Report（憑證報告）

(44) are part of an Amazon VPC
Ans: Subnet / Internet Gateway

(45) provision the same AWS infrastructure across multiple AWS accounts and regions
Ans: AWS CloudFormation

---

(41)
中文題目：哪項因素讓 AWS 能夠提供更低廉的隨用隨付價格？
答案：Massive economies of scale（大規模經濟效益）
解析：**Economies of Scale（規模經濟）** 是 AWS 雲端優勢的核心：
- AWS 匯聚數百萬客戶的使用量，採購硬體、電力、頻寬的單位成本遠低於個別企業
- 隨著 AWS 規模持續擴大，每單位運算成本持續下降，這些節省**回饋給客戶**（AWS 歷史上多次主動降價）
- 個別企業自建資料中心無法達到相同的規模效益
這是 AWS 六大雲端優勢中「Benefit from massive economies of scale」的核心概念。

(42)
中文題目：哪項 AWS 服務可在 EC2 Reserved Instance 使用率低於特定閾值時發送警示？
答案：AWS Budgets
解析：**AWS Budgets — Reservation Budget** 專門用於監控 RI 使用情況：
- 設定 RI 使用率或覆蓋率（Coverage）閾值
- 當使用率低於閾值時（表示 RI 未被充分利用，浪費預付費用）自動發送警示
- 可透過 Email 或 SNS 通知
這幫助企業確保已購買的 RI 得到充分使用，最大化 RI 投資回報。若使用率持續過低，可考慮在 RI Marketplace 轉售或調整部署策略。

(43)
中文題目：哪份 AWS 報告顯示帳戶中憑證的狀態，包含密碼、Access Key 與 MFA 裝置？
答案：Credentials Report（IAM 憑證報告）
解析：**IAM Credentials Report** 是帳戶層級的安全稽核報告：
- 列出所有 IAM 使用者及其憑證狀態
- 包含：**密碼**（是否已設定、最後使用時間、最後變更時間）、**Access Key**（是否啟用、最後使用時間）、**MFA**（是否啟用）
- 可從 IAM Console 或 API 下載（CSV 格式）
- 每 4 小時更新一次
用於識別：未啟用 MFA 的使用者、長期未使用的憑證、需要輪換的舊 Access Key，是安全稽核的重要工具。

(44)
中文題目：哪些元件屬於 Amazon VPC 的組成部分？
答案：Subnet（子網路）/ Internet Gateway（網際網路閘道）
解析：**Amazon VPC** 的核心元件：
- **Subnet（子網路）**：VPC 內的 IP 位址範圍細分，分為 Public Subnet（可透過 IGW 存取網際網路）與 Private Subnet（無直接網際網路存取）
- **Internet Gateway（IGW）**：VPC 與公共網際網路的連接點，附加至 VPC 後，Public Subnet 的資源可與網際網路雙向通訊
- 其他 VPC 元件：Route Table、Security Group、Network ACL、NAT Gateway、VPC Endpoint

(45)
中文題目：哪項 AWS 服務可在多個 AWS 帳戶和 Region 中佈建相同的 AWS 基礎設施？
答案：AWS CloudFormation
解析：**AWS CloudFormation** 是基礎設施即程式碼（IaC）服務：
- 以 JSON 或 YAML 範本定義 AWS 資源
- 可在**任意帳戶與 Region**中重複部署相同的基礎設施（Stack）
- **CloudFormation StackSets** 特別支援跨多帳戶、跨 Region 的一次性大規模部署
- 確保環境一致性，防止設定漂移（Configuration Drift）
是實現「Infrastructure as Code」、多環境一致部署的核心工具。

---

## Questions (46–50)

(46) privately connect your VPC to Amazon SQS
Ans: VPC Interface Endpoint

(47) AWS Organizations provides which benefits
Ans: Volume discounts for EC2 and S3 aggregated across member accounts / Share reserved EC2 instances amongst member accounts

(48) connect to an EC2 instance from Mac OS, Windows, or Linux via a browser-based client
Ans: Amazon EC2 Instance Connect

(49) MOST cost-effective EC2 instance purchasing option for short-term, spiky and critical workloads
Ans: On-Demand Instance

(50) Amazon S3 storage classes that do not charge any data retrieval fee
Ans: Amazon S3 Standard / Amazon S3 Intelligent-Tiering

---

(46)
中文題目：哪項 AWS 功能可讓 VPC 私下連接至 Amazon SQS，不經過公共網際網路？
答案：VPC Interface Endpoint（VPC 介面端點）
解析：**VPC Endpoint** 分為兩種類型：
- **Gateway Endpoint**：支援 **S3** 與 **DynamoDB**，透過路由表，免費
- **Interface Endpoint（AWS PrivateLink）**：支援大多數其他 AWS 服務，包含 **SQS、SNS、EC2 API、KMS** 等，使用 ENI（Elastic Network Interface），需收費
SQS 不在 Gateway Endpoint 支援清單內，因此連接 SQS 需使用 **Interface Endpoint**，流量透過 AWS 私有網路，不經過公共網際網路。

(47)
中文題目：AWS Organizations 提供哪些優勢？
答案：
- EC2 與 S3 的使用量跨成員帳戶合併計算，享受批量折扣
- 成員帳戶之間共享預留的 EC2 執行個體（RI）
解析：**AWS Organizations 的財務優勢**：
- **合併帳單（Consolidated Billing）**：所有成員帳戶的使用量加總計算，達到更高的使用量階梯，享受更大的**批量折扣（Volume Discounts）**
- **RI 共享**：未完全使用的 Reserved Instance 折扣自動套用至其他成員帳戶的相符執行個體，最大化 RI 投資回報
- **Savings Plans 共享**：類似 RI，Savings Plans 也可在組織內共享

(48)
中文題目：如何從 Mac OS、Windows 或 Linux 電腦透過瀏覽器型用戶端連接至 EC2 執行個體？
答案：Amazon EC2 Instance Connect
解析：**Amazon EC2 Instance Connect** 提供：
- 透過 **AWS Management Console 網頁瀏覽器**直接 SSH 連接至 EC2 Linux 執行個體
- 不需要本地 SSH 用戶端或金鑰管理
- AWS 臨時性地將公開金鑰推送至執行個體，連線完成後自動移除
- 支援跨作業系統（任何可開啟瀏覽器的平台）
與 **Session Manager** 差異：Instance Connect 使用 SSH 協定，仍需開放 Port 22；Session Manager 完全不需要開放任何 Port。

(49)
中文題目：對於短期、突發且關鍵的工作負載，哪種 EC2 購買選項最符合成本效益？
答案：On-Demand Instance（隨需執行個體）
解析：此題三個條件的分析：
- **短期（Short-term）**：排除 Reserved Instance（需 1-3 年承諾）
- **突發（Spiky）**：流量不可預測，需要彈性擴縮
- **關鍵（Critical）**：不能被中斷，排除 Spot Instance
**On-Demand** 完全符合：無承諾、按需啟動、保證不中斷，是應對不可預測的關鍵短期工作負載的最佳選擇，雖然單價最高，但在此場景下最具成本效益。

(50)
中文題目：哪些 Amazon S3 儲存類別不收取資料取回費用？
答案：Amazon S3 Standard / Amazon S3 Intelligent-Tiering
解析：S3 各儲存類別的取回費用比較：
- **S3 Standard**：**無取回費用**，適合頻繁存取
- **S3 Intelligent-Tiering**：**無取回費用**（自動分層，但不收取取回費）
- **S3 Standard-IA**：收取每 GB 取回費用
- **S3 One Zone-IA**：收取每 GB 取回費用
- **S3 Glacier 系列**：收取取回費用，且依取回速度不同費率不同
需注意：S3 Intelligent-Tiering 雖有監控與自動化費用，但取回本身免費。

---

## Questions (51–55)

(51) forecast your AWS account usage and costs
Ans: AWS Cost Explorer

(52) be directly used with on-premises systems
Ans: Amazon Elastic File System（Amazon EFS）

(53) be used for an EC2 instance to access a DynamoDB table
Ans: IAM role

(54) compare the cost of running IT infrastructure on-premises vs AWS Cloud
Ans: AWS Pricing Calculator

(55) MOST cost-optimal EC2 deployment strategy
Ans: Use Spot Instances for ad-hoc jobs that can be interrupted / Use Reserved Instances (RI) for applications with predictable usage over the next one year

---

(51)
中文題目：哪項 AWS 服務可預測（forecast）你的 AWS 帳戶使用量與費用？
答案：AWS Cost Explorer
解析：**AWS Cost Explorer** 提供費用視覺化與預測功能：
- **歷史費用分析**：以圖表呈現過去費用趨勢，依服務、Region、標籤等維度分析
- **費用預測（Forecast）**：基於歷史使用模式，預測未來 12 個月的費用
- **Right-Sizing 建議**：識別低使用率的 EC2 執行個體，建議降級以節省費用
- **RI 購買建議**：分析使用模式，建議最優的 RI 購買方案
與 AWS Budgets 差異：Budgets 設定警示閾值；Cost Explorer 提供深度分析與預測視覺化。

(52)
中文題目：哪項 AWS 服務可直接與本地端（on-premises）系統搭配使用？
答案：Amazon Elastic File System，Amazon EFS
解析：**Amazon EFS** 支援跨環境存取：
- 透過 **AWS Direct Connect** 或 **AWS VPN**，本地端伺服器可使用 NFS 協定直接掛載 EFS 檔案系統
- 實現雲端與本地端共享同一個檔案系統，支援混合雲工作負載
- 適合：本地端應用程式需要存取雲端共享檔案、遷移過渡期間的混合存取
比較：EBS 只能掛載至 AWS 內的 EC2，無法直接用於本地端系統。

(53)
中文題目：EC2 執行個體需要存取 DynamoDB 資料表，應使用哪種 IAM 實體？
答案：IAM Role（IAM 角色）
解析：**IAM Role** 是 AWS 資源互相存取的標準授權機制：
- 將 IAM Role 附加至 EC2 執行個體（Instance Profile）
- EC2 自動取得臨時安全憑證（透過 STS），無需在程式碼或設定檔中硬寫 Access Key
- 臨時憑證自動輪換，安全性更高
- **最佳實踐**：AWS 服務之間的互相存取永遠使用 IAM Role，絕不使用硬寫的 Access Key
相比使用 IAM User Access Key：Role 的臨時憑證自動過期，不存在長期憑證洩露風險。

(54)
中文題目：哪項 AWS 工具可比較在本地端與 AWS Cloud 上運行 IT 基礎設施的費用？
答案：AWS Pricing Calculator
解析：**AWS Pricing Calculator** 的使用場景：
- 選擇 AWS 服務與配置，估算每月 AWS 費用
- 與本地端 IT 基礎設施的 TCO（總持有成本）進行比較分析
- 產生可分享的估算報告（URL 連結）
- 支援多服務組合的整體架構費用估算
常與 **AWS TCO Calculator**（已整合入 Pricing Calculator）搭配，幫助企業量化遷移至 AWS 的財務效益。

(55)
中文題目：哪種 EC2 部署策略最符合成本效益？
答案：
- 臨時性可中斷工作使用 Spot Instance
- 可預測的長期工作負載使用 Reserved Instance（RI）
解析：**混合購買策略**是最佳成本優化實踐：
- **Spot Instance**：用於批次處理、CI/CD、資料分析等**可中斷、非持續性**任務，節省最高 90%
- **Reserved Instance（RI）**：用於 Web 伺服器、資料庫等**持續運行、使用量可預測**的核心工作負載，節省最高 72%
- **On-Demand**：用於突發的**不可中斷且短期**的任務
三種選項組合使用，讓成本優化效益最大化，避免過度依賴單一計費模式。

---

## Questions (56–60)

(56) provide alerts on which common security misconfigurations
Ans: When you allow public access to Amazon S3 buckets / When you don't turn on user activity logging (AWS CloudTrail)

(57) a perspective of the AWS Cloud Adoption Framework (AWS CAF)
Ans: Business

(58) host a static website with the LEAST effort
Ans: Amazon Simple Storage Service (Amazon S3)

(59) run a bootstrap script while launching an Amazon EC2 instance
Ans: Amazon EC2 instance user data

(60) always has the right amount of capacity to handle the current traffic demand
Ans: Amazon EC2 Auto Scaling

---

(56)
中文題目：哪項 AWS 服務可針對常見安全設定錯誤提供警示？
答案：
- 允許 Amazon S3 儲存桶公開存取時
- 未開啟使用者活動日誌（AWS CloudTrail）時
解析：**AWS Trusted Advisor** 的「安全性」類別會檢查並警示：
- **S3 公開存取**：偵測已設定公開讀取或寫入的 S3 儲存桶，標記為安全風險
- **CloudTrail 未啟用**：若帳戶未開啟 CloudTrail，無法稽核 API 操作，屬於重大安全缺口
其他 Trusted Advisor 安全檢查項目：Root MFA 未啟用、安全群組開放過多 Port、IAM 使用者無 MFA 等。

(57)
中文題目：哪個是 AWS Cloud Adoption Framework（AWS CAF）的視角之一？
答案：Business（業務視角）
解析：**AWS CAF** 定義六大視角（Perspectives）：
- **Business（業務）**：雲端策略與業務目標對齊
- **People（人員）**：組織文化變革與人才培養
- **Governance（治理）**：風險管理、合規、IT 財務管理
- **Platform（平台）**：技術架構與雲端平台建設
- **Security（安全性）**：資料保護與合規
- **Operations（營運）**：IT 服務管理與業務持續性
Business 視角聚焦於確保雲端投資能直接產生可衡量的業務成果。

(58)
中文題目：哪項 AWS 服務可以最少的工作量託管靜態網站？
答案：Amazon Simple Storage Service，Amazon S3
解析：**S3 靜態網站託管**的設定步驟極為簡單：
1. 建立 S3 儲存桶（名稱與網域一致）
2. 上傳 HTML、CSS、JS 等靜態檔案
3. 啟用「Static Website Hosting」功能
4. 設定 Bucket Policy 允許公開讀取
5. 取得 S3 網站端點 URL
無需伺服器、無需安裝 Web Server、無需管理基礎設施，是成本最低、設定最簡單的靜態網站託管方式，搭配 CloudFront 可進一步提升全球效能。

(59)
中文題目：如何在啟動 Amazon EC2 執行個體時執行初始化腳本（bootstrap script）？
答案：Amazon EC2 instance user data（EC2 執行個體使用者資料）
解析：**EC2 User Data** 是在執行個體首次啟動時自動執行的腳本：
- 在 EC2 啟動設定的「Advanced Details」中輸入 User Data
- 支援 Bash 腳本（Linux）或 PowerShell（Windows）
- 在執行個體**首次啟動**時以 root 權限執行一次
- 常見用途：安裝軟體、設定環境變數、下載應用程式、啟動服務
例如：自動安裝 Apache Web Server 並啟動服務，無需手動 SSH 登入操作。

(60)
中文題目：哪項 AWS 服務確保始終有適量的容量來處理當前的流量需求？
答案：Amazon EC2 Auto Scaling
解析：**Amazon EC2 Auto Scaling** 動態調整 EC2 執行個體數量：
- **流量增加時（Scale Out）**：自動新增執行個體，確保效能不下降
- **流量減少時（Scale In）**：自動移除多餘執行個體，避免資源浪費
- **確保最低執行個體數**：即使流量為零，也維持設定的最少執行個體數量（高可用性）
題目關鍵字「always has the right amount of capacity（始終有適量容量）」精確描述了 Auto Scaling 的核心價值——動態匹配供需。

---

## Questions (61–65)

(61) best practices for the AWS account root user
Ans: Enable MFA for the AWS account root user / Set up an IAM user with administrator permissions and do not use root user for administrative tasks

(62) Reserved Instance (RI) pricing is available for which AWS services
Ans: Amazon EC2 / Amazon RDS

(63) maintain the same data on S3 between production and multiple test accounts, retaining object metadata
Ans: Amazon S3 Replication

(64) provide access to different mobile devices with variations in firmware and OS versions
Ans: AWS Device Farm

(65) provide programmatic access (API Access) to AWS Support Center features
Ans: AWS Enterprise Support / AWS Business Support

---

(61)
中文題目：哪些是 AWS 帳戶 Root 使用者的最佳實踐？
答案：
- 為 AWS 帳戶 Root 使用者啟用 MFA
- 建立具有管理員權限的 IAM 使用者，不使用 Root 帳戶執行日常管理任務
解析：**Root 使用者安全最佳實踐**：
- **啟用 MFA**：Root 帳戶擁有最高權限（包含關閉帳戶、變更付款方式），必須使用 MFA 加強保護
- **不用 Root 日常操作**：建立具有 AdministratorAccess Policy 的 IAM 使用者，日常管理使用此 IAM 帳戶
- **Root 專用任務**：僅在必要時使用 Root，如：首次設定 IAM 管理員、變更帳戶電子郵件/密碼、啟用 MFA for Root、恢復 IAM 存取
- **不建立 Root Access Key**：如有需要應立即停用並刪除

(62)
中文題目：哪些 AWS 服務提供 Reserved Instance（RI）定價選項？
答案：Amazon EC2 / Amazon RDS
解析：支援 RI 預留定價的 AWS 服務：
- **Amazon EC2 RI**：預留運算容量，最高折扣 72%
- **Amazon RDS RI**：預留資料庫執行個體，折扣幅度與 EC2 類似
- 其他支援預留的服務：ElastiCache、OpenSearch、Redshift、DynamoDB（Reserved Capacity）
本題聚焦 EC2 與 RDS，是最常見的 RI 使用場景。RI 適合使用量穩定可預測的長期工作負載，透過預付承諾換取顯著折扣。

(63)
中文題目：企業需要在生產帳戶與多個測試帳戶之間維護相同的 S3 資料，且需保留物件 Metadata，應使用哪項功能？
答案：Amazon S3 Replication（S3 複寫）
解析：**Amazon S3 Replication** 提供跨帳號、跨 Region 的物件複寫：
- **Same-Region Replication（SRR）**：同 Region 跨帳號複寫（適合生產→測試帳戶）
- **Cross-Region Replication（CRR）**：跨 Region 複寫（適合災難復原、地理分散）
複寫時**完整保留物件 Metadata**（包含標籤、ACL、版本 ID、加密設定），確保測試環境與生產環境資料完全一致。啟用複寫需先開啟來源儲存桶的版本控制。

(64)
中文題目：哪項 AWS 服務可測試不同韌體版本與 OS 版本的行動裝置存取？
答案：AWS Device Farm
解析：**AWS Device Farm** 是雲端行動裝置測試平台：
- 提供實體 **iOS 與 Android 裝置**的遠端存取與自動化測試
- 涵蓋**多種韌體版本、OS 版本、螢幕尺寸**的真實裝置
- 支援自動化測試框架（Appium、XCUITest、Espresso）
- 可執行平行測試，同時在多台裝置上測試
- 無需自行購買與維護實體裝置庫
適合需要確保應用程式在多種裝置與 OS 版本上正常運作的行動 App 開發團隊。

(65)
中文題目：哪些 AWS Support 方案提供對 AWS Support Center 功能的程式化存取（API Access）？
答案：AWS Enterprise Support / AWS Business Support
解析：**AWS Support API** 允許透過程式化方式使用 Support Center 功能：
- 建立、管理、查詢 Support Case
- 查看 Trusted Advisor 結果
- 存取 Support Center 的完整功能
支援情況：
- **Basic Support**：不支援 Support API
- **Developer Support**：不支援 Support API
- **Business Support**：**支援 Support API**，可程式化存取
- **Enterprise Support**：**支援 Support API**，並有更高的 API 呼叫限制
此功能適合需要將 AWS Support 整合至企業 ITSM 系統或自動化運維流程的企業。