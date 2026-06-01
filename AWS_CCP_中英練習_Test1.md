# AWS Cloud Practitioner【TEST01】

(1) specific use-cases
Ans: Business
(2) choose how much traffic is routed
Ans: Weighted
(3) AWS account activity meets governance
Ans: CloudTrail
(4) have control over creating
Ans: Customer Managed Key (CMK)
(5) mitigate a Distributed Denial of Service (DDoS) attack
Ans: AWS Shield

---

(1)
中文題目：哪個 AWS Support 方案適合特定使用案例的企業需求？
答案：Business（商業方案）
解析：AWS Support 分為四個等級：Basic、Developer、Business、Enterprise。Business 方案提供 24/7 全天候電話、Email 及 Chat 技術支援，並包含 AWS Trusted Advisor 完整檢查、Health API 存取，以及針對特定使用情境（specific use-cases）提供指導建議，適合有生產環境工作負載的企業使用。Developer 方案僅提供 Email 支援；Enterprise 方案則針對大型關鍵任務企業，費用更高。

(2)
中文題目：哪種 Route 53 路由政策允許你選擇將多少流量導向特定資源？
答案：Weighted（加權路由）
解析：Amazon Route 53 提供多種路由政策：
- Simple（簡單）：單一資源，無特殊邏輯
- Weighted（加權）：依照設定的權重比例分配流量，例如 70% 流量到 A、30% 到 B，適合 A/B 測試或藍綠部署
- Latency（延遲）：依網路延遲最低的區域路由
- Failover（容錯移轉）：主要資源失敗時切換至備援
- Geolocation（地理位置）：依使用者所在地區路由

題目關鍵字「choose how much traffic」對應的就是 Weighted 路由政策。

(3)
中文題目：哪項 AWS 服務可協助確認 AWS 帳戶活動符合治理與合規要求？
答案：AWS CloudTrail
解析：AWS CloudTrail 是一項稽核與合規服務，會記錄所有 AWS 帳戶中的 API 呼叫與操作事件（誰在何時對哪個資源做了什麼），並將日誌儲存至 S3。常見的相似服務比較：
- CloudTrail：記錄「誰做了什麼操作」（API 層級稽核）
- CloudWatch：監控資源效能與指標
- AWS Config：持續評估資源設定是否符合規範
- GuardDuty：威脅偵測與異常行為分析

題目關鍵字「governance（治理）」與「account activity（帳戶活動）」直接對應 CloudTrail 的核心功能。

(4)
中文題目：哪種金鑰類型讓客戶對金鑰的建立、輪換與管理擁有完全控制權？
答案：Customer Managed Key，CMK（客戶自管金鑰）
解析：AWS KMS（Key Management Service）提供三種金鑰類型：
- AWS Managed Key（AWS 自管金鑰）：由 AWS 自動建立與管理，客戶無法控制輪換週期
- Customer Managed Key（CMK，客戶自管金鑰）：由客戶自行建立、定義使用政策（Key Policy）、控制輪換，彈性最高
- AWS Owned Key（AWS 擁有金鑰）：完全由 AWS 管理，客戶不可見也不可控

題目關鍵字「have control over creating（對建立擁有控制權）」明確指向 CMK。

(5)
中文題目：哪項 AWS 服務專門用來緩解分散式阻斷服務（DDoS）攻擊？
答案：AWS Shield
解析：AWS Shield 是專為防禦 DDoS 攻擊而設計的受管保護服務，分為兩個等級：
- Shield Standard（標準版）：免費，自動保護所有 AWS 客戶，防禦常見的第 3、4 層網路層攻擊
- Shield Advanced（進階版）：付費，提供更進階的第 7 層應用層防護、即時攻擊可視性、DDoS 回應團隊（DRT）支援，以及費用保護

常見混淆服務：
- AWS WAF：Web 應用程式防火牆，過濾 HTTP/HTTPS 惡意請求，通常與 Shield Advanced 搭配使用
- Security Groups / NACLs：網路層存取控制，非專用 DDoS 防護工具

題目關鍵字「mitigate DDoS attack」直接對應 AWS Shield 的核心定位。

---

## Questions (6–10)

(6) migrate its data and applications
Ans: AWS Professional Services / AWS Partner Network (APN)

(7) distribute incoming traffic across multiple targets
Ans: Elastic Load Balancing (ELB)

(8) EC2 instance for the lowest possible cost for a long-term, never be interrupted
Ans: EC2 Reserved Instance (RI)

(9) removing an AWS account
Ans: standalone account

(10) encrypted before sending
Ans: client-side

---

(6)
中文題目：企業想遷移資料與應用程式到 AWS，哪些資源可以協助？
答案：AWS Professional Services（AWS 專業服務）/ AWS Partner Network，APN（AWS 合作夥伴網路）
解析：AWS 提供兩種主要的遷移協助資源：
- **AWS Professional Services**：AWS 官方專業服務團隊，提供遷移規劃、架構設計、實作支援等端對端服務
- **AWS Partner Network（APN）**：AWS 認證的第三方合作夥伴生態系，包含 Consulting Partner（顧問夥伴）與 Technology Partner（技術夥伴），協助客戶設計與遷移解決方案
題目關鍵字「migrate data and applications（遷移資料與應用程式）」對應以上兩個資源，兩者皆可選。

(7)
中文題目：哪項 AWS 服務可將傳入流量分散到多個目標？
答案：Elastic Load Balancing，ELB（彈性負載平衡）
解析：ELB 是 AWS 的負載平衡服務，自動將傳入的應用程式流量分配到多個目標（如 EC2 執行個體、容器、IP 位址），分為三種類型：
- **ALB（Application Load Balancer）**：第 7 層，適合 HTTP/HTTPS 應用
- **NLB（Network Load Balancer）**：第 4 層，適合高效能 TCP/UDP 流量
- **CLB（Classic Load Balancer）**：舊世代，已逐漸淘汰
題目關鍵字「distribute incoming traffic across multiple targets（分散流量到多個目標）」直接對應 ELB 核心功能。

