# AWS Cloud Practitioner 考題中英對照詳解
# AWS Cloud Practitioner Exam Q&A with Bilingual Explanations

---

## 問題 1 / Question 1

**[題目 / Question]**
Which AWS Support plan provides architectural guidance contextual to your specific use-cases?
哪個 AWS Support 方案提供針對您特定使用案例的架構指導？

**✅ 正確答案 / Correct Answer：AWS Business Support**

**[中文詳解]**
AWS Business Support 適合在 AWS 上有生產工作負載的用戶，提供 24/7 電話、電子郵件和聊天技術支援，以及針對**特定使用案例的架構指導**。可完整使用 AWS Trusted Advisor 最佳實踐檢查，並可付費使用基礎設施事件管理。

**[English Explanation]**
AWS Business Support provides 24/7 phone, email, and chat access to technical support with architectural guidance **contextual to your specific use-cases**. It includes full access to AWS Trusted Advisor Best Practice Checks and access to Infrastructure Event Management for an additional fee.

**[選項比較 / Option Comparison]**

| 方案 / Plan | 架構指導 / Architectural Guidance |
|---|---|
| Basic | ❌ 無 / None |
| Developer | ⚠️ 一般通用指導 / General guidance only |
| **Business** | ✅ **針對特定使用案例 / Contextual to specific use-cases** |
| Enterprise On-Ramp | ✅ 每年一次 / Once per year |
| Enterprise | ✅ 針對應用程式 / Contextual to applications |

**[考試重點 / Exam Tip]**
記住 Business Support 是提供「use-case specific」架構指導的最低方案。

---

## 問題 2 / Question 2

**[題目 / Question]**
Which AWS Route 53 routing policy would you use to route traffic to multiple resources and also choose how much traffic is routed to each resource?
哪個 AWS Route 53 路由策略可將流量路由到多個資源，並選擇路由到每個資源的流量比例？

**✅ 正確答案 / Correct Answer：Weighted Routing（加權路由）**

**[中文詳解]**
**加權路由 (Weighted Routing)** 讓您能將單一域名關聯多個資源，並控制路由到每個資源的流量比例。透過指定相對權重來分配流量，適合用於負載均衡和新版本軟體測試。

**[English Explanation]**
**Weighted routing** lets you associate multiple resources with a single domain name and choose how much traffic is routed to each resource. You assign each record a relative weight corresponding to the proportion of traffic you want to send to each resource.

**[路由策略比較 / Routing Policy Comparison]**

| 策略 / Policy | 使用場景 / Use Case |
|---|---|
| Simple（簡單） | 路由到單一資源 / Route to a single resource |
| **Weighted（加權）** | **控制各資源流量比例 / Control traffic % per resource** |
| Latency-based（延遲） | 路由到最低延遲的區域 / Route to lowest latency region |
| Failover（容錯移轉） | 主動-被動容錯移轉 / Active-passive failover |

---

## 問題 3 / Question 3

**[題目 / Question]**
A financial services company wants to ensure that its AWS account activity meets governance, compliance, and auditing norms. Which AWS service would you recommend?
金融服務公司想確保 AWS 帳戶活動符合治理、合規和審計規範，推薦哪個服務？

**✅ 正確答案 / Correct Answer：AWS CloudTrail**

**[中文詳解]**
**AWS CloudTrail** 記錄並監控 AWS 帳戶中的所有 API 活動，包括透過管理控制台、SDK、命令列工具等執行的操作，提供完整的事件歷史記錄，適合治理、合規和審計需求。

**[English Explanation]**
**AWS CloudTrail** logs, monitors, and retains account activity related to actions across your AWS infrastructure, providing an event history including actions through the AWS Management Console, SDKs, CLI, and other AWS services.

**[三大監控服務比較 / Key Comparison — Must Know!]**

| 服務 / Service | 功能定位 / Purpose |
|---|---|
| **CloudWatch** | 資源效能監控、事件與告警 / Resource performance monitoring, events & alerts |
| **CloudTrail** | 帳戶操作活動與審計 / Account-specific activity & audit |
| **Config** | 資源配置變更歷史與合規 / Resource-specific change history & compliance |

**[考試重點 / Exam Tip]**
> 想到帳戶活動審計 → CloudTrail
> 想到資源效能監控 → CloudWatch
> 想到資源配置變更 → Config

---

## 問題 4 / Question 4

**[題目 / Question]**
A company wants to have control over creating and using its own keys for encryption on AWS services. Which of the following can be used?
公司希望自行建立並控制用於加密 AWS 服務的金鑰，應使用哪個方案？

**✅ 正確答案 / Correct Answer：Customer Managed Key (CMK)（客戶管理金鑰）**

**[中文詳解]**
**客戶管理金鑰 (CMK)** 是您在 AWS 帳戶中自行建立、擁有和管理的 KMS 金鑰。您對這些金鑰擁有完全控制權，包括設定金鑰策略、IAM 策略、啟用/停用、輪換加密材料等。

**[English Explanation]**
**Customer managed keys (CMK)** are KMS keys in your AWS account that you create, own, and manage. You have full control including establishing key policies, IAM policies, enabling/disabling, rotating cryptographic material, and scheduling deletion.

**[金鑰類型比較 / Key Type Comparison]**

| 金鑰類型 / Key Type | 控制者 / Controller | 使用場景 / Use Case |
|---|---|---|
| **Customer Managed Key** | **客戶 / Customer** | **自訂控制加密 / Custom encryption control** |
| AWS Managed Key | AWS（代客戶）/ AWS on behalf of customer | AWS 服務整合 / AWS service integration |
| AWS Owned Key | AWS | 多帳戶共用 / Multi-account use |

---

## 問題 5 / Question 5

**[題目 / Question]**
Which AWS Service can be used to mitigate a Distributed Denial of Service (DDoS) attack?
哪個 AWS 服務可用來緩解分散式阻斷服務 (DDoS) 攻擊？

**✅ 正確答案 / Correct Answer：AWS Shield**

**[中文詳解]**
**AWS Shield** 是託管型 DDoS 防護服務，提供即時偵測和自動緩解，無需聯繫 AWS 支援即可受益。分兩個層級：
- **Standard（標準版）**：免費，所有 AWS 客戶自動啟用，防護第 3、4 層攻擊
- **Advanced（進階版）**：付費，額外保護第 7 層，提供近即時可見性，整合 AWS WAF

**[English Explanation]**
**AWS Shield** is a managed DDoS protection service with always-on detection and automatic inline mitigations.
- **Standard**: Free, auto-enabled for all customers, protects against Layer 3 & 4 attacks
- **Advanced**: Paid, adds Layer 7 protection, near real-time visibility, integrates with AWS WAF

---

## 問題 6 / Question 6

**[題目 / Question]**
A startup wants to migrate its data and applications from on-premises to AWS Cloud. Which options can help with this migration? (Select two)
新創公司想從本地資料中心遷移到 AWS 雲端，哪兩個選項可協助遷移？（選兩個）

**✅ 正確答案 / Correct Answers：**
1. AWS Professional Services（AWS 專業服務）
2. AWS Partner Network (APN)（AWS 合作夥伴網路）

**[中文詳解]**
- **AWS Professional Services**：AWS 全球專家團隊，可協助加速基礎設施遷移，補充客戶團隊的專業技能
- **AWS Partner Network (APN)**：全球技術和諮詢合作夥伴計畫，APN 合作夥伴可協助建立客製化遷移解決方案

