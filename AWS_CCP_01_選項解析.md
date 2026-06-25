# AWS CCP 01 選項解析

來源：
- 題目與選項：[AWS_CCP_Test1.md](AWS_CCP_Test1.md)
- 原詳解：[AWS_CCP_01.md](AWS_CCP_01.md)

這份檔案針對每題列出中英對照題目與選項，並用中文說明正確答案與其他選項的差異。

---

## 問題 1

**題目**
Which AWS Support plan provides architectural guidance contextual to your specific use-cases?
哪個 AWS Support 方案提供針對您特定使用案例的架構指導？

**[選項]**
- A. AWS Enterprise Support／AWS 企業支援
- B. AWS Developer Support／AWS 開發者支援
- C. AWS Enterprise On-Ramp Support／AWS Enterprise On-Ramp 支援
- D. AWS Business Support／AWS 商業支援

**正確答案**
AWS Business Support／AWS 商業支援

**為什麼正確**
AWS Business Support 適合在 AWS 上有生產工作負載的用戶，提供 24/7 電話、電子郵件和聊天技術支援，以及針對**特定使用案例的架構指導**。可完整使用 AWS Trusted Advisor 最佳實踐檢查，並可付費使用基礎設施事件管理。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Enterprise Support／AWS 企業支援 | ❌ 錯誤 | Enterprise Support 是最高階支援，包含 TAM 與更高等級營運支援；題目描述的特定使用案例架構指導對應 Business Support。 |
| AWS Developer Support／AWS 開發者支援 | ❌ 錯誤 | Developer Support 偏向開發與測試階段支援，不提供生產工作負載所需的完整支援能力。 |
| AWS Enterprise On-Ramp Support／AWS Enterprise On-Ramp 支援 | ❌ 錯誤 | Enterprise On-Ramp 是較高階支援方案，重點在主動式指導與重大事件支援；本題考的是 Business Support 的 use-case 架構指導。 |
| AWS Business Support／AWS 商業支援 | ✅ 正確 | Business Support 提供針對特定使用案例的架構指導，適合有生產工作負載且需要 24/7 技術支援的客戶。 |

---

## 問題 2

**題目**
Which AWS Route 53 routing policy would you use to route traffic to multiple resources and also choose how much traffic is routed to each resource?
您會使用哪個 AWS Route 53 路由政策將流量路由至多個資源，並選擇路由至每個資源的流量比例？

**[選項]**
- A. Simple routing／簡單路由
- B. Failover routing／容錯移轉路由
- C. Latency-based routing／延遲型路由
- D. Weighted routing／加權路由

**正確答案**
Weighted routing／加權路由

**為什麼正確**
**加權路由 (Weighted Routing)** 讓您能將單一域名關聯多個資源，並控制路由到每個資源的流量比例。透過指定相對權重來分配流量，適合用於負載均衡和新版本軟體測試。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Simple routing／簡單路由 | ❌ 錯誤 | Simple routing 只做基本 DNS 回應，不能設定各資源的流量比例。 |
| Failover routing／容錯移轉路由 | ❌ 錯誤 | Failover routing 用於主備容錯切換，不是用權重分配流量。 |
| Latency-based routing／延遲型路由 | ❌ 錯誤 | Latency-based routing 依延遲選擇較快端點，不是按比例分流。 |
| Weighted routing／加權路由 | ✅ 正確 | Weighted routing 可設定權重，控制流量分配到各個資源的比例。 |

---

## 問題 3

**題目**
A financial services company wants to ensure that its AWS account activity meets the governance, compliance and auditing norms. Which AWS service would you recommend for this use-case?
一家金融服務公司希望確保其 AWS 帳戶活動符合治理、合規和稽核規範。您會推薦哪個 AWS 服務？

**[選項]**
- A. AWS Config（資源組態追蹤）
- B. AWS Trusted Advisor（最佳實務建議）
- C. Amazon CloudWatch（監控服務）
- D. AWS CloudTrail（活動稽核記錄）

**正確答案**
AWS CloudTrail（活動稽核記錄）

**為什麼正確**
**AWS CloudTrail** 記錄並監控 AWS 帳戶中的所有 API 活動，包括透過管理控制台、SDK、命令列工具等執行的操作，提供完整的事件歷史記錄，適合治理、合規和審計需求。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Config（資源組態追蹤） | ❌ 錯誤 | AWS Config 追蹤資源設定與變更歷史，重點是組態合規。 |
| AWS Trusted Advisor（最佳實務建議） | ❌ 錯誤 | Trusted Advisor 提供成本、安全、效能、容錯與服務限制建議，不會自動執行遷移或取代專家顧問。 |
| Amazon CloudWatch（監控服務） | ❌ 錯誤 | CloudWatch 用於監控指標、日誌與警示，重點是觀察系統狀態。 |
| AWS CloudTrail（活動稽核記錄） | ✅ 正確 | 記錄並監控 AWS 帳戶中的所有 API 活動，提供事件歷史記錄，適合治理、合規和稽核。 |

---

## 問題 4

**題目**
A company wants to have control over creating and using its own keys for encryption on AWS services. Which of the following can be used for this use-case?
一家公司希望控制在 AWS 服務上建立和使用自己的加密金鑰。以下哪個可用於此使用案例？

**[選項]**
- A. AWS Secrets Manager（機密管理）
- B. AWS managed key／AWS 受管金鑰
- C. AWS owned key／AWS 擁有的金鑰
- D. Customer managed key (CMK)／客戶受管金鑰

**正確答案**
Customer managed key (CMK)／客戶受管金鑰

**為什麼正確**
**客戶管理金鑰 (CMK)** 是您在 AWS 帳戶中自行建立、擁有和管理的 KMS 金鑰。您對這些金鑰擁有完全控制權，包括設定金鑰策略、IAM 策略、啟用/停用、輪換加密材料等。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Secrets Manager（機密管理） | ❌ 錯誤 | Secrets Manager 用於保存、輪換密碼與 API Key 等機密，不是加密金鑰或敏感資料掃描服務。 |
| AWS managed key／AWS 受管金鑰 | ❌ 錯誤 | AWS managed key 由 AWS 建立與管理，客戶不能完全控制金鑰政策與生命週期。 |
| AWS owned key／AWS 擁有的金鑰 | ❌ 錯誤 | AWS owned key 由 AWS 擁有並跨帳戶管理，客戶無法直接建立或管理。 |
| Customer managed key (CMK)／客戶受管金鑰 | ✅ 正確 | 客戶受管金鑰由客戶在自己的 AWS 帳戶中建立與管理，可控制金鑰政策、啟用停用與輪換。 |

---

## 問題 5

**題目**
Which AWS Service can be used to mitigate a Distributed Denial of Service (DDoS) attack?
哪個 AWS 服務可用於緩解分散式阻斷服務（DDoS）攻擊？

**[選項]**
- A. AWS Systems Manager（系統管理）
- B. Amazon CloudWatch（監控服務）
- C. AWS Key Management Service (AWS KMS)（加密金鑰管理）
- D. AWS Shield（DDoS 防護）

**正確答案**
AWS Shield（DDoS 防護）

**為什麼正確**
**AWS Shield** 是託管型 DDoS 防護服務，提供即時偵測和自動緩解，無需聯繫 AWS 支援即可受益。分兩個層級：
- **Standard（標準版）**：免費，所有 AWS 客戶自動啟用，防護第 3、4 層攻擊
- **Advanced（進階版）**：付費，額外保護第 7 層，提供近即時可見性，整合 AWS WAF


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Systems Manager（系統管理） | ❌ 錯誤 | Systems Manager 用於管理 EC2 或本地伺服器，例如命令執行、修補與盤點，不管理 Organizations 帳戶移除或 DDoS 防護。 |
| Amazon CloudWatch（監控服務） | ❌ 錯誤 | CloudWatch 用於監控指標、日誌與警示，重點是觀察系統狀態。 |
| AWS Key Management Service (AWS KMS)（加密金鑰管理） | ❌ 錯誤 | KMS 管理加密金鑰；若題目是 DDoS、防火牆或用戶端加密，KMS 不是直接答案。 |
| AWS Shield（DDoS 防護） | ✅ 正確 | AWS Shield 可緩解 DDoS 攻擊。 |

---

## 問題 6

**題目**
A startup wants to migrate its data and applications from the on-premises data center to AWS Cloud. Which of the following options can be used by the startup to help with this migration? (Select two)
一家新創公司希望將其資料和應用程式從本地資料中心遷移至 AWS 雲端。以下哪些選項可以幫助新創公司完成此遷移？（選兩項）

**[選項]**
- A. Raise a support ticket with AWS Support for further assistance／向 AWS Support 提交工單以獲得進一步協助
- B. Use AWS Trusted Advisor to automate the infrastructure migration／使用 AWS Trusted Advisor 自動化基礎設施遷移
- C. Consult moderators on AWS Developer Forums／諮詢 AWS 開發人員論壇的版主
- D. Leverage AWS Professional Services to accelerate the infrastructure migration／利用 AWS Professional Services 加速基礎設施遷移
- E. Utilize AWS Partner Network (APN) to build a custom solution for this infrastructure migration／利用 AWS Partner Network（APN）為此基礎設施遷移建立自訂解決方案

**正確答案**
Leverage AWS Professional Services to accelerate the infrastructure migration／利用 AWS Professional Services 加速基礎設施遷移；Utilize AWS Partner Network (APN) to build a custom solution for this infrastructure migration／利用 AWS Partner Network（APN）為此基礎設施遷移建立自訂解決方案

**為什麼正確**
- **AWS Professional Services**：AWS 全球專家團隊，可協助加速基礎設施遷移，補充客戶團隊的專業技能
- **AWS Partner Network (APN)**：全球技術和諮詢合作夥伴計畫，APN 合作夥伴可協助建立客製化遷移解決方案


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Raise a support ticket with AWS Support for further assistance／向 AWS Support 提交工單以獲得進一步協助 | ❌ 錯誤 | 開支援單可取得協助，但不是專案型遷移交付服務，也不會替客戶設計完整遷移方案。 |
| Use AWS Trusted Advisor to automate the infrastructure migration／使用 AWS Trusted Advisor 自動化基礎設施遷移 | ❌ 錯誤 | Trusted Advisor 提供成本、安全、效能、容錯與服務限制建議，不會自動執行遷移或取代專家顧問。 |
| Consult moderators on AWS Developer Forums／諮詢 AWS 開發人員論壇的版主 | ❌ 錯誤 | Developer Forums 是社群討論管道，不是正式支援、濫用回報或遷移交付服務。 |
| Leverage AWS Professional Services to accelerate the infrastructure migration／利用 AWS Professional Services 加速基礎設施遷移 | ✅ 正確 | AWS Professional Services 是 AWS 專家顧問團隊，可協助加速大型遷移與落地。 |
| Utilize AWS Partner Network (APN) to build a custom solution for this infrastructure migration／利用 AWS Partner Network（APN）為此基礎設施遷移建立自訂解決方案 | ✅ 正確 | AWS Partner Network 可提供合作夥伴資源，協助建立客製化遷移解決方案。 |

---

## 問題 7

**題目**
Which of the following AWS services should be used to automatically distribute incoming traffic across multiple targets?
以下哪個 AWS 服務應用於自動將傳入流量分配至多個目標？

**[選項]**
- A. AWS Auto Scaling（自動擴展）
- B. Amazon OpenSearch Service（搜尋與日誌分析）
- C. AWS Elastic Beanstalk（應用部署平台）
- D. AWS Elastic Load Balancing (ELB)（負載平衡）

**正確答案**
AWS Elastic Load Balancing (ELB)（負載平衡）

**為什麼正確**
**彈性負載平衡 (ELB)** 自動將應用程式傳入流量分配到所有執行中的 EC2 執行個體，確保沒有單一執行個體負載過重，作為所有傳入流量的單一聯絡點。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Auto Scaling（自動擴展） | ❌ 錯誤 | Auto Scaling 依需求增減資源數量，但不負責把流量分散到多個目標。 |
| Amazon OpenSearch Service（搜尋與日誌分析） | ❌ 錯誤 | OpenSearch Service 用於搜尋、日誌分析與全文檢索，不是流量分配服務。 |
| AWS Elastic Beanstalk（應用部署平台） | ❌ 錯誤 | Elastic Beanstalk 是應用部署平台，重點是代管部署流程，不是負載平衡或資料庫容錯設定本身。 |
| AWS Elastic Load Balancing (ELB)（負載平衡） | ✅ 正確 | Elastic Load Balancing 可自動把傳入流量分散到多個目標。 |

---

## 問題 8

**題目**
A startup wants to provision an EC2 instance for the lowest possible cost for a long-term duration but needs to make sure that the instance would never be interrupted. Which of the following options would you recommend?
一家新創公司希望以盡可能低的成本長期佈建 EC2 執行個體，但需要確保執行個體永遠不會被中斷。您會推薦以下哪個選項？

**[選項]**
- A. EC2 Dedicated Host／EC2 專用主機
- B. EC2 On-Demand Instance／EC2 隨需執行個體
- C. EC2 Spot Instance／EC2 Spot 執行個體
- D. EC2 Reserved Instance (RI)／EC2 保留執行個體

**正確答案**
EC2 Reserved Instance (RI)／EC2 保留執行個體

**為什麼正確**
**預留執行個體 (RI)** 與隨需定價相比可節省高達 75%，可承諾 1 年或 3 年期（3 年折扣更大），且**不會被中斷**，適合長期穩定工作負載。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| EC2 Dedicated Host／EC2 專用主機 | ❌ 錯誤 | Dedicated Host 是專用實體主機，常用於 BYOL 或合規需求，成本通常不是長期 EC2 的最低選擇。 |
| EC2 On-Demand Instance／EC2 隨需執行個體 | ❌ 錯誤 | On-Demand 不需長期承諾但單價較高，適合短期或不可預測工作負載。 |
| EC2 Spot Instance／EC2 Spot 執行個體 | ❌ 錯誤 | Spot 使用 AWS 閒置容量，價格低但可能被中斷。 |
| EC2 Reserved Instance (RI)／EC2 保留執行個體 | ✅ 正確 | Reserved Instance 適合長期穩定工作負載，可用承諾換取較低成本且不會像 Spot 一樣被中斷。 |

---

## 問題 9

**題目**
Which of the following is CORRECT regarding removing an AWS account from AWS Organizations?
以下哪項關於從 AWS Organizations 移除 AWS 帳戶的陳述是正確的？

**[選項]**
- A. Raise a support ticket with AWS Support to remove the account／向 AWS Support 提交工單以移除帳戶
- B. The AWS account can be removed from AWS Systems Manager／可以從 AWS Systems Manager 移除 AWS 帳戶
- C. The AWS account must not have any Service Control Policies (SCPs) attached to it. Only then it can be removed from AWS organizations／AWS 帳戶不得附加任何服務控制政策（SCP），才能從 AWS Organizations 中移除
- D. The AWS account must be able to operate as a standalone account. Only then it can be removed from AWS organizations／AWS 帳戶必須能夠作為獨立帳戶運作，才能從 AWS Organizations 中移除

**正確答案**
The AWS account must be able to operate as a standalone account. Only then it can be removed from AWS organizations／AWS 帳戶必須能夠作為獨立帳戶運作，才能從 AWS Organizations 中移除

