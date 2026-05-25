# AWS Cloud Practitioner 考題中英對照詳解（第二回）
# AWS Cloud Practitioner Exam Q&A — Bilingual Study Guide (Set 2)

---

## 問題 1 / Question 1

**[題目 / Question]**
Which AWS service can be used to store, manage, and deploy Docker container images?
哪個 AWS 服務可用於儲存、管理和部署 Docker 容器映像？

**✅ 正確答案 / Correct Answer：Amazon Elastic Container Registry (Amazon ECR)**

**[中文詳解]**
**Amazon ECR** 是全托管的容器映像倉庫，用於儲存、管理和部署 Docker 容器映像，無需自行管理容器倉庫。您可以從 ECR 拉取映像並在 Amazon ECS 上運行。

**[English Explanation]**
**Amazon ECR** is a fully managed container image registry to store, manage, and deploy Docker container images. You pull images from ECR and run them on Amazon ECS.

**[容器相關服務比較 / Container Services Comparison]**

| 服務 / Service | 功能 / Function |
|---|---|
| **Amazon ECR** | **儲存/管理容器映像 / Store & manage container images** |
| Amazon ECS | 運行/管理 Docker 容器 / Run & manage Docker containers |
| Amazon EKS | 管理 Kubernetes 容器 / Managed Kubernetes |
| AWS Fargate | 無伺服器容器運算 / Serverless container compute |

---

## 問題 2 / Question 2

**[題目 / Question]**
An e-commerce company wants to assess its EC2 instances for vulnerabilities and deviations from AWS best practices. Which AWS service can facilitate this?
電商公司想評估 EC2 執行個體的漏洞和 AWS 最佳實踐偏差，哪個服務可協助？

**✅ 正確答案 / Correct Answer：Amazon Inspector**

**[中文詳解]**
**Amazon Inspector** 是自動化安全評估服務，自動評估應用程式的暴露情況、漏洞和與最佳實踐的偏差，生成按嚴重性排列的安全發現清單。

**[English Explanation]**
**Amazon Inspector** automatically assesses applications for exposure, vulnerabilities, and deviations from best practices, producing a detailed list of security findings prioritized by severity.

**[混淆服務說明 / Distractor Clarification]**

| 服務 / Service | 功能 / Function |
|---|---|
| **Amazon Inspector** | **EC2 漏洞評估 / EC2 vulnerability assessment** ✅ |
| AWS Secrets Manager | 管理密鑰 / Manage secrets |
| AWS CloudHSM | 硬體安全模組 / Hardware Security Module |
| AWS Trusted Advisor | 最佳實踐建議 / Best practice recommendations |

---

## 問題 3 / Question 3

**[題目 / Question]**
A social media company wants to protect its web application from SQL injection and cross-site scripting. Which AWS service can be used?
社群媒體公司想保護 Web 應用程式免受 SQL 注入和跨站腳本攻擊，應使用哪個服務？

**✅ 正確答案 / Correct Answer：AWS Web Application Firewall (AWS WAF)**

**[中文詳解]**
**AWS WAF** 是 Web 應用程式防火牆，可建立安全規則來封鎖 SQL 注入和跨站腳本 (XSS) 等常見攻擊模式。也可使用基於速率的規則緩解 Web 層 DDoS 攻擊。

**[English Explanation]**
**AWS WAF** is a web application firewall that lets you create security rules to block common attack patterns like **SQL injection** and **cross-site scripting (XSS)**, and rate-based rules to mitigate Web layer DDoS attacks.

**[WAF 運作原理]**
- SQL 注入：攻擊者向 SQL 伺服器注入惡意代碼以竊取資料
- XSS 跨站腳本：在網站注入惡意代碼，在用戶瀏覽器執行

---

## 問題 4 / Question 4

**[題目 / Question]**
AWS Compute Optimizer delivers recommendations for which of the following AWS resources? (Select two)
AWS Compute Optimizer 為哪兩組 AWS 資源提供優化建議？

**✅ 正確答案 / Correct Answers：**
1. Amazon EC2 instances, Amazon EC2 Auto Scaling groups
2. Amazon EBS, AWS Lambda functions

**[Compute Optimizer 支援的資源 / Supported Resources]**

| 資源 / Resource | 說明 / Details |
|---|---|
| EC2 執行個體 | 推薦最多 3 種替代類型 |
| EC2 Auto Scaling groups | 固定群組大小 (desired=min=max) |
| **Amazon EBS** | gp3 的 IOPS/吞吐量；io1/io2 的 IOPS |
| **AWS Lambda** | 過度佈建的記憶體；CPU 密集型函數 |

> ⚠️ **不支援**：Amazon S3、Amazon EFS

---

## 問題 5 / Question 5

**[題目 / Question]**
Which of the following AWS services are global in scope? (Select two)
哪兩個 AWS 服務是全球範圍的？

**✅ 正確答案 / Correct Answers：**
1. Amazon CloudFront
2. AWS Identity and Access Management (AWS IAM)

**[全球 vs 區域服務 / Global vs Regional Services]**

| 全球服務 / Global | 區域服務 / Regional |
|---|---|
| **AWS IAM** | Amazon EC2 |
| **Amazon CloudFront** | Amazon RDS |
| Amazon Route 53 | Amazon S3（命名空間全球，但儲存桶是區域）|
| AWS WAF | Amazon VPC |

> ⚠️ **Amazon S3 考試提醒**：S3 遵循全球命名空間，但儲存桶是**區域性**的

---

## 問題 6 / Question 6

**[題目 / Question]**
Which of the following AWS services are always free to use? (Select two)
哪兩個 AWS 服務永遠免費使用？

**✅ 正確答案 / Correct Answers：**
1. AWS Identity and Access Management (AWS IAM)
2. AWS Auto Scaling

**[永遠免費的 AWS 服務 / Always-Free AWS Services]**

| 服務 / Service | 費用 / Cost | 說明 |
|---|---|---|
| **AWS IAM** | **免費 / Free** | AWS 帳戶功能，無額外費用 |
| **AWS Auto Scaling** | **免費 / Free** | 僅支付底層 EC2 和 CloudWatch 費用 |
| Amazon EC2 | 收費 | 按使用量計費 |
| Amazon S3 | 收費 | 按儲存類別計費 |
| Amazon DynamoDB | 收費 | 按讀寫和儲存計費 |

---

## 問題 7 / Question 7

**[題目 / Question]**
An IT company wants to run a log backup process every Monday at 2 AM (runtime ~5 minutes). Which AWS services would you recommend for a serverless solution? (Select two)
IT 公司想每週一凌晨 2 點執行日誌備份程序（約 5 分鐘），推薦哪兩個無伺服器服務？

**✅ 正確答案 / Correct Answers：**
1. AWS Lambda
2. Amazon EventBridge

**[無伺服器排程方案 / Serverless Scheduling Solution]**
```
Amazon EventBridge Scheduler（排程觸發）
        ↓
AWS Lambda（執行備份程序，最長 15 分鐘）
```

**[為什麼選這兩個 / Why These Two]**
- **EventBridge**：無伺服器任務排程器，可設定 cron 排程觸發
- **Lambda**：無伺服器執行代碼，最長執行時間 15 分鐘，符合 5 分鐘需求

> ⚠️ EC2 非無伺服器；Step Functions 無法排程執行；Systems Manager 無排程執行功能

---

## 問題 8 / Question 8

**[題目 / Question]**
Which AWS service helps with global application availability and performance using the AWS global network?
哪個 AWS 服務利用 AWS 全球網路提升全球應用程式的可用性和效能？

**✅ 正確答案 / Correct Answer：AWS Global Accelerator**

