# AWS Cloud Practitioner 考題中英對照詳解（第四回）
# AWS Cloud Practitioner Exam Q&A — Bilingual Study Guide (Set 4)

---

## 問題 1 / Question 1

**[題目 / Question]**
Which AWS service would you use to create a **logically isolated section** of the AWS Cloud where you can launch AWS resources in your virtual network?
哪個 AWS 服務可建立 AWS 雲端中**邏輯隔離的區段**，讓您在虛擬網路中啟動 AWS 資源？

**✅ 正確答案 / Correct Answer：Virtual Private Cloud (VPC)**

**[VPC 核心概念 / VPC Core Concepts]**

| 概念 / Concept | 說明 / Description |
|---|---|
| **Amazon VPC** | **邏輯隔離的 AWS 雲端區段，您定義的虛擬網路** |
| Subnet | VPC 內的 IP 地址範圍（不是 AWS 服務）|
| Network ACL | VPC 的可選安全層，控制子網路流量（不是 AWS 服務）|
| VPN | 加密隧道，連接本地到 AWS（不能建立隔離區段）|

> VPC 讓您完全控制虛擬網路環境，包括：IP 位址範圍選擇、子網路建立、路由表和網路閘道配置

---

## 問題 2 / Question 2

**[題目 / Question]**
Two VPCs need to **privately share data** between each other. Which is the most optimal way?
兩個 VPC 需要相互**私密共享資料**，哪個方式最佳？

**✅ 正確答案 / Correct Answer：VPC peering connection（VPC 對等連接）**

**[中文詳解]**
**VPC 對等連接**是兩個 VPC 之間的網路連接，可私密路由流量。任一 VPC 中的執行個體可以像在同一網路中一樣相互通信。可在自己帳戶的 VPC 之間、不同 AWS 帳戶的 VPC 之間，或不同 AWS Region 的 VPC 之間建立。

**[VPC 連接選項比較 / VPC Connectivity Options]**

| 方案 / Solution | 用途 / Purpose | VPC 互連 |
|---|---|---|
| **VPC Peering** | **兩個 VPC 之間私密連接** | **✅ 最佳（兩個 VPC）** |
| AWS Transit Gateway | 多個 VPC 中央樞紐連接 | ✅ 最佳（多個 VPC）|
| VPC Endpoint | VPC 連接 AWS 服務 | ❌ 不能連接兩個 VPC |
| AWS Direct Connect | 本地到 VPC 的專用連接 | ❌ 不能互連 VPC |
| Site-to-Site VPN | 本地到 AWS 的加密隧道 | ❌ 不能互連 VPC |

> ⚠️ VPC Peering 是**非傳遞性**的，大量 VPC 時用 Transit Gateway 更好

---

## 問題 3 / Question 3

**[題目 / Question]**
A financial services company wants to ensure that all customer data on Amazon S3 **always stays private**. Which is the MOST efficient solution?
金融服務公司想確保 S3 上的所有客戶資料**始終保持私密**，哪個最有效率？

**✅ 正確答案 / Correct Answer：Use Amazon S3 Block Public Access（使用 Amazon S3 封鎖公開存取）**

**[中文詳解]**
**Amazon S3 Block Public Access** 為存取點、儲存桶和帳戶提供設定，幫助管理對 S3 資源的公開存取。新儲存桶、存取點和物件預設不允許公開存取。S3 Block Public Access 設定可覆蓋儲存桶策略和物件權限，確保公開存取被限制。

**[為什麼不用其他方案 / Why Not Others]**
- Lambda 方案 → 雖可行但效率低，CRR 是開箱即用的最佳解決方案
- CloudWatch → 監控服務，不能確保 S3 資料隱私
- 委員會審查 → 干擾項，人工審查效率最低

---

## 問題 4 / Question 4

**[題目 / Question]**
Which of the following types are **free** under the Amazon S3 pricing model? (Select two)
以下哪兩個在 Amazon S3 定價模型中是**免費**的？

**✅ 正確答案 / Correct Answers：**
1. Data transferred **in** from the internet（從網際網路**傳入**的資料）
2. Data transferred out to an EC2 instance in the **same AWS Region** as the S3 bucket

**[Amazon S3 免費傳輸 / S3 Free Data Transfer]**

| 傳輸類型 / Transfer Type | 費用 / Cost |
|---|---|
| **從網際網路傳入 S3 / Inbound from internet** | **免費 / Free** ✅ |
| **傳出到同一 Region 的 EC2 / To EC2 in same Region** | **免費 / Free** ✅ |
| 傳出到 Amazon CloudFront | 免費 / Free ✅ |
| 傳出到不同 Region 的 EC2 | 收費 / Charged |
| 傳出到網際網路 | 收費 / Charged |

> **S3 定價四大組成**：儲存費用 + 請求和資料取回費用 + 資料傳輸費用 + 資料管理功能費用

---

## 問題 5 / Question 5

**[題目 / Question]**
A financial services company wants to review **Payment Card Industry (PCI) reports** on AWS Cloud. Which AWS resource can address this?
金融服務公司想審查 AWS 雲端的 **PCI 支付卡行業報告**，哪個 AWS 資源可解決？

**✅ 正確答案 / Correct Answer：AWS Artifact**

**[中文詳解]**
**AWS Artifact** 是合規相關資訊的中央資源，提供隨需存取 AWS 安全和合規報告，包括：
- **SOC 報告**（服務組織控制）
- **PCI 報告**（支付卡行業）
- 各地理位置和合規垂直領域的認證

這是免費的自助服務入口網站。

---

## 問題 6 / Question 6

**[題目 / Question]**
How is Amazon EC2 **different from traditional hosting systems**? (Select two)
Amazon EC2 與**傳統託管系統**有何不同？（選兩個）

**✅ 正確答案 / Correct Answers：**
1. With EC2, developers can **launch and terminate instances anytime**（可隨時啟動和終止執行個體）
2. Amazon EC2 can **scale with changing computing requirements**（可隨計算需求變化而擴展）

**[EC2 vs 傳統託管比較 / EC2 vs Traditional Hosting]**

| 特性 / Feature | EC2 | 傳統託管 |
|---|---|---|
| 控制生命週期 | ✅ 隨時啟動/終止 | ❌ 固定 |
| 擴展性 | ✅ 按需擴展 | ❌ 需預購容量 |
| 付款方式 | ✅ 按使用量（秒計費）| ❌ 固定月費 |
| 資源共享 | ❌ 獨立資源 | ✅ 與其他用戶共享 |
| 超購風險 | ❌ 無超購風險 | ✅ 有超購風險 |

---

## 問題 7 / Question 7

**[題目 / Question]**
Which AWS service would you choose for a data processing project that needs a **schemaless database**?
哪個 AWS 服務適合需要**無架構資料庫**的資料處理專案？

**✅ 正確答案 / Correct Answer：Amazon DynamoDB**

**[中文詳解]**
**Amazon DynamoDB** 是 NoSQL 資料庫，**schemaless（無架構/無模式）**意味著每行可以有任意數量的欄位。支援鍵值和文件資料模型，包括 JSON 文件，可管理結構化或半結構化資料。

**[關聯式 vs NoSQL 資料庫 / Relational vs NoSQL]**

| 特性 / Feature | Amazon DynamoDB | Amazon RDS / Aurora / Redshift |
|---|---|---|
| 架構 / Schema | **無架構 / Schemaless** ✅ | 需固定架構 / Fixed schema |
| 資料模型 | 鍵值/文件 | 表格/關聯式 |
| 擴展性 | 無限水平擴展 | 垂直擴展為主 |

---

## 問題 8 / Question 8

**[題目 / Question]**
Which of the following statements are **true** regarding Amazon S3? (Select two)
以下哪兩個關於 Amazon S3 的說法是**正確的**？

**✅ 正確答案 / Correct Answers：**
1. Amazon S3 stores data in a **flat non-hierarchical structure**（S3 以**扁平非層次結構**儲存資料）
2. Amazon S3 is a **key value based object storage service**（S3 是**基於鍵值的物件儲存服務**）

**[Amazon S3 核心特性 / S3 Core Characteristics]**

| 特性 / Characteristic | 說明 / Description |
|---|---|
| **非層次扁平結構** | 物件儲存在儲存桶中，使用前綴組織（非真正的資料夾）|
| **鍵值物件存儲** | 鍵（Key）= 物件名稱；值（Value）= 物件資料 |
| 可附加標籤 | 每個物件最多 10 個鍵值對標籤 |

**[S3 錯誤觀念澄清 / Common S3 Misconceptions]**
- ❌ S3 不是區塊存儲（那是 EBS）
- ❌ S3 不是文件系統（那是 EFS）
- ❌ S3 不能安裝資料庫

