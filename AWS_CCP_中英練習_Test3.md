# AWS Cloud Practitioner【TEST03】

---

## Questions (1–5)

(1) to submit historical configurations
Ans: AWS Config

(2) Amazon EC2 instances as well as on-premises instances
Ans: AWS CodeDeploy

(3) hybrid cloud architecture wants to centralize server logs
Ans: Use Amazon CloudWatch Logs for both

(4) prefers no physical devices
Ans: Virtual MFA device

(5) offer block-level storage
Ans: Amazon Elastic Block Store (Amazon EBS) / Instance Store

---

(1)
中文題目：哪項 AWS 服務可提交與查閱資源的歷史組態記錄？
答案：AWS Config
解析：**AWS Config** 持續記錄 AWS 資源的組態狀態與變更歷史，功能包含：
- 建立資源組態的時間軸快照（Configuration Timeline）
- 評估資源是否符合自訂合規規則（Config Rules）
- 查詢「某時間點某資源的組態為何」
與 CloudTrail 差異：CloudTrail 記錄「誰執行了哪個 API 操作」；Config 記錄「資源本身的組態狀態如何隨時間變化」，兩者互補，共同支援稽核與合規需求。

(2)
中文題目：哪項 AWS 服務可同時將程式碼部署至 EC2 執行個體與本地端（on-premises）執行個體？
答案：AWS CodeDeploy
解析：**AWS CodeDeploy** 是全受管的程式碼部署服務，支援：
- **Amazon EC2 執行個體**：雲端環境部署
- **On-Premises 執行個體**：本地伺服器部署（安裝 CodeDeploy Agent）
- **AWS Lambda**：無伺服器函數部署
- **Amazon ECS**：容器服務部署
題目關鍵字「EC2 instances as well as on-premises instances」直接對應 CodeDeploy 跨環境部署的核心能力，是混合雲架構下統一部署流程的最佳選擇。

(3)
中文題目：一家採用混合雲架構的 IT 公司想要集中管理伺服器日誌，應使用哪項服務？
答案：對兩種環境皆使用 Amazon CloudWatch Logs
解析：**Amazon CloudWatch Logs** 可集中收集、儲存與分析日誌，支援：
- **EC2 執行個體**：安裝 CloudWatch Agent 自動傳送系統日誌與應用程式日誌
- **On-Premises 伺服器**：同樣安裝 CloudWatch Agent，即可將本地伺服器日誌傳送至相同的 Log Group
兩種環境使用統一平台，實現混合雲日誌集中管理，搭配 CloudWatch Logs Insights 可進行跨環境的查詢與分析。

(4)
中文題目：使用者偏好不使用實體裝置，應選擇哪種 MFA 類型？
答案：Virtual MFA device（虛擬 MFA 裝置）
解析：AWS 支援多種 MFA 類型：
- **Virtual MFA device（虛擬 MFA）**：使用手機 App（如 Google Authenticator、Authy）產生 TOTP 動態驗證碼，**無需實體裝置**，免費且易於設定
- **Hardware MFA device（實體 MFA）**：專用硬體金鑰卡（如 Gemalto），需額外購買
- **FIDO Security Key**：實體 USB/NFC 安全金鑰（如 YubiKey）
題目關鍵字「no physical devices（不使用實體裝置）」對應 Virtual MFA，是最常見且低成本的 MFA 選擇。

(5)
中文題目：哪些 AWS 服務提供區塊層級儲存（block-level storage）？
答案：Amazon EBS / Instance Store
解析：區塊儲存將資料分割為固定大小的區塊，提供低延遲的隨機讀寫存取：
- **Amazon EBS（Elastic Block Store）**：持久性區塊儲存，可獨立於 EC2 存在，支援快照備份，適合資料庫、OS 磁碟
- **Instance Store（執行個體存放區）**：直接連接至主機實體硬體的臨時區塊儲存，效能極高但執行個體停止後資料消失，適合暫存快取
兩者皆使用區塊儲存介面，與物件儲存（S3）和檔案儲存（EFS）不同。

---

## Questions (6–10)

(6) CORRECT about AWS Auto Scaling group
Ans: Auto Scaling group scales out to match increased demand / Auto Scaling group scales in to match decreased demand

(7) for a flexible application that can be interrupted
Ans: Spot Instance

(8) use for active-passive configuration
Ans: Failover routing

(9) monitors malicious activity and detects threats
Ans: Amazon GuardDuty

(10) recommend for data archival
Ans: Amazon S3 Glacier Flexible Retrieval

---

(6)
中文題目：關於 AWS Auto Scaling 群組，哪些描述是正確的？
答案：
- Auto Scaling 群組在需求增加時**向外擴展（Scale Out）**，新增更多 EC2 執行個體
- Auto Scaling 群組在需求減少時**向內縮減（Scale In）**，減少 EC2 執行個體數量
解析：**AWS Auto Scaling** 的核心機制：
- **Scale Out（水平擴展）**：需求上升時自動新增執行個體，維持效能
- **Scale In（水平縮減）**：需求下降時自動移除多餘執行個體，節省成本
- 依 CloudWatch 指標（如 CPU 使用率）、排程或預測自動觸發
這確保資源供需動態平衡，是雲端彈性的核心體現。

(7)
中文題目：哪種 EC2 購買選項適合可容忍中斷的彈性應用程式？
答案：Spot Instance（競價執行個體）
解析：**EC2 Spot Instance** 利用 AWS 閒置運算容量，以最高省 90% 的折扣提供：
- AWS 可在 2 分鐘通知後隨時中斷執行個體（Spot Interruption）
- 適合**可容忍中斷**的工作負載：批次處理、大數據分析、CI/CD、機器學習訓練、影像渲染
- 不適合：需要持續運行的生產資料庫、關鍵業務應用
題目關鍵字「flexible + can be interrupted（可中斷）」直接對應 Spot Instance。

(8)
中文題目：哪種 Route 53 路由政策適用於主動-被動（active-passive）配置？
答案：Failover routing（容錯移轉路由）
解析：**Failover routing** 設定主要（Primary）與次要（Secondary）端點：
- 正常情況下流量路由至**主要端點（active）**
- Route 53 Health Check 偵測到主要端點失敗時，自動切換至**次要端點（passive）**
- 次要端點通常為備援站點或靜態 S3 錯誤頁面
這是 active-passive 高可用架構的標準實作方式，確保主要資源失效時服務不中斷。