(8)
中文題目：需要長期使用且絕不能中斷的 EC2 執行個體，哪種購買方式成本最低？
答案：EC2 Reserved Instance，RI（預留執行個體）
解析：EC2 提供多種購買選項：
- **On-Demand（隨需）**：彈性最高，但費用最貴
- **Reserved Instance（RI，預留執行個體）**：預付 1 年或 3 年，可節省最高 72%，適合長期穩定負載，且**不會被中斷**
- **Spot Instance（競價執行個體）**：最便宜（可省 90%），但 AWS 可隨時中斷
- **Savings Plans**：彈性更高的預付方案
題目關鍵字「never be interrupted（不能中斷）+ long-term（長期）」排除 Spot，對應 RI。

(9)
中文題目：將 AWS 帳戶從組織中移除後，該帳戶會變成什麼狀態？
答案：standalone account（獨立帳戶）
解析：在 AWS Organizations 中，若將一個成員帳戶從組織移除，該帳戶會恢復為**獨立帳戶（standalone account）**，不再受組織的服務控制政策（SCP）管理，也無法共享組織的合併帳單。移除前須確認帳戶已具備獨立帳單能力（綁定付款方式）。

(10)
中文題目：資料在傳送至 AWS 之前就先完成加密，這屬於哪種加密方式？
答案：client-side encryption（用戶端加密）
解析：AWS 加密方式分為兩大類：
- **Client-side encryption（用戶端加密）**：資料在客戶端（本地）加密後才傳送到 AWS，金鑰由客戶自行管理，AWS 無法讀取原始資料
- **Server-side encryption（伺服器端加密）**：資料傳送至 AWS 後，由 AWS 在伺服器端加密（SSE-S3、SSE-KMS、SSE-C）
題目關鍵字「encrypted before sending（傳送前先加密）」明確對應 client-side encryption。

---

## Questions (11–15)

(11) privately connect VPCs
Ans: AWS PrivateLink / AWS Transit Gateway

(12) Shield Advanced provides expanded DDoS attack protection for
Ans: Amazon EC2, Elastic Load Balancing (ELB), Amazon CloudFront, Amazon Route 53, AWS Global Accelerator

(13) Shared Responsibility Model, AWS is responsible for
Ans: Physical and Environmental controls

(14) AWS database service for data warehousing
Ans: Amazon Redshift

(15) the underlying OS for Amazon Aurora is managed by
Ans: AWS Product Team automatically

---

(11)
中文題目：哪些 AWS 服務可以讓 VPC 之間進行私有連線，不經過公共網際網路？
答案：AWS PrivateLink / AWS Transit Gateway
解析：
- **AWS PrivateLink**：透過私有端點（Endpoint）讓 VPC 內的資源存取其他 VPC 或 AWS 服務，流量完全不經過公共網路，安全性高
- **AWS Transit Gateway**：作為中央集線器，連接多個 VPC 與本地端環境，支援大規模多 VPC 互聯
兩者差異：PrivateLink 適合單向服務存取；Transit Gateway 適合多 VPC 全互聯架構。

(12)
中文題目：AWS Shield Advanced 針對哪些 AWS 服務提供擴展的 DDoS 攻擊防護？
答案：Amazon EC2、Elastic Load Balancing（ELB）、Amazon CloudFront、Amazon Route 53、AWS Global Accelerator
解析：Shield Advanced 在 Shield Standard 基礎上，額外針對以上五項服務提供進階 DDoS 防護，包含：
- 即時攻擊可視性與詳細診斷報告
- 與 AWS WAF 整合進行第 7 層防護
- DDoS 回應團隊（DRT）24/7 支援
- DDoS 相關費用保護（避免流量暴增導致帳單飆升）

(13)
中文題目：在 AWS 共同責任模型中，AWS 負責哪些項目？
答案：Physical and Environmental controls（實體與環境控制）
解析：AWS 共同責任模型將責任分為兩層：
- **AWS 負責（Security OF the Cloud）**：資料中心實體安全、硬體、網路基礎設施、Hypervisor、實體與環境控制
- **客戶負責（Security IN the Cloud）**：作業系統設定、應用程式、資料加密、存取管理（IAM）、防火牆規則
題目關鍵字「Physical and Environmental controls」屬於 AWS 負責的底層基礎設施安全。

(14)
中文題目：哪項 AWS 資料庫服務專門用於資料倉儲與大規模分析？
答案：Amazon Redshift
解析：AWS 提供多種資料庫服務，各有適用場景：
- **Redshift**：OLAP 資料倉儲，適合 PB 級資料分析與商業智慧（BI）
- **RDS**：關聯式資料庫，適合 OLTP 交易處理
- **DynamoDB**：NoSQL，適合高速鍵值存取
- **Aurora**：高效能關聯式資料庫（MySQL/PostgreSQL 相容）
題目關鍵字「data warehousing（資料倉儲）」直接對應 Redshift。

(15)
中文題目：Amazon Aurora 底層作業系統由誰負責管理？
答案：AWS Product Team automatically（AWS 產品團隊自動管理）
解析：Amazon Aurora 是 AWS 的**完全受管（Fully Managed）**關聯式資料庫服務。客戶**無需**也**無法**存取或管理底層作業系統，所有 OS 修補、更新、維護皆由 AWS 自動處理。這與 EC2 不同——EC2 上的 OS 由客戶自行管理。這也是選用 Managed Service 的核心優勢之一。

---

## Questions (16–20)

(16) AWS interoperability with third-party software
Ans: AWS Business Support / AWS Enterprise Support

(17) support VPC Gateway Endpoint
Ans: Amazon S3 / Amazon DynamoDB

