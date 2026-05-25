# AWS Cloud Practitioner 考題中英對照詳解（第五回）
# AWS Cloud Practitioner Exam Q&A — Bilingual Study Guide (Set 5)

---

## 問題 1 / Question 1

**[題目 / Question]**
Which security control tool can be used to **deny traffic from a specific IP address**?
哪個安全控制工具可用於**拒絕來自特定 IP 地址的流量**？

**✅ 正確答案 / Correct Answer：Network Access Control List (Network ACL)**

**[中文詳解]**
**Network ACL（網路存取控制清單）** 是 VPC 的可選安全層，作為控制一個或多個子網路流量進出的防火牆，在**子網路層級**運作。每條規則可以**允許或拒絕**流量，具有獨立的入站和出站規則。

**[Security Group vs Network ACL — 關鍵差異 / Key Difference]**

| 特性 / Feature | Security Group | Network ACL |
|---|---|---|
| 作用層級 / Level | 執行個體 / Instance | **子網路 / Subnet** |
| 規則類型 | **僅允許 / Allow only** | **允許 + 拒絕 / Allow & Deny** |
| 狀態 / Stateful | ✅ 有狀態 | ❌ 無狀態 |
| 拒絕特定 IP | ❌ 不能 | **✅ 可以** |

> **考試重點**：需要**拒絕**特定 IP → 用 **Network ACL**；Security Group 只能允許

---

## 問題 2 / Question 2

**[題目 / Question]**
Which of the following statements is an **AWS best practice** when architecting for the Cloud?
以下哪個是雲端架構設計的 **AWS 最佳實踐**？

**✅ 正確答案 / Correct Answer：Automation（自動化）**

**[AWS 雲端架構最佳實踐 / AWS Cloud Architecture Best Practices]**

| 最佳實踐 / Best Practice | 錯誤說法 / Wrong Statement |
|---|---|
| **Automation（自動化）** | ✅ 正確 |
| **Services, not Servers** | ❌ 題目說「Servers, not services」 |
| **Loose coupling（鬆散耦合）** | ❌ 題目說「Close coupling（緊密耦合）」 |
| **Security comes first** | ❌ 題目說「Security comes last」 |

> AWS 推薦的自動化服務：Elastic Beanstalk、Auto Scaling、AWS Lambda 等

---

## 問題 3 / Question 3

**[題目 / Question]**
Which AWS Support plan is the MOST cost-effective when getting **enhanced technical support by Cloud Support Engineers**?
哪個 AWS 支援方案在獲得 **Cloud Support Engineers 增強技術支援**方面最具成本效益？

**✅ 正確答案 / Correct Answer：AWS Business Support**

**[支援級別與 Support 工程師類型 / Support Engineers by Plan]**

| 方案 / Plan | 支援工程師類型 | 費用 |
|---|---|---|
| Basic | 無 | 免費 |
| Developer | **Cloud Support Associates** | 最低 |
| **Business** | **Cloud Support Engineers** | **最具成本效益** ✅ |
| Enterprise | Cloud Support Engineers（24/7）| 最貴 |

---

## 問題 4 / Question 4

**[題目 / Question]**
Which criteria are used to calculate the charge for **Amazon EBS Volumes**? (Select two)
哪兩個標準用於計算 **Amazon EBS 磁碟區**的費用？

**✅ 正確答案 / Correct Answers：**
1. Volume type（磁碟區類型）
2. Provisioned IOPS（佈建的 IOPS）

**[Amazon EBS 定價組成 / EBS Pricing Components]**

| 計費項目 / Charged | 不計費 / Not Charged |
|---|---|
| ✅ **磁碟區類型 / Volume type** | ❌ 資料傳入 / Data transfer IN（永遠免費）|
| ✅ **佈建的 IOPS / Provisioned IOPS** | ❌ 附加的 EC2 執行個體類型 |
| ✅ 每月佈建的 GB 儲存量 | ❌ 儲存的資料類型 |
| ✅ 快照消耗的儲存 | |
| ✅ 出站資料傳輸 | |

---

## 問題 5 / Question 5

**[題目 / Question]**
Which AWS service can be used to **generate, use, and manage encryption keys** on the AWS Cloud?
哪個 AWS 服務可用於在 AWS 雲端**生成、使用和管理加密金鑰**？

**✅ 正確答案 / Correct Answer：AWS CloudHSM**

**[加密金鑰管理服務比較 / Encryption Key Services]**

| 服務 / Service | 功能 / Function |
|---|---|
| **AWS CloudHSM** | **生成、儲存和管理加密金鑰（專用硬體 HSM）** |
| AWS KMS | 建立和控制加密金鑰，整合多個 AWS 服務 |
| AWS Secrets Manager | 保護應用程式密鑰（密碼、API 金鑰），整合 CloudHSM |
| Amazon Inspector | 安全評估，非金鑰管理 |
| Amazon GuardDuty | 威脅偵測，非金鑰管理 |

> **CloudHSM 特點**：您的金鑰**只有您可以存取**，使用 FIPS 140-2 Level 3 驗證的 HSM

---

## 問題 6 / Question 6

**[題目 / Question]**
A company needs a **secure online data transfer tool** that can **automate ongoing transfers from on-premises** while providing support for **incremental data backups**.
公司需要一個**安全的線上資料傳輸工具**，可以**自動化本地到 AWS 的持續傳輸**，並支援**增量資料備份**。

**✅ 正確答案 / Correct Answer：AWS DataSync**

**[中文詳解]**
**AWS DataSync** 是安全的線上資料傳輸服務，可簡化、自動化和加速將 TB 級資料複製到 AWS 儲存服務。支援 NFS、SMB、S3、EFS、FSx 等。適合持續傳輸和增量備份，使用 AWS 設計的傳輸協議進行網路優化（包括增量傳輸、在線壓縮、稀疏文件偵測）。

**[資料遷移服務比較 / Data Migration Services]**

| 服務 / Service | 線上/離線 | 持續傳輸 | 增量備份 | 適用場景 |
|---|---|---|---|---|
| **AWS DataSync** | **線上** | **✅** | **✅** | **自動化持續線上傳輸** |
| AWS Snowball | 離線（實體）| ❌ | ❌ | 大量資料，帶寬受限 |
| AWS Snowball Edge | 離線（實體）| ❌ | ❌ | 邊緣運算 + 離線傳輸 |
| AWS Storage Gateway | 混合雲 | ✅ | ✅ | 本地應用整合雲端儲存 |

---

## 問題 7 / Question 7

**[題目 / Question]**
Which of the following are recommendations in the **Operational Excellence pillar** of AWS Well-Architected Framework? (Select two)
以下哪兩個是 AWS Well-Architected Framework **卓越運營支柱**的建議？

**✅ 正確答案 / Correct Answers：**
1. Anticipate failure（預見失敗）
2. Make frequent, small, reversible changes（進行頻繁、小規模、可逆的變更）

**[六大支柱設計原則對照 / Six Pillars Design Principles]**

| 原則 / Principle | 所屬支柱 / Pillar |
|---|---|
| **Anticipate failure（預見失敗）** | **Operational Excellence（卓越運營）** |
| **Make frequent, small, reversible changes** | **Operational Excellence（卓越運營）** |
| Enable traceability（啟用可追溯性）| Security（安全）|
| Automatically recover from failure | Reliability（可靠性）|
| Use serverless architectures | Performance Efficiency（效能效率）|

---

## 問題 8 / Question 8

**[題目 / Question]**
A company needs to set up an AWS managed VPN between its on-premises network and AWS. Which item needs to be set up **on the company's side**?
公司需要在本地網路和 AWS 之間建立 VPN，**公司側**需要設定什麼？

