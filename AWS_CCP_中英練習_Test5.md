# AWS Cloud Practitioner【TEST05】

---

## Questions (1–5)

(1) used to deny traffic from a specific IP address
Ans: Network Access Control List (Network ACL)

(2) an AWS best practice when architecting for the Cloud
Ans: Automation（自動化）

(3) MOST cost-effective when getting enhanced technical support by Cloud Support Engineers
Ans: AWS Business Support

(4) used to calculate the charge for Amazon EBS Volumes
Ans: Volume type / Provisioned IOPS

(5) used to generate, use, and manage encryption keys on the AWS Cloud
Ans: AWS CloudHSM

---

(1)
中文題目：哪項 AWS 服務可用於拒絕來自特定 IP 位址的流量？
答案：Network Access Control List，Network ACL（網路存取控制清單）
解析：**Network ACL** 是子網路層級的無狀態防火牆，支援 Allow 與 **Deny** 規則：
- 可明確設定「拒絕（Deny）特定 IP 位址的所有流量」
- 規則依號碼升冪順序評估，第一條匹配即停止
- **無狀態（Stateless）**：入站與出站規則各自獨立，需分別設定
相比之下，**Security Group 只有 Allow 規則**，無法明確拒絕特定 IP（未被允許的流量隱式拒絕，但無法針對性地封鎖某個 IP）。題目關鍵字「deny traffic from a specific IP」需要明確 Deny 規則，因此對應 Network ACL。

(2)
中文題目：在雲端架構設計上，哪項是 AWS 的最佳實踐？
答案：Automation（自動化）
解析：**自動化**是 AWS Well-Architected Framework 跨多個支柱的核心設計原則：
- **Operational Excellence**：以程式碼執行操作，自動化變更管理與事件回應
- **Reliability**：自動化故障偵測、自我修復（Auto Scaling、Multi-AZ Failover）
- **Security**：自動化安全測試、合規評估（Config Rules、Security Hub）
雲端的最大優勢之一是可透過 API 驅動自動化，取代人工重複操作，降低錯誤率並提升速度。

(3)
中文題目：哪個 AWS Support 方案在取得雲端支援工程師的強化技術支援方面最符合成本效益？
答案：AWS Business Support
解析：Support 方案技術支援比較：
- **Basic**：無技術支援（僅文件與論壇）
- **Developer**：Email 支援（工作時間），1 位聯絡人
- **Business**：**24/7 電話、Email、Chat 技術支援**，由 Cloud Support Engineers 提供，無限聯絡人數
- **Enterprise**：同 Business，另加 TAM，但費用大幅更高
題目要求「Cloud Support Engineers + 最符合成本效益」，Business 是提供此等級支援的**最低成本方案**。

(4)
中文題目：計算 Amazon EBS Volume 費用時，哪些因素會被考量？
答案：Volume type（Volume 類型）/ Provisioned IOPS（預置 IOPS）
解析：**Amazon EBS 定價**的主要計費維度：
- **Volume Type（類型）**：不同類型費率不同
  - gp3（通用型 SSD）：最常用，基礎費率最低
  - io2/io1（佈建 IOPS SSD）：高效能，費率最高
  - st1（吞吐量 HDD）、sc1（冷 HDD）：低成本
- **Provisioned IOPS**：io1/io2 類型需額外為預置的 IOPS 付費
- **Storage Size（GB）**：儲存容量按 GB/月計費
- **Snapshot 儲存**：快照佔用的 S3 空間另計

(5)
中文題目：哪項 AWS 服務用於在 AWS Cloud 上生成、使用與管理加密金鑰？
答案：AWS CloudHSM（雲端硬體安全模組）
解析：**AWS CloudHSM** 提供 FIPS 140-2 Level 3 認證的**專用硬體安全模組**：
- 金鑰完全由客戶掌控，AWS 無法存取
- 適合需要最高安全等級的合規場景（金融、政府）
與 **AWS KMS** 比較：
- **KMS**：多租戶軟體管理的金鑰服務，AWS 管理底層硬體，使用簡單，成本低
- **CloudHSM**：客戶專屬實體硬體，客戶完全控制金鑰，合規要求更嚴格，成本較高

---

## Questions (6–10)

(6) secure online data transfer tool that can automate ongoing transfers from on-premises while providing support for incremental data backups
Ans: AWS DataSync

(7) recommendations in the Operational Excellence pillar of AWS Well-Architected Framework
Ans: Anticipate failure / Make frequent, small, reversible changes

(8) set up an AWS managed VPN — which item needs to be set up on the company's side
Ans: A customer gateway（客戶閘道）

(9) keep sensitive data in its own data center due to compliance but wants to deploy AWS resources
Ans: Hybrid Cloud（混合雲）

(10) is NOT a feature of Amazon Inspector
Ans: Track configuration changes（追蹤組態變更）

---

(6)
中文題目：哪項 AWS 服務是安全的線上資料傳輸工具，可自動化從本地端持續傳輸，並支援增量資料備份？
答案：AWS DataSync
解析：**AWS DataSync** 是線上資料傳輸服務，專為持續性、自動化傳輸設計：
- 支援從本地端 NAS、NFS、SMB 伺服器傳輸至 S3、EFS、FSx
- **增量傳輸（Incremental）**：只傳輸有變更的資料，節省頻寬
- **自動化排程**：設定後定期自動執行，無需人工觸發
- 傳輸過程加密，並驗證資料完整性
與 **Snowball** 差異：Snowball 適合大量離線遷移；DataSync 適合線上持續同步與增量備份。

(7)
中文題目：AWS Well-Architected Framework 卓越營運支柱（Operational Excellence）提出哪些建議？
答案：預期故障會發生（Anticipate failure）/ 頻繁進行小型且可逆的變更（Make frequent, small, reversible changes）
解析：**Operational Excellence 支柱**的五大設計原則：
- **以程式碼執行操作**：IaC、自動化運維
- **頻繁進行小型、可逆的變更**：降低每次變更的風險，出錯時可快速回滾
- **持續改進營運程序**：定期演練與優化
- **預期故障**：主動設計容錯機制，提前演練故障場景（Chaos Engineering）
- **從所有操作故障中學習**：建立事後回顧（Post-Mortem）文化

(8)
中文題目：設定 AWS 受管 VPN 時，企業端需要設定哪個元件？
答案：A customer gateway（客戶閘道）
解析：**AWS Site-to-Site VPN** 雙端元件：
- **AWS 端**：**Virtual Private Gateway（VGW）** 或 **Transit Gateway**，由 AWS 部署與管理
- **企業端（客戶側）**：**Customer Gateway（CGW）**，代表企業本地路由器或防火牆的 AWS 資源物件，需提供企業端設備的公有 IP 位址與 BGP ASN
企業只需在 AWS Console 建立 CGW 物件並設定本地路由器即可，VPN 隧道的 AWS 側由 AWS 自動管理。