(9)
中文題目：哪項 AWS 服務可監控惡意活動並偵測安全威脅？
答案：Amazon GuardDuty
解析：**Amazon GuardDuty** 是 AI 驅動的威脅偵測服務，持續分析：
- **AWS CloudTrail 事件**：異常 API 呼叫、未授權存取
- **VPC Flow Logs**：可疑的網路流量模式
- **DNS 日誌**：與惡意網域的通訊
- **S3 資料事件**：異常資料存取行為
自動偵測加密貨幣挖礦、憑證洩露、資料外洩等威脅，完全受管，無需部署任何 Agent。

(10)
中文題目：哪種 AWS 儲存服務適合資料封存（data archival）？
答案：Amazon S3 Glacier Flexible Retrieval
解析：S3 Glacier 系列專為長期封存設計：
- **S3 Glacier Instant Retrieval**：毫秒存取，適合偶爾需要快速存取的封存資料
- **S3 Glacier Flexible Retrieval**：取回時間 1 分鐘至 12 小時可選，是**標準封存**的最佳平衡選擇，成本低廉
- **S3 Glacier Deep Archive**：取回時間 12-48 小時，成本最低，適合 7-10 年以上的合規封存
Flexible Retrieval 在成本與存取彈性之間取得最佳平衡，是一般資料封存的首選。

---

## Questions (11–15)

(11) required to launch an Amazon EC2 instance
Ans: Amazon Machine Image (AMI)

(12) improves availability for a fleet of EC2 instances
Ans: Deploy EC2 instances across different AZs in the same AWS Region

(13) AWS CAF perspective that addresses strategy management
Ans: Business Perspective

(14) specialize in data migration from on-premises to AWS Cloud
Ans: AWS Snowball / AWS Database Migration Service (AWS DMS)

(15) most frequent questions from AWS customers and AWS provided solutions
Ans: AWS Knowledge Center

---

(11)
中文題目：啟動 Amazon EC2 執行個體時必須指定哪項元素？
答案：Amazon Machine Image，AMI（Amazon 機器映像）
解析：**Amazon Machine Image（AMI）** 是 EC2 執行個體的模板，包含：
- 作業系統（Windows、Linux 等）
- 預先安裝的應用程式與設定
- 根磁碟區快照
啟動 EC2 時，AMI 是唯一必須指定的元素（其他如執行個體類型、安全群組有預設值）。AMI 分為：AWS 提供的公有 AMI、AWS Marketplace AMI、自訂 AMI（由客戶從現有執行個體建立）。

(12)
中文題目：哪種做法可提升一組 EC2 執行個體的可用性？
答案：在同一 AWS Region 的不同 AZ 中部署 EC2 執行個體
解析：**跨 AZ 部署**是實現高可用性的核心策略：
- 每個 AZ 是獨立的故障域，擁有獨立電力、冷卻、網路
- 將執行個體分散至不同 AZ，確保單一 AZ 故障不影響整體服務
- 搭配 **Elastic Load Balancing** 將流量分散至多 AZ 的執行個體
- 搭配 **Auto Scaling Group** 在多 AZ 間自動維持執行個體數量
這是 AWS 高可用性架構的基本原則。

(13)
中文題目：AWS Cloud Adoption Framework（CAF）的哪個視角涵蓋策略管理（strategy management）？
答案：Business Perspective（業務視角）
解析：**AWS CAF Business Perspective** 關注雲端投資如何與業務目標對齊，核心能力包含：
- **策略管理（Strategy Management）**：制定雲端策略，確保 IT 與業務目標一致
- 投資組合管理、產品管理、業務洞察
- 資料變現、業務敏捷性
主要利害關係人：CEO、CFO、COO、CIO、業務分析師。Business Perspective 確保雲端轉型能直接創造業務價值。

(14)
中文題目：哪些 AWS 服務專門協助將資料從本地端遷移至 AWS Cloud？
答案：AWS Snowball / AWS Database Migration Service，AWS DMS
解析：
- **AWS Snowball**：實體資料傳輸裝置，適合大量資料（TB 至 PB 級）的離線遷移，在頻寬不足或資料量過大時使用，資料載入裝置後寄回 AWS 匯入
- **AWS DMS（Database Migration Service）**：線上資料庫遷移服務，支援同質性（MySQL → MySQL）與異質性（Oracle → Aurora）資料庫遷移，遷移期間來源資料庫持續運作，停機時間最短

(15)
中文題目：哪個 AWS 資源收錄了客戶最常見問題及 AWS 提供的解決方案？
答案：AWS Knowledge Center（AWS 知識中心）
解析：**AWS Knowledge Center** 是 AWS 官方維護的問答知識庫，包含：
- 客戶最常提出的技術問題
- AWS 官方提供的詳細解答與最佳實踐
- 按服務分類，易於搜尋
與其他資源比較：
- **AWS Documentation**：完整服務文件
- **AWS re:Post**：社群問答平台
- **Knowledge Center**：精選高頻問題與官方解答
是快速解決常見技術問題的第一站。

---

## Questions (16–20)

(16) store multiple copies of data in geographically distant locations
Ans: Use S3 cross-region replication (S3 CRR)

(17) are regional in scope
Ans: AWS Lambda / Amazon Rekognition

(18) search through old patents and documents (PDFs, Word, Text files)
Ans: Amazon Kendra

(19) Shared Responsibility Model — customer's responsibility
Ans: Maintain versions of an AWS Lambda function

(20) data encryption automatically enabled
Ans: Amazon S3 / AWS Storage Gateway

---

(16)
中文題目：如何將資料的多份副本儲存在地理位置遙遠的不同地點？
答案：使用 S3 跨區域複寫（S3 Cross-Region Replication，CRR）
解析：**S3 CRR** 自動將 S3 儲存桶中的物件複寫至不同 AWS Region 的目標儲存桶：
- 確保資料在地理上分散，提升災難復原能力
- 滿足資料主權與合規要求（跨地理位置備份）
- 支援跨帳號複寫
- 複寫的物件保留其 ACL、標籤與加密設定
啟用 CRR 需先開啟來源與目標儲存桶的版本控制（Versioning）。

