# AWS Cloud Practitioner 考題中英對照詳解（第六回）
# AWS Cloud Practitioner Exam Q&A — Bilingual Study Guide (Set 6)

---

## 問題 1 / Question 1

**[題目 / Question]**
A company provides you with a completed product that is run and managed by the company itself. As a customer, you only use the product without worrying about maintaining it. Which cloud computing model does this belong to?
公司提供一個由公司自行執行和管理的完整產品，客戶只需使用而無需擔心維護，這屬於哪種雲端運算模型？

**✅ 正確答案 / Correct Answer：Software as a Service (SaaS)**

**[雲端服務類型三層對照 / Three Cloud Service Layers]**

| 類型 / Type | 客戶管理 / Customer Manages | AWS 範例 |
|---|---|---|
| **SaaS** | **僅使用軟體** | Rekognition、Gmail |
| PaaS | 應用程式 + 資料 | Elastic Beanstalk |
| IaaS | 應用程式 + 資料 + OS + 網路 | Amazon EC2 |

> ⚠️ "Product as a Service (Paas)" 是虛構選項

---

## 問題 2 / Question 2

**[題目 / Question]**
As part of a flexible pricing model, AWS offers two types of Savings Plans. Which are the Savings Plans from AWS?
作為靈活定價模型的一部分，AWS 提供哪兩種 Savings Plans？

**✅ 正確答案 / Correct Answer：Compute Savings Plans, EC2 Instance Savings Plans**

**[AWS 兩種 Savings Plans 比較 / Two Savings Plan Types]**

| 類型 / Type | 折扣 / Discount | 靈活性 / Flexibility | 適用範圍 |
|---|---|---|---|
| **Compute Savings Plans** | **最高 66%** | **最高（最靈活）** | EC2、Fargate、Lambda；任何家族、大小、AZ、Region、OS |
| **EC2 Instance Savings Plans** | **最高 72%** | 中等（特定家族和 Region）| 特定 Region 中特定執行個體家族 |

> ⚠️ 常見錯誤選項："Storage Savings Plans"、"Reserved Instances Savings Plans" 均為虛構選項

---

## 問題 3 / Question 3

**[題目 / Question]**
A company wants to make its desktop applications available from browsers on devices/laptops without procuring servers or maintaining infrastructure. Which AWS service?
公司想讓員工從瀏覽器存取桌面應用程式，無需採購伺服器或維護基礎設施，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：Amazon AppStream 2.0**

**[中文詳解]**
**Amazon AppStream 2.0** 是全托管的非持久性應用程式和桌面串流服務。集中管理桌面應用程式，並安全地將其交付給任何電腦（包括 Chromebook、Mac、PC），無需採購、佈建和操作硬體或基礎設施。

**[AppStream 2.0 vs WorkSpaces 比較 / Comparison]**

| 服務 / Service | 提供內容 | 說明 |
|---|---|---|
| **Amazon AppStream 2.0** | **桌面應用程式串流** | 將**特定應用程式**串流到瀏覽器 |
| Amazon WorkSpaces | **完整桌面環境** | 提供整個虛擬桌面（Windows/Linux）|

---

## 問題 4 / Question 4

**[題目 / Question]**
Which points should be considered when choosing an **AWS Region** for a service? (Select two)
選擇 **AWS Region** 時應考慮哪兩個要點？

**✅ 正確答案 / Correct Answers：**
1. **Compliance and Data Residency** guidelines should match your business requirements（合規和資料駐留要求）
2. **AWS Region chosen should be geographically closer to the user base**（選擇地理位置更靠近用戶群的 Region）

**[選擇 AWS Region 的四大考量 / Four Factors for Region Selection]**

| 考量 / Factor | 說明 |
|---|---|
| ✅ **合規和資料駐留** | 資料必須存放在特定地理位置 |
| ✅ **地理位置接近用戶** | 降低延遲 |
| ✅ 服務可用性 | 不是所有服務在每個 Region 都可用 |
| ✅ 成本 | 不同 Region 定價不同 |

> ❌ 高可用性指數、5G 網路、AZ 在 100km 範圍內 → 均為錯誤選項（所有 Region 都具備高可用性）

---

## 問題 5 / Question 5

**[題目 / Question]**
A company is moving its CRM application running on MySQL to an AWS database service. Which is the right database service?
公司想將 MySQL 上的 CRM 應用程式遷移到 AWS 資料庫服務，哪個服務最合適？

**✅ 正確答案 / Correct Answer：Amazon Aurora**

**[中文詳解]**
**Amazon Aurora** 是相容 MySQL 和 PostgreSQL 的關聯式資料庫引擎，提供高端商業資料庫的速度和可靠性，以及開源資料庫的簡單性和成本效益。Aurora MySQL 效能比 MySQL 高達 5 倍。可使用 `mysqldump`/`mysqlimport` 工具從 MySQL 遷移資料。

**[資料庫服務選擇 / Database Selection]**

| 服務 / Service | 類型 / Type | 適用 MySQL 遷移 |
|---|---|---|
| **Amazon Aurora** | **關聯式（MySQL 相容）** | **✅ 最佳** |
| Amazon RDS for MySQL | 關聯式 | ✅ 可以 |
| Amazon DynamoDB | NoSQL 鍵值 | ❌ |
| Amazon Neptune | 圖形資料庫 | ❌ |
| Amazon ElastiCache | 記憶體快取 | ❌ |

---

## 問題 6 / Question 6

**[題目 / Question]**
A team manager needs data about **configuration changes** for AWS resources in his account during the past two weeks. Which AWS service?
團隊管理員需要過去兩週 AWS 帳戶中資源的**配置變更**資料，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Config**

**[Config vs CloudTrail 的關鍵區別 / Key Difference]**

| 問題 / Question | 使用服務 / Service |
|---|---|
| **"我的 AWS 資源看起來像什麼？"** | **AWS Config（配置歷史）** |
| **"誰做了 API 呼叫修改了這個資源？"** | **AWS CloudTrail（活動審計）** |

---

## 問題 7 / Question 7

**[題目 / Question]**
Which service offers a **graphical user interface to manage AWS Snowball devices** without needing command-line interface or REST APIs?
哪個服務提供**圖形使用者介面來管理 AWS Snowball 設備**，無需命令列介面或 REST API？

**✅ 正確答案 / Correct Answer：AWS OpsHub**

**[中文詳解]**
**AWS OpsHub** 是圖形使用者介面，可管理 AWS Snowball 設備，無需網路連接。功能包括：解鎖和配置設備、拖放資料到設備、啟動應用程式、監控設備指標。在筆記型電腦上下載安裝後即可使用。

---

## 問題 8 / Question 8

**[題目 / Question]**
An e-commerce company needs to generate **custom reports and interactive dashboards** for analyzing product sales data. The dashboards need to be **accessible from any device**. Which AWS service?
電商公司需要生成自定義報告和**互動式儀表板**分析銷售資料，儀表板需要**從任何設備存取**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：Amazon QuickSight**

**[中文詳解]**
**Amazon QuickSight** 是可擴展、無伺服器、可嵌入、ML 驅動的雲端商業智慧 (BI) 服務。可快速建立和發布包含 ML 驅動洞察的互動式 BI 儀表板，可從任何設備存取，按會話定價（只有用戶存取時才付費）。

**[數據分析工具對比 / Data Analysis Tools]**

| 服務 / Service | 功能 / Function |
|---|---|
| **Amazon QuickSight** | **BI 儀表板和視覺化（互動式報告）** |
| Amazon Athena | SQL 查詢 S3 資料 |
| AWS Glue | ETL 服務（準備資料）|
| Amazon SageMaker | 建立/訓練/部署 ML 模型 |

---

## 問題 9 / Question 9