(9)
中文題目：企業因合規需求必須將敏感資料保存在自有資料中心，同時又想部署 AWS 資源，這屬於哪種雲端架構？
答案：Hybrid Cloud（混合雲）
解析：**混合雲（Hybrid Cloud）** 同時使用本地端資料中心與公有雲：
- 本地端：存放敏感資料、滿足合規（資料主權、隱私法規）
- AWS Cloud：運行應用程式層、非敏感工作負載、彈性擴展
- 連接方式：**AWS Direct Connect**（專線）或 **Site-to-Site VPN**
常見合規驅動場景：金融、醫療、政府機構因法規要求部分資料不能離開特定地理位置，但希望利用雲端的彈性與服務。

(10)
中文題目：哪項功能**不是** Amazon Inspector 的特性？
答案：Track configuration changes（追蹤組態變更）
解析：**Amazon Inspector 的實際功能**：
- 自動化安全評估（EC2 OS 漏洞、Lambda 套件漏洞、ECR 容器映像掃描）
- 產生安全發現（Security Findings）報告
- 持續監控並偵測新的 CVE

**追蹤組態變更**是 **AWS Config** 的功能，而非 Inspector：
- **Inspector**：安全漏洞掃描（Vulnerability Assessment）
- **AWS Config**：資源組態變更歷史追蹤與合規評估
兩者常被混淆，關鍵差異在於 Inspector 關注安全漏洞，Config 關注組態狀態。

---

## Questions (11–15)

(11) primary use case for Amazon GuardDuty
Ans: Detecting malicious activity and threats in your AWS accounts and workloads

(12) billing timeframe applied when running a Windows EC2 On-Demand instance
Ans: Pay per second（按秒計費）

(13) can send, store, and receive messages between software components to decouple application tiers
Ans: Amazon Simple Queue Service (Amazon SQS)

(14) Total Cost of Ownership (TCO) estimate when moving to AWS
Ans: Server administration / Power/Cooling

(15) quickly add user sign-up, sign-in, and access control to web and mobile applications
Ans: Amazon Cognito

---

(11)
中文題目：Amazon GuardDuty 的主要使用案例為何？
答案：偵測 AWS 帳戶與工作負載中的惡意活動與威脅
解析：**Amazon GuardDuty** 是全受管的威脅偵測服務，持續分析多種資料來源：
- **AWS CloudTrail**：偵測異常 API 呼叫、未授權存取
- **VPC Flow Logs**：識別可疑網路流量（埠掃描、C&C 通訊）
- **DNS 日誌**：偵測與惡意網域的通訊
- **S3 資料事件**：識別異常資料存取行為
常見威脅偵測：加密貨幣挖礦、憑證洩露使用、資料外洩嘗試、勒索軟體行為
無需部署任何 Agent，幾分鐘內即可啟用，是 AWS 威脅情報的核心服務。

(12)
中文題目：執行 Windows EC2 On-Demand 執行個體時，適用哪種計費時間框架？
答案：按秒計費（Pay per second）
解析：**EC2 計費粒度**：
- **Linux 執行個體**：按**秒**計費，最低 60 秒
- **Windows 執行個體**：按**秒**計費（2017 年 10 月起 Windows 也改為按秒計費）
注意：早期版本的題目可能顯示 Windows 按小時計費（舊規則），但 AWS 現已統一 Linux 與 Windows 皆按秒計費，最低收費 60 秒。若考試題目選項只有「per hour」或「per second」，現行正確答案為 **per second**。

(13)
中文題目：哪項 AWS 服務可在軟體元件之間傳送、儲存與接收訊息，以解耦應用程式層？
答案：Amazon Simple Queue Service，Amazon SQS
解析：**Amazon SQS** 是完全受管的訊息佇列服務，解耦架構的核心工具：
- **生產者（Producer）**：將訊息放入佇列，無需等待消費者回應
- **消費者（Consumer）**：從佇列取出訊息獨立處理
- 兩端**完全解耦**：生產者與消費者可獨立擴展、部署、升級
- 支援兩種模式：Standard Queue（高吞吐、至少一次傳遞）和 FIFO Queue（嚴格順序、恰好一次傳遞）
題目關鍵字「send, store, receive messages + decouple」完全對應 SQS 的設計目標。

(14)
中文題目：計算遷移至 AWS 的總持有成本（TCO）估算時，哪些項目應納入考量？
答案：伺服器管理（Server administration）/ 電力與冷卻（Power/Cooling）
解析：**TCO 分析**比較本地端與雲端的完整成本：
本地端通常被低估的隱性成本：
- **伺服器管理**：IT 人員薪資、系統管理、修補與維護的人力成本
- **電力與冷卻**：資料中心的電費、空調、UPS 電源等基礎設施成本
- 其他：機房租金、硬體採購折舊、網路設備
遷移至 AWS 後，以上成本皆由 AWS 承擔，客戶改為按使用量付費的 OpEx 模式，TCO 往往大幅降低。

(15)
中文題目：哪項 AWS 服務可快速為 Web 與行動應用程式新增使用者註冊、登入與存取控制功能？
答案：Amazon Cognito
解析：**Amazon Cognito** 是 AWS 的身份驗證即服務（Identity as a Service）：
- **User Pools（使用者池）**：處理使用者註冊、登入、密碼管理、MFA、電子郵件驗證
- **Identity Pools（身份池）**：授予已認證使用者存取 AWS 資源的臨時憑證
- 支援社交登入（Google、Facebook、Apple）與 SAML/OIDC 企業身份提供者
- 可擴展至數百萬使用者，無需自建身份驗證基礎設施
題目關鍵字「user sign-up, sign-in, access control」精確對應 Cognito User Pools 的核心功能。

---

## Questions (16–20)

(16) enable customized content suggestions for its movie streaming platform
Ans: Amazon Personalize

(17) Amazon EBS snapshots are stored in which AWS service
Ans: Amazon Simple Storage Service (Amazon S3)

(18) has trouble identifying and protecting sensitive data at scale
Ans: Amazon Macie

(19) implement Chaos Engineering to expose blind spots that can disrupt application resiliency
Ans: AWS Fault Injection Simulator (AWS FIS)

(20) serverless service that allows you to prepare data for analytics
Ans: AWS Glue

---

(16)
中文題目：哪項 AWS 服務可為電影串流平台啟用個人化內容推薦？
答案：Amazon Personalize
解析：**Amazon Personalize** 是全受管的機器學習推薦系統服務：
- 使用與 Amazon.com 相同的推薦演算法技術
- 根據使用者行為（瀏覽、點擊、評分）即時生成個人化推薦
- 無需機器學習專業知識，透過 API 即可整合
- 適用場景：電影/音樂/商品推薦、個人化搜尋排序、行銷電子郵件個人化
題目關鍵字「customized content suggestions + streaming platform」直接對應 Amazon Personalize 的核心使用案例。

