# AWS CCP 02 選項解析

來源：
- 題目與選項：[AWS_CCP_Practice_Test2.md](AWS_CCP_Practice_Test2.md)
- 原詳解：[AWS_CCP_02.md](AWS_CCP_02.md)

這份檔案針對每題列出中英對照題目與選項，並用中文說明正確答案與其他選項的差異。

---

## 問題 1

**題目**
Which AWS service can be used to store, manage, and deploy Docker container images?
哪個 AWS 服務可用於儲存、管理和部署 Docker 容器映像？

**[選項]**
- A. Amazon Elastic Container Service (Amazon ECS)／容器編排服務
- B. AWS Lambda／無伺服器函數
- C. Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器
- D. Amazon Elastic Container Registry (Amazon ECR)／容器映像倉庫

**正確答案**
Amazon Elastic Container Registry (Amazon ECR)／容器映像倉庫

**為什麼正確**
**Amazon ECR** 是全託管的容器映像登錄檔服務，用來儲存、管理、分享和部署 Docker 容器映像。題目關鍵字是「container images」，不是「執行容器」。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic Container Service (Amazon ECS)／容器編排服務 | ❌ 錯誤 | ECS 用來執行和管理容器，不是專門儲存容器映像的倉庫。 |
| AWS Lambda／無伺服器函數 | ❌ 錯誤 | Lambda 用來執行函數程式碼，不是容器映像倉庫。 |
| Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器 | ❌ 錯誤 | EC2 提供虛擬伺服器，需要自行管理容器或映像流程。 |
| Amazon Elastic Container Registry (Amazon ECR)／容器映像倉庫 | ✅ 正確 | ECR 是 AWS 的受管容器映像倉庫，可儲存、管理和部署 Docker 映像。 |

---

## 問題 2

**題目**
An e-commerce company wants to assess its applications deployed on Amazon EC2 instances for vulnerabilities and deviations from AWS best practices. Which AWS service can be used to facilitate this?
一家電子商務公司希望評估其在 Amazon EC2 執行個體上部署的應用程式是否存在漏洞，以及是否偏離 AWS 最佳實務。哪個 AWS 服務可以用於此任務？

**[選項]**
- A. AWS Secrets Manager／機密管理
- B. AWS CloudHSM／雲端硬體安全模組
- C. AWS Trusted Advisor／最佳實務建議
- D. Amazon Inspector／自動化弱點評估

**正確答案**
Amazon Inspector／自動化弱點評估

**為什麼正確**
**Amazon Inspector** 會自動評估 EC2 工作負載和應用程式的弱點、暴露風險，以及與安全最佳實務的偏差，並產生依嚴重程度排序的安全發現。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Secrets Manager／機密管理 | ❌ 錯誤 | Secrets Manager 用於儲存、輪換密碼和 API 金鑰，不做 EC2 弱點掃描。 |
| AWS CloudHSM／雲端硬體安全模組 | ❌ 錯誤 | CloudHSM 提供專屬硬體安全模組，用於合規加密，不是弱點評估工具。 |
| AWS Trusted Advisor／最佳實務建議 | ❌ 錯誤 | Trusted Advisor 提供帳戶層級最佳實務建議，但題目強調 EC2 應用程式弱點評估。 |
| Amazon Inspector／自動化弱點評估 | ✅ 正確 | Inspector 專門自動化評估 EC2 等工作負載的漏洞與安全發現。 |

---

## 問題 3

**題目**
A social media company wants to protect its web application from common web exploits such as SQL injection and cross-site scripting. Which of the following AWS services can be used to address this use-case?
一家社群媒體公司希望保護其 Web 應用程式免受 SQL 注入和跨站腳本等常見 Web 攻擊。以下哪個 AWS 服務可以用於此使用案例？

**[選項]**
- A. Amazon GuardDuty／威脅偵測
- B. Amazon Inspector／弱點評估
- C. AWS CloudWatch／監控服務
- D. AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆

**正確答案**
AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆

**為什麼正確**
**AWS WAF** 可建立 Web ACL 規則來允許、封鎖或監控 HTTP/HTTPS 請求，特別適合防護 SQL injection、XSS 等第 7 層常見 Web 攻擊。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon GuardDuty／威脅偵測 | ❌ 錯誤 | GuardDuty 偵測帳戶、網路與工作負載中的威脅活動，不是用來設定 Web 請求封鎖規則。 |
| Amazon Inspector／弱點評估 | ❌ 錯誤 | Inspector 評估漏洞，不能直接在 Web 流量入口封鎖 SQL injection 或 XSS。 |
| AWS CloudWatch／監控服務 | ❌ 錯誤 | CloudWatch 監控指標、日誌和警示，不是 Web 防火牆。 |
| AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆 | ✅ 正確 | WAF 可針對 SQL injection、XSS 等 Web 攻擊建立防護規則。 |

---

## 問題 4

**題目**
AWS Compute Optimizer delivers recommendations for which of the following AWS resources? (Select two)
AWS Compute Optimizer 為以下哪些 AWS 資源提供建議？（選兩項）

**[選項]**
- A. AWS Lambda functions, Amazon Simple Storage Service (Amazon S3)／Lambda 函數、S3
- B. Amazon EC2 instances, Amazon Elastic File System (Amazon EFS)／EC2 執行個體、EFS
- C. Amazon Elastic File System (Amazon EFS), AWS Lambda functions／EFS、Lambda 函數
- D. Amazon EC2 instances, Amazon EC2 Auto Scaling groups／EC2 執行個體、EC2 Auto Scaling 群組
- E. Amazon Elastic Block Store (Amazon EBS), AWS Lambda functions／EBS、Lambda 函數

**正確答案**
Amazon EC2 instances, Amazon EC2 Auto Scaling groups／EC2 執行個體、EC2 Auto Scaling 群組；Amazon Elastic Block Store (Amazon EBS), AWS Lambda functions／EBS、Lambda 函數

**為什麼正確**
**AWS Compute Optimizer** 會分析使用率指標，為 EC2 執行個體、EC2 Auto Scaling 群組、EBS 磁碟區和 Lambda 函數等資源提供 rightsizing 與效能建議。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Lambda functions, Amazon Simple Storage Service (Amazon S3)／Lambda 函數、S3 | ❌ 錯誤 | Lambda 支援，但 S3 不是 Compute Optimizer 的主要建議資源。 |
| Amazon EC2 instances, Amazon Elastic File System (Amazon EFS)／EC2 執行個體、EFS | ❌ 錯誤 | EC2 支援，但 EFS 不屬於此題考點中的支援資源。 |
| Amazon Elastic File System (Amazon EFS), AWS Lambda functions／EFS、Lambda 函數 | ❌ 錯誤 | Lambda 支援，但 EFS 不支援。 |
| Amazon EC2 instances, Amazon EC2 Auto Scaling groups／EC2 執行個體、EC2 Auto Scaling 群組 | ✅ 正確 | Compute Optimizer 可提供 EC2 與 Auto Scaling 群組建議。 |
| Amazon Elastic Block Store (Amazon EBS), AWS Lambda functions／EBS、Lambda 函數 | ✅ 正確 | Compute Optimizer 可提供 EBS 磁碟區與 Lambda 函數建議。 |

---

## 問題 5

**題目**
Which of the following AWS services are global in scope? (Select two)
以下哪些 AWS 服務的範圍是全球性的？（選兩項）

**[選項]**
- A. Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器
- B. Amazon Relational Database Service (Amazon RDS)／關聯式資料庫
- C. Amazon Simple Storage Service (Amazon S3)／物件儲存
- D. Amazon CloudFront／內容交付網路
- E. AWS Identity and Access Management (AWS IAM)／身分與存取管理

**正確答案**
Amazon CloudFront／內容交付網路；AWS Identity and Access Management (AWS IAM)／身分與存取管理

**為什麼正確**
**CloudFront** 是全球內容交付網路，使用邊緣節點服務全球使用者；**IAM** 是全球服務，身分和政策不綁定單一區域。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器 | ❌ 錯誤 | EC2 是區域型服務，執行個體部署在特定區域和 AZ。 |
| Amazon Relational Database Service (Amazon RDS)／關聯式資料庫 | ❌ 錯誤 | RDS 是區域型資料庫服務。 |
| Amazon Simple Storage Service (Amazon S3)／物件儲存 | ❌ 錯誤 | S3 名稱空間近似全球，但儲存貯體建立在特定區域。 |
| Amazon CloudFront／內容交付網路 | ✅ 正確 | CloudFront 是全球 CDN 服務。 |
| AWS Identity and Access Management (AWS IAM)／身分與存取管理 | ✅ 正確 | IAM 是全球服務，不需要選擇區域。 |

---

## 問題 6

**題目**
Which of the following AWS services are always free to use? (Select two)
以下哪些 AWS 服務永遠免費使用？（選兩項）

**[選項]**
- A. Amazon DynamoDB／NoSQL 資料庫
- B. Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器
- C. Amazon Simple Storage Service (Amazon S3)／物件儲存
- D. AWS Auto Scaling／自動擴展
- E. AWS Identity and Access Management (AWS IAM)／身分與存取管理

**正確答案**
AWS Auto Scaling／自動擴展；AWS Identity and Access Management (AWS IAM)／身分與存取管理

**為什麼正確**
**IAM** 本身不額外收費；**AWS Auto Scaling** 服務本身免費，但被擴展的底層資源（例如 EC2、CloudWatch 指標）仍會照常收費。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon DynamoDB／NoSQL 資料庫 | ❌ 錯誤 | DynamoDB 依讀寫、儲存和其他功能計費。 |
| Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器 | ❌ 錯誤 | EC2 依執行時間、儲存、資料傳輸等計費。 |
| Amazon Simple Storage Service (Amazon S3)／物件儲存 | ❌ 錯誤 | S3 依儲存量、請求和資料傳輸等計費。 |
| AWS Auto Scaling／自動擴展 | ✅ 正確 | Auto Scaling 服務本身免費，只支付其管理的資源費用。 |
| AWS Identity and Access Management (AWS IAM)／身分與存取管理 | ✅ 正確 | IAM 使用者、群組、角色和政策本身免費。 |

---

## 問題 7

**題目**
An IT company wants to run a log backup process every Monday at 2 AM. The usual runtime of the process is 5 minutes. Which AWS services would you recommend to build a serverless solution for this use-case? (Select two)
一家 IT 公司希望每週一凌晨 2 點執行一次日誌備份流程，通常執行時間為 5 分鐘。您會推薦哪些 AWS 服務來建立無伺服器解決方案？（選兩項）

**[選項]**
- A. Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器
- B. AWS Step Functions／工作流程編排
- C. AWS Systems Manager／系統管理
- D. AWS Lambda／無伺服器函數
- E. Amazon EventBridge／事件匯流排與排程

**正確答案**
AWS Lambda／無伺服器函數；Amazon EventBridge／事件匯流排與排程

**為什麼正確**
**EventBridge** 可用排程或 cron 規則在每週一凌晨 2 點觸發任務；**Lambda** 可執行 5 分鐘的備份邏輯，且不需要管理伺服器。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器 | ❌ 錯誤 | EC2 需要管理伺服器，不符合無伺服器要求。 |
| AWS Step Functions／工作流程編排 | ❌ 錯誤 | Step Functions 用於編排工作流程，不是此題的排程觸發服務本身。 |
| AWS Systems Manager／系統管理 | ❌ 錯誤 | Systems Manager 可管理執行命令與修補，但此題最直接的無伺服器排程組合是 EventBridge + Lambda。 |
| AWS Lambda／無伺服器函數 | ✅ 正確 | Lambda 可無伺服器執行短時間備份程式。 |
| Amazon EventBridge／事件匯流排與排程 | ✅ 正確 | EventBridge 可依排程觸發 Lambda。 |

---

## 問題 8

**題目**
Which AWS service helps with global application availability and performance using the AWS global network?
哪個 AWS 服務使用 AWS 全球網路幫助提升全球應用程式的可用性和效能？

**[選項]**
- A. Elastic Load Balancing (ELB)／負載平衡
- B. Amazon Route 53／DNS 服務
- C. Amazon CloudFront／內容交付網路
- D. AWS Global Accelerator／全球加速器

**正確答案**
AWS Global Accelerator／全球加速器