**[English Explanation]**
- **AWS Professional Services**: Global team of experts to accelerate migration with specialized skills
- **APN**: Global partner program where consulting partners help design, build, migrate, and manage workloads on AWS

---

## 問題 7 / Question 7

**[題目 / Question]**
Which AWS service should be used to automatically distribute incoming traffic across multiple targets?
哪個 AWS 服務可自動將傳入流量分配到多個目標？

**✅ 正確答案 / Correct Answer：AWS Elastic Load Balancing (ELB)**

**[中文詳解]**
**彈性負載平衡 (ELB)** 自動將應用程式傳入流量分配到所有執行中的 EC2 執行個體，確保沒有單一執行個體負載過重，作為所有傳入流量的單一聯絡點。

**[English Explanation]**
**ELB** automatically distributes incoming application traffic across all running EC2 instances, acting as a single point of contact for all incoming web traffic to prevent any one instance from being overwhelmed.

**[相關服務比較 / Related Services]**

| 服務 / Service | 功能 / Function |
|---|---|
| **ELB** | **流量分配 / Traffic distribution** |
| Auto Scaling | 自動調整容量 / Auto adjust capacity |
| Elastic Beanstalk | 應用程式部署與管理 / App deployment & management |

---

## 問題 8 / Question 8

**[題目 / Question]**
A startup wants to provision an EC2 instance for the lowest possible cost for a long-term duration but needs to make sure the instance would never be interrupted. Which option would you recommend?
新創公司想以最低成本長期使用 EC2，且執行個體不能被中斷，推薦哪個選項？

**✅ 正確答案 / Correct Answer：EC2 Reserved Instance (RI)（預留執行個體）**

**[中文詳解]**
**預留執行個體 (RI)** 與隨需定價相比可節省高達 75%，可承諾 1 年或 3 年期（3 年折扣更大），且**不會被中斷**，適合長期穩定工作負載。

**[English Explanation]**
**EC2 Reserved Instances (RI)** offer savings up to 75% compared to On-Demand pricing, available for 1-year or 3-year commitment, and **cannot be interrupted**, making them ideal for long-term stable workloads.

**[EC2 定價選項比較 / EC2 Pricing Comparison]**

| 類型 / Type | 折扣 / Discount | 可中斷 / Interruptible | 適用場景 / Best For |
|---|---|---|---|
| On-Demand | 無 / None | ❌ | 短期靈活 / Short-term flexible |
| **Reserved (RI)** | **最高 75%** | **❌** | **長期穩定 / Long-term stable** |
| Spot | 最高 90% | ✅ 會被中斷 | 容錯批次處理 / Fault-tolerant batch |
| Dedicated Host | 無折扣 | ❌ | 授權軟體 / Licensed software |

---

## 問題 9 / Question 9

**[題目 / Question]**
Which is CORRECT regarding removing an AWS account from AWS Organizations?
關於從 AWS Organizations 移除 AWS 帳戶，哪個說法正確？

**✅ 正確答案 / Correct Answer：**
The AWS account must be able to operate as a standalone account.
AWS 帳戶必須能夠作為獨立帳戶運作。

**[中文詳解]**
要從組織中移除帳戶，該帳戶必須具備獨立運作所需的資訊：接受 AWS 客戶協議、選擇支援方案、提供並驗證聯絡資訊，以及提供有效的付款方式。

**[English Explanation]**
To remove an account from an organization, it must have the information required to operate as a standalone account: accept AWS Customer Agreement, choose a support plan, provide verified contact information, and provide a current payment method.

---

## 問題 10 / Question 10

**[題目 / Question]**
A web application needs data to be encrypted **before** sending it to Amazon S3. Which technique is correct?
Web 應用程式需要在**傳送之前**加密資料再送到 S3，哪個技術正確？

**✅ 正確答案 / Correct Answer：Enable client-side encryption using AWS encryption SDK（使用 AWS 加密 SDK 啟用用戶端加密）**

**[中文詳解]**
**用戶端加密 (Client-side encryption)** 指在傳送到 S3 之前就先加密資料。AWS Encryption SDK 是獨立的用戶端加密程式庫，不受特定語言 SDK 限制，也不限於 Amazon S3，可用於加密/解密任何地方儲存的資料。

**[English Explanation]**
**Client-side encryption** means encrypting data before sending it to S3. The AWS encryption SDK is a client-side library separate from language-specific SDKs and not tied to Amazon S3, enabling encryption best practices.

**[加密方式比較 / Encryption Type Comparison]**

| 加密方式 / Type | 加密發生位置 / Where | 誰執行 / Who |
|---|---|---|
| **Client-side（用戶端）** | **傳送前 / Before sending** | **您的應用程式 / Your app** |
| SSE-S3 | S3 收到後 / After received by S3 | S3（使用 S3 管理金鑰）|
| SSE-KMS | S3 收到後 / After received by S3 | S3（使用 KMS 金鑰）|

---

## 問題 11 / Question 11

**[題目 / Question]**
An organization wants to privately connect VPCs and supported AWS services without using the public internet. Which AWS services can meet this requirement? (Select two)
組織想在不使用公共網際網路的情況下私密連接 VPC 和 AWS 服務，哪兩個服務符合？

**✅ 正確答案 / Correct Answers：**
1. AWS PrivateLink
2. AWS Transit Gateway

**[中文詳解]**
- **AWS PrivateLink**：在 VPC 和支援的 AWS 服務之間啟用私有連接，流量不經過公共網際網路
- **AWS Transit Gateway**：高度可擴展的服務，透過中央樞紐連接多個 VPC 和本地網路，採用 Hub-and-Spoke 模型簡化管理

**[English Explanation]**
- **AWS PrivateLink**: Enables private connectivity between VPCs and AWS services without traffic traversing the public internet
- **AWS Transit Gateway**: Connects multiple VPCs and on-premises networks through a central hub using a hub-and-spoke model

---

## 問題 12 / Question 12

**[題目 / Question]**
AWS Shield Advanced provides expanded DDoS attack protection for web applications running on which resources? (Select two)
AWS Shield Advanced 為哪兩個資源上的 Web 應用程式提供擴展的 DDoS 防護？

**✅ 正確答案 / Correct Answers：**
1. Amazon Route 53
2. AWS Global Accelerator

**[中文詳解]**
AWS Shield Advanced 支援的資源：Amazon EC2、Elastic Load Balancing (ELB)、Amazon CloudFront、**Amazon Route 53**、**AWS Global Accelerator**

**[English Explanation]**
AWS Shield Advanced covers: Amazon EC2, ELB, Amazon CloudFront, **Amazon Route 53**, and **AWS Global Accelerator**.

> ⚠️ API Gateway、CloudFormation、Elastic Beanstalk 均**不**在 Shield Advanced 涵蓋範圍內

---

## 問題 13 / Question 13

**[題目 / Question]**
As part of the Shared Responsibility Model, AWS is responsible for which of the following?
在共同責任模型中，AWS 負責以下哪項？

**✅ 正確答案 / Correct Answer：Physical and Environmental controls（實體與環境控制）**

**[共同責任模型 / Shared Responsibility Model]**

| AWS 負責 / AWS Responsible | 客戶負責 / Customer Responsible |
|---|---|
| 實體與環境安全 / Physical & Environmental | 修補 Guest OS / Patching Guest OS |
| 硬體基礎設施 / Hardware infrastructure | 配置應用程式 / Configuring applications |
| 網路基礎設施 / Network infrastructure | 資料加密 / Data encryption |
| 虛擬化層 / Virtualization layer | IAM 政策 / IAM policies |