**✅ 正確答案 / Correct Answer：A customer gateway（客戶閘道）**

**[Site-to-Site VPN 兩端組件 / VPN Components on Each Side]**

| 端 / Side | 組件 / Component | 說明 |
|---|---|---|
| **公司側（您的側）/ Customer side** | **Customer Gateway** | **您的 VPN 設備或軟體設備** |
| AWS 側 / AWS side | Virtual Private Gateway (VGW) | AWS 側的 VPN 集中器 |

---

## 問題 9 / Question 9

**[題目 / Question]**
A company needs to keep sensitive data in its own data center due to **compliance** but wants to deploy AWS resources. Which Cloud deployment model does this refer to?
公司因**合規**需要將敏感資料保留在自己的資料中心，但仍想部署 AWS 資源，這是哪種雲端部署模型？

**✅ 正確答案 / Correct Answer：Hybrid Cloud（混合雲）**

**[雲端部署模型 / Cloud Deployment Models]**

| 模型 / Model | 定義 / Definition | 特徵 |
|---|---|---|
| **Hybrid Cloud（混合雲）** | **本地資料中心 + 雲端** | 合規要求保留本地，同時使用雲端 |
| Public Cloud（公有雲）| 完全在雲端中運行 | 所有資源在雲端 |
| Private Cloud（私有雲）| 完全在本地 | 自己的基礎設施 |
| On-premises（本地）| 本地部署 | 非雲端部署模型 |

---

## 問題 10 / Question 10

**[題目 / Question]**
Which of the following options is **NOT** a feature of Amazon Inspector?
以下哪個**不是** Amazon Inspector 的功能？

**✅ 正確答案 / Correct Answer：Track configuration changes（追蹤配置變更）**

**[中文詳解]**
**追蹤配置變更**是 **AWS Config** 的功能，不是 Amazon Inspector。

**[Amazon Inspector 真正的功能 / Amazon Inspector Real Features]**
- ✅ 自動化安全評估（Automate security assessments）
- ✅ 分析網路可達性（Analyze against unintended network accessibility）
- ✅ 針對已知漏洞檢查 OS（Inspect OS against known vulnerabilities）

> **記憶法**：追蹤配置 → Config；評估漏洞 → Inspector

---

## 問題 11 / Question 11

**[題目 / Question]**
What is the **primary use case** for Amazon GuardDuty?
Amazon GuardDuty 的**主要使用案例**是什麼？

**✅ 正確答案 / Correct Answer：Detecting malicious activity and threats in your AWS accounts and workloads（偵測 AWS 帳戶和工作負載中的惡意活動和威脅）**

**[安全服務使用案例分類 / Security Services by Use Case]**

| 服務 / Service | 主要使用案例 |
|---|---|
| **Amazon GuardDuty** | **威脅偵測（分析 CloudTrail、VPC Flow Logs、DNS 日誌）** |
| AWS WAF | 保護 Web 應用程式（SQL 注入、XSS）|
| AWS Network Firewall | 網路流量過濾，VPC 之間安全通信 |
| AWS KMS / ACM | 加密資料、管理 TLS 憑證 |

---

## 問題 12 / Question 12

**[題目 / Question]**
Which billing timeframe is applied when running a **Windows EC2 on-demand instance**?
執行 **Windows EC2 隨需執行個體**時適用哪種計費時間範圍？

**✅ 正確答案 / Correct Answer：Pay per second（按秒計費）**

**[EC2 計費說明 / EC2 Billing Notes]**
- **Windows EC2 按秒計費**（過去是按小時，現在已改為按秒）
- 最少計費時間：**1 分鐘（60 秒）**
- 可用選項：按秒 ✅ / 按小時 ❌ / 按分鐘 ❌ / 按天 ❌

---

## 問題 13 / Question 13

**[題目 / Question]**
Which AWS service can **send, store, and receive messages** between software components at any volume to **decouple application tiers**?
哪個 AWS 服務可在任何數量下**傳送、儲存和接收訊息**以**解耦應用程式層級**？

**✅ 正確答案 / Correct Answer：Amazon Simple Queue Service (Amazon SQS)**

**[SQS vs SNS 解耦比較 / SQS vs SNS for Decoupling]**

| 特性 / Feature | Amazon SQS | Amazon SNS |
|---|---|---|
| 模式 / Pattern | 訊息佇列 / Message Queue | 發布/訂閱 / Pub-Sub |
| **傳送、儲存、接收訊息** | **✅** | ❌（推送，不儲存）|
| 解耦應用程式層 | ✅ | ✅ |
| 接收者 | 單一消費者（或競爭消費者）| 多個訂閱者 |

---

## 問題 14 / Question 14

**[題目 / Question]**
Which of the following should be included in the **Total Cost of Ownership (TCO) estimate** when moving to AWS? (Select two)
遷移到 AWS 時，**TCO 估算**應包含哪兩個項目？

**✅ 正確答案 / Correct Answers：**
1. Server administration（伺服器管理）
2. Power/Cooling（電力/冷卻）

**[TCO 估算組成 / TCO Estimate Components]**

| 包含在 TCO / Included | 不包含在 TCO / Not Included |
|---|---|
| ✅ **伺服器管理（IT 人力）** | ❌ 應用程式廣告 |
| ✅ **電力/冷卻（伺服器、儲存、網路成本）** | ❌ 終端使用者數量 |
| ✅ 伺服器硬體 | ❌ 辦公室電子設備 |
| ✅ 儲存和網路 | |

> **AWS Pricing Calculator** 比較本地 vs AWS：伺服器、儲存、網路、IT 人力

---

## 問題 15 / Question 15

**[題目 / Question]**
Which AWS service allows you to quickly add **user sign-up, sign-in, and access control** to web and mobile applications?
哪個 AWS 服務讓您快速為 Web 和行動應用程式添加**使用者註冊、登入和存取控制**？

**✅ 正確答案 / Correct Answer：Amazon Cognito**

**[身份認證服務比較 / Identity Services Comparison]**

| 服務 / Service | 適用場景 / Use Case |
|---|---|
| **Amazon Cognito** | **Web/行動應用程式的使用者池和身份認證（B2C）** |
| AWS IAM | AWS 服務和資源的存取控制（AWS 用戶）|
| AWS IAM Identity Center | 多個 AWS 帳戶的員工 SSO（B2B/企業）|
| AWS Organizations | 多帳戶管理 |

---

## 問題 16 / Question 16

**[題目 / Question]**
A media company wants to enable **customized content suggestions** for its movie streaming platform. Which AWS service?
媒體公司想為其電影串流平台啟用**個人化內容推薦**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：Amazon Personalize**

**[中文詳解]**
**Amazon Personalize** 讓開發者能夠建立使用與 Amazon.com 相同 ML 技術的應用程式，提供即時個人化推薦。適用場景包括：電商產品推薦、媒體和社群網路新聞文章/內容推薦、旅遊網站酒店推薦等。

**[推薦引擎相關服務 / Recommendation Services]**

| 服務 / Service | 功能 |
|---|---|
| **Amazon Personalize** | **即時個人化推薦（使用歷史資料）** |
| Amazon Comprehend | 自然語言處理 (NLP)，文字分析 |
| Amazon SageMaker | 建立、訓練和部署 ML 模型（通用）|
| Amazon Customize | ❌ 虛構選項（干擾項）|

---

## 問題 17 / Question 17

**[題目 / Question]**
Where are **Amazon EBS snapshots** stored in the AWS Cloud?
**Amazon EBS 快照**在 AWS 雲端中儲存在哪裡？