(17)
中文題目：哪些 AWS 服務屬於區域性範圍（regional scope）？
答案：AWS Lambda / Amazon Rekognition
解析：AWS 服務依範圍分類：
- **區域性（Regional）**：Lambda、Rekognition、EC2、S3、RDS、VPC 等，資源部署於特定 Region
- **全球性（Global）**：IAM、CloudFront、Route 53、AWS Organizations，跨所有 Region 通用
Lambda 函數與 Rekognition 的資源（如模型端點）皆屬於特定 Region，在不同 Region 需分別部署，是常見的 Regional 服務考題。

(18)
中文題目：哪項 AWS 服務可搜尋舊有專利和文件（PDF、Word、文字檔）？
答案：Amazon Kendra
解析：**Amazon Kendra** 是機器學習驅動的企業智慧搜尋服務：
- 支援非結構化文件：PDF、Word、HTML、文字檔、PowerPoint 等
- 理解自然語言查詢，提供精確的文件級與段落級搜尋結果（而非關鍵字匹配）
- 可連接多種資料來源：S3、SharePoint、Confluence、資料庫
- 適合企業知識管理、法律文件搜尋、專利查詢等場景

(19)
中文題目：在 AWS 共同責任模型中，哪項屬於客戶的責任？
答案：維護 AWS Lambda 函數的版本（Maintain versions of an AWS Lambda function）
解析：Lambda 的責任劃分：
- **AWS 負責**：底層運算基礎設施、執行環境（Runtime）的安裝與修補、OS 維護
- **客戶負責**：函數程式碼、**版本管理（Versioning）**、環境變數、執行角色（IAM Role）、觸發器設定、記憶體與逾時配置
Lambda 版本與別名（Alias）管理是客戶端的業務邏輯控制，屬於客戶責任範疇。

(20)
中文題目：哪些 AWS 服務預設自動啟用資料加密？
答案：Amazon S3 / AWS Storage Gateway
解析：
- **Amazon S3**：自 2023 年起，所有新上傳至 S3 的物件預設使用 SSE-S3（AES-256）加密，無需額外設定
- **AWS Storage Gateway**：傳輸至 AWS 的資料預設使用 SSL/TLS 加密，儲存於 AWS 後亦自動加密
常見誤解：EBS Volume 預設不加密（可在帳戶層級開啟預設加密）；RDS 加密需在建立時手動啟用。

---

## Questions (21–25)

(21) correct regarding Amazon EFS
Ans: EC2 instances can access files on an EFS file system across many AZs, Regions and VPCs

(22) security assessments on its own AWS infrastructure without prior AWS approval
Ans: Penetration Testing（滲透測試）

(23) a part of the AWS Global Infrastructure
Ans: AWS Region

(24) static website on S3 but still inaccessible
Ans: Fix the Amazon S3 bucket policy

(25) receive separate invoices for development
Ans: Create separate AWS accounts for each environment

---

(21)
中文題目：關於 Amazon EFS，哪個描述是正確的？
答案：EC2 執行個體可跨多個 AZ、Region 與 VPC 存取 EFS 檔案系統上的檔案
解析：**Amazon EFS** 的存取範圍：
- **跨 AZ**：EFS 自動跨多個 AZ 冗餘儲存，同 Region 內任何 AZ 的 EC2 均可透過 Mount Target 掛載
- **跨 VPC**：透過 VPC Peering 或 Transit Gateway 可從其他 VPC 存取
- **跨 Region**：透過 AWS Direct Connect 或 VPN 可從其他 Region 或本地環境存取
這是 EFS 相較於 EBS 的核心優勢——共享式多點存取架構。

(22)
中文題目：企業可以在不事先取得 AWS 核准的情況下，對自己的 AWS 基礎設施進行哪種安全評估？
答案：Penetration Testing（滲透測試）
解析：AWS 允許客戶對**自己擁有的**部分 AWS 資源進行滲透測試，**無需事先申請許可**，支援的服務包含：EC2、NAT Gateway、ELB、RDS、CloudFront、API Gateway、Lambda、Lightsail 等。但以下行為**禁止**：
- DNS Zone Walking
- DDoS 攻擊模擬
- Port/Protocol/Request Flooding
若測試涉及 AWS 基礎設施本身（而非客戶資源），則需事先通知 AWS。

(23)
中文題目：哪項是 AWS 全球基礎設施（AWS Global Infrastructure）的組成部分？
答案：AWS Region（AWS 區域）
解析：**AWS 全球基礎設施**的層次結構：
- **AWS Region**：地理區域，如 us-east-1、ap-northeast-1，每個 Region 由多個 AZ 組成，彼此完全隔離
- **Availability Zone（AZ）**：Region 內的獨立故障域，由一或多個資料中心組成
- **Edge Location / Points of Presence**：CloudFront、Route 53 等全球邊緣服務的部署節點
- **Local Zones / Wavelength Zones**：延伸至特定都市或電信網路的基礎設施
Region 是 AWS 全球基礎設施的核心組織單位。

(24)
中文題目：企業在 S3 上部署了靜態網站，但網站仍無法存取，應如何解決？
答案：修正 Amazon S3 儲存桶政策（Bucket Policy）
解析：S3 靜態網站常見的無法存取原因：
- **Bucket Policy 未設定公開讀取權限**：需新增允許所有人（Principal: *）執行 s3:GetObject 的政策
- **Static Website Hosting 未啟用**：需在 S3 Console 開啟靜態網站託管功能，設定首頁（Index Document）
- **Block Public Access 設定**：若帳戶或儲存桶層級的 Block Public Access 未關閉，即使設定了 Bucket Policy 也無效
最常見原因是 Bucket Policy 缺少公開讀取授權。

(25)
中文題目：企業希望為開發、測試、生產等不同環境收到分開的帳單，應如何設定？
答案：為每個環境建立獨立的 AWS 帳戶
解析：**每個 AWS 帳戶獨立計費**，是環境隔離的最佳實踐：
- 不同帳戶的費用完全分開，各自收到獨立帳單
- 搭配 **AWS Organizations** 可同時實現帳戶隔離與合併帳單（視需求選擇）
- 帳戶隔離也提供更強的安全邊界——一個環境的資源無法意外影響另一環境
如果只想追蹤成本而不需要完全隔離，可使用**成本分配標籤（Cost Allocation Tags）**作為替代方案。

---

## Questions (26–30)

(26) will alert you and provide remedial action
Ans: AWS Health Dashboard — Your account health