**[題目 / Question]**
A company needs **real-time processing of streaming big data** for their ad-tech platform. Which AWS service?
公司需要對 ad-tech 平台的大數據進行**即時串流處理**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：Amazon Kinesis Data Streams**

**[中文詳解]**
**Amazon Kinesis Data Streams** 可建立自定義應用程式來處理或分析串流資料。可持續從數十萬個來源添加各種類型的資料（點擊流、應用程式日誌、社群媒體）到 Kinesis 數據流，幾秒內即可供應用程式讀取和處理。

**[串流 vs 佇列 vs 倉儲 / Stream vs Queue vs Warehouse]**

| 服務 / Service | 類型 | 適用場景 |
|---|---|---|
| **Amazon Kinesis Data Streams** | **即時串流** | **即時大數據分析** |
| Amazon SQS | 訊息佇列 | 應用程式解耦 |
| Amazon Redshift | 資料倉儲 | 大規模歷史資料分析 |
| Amazon EMR | 批次大數據 | Hadoop 工作負載 |

---

## 問題 10 / Question 10

**[題目 / Question]**
Which AWS service is used to **store and commit code privately** and offers features for version control?
哪個 AWS 服務用於**私密儲存和提交代碼**，並提供版本控制功能？

**✅ 正確答案 / Correct Answer：AWS CodeCommit**

**[AWS 開發者工具完整對照 / AWS Developer Tools Complete Reference]**

| 服務 / Service | 功能 / Function |
|---|---|
| **AWS CodeCommit** | **私密 Git 儲存庫（原始碼控制）** |
| AWS CodeBuild | 持續整合（編譯、測試、建立套件）|
| AWS CodeDeploy | 自動化代碼部署（EC2、Lambda、本地）|
| AWS CodePipeline | 持續交付管道（協調整個 CI/CD 流程）|
| AWS CodeArtifact | 套件依賴管理（Maven、npm 等）|
| AWS CodeStar | 整合開發工具鏈（包含上述所有服務）|

---

## 問題 11 / Question 11

**[題目 / Question]**
Which statements are true about AWS Regions and Availability Zones (AZ)? (Select two)
以下哪兩個關於 AWS Regions 和 AZ 的說法正確？

**✅ 正確答案 / Correct Answers：**
1. Each AWS Region consists of **multiple, isolated, and physically separate AZs** within a geographic area
2. **All traffic between AZs is encrypted**（AZ 之間的所有流量均已加密）

**[AWS 基礎設施重要事實 / Infrastructure Facts]**

| 事實 / Fact | 說明 |
|---|---|
| **Region 由多個 AZ 組成** | 每個 Region 最少 3 個 AZ |
| **AZ 之間流量已加密** | 透過冗餘專用 Metro 光纖連接 |
| Region = 物理位置 | AWS 在全球建立資料中心的物理位置 |
| AZ = 邏輯資料中心群 | AWS 稱之為「邏輯資料中心群組」|

> ⚠️ 常見錯誤：「AZ 之間流量未預設加密，但可配置」→ **錯誤！AZ 之間流量始終加密**

---

## 問題 12 / Question 12

**[題目 / Question]**
Which data sources are used by **Amazon Detective** to analyze events and identify potential security issues?
**Amazon Detective** 使用哪些資料來源分析事件並識別潛在安全問題？

**✅ 正確答案 / Correct Answer：AWS CloudTrail logs, Amazon VPC Flow Logs, and Amazon GuardDuty findings**

**[Amazon Detective 資料來源 / Amazon Detective Data Sources]**

```
Amazon Detective 分析來源：
✅ AWS CloudTrail logs（API 活動）
✅ Amazon VPC Flow Logs（網路流量）
✅ Amazon GuardDuty findings（威脅發現）
❌ CloudWatch Logs（非 Detective 的資料來源）
❌ S3 Access Logs（非 Detective 的資料來源）
❌ Amazon Inspector logs（非 Detective 的資料來源）
```

> **Amazon Detective** 的功能：分析數萬億事件，自動建立資源、用戶和互動的統一互動視圖，簡化安全調查和根本原因分析

---

## 問題 13 / Question 13

**[題目 / Question]**
Which statements are true about AWS Shared Responsibility Model? (Select two)
以下哪兩個關於 AWS 共同責任模型的說法正確？

**✅ 正確答案 / Correct Answers：**
1. AWS trains AWS employees, but a **customer must train their own employees**（AWS 培訓 AWS 員工，客戶必須培訓自己的員工）
2. **AWS is responsible for patching infrastructure, but customers patch their guest OS and applications**

**[共同責任模型 — 常見錯誤選項解析 / Common Distractor Analysis]**

| 說法 / Statement | 正確性 |
|---|---|
| ✅ AWS 修補基礎設施，客戶修補 Guest OS 和應用程式 | **正確** |
| ✅ AWS 培訓 AWS 員工，客戶培訓自己的員工 | **正確（共同責任）** |
| ❌ 客戶負責配置 Guest OS、資料庫和應用程式（AWS 只配置基礎設施設備）| 說反了 |
| ❌ EC2 是 IaaS，因此 AWS 負責所有安全配置 | **錯誤！EC2 IaaS，客戶負責所有安全配置** |
| ❌ 對於 S3，AWS 負責加密選項和存取許可 | **錯誤！客戶負責加密選項和 IAM 許可** |

---

## 問題 14 / Question 14

**[題目 / Question]**
Which of the below services are **encrypted by default** and need no user intervention?
以下哪些服務**預設加密**且無需用戶干預？

**✅ 正確答案 / Correct Answer：AWS CloudTrail Logs, Amazon S3 Glacier, AWS Storage Gateway**

**[預設加密服務完整清單 / Default Encrypted Services]**

| 服務 / Service | 預設加密 | 加密類型 |
|---|---|---|
| **AWS CloudTrail Logs** | **✅** | SSE-S3（儲存在 S3 中）|
| **Amazon S3 Glacier** | **✅** | AES-256（AWS 管理金鑰）|
| **AWS Storage Gateway** | **✅** | SSL（傳輸中）+ SSE-S3（靜態）|
| **Amazon S3** | **✅**（新版本）| SSE-S3 |
| Amazon EBS | ❌ 可選 | 需手動啟用 |
| Amazon EFS | ❌ 可選 | 需手動啟用 |
| Amazon Redshift | ❌ 可選 | 需手動啟用 |
| Amazon CloudFront | ❌ 可選 | 需配置 |
| Amazon EC2 | ❌ 可選 | 預設未加密 |

---

## 問題 15 / Question 15

**[題目 / Question]**
An e-commerce company has its on-premises data storage on an **NFS file system accessed in parallel by multiple applications**. Moving to AWS, which storage service should it use for EC2 instances?
電商公司的本地資料存儲在被**多個應用程式並行存取的 NFS 文件系統**上，遷移到 AWS 後，應使用哪個儲存服務？

**✅ 正確答案 / Correct Answer：Amazon Elastic File System (Amazon EFS)**

**[關鍵判斷要素 / Key Decision Factors]**
- **NFS 協議** → EFS 使用 NFS 協議
- **多個應用程式並行存取** → EFS 支援數千個 EC2 執行個體同時存取
- **文件系統** → EFS 是文件儲存，非物件（S3）或區塊（EBS）

---

## 問題 16 / Question 16

**[題目 / Question]**
A university provides AWS services for research and can tolerate **data loss of a few hours**. Which disaster recovery strategy is the best fit?
大學提供 AWS 服務給學生做研究，可以承受**幾小時的資料遺失**，哪個 DR 策略最合適？

**✅ 正確答案 / Correct Answer：Backup and restore strategy（備份和還原策略）**

**[DR 策略四象限（從最便宜到最貴）/ DR Strategies Cost Ranking]**