**[中文詳解]**
**AWS Global Accelerator** 提供靜態 IP 位址作為應用程式端點的固定入口點，使用 AWS 全球網路優化流量路徑，可提升效能最多 60%。適合非 HTTP 用例（遊戲 UDP、IoT MQTT、VoIP）以及需要靜態 IP 或快速區域容錯移轉的 HTTP 用例。

**[Global Accelerator vs CloudFront 比較 / Key Comparison]**

| 特性 / Feature | AWS Global Accelerator | Amazon CloudFront |
|---|---|---|
| 主要功能 | 網路層效能優化 / Network performance | 內容交付網路 CDN |
| 使用網路 | AWS 全球網路 | AWS 邊緣節點 |
| IP 位址 | 靜態 IP / Static IPs | 動態 / Dynamic |
| 適用協議 | TCP, UDP | HTTP/HTTPS |
| 快取 | ❌ 無 | ✅ 有 |

---

## 問題 9 / Question 9

**[題目 / Question]**
As per the AWS Shared Responsibility Model, which is a responsibility of the customer from a security and compliance point of view?
根據 AWS 共同責任模型，以下哪項是客戶的安全與合規責任？

**✅ 正確答案 / Correct Answer：Managing patches of the guest OS on Amazon EC2（管理 EC2 Guest OS 的修補程式）**

**[共同責任模型 / Shared Responsibility Model]**

| AWS 負責（雲端安全）| 客戶負責（雲端中的安全）|
|---|---|
| AZ 基礎設施管理 | **Guest OS 修補管理** ✅ |
| AWS 全球基礎設施配置管理 | 應用程式軟體 |
| 修補 AWS 基礎設施缺陷 | 安全群組配置 |
| 實體設施安全 | 資料加密 |

---

## 問題 10 / Question 10

**[題目 / Question]**
Which AWS support plan provides access to a **designated** Technical Account Manager (TAM)?
哪個 AWS 支援方案提供**專屬** TAM 技術客戶經理？

**✅ 正確答案 / Correct Answer：AWS Enterprise Support**

**[TAM 支援比較 / TAM Support Comparison]**

| 方案 / Plan | TAM 類型 |
|---|---|
| Basic | ❌ 無 |
| Developer | ❌ 無 |
| Business | ❌ 無 |
| Enterprise On-Ramp | ✅ 共享 TAM 池 / Pool of TAMs |
| **Enterprise** | **✅ 專屬 TAM / Designated TAM** |

---

## 問題 11 / Question 11

**[題目 / Question]**
Which AWS compute service provides the EASIEST way to access resizable compute capacity with **per-second billing** and **access to the underlying OS**?
哪個 AWS 運算服務最容易存取可調整的運算容量，支援**按秒計費**且可**存取底層 OS**？

**✅ 正確答案 / Correct Answer：Amazon EC2**

**[運算服務比較 / Compute Services Comparison]**

| 服務 / Service | 按秒計費 | 存取 OS | 管理複雜度 |
|---|---|---|---|
| **Amazon EC2** | **✅** | **✅** | 低 / Low |
| Amazon Lightsail | ❌（月費）| ✅ | 最低 |
| Amazon ECS | ✅ | 間接 / Indirect | 高 / High |
| AWS Lambda | ✅（按請求）| ❌ 無伺服器 | 最低 |

---

## 問題 12 / Question 12

**[題目 / Question]**
Which service gives a **personalized view** of the status of AWS services that are part of **your** Cloud architecture?
哪個服務提供針對**您的** AWS 架構中服務狀態的**個人化視圖**？

**✅ 正確答案 / Correct Answer：AWS Health - Your Account Health Dashboard（帳戶健康儀表板）**

**[兩個 AWS Health 儀表板比較 / Health Dashboard Comparison]**

| 儀表板 / Dashboard | 視圖範圍 / Scope | 用途 |
|---|---|---|
| **Account Health Dashboard（帳戶健康）** | **您的帳戶 / Your account** | **個人化告警與補救指導** |
| Service Health Dashboard（服務健康）| 所有 AWS / All AWS | AWS 所有服務的整體狀態 |

> 網址：帳戶健康 → phd.aws.amazon.com | 服務健康 → health.aws.amazon.com/health/status

---

## 問題 13 / Question 13

**[題目 / Question]**
A fleet of EC2 instances **across different AZs** needs to access, edit, and share file-based data stored centrally. Which AWS service would you recommend?
**跨不同 AZ** 的 EC2 執行個體需要存取、編輯和共享集中儲存的文件資料，推薦哪個服務？

**✅ 正確答案 / Correct Answer：Amazon Elastic File System (Amazon EFS)**

**[中文詳解]**
**Amazon EFS** 提供全托管的彈性 NFS 文件系統，可同時為數千個 EC2 執行個體提供大規模並行共享存取，橫跨多個 AZ，自動彈性擴展到 PB 級。

**[儲存服務選擇 / Storage Selection Guide]**

| 場景 / Scenario | 推薦服務 |
|---|---|
| **多 AZ 執行個體共享文件** | **Amazon EFS** ✅ |
| 單一執行個體高效能區塊儲存 | Amazon EBS |
| 臨時高速 I/O，容錯架構 | EC2 Instance Store |
| 物件儲存 | Amazon S3 |

---

## 問題 14 / Question 14

**[題目 / Question]**
Which of the following AWS services comes under the **Software as a Service (SaaS)** Cloud Computing Type?
以下哪個 AWS 服務屬於 **SaaS** 雲端運算類型？

**✅ 正確答案 / Correct Answer：Amazon Rekognition**

**[雲端服務類型 / Cloud Service Types]**

| 類型 / Type | 說明 / Description | AWS 範例 |
|---|---|---|
| **IaaS** | 基礎設施，最高控制權 | EC2, VPC, EBS |
| **PaaS** | 平台，無需管理底層基礎設施 | Elastic Beanstalk, Heroku |
| **SaaS** | 完整產品，由提供者運行管理 | **Amazon Rekognition**, Gmail, Dropbox |

**[Amazon Rekognition 功能]**
識別物件、人物、文字、場景、活動；偵測不當內容；臉部分析和搜索

---

## 問題 15 / Question 15

**[題目 / Question]**
As per the AWS Shared Responsibility Model, which is a responsibility of AWS from a security and compliance point of view?
根據 AWS 共同責任模型，以下哪項是 AWS 的安全與合規責任？

**✅ 正確答案 / Correct Answer：Edge Location Management（邊緣節點管理）**

**[AWS 全球基礎設施責任 / AWS Global Infrastructure Responsibility]**
AWS 負責「雲端安全」，涵蓋：
- **Regions（區域）**
- **Availability Zones（可用區域）**
- **Edge Locations（邊緣節點）**

**[客戶責任 / Customer Responsibilities]**
- 客戶資料 / Customer data
- 身份和存取管理 / Identity & Access Management
- 伺服器端加密 (SSE) / Server-side encryption

---

## 問題 16 / Question 16

**[題目 / Question]**
Due to regulatory compliance, an organization needs to use a **hardware device** for data encryption operations in the cloud. Which AWS service can meet this?
由於法規合規要求，組織需要使用**硬體設備**進行雲端資料加密，哪個服務符合？

**✅ 正確答案 / Correct Answer：AWS CloudHSM**

**[中文詳解]**
**AWS CloudHSM** 是雲端型**硬體安全模組 (HSM)**，使用 FIPS 140-2 Level 3 驗證的 HSM 來管理加密金鑰，是真正的硬體級加密設備。

**[加密服務比較 / Encryption Services]**

| 服務 / Service | 類型 / Type | 硬體設備 |
|---|---|---|
| **AWS CloudHSM** | **硬體 HSM / Hardware HSM** | **✅ 是** |
| AWS KMS | 軟體式金鑰管理 / Software KMS | ❌ 否（使用共享 HSM）|
| AWS Secrets Manager | 密鑰輪換 / Secret rotation | ❌ 否 |