**為什麼正確**
**AWS Global Accelerator** 透過 AWS 全球網路和靜態 Anycast IP，將使用者流量導向最佳的區域端點，提升全球應用程式的可用性、效能和故障移轉速度。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Elastic Load Balancing (ELB)／負載平衡 | ❌ 錯誤 | ELB 主要在區域內分配流量，不是全球網路加速服務。 |
| Amazon Route 53／DNS 服務 | ❌ 錯誤 | Route 53 可做 DNS 路由，但題目強調使用 AWS 全球網路改善效能。 |
| Amazon CloudFront／內容交付網路 | ❌ 錯誤 | CloudFront 是 CDN，適合快取和加速 HTTP/HTTPS 內容，不是本題描述的全球網路入口服務。 |
| AWS Global Accelerator／全球加速器 | ✅ 正確 | Global Accelerator 使用 AWS 全球網路改善全球應用可用性與效能。 |

---

## 問題 9

**題目**
As per the AWS Shared Responsibility Model, which of the following is a responsibility of the customer from a security and compliance point of view?
根據 AWS 共同責任模型，以下哪項是客戶從安全和合規角度的責任？

**[選項]**
- A. Availability Zone (AZ) infrastructure management／可用區域基礎設施管理
- B. Configuration management for AWS global infrastructure／AWS 全球基礎設施設定管理
- C. Patching/fixing flaws within the AWS infrastructure／修補 AWS 基礎設施缺陷
- D. Managing patches of the guest operating system on Amazon EC2／管理 Amazon EC2 客體作業系統修補程式

**正確答案**
Managing patches of the guest operating system on Amazon EC2／管理 Amazon EC2 客體作業系統修補程式

**為什麼正確**
在共同責任模型中，AWS 負責「雲端本身的安全」，客戶負責「雲端中的安全」。對 EC2 這類 IaaS 服務，客戶需要管理客體作業系統、修補程式、應用程式和安全設定。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Availability Zone (AZ) infrastructure management／可用區域基礎設施管理 | ❌ 錯誤 | AZ 的實體與基礎設施由 AWS 管理。 |
| Configuration management for AWS global infrastructure／AWS 全球基礎設施設定管理 | ❌ 錯誤 | AWS 全球基礎設施的設定與維運屬於 AWS 責任。 |
| Patching/fixing flaws within the AWS infrastructure／修補 AWS 基礎設施缺陷 | ❌ 錯誤 | AWS 負責修補其底層基礎設施。 |
| Managing patches of the guest operating system on Amazon EC2／管理 Amazon EC2 客體作業系統修補程式 | ✅ 正確 | EC2 的 guest OS 修補是客戶責任。 |

---

## 問題 10

**題目**
Which AWS support plan provides access to a designated Technical Account Manager (TAM)?
哪個 AWS 支援方案提供對指定技術帳戶管理員（TAM）的存取？

**[選項]**
- A. AWS Developer Support／開發者支援
- B. AWS Business Support／商業支援
- C. AWS Enterprise On-Ramp Support／Enterprise On-Ramp 支援
- D. AWS Enterprise Support／企業支援

**正確答案**
AWS Enterprise Support／企業支援

**為什麼正確**
**AWS Enterprise Support** 提供指定的 Technical Account Manager (TAM)。Enterprise On-Ramp 提供的是 TAM 池或主動式指導，不是指定 TAM。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Developer Support／開發者支援 | ❌ 錯誤 | Developer Support 不提供 TAM。 |
| AWS Business Support／商業支援 | ❌ 錯誤 | Business Support 提供 24/7 技術支援，但不提供指定 TAM。 |
| AWS Enterprise On-Ramp Support／Enterprise On-Ramp 支援 | ❌ 錯誤 | Enterprise On-Ramp 提供共享 TAM 池，不是指定 TAM。 |
| AWS Enterprise Support／企業支援 | ✅ 正確 | Enterprise Support 提供指定 TAM。 |

---

## 問題 11

**題目**
Which AWS compute service provides the EASIEST way to access resizable compute capacity in the cloud with support for per-second billing and access to the underlying OS?
哪個 AWS 運算服務提供最簡單的方式存取雲端中可調整大小的運算容量，並支援按秒計費和存取底層作業系統？

**[選項]**
- A. Amazon Lightsail／簡化型 VPS
- B. Amazon Elastic Container Service (Amazon ECS)／容器編排服務
- C. AWS Lambda／無伺服器函數
- D. Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器

**正確答案**
Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器

**為什麼正確**
**Amazon EC2** 提供可調整大小的雲端運算容量，Linux 執行個體支援按秒計費，且客戶可存取並管理底層作業系統。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Lightsail／簡化型 VPS | ❌ 錯誤 | Lightsail 是簡化的 VPS 服務，通常採用套裝資源模式，不是本題強調的 EC2 可調整容量。 |
| Amazon Elastic Container Service (Amazon ECS)／容器編排服務 | ❌ 錯誤 | ECS 是容器編排服務，不是最直接取得 OS 存取權的通用運算服務。 |
| AWS Lambda／無伺服器函數 | ❌ 錯誤 | Lambda 無需管理伺服器，也無法存取底層 OS。 |
| Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器 | ✅ 正確 | EC2 提供可調整運算容量、按秒計費和 OS 存取。 |

---

## 問題 12

**題目**
Which service gives a personalized view of the status of the AWS services that are part of your Cloud architecture so that you can quickly assess the impact on your business when AWS service(s) are experiencing issues?
哪個服務提供您雲端架構中 AWS 服務狀態的個人化視圖，以便在 AWS 服務出現問題時快速評估對業務的影響？

**[選項]**
- A. Amazon CloudWatch／監控服務
- B. Amazon Inspector／弱點評估
- C. AWS Health - Service Health Dashboard／AWS Health 服務健康儀表板
- D. AWS Health - Your Account Health Dashboard／AWS Health 您的帳戶健康儀表板

**正確答案**
AWS Health - Your Account Health Dashboard／AWS Health 您的帳戶健康儀表板

**為什麼正確**
**Your Account Health Dashboard** 提供與您帳戶和資源相關的個人化 AWS Health 事件與影響資訊，可用來判斷服務事件是否影響自己的架構。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon CloudWatch／監控服務 | ❌ 錯誤 | CloudWatch 監控您配置的指標、日誌與警示，不提供 AWS 服務健康的個人化事件視圖。 |
| Amazon Inspector／弱點評估 | ❌ 錯誤 | Inspector 用於安全弱點評估，不是服務健康儀表板。 |
| AWS Health - Service Health Dashboard／AWS Health 服務健康儀表板 | ❌ 錯誤 | Service Health 顯示所有 AWS 服務的一般狀態，不是針對您的帳戶。 |
| AWS Health - Your Account Health Dashboard／AWS Health 您的帳戶健康儀表板 | ✅ 正確 | Account Health Dashboard 提供個人化帳戶事件與影響資訊。 |

---

## 問題 13

**題目**
A fleet of Amazon EC2 instances spread across different Availability Zones (AZ) needs to access, edit and share file-based data stored centrally on a system. Which AWS service would you recommend for this use-case?
分散在不同可用區域（AZ）的 Amazon EC2 執行個體群需要存取、編輯和共享集中儲存的檔案型資料。您會推薦哪個 AWS 服務？

**[選項]**
- A. EC2 Instance Store／EC2 執行個體存放區
- B. Amazon Simple Storage Service (Amazon S3)／物件儲存
- C. Amazon Elastic Block Store (Amazon EBS)／區塊儲存
- D. Amazon Elastic File System (Amazon EFS)／共享檔案系統

**正確答案**
Amazon Elastic File System (Amazon EFS)／共享檔案系統

**為什麼正確**
**Amazon EFS** 是全託管 NFS 檔案系統，可被多個 AZ 中的多台 EC2 同時掛載與共享，適合集中式檔案存取、編輯和共享。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| EC2 Instance Store／EC2 執行個體存放區 | ❌ 錯誤 | Instance Store 是執行個體本機暫存儲存，不能跨多台 EC2 集中共享。 |
| Amazon Simple Storage Service (Amazon S3)／物件儲存 | ❌ 錯誤 | S3 是物件儲存，不是可由多台 EC2 同時掛載編輯的檔案系統。 |
| Amazon Elastic Block Store (Amazon EBS)／區塊儲存 | ❌ 錯誤 | EBS 主要附加到單一 EC2 或有限多附加場景，不適合跨 AZ 檔案共享。 |
| Amazon Elastic File System (Amazon EFS)／共享檔案系統 | ✅ 正確 | EFS 提供跨多 AZ 的共享檔案系統，支援多台 EC2 同時存取。 |

---

## 問題 14

**題目**
Which of the following AWS services comes under the Software as a Service (SaaS) Cloud Computing Type?
以下哪個 AWS 服務屬於軟體即服務（SaaS）雲端運算類型？

**[選項]**
- A. Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器
- B. Elastic Load Balancing (ELB)／負載平衡
- C. AWS Elastic Beanstalk／應用部署平台
- D. Amazon Rekognition／影像與影片分析服務

**正確答案**
Amazon Rekognition／影像與影片分析服務

**為什麼正確**
**Amazon Rekognition** 是可直接透過 API 使用的完整影像和影片分析服務，客戶不需要管理底層平台或基礎設施，因此屬於 SaaS 類型的服務。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器 | ❌ 錯誤 | EC2 提供虛擬伺服器，屬於 IaaS。 |
| Elastic Load Balancing (ELB)／負載平衡 | ❌ 錯誤 | ELB 是基礎設施層的網路流量分配服務。 |
| AWS Elastic Beanstalk／應用部署平台 | ❌ 錯誤 | Elastic Beanstalk 偏 PaaS，協助部署和管理應用平台。 |
| Amazon Rekognition／影像與影片分析服務 | ✅ 正確 | Rekognition 是完整受管的應用能力服務，可視為 SaaS。 |

---

## 問題 15

**題目**
As per the AWS Shared Responsibility Model, which of the following is a responsibility of AWS from a security and compliance point of view?
根據 AWS 共同責任模型，以下哪項是 AWS 從安全和合規角度的責任？

**[選項]**
- A. Customer Data／客戶資料
- B. Server-side Encryption (SSE)／伺服器端加密
- C. Identity and Access Management／身分和存取管理
- D. Edge Location Management／邊緣位置管理

**正確答案**
Edge Location Management／邊緣位置管理

**為什麼正確**
AWS 負責雲端底層基礎設施的安全與管理，包括區域、可用區域、邊緣節點和實體設施。**Edge Location Management** 屬於 AWS 的責任。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Customer Data／客戶資料 | ❌ 錯誤 | 客戶資料的分類、保護與管理屬於客戶責任。 |
| Server-side Encryption (SSE)／伺服器端加密 | ❌ 錯誤 | 是否啟用與如何設定資料加密通常由客戶決定。 |
| Identity and Access Management／身分和存取管理 | ❌ 錯誤 | 身分、權限與政策配置屬於客戶責任。 |
| Edge Location Management／邊緣位置管理 | ✅ 正確 | 邊緣節點作為 AWS 全球基礎設施的一部分，由 AWS 管理。 |

---

## 問題 16

**題目**
Due to regulatory and compliance reasons, an organization is supposed to use a hardware device for any data encryption operations in the cloud. Which AWS service can be used to meet this compliance requirement?
由於法規和合規原因，一個組織應使用硬體裝置進行雲端中的任何資料加密操作。哪個 AWS 服務可以用於滿足此合規要求？

**[選項]**
- A. AWS Secrets Manager／機密管理
- B. AWS Trusted Advisor／最佳實務建議
- C. AWS Key Management Service (AWS KMS)／金鑰管理服務
- D. AWS CloudHSM／雲端硬體安全模組

**正確答案**
AWS CloudHSM／雲端硬體安全模組

**為什麼正確**
**AWS CloudHSM** 提供雲端中的專屬硬體安全模組 (HSM)，可讓客戶在硬體裝置中產生、儲存和使用加密金鑰，適合法規要求使用硬體加密設備的場景。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Secrets Manager／機密管理 | ❌ 錯誤 | Secrets Manager 管理密碼和機密，不提供專屬硬體 HSM。 |
| AWS Trusted Advisor／最佳實務建議 | ❌ 錯誤 | Trusted Advisor 提供建議，不執行硬體加密。 |
| AWS Key Management Service (AWS KMS)／金鑰管理服務 | ❌ 錯誤 | KMS 是受管金鑰服務，底層由 AWS 管理，不等同於客戶專屬硬體裝置。 |
| AWS CloudHSM／雲端硬體安全模組 | ✅ 正確 | CloudHSM 提供專屬 HSM，可滿足硬體加密設備要求。 |

---

## 問題 17

**題目**
Which of the following solutions can you use to connect your on-premises network with AWS Cloud? (Select two)
以下哪些解決方案可用於將您的本地網路連接至 AWS 雲端？（選兩項）