---

## 問題 9 / Question 9

**[題目 / Question]**
Which of the following describes an **Availability Zone (AZ)** in the AWS Cloud?
以下哪個描述了 AWS 雲端中的**可用區域 (AZ)**？

**✅ 正確答案 / Correct Answer：One or more data centers in the **same location**（**同一位置**的一個或多個資料中心）**

**[AWS 全球基礎設施定義 / Global Infrastructure Definitions]**

| 元素 / Element | 定義 / Definition |
|---|---|
| AWS Region | 全球各地的物理位置，由多個 AZ 組成 |
| **Availability Zone (AZ)** | **同一地點的一個或多個獨立資料中心**，有冗餘電力、網路和連接 |
| Edge Location | CloudFront 使用的快取節點 |

> **記憶法**：AZ = 同一地點（Same location）的一個或多個資料中心，多個 AZ 組成一個 Region

---

## 問題 10 / Question 10

**[題目 / Question]**
Which statements are CORRECT regarding **AWS Global Accelerator**? (Select two)
以下哪兩個關於 **AWS Global Accelerator** 的說法正確？

**✅ 正確答案 / Correct Answers：**
1. AWS Global Accelerator **provides static IP addresses** that act as a fixed entry point to your applications
2. AWS Global Accelerator is a **good fit for non-HTTP use cases**（適合非 HTTP 使用案例）

**[Global Accelerator 關鍵特性 / Key Characteristics]**

| 特性 / Feature | 說明 / Description |
|---|---|
| **靜態 IP 位址** | 提供固定入口點，消除管理多個 Region 和 AZ 的 IP 複雜性 |
| **非 HTTP 使用案例** | 遊戲 (UDP)、IoT (MQTT)、Voice over IP |
| 使用 AWS 全球網路 | 優化流量路徑，可提升效能最多 60% |
| 邊緣節點 | **與 CloudFront 使用相同的邊緣節點** |

**[常見錯誤選項 / Common Distractor Clarification]**
- ❌ Global Accelerator 和 CloudFront **使用相同**邊緣節點（不是不同）
- ❌ Global Accelerator **可以**與 ELB 配合使用
- ❌ Global Accelerator 不能託管靜態網站（那是 S3）

---

## 問題 11 / Question 11

**[題目 / Question]**
Which of the following are **benefits of AWS WAF**? (Select two)
以下哪兩個是 **AWS WAF 的優勢**？

**✅ 正確答案 / Correct Answers：**
1. AWS WAF can **block all requests except the ones you allow**（可封鎖除您允許之外的所有請求）
2. AWS WAF can check for **SQL injection** code

**[AWS WAF 功能 / AWS WAF Capabilities]**

| 功能 / Feature | 說明 |
|---|---|
| ✅ 封鎖除允許外的所有請求 | 白名單模式，適合限制性網站 |
| ✅ SQL 注入偵測 | 識別可能是惡意的 SQL 代碼 |
| ✅ 跨站腳本 (XSS) 偵測 | 識別可能是惡意的腳本 |
| ✅ 基於速率的規則 | 緩解 Web 層 DDoS 攻擊 |
| ✅ IP 地址過濾 | 依 IP、標頭、正文、URI 字符串過濾 |

**[WAF 不能做的事 / What WAF Cannot Do]**
- ❌ 不提供第 3、4 層（Layer 3、4）基礎設施攻擊防護（那是 Shield）
- ❌ 不提供 DRT（DDoS 響應團隊）支援（那是 Shield Advanced）
- ❌ 不監控轉發到 Route 53 的請求（監控 CloudFront、ALB、API Gateway）

---

## 問題 12 / Question 12

**[題目 / Question]**
A DevOps team wants to **centrally manage servers** on AWS and on-premises to collect software inventory, run commands, configure and patch servers at scale. Which AWS service?
DevOps 團隊想**集中管理** AWS 和本地伺服器，進行軟體清單收集、指令執行、配置和修補，推薦哪個服務？

**✅ 正確答案 / Correct Answer：AWS Systems Manager**

**[中文詳解]**
**AWS Systems Manager** 提供統一的用戶介面，可查看多個 AWS 服務的運營資料，並自動化跨 AWS 雲端和本地基礎設施的操作任務，包括：收集軟體清單、執行命令、管理修補程式、配置伺服器。

**[Systems Manager 典型使用場景 / Typical Use Cases]**
- ✅ 大規模收集軟體清單
- ✅ 跨 AWS + 本地執行命令（Run Command）
- ✅ 修補程式管理（Patch Manager）
- ✅ 伺服器配置

---

## 問題 13 / Question 13

**[題目 / Question]**
Which AWS services can be used together to send **alerts whenever the AWS account root user signs in**? (Select two)
哪兩個 AWS 服務可結合使用，在 **AWS 帳戶 root 使用者登入時發送告警**？

**✅ 正確答案 / Correct Answers：**
1. Amazon CloudWatch
2. Amazon Simple Notification Service (Amazon SNS)

**[Root 使用者登入告警方案 / Root User Login Alert Solution]**
```
Root 使用者登入
    ↓
Amazon CloudWatch Events（偵測 userIdentity root 登入事件）
    ↓
Amazon SNS 主題（發送電子郵件/SMS 通知）
    ↓
管理員收到告警
```

> ⚠️ SQS 是訊息佇列，不能發送通知
> ⚠️ Lambda 是運算服務，不能直接監控登入
> ⚠️ Step Functions 協調工作流程，不能監控登入

---

## 問題 14 / Question 14

**[題目 / Question]**
A multi-national organization wants to **connect its on-premises data center with multiple VPCs** for organization-wide collaboration. Which AWS services? (Select two)
跨國組織想將**本地資料中心與多個 VPC 連接**，哪兩個 AWS 服務最有效？

**✅ 正確答案 / Correct Answers：**
1. AWS Transit Gateway（連接多個 VPC 的中央樞紐）
2. AWS Direct Connect（本地到 AWS 的專用連接）

**[最佳解決方案 / Optimal Solution]**
```
本地資料中心（On-premises）
    ↕（AWS Direct Connect — 專用私有連接）
AWS Transit Gateway（中央樞紐，連接所有 VPC）
    ↕
多個 VPC（VPC-1, VPC-2, VPC-3...）
```

**[為什麼不用其他選項 / Why Not Others]**
- VPC Peering → 非傳遞性，不適合多 VPC 場景
- Internet Gateway → 連接網際網路，非私密連接
- AWS Storage Gateway → 混合雲儲存，非網路連接

---

## 問題 15 / Question 15

**[題目 / Question]**
Which of the following is the best practice for application architecture on AWS Cloud?
以下哪個是 AWS 雲端應用程式架構的最佳實踐？

**✅ 正確答案 / Correct Answer：Build loosely coupled components（建構鬆散耦合組件）**

**[微服務架構 / Microservices Architecture]**

| 架構 / Architecture | 特性 / Characteristics | 推薦 |
|---|---|---|
| **Loosely coupled（鬆散耦合）** | **小型獨立服務，透過 API 通信** | **✅ AWS 推薦** |
| Tightly coupled（緊密耦合）| 所有進程緊密耦合，單一服務 | ❌ 風險高 |
| Monolithic（單體）| 所有進程在單一服務中運行 | ❌ 擴展困難 |
| Synchronous（同步）| 流量峰值時可能出現問題 | ❌ 使用 SNS/SQS 替代 |

> **解耦工具**：Amazon SNS、Amazon SQS 可用於解耦微服務組件

---

## 問題 16 / Question 16

**[題目 / Question]**
AWS Shield Advanced provides DDoS protection for web applications running on which resources? (Select two)
AWS Shield Advanced 為哪兩個資源上的 Web 應用程式提供 DDoS 防護？

**✅ 正確答案 / Correct Answers：**
1. Amazon Elastic Compute Cloud (Amazon EC2)
2. Amazon CloudFront

**[AWS Shield Advanced 支援的資源 / Shield Advanced Supported Resources]**
- ✅ Amazon EC2
- ✅ Elastic Load Balancing (ELB)
- ✅ Amazon CloudFront
- ✅ Amazon Route 53
- ✅ AWS Global Accelerator

**[不支援的資源 / NOT Supported]**
- ❌ Amazon S3
- ❌ AWS Elastic Beanstalk
- ❌ AWS IAM

---

## 問題 17 / Question 17

**[題目 / Question]**
An e-commerce company has migrated to AWS Cloud. Which costs is the company **responsible for**?
電商公司已遷移到 AWS 雲端，公司需要承擔哪個費用？