> **關鍵區別**：CloudHSM 是您**專屬**的硬體；KMS 使用 AWS **共享**的 HSM

---

## 問題 17 / Question 17

**[題目 / Question]**
Which of the following solutions can connect your on-premises network with AWS Cloud? (Select two)
哪兩個方案可將本地網路與 AWS 雲端連接？

**✅ 正確答案 / Correct Answers：**
1. AWS Direct Connect
2. AWS Virtual Private Network (VPN)

**[連接方案比較 / Connection Options]**

| 方案 / Solution | 連接類型 | 公共網路 | 建立時間 |
|---|---|---|---|
| **AWS Direct Connect** | 專用實體線路 | ❌ 繞過 | 1+ 個月 |
| **AWS VPN** | VPN 加密隧道 | ✅ 經過 | 分鐘 |
| Internet Gateway | 網際網路 | ✅ | 即時 |
| Amazon VPC | 虛擬私有雲（不連接本地）| N/A | N/A |

---

## 問題 18 / Question 18

**[題目 / Question]**
Access Key ID and Secret Access Key are tied to which AWS IAM entity?
存取金鑰 ID 和私密存取金鑰與哪個 AWS IAM 實體相關聯？

**✅ 正確答案 / Correct Answer：IAM User（IAM 使用者）**

**[IAM 實體與憑證 / IAM Entities & Credentials]**

| IAM 實體 / Entity | 存取金鑰 | 用戶名/密碼 | 說明 |
|---|---|---|---|
| **IAM User** | **✅** | **✅** | 長期憑證 |
| IAM Role | ❌（使用臨時憑證）| ❌ | 可被任何人擔任 |
| IAM Group | ❌ | ❌ | 用戶集合，管理權限 |
| IAM Policy | ❌ | ❌ | 定義權限的物件 |

---

## 問題 19 / Question 19

**[題目 / Question]**
Which of the following are examples of **Horizontal Scalability (Elasticity)**? (Select two)
以下哪兩個是**水平擴展（彈性）**的例子？

**✅ 正確答案 / Correct Answers：**
1. Elastic Load Balancing (ELB)
2. Read Replicas in Amazon RDS

**[水平 vs 垂直擴展 / Horizontal vs Vertical Scaling]**

| 類型 / Type | 方式 / Method | 範例 / Examples |
|---|---|---|
| **水平擴展 / Horizontal (Scale Out)** | 增加更多執行個體 | **ELB, RDS Read Replicas, Auto Scaling** |
| 垂直擴展 / Vertical (Scale Up) | 增加單一節點的 CPU/RAM | 更大的 CPU、更高的 EC2 類型、更高的 DB 配置 |

---

## 問題 20 / Question 20

**[題目 / Question]**
Which of the following statements is **INCORRECT** about AWS Auto Scaling?
以下哪個關於 AWS Auto Scaling 的說法**不正確**？

**✅ 正確答案（不正確的說法）/ Correct Answer (Incorrect Statement)：**
"You can automatically deploy AWS Shield when a DDoS attack is detected"
「偵測到 DDoS 攻擊時可自動部署 AWS Shield」

**[中文詳解]**
AWS Auto Scaling 在 DDoS 攻擊時可快速擴展資源，但**無法自動部署 AWS Shield 服務**。

**[Auto Scaling 可以做的 / What Auto Scaling CAN Do]**
- ✅ 按需擴增/縮減 EC2 執行個體
- ✅ 自動移除不健康的執行個體
- ✅ 自動將新執行個體注冊到負載平衡器

---

## 問題 21 / Question 21

**[題目 / Question]**
Multi-AZ deployment is an example of which of the following?
Multi-AZ 部署是以下哪個的範例？

**✅ 正確答案 / Correct Answer：High Availability（高可用性）**

**[雲端設計概念比較 / Cloud Design Concepts]**

| 概念 / Concept | 定義 / Definition | 範例 |
|---|---|---|
| **High Availability（高可用性）** | **在降級的同時保持可用 / Remain available despite degradation** | **Multi-AZ 部署** |
| Scale Out（水平擴展）| 增加更多執行個體 | Auto Scaling Group |
| Scale Up（垂直擴展）| 增加單節點資源 | 調整 EC2 類型 |
| Performance Efficiency | 有效使用運算資源 | 選擇正確的執行個體類型 |

---

## 問題 22 / Question 22

**[題目 / Question]**
Which of the following use-cases is **NOT** supported by Amazon Rekognition?
以下哪個使用案例**不**受 Amazon Rekognition 支援？

**✅ 正確答案 / Correct Answer：Quickly resize photos to create thumbnails（快速調整照片大小以建立縮圖）**

**[Amazon Rekognition 支援的功能 / Supported Features]**
- ✅ 識別圖片/視訊中的物件、人物、文字、場景、活動
- ✅ 偵測不當內容
- ✅ 臉部分析、臉部比較、人物識別
- ✅ 圖片中偵測文字

**[不支援 / NOT Supported]**
- ❌ 調整圖片大小（需使用 Amazon S3 + Lambda 或其他影像處理服務）

---

## 問題 23 / Question 23

**[題目 / Question]**
An organization wants to identify the right AWS services to build solutions on AWS Cloud. Which options would help? (Select two)
組織想找出正確的 AWS 服務來建構解決方案，哪兩個選項有幫助？

**✅ 正確答案 / Correct Answers：**
1. AWS Service Catalog（AWS 服務目錄）
2. AWS Partner Network (APN)

**[中文詳解]**
- **AWS Service Catalog**：讓組織建立和管理 AWS 上批准使用的 IT 服務目錄（包括 VM 映像、伺服器、軟體、資料庫到完整的多層應用程式架構）
- **AWS Partner Network (APN)**：全球合作夥伴計畫，諮詢合作夥伴可協助識別適合的 AWS 服務並建構解決方案

---

## 問題 24 / Question 24

**[題目 / Question]**
Which of the following statements are true about AWS Lambda? (Select two)
以下哪兩個關於 AWS Lambda 的說法正確？

**✅ 正確答案 / Correct Answers：**
1. AWS Lambda lets you run code without provisioning or managing servers
2. You pay for the compute time you consume for AWS Lambda

**[AWS Lambda 關鍵特性 / Key Characteristics]**

| 特性 / Feature | 說明 / Details |
|---|---|
| 無伺服器 / Serverless | ✅ 無需佈建或管理伺服器 |
| 計費方式 / Billing | ✅ 按請求數量和計算時間收費 |
| OS 存取 / OS Access | ❌ 無法存取底層 OS |
| 執行時間 / Max Duration | ⏱️ 最長 15 分鐘 |
| 資料庫安裝 | ❌ 無法安裝資料庫 |
| 容器編排 | ❌ 無法編排 Docker 容器（用 ECS）|

---

## 問題 25 / Question 25

**[題目 / Question]**
Which AWS service can provision resources to run big data workloads on **Hadoop clusters**?
哪個 AWS 服務可佈建資源以在 **Hadoop 叢集**上執行大數據工作負載？

**✅ 正確答案 / Correct Answer：Amazon EMR**

**[中文詳解]**
**Amazon EMR** 是業界領先的雲端大數據平台，使用 Hadoop、Apache Spark、Hive、HBase、Flink、Presto 等開源工具處理海量資料，可佈建資源在 Hadoop 叢集上執行大數據工作負載。

**[大數據/批次服務比較 / Big Data Services]**

| 服務 / Service | 功能 / Function |
|---|---|
| **Amazon EMR** | **Hadoop 叢集大數據 / Hadoop cluster big data** |
| AWS Batch | 批次運算工作規劃和排程 |
| AWS Step Functions | 協調多個 AWS 服務的無伺服器工作流程 |
| Amazon EC2 | 一般虛擬伺服器 |

> **考試提醒**：Step Functions 協調服務，不佈建資源；Batch 佈建運算資源執行批次工作