**[選項]**
- A. Internet Gateway／網際網路閘道
- B. Amazon Route 53／DNS 服務
- C. Amazon Virtual Private Cloud (Amazon VPC)／虛擬私有雲
- D. AWS Direct Connect／專用網路連線
- E. AWS Virtual Private Network (VPN)／虛擬私有網路

**正確答案**
AWS Direct Connect／專用網路連線；AWS Virtual Private Network (VPN)／虛擬私有網路

**為什麼正確**
**AWS Direct Connect** 提供本地資料中心到 AWS 的專用實體網路連線；**AWS VPN** 可透過加密隧道將本地網路連到 AWS VPC。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Internet Gateway／網際網路閘道 | ❌ 錯誤 | Internet Gateway 讓 VPC 內資源連接網際網路，不是本地網路到 AWS 的完整連線方案。 |
| Amazon Route 53／DNS 服務 | ❌ 錯誤 | Route 53 提供 DNS 與路由策略，不建立網路隧道或專線。 |
| Amazon Virtual Private Cloud (Amazon VPC)／虛擬私有雲 | ❌ 錯誤 | VPC 是 AWS 中的隔離網路環境，本身不是本地連線方案。 |
| AWS Direct Connect／專用網路連線 | ✅ 正確 | Direct Connect 可建立本地到 AWS 的專用連線。 |
| AWS Virtual Private Network (VPN)／虛擬私有網路 | ✅ 正確 | VPN 可透過加密通道連接本地網路與 AWS。 |

---

## 問題 18

**題目**
Access Key ID and Secret Access Key are tied to which of the following AWS IAM entities?
存取金鑰 ID 和私密存取金鑰與以下哪個 AWS IAM 實體相關聯？

**[選項]**
- A. IAM Role／IAM 角色
- B. IAM Policy／IAM 政策
- C. IAM User Group／IAM 使用者群組
- D. IAM User／IAM 使用者

**正確答案**
IAM User／IAM 使用者

**為什麼正確**
Access Key ID 和 Secret Access Key 是長期憑證，通常與 **IAM User** 關聯，供程式化方式存取 AWS API。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| IAM Role／IAM 角色 | ❌ 錯誤 | IAM Role 通常由服務或使用者擔任，取得臨時安全憑證。 |
| IAM Policy／IAM 政策 | ❌ 錯誤 | Policy 定義權限，不持有存取金鑰。 |
| IAM User Group／IAM 使用者群組 | ❌ 錯誤 | 群組用於集合管理使用者權限，不持有金鑰。 |
| IAM User／IAM 使用者 | ✅ 正確 | IAM User 可建立 Access Key ID 和 Secret Access Key。 |

---

## 問題 19

**題目**
Which of the following are examples of Horizontal Scalability (aka Elasticity)? (Select two)
以下哪些是水平擴展（即彈性）的範例？（選兩項）

**[選項]**
- A. Modify a Database instance to higher CPU and RAM／將資料庫執行個體修改為更高 CPU 和 RAM
- B. Modify an EC2 instance type from t2.nano to u-12tb1.metal／將 EC2 執行個體類型調整為更大型號
- C. Add a bigger CPU to a computer／為電腦新增更大的 CPU
- D. Elastic Load Balancing (ELB)／負載平衡
- E. Read Replicas in Amazon Relational Database Service (Amazon RDS)／Amazon RDS 讀取副本

**正確答案**
Elastic Load Balancing (ELB)／負載平衡；Read Replicas in Amazon RDS／Amazon RDS 讀取副本

**為什麼正確**
水平擴展是「增加更多節點」來分散負載。**ELB** 將流量分散到多個目標；**RDS Read Replicas** 透過增加讀取副本分散讀取流量。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Modify a Database instance to higher CPU and RAM／將資料庫執行個體修改為更高 CPU 和 RAM | ❌ 錯誤 | 增加單一節點資源是垂直擴展。 |
| Modify an EC2 instance type from t2.nano to u-12tb1.metal／將 EC2 執行個體類型調整為更大型號 | ❌ 錯誤 | 換更大的執行個體類型是垂直擴展。 |
| Add a bigger CPU to a computer／為電腦新增更大的 CPU | ❌ 錯誤 | 這是增加單一主機能力，屬於垂直擴展。 |
| Elastic Load Balancing (ELB)／負載平衡 | ✅ 正確 | ELB 支援將請求分散到多個執行個體，是水平擴展常見組件。 |
| Read Replicas in Amazon RDS／Amazon RDS 讀取副本 | ✅ 正確 | 讀取副本增加更多資料庫節點來分散讀取流量。 |

---

## 問題 20

**題目**
Which of the following statements is INCORRECT about AWS Auto Scaling?
以下哪項關於 AWS Auto Scaling 的陳述是不正確的？

**[選項]**
- A. You can scale out and add more EC2 instances to match an increase in demand as well as scale in and remove EC2 instances to match a reduced demand／可以依需求增加或移除 EC2 執行個體
- B. You can automatically remove unhealthy instances／可以自動移除不健康的執行個體
- C. You can automatically register new instances to a load balancer／可以自動將新執行個體註冊到負載平衡器
- D. You can automatically deploy AWS Shield when a DDoS attack is detected／偵測到 DDoS 攻擊時可以自動部署 AWS Shield

**正確答案**
You can automatically deploy AWS Shield when a DDoS attack is detected／偵測到 DDoS 攻擊時可以自動部署 AWS Shield

**為什麼正確**
本題要選「不正確」敘述。Auto Scaling 可依需求擴縮與替換不健康執行個體，但**不會在偵測 DDoS 時自動部署 AWS Shield**。DDoS 防護應使用 AWS Shield、AWS WAF、CloudFront 等服務。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| You can scale out and add more EC2 instances to match an increase in demand as well as scale in and remove EC2 instances to match a reduced demand／可以依需求增加或移除 EC2 執行個體 | ❌ 非答案 | 這是 Auto Scaling 的正確能力。 |
| You can automatically remove unhealthy instances／可以自動移除不健康的執行個體 | ❌ 非答案 | Auto Scaling 可替換或移除不健康執行個體。 |
| You can automatically register new instances to a load balancer／可以自動將新執行個體註冊到負載平衡器 | ❌ 非答案 | Auto Scaling 群組可與負載平衡器整合。 |
| You can automatically deploy AWS Shield when a DDoS attack is detected／偵測到 DDoS 攻擊時可以自動部署 AWS Shield | ✅ 正確答案（錯誤敘述） | Auto Scaling 不會自動部署 Shield；Shield 是獨立的 DDoS 防護服務。 |

---

## 問題 21

**題目**
Multi-AZ deployment is an example of which of the following?
多 AZ 部署是以下哪項的範例？

**[選項]**
- A. Scale out／向外擴展
- B. Performance Efficiency／效能效率
- C. Scale up／向上擴展
- D. High Availability／高可用性

**正確答案**
High Availability／高可用性

**為什麼正確**
**Multi-AZ** 透過跨可用區域部署來降低單一 AZ 故障造成的影響，讓服務在部分故障時仍可用，因此是高可用性的範例。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Scale out／向外擴展 | ❌ 錯誤 | Scale out 是增加更多節點，重點在容量擴展。 |
| Performance Efficiency／效能效率 | ❌ 錯誤 | 效能效率關注資源選型與高效使用，不是 Multi-AZ 的主要目的。 |
| Scale up／向上擴展 | ❌ 錯誤 | Scale up 是提升單一節點資源。 |
| High Availability／高可用性 | ✅ 正確 | Multi-AZ 的核心目的就是提升可用性。 |

---

## 問題 22

**題目**
Which of the following use-cases is NOT supported by Amazon Rekognition?
以下哪個使用案例不受 Amazon Rekognition 支援？

**[選項]**
- A. Detect text in a photo／偵測照片中的文字
- B. Identify person in a photo／識別照片中的人物
- C. Label objects in a photo／為照片中的物件加上標籤
- D. Quickly resize photos to create thumbnails／快速調整照片大小以建立縮圖

**正確答案**
Quickly resize photos to create thumbnails／快速調整照片大小以建立縮圖

**為什麼正確**
Amazon Rekognition 支援影像與影片分析，例如物件標籤、文字偵測、臉部分析與人物識別。**調整圖片尺寸和建立縮圖**是影像處理任務，通常可用 S3 + Lambda 或影像處理工具完成。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Detect text in a photo／偵測照片中的文字 | ❌ 非答案 | Rekognition 支援圖片文字偵測。 |
| Identify person in a photo／識別照片中的人物 | ❌ 非答案 | Rekognition 支援臉部分析與人物相關偵測能力。 |
| Label objects in a photo／為照片中的物件加上標籤 | ❌ 非答案 | Rekognition 可偵測並標記圖片中的物件與場景。 |
| Quickly resize photos to create thumbnails／快速調整照片大小以建立縮圖 | ✅ 正確答案（不支援） | Rekognition 不負責圖片縮放或產生縮圖。 |

---

## 問題 23

**題目**
An organization is planning to move its infrastructure from the on-premises datacenter to AWS Cloud. Which options would you recommend so that the organization can identify the right AWS services to build solutions on AWS Cloud? (Select two)
一個組織計劃將基礎設施從本地資料中心遷移至 AWS 雲端。您會推薦哪些選項，以幫助組織識別在 AWS 雲端上建立解決方案的正確 AWS 服務？（選兩項）

**[選項]**
- A. Amazon CloudWatch／監控服務
- B. AWS Organizations／多帳戶管理
- C. AWS CloudTrail／活動稽核
- D. AWS Service Catalog／服務目錄
- E. AWS Partner Network (APN)／AWS 合作夥伴網路

**正確答案**
AWS Service Catalog／服務目錄；AWS Partner Network (APN)／AWS 合作夥伴網路

**為什麼正確**
**AWS Service Catalog** 可讓組織建立和管理已核准的 AWS 服務與 IT 服務清單；**APN** 可透過合作夥伴協助識別合適服務並建構解決方案。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon CloudWatch／監控服務 | ❌ 錯誤 | CloudWatch 用於監控資源與應用，不是服務選型目錄或合作夥伴資源。 |
| AWS Organizations／多帳戶管理 | ❌ 錯誤 | Organizations 管理多帳戶、SCP 和整合帳單，不協助識別解決方案服務。 |
| AWS CloudTrail／活動稽核 | ❌ 錯誤 | CloudTrail 記錄帳戶 API 活動，不做服務選型。 |
| AWS Service Catalog／服務目錄 | ✅ 正確 | Service Catalog 可提供組織批准的服務與方案目錄。 |
| AWS Partner Network (APN)／AWS 合作夥伴網路 | ✅ 正確 | APN 合作夥伴可協助設計、選型與建置 AWS 解決方案。 |

---

## 問題 24

**題目**
Which of the following statements are true about AWS Lambda? (Select two)
以下哪些陳述關於 AWS Lambda 是正確的？（選兩項）

**[選項]**
- A. AWS Lambda provides access to the underlying operating system to control its behavior through code／Lambda 提供底層作業系統存取
- B. AWS Lambda allows you to install databases on the underlying serverless Operating System／Lambda 允許在底層無伺服器 OS 安裝資料庫
- C. AWS Lambda allows you to orchestrate and manage Docker containers to facilitate complex containerized applications on AWS／Lambda 可編排和管理 Docker 容器
- D. AWS Lambda lets you run code without provisioning or managing servers／Lambda 讓您無需佈建或管理伺服器即可執行程式碼
- E. You pay for the compute time you consume for AWS Lambda／您為 Lambda 消耗的運算時間付費

**正確答案**
AWS Lambda lets you run code without provisioning or managing servers／無需佈建或管理伺服器即可執行程式碼；You pay for the compute time you consume for AWS Lambda／為消耗的運算時間付費

**為什麼正確**
**AWS Lambda** 是無伺服器運算服務，客戶只上傳程式碼並配置觸發器，不需要管理伺服器；計費依請求數量和實際執行時間計算。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Lambda provides access to the underlying operating system to control its behavior through code／Lambda 提供底層作業系統存取 | ❌ 錯誤 | Lambda 不提供底層 OS 存取權。 |
| AWS Lambda allows you to install databases on the underlying serverless Operating System／Lambda 允許在底層無伺服器 OS 安裝資料庫 | ❌ 錯誤 | Lambda 無法讓您安裝和管理底層 OS 上的資料庫。 |
| AWS Lambda allows you to orchestrate and manage Docker containers to facilitate complex containerized applications on AWS／Lambda 可編排和管理 Docker 容器 | ❌ 錯誤 | 容器編排應使用 ECS、EKS 或 Fargate。 |
| AWS Lambda lets you run code without provisioning or managing servers／Lambda 讓您無需佈建或管理伺服器即可執行程式碼 | ✅ 正確 | 這是 Lambda 的核心無伺服器特性。 |
| You pay for the compute time you consume for AWS Lambda／您為 Lambda 消耗的運算時間付費 | ✅ 正確 | Lambda 依請求與運算時間計費。 |