(18) moving 500 GB of data from an EC2 instance to an S3 bucket in the same region
Ans: would not be charged（不收費）

(19) AWS Shared Responsibility Model — responsibilities of AWS
Ans: Operating the infrastructure layer, OS, and platform for Amazon S3 / Replacing faulty hardware of Amazon EC2 instances

(20) identify sensitive data on S3
Ans: Amazon Macie

---

(16)
中文題目：哪些 AWS Support 方案提供與第三方軟體互通性（interoperability）的支援？
答案：AWS Business Support / AWS Enterprise Support
解析：
- **Business Support**：提供第三方軟體與 AWS 互通性的有限指導（interoperability guidance）
- **Enterprise Support**：提供更全面的第三方軟體整合支援，並有 TAM（Technical Account Manager）專屬技術客戶經理
- **Developer Support**：不包含第三方軟體互通性支援
題目關鍵字「interoperability with third-party software」是 Business 與 Enterprise 方案的特有功能。

(17)
中文題目：哪些 AWS 服務支援 VPC Gateway Endpoint？
答案：Amazon S3 / Amazon DynamoDB
解析：VPC Endpoint 分為兩種類型：
- **Gateway Endpoint**：僅支援 **Amazon S3** 與 **Amazon DynamoDB**，透過路由表設定，流量不經過公共網路，免費使用
- **Interface Endpoint（PrivateLink）**：支援大多數其他 AWS 服務，使用 ENI（彈性網路介面），需收費
考試常考：Gateway Endpoint 只有 S3 和 DynamoDB，其他皆為 Interface Endpoint。

(18)
中文題目：將 500 GB 資料從 EC2 執行個體移動到同一 Region 的 S3 儲存桶，會產生費用嗎？
答案：would not be charged（不會收費）
解析：AWS 資料傳輸費用規則：
- **同一 Region 內，EC2 → S3**：**免費**
- **跨 Region 傳輸**：收費
- **從 AWS 傳出到網際網路**：收費
- **從網際網路傳入 AWS**：免費
題目情境為同一 Region 內傳輸，因此不收取資料傳輸費用。

(19)
中文題目：在 AWS 共同責任模型中，以下哪些屬於 AWS 的責任？
答案：
- 負責 Amazon S3 的基礎設施層、作業系統與平台運作
- 替換 Amazon EC2 執行個體的故障硬體
解析：AWS 負責所有底層基礎設施的運作與維護：
- **S3**：完全受管服務，AWS 負責從硬體到平台的所有層級
- **EC2**：AWS 負責實體主機硬體（含故障更換），客戶負責 Guest OS 以上的層級
客戶不需擔心硬體故障或底層 OS 維護，這些皆由 AWS 處理。

(20)
中文題目：哪項 AWS 服務可自動識別 S3 中的敏感資料？
答案：Amazon Macie
解析：**Amazon Macie** 是機器學習驅動的資料安全服務，可自動掃描 S3 儲存桶，識別並保護敏感資料，例如：
- 個人識別資訊（PII）：姓名、電話、信用卡號
- 財務資料、醫療資料
Macie 會持續監控 S3 存取模式，並發出安全警示。常與合規需求（如 GDPR、HIPAA）相關聯。

---

## Questions (21–25)

(21) decouple components of a microservices architecture
Ans: Amazon SQS / Amazon SNS

(22) rapidly develop, test, and launch — this benefit is called
Ans: Agility

(23) AZ-specific characteristics of Amazon EBS and Amazon EFS
Ans: EBS volume can be attached to a single instance in the same AZ / EFS file system can be mounted on instances across multiple AZs

(24) only core checks from the AWS Trusted Advisor
Ans: AWS Basic Support / AWS Developer Support

(25) move to a fully managed AWS database — this migration strategy is called
Ans: Replatform

---

(21)
中文題目：哪些 AWS 服務可用來解耦微服務架構的各個元件？
答案：Amazon SQS（簡單佇列服務）/ Amazon SNS（簡單通知服務）
解析：
- **Amazon SQS（Simple Queue Service）**：訊息佇列服務，實現非同步解耦。生產者將訊息放入佇列，消費者自行取用，兩端互不依賴
- **Amazon SNS（Simple Notification Service）**：發布/訂閱（Pub/Sub）通知服務，一對多廣播訊息至多個訂閱者
兩者皆是微服務解耦的核心工具，SQS 適合點對點，SNS 適合廣播通知。

(22)
中文題目：雲端讓企業能快速開發、測試與推出產品，這對應雲端的哪項優勢？
答案：Agility（敏捷性）
解析：AWS 定義的六大雲端優勢中，**Agility（敏捷性）** 指的是：
- 可在幾分鐘內部署資源，縮短從構想到產品的時間
- 快速實驗、迭代，降低失敗成本
- 相比傳統 IT 採購流程（數週至數月），雲端可即時取得所需資源
題目關鍵字「rapidly develop, test, and launch」直接對應 Agility。

(23)
中文題目：Amazon EBS 與 Amazon EFS 在可用區（AZ）層面的特性差異為何？
答案：
- EBS Volume 只能掛載到**同一 AZ 內的單一執行個體**
- EFS 檔案系統可以跨**多個 AZ** 掛載到多個執行個體
解析：
- **EBS（Elastic Block Store）**：區塊儲存，綁定特定 AZ，一次只能掛載一個 EC2（除非使用 Multi-Attach，但有限制）
- **EFS（Elastic File System）**：共享檔案儲存，跨 AZ 可用，支援數百個 EC2 同時掛載，適合共享工作負載

(24)
中文題目：哪些 AWS Support 方案只提供 Trusted Advisor 的核心檢查？
答案：AWS Basic Support / AWS Developer Support
解析：AWS Trusted Advisor 的存取權限依 Support 方案而異：
- **Basic / Developer**：僅限**核心（core）安全與服務限制**類別的基本檢查（約 7 項）
- **Business**：解鎖全部 Trusted Advisor 檢查（100+ 項），涵蓋成本優化、效能、安全、容錯、服務限制
- **Enterprise**：同 Business，另加 TAM 支援
考試常考：完整 Trusted Advisor 功能需 Business 以上方案。