---

## 問題 26 / Question 26

**[題目 / Question]**
Which AWS service enables users to find, buy, and immediately start using software solutions in their AWS environment?
哪個 AWS 服務讓使用者能在 AWS 環境中尋找、購買並立即開始使用軟體解決方案？

**✅ 正確答案 / Correct Answer：AWS Marketplace**

**[中文詳解]**
**AWS Marketplace** 是數位目錄，提供數千個獨立軟體供應商的軟體清單，涵蓋安全、網路、儲存、ML、IoT、BI、資料庫、DevOps 等類別。用戶可作為購買者或銷售者，或兩者兼具。

**[English Explanation]**
**AWS Marketplace** is a digital catalog with thousands of software listings from independent software vendors, allowing users to find, test, buy, and deploy software that runs on AWS.

---

## 問題 27 / Question 27

**[題目 / Question]**
Which AWS technology/service helps you scale resources to match supply with demand while keeping the solution cost-effective?
哪個 AWS 技術/服務可在保持成本效益的同時，調整資源以匹配供需？

**✅ 正確答案 / Correct Answer：AWS Auto Scaling**

**[中文詳解]**
**AWS Auto Scaling** 監控應用程式並自動調整容量，以最低成本維持穩定可預測的效能。支援 EC2 執行個體、Spot Fleets、ECS 任務、DynamoDB 表格和索引、Aurora 副本等多種資源。

**[擴展 vs 其他服務 / Auto Scaling vs Others]**

| 服務 / Service | 功能 / Function |
|---|---|
| **AWS Auto Scaling** | **自動調整容量以匹配需求 / Auto-scale capacity** |
| Cost Explorer | 視覺化成本 / Visualize costs |
| Systems Manager | 基礎設施可見性和自動化 |
| CloudFormation | 基礎設施即代碼 / IaC |

---

## 問題 28 / Question 28

**[題目 / Question]**
Which tool will help you review workloads against AWS best practices for cost optimization, security, and performance, and obtain advice?
哪個工具可根據 AWS 最佳實踐審查工作負載並獲得建議？

**✅ 正確答案 / Correct Answer：AWS Trusted Advisor**

**[Trusted Advisor 五大檢查類別 / Five Check Categories]**
1. 💰 Cost Optimization（成本優化）
2. 🔒 Security（安全）
3. ⚡ Performance（效能）
4. 🔧 Fault Tolerance（容錯）
5. 📊 Service Limits（服務限制）

**[考試提醒 / Exam Tip]**
- Trusted Advisor → AWS 最佳實踐建議
- Cost Explorer → 視覺化成本趨勢
- CloudWatch → 資源效能監控
- Inspector → EC2 漏洞評估

---

## 問題 29 / Question 29

**[題目 / Question]**
What is the **primary benefit** of deploying an Amazon RDS Multi-AZ database with one standby?
部署具有一個備用的 Amazon RDS Multi-AZ 資料庫的**主要優勢**是什麼？

**✅ 正確答案 / Correct Answer：Amazon RDS Multi-AZ enhances database availability（提高資料庫可用性）**

**[RDS 部署模式比較 / RDS Deployment Modes]**

| 部署模式 | 主要目的 | 特點 |
|---|---|---|
| **Multi-AZ（單備用）** | **高可用性 / High Availability** | 自動容錯移轉，端點不變 |
| Read Replicas | 讀取擴展 / Read scaling | 提升讀取效能，可手動提升 |
| Multi-Region | 區域容錯 / Regional DR | 跨區域保護 |

> ⚠️ Multi-AZ 備用執行個體**不接受讀取請求**；讀取副本才能提升讀取效能

---

## 問題 30 / Question 30

**[題目 / Question]**
The engineering team wants to monitor EC2 CPU utilization and send an email if it exceeds 80%. Which AWS services would you recommend? (Select two)
工程團隊想監控 EC2 CPU 使用率，超過 80% 時發送電子郵件，推薦哪兩個服務？

**✅ 正確答案 / Correct Answers：**
1. Amazon CloudWatch
2. Amazon Simple Notification Service (SNS)

**[監控告警方案 / Monitoring Alert Solution]**
```
Amazon CloudWatch（監控 CPU 使用率並設置告警）
        ↓（超過 80% 時觸發）
Amazon SNS（發送電子郵件通知）
```

**[為什麼不用其他服務 / Why Not Others]**
- CloudTrail → 帳戶活動審計，不監控 CPU
- Lambda → 運算服務，不發送監控告警
- SQS → 訊息佇列，不監控 CPU 或發送電子郵件

---

## 問題 31 / Question 31

**[題目 / Question]**
A gaming company wants to deliver **consistent low-latency gameplay** to end-users in various locations. Which AWS technology will provide necessary low-latency access?
遊戲公司想為各地用戶提供**一致的低延遲遊戲體驗**，哪個 AWS 技術提供必要的低延遲存取？

**✅ 正確答案 / Correct Answer：AWS Local Zones**

**[中文詳解]**
**AWS Local Zones** 讓您將 EC2、VPC、EBS 等 AWS 服務部署在更靠近終端用戶的地方，提供極低延遲存取。同時透過 Amazon 的高頻寬私有網路連接到父區域。

**[邊緣/本地服務比較 / Edge & Local Services]**

| 服務 / Service | 用途 / Use Case |
|---|---|
| **AWS Local Zones** | **將運算/儲存部署在靠近終端用戶的地方** |
| AWS Wavelength | 5G 邊緣位置的超低延遲應用 |
| AWS Edge Locations | CloudFront CDN 快取節點 |
| AWS Direct Connect | 本地到 AWS 的專用連接 |

---

## 問題 32 / Question 32

**[題目 / Question]**
Which of the following options are the **pillars** mentioned in the AWS Well-Architected Framework? (Select two)
以下哪兩個是 AWS Well-Architected Framework 的**支柱**？

**✅ 正確答案 / Correct Answers：**
1. Reliability（可靠性）
2. Cost Optimization（成本優化）

**[AWS Well-Architected Framework 六大支柱 / Six Pillars — Must Memorize!]**

| # | 支柱 / Pillar | 關鍵字 |
|---|---|---|
| 1 | Operational Excellence（卓越運營）| 自動化、持續改進 |
| 2 | Security（安全）| 保護資訊和系統 |
| 3 | **Reliability（可靠性）** | **從故障恢復** |
| 4 | Performance Efficiency（效能效率）| 高效使用資源 |
| 5 | **Cost Optimization（成本優化）** | **最低成本交付業務價值** |
| 6 | Sustainability（可持續性）| 降低環境影響 |

> ⚠️ Elasticity、Availability、Scalability **不是** WAF 支柱

---

## 問題 33 / Question 33

**[題目 / Question]**
Which AWS service is **essential** for implementing security of resources in AWS Cloud?
哪個 AWS 服務對於實現 AWS 雲端資源安全**至關重要**？

**✅ 正確答案 / Correct Answer：AWS Identity and Access Management (IAM)**

**[中文詳解]**
**AWS IAM** 讓您安全管理對 AWS 服務和資源的存取，透過授予唯一安全憑證並指定可存取的 API 和資源，實現安全最佳實踐。IAM 預設安全——用戶在未被明確授予權限之前，無法存取 AWS 資源。

---

## 問題 34 / Question 34

**[題目 / Question]**
A company wants a fully managed, flexible, scalable file storage with low latency for its **Windows-based applications**. Which AWS service is the right choice?
公司想為**Windows 應用程式**提供全托管、彈性、可擴展且低延遲的文件儲存，哪個服務最合適？

**✅ 正確答案 / Correct Answer：Amazon FSx for Windows File Server**

**[FSx 服務比較 / FSx Services Comparison]**