---

## 問題 14 / Question 14

**[題目 / Question]**
Which of the following is an AWS database service?
以下哪個是 AWS 資料庫服務？

**✅ 正確答案 / Correct Answer：Amazon Redshift**

**[中文詳解]**
**Amazon Redshift** 是全托管的 PB 級雲端資料倉儲，專為大規模資料集儲存和分析設計。

**[English Explanation]**
**Amazon Redshift** is a fully-managed petabyte-scale cloud-based data warehouse designed for large scale data set storage and analysis.

**[混淆選項說明 / Distractor Explanation]**

| 服務 / Service | 實際功能 / Actual Function |
|---|---|
| AWS Glue | ETL 服務 / ETL service |
| AWS Storage Gateway | 混合雲儲存 / Hybrid cloud storage |
| AWS DMS | 資料庫遷移 / Database migration |
| **Amazon Redshift** | **資料倉儲 / Data warehouse** ✅ |

---

## 問題 15 / Question 15

**[題目 / Question]**
Which of the following entities applies patches to the underlying OS for Amazon Aurora?
哪個實體負責對 Amazon Aurora 的底層 OS 套用修補程式？

**✅ 正確答案 / Correct Answer：The AWS Product Team automatically（AWS 產品團隊自動執行）**

**[中文詳解]**
Amazon Aurora 由 Amazon RDS 完全託管，AWS 產品團隊自動處理底層 OS 修補、硬體佈建、資料庫設定和備份等管理工作，客戶無需介入。

**[English Explanation]**
Amazon Aurora is fully managed by Amazon RDS, which automates administration tasks like hardware provisioning, database setup, **patching**, and backups. The AWS Product Team applies patches automatically.

---

## 問題 16 / Question 16

**[題目 / Question]**
Which AWS Support plans provide access to guidance, configuration, and troubleshooting of AWS interoperability with third-party software? (Select two)
哪兩個 AWS Support 方案提供 AWS 與第三方軟體互通性的指導、配置和故障排除？

**✅ 正確答案 / Correct Answers：**
1. AWS Business Support
2. AWS Enterprise Support

**[支援方案功能比較 / Support Plan Comparison]**

| 功能 / Feature | Basic | Developer | Business | Enterprise On-Ramp | Enterprise |
|---|---|---|---|---|---|
| 第三方軟體支援 | ❌ | ❌ | ✅ | ✅ | ✅ |
| Trusted Advisor 完整檢查 | ❌ | ❌ | ✅ | ✅ | ✅ |
| TAM 技術客戶經理 | ❌ | ❌ | ❌ | ✅ (共享) | ✅ (專屬) |

---

## 問題 17 / Question 17

**[題目 / Question]**
Which AWS services support VPC Gateway Endpoint for a private connection from a VPC? (Select two)
哪兩個 AWS 服務支援 VPC Gateway Endpoint？

**✅ 正確答案 / Correct Answers：**
1. Amazon S3
2. Amazon DynamoDB

**[考試重點 / Exam Tip — Must Memorize!]**
> **只有 Amazon S3 和 Amazon DynamoDB 支援 VPC Gateway Endpoint！**
> **Only Amazon S3 and Amazon DynamoDB support VPC Gateway Endpoints!**
> 其他服務使用 VPC Interface Endpoint（由 AWS PrivateLink 提供）

---

## 問題 18 / Question 18

**[題目 / Question]**
The DevOps team is moving 500 GB of data from an EC2 instance to an S3 bucket **in the same region**. What are the charges?
DevOps 團隊將 500 GB 資料從 EC2 移動到**同一區域**的 S3 儲存桶，費用為何？

**✅ 正確答案 / Correct Answer：The company would not be charged for this data transfer（不收取任何資料傳輸費用）**

**[AWS 資料傳輸費用規則 / AWS Data Transfer Pricing Rules]**

| 傳輸類型 / Transfer Type | 費用 / Cost |
|---|---|
| 同區域內 EC2 ↔ S3 / Same-region EC2 ↔ S3 | **免費 / Free** ✅ |
| 傳入 AWS / Inbound to AWS | 免費 / Free |
| 跨區域 / Cross-region | 收費 / Charged |
| 傳出到網際網路 / Outbound to internet | 收費 / Charged |

---

## 問題 19 / Question 19

**[題目 / Question]**
According to the AWS Shared Responsibility Model, which are responsibilities of AWS? (Select two)
根據 AWS 共同責任模型，哪兩項是 AWS 的責任？

**✅ 正確答案 / Correct Answers：**
1. Operating the infrastructure layer, OS, and platform for Amazon S3
2. Replacing faulty hardware of Amazon EC2 instances

**[中文詳解]**
- 對於抽象服務（如 S3、DynamoDB），AWS 負責基礎設施層、作業系統和平台的運作
- 替換故障的 EC2 硬體屬於「雲端安全」，是 AWS 的責任

**[客戶責任 / Customer Responsibilities]**
- 啟用多重要素驗證 (MFA) / Enabling MFA
- 建立 IAM 角色 / Creating IAM roles
- 建立 S3 儲存桶策略 / Creating S3 bucket policies

---

## 問題 20 / Question 20

**[題目 / Question]**
A healthcare startup wants to discover and identify sensitive data on S3 to prevent data leaks. Which AWS service would you recommend?
醫療新創公司想在 S3 上發現並識別敏感資料以防止洩漏，推薦哪個服務？

**✅ 正確答案 / Correct Answer：Amazon Macie**

**[中文詳解]**
**Amazon Macie** 是全托管的資料安全和隱私服務，使用機器學習和模式比對來發現和保護 AWS 中的敏感資料，自動識別未加密的儲存桶、公開訪問的儲存桶，並識別 PII（個人識別資訊）等敏感資料。

**[English Explanation]**
**Amazon Macie** uses machine learning and pattern matching to automatically discover and protect sensitive data in AWS, identifying unencrypted/publicly accessible S3 buckets and sensitive data like PII.

---

## 問題 21 / Question 21

**[題目 / Question]**
Which AWS services can be used to decouple components of a microservices based application? (Select two)
哪兩個 AWS 服務可用來解耦微服務架構應用程式的組件？

**✅ 正確答案 / Correct Answers：**
1. Amazon SQS（簡單佇列服務）
2. Amazon SNS（簡單通知服務）

**[解耦服務說明 / Decoupling Services]**

| 服務 / Service | 模式 / Pattern | 說明 / Description |
|---|---|---|
| **SQS** | **訊息佇列 / Message Queue** | 傳送、儲存、接收訊息 |
| **SNS** | **發布/訂閱 / Pub/Sub** | 扇出通知到多個訂閱者 |
| Lambda | 無伺服器運算 | 無法用於解耦 |
| Step Functions | 工作流程協調 | 無法用於解耦 |

---

## 問題 22 / Question 22

**[題目 / Question]**
A company wants to rapidly develop, test, and launch software applications utilizing relevant AWS services. Which cloud characteristic does it want to leverage?
公司希望快速開發、測試和發布軟體應用程式，這利用了雲端的哪個特性？

**✅ 正確答案 / Correct Answer：Agility（敏捷性）**

**[雲端特性定義 / Cloud Characteristics]**