**✅ 正確答案 / Correct Answer：Application software license costs（應用程式軟體授權費用）**

**[遷移到 AWS 後的費用責任 / Cost Responsibility After Migration]**

| 費用類型 / Cost Type | AWS 負責 | 客戶負責 |
|---|---|---|
| 硬體基礎設施 / Hardware infrastructure | ✅ | ❌ |
| 資料中心物理安全 / DC physical security | ✅ | ❌ |
| 伺服器電力 / Server power | ✅ | ❌ |
| **應用程式軟體授權 / Software licenses** | ❌ | **✅** |
| 人力資源成本 / HR costs | ❌ | ✅ |

---

## 問題 18 / Question 18

**[題目 / Question]**
Which of the following are the **serverless computing services** offered by AWS? (Select two)
以下哪兩個是 AWS 提供的**無伺服器運算服務**？

**✅ 正確答案 / Correct Answers：**
1. AWS Fargate
2. AWS Lambda

**[無伺服器 vs 非無伺服器 / Serverless vs Non-Serverless]**

| 服務 / Service | 無伺服器 | 說明 |
|---|---|---|
| **AWS Lambda** | **✅** | 執行代碼，按請求計費 |
| **AWS Fargate** | **✅** | 無伺服器容器運算引擎 |
| Amazon EC2 | ❌ | 需管理伺服器 |
| AWS Elastic Beanstalk | ❌ | 佈建伺服器（PaaS，非無伺服器）|
| Amazon Lightsail | ❌ | 簡化的 VPS，需管理伺服器 |

---

## 問題 19 / Question 19

**[題目 / Question]**
Which Amazon S3 storage class has **NO constraint of a minimum storage duration charge**?
哪個 Amazon S3 儲存類別**沒有最低儲存期限費用限制**？

**✅ 正確答案 / Correct Answer：Amazon S3 Standard**

**[S3 最低儲存期限對照 / Minimum Storage Duration]**

| 儲存類別 / Storage Class | 最低儲存期限 / Min Duration | 取回費用 |
|---|---|---|
| **S3 Standard** | **無限制 / None** ✅ | 無 |
| S3 Intelligent-Tiering | 無限制 / None | 無 |
| S3 Standard-IA | 30 天 / 30 days | 有 |
| S3 One Zone-IA | 30 天 / 30 days | 有 |
| S3 Glacier Flexible Retrieval | 90 天 / 90 days | 有 |
| S3 Glacier Deep Archive | 180 天 / 180 days | 有 |

---

## 問題 20 / Question 20

**[題目 / Question]**
Which of the following is correct regarding Amazon RDS?
以下哪個關於 Amazon RDS 的說法正確？

**✅ 正確答案 / Correct Answer：**
You can use **both read replicas and multi-AZ deployment for disaster recovery**.
您可以將**讀取副本和 Multi-AZ 部署都**用於災難恢復。

**[RDS 部署模式詳解 / RDS Deployment Modes — Advanced]**

| 部署模式 | 主要用途 | DR 能力 | 讀取效能 |
|---|---|---|---|
| **Read Replica** | 讀取擴展 | ✅ 跨 Region 副本可用於 DR | ✅ 提升 |
| **Multi-AZ（單備用）** | 高可用性 | ✅ 同 Region 故障切換 | ❌ 備用不接受讀取 |
| **Multi-AZ（兩個可讀備用）** | 高可用性 + 讀取擴展 | ✅ | ✅ 最大化讀取效能 |

> **重要更新**：RDS Multi-AZ 有兩個版本——**單備用**（不接受讀取）和**兩個可讀備用**（可接受讀取）

---

## 問題 21 / Question 21

**[題目 / Question]**
Which Amazon Route 53 routing policy would you use to route traffic to a **single resource** such as a web server?
哪個 Amazon Route 53 路由策略用於將流量路由到**單一資源**（如 Web 伺服器）？

**✅ 正確答案 / Correct Answer：Simple routing（簡單路由）**

**[Route 53 路由策略快速記憶表 / Routing Policies Quick Reference]**

| 策略 / Policy | 適用場景 |
|---|---|
| **Simple（簡單）** | **路由到單一資源** ✅ |
| Weighted（加權）| 按比例分配到多個資源 |
| Latency-based（延遲）| 最低延遲的 AWS 區域 |
| Failover（容錯移轉）| 主動-被動容錯移轉 |
| Geolocation（地理位置）| 按用戶地理位置 |
| Multivalue Answer | 返回多個健康 IP |

---

## 問題 22 / Question 22

**[題目 / Question]**
Which of the following is available **across all AWS Support plans**?
以下哪個在**所有 AWS 支援方案**中都可用？

**✅ 正確答案 / Correct Answer：AWS Health Dashboard – Your account health（帳戶健康儀表板）**

**[各方案功能可用性 / Feature Availability by Plan]**

| 功能 / Feature | Basic | Developer | Business | Enterprise On-Ramp | Enterprise |
|---|---|---|---|---|---|
| **帳戶健康儀表板** | **✅** | **✅** | **✅** | **✅** | **✅** |
| Trusted Advisor 完整檢查 | ❌ | ❌ | ✅ | ✅ | ✅ |
| 第三方軟體支援 | ❌ | ❌ | ✅ | ✅ | ✅ |
| 24/7 電話支援 | ❌ | ❌ | ✅ | ✅ | ✅ |
| TAM | ❌ | ❌ | ❌ | ✅（共享）| ✅（專屬）|

---

## 問題 23 / Question 23

**[題目 / Question]**
Which of the following is a **container service** of AWS?
以下哪個是 AWS 的**容器服務**？

**✅ 正確答案 / Correct Answer：AWS Fargate**

**[容器相關服務分類 / Container Services]**

| 服務 / Service | 類別 / Category | 說明 |
|---|---|---|
| **AWS Fargate** | **容器 + 無伺服器** | 無伺服器容器運算引擎，與 ECS/EKS 搭配 |
| Amazon ECS | 容器管理 | 可選 EC2 或 Fargate 啟動類型 |
| Amazon ECR | 容器映像倉庫 | 儲存/管理 Docker 映像 |
| Amazon EKS | Kubernetes 管理 | 托管 Kubernetes 服務 |
| AWS Elastic Beanstalk | PaaS 部署 | 不是容器服務 |
| Amazon SageMaker | ML 平台 | 不是容器服務 |
| Amazon SNS | 訊息服務 | 不是容器服務 |

---

## 問題 24 / Question 24

**[題目 / Question]**
Which AWS service can identify **unattached or underutilized Amazon EBS volumes**?
哪個 AWS 服務可以識別**未附加或低使用率的 Amazon EBS 磁碟區**？

**✅ 正確答案 / Correct Answer：AWS Trusted Advisor**

**[中文詳解]**
**AWS Trusted Advisor** 可以檢查 EBS 磁碟區配置，當磁碟區在一段時間內未附加或寫入活動很少時（不包括啟動磁碟區）發出警告，因為這些磁碟區很可能未被使用。磁碟區建立即開始計費。

**[Trusted Advisor EBS 相關檢查 / Trusted Advisor EBS Checks]**
- 未附加或低使用率的 EBS 磁碟區（成本優化類別）

> ⚠️ AWS Config → 配置歷史（不識別低使用率）
> ⚠️ CloudWatch → 可設定告警但需手動配置閾值
> ⚠️ Inspector → 安全評估服務

---

## 問題 25 / Question 25

**[題目 / Question]**
A media company uploads audio and video files to a centralized S3 bucket **from geographically dispersed locations**. Which solution can optimize transfer speeds?
媒體公司從**地理位置分散的地點**將媒體文件上傳到集中的 S3 儲存桶，哪個解決方案可優化傳輸速度？

**✅ 正確答案 / Correct Answer：Amazon S3 Transfer Acceleration (S3TA)**

**[中文詳解]**
**Amazon S3 Transfer Acceleration (S3TA)** 利用 Amazon CloudFront 全球分佈的 AWS 邊緣節點，加快客戶端和 S3 儲存桶之間長距離的文件傳輸速度。資料到達邊緣節點後，透過優化的網路路徑路由到 S3 儲存桶。

**[上傳優化服務比較 / Upload Speed Services]**

| 服務 / Service | 適用場景 | 優化方向 |
|---|---|---|
| **S3 Transfer Acceleration** | **跨地理位置上傳到 S3** | **上傳速度** ✅ |
| Amazon CloudFront | 內容交付（下載）| 下載速度 |
| AWS Global Accelerator | 應用程式效能 | TCP/UDP 應用效能 |
| AWS Direct Connect | 本地到 AWS 專用連接 | 持續高頻寬 |