(17)
中文題目：Amazon EBS Snapshot 儲存在哪項 AWS 服務中？
答案：Amazon Simple Storage Service，Amazon S3
解析：**EBS Snapshot** 的儲存機制：
- EBS 快照儲存於 **Amazon S3**，但為 AWS 管理的私有儲存桶（客戶無法在 S3 Console 直接看到）
- 採用**增量儲存（Incremental）**：第一次快照為完整備份，後續只儲存變更的區塊
- 可跨 Region 複製快照，用於災難復原或 AMI 跨 Region 部署
- 快照可用於還原 EBS Volume 或建立新 Volume，是 EBS 資料保護的核心機制

(18)
中文題目：哪項 AWS 服務可協助企業大規模識別並保護敏感資料？
答案：Amazon Macie
解析：**Amazon Macie** 是機器學習驅動的資料安全服務：
- 自動掃描 **Amazon S3** 儲存桶，識別敏感資料
- 可偵測：PII（個人識別資訊）、財務資料、憑證、醫療資訊
- 持續監控 S3 存取模式，發現異常行為（如大量下載）時發出警示
- 產生詳細的資料發現報告，協助滿足 GDPR、HIPAA 等合規需求
題目關鍵字「identifying and protecting sensitive data at scale」精確對應 Macie 的核心功能。

(19)
中文題目：哪項 AWS 服務可實施混沌工程（Chaos Engineering），暴露影響應用程式韌性的盲點？
答案：AWS Fault Injection Simulator，AWS FIS
解析：**AWS Fault Injection Simulator（FIS）** 是受管的混沌工程服務：
- 在受控環境中注入故障（如終止 EC2 執行個體、增加網路延遲、模擬 AZ 中斷）
- 觀察系統在故障條件下的行為，識別韌性弱點
- 支援預定義的故障場景（Experiment Templates）
- 整合 CloudWatch 監控，確保故障注入在安全範圍內
混沌工程的目標：在可控情境下主動引發故障，確保系統在真實故障時能夠正常恢復，是 Operational Excellence 的重要實踐。

(20)
中文題目：哪項無伺服器 AWS 服務可讓你為分析準備資料？
答案：AWS Glue
解析：**AWS Glue** 是全受管的無伺服器 ETL（Extract, Transform, Load）服務：
- **資料目錄（Data Catalog）**：自動探索並記錄資料結構（Schema）
- **ETL 作業**：轉換、清洗、整合來自不同來源的資料，準備供分析使用
- **無伺服器**：無需管理基礎設施，依需求自動擴展
- 與 **Amazon Athena、Redshift、S3** 原生整合
- 支援 Python（PySpark）與 Scala 腳本
題目關鍵字「serverless + prepare data for analytics」直接對應 AWS Glue 的核心定位。

---

## Questions (21–25)

(21) build a chatbot using Natural Language Understanding (NLU)
Ans: Amazon Lex

(22) provided by Amazon Route 53
Ans: Domain registration / Health checks and monitoring

(23) reserve EC2 capacity for 3 years and plans to increase workloads
Ans: Convertible Reserved Instance (RI)

(24) length terms available for Amazon EC2 Reserved Instances (RI)
Ans: 1 year / 3 years

(25) AWS Shared Responsibility Model — both the responsibility of AWS and the customer
Ans: Configuration management / Operating system (OS) configuration

---

(21)
中文題目：哪項 AWS 服務可用於建立使用自然語言理解（NLU）的聊天機器人？
答案：Amazon Lex
解析：**Amazon Lex** 是建立對話介面（聊天機器人、語音機器人）的 AI 服務：
- 使用與 Amazon Alexa 相同的深度學習技術
- 支援**自然語言理解（NLU）**：理解使用者意圖（Intent）與實體（Entity）
- 支援文字與語音輸入
- 可整合 Lambda 執行業務邏輯，串接 CRM、資料庫等後端系統
- 部署至 Web、Mobile App、Facebook Messenger、Slack 等多種管道
題目關鍵字「chatbot + NLU」直接對應 Amazon Lex。

(22)
中文題目：Amazon Route 53 提供哪些功能？
答案：網域名稱註冊（Domain registration）/ 健康檢查與監控（Health checks and monitoring）
解析：**Amazon Route 53** 提供三大核心功能：
- **DNS 服務**：將網域名稱解析為 IP 位址，支援多種路由政策（Weighted、Latency、Failover、Geolocation 等）
- **網域名稱註冊（Domain Registration）**：可直接透過 Route 53 購買與管理網域
- **健康檢查（Health Checks）**：定期探測端點可用性，與 DNS 路由整合，自動將流量從不健康端點切換至健康端點
Route 53 是 AWS 全球性的 DNS 服務，SLA 保證 100% 可用性。

(23)
中文題目：企業需要預留 EC2 容量達 3 年，且計劃未來增加工作負載，應選擇哪種 RI 類型？
答案：Convertible Reserved Instance，可轉換預留執行個體
解析：**EC2 RI 兩大類型**比較：
- **Standard RI**：折扣最高（最高 72%），但**不能**變更執行個體系列、OS 或租用方式，靈活性低
- **Convertible RI**：折扣稍低（最高 66%），但**可以**在合約期間變更執行個體類型、系列、OS，靈活性高
題目關鍵字「plans to increase workloads（計劃增加工作負載）」意味著未來可能需要更大的執行個體類型，**Convertible RI** 允許在合約期內升級執行個體規格，最適合此場景。

(24)
中文題目：Amazon EC2 Reserved Instance 提供哪些期限選項？
答案：1 年 / 3 年
解析：**EC2 RI 期限選項**：
- **1 年期**：折扣較小（約 40%），適合短期承諾
- **3 年期**：折扣最大（最高 72%），適合長期穩定工作負載
兩種期限各可選擇：No Upfront（零預付）、Partial Upfront（部分預付）、All Upfront（全額預付），付款方式影響折扣幅度（全額預付折扣最高）。AWS 不提供 2 年期 RI，只有 1 年與 3 年兩種選項。

(25)
中文題目：在 AWS 共同責任模型中，哪些是 AWS 與客戶**共同**負責的事項？
答案：組態管理（Configuration management）/ 作業系統設定（Operating system configuration）
解析：**共同責任的灰色地帶**：
- **Configuration Management（組態管理）**：AWS 負責底層硬體與網路設備的組態；客戶負責 Guest OS、應用程式、AWS 服務的組態設定，兩者各管一層
- **OS Configuration（OS 設定）**：受管服務（如 RDS）的 OS 由 AWS 管理；EC2 的 Guest OS 由客戶管理，根據服務類型責任歸屬不同
這些項目無法明確歸屬單一方，體現了共同責任模型的彈性與情境依賴性。