(27) use to privately connect your VPC to Amazon S3
Ans: VPC Endpoint

(28) the highest possible discount for Reserved Instances (RI)
Ans: 72%

(29) best suited for Amazon EFS Standard-Infrequent Access (EFS Standard-IA)
Ans: Storing files in an accessible location to satisfy audit requirements

(30) move IT resources from US AWS Region to European AWS Region
Ans: Start creating new resources in the destination Region, then migrate relevant data and applications

---

(26)
中文題目：哪項 AWS 服務會針對影響你帳戶的事件發出警示並提供補救建議？
答案：AWS Health Dashboard — Your Account Health（帳戶健康儀表板）
解析：**AWS Health Dashboard — Your Account Health** 提供：
- 針對**你的帳戶**的個人化健康狀態通知
- AWS 排程維護、服務中斷、帳戶層級的合規問題警示
- **補救建議（Remedial Actions）**：提供具體的修復步驟或建議動作
- 可透過 EventBridge 設定自動化回應
與 Service Health Dashboard 差異：後者顯示所有服務的通用狀態，前者僅顯示影響你帳戶的特定事件，並提供行動指引。

(27)
中文題目：哪項 AWS 服務可讓 VPC 私下連接至 Amazon S3，不經過公共網際網路？
答案：VPC Endpoint（VPC 端點）
解析：**VPC Endpoint** 讓 VPC 內的資源可透過 AWS 私有網路存取 AWS 服務，流量不經過公共網路：
- **Gateway Endpoint**：支援 **S3** 與 **DynamoDB**，透過路由表設定，**免費**
- **Interface Endpoint（PrivateLink）**：支援其他大多數 AWS 服務，使用 ENI，需收費
連接 S3 使用 **Gateway Endpoint**，是最常見且免費的私有連線方式，可降低安全風險並減少 NAT Gateway 費用。

(28)
中文題目：EC2 Reserved Instance 最高可享有多少折扣？
答案：72%（相較於 On-Demand 價格）
解析：EC2 RI 折扣比較：
- **1 年期，No Upfront**：約 36% 折扣
- **1 年期，All Upfront**：約 40% 折扣
- **3 年期，No Upfront**：約 56% 折扣
- **3 年期，All Upfront**：最高約 **72%** 折扣
最高折扣條件：**3 年期 + 全額預付（All Upfront）+ Standard RI**。Spot Instance 雖可省更多（最高 90%），但有中斷風險，不在 RI 討論範疇。

(29)
中文題目：哪種使用場景最適合 Amazon EFS Standard-Infrequent Access（EFS Standard-IA）儲存類別？
答案：將檔案存放於可存取的位置以滿足稽核要求
解析：**Amazon EFS Standard-IA** 的設計定位：
- **低存取頻率**：儲存費用比 EFS Standard 低，適合不常存取的資料
- **立即可存取**：與 EFS Standard 相同的存取介面，無需等待（不同於 Glacier）
- **按存取計費**：每次讀寫時額外收取少量費用
稽核文件的特性：長期保存、鮮少讀取但需要時必須能立即取得，完全符合 EFS Standard-IA 的設計目標。

(30)
中文題目：企業想將 IT 資源從美國 AWS Region 遷移至歐洲 AWS Region，正確的做法為何？
答案：先在目的地 Region 建立新資源，再遷移相關資料與應用程式
解析：跨 Region 遷移的正確流程：
1. **在目的地 Region 建立新資源**：重新部署基礎設施（可使用 CloudFormation 範本加速）
2. **遷移資料**：使用 S3 CRR、DMS、DataSync 等工具將資料複製至新 Region
3. **測試與驗證**：確認新環境正常運作
4. **切換流量**：更新 DNS 或路由，逐步將流量切換至新 Region
5. **下線舊環境**：確認遷移完成後移除原 Region 資源
注意：AWS 資源無法跨 Region「移動」，必須在目的地 Region 重新建立。

---

## Questions (31–35)

(31) best practices for AWS IAM
Ans: Rotate credentials regularly / Enable MFA for all users

(32) used for online analytical processing (OLAP)
Ans: Amazon Redshift

(33) detailed reports that break down AWS costs by the hour to an S3 bucket
Ans: AWS Cost & Usage Report (AWS CUR)

(34) recommends maintaining infrastructure as code (IaC)
Ans: Operational Excellence（卓越營運）

(35) offers the lowest availability
Ans: Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)

---

(31)
中文題目：哪些是 AWS IAM 的最佳實踐？
答案：定期輪換憑證（Rotate credentials regularly）/ 為所有使用者啟用 MFA
解析：**AWS IAM 最佳實踐**核心原則：
- **定期輪換憑證**：定期更換 IAM 使用者的密碼與 Access Key，降低憑證洩露風險
- **為所有使用者啟用 MFA**：加入第二層驗證，即使密碼洩露也能防止未授權存取
- **最小權限原則（Least Privilege）**：只授予完成任務所需的最低權限
- **不使用 Root 帳戶進行日常操作**：Root 帳戶應立即啟用 MFA 並妥善保管
- **使用 IAM Role 取代 Access Key**：EC2 或 Lambda 應透過 Role 存取 AWS 資源

(32)
中文題目：哪項 AWS 服務用於線上分析處理（OLAP）？
答案：Amazon Redshift
解析：資料庫類型比較：
- **OLTP（Online Transaction Processing）**：處理即時交易，如訂單、庫存，對應 **RDS、Aurora、DynamoDB**
- **OLAP（Online Analytical Processing）**：大規模資料分析、商業智慧（BI）、報表，對應 **Amazon Redshift**
Redshift 是 AWS 的全受管雲端資料倉儲，採用列式儲存（Columnar Storage）與大規模平行處理（MPP），可快速對 PB 級資料執行複雜的分析查詢。

(33)
中文題目：哪項 AWS 服務可提供詳細的逐小時 AWS 費用明細報告並儲存至 S3？
答案：AWS Cost & Usage Report，AWS CUR
解析：**AWS Cost & Usage Report（CUR）** 是 AWS 最詳細的費用報告工具：
- 提供**逐小時（或逐日、逐月）**的費用與使用量明細
- 涵蓋每項 AWS 服務、每個資源的費用細目
- 自動將報告匯出至指定的 **S3 儲存桶**
- 可與 Amazon Athena、QuickSight、Redshift 整合進行深度分析
與 Cost Explorer 差異：Cost Explorer 提供視覺化儀表板；CUR 提供原始明細資料，適合自訂分析。

