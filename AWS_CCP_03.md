# AWS Cloud Practitioner 考題中英對照詳解（第三回）
# AWS Cloud Practitioner Exam Q&A — Bilingual Study Guide (Set 3)

---

## 問題 1 / Question 1

**[題目 / Question]**
A multi-national company needs to submit **historical configurations** on a regular basis to demonstrate compliance. Which AWS service is best suited?
跨國公司需要定期提交**歷史配置**以展示合規性，哪個 AWS 服務最合適？

**✅ 正確答案 / Correct Answer：AWS Config**

**[中文詳解]**
**AWS Config** 提供 AWS 帳戶中資源配置的詳細視圖，包括資源之間的關係以及過去的配置方式，讓您查看配置和關係如何隨時間變化。適用於資源管理、審計合規、配置變更管理和安全分析。

**[三大監控服務比較 / Key Trio Comparison]**

| 服務 / Service | 功能重點 | 記憶口訣 |
|---|---|---|
| **AWS Config** | **資源配置歷史和合規** | 想到資源配置變更 → Config |
| AWS CloudTrail | 帳戶 API 活動審計 | 想到帳戶操作審計 → CloudTrail |
| Amazon CloudWatch | 資源效能監控和告警 | 想到效能監控 → CloudWatch |
| Amazon Macie | S3 敏感資料探索 | 想到敏感資料 → Macie |
| Amazon GuardDuty | 威脅偵測 | 想到威脅偵測 → GuardDuty |

---

## 問題 2 / Question 2

**[題目 / Question]**
Which AWS service can automate code deployment to Amazon EC2 instances **as well as on-premises instances**?
哪個 AWS 服務可將代碼部署自動化到 EC2 執行個體**以及本地執行個體**？

**✅ 正確答案 / Correct Answer：AWS CodeDeploy**

**[中文詳解]**
**AWS CodeDeploy** 自動化代碼部署到任何執行個體，包括 EC2 和本地執行個體，幫助快速發布新功能，避免部署期間停機，並處理應用程式更新的複雜性，可擴展至數千個執行個體。

**[AWS 開發者工具比較 / Developer Tools Comparison]**

| 服務 / Service | 功能 / Function |
|---|---|
| **AWS CodeDeploy** | **自動化代碼部署（EC2 + 本地）** |
| AWS CodeCommit | 托管 Git 原始碼控制 |
| AWS CodeBuild | 建構和測試代碼 |
| AWS CodePipeline | 持續交付管道（整合上述服務）|

> **記憶法**：CodePipeline 是整合協調者，**本身不部署**；CodeDeploy 才是實際執行部署的服務

---

## 問題 3 / Question 3

**[題目 / Question]**
An IT company with a **hybrid cloud architecture** wants to **centralize server logs** for EC2 instances and on-premises servers. Which is MOST effective?
**混合雲**架構的 IT 公司想**集中化**管理 EC2 和本地伺服器的伺服器日誌，哪個最有效？

**✅ 正確答案 / Correct Answer：Use Amazon CloudWatch Logs for both（兩者都使用 Amazon CloudWatch Logs）**

**[中文詳解]**
**Amazon CloudWatch Logs** 可監控、儲存和存取來自 EC2 執行個體、AWS CloudTrail、Route 53 以及**本地伺服器**等來源的日誌文件，提供集中化的單一高度可擴展服務。

**[English Explanation]**
**Amazon CloudWatch Logs** centralizes logs from all systems, applications, and AWS services you use — including on-premises servers — in a single, highly scalable service.

> ⚠️ CloudTrail 記錄 API 活動，**不能**集中化伺服器日誌

---

## 問題 4 / Question 4

**[題目 / Question]**
A financial enterprise wants MFA for employees but prefers **no physical devices** for ease of travel. Which option is best suited?
金融企業想為員工啟用 MFA，但為了出行方便希望**不使用實體設備**，哪個選項最合適？

**✅ 正確答案 / Correct Answer：Virtual MFA device（虛擬 MFA 設備）**

**[MFA 類型比較 / MFA Types Comparison]**

| MFA 類型 / Type | 實體設備 | 說明 / Description |
|---|---|---|
| **Virtual MFA** | **❌ 無需** | **手機 App（如 Google Authenticator）產生 6 位數代碼** |
| Hardware MFA | ✅ 需要 | 硬體設備產生 6 位數代碼 |
| U2F Security Key | ✅ 需要 | 插入 USB 的實體金鑰，點擊設備登入 |
| Soft Token MFA | 虛構選項 | 干擾項 |

---

## 問題 5 / Question 5

**[題目 / Question]**
Which of the following AWS services offer **block-level storage**? (Select two)
以下哪兩個 AWS 服務提供**區塊層級儲存**？

**✅ 正確答案 / Correct Answers：**
1. Amazon Elastic Block Store (Amazon EBS)
2. Instance Store

**[儲存類型分類 / Storage Type Classification]**

| 儲存服務 / Service | 儲存類型 / Type | 特點 |
|---|---|---|
| **Amazon EBS** | **區塊 / Block** | 持久、高效能、可與 EC2 掛載 |
| **Instance Store** | **區塊 / Block** | 臨時、實體附加主機、高速 |
| Amazon EFS | 文件 / File | NFS 協議、多執行個體共享 |
| Amazon S3 | 物件 / Object | 高擴展性、網際網路存取 |
| Amazon ECS | 不是儲存服務 | 容器管理（干擾項）|

---

## 問題 6 / Question 6

**[題目 / Question]**
Which statements are CORRECT about the AWS Auto Scaling group? (Select two)
以下哪兩個關於 AWS Auto Scaling 群組的說法正確？

**✅ 正確答案 / Correct Answers：**
1. Auto Scaling group **scales out** and adds more EC2 instances to match an increase in demand
2. Auto Scaling group **scales in** and reduces the number of EC2 instances to match a decrease in demand

**[Auto Scaling 術語 / Auto Scaling Terminology — Must Know!]**

| 術語 / Term | 方向 / Direction | 動作 / Action |
|---|---|---|
| **Scale Out（向外擴展）** | ↑ 增加 | 新增更多執行個體 |
| **Scale In（向內縮減）** | ↓ 減少 | 移除執行個體 |
| Scale Up（向上擴展）| ↑ 升級 | 升級到更強大的執行個體（垂直，Auto Scaling **不做**）|
| Scale Down（向下縮減）| ↓ 降級 | 降級到較弱執行個體（垂直，Auto Scaling **不做**）|

> ⚠️ Auto Scaling 只做 **Scale Out / Scale In**（水平）；**不做** Scale Up / Scale Down（垂直）

---

## 問題 7 / Question 7

**[題目 / Question]**
A research group wants to provision an EC2 instance for a **flexible application that can be interrupted**. Which is the MOST cost-optimal?
研究組想為**可中斷的彈性應用程式**佈建 EC2，哪個最具成本效益？

**✅ 正確答案 / Correct Answer：Spot Instance（競價執行個體）**

**[中文詳解]**
**Spot 執行個體**是 AWS 未使用的 EC2 容量，可節省高達 90% 的費用。適合可容錯的工作負載：資料分析、批次作業、背景處理。**可在短暫通知後被終止**，因此不適合關鍵工作負載。

**[EC2 定價 — 中斷風險與折扣 / Pricing vs Interruption Risk]**

| 類型 / Type | 折扣 / Discount | 可中斷 | 適用場景 |
|---|---|---|---|
| On-Demand | 基準 / Baseline | ❌ | 靈活、無承諾 |
| Reserved (RI) | 最高 72% | ❌ | 長期穩定 |
| **Spot** | **最高 90%** | **✅ 會中斷** | **容錯、彈性工作** |
| Dedicated Host | 無折扣 | ❌ | 授權合規 |

---

## 問題 8 / Question 8

**[題目 / Question]**
Which Amazon Route 53 routing policy would you use for **active-passive configuration**?
哪個 Amazon Route 53 路由策略用於**主動-被動配置**？

**✅ 正確答案 / Correct Answer：Failover routing（容錯移轉路由）**

**[Route 53 路由策略完整對照 / Route 53 Routing Policies]**