**✅ 正確答案 / Correct Answer：Amazon Simple Storage Service (Amazon S3)**

**[中文詳解]**
**Amazon EBS 快照**是 EBS 磁碟區的時間點副本，備份到 **Amazon S3**。快照是增量的——新快照只保存自上次快照以來更改的區塊。可使用 EBS 快照跨不同可用區域複製資料（因為 S3 是區域範圍服務）。

---

## 問題 18 / Question 18

**[題目 / Question]**
A growing start-up has trouble **identifying and protecting sensitive data at scale**. Which AWS service can assist?
新創公司難以大規模**識別和保護敏感資料**，哪個 AWS 服務可協助？

**✅ 正確答案 / Correct Answer：Amazon Macie**

**[中文詳解]**
**Amazon Macie** 是全托管資料安全和隱私服務，使用機器學習和模式匹配大規模發現和保護 AWS 中的敏感資料。自動偵測 PII（個人識別資訊）如姓名、地址、信用卡號。提供 S3 資料安全和隱私的持續可見性。

---

## 問題 19 / Question 19

**[題目 / Question]**
A company wants to implement **Chaos Engineering** to expose blind spots that can disrupt application resiliency. Which AWS service?
公司想實施**混沌工程**來暴露可能破壞應用程式彈性的盲點，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Fault Injection Simulator (AWS FIS)**

**[中文詳解]**
**AWS Fault Injection Simulator (AWS FIS)** 是全托管服務，用於在 AWS 上執行錯誤注入實驗（混沌工程）。可通過建立破壞性事件（如 CPU 或記憶體消耗突增）來壓力測試應用程式，觀察系統如何響應，並實施改進。

**[混沌工程核心概念 / Chaos Engineering Core Concept]**
```
設定實驗（使用預建模板）
→ 注入錯誤（CPU、記憶體、網路延遲等）
→ 觀察系統響應
→ 自動回滾（如達到停止條件）
→ 識別隱藏弱點並改進
```

---

## 問題 20 / Question 20

**[題目 / Question]**
Which AWS **serverless** service allows you to **prepare data for analytics**?
哪個 AWS **無伺服器**服務讓您**為分析準備資料**？

**✅ 正確答案 / Correct Answer：AWS Glue**

**[數據分析管道服務比較 / Data Analytics Pipeline Services]**

| 服務 / Service | 功能 / Function | 無伺服器 |
|---|---|---|
| **AWS Glue** | **ETL 服務（提取、轉換、載入）— 準備資料** | **✅** |
| Amazon Athena | SQL 查詢 S3 資料（分析）| ✅ |
| Amazon Redshift | 資料倉儲（分析）| ❌ |
| Amazon EMR | Hadoop 大數據處理（分析）| ❌ |

> **記憶法**：ETL（準備資料）→ Glue；查詢 S3 → Athena；資料倉儲 → Redshift

---

## 問題 21 / Question 21

**[題目 / Question]**
An e-commerce company would like to build a **chatbot** using Natural Language Understanding (NLU). Which AWS service?
電商公司想使用 NLU 建立**聊天機器人**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：Amazon Lex**

**[對話式 AI 服務 / Conversational AI Services]**

| 服務 / Service | 功能 / Function |
|---|---|
| **Amazon Lex** | **建立對話介面（語音 + 文字聊天機器人）** |
| Amazon Polly | 文字 → 語音（TTS）|
| Amazon Transcribe | 語音 → 文字（ASR）|
| Amazon Comprehend | NLP（理解文字含義）|
| Amazon Rekognition | 圖像/視訊分析 |

> **Amazon Lex** 由 Amazon Alexa 相同的對話引擎驅動

---

## 問題 22 / Question 22

**[題目 / Question]**
Which services are provided by **Amazon Route 53**? (Select two)
**Amazon Route 53** 提供哪兩個服務？

**✅ 正確答案 / Correct Answers：**
1. Domain registration（域名注冊）
2. Health checks and monitoring（健康檢查和監控）

**[Amazon Route 53 功能 / Route 53 Features]**

| Route 53 功能 | Route 53 不提供（由其他服務提供）|
|---|---|
| ✅ **域名注冊** | ❌ 負載均衡（那是 ELB）|
| ✅ **健康檢查和監控** | ❌ IP 路由（儘管名字叫 Route 53）|
| ✅ DNS 解析 | ❌ 傳輸加速（那是 S3 Transfer Acceleration）|
| ✅ 路由策略（加權、延遲等）| |

---

## 問題 23 / Question 23

**[題目 / Question]**
A company would like to **reserve EC2 capacity for 3 years** and plans to **increase workloads**. Which EC2 Reserved Instance (RI) type?
公司想**保留 3 年 EC2 容量**並計劃**增加工作負載**，哪種 EC2 Reserved Instance 類型？

**✅ 正確答案 / Correct Answer：Convertible reserved instance (RI)（可轉換預留執行個體）**

**[RI 類型比較 / Reserved Instance Types]**

| 類型 / Type | 折扣 / Discount | 靈活性 / Flexibility | 適用場景 |
|---|---|---|---|
| **Standard RI** | **最高 72%** | 低（不能更改執行個體家族）| 穩定、不變工作負載 |
| **Convertible RI** | **最高 54%** | **高（可更改執行個體家族、OS、租用）** | **工作負載可能變化** |
| Scheduled RI | N/A | ❌ AWS 不再支援 | 已廢棄 |

> **選 Convertible RI 的關鍵**：工作負載**可能增加或改變**，需要靈活性

---

## 問題 24 / Question 24

**[題目 / Question]**
Which length terms are available for Amazon EC2 reserved instances (RI)? (Select two)
Amazon EC2 保留執行個體的哪兩個期限可供選擇？

**✅ 正確答案 / Correct Answers：**
1. 1 year（1 年）
2. 3 years（3 年）

**[RI 期限選項 / RI Term Options]**
- ✅ 1 年 / 1 year
- ✅ 3 年 / 3 years（折扣更大）
- ❌ 6 個月 / 6 months
- ❌ 2 年 / 2 years
- ❌ 5 年 / 5 years

---

## 問題 25 / Question 25

**[題目 / Question]**
According to the AWS Shared Responsibility Model, which of the following is **both the responsibility of AWS and the customer**? (Select two)
根據 AWS 共同責任模型，以下哪兩個是 **AWS 和客戶的共同責任**？

**✅ 正確答案 / Correct Answers：**
1. Configuration management（配置管理）
2. Operating system (OS) configuration（作業系統配置）

**[共同責任詳解 / Shared Responsibility Detail]**

| 項目 / Item | AWS 負責 | 客戶負責 |
|---|---|---|
| **配置管理** | 基礎設施設備配置 | Guest OS、資料庫、應用程式配置 |
| **OS 配置** | **主機 OS 配置** | **Guest OS 配置** |
| 客戶資料 | ❌ | ✅（完全客戶責任）|
| 資料中心安全 | ✅（完全 AWS 責任）| ❌ |
| 磁碟驅動器處置 | ✅（完全 AWS 責任）| ❌ |

---

## 問題 26 / Question 26

**[題目 / Question]**
Which AWS service can **subscribe to an RSS feed** to be notified of the status of all AWS service interruptions?
哪個 AWS 服務可**訂閱 RSS 提要**以獲得所有 AWS 服務中斷的通知？

**✅ 正確答案 / Correct Answer：AWS Health Dashboard - Service Health（服務健康儀表板）**

**[健康儀表板功能對比 / Health Dashboards Comparison]**