(34)
中文題目：AWS Well-Architected Framework 的哪個支柱建議維護基礎設施即程式碼（IaC）？
答案：Operational Excellence（卓越營運）
解析：**Operational Excellence 支柱**強調透過自動化和程式碼管理來提升營運效能，核心設計原則包含：
- **以程式碼執行操作（Perform operations as code）**：使用 CloudFormation、CDK 等 IaC 工具，使基礎設施可版本控制、可重複部署、可稽核
- 頻繁進行小型、可逆的變更
- 持續改進營運流程
IaC 是 Operational Excellence 的核心實踐，確保基礎設施一致性與可重複性。

(35)
中文題目：哪種 S3 儲存類別提供最低的可用性（availability）？
答案：Amazon S3 One Zone-Infrequent Access，S3 One Zone-IA
解析：S3 儲存類別可用性比較：
- **S3 Standard**：99.99% 可用性，跨 3+ AZ
- **S3 Standard-IA**：99.9% 可用性，跨 3+ AZ
- **S3 Intelligent-Tiering**：99.9% 可用性
- **S3 One Zone-IA**：**99.5% 可用性**，僅儲存於**單一 AZ**
S3 One Zone-IA 因為只使用一個 AZ，當該 AZ 發生故障時資料可能遺失，因此可用性最低，但儲存費用也最便宜，適合可重新生成的資料。

---

## Questions (36–40)

(36) on Docker and still wants access to the underlying servers
Ans: Amazon Elastic Container Service (Amazon ECS)

(37) restrict access from specific countries to comply with regional regulations
Ans: Amazon WAF

(38) components of an AWS Site-to-Site VPN
Ans: Virtual Private Gateway (VGW) / Customer Gateway

(39) AWS Lambda pricing is based on
Ans: Number of requests / Time it takes for the Lambda function to execute

(40) budget types that can be created under AWS Budgets
Ans: Cost budget / Usage budget / Reservation budget

---

(36)
中文題目：企業使用 Docker 容器，且仍需存取底層伺服器，應選擇哪項 AWS 服務？
答案：Amazon Elastic Container Service，Amazon ECS
解析：容器服務選擇比較：
- **Amazon ECS（EC2 launch type）**：在客戶管理的 EC2 執行個體上運行容器，客戶可完全存取與控制底層 OS 與伺服器
- **Amazon ECS（Fargate launch type）**：無伺服器，AWS 管理底層基礎設施，客戶無法存取伺服器
- **Amazon EKS**：受管 Kubernetes 服務，同樣支援 EC2 與 Fargate 啟動類型
題目關鍵字「still wants access to the underlying servers（仍需存取底層伺服器）」對應 **ECS EC2 launch type**。

(37)
中文題目：哪項 AWS 服務可封鎖來自特定國家的存取以符合地區法規？
答案：Amazon WAF（AWS Web Application Firewall）
解析：**AWS WAF** 支援**地理位置匹配規則（Geo Match Rule）**，可依使用者 IP 的地理位置：
- 封鎖特定國家或地區的所有請求
- 或僅允許特定國家的流量（白名單模式）
部署於 CloudFront、ALB、API Gateway 前端，是實現地理封鎖合規的最直接方式。也可使用 **CloudFront 地理限制（Geo Restriction）** 功能，但 WAF 提供更細粒度的規則控制。

(38)
中文題目：AWS Site-to-Site VPN 的組成元件為何？
答案：Virtual Private Gateway，VGW（虛擬私有閘道）/ Customer Gateway（客戶閘道）
解析：**AWS Site-to-Site VPN** 連線架構：
- **Virtual Private Gateway（VGW）**：AWS 端的 VPN 集中器，部署於 VPC 邊緣，是 AWS 端的 VPN 終端點
- **Customer Gateway（CGW）**：客戶端的 VPN 裝置或軟體，代表本地端路由器或防火牆的 AWS 資源物件
兩者之間建立加密的 IPSec 隧道，透過公共網際網路傳輸，實現本地網路與 VPC 的安全連線。每個 VPN 連線包含兩條隧道提供冗餘。

(39)
中文題目：AWS Lambda 的定價依據為何？
答案：請求次數（Number of requests）/ Lambda 函數的執行時間
解析：**AWS Lambda 計費模型**：
- **請求次數**：每百萬次請求收費（前 100 萬次免費，永久免費方案）
- **執行持續時間**：以毫秒計算，依記憶體配置與執行時間的乘積計費（GB-秒）
Lambda 閒置時不產生費用，只有實際執行時才計費，是最典型的按需付費模式，非常適合低頻或不規則的工作負載。

(40)
中文題目：AWS Budgets 支援建立哪些類型的預算？
答案：Cost budget（費用預算）/ Usage budget（使用量預算）/ Reservation budget（預留預算）
解析：**AWS Budgets** 四大預算類型：
- **Cost Budget**：監控實際或預測費用，超出閾值時發送警示
- **Usage Budget**：監控特定服務的使用量（如 EC2 小時數、S3 儲存量）
- **Reservation Budget**：監控 RI 或 Savings Plans 的使用率與覆蓋率
- **Savings Plans Budget**：監控 Savings Plans 的使用情況
每種預算類型皆可設定多個警示閾值，透過 Email 或 SNS 通知。

---

## Questions (41–45)

(41) innovate faster and rapidly develop, test and launch software applications
Ans: Agility（敏捷性）

(42) correct regarding AWS Shield Advanced pricing
Ans: AWS Shield Advanced offers protection against higher fees that could result from a DDoS attack

(43) execute code triggered by new files being uploaded to Amazon S3
Ans: AWS Lambda

(44) mandatory elements of an IAM policy
Ans: Effect / Action

(45) optimize caching for scientific computations on EC2 instances
Ans: Instance Store

---

(41)
中文題目：雲端讓企業能更快創新、快速開發、測試與推出軟體應用程式，這對應雲端的哪項優勢？
答案：Agility（敏捷性）
解析：**Agility** 是 AWS 六大雲端優勢之一：
- 可在幾分鐘內取得所需資源，而非等待數週採購硬體
- 降低實驗成本，鼓勵快速迭代與試錯
- 縮短從構想到上市（Time to Market）的時間
- 支援 DevOps 與 CI/CD 實踐，加速軟體交付週期
題目關鍵字「innovate faster + rapidly develop, test and launch」直接對應 Agility 的核心定義。