| 策略 / Policy | 使用場景 / Use Case |
|---|---|
| Simple（簡單）| 路由到單一資源 |
| Weighted（加權）| 按比例分配流量（A/B 測試）|
| Latency-based（延遲）| 路由到最低延遲的 AWS 區域 |
| **Failover（容錯移轉）** | **主動-被動容錯移轉** ✅ |
| Geolocation（地理位置）| 按用戶地理位置路由 |
| Multivalue Answer（多值）| 返回多個健康 IP |

---

## 問題 9 / Question 9

**[題目 / Question]**
Which AWS service **monitors malicious activity and detects threats** to protect your AWS account?
哪個 AWS 服務**監控惡意活動並偵測威脅**以保護您的 AWS 帳戶？

**✅ 正確答案 / Correct Answer：Amazon GuardDuty**

**[中文詳解]**
**Amazon GuardDuty** 是威脅偵測服務，分析來自 AWS CloudTrail、Amazon VPC Flow Logs 和 DNS 日誌的數十億個事件，識別惡意活動和未授權行為。安全發現結果保留 90 天，可透過 CloudWatch Events 將結果推送到 S3 長期保留。

**[安全服務功能對照 / Security Services]**

| 服務 / Service | 功能 / Function |
|---|---|
| **Amazon GuardDuty** | **威脅偵測，分析 CloudTrail/VPC Flow Logs/DNS** |
| AWS CloudTrail | 帳戶 API 活動記錄（不偵測威脅）|
| Amazon CloudWatch | 效能監控（不偵測威脅）|
| AWS Trusted Advisor | 最佳實踐建議（不偵測威脅）|

---

## 問題 10 / Question 10

**[題目 / Question]**
As a Cloud Practitioner, which Amazon S3 storage class would you recommend for **data archival**?
作為 Cloud Practitioner，您會推薦哪個 Amazon S3 儲存類別用於**資料存檔**？

**✅ 正確答案 / Correct Answer：Amazon S3 Glacier Flexible Retrieval**

**[S3 存檔儲存類別比較 / S3 Archive Storage Classes]**

| 儲存類別 / Class | 費用 / Cost | 取回時間 / Retrieval | 適用場景 |
|---|---|---|---|
| S3 Standard | 最高 | 毫秒 | 頻繁存取 |
| S3 Intelligent-Tiering | 中等 | 毫秒 | 不確定存取模式 |
| S3 One Zone-IA | 低 | 毫秒 | 不頻繁+可重建 |
| **S3 Glacier Flexible Retrieval** | **極低** | **分鐘到小時** | **存檔、備份、DR** |
| S3 Glacier Deep Archive | 最低 | 12-48 小時 | 7-10 年長期合規存檔 |

---

## 問題 11 / Question 11

**[題目 / Question]**
Which AWS entity provides the information required to **launch an Amazon EC2 instance**?
哪個 AWS 實體提供**啟動 Amazon EC2 執行個體**所需的資訊？

**✅ 正確答案 / Correct Answer：Amazon Machine Image (AMI)（亞馬遜機器映像）**

**[中文詳解]**
**AMI** 包含啟動執行個體所需的所有資訊：
- EBS 快照（或 Instance Store 的根磁碟區模板）
- 啟動權限（控制哪些 AWS 帳戶可使用此 AMI）
- 區塊設備映射（指定啟動時要附加的磁碟區）

**[English Explanation]**
**AMI** provides all information needed to launch an instance: EBS snapshots (or root volume template), launch permissions, and block device mapping.

> ⚠️ **重要：AMI 必須與 EC2 執行個體在同一個 Region！如需跨 Region，必須先複製 AMI。**

---

## 問題 12 / Question 12

**[題目 / Question]**
Which of the following improves **availability** for a fleet of Amazon EC2 instances?
以下哪個提高了 Amazon EC2 執行個體群的**可用性**？

**✅ 正確答案 / Correct Answer：Deploy EC2 instances across different AZs in the same AWS Region（在同一 AWS 區域的不同 AZ 部署）**

**[中文詳解]**
將 EC2 執行個體跨不同可用區域部署，可確保在單一 AZ 故障時，其他 AZ 中的執行個體仍可繼續服務，從而提高整體可用性。

**[常見錯誤選項解析 / Common Distractor Analysis]**
- ❌ 在同一 AZ 中部署 → 無法提高可用性（單點故障）
- ❌ 「相同 AZ 跨兩個不同 Region」→ 邏輯錯誤！AZ 不能屬於兩個 Region
- ❌ 「不同 Region 的相同 AZ」→ 邏輯錯誤！Region 不能在 AZ 內部

---

## 問題 13 / Question 13

**[題目 / Question]**
An enterprise wants to ensure its IT investments align with business objectives. Which perspective of AWS CAF addresses **strategy management**?
企業想確保 IT 投資與業務目標一致，AWS CAF 哪個視角涵蓋**策略管理**？

**✅ 正確答案 / Correct Answer：Business Perspective（業務視角）**

**[AWS CAF 六大視角與能力 / AWS CAF Six Perspectives]**

| 視角 / Perspective | 重點 / Focus | 代表能力 |
|---|---|---|
| **Business（業務）** | **策略對齊、價值實現** | **策略管理、業務洞察** |
| People（人員）| 組織變革 | 雲端流暢性、人才管理 |
| Governance（治理）| 風險、合規、財務 | 應用程式組合管理 |
| Platform（平台）| 雲端設計和實施 | 平台工程 |
| Security（安全）| 保護資訊和系統 | 漏洞管理 |
| Operations（運營）| 日常運營和效能 | 效能和容量管理 |

---

## 問題 14 / Question 14

**[題目 / Question]**
Which AWS services specialize in **data migration** from on-premises to AWS Cloud? (Select two)
哪兩個 AWS 服務專門用於從本地到 AWS 雲端的**資料遷移**？

**✅ 正確答案 / Correct Answers：**
1. AWS Snowball（大量實體資料遷移）
2. AWS Database Migration Service (AWS DMS)（資料庫遷移）

**[資料遷移 vs 連接服務 / Migration vs Connectivity]**

| 服務 / Service | 類別 / Category | 說明 |
|---|---|---|
| **AWS Snowball** | **資料遷移** | 實體設備，TB 到 PB 級資料 |
| **AWS DMS** | **資料庫遷移** | 同構/異構資料庫遷移 |
| AWS Direct Connect | 連接服務 | 專用網路連接（非資料遷移）|
| AWS Transit Gateway | 連接服務 | VPC 互連（非資料遷移）|
| AWS Site-to-Site VPN | 連接服務 | 加密隧道（非資料遷移）|

---

## 問題 15 / Question 15

**[題目 / Question]**
A development team is looking for a forum with **the most frequent questions from AWS customers** and AWS provided solutions. Which AWS service can be used?
開發團隊想找包含 **AWS 客戶最常見問題**和 AWS 解決方案的資源，哪個服務？

**✅ 正確答案 / Correct Answer：AWS Knowledge Center（AWS 知識中心）**

**[AWS 支援資源比較 / AWS Support Resources]**

| 資源 / Resource | 用途 / Purpose | 網址 |
|---|---|---|
| **AWS Knowledge Center** | **最常見問題和 AWS 解決方案** | aws.amazon.com/premiumsupport/knowledge-center/ |
| AWS Support Center | 管理支援案例 | 透過管理控制台 |
| Service Health Dashboard | AWS 服務整體狀態 | health.aws.amazon.com/health/status |
| AWS Marketplace | 購買和部署第三方軟體 | marketplace.aws |

---

## 問題 16 / Question 16

**[題目 / Question]**
A financial company must store **multiple copies of data in geographically distant locations**. Which S3 solution is MOST resource-efficient?
金融公司必須在**地理位置遙遠的地方儲存多份資料副本**，哪個 S3 解決方案最具資源效率？

**✅ 正確答案 / Correct Answer：Use S3 cross-region replication (S3 CRR)（使用 S3 跨區域複製）**

**[S3 複製類型比較 / S3 Replication Types]**

| 類型 / Type | 複製範圍 | 適用場景 |
|---|---|---|
| **S3 CRR（跨區域複製）** | **不同 AWS 區域** | **合規、DR、地理分散** |
| S3 SRR（同區域複製）| 同一 AWS 區域內 | 日誌聚合、測試環境複製 |