| 特性 / Characteristic | 定義 / Definition |
|---|---|
| **Agility（敏捷性）** | **快速開發、測試和發布軟體的能力 / Ability to rapidly develop, test & launch software** |
| Elasticity（彈性） | 按需獲取和釋放資源 / Acquire & release resources as needed |
| Scalability（可擴展性） | 系統因應需求增減的能力 / System's ability to grow/shrink with demand |
| Reliability（可靠性） | 從故障中恢復的能力 / Ability to recover from disruptions |

---

## 問題 23 / Question 23

**[題目 / Question]**
Which statement is CORRECT regarding AZ-specific characteristics of Amazon EBS and Amazon EFS?
關於 Amazon EBS 和 Amazon EFS 的可用區域特性，哪個說法正確？

**✅ 正確答案 / Correct Answer：**
EBS volume can be attached to a single instance **in the same AZ** whereas EFS file system can be mounted on instances **across multiple AZs**.
EBS 磁碟區只能掛載到**同一 AZ** 的單一執行個體，而 EFS 可以掛載到**跨多個 AZ** 的執行個體。

**[EBS vs EFS 比較 / Comparison]**

| 特性 / Feature | Amazon EBS | Amazon EFS |
|---|---|---|
| 儲存類型 / Storage Type | 區塊儲存 / Block | 文件儲存 / File (NFS) |
| 可用區域 / AZ Scope | 單一 AZ / Single AZ | 跨多個 AZ / Multiple AZs |
| 同時存取 / Concurrent Access | 單一執行個體（Multi-Attach 除外）| 數千個執行個體 / Thousands |
| 擴展性 / Scalability | 手動 / Manual | 自動彈性 / Auto elastic |

---

## 問題 24 / Question 24

**[題目 / Question]**
Which AWS Support plans provide access to only **core checks** from the AWS Trusted Advisor Best Practice Checks? (Select two)
哪兩個 AWS Support 方案只提供 Trusted Advisor 的**核心檢查**？

**✅ 正確答案 / Correct Answers：**
1. AWS Basic Support
2. AWS Developer Support

**[Trusted Advisor 存取層級 / Access Levels]**

| 方案 / Plan | Trusted Advisor 存取 |
|---|---|
| Basic | 僅核心檢查 / Core checks only |
| Developer | 僅核心檢查（服務配額和基本安全）|
| Business | **完整存取 / Full access** ✅ |
| Enterprise On-Ramp | **完整存取 / Full access** ✅ |
| Enterprise | **完整存取 / Full access** ✅ |

---

## 問題 25 / Question 25

**[題目 / Question]**
An organization operating MySQL databases on-premises wants to move to a **fully managed AWS database** offering. Which migration strategy best aligns with this goal?
組織想從本地 MySQL 資料庫遷移到**全托管 AWS 資料庫**，哪個遷移策略最符合？

**✅ 正確答案 / Correct Answer：Replatform（重新平台化）**

**[6R 遷移策略 / 6R Migration Strategies]**

| 策略 / Strategy | 說明 / Description | 此案例 |
|---|---|---|
| Rehost（重新託管）| 直接搬移，不變架構 / Lift-and-shift | ❌ 仍需自管 |
| **Replatform（重新平台化）** | **遷移並部分優化（如改用 RDS）** | **✅** |
| Repurchase（重新購買）| 換用全新 SaaS 產品 | ❌ |
| Refactor（重新架構）| 重新設計應用程式 | ❌ 過於複雜 |

---

## 問題 26 / Question 26

**[題目 / Question]**
Which of the following are advantages of cloud computing? (Select three)
以下哪三項是雲端運算的優勢？

**✅ 正確答案 / Correct Answers：**
1. Benefit from massive economies of scale（受益於大規模經濟）
2. Trade capital expense for variable expense（將資本支出換為可變支出）
3. Go global in minutes（幾分鐘內全球部署）

**[雲端運算六大優勢 / 6 Advantages of Cloud Computing]**
1. 將資本支出換為可變支出 / Trade CapEx for variable expense
2. 受益於大規模經濟 / Benefit from massive economies of scale
3. 停止猜測容量 / Stop guessing capacity
4. 提高速度和敏捷性 / Increase speed and agility
5. 停止在資料中心上花費 / Stop spending money on data centers
6. 幾分鐘內全球化 / Go global in minutes

---

## 問題 27 / Question 27

**[題目 / Question]**
An analytics application needs speech-based input (speech → text → processing → speech output). Which solution would you recommend?
分析應用程式需要語音輸入和語音輸出，推薦哪個解決方案？

**✅ 正確答案 / Correct Answer：**
Use **Amazon Transcribe** to convert speech to text, then use **Amazon Polly** to convey results via speech.
使用 **Amazon Transcribe** 將語音轉為文字，再使用 **Amazon Polly** 將文字結果轉為語音。

**[AI/ML 語音服務 / AI/ML Speech Services]**

| 服務 / Service | 功能 / Function |
|---|---|
| **Amazon Transcribe** | **語音 → 文字 / Speech → Text (ASR)** |
| **Amazon Polly** | **文字 → 語音 / Text → Speech (TTS)** |
| Amazon Translate | 語言翻譯 / Language translation |
| Amazon Rekognition | 影像/視訊分析 / Image & video analysis |

---

## 問題 28 / Question 28

**[題目 / Question]**
Which AWS service will help you receive alerts when the reservation utilization falls below the defined threshold?
哪個 AWS 服務可在預留使用率低於設定閾值時發送警示？

**✅ 正確答案 / Correct Answer：AWS Budgets（AWS 預算）**

**[成本管理服務比較 / Cost Management Services]**

| 服務 / Service | 主要功能 / Main Function |
|---|---|
| **AWS Budgets** | **設定預算和警示（含預留使用率）/ Set budgets & alerts (incl. reservation utilization)** |
| Cost Explorer | 視覺化成本和使用情況 / Visualize costs & usage |
| Pricing Calculator | 估算 AWS 服務成本 / Estimate service costs |
| Cost & Usage Report | 詳細的帳單報告 / Detailed billing report |

---

## 問題 29 / Question 29

**[題目 / Question]**
A company wants to identify the optimal AWS resource configuration to reduce costs and increase performance. Which service can be used?
公司想找出最佳 AWS 資源配置以降低成本和提升效能，應使用哪個服務？

**✅ 正確答案 / Correct Answer：AWS Compute Optimizer**

**[中文詳解]**
**AWS Compute Optimizer** 使用機器學習分析歷史使用指標，為以下資源提供最優配置建議：
- Amazon EC2 執行個體
- Amazon EBS 磁碟區
- AWS Lambda 函數

**[English Explanation]**
**AWS Compute Optimizer** uses machine learning to analyze historical utilization metrics and recommends optimal configurations for EC2 instances, EBS volumes, and Lambda functions to reduce costs and improve performance.

---

## 問題 30 / Question 30

**[題目 / Question]**
Which is the MOST cost-effective option to purchase an EC2 Reserved Instance (RI)?
購買 EC2 預留執行個體最具成本效益的選項是？

**✅ 正確答案 / Correct Answer：Partial upfront payment option with standard 3-years term（3 年期部分預付）**

**[RI 費用節省比較 / RI Savings Comparison]**

| 選項 / Option | 節省 / Savings |
|---|---|
| 1 年期無預付 / 1-year No Upfront | 36% |
| 1 年期全額預付 / 1-year All Upfront | 40% |
| 3 年期無預付 / 3-year No Upfront | 56% |
| **3 年期部分預付 / 3-year Partial Upfront** | **59% ✅** |