| 儀表板 / Dashboard | 功能 / Feature | RSS 訂閱 |
|---|---|---|
| **Service Health（服務健康）** | **所有 AWS 服務的整體狀態** | **✅ 支援 RSS** |
| Account Health（帳戶健康）| 您的特定帳戶的個人化告警 | ❌ 不是 RSS |

---

## 問題 27 / Question 27

**[題目 / Question]**
A corporation would like to **simplify access management to multiple AWS accounts** and facilitate **AWS Single Sign-On (AWS SSO)**. Which AWS service?
公司想**簡化多個 AWS 帳戶的存取管理**並促進 **AWS SSO**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS IAM Identity Center**

**[中文詳解]**
**AWS IAM Identity Center**（AWS SSO 的後繼者）建立在 IAM 之上，簡化對多個 AWS 帳戶、AWS 應用程式和其他 SAML 啟用的雲端應用程式的存取管理。提供統一的用戶入口網站存取所有分配的 AWS 帳戶或應用程式。

**[身份服務比較 / Identity Services Comparison]**

| 服務 / Service | 適用場景 |
|---|---|
| **AWS IAM Identity Center** | **企業員工多帳戶 SSO（企業用戶）** |
| Amazon Cognito | Web/行動應用程式使用者池（終端客戶）|
| AWS IAM | 單一 AWS 帳戶的存取控制 |

---

## 問題 28 / Question 28

**[題目 / Question]**
Which AWS tool helps you define cloud infrastructure using **popular programming languages** such as Python and JavaScript?
哪個 AWS 工具可以使用 **Python、JavaScript 等流行程式語言**定義雲端基礎設施？

**✅ 正確答案 / Correct Answer：AWS Cloud Development Kit (AWS CDK)**

**[中文詳解]**
**AWS CDK** 是開源軟體開發框架，使用熟悉的程式語言（Python、JavaScript、TypeScript、Java、C#）來定義雲端應用程式資源。使用高階構造元件（constructs）預配置雲端資源。最終轉換成 AWS CloudFormation 模板進行佈建。

**[IaC 工具比較 / IaC Tools Comparison]**

| 工具 / Tool | 語言 / Language | 功能 |
|---|---|---|
| **AWS CDK** | **Python、JS、TS、Java、C#** | **高階程式語言定義 IaC** |
| AWS CloudFormation | YAML / JSON | 資源模板，CDK 的底層 |
| AWS Elastic Beanstalk | 任何（應用程式代碼）| PaaS 部署平台 |
| AWS CodeBuild | N/A | CI 建構服務 |

---

## 問題 29 / Question 29

**[題目 / Question]**
According to the AWS Shared Responsibility Model, which are the **responsibilities of AWS**? (Select two)
根據 AWS 共同責任模型，以下哪兩個是 **AWS 的責任**？

**✅ 正確答案 / Correct Answers：**
1. Network operability（網路可操作性）
2. Data center security（資料中心安全）

**[AWS 責任範圍 / AWS Responsibilities]**
AWS 負責「雲端安全」，包括：
- ✅ 硬體 / Hardware
- ✅ 軟體 / Software
- ✅ **網路可操作性 / Network operability**
- ✅ **資料中心安全 / Data center security**
- ✅ 設施 / Facilities

**[客戶責任 / Customer Responsibilities]**
- ❌ 修補 Guest OS（客戶責任）
- ❌ 加密應用程式資料（客戶責任）
- ❌ 配置 IAM 角色（客戶責任）

---

## 問題 30 / Question 30

**[題目 / Question]**
A company manages 300 microservices and wants to **automate code reviews** to improve code quality. Which tool?
公司管理 300 個微服務，想**自動化代碼審查**以提高代碼品質，哪個工具？

**✅ 正確答案 / Correct Answer：Amazon CodeGuru**

**[中文詳解]**
**Amazon CodeGuru** 是開發者工具，提供智能建議以提高代碼品質和識別應用程式最昂貴的代碼行。包含兩個部分：
- **CodeGuru Reviewer**：使用 ML 識別關鍵問題、安全漏洞和難以發現的 bug
- **CodeGuru Profiler**：找出應用程式最昂貴的代碼行，幫助優化效能

**[開發工具比較 / Developer Tools]**

| 工具 / Tool | 功能 / Function |
|---|---|
| **Amazon CodeGuru** | **自動化代碼審查 + 效能分析** |
| AWS X-Ray | 分析和偵錯分散式應用程式 |
| AWS CodeBuild | 持續整合，編譯和測試代碼 |
| AWS Trusted Advisor | AWS 最佳實踐建議 |

---

## 問題 31 / Question 31

**[題目 / Question]**
A multinational company has moved to AWS and employees travel to different offices around the world. How should they set up AWS accounts?
跨國公司已遷移到 AWS，員工出差到世界各地不同辦公室，應如何設置 AWS 帳戶？

**✅ 正確答案 / Correct Answer：There is nothing to do — AWS IAM is a **global service**（無需任何操作 — AWS IAM 是**全球服務**）**

**[AWS IAM 全球服務特性 / IAM Global Service Characteristics]**
- AWS IAM 是全球服務（非區域性）
- 在 IAM 中建立的使用者可以從世界各地存取帳戶
- 可以在每個 Region 部署資源
- **無需為不同 Region 建立不同的 IAM 使用者**

---

## 問題 32 / Question 32

**[題目 / Question]**
Which AWS service can inspect **Amazon CloudFront distributions** running on any HTTP web server?
哪個 AWS 服務可以檢查在任何 HTTP Web 伺服器上運行的 **Amazon CloudFront 分佈**？

**✅ 正確答案 / Correct Answer：AWS Web Application Firewall (AWS WAF)**

**[中文詳解]**
**AWS WAF** 可監控轉發到 Amazon CloudFront 的 HTTP 和 HTTPS 請求，並控制對內容的存取。在 CloudFront 上使用 WAF 時，規則在所有全球 AWS 邊緣節點運行，封鎖的請求在到達 Web 伺服器之前就被阻止。

---

## 問題 33 / Question 33

**[題目 / Question]**
According to the AWS Well-Architected Framework, which action is recommended in the **Security pillar**?
根據 AWS Well-Architected Framework，**安全支柱**推薦哪個動作？

**✅ 正確答案 / Correct Answer：Use AWS KMS to encrypt data（使用 AWS KMS 加密資料）**

**[Well-Architected 六大支柱 — 關鍵服務對照 / Six Pillars Key Services]**

| 支柱 / Pillar | 推薦服務/動作 |
|---|---|
| **Security（安全）** | **AWS KMS 加密資料、IAM、GuardDuty** |
| Cost Optimization | AWS Cost Explorer、使用預留/Spot |
| Reliability | 多 AZ 部署、Auto Scaling、備份 |
| Performance Efficiency | 選擇正確資源類型、CloudWatch 監控 |
| Operational Excellence | IaC（CloudFormation/CDK）、自動化 |

---

## 問題 34 / Question 34

**[題目 / Question]**
A research lab needs to be **notified in case of a configuration change** for security and compliance reasons. Which AWS service?
研究實驗室需要在出現**配置變更時收到通知**以滿足安全和合規要求，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Config**

**[中文詳解]**
**AWS Config** 持續監控和記錄 AWS 資源配置，並允許自動評估記錄的配置是否符合期望配置。可在資源**建立、修改或刪除**時收到通知，幫助簡化合規審計、安全分析、變更管理和運營故障排除。

---

## 問題 35 / Question 35

**[題目 / Question]**
Which Amazon EC2 Auto Scaling feature can help with **fault tolerance**?
哪個 Amazon EC2 Auto Scaling 功能可協助實現**容錯**？

**✅ 正確答案 / Correct Answer：Replacing unhealthy Amazon EC2 instances（替換不健康的 EC2 執行個體）**