> ⚠️ Lambda 和 EC2 方案雖可行但不夠「資源高效」，CRR 是開箱即用的最佳解決方案

---

## 問題 17 / Question 17

**[題目 / Question]**
Which of the following AWS services are **regional in scope**? (Select two)
以下哪兩個 AWS 服務是**區域範圍**的？

**✅ 正確答案 / Correct Answers：**
1. AWS Lambda
2. Amazon Rekognition

**[全球 vs 區域服務快速記憶 / Global vs Regional]**

| 全球服務 / Global | 區域服務 / Regional |
|---|---|
| AWS IAM | **AWS Lambda** ✅ |
| Amazon CloudFront | **Amazon Rekognition** ✅ |
| Amazon Route 53 | Amazon EC2, RDS, VPC |
| AWS WAF | Amazon S3（桶是區域的）|

---

## 問題 18 / Question 18

**[題目 / Question]**
A research firm needs to search through old patents and documents (PDFs, Word, Text files) to find the most relevant files. Which AWS service is correct?
研究公司需要搜索舊專利和文件（PDF、Word、文字文件）找到最相關文件，哪個服務正確？

**✅ 正確答案 / Correct Answer：Amazon Kendra**

**[中文詳解]**
**Amazon Kendra** 是由機器學習驅動的智能搜索服務，支援非結構化和半結構化資料（HTML、MS Office、PDF、文字格式），提供自然語言搜索能力，無需伺服器，預先訓練了 14 個行業領域的深度學習模型。

**[AI/ML 服務比較 / AI/ML Services]**

| 服務 / Service | 功能 / Function |
|---|---|
| **Amazon Kendra** | **企業智能搜索（文件搜索）** |
| Amazon Comprehend | 自然語言處理 (NLP)，理解文字 |
| Amazon Personalize | 個人化推薦（如 Amazon.com）|
| Amazon Lex | 建立對話介面（聊天機器人）|
| Amazon Rekognition | 圖像/視訊分析 |

---

## 問題 19 / Question 19

**[題目 / Question]**
Under the AWS Shared Responsibility Model, which is the customer's responsibility regarding AWS Lambda?
在 AWS 共同責任模型下，以下哪項是客戶對 AWS Lambda 的責任？

**✅ 正確答案 / Correct Answer：Maintain versions of an AWS Lambda function（維護 Lambda 函數的版本）**

**[Lambda 共同責任劃分 / Lambda Shared Responsibility]**

| 責任項目 / Item | AWS | 客戶 |
|---|---|---|
| 修補底層 OS | ✅ | ❌ |
| 維護所有運行環境 | ✅ | ❌ |
| 配置網路基礎設施 | ✅ | ❌ |
| **維護 Lambda 函數版本** | ❌ | **✅** |
| 函數代碼 / Function code | ❌ | ✅ |

> **記憶法**：Lambda 是抽象服務（如 S3、DynamoDB），AWS 管底層；客戶管**自己的代碼和函數版本**

---

## 問題 20 / Question 20

**[題目 / Question]**
Which of the following AWS services have **data encryption automatically enabled**? (Select two)
以下哪兩個 AWS 服務**預設自動啟用**資料加密？

**✅ 正確答案 / Correct Answers：**
1. Amazon Simple Storage Service (Amazon S3)
2. AWS Storage Gateway

**[加密預設狀態 / Default Encryption Status]**

| 服務 / Service | 預設加密 / Default | 說明 |
|---|---|---|
| **Amazon S3** | **✅ 預設啟用** | 所有儲存桶預設使用 SSE-S3 |
| **AWS Storage Gateway** | **✅ 預設啟用** | 傳輸時使用 SSL（三種閘道類型均適用）|
| CloudTrail Logs | ✅ 預設啟用（S3 SSE-S3）| |
| Amazon EBS | ❌ 可選 | 需手動啟用 |
| Amazon Redshift | ❌ 可選 | 加密是可選設定 |
| Amazon EFS | ❌ 可選 | 靜態和傳輸中加密均為可選 |

---

## 問題 21 / Question 21

**[題目 / Question]**
Which statement is correct regarding Amazon Elastic File System (Amazon EFS)?
以下哪個關於 Amazon EFS 的說法正確？

**✅ 正確答案 / Correct Answer：**
EC2 instances can access files on an Amazon EFS file system **across many AZs, Regions and VPCs**.
EC2 執行個體可以跨**多個 AZ、Region 和 VPC** 存取 EFS 文件系統。

**[EFS 存取範圍 / EFS Access Scope]**
- ✅ 跨多個可用區域 (AZ)
- ✅ 跨多個 Region（透過 VPC Peering 或 Transit Gateway）
- ✅ 跨多個 VPC
- ✅ 本地伺服器（透過 AWS Direct Connect 或 AWS VPN）

> EFS 是**區域**服務，在 AZ 之間和 AZ 內部儲存資料以實現高可用性和耐久性

---

## 問題 22 / Question 22

**[題目 / Question]**
A cyber-security agency wants to carry out **security assessments on its own AWS infrastructure without prior AWS approval**. Which describes this practice?
網路安全機構想在**無需 AWS 事先批准**的情況下對自己的 AWS 基礎設施進行安全評估，哪個描述了這個實踐？

**✅ 正確答案 / Correct Answer：Penetration Testing（滲透測試）**

**[中文詳解]**
AWS 客戶可以對自己的 AWS 基礎設施進行安全評估或滲透測試，**無需事先獲得 AWS 批准**，適用於幾種常見 AWS 服務。但客戶**不得**對 AWS 基礎設施本身或 AWS 服務進行安全評估。

**[English Explanation]**
AWS customers can conduct security assessments or penetration tests against their own AWS infrastructure **without prior approval** for common AWS services. Customers are NOT permitted to conduct assessments of AWS infrastructure itself.

> ⚠️ 網路壓力測試（Network Stress Testing）≠ 滲透測試（Penetration Testing）

---

## 問題 23 / Question 23

**[題目 / Question]**
Which of the following is a part of the **AWS Global Infrastructure**?
以下哪個是 **AWS 全球基礎設施**的一部分？

**✅ 正確答案 / Correct Answer：AWS Region（AWS 區域）**

**[AWS 全球基礎設施組成 / AWS Global Infrastructure Components]**

| 組成 / Component | AWS 全球基礎設施 | 說明 |
|---|---|---|
| **AWS Region** | **✅ 是** | 全球物理位置，每個 Region 含多個 AZ |
| Availability Zone (AZ) | ✅ 是 | Region 內的獨立資料中心群 |
| Edge Locations | ✅ 是 | CloudFront CDN 快取節點 |
| Amazon VPC | ❌ 不是 | 邏輯隔離的網路環境（客戶資源）|
| VPN | ❌ 不是 | 連接服務 |
| Subnet | ❌ 不是 | VPC 內的 IP 範圍（單一 AZ）|

---

## 問題 24 / Question 24

**[題目 / Question]**
An IT company has deployed a static website on Amazon S3, but the website is **still inaccessible**. What would you suggest?
IT 公司在 S3 上部署了靜態網站，但網站**仍然無法存取**，您會建議什麼？

**✅ 正確答案 / Correct Answer：Fix the Amazon S3 bucket policy（修復 Amazon S3 儲存桶策略）**

**[中文詳解]**
在 S3 上託管靜態網站時，必須**啟用網站託管、設定公開存取許可並建立索引文件**。網站無法存取最常見的原因是儲存桶策略限制了公開存取（包括帳戶層級或儲存桶層級的 Block Public Access 設定）。

**[S3 靜態網站故障排除 / Static Website Troubleshooting]**
- ✅ 修復儲存桶策略（啟用公開存取）
- ❌ 停用加密 → 不影響網站存取
- ❌ 啟用版本控制 → 不影響網站存取
- ❌ 啟用複製 → 不影響網站存取

---

## 問題 25 / Question 25

**[題目 / Question]**
An e-commerce company wants to receive **separate invoices** for development and production environments. Which solution would you recommend?
電商公司想為開發和生產環境接收**獨立發票**，您會推薦哪個解決方案？

**✅ 正確答案 / Correct Answer：Create separate AWS accounts for each environment（為每個環境建立獨立 AWS 帳戶）**

**[中文詳解]**
每個 AWS 帳戶每月都會提供獨立的發票。為開發和生產環境設定獨立的 AWS 帳戶，即可獲得獨立發票。