**為什麼正確**
要從組織中移除帳戶，該帳戶必須具備獨立運作所需的資訊：接受 AWS 客戶協議、選擇支援方案、提供並驗證聯絡資訊，以及提供有效的付款方式。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Raise a support ticket with AWS Support to remove the account／向 AWS Support 提交工單以移除帳戶 | ❌ 錯誤 | 從 Organizations 移除帳戶不靠開支援單完成，帳戶本身必須能作為獨立帳戶運作。 |
| The AWS account can be removed from AWS Systems Manager／可以從 AWS Systems Manager 移除 AWS 帳戶 | ❌ 錯誤 | Systems Manager 用於管理 EC2 或本地伺服器，例如命令執行、修補與盤點，不管理 Organizations 帳戶移除或 DDoS 防護。 |
| The AWS account must not have any Service Control Policies (SCPs) attached to it. Only then it can be removed from AWS organizations／AWS 帳戶不得附加任何服務控制政策（SCP），才能從 AWS Organizations 中移除 | ❌ 錯誤 | SCP 會限制帳戶權限，但移除 Organizations 帳戶的關鍵是帳戶能獨立運作並具備必要資訊。 |
| The AWS account must be able to operate as a standalone account. Only then it can be removed from AWS organizations／AWS 帳戶必須能夠作為獨立帳戶運作，才能從 AWS Organizations 中移除 | ✅ 正確 | 成員帳戶必須能作為獨立帳戶運作，才能從 AWS Organizations 移除。 |

---

## 問題 10

**題目**
A web application stores all of its data on Amazon S3 buckets. A client has mandated that data be encrypted before sending it to Amazon S3. Which of the following is the right technique for encrypting data?
一個 Web 應用程式將所有資料儲存在 Amazon S3 儲存貯體上。客戶要求資料在傳送至 Amazon S3 之前必須加密。以下哪個是加密資料的正確技術？

**[選項]**
- A. Encryption is enabled by default for all the objects written to Amazon S3. Additional configuration is not required／寫入 Amazon S3 的所有物件預設啟用加密，無需額外設定
- B. Enable server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS)／使用 AWS KMS 金鑰（SSE-KMS）啟用伺服器端加密
- C. Enable server-side encryption with Amazon S3 Managed Keys (SSE-S3)／使用 Amazon S3 受管金鑰（SSE-S3）啟用伺服器端加密
- D. Enable client-side encryption using AWS encryption SDK／使用 AWS 加密 SDK 啟用用戶端加密

**正確答案**
Enable client-side encryption using AWS encryption SDK／使用 AWS 加密 SDK 啟用用戶端加密

**為什麼正確**
**用戶端加密 (Client-side encryption)** 指在傳送到 S3 之前就先加密資料。AWS Encryption SDK 是獨立的用戶端加密程式庫，不受特定語言 SDK 限制，也不限於 Amazon S3，可用於加密/解密任何地方儲存的資料。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Encryption is enabled by default for all the objects written to Amazon S3. Additional configuration is not required／寫入 Amazon S3 的所有物件預設啟用加密，無需額外設定 | ❌ 錯誤 | 預設加密仍屬於 S3 端的保護；題目要求資料送出前先加密時，要使用用戶端加密。 |
| Enable server-side encryption with AWS Key Management Service (AWS KMS) keys (SSE-KMS)／使用 AWS KMS 金鑰（SSE-KMS）啟用伺服器端加密 | ❌ 錯誤 | KMS 管理加密金鑰；若題目是 DDoS、防火牆或用戶端加密，KMS 不是直接答案。 |
| Enable server-side encryption with Amazon S3 Managed Keys (SSE-S3)／使用 Amazon S3 受管金鑰（SSE-S3）啟用伺服器端加密 | ❌ 錯誤 | SSE-S3 是 S3 服務端加密，資料是送到 S3 後才由服務端加密。 |
| Enable client-side encryption using AWS encryption SDK／使用 AWS 加密 SDK 啟用用戶端加密 | ✅ 正確 | 用戶端加密是在資料送到 Amazon S3 前先加密，符合題目要求。 |

---

## 問題 11

**題目**
An organization needs to securely access AWS services and establish private connectivity between its VPCs and supported AWS services without using the public internet. Which AWS services can meet this requirement? (Select two)
一個組織需要安全地存取 AWS 服務，並在其 VPC 和受支援的 AWS 服務之間建立私有連接，而不使用公共網際網路。哪些 AWS 服務可以滿足此需求？（選兩項）

**[選項]**
- A. Amazon Inspector（弱點評估）
- B. Amazon Connect（雲端客服中心）
- C. AWS Internet Gateway／AWS 網際網路閘道
- D. AWS Transit Gateway（VPC 與網路中樞）
- E. AWS PrivateLink（私有服務連線）

**正確答案**
AWS Transit Gateway（VPC 與網路中樞）；AWS PrivateLink（私有服務連線）

**為什麼正確**
- **AWS PrivateLink**：在 VPC 和支援的 AWS 服務之間啟用私有連接，流量不經過公共網際網路
- **AWS Transit Gateway**：高度可擴展的服務，透過中央樞紐連接多個 VPC 和本地網路，採用 Hub-and-Spoke 模型簡化管理


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Inspector（弱點評估） | ❌ 錯誤 | Inspector 用於自動化弱點評估，重點是找 EC2、容器映像或 Lambda 的漏洞。 |
| Amazon Connect（雲端客服中心） | ❌ 錯誤 | Amazon Connect 是雲端客服中心服務，用來建立客服電話與聯絡中心，不是 VPC 私有連線服務。 |
| AWS Internet Gateway／AWS 網際網路閘道 | ❌ 錯誤 | Internet Gateway 讓 VPC 公有子網路連上網際網路，不提供私有 AWS 服務連線。 |
| AWS Transit Gateway（VPC 與網路中樞） | ✅ 正確 | Transit Gateway 可作為中央樞紐連接多個 VPC 與本地網路。 |
| AWS PrivateLink（私有服務連線） | ✅ 正確 | PrivateLink 可讓 VPC 私有連接支援的 AWS 服務，流量不經公共網際網路。 |

---

## 問題 12

**題目**
AWS Shield Advanced provides expanded DDoS attack protection for web applications running on which of the following resources? (Select two)
AWS Shield Advanced 為在以下哪些資源上執行的 Web 應用程式提供擴展的 DDoS 攻擊防護？（選兩項）

**[選項]**
- A. AWS Elastic Beanstalk（應用部署平台）
- B. AWS CloudFormation（基礎設施模板）
- C. Amazon API Gateway（API 管理服務）
- D. AWS Global Accelerator（全球連線加速）
- E. Amazon Route 53（DNS 服務）

**正確答案**
AWS Global Accelerator（全球連線加速）；Amazon Route 53（DNS 服務）

**為什麼正確**
AWS Shield Advanced 支援的資源：Amazon EC2、Elastic Load Balancing (ELB)、Amazon CloudFront、**Amazon Route 53**、**AWS Global Accelerator**


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Elastic Beanstalk（應用部署平台） | ❌ 錯誤 | Elastic Beanstalk 是應用部署平台，重點是代管部署流程，不是負載平衡或資料庫容錯設定本身。 |
| AWS CloudFormation（基礎設施模板） | ❌ 錯誤 | CloudFormation 用模板建立與管理 AWS 資源，不是除錯追蹤、帳單估算或資料庫容錯服務。 |
| Amazon API Gateway（API 管理服務） | ❌ 錯誤 | API Gateway 用於建立與管理 API 入口，不是部署平台、DNS 或全球流量加速服務。 |
| AWS Global Accelerator（全球連線加速） | ✅ 正確 | Global Accelerator 使用 AWS 全球網路改善應用程式連線效能與可用性。 |
| Amazon Route 53（DNS 服務） | ✅ 正確 | Route 53 提供 DNS 與路由政策，可將使用者導向合適端點。 |

---

## 問題 13

**題目**
A multi-national company has just moved its infrastructure from its on-premises data center to AWS Cloud. As part of the shared responsibility model, AWS is responsible for which of the following?
一家跨國公司剛將其基礎設施從本地資料中心遷移至 AWS 雲端。作為共同責任模型的一部分，AWS 負責以下哪項？

**[選項]**
- A. Patching guest OS／修補客體作業系統
- B. Configuring customer applications／設定客戶應用程式
- C. Service and Communications Protection or Zone Security／服務和通訊保護或區域安全
- D. Physical and Environmental controls／實體和環境控制

**正確答案**
Physical and Environmental controls／實體和環境控制

**為什麼正確**
**[共同責任模型]**
| AWS 負責 | 客戶負責 |
| --- | --- |
| 實體與環境安全 | 修補 Guest OS |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Patching guest OS／修補客體作業系統 | ❌ 錯誤 | 修補 Guest OS 是客戶在 EC2 上的責任。 |
| Configuring customer applications／設定客戶應用程式 | ❌ 錯誤 | 設定與保護客戶應用程式屬於客戶責任。 |
| Service and Communications Protection or Zone Security／服務和通訊保護或區域安全 | ❌ 錯誤 | 這偏向客戶在雲端中的通訊與服務保護設計，不是 AWS 實體環境控制。 |
| Physical and Environmental controls／實體和環境控制 | ✅ 正確 | 實體與環境控制屬於 AWS 對雲端底層基礎設施的責任。 |

---

## 問題 14

**題目**
Which of the following is an AWS database service?
以下哪個是 AWS 資料庫服務？

**[選項]**
- A. AWS Storage Gateway（混合雲儲存閘道）
- B. AWS Glue（資料整合 ETL）
- C. AWS Database Migration Service (AWS DMS)（資料庫遷移）
- D. Amazon Redshift（資料倉儲）

**正確答案**
Amazon Redshift（資料倉儲）

**為什麼正確**
**Amazon Redshift** 是全托管的 PB 級雲端資料倉儲，專為大規模資料集儲存和分析設計。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Storage Gateway（混合雲儲存閘道） | ❌ 錯誤 | Storage Gateway 連接本地環境與 AWS 雲端儲存，重點是混合雲儲存。 |
| AWS Glue（資料整合 ETL） | ❌ 錯誤 | Glue 是資料整合、ETL 與資料目錄服務，不是資料庫或敏感資料探索服務。 |
| AWS Database Migration Service (AWS DMS)（資料庫遷移） | ❌ 錯誤 | DMS 用於資料庫遷移，不是用來儲存、查詢或分析資料的資料庫服務。 |
| Amazon Redshift（資料倉儲） | ✅ 正確 | Amazon Redshift 是 AWS 資料倉儲服務。 |

---

## 問題 15

**題目**
Which of the following entities applies patches to the underlying OS for Amazon Aurora?
以下哪個實體為 Amazon Aurora 的底層作業系統套用修補程式？

**[選項]**
- A. The AWS customer by using AWS Systems Manager／AWS 客戶使用 AWS Systems Manager
- B. The AWS customer by SSHing on the instances／AWS 客戶透過 SSH 連接執行個體
- C. The AWS Support after receiving a request from the customer／AWS Support 在收到客戶請求後
- D. The AWS Product Team automatically／AWS 產品團隊自動執行

**正確答案**
The AWS Product Team automatically／AWS 產品團隊自動執行

**為什麼正確**
Amazon Aurora 由 Amazon RDS 完全託管，AWS 產品團隊自動處理底層 OS 修補、硬體佈建、資料庫設定和備份等管理工作，客戶無需介入。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| The AWS customer by using AWS Systems Manager／AWS 客戶使用 AWS Systems Manager | ❌ 錯誤 | Systems Manager 用於管理 EC2 或本地伺服器，例如命令執行、修補與盤點，不管理 Organizations 帳戶移除或 DDoS 防護。 |
| The AWS customer by SSHing on the instances／AWS 客戶透過 SSH 連接執行個體 | ❌ 錯誤 | SSH 只能登入客戶可管理的作業系統層，無法更換 AWS 實體硬體。 |
| The AWS Support after receiving a request from the customer／AWS Support 在收到客戶請求後 | ❌ 錯誤 | EC2 底層故障硬體由 AWS 自動處理，不需要等客戶開支援單後才由 AWS Support 更換。 |
| The AWS Product Team automatically／AWS 產品團隊自動執行 | ✅ 正確 | EC2 底層故障硬體由 AWS 自動處理。 |

---

## 問題 16

**題目**
Which of the following AWS Support plans provide access to guidance, configuration, and troubleshooting of AWS interoperability with third-party software? (Select two)
以下哪些 AWS Support 方案提供對 AWS 與第三方軟體互操作性的指導、設定和疑難排解？（選兩項）

**[選項]**
- A. AWS Corporate Support（非標準支援方案）
- B. AWS Developer Support／AWS 開發者支援
- C. AWS Basic Support／AWS 基本支援
- D. AWS Enterprise Support／AWS 企業支援
- E. AWS Business Support／AWS 商業支援

**正確答案**
AWS Enterprise Support／AWS 企業支援；AWS Business Support／AWS 商業支援

**為什麼正確**
1. AWS Business Support
2. AWS Enterprise Support
**[支援方案功能比較]**
| 功能 | Basic | Developer | Business | Enterprise On-Ramp | Enterprise |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Corporate Support（非標準支援方案） | ❌ 錯誤 | AWS Corporate Support 不是標準 AWS Support 方案名稱。 |
| AWS Developer Support／AWS 開發者支援 | ❌ 錯誤 | Developer Support 偏向開發與測試階段支援，不提供生產工作負載所需的完整支援能力。 |
| AWS Basic Support／AWS 基本支援 | ❌ 錯誤 | Basic Support 主要提供文件、帳務與服務健康資訊，不包含進階技術支援。 |
| AWS Enterprise Support／AWS 企業支援 | ✅ 正確 | Business Support 和 Enterprise Support 都提供進階技術支援，包含常見作業系統、平台與應用堆疊的互通性指導。 |
| AWS Business Support／AWS 商業支援 | ✅ 正確 | Business Support 和 Enterprise Support 都提供進階技術支援，包含常見作業系統、平台與應用堆疊的互通性指導。 |

---

## 問題 17

**題目**
Which of the following AWS services support VPC Gateway Endpoint for a private connection from a VPC? (Select two)
以下哪些 AWS 服務支援 VPC 閘道端點以從 VPC 進行私有連接？（選兩項）

**[選項]**
- A. Amazon Simple Queue Service (SQS)（訊息佇列）
- B. Amazon Simple Notification Service (SNS)（一對多通知）
- C. Amazon Elastic Compute Cloud (Amazon EC2)（虛擬伺服器）
- D. Amazon DynamoDB（NoSQL 資料庫）
- E. Amazon Simple Storage Service (Amazon S3)（物件儲存）

**正確答案**
Amazon DynamoDB（NoSQL 資料庫）；Amazon Simple Storage Service (Amazon S3)（物件儲存）

**為什麼正確**
1. Amazon S3
2. Amazon DynamoDB
**[考試重點!]**
> **只有 Amazon S3 和 Amazon DynamoDB 支援 VPC Gateway Endpoint！**


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Simple Queue Service (SQS)（訊息佇列） | ❌ 錯誤 | SQS 是訊息佇列，用來暫存訊息並解耦生產者與消費者。 |
| Amazon Simple Notification Service (SNS)（一對多通知） | ❌ 錯誤 | SNS 是一對多發布通知服務，適合把同一則訊息廣播給多個訂閱者。 |
| Amazon Elastic Compute Cloud (Amazon EC2)（虛擬伺服器） | ❌ 錯誤 | EC2 是可管理的虛擬伺服器，屬於運算服務，不是受管儲存、資料庫或訊息服務。 |
| Amazon DynamoDB（NoSQL 資料庫） | ✅ 正確 | S3 和 DynamoDB 是支援 VPC Gateway Endpoint 的服務，可從 VPC 私有連線存取。 |
| Amazon Simple Storage Service (Amazon S3)（物件儲存） | ✅ 正確 | S3 和 DynamoDB 是支援 VPC Gateway Endpoint 的服務，可從 VPC 私有連線存取。 |