**[Auto Scaling 功能與優勢對應 / Auto Scaling Features & Benefits]**

| Auto Scaling 功能 / Feature | 對應優勢 / Benefit |
|---|---|
| **替換不健康的執行個體** | **容錯 / Fault tolerance** ✅ |
| 按需增加執行個體數量 | 擴展性 / Scalability |
| 調整執行個體數量以降低成本 | 成本優化 / Cost optimization |
| 確保正確的運算容量 | 可用性 / Availability |

> ⚠️ **負載分配**是 ELB 的功能，**不是** Auto Scaling 的功能

---

## 問題 36 / Question 36

**[題目 / Question]**
An engineering team new to AWS Cloud would like to launch a **dev/test environment with low monthly pricing**. Which AWS service?
對 AWS 不熟悉的工程團隊想以**低月費**啟動 dev/test 環境，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：Amazon Lightsail**

**[中文詳解]**
**Amazon Lightsail** 是啟動和管理 VPS（虛擬私有伺服器）最簡單的方式，包含項目包括：虛擬機器、SSD 儲存、資料傳輸、DNS 管理、靜態 IP——全部以低廉可預測的價格提供。非常適合雲端經驗少的人快速啟動。

**[Lightsail vs EC2 / Lightsail vs EC2 Comparison]**

| 特性 / Feature | Amazon Lightsail | Amazon EC2 |
|---|---|---|
| 目標用戶 | 初學者、簡單應用 | 進階用戶、複雜架構 |
| 定價模型 | 固定月費 | 按秒計費（複雜）|
| 需要 VPC 知識 | ❌ 不需要 | ✅ 需要 |
| 彈性 | 較低 | 非常高 |

---

## 問題 37 / Question 37

**[題目 / Question]**
A company wants to define a set of rules to **manage objects cost-effectively between S3 storage classes**. Which S3 feature?
公司想定義規則以**在 S3 儲存類別之間成本最優地管理物件**，哪個 S3 功能？

**✅ 正確答案 / Correct Answer：Amazon S3 Lifecycle configuration（Amazon S3 生命週期配置）**

**[S3 生命週期配置兩種動作 / S3 Lifecycle Actions]**

| 動作類型 / Action | 說明 / Description |
|---|---|
| **Transition actions（轉換動作）** | 物件何時轉移到另一個儲存類別（如 30 天後 → Standard-IA）|
| **Expiration actions（到期動作）** | 物件何時到期並被刪除 |

---

## 問題 38 / Question 38

**[題目 / Question]**
A hybrid cloud company wants to store **secondary backup copies** of on-premises data. Which S3 storage class is cost-optimal yet provides rapid access?
混合雲公司想儲存本地資料的**次要備份副本**，哪個 S3 儲存類別最具成本效益且提供快速存取？

**✅ 正確答案 / Correct Answer：Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)**

**[選擇理由 / Why One Zone-IA]**
- 比 Standard-IA 便宜 **20%**
- 次要備份副本：**可重新創建或從其他地方恢復**，單一 AZ 的較低可用性不是問題
- 仍提供**快速存取**（毫秒）

**[S3 儲存類別備份場景選擇 / S3 for Backup]**

| 備份類型 / Backup Type | 推薦 / Recommended |
|---|---|
| 主要備份（不可重建）| S3 Standard-IA（多 AZ）|
| **次要備份（可重建）** | **S3 One Zone-IA（最便宜）** ✅ |
| 長期存檔 | S3 Glacier Flexible Retrieval |
| 7-10 年合規 | S3 Glacier Deep Archive |

---

## 問題 39 / Question 39

**[題目 / Question]**
Which statement is CORRECT regarding the **scope of an Amazon VPC**?
以下哪個關於 **Amazon VPC 範圍**的說法正確？

**✅ 正確答案 / Correct Answer：A VPC spans **all Availability Zones (AZs) within an AWS region**（VPC 跨越 AWS 區域中的**所有可用區域**）**

**[VPC 和 Subnet 的範圍 / VPC and Subnet Scope]**

| 組件 / Component | 範圍 / Scope |
|---|---|
| **Amazon VPC** | **一個 AWS Region 中的所有 AZ** |
| Subnet | **只有一個 AZ** |

**[常見錯誤說法 / Common Wrong Statements]**
- ❌ VPC 跨所有 AZ 和所有 Region → 錯誤（只在一個 Region 內）
- ❌ VPC 只在一個 AZ → 錯誤（跨所有 AZ）
- ❌ Region 在 AZ 內部 → 邏輯錯誤

---

## 問題 40 / Question 40

**[題目 / Question]**
Which service/tool will you use to create and provide trusted users with **temporary security credentials**?
哪個服務/工具可建立並向受信任的用戶提供**臨時安全憑證**？

**✅ 正確答案 / Correct Answer：AWS Security Token Service (AWS STS)**

**[中文詳解]**
**AWS STS** 可請求 IAM 用戶或聯合用戶的臨時、受限權限憑證。臨時憑證的特點：
- 短期（幾分鐘到幾小時）
- 動態生成，不儲存在用戶處
- 到期後 AWS 不再識別這些憑證

**[身份和憑證服務比較 / Identity & Credentials Services]**

| 服務 / Service | 用途 / Purpose |
|---|---|
| **AWS STS** | **臨時安全憑證（短期）** |
| AWS IAM | 長期憑證（存取金鑰）和權限管理 |
| Amazon Cognito | Web/行動應用程式用戶池（含 STS 支援）|
| AWS IAM Identity Center | 企業員工 SSO |

---

## 問題 41 / Question 41

**[題目 / Question]**
Which of the following statements is **INCORRECT** regarding Amazon EBS Elastic Volumes?
以下哪個關於 Amazon EBS Elastic Volumes 的說法**不正確**？

**✅ 正確答案（不正確的說法）/ Correct Answer (Incorrect Statement)：**
"Amazon EBS Elastic Volumes can be **bound to several Availability Zones (AZs)**"
「Amazon EBS 磁碟區可以綁定到**多個可用區域**」

**[EBS 磁碟區的正確特性 / Correct EBS Volume Characteristics]**
- ✅ EBS 磁碟區在**同一 AZ** 中只能掛載到**一個**執行個體（在 CCP 層面）
- ✅ EBS 磁碟區**綁定到特定 AZ**（磁碟區和執行個體必須在同一 AZ）
- ✅ EBS 磁碟區可以在終止後**持久儲存資料**
- ❌ EBS 磁碟區**不能**綁定到多個 AZ

---

## 問題 42 / Question 42

**[題目 / Question]**
A university's IT infrastructure is experiencing a **read-intensive workload** and wants to take the load off databases. Which AWS service?
大學 IT 基礎設施正在遭受**讀取密集的工作負載**，想減輕資料庫負擔，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：Amazon ElastiCache**

**[中文詳解]**
**Amazon ElastiCache** 是記憶體內快取服務，讓 Web 應用程式能夠從快速的記憶體快取中獲取資訊，而不是完全依賴較慢的磁碟型資料庫。可快取一些值以減輕資料庫負擔，通常與 Amazon RDS 配合使用。

---

## 問題 43 / Question 43

**[題目 / Question]**
A start-up wants to **monitor costs and choose an optimal Savings Plan**. Which AWS service?
新創公司想**監控費用並選擇最優的 Savings Plan**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Cost Explorer**

**[Savings Plan 建議功能 / Savings Plan Recommendations]**
- **AWS Cost Explorer** 提供 Savings Plan 建議，可在成員（連結）帳戶層級或組織層級收到建議

**[成本工具功能對比 / Cost Tools Feature Comparison]**