**[重要澄清 / Key Clarification]**
- **獨立帳戶** → 獨立發票 ✅
- AWS Organizations → 集中計費，單一付款方式（不是獨立發票）
- 標籤 → 可追蹤成本，但無法產生獨立發票
- Cost Explorer → 視覺化費用，無法產生獨立發票

---

## 問題 26 / Question 26

**[題目 / Question]**
An AWS hardware failure has impacted one of your Amazon EBS volumes. Which AWS service will **alert you and provide remedial action**?
AWS 硬體故障影響了 EBS 磁碟區，哪個 AWS 服務會**告警您並提供補救措施**？

**✅ 正確答案 / Correct Answer：AWS Health Dashboard – Your account health（帳戶健康儀表板）**

**[中文詳解]**
**AWS Health Dashboard – Your account health** 在 AWS 事件影響到您時提供告警和補救指導。告警由您的 AWS 資源健康狀況變化觸發，提供事件可見性和快速診斷解決問題的指導。

**[帳戶健康儀表板 vs 服務健康儀表板 / Account vs Service Health]**

| 儀表板 / Dashboard | 觸發條件 | 網址 |
|---|---|---|
| **Account Health（帳戶）** | **您的資源受影響** | health.aws.amazon.com/health/home |
| Service Health（服務）| 所有 AWS 服務狀態 | health.aws.amazon.com/health/status |

---

## 問題 27 / Question 27

**[題目 / Question]**
Which AWS service will you use to **privately connect your VPC to Amazon S3**?
哪個 AWS 服務可**私密連接您的 VPC 到 Amazon S3**？

**✅ 正確答案 / Correct Answer：VPC Endpoint（VPC 端點）**

**[VPC 端點類型 / VPC Endpoint Types]**

| 類型 / Type | 說明 / Description | 支援服務 |
|---|---|---|
| **Gateway Endpoint（閘道端點）** | 在路由表中指定為目標的閘道 | **僅 S3 和 DynamoDB** |
| Interface Endpoint（介面端點）| 帶有私有 IP 的彈性網路介面 | 其他大多數 AWS 服務 |

> **考試提醒**：只有 **S3** 和 **DynamoDB** 支援 **VPC Gateway Endpoint**！
> Amazon S3 同時支援 Interface 和 Gateway 兩種端點

---

## 問題 28 / Question 28

**[題目 / Question]**
Compared to on-demand prices, what is the highest possible discount for **reserved instances (RI)**?
與隨需價格相比，**預留執行個體**最高可享多少折扣？

**✅ 正確答案 / Correct Answer：72%**

**[EC2 最高折扣對照 / Maximum Discounts]**

| 類型 / Type | 最高折扣 / Max Discount |
|---|---|
| Reserved Instance (RI) | **最高 72%** |
| Spot Instance | 最高 90% |

> ⚠️ **注意**：第一回題目說 RI 最高節省 75%，本題說最高 72%。以官方最新資料為準（72% 是較新的數字）。考試中不需記住精確數字，只需記得 RI 提供重大折扣，Spot 折扣最高。

---

## 問題 29 / Question 29

**[題目 / Question]**
Which use case is best suited for **Amazon EFS Standard-Infrequent Access (EFS Standard-IA)** storage class?
哪個使用案例最適合 **Amazon EFS Standard-IA** 儲存類別？

**✅ 正確答案 / Correct Answer：Storing files in an accessible location to satisfy audit requirements（在可存取位置儲存文件以滿足審計要求）**

**[EFS 儲存類別比較 / EFS Storage Classes]**

| 儲存類別 / Class | 說明 / Description | 使用場景 |
|---|---|---|
| EFS Standard | 頻繁存取 | 日常工作文件 |
| **EFS Standard-IA** | **不頻繁存取，多 AZ** | **審計合規、歷史分析、備份** |
| EFS One Zone-IA | 不頻繁存取，單一 AZ | 非關鍵性不頻繁存取 |

**[EFS Standard-IA 不適用的場景 / What EFS Standard-IA Cannot Do]**
- ❌ 用作 EC2 啟動磁碟區（需用 EBS）
- ❌ 物件儲存（EFS 是文件服務，不是物件服務）
- ❌ 儲存在單一 AZ（那是 One Zone-IA）

---

## 問題 30 / Question 30

**[題目 / Question]**
An IT company wants to move its IT resources from a US AWS Region to a European AWS Region. Which solution is correct?
IT 公司想將 IT 資源從美國 AWS 區域遷移到歐洲 AWS 區域，哪個解決方案正確？

**✅ 正確答案 / Correct Answer：**
The company should **start creating new resources in the destination Region** and then migrate relevant data and applications.
公司應該**在目標 Region 中建立新資源**，然後遷移相關資料和應用程式。

**[中文詳解]**
跨 AWS Region 遷移整個 IT 資源沒有開箱即用的遷移解決方案或服務。公司需要在新 Region 建立資源，再手動遷移資料和應用程式。

> ⚠️ CloudFormation 可以協助跨 Region 佈建資源，但**無法幫助遷移資料**
> ⚠️ AWS DMS 只能遷移資料庫，不能遷移整個 IT 資源

---

## 問題 31 / Question 31

**[題目 / Question]**
Which of the following are recommended best practices for AWS IAM? (Select two)
以下哪兩個是 AWS IAM 的推薦最佳實踐？

**✅ 正確答案 / Correct Answers：**
1. Rotate credentials regularly（定期輪換憑證）
2. Enable MFA for all users（為所有使用者啟用 MFA）

**[AWS IAM 最佳實踐完整清單 / IAM Best Practices]**

| 最佳實踐 / Best Practice | 說明 |
|---|---|
| ✅ 為所有使用者啟用 MFA | 包括 root 使用者 |
| ✅ 定期輪換憑證 | 密碼和存取金鑰 |
| ✅ 最小權限原則 | 只授予必要的權限 |
| ✅ 不分享 root 憑證 | 任何人都不分享 |
| ❌ 共享帳戶憑證 | 嚴禁，應建立個別帳戶 |
| ❌ 授予最大權限 | 違反最小權限原則 |

---

## 問題 32 / Question 32

**[題目 / Question]**
Which AWS service can be used for **online analytical processing (OLAP)**?
哪個 AWS 服務可用於**線上分析處理 (OLAP)**？

**✅ 正確答案 / Correct Answer：Amazon Redshift**

**[資料庫使用場景 / Database Use Cases]**

| 服務 / Service | 類型 / Type | 使用場景 |
|---|---|---|
| **Amazon Redshift** | **資料倉儲 / Data Warehouse** | **OLAP（分析、報告、BI）** |
| Amazon RDS | 關聯式資料庫 | OLTP（線上交易處理）|
| Amazon DynamoDB | NoSQL | 高效能應用程式 |
| Amazon ElastiCache | 記憶體快取 | 即時快取、會話儲存 |
| Amazon Athena | 無伺服器查詢 | 直接分析 S3 資料 |

> **記憶法**：OLTP（交易）→ RDS；OLAP（分析）→ Redshift

---

## 問題 33 / Question 33

**[題目 / Question]**
A startup's CTO would like **detailed reports that break down AWS costs by the hour** to an Amazon S3 bucket. Which AWS service would you recommend?
新創公司 CTO 想要**按小時明細分解 AWS 費用的詳細報告**存入 S3，推薦哪個服務？

**✅ 正確答案 / Correct Answer：AWS Cost & Usage Report (AWS CUR)**

**[成本工具功能比較 / Cost Tools Comparison — Exam Alert!]**

| 工具 / Tool | 主要功能 | 輸出到 S3 | 按小時明細 |
|---|---|---|---|
| **AWS CUR** | **最詳細的費用和使用資料** | **✅** | **✅** |
| AWS Cost Explorer | 視覺化費用趨勢（最多 12 個月）| ❌ | ❌ |
| AWS Budgets | 預算告警 | ❌ | ❌ |
| Pricing Calculator | 事前成本估算 | ❌ | N/A |

> **關鍵區別**：
> - **AWS CUR** → 最詳細的成本資料，輸出到 S3，**按小時/月細分**
> - **AWS Cost Explorer** → 高層次視覺化工具，分析趨勢