---

## Questions (26–30)

(26) subscribe to an RSS feed to be notified of the status of all AWS service interruptions
Ans: AWS Health Dashboard — Service Health

(27) simplify access management to multiple AWS accounts and facilitate AWS Single Sign-On
Ans: AWS IAM Identity Center

(28) define AWS infrastructure using popular programming languages such as Python and JavaScript
Ans: AWS Cloud Development Kit (AWS CDK)

(29) AWS Shared Responsibility Model — responsibilities of AWS
Ans: Network operability / Data center security

(30) wants to automate code reviews to improve code quality
Ans: Amazon CodeGuru

---

(26)
中文題目：哪項 AWS 服務支援訂閱 RSS Feed 以接收所有 AWS 服務中斷狀態通知？
答案：AWS Health Dashboard — Service Health（服務健康儀表板）
解析：**AWS Health Dashboard — Service Health**：
- 公開頁面（service.aws.amazon.com/health），顯示所有 AWS 服務在所有 Region 的即時狀態
- 提供 **RSS Feed 訂閱**，讓使用者透過 RSS 閱讀器接收服務中斷與恢復通知
- 歷史事件記錄可供查閱
與 **Your Account Health Dashboard** 差異：後者顯示影響**你帳戶**的特定事件，不提供 RSS；Service Health 顯示全 AWS 服務狀態，支援 RSS 訂閱。

(27)
中文題目：哪項 AWS 服務可簡化多帳戶存取管理並提供 AWS 單一登入（AWS SSO）功能？
答案：AWS IAM Identity Center（前稱 AWS SSO）
解析：**AWS IAM Identity Center** 是 AWS 的集中式身份與存取管理服務：
- 提供**單一登入（SSO）**：使用者只需一次登入即可存取多個 AWS 帳戶與業務應用程式
- 集中管理多個 AWS 帳戶的存取權限（與 AWS Organizations 整合）
- 支援外部身份提供者（IdP）：Active Directory、Okta、Azure AD 等
- 提供使用者入口網站，列出所有可存取的帳戶與應用程式
是大型組織管理多帳戶存取的最佳實踐工具。

(28)
中文題目：哪項 AWS 服務允許使用 Python、JavaScript 等熱門程式語言定義 AWS 基礎設施？
答案：AWS Cloud Development Kit，AWS CDK
解析：**AWS CDK** 是開源的基礎設施即程式碼（IaC）框架：
- 使用**熟悉的程式語言**定義 AWS 資源：Python、TypeScript/JavaScript、Java、C#、Go
- 在底層將程式碼合成為 **CloudFormation 範本**並部署
- 支援物件導向設計，可建立可重用的基礎設施元件（Constructs）
與 **CloudFormation** 差異：CloudFormation 使用 JSON/YAML 宣告式模板；CDK 使用程式語言的命令式方式，更適合熟悉開發的工程師。

(29)
中文題目：在 AWS 共同責任模型中，哪些屬於 AWS 的責任？
答案：網路可操作性（Network operability）/ 資料中心安全（Data center security）
解析：**AWS 的責任（Security OF the Cloud）**涵蓋所有底層基礎設施：
- **Network operability**：AWS 全球骨幹網路的運作、維護與安全，確保服務可連線性
- **Data center security**：實體資料中心的門禁控管、監控攝影機、生物辨識、防災措施
客戶無需（也無法）存取這些底層設施，完全由 AWS 負責，這是雲端「無需管理實體基礎設施」核心優勢的體現。

(30)
中文題目：哪項 AWS 服務可自動化程式碼審查以提升程式碼品質？
答案：Amazon CodeGuru
解析：**Amazon CodeGuru** 是 AI 驅動的程式碼品質工具，分為兩個元件：
- **CodeGuru Reviewer**：自動分析 Pull Request，提供程式碼品質建議，識別安全漏洞、效能問題、最佳實踐偏差
- **CodeGuru Profiler**：分析應用程式執行時的效能瓶頸，識別 CPU 使用率最高的程式碼行，建議優化方案
支援 Java 與 Python，與 GitHub、CodeCommit、Bitbucket 整合，讓程式碼審查自動化，減少人工 Code Review 的負擔。

---

## Questions (31–35)

(31) employees travel to different offices around the world — how should they set up AWS accounts
Ans: There is nothing to do — AWS IAM is a global service

(32) inspect Amazon CloudFront distributions running on any HTTP web server
Ans: AWS Web Application Firewall (AWS WAF)

(33) recommended in the Security pillar of Well-Architected Framework
Ans: Use AWS KMS to encrypt data

(34) be notified in case of a configuration change for security and compliance reasons
Ans: AWS Config

(35) help with fault tolerance
Ans: Replacing unhealthy Amazon EC2 instances（替換不健康的 EC2 執行個體）

---

(31)
中文題目：企業遷移至 AWS 後，員工在世界各地辦公室出差時應如何設定 AWS 帳戶？
答案：無需任何額外設定——AWS IAM 是全球性服務
解析：**AWS IAM 是全球服務（Global Service）**：
- IAM 使用者、群組、角色、政策在帳戶建立後即可在**所有 AWS Region** 中使用
- 無論員工在哪個國家的辦公室，都使用相同的 IAM 憑證存取 AWS
- 不需要為不同地理位置的辦公室建立不同的 IAM 設定
- 僅需確保 IAM 政策設定正確、MFA 啟用即可
這與 EC2、S3 等 Regional 服務不同，IAM 不需要在每個 Region 分別設定。

(32)
中文題目：哪項 AWS 服務可檢查在任何 HTTP Web 伺服器上運行的 Amazon CloudFront 發布？
答案：AWS Web Application Firewall，AWS WAF
解析：**AWS WAF** 可部署於 CloudFront 前端：
- 在 CloudFront 邊緣節點（Edge Location）層級過濾惡意 HTTP/HTTPS 請求
- 請求在到達源站（Origin）之前就被 WAF 規則評估，惡意流量在邊緣即被封鎖
- 可保護任何透過 CloudFront 分發的 Web 應用程式（無論源站是 EC2、S3、ALB 或任何 HTTP 伺服器）
- 支援 SQL Injection、XSS、Bot 防護、IP 封鎖等規則

(33)
中文題目：AWS Well-Architected Framework 安全性支柱（Security Pillar）建議哪項最佳實踐？
答案：使用 AWS KMS 加密資料
解析：**Security Pillar** 的七大設計原則中，**資料保護**是核心之一：
- **靜態資料加密（Encryption at Rest）**：使用 **AWS KMS** 管理加密金鑰，加密 S3 物件、EBS Volume、RDS 資料庫
- **傳輸中加密（Encryption in Transit）**：使用 TLS/SSL 保護資料傳輸
- 最小權限存取資料
AWS KMS 是安全支柱中最常被引用的加密服務，提供集中式金鑰管理，與大多數 AWS 服務原生整合。