**[考試重點 / Exam Tip]**
> 3 年 > 1 年；全額預付 > 部分預付 > 無預付（以節省成本排序）

---

## 問題 31 / Question 31

**[題目 / Question]**
Which AWS service can connect a company's on-premises environment to a VPC **without using the public internet**?
哪個 AWS 服務可在**不使用公共網際網路**的情況下連接本地環境到 VPC？

**✅ 正確答案 / Correct Answer：AWS Direct Connect**

**[連接選項比較 / Connection Options]**

| 服務 / Service | 連接方式 / Connection | 公共網際網路 / Public Internet |
|---|---|---|
| **AWS Direct Connect** | **專用實體線路 / Dedicated physical** | **❌ 不經過 / Bypasses** |
| AWS Site-to-Site VPN | VPN 加密隧道 / VPN tunnel | ✅ 經過 / Goes through |
| Internet Gateway | 網際網路 / Internet | ✅ 是 / Yes |

> ⚠️ Direct Connect 需要至少一個月建立實體連線

---

## 問題 32 / Question 32

**[題目 / Question]**
Credit one ($100, expires July 2022, usable for EC2 or S3). Credit two ($50, expires Dec 2022, EC2 only). Charges: $1000 EC2 + $500 S3. What's the outcome? (Select two)
信用額度一 ($100，7月到期，可用於 EC2 或 S3)。信用額度二 ($50，12月到期，僅限 EC2)。費用：EC2 $1000 + S3 $500，結果為何？

**✅ 正確答案 / Correct Answers：**
1. Credit one applied to EC2 → $900 EC2, $500 S3 remaining
2. Credit two applied to $900 EC2 → Final: $850 EC2 + $500 S3

**[AWS 信用額度套用順序 / Credit Application Order]**
1. 最快到期的 / Soonest expiring
2. 適用產品最少的 / Least number of applicable products
3. 最舊的 / Oldest credit

---

## 問題 33 / Question 33

**[題目 / Question]**
Which of the following AWS services has encryption **enabled by default**?
哪個 AWS 服務**預設啟用**加密？

**✅ 正確答案 / Correct Answer：AWS CloudTrail Logs**

**[中文詳解]**
CloudTrail 日誌預設使用 Amazon S3 管理金鑰的伺服器端加密 (SSE-S3)。EBS、EFS 和 RDS 的加密是**可選功能**，需要用戶手動啟用。

**[加密預設狀態 / Default Encryption Status]**

| 服務 / Service | 預設加密 / Default Encryption |
|---|---|
| **CloudTrail Logs** | **✅ 預設啟用 / Enabled by default** |
| EBS | ❌ 需手動啟用 / Manual |
| EFS | ❌ 需手動啟用 / Manual |
| RDS | ❌ 需手動啟用 / Manual |

---

## 問題 34 / Question 34

**[題目 / Question]**
Which statements are CORRECT regarding the AWS Global Infrastructure? (Select two)
哪兩個關於 AWS 全球基礎設施的說法正確？

**✅ 正確答案 / Correct Answers：**
1. Each AWS Region consists of a minimum of **three** Availability Zones
2. Each AZ consists of **one or more** discrete data centers

**[AWS 全球基礎設施架構 / Global Infrastructure]**
```
AWS Global Infrastructure
├── Region（區域）
│   ├── 最少 3 個可用區域 / Minimum 3 AZs
│   └── AZ（可用區域）
│       └── 1 個或多個資料中心 / 1 or more data centers
└── Edge Locations（邊緣節點）
    └── 用於 CloudFront CDN / For CloudFront CDN
```

---

## 問題 35 / Question 35

**[題目 / Question]**
Which security service is enabled for all AWS customers, by default, at no additional cost?
哪個安全服務預設為所有 AWS 客戶啟用且無需額外費用？

**✅ 正確答案 / Correct Answer：AWS Shield Standard**

**[Shield 層級比較 / Shield Tier Comparison]**

| 層級 / Tier | 費用 / Cost | 保護 / Protection |
|---|---|---|
| **Standard** | **免費 / Free** | Layer 3 & 4 DDoS |
| Advanced | 付費 / Paid | Layer 3, 4 & 7 + WAF 整合 |

---

## 問題 36 / Question 36

**[題目 / Question]**
Which statements are CORRECT regarding the AWS VPC service? (Select two)
哪兩個關於 AWS VPC 服務的說法正確？

**✅ 正確答案 / Correct Answers：**
1. A Security Group can have **allow rules only**（安全群組只能有允許規則）
2. A NAT Gateway is **managed by AWS**（NAT 閘道由 AWS 管理）

**[VPC 安全組件比較 / VPC Security Components]**

| 組件 / Component | 規則類型 / Rules | 層級 / Level | 管理者 / Manager |
|---|---|---|---|
| Security Group（安全群組） | 僅允許 / Allow only | 執行個體 / Instance | 客戶 / Customer |
| Network ACL（網路 ACL） | 允許 + 拒絕 / Allow & Deny | 子網路 / Subnet | 客戶 / Customer |
| NAT Gateway | N/A | VPC | **AWS** ✅ |
| NAT Instance | N/A | VPC | 客戶 / Customer |

---

## 問題 37 / Question 37

**[題目 / Question]**
A company with multiple AWS accounts wants to share reserved EC2 instances among all units to optimize costs. What is the most cost-optimal solution?
擁有多個 AWS 帳戶的公司想共享預留 EC2 執行個體以優化成本，最佳方案是？

**✅ 正確答案 / Correct Answer：Use AWS Organizations**

**[中文詳解]**
**AWS Organizations** 允許集中管理多個 AWS 帳戶的計費，並在帳戶之間共享預留執行個體，對所有 AWS 客戶免費提供。

**[English Explanation]**
**AWS Organizations** enables centralized billing management and allows sharing reserved EC2 instances among multiple AWS accounts at no additional cost.

---

## 問題 38 / Question 38

**[題目 / Question]**
A company wants to automate timely assessments and check for OS vulnerabilities on EC2 instances. Which service would you suggest?
公司想自動化定期評估並檢查 EC2 執行個體的 OS 漏洞，推薦哪個服務？

**✅ 正確答案 / Correct Answer：Amazon Inspector**

**[安全服務比較 / Security Services Comparison]**

| 服務 / Service | 功能 / Function |
|---|---|
| **Amazon Inspector** | **EC2 執行個體漏洞評估 / EC2 vulnerability assessment** |
| Amazon GuardDuty | 帳戶層級威脅偵測 / Account-level threat detection |
| Amazon Macie | S3 敏感資料探索 / S3 sensitive data discovery |
| AWS Shield | DDoS 防護 / DDoS protection |

---

## 問題 39 / Question 39

**[題目 / Question]**
Which is a recommended way to provide programmatic access to AWS resources?
哪個是對 AWS 資源提供程式化訪問的建議方式？

**✅ 正確答案 / Correct Answer：Use Access Key ID and Secret Access Key**

**[中文詳解]**
**存取金鑰 (Access Keys)** 由兩部分組成：存取金鑰 ID 和私密存取金鑰，用於簽署 AWS CLI 或 API 的程式化請求。兩者必須同時使用才能驗證請求。

**[考試重點 / Exam Tip]**
> 程式化訪問 → Access Key ID + Secret Access Key
> 控制台訪問 → 使用者名稱 + 密碼 (+ MFA)

---