---

## 問題 25

**題目**
Which AWS service can be used to provision resources to run big data workloads on Hadoop clusters?
哪個 AWS 服務可用於佈建資源以在 Hadoop 叢集上執行大數據工作負載？

**[選項]**
- A. Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器
- B. AWS Batch／批次運算
- C. AWS Step Functions／工作流程編排
- D. Amazon EMR／大數據處理平台

**正確答案**
Amazon EMR／大數據處理平台

**為什麼正確**
**Amazon EMR** 是 AWS 的受管大數據平台，可快速佈建 Hadoop、Spark、Hive、Presto 等叢集，用於執行大數據工作負載。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器 | ❌ 錯誤 | 可以自行在 EC2 上安裝 Hadoop，但不是最適合的受管大數據服務。 |
| AWS Batch／批次運算 | ❌ 錯誤 | Batch 用於排程和執行批次工作，不是 Hadoop 叢集服務。 |
| AWS Step Functions／工作流程編排 | ❌ 錯誤 | Step Functions 負責編排流程，不佈建 Hadoop 叢集。 |
| Amazon EMR／大數據處理平台 | ✅ 正確 | EMR 專門用於受管 Hadoop/Spark 等大數據工作負載。 |

---

## 問題 26

**題目**
Which AWS service enables users to find, buy, and immediately start using software solutions in their AWS environment?
哪個 AWS 服務使使用者能夠在其 AWS 環境中尋找、購買並立即開始使用軟體解決方案？

**[選項]**
- A. AWS CloudFormation／基礎設施即程式碼
- B. AWS Systems Manager／系統管理
- C. AWS Config／資源組態追蹤
- D. AWS Marketplace／軟體市集

**正確答案**
AWS Marketplace／軟體市集

**為什麼正確**
**AWS Marketplace** 是 AWS 的數位軟體目錄，使用者可尋找、試用、購買、部署並立即使用第三方或 AWS 相關軟體解決方案。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS CloudFormation／基礎設施即程式碼 | ❌ 錯誤 | CloudFormation 用範本佈建 AWS 資源，不是購買軟體的市集。 |
| AWS Systems Manager／系統管理 | ❌ 錯誤 | Systems Manager 用於管理和自動化資源操作。 |
| AWS Config／資源組態追蹤 | ❌ 錯誤 | Config 用於追蹤資源組態與合規狀態。 |
| AWS Marketplace／軟體市集 | ✅ 正確 | Marketplace 可搜尋、購買並部署軟體解決方案。 |

---

## 問題 27

**題目**
Which AWS technology/service helps you to scale your resources to match supply with demand while still keeping your cloud solution cost-effective?
哪個 AWS 技術/服務幫助您擴展資源以使供給與需求相匹配，同時保持雲端解決方案的成本效益？

**[選項]**
- A. AWS Systems Manager／系統管理
- B. AWS CloudFormation／基礎設施即程式碼
- C. AWS Cost Explorer／成本分析
- D. AWS Auto Scaling／自動擴展

**正確答案**
AWS Auto Scaling／自動擴展

**為什麼正確**
**AWS Auto Scaling** 可監控應用程式並自動調整容量，在需求增加時擴展、需求降低時縮減，協助維持效能並降低成本浪費。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Systems Manager／系統管理 | ❌ 錯誤 | Systems Manager 用於管理執行個體、修補和自動化操作，不是自動容量擴縮核心服務。 |
| AWS CloudFormation／基礎設施即程式碼 | ❌ 錯誤 | CloudFormation 用來定義和佈建資源，不會根據需求自動擴縮。 |
| AWS Cost Explorer／成本分析 | ❌ 錯誤 | Cost Explorer 用於分析成本，不會調整資源容量。 |
| AWS Auto Scaling／自動擴展 | ✅ 正確 | Auto Scaling 根據需求調整資源供給，兼顧效能與成本。 |

---

## 問題 28

**題目**
Which tool will help you review your workloads against current AWS best practices for cost optimization, security, and performance improvement and then obtain advice to architect them better?
哪個工具可以幫助您根據目前 AWS 最佳實務審查工作負載，包括成本優化、安全性和效能改善，並獲得更好的架構建議？

**[選項]**
- A. Amazon Inspector／弱點評估
- B. AWS Cost Explorer／成本分析
- C. Amazon CloudWatch／監控服務
- D. AWS Trusted Advisor／最佳實務建議

**正確答案**
AWS Trusted Advisor／最佳實務建議

**為什麼正確**
**AWS Trusted Advisor** 會依成本最佳化、安全、效能、容錯和服務限制等類別檢查 AWS 環境，並提供最佳實務建議。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Inspector／弱點評估 | ❌ 錯誤 | Inspector 偏安全弱點評估，不涵蓋成本、效能、容錯等完整最佳實務建議。 |
| AWS Cost Explorer／成本分析 | ❌ 錯誤 | Cost Explorer 用於分析成本趨勢，不是全面架構建議工具。 |
| Amazon CloudWatch／監控服務 | ❌ 錯誤 | CloudWatch 監控指標和日誌，不提供最佳實務審查。 |
| AWS Trusted Advisor／最佳實務建議 | ✅ 正確 | Trusted Advisor 會依多個最佳實務類別提供建議。 |

---

## 問題 29

**題目**
What is the primary benefit of deploying an Amazon RDS Multi-AZ database with one standby?
部署具有一個待機的 Amazon RDS Multi-AZ 資料庫的主要優點是什麼？

**[選項]**
- A. Amazon RDS Multi-AZ reduces database usage costs／降低資料庫使用成本
- B. Amazon RDS Multi-AZ improves database performance for read-heavy workloads／改善讀取密集型工作負載效能
- C. Amazon RDS Multi-AZ protects the database from a regional failure／保護資料庫免受區域故障影響
- D. Amazon RDS Multi-AZ enhances database availability／提升資料庫可用性

**正確答案**
Amazon RDS Multi-AZ enhances database availability／提升資料庫可用性

**為什麼正確**
**RDS Multi-AZ** 會在另一個 AZ 建立同步待機副本，主要用途是提高可用性和自動容錯移轉，而不是降低成本或提升讀取效能。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon RDS Multi-AZ reduces database usage costs／降低資料庫使用成本 | ❌ 錯誤 | Multi-AZ 會增加待機資源，通常不是降成本方案。 |
| Amazon RDS Multi-AZ improves database performance for read-heavy workloads／改善讀取密集型工作負載效能 | ❌ 錯誤 | Multi-AZ 待機副本通常不處理讀取；讀取效能應用 Read Replica。 |
| Amazon RDS Multi-AZ protects the database from a regional failure／保護資料庫免受區域故障影響 | ❌ 錯誤 | Multi-AZ 是同一區域內跨 AZ，不是跨區域災難復原。 |
| Amazon RDS Multi-AZ enhances database availability／提升資料庫可用性 | ✅ 正確 | Multi-AZ 主要提供高可用性和自動容錯移轉。 |

---

## 問題 30

**題目**
The engineering team at an IT company wants to monitor the CPU utilization for its fleet of Amazon EC2 instances and send an email to the administrator if the utilization exceeds 80%. Which AWS services would you recommend to build this solution? (Select two)
一家 IT 公司的工程團隊希望監控其 Amazon EC2 執行個體群的 CPU 使用率，並在使用率超過 80% 時向管理員發送電子郵件。您會推薦哪些 AWS 服務來建立此解決方案？（選兩項）

**[選項]**
- A. Amazon Simple Queue Service (SQS)／訊息佇列
- B. AWS Lambda／無伺服器函數
- C. AWS CloudTrail／活動稽核
- D. Amazon CloudWatch／監控服務
- E. Amazon Simple Notification Service (SNS)／通知服務

**正確答案**
Amazon CloudWatch／監控服務；Amazon Simple Notification Service (SNS)／通知服務

**為什麼正確**
**CloudWatch** 可監控 EC2 CPUUtilization 並設定超過 80% 的警示；**SNS** 可作為警示動作發送電子郵件通知。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Simple Queue Service (SQS)／訊息佇列 | ❌ 錯誤 | SQS 用於訊息排隊，不發送電子郵件通知。 |
| AWS Lambda／無伺服器函數 | ❌ 錯誤 | Lambda 可執行程式碼，但此題不需要自訂運算邏輯。 |
| AWS CloudTrail／活動稽核 | ❌ 錯誤 | CloudTrail 記錄 API 活動，不監控 CPU 指標。 |
| Amazon CloudWatch／監控服務 | ✅ 正確 | CloudWatch 可監控 EC2 CPU 並觸發告警。 |
| Amazon Simple Notification Service (SNS)／通知服務 | ✅ 正確 | SNS 可將 CloudWatch 告警通知寄送到電子郵件訂閱者。 |

---

## 問題 31

**題目**
A gaming company is looking at a technology/service that can deliver a consistent low-latency gameplay to ensure a great user experience for end-users in various locations. Which AWS technology/service will provide the necessary low-latency access to the end-users?
一家遊戲公司正在尋找可提供一致低延遲遊戲體驗的技術/服務，以確保各地終端使用者獲得良好體驗。哪個 AWS 技術/服務將提供必要的低延遲存取？

**[選項]**
- A. AWS Wavelength／5G 邊緣運算
- B. AWS Edge Locations／AWS 邊緣位置
- C. AWS Direct Connect／專用網路連線
- D. AWS Local Zones／本地區域

**正確答案**
AWS Local Zones／本地區域

**為什麼正確**
**AWS Local Zones** 將運算、儲存、資料庫等 AWS 服務放在更靠近大型人口、產業或 IT 中心的位置，適合需要極低延遲的遊戲、媒體和即時互動應用。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Wavelength／5G 邊緣運算 | ❌ 錯誤 | Wavelength 適合電信商 5G 邊緣應用，本題一般低延遲遊戲體驗更符合 Local Zones。 |
| AWS Edge Locations／AWS 邊緣位置 | ❌ 錯誤 | Edge Locations 主要支援 CloudFront CDN 和邊緣服務，不是完整運算部署區域。 |
| AWS Direct Connect／專用網路連線 | ❌ 錯誤 | Direct Connect 連接本地環境與 AWS，不是把運算部署到終端用戶附近。 |
| AWS Local Zones／本地區域 | ✅ 正確 | Local Zones 可在靠近終端用戶的位置部署 AWS 運算與儲存，降低延遲。 |

---

## 問題 32

**題目**
Which of the following options are the pillars mentioned in the AWS Well-Architected Framework? (Select two)
以下哪些選項是 AWS Well-Architected Framework 中提到的支柱？（選兩項）

**[選項]**
- A. Scalability／可擴展性
- B. Elasticity／彈性
- C. Availability／可用性
- D. Reliability／可靠性
- E. Cost Optimization／成本優化

**正確答案**
Reliability／可靠性；Cost Optimization／成本優化

**為什麼正確**
AWS Well-Architected Framework 六大支柱包括卓越營運、安全性、**可靠性**、效能效率、**成本優化**和永續性。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Scalability／可擴展性 | ❌ 錯誤 | 可擴展性是重要設計概念，但不是六大支柱名稱。 |
| Elasticity／彈性 | ❌ 錯誤 | 彈性是雲端特性，不是 Well-Architected 支柱名稱。 |
| Availability／可用性 | ❌ 錯誤 | 可用性與可靠性相關，但支柱名稱是 Reliability。 |
| Reliability／可靠性 | ✅ 正確 | Reliability 是 Well-Architected 六大支柱之一。 |
| Cost Optimization／成本優化 | ✅ 正確 | Cost Optimization 是 Well-Architected 六大支柱之一。 |

---

## 問題 33

**題目**
Which of the following AWS services is essential for implementing security of resources in AWS Cloud?
以下哪個 AWS 服務對於實施 AWS 雲端中資源的安全性至關重要？

**[選項]**
- A. Amazon CloudWatch／監控服務
- B. AWS Shield／DDoS 防護
- C. AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆
- D. AWS Identity and Access Management (IAM)／身分與存取管理

**正確答案**
AWS Identity and Access Management (IAM)／身分與存取管理