(34)
中文題目：哪項 AWS 服務可在資源組態發生變更時發送通知，以滿足安全與合規需求？
答案：AWS Config
解析：**AWS Config** 持續監控資源組態並在變更時採取行動：
- 偵測資源組態變更事件
- 評估是否符合自訂合規規則（Config Rules）
- 可透過 **SNS** 發送通知，或透過 **EventBridge** 觸發自動修復
- 提供組態變更時間軸，可還原查閱任意時間點的資源狀態
題目關鍵字「notified in case of a configuration change + security and compliance」完全對應 Config 的核心使用場景。

(35)
中文題目：哪項機制有助於實現容錯（Fault Tolerance）？
答案：替換不健康的 Amazon EC2 執行個體
解析：**容錯（Fault Tolerance）** 指系統在元件故障時仍能繼續運作，透過**冗餘與自動修復**實現：
- **Auto Scaling 的健康檢查**：偵測不健康的 EC2 執行個體並自動終止，啟動新的健康執行個體替換
- **ELB 健康檢查**：停止將流量路由至不健康的執行個體
- **RDS Multi-AZ**：主要執行個體故障時自動切換至備用副本
「替換不健康執行個體」是 Auto Scaling 自動修復（Auto Healing）功能的體現，確保系統始終有足夠的健康容量，是容錯架構的核心機制。

---

## Questions (36–40)

(36) launch a dev/test environment with low monthly pricing
Ans: Amazon Lightsail

(37) define a set of rules to manage objects cost-effectively between S3 storage classes
Ans: Amazon S3 Lifecycle configuration

(38) store secondary backup copies of on-premises data — cost-optimal yet provides rapid access
Ans: Amazon S3 One Zone-Infrequent Access

(39) CORRECT regarding the scope of an Amazon VPC
Ans: A VPC spans all Availability Zones (AZs) within an AWS Region

(40) create and provide trusted users with temporary security credentials
Ans: AWS Security Token Service (AWS STS)

---

(36)
中文題目：哪項 AWS 服務適合以低月費啟動開發/測試環境？
答案：Amazon Lightsail
解析：**Amazon Lightsail** 是 AWS 的簡化雲端服務，專為個人開發者、小型企業與入門使用者設計：
- **低月費固定方案**（從 $3.5/月起），包含運算、儲存、資料傳輸
- 簡化的管理介面，無需深入了解 AWS 複雜設定
- 適合：個人網站、Blog、WordPress、開發測試環境
- 包含：虛擬機器（類 EC2）、管理資料庫、負載平衡器、CDN
與 EC2 差異：Lightsail 固定費率、設定簡單；EC2 彈性高、設定複雜，適合企業級生產環境。

(37)
中文題目：哪項 AWS 功能可定義規則，在 S3 儲存類別之間以符合成本效益的方式管理物件？
答案：Amazon S3 Lifecycle configuration（S3 生命週期設定）
解析：**S3 Lifecycle Configuration** 透過自動化規則管理物件的儲存類別轉換：
- **Transition Actions（轉換動作）**：如建立後 30 天移至 Standard-IA，90 天移至 Glacier
- **Expiration Actions（到期動作）**：在指定天數後自動刪除物件或舊版本
- 無需人工介入，系統自動執行
典型成本優化生命週期：Standard → Standard-IA（30天）→ Glacier Flexible Retrieval（90天）→ Glacier Deep Archive（180天）→ 自動刪除
使資料隨時間老化而自動降至更低成本的儲存層。

(38)
中文題目：混合雲企業想儲存本地端資料的次要備份副本，需要符合成本效益且可快速存取，應選擇哪種 S3 儲存類別？
答案：Amazon S3 One Zone-Infrequent Access，S3 One Zone-IA
解析：本題的三個條件分析：
- **次要備份（Secondary Backup）**：即使資料遺失也有主要備份可恢復，容忍單 AZ 故障風險
- **符合成本效益（Cost-Optimal）**：One Zone-IA 比 Standard-IA 便宜約 20%
- **快速存取（Rapid Access）**：毫秒級存取，無需等待（不同於 Glacier）
S3 One Zone-IA 的低可用性（單 AZ）風險對於「次要備份」場景可接受，且同時滿足低成本與快速存取的需求，是最佳選擇。

(39)
中文題目：關於 Amazon VPC 的範圍，哪個描述是正確的？
答案：VPC 跨越 AWS Region 內的**所有**可用區（AZ）
解析：**VPC 的範圍架構**：
- **VPC**：Region 層級，自動涵蓋該 Region 的所有 AZ
- **Subnet**：AZ 層級，每個子網路只存在於單一 AZ 內
- **最佳實踐**：在每個 AZ 各建立 Public 與 Private Subnet，確保高可用性
VPC 本身的 IP 位址範圍（CIDR）跨越整個 Region，子網路是 VPC CIDR 的細分，分配至各 AZ。一個 VPC 可包含多個 AZ 中的多個子網路。

(40)
中文題目：哪項 AWS 服務可建立並提供受信任使用者臨時安全憑證？
答案：AWS Security Token Service，AWS STS
解析：**AWS STS** 是 IAM 的核心元件，提供短期臨時憑證：
- **臨時憑證**：包含 Access Key ID、Secret Access Key、Session Token，有效期可設定（15 分鐘至 36 小時）
- **常見使用場景**：
  - **AssumeRole**：EC2 或 Lambda 假設 IAM Role 取得臨時存取權
  - **Cross-Account Access**：跨帳號存取
  - **Federation**：企業身份（AD、SAML）對應至 AWS 臨時憑證
臨時憑證自動過期，相較於長期 Access Key 安全性更高，是 AWS 身份存取的最佳實踐。

---

## Questions (41–45)

(41) INCORRECT regarding Amazon EBS Elastic Volumes
Ans: "Amazon EBS Elastic Volumes can be bound to several Availability Zones (AZs)"

(42) experiencing a read-intensive workload and wants to take the load off databases
Ans: Amazon ElastiCache

(43) monitor costs and choose an optimal Savings Plan
Ans: AWS Cost Explorer

(44) to review permissions granted to an IAM user
Ans: AWS IAM Access Advisor

(45) provide best practice recommendations for performance, service limits, and cost optimization
Ans: AWS Trusted Advisor

---