---

## 問題 26 / Question 26

**[題目 / Question]**
Which AWS storage service offers **Lifecycle configuration** for cost-optimal storage?
哪個 AWS 儲存服務提供**生命週期配置**以實現最優成本儲存？

**✅ 正確答案 / Correct Answer：Amazon Simple Storage Service (Amazon S3)**

**[S3 生命週期配置兩種動作 / S3 Lifecycle Actions]**

| 動作類型 / Action Type | 說明 |
|---|---|
| **Transition actions（轉換動作）** | 定義物件何時轉移到另一個儲存類別（例如 30 天後轉到 Standard-IA，1 年後轉到 Glacier）|
| **Expiration actions（到期動作）** | 定義物件何時到期（S3 代表您刪除到期的物件）|

**[其他服務是否支援生命週期 / Lifecycle Support]**
- ❌ Amazon EBS → 不支援生命週期配置
- ❌ EC2 Instance Store → 不支援生命週期配置
- ❌ AWS Storage Gateway → 不支援生命週期配置

---

## 問題 27 / Question 27

**[題目 / Question]**
Which AWS authentication mechanism supports an MFA device that you can **plug into a USB port** on your computer?
哪個 AWS 身份驗證機制支援可以**插入電腦 USB 端口**的 MFA 設備？

**✅ 正確答案 / Correct Answer：U2F security key（U2F 安全金鑰）**

**[MFA 類型完整比較 / MFA Types Comparison]**

| MFA 類型 / Type | 操作方式 | 實體設備 | 適用場景 |
|---|---|---|---|
| **U2F Security Key** | **插入 USB，點擊設備** | **✅ USB 金鑰** | 出差但帶設備 |
| Hardware MFA | 產生 6 位數代碼，手動輸入 | ✅ 硬體設備 | 固定辦公 |
| Virtual MFA | 手機 App 產生代碼 | ❌ 手機 App | 出差不帶設備 |
| SMS MFA | 手機收到 6 位數簡訊 | ❌ 手機 | 簡單便捷 |

---

## 問題 28 / Question 28

**[題目 / Question]**
Bob and Susan are in the same AWS Organization. Susan has 5 Reserved Instances, Bob has 0. During one hour, Susan uses 3, Bob uses 6 (total 9). Which statements are correct about consolidated billing? (Select two)
Bob 和 Susan 在同一 AWS 組織中。Susan 有 5 個 RI，Bob 有 0 個。某小時 Susan 使用 3 個，Bob 使用 6 個（總計 9 個），關於整合計費的哪兩個說法正確？

**✅ 正確答案 / Correct Answers：**
1. AWS bills **five** instances as Reserved Instances, remaining **four** as regular instances
2. Bob receives cost-benefit from Susan's RIs **only if he launches in the same AZ** where Susan purchased her RIs

**[整合計費 RI 共享規則 / Consolidated Billing RI Sharing Rules]**

| 規則 / Rule | 說明 |
|---|---|
| **RI 數量** | Susan 有 5 個 RI → AWS 按 RI 計費 5 個，剩餘 4 個按正常計費 |
| **AZ 要求** | Bob 必須在 Susan 購買 RI 的**相同 AZ**啟動執行個體 |
| RI 共享原則 | 整合計費將所有帳戶視為一個，RI 效益可跨帳戶共享 |

> ⚠️ 不是「相同 Region」（那是錯誤的），而是「相同 **AZ**」
> ⚠️ Bob 不需要自己有 RI 也能享受 Susan RI 的折扣效益

---

## 問題 29 / Question 29

**[題目 / Question]**
Which AWS service will help you **deploy application code automatically** to an Amazon EC2 instance?
哪個 AWS 服務可以幫助您**自動部署應用程式代碼**到 Amazon EC2 執行個體？

**✅ 正確答案 / Correct Answer：AWS CodeDeploy**

**[AWS 開發者工具詳細比較 / Developer Tools Detailed Comparison]**

| 服務 / Service | 功能 / Function | 能否部署到 EC2 |
|---|---|---|
| **AWS CodeDeploy** | **自動部署代碼到 EC2、Fargate、Lambda、本地** | **✅** |
| AWS CodeBuild | 編譯源代碼、執行測試、生成套件 | ❌（建構不是部署）|
| AWS CodePipeline | 整合 CI/CD 管道（協調者）| ❌（需要 CodeDeploy 執行部署）|
| AWS Elastic Beanstalk | 端到端應用平台，自動處理容量等 | ❌（平台服務，非代碼部署自動化）|
| AWS CloudFormation | 基礎設施即代碼（IaC）| ❌（佈建資源，非部署代碼）|

---

## 問題 30 / Question 30

**[題目 / Question]**
Which scenarios can be handled by AWS Lambda? (Select two)
以下哪兩個場景可以由 AWS Lambda 處理？

**✅ 正確答案 / Correct Answers：**
1. AWS Lambda can be used for **preprocessing data** before storing in S3
2. AWS Lambda can execute code **in response to events** such as updates to DynamoDB tables

**[Lambda 可以做 vs 不能做 / Lambda Can vs Cannot]**

| 能做 / CAN Do | 不能做 / CANNOT Do |
|---|---|
| ✅ S3 事件觸發（上傳處理）| ❌ 安裝軟體/資料庫（無法存取物理伺服器）|
| ✅ DynamoDB 更新觸發 | ❌ 安裝容器服務 |
| ✅ 資料預處理和過濾 | ❌ 儲存敏感環境變數（Lambda 非存儲服務）|
| ✅ 即時資料轉換 | ❌ 執行超過 15 分鐘的任務 |
| ✅ 圖片縮圖、視訊轉碼 | |

---

## 問題 31 / Question 31

**[題目 / Question]**
Which pillar of AWS Well-Architected Framework is responsible for **selecting the right resource types and sizes based on workload requirements**?
AWS Well-Architected Framework 哪個支柱負責**根據工作負載需求選擇正確的資源類型和大小**？

**✅ 正確答案 / Correct Answer：Performance Efficiency（效能效率）**

**[六大支柱關鍵字對照 / Six Pillars Keywords]**

| 支柱 / Pillar | 關鍵字 / Keywords |
|---|---|
| Operational Excellence | IaC、自動化操作程序 |
| Security | 保護資訊和系統 |
| Reliability | 從故障恢復、動態獲取資源 |
| **Performance Efficiency** | **選擇正確資源類型和大小** |
| Cost Optimization | 避免不必要費用 |
| Sustainability | 降低環境影響 |

---

## 問題 32 / Question 32

**[題目 / Question]**
A media company wants to convert **English language subtitles into Spanish**. Which AWS service?
媒體公司想將**英語字幕轉換為西班牙語**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：Amazon Translate**

**[AI/ML 語言/語音服務完整對照 / AI/ML Language & Speech Services]**

| 服務 / Service | 功能 / Function |
|---|---|
| **Amazon Translate** | **語言翻譯（英語 → 西班牙語）** ✅ |
| Amazon Transcribe | 語音 → 文字（自動語音識別 ASR）|
| Amazon Polly | 文字 → 語音（TTS）|
| Amazon Rekognition | 圖像/視訊分析 |
| Amazon Comprehend | 自然語言處理（NLP）|
| Amazon Lex | 對話介面（聊天機器人）|

---

## 問題 33 / Question 33

**[題目 / Question]**
Which is best-suited for **load-balancing HTTP and HTTPS traffic**?
哪個最適合**負載均衡 HTTP 和 HTTPS 流量**？

**✅ 正確答案 / Correct Answer：Application Load Balancer（應用程式負載均衡器）**

**[ELB 三種類型比較 / ELB Three Types Comparison]**

| 類型 / Type | 最適合 / Best For | 協議 / Protocols |
|---|---|---|
| **Application Load Balancer (ALB)** | **HTTP/HTTPS，微服務，容器** | Layer 7 |
| Network Load Balancer (NLB) | 極高效能，TCP/UDP/TLS | Layer 4 |
| Gateway Load Balancer (GWLB) | 第三方網路設備 | Layer 3 |

---

## 問題 34 / Question 34

**[題目 / Question]**
As per the AWS Shared Responsibility Model, which is a responsibility of AWS from a security and compliance point of view?
根據 AWS 共同責任模型，哪項是 AWS 的安全與合規責任？

**✅ 正確答案 / Correct Answer：Patching networking infrastructure（修補網路基礎設施）**

**[AWS vs 客戶責任 / AWS vs Customer Responsibility]**

| 責任 / Responsibility | AWS | 客戶 |
|---|---|---|
| **修補網路基礎設施** | **✅** | ❌ |
| Service and Communications Protection | ❌ | ✅ |
| Identity and Access Management | ❌ | ✅ |
| 修補 Guest OS 和應用程式 | ❌ | ✅ |