(42)
中文題目：關於 AWS Shield Advanced 定價，哪個描述是正確的？
答案：AWS Shield Advanced 提供保護，防止因 DDoS 攻擊而產生的額外費用
解析：**AWS Shield Advanced** 的費用保護機制：
- DDoS 攻擊期間，大量惡意流量可能導致 EC2、CloudFront、ELB 等資源的使用量暴增，進而產生巨額帳單
- Shield Advanced 提供**費用保護（Cost Protection）**：若因 DDoS 攻擊導致受保護資源的使用費用增加，AWS 會以服務積分（Credits）補償這些額外費用
這是 Shield Advanced 相較於 Standard 的重要差異之一，讓企業無需擔心 DDoS 攻擊帶來的財務風險。

(43)
中文題目：哪項 AWS 服務可在新檔案上傳至 Amazon S3 時觸發程式碼執行？
答案：AWS Lambda
解析：**S3 + Lambda** 是 AWS 最經典的事件驅動架構之一：
- 設定 **S3 Event Notification** 在物件上傳（PUT）時觸發 Lambda 函數
- Lambda 可接收事件資訊（儲存桶名稱、物件金鑰），執行後續處理
常見應用：圖片縮圖生成、文件格式轉換、資料驗證與處理、日誌分析
整個流程無伺服器、事件驅動、自動擴縮，是雲端原生設計的典型範例。

(44)
中文題目：IAM Policy 的哪些元素是必要（mandatory）的？
答案：Effect（效果）/ Action（動作）
解析：**IAM Policy JSON 結構**的必要與選用元素：
- **必要元素**：
  - **Effect**：Allow 或 Deny，指定允許或拒絕
  - **Action**：指定允許或拒絕的 AWS 服務動作（如 s3:GetObject）
- **常見但非絕對必要**：
  - **Resource**：指定動作的目標資源（ARN），若不指定則需使用 * 
  - **Principal**：指定政策套用的主體（用於 Resource-based Policy）
  - **Condition**：附加條件限制
Effect 與 Action 是構成有效 IAM Policy 陳述的最核心要素。

(45)
中文題目：企業需要為 EC2 上的科學運算優化快取效能，哪種儲存最合適？
答案：Instance Store（執行個體存放區）
解析：**Instance Store** 是優化快取的最佳選擇：
- 直接連接至主機實體硬體，提供**極低延遲與極高 I/O 吞吐量**
- 不額外收費（包含在執行個體費用中）
- 資料為暫存性（執行個體停止後消失），完全符合快取的特性
科學運算場景常需要高速暫存中間計算結果，Instance Store 的硬體級效能遠優於 EBS，是高效能計算快取的首選。

---

## Questions (46–50)

(46) correct regarding Amazon EFS and Amazon EBS pricing
Ans: EBS Snapshots are stored incrementally — billed only for changed blocks / You pay a fee each time you read from or write to EFS Standard-IA

(47) protect your data from accidental deletion on Amazon S3
Ans: Amazon S3 Versioning

(48) primary benefit of Amazon RDS in a Read Replica configuration
Ans: Read Replica improves database scalability（可擴展性）

(49) support High Availability by default
Ans: Amazon EFS / Amazon DynamoDB

(50) maintains separate VPCs for each department and wants to connect all VPCs
Ans: AWS Transit Gateway

---

(46)
中文題目：關於 Amazon EFS 與 Amazon EBS 的定價，哪些描述是正確的？
答案：
- EBS Snapshot 採增量儲存，只對變更的區塊收費
- 每次讀取或寫入 EFS Standard-IA 時需支付額外費用
解析：
- **EBS Snapshot 增量計費**：第一次快照為完整備份，後續快照只儲存與前一次不同的區塊，大幅降低儲存成本
- **EFS Standard-IA 存取費用**：EFS Standard-IA 儲存費用低，但每次 I/O 操作（讀取或寫入）需支付額外的存取費用，適合讀寫頻率低的資料；若頻繁存取，總費用可能高於 EFS Standard

(47)
中文題目：如何保護 Amazon S3 上的資料免於意外刪除？
答案：Amazon S3 Versioning（S3 版本控制）
解析：**Amazon S3 Versioning** 在同一儲存桶內保留物件的所有歷史版本：
- 「刪除」操作實際上是新增一個刪除標記（Delete Marker），原始版本仍保留
- 可隨時還原至任何歷史版本
- 防止意外覆寫或誤刪
進階保護：搭配 **S3 Object Lock（MFA Delete）** 可實現合規級別的防刪除保護，連管理員也無法刪除特定版本的物件。

(48)
中文題目：Amazon RDS Read Replica 配置的主要優勢為何？
答案：Read Replica 提升資料庫的可擴展性（Scalability）
解析：**RDS Read Replica** 的核心用途：
- 將**讀取流量**分散至多個唯讀複本，減輕主要執行個體的讀取壓力
- 支援跨 Region 的 Read Replica（降低讀取延遲）
- 最多可建立 5 個 Read Replica（Aurora 支援最多 15 個）
- 主要目的是**水平擴展讀取能力（Read Scalability）**
與 Multi-AZ 差異：Multi-AZ 的 Standby 不接受讀取，主要提供**高可用性**；Read Replica 提供**可擴展性**。

(49)
中文題目：哪些 AWS 服務預設支援高可用性（High Availability）？
答案：Amazon EFS / Amazon DynamoDB
解析：
- **Amazon EFS**：資料自動跨多個 AZ 冗餘儲存，單一 AZ 故障不影響資料可用性，預設 HA
- **Amazon DynamoDB**：資料自動在同一 Region 的多個 AZ 之間複寫，提供內建的高可用性與持久性
- **Amazon EC2**：單一執行個體預設不提供 HA，需搭配 Multi-AZ + ELB + Auto Scaling
- **Amazon RDS**：需手動啟用 Multi-AZ 才具備 HA，非預設