## 問題 40 / Question 40

**[題目 / Question]**
A fault tolerant scientific computation application needs high-performance hardware disks with fast I/O. Which storage option is the MOST cost-effective?
具有容錯架構的科學計算應用程式需要高效能、快速 I/O 的硬碟，最具成本效益的儲存選項是？

**✅ 正確答案 / Correct Answer：Instance Store（執行個體存放區）**

**[中文詳解]**
**Instance Store** 提供臨時性區塊層級儲存，實體附加在主機電腦上，具有極低延遲。由於已包含在執行個體使用成本中（無需額外費用），且應用程式本身具有容錯架構可處理資料遺失，因此是最具成本效益的選擇。

**[儲存選項比較 / Storage Options Comparison]**

| 儲存 / Storage | 延遲 / Latency | 持久性 / Durability | 費用 / Cost |
|---|---|---|---|
| **Instance Store** | **最低 / Lowest** | ❌ 臨時性 / Temporary | **包含在執行個體費用 / Included** |
| EBS | 低 / Low | ✅ 持久 / Durable | 額外費用 / Extra |
| EFS | 中 / Medium | ✅ 持久 / Durable | 額外費用 / Extra |
| S3 | 高 / High | ✅ 持久 / Durable | 額外費用 / Extra |

---

## 問題 41 / Question 41

**[題目 / Question]**
An RDS database in a single AZ needs to continue working on the same endpoint without manual intervention during an AZ outage. Which solution addresses this?
單一 AZ 的 RDS 資料庫需要在 AZ 中斷時自動繼續工作且端點不變，哪個解決方案符合？

**✅ 正確答案 / Correct Answer：Configure RDS Multi-AZ deployment with automatic failover**

**[中文詳解]**
**RDS Multi-AZ** 自動在不同 AZ 建立備用執行個體並同步複製資料。發生故障時自動容錯移轉，且**資料庫端點保持不變**，無需手動干預。

**[Multi-AZ vs 讀取副本 / Multi-AZ vs Read Replica]**

| 特性 / Feature | Multi-AZ | Read Replica |
|---|---|---|
| 主要目的 | 高可用性 / High availability | 讀取擴展 / Read scaling |
| 容錯移轉 | ✅ 自動 / Automatic | ❌ 需手動提升 |
| 端點變更 | ❌ 不變 / Same | ✅ 會變更 / Changes |
| 同步複製 | ✅ 是 / Yes | ❌ 非同步 / Async |

---

## 問題 42 / Question 42

**[題目 / Question]**
Compared to on-demand prices, what is the highest possible discount for spot instances?
與隨需價格相比，Spot 執行個體最高可享多少折扣？

**✅ 正確答案 / Correct Answer：90%**

**[EC2 最高折扣 / Maximum Discounts]**
- On-Demand：基準價格 / Baseline
- Reserved Instance：最高 **75%** 折扣
- Spot Instance：最高 **90%** 折扣（但可被中斷）

---

## 問題 43 / Question 43

**[題目 / Question]**
AWS owned IP-addresses are being used to carry out malicious attacks. Which is the correct solution?
AWS 所擁有的 IP 位址被用於惡意攻擊，正確的解決方案是？

**✅ 正確答案 / Correct Answer：Contact AWS Abuse Team（聯繫 AWS 濫用團隊）**

**[中文詳解]**
**AWS 濫用團隊**專門處理 AWS 資源被用於濫用行為的情況，包括垃圾郵件、DDoS 攻擊、惡意軟體傳播等。

---

## 問題 44 / Question 44

**[題目 / Question]**
Which is an INCORRECT statement about Scaling as a design principle of the Reliability pillar?
以下哪個關於可靠性支柱擴展的說法不正確？

**✅ 正確答案（不正確的說法）/ Correct Answer (Incorrect Statement)：**
"Fault tolerance is achieved by a **scale up** operation"
「容錯是透過**向上擴展**操作實現的」

**[水平擴展 vs 垂直擴展 / Scale Out vs Scale Up]**

| 擴展類型 / Type | 方式 / Method | 容錯能力 / Fault Tolerance |
|---|---|---|
| Scale Out（水平）| 增加更多執行個體 | ✅ 有（無單一故障點）|
| Scale Up（垂直）| 增加 CPU/RAM | ❌ 無（單一執行個體）|

---

## 問題 45 / Question 45

**[題目 / Question]**
Which are the storage services offered by AWS Cloud? (Select two)
哪兩個是 AWS 雲端提供的儲存服務？

**✅ 正確答案 / Correct Answers：**
1. Amazon S3（物件儲存 / Object Storage）
2. Amazon EFS（文件儲存 / File Storage）

**[AWS 儲存服務 / AWS Storage Services]**
- **S3**：物件儲存 / Object storage
- **EBS**：區塊儲存 / Block storage
- **EFS**：文件儲存 / File storage
- **Instance Store**：臨時區塊儲存 / Temporary block storage

---

## 問題 46 / Question 46

**[題目 / Question]**
A startup's CTO wants an estimate of the monthly AWS bill based on the AWS services they plan to use. Which AWS service would you suggest?
新創公司的 CTO 想根據計劃使用的服務估算每月 AWS 費用，推薦哪個服務？

**✅ 正確答案 / Correct Answer：AWS Pricing Calculator**

**[中文詳解]**
**AWS Pricing Calculator** 讓您在建構前探索 AWS 服務並建立成本估算，可模擬解決方案、探索定價點和計算方式，以及找到可用的執行個體類型和合約條款。

網址 / URL：https://calculator.aws/

---

## 問題 47 / Question 47

**[題目 / Question]**
According to AWS CAF, what tasks should a company perform to become more responsive to customer inquiries and feedback? (Select two)
根據 AWS CAF，公司應執行哪兩個任務以更快回應客戶需求？

**✅ 正確答案 / Correct Answers：**
1. Organize your teams around products and value streams（圍繞產品和價值流組織團隊）
2. Leverage agile methods to rapidly iterate and evolve（利用敏捷方法快速迭代和演進）

**[AWS CAF 六大視角 / AWS CAF 6 Perspectives]**
Business → People → Governance → Platform → Security → Operations

---

## 問題 48 / Question 48

**[題目 / Question]**
A company has server-bound software licenses that it wants to use on AWS. Which EC2 instance type would you recommend?
公司有伺服器綁定的軟體授權想在 AWS 上使用，推薦哪種 EC2 執行個體類型？

**✅ 正確答案 / Correct Answer：EC2 Dedicated Host（專用主機）**

**[Dedicated Host vs Dedicated Instance]**

| 特性 / Feature | Dedicated Host | Dedicated Instance |
|---|---|---|
| 實體伺服器控制 / Physical server control | ✅ 完整 / Full | ❌ 無 / None |
| 伺服器綁定授權 / Server-bound licenses | ✅ 支援 / Supported | ❌ 不支援 |
| 實體隔離 / Physical isolation | ✅ | ✅ |
| 插槽/核心可見性 / Socket/core visibility | ✅ | ❌ |

---

## 問題 49 / Question 49

**[題目 / Question]**
Under the AWS Shared Responsibility Model, which is a **shared** responsibility of both AWS and the customer?
在 AWS 共同責任模型下，哪項是 AWS 和客戶的**共同**責任？

**✅ 正確答案 / Correct Answer：Configuration Management（配置管理）**

**[中文詳解]**
**配置管理**是共同控制項目：AWS 負責維護其基礎設施設備的配置，而客戶負責配置自己的 Guest OS、資料庫和應用程式。