---

## 問題 35 / Question 35

**[題目 / Question]**
According to the AWS Shared Responsibility Model, which are customer responsibilities for **AWS IAM**? (Select two)
根據 AWS 共同責任模型，以下哪兩個是客戶對 **AWS IAM** 的責任？

**✅ 正確答案 / Correct Answers：**
1. Analyze user access patterns and review AWS IAM permissions（分析用戶存取模式並審查 IAM 權限）
2. Enable MFA on all accounts（在所有帳戶上啟用 MFA）

**[IAM 共同責任劃分 / IAM Shared Responsibility]**

| 責任項目 / Item | AWS | 客戶 |
|---|---|---|
| **啟用所有帳戶的 MFA** | ❌ | **✅** |
| **分析存取模式和審查 IAM 權限** | ❌ | **✅** |
| 管理全球網路安全基礎設施 | ✅ | ❌ |
| 底層軟體基礎設施配置和漏洞分析 | ✅ | ❌ |
| 底層軟體基礎設施合規驗證 | ✅ | ❌ |

---

## 問題 36 / Question 36

**[題目 / Question]**
Amazon EC2 **Spot instances** are a best-fit for which scenario?
Amazon EC2 **Spot 執行個體**最適合哪個場景？

**✅ 正確答案 / Correct Answer：To run any containerized workload with Amazon ECS that **can be interrupted**（執行**可中斷**的 ECS 容器工作負載）**

**[Spot 執行個體適用場景 / Spot Instance Use Cases]**

| 場景 / Scenario | Spot 適用 | 原因 |
|---|---|---|
| **可中斷的容器工作負載（ECS）** | **✅ 最佳** | 容器無狀態、容錯，最高 90% 折扣 |
| 定時排程工作（每天固定時間）| ❌ | 無法保證特定時間可用 |
| Amazon RDS 資料庫 | ❌ | 資料庫容量不能被隨意收回 |
| 關鍵批次處理 | ❌ | 業務關鍵工作負載不適合被中斷 |

---

## 問題 37 / Question 37

**[題目 / Question]**
The DevOps team has set up EC2 instances **across two AWS Regions**. Which of the following characterizes this application architecture?
DevOps 團隊在**兩個 AWS Region**部署了 EC2 執行個體，這個應用架構的特徵是什麼？

**✅ 正確答案 / Correct Answer：Deploying across two AWS Regions improves **availability**（跨兩個 Region 部署提高**可用性**）**

**[多 Region 部署的優勢 / Multi-Region Deployment Benefits]**

| 優勢 / Benefit | 是否正確 | 備註 |
|---|---|---|
| **提高可用性 / Improve availability** | **✅ 正確** | 隔離故障，保持可用 |
| 提高敏捷性 / Improve agility | ❌ | 敏捷性是快速創新，非多 Region 部署 |
| 提高安全性 / Improve security | ❌ | 安全性由 IAM、加密等決定，非 Region 數量 |
| 提高可擴展性 / Improve scalability | ❌ | 可擴展性透過 Auto Scaling + ALB 實現 |

---

## 問題 38 / Question 38

**[題目 / Question]**
A cargo company has CRM applications that need to be accessible 24/7 but are not mission-critical. In a disaster, they can run on fewer instances for some time. Which disaster recovery strategy?
貨運公司的 CRM 應用需要 24/7 可用但非任務關鍵，災難時可臨時在較少執行個體上運行，哪個 DR 策略？

**✅ 正確答案 / Correct Answer：Warm Standby strategy（暖備用策略）**

**[四種 DR 策略比較 / Four DR Strategies — Must Know!]**

| 策略 / Strategy | RTO/RPO | 成本 | 說明 |
|---|---|---|---|
| Backup & Restore | 最高 / Highest | 最低 | 備份還原，停機時間長 |
| **Pilot Light** | 中 / Medium | 低 | 最小核心運行，需要擴展才能服務請求 |
| **Warm Standby** | 低 / Low | 中 | 功能完整但容量縮減，**立即可處理請求** ✅ |
| Multi-site Active-Active | 最低 / Lowest | 最高 | 全容量雙主動，適合任務關鍵 |

> **暖備用 vs 試驗燈的關鍵區別**：
> - Pilot Light → DR 環境需要額外步驟才能提供服務
> - **Warm Standby** → DR 環境立即可以（以縮減容量）提供服務

---

## 問題 39 / Question 39

**[題目 / Question]**
AWS Marketplace facilitates which use-cases? (Select two)
AWS Marketplace 支援哪兩個使用案例？

**✅ 正確答案 / Correct Answers：**
1. Sell **Software as a Service (SaaS)** solutions to AWS customers
2. AWS customers can buy software bundled into **customized AMIs** by Marketplace sellers

**[AWS Marketplace 兩種銷售方式 / Two Selling Methods]**

| 方式 / Method | 說明 |
|---|---|
| **Amazon Machine Image (AMI)** | 偏好選項；免費或付費（按小時/月）；支援 BYOL |
| **Software as a Service (SaaS)** | 運行在 AWS 上的 SaaS 解決方案 |

**[AWS Marketplace 不能做的 / What Marketplace Cannot Do]**
- ❌ 購買合規文件（那是 AWS Artifact）
- ❌ 購買 EC2 Reserved Instances（透過 EC2 控制台購買）
- ❌ 申請 AWS Direct Connect（透過 AWS 控制台申請）

---

## 問題 40 / Question 40

**[題目 / Question]**
Which AWS service can be used to set up **billing alarms** to monitor estimated charges on your AWS account?
哪個 AWS 服務可用於設置**計費告警**以監控 AWS 帳戶的估算費用？

**✅ 正確答案 / Correct Answer：Amazon CloudWatch**

**[CloudWatch 計費告警特點 / CloudWatch Billing Alarm Features]**
- 計費指標資料每天更新數次並發送到 CloudWatch
- 計費告警由 CloudWatch 觸發，訊息透過 SNS 發送
- 計費指標資料儲存在 **us-east-1（美國東部維吉尼亞北部）**
- 告警只在**實際費用**超過閾值時觸發（不使用使用量投影）

**[CloudWatch Billing vs AWS Budgets — Exam Alert!]**

| 特性 / Feature | CloudWatch Billing | AWS Budgets |
|---|---|---|
| 告警觸發 | 實際費用超過閾值 | 實際費用**或預測費用**超過 |
| 靈活性 | 較簡單 | 更靈活（多維度）|

---

## 問題 41 / Question 41

**[題目 / Question]**
Which benefit of Cloud Computing allows AWS to offer **lower pay-as-you-go prices** as usage from hundreds of thousands of customers is aggregated?
雲端運算的哪個優勢讓 AWS 能夠提供**更低的按使用量定價**，因為數十萬客戶的使用量在雲端彙總？

**✅ 正確答案 / Correct Answer：Massive economies of scale（大規模經濟）**

**[雲端六大優勢 — 定義辨別 / Six Cloud Advantages]**

| 優勢 / Advantage | 定義 / Definition |
|---|---|
| **Massive economies of scale（大規模經濟）** | **數十萬客戶彙總使用量 → 更低的按使用量定價** |
| Trade capital expense for variable expense | 資本支出換可變支出 |
| Increased speed and agility | 分鐘內獲得 IT 資源（原來需要幾週）|
| Stop guessing capacity | 停止猜測容量需求 |
| Stop spending on data centers | 專注業務而非運維 |
| Go global in minutes | 幾分鐘內全球部署 |

---

## 問題 42 / Question 42

**[題目 / Question]**
Which AWS service can be used to receive alerts when **Amazon EC2 Reserved Instances (RI) utilization drops below a certain threshold**?
哪個 AWS 服務可在 **EC2 Reserved Instances 使用率低於某個閾值**時接收告警？

**✅ 正確答案 / Correct Answer：AWS Budgets**

**[中文詳解]**
**AWS Budgets** 可設置預留使用率或覆蓋率目標，並在利用率低於您定義的閾值時接收告警。您可以定義使用率閾值，當 RI 使用率低於該閾值時接收告警，幫助您查看 RI 是否未使用或利用率不足。

**[RI 使用率監控工具比較 / RI Utilization Monitoring]**

| 工具 / Tool | 可生成 RI 報告 | 可設置低使用率告警 |
|---|---|---|
| **AWS Budgets** | ✅ | **✅** |
| AWS Cost Explorer | ✅（生成 RI 報告）| ❌（不能設置告警）|
| AWS Trusted Advisor | ✅（建議）| ❌ |