---

## 問題 34 / Question 34

**[題目 / Question]**
Which pillar of the AWS Well-Architected Framework recommends maintaining **infrastructure as code (IaC)**?
AWS Well-Architected Framework 哪個支柱建議維護**基礎設施即代碼 (IaC)**？

**✅ 正確答案 / Correct Answer：Operational Excellence（卓越運營）**

**[中文詳解]**
**卓越運營支柱**包括以代碼形式定義整個工作負載（應用程式、基礎設施），並以代碼更新。可以將操作程序實作為代碼，並透過觸發事件自動執行。IaC 是卓越運營的核心原則。

**[六大支柱關鍵字 / Six Pillars Keywords]**

| 支柱 / Pillar | 關鍵字 / Keywords |
|---|---|
| **Operational Excellence（卓越運營）** | **IaC、自動化操作、持續改進** |
| Security（安全）| 保護資訊和系統 |
| Reliability（可靠性）| 從故障恢復 |
| Performance Efficiency（效能效率）| 高效使用資源 |
| Cost Optimization（成本優化）| 避免不必要費用 |
| Sustainability（可持續性）| 降低環境影響 |

---

## 問題 35 / Question 35

**[題目 / Question]**
Which Amazon S3 storage class offers the **lowest availability**?
哪個 Amazon S3 儲存類別提供**最低可用性**？

**✅ 正確答案 / Correct Answer：Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)**

**[原因 / Reason]**
S3 One Zone-IA 只在**單一 AZ** 中儲存資料，不像其他儲存類別最少跨三個 AZ。雖然可用性較低（99.5%），但費用比 Standard-IA 便宜 20%，適合可重新生成或非關鍵的資料。

**[S3 可用性排序 / Availability Ranking — Lowest]**
> S3 One Zone-IA (99.5%) < S3 Standard-IA / Glacier / Intelligent-Tiering (99.9%) < S3 Standard (99.99%)

---

## 問題 36 / Question 36

**[題目 / Question]**
A startup runs containers on Docker and wants to **still have access to the underlying servers**. Which AWS service would you recommend?
新創公司在 Docker 上運行容器，但仍想**存取底層伺服器**，推薦哪個服務？

**✅ 正確答案 / Correct Answer：Amazon Elastic Container Service (Amazon ECS)**

**[容器服務存取底層對比 / Container Services — Underlying Server Access]**

| 服務 / Service | 存取底層伺服器 | 說明 |
|---|---|---|
| **Amazon ECS** | **✅ 可以** | 非全托管，可管理底層 EC2 |
| AWS Fargate | ❌ 不可以 | 全托管無伺服器，不暴露底層 |
| AWS Lambda | ❌ 不可以 | 無伺服器，不運行容器 |
| Amazon ECR | ❌ 不可以 | 存放映像，不運行容器 |

---

## 問題 37 / Question 37

**[題目 / Question]**
A global e-commerce platform wants to **restrict access from specific countries** to comply with regional regulations. Which AWS service is best suited?
全球電商平台想**限制特定國家的存取**以符合區域法規，哪個服務最合適？

**✅ 正確答案 / Correct Answer：Amazon WAF**

**[中文詳解]**
**AWS WAF** 可建立地理比對 (geo-match) 條件，封鎖來自特定國家/地區的 Web 請求，確保符合區域政策。IP 位址到國家的對應準確率達 **99.8%**。

**[混淆選項 / Distractor Clarification]**
- Amazon Pinpoint → 客戶參與和行銷（不限制地理存取）
- Amazon Fraud Detector → 詐騙識別（不限制地理存取）
- AWS Shield → DDoS 防護（不限制地理存取）

---

## 問題 38 / Question 38

**[題目 / Question]**
Which of the following are components of an **AWS Site-to-Site VPN**? (Select two)
以下哪兩個是 **AWS Site-to-Site VPN** 的組件？

**✅ 正確答案 / Correct Answers：**
1. Virtual private gateway (VGW)（虛擬私有閘道）
2. Customer gateway（客戶閘道）

**[Site-to-Site VPN 架構 / VPN Architecture]**
```
您的本地網路 / On-premises
        ↕（IPsec 加密隧道 / Encrypted tunnel）
Customer Gateway（您的 VPN 設備資訊在 AWS 中的表示）
        ↕
Virtual Private Gateway（AWS VPC 側的 VPN 集中器）
        ↕
Amazon VPC
```

**[VPN 相關組件澄清 / VPN Components Clarification]**
- NAT Gateway → NAT 轉換，不是 VPN 組件
- AWS Storage Gateway → 混合雲儲存，不是 VPN 組件
- Internet Gateway → VPC 上網，不是 VPN 組件

---

## 問題 39 / Question 39

**[題目 / Question]**
AWS Lambda pricing is based on which criteria? (Select two)
AWS Lambda 定價基於哪兩個標準？

**✅ 正確答案 / Correct Answers：**
1. Number of requests（請求次數）
2. The time it takes for the Lambda function to execute（函數執行時間）

**[Lambda 定價公式 / Lambda Pricing Formula]**
```
Lambda 費用 = 請求費用 + 計算時間費用

請求費用：每次函數執行計為一次請求
計算時間：從代碼開始執行到終止，四捨五入到最近的 100ms
```

**[不影響定價的因素 / Factors NOT Affecting Pricing]**
- ❌ 程式語言運行環境（NodeJS、Python、Go 等）
- ❌ 代碼行數
- ❌ 部署套件大小

---

## 問題 40 / Question 40

**[題目 / Question]**
Which budget types can be created under AWS Budgets? (Select three)
在 AWS Budgets 下可以建立哪三種預算類型？

**✅ 正確答案 / Correct Answers：**
1. Cost budget（費用預算）
2. Usage budget（使用量預算）
3. Reservation budget（預留預算）

**[AWS Budgets 四種預算類型 / Four Budget Types]**

| 類型 / Type | 用途 / Purpose |
|---|---|
| **Cost budget（費用預算）** | 規劃在服務上的花費 |
| **Usage budget（使用量預算）** | 規劃使用一個或多個服務的數量 |
| **Reservation budget（預留預算）** | 追蹤 RI 使用率和覆蓋率 |
| Savings Plans budget | 追蹤 Savings Plans 使用率 |

> ⚠️ Resource budget、Software budget、Hardware budget 均為**虛構選項**

---

## 問題 41 / Question 41

**[題目 / Question]**
Which cloud feature offers the ability to **innovate faster and rapidly develop, test and launch software applications**?
哪個雲端功能提供**更快創新、快速開發、測試和發布軟體應用程式**的能力？

**✅ 正確答案 / Correct Answer：Agility（敏捷性）**

**[雲端優勢 vs 雲端特性辨別 / Cloud Benefits vs Characteristics]**

| 概念 / Concept | 定義 |
|---|---|
| **Agility（敏捷性）** | **快速存取廣泛技術，加速創新** |
| Elasticity（彈性）| 按需獲取並釋放資源 |
| Cost savings（成本節省）| 資本支出換可變支出 |
| 全球部署 | 幾分鐘內擴展到全球區域 |

---

## 問題 42 / Question 42

**[題目 / Question]**
Which is correct regarding **AWS Shield Advanced pricing**?
以下哪個關於 **AWS Shield Advanced 定價**的說法正確？

**✅ 正確答案 / Correct Answer：**
AWS Shield Advanced offers **protection against higher fees** that could result from a DDoS attack.
AWS Shield Advanced 提供針對 DDoS 攻擊可能導致的**更高費用的保護**。

**[中文詳解]**
AWS Shield Advanced 提供一定的成本保護，防止因 DDoS 攻擊導致的 AWS 帳單飆升，保護的資源包括：ELB、CloudFront、Route 53、EC2、AWS Global Accelerator。

> ⚠️ **AWS Shield Advanced 是付費服務，對所有客戶收費，無論支援方案為何！**
> - Shield Standard → 免費，所有客戶自動啟用
> - **Shield Advanced → 付費，需訂閱**

---

## 問題 43 / Question 43

**[題目 / Question]**
Which AWS service can **execute code triggered by new files being uploaded to Amazon S3**?
哪個 AWS 服務可以**執行由新文件上傳到 S3 觸發的代碼**？