(41)
中文題目：關於 Amazon EBS Elastic Volumes，哪個描述是**錯誤的**？
答案：「Amazon EBS Elastic Volumes 可以綁定到多個可用區（AZ）」——此為錯誤說法
解析：**EBS Volume 的 AZ 限制**：
- EBS Volume **只能存在於單一 AZ**，且只能掛載至**同一 AZ** 的 EC2 執行個體
- 無法跨 AZ 掛載或綁定
**EBS Elastic Volumes** 的實際功能是允許在**不中斷服務的情況下**動態修改：
- 增加 Volume 大小（只能增加，不能縮小）
- 更改 Volume 類型（如從 gp2 升級至 gp3）
- 調整 IOPS 與吞吐量設定
「綁定多個 AZ」是錯誤描述，EBS 永遠是單一 AZ 的資源。

(42)
中文題目：企業面臨讀取密集型工作負載，想要減輕資料庫的讀取壓力，應使用哪項服務？
答案：Amazon ElastiCache
解析：**Amazon ElastiCache** 是記憶體快取服務，用於分擔資料庫讀取壓力：
- 將頻繁查詢的結果快取於記憶體，後續相同查詢直接從快取返回，無需再查資料庫
- 延遲從毫秒降至微秒，吞吐量大幅提升
- 支援 **Redis** 和 **Memcached**
- 適合：Session 快取、資料庫查詢結果、排行榜、即時計數器
題目關鍵字「read-intensive workload + take the load off databases」對應 ElastiCache 的核心使用場景。

(43)
中文題目：哪項 AWS 服務可監控費用並選擇最佳的 Savings Plans？
答案：AWS Cost Explorer
解析：**AWS Cost Explorer** 提供 Savings Plans 最佳化功能：
- **Savings Plans 建議**：分析過去 7/30/60 天的 EC2 使用模式，計算最佳的 Savings Plans 購買金額與類型
- **費用視覺化**：以圖表呈現歷史費用趨勢，識別費用異常
- **預測**：預估未來 12 個月費用
- **Coverage Report**：顯示哪些使用量已被 Savings Plans 覆蓋，哪些還是 On-Demand
幫助企業做出有資料支撐的 Savings Plans 購買決策。

(44)
中文題目：哪項 AWS 工具可審查授予 IAM 使用者的權限？
答案：AWS IAM Access Advisor（IAM 存取顧問）
解析：**AWS IAM Access Advisor** 提供權限使用情況的可見性：
- 顯示 IAM 使用者、群組或角色被授予哪些服務的存取權限
- 顯示**最後存取各服務的時間（Last Accessed）**
- 協助識別**未使用的權限**（長期未使用的服務存取），以便移除，實踐最小權限原則
與 **Credentials Report** 差異：Credentials Report 顯示憑證狀態；Access Advisor 顯示**服務層級的存取使用歷史**，是精簡 IAM 權限的重要工具。

(45)
中文題目：哪項 AWS 服務提供效能、服務限制與成本優化方面的最佳實踐建議？
答案：AWS Trusted Advisor
解析：**AWS Trusted Advisor** 分析 AWS 環境並提供五大類別建議：
- **Cost Optimization（成本優化）**：識別閒置資源、RI 購買建議
- **Performance（效能）**：EC2 類型優化、CloudFront 設定建議
- **Security（安全性）**：MFA 啟用、S3 公開存取、安全群組設定
- **Fault Tolerance（容錯）**：Multi-AZ 建議、備份狀態
- **Service Limits（服務限制）**：監控接近 AWS 配額上限的資源
題目提及「performance, service limits, cost optimization」皆屬於 Trusted Advisor 的檢查類別。

---

## Questions (46–50)

(46) run hundreds of thousands of batch computing workloads
Ans: AWS Batch

(47) help optimize Amazon EC2 costs
Ans: Set up Auto Scaling groups to align the number of instances with demand / Purchase Amazon EC2 Reserved Instances (RIs)

(48) wants the fastest migration path and has decided not to update application code or make any architectural changes
Ans: Rehost（重新託管 / Lift & Shift）

(49) deploy the same EC2 instances in eu-south-1
Ans: Amazon Machine Image (AMI)

(50) best practices when using AWS Organizations
Ans: Restrict account privileges using Service Control Policies (SCP) / Create AWS accounts per department

---

(46)
中文題目：哪項 AWS 服務可執行數十萬個批次運算工作負載？
答案：AWS Batch
解析：**AWS Batch** 是全受管的批次運算服務：
- 根據工作負載需求**自動佈建最佳數量與類型的運算資源**（EC2 或 Fargate）
- 支援大規模平行批次作業（數十萬個並行任務）
- 工作完成後自動縮減資源，節省成本
- 支援 Docker 容器化的批次作業
- 適用場景：基因組學分析、財務風險模擬、媒體轉碼、機器學習訓練
與 Lambda 差異：Lambda 最長 15 分鐘，適合短暫事件；AWS Batch 適合長時間、大量的批次計算任務。

(47)
中文題目：哪些方法有助於優化 Amazon EC2 費用？
答案：
- 設定 Auto Scaling 群組使執行個體數量與需求對齊
- 購買 Amazon EC2 Reserved Instance，RI
解析：**EC2 成本優化雙管齊下**：
- **Auto Scaling（動態擴縮）**：需求低時自動縮減執行個體數量，避免為閒置資源付費；需求高時擴展，確保效能，實現精準的供需匹配
- **Reserved Instance（預留承諾）**：對可預測的基礎工作負載購買 RI，節省最高 72%
組合策略：**RI 覆蓋基礎負載（Base Load）+ Spot 覆蓋尖峰 + On-Demand 作為緩衝**，搭配 Auto Scaling 動態管理，是最佳成本架構。

(48)
中文題目：企業想要最快的遷移路徑，且決定不更新應用程式程式碼或進行任何架構變更，這屬於哪種遷移策略？
答案：Rehost（重新託管），又稱 Lift & Shift
解析：**AWS 7R 遷移策略**中：
- **Rehost（Lift & Shift）**：原樣將應用程式遷移至 AWS（如從實體伺服器搬至 EC2），**無需修改程式碼或架構**，遷移速度最快
- **Replatform（Lift, Tinker & Shift）**：少量調整以利用雲端優勢（如改用 RDS）
- **Refactor / Re-architect**：大幅重新設計以充分利用雲端原生功能
題目關鍵字「fastest migration path + no code changes + no architectural changes」精確對應 **Rehost**。

(49)
中文題目：哪項 AWS 服務可用於在 eu-south-1 Region 部署相同的 EC2 執行個體？
答案：Amazon Machine Image，AMI
解析：**跨 Region 部署相同 EC2 的流程**：
1. 從現有 EC2 執行個體建立 **AMI（自訂映像）**
2. **複製 AMI（Copy AMI）** 至目標 Region（eu-south-1）
3. 在目標 Region 使用複製的 AMI 啟動相同配置的 EC2 執行個體
AMI 包含 OS、已安裝的軟體與設定，是確保跨 Region 部署一致性的標準工具。注意：AMI 是 Region 特定資源，必須先複製才能在其他 Region 使用。