(50)
中文題目：企業為每個部門維護獨立的 VPC，並希望連接所有 VPC 以促進協作，應使用哪項服務？
答案：AWS Transit Gateway
解析：**AWS Transit Gateway** 是雲端網路的中央集線器（Hub）：
- 允許多個 VPC 透過單一閘道互相連接，形成星型（Hub-and-Spoke）拓撲
- 避免大量 VPC Peering 的管理複雜性（N 個 VPC 若兩兩 Peering 需 N×(N-1)/2 條連線）
- 同時支援 VPN 與 Direct Connect 連接，整合本地環境與多個 VPC
- 支援跨帳號、跨 Region 連接（Cross-Region Peering）
是大規模多 VPC 架構的最佳解決方案。

---

## Questions (51–55)

(51) Amazon Rekognition provides as a ready-to-use feature
Ans: Identify objects in a photo

(52) region-specific constraint that an AMI must meet for EC2
Ans: You must use an AMI from the same region as the EC2 instance; the region of the AMI has no bearing on performance

(53) used as an in-memory database with high-performance and low latency
Ans: Amazon ElastiCache

(54) CORRECT regarding security groups and network ACL
Ans: A security group is stateful / A network ACL contains a numbered list of rules evaluated in increasing order

(55) static website on S3 in Asia Region wants to improve global performance
Ans: Use Amazon CloudFront

---

(51)
中文題目：Amazon Rekognition 提供哪項開箱即用的功能？
答案：識別照片中的物件（Identify objects in a photo）
解析：**Amazon Rekognition** 的核心現成功能（無需訓練模型）：
- **物件與場景標記（Object & Scene Detection）**：識別照片中的物件、場景、活動
- 臉部偵測與分析（情緒、年齡範圍、眼鏡等屬性）
- 臉部比對與搜尋
- 不安全內容偵測（Moderation）
- 文字識別（OCR）
- 名人辨識
這些功能皆透過 API 呼叫即可使用，是典型的 AI/ML 即服務（AI as a Service）。

(52)
中文題目：AMI 在與 EC2 執行個體搭配使用時，必須滿足哪項區域限制？
答案：必須使用與 EC2 執行個體**相同 Region** 的 AMI；AMI 所在的 Region 對效能沒有影響
解析：**AMI 的區域限制**：
- AMI 是區域性（Regional）資源，只能在建立它的 Region 內啟動 EC2 執行個體
- 若要在其他 Region 使用，必須先**複製 AMI（Copy AMI）**至目標 Region
- AMI 的 Region 來源不影響執行個體效能，效能取決於執行個體類型與底層硬體
- 跨帳號共享 AMI 也受相同的 Region 限制

(53)
中文題目：哪項 AWS 服務用作高效能、低延遲的記憶體內資料庫（in-memory database）？
答案：Amazon ElastiCache
解析：**Amazon ElastiCache** 是全受管的記憶體快取服務，支援兩種引擎：
- **Redis**：支援豐富資料結構（List、Set、Hash）、持久化、主從複製、Multi-AZ 高可用、Pub/Sub
- **Memcached**：簡單高速的鍵值快取，支援多執行緒
常見應用：Session 管理、資料庫查詢結果快取、排行榜、即時分析，可將資料庫讀取延遲從毫秒降至微秒。

(54)
中文題目：關於 Security Group 與 Network ACL，哪些描述是正確的？
答案：
- Security Group 是**有狀態的（Stateful）**，自動允許回應流量
- Network ACL 包含**編號的規則清單**，按號碼由小到大依序評估
解析：

| 特性 | Security Group | Network ACL |
|------|----------------|-------------|
| 狀態 | **有狀態（Stateful）**：允許出站流量，對應的入站回應自動允許 | **無狀態（Stateless）**：入站與出站規則各自獨立評估 |
| 規則評估 | 所有規則一次評估 | **按號碼升冪順序**，第一條匹配即停止 |
| 規則類型 | 僅 Allow | Allow 與 Deny |
| 作用層級 | 執行個體 | 子網路 |

(55)
中文題目：企業在亞洲 Region 的 S3 上有一個靜態網站，想改善全球存取效能，應使用哪項服務？
答案：使用 Amazon CloudFront
解析：**Amazon CloudFront** 是 AWS 的全球 CDN（內容傳遞網路）：
- 在全球 400+ 個邊緣節點快取靜態內容（HTML、CSS、JS、圖片）
- 使用者從最近的邊緣節點取得內容，大幅降低延遲
- 與 S3 原生整合，設定 S3 為 Origin 即可
- 提供 HTTPS、壓縮、快取控制等優化功能
亞洲 S3 的內容透過 CloudFront 分發後，全球使用者皆可享受低延遲的存取體驗。

---

## Questions (56–60)

(56) responsibilities of the customer in the AWS Shared Responsibility Model
Ans: Operating system patches and updates of an EC2 instance / Managing IAM users and roles

(57) Which Cloud Computing model does Gmail represent
Ans: Software as a Service (SaaS)

(58) security service that falls under AWS's purview in the Shared Responsibility Model
Ans: AWS Shield Standard

(59) correct regarding the AWS Shared Responsibility Model
Ans: For abstracted services like S3, AWS operates the infrastructure layer, OS, and platforms / AWS is responsible for Security 'of' the Cloud

(60) identify all under-utilized EC2 instances without manual configurations
Ans: AWS Trusted Advisor / AWS Cost Explorer

---

(56)
中文題目：在 AWS 共同責任模型中，哪些屬於客戶的責任？
答案：EC2 執行個體的作業系統修補與更新 / 管理 IAM 使用者與角色
解析：**客戶責任（Security IN the Cloud）**包含：
- **OS 修補與更新**：EC2 是 IaaS，客戶完全負責 Guest OS 的安全更新
- **IAM 使用者與角色管理**：帳戶內的身份與存取管理完全由客戶負責
- 應用程式安全、資料加密、網路設定（Security Group、NACL）
- 客體資料（Customer Data）的保護
**AWS 責任**：硬體、Hypervisor、資料中心實體安全、受管服務的底層 OS

(57)
中文題目：Gmail 代表哪種雲端運算服務模型？
答案：Software as a Service，SaaS（軟體即服務）
解析：雲端服務三大模型：
- **IaaS（基礎設施即服務）**：EC2、Azure VM——提供虛擬基礎設施，客戶管理 OS 以上層級
- **PaaS（平台即服務）**：Elastic Beanstalk、Google App Engine——提供應用程式執行平台
- **SaaS（軟體即服務）**：**Gmail、Salesforce、Office 365、Amazon Rekognition**——完整的軟體應用，使用者只需使用功能，完全不需管理任何基礎設施
Gmail 使用者只需登入使用，不需管理伺服器、OS 或應用程式，是 SaaS 最典型的例子。