| 服務 / Service | 適用系統 / OS | 協議 / Protocol | 使用場景 |
|---|---|---|---|
| **FSx for Windows File Server** | **Windows（和 Linux）** | **SMB** | **Windows 應用程式、AD 整合** |
| Amazon EFS | Linux | NFS | Linux 多執行個體共享 |
| FSx for Lustre | Linux | Lustre | HPC、ML、媒體處理 |
| Amazon EBS | 單執行個體 | 區塊 / Block | 高效能區塊儲存 |

---

## 問題 35 / Question 35

**[題目 / Question]**
Which cloud transformation journey phase of the AWS CAF focuses on **demonstrating how the cloud will help accelerate your business outcomes**?
AWS CAF 哪個雲端轉型旅程階段專注於**展示雲端如何加速業務成果**？

**✅ 正確答案 / Correct Answer：Envision（構想）**

**[AWS CAF 四個轉型階段 / Four Transformation Phases]**

| 階段 / Phase | 重點 / Focus |
|---|---|
| **Envision（構想）** | **展示雲端如何加速業務成果 / Demonstrate cloud accelerates outcomes** |
| Align（調整）| 識別能力差距、跨組織依賴關係 |
| Launch（啟動）| 在生產中交付試點，展示增量業務價值 |
| Scale（擴展）| 擴展到理想規模，實現業務效益 |

---

## 問題 36 / Question 36

**[題目 / Question]**
Which characteristic of Cloud Computing imparts the ability to acquire resources as you need and release when you no longer need them?
雲端運算的哪個特性賦予了按需獲取資源並在不再需要時釋放的能力？

**✅ 正確答案 / Correct Answer：Elasticity（彈性）**

**[雲端特性定義 / Cloud Computing Characteristics]**

| 特性 / Characteristic | 定義 / Definition |
|---|---|
| **Elasticity（彈性）** | **按需獲取並在不需要時釋放資源 / Acquire & release as needed** |
| Reliability（可靠性）| 從故障中恢復 / Recover from disruptions |
| Durability（耐久性）| 資料持久存在不損壞 / Data remains consistent |
| Resiliency（韌性）| 從負載/攻擊/硬體故障中恢復 / Recover from failures |

---

## 問題 37 / Question 37

**[題目 / Question]**
Which foundational capability is found under the **Operations Perspective** of the AWS Cloud Adoption Framework?
哪個基礎能力屬於 AWS CAF 的**運營視角**？

**✅ 正確答案 / Correct Answer：Performance and capacity management（效能和容量管理）**

**[AWS CAF 六大視角能力分類 / CAF Capabilities by Perspective]**

| 視角 / Perspective | 能力範例 / Capability Examples |
|---|---|
| Business（業務）| 策略、投資組合管理 |
| People（人員）| 雲端流暢性、人才管理 |
| Governance（治理）| **應用程式組合管理** |
| **Platform（平台）** | **平台工程 / Platform engineering** |
| **Security（安全）** | **漏洞管理 / Vulnerability management** |
| **Operations（運營）** | **效能和容量管理** ✅ |

---

## 問題 38 / Question 38

**[題目 / Question]**
An online gaming company wants to **block users from certain geographies** from accessing its content. Which AWS service can accomplish this?
線上遊戲公司想**封鎖特定地理位置的使用者**存取，哪個 AWS 服務可實現？

**✅ 正確答案 / Correct Answer：AWS Web Application Firewall (AWS WAF)**

**[中文詳解]**
**AWS WAF** 可根據 IP 位址、HTTP 標頭、HTTP 正文、URI 字符串等條件配置允許、封鎖或監控 Web 請求的規則。可使用**基於 IP 位址的比對規則**封鎖特定地理位置，IP 到國家的對應準確率達 **99.8%**。

---

## 問題 39 / Question 39

**[題目 / Question]**
Which is correct regarding the AWS pricing policy for data transfer charges into or out of an AWS Region?
關於 AWS 區域資料傳輸費用的定價政策，哪個說法正確？

**✅ 正確答案 / Correct Answer：Only outbound data transfer is charged（只有出站資料傳輸收費）**

**[AWS 資料傳輸費用規則 / Data Transfer Pricing]**

| 方向 / Direction | 費用 / Cost |
|---|---|
| 傳入（網際網路 → AWS）/ Inbound | **免費 / Free** |
| **傳出（AWS → 網際網路）/ Outbound** | **收費（按區域分層計費）** |
| 同區域內服務間 / Same-region | 免費 / Free |
| 跨區域 / Cross-region | 收費 / Charged |

> AWS 三大基本費用驅動因素：**Compute（運算）+ Storage（儲存）+ Outbound Data Transfer（出站資料傳輸）**

---

## 問題 40 / Question 40

**[題目 / Question]**
Which of the following statements are correct about the AWS root user account? (Select two)
以下哪兩個關於 AWS root 使用者帳戶的說法正確？

**✅ 正確答案 / Correct Answers：**
1. It is highly recommended to enable MFA for root user account（強烈建議啟用 MFA）
2. Root user access credentials are the email address and password used to create the AWS account（Root 憑證是建立帳戶的電子郵件和密碼）

**[Root 使用者最佳實踐 / Root User Best Practices]**

| 事項 / Item | 說明 |
|---|---|
| ✅ 啟用 MFA | 強烈建議 / Highly recommended |
| ✅ 密碼可更改 | 可在建立後更改 / Can change after creation |
| ❌ 分享給管理者 | 絕不分享 / Never share |
| ❌ 限制 Root 權限 | 無法用 IAM Policy 限制 / Cannot restrict |
| ✅ 日常操作 | 建立個別 IAM 用戶 / Create individual IAM users |

---

## 問題 41 / Question 41

**[題目 / Question]**
Which AWS service will help an organization track the **history of configuration changes** for all resources?
哪個 AWS 服務可幫助組織追蹤所有資源的**配置變更歷史**？

**✅ 正確答案 / Correct Answer：AWS Config**

**[中文詳解]**
**AWS Config** 持續監控並記錄 AWS 資源配置，並允許自動評估記錄的配置是否符合期望配置。可評估 AWS 資源配置、取得配置快照、取回配置歷史，並在資源建立/修改/刪除時收到通知。

**[三大監控服務記憶口訣 / Key Memory Aid]**
> **CloudWatch** → 效能監控/告警
> **CloudTrail** → 帳戶操作審計
> **Config** → 資源配置歷史和合規

---

## 問題 42 / Question 42

**[題目 / Question]**
Which of the following options can be used to access and manage all AWS services? (Select three)
以下哪三個選項可用於存取和管理所有 AWS 服務？

**✅ 正確答案 / Correct Answers：**
1. AWS Management Console（管理控制台）
2. AWS Command Line Interface (AWS CLI)（命令列介面）
3. AWS Software Development Kit (SDK)（軟體開發工具包）

**[AWS 三種存取方式 / Three Access Methods]**

| 方式 / Method | 說明 / Description | 適用對象 |
|---|---|---|
| **AWS Console** | Web 圖形介面 | 視覺化管理 |
| **AWS CLI** | 命令列工具 | 腳本自動化 |
| **AWS SDK** | 語言特定 API | 程式碼整合 |

---

## 問題 43 / Question 43

**[題目 / Question]**
A startup is looking for **24x7 phone based technical support** for its AWS account. Which is the MOST cost-effective AWS support plan?
新創公司需要 **24/7 電話技術支援**，最具成本效益的 AWS 支援方案是？

**✅ 正確答案 / Correct Answer：AWS Business Support**

**[支援方案電話支援比較 / Phone Support Comparison]**

| 方案 / Plan | 24/7 電話支援 | 成本 |
|---|---|---|
| Basic | ❌ | 免費 |
| Developer | ❌（僅工作時間電子郵件）| 最低 |
| **Business** | **✅** | **最具成本效益** |
| Enterprise On-Ramp | ✅ | 較貴 |
| Enterprise | ✅ | 最貴 |