(50)
中文題目：使用 AWS Organizations 的最佳實踐為何？
答案：
- 使用服務控制政策（SCP）限制帳戶權限
- 按部門建立 AWS 帳戶
解析：**AWS Organizations 最佳實踐**：
- **Service Control Policies（SCP）**：在組織單位（OU）或帳戶層級設定最大可用權限邊界，即使帳戶內的 IAM 管理員也無法超越 SCP 的限制，是跨帳戶權限治理的核心工具
- **按部門建立獨立帳戶**：實現費用分離（各部門獨立計費）、安全隔離（一個帳戶的資源無法影響另一個帳戶）、合規邊界清晰
兩者是 AWS 多帳戶治理架構的基礎原則。

---

## Questions (51–55)

(51) the advantages of using the AWS Cloud
Ans: Stop guessing about capacity / Increase speed and agility

(52) the benefits of using AWS Elastic Load Balancing (ELB)
Ans: Fault tolerance（容錯）/ High availability（高可用性）

(53) create a private, high bandwidth network connection between its on-premises data centers and AWS Cloud
Ans: AWS Direct Connect

(54) deploy identical resources across all AWS regions and accounts using templates and estimate costs
Ans: AWS CloudFormation

(55) AWS Shared Responsibility Model — responsibility of the customer
Ans: Firewall & networking configuration of Amazon EC2

---

(51)
中文題目：哪些是使用 AWS Cloud 的優勢？
答案：停止猜測基礎設施容量（Stop guessing about capacity）/ 提升速度與敏捷性（Increase speed and agility）
解析：AWS 六大雲端優勢：
- **Stop guessing capacity**：雲端可按需擴縮，無需預先估算並採購容量，避免過度配置（浪費）或配置不足（效能問題）
- **Increase speed and agility**：幾分鐘內即可取得資源，加速創新週期，縮短從構想到上市的時間
- 其他優勢：Trade CapEx for OpEx、Benefit from economies of scale、Stop spending money on data centers、Go global in minutes

(52)
中文題目：使用 AWS Elastic Load Balancing（ELB）有哪些優勢？
答案：容錯（Fault Tolerance）/ 高可用性（High Availability）
解析：**ELB 提供的架構優勢**：
- **Fault Tolerance（容錯）**：ELB 的健康檢查自動偵測並停止將流量路由至不健康的目標，其他健康的執行個體繼續服務，系統不因單點故障而中斷
- **High Availability（高可用性）**：ELB 將流量分散至多個 AZ 的執行個體，即使單一 AZ 故障，流量自動切換至其他 AZ 的健康執行個體
ELB 本身也是多 AZ 高可用設計，AWS 管理其可用性，客戶只需設定目標群組與規則。

(53)
中文題目：哪項 AWS 服務可在本地端資料中心與 AWS Cloud 之間建立私有、高頻寬的網路連線？
答案：AWS Direct Connect
解析：**AWS Direct Connect** 的核心特性：
- **實體專線**：從企業資料中心到 AWS 的專用光纖連線，不經過公共網際網路
- **私有（Private）**：流量完全在私有網路中傳輸，更安全
- **高頻寬**：支援 1 Gbps、10 Gbps、100 Gbps 連線
- **穩定低延遲**：固定頻寬，不受公網擁塞影響
- 適合：大量資料傳輸、對延遲敏感的應用、法規要求不走公網的場景
題目關鍵字「private + high bandwidth」精確對應 Direct Connect。

(54)
中文題目：哪項 AWS 服務可使用範本在所有 AWS Region 與帳戶中部署相同的資源，並估算費用？
答案：AWS CloudFormation
解析：**AWS CloudFormation** 的跨環境部署能力：
- **Infrastructure as Code（IaC）**：以 JSON/YAML 範本定義所有 AWS 資源
- **跨帳戶、跨 Region 部署**：**CloudFormation StackSets** 支援一次性在多個帳戶與 Region 部署相同的 Stack
- **費用估算**：CloudFormation Designer 整合 AWS Pricing Calculator，可在部署前估算費用
- **一致性保證**：所有環境使用相同範本，確保設定一致，防止環境漂移

(55)
中文題目：在 AWS 共同責任模型中，哪項是客戶的責任？
答案：Amazon EC2 的防火牆與網路設定
解析：**EC2 的客戶責任（Security IN the Cloud）**：
- **Security Group（防火牆）**：設定允許哪些 Port、Protocol 和 IP 範圍的流量進出，完全由客戶控制
- **Network ACL**：子網路層級的防火牆規則，由客戶設定
- **VPC 路由表**：定義網路流量路由，客戶設定
- **Guest OS 網路設定**：作業系統內部的網路設定（如 iptables）
AWS 負責底層實體網路基礎設施，但 EC2 的網路安全設定由客戶全權負責。

---

## Questions (56–60)

(56) monitoring can be provided by Amazon CloudWatch
Ans: Application performance / Resource utilization

(57) audit requests made to an S3 bucket
Ans: Amazon S3 Access Logs

(58) view the most comprehensive billing details for the past month
Ans: AWS Cost & Usage Report (AWS CUR)

(59) quickly deploy a popular technology on AWS
Ans: AWS Partner Solutions (formerly Quick Starts)

(60) to build Machine Learning models
Ans: Amazon SageMaker

---

(56)
中文題目：Amazon CloudWatch 可提供哪些監控功能？
答案：應用程式效能（Application performance）/ 資源使用率（Resource utilization）
解析：**Amazon CloudWatch** 是 AWS 的統一監控服務，涵蓋：
- **Resource Utilization（資源使用率）**：EC2 CPU 使用率、記憶體、磁碟 I/O、網路流量；EBS 吞吐量；RDS 連線數等
- **Application Performance（應用程式效能）**：透過自訂指標（Custom Metrics）監控應用程式層面的效能指標（如 API 回應時間、錯誤率）
- **Log Analysis**：CloudWatch Logs 收集與分析日誌
- **Alarms**：設定閾值警示，觸發 SNS 通知或 Auto Scaling 動作
CloudWatch 是 AWS 可觀測性（Observability）的核心工具。

(57)
中文題目：哪項功能可稽核對 S3 儲存桶所發出的請求？
答案：Amazon S3 Access Logs（S3 存取日誌）
解析：**Amazon S3 Access Logs** 記錄對 S3 儲存桶的所有請求明細：
- 記錄內容：請求者、儲存桶名稱、請求時間、動作（GET/PUT/DELETE）、回應狀態碼、傳輸位元組數
- 日誌儲存至指定的 S3 儲存桶（需與來源桶不同）
- 用途：安全稽核、存取模式分析、合規要求
與 **CloudTrail** 差異：CloudTrail 記錄 API 層級的 S3 操作（如管理操作）；S3 Access Logs 記錄物件層級的所有 HTTP 請求，更詳細但不即時。