(25)
中文題目：將應用程式遷移至完全受管的 AWS 資料庫，這種遷移策略稱為什麼？
答案：Replatform（重新平台化）
解析：AWS 遷移的 7R 策略中：
- **Rehost（重新託管 / Lift & Shift）**：原樣搬移到 AWS，不做更動
- **Replatform（重新平台化 / Lift, Tinker & Shift）**：少量調整以利用雲端優勢，例如改用受管資料庫（RDS），不重寫應用程式
- **Refactor / Re-architect**：大幅重新設計以充分利用雲端原生功能
題目情境「移至 fully managed 資料庫」屬於小幅調整，對應 **Replatform**。

---

## Questions (26–30)

(26) advantages of cloud computing
Ans: Benefit from massive economies of scale / Trade capital expense for variable expense / Go global in minutes

(27) needs speech-based input and output
Ans: Use Amazon Transcribe to convert speech to text, then use Amazon Polly to convey results via speech

(28) receive alerts when reservation utilization falls below the defined threshold
Ans: AWS Budgets

(29) optimal AWS resource configuration to reduce costs
Ans: AWS Compute Optimizer

(30) MOST cost-effective option to purchase an EC2 Reserved Instance
Ans: Partial upfront payment option with standard 3-year term

---

(26)
中文題目：以下哪些是雲端運算的優勢？
答案：
- 受益於大規模經濟效益（Benefit from massive economies of scale）
- 以變動費用取代資本支出（Trade capital expense for variable expense）
- 幾分鐘內走向全球（Go global in minutes）
解析：AWS 定義的六大雲端優勢包含：
1. Trade capital expense for variable expense（CapEx → OpEx）
2. Benefit from massive economies of scale（共享規模效益，單位成本更低）
3. Stop guessing capacity（按需取用，無需預估容量）
4. Increase speed and agility（加快創新速度）
5. Stop spending money running and maintaining data centers（無需維運機房）
6. Go global in minutes（快速全球部署）

(27)
中文題目：應用程式需要語音輸入並以語音回應，應使用哪些 AWS 服務？
答案：使用 Amazon Transcribe 將語音轉為文字，再使用 Amazon Polly 將結果轉換為語音輸出
解析：
- **Amazon Transcribe**：自動語音辨識（ASR），將音訊轉換為文字（Speech to Text）
- **Amazon Polly**：文字轉語音（TTS，Text to Speech），將文字合成自然語音
兩者串接可實現完整的語音輸入→處理→語音輸出流程，常用於語音助理、客服機器人等場景。

(28)
中文題目：當預留使用量低於設定閾值時，哪項 AWS 服務可發送警示？
答案：AWS Budgets
解析：**AWS Budgets** 可設定成本、使用量、預留（Reservation）及 Savings Plans 的預算警示：
- **Cost Budget**：當實際或預測費用超出預算時通知
- **Usage Budget**：監控使用量
- **Reservation Budget**：當 RI 或 Savings Plans 使用率低於閾值時發出警示
題目關鍵字「reservation utilization falls below threshold（使用率低於閾值）」直接對應 AWS Budgets 的 Reservation Budget 功能。

(29)
中文題目：哪項 AWS 服務可分析並建議最佳資源配置以降低成本？
答案：AWS Compute Optimizer
解析：**AWS Compute Optimizer** 使用機器學習分析 CloudWatch 歷史指標，針對以下資源提供最佳化建議：
- EC2 執行個體類型
- EC2 Auto Scaling 群組
- EBS Volume 類型與大小
- AWS Lambda 記憶體設定
可協助識別過度配置（over-provisioned）或配置不足（under-provisioned）的資源，達到降本目的。

(30)
中文題目：購買 EC2 Reserved Instance 最符合成本效益的方案是？
答案：Partial Upfront，3 年期標準 RI（部分預付 + 3 年期）
解析：EC2 RI 付款方式比較：
- **All Upfront（全額預付）**：折扣最高，但需一次付清全額
- **Partial Upfront（部分預付）**：先付一部分，剩餘按月計費，折扣次之
- **No Upfront（零預付）**：無需預付，折扣最低
期間選項：1 年 vs **3 年**（3 年折扣更大）
題目要求「最符合成本效益」且兼顧現金流，**Partial Upfront + 3 年期** 在折扣幅度與資金靈活性之間取得最佳平衡。

---

## Questions (31–35)

(31) connect on-premises environment to VPC without public internet
Ans: AWS Direct Connect

(32) Credit billing scenario
Ans: Credit one applied to EC2 → $900 EC2, $500 S3 remaining / Credit two applied to $900 EC2 → Final: $850 EC2 + $500 S3

(33) encryption enabled by default
Ans: CloudTrail Logs

(34) statements are CORRECT about AWS Regions and AZs
Ans: Each AWS Region consists of a minimum of three Availability Zones / Each AZ consists of one or more discrete data centers

(35) available for all AWS customers by default at no additional cost
Ans: AWS Shield Standard

---

(31)
中文題目：哪項 AWS 服務可讓企業從本地環境連接到 VPC，且不經過公共網際網路？
答案：AWS Direct Connect
解析：**AWS Direct Connect** 提供從企業資料中心到 AWS 的**專用私有網路連線**，優勢包含：
- 不經過公共網際網路，安全性與穩定性更高
- 固定頻寬，延遲更低且一致
- 適合大量資料傳輸或對網路品質要求高的企業
與 VPN 比較：VPN 透過公共網路加密傳輸，Direct Connect 則是實體專線，兩者皆可連接本地與 VPC，但 Direct Connect 更穩定且通常成本效益更佳（大流量時）。