| 工具 / Tool | Savings Plan 建議 | 功能 |
|---|---|---|
| **AWS Cost Explorer** | **✅** | 視覺化費用 + Savings Plan 建議 |
| AWS CUR | ❌ | 最詳細的費用資料 |
| AWS Pricing Calculator | ❌ | 事前估算 |
| AWS Budgets | ❌ | 預算告警 |

---

## 問題 44 / Question 44

**[題目 / Question]**
Which AWS IAM Security Tool allows you to **review permissions granted to an IAM user**?
哪個 AWS IAM 安全工具讓您**審查授予 IAM 使用者的權限**？

**✅ 正確答案 / Correct Answer：AWS IAM Access Advisor（IAM 存取顧問）**

**[IAM 安全工具比較 / IAM Security Tools]**

| 工具 / Tool | 用途 / Purpose |
|---|---|
| **IAM Access Advisor** | **顯示授予使用者的服務權限及上次使用時間（識別不必要的權限）** |
| IAM Credentials Report | 列出所有帳戶使用者及其憑證狀態（密碼、金鑰、MFA）|
| IAM Policy | 定義操作的權限（不是審查工具）|
| MFA | 多重要素驗證（不是審查工具）|

---

## 問題 45 / Question 45

**[題目 / Question]**
Which AWS tool can provide **best practice recommendations** for performance, service limits, and cost optimization?
哪個 AWS 工具可以為效能、服務限制和成本優化提供**最佳實踐建議**？

**✅ 正確答案 / Correct Answer：AWS Trusted Advisor**

**[Trusted Advisor 五大類別 / Five Categories]**

| 類別 / Category | 說明 |
|---|---|
| 💰 Cost Optimization | 識別閒置資源 |
| ⚡ **Performance** | 提升效能 |
| 🔒 Security | 強化安全 |
| 🔧 Fault Tolerance | 提高容錯 |
| 📊 **Service Limits** | 識別接近限制的服務 |

---

## 問題 46 / Question 46

**[題目 / Question]**
An engineering team would like to **run hundreds of thousands of batch computing workloads** cost-effectively on AWS. Which AWS service?
工程團隊想在 AWS 上以成本效益方式**執行數十萬個批次運算工作負載**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Batch**

**[批次處理服務比較 / Batch Processing Services]**

| 服務 / Service | 批次工作負載 | 規模 | 說明 |
|---|---|---|---|
| **AWS Batch** | **✅ 最佳** | **數十萬個** | **完全管理批次運算，動態佈建最優資源** |
| AWS Lambda | ✅（較小）| 有限 | 有時間和大小限制 |
| AWS Fargate | ✅（可以）| 中等 | 比 Batch 更貴 |
| Amazon Lightsail | ❌ | N/A | VPS 服務，非批次 |

---

## 問題 47 / Question 47

**[題目 / Question]**
Which actions can help **optimize Amazon EC2 costs**? (Select two)
哪兩個動作可以幫助**優化 Amazon EC2 費用**？

**✅ 正確答案 / Correct Answers：**
1. Set up Auto Scaling groups to align the number of instances with the demand（設置 Auto Scaling 群組使執行個體數量與需求一致）
2. Purchase Amazon EC2 Reserved instances (RIs)（購買 EC2 預留執行個體）

**[EC2 成本優化策略 / EC2 Cost Optimization Strategies]**

| 策略 / Strategy | 效果 / Effect |
|---|---|
| ✅ **Auto Scaling** | 按需調整，只為使用的資源付費 |
| ✅ **Reserved Instances** | 最高 72% 折扣（長期穩定工作負載）|
| ❌ 垂直擴展 | 更貴，不是成本優化方式 |
| ❌ 更高支援方案 | 與 EC2 費用無關 |
| ❌ 建立自己的伺服器 | 比 EC2 更貴 |

---

## 問題 48 / Question 48

**[題目 / Question]**
An enterprise wants the **fastest migration path** and has decided **not to update application code or make any architectural changes**. Which migration strategy?
企業想要**最快的遷移路徑**，決定**不更新應用程式代碼或進行任何架構變更**，哪個遷移策略？

**✅ 正確答案 / Correct Answer：Rehost（重新託管 / Lift and Shift）**

**[6R 遷移策略快速對照 / 6R Migration Strategies]**

| 策略 / Strategy | 說明 | 代碼變更 | 速度 |
|---|---|---|---|
| **Rehost（重新託管）** | **直接搬移，不修改（Lift & Shift）** | **❌ 無** | **最快** |
| Replatform | 少量修改（如 MySQL → RDS）| 少量 | 中等 |
| Repurchase | 換用新的 SaaS 產品 | 流程變更 | 中等 |
| Refactor | 重新架構（最多工作）| 大量 | 最慢 |

---

## 問題 49 / Question 49

**[題目 / Question]**
A company based in Sydney wants to deploy the same EC2 instances in eu-south-1. Which AWS entity can address this?
悉尼的公司想在 eu-south-1 部署相同的 EC2 執行個體，哪個 AWS 實體可以解決？

**✅ 正確答案 / Correct Answer：Amazon Machine Image (AMI)**

**[AMI 跨 Region 使用 / AMI Cross-Region Usage]**
- AMI 必須與 EC2 執行個體在**同一個 Region**
- 要跨 Region 使用，需要先**複製 AMI 到目標 Region**
- 可以從單一 AMI 啟動多個相同配置的執行個體

---

## 問題 50 / Question 50

**[題目 / Question]**
Which are the **best practices when using AWS Organizations**? (Select two)
使用 **AWS Organizations** 的哪兩個最佳實踐？

**✅ 正確答案 / Correct Answers：**
1. Restrict account privileges using **Service Control Policies (SCP)**（使用 SCP 限制帳戶權限）
2. Create **AWS accounts per department**（按部門建立 AWS 帳戶）

**[AWS Organizations 最佳實踐 / Organizations Best Practices]**

| 最佳實踐 / Best Practice | 說明 |
|---|---|
| ✅ **按部門建立帳戶** | 更好的資源隔離、服務限制分離 |
| ✅ **使用 SCP 限制權限** | 治理護欄，控制允許的服務和操作 |
| ✅ 使用標籤管理費用 | 標準化標籤用於計費追蹤 |
| ✅ 啟用 CloudTrail | 監控所有帳戶活動 |
| ❌ 停用 CloudTrail | 違反安全最佳實踐 |
| ❌ 不使用 AWS Organizations 自動化帳戶建立 | 違反自動化最佳實踐 |

---

## 問題 51 / Question 51

**[題目 / Question]**
Which are the **advantages of using the AWS Cloud**? (Select two)
使用 **AWS Cloud 的哪兩個優勢**？

**✅ 正確答案 / Correct Answers：**
1. Stop guessing about capacity（停止猜測容量）
2. Increase speed and agility（提高速度和敏捷性）

**[雲端六大優勢 — 常見錯誤選項澄清 / Cloud Advantages — Common Distractors]**

| 說法 / Statement | 正確/錯誤 | 說明 |
|---|---|---|
| ✅ Stop guessing about capacity | 正確 | 雲端六大優勢之一 |
| ✅ Increase speed and agility | 正確 | 雲端六大優勢之一 |
| ❌ Limited scaling（有限擴展）| 錯誤 | 雲端擴展是無限的 |
| ❌ AWS is responsible for security IN the cloud | 錯誤 | AWS 負責「雲端安全（OF）」，客戶負責「雲端中的安全（IN）」|
| ❌ Trade operational for capital expense | 錯誤 | 應該是「Trade **capital** for **operational** expense（資本換可變）」|