(58)
中文題目：哪項 AWS 服務可查看過去一個月最完整的帳單明細？
答案：AWS Cost & Usage Report，AWS CUR
解析：**AWS Cost & Usage Report（CUR）** 是 AWS 最詳細的費用報告：
- 提供**最細粒度**的費用與使用量明細（逐小時、逐資源）
- 涵蓋每項 AWS 服務、每個資源的費用細目、標籤、折扣、信用點數
- 匯出至 S3 儲存桶，可用 Athena、Redshift、QuickSight 分析
費用工具比較：
- **Cost Explorer**：視覺化儀表板，適合快速分析
- **Billing Dashboard**：帳單摘要
- **CUR**：最完整的原始明細資料，適合深度自訂分析

(59)
中文題目：哪項 AWS 資源可快速在 AWS 上部署熱門技術？
答案：AWS Partner Solutions（前稱 Quick Starts）
解析：**AWS Partner Solutions（Quick Starts）** 提供：
- 由 AWS 與合作夥伴共同開發的**自動化部署參考架構**
- 以 CloudFormation 範本打包，幾分鐘內即可部署
- 涵蓋熱門技術：SAP、Microsoft SharePoint、Kubernetes、WordPress 等數百種
- 遵循 AWS 最佳實踐，經過安全與效能驗證
讓企業無需從頭設計架構，直接使用經過驗證的範本快速部署標準化解決方案。

(60)
中文題目：哪項 AWS 服務用於建立機器學習（Machine Learning）模型？
答案：Amazon SageMaker
解析：**Amazon SageMaker** 是完整的機器學習平台，覆蓋 ML 生命週期的所有階段：
- **資料準備**：SageMaker Data Wrangler、Feature Store
- **模型訓練**：內建演算法、自訂訓練腳本，支援分散式訓練
- **模型評估**：SageMaker Experiments、Clarify（偏差檢測）
- **模型部署**：SageMaker Endpoints，一鍵部署為 API
- **MLOps**：SageMaker Pipelines，自動化 ML 工作流程
無需管理底層基礎設施，資料科學家可專注於模型開發。

---

## Questions (61–65)

(61) centrally view, manage, and operate nodes to identify issues impacting applications
Ans: AWS Systems Manager

(62) Adding more CPU/RAM to an Amazon EC2 instance
Ans: Vertical scaling（垂直擴展）

(63) when describing AWS Elastic Beanstalk
Ans: It is a Platform as a Service (PaaS) that allows you to deploy and scale web applications and services

(64) remove its need to manage underlying infrastructure and focus on deployment and management of applications
Ans: Platform as a Service (PaaS)

(65) wants to separate cost for AWS services by the department for cost allocation
Ans: Create tags for each department（為每個部門建立標籤）

---

(61)
中文題目：哪項 AWS 服務可集中查看、管理並操作節點，以識別影響應用程式的問題？
答案：AWS Systems Manager
解析：**AWS Systems Manager** 提供統一的基礎設施管理平台：
- **Fleet Manager**：集中查看與管理 EC2 執行個體（節點）的狀態、效能指標、日誌
- **Session Manager**：無需 SSH 即可安全連接至執行個體進行操作
- **Run Command**：跨多個執行個體批量執行命令
- **Patch Manager**：集中管理 OS 修補
- **OpsCenter**：彙整來自 CloudWatch、Config、Trusted Advisor 的問題，集中追蹤與解決
題目關鍵字「centrally view, manage, operate nodes + identify issues」對應 Systems Manager 的 Fleet Manager 與 OpsCenter 功能。

(62)
中文題目：為 Amazon EC2 執行個體增加更多 CPU 或 RAM，這屬於哪種擴展類型？
答案：Vertical scaling（垂直擴展）
解析：兩種擴展類型的對比：
- **Vertical Scaling（垂直擴展 / Scale Up）**：升級單一執行個體的規格（更多 CPU、更大記憶體），如從 t3.medium 升至 t3.2xlarge，有單機上限
- **Horizontal Scaling（水平擴展 / Scale Out）**：增加更多執行個體的數量（多台 t3.medium），理論上無上限，更符合雲端彈性設計原則
AWS 鼓勵**水平擴展**設計，搭配 Auto Scaling 與 ELB，比垂直擴展更具彈性與容錯能力。

(63)
中文題目：哪個描述正確說明了 AWS Elastic Beanstalk？
答案：它是一種 PaaS（平台即服務），讓你能夠部署與擴展 Web 應用程式與服務
解析：**AWS Elastic Beanstalk** 的定位：
- **PaaS（Platform as a Service）**：客戶只需上傳應用程式程式碼，Beanstalk 自動處理底層基礎設施（EC2 佈建、負載平衡、Auto Scaling、監控）
- 支援多種語言：Java、Python、PHP、Node.js、Ruby、.NET、Go、Docker
- 客戶仍可選擇性地存取底層 EC2（保留 IaaS 控制權）
- **免費服務**：只需支付底層 EC2、RDS 等資源的費用
Beanstalk 是 IaaS 與 PaaS 之間的折衷：比 EC2 簡單，比 Lambda 更有控制權。

(64)
中文題目：企業想要移除管理底層基礎設施的需求，專注於應用程式的部署與管理，這對應哪種雲端服務模型？
答案：Platform as a Service，PaaS（平台即服務）
解析：**PaaS** 的核心價值：
- **AWS 管理**：底層硬體、OS、執行環境、中介軟體、網路基礎設施
- **客戶專注**：應用程式程式碼、資料、設定
- AWS PaaS 服務範例：**Elastic Beanstalk**（Web 應用）、**AWS Lambda**（函數）、**Amazon RDS**（資料庫）、**AWS Fargate**（容器）
相比 IaaS（EC2）：PaaS 移除了 OS 管理負擔；相比 SaaS：PaaS 仍需客戶部署應用程式邏輯。

(65)
中文題目：企業想按部門分開 AWS 服務的費用以進行成本分配，應怎麼做？
答案：為每個部門建立標籤（Create tags for each department）
解析：**AWS 資源標籤（Tags）** 是成本分配的核心工具：
- 為每個 AWS 資源加上部門標籤（如 Key: Department, Value: Engineering）
- 在 **AWS Billing Console** 啟用「成本分配標籤（Cost Allocation Tags）」
- 之後在 **AWS Cost Explorer** 或 **Cost & Usage Report** 可依標籤篩選與分組，查看各部門的費用
- 標籤策略建議：制定統一的標籤命名規範，使用 AWS Config Rules 強制執行標籤合規
無需為不同部門建立獨立帳戶，即可實現細粒度的成本追蹤與分配。