---

## 問題 44 / Question 44

**[題目 / Question]**
A photo sharing app wants to store thumbnails that are **rarely used** but need to be **immediately accessible**, and **can be regenerated if lost**. Which is the most cost-effective S3 storage class?
照片分享應用程式想儲存**很少使用**但需要**立即存取**、且**遺失可重新產生**的縮圖，最具成本效益的 S3 儲存類別是？

**✅ 正確答案 / Correct Answer：Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)**

**[中文詳解]**
**S3 One Zone-IA** 比 S3 Standard-IA 便宜 20%，但只儲存在**單一 AZ**（較低可用性）。由於縮圖遺失可重新產生，可用性降低不是問題，因此這是最具成本效益的選擇。

**[S3 儲存類別選擇邏輯 / Selection Logic]**

| 需求 / Requirement | 推薦 / Recommended |
|---|---|
| 頻繁存取 | S3 Standard |
| 不頻繁 + 快速 + 多 AZ 持久 | S3 Standard-IA |
| **不頻繁 + 快速 + 可損失數據** | **S3 One Zone-IA ✅ (最便宜)** |
| 存檔，需快速取回 | S3 Glacier Instant Retrieval |
| 存檔，數分鐘到小時取回 | S3 Glacier Flexible Retrieval |

---

## 問題 45 / Question 45

**[題目 / Question]**
An e-commerce company wants to store data from a recommendation engine with the **LEAST operational overhead** for **any scale**. Which AWS service would you recommend?
電商公司想以**最少的運營負擔**在**任何規模**下儲存推薦引擎資料，推薦哪個服務？

**✅ 正確答案 / Correct Answer：Amazon DynamoDB**

**[中文詳解]**
**Amazon DynamoDB** 是全托管的 NoSQL 資料庫，客戶無需擔心硬體佈建、設定配置、吞吐量規劃、複製、軟體修補或叢集擴展，可在任何規模提供個位數毫秒效能。

**[資料庫最少運營負擔比較 / Least Operational Overhead]**

| 服務 / Service | 運營負擔 | 擴展性 |
|---|---|---|
| **Amazon DynamoDB** | **最少 / Least** | **無限 / Unlimited** |
| Amazon RDS | 中等 / Medium | 有限 / Limited |
| Amazon Neptune | 中等 / Medium | 圖形 / Graph |
| Amazon S3 | 最少（但非資料庫）| 無限 |

---

## 問題 46 / Question 46

**[題目 / Question]**
A developer wants to upload PHP code to AWS and have AWS handle deployment automatically, but still wants **access to the underlying OS**. Which AWS service would you recommend?
開發者想上傳 PHP 代碼讓 AWS 自動處理部署，但仍需**存取底層 OS**，推薦哪個服務？

**✅ 正確答案 / Correct Answer：AWS Elastic Beanstalk**

**[中文詳解]**
**AWS Elastic Beanstalk** 支援 Java、.NET、PHP、Node.js、Python、Ruby、Go 和 Docker，只需上傳代碼，自動處理部署、容量佈建、負載均衡、自動擴展到應用程式健康監控。同時**保留對底層 AWS 資源的完全控制**，可隨時存取底層資源。無額外費用，僅支付底層資源費用。

**[部署服務比較 / Deployment Services]**

| 服務 / Service | 自動部署 | OS 存取 | 說明 |
|---|---|---|---|
| **Elastic Beanstalk** | **✅** | **✅** | **上傳代碼即可** |
| EC2 | ❌（手動）| ✅ | 自行管理 |
| Lambda | ✅ | ❌ | 無伺服器 |
| CloudFormation | 需定義資源 | ✅ | 基礎設施即代碼 |

---

## 問題 47 / Question 47

**[題目 / Question]**
According to the AWS Shared Responsibility Model, which is a responsibility of the **customer** for Amazon RDS?
根據 AWS 共同責任模型，哪項是客戶對於 Amazon RDS 的**客戶責任**？

**✅ 正確答案 / Correct Answer：Database encryption（資料庫加密）**

**[Amazon RDS 責任劃分 / RDS Responsibility Division]**

| 責任項目 / Item | AWS | 客戶 |
|---|---|---|
| 底層伺服器硬體管理 | ✅ | ❌ |
| RDS 資料庫修補 | ✅ | ❌ |
| 底層 OS 修補 | ✅ | ❌ |
| **資料庫加密 / Database encryption** | ❌ | **✅** |
| 資料管理 / Data management | ❌ | ✅ |

> **記憶法**：RDS 是托管服務，AWS 負責底層所有事項；客戶負責**資料**和**加密**

---

## 問題 48 / Question 48

**[題目 / Question]**
Which AWS database service allows a **flexible schema** and supports **document data models**?
哪個 AWS 資料庫服務允許**靈活架構**並支援**文件資料模型**？

**✅ 正確答案 / Correct Answer：Amazon DynamoDB**

**[中文詳解]**
**Amazon DynamoDB** 是 NoSQL 資料庫，支援鍵值和文件資料模型，具有靈活架構——每行可以有任意數量的欄位，無需重新定義表格架構，適合業務需求快速變化的場景。

**[資料庫類型比較 / Database Types]**

| 資料庫 / Database | 類型 | 靈活架構 |
|---|---|---|
| **Amazon DynamoDB** | **NoSQL（鍵值/文件）** | **✅ 是** |
| Amazon RDS | 關聯式 / Relational | ❌ 固定架構 |
| Amazon Aurora | 關聯式 / Relational | ❌ 固定架構 |
| Amazon Redshift | 資料倉儲 / Data warehouse | ❌ 固定架構 |

---

## 問題 49 / Question 49

**[題目 / Question]**
A company needs to provide secure shell access to EC2 instances **without opening new ports or using public IP addresses**. Which tool/service will help?
公司需要在**不開放新端口或使用公共 IP** 的情況下提供 EC2 安全 Shell 存取，哪個服務可實現？

**✅ 正確答案 / Correct Answer：AWS Systems Manager Session Manager**

**[中文詳解]**
**AWS Systems Manager Session Manager** 提供互動式瀏覽器型 Shell 和 CLI 體驗，無需：
- 開放入站端口（無需開放 port 22）
- 維護堡壘主機 (bastion host)
- 管理 SSH 金鑰

**[EC2 存取方式比較 / EC2 Access Methods]**

| 方式 / Method | 開放 Port 22 | 公共 IP | 說明 |
|---|---|---|---|
| **Session Manager** | **❌ 不需要** | **❌ 不需要** | **最安全** |
| EC2 Instance Connect | ✅ 需要 | 可選 | 使用 IAM 控制 |
| SSH 直連 | ✅ 需要 | ✅ 需要 | 傳統方式 |

---

## 問題 50 / Question 50

**[題目 / Question]**
Which is the correct statement regarding AWS Storage services?
以下哪個關於 AWS 儲存服務的說法正確？

**✅ 正確答案 / Correct Answer：**
S3 is **object** based, EBS is **block** based, EFS is **file** based storage
S3 是**物件**儲存，EBS 是**區塊**儲存，EFS 是**文件**儲存

**[AWS 三大儲存類型 / Three Storage Types — Must Know!]**

| 服務 / Service | 儲存類型 | 協議 | 使用場景 |
|---|---|---|---|
| **Amazon S3** | **物件 / Object** | HTTPS | 網站、備份、大數據 |
| **Amazon EBS** | **區塊 / Block** | 區塊 | EC2 高效能磁碟 |
| **Amazon EFS** | **文件 / File** | NFS | 多執行個體共享 |

---

## 問題 51 / Question 51

**[題目 / Question]**
Which Amazon Route 53 routing policy improves performance by routing requests to the endpoint that provides the **fastest experience**?
哪個 Amazon Route 53 路由策略通過將請求路由到提供**最快體驗**的端點來提升效能？