| 策略 / Strategy | RTO | RPO | 成本 / Cost | 適用場景 |
|---|---|---|---|---|
| **Backup & Restore** | **最高** | **最高（幾小時）** | **最低** | **可承受資料遺失** |
| Pilot Light | 中 | 中 | 低 | 快速啟動核心基礎設施 |
| Warm Standby | 低 | 低 | 中 | 業務重要應用 |
| Multi-site Active/Active | 最低 | 最低 | 最高 | 任務關鍵 |

---

## 問題 17 / Question 17

**[題目 / Question]**
An organization needs additional IT infrastructure for a new product line and wants **rapid deployment** and **minimal setup time**. Which cloud computing advantages? (Select two)
組織需要額外的 IT 基礎設施，希望**快速部署**和**最少設置時間**，哪兩個雲端運算優勢？

**✅ 正確答案 / Correct Answers：**
1. Increase speed and agility（提高速度和敏捷性）
2. Enable automatic scaling of resources based on demand（按需自動擴展資源）

**[六大優勢 — 場景對應 / Six Advantages — Scenario Mapping]**

| 場景 / Scenario | 對應優勢 / Advantage |
|---|---|
| **快速部署 + 最少設置時間** | **速度和敏捷性 + 自動擴展** |
| 成本共享降低費用 | 大規模經濟 |
| 按需付費不買硬體 | 資本換可變支出 |
| 全球快速部署 | 幾分鐘內全球化 |

---

## 問題 18 / Question 18

**[題目 / Question]**
Which are the **security best practices** suggested by AWS for IAM? (Select two)
AWS 為 IAM 建議的哪兩個**安全最佳實踐**？

**✅ 正確答案 / Correct Answers：**
1. **Do not share security credentials** between accounts, use IAM roles instead（不共享安全憑證，改用 IAM 角色）
2. When creating IAM policies, **grant the least privileges** required to perform a task（授予最少所需權限）

**[IAM 安全最佳實踐 / IAM Security Best Practices]**

| 最佳實踐 / Best Practice | 說明 |
|---|---|
| ✅ 最少權限原則 | 只授予完成任務所需的最少權限 |
| ✅ 不共享憑證，使用 IAM 角色 | 跨帳戶存取應使用 IAM Role |
| ✅ 定期輪換密碼和存取金鑰 | 降低憑證洩露風險 |
| ✅ 啟用 MFA | 為所有用戶特別是 root 帳戶 |
| ❌ 永不共享 root 憑證 | 即使是重要計費操作也不行 |

---

## 問題 19 / Question 19

**[題目 / Question]**
IT departments historically over-provision for peak demand. Which feature of AWS Cloud refers to **right-sizing the resources**?
IT 部門傳統上為峰值需求過度佈建，AWS 雲端的哪個特性是指**調整資源至合適大小**？

**✅ 正確答案 / Correct Answer：Elasticity（彈性）**

**[雲端特性定義 / Cloud Characteristics Definitions]**

| 特性 / Characteristic | 定義 / Definition |
|---|---|
| **Elasticity（彈性）** | **按需獲取並在不需要時釋放資源（自動伸縮，避免過度佈建）** |
| Reliability（可靠性）| 工作負載正確且一致地執行其預期功能 |
| Resiliency（韌性）| 從基礎設施/服務中斷中恢復 |
| Horizontal Scaling | 透過增加更多電腦/執行個體來增加容量 |

---

## 問題 20 / Question 20

**[題目 / Question]**
Per the AWS Shared Responsibility Model, which AWS service is the **responsibility of the customer** to manage?
根據 AWS 共同責任模型，哪個 AWS 服務是**客戶的責任**來管理？

**✅ 正確答案 / Correct Answer：Amazon Elastic Compute Cloud (Amazon EC2)**

**[EC2 vs 托管服務責任對比 / EC2 vs Managed Services Responsibility]**

| 服務 / Service | 類型 / Type | 客戶責任 |
|---|---|---|
| **Amazon EC2** | **IaaS** | **客戶管理 OS、應用程式、安全群組** |
| Amazon S3 | 抽象服務 | 客戶管理資料和 IAM 許可 |
| Amazon DynamoDB | 托管服務 | 客戶管理資料和 IAM 許可 |
| AWS Elastic Beanstalk | 托管服務（PaaS）| 客戶管理資料和 IAM 許可 |

> **記憶法**：EC2 = IaaS = 客戶負責**所有**安全配置和管理；S3/DynamoDB/Beanstalk = 抽象/托管服務 = AWS 負責底層

---

## 問題 21 / Question 21

**[題目 / Question]**
You realized that **AWS-owned IP addresses are being used for port scanning** your on-premises server. Which service/team should you connect?
您發現 **AWS 擁有的 IP 位址正在對您的本地伺服器進行端口掃描**，應聯繫哪個服務/團隊？

**✅ 正確答案 / Correct Answer：Contact AWS Abuse Team（聯繫 AWS 濫用團隊）**

**[AWS Abuse Team 可協助的濫用行為 / Abuse Team Coverage]**
- ✅ 垃圾郵件（Spam）
- ✅ 端口掃描（Port scanning）
- ✅ DDoS 攻擊
- ✅ 入侵嘗試
- ✅ 存放不當或侵權內容
- ✅ 分發惡意軟體

> 聯繫方式：AWS Abuse Report Form 或 abuse@amazonaws.com

---

## 問題 22 / Question 22

**[題目 / Question]**
An organization wants to **break down AWS spending so each department and project can be accurately charged**. Which AWS feature is the best fit?
組織想要**細分 AWS 支出以便每個部門和專案能準確收費**，哪個 AWS 功能最合適？

**✅ 正確答案 / Correct Answer：AWS cost allocation tags（AWS 費用分配標籤）**

**[費用分配工具比較 / Cost Attribution Tools]**

| 工具 / Tool | 用途 | 支援按部門/專案分配 |
|---|---|---|
| **AWS cost allocation tags** | **為資源打標籤，按業務維度追蹤費用** | **✅ 直接** |
| AWS Budgets | 設置預算並告警 | ❌（需配合標籤）|
| AWS CUR | 最詳細的費用資料（輸出到 S3）| ❌（需配合標籤）|
| AWS Marketplace | 第三方軟體目錄 | ❌ |

---

## 問題 23 / Question 23

**[題目 / Question]**
A company wants to establish a **private, dedicated connection** between AWS and its on-premises data center. Which AWS service?
公司想在 AWS 和本地資料中心之間建立**私密、專用的連接**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Direct Connect**

**[Direct Connect 重要特點 / Direct Connect Key Facts]**
- 專用網路連接（不走公共網際網路）
- 可降低網路費用、提高帶寬和一致性
- ⚠️ **不加密傳輸中的流量**（如需加密，需與 VPN 結合）
- 建立時間至少需要一個月

---

## 問題 24 / Question 24

**[題目 / Question]**
Which is the **least effort way to encrypt data for AWS services only in your account** using AWS KMS?
使用 AWS KMS **對帳戶中 AWS 服務加密的最少努力方式**是？

**✅ 正確答案 / Correct Answer：Use AWS managed master keys that are automatically created in your account for each service（使用為每個服務自動建立的 AWS 管理主金鑰）**

**[AWS KMS 金鑰類型 / KMS Key Types]**

| 類型 / Type | 建立者 | 費用 | 控制程度 | 適用範圍 |
|---|---|---|---|---|
| **AWS managed CMK** | **AWS（代您）** | **無月費（部分使用費）** | **低（只能查看）** | **您的帳戶** |
| Customer managed CMK | 客戶 | 月費 + 使用費 | 高（完全控制）| 您的帳戶 |
| AWS owned CMK | AWS | 無費用 | 無（不可見）| **多個 AWS 帳戶** |