---

## 問題 43 / Question 43

**[題目 / Question]**
Which AWS entity lists all users in your account and the status of their credentials including **passwords, access keys, and MFA devices**?
哪個 AWS 實體列出您帳戶中的所有使用者及其憑證狀態，包括**密碼、存取金鑰和 MFA 設備**？

**✅ 正確答案 / Correct Answer：Credentials Report（憑證報告）**

**[中文詳解]**
**IAM 憑證報告**可以產生並下載，列出帳戶中所有使用者及其各種憑證的狀態，包括密碼、存取金鑰和 MFA 設備。可協助審計和合規工作，審查憑證生命週期要求的影響，可提供給外部審計員。

**[憑證報告 vs 其他 IAM 工具 / Credentials Report vs Other IAM Tools]**

| 工具 / Tool | 用途 / Purpose |
|---|---|
| **Credentials Report** | **列出所有使用者及憑證狀態（密碼、金鑰、MFA）** |
| Access Advisor | 查看使用者/角色上次使用各服務的時間 |
| IAM Policy Simulator | 測試 IAM 策略效果 |

---

## 問題 44 / Question 44

**[題目 / Question]**
Which of the following entities are **part of an Amazon VPC** in the AWS Cloud? (Select two)
以下哪兩個是 AWS 雲端中 **Amazon VPC 的組成部分**？

**✅ 正確答案 / Correct Answers：**
1. Subnet（子網路）
2. Internet Gateway（網際網路閘道）

**[Amazon VPC 關鍵概念 / VPC Key Concepts]**

| 組件 / Component | 是否是 VPC 的一部分 | 說明 |
|---|---|---|
| **Subnet** | **✅** | VPC 內的 IP 地址範圍 |
| **Internet Gateway** | **✅** | 允許 VPC 資源與網際網路通信 |
| Route table | ✅ | 決定網路流量方向的規則 |
| VPC Endpoint | ✅ | 私密連接 AWS 服務 |
| AWS Storage Gateway | ❌ | 混合雲儲存服務，非 VPC 組件 |
| Amazon API Gateway | ❌ | API 管理服務，非 VPC 組件 |
| S3 Object | ❌ | S3 物件，非 VPC 組件 |

---

## 問題 45 / Question 45

**[題目 / Question]**
Which AWS service will you use to provision the same AWS infrastructure **across multiple AWS accounts and regions**?
哪個 AWS 服務可在**多個 AWS 帳戶和 Region**中佈建相同的 AWS 基礎設施？

**✅ 正確答案 / Correct Answer：AWS CloudFormation**

**[中文詳解]**
**AWS CloudFormation StackSets** 透過單一操作擴展了堆疊功能，使您能夠跨多個帳戶和 Region 建立、更新或刪除堆疊。使用管理員帳戶，您定義和管理 CloudFormation 模板，並使用模板作為在指定 Region 的目標帳戶中佈建堆疊的基礎。

**[基礎設施即代碼服務對比 / IaC Services Comparison]**

| 服務 / Service | 跨帳戶/Region | 功能 |
|---|---|---|
| **AWS CloudFormation (StackSets)** | **✅** | **跨帳戶/Region 佈建基礎設施** |
| AWS CDK | 可以（透過 CloudFormation）| 代碼方式定義 IaC |
| AWS CodeDeploy | ❌ | 代碼部署自動化 |
| AWS Systems Manager | ❌ | 運營管理 |

---

## 問題 46 / Question 46

**[題目 / Question]**
Which AWS entity enables you to **privately connect your VPC to Amazon SQS**?
哪個 AWS 實體可讓您**私密連接 VPC 到 Amazon SQS**？

**✅ 正確答案 / Correct Answer：VPC Interface Endpoint（VPC 介面端點）**

**[VPC Endpoint 類型 — 重要考點 / VPC Endpoint Types — Exam Alert!]**

| 端點類型 / Type | 說明 | 支援的服務 |
|---|---|---|
| **VPC Interface Endpoint** | **帶有私有 IP 的彈性網路介面（ENI）** | **除 S3/DynamoDB 外的大多數 AWS 服務（包括 SQS）** |
| VPC Gateway Endpoint | 在路由表中指定的閘道 | **只有 S3 和 DynamoDB** |

> **超高頻考點**：
> - **Gateway Endpoint** → **只支援 S3 和 DynamoDB**
> - **Interface Endpoint** → **所有其他服務**（SQS、SNS、CloudWatch、Systems Manager 等）
> - **S3 同時支援**兩種端點

---

## 問題 47 / Question 47

**[題目 / Question]**
AWS Organizations provides which benefits? (Select two)
AWS Organizations 提供哪兩個優勢？

**✅ 正確答案 / Correct Answers：**
1. **Volume discounts** for EC2 and S3 aggregated across member accounts（跨成員帳戶彙總的**批量折扣**）
2. **Share reserved EC2 instances** amongst member accounts（在成員帳戶之間**共享預留 EC2 執行個體**）

**[AWS Organizations 主要功能 / Key Features of AWS Organizations]**

| 功能 / Feature | 說明 |
|---|---|
| ✅ 批量折扣 | EC2 和 S3 使用量彙總，享受更大折扣 |
| ✅ 共享 RI | 跨帳戶共享預留執行個體 |
| ✅ 集中計費 | 單一付款方式 |
| ✅ 帳戶自動建立 | 自動化帳戶建立 |
| ✅ SCPs | 服務控制策略，治理和合規 |

**[組織不能做的 / What Organizations CANNOT Do]**
- ❌ 跨帳戶部署修補程式（那是 Systems Manager）
- ❌ 檢查 EC2 漏洞（那是 Amazon Inspector）
- ❌ 佈建 Spot 執行個體（那是 EC2 功能）

---

## 問題 48 / Question 48

**[題目 / Question]**
Which entity can connect to an EC2 instance from Mac OS, Windows, or Linux computer **via a browser-based client**?
哪個實體可以從 Mac OS、Windows 或 Linux 電腦**透過瀏覽器客戶端**連接到 EC2 執行個體？

**✅ 正確答案 / Correct Answer：Amazon EC2 Instance Connect**

**[EC2 連接方式比較 / EC2 Connection Methods]**

| 方法 / Method | 瀏覽器連接 | 支援的 OS | 特點 |
|---|---|---|---|
| **EC2 Instance Connect** | **✅** | **Mac/Windows/Linux** | IAM 控制、記錄到 CloudTrail |
| SSH | ❌（命令列）| Mac/Linux | 需要金鑰對 |
| Putty | ❌（客戶端）| **僅 Windows** | 需要金鑰對 |
| Session Manager | ✅（透過 Systems Manager）| 所有 | 不需要 Port 22 |
| AWS Direct Connect | ❌ | N/A | 網路連接服務，非 EC2 連接 |

---

## 問題 49 / Question 49

**[題目 / Question]**
Which is the MOST cost-effective EC2 instance purchasing option for **short-term, spiky and critical workloads**?
對於**短期、突發且關鍵**的工作負載，哪個 EC2 定價選項最具成本效益？

**✅ 正確答案 / Correct Answer：On-Demand Instance（隨需執行個體）**

**[EC2 選擇指南 / EC2 Selection Guide]**

| 工作負載類型 / Workload | 最佳選擇 / Best Option |
|---|---|
| **短期 + 突發 + 關鍵** | **On-Demand** ✅ |
| 長期 + 穩定 + 可預測 | Reserved Instance (RI) |
| 可中斷 + 彈性 | Spot Instance |
| 授權軟體 + 合規 | Dedicated Host |
| 短期 + 突發 + 非關鍵 | Spot Instance（更便宜）|

---

## 問題 50 / Question 50

**[題目 / Question]**
Which Amazon S3 storage classes do **not charge any data retrieval fee**? (Select two)
哪兩個 Amazon S3 儲存類別**不收取任何資料取回費用**？

**✅ 正確答案 / Correct Answers：**
1. Amazon S3 Standard
2. Amazon S3 Intelligent-Tiering

**[S3 取回費用對照表 / S3 Retrieval Fee Summary]**

| 儲存類別 / Storage Class | 取回費用 / Retrieval Fee |
|---|---|
| **S3 Standard** | **免費 / Free** ✅ |
| **S3 Intelligent-Tiering** | **免費 / Free** ✅ |
| S3 Standard-IA | 有 / Yes |
| S3 One Zone-IA | 有 / Yes |
| S3 Glacier Instant Retrieval | 有 / Yes |
| S3 Glacier Flexible Retrieval | 有 / Yes |
| S3 Glacier Deep Archive | 有 / Yes |