---

## 問題 18

**題目**
The DevOps team at an IT company is moving 500 GB of data from an EC2 instance to an S3 bucket in the same region. Which of the following scenario captures the correct charges for this data transfer?
一家 IT 公司的 DevOps 團隊正在將 500 GB 的資料從 EC2 執行個體移動至同一區域的 S3 儲存貯體。以下哪個情境描述了此資料傳輸的正確費用？

**[選項]**
- A. The company would only be charged for the inbound data transfer into the S3 bucket／公司只需為傳入 S3 儲存貯體的入站資料傳輸付費
- B. The company would be charged for both the outbound data transfer from EC2 instance as well as the inbound data transfer into the S3 bucket／公司需為 EC2 執行個體的出站資料傳輸和傳入 S3 儲存貯體的入站資料傳輸付費
- C. The company would only be charged for the outbound data transfer from EC2 instance／公司只需為 EC2 執行個體的出站資料傳輸付費
- D. The company would not be charged for this data transfer／公司無需為此資料傳輸付費

**正確答案**
The company would not be charged for this data transfer／公司無需為此資料傳輸付費

**為什麼正確**
**[AWS 資料傳輸費用規則]**
| 傳輸類型 | 費用 |
| --- | --- |
| 同區域內 EC2 ↔ S3 | **免費** ✅ |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| The company would only be charged for the inbound data transfer into the S3 bucket／公司只需為傳入 S3 儲存貯體的入站資料傳輸付費 | ❌ 錯誤 | 同一區域內 EC2 與 S3 之間的資料傳輸不收取資料傳輸費。 |
| The company would be charged for both the outbound data transfer from EC2 instance as well as the inbound data transfer into the S3 bucket／公司需為 EC2 執行個體的出站資料傳輸和傳入 S3 儲存貯體的入站資料傳輸付費 | ❌ 錯誤 | 同一區域內 EC2 與 S3 之間的資料傳輸不收取資料傳輸費。 |
| The company would only be charged for the outbound data transfer from EC2 instance／公司只需為 EC2 執行個體的出站資料傳輸付費 | ❌ 錯誤 | 同一區域內 EC2 與 S3 之間的資料傳輸不收取資料傳輸費。 |
| The company would not be charged for this data transfer／公司無需為此資料傳輸付費 | ✅ 正確 | 同一區域內 EC2 與 S3 之間的資料傳輸不收取資料傳輸費。 |

---

## 問題 19

**題目**
According to the AWS Shared Responsibility Model, which of the following are responsibilities of AWS? (Select two)
根據 AWS 共同責任模型，以下哪些是 AWS 的責任？（選兩項）

**[選項]**
- A. Enabling Multi Factor Authentication on AWS accounts in your organization／在您組織中的 AWS 帳戶上啟用多重要素驗證
- B. Creating S3 bucket policies for appropriate user access／為適當的使用者存取建立 S3 儲存貯體政策
- C. Creating IAM role for accessing Amazon EC2 instances／建立用於存取 Amazon EC2 執行個體的 IAM 角色
- D. Operating the infrastructure layer, the operating system and the platform for the Amazon S3 service／負責 Amazon S3 服務的基礎設施層、作業系統和平台的運作
- E. Replacing faulty hardware of Amazon EC2 instances／更換 Amazon EC2 執行個體的故障硬體

**正確答案**
Operating the infrastructure layer, the operating system and the platform for the Amazon S3 service／負責 Amazon S3 服務的基礎設施層、作業系統和平台的運作；Replacing faulty hardware of Amazon EC2 instances／更換 Amazon EC2 執行個體的故障硬體

**為什麼正確**
- 對於抽象服務（如 S3、DynamoDB），AWS 負責基礎設施層、作業系統和平台的運作
- 替換故障的 EC2 硬體屬於「雲端安全」，是 AWS 的責任


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Enabling Multi Factor Authentication on AWS accounts in your organization／在您組織中的 AWS 帳戶上啟用多重要素驗證 | ❌ 錯誤 | 啟用 MFA 是客戶保護 AWS 帳戶登入安全的責任。 |
| Creating S3 bucket policies for appropriate user access／為適當的使用者存取建立 S3 儲存貯體政策 | ❌ 錯誤 | S3 bucket policy 是客戶設定資料存取權限的責任。 |
| Creating IAM role for accessing Amazon EC2 instances／建立用於存取 Amazon EC2 執行個體的 IAM 角色 | ❌ 錯誤 | IAM role 是客戶管理身分與權限的責任。 |
| Operating the infrastructure layer, the operating system and the platform for the Amazon S3 service／負責 Amazon S3 服務的基礎設施層、作業系統和平台的運作 | ✅ 正確 | 對於 S3 這類抽象服務，AWS 負責底層基礎設施、作業系統與平台。 |
| Replacing faulty hardware of Amazon EC2 instances／更換 Amazon EC2 執行個體的故障硬體 | ✅ 正確 | EC2 底層故障硬體由 AWS 負責更換。 |

---

## 問題 20

**題目**
A silicon valley based healthcare startup stores anonymized patient health data on Amazon S3. The CTO further wants to ensure that any sensitive data on S3 is discovered and identified to prevent any sensitive data leaks. Which AWS service would you recommend addressing this use-case?
一家位於矽谷的醫療保健新創公司將匿名化的患者健康資料儲存在 Amazon S3 上。CTO 希望確保 S3 上的任何敏感資料都能被發現和識別，以防止敏感資料洩漏。您會推薦哪個 AWS 服務？

**[選項]**
- A. AWS Secrets Manager（機密管理）
- B. Amazon Polly（文字轉語音）
- C. AWS Glue（資料整合 ETL）
- D. Amazon Macie（敏感資料探索）

**正確答案**
Amazon Macie（敏感資料探索）

**為什麼正確**
**Amazon Macie** 是全托管的資料安全和隱私服務，使用機器學習和模式比對來發現和保護 AWS 中的敏感資料，自動識別未加密的儲存桶、公開訪問的儲存桶，並識別 PII（個人識別資訊）等敏感資料。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Secrets Manager（機密管理） | ❌ 錯誤 | Secrets Manager 用於保存、輪換密碼與 API Key 等機密，不是加密金鑰或敏感資料掃描服務。 |
| Amazon Polly（文字轉語音） | ❌ 錯誤 | Polly 將文字轉成自然語音。 |
| AWS Glue（資料整合 ETL） | ❌ 錯誤 | Glue 是資料整合、ETL 與資料目錄服務，不是資料庫或敏感資料探索服務。 |
| Amazon Macie（敏感資料探索） | ✅ 正確 | Amazon Macie 可探索與識別 S3 中的敏感資料。 |

---

## 問題 21

**題目**
Which AWS services can be used to decouple components of a microservices based application on AWS Cloud? (Select two)
哪些 AWS 服務可用於解耦 AWS 雲端上基於微服務的應用程式元件？（選兩項）

**[選項]**
- A. AWS Lambda（無伺服器函數）
- B. Amazon Elastic Compute Cloud (Amazon EC2)（虛擬伺服器）
- C. AWS Step Functions（工作流程協調）
- D. Amazon Simple Notification Service (SNS)（一對多通知）
- E. Amazon Simple Queue Service (SQS)（訊息佇列）

**正確答案**
Amazon Simple Notification Service (SNS)（一對多通知）；Amazon Simple Queue Service (SQS)（訊息佇列）

**為什麼正確**
1. Amazon SQS（簡單佇列服務）
2. Amazon SNS（簡單通知服務）
**[解耦服務說明]**
| 服務 | 模式 | 說明 |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Lambda（無伺服器函數） | ❌ 錯誤 | Lambda 是無伺服器函數運算服務，負責執行程式碼，不是訊息解耦服務本身。 |
| Amazon Elastic Compute Cloud (Amazon EC2)（虛擬伺服器） | ❌ 錯誤 | EC2 是可管理的虛擬伺服器，屬於運算服務，不是受管儲存、資料庫或訊息服務。 |
| AWS Step Functions（工作流程協調） | ❌ 錯誤 | Step Functions 用來協調多步驟工作流程，不是單純的訊息佇列或發布訂閱服務。 |
| Amazon Simple Notification Service (SNS)（一對多通知） | ✅ 正確 | SNS 是發布/訂閱通知服務，可把訊息廣播給多個訂閱者以解耦系統。 |
| Amazon Simple Queue Service (SQS)（訊息佇列） | ✅ 正確 | SQS 是訊息佇列服務，可暫存訊息並解耦生產者與消費者。 |

---

## 問題 22

**題目**
A company wants to move to AWS cloud and release new features with quick iterations by utilizing relevant AWS services whenever required. Which of the following characteristics of AWS Cloud does it want to leverage?
一家公司希望遷移至 AWS 雲端，並在需要時利用相關 AWS 服務快速迭代發布新功能。它希望利用 AWS 雲端的哪項特性？

**[選項]**
- A. Elasticity／彈性
- B. Scalability／可擴展性
- C. Reliability／可靠性
- D. Agility／敏捷性

**正確答案**
Agility／敏捷性

**為什麼正確**
**[雲端特性定義]**
| 特性 | 定義 |
| --- | --- |
| **Agility（敏捷性）** | **快速開發、測試和發布軟體的能力** |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Elasticity／彈性 | ❌ 錯誤 | Elasticity 指依需求自動增減資源，重點是容量隨負載變化。 |
| Scalability／可擴展性 | ❌ 錯誤 | Scalability 指系統能隨需求變大或變小，重點是承受成長。 |
| Reliability／可靠性 | ❌ 錯誤 | Reliability 指系統穩定運作並能從故障恢復。 |
| Agility／敏捷性 | ✅ 正確 | Agility 指快速開發、測試與發布，能更快回應需求變化。 |

---

## 問題 23

**題目**
Which of the following statements are CORRECT regarding the Availability Zone (AZ) specific characteristics of Amazon EBS and Amazon EFS storage types?
以下哪項陳述關於 Amazon EBS 和 Amazon EFS 儲存類型的可用區域（AZ）特定特性是正確的？

**[選項]**
- A. EBS volume can be attached to one or more instances in multiple AZs and EFS file system can be mounted on instances across multiple AZs／EBS 磁碟區可附加至多個 AZ 中的一個或多個執行個體，EFS 檔案系統可掛載至多個 AZ 的執行個體
- B. EBS volume can be attached to one or more instances in multiple AZs and EFS file system can be mounted on instances in the same AZ／EBS 磁碟區可附加至多個 AZ 中的一個或多個執行個體，EFS 檔案系統只能掛載至同一 AZ 的執行個體
- C. EBS volume can be attached to a single instance in the same AZ and EFS file system can only be mounted on instances in the same AZ／EBS 磁碟區只能附加至同一 AZ 中的單一執行個體，EFS 檔案系統只能掛載至同一 AZ 的執行個體
- D. EBS volume can be attached to a single instance in the same AZ whereas EFS file system can be mounted on instances across multiple AZs／EBS 磁碟區只能附加至同一 AZ 中的單一執行個體，而 EFS 檔案系統可以掛載至多個 AZ 的執行個體

**正確答案**
EBS volume can be attached to a single instance in the same AZ whereas EFS file system can be mounted on instances across multiple AZs／EBS 磁碟區只能附加至同一 AZ 中的單一執行個體，而 EFS 檔案系統可以掛載至多個 AZ 的執行個體

**為什麼正確**
EBS volume can be attached to a single instance **in the same AZ** whereas EFS file system can be mounted on instances **across multiple AZs**.
EBS 磁碟區只能掛載到**同一 AZ** 的單一執行個體，而 EFS 可以掛載到**跨多個 AZ** 的執行個體。
**[EBS vs EFS 比較]**
| 特性 | Amazon EBS | Amazon EFS |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| EBS volume can be attached to one or more instances in multiple AZs and EFS file system can be mounted on instances across multiple AZs／EBS 磁碟區可附加至多個 AZ 中的一個或多個執行個體，EFS 檔案系統可掛載至多個 AZ 的執行個體 | ❌ 錯誤 | EBS 是 EC2 的區塊儲存，通常附加到單一 AZ 內的執行個體，不適合數百台 EC2 同時共享檔案。 |
| EBS volume can be attached to one or more instances in multiple AZs and EFS file system can be mounted on instances in the same AZ／EBS 磁碟區可附加至多個 AZ 中的一個或多個執行個體，EFS 檔案系統只能掛載至同一 AZ 的執行個體 | ❌ 錯誤 | EBS 是 EC2 的區塊儲存，通常附加到單一 AZ 內的執行個體，不適合數百台 EC2 同時共享檔案。 |
| EBS volume can be attached to a single instance in the same AZ and EFS file system can only be mounted on instances in the same AZ／EBS 磁碟區只能附加至同一 AZ 中的單一執行個體，EFS 檔案系統只能掛載至同一 AZ 的執行個體 | ❌ 錯誤 | EBS 是 EC2 的區塊儲存，通常附加到單一 AZ 內的執行個體，不適合數百台 EC2 同時共享檔案。 |
| EBS volume can be attached to a single instance in the same AZ whereas EFS file system can be mounted on instances across multiple AZs／EBS 磁碟區只能附加至同一 AZ 中的單一執行個體，而 EFS 檔案系統可以掛載至多個 AZ 的執行個體 | ✅ 正確 | EBS 磁碟區屬於單一 AZ，EFS 可跨多個 AZ 由多台執行個體掛載。 |

---

## 問題 24

**題目**
Which of the following AWS Support plans provide access to only core checks from the AWS Trusted Advisor Best Practice Checks? (Select two)
以下哪些 AWS Support 方案僅提供 AWS Trusted Advisor 最佳實務檢查的核心檢查存取？（選兩項）

**[選項]**
- A. AWS Enterprise Support／AWS 企業支援
- B. AWS Enterprise On-Ramp Support／AWS Enterprise On-Ramp 支援
- C. AWS Business Support／AWS 商業支援
- D. AWS Developer Support／AWS 開發者支援
- E. AWS Basic Support／AWS 基本支援

**正確答案**
AWS Developer Support／AWS 開發者支援；AWS Basic Support／AWS 基本支援

**為什麼正確**
1. AWS Basic Support
2. AWS Developer Support
**[Trusted Advisor 存取層級]**
| 方案 | Trusted Advisor 存取 |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Enterprise Support／AWS 企業支援 | ❌ 錯誤 | Enterprise Support 可使用完整 Trusted Advisor 檢查，不是只有 core checks。 |
| AWS Enterprise On-Ramp Support／AWS Enterprise On-Ramp 支援 | ❌ 錯誤 | Enterprise On-Ramp 是較高階支援方案，重點在主動式指導與重大事件支援；本題考的是 Business Support 的 use-case 架構指導。 |
| AWS Business Support／AWS 商業支援 | ❌ 錯誤 | Business Support 可使用完整 Trusted Advisor 檢查，不是只有 core checks。 |
| AWS Developer Support／AWS 開發者支援 | ✅ 正確 | Basic Support 和 Developer Support 只提供 Trusted Advisor 的核心檢查。 |
| AWS Basic Support／AWS 基本支援 | ✅ 正確 | Basic Support 和 Developer Support 只提供 Trusted Advisor 的核心檢查。 |

---

## 問題 25