**✅ 正確答案 / Correct Answer：Latency-based routing（延遲路由）**

**[Route 53 路由策略總整理 / Routing Policies Summary]**

| 策略 / Policy | 使用場景 / Use Case |
|---|---|
| Simple（簡單）| 路由到單一資源 |
| **Latency-based（延遲）** | **路由到最低延遲的 AWS 區域** ✅ |
| Weighted（加權）| 按比例分配流量到多個資源 |
| Failover（容錯移轉）| 主動-被動容錯移轉 |
| Geolocation（地理位置）| 按用戶地理位置路由 |
| Multivalue Answer（多值）| 返回多個健康記錄 |

---

## 問題 52 / Question 52

**[題目 / Question]**
Which AWS service publishes up-to-the-minute information on the **general status and availability of ALL AWS services in ALL Regions**?
哪個 AWS 服務發布所有 AWS 服務在**所有區域**的即時整體狀態和可用性資訊？

**✅ 正確答案 / Correct Answer：AWS Health Dashboard - service health（服務健康儀表板）**

**[兩個健康儀表板比較 / Health Dashboard Comparison — Exam Alert!]**

| 儀表板 / Dashboard | 範圍 / Scope | 網址 |
|---|---|---|
| **Service Health（服務健康）** | **所有 AWS 服務/所有區域** | health.aws.amazon.com/health/status |
| Account Health（帳戶健康）| 您的特定帳戶 | phd.aws.amazon.com |

---

## 問題 53 / Question 53

**[題目 / Question]**
What are the **fundamental drivers of cost** with AWS Cloud?
AWS 雲端的**基本費用驅動因素**是什麼？

**✅ 正確答案 / Correct Answer：Compute, Storage and Outbound Data Transfer**
運算、儲存和出站資料傳輸

**[AWS 三大費用驅動因素 / Three Fundamental Cost Drivers]**

```
💻 Compute（運算）
💾 Storage（儲存）
📤 Outbound Data Transfer（出站資料傳輸）
```

> ⚠️ **Inbound data transfer（入站資料傳輸）是免費的！**
> **Databases（資料庫）不在三大費用驅動因素中**（雖然資料庫有費用，但不是基本驅動因素）

---

## 問題 54 / Question 54

**[題目 / Question]**
Which EC2 pricing model is the most cost-effective and flexible with **no long-term commitment, no upfront payment**, and **guarantees the instance won't be interrupted**?
哪個 EC2 定價模型最具靈活性，**無長期承諾、無預付款**，且**保證執行個體不被中斷**？

**✅ 正確答案 / Correct Answer：On-demand Instance（隨需執行個體）**

**[EC2 定價模型比較 / EC2 Pricing Models]**

| 類型 / Type | 中斷風險 | 承諾期 | 折扣 | 適用場景 |
|---|---|---|---|---|
| **On-Demand** | **❌ 不中斷** | **無** | **無** | 靈活短期 |
| Reserved (RI) | ❌ 不中斷 | 1/3 年 | 75% | 長期穩定 |
| Spot | ✅ 會中斷 | 無 | 90% | 容錯批次 |
| Dedicated Host | ❌ 不中斷 | 可選 | 無 | 授權合規 |

---

## 問題 55 / Question 55

**[題目 / Question]**
A customer creates a VPC and a subnet. Which statement is correct about their AZ scope?
客戶建立了 VPC 和子網路，關於其 AZ 範圍哪個說法正確？

**✅ 正確答案 / Correct Answer：**
VPC spans **all AZs** in the Region; subnet spans **only one AZ**.
VPC 跨越區域中的**所有 AZ**；子網路只跨越**一個 AZ**。

**[VPC 網路架構 / VPC Network Architecture]**
```
AWS Region（區域）
└── Amazon VPC（跨所有 AZ / Spans all AZs）
    ├── AZ-1
    │   └── Subnet（只在一個 AZ / Only one AZ）
    ├── AZ-2
    │   └── Subnet
    └── AZ-3
        └── Subnet
```

---

## 問題 56 / Question 56

**[題目 / Question]**
Which AWS service should be used to run container applications while **avoiding the operational overhead of scaling, patching, securing, and managing servers**?
哪個 AWS 服務可在**避免管理伺服器的運營負擔**的同時運行容器應用程式？

**✅ 正確答案 / Correct Answer：Amazon ECS - Fargate launch type**

**[ECS 啟動類型比較 / ECS Launch Types]**

| 啟動類型 / Launch Type | 伺服器管理 | 無伺服器 | 說明 |
|---|---|---|---|
| **ECS Fargate** | **❌ 無需管理** | **✅** | **全托管無伺服器容器** |
| ECS EC2 | ✅ 需管理 EC2 | ❌ | 自行管理底層叢集 |

> **AWS Fargate** 同時支援 ECS 和 EKS，按應用程式實際使用的資源付費

---

## 問題 57 / Question 57

**[題目 / Question]**
Which statement is correct for a **Security Group** and a **Network ACL**?
關於**安全群組**和**網路 ACL** 哪個說法正確？

**✅ 正確答案 / Correct Answer：**
Security Group acts as a firewall at the **instance level**; Network ACL acts at the **subnet level**.
安全群組在**執行個體層級**作為防火牆；網路 ACL 在**子網路層級**作為防火牆。

**[安全群組 vs 網路 ACL / Security Group vs Network ACL]**

| 特性 / Feature | Security Group（安全群組）| Network ACL（網路 ACL）|
|---|---|---|
| 作用層級 / Level | **執行個體 / Instance** | **子網路 / Subnet** |
| 規則類型 / Rules | 僅允許 / Allow only | 允許 + 拒絕 / Allow & Deny |
| 狀態 / Stateful | ✅ 有狀態 | ❌ 無狀態 |
| 預設 / Default | 拒絕所有入站 | 允許所有流量 |

---

## 問題 58 / Question 58

**[題目 / Question]**
Which AWS service would you use to send alerts when the costs for your AWS account **exceed your budgeted amount**?
哪個 AWS 服務可在費用**超出預算時**發送告警？

**✅ 正確答案 / Correct Answer：AWS Budgets**

**[成本工具比較 / Cost Tools Comparison — Exam Alert!]**

| 工具 / Tool | 主要功能 / Main Function |
|---|---|
| **AWS Budgets** | **設定預算並在超出時告警（含預測超出）** |
| CloudWatch Billing Alarms | 實際費用超出閾值時告警 |
| AWS Cost Explorer | 視覺化和管理費用趨勢 |
| AWS Pricing Calculator | 事前估算 AWS 服務費用 |

> **關鍵區別**：
> - CloudWatch Billing → 實際費用超出 → 告警
> - **AWS Budgets** → 實際費用**或預測費用**超出 → 告警（更強大）

---

## 問題 59 / Question 59

**[題目 / Question]**
Which policy describes **prohibited uses** of the web services offered by Amazon Web Services?
哪個政策描述了 Amazon Web Services 提供的 Web 服務的**禁止使用**行為？

**✅ 正確答案 / Correct Answer：AWS Acceptable Use Policy（AWS 可接受使用政策）**

**[中文詳解]**
**AWS Acceptable Use Policy（AUP）** 描述了 AWS 服務的禁止使用行為，網址為 https://aws.amazon.com/aup/，由 AWS 根據需要更新。

> ⚠️ "AWS Fair Use Policy" 和 "AWS Applicable Use Policy" 都是虛構選項（干擾項）

---

## 問題 60 / Question 60

**[題目 / Question]**
An organization deploys IT infrastructure in a combination of **on-premises data center** and **AWS Cloud**. How would you categorize this deployment model?
組織將 IT 基礎設施部署在**本地資料中心**和 **AWS 雲端**的組合中，這是什麼部署模型？