> **最少努力 = AWS managed CMK**（自動建立，格式為 `aws/service-name`）

---

## 問題 25 / Question 25

**[題目 / Question]**
An e-learning company wants to build a **knowledge graph** by leveraging a fully managed database. Which is the best fit?
電子學習公司想利用全托管資料庫建立**知識圖譜**，哪個最合適？

**✅ 正確答案 / Correct Answer：Amazon Neptune**

**[圖形資料庫使用案例 / Graph Database Use Cases]**

| 使用案例 / Use Case | 最佳資料庫 |
|---|---|
| **知識圖譜、身份圖譜、詐騙偵測、推薦引擎、社群網路** | **Amazon Neptune** |
| 電商、IoT 高效能應用 | Amazon DynamoDB |
| MySQL 遷移、CRM | Amazon Aurora |
| 文件儲存（MongoDB）| Amazon DocumentDB |
| 大規模分析 | Amazon Redshift |

---

## 問題 26 / Question 26

**[題目 / Question]**
Which statements are correct regarding **AWS Elastic Beanstalk health monitoring**? (Select two)
以下哪兩個關於 **AWS Elastic Beanstalk 健康監控**的說法正確？

**✅ 正確答案 / Correct Answers：**
1. Elastic Beanstalk health monitoring can determine that the environment's **Auto Scaling group is available and has at least one instance**
2. With basic health reporting, **Elastic Beanstalk does not publish any metrics to Amazon CloudWatch**

**[Elastic Beanstalk 健康監控要點 / Health Monitoring Notes]**
- 基本健康報告不向 CloudWatch 發布指標（CloudWatch 指標由環境中的資源發布）
- 單一執行個體環境使用 EC2 狀態（非 ELB）
- 負載均衡環境使用 ELB 健康檢查

---

## 問題 27 / Question 27

**[題目 / Question]**
Which credentials would you recommend for **signing in to the AWS Management Console** to meet security best practices? (Select two)
哪兩個憑證符合**登入 AWS 管理控制台**的安全最佳實踐？

**✅ 正確答案 / Correct Answers：**
1. **IAM Username and password**（IAM 使用者名稱和密碼）
2. **Multi Factor Authentication (MFA)**（多重要素驗證）

**[AWS 各類憑證用途 / AWS Credentials Use Cases]**

| 憑證 / Credential | 用途 |
|---|---|
| **IAM Username + Password** | **管理控制台登入** |
| **MFA** | **增加第二層安全驗證** |
| Access Key ID + Secret Access Key | 程式化存取（CLI、API、SDK）|
| X.509 certificate | AWS Certificate Manager (ACM)，TLS/SSL |

---

## 問題 28 / Question 28

**[題目 / Question]**
Which statements are correct regarding AWS Support Plans? (Select two)
以下哪兩個關於 AWS 支援方案的說法正確？

**✅ 正確答案 / Correct Answers：**
1. **A designated TAM is available only for AWS Enterprise Support plan**（專屬 TAM 只在 Enterprise 方案）
2. **Both Basic and Developer plans have access to core Trusted Advisor checks only**

**[支援方案重要差異 / Support Plan Key Differences]**

| 功能 / Feature | Basic | Developer | Business | Enterprise On-Ramp | Enterprise |
|---|---|---|---|---|---|
| Trusted Advisor | 核心 | 核心 | 全部 | 全部 | 全部 |
| **TAM** | ❌ | ❌ | ❌ | ✅（共享池）| **✅（專屬）** |
| AWS Concierge | ❌ | ❌ | ❌ | ✅ | ✅ |
| Infrastructure Event Mgmt | ❌ | ❌ | 付費額外購買 | ✅（每年一次）| ✅ |

> ⚠️ **Concierge 服務只在 Enterprise On-Ramp 和 Enterprise** 方案，不包含 Business

---

## 問題 29 / Question 29

**[題目 / Question]**
A manufacturing company needs AWS infrastructure, services, APIs, and tools in its **on-premises data center** for running **low latency applications**. Which AWS service?
製造公司需要在**本地資料中心**運行**低延遲應用程式**的 AWS 基礎設施、服務、API 和工具，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Outposts**

**[邊緣/本地服務完整比較 / Edge & Local Services Comparison]**

| 服務 / Service | 位置 / Location | 適用場景 |
|---|---|---|
| **AWS Outposts** | **客戶資料中心（本地）** | **需要資料駐留、本地低延遲、應用程式互依性** |
| AWS Local Zones | 靠近終端用戶的城市位置 | 城市用戶單個位數毫秒延遲 |
| AWS Wavelength | CSP 5G 邊緣 | 5G 設備超低延遲 |
| AWS Snow Family | 實體設備 | 大量資料遷移、邊緣運算（離線）|

---

## 問題 30 / Question 30

**[題目 / Question]**
A blogging company needs an **easy solution to host WordPress blogs** without managing servers or databases. Which AWS service?
部落格公司需要**簡單的解決方案來託管 WordPress 部落格**，無需管理伺服器或資料庫，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：Amazon Lightsail**

**[Lightsail 特點 / Lightsail Features]**
- 預配置的 VPS 方案（含 VM、儲存、傳輸、DNS 管理、靜態 IP）
- 一鍵啟動的操作系統、開發堆疊和 Web 應用程式（含 WordPress）
- 按小時按需計費，可預測的低月費
- 適合：網站、Web 應用程式、部落格、電商、簡單軟體

---

## 問題 31 / Question 31

**[題目 / Question]**
A healthcare company wants **continuous replication based disaster recovery** and fast recovery of physical, virtual, and cloud-based servers into AWS. Which solution?
醫療公司需要**基於持續複製的災難恢復**，以及物理、虛擬和雲端伺服器到 AWS 的快速恢復，哪個解決方案？

**✅ 正確答案 / Correct Answer：CloudEndure Disaster Recovery**

**[CloudEndure DR 主要功能 / CloudEndure DR Features]**
- **持續複製**：異步區塊級複製，實現亞秒級 RPO
- **低成本暫存區**：在目標 AWS Region 中持續同步
- **自動化機器轉換**：幾分鐘內在目標 Region 啟動數千台機器（RTO）
- **時間點恢復**：從以前的一致時間點恢復（防止勒索軟體）
- **非破壞性演練**：不影響源環境或造成資料遺失

---

## 問題 32 / Question 32

**[題目 / Question]**
A company wants to **automate keeping server images up-to-date** for both EC2 instances and on-premises systems. Which AWS service?
公司想**自動化保持伺服器映像最新狀態**，適用於 EC2 和本地系統，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：Amazon EC2 Image Builder**

**[中文詳解]**
**Amazon EC2 Image Builder** 簡化了虛擬機和容器映像的建立、測試和部署，可用於 AWS 或本地。提供簡單的圖形介面、內建自動化和 AWS 提供的安全設定，無需手動步驟即可更新映像，也無需建立自己的自動化管道。

---

## 問題 33 / Question 33

**[題目 / Question]**
Which features are covered as part of the **AWS Basic Support Plan**? (Select two)
以下哪兩個功能包含在 **AWS Basic 支援方案**中？

**✅ 正確答案 / Correct Answers：**
1. **One-on-one responses to account and billing questions**（帳戶和計費問題的一對一響應）
2. **Service health checks**（服務健康檢查）

**[AWS Basic 支援方案包含的功能 / Basic Support Plan Features]**

| 包含 / Included | 不包含 / Not Included |
|---|---|
| ✅ 24/7 帳戶和計費支援 | ❌ 客戶端診斷工具（Developer+）|
| ✅ 服務健康檢查 | ❌ 使用案例指導（Business+）|
| ✅ 支援論壇 | ❌ 基礎設施事件管理（Enterprise On-Ramp/Enterprise）|
| ✅ 核心 Trusted Advisor 檢查 | ❌ 第三方軟體支援 |
| ✅ 文件、技術文件和最佳實踐指南 | ❌ 24/7 電話技術支援 |