(32)
中文題目：點數（Credit）套用的計費情境題解析？
答案：
- 點數一（$100，2022年7月到期，可用於 EC2 或 S3）→ 優先套用，選擇套用於 EC2 → EC2 剩 $900，S3 $500 不變
- 點數二（$50，2022年12月到期，僅限 EC2）→ 套用於 EC2 $900 → EC2 剩 $850
- 最終帳單：EC2 $850 + S3 $500
解析：AWS 點數套用規則：
1. **最早到期**的點數優先使用
2. **限制最多**的點數（用途最窄）優先套用
3. 點數一到期較早且可用於 EC2 或 S3，優先套用於 EC2（與點數二相同用途，避免浪費靈活性）
4. 點數二僅限 EC2，套用於剩餘 EC2 費用

(33)
中文題目：哪項 AWS 服務的日誌預設即啟用加密？
答案：CloudTrail Logs（CloudTrail 日誌）
解析：**AWS CloudTrail** 預設將日誌儲存至 S3，並自動使用 **SSE-S3（伺服器端加密）** 進行加密保護，無需額外設定。若需更高控制，可改用 SSE-KMS 加密。這確保稽核日誌在靜態儲存時受到保護，符合合規要求。

(34)
中文題目：關於 AWS Region 與可用區（AZ）的正確描述為何？
答案：
- 每個 AWS Region 至少包含**三個**可用區（AZ）
- 每個 AZ 由一個或多個**獨立資料中心**組成
解析：
- **Region**：地理區域，如 us-east-1，各 Region 彼此完全獨立
- **AZ（Availability Zone）**：Region 內的獨立故障域，擁有獨立電力、冷卻、網路
- **資料中心**：AZ 的物理組成單位，一個 AZ 可含多個資料中心
此架構設計確保單一 AZ 故障不影響其他 AZ，提升高可用性。

(35)
中文題目：哪項 AWS 服務預設提供給所有 AWS 客戶，且無需額外付費？
答案：AWS Shield Standard
解析：**AWS Shield Standard** 自動保護所有 AWS 客戶，免費提供：
- 防禦常見的第 3 層（網路層）與第 4 層（傳輸層）DDoS 攻擊
- 與 CloudFront、Route 53 整合，提供基本防護
無需啟用或設定，所有 AWS 帳戶即自動享有。若需進階防護則升級至 Shield Advanced（付費）。

---

## Questions (36–40)

(36) statements are CORRECT about Security Groups and NAT Gateway
Ans: A Security Group can have allow rules only / A NAT Gateway is managed by AWS

(37) multiple AWS accounts wants to share reserved EC2 instances
Ans: Use AWS Organizations

(38) automate timely assessments and check for OS vulnerabilities
Ans: Amazon Inspector

(39) provide programmatic access to AWS resources
Ans: Use Access Key ID and Secret Access Key

(40) needs high-performance hardware disks with fast I/O — the MOST cost-effective
Ans: Instance Store

---

(36)
中文題目：關於 Security Group 與 NAT Gateway 的正確描述為何？
答案：
- Security Group 只能設定**允許（allow）規則**，無法設定拒絕規則
- NAT Gateway 由 **AWS 負責管理**
解析：
- **Security Group**：有狀態（stateful）防火牆，僅支援 Allow 規則，沒有 Deny 規則。若未明確允許，流量預設拒絕（隱式拒絕）。與 NACL 不同——NACL 同時支援 Allow 與 Deny 規則，且為無狀態（stateless）
- **NAT Gateway**：AWS 完全受管服務，客戶無需維護底層基礎設施，只需在 Public Subnet 建立並設定路由即可

(37)
中文題目：擁有多個 AWS 帳戶的企業希望共享預留的 EC2 執行個體，應使用哪項服務？
答案：AWS Organizations
解析：**AWS Organizations** 提供多帳戶管理功能，其中包含**合併帳單（Consolidated Billing）**，讓組織內所有成員帳戶的 RI 與 Savings Plans 使用量可以共享與合併計算，未使用的 RI 折扣可自動套用至其他帳戶，最大化預留資源的利用率。

(38)
中文題目：哪項 AWS 服務可自動化定期評估並檢查作業系統漏洞？
答案：Amazon Inspector
解析：**Amazon Inspector** 是自動化安全評估服務，可：
- 掃描 EC2 執行個體的作業系統漏洞（CVE 資料庫）
- 檢查 Lambda 函數與 ECR 容器映像的安全性
- 持續監控並產生安全發現（findings）報告
題目關鍵字「OS vulnerabilities（作業系統漏洞）+ automated assessments（自動評估）」直接對應 Inspector。

(39)
中文題目：如何提供對 AWS 資源的程式化存取（programmatic access）？
答案：使用 Access Key ID 與 Secret Access Key
解析：AWS 身份驗證方式：
- **控制台登入**：使用帳號密碼（+MFA）
- **程式化存取（Programmatic Access）**：使用 **Access Key ID + Secret Access Key**，搭配 AWS CLI、SDK 或 API 呼叫
注意：Access Key 僅在建立時顯示一次，需妥善保存。最佳實踐建議使用 IAM Role 取代長期 Access Key，尤其在 EC2 或 Lambda 上。

(40)
中文題目：需要高效能硬體磁碟與快速 I/O，且最符合成本效益的選項為何？
答案：Instance Store（執行個體存放區）
解析：
- **Instance Store**：直接連接到主機實體硬體的臨時性儲存，提供極低延遲與極高 I/O 效能，**不額外收費**（包含在執行個體費用中）
- **EBS（gp3/io2）**：持久性區塊儲存，效能佳但需額外付費
- **EFS**：共享檔案儲存，效能不如 Instance Store
注意：Instance Store 資料在執行個體停止或終止時會**遺失**，適合暫存快取、緩衝區等不需持久化的高速資料。