> **記憶法**：只有 **S3 Standard** 和 **S3 Intelligent-Tiering** 無取回費用

---

## 問題 51 / Question 51

**[題目 / Question]**
Which AWS service can **forecast your AWS account usage and costs**?
哪個 AWS 服務可以**預測您的 AWS 帳戶使用量和費用**？

**✅ 正確答案 / Correct Answer：AWS Cost Explorer**

**[成本管理工具功能對照 / Cost Management Tools]**

| 工具 / Tool | 預測 / Forecast | 歷史資料 | 主要功能 |
|---|---|---|---|
| **AWS Cost Explorer** | **✅** | 最多 12 個月 | 視覺化 + 預測費用趨勢 |
| AWS Budgets | ❌（設置預測告警）| N/A | 自定義預算告警 |
| AWS CUR | ❌ | 詳細歷史 | 最詳細的費用資料，輸出到 S3 |
| AWS Pricing Calculator | ❌（事前估算）| N/A | 建構前估算費用 |

---

## 問題 52 / Question 52

**[題目 / Question]**
Which AWS storage service can be **directly used with on-premises systems**?
哪個 AWS 儲存服務可以**直接與本地系統一起使用**？

**✅ 正確答案 / Correct Answer：Amazon Elastic File System (Amazon EFS)**

**[中文詳解]**
**Amazon EFS** 可與 AWS 雲端服務和**本地資源**一起使用。要從本地存取 EFS 文件系統，需要有 AWS Direct Connect 或 AWS VPN 連接。使用標準 Linux 掛載命令掛載 EFS 文件系統到本地 Linux 伺服器。

**[儲存服務本地存取性 / Storage Services On-Premises Access]**

| 服務 / Service | 本地存取 / On-premises | 方式 |
|---|---|---|
| **Amazon EFS** | **✅ 直接** | 透過 Direct Connect 或 VPN 掛載 |
| Amazon EBS | ❌ | 只能掛載到 EC2 |
| EC2 Instance Store | ❌ | 實體附加在主機，無法本地存取 |
| Amazon S3 | ❌ 直接 | 只能透過 AWS Storage Gateway 存取 |

---

## 問題 53 / Question 53

**[題目 / Question]**
Which entity should be used for an **EC2 instance to access a DynamoDB table**?
哪個實體應用於讓 **EC2 執行個體存取 DynamoDB 表格**？

**✅ 正確答案 / Correct Answer：IAM role（IAM 角色）**

**[EC2 存取 AWS 服務的最佳實踐 / Best Practice for EC2 Accessing AWS Services]**

| 方法 / Method | 推薦 | 說明 |
|---|---|---|
| **IAM Role** | **✅ 最佳** | **提供臨時安全憑證，自動輪換，無需管理長期金鑰** |
| IAM User Access Keys | ❌ 不建議 | 長期憑證，需要手動管理，存在安全風險 |
| Amazon Cognito | ❌ | 用戶身份認證，非 EC2 到 AWS 服務 |
| AWS KMS | ❌ | 金鑰管理，非存取控制 |

> **AWS 最佳實踐**：使用臨時安全憑證（IAM 角色）而非長期存取金鑰

---

## 問題 54 / Question 54

**[題目 / Question]**
A financial company wants to **compare the cost of running IT infrastructure on-premises vs AWS Cloud**. Which AWS service?
金融公司想**比較在本地和 AWS 雲端運行 IT 基礎設施的費用**，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Pricing Calculator**

**[中文詳解]**
**AWS Pricing Calculator** 讓您探索 AWS 服務並為您在 AWS 上的使用案例建立費用估算，可在建構前模擬解決方案，探索定價點和計算方式，幫助比較本地 vs AWS 雲端的費用。

> **AWS 也提供 Migration Evaluator（前身為 TSO Logic）**：為 AWS 雲端規劃和遷移建立資料驅動的商業案例，是更專業的本地 vs 雲端費用比較工具。

---

## 問題 55 / Question 55

**[題目 / Question]**
A social media company wants the MOST cost-optimal EC2 deployment strategy. Which two options would you recommend? (Select two)
社群媒體公司想要最具成本效益的 EC2 部署策略，推薦哪兩個選項？

**✅ 正確答案 / Correct Answers：**
1. Use **Spot Instances** for ad-hoc jobs that can be interrupted
2. Use **Reserved Instances (RI)** to run applications with **predictable usage** over the next one year

**[EC2 成本最優化選擇 / Cost-Optimal EC2 Selection]**

| 使用案例 / Use Case | 最佳選擇 | 次佳 |
|---|---|---|
| **可中斷的臨時工作** | **Spot（最高 90% 折扣）** | On-Demand |
| **可預測的長期工作負載（1 年+）** | **Reserved Instance（最高 72%）** | On-Demand |
| 短期 + 關鍵 | On-Demand | Reserved |

---

## 問題 56 / Question 56

**[題目 / Question]**
AWS Trusted Advisor can provide alerts on which **common security misconfigurations**? (Select two)
AWS Trusted Advisor 可對哪兩個**常見安全錯誤配置**提供告警？

**✅ 正確答案 / Correct Answers：**
1. When you **allow public access to Amazon S3 buckets**（允許公開存取 S3 儲存桶）
2. When you **don't turn on user activity logging** (AWS CloudTrail)（未啟用 CloudTrail 用戶活動記錄）

**[Trusted Advisor 安全類告警 / Security Category Alerts]**

| 告警類型 / Alert Type | 支援 |
|---|---|
| ✅ S3 儲存桶公開存取 | ✅ |
| ✅ 未啟用 CloudTrail | ✅ |
| ✅ 某些端口開放（易受駭客攻擊）| ✅ |
| ✅ 未建立 IAM 帳戶 | ✅ |
| ✅ root 帳戶未啟用 MFA | ✅ |
| ❌ S3 物件未加標籤 | ❌（非安全威脅）|
| ❌ 共享 IAM 憑證 | ❌（客戶責任，Trusted Advisor 無法偵測）|

---

## 問題 57 / Question 57

**[題目 / Question]**
Which of the following is a **perspective** of the AWS Cloud Adoption Framework (AWS CAF)?
以下哪個是 AWS 雲端採用框架 (AWS CAF) 的**視角**？

**✅ 正確答案 / Correct Answer：Business（業務）**

**[AWS CAF 六大視角 / AWS CAF Six Perspectives — Must Memorize!]**

| 視角 / Perspective | 焦點 / Focus |
|---|---|
| **Business（業務）** | 策略對齊、IT 投資與業務目標 |
| **People（人員）** | 組織變革、雲端流暢性 |
| **Governance（治理）** | 風險管理、合規、財務管理 |
| **Platform（平台）** | 雲端設計和實施、平台工程 |
| **Security（安全）** | 資料保護、漏洞管理 |
| **Operations（運營）** | 日常運營、效能管理 |

> ⚠️ Process、Product、Architecture 均**不是** AWS CAF 視角

---

## 問題 58 / Question 58

**[題目 / Question]**
Which AWS service can host a **static website** with the LEAST effort?
哪個 AWS 服務可以用最少努力託管**靜態網站**？

**✅ 正確答案 / Correct Answer：Amazon Simple Storage Service (Amazon S3)**

**[靜態網站託管 / Static Website Hosting]**
- ✅ S3 → 直接設置儲存桶為網站，啟用網站託管，設置許可，建立索引文件
- ❌ EFS → 需要掛載到 EC2 才能作為靜態網站
- ❌ S3 Glacier → 用於存檔，不能託管網站
- ❌ AWS Storage Gateway → 混合雲儲存，不能託管網站

---

## 問題 59 / Question 59

**[題目 / Question]**
Which of the following can you use to run a **bootstrap script** while launching an Amazon EC2 instance?
啟動 Amazon EC2 執行個體時，哪個可用於執行**啟動腳本**？

**✅ 正確答案 / Correct Answer：Amazon EC2 instance user data（EC2 執行個體使用者資料）**

**[EC2 Metadata vs User Data vs AMI Data / 元資料 vs 使用者資料 vs AMI 資料]**

| 項目 / Item | 用途 / Purpose | 說明 |
|---|---|---|
| **EC2 Instance User Data** | **執行啟動腳本（bootstrap script）** | 啟動時以 root 身份執行的腳本或配置 |
| EC2 Instance Metadata | 查看執行個體資訊 | ami-id、public-ip、instance-id 等 |
| EC2 AMI data | 虛構選項 | 干擾項 |
| EC2 configuration data | 虛構選項 | 干擾項 |

---

## 問題 60 / Question 60