---

## 問題 34 / Question 34

**[題目 / Question]**
Which statements are correct regarding **AWS Control Tower and Service Control Policies (SCPs)**? (Select two)
以下哪兩個關於 **AWS Control Tower 和 SCP** 的說法正確？

**✅ 正確答案 / Correct Answers：**
1. **AWS Control Tower** provides a pre-defined set of blueprints and guardrails to implement a landing zone for new AWS accounts
2. **SCPs are a type of organization policy** that you can use to manage permissions in your organization

**[SCP 重要特性 / SCP Key Characteristics]**

| SCP 特性 / Characteristic | 說明 |
|---|---|
| 不直接授予權限 | SCP 設置護欄/限制，不授予權限 |
| **只影響成員帳戶** | **不影響管理帳戶（根帳戶）的使用者和角色** |
| 僅在啟用所有功能的組織中可用 | 不適用於只啟用整合計費功能的組織 |
| 定義最大可用權限 | 有效權限 = SCP ∩ IAM 策略 |

> ⚠️ SCP **不能**授予權限；它設置帳戶管理員可以委派的最大限制

---

## 問題 35 / Question 35

**[題目 / Question]**
Which AWS service allows you to connect any number of **IoT devices to the cloud** without provisioning or managing servers?
哪個 AWS 服務讓您在不佈建或管理伺服器的情況下將任意數量的 **IoT 設備連接到雲端**？

**✅ 正確答案 / Correct Answer：AWS IoT Core**

**[中文詳解]**
**AWS IoT Core** 讓您無需佈建或管理伺服器即可將 IoT 設備連接到 AWS 雲端。可支援數十億設備和萬億消息，安全可靠地路由到 AWS 端點和其他設備。支援 MQTT、HTTPS、MQTT over WSS 和 LoRaWAN 協議。

---

## 問題 36 / Question 36

**[題目 / Question]**
Which tool/service will help you get a **forecast of your spending for the next 12 months**?
哪個工具/服務幫助您獲得**未來 12 個月的支出預測**？

**✅ 正確答案 / Correct Answer：AWS Cost Explorer**

**[成本工具時間範圍 / Cost Tools Time Range]**

| 工具 / Tool | 歷史資料 / History | 預測 / Forecast |
|---|---|---|
| **AWS Cost Explorer** | **最多 12 個月** | **✅ 未來 12 個月** |
| AWS CUR | 詳細歷史 | ❌ |
| AWS Budgets | N/A | ❌（設置預算告警）|
| AWS Pricing Calculator | N/A | ❌（事前估算）|

---

## 問題 37 / Question 37

**[題目 / Question]**
Which AWS service is delivered **globally** rather than regionally?
哪個 AWS 服務是**全球性**而非區域性的？

**✅ 正確答案 / Correct Answer：Amazon WorkSpaces**

**[全球性 AWS 服務 / Global AWS Services]**
- ✅ AWS IAM
- ✅ Amazon CloudFront
- ✅ Amazon Route 53
- ✅ **Amazon WorkSpaces**
- ✅ Amazon WorkMail、WorkDocs、WorkLink、Amazon Chime

**[區域性服務 / Regional Services]**
- ❌ Amazon EFS（區域服務）
- ❌ Amazon S3 儲存桶（區域服務，雖命名空間全球）
- ❌ AWS Snowball（特定 Region 可用）

---

## 問題 38 / Question 38

**[題目 / Question]**
Which AWS service can **continuously monitor both malicious activities and unauthorized behavior** to protect AWS accounts and workloads?
哪個 AWS 服務可以**持續監控惡意活動和未授權行為**以保護 AWS 帳戶和工作負載？

**✅ 正確答案 / Correct Answer：Amazon GuardDuty**

**[安全服務功能釐清 / Security Services Clarification]**

| 服務 / Service | 主要功能 |
|---|---|
| **Amazon GuardDuty** | **持續威脅偵測（ML + CloudTrail + VPC Flow Logs + DNS）** |
| AWS Security Hub | 彙總多個 AWS 服務的安全告警（單一視圖）|
| Amazon Detective | 調查安全發現的根本原因 |
| Amazon Inspector | EC2 執行個體的自動化漏洞評估 |

---

## 問題 39 / Question 39

**[題目 / Question]**
A gaming company needs compute and storage services close to **edge locations in 5G mobile networks**. Which AWS service?
遊戲公司需要靠近 **5G 移動網路邊緣位置**的運算和儲存服務，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Wavelength**

**[邊緣服務快速選擇指南 / Edge Services Quick Guide]**

| 關鍵詞 / Keywords | 服務 / Service |
|---|---|
| **5G 邊緣、CSP 數據中心、移動網路** | **AWS Wavelength** |
| 本地資料中心、資料駐留、本地 AWS 基礎設施 | AWS Outposts |
| 靠近城市終端用戶、單位數毫秒延遲 | AWS Local Zones |
| 大量資料遷移、邊緣運算（離線）| AWS Snow Family |

---

## 問題 40 / Question 40

**[題目 / Question]**
Which pillar of AWS Well-Architected Framework focuses on **using IT and computing resources efficiently** and selecting the right resource types and sizes?
AWS Well-Architected Framework 哪個支柱專注於**有效使用 IT 和運算資源**並選擇正確的資源類型和大小？

**✅ 正確答案 / Correct Answer：Performance Efficiency Pillar（效能效率支柱）**

**[六大支柱關鍵設計原則 / Six Pillars Design Principles]**

| 支柱 / Pillar | 設計原則 / Design Principles |
|---|---|
| Operational Excellence | IaC、頻繁可逆變更、預見失敗 |
| Security | KMS 加密、啟用可追溯性 |
| Reliability | 自動從故障恢復、測試恢復程序 |
| **Performance Efficiency** | **選擇正確資源類型和大小、使用無伺服器、實驗更多** |
| Cost Optimization | 使用節省方案、避免閒置資源 |
| Sustainability | 降低環境影響 |

---

## 問題 41 / Question 41

**[題目 / Question]**
Which are **NoSQL database services** from AWS? (Select two)
以下哪兩個是 AWS 的 **NoSQL 資料庫服務**？

**✅ 正確答案 / Correct Answers：**
1. Amazon DocumentDB（文件資料庫）
2. Amazon Neptune（圖形資料庫）

**[AWS 資料庫服務分類 / AWS Database Services Classification]**

| 類別 / Category | 服務 / Services |
|---|---|
| **關聯式 / Relational** | Amazon RDS、Amazon Aurora |
| **NoSQL — 鍵值** | Amazon DynamoDB |
| **NoSQL — 文件** | **Amazon DocumentDB** |
| **NoSQL — 圖形** | **Amazon Neptune** |
| 記憶體快取 | Amazon ElastiCache |
| 資料倉儲 | Amazon Redshift |
| 時間序列 | Amazon Timestream |
| 帳本資料庫 | Amazon QLDB |

---

## 問題 42 / Question 42

**[題目 / Question]**
A financial consulting company needs **automated reference deployments** to speed up deploying financial solutions on AWS. Which AWS service?
金融諮詢公司需要**自動化參考部署**來加速在 AWS 部署金融解決方案，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Partner Solutions (formerly Quick Starts)**