---

## Questions (41–45)

(41) needs to continue working on the same endpoint without manual intervention during an AZ outage
Ans: Configure RDS Multi-AZ deployment with automatic failover

(42) the highest possible discount for Spot Instances
Ans: 90%

(43) AWS resources being used to carry out malicious attacks
Ans: Contact AWS Abuse Team

(44) an INCORRECT statement about fault tolerance and scaling
Ans: Fault tolerance is achieved by a scale up operation

(45) storage services
Ans: Amazon S3 (Object Storage) / Amazon EFS (File Storage)

---

(41)
中文題目：需要在 AZ 中斷時，不需人工介入即可繼續使用相同端點，應如何設定 RDS？
答案：設定 RDS Multi-AZ 部署並啟用自動容錯移轉（Automatic Failover）
解析：**RDS Multi-AZ** 在不同 AZ 維護一個同步的備用副本（Standby），當主要執行個體發生故障或 AZ 中斷時：
- 自動切換至備用副本（通常在 1-2 分鐘內完成）
- **端點（Endpoint）不變**，應用程式無需修改連線字串
- 整個過程無需人工介入
題目關鍵字「same endpoint（相同端點）+ no manual intervention（無需人工介入）」對應 Multi-AZ 自動容錯移轉。

(42)
中文題目：EC2 Spot Instance 最高可享有多少折扣？
答案：90%（相較於 On-Demand 價格）
解析：**EC2 Spot Instance** 利用 AWS 的閒置運算容量，價格依市場供需即時波動，最高可比 On-Demand 便宜 **90%**，是最具成本效益的 EC2 購買選項。缺點是 AWS 可在 2 分鐘通知後中斷執行個體，因此適合可容忍中斷的工作負載（如批次處理、大數據分析、CI/CD）。

(43)
中文題目：發現 AWS 資源被用來執行惡意攻擊，應聯絡哪個團隊？
答案：聯絡 AWS Abuse Team（AWS 濫用回報團隊）
解析：**AWS Abuse Team** 專門處理 AWS 資源被濫用的情況，包含：
- 來自 AWS IP 的 DDoS 攻擊、垃圾郵件、掃描、惡意軟體散佈
- 回報途徑：透過 AWS Support 或直接寄信至 abuse@amazonaws.com
若是自己帳戶遭入侵，應同時聯絡 AWS Support 進行事件回應。

(44)
中文題目：關於容錯（Fault Tolerance）與擴展，哪個敘述是**錯誤的**？
答案：「容錯是透過垂直擴展（Scale Up）來實現的」——這是錯誤說法
解析：
- **容錯（Fault Tolerance）**：系統在元件故障時仍能持續運作，透過**冗餘（redundancy）**實現，例如 Multi-AZ、多執行個體部署
- **Scale Up（垂直擴展）**：升級單一資源的規格（更大的 EC2），提升效能，但不解決單點故障問題
- **Scale Out（水平擴展）**：增加執行個體數量，搭配 ELB 實現高可用性，更接近容錯的概念
容錯的核心是**冗餘與備援**，而非單純擴展規格。

(45)
中文題目：哪些是 AWS 的儲存服務，分別屬於哪種儲存類型？
答案：
- **Amazon S3**：物件儲存（Object Storage）
- **Amazon EFS**：檔案儲存（File Storage）
解析：AWS 三大儲存類型：
- **物件儲存（Object Storage）**：S3，儲存非結構化資料（圖片、影片、備份），以 URL 存取
- **區塊儲存（Block Storage）**：EBS、Instance Store，掛載至 EC2 如同本機硬碟
- **檔案儲存（File Storage）**：EFS（Linux 共享）、FSx（Windows/HPC），支援多執行個體同時掛載

---

## Questions (46–50)

(46) wants an estimate of the monthly AWS bill
Ans: AWS Pricing Calculator

(47) to respond to customer inquiries and feedback
Ans: Organize teams around products and value streams / Leverage agile methods to rapidly iterate and evolve

(48) server-bound software licenses
Ans: EC2 Dedicated Host

(49) shared responsibility of both AWS and the customer
Ans: Configuration Management

(50) review HIPAA compliance and governance-related documents on AWS
Ans: AWS Artifact

---

(46)
中文題目：哪項 AWS 工具可協助估算每月 AWS 帳單金額？
答案：AWS Pricing Calculator
解析：**AWS Pricing Calculator**（前身為 Simple Monthly Calculator）可讓使用者：
- 選擇 AWS 服務與配置參數
- 估算每月費用
- 分享估算結果（產生連結）
適合規劃新專案或評估架構成本，不需要有 AWS 帳戶即可使用。

(47)
中文題目：企業想快速回應客戶詢問與回饋，應採取哪些做法？
答案：
- 將團隊組織圍繞產品與價值流（Organize teams around products and value streams）
- 運用敏捷方法快速迭代與演進（Leverage agile methods to rapidly iterate and evolve）
解析：這題考察 **AWS Cloud Adoption Framework（CAF）** 或雲端轉型的組織文化面向。快速回應客戶需要：打破孤島式組織結構、以產品為中心組建跨職能團隊，並採用敏捷開發方法（Scrum、Kanban）縮短交付週期，提升對市場與客戶需求的反應速度。

(48)
中文題目：哪種 EC2 選項適合需要繫結至特定伺服器的軟體授權（server-bound licenses）？
答案：EC2 Dedicated Host（專用主機）
解析：**EC2 Dedicated Host** 提供專屬的實體伺服器，可見並控制伺服器的插槽（Socket）、核心（Core）數量，適合攜帶 BYOL（Bring Your Own License）授權的軟體，例如 Windows Server、SQL Server、Oracle，這些軟體授權通常以實體 CPU Socket 或核心數為授權基準。
與 Dedicated Instance 差異：Dedicated Instance 確保不與他人共享硬體，但不提供硬體的可見性與控制。