(58)
中文題目：在 AWS 共同責任模型中，哪項安全服務屬於 AWS 的責任範疇？
答案：AWS Shield Standard
解析：**AWS Shield Standard** 由 AWS 全權管理，自動保護所有 AWS 客戶：
- 防禦第 3/4 層 DDoS 攻擊
- 無需客戶設定或啟用，AWS 自動提供
- 屬於 AWS 對底層基礎設施安全的承諾
相比之下，**AWS WAF** 雖然是 AWS 提供的服務，但規則設定與管理是客戶的責任（設定哪些流量被允許或封鎖）。Shield Standard 的保護完全由 AWS 負責，是 AWS 責任範疇的安全服務。

(59)
中文題目：關於 AWS 共同責任模型，哪些描述是正確的？
答案：
- 對於 S3 等抽象服務，AWS 負責基礎設施層、OS 與平台的運作
- AWS 負責「雲端本身」的安全性（Security of the Cloud）
解析：共同責任模型的核心概念：
- **AWS 負責（Security OF the Cloud）**：實體設施、網路基礎設施、Hypervisor，以及受管服務（如 S3）的所有底層層級
- **客戶負責（Security IN the Cloud）**：在 AWS 提供的平台上運行的應用程式、資料、存取管理
- S3 是完全抽象的受管服務，客戶看不到也不需管理底層 OS，AWS 全權負責

(60)
中文題目：哪些 AWS 服務可在不需要手動設定的情況下，識別所有使用率過低的 EC2 執行個體？
答案：AWS Trusted Advisor / AWS Cost Explorer
解析：
- **AWS Trusted Advisor**：自動掃描 AWS 環境，在「成本優化」類別中提供低使用率 EC2 執行個體的建議，直接列出具體資源
- **AWS Cost Explorer**：分析費用與使用量數據，可識別閒置或低使用率的資源，並提供右型化（right-sizing）建議
兩者皆無需手動設定分析邏輯，是發現浪費資源的自動化工具。

---

## Questions (61–65)

(61) durable, cost-effective storage for historic data stored for 10 years for compliance
Ans: Amazon S3 Glacier Deep Archive

(62) true about Cost Allocation Tags in AWS Billing
Ans: Each tag key must be unique per resource, and each key can have only one value / Must activate both AWS generated tags and user-defined tags separately before they appear in Cost Explorer

(63) AWS Trusted Advisor analyzes and provides best practice recommendations for which categories
Ans: Cost Optimization / Service Limits

(64) move large volumes of on-premises data from a remote location with limited bandwidth
Ans: AWS Snowball

(65) billing metric data is stored in which AWS Region
Ans: US East (N. Virginia) — us-east-1

---

(61)
中文題目：哪項 AWS 服務可為需要保存 10 年的歷史合規資料提供耐久且符合成本效益的儲存？
答案：Amazon S3 Glacier Deep Archive
解析：**S3 Glacier Deep Archive** 是 AWS 成本最低的儲存類別，專為長期封存設計：
- 資料最低保存期限建議：**180 天**（計費考量）
- 取回時間：**12 至 48 小時**
- 提供 **99.999999999%（11 個 9）**的資料持久性
- 費用極低，適合法規要求的 7-10 年以上長期保存
合規封存場景通常不需要快速存取，Deep Archive 的超低成本完全符合「成本效益 + 長期保存 + 高耐久性」三項需求。

(62)
中文題目：關於 AWS 帳單中的成本分配標籤（Cost Allocation Tags），哪些描述是正確的？
答案：
- 每個資源的每個標籤鍵（Tag Key）必須唯一，且每個鍵只能有一個值
- 必須分別啟用 AWS 產生的標籤與使用者自訂標籤，它們才會出現在 Cost Explorer 中
解析：**Cost Allocation Tags** 的重要規則：
- **標籤唯一性**：同一資源上，相同的 Key 只能出現一次（每個 Key 對應一個 Value）
- **必須手動啟用**：在 AWS Billing Console 中，AWS 產生的標籤（如 aws:createdBy）與使用者自訂標籤需**分別**啟用，才能在 Cost Explorer 中用於成本分析
- 啟用後通常需要 24 小時才開始顯示

(63)
中文題目：AWS Trusted Advisor 分析 AWS 環境並提供哪些類別的最佳實踐建議？
答案：Cost Optimization（成本優化）/ Service Limits（服務限制）
解析：**AWS Trusted Advisor** 提供五大類別的最佳實踐建議：
1. **Cost Optimization（成本優化）**：識別閒置資源、RI 購買建議
2. **Performance（效能）**：提升服務效能的建議
3. **Security（安全性）**：安全設定漏洞偵測
4. **Fault Tolerance（容錯）**：提升高可用性的建議
5. **Service Limits（服務限制）**：監控接近 AWS 配額上限的資源
本題選項 Cost Optimization 與 Service Limits 皆為五大類別中的一部分。

(64)
中文題目：如何將大量本地端資料從頻寬有限的偏遠地點遷移至 AWS？
答案：AWS Snowball
解析：**AWS Snowball** 是實體資料傳輸裝置，適用於頻寬受限的資料遷移場景：
- 將資料載入 Snowball 裝置（容量 80TB 或 210TB）
- 實體寄送至 AWS 資料中心，由 AWS 直接匯入 S3
- 避免透過有限頻寬傳輸大量資料（可能需要數週或數月）
- 資料傳輸過程全程加密（AES-256）
判斷使用 Snowball 的原則：若網路傳輸完成資料遷移需要超過 1 週，Snowball 通常更有效率。

(65)
中文題目：AWS 的帳單指標資料（billing metric data）儲存在哪個 AWS Region？
答案：US East（N. Virginia）— us-east-1
解析：**us-east-1（美國東部，維吉尼亞北部）** 是 AWS 的核心 Region，多項全球性服務與資料集中於此：
- **帳單指標資料（Billing Metrics）**：所有 AWS 帳戶的 CloudWatch 帳單指標統一儲存於 us-east-1
- **IAM**：全球服務，但後端資料亦集中管理
- 設定帳單警示（Billing Alarm）時，CloudWatch Region 必須切換至 **us-east-1** 才能看到帳單相關指標
這是考試常考的細節，務必記住帳單資料 = us-east-1。