**[責任分工 / Responsibility Division]**

| 責任類型 / Type | AWS | 客戶 / Customer |
|---|---|---|
| 配置管理 / Config Management | 基礎設施設備 / Infrastructure devices | Guest OS、DB、應用程式 |
| 修補管理 / Patch Management | 基礎設施 / Infrastructure | Guest OS |
| 意識與培訓 / Awareness & Training | AWS 員工 / AWS employees | 客戶員工 / Customer employees |

---

## 問題 50 / Question 50

**[題目 / Question]**
A medical research startup wants to review HIPAA compliance and governance-related documents on AWS. Which AWS service can be used?
醫療研究新創公司想審查 AWS 上的 HIPAA 合規和治理相關文件，應使用哪個服務？

**✅ 正確答案 / Correct Answer：AWS Artifact**

**[中文詳解]**
**AWS Artifact** 是合規相關資訊的中央資源，提供隨需存取 AWS 安全和合規報告，包括 SOC 報告、PCI 報告，以及供 HIPAA 合規客戶使用的商業夥伴附件 (BAA)。這是一個免費的自助服務入口網站。

**[English Explanation]**
**AWS Artifact** provides on-demand access to AWS compliance reports (SOC, PCI) and select online agreements including the Business Associate Addendum (BAA) for HIPAA compliance. It's a no-cost, self-service portal.

---

## 問題 51 / Question 51

**[題目 / Question]**
Which expense areas would result in cost savings when moving to AWS Cloud? (Select two)
遷移到 AWS 雲端後，哪兩個支出領域可以節省成本？

**✅ 正確答案 / Correct Answers：**
1. Data center hardware infrastructure expenditure（資料中心硬體基礎設施支出）
2. Data center physical security expenditure（資料中心實體安全支出）

**[成本分析 / Cost Analysis]**

| 支出類型 / Expense | 遷移後變化 / After Migration |
|---|---|
| 資料中心硬體 / DC Hardware | ✅ **節省 / Saved** |
| 資料中心安全 / DC Security | ✅ **節省 / Saved** |
| SaaS 授權費 / SaaS License | ❌ 不變 / Same |
| 開發人員薪資 / Dev Salary | ❌ 不變 / Same |
| 專案管理薪資 / PM Salary | ❌ 不變 / Same |

---

## 問題 52 / Question 52

**[題目 / Question]**
What are the advantages AWS Cloud offers over traditional on-premises IT infrastructure? (Select two)
與傳統本地 IT 基礎設施相比，AWS 雲端的優勢是哪兩個？

**✅ 正確答案 / Correct Answers：**
1. Trade capital expense for variable expense（將資本支出換為可變支出）
2. Eliminate guessing on your infrastructure capacity needs（消除對基礎設施容量需求的猜測）

---

## 問題 53 / Question 53

**[題目 / Question]**
An intern provisioned a Linux-based On-Demand EC2 instance with per-second billing but terminated it within 30 seconds. What is the charge duration?
實習生使用按秒計費啟動了 Linux EC2 執行個體，但在 30 秒內終止，收費時長為多少？

**✅ 正確答案 / Correct Answer：60 seconds（60 秒）**

**[中文詳解]**
Linux 型 EC2 執行個體有**最少一分鐘**計費規定，即使在 30 秒內終止，仍會按 60 秒收費。

> ⚠️ 雖然 EC2 支援按秒計費，但最少計費時間為 1 分鐘（60 秒）

---

## 問題 54 / Question 54

**[題目 / Question]**
Which type of cloud computing does Amazon EC2 represent?
Amazon EC2 代表哪種類型的雲端運算？

**✅ 正確答案 / Correct Answer：Infrastructure as a Service (IaaS)（基礎設施即服務）**

**[雲端服務類型 / Cloud Service Types]**

| 類型 / Type | 說明 / Description | AWS 範例 |
|---|---|---|
| **IaaS** | **基本構建塊，最高控制權** | **EC2, VPC, EBS** |
| PaaS | 無需管理底層基礎設施 | Elastic Beanstalk |
| SaaS | 完整產品，由服務提供者運行 | Amazon Rekognition |

---

## 問題 55 / Question 55

**[題目 / Question]**
AWS Web Application Firewall (WAF) offers protection from common web exploits at which layer?
AWS WAF 在哪一層提供對常見 Web 漏洞的防護？

**✅ 正確答案 / Correct Answer：Layer 7（第 7 層 — 應用層）**

**[OSI 模型與 AWS 安全 / OSI Model & AWS Security]**

| OSI 層 / Layer | 名稱 / Name | AWS 服務 |
|---|---|---|
| 3 | 網路層 / Network | AWS Shield |
| 4 | 傳輸層 / Transport | AWS Shield |
| **7** | **應用層 / Application** | **AWS WAF** |

---

## 問題 56 / Question 56

**[題目 / Question]**
Which tool/service will help you access AWS services using programming language-specific APIs?
哪個工具/服務可讓您使用程式語言特定的 API 存取 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Software Developer Kit (SDK)**

**[AWS 存取方式比較 / AWS Access Methods]**

| 工具 / Tool | 方式 / Method | 適用場景 / Use Case |
|---|---|---|
| **AWS SDK** | **語言特定 API / Language-specific APIs** | **程式碼整合 / Code integration** |
| AWS CLI | 命令列 / Command line | 腳本自動化 / Script automation |
| AWS Console | Web 瀏覽器 / Web browser | 視覺化管理 / Visual management |

---

## 問題 57 / Question 57

**[題目 / Question]**
Which of the following is a serverless AWS service?
以下哪個是無伺服器 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Lambda**

**[無伺服器服務 / Serverless Services]**
- ✅ AWS Lambda
- ✅ Amazon S3
- ✅ Amazon DynamoDB
- ✅ Amazon Aurora Serverless
- ❌ EC2（需管理伺服器）
- ❌ Elastic Beanstalk（配置伺服器）
- ❌ Amazon EMR（配置 EC2）

---

## 問題 58 / Question 58

**[題目 / Question]**
Which Amazon S3 storage class takes the most time to retrieve data (first byte latency)?
哪個 Amazon S3 儲存類別的資料取回時間最長？

**✅ 正確答案 / Correct Answer：Amazon S3 Glacier Deep Archive**

**[S3 儲存類別取回時間 / S3 Storage Class Retrieval Times]**

| 儲存類別 / Storage Class | 取回時間 / Retrieval Time | 使用場景 |
|---|---|---|
| S3 Standard | 毫秒 / Milliseconds | 頻繁存取 / Frequent access |
| S3 Standard-IA | 毫秒 / Milliseconds | 不頻繁但需快速 |
| S3 Intelligent-Tiering | 毫秒 / Milliseconds | 存取模式不確定 |
| S3 Glacier Instant Retrieval | 毫秒 / Milliseconds | 偶爾存取 |
| S3 Glacier Flexible Retrieval | 分鐘到小時 / Minutes to hours | 備份/DR |
| **S3 Glacier Deep Archive** | **12-48 小時 / 12-48 hours** | **長期存檔 / Long-term archive** |

---

## 問題 59 / Question 59

**[題目 / Question]**
Which are common stakeholder roles for the AWS CAF **platform** perspective? (Select two)
哪兩個是 AWS CAF **平台**視角的常見利害關係人角色？