---

## 問題 52 / Question 52

**[題目 / Question]**
Which are the **benefits of using AWS Elastic Load Balancing (ELB)**? (Select two)
使用 **AWS Elastic Load Balancing (ELB) 的哪兩個優勢**？

**✅ 正確答案 / Correct Answers：**
1. Fault tolerance（容錯）
2. High availability（高可用性）

**[ELB 提供 vs 不提供的優勢 / ELB Provides vs Not Provides]**

| ELB 提供 / ELB Provides | ELB 不提供 / Not Provides |
|---|---|
| ✅ **高可用性 / High availability** | ❌ 敏捷性（那是雲端的特性）|
| ✅ **容錯 / Fault tolerance** | ❌ 成本降低（ELB 本身有費用）|
| ✅ 自動擴展 / Auto scaling | ❌ 儲存 |
| ✅ 強大安全性 / Robust security | |

---

## 問題 53 / Question 53

**[題目 / Question]**
A company wants to create a **private, high bandwidth network connection** between its on-premises data centers and AWS Cloud. Which option?
公司想在本地資料中心和 AWS 雲端之間建立**私密、高帶寬的網路連接**，哪個選項？

**✅ 正確答案 / Correct Answer：AWS Direct Connect**

**[連接選項比較 / Connectivity Options]**

| 方案 / Solution | 私密 | 帶寬 | 不走公網 | 建立時間 |
|---|---|---|---|---|
| **AWS Direct Connect** | **✅** | **高** | **✅** | **1+ 個月** |
| AWS Site-to-Site VPN | ✅（加密）| 中 | ❌（走公網）| 分鐘 |
| VPC Endpoints | ✅ | 中 | ✅ | 即時 |
| VPC Peering | ✅ | 中 | ✅ | 即時 |

---

## 問題 54 / Question 54

**[題目 / Question]**
A Cloud Practitioner wants to deploy identical resources **across all AWS regions and accounts** using templates and **estimate costs**. Which AWS service?
Cloud Practitioner 想使用模板跨**所有 AWS 區域和帳戶**部署相同資源並**估算費用**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS CloudFormation**

**[CloudFormation 主要功能 / CloudFormation Key Features]**
- ✅ 跨多個帳戶和 Region 佈建（StackSets）
- ✅ 使用模板估算費用（Cost Estimation）
- ✅ 基礎設施即代碼（IaC）
- ✅ 自動回滾

---

## 問題 55 / Question 55

**[題目 / Question]**
According to the AWS Shared Responsibility Model, which is the **responsibility of the customer**?
根據 AWS 共同責任模型，哪項是**客戶的責任**？

**✅ 正確答案 / Correct Answer：Firewall & networking configuration of Amazon EC2（EC2 的防火牆和網路配置）**

**[共同責任 — EC2 / Shared Responsibility for EC2]**

| 責任項目 / Responsibility | AWS | 客戶 |
|---|---|---|
| **EC2 防火牆和網路配置（安全群組）** | ❌ | **✅** |
| 保護硬體基礎設施 | ✅ | ❌ |
| 邊緣節點安全 | ✅ | ❌ |
| 管理 Amazon DynamoDB（全托管服務）| ✅ | ❌ |

---

## 問題 56 / Question 56

**[題目 / Question]**
Which types of monitoring can be provided by Amazon CloudWatch? (Select two)
Amazon CloudWatch 可以提供哪兩種類型的監控？

**✅ 正確答案 / Correct Answers：**
1. Application performance（應用程式效能）
2. Resource utilization（資源使用率）

**[CloudWatch 監控範圍 / CloudWatch Monitoring Scope]**

| CloudWatch 監控 / Monitors | 非 CloudWatch 功能 |
|---|---|
| ✅ **應用程式效能** | ❌ API 存取記錄（那是 CloudTrail）|
| ✅ **資源使用率** | ❌ AWS 服務效能和可用性（那是 Health Dashboard）|
| ✅ EC2 指標（CPU、記憶體等）| ❌ 帳戶管理（那是 IAM）|
| ✅ 日誌監控（CloudWatch Logs）| |
| ✅ 設置告警 | |

---

## 問題 57 / Question 57

**[題目 / Question]**
A company wants to **audit requests made to an S3 bucket**. Which Amazon S3 feature?
公司想**審計對 S3 儲存桶發出的請求**，哪個 Amazon S3 功能？

**✅ 正確答案 / Correct Answer：Amazon S3 Access Logs（Amazon S3 存取日誌）**

**[中文詳解]**
**Amazon S3 存取日誌（Server Access Logging）** 提供對 S3 儲存桶發出的請求的詳細記錄。存取日誌資訊可用於安全和存取審計，幫助了解客戶群並理解 S3 費用。

**[S3 功能 vs 審計 / S3 Features vs Audit]**

| S3 功能 | 支援請求審計 |
|---|---|
| **Amazon S3 Access Logs** | **✅ 最佳** |
| S3 Versioning | ❌（版本管理，非審計）|
| S3 CRR | ❌（跨區域複製）|
| S3 Bucket Policies | ❌（存取控制，非審計）|

---

## 問題 58 / Question 58

**[題目 / Question]**
Which AWS service can view the **most comprehensive billing details** for the past month?
哪個 AWS 服務可查看上個月**最全面的計費詳細資料**？

**✅ 正確答案 / Correct Answer：AWS Cost & Usage Report (AWS CUR)**

**[成本工具功能定位 / Cost Tools Positioning — Exam Alert!]**

| 工具 / Tool | 功能定位 |
|---|---|
| **AWS CUR** | **最全面詳細的費用和使用資料（可輸出到 S3，按小時細分）** |
| AWS Cost Explorer | 高層次視覺化工具（歷史資料最多 12 個月）|
| AWS Budgets | 預算設置和告警 |
| AWS Pricing Calculator | 事前估算未來費用 |

> **記憶法**：最詳細 → **CUR（Cost & Usage Report）**；視覺化 → **Cost Explorer**

---

## 問題 59 / Question 59

**[題目 / Question]**
A start-up wants to **quickly deploy a popular technology** on AWS. Which AWS tool?
新創公司想在 AWS 上**快速部署流行技術**，哪個 AWS 工具？

**✅ 正確答案 / Correct Answer：AWS Partner Solutions (formerly Quick Starts)**

**[中文詳解]**
**AWS Partner Solutions（前身為 Quick Starts）** 是由 AWS 解決方案架構師和 AWS 合作夥伴建立的自動化參考部署。幫助您根據 AWS 最佳實踐將流行技術部署到 AWS，將數百個手動程序減少到幾個步驟，幾分鐘內即可開始使用環境。

**[快速部署資源對比 / Quick Deployment Resources]**

| 工具 / Tool | 用途 |
|---|---|
| **AWS Partner Solutions（Quick Starts）** | **自動化部署流行技術（幾分鐘內可用）** |
| AWS Whitepapers | 技術文件（不是部署服務）|
| AWS Forums | 社群支援（不是部署服務）|
| AWS CodeDeploy | 代碼部署自動化（非流行技術快速部署）|

---

## 問題 60 / Question 60

**[題目 / Question]**
A data science team wants to **build Machine Learning models**. Which AWS service?
資料科學團隊想**建立機器學習模型**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：Amazon SageMaker**

**[ML 服務完整對照 / ML Services Complete Reference]**