**為什麼正確**
**IAM** 是 AWS 安全的核心，用來管理誰可以登入、誰可以呼叫 API、以及哪些身分可存取哪些 AWS 資源。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon CloudWatch／監控服務 | ❌ 錯誤 | CloudWatch 用於監控與告警，不是身分和權限控制核心。 |
| AWS Shield／DDoS 防護 | ❌ 錯誤 | Shield 專注 DDoS 防護，範圍較窄。 |
| AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆 | ❌ 錯誤 | WAF 防護 Web 請求，不管理 AWS 資源存取權。 |
| AWS Identity and Access Management (IAM)／身分與存取管理 | ✅ 正確 | IAM 是實作 AWS 資源安全存取控制的基礎服務。 |

---

## 問題 34

**題目**
A company wants a fully managed, flexible, and scalable file storage system, with low latency access, for its Windows-based applications. Which AWS service is the right choice?
一家公司希望為 Windows 型應用程式提供全受管、靈活且可擴展的檔案儲存系統，且具有低延遲存取。哪個 AWS 服務是正確選擇？

**[選項]**
- A. Amazon Elastic File System (Amazon EFS)／Linux NFS 檔案系統
- B. Amazon Elastic Block Storage (Amazon EBS)／區塊儲存
- C. Amazon FSx for Lustre／高效能 Lustre 檔案系統
- D. Amazon FSx for Windows File Server／Windows 檔案伺服器

**正確答案**
Amazon FSx for Windows File Server／Windows 檔案伺服器

**為什麼正確**
**Amazon FSx for Windows File Server** 提供全受管 Windows 原生檔案系統，支援 SMB、Windows ACL 和 Active Directory 整合，適合 Windows 應用程式。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic File System (Amazon EFS)／Linux NFS 檔案系統 | ❌ 錯誤 | EFS 主要支援 Linux/NFS 場景。 |
| Amazon Elastic Block Storage (Amazon EBS)／區塊儲存 | ❌ 錯誤 | EBS 是區塊儲存，不是共享 Windows 檔案系統。 |
| Amazon FSx for Lustre／高效能 Lustre 檔案系統 | ❌ 錯誤 | FSx for Lustre 適合 HPC、機器學習等高效能 Linux 檔案工作負載。 |
| Amazon FSx for Windows File Server／Windows 檔案伺服器 | ✅ 正確 | FSx for Windows 提供 Windows 原生、全受管 SMB 檔案儲存。 |

---

## 問題 35

**題目**
Which cloud transformation journey phase of the AWS Cloud Adoption Framework (AWS CAF) focuses on demonstrating how the cloud will help accelerate your business outcomes?
AWS 雲端採用框架（AWS CAF）的哪個雲端轉型旅程階段專注於展示雲端如何幫助加速業務成果？

**[選項]**
- A. Scale／擴展
- B. Launch／啟動
- C. Align／對齊
- D. Envision／願景

**正確答案**
Envision／願景

**為什麼正確**
AWS CAF 的 **Envision** 階段會展示雲端如何加速業務成果，幫助組織建立轉型願景與商業價值方向。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Scale／擴展 | ❌ 錯誤 | Scale 著重擴大雲端採用與實現規模化價值。 |
| Launch／啟動 | ❌ 錯誤 | Launch 著重交付試點或初始生產工作負載。 |
| Align／對齊 | ❌ 錯誤 | Align 著重找出能力差距與組織依賴關係。 |
| Envision／願景 | ✅ 正確 | Envision 著重說明雲端如何加速業務成果。 |

---

## 問題 36

**題目**
Which characteristic of Cloud Computing imparts the ability to acquire resources as you need and release when you no longer need them?
雲端運算的哪項特性賦予了在需要時獲取資源並在不再需要時釋放資源的能力？

**[選項]**
- A. Resiliency／韌性
- B. Reliability／可靠性
- C. Durability／持久性
- D. Elasticity／彈性

**正確答案**
Elasticity／彈性

**為什麼正確**
**Elasticity** 指能依需求快速取得資源，並在不需要時釋放資源，避免長期過度佈建。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Resiliency／韌性 | ❌ 錯誤 | 韌性是從故障、負載或攻擊中恢復的能力。 |
| Reliability／可靠性 | ❌ 錯誤 | 可靠性是系統持續正確運作並從故障恢復的能力。 |
| Durability／持久性 | ❌ 錯誤 | 持久性通常指資料長期保存不遺失。 |
| Elasticity／彈性 | ✅ 正確 | 彈性就是按需取得和釋放資源。 |

---

## 問題 37

**題目**
Which of the following foundational capabilities can be found under the Operations Perspective of the AWS Cloud Adoption Framework?
以下哪些基礎功能可以在 AWS 雲端採用框架的營運觀點下找到？

**[選項]**
- A. Platform engineering／平台工程
- B. Application portfolio management／應用程式組合管理
- C. Vulnerability management／漏洞管理
- D. Performance and capacity management／效能和容量管理

**正確答案**
Performance and capacity management／效能和容量管理

**為什麼正確**
AWS CAF 的 **Operations Perspective** 關注雲端營運、服務交付、事件、問題、變更、效能與容量管理等能力。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Platform engineering／平台工程 | ❌ 錯誤 | Platform engineering 屬於平台觀點。 |
| Application portfolio management／應用程式組合管理 | ❌ 錯誤 | Application portfolio management 屬於治理觀點。 |
| Vulnerability management／漏洞管理 | ❌ 錯誤 | Vulnerability management 屬於安全觀點。 |
| Performance and capacity management／效能和容量管理 | ✅ 正確 | 這是營運觀點下的基礎能力。 |

---

## 問題 38

**題目**
An online gaming company wants to block users from certain geographies from accessing its content. Which AWS service can be used to accomplish this task?
一家線上遊戲公司希望封鎖特定地區的使用者存取其內容。哪個 AWS 服務可用於完成此任務？

**[選項]**
- A. Security group／安全群組
- B. Amazon CloudWatch／監控服務
- C. AWS Shield／DDoS 防護
- D. AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆

**正確答案**
AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆

**為什麼正確**
**AWS WAF** 可用地理比對條件建立規則，允許或封鎖來自特定國家/地區的 Web 請求。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Security group／安全群組 | ❌ 錯誤 | Security Group 控制執行個體層級入站/出站流量，不提供地理位置封鎖規則。 |
| Amazon CloudWatch／監控服務 | ❌ 錯誤 | CloudWatch 用於監控，不封鎖請求。 |
| AWS Shield／DDoS 防護 | ❌ 錯誤 | Shield 用於 DDoS 防護，不做地理位置內容存取控制。 |
| AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆 | ✅ 正確 | WAF 可基於地理位置封鎖 Web 請求。 |

---

## 問題 39

**題目**
Which of the following statement is correct regarding the AWS pricing policy for data transfer charges into or out of an AWS Region?
以下哪項陳述關於 AWS 對進出 AWS 區域的資料傳輸費用定價政策是正確的？

**[選項]**
- A. Neither inbound nor outbound data transfer are charged／進出站資料傳輸均不收費
- B. Only inbound data transfer is charged／只有入站資料傳輸收費
- C. Both inbound data transfer and outbound data transfer are charged／入站和出站資料傳輸均收費
- D. Only outbound data transfer is charged／只有出站資料傳輸收費

**正確答案**
Only outbound data transfer is charged／只有出站資料傳輸收費

**為什麼正確**
一般而言，傳入 AWS 的資料傳輸免費；從 AWS 傳出到網際網路或跨區域傳輸通常會收費。因此 CCP 考點常記為：**Outbound Data Transfer 是主要成本驅動因素之一**。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Neither inbound nor outbound data transfer are charged／進出站資料傳輸均不收費 | ❌ 錯誤 | 出站資料傳輸通常會收費。 |
| Only inbound data transfer is charged／只有入站資料傳輸收費 | ❌ 錯誤 | 入站資料傳輸通常免費。 |
| Both inbound data transfer and outbound data transfer are charged／入站和出站資料傳輸均收費 | ❌ 錯誤 | 入站通常不收費。 |
| Only outbound data transfer is charged／只有出站資料傳輸收費 | ✅ 正確 | AWS 常見計費規則是入站免費、出站收費。 |

---

## 問題 40

**題目**
Which of the following statements are correct about the AWS root user account? (Select two)
以下哪些陳述關於 AWS 根使用者帳戶是正確的？（選兩項）

**[選項]**
- A. Root user credentials should only be shared with managers requiring administrative responsibilities to complete their jobs／根使用者憑證可分享給需要管理職責的管理員
- B. Root user account gets unrestricted permissions when the account is created, but these can be restricted using IAM policies／Root 權限可用 IAM 政策限制
- C. Root user account password cannot be changed once it is set／Root 密碼一旦設定就無法更改
- D. It is highly recommended to enable Multi-Factor Authentication (MFA) for root user account／強烈建議為 root 使用者啟用 MFA
- E. Root user access credentials are the email address and password used to create the AWS account／Root 憑證是建立 AWS 帳戶所用的電子郵件地址和密碼

**正確答案**
It is highly recommended to enable MFA for root user account／強烈建議啟用 MFA；Root user access credentials are the email address and password used to create the AWS account／Root 憑證是建立帳戶的電子郵件和密碼

**為什麼正確**
Root user 是 AWS 帳戶的最高權限身分，登入憑證是建立帳戶時使用的電子郵件和密碼。最佳實務是啟用 MFA 並避免日常使用 root。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Root user credentials should only be shared with managers requiring administrative responsibilities to complete their jobs／根使用者憑證可分享給需要管理職責的管理員 | ❌ 錯誤 | Root 憑證不應分享，應建立個別 IAM 使用者或角色。 |
| Root user account gets unrestricted permissions when the account is created, but these can be restricted using IAM policies／Root 權限可用 IAM 政策限制 | ❌ 錯誤 | IAM 政策不能限制 root user 的完整帳戶權限。 |
| Root user account password cannot be changed once it is set／Root 密碼一旦設定就無法更改 | ❌ 錯誤 | Root 密碼可以變更。 |
| It is highly recommended to enable Multi-Factor Authentication (MFA) for root user account／強烈建議為 root 使用者啟用 MFA | ✅ 正確 | Root 權限極高，必須強化保護。 |
| Root user access credentials are the email address and password used to create the AWS account／Root 憑證是建立 AWS 帳戶所用的電子郵件地址和密碼 | ✅ 正確 | AWS 帳戶 root 使用者以建立帳戶的電子郵件和密碼登入。 |

---

## 問題 41

**題目**
An organization has a complex IT architecture involving a lot of system dependencies and it wants to track the history of changes to each resource. Which AWS service will help the organization track the history of configuration changes for all the resources?
一個組織擁有涉及許多系統相依關係的複雜 IT 架構，希望追蹤每個資源的變更歷史。哪個 AWS 服務將幫助組織追蹤所有資源的設定變更歷史？

**[選項]**
- A. AWS Service Catalog／服務目錄
- B. AWS CloudTrail／活動稽核
- C. AWS CloudFormation／基礎設施即程式碼
- D. AWS Config／資源組態追蹤

**正確答案**
AWS Config／資源組態追蹤

**為什麼正確**
**AWS Config** 會記錄 AWS 資源組態、組態變更歷史與資源關聯，並可用規則評估資源是否符合期望設定。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Service Catalog／服務目錄 | ❌ 錯誤 | Service Catalog 管理已核准的服務目錄，不追蹤資源組態歷史。 |
| AWS CloudTrail／活動稽核 | ❌ 錯誤 | CloudTrail 記錄 API 呼叫與帳戶活動，不是資源組態狀態歷史。 |
| AWS CloudFormation／基礎設施即程式碼 | ❌ 錯誤 | CloudFormation 用模板佈建資源，不是完整配置歷史追蹤服務。 |
| AWS Config／資源組態追蹤 | ✅ 正確 | Config 專門追蹤資源組態變更與合規。 |

---

## 問題 42

**題目**
Which of the following options can be used to access and manage all AWS services? (Select three)
以下哪些選項可用於存取和管理所有 AWS 服務？（選三項）

**[選項]**
- A. Amazon API Gateway／API 閘道
- B. AWS Secrets Manager／機密管理
- C. AWS Systems Manager／系統管理
- D. AWS Software Development Kit (SDK)／軟體開發套件
- E. AWS Command Line Interface (AWS CLI)／命令列介面
- F. AWS Management Console／管理主控台

**正確答案**
AWS Software Development Kit (SDK)／軟體開發套件；AWS Command Line Interface (AWS CLI)／命令列介面；AWS Management Console／管理主控台