**✅ 正確答案 / Correct Answer：Hybrid deployment（混合部署）**

**[雲端部署模型 / Cloud Deployment Models]**

| 模型 / Model | 說明 / Description |
|---|---|
| **Hybrid（混合）** | **本地基礎設施 + 雲端 / On-premises + Cloud** |
| Cloud（雲端）| 完全在雲端中運行 / Fully in cloud |
| Private / On-premises（私有）| 完全在本地數據中心 / Fully on-premises |

---

## 問題 61 / Question 61

**[題目 / Question]**
A data analytics company stores data on Amazon S3 and wants to do **SQL-based analysis** with minimum effort. Which AWS service would you suggest?
資料分析公司將資料存儲在 S3 上，想以最少努力進行 **SQL 分析**，推薦哪個服務？

**✅ 正確答案 / Correct Answer：Amazon Athena**

**[中文詳解]**
**Amazon Athena** 是互動式查詢服務，使用標準 SQL 直接分析 S3 中的資料。無伺服器，無需管理基礎設施，只需為執行的查詢付費。無需 ETL 作業，任何有 SQL 技能的人都可快速分析大規模資料集。

**[S3 資料分析服務比較 / S3 Data Analysis Services]**

| 服務 / Service | 用途 | 直接查詢 S3 |
|---|---|---|
| **Amazon Athena** | **SQL 查詢 S3 資料** | **✅ 直接** |
| Amazon Redshift | 資料倉儲（需載入資料）| ❌ 需先 ETL |
| Amazon Aurora | 關聯式資料庫 | ❌ |
| Amazon DynamoDB | NoSQL 資料庫 | ❌ |

---

## 問題 62 / Question 62

**[題目 / Question]**
What are the different gateway types supported by AWS Storage Gateway service?
AWS Storage Gateway 服務支援哪些不同的閘道類型？

**✅ 正確答案 / Correct Answer：Tape Gateway, File Gateway and Volume Gateway**

**[AWS Storage Gateway 三種類型 / Three Gateway Types — Must Memorize!]**

| 閘道類型 / Gateway Type | 說明 / Description | 使用場景 |
|---|---|---|
| **File Gateway** | 文件存取（NFS/SMB）→ S3 | 雲端備份文件共享 |
| **Volume Gateway** | 區塊存儲 → S3（iSCSI）| 低延遲本地存取 |
| **Tape Gateway** | 虛擬磁帶庫 → S3/Glacier | 磁帶備份遷移到雲端 |

> ⚠️ "Block Gateway" 和 "Object Gateway" 是虛構選項

---

## 問題 63 / Question 63

**[題目 / Question]**
A retail company with multiple AWS accounts for each department needs **consolidated billing** and a **single payment method**. Which AWS service can be used?
零售公司有多個部門的 AWS 帳戶，需要**整合計費**和**單一付款方式**，哪個服務？

**✅ 正確答案 / Correct Answer：AWS Organizations**

**[AWS Organizations 主要功能 / Key Features]**
- ✅ 集中管理多個帳戶的計費
- ✅ 設置單一付款方式
- ✅ 自動建立帳戶
- ✅ 按業務需求建立帳戶群組
- ✅ 套用治理策略 (SCPs)
- ✅ 共享預留執行個體

> ⚠️ 對所有 AWS 客戶**免費**提供

---

## 問題 64 / Question 64

**[題目 / Question]**
A company using a **message broker** on-premises wants to move this messaging functionality to AWS Cloud **easily**, without rewriting code. Which AWS service is the right choice?
公司在本地使用**訊息代理服務**，想**輕鬆**遷移到 AWS 且不重寫代碼，哪個服務最合適？

**✅ 正確答案 / Correct Answer：Amazon MQ**

**[中文詳解]**
**Amazon MQ** 是 Apache ActiveMQ 和 RabbitMQ 的托管訊息代理服務，支援行業標準 API 和協議（AMQP、MQTT、OpenWire、STOMP），可從現有的標準訊息代理遷移到 AWS，**無需重寫代碼**。

**[訊息服務選擇 / Messaging Service Selection]**

| 服務 / Service | 適用場景 |
|---|---|
| **Amazon MQ** | **現有訊息代理遷移（保留標準協議）** |
| Amazon SQS | 新建雲端原生訊息佇列 |
| Amazon SNS | 新建雲端原生發布/訂閱 |
| Amazon Kinesis | 大規模即時串流資料 |

> **關鍵選擇原則**：
> - 遷移**現有**訊息代理 → **Amazon MQ**
> - 建立**全新**雲端應用程式 → **SQS/SNS**

---

## 問題 65 / Question 65

**[題目 / Question]**
Which of the following AWS services can be used to prevent DDoS attacks? (Select three)
哪三個 AWS 服務可用於防止 DDoS 攻擊？

**✅ 正確答案 / Correct Answers：**
1. AWS Shield
2. AWS Web Application Firewall (AWS WAF)
3. Amazon CloudFront with Amazon Route 53

**[DDoS 防護服務 / DDoS Protection Services]**

| 服務 / Service | DDoS 防護 | 防護層級 |
|---|---|---|
| **AWS Shield** | **✅** | Layer 3, 4, 7 |
| **AWS WAF** | **✅** | Layer 7（速率限制）|
| **CloudFront + Route 53** | **✅** | 邊緣節點吸收攻擊 |
| AWS CloudHSM | ❌ | 加密，非 DDoS |
| AWS Trusted Advisor | ❌ | 最佳實踐建議 |
| Amazon Inspector | ❌ | 漏洞評估 |

**[DDoS 防護架構 / DDoS Defense Architecture]**
```
Internet → CloudFront + Route 53（邊緣節點分散攻擊）
        → AWS WAF（過濾惡意請求）
        → AWS Shield（自動緩解 DDoS）
        → 您的應用程式
```

---

## 📊 考題領域統計 / Domain Summary

| 領域 / Domain | 題數 / Questions | 百分比 / % |
|---|---|---|
| Technology（技術）| 26 | 40% |
| Security and Compliance（安全與合規）| 17 | 26.2% |
| Cloud Concepts（雲端概念）| 15 | 23.1% |
| Billing and Pricing（計費與定價）| 7 | 10.8% |

---

## 🎯 本回必考重點整理 / Key Exam Points (Set 2)

### 容器服務快速記憶
- **ECR** → 儲存容器映像（倉庫）
- **ECS** → 執行容器（管理）
- **Fargate** → 無伺服器執行容器（無需管理伺服器）
- **EKS** → 管理 Kubernetes 容器

### 儲存服務類型
- **S3** → 物件 Object
- **EBS** → 區塊 Block
- **EFS** → 文件 File（NFS，Linux，多 AZ）
- **FSx for Windows** → 文件 File（SMB，Windows）
- **FSx for Lustre** → 文件 File（Linux，HPC）

### AWS Health 儀表板
- **Service Health** → 所有服務、所有區域的整體狀態
- **Account Health** → 您的帳戶的個人化狀態

### Route 53 路由策略
- Simple → 單一資源
- **Weighted** → 控制流量比例（A/B 測試）
- **Latency** → 最低延遲區域（最佳效能）
- Failover → 主動-被動容錯移轉
- Geolocation → 按地理位置路由

### 訊息服務選擇
- **遷移現有訊息代理** → Amazon MQ（支援標準協議）
- **新建雲端訊息佇列** → Amazon SQS
- **新建雲端發布/訂閱** → Amazon SNS

### DDoS 防護三劍客
**Shield + WAF + CloudFront/Route 53**

### AWS CAF 四個轉型階段
**Envision → Align → Launch → Scale**
（構想 → 調整 → 啟動 → 擴展）

### Well-Architected Framework 六大支柱
**卓越運營 + 安全 + 可靠性 + 效能效率 + 成本優化 + 可持續性**