**題目**
An organization is currently operating MySQL databases on its own on-premises servers. To reduce the operational burden of database maintenance and management, the organization wants to move to a fully managed AWS database offering. Which migration strategy best aligns with this goal?
一個組織目前在自己的本地伺服器上運作 MySQL 資料庫。為了減少資料庫維護和管理的營運負擔，組織希望遷移至完全受管的 AWS 資料庫服務。哪種遷移策略最符合此目標？

**[選項]**
- A. Refactor／重構
- B. Rehost／重新託管
- C. Repurchase／重新購買
- D. Replatform／重新平台化

**正確答案**
Replatform／重新平台化

**為什麼正確**
**[6R 遷移策略]**
| 策略 | 說明 | 此案例 |
| --- | --- | --- |
| Rehost（重新託管） | 直接搬移，不變架構 | ❌ 仍需自管 |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Refactor／重構 | ❌ 錯誤 | Refactor 是重新設計應用程式架構，改動最大。 |
| Rehost／重新託管 | ❌ 錯誤 | Rehost 是 lift-and-shift，直接搬移到雲端但架構改動最少。 |
| Repurchase／重新購買 | ❌ 錯誤 | Repurchase 是改買 SaaS 或新產品取代原系統。 |
| Replatform／重新平台化 | ✅ 正確 | Replatform 是適度調整平台，例如改用受管資料庫，以降低維運負擔但不大幅重寫應用。 |

---

## 問題 26

**題目**
Which of the following are the advantages of cloud computing? (Select three)
以下哪些是雲端運算的優勢？（選三項）

**[選項]**
- A. Trade variable expense for capital expense／以資本支出換取可變支出
- B. Spend money on building and maintaining data centers／花費資金建設和維護資料中心
- C. Allocate a few months of planning for your infrastructure capacity needs／為基礎設施容量需求分配幾個月的規劃時間
- D. Benefit from massive economies of scale／受益於大規模規模經濟
- E. Trade capital expense for variable expense／以可變支出換取資本支出
- F. Go global in minutes and deploy applications in multiple regions around the world with just a few clicks／幾分鐘內實現全球化，只需幾次點擊即可在世界各地多個區域部署應用程式

**正確答案**
Benefit from massive economies of scale／受益於大規模規模經濟；Trade capital expense for variable expense／以可變支出換取資本支出；Go global in minutes and deploy applications in multiple regions around the world with just a few clicks／幾分鐘內實現全球化，只需幾次點擊即可在世界各地多個區域部署應用程式

**為什麼正確**
1. 受益於大規模經濟
2. 將資本支出換為可變支出
3. 幾分鐘內全球部署
**[雲端運算六大優勢]**


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Trade variable expense for capital expense／以資本支出換取可變支出 | ❌ 錯誤 | 雲端的優勢是把資本支出轉為可變支出，不是反過來。 |
| Spend money on building and maintaining data centers／花費資金建設和維護資料中心 | ❌ 錯誤 | 使用雲端可減少自行建置與維護資料中心的負擔。 |
| Allocate a few months of planning for your infrastructure capacity needs／為基礎設施容量需求分配幾個月的規劃時間 | ❌ 錯誤 | 雲端可降低容量預估風險，不需要長時間預先猜測容量。 |
| Benefit from massive economies of scale／受益於大規模規模經濟 | ✅ 正確 | 受益於大規模規模經濟。 |
| Trade capital expense for variable expense／以可變支出換取資本支出 | ✅ 正確 | 以可變支出換取資本支出。 |
| Go global in minutes and deploy applications in multiple regions around the world with just a few clicks／幾分鐘內實現全球化，只需幾次點擊即可在世界各地多個區域部署應用程式 | ✅ 正確 | 幾分鐘內實現全球化，只需幾次點擊即可在世界各地多個區域部署應用程式。 |

---

## 問題 27

**題目**
A unicorn startup is building an analytics application with support for a speech-based interface. The application will accept speech-based input from users and then convey results via speech. Which solution would you recommend for the given use-case?
一家獨角獸新創公司正在建立支援語音介面的分析應用程式。應用程式將接受使用者的語音輸入，然後透過語音傳達結果。您會推薦哪個解決方案？

**[選項]**
- A. Use Amazon Polly to convert speech to text for downstream analysis. Then use Amazon Transcribe to convey the text results via speech／使用 Amazon Polly 將語音轉換為文字進行下游分析，然後使用 Amazon Transcribe 透過語音傳達文字結果
- B. Use Amazon Translate to convert speech to text for downstream analysis. Then use Amazon Polly to convey the text results via speech／使用 Amazon Translate 將語音轉換為文字進行下游分析，然後使用 Amazon Polly 透過語音傳達文字結果
- C. Use Amazon Polly to convert speech to text for downstream analysis. Then use Amazon Translate to convey the text results via speech／使用 Amazon Polly 將語音轉換為文字進行下游分析，然後使用 Amazon Translate 透過語音傳達文字結果
- D. Use Amazon Transcribe to convert speech to text for downstream analysis. Then use Amazon Polly to convey the text results via speech／使用 Amazon Transcribe 將語音轉換為文字進行下游分析，然後使用 Amazon Polly 透過語音傳達文字結果

**正確答案**
Use Amazon Transcribe to convert speech to text for downstream analysis. Then use Amazon Polly to convey the text results via speech／使用 Amazon Transcribe 將語音轉換為文字進行下游分析，然後使用 Amazon Polly 透過語音傳達文字結果

**為什麼正確**
Use **Amazon Transcribe** to convert speech to text, then use **Amazon Polly** to convey results via speech.
使用 **Amazon Transcribe** 將語音轉為文字，再使用 **Amazon Polly** 將文字結果轉為語音。
**[AI/ML 語音服務]**
| 服務 | 功能 |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Use Amazon Polly to convert speech to text for downstream analysis. Then use Amazon Transcribe to convey the text results via speech／使用 Amazon Polly 將語音轉換為文字進行下游分析，然後使用 Amazon Transcribe 透過語音傳達文字結果 | ❌ 錯誤 | Polly 是文字轉語音，不負責語音轉文字。 |
| Use Amazon Translate to convert speech to text for downstream analysis. Then use Amazon Polly to convey the text results via speech／使用 Amazon Translate 將語音轉換為文字進行下游分析，然後使用 Amazon Polly 透過語音傳達文字結果 | ❌ 錯誤 | Translate 是文字翻譯服務，不是語音轉文字服務。 |
| Use Amazon Polly to convert speech to text for downstream analysis. Then use Amazon Translate to convey the text results via speech／使用 Amazon Polly 將語音轉換為文字進行下游分析，然後使用 Amazon Translate 透過語音傳達文字結果 | ❌ 錯誤 | Polly 是文字轉語音，不負責語音轉文字。 |
| Use Amazon Transcribe to convert speech to text for downstream analysis. Then use Amazon Polly to convey the text results via speech／使用 Amazon Transcribe 將語音轉換為文字進行下游分析，然後使用 Amazon Polly 透過語音傳達文字結果 | ✅ 正確 | Amazon Transcribe 將語音轉文字，Amazon Polly 再將文字轉成語音。 |

---

## 問題 28

**題目**
Which AWS service will help you receive alerts when the reservation utilization falls below the defined threshold?
哪個 AWS 服務將在預留使用率低於定義閾值時幫助您接收警報？

**[選項]**
- A. AWS Trusted Advisor（最佳實務建議）
- B. AWS Pricing Calculator（費用估算）
- C. AWS CloudTrail（活動稽核記錄）
- D. AWS Budgets（預算警示）

**正確答案**
AWS Budgets（預算警示）

**為什麼正確**
**[成本管理服務比較]**
| 服務 | 主要功能 |
| --- | --- |
| **AWS Budgets** | **設定預算和警示（含預留使用率）** |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Trusted Advisor（最佳實務建議） | ❌ 錯誤 | Trusted Advisor 提供成本、安全、效能、容錯與服務限制建議，不會自動執行遷移或取代專家顧問。 |
| AWS Pricing Calculator（費用估算） | ❌ 錯誤 | Pricing Calculator 用來事前估算 AWS 架構的月費。 |
| AWS CloudTrail（活動稽核記錄） | ❌ 錯誤 | CloudTrail 記錄 API 呼叫與帳號活動，重點是稽核誰在何時做了什麼。 |
| AWS Budgets（預算警示） | ✅ 正確 | AWS Budgets 可設定成本、用量與預留使用率警示。 |

---

## 問題 29

**題目**
A company wants to identify the optimal AWS resource configuration for its workloads so that the company can reduce costs and increase workload performance. Which of the following services can be used to meet this requirement?
一家公司希望為其工作負載識別最佳 AWS 資源設定，以降低成本並提升工作負載效能。以下哪個服務可用於滿足此需求？

**[選項]**
- A. AWS Cost Explorer（成本分析）
- B. AWS Budgets（預算警示）
- C. AWS Systems Manager（系統管理）
- D. AWS Compute Optimizer（資源規格建議）

**正確答案**
AWS Compute Optimizer（資源規格建議）

**為什麼正確**
**AWS Compute Optimizer** 使用機器學習分析歷史使用指標，為以下資源提供最優配置建議：
- Amazon EC2 執行個體
- Amazon EBS 磁碟區
- AWS Lambda 函數


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Cost Explorer（成本分析） | ❌ 錯誤 | Cost Explorer 用於分析已產生或歷史成本趨勢，不是最細報表或事前估價工具。 |
| AWS Budgets（預算警示） | ❌ 錯誤 | AWS Budgets 用來設定預算與警示，重點是事後追蹤或避免超支。 |
| AWS Systems Manager（系統管理） | ❌ 錯誤 | Systems Manager 用於管理 EC2 或本地伺服器，例如命令執行、修補與盤點，不管理 Organizations 帳戶移除或 DDoS 防護。 |
| AWS Compute Optimizer（資源規格建議） | ✅ 正確 | AWS Compute Optimizer 使用機器學習分析歷史使用指標，為以下資源提供最優配置建議：；Amazon EC2 執行個體；Amazon EBS 磁碟區；AWS Lambda 函數。 |

---

## 問題 30

**題目**
Which of the following is the MOST cost-effective option to purchase an EC2 Reserved Instance (RI)?
以下哪個是購買 EC2 保留執行個體（RI）最具成本效益的選項？

**[選項]**
- A. All upfront payment option with the standard 1-year term／標準 1 年期全額預付選項
- B. No upfront payment option with standard 1-year term／標準 1 年期無預付選項
- C. No upfront payment option with standard 3-years term／標準 3 年期無預付選項
- D. Partial upfront payment option with standard 3-years term／標準 3 年期部分預付選項

**正確答案**
Partial upfront payment option with standard 3-years term／標準 3 年期部分預付選項

**為什麼正確**
**[RI 費用節省比較]**
| 選項 | 節省 |
| --- | --- |
| 1 年期無預付 | 36% |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| All upfront payment option with the standard 1-year term／標準 1 年期全額預付選項 | ❌ 錯誤 | 1 年期全額預付通常仍不如 3 年期方案省。 |
| No upfront payment option with standard 1-year term／標準 1 年期無預付選項 | ❌ 錯誤 | 1 年期無預付折扣較低，通常不是 Reserved Instance 最省成本的購買方式。 |
| No upfront payment option with standard 3-years term／標準 3 年期無預付選項 | ❌ 錯誤 | 3 年期無預付有折扣，但通常不如 3 年期部分預付或全預付省。 |
| Partial upfront payment option with standard 3-years term／標準 3 年期部分預付選項 | ✅ 正確 | 3 年期部分預付通常比 1 年期或無預付方案更省成本。 |

---

## 問題 31

**題目**
Which of the following AWS services can be used to connect a company's on-premises environment to a VPC without using the public internet?
以下哪個 AWS 服務可用於在不使用公共網際網路的情況下將公司的本地環境連接至 VPC？

**[選項]**
- A. AWS Site-to-Site VPN（站台對站台 VPN）
- B. Internet Gateway／網際網路閘道
- C. VPC Endpoint／VPC 端點
- D. AWS Direct Connect（專線連線）

**正確答案**
AWS Direct Connect（專線連線）

**為什麼正確**
**[連接選項比較]**
| 服務 | 連接方式 | 公共網際網路 |
| --- | --- | --- |
| **AWS Direct Connect** | **專用實體線路** | **❌ 不經過** |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Site-to-Site VPN（站台對站台 VPN） | ❌ 錯誤 | Site-to-Site VPN 是經公共網際網路建立的加密通道，不是專用實體線路。 |
| Internet Gateway／網際網路閘道 | ❌ 錯誤 | Internet Gateway 讓 VPC 公有子網路連上網際網路，不提供私有 AWS 服務連線。 |
| VPC Endpoint／VPC 端點 | ❌ 錯誤 | VPC Endpoint 可讓 VPC 私有連到支援服務；若題目問本地到 AWS 的專線，這不是答案。 |
| AWS Direct Connect（專線連線） | ✅ 正確 | Direct Connect 是本地資料中心到 AWS 的專用實體線路，不經公共網際網路。 |

---

## 問題 32

**題目**
A Project Manager is confused about how credits are used in AWS. There are two credits available: Credit one is for $100, expires July 2022, and can be used for either Amazon S3 or Amazon EC2. Credit two is for $50, expires December 2022, and can be used only for Amazon EC2. The account has incurred charges: $1000 for Amazon EC2 and $500 for Amazon S3. What will be the outcome on the overall bill once the credits are used? (Select two)
一位專案經理對 AWS 中的信用額度使用方式感到困惑。有兩個可用信用額度：信用額度一為 100 美元，2022 年 7 月到期，可用於 Amazon S3 或 Amazon EC2；信用額度二為 50 美元，2022 年 12 月到期，只能用於 Amazon EC2。帳戶已產生費用：Amazon EC2 1000 美元，Amazon S3 500 美元。使用信用額度後，整體帳單會有什麼結果？（選兩項）

**[選項]**
- A. Then, credit two is applied to $500 for Amazon S3 usage／然後，信用額度二套用於 Amazon S3 使用的 500 美元
- B. Only one credit can be used in one billing cycle and the customer has a choice to choose from the available ones／在一個帳單週期內只能使用一個信用額度，客戶可以從可用的信用額度中選擇
- C. Credit one is applied, which expires in July, to Amazon S3 usage which leaves you with a $1000 Amazon EC2 charge and a $400 Amazon S3 charge／7 月到期的信用額度一套用於 Amazon S3 使用費，剩餘 Amazon EC2 費用 1000 美元和 Amazon S3 費用 400 美元
- D. Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge／7 月到期的信用額度一套用於 Amazon EC2 費用，剩餘 Amazon EC2 費用 900 美元和 Amazon S3 費用 500 美元
- E. Then, credit two is applied to the remaining $900 of Amazon EC2 usage／然後，信用額度二套用於剩餘 900 美元的 Amazon EC2 使用費

**正確答案**
Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge／7 月到期的信用額度一套用於 Amazon EC2 費用，剩餘 Amazon EC2 費用 900 美元和 Amazon S3 費用 500 美元；Then, credit two is applied to the remaining $900 of Amazon EC2 usage／然後，信用額度二套用於剩餘 900 美元的 Amazon EC2 使用費