**為什麼正確**
AWS 服務可透過三種主要方式管理：**Management Console**（圖形介面）、**AWS CLI**（命令列）、**AWS SDK**（程式語言 API）。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon API Gateway／API 閘道 | ❌ 錯誤 | API Gateway 用於建立和管理 API，不是通用 AWS 管理入口。 |
| AWS Secrets Manager／機密管理 | ❌ 錯誤 | Secrets Manager 管理機密，不用來管理所有 AWS 服務。 |
| AWS Systems Manager／系統管理 | ❌ 錯誤 | Systems Manager 管理部分資源操作，不是通用全服務存取方式。 |
| AWS Software Development Kit (SDK)／軟體開發套件 | ✅ 正確 | SDK 提供語言特定 API，可程式化管理 AWS 服務。 |
| AWS Command Line Interface (AWS CLI)／命令列介面 | ✅ 正確 | CLI 可用命令列管理 AWS 服務。 |
| AWS Management Console／管理主控台 | ✅ 正確 | Console 是管理 AWS 服務的 Web 圖形介面。 |

---

## 問題 43

**題目**
A startup is looking for 24x7 phone based technical support for its AWS account. Which of the following is the MOST cost-effective AWS support plan for this use-case?
一家新創公司正在尋找 24 小時全天候電話技術支援。以下哪個是此使用案例最具成本效益的 AWS 支援方案？

**[選項]**
- A. AWS Enterprise On-Ramp Support／Enterprise On-Ramp 支援
- B. AWS Developer Support／開發者支援
- C. AWS Enterprise Support／企業支援
- D. AWS Business Support／商業支援

**正確答案**
AWS Business Support／商業支援

**為什麼正確**
**AWS Business Support** 是可提供 24/7 電話、聊天與電子郵件技術支援的較低成本支援方案；Enterprise 類方案更高階也更昂貴。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Enterprise On-Ramp Support／Enterprise On-Ramp 支援 | ❌ 錯誤 | 也提供較高階支援，但成本高於 Business，不是最具成本效益。 |
| AWS Developer Support／開發者支援 | ❌ 錯誤 | Developer Support 不提供 24/7 電話支援。 |
| AWS Enterprise Support／企業支援 | ❌ 錯誤 | Enterprise Support 提供最高階支援，但成本最高，不符合最具成本效益。 |
| AWS Business Support／商業支援 | ✅ 正確 | Business Support 是提供 24/7 電話技術支援的最具成本效益選擇。 |

---

## 問題 44

**題目**
A photo sharing web application wants to store thumbnails of user-uploaded images on Amazon S3. The thumbnails are rarely used but need to be immediately accessible from the web application. The thumbnails can be regenerated easily if they are lost. Which is the most cost-effective way to store these thumbnails?
一個照片共享 Web 應用程式希望在 Amazon S3 上儲存使用者上傳圖片的縮圖。縮圖很少使用，但需要能從 Web 應用程式立即存取。如果縮圖遺失，可以輕鬆重新生成。儲存這些縮圖最具成本效益的方式是什麼？

**[選項]**
- A. Use Amazon S3 Standard to store the thumbnails／使用 S3 Standard 儲存縮圖
- B. Use Amazon S3 Standard-Infrequent Access (S3 Standard-IA) to store the thumbnails／使用 S3 Standard-IA 儲存縮圖
- C. Use Amazon S3 Glacier Flexible Retrieval to store the thumbnails／使用 S3 Glacier Flexible Retrieval 儲存縮圖
- D. Use Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA) to store the thumbnails／使用 S3 One Zone-IA 儲存縮圖

**正確答案**
Use Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA) to store the thumbnails／使用 S3 One Zone-IA 儲存縮圖

**為什麼正確**
縮圖很少使用但需要立即存取，且遺失可重新產生，因此可接受單一 AZ 較低可用性。**S3 One Zone-IA** 比 Standard-IA 成本更低，適合可重新產生、不常存取但需快速取回的資料。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Use Amazon S3 Standard to store the thumbnails／使用 S3 Standard 儲存縮圖 | ❌ 錯誤 | S3 Standard 適合頻繁存取，對很少使用的縮圖成本較高。 |
| Use Amazon S3 Standard-Infrequent Access (S3 Standard-IA) to store the thumbnails／使用 S3 Standard-IA 儲存縮圖 | ❌ 錯誤 | Standard-IA 適合低頻但需多 AZ 高可用資料；本題資料可重建，可用更便宜 One Zone-IA。 |
| Use Amazon S3 Glacier Flexible Retrieval to store the thumbnails／使用 S3 Glacier Flexible Retrieval 儲存縮圖 | ❌ 錯誤 | Glacier Flexible Retrieval 不是立即存取，通常需數分鐘到數小時取回。 |
| Use Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA) to store the thumbnails／使用 S3 One Zone-IA 儲存縮圖 | ✅ 正確 | One Zone-IA 低成本、低頻且可立即存取，適合可重建縮圖。 |

---

## 問題 45

**題目**
An e-commerce company wants to store data from a recommendation engine in a database. Which AWS service would you recommend to provide this functionality with the LEAST operational overhead for any scale?
一家電子商務公司希望將推薦引擎的資料儲存在資料庫中。您會推薦哪個 AWS 服務，以在任何規模下提供最少的營運負擔？

**[選項]**
- A. Amazon Relational Database Service (Amazon RDS)／關聯式資料庫
- B. Amazon Simple Storage Service (Amazon S3)／物件儲存
- C. Amazon Neptune／圖形資料庫
- D. Amazon DynamoDB／NoSQL 資料庫

**正確答案**
Amazon DynamoDB／NoSQL 資料庫

**為什麼正確**
**Amazon DynamoDB** 是全託管 NoSQL 資料庫，可在任意規模提供低延遲讀寫，無需管理伺服器、修補、擴展或容量規劃細節，營運負擔最低。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Relational Database Service (Amazon RDS)／關聯式資料庫 | ❌ 錯誤 | RDS 是受管關聯式資料庫，但仍有較多容量、版本與資料庫層設定考量。 |
| Amazon Simple Storage Service (Amazon S3)／物件儲存 | ❌ 錯誤 | S3 是物件儲存，不是資料庫服務。 |
| Amazon Neptune／圖形資料庫 | ❌ 錯誤 | Neptune 適合圖形關係資料，不是一般推薦引擎資料最低營運負擔首選。 |
| Amazon DynamoDB／NoSQL 資料庫 | ✅ 正確 | DynamoDB 全託管、可自動擴展，適合任意規模與低營運負擔。 |

---

## 問題 46

**題目**
A developer has written a simple web application in PHP and he wants to just upload his code to AWS Cloud and have AWS handle the deployment automatically but still wants access to the underlying operating system. Which of the following AWS services would you recommend for this use-case?
一位開發人員用 PHP 編寫了一個簡單的 Web 應用程式，希望只需將程式碼上傳至 AWS 雲端，讓 AWS 自動處理部署，但仍希望存取底層作業系統。您會推薦以下哪個 AWS 服務？

**[選項]**
- A. Amazon Elastic Container Service (Amazon ECS)／容器編排
- B. Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器
- C. AWS CloudFormation／基礎設施即程式碼
- D. AWS Elastic Beanstalk／應用部署平台

**正確答案**
AWS Elastic Beanstalk／應用部署平台

**為什麼正確**
**Elastic Beanstalk** 可讓開發者上傳 PHP 等應用程式碼，由 AWS 自動處理部署、容量佈建、負載平衡、擴展與健康監控，同時仍可存取底層 EC2 等資源。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic Container Service (Amazon ECS)／容器編排 | ❌ 錯誤 | ECS 用於容器化應用，需要容器與任務定義，不是單純上傳 PHP 程式碼的最簡方式。 |
| Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器 | ❌ 錯誤 | EC2 可存取 OS，但需要自行部署和管理應用環境。 |
| AWS CloudFormation／基礎設施即程式碼 | ❌ 錯誤 | CloudFormation 是佈建資源工具，不是應用部署平台本身。 |
| AWS Elastic Beanstalk／應用部署平台 | ✅ 正確 | Beanstalk 支援上傳程式碼自動部署，且保留底層資源存取能力。 |

---

## 問題 47

**題目**
According to the AWS Shared Responsibility Model, which of the following are responsibilities of the customer for Amazon RDS?
根據 AWS 共同責任模型，以下哪些是客戶對 Amazon RDS 的責任？

**[選項]**
- A. Applying patches to the Amazon RDS database／為 Amazon RDS 資料庫套用修補程式
- B. Applying patches to the underlying OS／為底層作業系統套用修補程式
- C. Managing the underlying server hardware on which Amazon RDS runs／管理 RDS 底層伺服器硬體
- D. Database encryption／資料庫加密

**正確答案**
Database encryption／資料庫加密

**為什麼正確**
Amazon RDS 是受管資料庫，AWS 負責底層硬體、作業系統與資料庫引擎修補等管理工作；客戶仍負責資料、存取控制與是否啟用/設定資料庫加密。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Applying patches to the Amazon RDS database／為 Amazon RDS 資料庫套用修補程式 | ❌ 錯誤 | RDS 的資料庫引擎修補由 AWS 代管。 |
| Applying patches to the underlying OS／為底層作業系統套用修補程式 | ❌ 錯誤 | RDS 底層 OS 由 AWS 管理。 |
| Managing the underlying server hardware on which Amazon RDS runs／管理 RDS 底層伺服器硬體 | ❌ 錯誤 | 伺服器硬體由 AWS 負責。 |
| Database encryption／資料庫加密 | ✅ 正確 | 客戶負責決定和設定資料庫加密與資料保護。 |

---

## 問題 48

**題目**
Which of the following AWS services allows a database to have flexible schema and supports document data models?
以下哪個 AWS 服務允許資料庫具有靈活的結構描述並支援文件資料模型？

**[選項]**
- A. Amazon Relational Database Service (Amazon RDS)／關聯式資料庫
- B. Amazon Aurora／雲端關聯式資料庫
- C. Amazon Redshift／資料倉儲
- D. Amazon DynamoDB／NoSQL 資料庫

**正確答案**
Amazon DynamoDB／NoSQL 資料庫

**為什麼正確**
**Amazon DynamoDB** 是 NoSQL 資料庫，支援鍵值與文件資料模型，可使用彈性 schema，不需要像關聯式資料庫一樣固定欄位結構。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Relational Database Service (Amazon RDS)／關聯式資料庫 | ❌ 錯誤 | RDS 是關聯式資料庫，通常使用固定 schema。 |
| Amazon Aurora／雲端關聯式資料庫 | ❌ 錯誤 | Aurora 是關聯式資料庫，支援 MySQL/PostgreSQL 相容模型。 |
| Amazon Redshift／資料倉儲 | ❌ 錯誤 | Redshift 是資料倉儲，使用結構化表格模型。 |
| Amazon DynamoDB／NoSQL 資料庫 | ✅ 正確 | DynamoDB 支援彈性 schema 和文件資料模型。 |

---

## 問題 49

**題目**
A company's flagship application runs on a fleet of Amazon EC2 instances. The system administrators are looking for the best way to provide secure shell access to Amazon EC2 instances without opening new ports or using public IP addresses. Which tool/service will help you achieve this requirement?
一家公司的旗艦應用程式在 Amazon EC2 執行個體群上執行。系統管理員正在尋找最佳方式，在不開啟新連接埠或使用公用 IP 位址的情況下提供對 Amazon EC2 執行個體的安全 Shell 存取。哪個工具/服務可以實現此需求？

**[選項]**
- A. Amazon Route 53／DNS 服務
- B. Amazon Inspector／弱點評估
- C. Amazon EC2 Instance Connect／EC2 連線工具
- D. AWS Systems Manager Session Manager／Session Manager

**正確答案**
AWS Systems Manager Session Manager／Session Manager

**為什麼正確**
**Session Manager** 可透過瀏覽器或 CLI 安全連線到 EC2，不需要開放 SSH 連接埠、不需要公用 IP，也不需要管理 SSH 金鑰或堡壘主機。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Route 53／DNS 服務 | ❌ 錯誤 | Route 53 是 DNS 服務，不提供 Shell 存取。 |
| Amazon Inspector／弱點評估 | ❌ 錯誤 | Inspector 評估弱點，不提供互動式連線。 |
| Amazon EC2 Instance Connect／EC2 連線工具 | ❌ 錯誤 | EC2 Instance Connect 仍常涉及 SSH 存取路徑，不是「不開新 port 或不用公用 IP」的最佳答案。 |
| AWS Systems Manager Session Manager／Session Manager | ✅ 正確 | Session Manager 可無需開放 SSH port 或公用 IP 安全連線 EC2。 |

---

## 問題 50

**題目**
Which of the following is the correct statement regarding the AWS Storage services?
以下哪項是關於 AWS 儲存服務的正確陳述？