(49)
中文題目：在 AWS 共同責任模型中，哪個項目是 AWS 與客戶**共同**負責的？
答案：Configuration Management（組態管理）
解析：**Configuration Management** 是少數落在責任共享區域的項目：
- **AWS 負責**：底層基礎設施的組態（硬體、網路設備）
- **客戶負責**：Guest OS、應用程式、AWS 服務（如 S3 存取政策、Security Group 規則）的組態
因此，整體「組態管理」是雙方共同承擔的責任範疇，不屬於任何一方單獨負責。

(50)
中文題目：哪項 AWS 服務可讓客戶查閱 HIPAA 合規與治理相關文件？
答案：AWS Artifact
解析：**AWS Artifact** 是 AWS 的合規文件自助下載入口，提供：
- **AWS 合規報告**：SOC 1/2/3、PCI DSS、ISO 27001、HIPAA BAA 等第三方稽核報告
- **AWS 合規協議**：如業務夥伴協議（BAA，Business Associate Agreement），供 HIPAA 需求使用
完全免費，可透過 AWS Management Console 存取，無需聯絡 AWS 支援。

---

## Questions (51–55)

(51) moving to AWS would result in cost savings
Ans: Data center hardware infrastructure expenditure / Data center physical security expenditure

(52) the advantages AWS Cloud offers
Ans: Trade capital expense for variable expense / Eliminate guessing on your infrastructure capacity needs

(53) a Linux-based On-Demand EC2 instance with per-second billing but terminated within 30 seconds
Ans: Charged for 60 seconds

(54) Which type of cloud computing does Amazon EC2 represent
Ans: Infrastructure as a Service (IaaS)

(55) AWS WAF offers protection from common web exploits at which layer
Ans: Layer 7

---

(51)
中文題目：遷移至 AWS 後，哪些費用可以節省？
答案：
- 資料中心硬體基礎設施支出
- 資料中心實體安全支出
解析：遷移至 AWS 後，企業無需自行購買與維護伺服器、儲存設備、網路設備等硬體，也不需負擔資料中心的實體安全（門禁、監控、保全）費用，這些皆由 AWS 承擔。這體現了雲端「以 OpEx 取代 CapEx」的核心優勢。

(52)
中文題目：哪些是 AWS 雲端提供的優勢？
答案：
- 以變動費用取代資本支出（Trade capital expense for variable expense）
- 消除對基礎設施容量的猜測（Eliminate guessing on your infrastructure capacity needs）
解析：
- **Trade CapEx for OpEx**：不需預先大量投資固定資產，改為按使用量付費
- **Eliminate guessing capacity**：雲端可按需擴縮，無需預估並預購過多或過少的容量，避免資源浪費或效能不足

(53)
中文題目：啟動一個 Linux On-Demand EC2 執行個體（按秒計費），但 30 秒後就終止，會被收取多少費用？
答案：收取 **60 秒**（1 分鐘）的費用
解析：**EC2 Linux 按秒計費**有一個重要規則：**最低收費為 60 秒**。即使執行時間不足 60 秒，仍會被收取 60 秒費用。30 秒 < 60 秒最低門檻，因此收取 60 秒費用。Windows 執行個體則以小時為單位計費。

(54)
中文題目：Amazon EC2 屬於哪種雲端運算服務類型？
答案：Infrastructure as a Service，IaaS（基礎設施即服務）
解析：雲端服務三大類型：
- **IaaS**：提供虛擬化基礎設施（運算、儲存、網路），客戶管理 OS 以上層級，如 **EC2**
- **PaaS**：提供執行平台，客戶只需部署應用程式，如 AWS Elastic Beanstalk
- **SaaS**：完整軟體服務，如 Gmail、Salesforce
EC2 讓客戶控制 OS、中介軟體、應用程式，符合 IaaS 定義。

(55)
中文題目：AWS WAF 在哪一層提供對常見 Web 攻擊的防護？
答案：Layer 7（應用層）
解析：**AWS WAF（Web Application Firewall）** 運作於 OSI 模型第 7 層（應用層），可過濾 HTTP/HTTPS 請求，防禦：
- SQL Injection（SQL 注入）
- Cross-Site Scripting（XSS，跨站腳本）
- 惡意 Bot 流量
- IP 黑白名單
與 Shield 比較：Shield 防護第 3/4 層（網路/傳輸層）DDoS，WAF 防護第 7 層應用攻擊，兩者互補。

---

## Questions (56–60)

(56) will help you access AWS services using programming language-specific APIs
Ans: AWS Software Developer Kit (SDK)

(57) serverless AWS service
Ans: AWS Lambda

(58) takes the most time to retrieve data
Ans: Amazon S3 Glacier Deep Archive

(59) stakeholder roles for the AWS CAF platform perspective
Ans: Engineer / Chief Technology Officer (CTO)

(60) debug performance issues for serverless application built using microservices
Ans: AWS X-Ray

---

(56)
中文題目：哪項 AWS 工具可讓你使用特定程式語言的 API 存取 AWS 服務？
答案：AWS Software Developer Kit，SDK（軟體開發套件）
解析：**AWS SDK** 提供多種程式語言的函式庫，讓開發人員以原生語言風格呼叫 AWS API，支援語言包含：Python（Boto3）、JavaScript/Node.js、Java、.NET、Go、Ruby、PHP 等。SDK 封裝底層 HTTP 請求與認證邏輯，簡化與 AWS 服務的整合。

(57)
中文題目：哪項 AWS 服務是無伺服器（serverless）服務？
答案：AWS Lambda
解析：**AWS Lambda** 是 AWS 核心的無伺服器運算服務，特點：
- 無需佈建或管理伺服器
- 按實際執行時間與請求次數計費（毫秒計費）
- 自動擴縮，支援觸發器（S3、API Gateway、DynamoDB Streams 等）
- 最長執行時間 15 分鐘
適合事件驅動架構、API 後端、資料處理等場景。