**✅ 正確答案 / Correct Answers：**
1. Engineer（工程師）
2. Chief Technology Officer (CTO)（技術長）

**[AWS CAF 各視角利害關係人 / CAF Perspective Stakeholders]**

| 視角 / Perspective | 主要利害關係人 / Key Stakeholders |
|---|---|
| Business（業務） | CEO, CFO, COO, CIO |
| People（人員） | CHRO, 各部門主管 |
| Governance（治理） | CIO, Program Managers |
| **Platform（平台）** | **CTO, 架構師, 工程師** |
| Security（安全） | CISO, 安全架構師 |
| Operations（運營） | IT 運營經理 |

---

## 問題 60 / Question 60

**[題目 / Question]**
A DevOps team wants to debug performance issues for its serverless application built using a microservices architecture. Which AWS service would you recommend?
DevOps 團隊想偵錯微服務架構無伺服器應用程式的效能問題，推薦哪個服務？

**✅ 正確答案 / Correct Answer：AWS X-Ray**

**[中文詳解]**
**AWS X-Ray** 可分析和偵錯無伺服器及分散式應用程式，幫助您了解應用程式和底層服務的執行情況，識別和排除效能問題及錯誤的根本原因。

**[English Explanation]**
**AWS X-Ray** analyzes and debugs serverless and distributed applications, helping you understand how your application and underlying services perform to identify root causes of performance issues.

---

## 問題 61 / Question 61

**[題目 / Question]**
Which AWS services support reservations to optimize costs? (Select three)
哪三個 AWS 服務支援預留以優化成本？

**✅ 正確答案 / Correct Answers：**
1. Amazon EC2（預留執行個體）
2. Amazon DynamoDB（預留容量）
3. Amazon RDS（預留執行個體）

**[支援預留的服務 / Services with Reservation]**
- ✅ Amazon EC2 Reserved Instances
- ✅ Amazon DynamoDB Reserved Capacity
- ✅ Amazon RDS Reserved Instances
- ✅ Amazon ElastiCache Reserved Nodes
- ✅ Amazon Redshift Reserved Nodes
- ❌ Lambda（按使用量 / Pay per use）
- ❌ S3（按使用量 / Pay per use）

---

## 問題 62 / Question 62

**[題目 / Question]**
A batch analytics application needs storage that can be accessed by hundreds of EC2 instances **simultaneously** to **append data** to existing files. Which service would you suggest?
批次分析應用程式需要數百個 EC2 執行個體**同時**存取的儲存，可**附加資料**到現有文件，推薦哪個服務？

**✅ 正確答案 / Correct Answer：Amazon EFS**

**[為什麼選 EFS / Why EFS]**
- ✅ 支援數千個 EC2 執行個體同時存取
- ✅ 提供文件系統介面（支援附加操作）
- ✅ 使用 NFS 協議
- ✅ 自動彈性擴展到 PB 級

**[為什麼其他選項不符 / Why Others Don't Qualify]**
- EBS：不支援多執行個體同時存取
- Instance Store：不支援多執行個體同時存取
- S3：物件儲存，不支援文件附加操作

---

## 問題 63 / Question 63

**[題目 / Question]**
A company needs a managed AWS NoSQL database service to support **active-active configuration** in both East and West US AWS regions. Which database service is the right fit?
公司需要支援美國東西部兩區**主動-主動配置**的 NoSQL 資料庫服務，哪個服務最合適？

**✅ 正確答案 / Correct Answer：Amazon DynamoDB with global tables**

**[中文詳解]**
**DynamoDB 全球表格**自動跨多個 AWS 區域複製資料，支援**主動-主動跨區域配置**，全球分散式應用程式可在選定區域中本地存取資料，達到個位數毫秒的讀寫效能。

**[English Explanation]**
**DynamoDB global tables** replicate data across AWS Regions and support **active-active cross-region configuration**, enabling globally distributed applications to access data locally with single-digit millisecond read/write performance.

---

## 問題 64 / Question 64

**[題目 / Question]**
A multi-national corporation wants expert professional advice on migrating to AWS and managing applications on AWS Cloud. Which entity would you recommend?
跨國公司想獲得遷移到 AWS 和管理 AWS 應用程式的專業建議，推薦哪個實體？

**✅ 正確答案 / Correct Answer：APN Consulting Partner（APN 諮詢合作夥伴）**

**[APN 合作夥伴類型 / APN Partner Types]**

| 類型 / Type | 說明 / Description |
|---|---|
| **APN Consulting Partners** | **專業服務公司，協助設計、建構、遷移和管理 AWS 工作負載** |
| APN Technology Partners | 提供硬體、連接服務或軟體解決方案 |

---

## 問題 65 / Question 65

**[題目 / Question]**
A project has data that is accessed **less frequently** but needs **rapid access when required**. Which S3 storage class is the MOST cost-effective?
資料存取頻率較低但需要快速存取時，哪個 S3 儲存類別最具成本效益？

**✅ 正確答案 / Correct Answer：Amazon S3 Standard-Infrequent Access (S3 Standard-IA)**

**[中文詳解]**
**S3 Standard-IA** 適合存取頻率較低但需要快速存取的資料，提供高耐久性、高吞吐量和低延遲，每 GB 儲存費用低，但有每 GB 取回費用。非常適合長期儲存、備份和災難復原。

**[S3 儲存類別選擇指南 / S3 Storage Class Selection Guide]**

| 使用場景 / Use Case | 推薦類別 / Recommended Class |
|---|---|
| 頻繁存取 / Frequent access | S3 Standard |
| 不確定存取模式 / Unknown pattern | S3 Intelligent-Tiering |
| **不頻繁但需快速 / Infrequent + rapid** | **S3 Standard-IA ✅** |
| 長期存檔，偶爾 / Archive, occasional | S3 Glacier Flexible Retrieval |
| 長期存檔，極少 / Archive, rare | S3 Glacier Deep Archive |

---

## 📊 考題領域統計 / Domain Summary

| 領域 / Domain | 題數 / Questions | 百分比 / % |
|---|---|---|
| Technology（技術）| 22 | 33.8% |
| Security and Compliance（安全與合規）| 18 | 27.7% |
| Cloud Concepts（雲端概念）| 16 | 24.6% |
| Billing and Pricing（計費與定價）| 9 | 13.8% |

---

## 🎯 必考重點整理 / Key Exam Points

### CloudWatch vs CloudTrail vs Config
- **CloudWatch** → 效能監控、告警
- **CloudTrail** → 帳戶活動審計
- **Config** → 資源配置合規

### VPC Gateway Endpoint
只支援 **S3** 和 **DynamoDB**

### EC2 定價（成本由低到高）
Spot < Reserved < On-Demand < Dedicated Host

### S3 儲存類別（取回時間由短到長）
Standard ≈ Standard-IA ≈ Intelligent-Tiering < Glacier Flexible < **Glacier Deep Archive**

### AWS Support 方案
- Trusted Advisor 完整存取：Business、Enterprise On-Ramp、Enterprise
- 第三方軟體支援：Business、Enterprise
- TAM：Enterprise On-Ramp（共享）、Enterprise（專屬）

### 加密方式
- 傳送前加密 → Client-side encryption（AWS Encryption SDK）
- 預設加密啟用 → CloudTrail Logs

### 共同責任模型關鍵記憶
- **AWS**：實體安全、硬體維護、底層網路
- **客戶**：Guest OS 修補、應用程式配置、IAM 管理
- **共同**：配置管理、修補管理、意識培訓