**[題目 / Question]**
Which entity ensures that your EC2 application always has the **right amount of capacity** to handle the **current traffic demand**?
哪個實體確保您的 EC2 應用程式始終具有處理**當前流量需求**所需的**正確容量**？

**✅ 正確答案 / Correct Answer：Amazon EC2 Auto Scaling**

**[EC2 Auto Scaling vs 負載均衡 / Auto Scaling vs Load Balancing]**

| 服務 / Service | 功能 / Function | 自動調整容量 |
|---|---|---|
| **Amazon EC2 Auto Scaling** | **確保正確數量的 EC2 執行個體處理負載** | **✅** |
| Application Load Balancer | 在多個目標間分配流量 | ❌（分配，不擴展）|
| Network Load Balancer | 高效能 TCP/UDP 負載均衡 | ❌（分配，不擴展）|
| Multi-AZ deployment | 高可用性容錯移轉 | ❌（可用性，不擴展）|

---

## 問題 61 / Question 61

**[題目 / Question]**
Which are recommended security best practices for the **AWS account root user**? (Select two)
以下哪兩個是 **AWS 帳戶 root 使用者**的推薦安全最佳實踐？

**✅ 正確答案 / Correct Answers：**
1. **Enable MFA** for the AWS account root user
2. Set up an **IAM user with administrator permissions** and do **not** use root user for administrative tasks

**[Root 使用者安全最佳實踐清單 / Root User Security Best Practices]**

| 最佳實踐 / Best Practice | 建議 |
|---|---|
| ✅ 啟用 MFA | 強烈建議 |
| ✅ 建立 IAM 管理員用戶 | 日常操作使用 IAM，不用 root |
| ✅ 不建立 root 存取金鑰（如已有，刪除）| 避免長期憑證 |
| ✅ 強密碼 | 保護控制台存取 |
| ❌ 停用 MFA（害怕設備遺失鎖定帳戶）| 不正確；MFA 遺失有恢復程序 |
| ❌ 在 S3 加密文件中儲存 root 金鑰 | 不正確；應刪除 root 金鑰 |
| ❌ 與管理員共享 root 憑證 | 嚴禁 |

---

## 問題 62 / Question 62

**[題目 / Question]**
Reserved Instance (RI) pricing is available for which AWS services? (Select two)
哪兩個 AWS 服務提供 Reserved Instance (RI) 定價？

**✅ 正確答案 / Correct Answers：**
1. Amazon Elastic Compute Cloud (Amazon EC2)
2. Amazon Relational Database Service (Amazon RDS)

**[RI 定價可用服務 / Services with RI Pricing]**

| 服務 / Service | RI 可用 | 說明 |
|---|---|---|
| **Amazon EC2** | **✅** | EC2 Reserved Instances |
| **Amazon RDS** | **✅** | RDS Reserved DB Instances |
| Amazon ElastiCache | ✅ | Reserved Nodes |
| Amazon Redshift | ✅ | Reserved Nodes |
| Amazon DynamoDB | ✅ | Reserved Capacity |
| Amazon CloudFront | ❌ | 無 RI（無保留容量定價）|
| Amazon S3 | ❌ | 無 RI（提供批量折扣）|
| AWS IAM | ❌ | 免費服務 |

---

## 問題 63 / Question 63

**[題目 / Question]**
A firm wants to maintain the same data on S3 between its production account and multiple test accounts, **retaining object metadata**. Which technique?
公司想在生產帳戶和多個測試帳戶之間維護相同的 S3 資料，且**保留物件元資料**，應使用哪個技術？

**✅ 正確答案 / Correct Answer：Amazon S3 Replication（Amazon S3 複製）**

**[中文詳解]**
**Amazon S3 複製**可自動、非同步地跨 S3 儲存桶複製物件。可以跨帳戶複製，**保留所有元資料**（包括原始物件建立時間和版本 ID），確保副本與源物件完全相同。

**[S3 複製類型 / S3 Replication Types]**

| 類型 / Type | 範圍 | 適用場景 |
|---|---|---|
| **S3 CRR（跨區域複製）** | 不同 Region | 合規、地理分散 |
| **S3 SRR（同區域複製）** | 同一 Region | 跨帳戶複製（生產到測試）|

---

## 問題 64 / Question 64

**[題目 / Question]**
A QA team wants a tool that can provide access to **different mobile devices with variations in firmware and OS versions**. Which AWS service?
QA 團隊想要一個可提供**不同固件和 OS 版本的行動設備**存取的工具，哪個 AWS 服務？

**✅ 正確答案 / Correct Answer：AWS Device Farm**

**[中文詳解]**
**AWS Device Farm** 是應用程式測試服務，讓您透過在大量桌面瀏覽器和真實行動設備上測試來提高 Web 和行動應用程式的品質，無需佈建和管理測試基礎設施。可並發在多個設備上執行測試，生成視訊和日誌幫助快速識別問題。

**[適用對象 / Target Users]**
- 開發者
- QA 團隊
- 客戶支援代表

---

## 問題 65 / Question 65

**[題目 / Question]**
Which AWS Support plans provide **programmatic access** (API Access) to AWS Support Center features? (Select two)
哪兩個 AWS 支援方案提供 AWS Support Center 功能的**程式化存取**（API 存取）？

**✅ 正確答案 / Correct Answers：**
1. AWS Enterprise Support
2. AWS Business Support

**[程式化 API 存取 — 支援方案 / Programmatic API Access by Plan]**

| 方案 / Plan | API 存取 | 說明 |
|---|---|---|
| Basic | ❌ | 無 API 存取 |
| Developer | ❌ | 無 API 存取 |
| **Business** | **✅** | **可程式化建立/管理/關閉支援案例** |
| Enterprise On-Ramp | ✅ | 也提供 API 存取 |
| **Enterprise** | **✅** | **可程式化存取 + 管理 Trusted Advisor 請求** |

> ⚠️ "AWS Corporate Support" 是虛構選項（干擾項）

---

## 📊 考題領域統計 / Domain Summary

| 領域 / Domain | 題數 / Questions | 百分比 / % |
|---|---|---|
| Technology（技術）| 24 | 36.9% |
| Security and Compliance（安全與合規）| 17 | 26.2% |
| Cloud Concepts（雲端概念）| 14 | 21.5% |
| Billing and Pricing（計費與定價）| 10 | 15.4% |

---

## 🎯 本回必考重點整理 / Key Exam Points (Set 4)

### VPC 端點類型（超高頻）
- **Gateway Endpoint** → 只支援 **S3 和 DynamoDB**
- **Interface Endpoint** → 所有其他服務（SQS、SNS、Systems Manager 等）
- S3 同時支援兩種端點

### EC2 選擇指南
- **短期 + 突發 + 關鍵** → On-Demand
- **長期 + 穩定** → Reserved Instance
- **可中斷 + 彈性** → Spot Instance（最高 90% 折扣）
- **授權軟體 + 合規** → Dedicated Host

### DR 四種策略（由簡到複雜）
1. **Backup & Restore** → 最高 RTO，最低成本
2. **Pilot Light** → 最小核心運行，需額外步驟才能服務
3. **Warm Standby** → 縮減容量但立即可服務
4. **Multi-site Active-Active** → 最低 RTO，最高成本

### S3 定價重要規則
- 無取回費：**S3 Standard** 和 **S3 Intelligent-Tiering**
- 無最低儲存期限：**S3 Standard** 和 **S3 Intelligent-Tiering**
- 免費傳入：網際網路傳入 S3、同 Region 傳到 EC2、傳到 CloudFront

### 整合計費 RI 共享
- Bob 享受 Susan RI 折扣的條件：在 Susan 購買 RI 的**相同 AZ** 啟動執行個體
- **不是**相同 Region，而是相同 **AZ**

### IAM 憑證報告
- 列出帳戶中**所有使用者**及其**密碼、存取金鑰、MFA 設備**狀態
- 用於審計和合規

### EC2 連接方式
- **EC2 Instance Connect** → 瀏覽器型，支援 Mac/Windows/Linux
- **Session Manager** → 不需 Port 22，最安全
- Putty → 只支援 Windows

### 重要 AWS 服務定位
- **Amazon Translate** → 語言翻譯（英語 ↔ 其他語言）
- **AWS Device Farm** → 行動/Web 應用測試（多設備）
- **Credentials Report** → 帳戶所有用戶憑證狀態清單
- **S3 Transfer Acceleration** → 跨地理位置上傳加速
- **S3 Block Public Access** → 確保 S3 資源保持私密

### 常混淆：AWS 服務 vs VPC 組件
- **VPC 的組件**：Subnet、Internet Gateway、Route Table、VPC Endpoint
- **不是 VPC 組件**：Storage Gateway、API Gateway、S3 Object