(58)
中文題目：哪種 AWS 儲存選項的資料取回時間最長？
答案：Amazon S3 Glacier Deep Archive
解析：S3 儲存類別依取回速度排列（從快到慢）：
1. S3 Standard：毫秒
2. S3 Standard-IA：毫秒
3. S3 Glacier Instant Retrieval：毫秒
4. S3 Glacier Flexible Retrieval：數分鐘至數小時
5. **S3 Glacier Deep Archive**：**12 至 48 小時**（最長）
Deep Archive 是 AWS 成本最低的儲存類別，適合需長期保存且極少存取的資料（如法規要求的 7-10 年封存）。

(59)
中文題目：AWS Cloud Adoption Framework（CAF）平台視角的利害關係人角色為何？
答案：Engineer（工程師）/ Chief Technology Officer，CTO（技術長）
解析：**AWS CAF** 定義六大視角（Perspectives）：Business、People、Governance、Platform、Security、Operations。**Platform 視角**關注技術架構與雲端平台建設，主要利害關係人為：
- **CTO**：制定技術方向與平台策略
- **Engineer**：實作與維護雲端平台
此視角涵蓋架構模式、資料策略、平台工程等能力。

(60)
中文題目：哪項 AWS 服務可協助除錯無伺服器微服務應用程式的效能問題？
答案：AWS X-Ray
解析：**AWS X-Ray** 是分散式追蹤服務，可：
- 視覺化微服務之間的請求路徑（Service Map）
- 識別效能瓶頸與錯誤根因
- 追蹤跨 Lambda、API Gateway、DynamoDB 等服務的請求鏈
- 分析延遲分佈與錯誤率
題目關鍵字「debug performance issues + serverless + microservices」直接對應 X-Ray 的核心使用場景。

---

## Questions (61–65)

(61) support reservations to optimize costs
Ans: Amazon EC2 / Amazon DynamoDB / Amazon RDS

(62) storage accessed by hundreds of EC2 instances simultaneously to append data to existing files
Ans: Amazon EFS

(63) support active-active configuration in both East and West US AWS regions
Ans: Amazon DynamoDB with global tables

(64) wants expert professional advice on migrating to AWS and managing applications
Ans: APN Consulting Partner

(65) accessed less frequently but needs rapid access when required
Ans: Amazon S3 Standard-Infrequent Access (S3 Standard-IA)

---

(61)
中文題目：哪些 AWS 服務支援透過預留（Reservations）來優化成本？
答案：Amazon EC2（預留執行個體）/ Amazon DynamoDB（預留容量）/ Amazon RDS（預留執行個體）
解析：AWS 多項服務提供預留選項以換取折扣：
- **EC2 Reserved Instance（RI）**：預留運算容量，折扣最高 72%
- **RDS Reserved Instance**：預留資料庫執行個體，折扣類似 EC2
- **DynamoDB Reserved Capacity**：預留讀寫容量單位（RCU/WCU），適合穩定負載
- **ElastiCache / OpenSearch / Redshift** 亦支援預留，但本題選項聚焦以上三者

(62)
中文題目：批次分析應用程式需要可被數百個 EC2 執行個體同時存取、並能對現有檔案附加資料的儲存，應選擇哪個服務？
答案：Amazon EFS（彈性檔案系統）
解析：**Amazon EFS** 是 NFS 協定的共享檔案儲存，支援：
- **數千個** EC2 執行個體同時掛載（跨多 AZ）
- 標準檔案系統語義，支援 append（附加寫入）操作
- 自動擴縮，無需預先配置容量
S3 雖可被多個執行個體存取，但不支援傳統檔案系統的 append 操作（物件不可變更，需整體覆寫）。EFS 最符合本題需求。

(63)
中文題目：哪項 AWS 服務支援在美國東部與西部兩個 Region 同時進行主動-主動（active-active）配置？
答案：Amazon DynamoDB with Global Tables（全域資料表）
解析：**DynamoDB Global Tables** 提供跨 Region 的多主動（multi-master）複寫：
- 每個 Region 都可讀寫（active-active）
- 資料在 Region 間自動同步（通常在 1 秒內）
- 支援低延遲全球讀寫存取
與 RDS Multi-AZ 比較：Multi-AZ 為主動-被動（active-passive），僅單一 Region 內。Global Tables 才支援跨 Region active-active。

(64)
中文題目：企業需要專業建議來協助遷移至 AWS 並管理雲端應用程式，應尋找哪類合作夥伴？
答案：APN Consulting Partner（AWS 合作夥伴網路顧問夥伴）
解析：**AWS Partner Network（APN）** 包含兩大類別：
- **Consulting Partner（顧問夥伴）**：提供專業服務，協助客戶設計、遷移、建置與管理 AWS 工作負載，如系統整合商（SI）、託管服務提供商（MSP）
- **Technology Partner（技術夥伴）**：提供在 AWS 上運行的軟體產品與服務
題目強調「expert advice + migration + managing applications」對應 **Consulting Partner**。

(65)
中文題目：資料存取頻率較低，但需要時能快速存取，應使用哪種 S3 儲存類別？
答案：Amazon S3 Standard-Infrequent Access，S3 Standard-IA
解析：S3 儲存類別中，**S3 Standard-IA** 的設計正是為了：
- **低頻存取**：儲存費用低於 S3 Standard
- **快速取回**：毫秒級存取（與 S3 Standard 相同速度），無需等待
- 取回時額外收取取回費用（per GB）
與其他低頻類別比較：Glacier 系列雖更便宜，但取回需等待分鐘至小時，不符合「rapid access（快速存取）」需求。題目關鍵字「less frequently + rapid access when required」直接對應 S3 Standard-IA。