**為什麼正確**
1. Credit one applied to EC2 → $900 EC2, $500 S3 remaining
2. Credit two applied to $900 EC2 → Final: $850 EC2 + $500 S3
**[AWS 信用額度套用順序]**
1. 最快到期的


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Then, credit two is applied to $500 for Amazon S3 usage／然後，信用額度二套用於 Amazon S3 使用的 500 美元 | ❌ 錯誤 | S3 是物件儲存，適合物件、備份與靜態內容，不是可被多台 EC2 同時附加寫入的檔案系統。 |
| Only one credit can be used in one billing cycle and the customer has a choice to choose from the available ones／在一個帳單週期內只能使用一個信用額度，客戶可以從可用的信用額度中選擇 | ❌ 錯誤 | AWS credits 會依可用服務、到期日與帳單套用規則抵扣，不是讓客戶在每個帳單週期手動任選單一 credit。 |
| Credit one is applied, which expires in July, to Amazon S3 usage which leaves you with a $1000 Amazon EC2 charge and a $400 Amazon S3 charge／7 月到期的信用額度一套用於 Amazon S3 使用費，剩餘 Amazon EC2 費用 1000 美元和 Amazon S3 費用 400 美元 | ❌ 錯誤 | S3 是物件儲存，適合物件、備份與靜態內容，不是可被多台 EC2 同時附加寫入的檔案系統。 |
| Credit one is applied, which expires in July, to the Amazon EC2 charge which leaves you with a $900 Amazon EC2 charge and a $500 Amazon S3 charge／7 月到期的信用額度一套用於 Amazon EC2 費用，剩餘 Amazon EC2 費用 900 美元和 Amazon S3 費用 500 美元 | ✅ 正確 | AWS credits 會依到期日與適用服務依序抵扣；先套用較早到期且適用 EC2 的 credit，再套用剩餘 credit。 |
| Then, credit two is applied to the remaining $900 of Amazon EC2 usage／然後，信用額度二套用於剩餘 900 美元的 Amazon EC2 使用費 | ✅ 正確 | AWS credits 會依到期日與適用服務依序抵扣；先套用較早到期且適用 EC2 的 credit，再套用剩餘 credit。 |

---

## 問題 33

**題目**
Which of the following AWS services has encryption enabled by default?
以下哪個 AWS 服務預設啟用加密？

**[選項]**
- A. Amazon Elastic Block Store (Amazon EBS)（區塊儲存）
- B. Amazon Relational Database Service (Amazon RDS)（關聯式資料庫）
- C. Amazon Elastic File System (Amazon EFS)（共享檔案系統）
- D. AWS CloudTrail Logs（稽核事件日誌）

**正確答案**
AWS CloudTrail Logs（稽核事件日誌）

**為什麼正確**
CloudTrail 日誌預設使用 Amazon S3 管理金鑰的伺服器端加密 (SSE-S3)。EBS、EFS 和 RDS 的加密是**可選功能**，需要用戶手動啟用。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic Block Store (Amazon EBS)（區塊儲存） | ❌ 錯誤 | EBS 是 EC2 的區塊儲存，通常附加到單一 AZ 內的執行個體，不適合數百台 EC2 同時共享檔案。 |
| Amazon Relational Database Service (Amazon RDS)（關聯式資料庫） | ❌ 錯誤 | RDS 是關聯式資料庫服務，不是 NoSQL active-active 的主要答案。 |
| Amazon Elastic File System (Amazon EFS)（共享檔案系統） | ❌ 錯誤 | EFS 是可由多台 Linux EC2 同時掛載的共享檔案系統。 |
| AWS CloudTrail Logs（稽核事件日誌） | ✅ 正確 | 記錄並監控 AWS 帳戶中的所有 API 活動，提供事件歷史記錄，適合治理、合規和稽核。 |

---

## 問題 34

**題目**
Which of the following are correct statements regarding the AWS Global Infrastructure? (Select two)
以下哪些陳述關於 AWS 全球基礎設施是正確的？（選兩項）

**[選項]**
- A. Each AWS Region consists of two or more Edge Locations／每個 AWS 區域由兩個或多個邊緣位置組成
- B. Each AWS Region consists of a minimum of two Availability Zones (AZ)／每個 AWS 區域至少由兩個可用區域（AZ）組成
- C. Each Availability Zone (AZ) consists of two or more discrete data centers／每個可用區域（AZ）由兩個或多個獨立資料中心組成
- D. Each AWS Region consists of a minimum of three Availability Zones (AZ)／每個 AWS 區域至少由三個可用區域（AZ）組成
- E. Each Availability Zone (AZ) consists of one or more discrete data centers／每個可用區域（AZ）由一個或多個獨立資料中心組成

**正確答案**
Each AWS Region consists of a minimum of three Availability Zones (AZ)／每個 AWS 區域至少由三個可用區域（AZ）組成；Each Availability Zone (AZ) consists of one or more discrete data centers／每個可用區域（AZ）由一個或多個獨立資料中心組成