**✅ 正確答案 / Correct Answer：AWS Lambda**

**[S3 觸發 Lambda 的典型使用案例 / S3 → Lambda Use Cases]**
- 圖片縮圖生成
- 視訊轉碼
- 文件索引
- 日誌處理
- 資料驗證
- 即時資料彙總和過濾

**[為什麼其他選項不符 / Why Others Don't Qualify]**
- EC2 → 無法透過 S3 事件觸發執行代碼
- ECS → 無法透過 S3 事件觸發執行代碼
- SQS → 雖可接收 S3 事件通知，但 SQS 是訊息佇列，**不能執行代碼**

---

## 問題 44 / Question 44

**[題目 / Question]**
AWS IAM policies are written as JSON documents. Which are **mandatory elements** of an IAM policy?
AWS IAM 策略以 JSON 文件編寫，IAM 策略的**必要元素**是哪些？

**✅ 正確答案 / Correct Answer：Effect, Action**

**[IAM 策略 JSON 元素 / IAM Policy JSON Elements]**

| 元素 / Element | 必要性 / Required | 說明 / Description |
|---|---|---|
| Version | 建議 | 策略語言版本（建議使用 2012-10-17）|
| Statement | ✅ | 策略陳述容器 |
| **Effect** | **✅ 必要** | **Allow 或 Deny** |
| Principal | 部分情況必要 | 資源型策略需要 |
| **Action** | **✅ 必要** | **允許或拒絕的操作列表** |
| Resource | 部分情況必要 | IAM 許可策略需要 |
| Sid | ❌ 可選 | 陳述識別符 |
| Condition | ❌ 可選 | 授予權限的條件 |

---

## 問題 45 / Question 45

**[題目 / Question]**
A research lab wants to **optimize caching** for its scientific computations on EC2 instances. Which EC2 storage option is best?
研究實驗室想**優化 EC2 執行個體上科學計算的快取**，哪個儲存選項最好？

**✅ 正確答案 / Correct Answer：Instance Store（執行個體存放區）**

**[中文詳解]**
**Instance Store** 最適合需要頻繁變化的臨時資訊儲存：緩衝區、快取、暫存資料和其他臨時內容。實體附加在主機電腦上，提供最低延遲的 I/O 效能。執行個體終止時資料遺失，但快取資料可重新生成，因此這不是問題。

**[快取最佳儲存 / Best Storage for Caching]**

| 儲存 / Storage | 延遲 / Latency | 快取適用性 |
|---|---|---|
| **Instance Store** | **最低 / Lowest** | **✅ 最佳（臨時高速）** |
| EBS | 低 / Low | 可用但非最佳 |
| EFS | 中等 / Medium | 不適合快取 |
| S3 | 高 / High | 不適合快取 |

---

## 問題 46 / Question 46

**[題目 / Question]**
Which statements are correct regarding Amazon EFS and Amazon EBS pricing? (Select two)
以下哪兩個關於 Amazon EFS 和 EBS 定價的說法正確？

**✅ 正確答案 / Correct Answers：**
1. **EBS Snapshots are stored incrementally** — you are billed only for changed blocks stored
2. **You pay a fee each time you read from or write to EFS Standard-IA**

**[EFS 和 EBS 定價要點 / EFS & EBS Pricing Points]**

| 服務/功能 | 定價模式 | 說明 |
|---|---|---|
| **EBS Snapshots** | **增量儲存計費** | 只為變更的區塊付費；儲存在 S3 |
| **EFS Standard-IA** | **儲存費用低 + 每次讀寫收費** | 適合不頻繁存取的文件 |
| EBS Snapshot 儲存 | 基於 S3 空間（非 EBS 空間）| EBS 不儲存空區塊 |
| AWS Backup (EFS) | 備份儲存 + 恢復費用 | 恢復資料**需要**付費 |

---

## 問題 47 / Question 47

**[題目 / Question]**
What is the best way to **protect your data from accidental deletion** on Amazon S3?
在 Amazon S3 上**防止資料意外刪除**的最佳方法是什麼？

**✅ 正確答案 / Correct Answer：Amazon S3 Versioning（Amazon S3 版本控制）**

**[中文詳解]**
**Amazon S3 版本控制**在同一儲存桶中保留物件的多個變體，可保存、取回和恢復每個物件的每個版本。啟用版本控制後，刪除物件不會永久移除，而是插入一個刪除標記，使其成為當前版本，原始資料仍可恢復。

**[S3 功能 vs 資料保護 / S3 Features vs Data Protection]**

| S3 功能 / Feature | 用途 / Purpose | 防止意外刪除 |
|---|---|---|
| **S3 Versioning** | **保留物件多個版本** | **✅ 最佳** |
| S3 Lifecycle | 管理物件生命週期和費用 | ❌ |
| Storage Classes | 不同存取模式的儲存選擇 | ❌ |
| Transfer Acceleration | 加快長距離文件傳輸 | ❌ |

---

## 問題 48 / Question 48

**[題目 / Question]**
What is the **primary benefit** of Amazon RDS in a **Read Replica** configuration?
Amazon RDS **讀取副本**配置的**主要優勢**是什麼？

**✅ 正確答案 / Correct Answer：Read Replica improves database **scalability**（讀取副本提高資料庫**可擴展性**）**

**[RDS 三種部署模式比較 / RDS Deployment Modes — Must Know!]**

| 部署模式 / Mode | 主要優勢 / Primary Benefit | 特點 |
|---|---|---|
| **Read Replica（讀取副本）** | **可擴展性（讀取效能）** | 非同步複製，可手動提升，端點會變 |
| Multi-AZ（多 AZ，單備用）| 高可用性 | 同步複製，自動容錯移轉，端點不變 |
| Multi-Region（多區域）| 區域容災保護 | 跨區域保護 |

---

## 問題 49 / Question 49

**[題目 / Question]**
Which AWS services/features support **High Availability by default**? (Select two)
哪兩個 AWS 服務/功能**預設支援高可用性**？

**✅ 正確答案 / Correct Answers：**
1. Amazon Elastic File System (Amazon EFS)
2. Amazon DynamoDB

**[預設高可用性服務 / Services with Default HA]**

| 服務 / Service | 預設 HA | 說明 |
|---|---|---|
| **Amazon DynamoDB** | **✅** | 自動跨多個 AZ 複製資料 |
| **Amazon EFS** | **✅** | 區域服務，跨多個 AZ 儲存 |
| Amazon EBS | ❌ | 在 AZ 內複製（單 AZ）|
| Instance Store | ❌ | 單一 AZ，臨時性 |
| Subnet | ❌ | 只在單一 AZ |

---

## 問題 50 / Question 50

**[題目 / Question]**
An organization maintains **separate VPCs for each department** and wants to **connect all VPCs for collaboration**. Which AWS service will help effectively?
組織為每個部門維護**獨立 VPC**，想**連接所有 VPC**促進協作，哪個服務最有效？

**✅ 正確答案 / Correct Answer：AWS Transit Gateway**

**[VPC 連接方案比較 / VPC Connectivity Options]**

| 方案 / Solution | 擴展性 | 管理複雜度 | 傳遞性 |
|---|---|---|---|
| **AWS Transit Gateway** | **✅ 高** | **低（Hub-and-Spoke）** | **✅ 支援** |
| VPC Peering | 有限 | 高（N×(N-1)/2 連接）| ❌ 不支援傳遞 |
| AWS Direct Connect | 本地到 VPC | 中 | N/A |

> **VPC Peering 的問題**：非傳遞性，大量 VPC 時需建立大量點對點連接，複雜且難管理
> **Transit Gateway** 的優勢：中央樞紐，每個連接只需建立一次

---

## 問題 51 / Question 51

**[題目 / Question]**
Which of the following capabilities does Amazon Rekognition provide as a **ready-to-use feature**?
Amazon Rekognition 提供哪個**開箱即用**的功能？

**✅ 正確答案 / Correct Answer：Identify objects in a photo（識別照片中的物件）**

**[Amazon Rekognition 支援 vs 不支援 / Rekognition Capabilities]**

| 功能 / Feature | 支援 / Supported |
|---|---|
| ✅ 識別物件、人物、文字、場景、活動 | ✅ |
| ✅ 偵測不當內容 | ✅ |
| ✅ 臉部分析和搜索 | ✅ |
| ❌ 調整圖片大小 / Resize images | ❌ |
| ❌ 轉換灰階 / Convert to greyscale | ❌ |
| ❌ 人體姿態偵測 / Human pose detection | ❌ |

---

## 問題 52 / Question 52

**[題目 / Question]**
What is the **region-specific constraint** that an AMI must meet for use with an EC2 instance?
AMI 在與 EC2 執行個體搭配使用時必須符合哪個**區域特定限制**？

**✅ 正確答案 / Correct Answer：**
You must use an AMI from the **same region** as the EC2 instance. **The region of the AMI has no bearing on performance.**
AMI 必須與 EC2 執行個體在**同一個 Region**。**AMI 的 Region 不影響效能。**

**[AMI 區域規則 / AMI Region Rules]**
- ✅ AMI 必須與 EC2 在同一個 Region
- ✅ 可以將 AMI 複製到其他 Region
- ❌ AMI 不是全球實體
- ❌ 使用不同 Region 的 AMI 不影響效能（但不允許直接使用）

---

## 問題 53 / Question 53

**[題目 / Question]**
Which AWS service can be used as an **in-memory database with high-performance and low latency**?
哪個 AWS 服務可用作**高效能低延遲的記憶體資料庫**？

**✅ 正確答案 / Correct Answer：Amazon ElastiCache**

**[中文詳解]**
**Amazon ElastiCache** 讓您在雲端無縫設定、運行和擴展開源相容的記憶體資料存儲（Redis 和 Memcached）。適用場景：快取、會話儲存、遊戲、地理空間服務、即時分析和佇列。

**[資料庫類型完整對照 / Database Types Reference]**

| 服務 / Service | 類型 / Type | 使用場景 |
|---|---|---|
| **Amazon ElastiCache** | **記憶體 / In-memory** | **快取、即時低延遲** |
| Amazon DynamoDB | NoSQL 鍵值/文件 | 高擴展性應用 |
| Amazon RDS | 關聯式 OLTP | 交易型應用 |
| Amazon Redshift | 資料倉儲 OLAP | 分析報告 |
| Amazon Athena | 無伺服器查詢 | S3 資料 SQL 查詢 |
| Amazon Neptune | 圖形資料庫 | 社交網路、推薦引擎 |

---

## 問題 54 / Question 54

**[題目 / Question]**
Which statements are CORRECT regarding **security groups** and **network ACL**? (Select two)
以下哪兩個關於**安全群組**和**網路 ACL** 的說法正確？

**✅ 正確答案 / Correct Answers：**
1. **A security group is stateful** — it automatically allows return traffic
2. **A network ACL contains a numbered list of rules** and evaluates them in increasing order

**[安全群組 vs 網路 ACL 詳細比較 / Security Group vs Network ACL]**

| 特性 / Feature | 安全群組 / Security Group | 網路 ACL / Network ACL |
|---|---|---|
| 作用層級 | 執行個體 / Instance | 子網路 / Subnet |
| 規則類型 | 僅允許 / Allow only | 允許 + 拒絕 / Allow & Deny |
| **狀態 / Stateful** | **✅ 有狀態（回傳流量自動允許）** | **❌ 無狀態（回傳流量需明確允許）** |
| 規則評估 | **評估所有規則** | **按編號順序（由小到大）** |
| 規則編號 | 無需編號 | 需要編號（1-32766）|

---

## 問題 55 / Question 55

**[題目 / Question]**
A company has a static website on S3 in an Asia Region, and wants to **improve global performance**. How can it improve the global performance?
公司在亞洲 Region 的 S3 上有靜態網站，想**提升全球效能**，如何實現？

**✅ 正確答案 / Correct Answer：Use Amazon CloudFront（使用 Amazon CloudFront）**

**[中文詳解]**
**Amazon CloudFront** 是全球 CDN 服務，透過世界各地的邊緣節點提供網站文件（HTML、圖片、視訊）。訪客請求文件時，CloudFront 自動從最近的邊緣節點提供，比從遠端資料中心更快。

**[混淆選項澄清 / Distractor Clarification]**
- S3 Transfer Acceleration → 加快上傳到 S3 的速度（不是提升靜態網站全球效能）
- AWS WAF → 安全防護（不是效能）
- CloudFormation → 基礎設施佈建（不是效能）

---

## 問題 56 / Question 56

**[題目 / Question]**
According to the AWS Shared Responsibility Model, which are the responsibilities of the **customer**? (Select two)
根據 AWS 共同責任模型，以下哪兩項是**客戶**的責任？

**✅ 正確答案 / Correct Answers：**
1. Operating system patches and updates of an Amazon EC2 instance（EC2 的 OS 修補和更新）
2. Managing IAM users and roles（管理 IAM 使用者和角色）

**[共同責任快速記憶 / Shared Responsibility Quick Reference]**

| 責任 / Responsibility | AWS | 客戶 |
|---|---|---|
| EC2 Guest OS 修補 | ❌ | ✅ |
| IAM 使用者和角色管理 | ❌ | ✅ |
| AWS 全球網路安全 | ✅ | ❌ |
| 確保 AWS 員工無法存取客戶資料 | ✅ | ❌ |
| 雲端基礎設施合規驗證 | ✅ | ❌ |

---

## 問題 57 / Question 57

**[題目 / Question]**
Which Cloud Computing model does the **'Gmail'** service represent?
**'Gmail'** 服務代表哪種雲端運算模型？

**✅ 正確答案 / Correct Answer：Software as a Service (SaaS)（軟體即服務）**

**[雲端服務模型範例 / Cloud Service Model Examples]**

| 模型 / Model | 說明 / Description | 範例 / Examples |
|---|---|---|
| **SaaS** | **完整產品，提供者運行管理** | **Gmail、Dropbox、Zoom、Amazon Rekognition** |
| PaaS | 平台，無需管理底層 OS | Elastic Beanstalk、Heroku |
| IaaS | 基礎設施，最高控制權 | Amazon EC2、GCP、Azure |
| **FaaS** | **函數，無需管理伺服器** | **AWS Lambda** |

> ⚠️ FaaS 是 SaaS 的子集，AWS Lambda 通常被歸類為 FaaS

---

## 問題 58 / Question 58

**[題目 / Question]**
Under the AWS Shared Responsibility Model, which security service falls under **AWS's purview**?
在 AWS 共同責任模型下，哪個安全服務屬於 **AWS 的管轄範圍**？

**✅ 正確答案 / Correct Answer：AWS Shield Standard**

**[中文詳解]**
**AWS Shield Standard** 對所有 AWS 客戶自動啟用，無需任何配置選項，因此 AWS 需要管理其維護和配置，屬於 AWS 的責任。

**[安全服務責任劃分 / Security Service Responsibility]**

| 服務 / Service | 責任方 / Responsible |
|---|---|
| **AWS Shield Standard** | **AWS（自動啟用，客戶無法配置）** |
| AWS Shield Advanced | 客戶（需訂閱並付費）|
| AWS WAF | 客戶（需配置 ACL 規則）|
| Security Group | 客戶（需配置入站/出站規則）|

---

## 問題 59 / Question 59

**[題目 / Question]**
Which statements are correct regarding the **AWS Shared Responsibility Model**? (Select two)
以下哪兩個關於 **AWS 共同責任模型**的說法正確？

**✅ 正確答案 / Correct Answers：**
1. For abstracted services like Amazon S3, **AWS operates the infrastructure layer, OS, and platforms**
2. **AWS is responsible for Security 'of' the Cloud**

**[共同責任模型核心原則 / Core Principles]**
- **AWS 負責**：雲端安全（Security "OF" the Cloud）— 硬體、軟體、網路、設施
- **客戶負責**：雲端中的安全（Security "IN" the Cloud）— 資料、IAM、應用程式配置

**[共同責任 / Shared Responsibilities]**
- 配置管理：AWS 管基礎設施設備；客戶管自己的 OS、資料庫、應用程式
- 意識和培訓：AWS 訓練 AWS 員工；客戶訓練自己的員工

---

## 問題 60 / Question 60

**[題目 / Question]**
A company wants to identify all **under-utilized EC2 instances** without manual configurations. Which AWS services can be used? (Select two)
公司想在無需手動配置的情況下識別所有**低使用率 EC2 執行個體**，哪兩個服務可用？

**✅ 正確答案 / Correct Answers：**
1. AWS Trusted Advisor
2. AWS Cost Explorer（右尺寸建議功能）

**[識別低使用率 EC2 的工具 / Tools for Under-utilized EC2]**

| 工具 / Tool | 功能 / Function | 需手動配置 |
|---|---|---|
| **AWS Trusted Advisor** | 自動檢查 14 天內 CPU ≤10% 且 網路 I/O ≤5MB 的執行個體 | ❌ 無需 |
| **AWS Cost Explorer** | 右尺寸建議，識別低使用率 EC2 | ❌ 無需 |
| Amazon CloudWatch | 需手動設定告警閾值 | ✅ 需要 |
| AWS Budgets | 需手動設定覆蓋目標 | ✅ 需要 |
| AWS CUR | 費用報告，不識別低使用率 | N/A |

---

## 問題 61 / Question 61

**[題目 / Question]**
A medical device company needs **durable, cost-effective storage** for historic data that must be stored for **10 years** to meet compliance. Which solution?
醫療設備公司需要為符合合規要求需儲存 **10 年**的歷史資料提供**耐久、低成本**儲存，哪個方案？

**✅ 正確答案 / Correct Answer：Amazon S3 Glacier Deep Archive**

**[長期存檔選擇指南 / Long-term Archive Guide]**

| 需求 / Requirement | 推薦 / Recommended |
|---|---|
| 存檔，偶爾快速取回 | S3 Glacier Flexible Retrieval |
| **7-10 年以上合規存檔** | **S3 Glacier Deep Archive ✅（最低成本）** |
| 混合雲儲存 | AWS Storage Gateway（非存檔）|
| 共享文件儲存 | EFS（非存檔）|

> **S3 Glacier Deep Archive** 是 AWS 成本最低的儲存類別，專為高度監管行業（金融、醫療、公共部門）設計

---

## 問題 62 / Question 62

**[題目 / Question]**
Which statements are true about **Cost Allocation Tags** in AWS Billing? (Select two)
以下哪兩個關於 AWS 計費中**成本分配標籤**的說法正確？

**✅ 正確答案 / Correct Answers：**
1. For each resource, **each tag key must be unique**, and each tag key can have **only one value**
2. You must **activate both AWS generated tags and user-defined tags separately** before they appear in Cost Explorer

**[成本分配標籤規則 / Cost Allocation Tag Rules]**

| 規則 / Rule | 說明 |
|---|---|
| 每個資源的每個標籤鍵必須唯一 | ✅ 一個鍵只能有一個值 |
| **兩種類型需分別啟用** | **AWS 生成標籤 + 用戶定義標籤** |
| 標籤是強制性的 | ❌ 標籤是可選的 |
| 只需啟用用戶定義標籤 | ❌ 兩種都需要分別啟用 |

**[標籤類型 / Tag Types]**
- **AWS 生成標籤**：AWS 定義、建立和套用（如 aws:createdBy）
- **用戶定義標籤**：您定義、建立和套用（如 Environment:Production）

---

## 問題 63 / Question 63

**[題目 / Question]**
AWS Trusted Advisor analyzes your AWS environment and provides best practice recommendations for which categories? (Select two)
AWS Trusted Advisor 為哪兩個類別提供最佳實踐建議？

**✅ 正確答案 / Correct Answers：**
1. Cost Optimization（成本優化）
2. Service Limits（服務限制）

**[Trusted Advisor 五大類別 / Five Categories — Must Memorize!]**

| 類別 / Category | 說明 |
|---|---|
| 💰 **Cost Optimization** | 識別閒置資源、降低費用 |
| ⚡ **Performance** | 提升服務速度和響應性 |
| 🔒 **Security** | 加強安全設定 |
| 🔧 **Fault Tolerance** | 提高可用性和冗餘 |
| 📊 **Service Limits** | 識別接近限制的服務使用量 |

> ⚠️ Elasticity、Documentation、Change Management 均為**虛構選項**

---

## 問題 64 / Question 64

**[題目 / Question]**
A company needs to move **large volumes of on-premises data** to AWS from a **remote location with limited bandwidth**. Which service?
公司需要從**帶寬有限的遠端位置**將**大量本地資料**遷移到 AWS，哪個服務？

**✅ 正確答案 / Correct Answer：AWS Snowball**

**[中文詳解]**
**AWS Snowball** 是 AWS Snow Family 的資料遷移和邊緣運算設備，可克服帶寬有限的挑戰，在約一週內遷移 TB 級資料。適合：資料庫、備份、存檔、醫療記錄、分析資料集、IoT 感測器資料和媒體內容。

**[帶寬限制時的遷移選擇 / Migration with Limited Bandwidth]**

| 方案 / Solution | 帶寬依賴 | 適合場景 |
|---|---|---|
| **AWS Snowball** | **❌（實體運輸）** | **大量資料 + 帶寬受限** |
| AWS Direct Connect | 需要設施（1+ 個月）| 持續高頻寬連接 |
| AWS VPN | 需要帶寬 | 一般連接 |
| AWS Transit Gateway | 網路連接服務 | VPC 互連 |

---

## 問題 65 / Question 65

**[題目 / Question]**
Amazon CloudWatch **billing metric data** is stored in which AWS Region?
Amazon CloudWatch **計費指標資料**儲存在哪個 AWS Region？

**✅ 正確答案 / Correct Answer：US East (N. Virginia) - us-east-1**

**[中文詳解]**
計費指標資料儲存在**美國東部（維吉尼亞北部）區域 (us-east-1)**，代表**全球費用**。此資料包括您使用的每個 AWS 服務的估算費用，以及 AWS 費用的估計總計。

> ⚠️ 不論 AWS 資源在哪個 Region 佈建，也不論 AWS 帳戶在哪個 Region 建立，計費指標**一律**儲存在 **us-east-1**

---

## 📊 考題領域統計 / Domain Summary

| 領域 / Domain | 題數 / Questions | 百分比 / % |
|---|---|---|
| Technology（技術）| 24 | 36.9% |
| Security and Compliance（安全與合規）| 20 | 30.8% |
| Cloud Concepts（雲端概念）| 11 | 16.9% |
| Billing and Pricing（計費與定價）| 10 | 15.4% |

---

## 🎯 本回必考重點整理 / Key Exam Points (Set 3)

### Auto Scaling 術語（高頻考點）
- **Scale Out** → 增加執行個體數量（水平）
- **Scale In** → 減少執行個體數量（水平）
- **Scale Up** → 升級執行個體規格（垂直，Auto Scaling 不做）
- **Scale Down** → 降級執行個體規格（垂直，Auto Scaling 不做）

### IAM 策略必要元素
- **Effect（必要）** + **Action（必要）**
- Sid、Condition → 可選
- Principal、Resource → 部分情況必要

### 安全群組 vs 網路 ACL（進階）
- 安全群組：**有狀態、評估所有規則、執行個體層級**
- 網路 ACL：**無狀態、按編號順序、子網路層級**

### S3 複製類型
- **CRR（跨區域複製）** → 不同 Region，合規/DR
- **SRR（同區域複製）** → 同一 Region，日誌聚合

### RDS 三種部署模式
- **Multi-AZ（單備用）** → 高可用性，自動容錯移轉
- **Read Replica（讀取副本）** → 可擴展性，讀取效能
- **Multi-Region** → 區域容災保護

### Lambda 定價
- **請求次數 + 執行時間** → 與語言/代碼行數/部署大小無關

### CloudWatch 計費資料
- **永遠**儲存在 **us-east-1（美國東部維吉尼亞北部）**

### AWS 預設加密服務
- **S3** → 預設 SSE-S3 加密
- **AWS Storage Gateway** → 傳輸時 SSL 加密
- **CloudTrail Logs** → 預設 SSE-S3 加密
- EBS、EFS、Redshift → **需手動啟用**

### 常混淆服務釐清
- **Amazon Kendra** → 智能企業搜索（文件搜索）
- **Amazon Comprehend** → NLP（理解文字）
- **Amazon Lex** → 對話介面（聊天機器人）
- **Amazon Personalize** → 個人化推薦
- **Amazon Rekognition** → 圖像/視訊分析