**[選項]**
- A. Amazon S3 is file based storage, Amazon EBS is block based storage and Amazon EFS is object based storage／S3 是檔案，EBS 是區塊，EFS 是物件
- B. Amazon S3 is block based storage, Amazon EBS is object based storage and Amazon EFS is file based storage／S3 是區塊，EBS 是物件，EFS 是檔案
- C. Amazon S3 is object based storage, Amazon EBS is file based storage and Amazon EFS is block based storage／S3 是物件，EBS 是檔案，EFS 是區塊
- D. Amazon S3 is object based storage, Amazon EBS is block based storage and Amazon EFS is file based storage／S3 是物件，EBS 是區塊，EFS 是檔案

**正確答案**
Amazon S3 is object based storage, Amazon EBS is block based storage and Amazon EFS is file based storage／S3 是物件，EBS 是區塊，EFS 是檔案

**為什麼正確**
AWS 三大常見儲存類型：**S3 是物件儲存**、**EBS 是區塊儲存**、**EFS 是檔案儲存**。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3 is file based storage, Amazon EBS is block based storage and Amazon EFS is object based storage／S3 是檔案，EBS 是區塊，EFS 是物件 | ❌ 錯誤 | S3 與 EFS 類型被對調。 |
| Amazon S3 is block based storage, Amazon EBS is object based storage and Amazon EFS is file based storage／S3 是區塊，EBS 是物件，EFS 是檔案 | ❌ 錯誤 | S3 與 EBS 類型錯誤。 |
| Amazon S3 is object based storage, Amazon EBS is file based storage and Amazon EFS is block based storage／S3 是物件，EBS 是檔案，EFS 是區塊 | ❌ 錯誤 | EBS 與 EFS 類型被對調。 |
| Amazon S3 is object based storage, Amazon EBS is block based storage and Amazon EFS is file based storage／S3 是物件，EBS 是區塊，EFS 是檔案 | ✅ 正確 | S3、EBS、EFS 分別對應物件、區塊、檔案儲存。 |

---

## 問題 51

**題目**
Which Amazon Route 53 routing policy would you use to improve the performance for your customers by routing the requests to the AWS endpoint that provides the fastest experience?
您會使用哪個 Amazon Route 53 路由政策，透過將請求路由至提供最快體驗的 AWS 端點來改善客戶的效能？

**[選項]**
- A. Weighted routing／加權路由
- B. Failover routing／容錯移轉路由
- C. Simple routing／簡單路由
- D. Latency-based routing／延遲型路由

**正確答案**
Latency-based routing／延遲型路由

**為什麼正確**
**Latency-based routing** 會根據使用者到各 AWS 區域或端點的延遲，將請求導向預期延遲最低、體驗最快的端點。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Weighted routing／加權路由 | ❌ 錯誤 | Weighted routing 用於按比例分配流量，不一定選最快端點。 |
| Failover routing／容錯移轉路由 | ❌ 錯誤 | Failover routing 用於主備切換，不是效能最佳化。 |
| Simple routing／簡單路由 | ❌ 錯誤 | Simple routing 是基本 DNS 回應，沒有依延遲選路。 |
| Latency-based routing／延遲型路由 | ✅ 正確 | Latency-based routing 會導向最低延遲端點以改善效能。 |

---

## 問題 52

**題目**
Which AWS service publishes up-to-the-minute information on the general status and availability of all AWS services in all the Regions of AWS Cloud?
哪個 AWS 服務發布 AWS 雲端所有區域中所有 AWS 服務的一般狀態和可用性的最新資訊？

**[選項]**
- A. AWS Health Dashboard - Your account health／您的帳戶健康狀態
- B. Amazon CloudWatch／監控服務
- C. AWS CloudFormation／基礎設施即程式碼
- D. AWS Health Dashboard - service health／服務健康狀態

**正確答案**
AWS Health Dashboard - service health／服務健康狀態

**為什麼正確**
**Service Health Dashboard** 顯示所有 AWS 服務在所有區域的一般公開狀態與可用性。若要看自己帳戶受影響情況，則用 Your Account Health Dashboard。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Health Dashboard - Your account health／您的帳戶健康狀態 | ❌ 錯誤 | 這是個人化帳戶影響視圖，不是所有服務的一般公開狀態。 |
| Amazon CloudWatch／監控服務 | ❌ 錯誤 | CloudWatch 監控客戶資源指標與日誌。 |
| AWS CloudFormation／基礎設施即程式碼 | ❌ 錯誤 | CloudFormation 用於佈建資源。 |
| AWS Health Dashboard - service health／服務健康狀態 | ✅ 正確 | Service Health 提供所有 AWS 服務和區域的一般健康狀態。 |

---

## 問題 53

**題目**
What are the fundamental drivers of cost with AWS Cloud?
AWS 雲端的基本成本驅動因素是什麼？

**[選項]**
- A. Compute, Databases and Outbound Data Transfer／運算、資料庫和出站資料傳輸
- B. Compute, Storage and Inbound Data Transfer／運算、儲存和入站資料傳輸
- C. Compute, Databases and Inbound Data Transfer／運算、資料庫和入站資料傳輸
- D. Compute, Storage and Outbound Data Transfer／運算、儲存和出站資料傳輸

**正確答案**
Compute, Storage and Outbound Data Transfer／運算、儲存和出站資料傳輸

**為什麼正確**
AWS 成本的基本驅動因素通常概括為三類：**運算**、**儲存**、**出站資料傳輸**。入站資料傳輸通常免費；資料庫雖會產生成本，但不是這個經典三分類的名稱。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Compute, Databases and Outbound Data Transfer／運算、資料庫和出站資料傳輸 | ❌ 錯誤 | 資料庫不是此題所問的三大基本成本驅動因素之一。 |
| Compute, Storage and Inbound Data Transfer／運算、儲存和入站資料傳輸 | ❌ 錯誤 | 入站資料傳輸通常免費，不是主要成本驅動因素。 |
| Compute, Databases and Inbound Data Transfer／運算、資料庫和入站資料傳輸 | ❌ 錯誤 | 同時包含資料庫和入站資料傳輸，與考點不符。 |
| Compute, Storage and Outbound Data Transfer／運算、儲存和出站資料傳輸 | ✅ 正確 | 運算、儲存和出站資料傳輸是 AWS 的基本成本驅動因素。 |

---

## 問題 54

**題目**
Which Amazon EC2 pricing model is the most cost-effective and flexible with no requirement for a long term resource commitment or upfront payment but still guarantees that instance would not be interrupted?
哪種 Amazon EC2 定價模型最具成本效益和靈活性，不需要長期資源承諾或預付款，但仍保證執行個體不會被中斷？

**[選項]**
- A. Reserved Instance (RI)／保留執行個體
- B. Dedicated Host／專用主機
- C. Spot Instance／Spot 執行個體
- D. On-demand Instance／隨需執行個體

**正確答案**
On-demand Instance／隨需執行個體

**為什麼正確**
題目同時要求「無長期承諾」、「無預付款」和「不會被中斷」。**On-Demand Instance** 符合這三點，雖然單價不是最低，但在不承諾且不中斷的條件下最適合。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Reserved Instance (RI)／保留執行個體 | ❌ 錯誤 | RI 可降低成本且不中斷，但需要 1 年或 3 年承諾。 |
| Dedicated Host／專用主機 | ❌ 錯誤 | Dedicated Host 適合授權或合規需求，通常不是此題的成本與彈性最佳選擇。 |
| Spot Instance／Spot 執行個體 | ❌ 錯誤 | Spot 成本最低但可能被中斷。 |
| On-demand Instance／隨需執行個體 | ✅ 正確 | On-Demand 無長期承諾、無預付款，且不會像 Spot 一樣被中斷。 |

---

## 問題 55

**題目**
A customer has created a VPC and a subnet within AWS Cloud. Which of the following statements is correct?
一位客戶在 AWS 雲端中建立了 VPC 和子網路。以下哪項陳述是正確的？

**[選項]**
- A. Both the VPC and the subnet span only one AZ in the Region／VPC 和子網路都只跨越一個 AZ
- B. A subnet spans all of the AZs in the Region whereas a VPC spans only one AZ in the Region／子網路跨越所有 AZ，VPC 只跨越一個 AZ
- C. Both the VPC and the subnet span all of the AZs in the Region／VPC 和子網路都跨越所有 AZ
- D. A VPC spans all of the AZs in the Region whereas a subnet spans only one AZ in the Region／VPC 跨越區域中所有 AZ，子網路只跨越一個 AZ

**正確答案**
A VPC spans all of the AZs in the Region whereas a subnet spans only one AZ in the Region／VPC 跨越區域中所有 AZ，子網路只跨越一個 AZ

**為什麼正確**
**VPC 是區域級資源**，可涵蓋該區域內多個 AZ；**Subnet 是 AZ 級資源**，每個子網路只能位於單一 AZ。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Both the VPC and the subnet span only one AZ in the Region／VPC 和子網路都只跨越一個 AZ | ❌ 錯誤 | VPC 不是單 AZ 資源。 |
| A subnet spans all of the AZs in the Region whereas a VPC spans only one AZ in the Region／子網路跨越所有 AZ，VPC 只跨越一個 AZ | ❌ 錯誤 | 說反了；子網路只在單一 AZ。 |
| Both the VPC and the subnet span all of the AZs in the Region／VPC 和子網路都跨越所有 AZ | ❌ 錯誤 | 子網路不跨多 AZ。 |
| A VPC spans all of the AZs in the Region whereas a subnet spans only one AZ in the Region／VPC 跨越區域中所有 AZ，子網路只跨越一個 AZ | ✅ 正確 | VPC 是區域範圍，Subnet 是單一 AZ 範圍。 |

---

## 問題 56

**題目**
Which AWS service should be used when you want to run container applications, but want to avoid the operational overhead of scaling, patching, securing, and managing servers?
當您想執行容器應用程式，但又想避免擴展、修補、保護和管理伺服器的營運負擔時，應使用哪個 AWS 服務？

**[選項]**
- A. AWS Lambda／無伺服器函數
- B. Amazon Elastic Container Service (Amazon ECS) - EC2 launch type／ECS EC2 啟動類型
- C. Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器
- D. Amazon Elastic Container Service (Amazon ECS) - Fargate launch type／ECS Fargate 啟動類型

**正確答案**
Amazon Elastic Container Service (Amazon ECS) - Fargate launch type／ECS Fargate 啟動類型

**為什麼正確**
**AWS Fargate** 是 ECS 的無伺服器啟動類型，可執行容器而不需要管理 EC2 伺服器、叢集容量、修補或底層安全維護。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Lambda／無伺服器函數 | ❌ 錯誤 | Lambda 執行函數，不是用來管理一般長時間容器化應用的主要容器平台。 |
| Amazon Elastic Container Service (Amazon ECS) - EC2 launch type／ECS EC2 啟動類型 | ❌ 錯誤 | ECS EC2 啟動類型仍需管理 EC2 叢集。 |
| Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器 | ❌ 錯誤 | EC2 需要自行管理伺服器。 |
| Amazon Elastic Container Service (Amazon ECS) - Fargate launch type／ECS Fargate 啟動類型 | ✅ 正確 | ECS Fargate 可無伺服器執行容器，減少伺服器營運負擔。 |

---

## 問題 57

**題目**
Which of the following statement is correct for a Security Group and a Network Access Control List (Network ACL)?
以下哪項陳述關於安全群組和網路存取控制清單（Network ACL）是正確的？

**[選項]**
- A. Security Group acts as a firewall at the subnet level whereas Network ACL acts as a firewall at the instance level／安全群組在子網路層級，NACL 在執行個體層級
- B. Security Group acts as a firewall at the VPC level whereas Network ACL acts as a firewall at the AZ level／安全群組在 VPC 層級，NACL 在 AZ 層級
- C. Security Group acts as a firewall at the AZ level whereas Network ACL acts as a firewall at the VPC level／安全群組在 AZ 層級，NACL 在 VPC 層級
- D. Security Group acts as a firewall at the instance level whereas Network ACL acts as a firewall at the subnet level／安全群組在執行個體層級，NACL 在子網路層級

**正確答案**
Security Group acts as a firewall at the instance level whereas Network ACL acts as a firewall at the subnet level／安全群組在執行個體層級，NACL 在子網路層級