| 服務 / Service | 功能 / Function |
|---|---|
| **Amazon SageMaker** | **建立、訓練和部署 ML 模型（完整 ML 平台）** |
| Amazon Personalize | 個人化推薦（無需 ML 專業知識）|
| Amazon Comprehend | NLP（自然語言處理）|
| Amazon Rekognition | 圖像/視訊分析（圖像 ML）|
| Amazon Lex | 對話式 AI（聊天機器人）|
| Amazon Polly | 文字轉語音 |
| Amazon Transcribe | 語音轉文字 |
| Amazon Kendra | 企業智能搜索 |

---

## 問題 61 / Question 61

**[題目 / Question]**
A Cloud Practitioner wants to **centrally view, manage, and operate nodes** to identify issues impacting applications. Which AWS service?
Cloud Practitioner 想**集中查看、管理和操作節點**以快速識別影響應用程式的問題，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Systems Manager**

**[AWS Systems Manager 核心功能 / Systems Manager Core Capabilities]**
- ✅ 集中視圖管理節點（EC2、VM、本地伺服器）
- ✅ 安裝軟體、套用修補程式
- ✅ 跨 AWS 和本地的統一介面
- ✅ Session Manager（安全 Shell 存取）
- ✅ Run Command（遠端執行命令）

---

## 問題 62 / Question 62

**[題目 / Question]**
Adding more CPU/RAM to an Amazon EC2 instance represents which of the following?
為 Amazon EC2 執行個體添加更多 CPU/RAM 代表以下哪個？

**✅ 正確答案 / Correct Answer：Vertical scaling（垂直擴展）**

**[擴展類型定義 / Scaling Types]**

| 類型 / Type | 方式 / Method | 範例 |
|---|---|---|
| **垂直擴展 / Vertical Scaling（Scale Up）** | **增加單一節點的資源（CPU/RAM）** | **EC2 添加 CPU/RAM** |
| 水平擴展 / Horizontal Scaling（Scale Out）| 增加更多節點/電腦 | Auto Scaling Group、ELB |

---

## 問題 63 / Question 63

**[題目 / Question]**
Which statement is the MOST accurate when describing **AWS Elastic Beanstalk**?
哪個說法最準確地描述了 **AWS Elastic Beanstalk**？

**✅ 正確答案 / Correct Answer：It is a **Platform as a Service (PaaS)** that allows you to **deploy and scale web applications and services**（這是一個 **PaaS**，讓您**部署和擴展 Web 應用程式和服務**）**

**[Elastic Beanstalk 的正確定位 / Elastic Beanstalk Correct Positioning]**

| 特性 / Characteristic | 說明 |
|---|---|
| **服務類型** | **PaaS（您只管應用程式和資料）** |
| 功能 | 部署和擴展 Web 應用（非模型和佈建資源）|
| 底層 | 自動配置容量、ELB、Auto Scaling |

**[容易混淆的說法 / Common Confusions]**
- ❌ "允許您**模型和佈建**資源" → 那是 **CloudFormation**（IaC）
- ❌ "IaaS" → Elastic Beanstalk 是 **PaaS**，不需要管理 OS
- ✅ "PaaS，部署和擴展 Web 應用" → 正確

---

## 問題 64 / Question 64

**[題目 / Question]**
A startup wants to **remove its need to manage underlying infrastructure** and focus on deployment and management of applications. Which cloud computing type?
新創公司想**不再需要管理底層基礎設施**，專注於應用程式的部署和管理，這是哪種雲端運算類型？

**✅ 正確答案 / Correct Answer：Platform as a Service (PaaS)**

**[雲端服務類型 — 管理層級 / Cloud Types — Management Levels]**

```
                客戶管理 / Customer Manages
IaaS: 應用+資料+OS+運行環境+網路防火牆
PaaS: 應用+資料                           ← 此題答案
SaaS: 僅使用軟體
                AWS 管理 / AWS Manages
```

---

## 問題 65 / Question 65

**[題目 / Question]**
A company wants to **separate cost for AWS services by the department** for cost allocation. Which is the simplest way?
公司想按**部門分離 AWS 服務費用**以進行費用分配，最簡單的方法是？

**✅ 正確答案 / Correct Answer：Create tags for each department（為每個部門建立標籤）**

**[中文詳解]**
**AWS 標籤（Tags）** 是分配給 AWS 資源的元資料，每個標籤由使用者定義的鍵和值組成。可使用業務標籤（如成本中心/業務單位、客戶或專案）將 AWS 費用與傳統費用分配維度關聯起來。費用分配報告可包含任何標籤。

**[費用分配方法比較 / Cost Allocation Methods]**

| 方法 / Method | 難度 / Complexity | 推薦 |
|---|---|---|
| **建立標籤 / Create tags** | **最簡單** | **✅ 最佳** |
| 為每個部門建立不同帳戶 | 複雜（用戶可能屬於多個部門）| 不推薦 |
| 共享一個帳戶 | 最簡單但不安全 | ❌ 違反安全最佳實踐 |
| 建立不同 VPC | 不能分離費用 | ❌ |

---

## 📊 考題領域統計 / Domain Summary

| 領域 / Domain | 題數 / Questions | 百分比 / % |
|---|---|---|
| Technology（技術）| 27 | 41.5% |
| Security and Compliance（安全與合規）| 15 | 23.1% |
| Cloud Concepts（雲端概念）| 13 | 20.0% |
| Billing and Pricing（計費與定價）| 10 | 15.4% |

---

## 🎯 本回必考重點整理 / Key Exam Points (Set 5)

### 拒絕特定 IP 流量 → Network ACL（不是 Security Group）
Security Group 只能**允許**；Network ACL 可以**允許和拒絕**

### AWS DataSync vs Snowball
- **DataSync** → 線上、自動化、持續傳輸、增量備份
- **Snowball** → 離線、實體設備、一次性大量遷移

### Well-Architected Framework 各支柱設計原則
- **卓越運營** → 預見失敗、小規模可逆變更、IaC
- **安全** → 啟用可追溯性、KMS 加密
- **可靠性** → 自動從故障恢復
- **效能效率** → 使用無伺服器架構

### 新服務（本回新增）
- **AWS Fault Injection Simulator (FIS)** → 混沌工程（Chaos Engineering）
- **Amazon CodeGuru** → 自動化代碼審查（ML 驅動）
- **AWS DataSync** → 線上自動化資料傳輸
- **AWS CDK** → 用 Python/JS 等語言定義 IaC
- **Amazon Lightsail** → 最簡單的 VPS，低月費，適合初學者
- **AWS Partner Solutions（Quick Starts）** → 快速部署流行技術
- **AWS IAM Identity Center** → 多帳戶 SSO（AWS SSO 後繼者）
- **AWS STS** → 臨時安全憑證
- **IAM Access Advisor** → 審查使用者被授予的權限

### EBS 磁碟區重要規則
- EBS 磁碟區**綁定到特定 AZ**
- 磁碟區和執行個體**必須在同一 AZ**
- **不能**跨多個 AZ

### Amazon Personalize vs SageMaker
- **Personalize** → 即時個人化推薦（電商、媒體）
- **SageMaker** → 建立、訓練和部署通用 ML 模型

### VPC 和 Subnet 範圍
- **VPC** → 跨一個 Region 的**所有 AZ**
- **Subnet** → 只在**一個 AZ**

### S3 存取日誌
- 要**審計 S3 請求** → 使用 **S3 Access Logs（存取日誌）**

### AWS Organizations 最佳實踐
- ✅ 按部門建立帳戶
- ✅ 使用 SCP 限制權限
- ✅ 啟用 CloudTrail
- ✅ 使用標籤管理費用

### 費用標籤分配
- 最簡單的費用按部門分配方式 → **標籤（Tags）**

### Site-to-Site VPN 兩端組件
- **公司側** → **Customer Gateway**
- **AWS 側** → **Virtual Private Gateway (VGW)**