**[AWS Partner Solutions 內容 / What's Included]**
1. 部署的參考架構
2. 自動化和配置部署的 CloudFormation 模板（JSON 或 YAML）
3. 詳細說明架構和實施的部署指南（含自定義指令）

---

## 問題 43 / Question 43

**[題目 / Question]**
A DynamoDB-based weather application experiences high read requests during holidays. Which feature/service will help resolve this?
基於 DynamoDB 的天氣應用程式在假期期間讀取請求過高，哪個功能/服務可解決？

**✅ 正確答案 / Correct Answer：Amazon DynamoDB Accelerator (DAX)**

**[中文詳解]**
**Amazon DynamoDB Accelerator (DAX)** 是 DynamoDB 相容的記憶體快取服務，可將讀取響應時間從毫秒降低到微秒級別，特別適合讀取密集型工作負載。與 DynamoDB API 相容，只需最少的功能變更即可使用。

**[DAX vs ElastiCache 選擇 / DAX vs ElastiCache]**

| 場景 / Scenario | 推薦 / Recommended |
|---|---|
| **DynamoDB 讀取效能問題** | **DAX（DynamoDB 原生快取）** |
| 通用 RDS 讀取效能問題 | Amazon ElastiCache |

---

## 問題 44 / Question 44

**[題目 / Question]**
A media company uses Amazon S3 for storing data with **random access patterns**. Which storage class should it consider for cost-optimal storage?
媒體公司使用 Amazon S3 儲存具有**隨機存取模式**的資料，哪個儲存類別最具成本效益？

**✅ 正確答案 / Correct Answer：Amazon S3 Intelligent-Tiering (S3 Intelligent-Tiering)**

**[S3 Intelligent-Tiering 特點 / S3 Intelligent-Tiering Features]**
- 自動在四個存取層之間移動物件
- 無取回費用（與 Standard-IA 不同）
- 監控存取模式並自動移動到最具成本效益的層
- **適合：未知存取模式、新應用程式、不可預測的存取模式**

**[S3 儲存類別選擇 — 按存取模式 / S3 Class by Access Pattern]**

| 存取模式 / Pattern | 推薦 |
|---|---|
| 頻繁 | S3 Standard |
| **未知/隨機/不可預測** | **S3 Intelligent-Tiering** |
| 不頻繁 + 快速 + 多 AZ | S3 Standard-IA |
| 不頻繁 + 快速 + 可重建 | S3 One Zone-IA |

---

## 問題 45 / Question 45

**[題目 / Question]**
An application uses **in-memory caches for running custom workloads**. Which Amazon EC2 instance type is the right choice?
應用程式使用**記憶體內快取執行自定義工作負載**，哪個 Amazon EC2 執行個體類型最合適？

**✅ 正確答案 / Correct Answer：Memory Optimized instance types（記憶體優化執行個體類型）**

**[EC2 執行個體類型對照 / EC2 Instance Types]**

| 類型 / Type | 適用工作負載 |
|---|---|
| **Memory Optimized** | **記憶體內應用程式、記憶體內資料庫、快取（大型記憶體）** |
| Compute Optimized | 高效能 Web 伺服器、HPC、ML 推理 |
| Storage Optimized | Hadoop、大規模並行資料倉儲、日誌處理 |
| Accelerated Computing | GPU 計算、機器學習、FPGA |
| General Purpose | 均衡工作負載（Web 伺服器、中小型資料庫）|

---

## 問題 46 / Question 46

**[題目 / Question]**
Which scenario can effectively use Auto Scaling group's **predictive scaling**?
哪個場景可以有效使用 Auto Scaling 群組的**預測性擴展**？

**✅ 正確答案 / Correct Answer：To manage a workload that exhibits **recurring load patterns** specific to the day of the week or time of day（管理表現出每週特定日期或每天特定時間的**週期性負載模式**的工作負載）**

**[Auto Scaling 擴展策略 / Auto Scaling Policies]**

| 策略 / Policy | 適用場景 |
|---|---|
| **Predictive Scaling（預測性擴展）** | **週期性、循環性負載模式（每週/每天）** |
| Target Tracking（目標追蹤）| 維持特定指標（如 CPU 40%）|
| Step Scaling | 按需動態擴展 |
| Manual Scaling | 固定數量執行個體 |

---

## 問題 47 / Question 47

**[題目 / Question]**
A Security Group was changed in an AWS account. The manager wants to find out the details of the **user who changed it**. Which AWS service?
AWS 帳戶中的安全群組被更改，管理者想了解**更改者的詳細資訊**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS CloudTrail**

**[服務記憶法 / Service Memory Aid]**
> **"誰做了這件事？"** → **CloudTrail**（記錄所有 API 呼叫和使用者活動）
> **"什麼發生了變化？"** → **Config**（記錄資源配置歷史）
> **"應用程式效能如何？"** → **X-Ray**

---

## 問題 48 / Question 48

**[題目 / Question]**
A Cloud Practitioner wants to find examples of **AWS Cloud solution designs**. Which service/feature?
Cloud Practitioner 想找 **AWS 雲端解決方案設計**的範例，哪個服務/功能？

**✅ 正確答案 / Correct Answer：AWS Architecture Center（AWS 架構中心）**

**[中文詳解]**
**AWS Architecture Center** 提供：
- 參考架構圖
- 經過驗證的架構解決方案
- Well-Architected 最佳實踐
- 設計模式和圖示

---

## 問題 49 / Question 49

**[題目 / Question]**
A company stores media files in S3 and wants to **convert these media files into formats for mobile device playback**. Which AWS service?
公司在 S3 儲存媒體文件，想將這些媒體文件**轉換為行動設備播放格式**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：Amazon Elastic Transcoder**

**[中文詳解]**
**Amazon Elastic Transcoder** 讓您將儲存在 Amazon S3 中的媒體文件轉換為消費者設備（行動設備、平板電腦、Web 瀏覽器）所需格式。自動管理整個媒體轉碼過程，為流行的輸出格式提供轉碼預設。

**[媒體相關服務對比 / Media Services]**

| 服務 / Service | 功能 |
|---|---|
| **Amazon Elastic Transcoder** | **媒體格式轉換（轉碼）** |
| Amazon Transcribe | 語音 → 文字（ASR）|
| Amazon Comprehend | 自然語言處理（NLP）|
| AWS Glue | ETL 服務（資料準備）|

---

## 問題 50 / Question 50

**[題目 / Question]**
Which AWS services are offered **free of cost**? (Select two)
哪兩個 AWS 服務**免費提供**？

**✅ 正確答案 / Correct Answers：**
1. **AWS Elastic Beanstalk**（服務本身免費，只付底層資源）
2. **AWS Auto Scaling**（服務本身免費，只付 EC2 和 CloudWatch 費用）

**[AWS 永久免費服務 / Always-Free Services]**

| 免費服務 / Free Service | 說明 |
|---|---|
| **AWS IAM** | 完全免費 |
| **AWS Auto Scaling** | 免費（付底層資源）|
| **AWS Elastic Beanstalk** | 免費（付底層資源）|
| **AWS CloudFormation** | 免費（付佈建的資源）|
| **Amazon VPC** | 基本功能免費 |
| **AWS Organizations** | 免費 |

**[不免費的常見誤解 / Common Misconceptions]**
- ❌ EC2 Spot Instances → 有折扣但**不免費**
- ❌ CloudWatch 詳細監控 → **需付費**（基本監控免費）
- ❌ Elastic IP → 關聯到運行 EC2 時免費，其他情況**收費**

---

## 問題 51 / Question 51

**[題目 / Question]**
Which statements are correct regarding **Amazon API Gateway**? (Select two)
以下哪兩個關於 **Amazon API Gateway** 的說法正確？

**✅ 正確答案 / Correct Answers：**
1. Amazon API Gateway **can call an AWS Lambda function** to create the front door of a serverless application
2. API Gateway **can be configured to send data directly to Amazon Kinesis Data Stream**

**[API Gateway 功能澄清 / API Gateway Features Clarification]**

| 說法 / Statement | 正確性 |
|---|---|
| ✅ 可呼叫 Lambda 建立無伺服器前端 | 正確 |
| ✅ 可直接發送資料到 Kinesis | 正確 |
| ✅ 支援 API 結果快取 | 正確（可配置）|
| ❌ 快取服務的 API 呼叫不計入計費 | **錯誤！計費相同** |
| ❌ Storage Gateway 建立 WebSocket APIs | **錯誤！API Gateway 建立 REST、HTTP 和 WebSocket APIs** |

---

## 問題 52 / Question 52

**[題目 / Question]**
Which statements are true about **AWS Elastic Beanstalk**? (Select two)
以下哪兩個關於 **AWS Elastic Beanstalk** 的說法正確？

**✅ 正確答案 / Correct Answers：**
1. **There is no additional charge** for AWS Elastic Beanstalk（無額外費用，只付底層資源）
2. You can quickly deploy and manage applications **without having to learn about the infrastructure**（無需學習底層基礎設施）

**[Elastic Beanstalk 重要事實 / Elastic Beanstalk Key Facts]**
- ✅ 支援語言：Go、Java、.NET、Node.js、PHP、Python、Ruby 和 Docker
- ✅ 自動化：容量佈建、負載均衡、**自動擴展**、應用程式健康監控
- ✅ 非 Web 應用程式也可部署（Beanstalk 的開放架構）
- ✅ 完全免費（只付底層 AWS 資源）

---

## 問題 53 / Question 53

**[題目 / Question]**
Which use-case can be solved using **Amazon Forecast** service?
哪個使用案例可以用 **Amazon Forecast** 服務解決？

**✅ 正確答案 / Correct Answer：Predict the web traffic of a website for the next few weeks（預測網站未來幾週的 Web 流量）**

**[Amazon Forecast 適用場景 / Amazon Forecast Use Cases]**
Amazon Forecast 可預測任何時間序列資料：
- ✅ 零售需求預測
- ✅ 製造需求
- ✅ 旅行需求
- ✅ IT 容量
- ✅ 物流
- ✅ **Web 流量**

**[ML 服務使用案例對照 / ML Services Use Cases]**

| 服務 / Service | 使用案例 |
|---|---|
| **Amazon Forecast** | **時間序列預測（Web 流量、需求）** |
| Amazon SageMaker | 建立/訓練/部署通用 ML 模型 |
| Amazon Kendra | 智能企業文件搜索 |
| Amazon Personalize | 個人化推薦 |

---

## 問題 54 / Question 54

**[題目 / Question]**
A financial services company needs to retain data for **10 years** to meet compliance. Which S3 storage class at minimal cost?
金融服務公司需要保留資料 **10 年**以滿足合規，哪個 S3 儲存類別費用最低？

**✅ 正確答案 / Correct Answer：Amazon S3 Glacier Deep Archive**

**[長期合規存檔的最佳選擇 / Best for Long-term Compliance]**
- **S3 Glacier Deep Archive** → AWS 最低成本儲存類別
- 設計用於 7-10 年以上合規要求（金融服務、醫療保健、公共部門）
- 資料跨至少 3 個 AZ 複製，提供 99.999999999% 耐久性
- 可在 12 小時內還原

---

## 問題 55 / Question 55

**[題目 / Question]**
Employees are provisioning additional resources via API calls beyond baseline. Which AWS service will raise alarms?
員工透過 API 呼叫佈建超出基線的額外資源，哪個 AWS 服務可以發出告警？

**✅ 正確答案 / Correct Answer：AWS CloudTrail Insights**

**[中文詳解]**
**AWS CloudTrail Insights** 通過持續分析 CloudTrail 管理事件，幫助識別和響應與寫入 API 呼叫相關的異常活動。CloudTrail Insights 測量正常的 API 呼叫量模式（基線），並在呼叫量超出正常模式時生成 Insights 事件。

**[CloudTrail 相關功能 / CloudTrail Related Features]**

| 功能 / Feature | 說明 |
|---|---|
| **CloudTrail Insights** | **偵測異常 API 呼叫量（超出基線）** |
| CloudTrail Management Events | 管理操作記錄（預設啟用）|
| CloudTrail Data Events | 資源操作記錄（需額外啟用，有費用）|

---

## 問題 56 / Question 56

**[題目 / Question]**
Which AWS service will help **provision a logically isolated network** for your AWS resources?
哪個 AWS 服務幫助**佈建 AWS 資源的邏輯隔離網路**？

**✅ 正確答案 / Correct Answer：Amazon Virtual Private Cloud (Amazon VPC)**

**[VPC 相關服務對比 / VPC Related Services]**

| 服務 / Service | 功能 / Function |
|---|---|
| **Amazon VPC** | **建立邏輯隔離的虛擬網路** |
| AWS PrivateLink | VPC 到 AWS 服務的私密連接 |
| Amazon Route 53 | DNS 服務 |
| AWS Firewall Manager | 集中管理防火牆規則 |

---

## 問題 57 / Question 57

**[題目 / Question]**
Which is the responsibility of the **customer** when running applications using **AWS Lambda**?
使用 **AWS Lambda** 執行應用程式時，哪項是**客戶的責任**？

**✅ 正確答案 / Correct Answer：Writing and maintaining the function code and its dependencies（編寫和維護函數代碼及其依賴項）**

**[Lambda 共同責任 / Lambda Shared Responsibility]**

| 責任 / Responsibility | AWS | 客戶 |
|---|---|---|
| 物理伺服器管理 | ✅ | ❌ |
| 配置 Lambda 服務的網路基礎設施 | ✅ | ❌ |
| 更新 OS 和運行環境 | ✅ | ❌ |
| **編寫和維護函數代碼及依賴項** | ❌ | **✅** |

---

## 問題 58 / Question 58

**[題目 / Question]**
Which **free tool** helps review workloads and compare them to AWS architectural best practices after answering a series of questions?
哪個**免費工具**幫助審查工作負載並在回答一系列問題後與 AWS 架構最佳實踐進行比較？

**✅ 正確答案 / Correct Answer：AWS Well-Architected Tool（AWS Well-Architected 工具）**

**[三個相關資源對比 / Three Related Resources]**

| 資源 / Resource | 說明 |
|---|---|
| **AWS Well-Architected Tool** | **免費工具（在控制台中），回答問題後生成行動計劃** |
| AWS Well-Architected Framework | 框架文件（六大支柱的概念和最佳實踐）|
| AWS Trusted Advisor | 即時告警，基於實際資源配置（不需回答問題）|

---

## 問題 59 / Question 59

**[題目 / Question]**
AWS WAF can be deployed on which services?
AWS WAF 可部署在哪些服務上？

**✅ 正確答案 / Correct Answer：Amazon CloudFront, Application Load Balancer, Amazon API Gateway, AWS AppSync**

**[AWS WAF 部署目標 / AWS WAF Deployment Targets]**

| 可部署 / Can Deploy | 不能直接部署 |
|---|---|
| ✅ Amazon CloudFront | ❌ Amazon EC2（需在 ALB 前面）|
| ✅ Application Load Balancer | |
| ✅ Amazon API Gateway | |
| ✅ AWS AppSync | |

---

## 問題 60 / Question 60

**[題目 / Question]**
Which AWS network services allow **CIDR block notation** for IP address ranges? (Select two)
哪兩個 AWS 網路服務允許使用 **CIDR 區塊表示法**指定 IP 地址範圍？

**✅ 正確答案 / Correct Answers：**
1. **Network access control list (Network ACL)**
2. **Security group**

**[CIDR 表示法支援 / CIDR Notation Support]**
- ✅ Security Group → 允許使用 CIDR 指定 IP 範圍
- ✅ Network ACL → 允許使用 CIDR 指定 IP 範圍
- ❌ AWS Lambda → 無 IP 範圍設定功能
- ❌ AWS Cost Explorer → 費用管理工具
- ❌ Amazon S3 → 物件儲存，不是網路服務

---

## 問題 61 / Question 61

**[題目 / Question]**
Which will help **control the incoming traffic** to an Amazon EC2 instance?
哪個可以幫助**控制傳入 Amazon EC2 執行個體的流量**？

**✅ 正確答案 / Correct Answer：Security Group（安全群組）**

**[VPC 安全組件功能對比 / VPC Security Components]**

| 組件 / Component | 控制範圍 | 適用場景 |
|---|---|---|
| **Security Group** | **執行個體進出流量** | **控制 EC2 傳入流量** |
| Network ACL | 子網路進出流量 | 子網路層級控制 |
| Route Table | 路由決策 | 決定流量去向 |
| AWS Resource Group | 資源分組管理 | 批量管理資源 |

---

## 問題 62 / Question 62

**[題目 / Question]**
An e-commerce application sends messages to a downstream application when orders are created. They want to **decouple this architecture without communication loss**. Which service?
電商應用程式在訂單建立時向下游應用程式發送消息，想**解耦此架構且不丟失通信**，哪個服務？

**✅ 正確答案 / Correct Answer：Amazon Simple Queue Service (SQS)**

**[SQS vs SNS 解耦場景對比 / SQS vs SNS for Decoupling]**

| 需求 / Requirement | SQS | SNS |
|---|---|---|
| **無通信遺失（訊息持久化）** | **✅（訊息儲存直到被消費）** | ❌（推送，接收者不在線則遺失）|
| 多個訂閱者 | ❌（點對點）| ✅ |
| 解耦架構 | ✅ | ✅ |

> **關鍵**：SQS 使用**拉取機制**，訊息在佇列中等待直到被處理，確保不遺失

---

## 問題 63 / Question 63

**[題目 / Question]**
By default, which events are logged by **AWS CloudTrail**?
**AWS CloudTrail** 預設記錄哪些事件？

**✅ 正確答案 / Correct Answer：Management events（管理事件）**

**[CloudTrail 事件類型 / CloudTrail Event Types]**

| 事件類型 / Event Type | 預設記錄 / Default | 額外費用 |
|---|---|---|
| **Management events（管理事件）** | **✅ 預設啟用** | 無 |
| Data events（資料事件）| ❌ 需明確添加 | ✅ 有 |
| Insights events | ❌ 需明確啟用 | ✅ 有 |

> **管理事件**範例：建立/刪除 S3 儲存桶、配置路由規則、設置日誌記錄
> **資料事件**範例：S3 物件級 API、Lambda 函數執行

---

## 問題 64 / Question 64

**[題目 / Question]**
Which service is a repository service for **maintaining application dependencies** via integration with package managers like Maven, Gradle, npm?
哪個服務是整合 Maven、Gradle、npm 等套件管理器的**應用程式依賴項管理**儲存庫服務？

**✅ 正確答案 / Correct Answer：AWS CodeArtifact**

**[中文詳解]**
**AWS CodeArtifact** 是全托管的套件儲存庫服務，讓組織能安全地儲存、發布和共享開發過程中使用的軟體套件。可自動從公共套件儲存庫獲取軟體套件，支援 Maven、Gradle、npm、yarn、pip、NuGet 等。

**[開發工具鏈 / Developer Toolchain]**
```
CodeCommit（原始碼）
    → CodeBuild（建構和測試）
    → CodeDeploy（部署）
    → CodePipeline（整個 CI/CD 管道）
    → CodeArtifact（套件依賴管理）
    → CodeStar（整合工具鏈）
```

---

## 問題 65 / Question 65

**[題目 / Question]**
Which feature/functionality will help you **organize AWS resources and automate tasks on large numbers of resources** at a time?
哪個功能/特性幫助您**組織 AWS 資源並一次自動化大量資源上的任務**？

**✅ 正確答案 / Correct Answer：AWS Resource Groups**

**[資源管理工具對比 / Resource Management Tools]**

| 工具 / Tool | 用途 / Purpose |
|---|---|
| **AWS Resource Groups** | **組織資源並批量自動化任務（按標籤或 CloudFormation 堆疊分組）** |
| Tags（標籤）| 為資源分配元資料，Resource Groups 使用標籤 |
| AWS Organizations | 集中管理多個 AWS 帳戶 |
| Amazon WorkSpaces | 虛擬桌面服務 |

---

## 📊 考題領域統計 / Domain Summary

| 領域 / Domain | 題數 / Questions | 百分比 / % |
|---|---|---|
| Technology（技術）| 31 | 47.7% |
| Security and Compliance（安全與合規）| 15 | 23.1% |
| Cloud Concepts（雲端概念）| 13 | 20.0% |
| Billing and Pricing（計費與定價）| 6 | 9.2% |

---

## 🎯 本回必考重點整理 / Key Exam Points (Set 6)

### 全新登場服務（首次出現）
- **Amazon AppStream 2.0** → 應用程式串流（vs WorkSpaces 提供完整桌面）
- **AWS OpsHub** → 管理 Snowball 設備的圖形界面
- **Amazon QuickSight** → BI 儀表板和視覺化，按會話定價
- **Amazon Kinesis Data Streams** → 即時串流大數據處理
- **Amazon Detective** → 分析安全發現的根本原因（資料來源：CloudTrail + VPC Flow Logs + GuardDuty）
- **AWS Savings Plans** → Compute（66%）和 EC2 Instance（72%）兩種類型
- **CloudEndure Disaster Recovery** → 持續複製 DR，亞秒級 RPO
- **Amazon EC2 Image Builder** → 自動化伺服器映像更新
- **Amazon Forecast** → 時間序列預測服務
- **Amazon Elastic Transcoder** → 媒體格式轉換
- **AWS IoT Core** → IoT 設備連接雲端
- **AWS CodeArtifact** → 套件依賴管理
- **AWS Resource Groups** → 組織和批量管理 AWS 資源
- **AWS Control Tower** → 多帳戶著陸區（Landing Zone）藍圖和護欄
- **AWS CloudTrail Insights** → 偵測異常 API 呼叫（超出基線）
- **Amazon Neptune** → 圖形資料庫（NoSQL）
- **Amazon DocumentDB** → 文件資料庫（NoSQL，MongoDB 相容）
- **Amazon DynamoDB Accelerator (DAX)** → DynamoDB 的記憶體快取
- **AWS Well-Architected Tool** → 審查工作負載並比較最佳實踐的免費工具
- **Auto Scaling Predictive Scaling** → 基於 ML 預測週期性負載模式

### AZ 之間流量加密
- **AZ 之間的所有流量始終加密**（常見考題陷阱）

### AWS Savings Plans 類型
- **Compute Savings Plans** → 66% 折扣，最靈活（EC2、Fargate、Lambda）
- **EC2 Instance Savings Plans** → 72% 折扣，特定 Region 和執行個體家族

### CloudTrail 事件類型預設記錄
- **Management Events** → 預設記錄（無額外費用）
- Data Events / Insights Events → 需明確啟用（有額外費用）

### 選擇 AWS Region 的四大因素
1. 合規和資料駐留要求
2. 地理位置接近用戶
3. 服務可用性
4. 成本差異

### 資料庫類型釐清
- **關聯式**：RDS、Aurora
- **NoSQL 鍵值**：DynamoDB
- **NoSQL 文件**：DocumentDB
- **NoSQL 圖形**：Neptune
- **時間序列**：Timestream
- **帳本**：QLDB

### WAF 部署目標（常考）
CloudFront + **ALB** + API Gateway + AppSync（**不能直接部署在 EC2**，需透過 ALB）