**為什麼正確**
1. Each AWS Region consists of a minimum of **three** Availability Zones
2. Each AZ consists of **one or more** discrete data centers
**[AWS 全球基礎設施架構]**
```


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Each AWS Region consists of two or more Edge Locations／每個 AWS 區域由兩個或多個邊緣位置組成 | ❌ 錯誤 | Edge Location 是 CloudFront 等服務的邊緣節點，不是 Region 的組成單位。 |
| Each AWS Region consists of a minimum of two Availability Zones (AZ)／每個 AWS 區域至少由兩個可用區域（AZ）組成 | ❌ 錯誤 | 這份題庫採用的考點是每個 Region 至少三個 AZ。 |
| Each Availability Zone (AZ) consists of two or more discrete data centers／每個可用區域（AZ）由兩個或多個獨立資料中心組成 | ❌ 錯誤 | Availability Zone 可由一個或多個資料中心組成，不一定是兩個以上。 |
| Each AWS Region consists of a minimum of three Availability Zones (AZ)／每個 AWS 區域至少由三個可用區域（AZ）組成 | ✅ 正確 | 每個 AWS 區域至少由三個可用區域組成。 |
| Each Availability Zone (AZ) consists of one or more discrete data centers／每個可用區域（AZ）由一個或多個獨立資料中心組成 | ✅ 正確 | 每個可用區域由一個或多個獨立資料中心組成。 |

---

## 問題 35

**題目**
Which security service of AWS is enabled for all AWS customers, by default, at no additional cost?
哪個 AWS 安全服務預設為所有 AWS 客戶啟用，且無需額外費用？

**[選項]**
- A. AWS Shield Advanced（進階 DDoS 防護）
- B. AWS Web Application Firewall (AWS WAF)（Web 應用程式防火牆）
- C. AWS Secrets Manager（機密管理）
- D. AWS Shield Standard（標準 DDoS 防護）

**正確答案**
AWS Shield Standard（標準 DDoS 防護）

**為什麼正確**
**[Shield 層級比較]**
| 層級 | 費用 | 保護 |
| --- | --- | --- |
| **Standard** | **免費** | Layer 3 & 4 DDoS |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Shield Advanced（進階 DDoS 防護） | ❌ 錯誤 | Shield Advanced 是進階 DDoS 防護，常用於需要額外防護與回應支援的工作負載。 |
| AWS Web Application Firewall (AWS WAF)（Web 應用程式防火牆） | ❌ 錯誤 | AWS WAF 保護 Web 應用程式並過濾 Layer 7 HTTP/HTTPS 請求，不是 DDoS 進階防護本身。 |
| AWS Secrets Manager（機密管理） | ❌ 錯誤 | Secrets Manager 用於保存、輪換密碼與 API Key 等機密，不是加密金鑰或敏感資料掃描服務。 |
| AWS Shield Standard（標準 DDoS 防護） | ✅ 正確 | AWS Shield 可緩解 DDoS 攻擊。 |

---

## 問題 36

**題目**
Which of the following statements are CORRECT regarding the AWS VPC service? (Select two)
以下哪些陳述關於 AWS VPC 服務是正確的？（選兩項）

**[選項]**
- A. A network access control list (network ACL) can have allow rules only／網路存取控制清單（網路 ACL）只能有允許規則
- B. A Security Group can have both allow and deny rules／安全群組可以同時具有允許和拒絕規則
- C. A Network Address Translation instance (NAT instance) is managed by AWS／網路位址轉換執行個體（NAT 執行個體）由 AWS 管理
- D. A Network Address Translation gateway (NAT gateway) is managed by AWS／網路位址轉換閘道（NAT 閘道）由 AWS 管理
- E. A Security Group can have allow rules only／安全群組只能有允許規則

**正確答案**
A Network Address Translation gateway (NAT gateway) is managed by AWS／網路位址轉換閘道（NAT 閘道）由 AWS 管理；A Security Group can have allow rules only／安全群組只能有允許規則

**為什麼正確**
1. 安全群組只能有允許規則
2. NAT 閘道由 AWS 管理
**[VPC 安全組件比較]**
| 組件 | 規則類型 | 層級 | 管理者 |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| A network access control list (network ACL) can have allow rules only／網路存取控制清單（網路 ACL）只能有允許規則 | ❌ 錯誤 | Network ACL 同時支援 allow 與 deny 規則。 |
| A Security Group can have both allow and deny rules／安全群組可以同時具有允許和拒絕規則 | ❌ 錯誤 | Security Group 只支援 allow 規則，不支援 deny 規則。 |
| A Network Address Translation instance (NAT instance) is managed by AWS／網路位址轉換執行個體（NAT 執行個體）由 AWS 管理 | ❌ 錯誤 | NAT Instance 是客戶自行在 EC2 上管理，AWS 代管的是 NAT Gateway。 |
| A Network Address Translation gateway (NAT gateway) is managed by AWS／網路位址轉換閘道（NAT 閘道）由 AWS 管理 | ✅ 正確 | 網路位址轉換閘道由 AWS 管理。 |
| A Security Group can have allow rules only／安全群組只能有允許規則 | ✅ 正確 | 安全群組只能有允許規則。 |

---

## 問題 37

**題目**
A company uses reserved EC2 instances across multiple units with each unit having its own AWS account. However, some of the units under-utilize their reserved instances while other units need more. Which of the following would you recommend as the most cost-optimal solution?
一家公司在多個業務單元中使用保留 EC2 執行個體，每個業務單元都有自己的 AWS 帳戶。但是，一些業務單元未充分使用其保留執行個體，而其他業務單元需要更多。您會推薦以下哪個最具成本效益的解決方案？

**[選項]**
- A. Use AWS Cost Explorer to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units／使用 AWS Cost Explorer 管理所有業務單元的 AWS 帳戶，然後在所有業務單元之間共享保留 EC2 執行個體
- B. Use AWS Systems Manager to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units／使用 AWS Systems Manager 管理所有業務單元的 AWS 帳戶，然後在所有業務單元之間共享保留 EC2 執行個體
- C. Use AWS Trusted Advisor to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units／使用 AWS Trusted Advisor 管理所有業務單元的 AWS 帳戶，然後在所有業務單元之間共享保留 EC2 執行個體
- D. Use AWS Organizations to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units／使用 AWS Organizations 管理所有業務單元的 AWS 帳戶，然後在所有業務單元之間共享保留 EC2 執行個體

**正確答案**
Use AWS Organizations to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units／使用 AWS Organizations 管理所有業務單元的 AWS 帳戶，然後在所有業務單元之間共享保留 EC2 執行個體

**為什麼正確**
**AWS Organizations** 允許集中管理多個 AWS 帳戶的計費，並在帳戶之間共享預留執行個體，對所有 AWS 客戶免費提供。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Use AWS Cost Explorer to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units／使用 AWS Cost Explorer 管理所有業務單元的 AWS 帳戶，然後在所有業務單元之間共享保留 EC2 執行個體 | ❌ 錯誤 | EC2 是可管理的虛擬伺服器，屬於運算服務，不是受管儲存、資料庫或訊息服務。 |
| Use AWS Systems Manager to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units／使用 AWS Systems Manager 管理所有業務單元的 AWS 帳戶，然後在所有業務單元之間共享保留 EC2 執行個體 | ❌ 錯誤 | Systems Manager 用於管理 EC2 或本地伺服器，例如命令執行、修補與盤點，不管理 Organizations 帳戶移除或 DDoS 防護。 |
| Use AWS Trusted Advisor to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units／使用 AWS Trusted Advisor 管理所有業務單元的 AWS 帳戶，然後在所有業務單元之間共享保留 EC2 執行個體 | ❌ 錯誤 | Trusted Advisor 提供成本、安全、效能、容錯與服務限制建議，不會自動執行遷移或取代專家顧問。 |
| Use AWS Organizations to manage AWS accounts of all units and then share the reserved EC2 instances amongst all units／使用 AWS Organizations 管理所有業務單元的 AWS 帳戶，然後在所有業務單元之間共享保留 EC2 執行個體 | ✅ 正確 | AWS Organizations 可集中管理多個帳戶，並讓 Reserved Instance 折扣在組織內共享。 |

---

## 問題 38

**題目**
A company runs an application on a fleet of EC2 instances. The company wants to automate the traditional maintenance job of running timely assessments and checking for OS vulnerabilities. Which service will you suggest for this use case?
一家公司在 EC2 執行個體群上執行應用程式。公司希望自動化執行定期評估和檢查作業系統漏洞的傳統維護工作。您會建議哪個服務？

**[選項]**
- A. Amazon GuardDuty（威脅偵測）
- B. Amazon Macie（敏感資料探索）
- C. AWS Shield（DDoS 防護）
- D. Amazon Inspector（弱點評估）

**正確答案**
Amazon Inspector（弱點評估）

**為什麼正確**
**[安全服務比較]**
| 服務 | 功能 |
| --- | --- |
| **Amazon Inspector** | **EC2 執行個體漏洞評估** |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon GuardDuty（威脅偵測） | ❌ 錯誤 | GuardDuty 是威脅偵測服務，分析可疑帳號、網路與工作負載活動。 |
| Amazon Macie（敏感資料探索） | ❌ 錯誤 | Macie 用於探索與識別 S3 中的敏感資料，例如個資或機密資料。 |
| AWS Shield（DDoS 防護） | ❌ 錯誤 | AWS Shield 主要防護 DDoS 攻擊，不是弱點掃描、敏感資料探索或 Web 規則過濾。 |
| Amazon Inspector（弱點評估） | ✅ 正確 | 此選項符合題目中的核心需求。 |

---

## 問題 39

**題目**
Which of the following is a recommended way to provide programmatic access to AWS resources?
以下哪項是提供對 AWS 資源進行程式化存取的推薦方式？

**[選項]**
- A. Create a new IAM user and share the username and password／建立新的 IAM 使用者並共享使用者名稱和密碼
- B. Use IAM user group to access AWS resources programmatically／使用 IAM 使用者群組以程式化方式存取 AWS 資源
- C. Use AWS Multi-Factor Authentication (AWS MFA) to access AWS resources programmatically／使用 AWS 多重要素驗證（AWS MFA）以程式化方式存取 AWS 資源
- D. Use Access Key ID and Secret Access Key to access AWS resources programmatically／使用存取金鑰 ID 和私密存取金鑰以程式化方式存取 AWS 資源

**正確答案**
Use Access Key ID and Secret Access Key to access AWS resources programmatically／使用存取金鑰 ID 和私密存取金鑰以程式化方式存取 AWS 資源

**為什麼正確**
**存取金鑰 (Access Keys)** 由兩部分組成：存取金鑰 ID 和私密存取金鑰，用於簽署 AWS CLI 或 API 的程式化請求。兩者必須同時使用才能驗證請求。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Create a new IAM user and share the username and password／建立新的 IAM 使用者並共享使用者名稱和密碼 | ❌ 錯誤 | 共用 IAM 使用者帳密不安全，也無法提供可追蹤的個別程式化存取。 |
| Use IAM user group to access AWS resources programmatically／使用 IAM 使用者群組以程式化方式存取 AWS 資源 | ❌ 錯誤 | IAM user group 用來套用權限，不是 API 請求使用的憑證。 |
| Use AWS Multi-Factor Authentication (AWS MFA) to access AWS resources programmatically／使用 AWS 多重要素驗證（AWS MFA）以程式化方式存取 AWS 資源 | ❌ 錯誤 | MFA 是第二層驗證，不取代 Access Key 與 Secret Access Key 簽署 API 請求。 |
| Use Access Key ID and Secret Access Key to access AWS resources programmatically／使用存取金鑰 ID 和私密存取金鑰以程式化方式存取 AWS 資源 | ✅ 正確 | Access Key ID 與 Secret Access Key 用來簽署 AWS API/CLI 的程式化請求。 |

---

## 問題 40

**題目**
A research group wants to use EC2 instances to run a scientific computation application that already has a fault tolerant architecture. The application needs high-performance hardware disks that provide fast I/O performance. Which of the following storage options would you recommend as the MOST cost-effective solution?
一個研究群組希望使用 EC2 執行個體執行已具有容錯架構的科學運算應用程式。應用程式需要提供快速 I/O 效能的高效能硬體磁碟。您會推薦以下哪個儲存選項作為最具成本效益的解決方案？

**[選項]**
- A. Amazon Simple Storage Service (Amazon S3)（物件儲存）
- B. Amazon Elastic Block Store (EBS)（區塊儲存）
- C. Amazon Elastic File System (Amazon EFS)（共享檔案系統）
- D. Instance Store／執行個體存放區

**正確答案**
Instance Store／執行個體存放區

**為什麼正確**
**Instance Store** 提供臨時性區塊層級儲存，實體附加在主機電腦上，具有極低延遲。由於已包含在執行個體使用成本中（無需額外費用），且應用程式本身具有容錯架構可處理資料遺失，因此是最具成本效益的選擇。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Simple Storage Service (Amazon S3)（物件儲存） | ❌ 錯誤 | S3 是物件儲存，適合物件、備份與靜態內容，不是可被多台 EC2 同時附加寫入的檔案系統。 |
| Amazon Elastic Block Store (EBS)（區塊儲存） | ❌ 錯誤 | EBS 是 EC2 的區塊儲存，通常附加到單一 AZ 內的執行個體，不適合數百台 EC2 同時共享檔案。 |
| Amazon Elastic File System (Amazon EFS)（共享檔案系統） | ❌ 錯誤 | EFS 是可由多台 Linux EC2 同時掛載的共享檔案系統。 |
| Instance Store／執行個體存放區 | ✅ 正確 | Instance Store 是附加在實體主機上的暫時性高速儲存，適合可容忍資料遺失的高 I/O 工作負載。 |

---

## 問題 41

**題目**
An e-commerce company has deployed an RDS database in a single Availability Zone (AZ). The engineering team wants to ensure that in case of an AZ outage, the database should continue working on the same endpoint without any manual administrative intervention. Which of the following solutions can address this use-case?
一家電子商務公司在單一可用區域（AZ）中部署了 RDS 資料庫。工程團隊希望確保在 AZ 中斷的情況下，資料庫應在同一端點上繼續工作，無需任何手動管理干預。以下哪個解決方案可以解決此使用案例？

**[選項]**
- A. Configure the database in RDS read replica mode with automatic failover to the standby／以自動容錯移轉至待機的 RDS 讀取副本模式設定資料庫
- B. Provision the database via AWS CloudFormation／透過 AWS CloudFormation 佈建資料庫
- C. Deploy the database via AWS Elastic Beanstalk／透過 AWS Elastic Beanstalk 部署資料庫
- D. Configure the database in RDS Multi-AZ deployment with automatic failover to the standby／以自動容錯移轉至待機的 RDS Multi-AZ 部署模式設定資料庫

**正確答案**
Configure the database in RDS Multi-AZ deployment with automatic failover to the standby／以自動容錯移轉至待機的 RDS Multi-AZ 部署模式設定資料庫

**為什麼正確**
**RDS Multi-AZ** 自動在不同 AZ 建立備用執行個體並同步複製資料。發生故障時自動容錯移轉，且**資料庫端點保持不變**，無需手動干預。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Configure the database in RDS read replica mode with automatic failover to the standby／以自動容錯移轉至待機的 RDS 讀取副本模式設定資料庫 | ❌ 錯誤 | RDS Read Replica 主要用於讀取擴展，傳統上不提供與 Multi-AZ standby 相同的同步備援與同端點自動容錯移轉。 |
| Provision the database via AWS CloudFormation／透過 AWS CloudFormation 佈建資料庫 | ❌ 錯誤 | CloudFormation 用模板建立與管理 AWS 資源，不是除錯追蹤、帳單估算或資料庫容錯服務。 |
| Deploy the database via AWS Elastic Beanstalk／透過 AWS Elastic Beanstalk 部署資料庫 | ❌ 錯誤 | Elastic Beanstalk 是應用部署平台，重點是代管部署流程，不是負載平衡或資料庫容錯設定本身。 |
| Configure the database in RDS Multi-AZ deployment with automatic failover to the standby／以自動容錯移轉至待機的 RDS Multi-AZ 部署模式設定資料庫 | ✅ 正確 | RDS Multi-AZ 會同步複寫到備用執行個體，故障時可自動容錯移轉且端點不變。 |

---

## 問題 42

**題目**
Compared to the on-demand instance prices, what is the highest possible discount offered for spot instances?
與隨需執行個體價格相比，Spot 執行個體提供的最高折扣是多少？

**[選項]**
- A. 50%
- B. 75%
- C. 10%
- D. 90%

**正確答案**
90%

**為什麼正確**
**[EC2 最高折扣]**
- On-Demand：基準價格
- Reserved Instance：最高 **75%** 折扣
- Spot Instance：最高 **90%** 折扣（但可被中斷）


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| 50% | ❌ 錯誤 | Spot Instances 最高可比 On-Demand 價格便宜到 90%，這不是最高折扣。 |
| 75% | ❌ 錯誤 | Spot Instances 最高可比 On-Demand 價格便宜到 90%，這不是最高折扣。 |
| 10% | ❌ 錯誤 | Spot Instances 最高可比 On-Demand 價格便宜到 90%，這不是最高折扣。 |
| 90% | ✅ 正確 | Spot Instances 最高可比 On-Demand 價格便宜 90%。 |

---

## 問題 43

**題目**
A cyber forensics team has detected that AWS owned IP-addresses are being used to carry out malicious attacks. Which is the correct solution to address this issue?
一個網路鑑識團隊發現 AWS 擁有的 IP 位址被用於執行惡意攻擊。解決此問題的正確解決方案是什麼？

**[選項]**
- A. Contact AWS Support／聯繫 AWS Support
- B. Write an email to Jeff Bezos, the founder of Amazon, with the details of the incident／向 Amazon 創始人 Jeff Bezos 發送電子郵件，說明事件詳情
- C. Contact AWS Developer Forum moderators／聯繫 AWS 開發人員論壇版主
- D. Contact AWS Abuse Team／聯繫 AWS 濫用團隊

**正確答案**
Contact AWS Abuse Team／聯繫 AWS 濫用團隊

**為什麼正確**
**AWS 濫用團隊**專門處理 AWS 資源被用於濫用行為的情況，包括垃圾郵件、DDoS 攻擊、惡意軟體傳播等。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Contact AWS Support／聯繫 AWS Support | ❌ 錯誤 | AWS Support 處理一般技術與帳務支援；AWS IP 被濫用攻擊時應走 Abuse 回報流程。 |
| Write an email to Jeff Bezos, the founder of Amazon, with the details of the incident／向 Amazon 創始人 Jeff Bezos 發送電子郵件，說明事件詳情 | ❌ 錯誤 | 寄信給公司創辦人不是 AWS 官方事件回報流程。 |
| Contact AWS Developer Forum moderators／聯繫 AWS 開發人員論壇版主 | ❌ 錯誤 | Developer Forums 是社群討論管道，不是正式支援、濫用回報或遷移交付服務。 |
| Contact AWS Abuse Team／聯繫 AWS 濫用團隊 | ✅ 正確 | AWS Abuse Team 是回報 AWS 資源遭濫用或被用於惡意活動的正式管道。 |

---

## 問題 44

**題目**
Which of the following is an INCORRECT statement about Scaling, a design principle of Reliability pillar of the AWS Well-Architected Framework?
以下哪項關於 AWS Well-Architected Framework 可靠性支柱的設計原則「擴展」的陳述是不正確的？

**[選項]**
- A. Fault tolerance is achieved by a scale out operation／容錯能力透過向外擴展操作實現
- B. A scale out operation implies you scale by adding more instances to your existing pool of resources／向外擴展操作意味著透過向現有資源池中新增更多執行個體來擴展
- C. A scale up operation implies you scale by adding more power (CPU, RAM) to your existing machine/node／向上擴展操作意味著透過向現有機器/節點新增更多算力（CPU、RAM）來擴展
- D. Fault tolerance is achieved by a scale up operation／容錯能力透過向上擴展操作實現

**正確答案**
Fault tolerance is achieved by a scale up operation／容錯能力透過向上擴展操作實現

**為什麼正確**
"Fault tolerance is achieved by a **scale up** operation"
「容錯是透過**向上擴展**操作實現的」
**[水平擴展 vs 垂直擴展]**
| 擴展類型 | 方式 | 容錯能力 |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Fault tolerance is achieved by a scale out operation／容錯能力透過向外擴展操作實現 | ❌ 錯誤 | 這句話本身是正確的：向外擴展是增加更多執行個體，通常能提升容錯能力。 |
| A scale out operation implies you scale by adding more instances to your existing pool of resources／向外擴展操作意味著透過向現有資源池中新增更多執行個體來擴展 | ❌ 錯誤 | 這句話本身是正確的：向外擴展是增加更多執行個體，通常能提升容錯能力。 |
| A scale up operation implies you scale by adding more power (CPU, RAM) to your existing machine/node／向上擴展操作意味著透過向現有機器/節點新增更多算力（CPU、RAM）來擴展 | ❌ 錯誤 | 這句話本身是正確的：向上擴展是增加單一機器的 CPU、記憶體等資源。 |
| Fault tolerance is achieved by a scale up operation／容錯能力透過向上擴展操作實現 | ✅ 正確 | 這句話是不正確的：容錯能力通常靠向外擴展增加多個節點，而不是只把單一節點加大。 |

---

## 問題 45

**題目**
Which of the following are the storage services offered by the AWS Cloud? (Select two)
以下哪些是 AWS 雲端提供的儲存服務？（選兩項）

**[選項]**
- A. Amazon Simple Notification Service (SNS)（一對多通知）
- B. Amazon Simple Queue Service (SQS)（訊息佇列）
- C. Amazon Elastic Compute Cloud (Amazon EC2)（虛擬伺服器）
- D. Amazon Simple Storage Service (Amazon S3)（物件儲存）
- E. Amazon Elastic File System (Amazon EFS)（共享檔案系統）

**正確答案**
Amazon Simple Storage Service (Amazon S3)（物件儲存）；Amazon Elastic File System (Amazon EFS)（共享檔案系統）

**為什麼正確**
1. Amazon S3（物件儲存）
2. Amazon EFS（文件儲存）
**[AWS 儲存服務]**
- **S3**：物件儲存


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Simple Notification Service (SNS)（一對多通知） | ❌ 錯誤 | SNS 是一對多發布通知服務，適合把同一則訊息廣播給多個訂閱者。 |
| Amazon Simple Queue Service (SQS)（訊息佇列） | ❌ 錯誤 | SQS 是訊息佇列，用來暫存訊息並解耦生產者與消費者。 |
| Amazon Elastic Compute Cloud (Amazon EC2)（虛擬伺服器） | ❌ 錯誤 | EC2 是可管理的虛擬伺服器，屬於運算服務，不是受管儲存、資料庫或訊息服務。 |
| Amazon Simple Storage Service (Amazon S3)（物件儲存） | ✅ 正確 | Amazon S3 是 AWS 物件儲存服務。 |
| Amazon Elastic File System (Amazon EFS)（共享檔案系統） | ✅ 正確 | Amazon EFS 是 AWS 共享檔案系統服務。 |

---

## 問題 46

**題目**
A startup wants to set up its IT infrastructure on AWS Cloud. The CTO would like to get an estimate of the monthly AWS bill based on the AWS services that the startup wants to use. Which AWS service would you suggest for this use-case?
一家新創公司希望在 AWS 雲端上建立其 IT 基礎設施。CTO 希望根據新創公司想要使用的 AWS 服務獲得每月 AWS 帳單的估算。您會建議哪個 AWS 服務？

**[選項]**
- A. AWS Budgets（預算警示）
- B. AWS Cost Explorer（成本分析）
- C. AWS Cost & Usage Report (AWS CUR)（成本用量報表）
- D. AWS Pricing Calculator（費用估算）

**正確答案**
AWS Pricing Calculator（費用估算）

**為什麼正確**
**AWS Pricing Calculator** 讓您在建構前探索 AWS 服務並建立成本估算，可模擬解決方案、探索定價點和計算方式，以及找到可用的執行個體類型和合約條款。
網址：https://calculator.aws/


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Budgets（預算警示） | ❌ 錯誤 | AWS Budgets 用來設定預算與警示，重點是事後追蹤或避免超支。 |
| AWS Cost Explorer（成本分析） | ❌ 錯誤 | Cost Explorer 用於分析已產生或歷史成本趨勢，不是最細報表或事前估價工具。 |
| AWS Cost & Usage Report (AWS CUR)（成本用量報表） | ❌ 錯誤 | Cost & Usage Report 提供最細的成本與用量資料，不是互動式月費估算器。 |
| AWS Pricing Calculator（費用估算） | ✅ 正確 | AWS Pricing Calculator 可在使用前估算 AWS 服務的每月費用。 |

---

## 問題 47

**題目**
According to the AWS Cloud Adoption Framework (AWS CAF), what are two tasks that a company should perform when planning to migrate to the AWS Cloud and aiming to become more responsive to customer inquiries and feedback as part of their organizational transformation? (Select two)
根據 AWS 雲端採用框架（AWS CAF），一家公司在計劃遷移至 AWS 雲端並作為組織轉型的一部分以更快速回應客戶詢問和回饋時，應執行哪兩項任務？（選兩項）

**[選項]**
- A. Organize your teams around bureaucratic design principles／圍繞官僚設計原則組織您的團隊
- B. Leverage legacy infrastructure for cost efficiencies／利用舊有基礎設施提高成本效益
- C. Create new analytical insights with existing products and services／利用現有產品和服務建立新的分析洞察
- D. Organize your teams around products and value streams／圍繞產品和價值流組織您的團隊
- E. Leverage agile methods to rapidly iterate and evolve／利用敏捷方法快速迭代和演進

**正確答案**
Organize your teams around products and value streams／圍繞產品和價值流組織您的團隊；Leverage agile methods to rapidly iterate and evolve／利用敏捷方法快速迭代和演進

**為什麼正確**
1. 圍繞產品和價值流組織團隊
2. 利用敏捷方法快速迭代和演進
**[AWS CAF 六大視角]**
Business → People → Governance → Platform → Security → Operations


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Organize your teams around bureaucratic design principles／圍繞官僚設計原則組織您的團隊 | ❌ 錯誤 | CAF 組織轉型鼓勵以產品和價值流組織團隊，不是官僚式設計。 |
| Leverage legacy infrastructure for cost efficiencies／利用舊有基礎設施提高成本效益 | ❌ 錯誤 | CAF 組織轉型強調產品、價值流與敏捷方法，不是依賴舊有基礎設施。 |
| Create new analytical insights with existing products and services／利用現有產品和服務建立新的分析洞察 | ❌ 錯誤 | 建立分析洞察偏資料與分析能力，不是組織轉型中提升回應速度的核心任務。 |
| Organize your teams around products and value streams／圍繞產品和價值流組織您的團隊 | ✅ 正確 | 圍繞產品和價值流組織您的團隊。 |
| Leverage agile methods to rapidly iterate and evolve／利用敏捷方法快速迭代和演進 | ✅ 正確 | 利用敏捷方法快速迭代和演進。 |

---

## 問題 48

**題目**
A big data analytics company is moving its IT infrastructure from an on-premises data center to AWS Cloud. The company has some server-bound software licenses that it wants to use on AWS. Which of the following EC2 instance types would you recommend to the company?
一家大數據分析公司正在將其 IT 基礎設施從本地資料中心遷移至 AWS 雲端。公司有一些希望在 AWS 上使用的伺服器綁定軟體授權。您會向公司推薦以下哪種 EC2 執行個體類型？

**[選項]**
- A. Dedicated Instance／專用執行個體
- B. On-Demand Instance／隨需執行個體
- C. Reserved Instance (RI)／保留執行個體
- D. Dedicated Host／專用主機

**正確答案**
Dedicated Host／專用主機

**為什麼正確**
**[Dedicated Host vs Dedicated Instance]**
| 特性 | Dedicated Host | Dedicated Instance |
| --- | --- | --- |
| 實體伺服器控制 | ✅ 完整 | ❌ 無 |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Dedicated Instance／專用執行個體 | ❌ 錯誤 | Dedicated Instance 會在專用硬體上執行，但客戶不能像 Dedicated Host 一樣控制實體主機層級。 |
| On-Demand Instance／隨需執行個體 | ❌ 錯誤 | On-Demand 不需長期承諾但單價較高，適合短期或不可預測工作負載。 |
| Reserved Instance (RI)／保留執行個體 | ❌ 錯誤 | Reserved Instance 適合長期穩定使用；若題目問短期彈性或硬體專用，RI 不是重點。 |
| Dedicated Host／專用主機 | ✅ 正確 | Dedicated Host 提供專用實體伺服器控制能力，適合 BYOL 或合規需求。 |

---

## 問題 49

**題目**
Under the AWS Shared Responsibility Model, which of the following is a shared responsibility of both AWS and the customer?
根據 AWS 共同責任模型，以下哪項是 AWS 和客戶的共同責任？

**[選項]**
- A. Availability Zone (AZ) infrastructure maintenance／可用區域（AZ）基礎設施維護
- B. Infrastructure maintenance of Amazon S3 storage servers／Amazon S3 儲存伺服器的基礎設施維護
- C. Guarantee data separation among various AWS customers／保證不同 AWS 客戶之間的資料隔離
- D. Configuration Management／設定管理

**正確答案**
Configuration Management／設定管理

**為什麼正確**
**配置管理**是共同控制項目：AWS 負責維護其基礎設施設備的配置，而客戶負責配置自己的 Guest OS、資料庫和應用程式。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Availability Zone (AZ) infrastructure maintenance／可用區域（AZ）基礎設施維護 | ❌ 錯誤 | 可用區域基礎設施維護屬於 AWS 對雲端底層設施的責任，不是客戶需要負責的雲中設定。 |
| Infrastructure maintenance of Amazon S3 storage servers／Amazon S3 儲存伺服器的基礎設施維護 | ❌ 錯誤 | S3 儲存伺服器的基礎設施維護由 AWS 負責，不是客戶在雲中自行設定的項目。 |
| Guarantee data separation among various AWS customers／保證不同 AWS 客戶之間的資料隔離 | ❌ 錯誤 | 不同 AWS 客戶之間的底層隔離由 AWS 雲端基礎設施負責，不是客戶自行維護的責任。 |
| Configuration Management／設定管理 | ✅ 正確 | Configuration Management 是客戶在雲中管理設定與組態的責任。 |

---

## 問題 50

**題目**
A medical research startup wants to understand the compliance of AWS services concerning HIPAA guidelines. Which AWS service can be used to review the HIPAA compliance and governance-related documents on AWS?
一家醫療研究新創公司希望了解 AWS 服務關於 HIPAA 準則的合規性。哪個 AWS 服務可用於審查 AWS 上與 HIPAA 合規性和治理相關的文件？

**[選項]**
- A. AWS Secrets Manager（機密管理）
- B. AWS Trusted Advisor（最佳實務建議）
- C. AWS Systems Manager（系統管理）
- D. AWS Artifact（合規文件）

**正確答案**
AWS Artifact（合規文件）

**為什麼正確**
**AWS Artifact** 是合規相關資訊的中央資源，提供隨需存取 AWS 安全和合規報告，包括 SOC 報告、PCI 報告，以及供 HIPAA 合規客戶使用的商業夥伴附件 (BAA)。這是一個免費的自助服務入口網站。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Secrets Manager（機密管理） | ❌ 錯誤 | Secrets Manager 用於保存、輪換密碼與 API Key 等機密，不是加密金鑰或敏感資料掃描服務。 |
| AWS Trusted Advisor（最佳實務建議） | ❌ 錯誤 | Trusted Advisor 提供成本、安全、效能、容錯與服務限制建議，不會自動執行遷移或取代專家顧問。 |
| AWS Systems Manager（系統管理） | ❌ 錯誤 | Systems Manager 用於管理 EC2 或本地伺服器，例如命令執行、修補與盤點，不管理 Organizations 帳戶移除或 DDoS 防護。 |
| AWS Artifact（合規文件） | ✅ 正確 | AWS Artifact 提供合規報告與協議文件。 |

---

## 問題 51

**題目**
An IT company is planning to migrate from an on-premises environment to AWS Cloud. Which of the following expense areas would result in cost savings when the company moves to AWS Cloud? (Select two)
一家 IT 公司計劃從本地環境遷移至 AWS 雲端。當公司遷移至 AWS 雲端時，以下哪些費用領域會節省成本？（選兩項）

**[選項]**
- A. Project manager salary／專案經理薪資
- B. Developer salary／開發人員薪資
- C. SaaS application license fee／SaaS 應用程式授權費
- D. Data center physical security expenditure／資料中心實體安全支出
- E. Data center hardware infrastructure expenditure／資料中心硬體基礎設施支出

**正確答案**
Data center physical security expenditure／資料中心實體安全支出；Data center hardware infrastructure expenditure／資料中心硬體基礎設施支出

**為什麼正確**
1. 資料中心硬體基礎設施支出
2. 資料中心實體安全支出
**[成本分析]**
| 支出類型 | 遷移後變化 |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Project manager salary／專案經理薪資 | ❌ 錯誤 | 這屬於軟體授權或人力成本，不是雲端遷移後由 AWS 取代的資料中心基礎設施支出。 |
| Developer salary／開發人員薪資 | ❌ 錯誤 | 這屬於軟體授權或人力成本，不是雲端遷移後由 AWS 取代的資料中心基礎設施支出。 |
| SaaS application license fee／SaaS 應用程式授權費 | ❌ 錯誤 | 這屬於軟體授權或人力成本，不是雲端遷移後由 AWS 取代的資料中心基礎設施支出。 |
| Data center physical security expenditure／資料中心實體安全支出 | ✅ 正確 | 資料中心實體安全支出。 |
| Data center hardware infrastructure expenditure／資料中心硬體基礎設施支出 | ✅ 正確 | 資料中心硬體基礎設施支出。 |

---

## 問題 52

**題目**
What are the advantages that AWS Cloud offers over a traditional on-premises IT infrastructure? (Select two)
AWS 雲端相對於傳統本地 IT 基礎設施提供哪些優勢？（選兩項）

**[選項]**
- A. Make a capacity decision before deploying an application, to reduce costs／在部署應用程式之前做出容量決策，以降低成本
- B. Provide lower latency to applications by maintaining servers on-premises／透過在本地維護伺服器為應用程式提供更低延遲
- C. Increase speed and agility by keeping servers and other required resources ready before time in your data centers／透過提前在資料中心準備好伺服器和其他所需資源來提高速度和敏捷性
- D. Trade capital expense for variable expense／以可變支出換取資本支出
- E. Eliminate guessing on your infrastructure capacity needs／消除對基礎設施容量需求的猜測

**正確答案**
Trade capital expense for variable expense／以可變支出換取資本支出；Eliminate guessing on your infrastructure capacity needs／消除對基礎設施容量需求的猜測

**為什麼正確**
1. 將資本支出換為可變支出
2. 消除對基礎設施容量需求的猜測


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Make a capacity decision before deploying an application, to reduce costs／在部署應用程式之前做出容量決策，以降低成本 | ❌ 錯誤 | 雲端可降低容量預估風險，不需要長時間預先猜測容量。 |
| Provide lower latency to applications by maintaining servers on-premises／透過在本地維護伺服器為應用程式提供更低延遲 | ❌ 錯誤 | 雲端優勢不是靠維持本地伺服器取得低延遲，而是利用全球基礎設施靠近使用者。 |
| Increase speed and agility by keeping servers and other required resources ready before time in your data centers／透過提前在資料中心準備好伺服器和其他所需資源來提高速度和敏捷性 | ❌ 錯誤 | Agility 指快速開發、測試與發布，能更快回應需求變化。 |
| Trade capital expense for variable expense／以可變支出換取資本支出 | ✅ 正確 | 以可變支出換取資本支出。 |
| Eliminate guessing on your infrastructure capacity needs／消除對基礎設施容量需求的猜測 | ✅ 正確 | 消除對基礎設施容量需求的猜測。 |

---

## 問題 53

**題目**
An intern at an IT company provisioned a Linux based On-demand EC2 instance with per-second billing but terminated it within 30 seconds. What is the duration for which the instance would be charged?
一家 IT 公司的實習生佈建了一個按秒計費的基於 Linux 的隨需 EC2 執行個體，但在 30 秒內終止了它。執行個體的計費時間是多少？

**[選項]**
- A. 30 seconds／30 秒
- B. 600 seconds／600 秒
- C. 300 seconds／300 秒
- D. 60 seconds／60 秒

**正確答案**
60 seconds／60 秒

**為什麼正確**
Linux 型 EC2 執行個體有**最少一分鐘**計費規定，即使在 30 秒內終止，仍會按 60 秒收費。
> ⚠️ 雖然 EC2 支援按秒計費，但最少計費時間為 1 分鐘（60 秒）


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| 30 seconds／30 秒 | ❌ 錯誤 | Linux On-Demand 雖然按秒計費，但最低收費時間是 60 秒。 |
| 600 seconds／600 秒 | ❌ 錯誤 | 這超過 Linux On-Demand 執行個體的最低 60 秒收費時間。 |
| 300 seconds／300 秒 | ❌ 錯誤 | 這超過 Linux On-Demand 執行個體的最低 60 秒收費時間。 |
| 60 seconds／60 秒 | ✅ 正確 | Linux On-Demand EC2 雖按秒計費，但最低收費時間是 60 秒。 |

---

## 問題 54

**題目**
Which type of cloud computing does Amazon Elastic Compute Cloud (EC2) represent?
Amazon Elastic Compute Cloud（EC2）代表哪種類型的雲端運算？

**[選項]**
- A. Software as a Service (SaaS)／軟體即服務
- B. Platform as a Service (PaaS)／平台即服務
- C. Network as a Service (NaaS)／網路即服務
- D. Infrastructure as a Service (IaaS)／基礎設施即服務

**正確答案**
Infrastructure as a Service (IaaS)／基礎設施即服務

**為什麼正確**
**[雲端服務類型]**
| 類型 | 說明 | AWS 範例 |
| --- | --- | --- |
| **IaaS** | **基本構建塊，最高控制權** | **EC2, VPC, EBS** |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Software as a Service (SaaS)／軟體即服務 | ❌ 錯誤 | SaaS 是完整軟體應用服務，不是 EC2 代表的基礎設施層。 |
| Platform as a Service (PaaS)／平台即服務 | ❌ 錯誤 | PaaS 抽象化作業系統與平台管理，較像代管應用平台。 |
| Network as a Service (NaaS)／網路即服務 | ❌ 錯誤 | NaaS 偏網路能力服務，不是 EC2 代表的雲端運算類型。 |
| Infrastructure as a Service (IaaS)／基礎設施即服務 | ✅ 正確 | EC2 提供基礎設施層的虛擬伺服器能力，屬於 IaaS。 |

---

## 問題 55

**題目**
AWS Web Application Firewall (WAF) offers protection from common web exploits at which layer?
AWS Web Application Firewall（WAF）在哪一層提供針對常見 Web 攻擊的保護？

**[選項]**
- A. Layer 3／第 3 層
- B. Layer 4 and 7／第 4 層和第 7 層
- C. Layer 4／第 4 層
- D. Layer 7／第 7 層

**正確答案**
Layer 7／第 7 層

**為什麼正確**
**[OSI 模型與 AWS 安全]**
| OSI 層 | 名稱 | AWS 服務 |
| --- | --- | --- |
| 3 | 網路層 | AWS Shield |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Layer 3／第 3 層 | ❌ 錯誤 | Layer 3 是網路層，較接近 IP 層防護，不是 WAF 的 Web 應用層。 |
| Layer 4 and 7／第 4 層和第 7 層 | ❌ 錯誤 | WAF 重點是 Layer 7 HTTP/HTTPS Web 請求規則，不包含 Layer 4。 |
| Layer 4／第 4 層 | ❌ 錯誤 | Layer 4 是傳輸層，常見於 TCP/UDP 防護，不是 WAF 的主要層級。 |
| Layer 7／第 7 層 | ✅ 正確 | AWS WAF 在 Layer 7 應用層保護 Web 應用程式。 |

---

## 問題 56

**題目**
Which tool/service will help you access AWS services using programming language-specific APIs?
哪個工具/服務將幫助您使用程式語言特定的 API 存取 AWS 服務？

**[選項]**
- A. AWS Management Console／AWS 管理主控台
- B. AWS Command Line Interface (CLI)／AWS 命令列介面
- C. Integrated Development Environments (IDE)／整合開發環境
- D. AWS Software Developer Kit (SDK)／AWS 軟體開發套件

**正確答案**
AWS Software Developer Kit (SDK)／AWS 軟體開發套件

**為什麼正確**
**[AWS 存取方式比較]**
| 工具 | 方式 | 適用場景 |
| --- | --- | --- |
| **AWS SDK** | **語言特定 API** | **程式碼整合** |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Management Console／AWS 管理主控台 | ❌ 錯誤 | Management Console 是圖形化網頁介面，不是程式語言 API 工具。 |
| AWS Command Line Interface (CLI)／AWS 命令列介面 | ❌ 錯誤 | CLI 是命令列工具，不是語言特定 API 函式庫。 |
| Integrated Development Environments (IDE)／整合開發環境 | ❌ 錯誤 | IDE 是開發環境，本身不是 AWS 服務 API 函式庫。 |
| AWS Software Developer Kit (SDK)／AWS 軟體開發套件 | ✅ 正確 | AWS SDK 提供特定程式語言的 AWS API 函式庫。 |

---

## 問題 57

**題目**
Which of the following is a serverless AWS service?
以下哪個是無伺服器 AWS 服務？

**[選項]**
- A. Amazon Elastic Compute Cloud (Amazon EC2)（虛擬伺服器）
- B. AWS Elastic Beanstalk（應用部署平台）
- C. Amazon EMR（大數據處理）
- D. AWS Lambda（無伺服器函數）

**正確答案**
AWS Lambda（無伺服器函數）

**為什麼正確**
**[無伺服器服務]**
- ✅ AWS Lambda
- ✅ Amazon S3
- ✅ Amazon DynamoDB


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic Compute Cloud (Amazon EC2)（虛擬伺服器） | ❌ 錯誤 | EC2 是可管理的虛擬伺服器，屬於運算服務，不是受管儲存、資料庫或訊息服務。 |
| AWS Elastic Beanstalk（應用部署平台） | ❌ 錯誤 | Elastic Beanstalk 是應用部署平台，重點是代管部署流程，不是負載平衡或資料庫容錯設定本身。 |
| Amazon EMR（大數據處理） | ❌ 錯誤 | EMR 是大數據處理平台，不是一般無伺服器函數服務。 |
| AWS Lambda（無伺服器函數） | ✅ 正確 | AWS Lambda 是無伺服器函數運算服務。 |

---

## 問題 58

**題目**
Which of the following Amazon S3 storage classes takes the most time to retrieve data (also known as first byte latency)?
以下哪個 Amazon S3 儲存類別需要最長時間來取得資料（也稱為第一個位元組延遲）？

**[選項]**
- A. Amazon S3 Standard（標準儲存）
- B. Amazon S3 Glacier Flexible Retrieval（彈性取回封存）
- C. Amazon S3 Intelligent-Tiering（智慧分層）
- D. Amazon S3 Glacier Deep Archive（深度封存）

**正確答案**
Amazon S3 Glacier Deep Archive（深度封存）

**為什麼正確**
**[S3 儲存類別取回時間]**
| 儲存類別 | 取回時間 | 使用場景 |
| --- | --- | --- |
| S3 Standard | 毫秒 | 頻繁存取 |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3 Standard（標準儲存） | ❌ 錯誤 | S3 Standard 適合頻繁存取，成本高於低頻存取類別。 |
| Amazon S3 Glacier Flexible Retrieval（彈性取回封存） | ❌ 錯誤 | S3 Glacier 類儲存適合封存資料，取回速度不如需要快速存取的低頻資料類別。 |
| Amazon S3 Intelligent-Tiering（智慧分層） | ❌ 錯誤 | S3 Intelligent-Tiering 適合存取模式不固定的資料，會自動調整儲存層。 |
| Amazon S3 Glacier Deep Archive（深度封存） | ✅ 正確 | Amazon S3 是 AWS 物件儲存服務。 |

---

## 問題 59

**題目**
Which option is a common stakeholder role for the AWS Cloud Adoption Framework (AWS CAF) platform perspective? (Select two)
哪個選項是 AWS 雲端採用框架（AWS CAF）平台觀點的常見利害關係人角色？（選兩項）

**[選項]**
- A. Chief Information Officer (CIO)／首席資訊長
- B. Chief Data Officer (CDO)／首席資料長
- C. Chief Product Officer (CPO)／首席產品長
- D. Engineer／工程師
- E. Chief Technology Officer (CTO)／首席技術長

**正確答案**
Engineer／工程師；Chief Technology Officer (CTO)／首席技術長

**為什麼正確**
1. 工程師
2. 技術長
**[AWS CAF 各視角利害關係人]**
| 視角 | 主要利害關係人 |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Chief Information Officer (CIO)／首席資訊長 | ❌ 錯誤 | CIO 偏整體資訊策略與治理，不是本題平台觀點的指定角色。 |
| Chief Data Officer (CDO)／首席資料長 | ❌ 錯誤 | CDO 較偏資料治理與資料價值，不是平台觀點的主要角色。 |
| Chief Product Officer (CPO)／首席產品長 | ❌ 錯誤 | CPO 偏產品策略，不是平台觀點的常見核心角色。 |
| Engineer／工程師 | ✅ 正確 | 工程師。 |
| Chief Technology Officer (CTO)／首席技術長 | ✅ 正確 | 首席技術長。 |

---

## 問題 60

**題目**
The DevOps team at an e-commerce company is trying to debug performance issues for its serverless application built using a microservices architecture. Which AWS service would you recommend addressing this use-case?
一家電子商務公司的 DevOps 團隊正在嘗試偵錯使用微服務架構建立的無伺服器應用程式的效能問題。您會推薦哪個 AWS 服務？

**[選項]**
- A. Amazon Pinpoint（使用者互動訊息）
- B. AWS Trusted Advisor（最佳實務建議）
- C. AWS CloudFormation（基礎設施模板）
- D. AWS X-Ray（分散式追蹤）

**正確答案**
AWS X-Ray（分散式追蹤）

**為什麼正確**
**AWS X-Ray** 可分析和偵錯無伺服器及分散式應用程式，幫助您了解應用程式和底層服務的執行情況，識別和排除效能問題及錯誤的根本原因。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Pinpoint（使用者互動訊息） | ❌ 錯誤 | Pinpoint 用於使用者互動、行銷訊息與通知活動，不是微服務效能追蹤工具。 |
| AWS Trusted Advisor（最佳實務建議） | ❌ 錯誤 | Trusted Advisor 提供成本、安全、效能、容錯與服務限制建議，不會自動執行遷移或取代專家顧問。 |
| AWS CloudFormation（基礎設施模板） | ❌ 錯誤 | CloudFormation 用模板建立與管理 AWS 資源，不是除錯追蹤、帳單估算或資料庫容錯服務。 |
| AWS X-Ray（分散式追蹤） | ✅ 正確 | AWS X-Ray 可追蹤與除錯微服務或無伺服器應用程式的效能問題。 |

---

## 問題 61

**題目**
Which of the following AWS services support reservations to optimize costs? (Select three)
以下哪些 AWS 服務支援預留以優化成本？（選三項）

**[選項]**
- A. AWS Lambda（無伺服器函數）
- B. Amazon Simple Storage Service (Amazon S3)（物件儲存）
- C. Amazon DocumentDB（文件資料庫）
- D. Amazon Relational Database Service (Amazon RDS)（關聯式資料庫）
- E. Amazon Elastic Compute Cloud (Amazon EC2)（虛擬伺服器）
- F. Amazon DynamoDB（NoSQL 資料庫）

**正確答案**
Amazon Relational Database Service (Amazon RDS)（關聯式資料庫）；Amazon Elastic Compute Cloud (Amazon EC2)（虛擬伺服器）；Amazon DynamoDB（NoSQL 資料庫）

**為什麼正確**
1. Amazon EC2（預留執行個體）
2. Amazon DynamoDB（預留容量）
3. Amazon RDS（預留執行個體）
**[支援預留的服務]**


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Lambda（無伺服器函數） | ❌ 錯誤 | Lambda 是無伺服器函數運算服務，負責執行程式碼，不是訊息解耦服務本身。 |
| Amazon Simple Storage Service (Amazon S3)（物件儲存） | ❌ 錯誤 | S3 是物件儲存，適合物件、備份與靜態內容，不是可被多台 EC2 同時附加寫入的檔案系統。 |
| Amazon DocumentDB（文件資料庫） | ❌ 錯誤 | DocumentDB 是文件資料庫服務，但 CCP 題庫中的預留成本最佳化重點通常不是 DocumentDB。 |
| Amazon Relational Database Service (Amazon RDS)（關聯式資料庫） | ✅ 正確 | Amazon RDS 支援 Reserved Instance 以降低長期資料庫成本。 |
| Amazon Elastic Compute Cloud (Amazon EC2)（虛擬伺服器） | ✅ 正確 | Amazon EC2 支援 Reserved Instance 以降低長期運算成本。 |
| Amazon DynamoDB（NoSQL 資料庫） | ✅ 正確 | DynamoDB 可透過預留容量最佳化成本。 |

---

## 問題 62

**題目**
A data analytics company is running a proprietary batch analytics application on AWS and wants to use a storage service which would be accessed by hundreds of EC2 instances simultaneously to append data to existing files. Which AWS service would you suggest for this use-case?
一家資料分析公司在 AWS 上執行專有的批次分析應用程式，希望使用可被數百個 EC2 執行個體同時存取以將資料附加至現有檔案的儲存服務。您會建議哪個 AWS 服務？

**[選項]**
- A. Instance Store／執行個體存放區
- B. Amazon Simple Storage Service (Amazon S3)（物件儲存）
- C. Amazon Elastic Block Store (Amazon EBS)（區塊儲存）
- D. Amazon Elastic File System (Amazon EFS)（共享檔案系統）

**正確答案**
Amazon Elastic File System (Amazon EFS)（共享檔案系統）

**為什麼正確**
**[為什麼選 EFS]**
- ✅ 支援數千個 EC2 執行個體同時存取
- ✅ 提供文件系統介面（支援附加操作）
- ✅ 使用 NFS 協議


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Instance Store／執行個體存放區 | ❌ 錯誤 | Instance Store 是暫時性本機儲存，資料會隨執行個體停止或終止而遺失。 |
| Amazon Simple Storage Service (Amazon S3)（物件儲存） | ❌ 錯誤 | S3 是物件儲存，適合物件、備份與靜態內容，不是可被多台 EC2 同時附加寫入的檔案系統。 |
| Amazon Elastic Block Store (Amazon EBS)（區塊儲存） | ❌ 錯誤 | EBS 是 EC2 的區塊儲存，通常附加到單一 AZ 內的執行個體，不適合數百台 EC2 同時共享檔案。 |
| Amazon Elastic File System (Amazon EFS)（共享檔案系統） | ✅ 正確 | Amazon EFS 可被多台 EC2 同時掛載，適合共享檔案存取。 |

---

## 問題 63

**題目**
A company wants to improve the resiliency of its flagship application so it wants to move from its traditional database system to a managed AWS NoSQL database service to support active-active configuration in both the East and West US AWS regions. Which AWS database service is the right fit for this requirement?
一家公司希望提升其旗艦應用程式的韌性，計劃從傳統資料庫系統遷移至受管 AWS NoSQL 資料庫服務，以支援美國東部和西部 AWS 區域的主動-主動設定。哪個 AWS 資料庫服務最適合此需求？

**[選項]**
- A. Amazon Aurora with multi-master clusters／具有多主叢集的 Amazon Aurora
- B. Amazon DynamoDB with DynamoDB Accelerator／具有 DynamoDB Accelerator 的 Amazon DynamoDB
- C. Amazon Relational Database Service (Amazon RDS) for MYSQL（關聯式資料庫）
- D. Amazon DynamoDB with global tables／具有全球資料表的 Amazon DynamoDB

**正確答案**
Amazon DynamoDB with global tables／具有全球資料表的 Amazon DynamoDB

**為什麼正確**
**DynamoDB 全球表格**自動跨多個 AWS 區域複製資料，支援**主動-主動跨區域配置**，全球分散式應用程式可在選定區域中本地存取資料，達到個位數毫秒的讀寫效能。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Aurora with multi-master clusters／具有多主叢集的 Amazon Aurora | ❌ 錯誤 | Aurora 是關聯式資料庫，題目若要求受管 NoSQL 與跨區域 active-active，應看 DynamoDB global tables。 |
| Amazon DynamoDB with DynamoDB Accelerator／具有 DynamoDB Accelerator 的 Amazon DynamoDB | ❌ 錯誤 | DAX 是 DynamoDB 快取加速器，不是跨區域 active-active 複寫能力。 |
| Amazon Relational Database Service (Amazon RDS) for MYSQL（關聯式資料庫） | ❌ 錯誤 | RDS 是關聯式資料庫服務，不是 NoSQL active-active 的主要答案。 |
| Amazon DynamoDB with global tables／具有全球資料表的 Amazon DynamoDB | ✅ 正確 | DynamoDB global tables 支援跨區域 active-active 複寫，適合多區域 NoSQL 韌性需求。 |

---

## 問題 64

**題目**
A multi-national corporation wants to get expert professional advice on migrating to AWS and managing their applications on AWS Cloud. Which of the following entities would you recommend for this engagement?
一家跨國公司希望獲得關於遷移至 AWS 和在 AWS 雲端上管理其應用程式的專業建議。您會推薦以下哪個實體參與此項目？

**[選項]**
- A. AWS Trusted Advisor（最佳實務建議）
- B. Concierge Support Team／禮賓支援團隊
- C. APN Technology Partner／APN 技術合作夥伴
- D. APN Consulting Partner／APN 諮詢合作夥伴

**正確答案**
APN Consulting Partner／APN 諮詢合作夥伴

**為什麼正確**
**[APN 合作夥伴類型]**
| 類型 | 說明 |
| --- | --- |
| **APN Consulting Partners** | **專業服務公司，協助設計、建構、遷移和管理 AWS 工作負載** |


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Trusted Advisor（最佳實務建議） | ❌ 錯誤 | Trusted Advisor 提供成本、安全、效能、容錯與服務限制建議，不會自動執行遷移或取代專家顧問。 |
| Concierge Support Team／禮賓支援團隊 | ❌ 錯誤 | Concierge Support Team 主要協助 Enterprise Support 的帳務與帳戶問題，不是遷移顧問實作團隊。 |
| APN Technology Partner／APN 技術合作夥伴 | ❌ 錯誤 | APN 是合作夥伴網路；Technology Partner 偏軟體產品，Consulting Partner 才偏顧問與遷移服務。 |
| APN Consulting Partner／APN 諮詢合作夥伴 | ✅ 正確 | APN Consulting Partner 提供顧問、遷移與管理 AWS 工作負載的專業服務。 |

---

## 問題 65

**題目**
A company needs a storage solution for a project wherein the data is accessed less frequently but needs rapid access when required. Which S3 storage class is the MOST cost-effective for the given use-case?
一家公司需要一個儲存解決方案，其中資料存取頻率較低，但在需要時需要快速存取。哪個 S3 儲存類別對於給定的使用案例最具成本效益？

**[選項]**
- A. Amazon S3 Standard（標準儲存）
- B. Amazon S3 Intelligent-Tiering (S3 Intelligent-Tiering)（智慧分層）
- C. Amazon S3 Glacier (S3 Glacier)（封存儲存）
- D. Amazon S3 Standard-Infrequent Access (S3 Standard-IA)（低頻存取）

**正確答案**
Amazon S3 Standard-Infrequent Access (S3 Standard-IA)（低頻存取）

**為什麼正確**
**S3 Standard-IA** 適合存取頻率較低但需要快速存取的資料，提供高耐久性、高吞吐量和低延遲，每 GB 儲存費用低，但有每 GB 取回費用。非常適合長期儲存、備份和災難復原。


**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3 Standard（標準儲存） | ❌ 錯誤 | S3 Standard 適合頻繁存取，成本高於低頻存取類別。 |
| Amazon S3 Intelligent-Tiering (S3 Intelligent-Tiering)（智慧分層） | ❌ 錯誤 | S3 Intelligent-Tiering 適合存取模式不固定的資料，會自動調整儲存層。 |
| Amazon S3 Glacier (S3 Glacier)（封存儲存） | ❌ 錯誤 | S3 Glacier 類儲存適合封存資料，取回速度不如需要快速存取的低頻資料類別。 |
| Amazon S3 Standard-Infrequent Access (S3 Standard-IA)（低頻存取） | ✅ 正確 | Amazon S3 是 AWS 物件儲存服務。 |

---