**為什麼正確**
**Security Group** 附加到 ENI/執行個體層級且是有狀態；**Network ACL** 附加到子網路層級且是無狀態。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Security Group acts as a firewall at the subnet level whereas Network ACL acts as a firewall at the instance level／安全群組在子網路層級，NACL 在執行個體層級 | ❌ 錯誤 | 層級說反了。 |
| Security Group acts as a firewall at the VPC level whereas Network ACL acts as a firewall at the AZ level／安全群組在 VPC 層級，NACL 在 AZ 層級 | ❌ 錯誤 | 兩者都不是這樣作用。 |
| Security Group acts as a firewall at the AZ level whereas Network ACL acts as a firewall at the VPC level／安全群組在 AZ 層級，NACL 在 VPC 層級 | ❌ 錯誤 | 兩者層級錯誤。 |
| Security Group acts as a firewall at the instance level whereas Network ACL acts as a firewall at the subnet level／安全群組在執行個體層級，NACL 在子網路層級 | ✅ 正確 | Security Group 是執行個體/ENI 層級，Network ACL 是子網路層級。 |

---

## 問題 58

**題目**
Which AWS service would you use to send alerts when the costs for your AWS account exceed your budgeted amount?
哪個 AWS 服務可讓您在 AWS 帳戶的成本超過預算金額時發送警報？

**[選項]**
- A. AWS Pricing Calculator／定價試算
- B. AWS Cost Explorer／成本分析
- C. AWS Organizations／多帳戶管理
- D. AWS Budgets／預算管理

**正確答案**
AWS Budgets／預算管理

**為什麼正確**
**AWS Budgets** 可設定成本、用量、RI 或 Savings Plans 預算，並在實際或預測成本超過門檻時發送告警。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Pricing Calculator／定價試算 | ❌ 錯誤 | Pricing Calculator 用於事前估算成本，不監控實際花費。 |
| AWS Cost Explorer／成本分析 | ❌ 錯誤 | Cost Explorer 用於查看和分析成本趨勢，不是預算告警服務。 |
| AWS Organizations／多帳戶管理 | ❌ 錯誤 | Organizations 用於多帳戶與整合帳單管理。 |
| AWS Budgets／預算管理 | ✅ 正確 | Budgets 可在成本超出或預測超出預算時發送通知。 |

---

## 問題 59

**題目**
Which policy describes prohibited uses of the web services offered by Amazon Web Services?
哪個政策描述了 Amazon Web Services 提供的 Web 服務的禁止使用行為？

**[選項]**
- A. AWS Trusted Advisor／最佳實務建議
- B. AWS Applicable Use Policy／AWS 適用使用政策
- C. AWS Fair Use Policy／AWS 公平使用政策
- D. AWS Acceptable Use Policy／AWS 可接受使用政策

**正確答案**
AWS Acceptable Use Policy／AWS 可接受使用政策

**為什麼正確**
**AWS Acceptable Use Policy (AUP)** 描述禁止使用 AWS 服務的行為，例如非法、有害、侵權或濫用網路的活動。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Trusted Advisor／最佳實務建議 | ❌ 錯誤 | Trusted Advisor 是最佳實務建議工具，不是政策文件。 |
| AWS Applicable Use Policy／AWS 適用使用政策 | ❌ 錯誤 | 這不是正確的 AWS 政策名稱。 |
| AWS Fair Use Policy／AWS 公平使用政策 | ❌ 錯誤 | 這不是題目所指的 AWS 禁止使用政策。 |
| AWS Acceptable Use Policy／AWS 可接受使用政策 | ✅ 正確 | AUP 定義 AWS 服務的禁止使用行為。 |

---

## 問題 60

**題目**
An organization deploys its IT infrastructure in a combination of its on-premises data center along with AWS Cloud. How would you categorize this deployment model?
一個組織將其 IT 基礎設施部署在本地資料中心和 AWS 雲端的組合中。您如何分類此部署模型？

**[選項]**
- A. Cloud deployment／雲端部署
- B. Private deployment／私有部署
- C. Mixed deployment／混合部署
- D. Hybrid deployment／混合部署

**正確答案**
Hybrid deployment／混合部署

**為什麼正確**
**Hybrid deployment** 指同時使用本地資料中心與雲端環境的部署模式。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Cloud deployment／雲端部署 | ❌ 錯誤 | Cloud deployment 通常表示完全部署在雲端。 |
| Private deployment／私有部署 | ❌ 錯誤 | Private deployment 通常指私有環境或本地環境，不包含公有雲組合。 |
| Mixed deployment／混合部署 | ❌ 錯誤 | 「Mixed deployment」不是 AWS 考點中的標準部署模型名稱。 |
| Hybrid deployment／混合部署 | ✅ 正確 | 本地資料中心加 AWS Cloud 是混合部署。 |

---

## 問題 61

**題目**
A data analytics company stores its data on Amazon S3 and wants to do SQL based analysis on this data with minimum effort. Which of the following AWS services will you suggest for this use case?
一家資料分析公司將其資料儲存在 Amazon S3 上，希望以最少的工作量對此資料進行基於 SQL 的分析。您會建議哪個 AWS 服務？

**[選項]**
- A. Amazon Aurora／關聯式資料庫
- B. Amazon DynamoDB／NoSQL 資料庫
- C. Amazon Redshift／資料倉儲
- D. Amazon Athena／互動式查詢服務

**正確答案**
Amazon Athena／互動式查詢服務

**為什麼正確**
**Amazon Athena** 是無伺服器互動式查詢服務，可直接使用標準 SQL 查詢 Amazon S3 中的資料，不需要先載入資料或管理基礎設施。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Aurora／關聯式資料庫 | ❌ 錯誤 | Aurora 是關聯式資料庫，不是直接查詢 S3 資料的最小工作量方案。 |
| Amazon DynamoDB／NoSQL 資料庫 | ❌ 錯誤 | DynamoDB 是 NoSQL 資料庫，不用來直接 SQL 查詢 S3。 |
| Amazon Redshift／資料倉儲 | ❌ 錯誤 | Redshift 可做分析，但通常涉及資料倉儲和載入/外部表設定，不是最少工作量答案。 |
| Amazon Athena／互動式查詢服務 | ✅ 正確 | Athena 可無伺服器直接用 SQL 查詢 S3 資料。 |

---

## 問題 62

**題目**
What are the different gateway types supported by AWS Storage Gateway service?
AWS Storage Gateway 服務支援哪些不同的閘道類型？

**[選項]**
- A. Tape Gateway, Object Gateway and Volume Gateway／磁帶閘道、物件閘道和磁碟區閘道
- B. Tape Gateway, File Gateway and Block Gateway／磁帶閘道、檔案閘道和區塊閘道
- C. Object Gateway, File Gateway and Block Gateway／物件閘道、檔案閘道和區塊閘道
- D. Tape Gateway, File Gateway and Volume Gateway／磁帶閘道、檔案閘道和磁碟區閘道

**正確答案**
Tape Gateway, File Gateway and Volume Gateway／磁帶閘道、檔案閘道和磁碟區閘道

**為什麼正確**
**AWS Storage Gateway** 的主要閘道類型是 **File Gateway**、**Volume Gateway** 和 **Tape Gateway**，分別支援檔案、區塊磁碟區與虛擬磁帶備份整合。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Tape Gateway, Object Gateway and Volume Gateway／磁帶閘道、物件閘道和磁碟區閘道 | ❌ 錯誤 | Storage Gateway 沒有 Object Gateway 這個類型。 |
| Tape Gateway, File Gateway and Block Gateway／磁帶閘道、檔案閘道和區塊閘道 | ❌ 錯誤 | 正確名稱是 Volume Gateway，不是 Block Gateway。 |
| Object Gateway, File Gateway and Block Gateway／物件閘道、檔案閘道和區塊閘道 | ❌ 錯誤 | Object Gateway 和 Block Gateway 都不是正確類型。 |
| Tape Gateway, File Gateway and Volume Gateway／磁帶閘道、檔案閘道和磁碟區閘道 | ✅ 正確 | 這是 Storage Gateway 支援的三種主要閘道類型。 |

---

## 問題 63

**題目**
A retail company has multiple AWS accounts for each of its departments. Which of the following AWS services can be used to set up consolidated billing and a single payment method for these AWS accounts?
一家零售公司為其每個部門擁有多個 AWS 帳戶。以下哪個 AWS 服務可用於為這些 AWS 帳戶設定合併計費和單一付款方式？

**[選項]**
- A. AWS Budgets／預算管理
- B. AWS Secrets Manager／機密管理
- C. AWS Cost Explorer／成本分析
- D. AWS Organizations／多帳戶管理

**正確答案**
AWS Organizations／多帳戶管理

**為什麼正確**
**AWS Organizations** 可集中管理多個 AWS 帳戶，支援整合帳單、單一付款方式、組織單位和服務控制政策。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Budgets／預算管理 | ❌ 錯誤 | Budgets 用於設定預算與告警，不建立整合帳單付款結構。 |
| AWS Secrets Manager／機密管理 | ❌ 錯誤 | Secrets Manager 管理密碼與機密。 |
| AWS Cost Explorer／成本分析 | ❌ 錯誤 | Cost Explorer 用於分析成本，不管理多帳戶付款方式。 |
| AWS Organizations／多帳戶管理 | ✅ 正確 | Organizations 提供多帳戶集中管理與合併計費。 |

---

## 問題 64

**題目**
A company is using a message broker service on its on-premises application and wants to move this messaging functionality to AWS Cloud. Which of the following AWS services is the right choice to move the existing functionality easily?
一家公司在其本地應用程式上使用訊息代理服務，並希望將此訊息功能移至 AWS 雲端。以下哪個 AWS 服務是輕鬆遷移現有功能的正確選擇？

**[選項]**
- A. Amazon Simple Queue Service (Amazon SQS)／訊息佇列
- B. Amazon Kinesis Data Streams／串流資料
- C. Amazon Simple Notification Service (Amazon SNS)／發布訂閱通知
- D. Amazon MQ／受管訊息代理

**正確答案**
Amazon MQ／受管訊息代理

**為什麼正確**
**Amazon MQ** 是 Apache ActiveMQ 和 RabbitMQ 的受管訊息代理服務，支援常見協定與 API，適合將既有本地 message broker 功能較容易地遷移到 AWS。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Simple Queue Service (Amazon SQS)／訊息佇列 | ❌ 錯誤 | SQS 是雲端原生佇列服務，通常需要調整應用程式整合方式。 |
| Amazon Kinesis Data Streams／串流資料 | ❌ 錯誤 | Kinesis 用於即時串流資料處理，不是傳統 message broker 遷移服務。 |
| Amazon Simple Notification Service (Amazon SNS)／發布訂閱通知 | ❌ 錯誤 | SNS 是發布/訂閱通知服務，不是相容傳統 broker 的遷移選項。 |
| Amazon MQ／受管訊息代理 | ✅ 正確 | Amazon MQ 可遷移既有 ActiveMQ/RabbitMQ 類型訊息代理功能。 |

---

## 問題 65

**題目**
Which of the following AWS services can be used to prevent Distributed Denial-of-Service (DDoS) attack? (Select three)
以下哪些 AWS 服務可用於防止分散式阻斷服務（DDoS）攻擊？（選三項）

**[選項]**
- A. AWS CloudHSM／雲端硬體安全模組
- B. Amazon Inspector／弱點評估
- C. AWS Trusted Advisor／最佳實務建議
- D. Amazon CloudFront with Amazon Route 53／CloudFront 搭配 Route 53
- E. AWS Shield／DDoS 防護
- F. AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆

**正確答案**
Amazon CloudFront with Amazon Route 53／CloudFront 搭配 Route 53；AWS Shield／DDoS 防護；AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆

**為什麼正確**
DDoS 防護常見組合是 **AWS Shield** 提供自動 DDoS 緩解，**AWS WAF** 過濾第 7 層惡意請求與速率型規則，**CloudFront + Route 53** 利用全球邊緣網路和 DNS 韌性吸收與分散攻擊流量。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS CloudHSM／雲端硬體安全模組 | ❌ 錯誤 | CloudHSM 用於硬體加密金鑰管理，不是 DDoS 防護。 |
| Amazon Inspector／弱點評估 | ❌ 錯誤 | Inspector 用於弱點掃描，不防止 DDoS。 |
| AWS Trusted Advisor／最佳實務建議 | ❌ 錯誤 | Trusted Advisor 提供最佳實務建議，不直接防止 DDoS。 |
| Amazon CloudFront with Amazon Route 53／CloudFront 搭配 Route 53 | ✅ 正確 | 全球邊緣網路和 DNS 韌性可協助分散和吸收 DDoS 流量。 |
| AWS Shield／DDoS 防護 | ✅ 正確 | Shield 是 AWS 的 DDoS 防護服務。 |
| AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆 | ✅ 正確 | WAF 可用第 7 層規則和速率限制協助抵禦 Web 層攻擊。 |

---
