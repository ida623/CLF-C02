# AWS CCP 05 選項解析

來源：
- 題目與選項：[AWS_CCP_Practice_Test5.md](AWS_CCP_Practice_Test5.md)
- 原詳解：[AWS_CCP_05.md](AWS_CCP_05.md)

這份檔案針對每題列出中英對照題目與選項，並用中文說明正確答案與其他選項的差異。

---

## 問題 1

**題目**
Which security control tool can be used to deny traffic from a specific IP address?
哪個安全控制工具可以用來拒絕來自特定 IP 位址的流量？

**[選項]**
- A. VPC Flow Logs
- B. Amazon GuardDuty
- C. Security Group／安全群組
- D. Network Access Control List (network ACL)／網路存取控制清單

**正確答案**
Network Access Control List (network ACL)／網路存取控制清單

**為什麼正確**
**Network ACL** 在子網路層級控制流量，規則可以允許或拒絕特定來源、目的地與連接埠，因此可以用來拒絕來自特定 IP 位址的流量。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| VPC Flow Logs | ❌ 錯誤 | VPC Flow Logs 用來記錄網路流量，不會主動允許或拒絕流量。 |
| Amazon GuardDuty | ❌ 錯誤 | GuardDuty 是威脅偵測服務，不是流量控制工具。 |
| Security Group／安全群組 | ❌ 錯誤 | Security Group 只能設定允許規則，不能明確拒絕特定 IP。 |
| Network Access Control List (network ACL)／網路存取控制清單 | ✅ 正確 | Network ACL 可設定允許與拒絕規則，適合封鎖特定 IP。 |

---

## 問題 2

**題目**
Which of the following statements is an AWS best practice when architecting for the Cloud?
以下哪項陳述是 AWS 雲端架構的最佳實務？

**[選項]**
- A. Close coupling／緊耦合
- B. Servers, not services／伺服器，而非服務
- C. Security comes last／安全最後考量
- D. Automation／自動化

**正確答案**
Automation／自動化

**為什麼正確**
AWS 雲端架構鼓勵用自動化降低人工操作、提升一致性與可重複性，例如自動化部署、擴展、修補與復原。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Close coupling／緊耦合 | ❌ 錯誤 | 雲端最佳實務是鬆耦合，讓元件能獨立擴展與失敗隔離。 |
| Servers, not services／伺服器，而非服務 | ❌ 錯誤 | AWS 建議優先使用受管服務，減少伺服器維運負擔。 |
| Security comes last／安全最後考量 | ❌ 錯誤 | 安全應從設計初期就納入，而不是最後才補上。 |
| Automation／自動化 | ✅ 正確 | 自動化是雲端架構的重要最佳實務。 |

---

## 問題 3

**題目**
Which of the following AWS Support plans is the MOST cost-effective when getting enhanced technical support by Cloud Support Engineers?
以下哪個 AWS Support 方案在獲得 Cloud Support Engineers 強化技術支援方面最具成本效益？

**[選項]**
- A. AWS Basic Support
- B. AWS Developer Support
- C. AWS Enterprise Support
- D. AWS Business Support

**正確答案**
AWS Business Support

**為什麼正確**
**AWS Business Support** 提供 Cloud Support Engineers 的增強技術支援，而且成本低於 Enterprise Support，因此在題目要求的支援等級中最具成本效益。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Basic Support | ❌ 錯誤 | Basic Support 不提供進階技術支援工程師服務。 |
| AWS Developer Support | ❌ 錯誤 | Developer Support 較適合開發測試，支援層級低於 Business。 |
| AWS Enterprise Support | ❌ 錯誤 | Enterprise Support 支援更完整但成本最高，不是最具成本效益。 |
| AWS Business Support | ✅ 正確 | Business Support 提供 Cloud Support Engineers 支援，且比 Enterprise 成本更低。 |

---

## 問題 4

**題目**
Which of the following criteria are used to calculate the charge for Amazon EBS Volumes? (Select Two)
以下哪些標準用於計算 Amazon EBS 磁碟區的費用？（選兩項）

**[選項]**
- A. Data type／資料類型
- B. The Amazon EC2 instance type the EBS volume is attached to／附加的 EC2 執行個體類型
- C. Data transfer IN／資料傳入
- D. Volume type／磁碟區類型
- E. Provisioned IOPS／佈建的 IOPS

**正確答案**
Volume type／磁碟區類型；Provisioned IOPS／佈建的 IOPS

**為什麼正確**
Amazon EBS 的費用會受到磁碟區類型、佈建容量、佈建 IOPS、快照與資料傳出等因素影響。題目選項中，**Volume type** 與 **Provisioned IOPS** 是正確計費標準。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Data type／資料類型 | ❌ 錯誤 | EBS 不會依儲存的資料內容類型計費。 |
| The Amazon EC2 instance type the EBS volume is attached to／附加的 EC2 執行個體類型 | ❌ 錯誤 | EC2 執行個體類型影響 EC2 費用，不是 EBS 磁碟區的直接計費標準。 |
| Data transfer IN／資料傳入 | ❌ 錯誤 | 資料傳入 AWS 通常不收費，且不是 EBS Volume 的主要計費項。 |
| Volume type／磁碟區類型 | ✅ 正確 | 不同 EBS 類型有不同儲存與效能價格。 |
| Provisioned IOPS／佈建的 IOPS | ✅ 正確 | io1/io2 等類型會依佈建 IOPS 收費。 |

---

## 問題 5

**題目**
Which of the following AWS services can be used to generate, use, and manage encryption keys on the AWS Cloud?
以下哪個 AWS 服務可用於在 AWS 雲端上產生、使用和管理加密金鑰？

**[選項]**
- A. AWS GuardDuty
- B. AWS Secrets Manager
- C. Amazon Inspector
- D. AWS CloudHSM

**正確答案**
AWS CloudHSM

**為什麼正確**
**AWS CloudHSM** 提供專用硬體安全模組，讓客戶在 AWS 雲端中產生、使用和管理加密金鑰，並能掌控自己的 HSM 金鑰材料。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS GuardDuty | ❌ 錯誤 | GuardDuty 用於偵測威脅，不是金鑰管理服務。 |
| AWS Secrets Manager | ❌ 錯誤 | Secrets Manager 管理密碼、API key 等機密，不是 HSM 金鑰管理。 |
| Amazon Inspector | ❌ 錯誤 | Inspector 用於漏洞與安全評估，不負責加密金鑰管理。 |
| AWS CloudHSM | ✅ 正確 | CloudHSM 可在專用 HSM 中產生、使用與管理加密金鑰。 |

---

## 問題 6

**題目**
A company needs to use a secure online data transfer tool/service that can automate the ongoing transfers from on-premises systems into AWS while providing support for incremental data backups.
一家公司需要使用安全的線上資料傳輸工具，能自動化將本地系統持續傳輸至 AWS，並支援增量資料備份。

**[選項]**
- A. AWS Snowball
- B. AWS Snowball Edge
- C. AWS Storage Gateway
- D. AWS DataSync

**正確答案**
AWS DataSync

**為什麼正確**
**AWS DataSync** 是安全的線上資料傳輸服務，可自動化本地端與 AWS 儲存服務之間的持續資料傳輸，也支援增量傳輸與備份情境。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Snowball | ❌ 錯誤 | Snowball 是離線實體裝置，適合一次性大量資料遷移。 |
| AWS Snowball Edge | ❌ 錯誤 | Snowball Edge 偏向離線資料搬移與邊緣運算，不是持續線上同步工具。 |
| AWS Storage Gateway | ❌ 錯誤 | Storage Gateway 是混合雲儲存整合服務，不是題目強調的線上自動化資料傳輸工具。 |
| AWS DataSync | ✅ 正確 | DataSync 可自動化、安全且持續地將本地資料傳入 AWS。 |

---

## 問題 7

**題目**
According to the AWS Well-Architected Framework, which of the following statements are recommendations in the Operational Excellence pillar? (Select two)
根據 AWS Well-Architected Framework，以下哪些陳述是卓越營運支柱的建議？（選兩項）

**[選項]**
- A. Enable traceability／啟用可追溯性
- B. Automatically recover from failure／自動從故障中恢復
- C. Use serverless architectures／使用無伺服器架構
- D. Anticipate failure／預測故障
- E. Make frequent, small, reversible changes／進行頻繁、小型、可回復的變更

**正確答案**
Anticipate failure／預測故障；Make frequent, small, reversible changes／進行頻繁、小型、可回復的變更

**為什麼正確**
卓越營運支柱強調以小而可逆的變更降低風險，並預先假設可能失敗、演練與改進營運流程。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Enable traceability／啟用可追溯性 | ❌ 錯誤 | 啟用可追溯性主要屬於安全支柱的設計原則。 |
| Automatically recover from failure／自動從故障中恢復 | ❌ 錯誤 | 自動從故障恢復屬於可靠性支柱。 |
| Use serverless architectures／使用無伺服器架構 | ❌ 錯誤 | 使用無伺服器架構主要屬於效能效率支柱的建議。 |
| Anticipate failure／預測故障 | ✅ 正確 | 預測與演練失敗是卓越營運支柱的重要原則。 |
| Make frequent, small, reversible changes／進行頻繁、小型、可回復的變更 | ✅ 正確 | 小型且可回復的變更能降低營運風險。 |

---

## 問題 8

**題目**
A production company would like to establish an AWS managed virtual private network (VPN) service between its on-premises network and AWS. Which item needs to be set up on the company's side?
一家公司希望在本地網路與 AWS 之間建立 AWS 管理的 VPN 服務。公司端需要設定哪個項目？

**[選項]**
- A. A security group／安全群組
- B. A virtual private gateway (VGW)／虛擬私有閘道
- C. A VPC endpoint interface／VPC 端點介面
- D. A customer gateway／客戶閘道

**正確答案**
A customer gateway／客戶閘道

**為什麼正確**
Site-to-Site VPN 連線中，公司本地端要設定 **Customer Gateway**，代表客戶端 VPN 裝置或軟體設備；AWS 端則使用 Virtual Private Gateway 或 Transit Gateway。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| A security group／安全群組 | ❌ 錯誤 | Security Group 控制 AWS 資源流量，不是 VPN 公司端元件。 |
| A virtual private gateway (VGW)／虛擬私有閘道 | ❌ 錯誤 | VGW 是 AWS 端的 VPN 元件，不是公司端設定。 |
| A VPC endpoint interface／VPC 端點介面 | ❌ 錯誤 | VPC endpoint 用於私有連線至 AWS 服務，不是 Site-to-Site VPN 公司端。 |
| A customer gateway／客戶閘道 | ✅ 正確 | Customer Gateway 代表客戶端 VPN 裝置或設定。 |

---

## 問題 9

**題目**
A company needs to keep sensitive data in its own data center due to compliance but would still like to deploy resources using AWS. Which Cloud deployment model does this refer to?
一家公司因合規需要將敏感資料保存在自有資料中心，但仍希望使用 AWS 部署資源。這是指哪種雲端部署模型？

**[選項]**
- A. Public Cloud／公有雲
- B. Private Cloud／私有雲
- C. On-premises／地端
- D. Hybrid Cloud／混合雲

**正確答案**
Hybrid Cloud／混合雲

**為什麼正確**
**Hybrid Cloud** 指同時使用本地資料中心與雲端資源。題目描述敏感資料留在自有資料中心，但仍使用 AWS 部署資源，正是混合雲。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Public Cloud／公有雲 | ❌ 錯誤 | 公有雲代表資源主要部署在雲端，不包含題目的本地保留需求。 |
| Private Cloud／私有雲 | ❌ 錯誤 | 私有雲通常指專用私有環境，題目還要使用 AWS。 |
| On-premises／地端 | ❌ 錯誤 | 完全地端不符合「仍使用 AWS 部署資源」。 |
| Hybrid Cloud／混合雲 | ✅ 正確 | 混合雲結合本地環境與 AWS 雲端。 |

---

## 問題 10

**題目**
Which of the following options is NOT a feature of Amazon Inspector?
以下哪項不是 Amazon Inspector 的功能？

**[選項]**
- A. Automate security assessments／自動化安全評估
- B. Analyze against unintended network accessibility／分析非預期的網路可存取性
- C. Inspect running OS against known vulnerabilities／檢查執行中的作業系統是否存在已知漏洞
- D. Track configuration changes／追蹤設定變更

**正確答案**
Track configuration changes／追蹤設定變更

**為什麼正確**
Amazon Inspector 用於自動化漏洞與安全評估；追蹤 AWS 資源設定變更是 **AWS Config** 的用途，因此不是 Inspector 的功能。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Automate security assessments／自動化安全評估 | ❌ 錯誤 | 這是 Amazon Inspector 的功能，因此不是本題答案。 |
| Analyze against unintended network accessibility／分析非預期的網路可存取性 | ❌ 錯誤 | Inspector 可協助分析非預期的網路可達性。 |
| Inspect running OS against known vulnerabilities／檢查執行中的作業系統是否存在已知漏洞 | ❌ 錯誤 | Inspector 可檢查已知漏洞。 |
| Track configuration changes／追蹤設定變更 | ✅ 正確 | 追蹤設定變更是 AWS Config 的功能，不是 Inspector。 |

---

## 問題 11

**題目**
What is the primary use case for Amazon GuardDuty?
Amazon GuardDuty 的主要使用案例是什麼？

**[選項]**
- A. Enforcing secure communication between VPCs using network traffic filtering／使用網路流量過濾強制執行 VPC 之間的安全通訊
- B. Protecting web applications from common exploits such as SQL injection／保護 Web 應用程式免受 SQL 注入等常見攻擊
- C. Encrypting data in transit between AWS services using TLS certificates／使用 TLS 憑證加密 AWS 服務之間的傳輸資料
- D. Detecting malicious activity and threats in your AWS accounts and workloads／偵測 AWS 帳戶和工作負載中的惡意活動與威脅

**正確答案**
Detecting malicious activity and threats in your AWS accounts and workloads／偵測 AWS 帳戶和工作負載中的惡意活動與威脅

**為什麼正確**
**Amazon GuardDuty** 是智慧威脅偵測服務，會分析 CloudTrail、VPC Flow Logs、DNS logs 等資料，找出 AWS 帳戶與工作負載中的可疑活動。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Enforcing secure communication between VPCs using network traffic filtering／使用網路流量過濾強制執行 VPC 之間的安全通訊 | ❌ 錯誤 | 這較接近網路防火牆或流量控制服務。 |
| Protecting web applications from common exploits such as SQL injection／保護 Web 應用程式免受 SQL 注入等常見攻擊 | ❌ 錯誤 | 防護 SQL injection、XSS 等 Web 攻擊是 AWS WAF 的用途。 |
| Encrypting data in transit between AWS services using TLS certificates／使用 TLS 憑證加密 AWS 服務之間的傳輸資料 | ❌ 錯誤 | TLS 憑證通常由 AWS Certificate Manager 管理。 |
| Detecting malicious activity and threats in your AWS accounts and workloads／偵測 AWS 帳戶和工作負載中的惡意活動與威脅 | ✅ 正確 | GuardDuty 的核心用途就是威脅偵測。 |

---

## 問題 12

**題目**
Which of the following billing timeframes is applied when running a Windows EC2 on-demand instance?
執行 Windows EC2 隨需執行個體時，適用以下哪種計費時間單位？

**[選項]**
- A. Pay per day／按天計費
- B. Pay per hour／按小時計費
- C. Pay per minute／按分鐘計費
- D. Pay per second／按秒計費

**正確答案**
Pay per second／按秒計費

**為什麼正確**
Windows EC2 On-Demand 執行個體採用按秒計費，通常有最低 60 秒計費門檻，因此題目中的正確時間單位是按秒。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Pay per day／按天計費 | ❌ 錯誤 | EC2 On-Demand 不以天作為標準計費單位。 |
| Pay per hour／按小時計費 | ❌ 錯誤 | 舊觀念容易混淆，現行 Windows EC2 On-Demand 可按秒計費。 |
| Pay per minute／按分鐘計費 | ❌ 錯誤 | 不是主要計費粒度，雖有最低 60 秒但仍是按秒。 |
| Pay per second／按秒計費 | ✅ 正確 | Windows EC2 On-Demand 以秒為計費單位。 |

---

## 問題 13

**題目**
Which AWS service can be used to send, store, and receive messages between software components at any volume to decouple application tiers?
哪個 AWS 服務可用於在任意規模的軟體元件之間傳送、儲存和接收訊息，以解耦應用程式層？

**[選項]**
- A. AWS Organizations
- B. AWS Elastic Beanstalk
- C. Amazon Simple Notification Service (Amazon SNS)
- D. Amazon Simple Queue Service (Amazon SQS)

**正確答案**
Amazon Simple Queue Service (Amazon SQS)

**為什麼正確**
**Amazon SQS** 是訊息佇列服務，可在元件之間傳送、儲存與接收訊息，讓應用程式層之間鬆耦合並可獨立擴展。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Organizations | ❌ 錯誤 | Organizations 用於多帳戶治理，不處理應用程式訊息。 |
| AWS Elastic Beanstalk | ❌ 錯誤 | Beanstalk 是應用程式部署與管理平台，不是訊息佇列。 |
| Amazon Simple Notification Service (Amazon SNS) | ❌ 錯誤 | SNS 是發布/訂閱推播服務，不是用來儲存並讓消費者拉取訊息的佇列。 |
| Amazon Simple Queue Service (Amazon SQS) | ✅ 正確 | SQS 能傳送、儲存、接收訊息並解耦應用元件。 |

---

## 問題 14

**題目**
A company would like to move its infrastructure to AWS Cloud. Which of the following should be included in the Total Cost of Ownership (TCO) estimate? (Select TWO)
一家公司希望將基礎設施遷移至 AWS 雲端。以下哪些項目應包含在 TCO 估算中？（選兩項）

**[選項]**
- A. Electronic equipment at office／辦公室電子設備
- B. Number of end-users／終端使用者數量
- C. Application advertising／應用程式廣告
- D. Server administration／伺服器管理
- E. Power/Cooling／電力／冷卻

**正確答案**
Server administration／伺服器管理；Power/Cooling／電力／冷卻

**為什麼正確**
TCO 估算比較本地基礎設施與雲端成本，會納入伺服器管理、人力、硬體、電力與冷卻等基礎設施相關成本。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Electronic equipment at office／辦公室電子設備 | ❌ 錯誤 | 一般辦公設備不是資料中心基礎設施 TCO 重點。 |
| Number of end-users／終端使用者數量 | ❌ 錯誤 | 使用者數可能影響需求，但不是本題 TCO 項目。 |
| Application advertising／應用程式廣告 | ❌ 錯誤 | 廣告成本不是基礎設施遷移 TCO。 |
| Server administration／伺服器管理 | ✅ 正確 | 伺服器維運人力與管理成本應納入 TCO。 |
| Power/Cooling／電力／冷卻 | ✅ 正確 | 本地資料中心的電力與冷卻是重要成本。 |

---

## 問題 15

**題目**
Which AWS service allows you to quickly and easily add user sign-up, sign-in, and access control to web and mobile applications?
哪個 AWS 服務可讓您快速輕鬆地為 Web 和行動應用程式新增使用者註冊、登入和存取控制？

**[選項]**
- A. AWS IAM Identity Center
- B. AWS Identity and Access Management (AWS IAM)
- C. AWS Organizations
- D. Amazon Cognito

**正確答案**
Amazon Cognito

**為什麼正確**
**Amazon Cognito** 專門用於 Web 與行動應用程式的使用者註冊、登入、身分驗證與存取控制，適合面向終端使用者的 App。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS IAM Identity Center | ❌ 錯誤 | IAM Identity Center 用於企業員工對多帳戶與應用程式的 SSO。 |
| AWS Identity and Access Management (AWS IAM) | ❌ 錯誤 | IAM 管理 AWS 資源存取，不是 App 使用者註冊登入服務。 |
| AWS Organizations | ❌ 錯誤 | Organizations 管理多個 AWS 帳戶。 |
| Amazon Cognito | ✅ 正確 | Cognito 提供 App 使用者註冊、登入與存取控制。 |

---

## 問題 16

**題目**
A media company wants to enable customized content suggestions for the users of its movie streaming platform. Which AWS service can provide these personalized recommendations based on historic data?
一家媒體公司希望為其電影串流平台的使用者提供個人化內容建議。哪個 AWS 服務可根據歷史資料提供這些個人化推薦？

**[選項]**
- A. Amazon Customize
- B. Amazon SageMaker
- C. Amazon Comprehend
- D. Amazon Personalize

**正確答案**
Amazon Personalize

**為什麼正確**
**Amazon Personalize** 用機器學習建立即時個人化推薦，常用於影音內容、電商商品與新聞推薦等情境。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Customize | ❌ 錯誤 | 這不是正確的 AWS 服務名稱。 |
| Amazon SageMaker | ❌ 錯誤 | SageMaker 是通用 ML 建模平台，需要自行建立訓練流程。 |
| Amazon Comprehend | ❌ 錯誤 | Comprehend 是自然語言處理服務，不是推薦引擎。 |
| Amazon Personalize | ✅ 正確 | Personalize 專門提供個人化推薦。 |

---

## 問題 17

**題目**
An organization would like to copy data across different Availability Zones (AZs) using Amazon EBS snapshots. Where are Amazon EBS snapshots stored in the AWS Cloud?
一個組織希望使用 Amazon EBS 快照跨不同可用區域複製資料。Amazon EBS 快照儲存在 AWS 雲端的哪裡？

**[選項]**
- A. Amazon EC2
- B. Amazon RDS
- C. Amazon EFS
- D. Amazon Simple Storage Service (Amazon S3)

**正確答案**
Amazon Simple Storage Service (Amazon S3)

**為什麼正確**
Amazon EBS 快照是 EBS 磁碟區的時間點備份，底層儲存在 **Amazon S3**，可用來在同一 Region 的不同 AZ 建立新磁碟區。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon EC2 | ❌ 錯誤 | EC2 是運算服務，不是 EBS 快照的儲存位置。 |
| Amazon RDS | ❌ 錯誤 | RDS 是受管關聯式資料庫服務。 |
| Amazon EFS | ❌ 錯誤 | EFS 是檔案系統服務，不儲存 EBS 快照。 |
| Amazon Simple Storage Service (Amazon S3) | ✅ 正確 | EBS 快照底層儲存在 S3。 |

---

## 問題 18

**題目**
A growing start-up has trouble identifying and protecting sensitive data at scale. Which AWS fully managed service can assist with this task?
一家成長中的新創公司難以大規模識別和保護敏感資料。哪個 AWS 全受管服務可以協助完成此任務？

**[選項]**
- A. AWS Artifact
- B. AWS Secrets Manager
- C. AWS Key Management Service (AWS KMS)
- D. Amazon Macie

**正確答案**
Amazon Macie

**為什麼正確**
**Amazon Macie** 是全受管資料安全與隱私服務，可使用機器學習與模式比對在 S3 中大規模識別敏感資料，例如 PII。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Artifact | ❌ 錯誤 | Artifact 提供合規報告與協議文件，不負責掃描敏感資料。 |
| AWS Secrets Manager | ❌ 錯誤 | Secrets Manager 用來管理密碼與 API key 等機密。 |
| AWS Key Management Service (AWS KMS) | ❌ 錯誤 | KMS 管理加密金鑰，不會大規模識別敏感資料。 |
| Amazon Macie | ✅ 正確 | Macie 可自動探索與保護敏感資料。 |

---

## 問題 19

**題目**
A company is planning to implement Chaos Engineering to expose any blind spots that can disrupt the resiliency of the application. Which AWS service will help implement this requirement with the least effort?
一家公司計劃實施混沌工程以找出影響應用程式韌性的盲點。哪個 AWS 服務能以最少工作量幫助實現此需求？

**[選項]**
- A. Amazon GuardDuty
- B. AWS Trusted Advisor
- C. Amazon Inspector
- D. AWS Fault Injection Simulator (AWS FIS)

**正確答案**
AWS Fault Injection Simulator (AWS FIS)

**為什麼正確**
**AWS Fault Injection Simulator** 是用於執行錯誤注入實驗的受管服務，可模擬故障並驗證系統韌性，是 AWS 上實作混沌工程的對應服務。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon GuardDuty | ❌ 錯誤 | GuardDuty 偵測威脅，不做錯誤注入。 |
| AWS Trusted Advisor | ❌ 錯誤 | Trusted Advisor 提供最佳實務建議，不執行混沌工程實驗。 |
| Amazon Inspector | ❌ 錯誤 | Inspector 評估漏洞，不模擬故障。 |
| AWS Fault Injection Simulator (AWS FIS) | ✅ 正確 | FIS 可用於故障注入與韌性測試。 |

---

## 問題 20

**題目**
Which AWS serverless service allows you to prepare data for analytics?
哪個 AWS 無伺服器服務可讓您為分析準備資料？

**[選項]**
- A. Amazon Redshift
- B. Amazon Athena
- C. Amazon EMR
- D. AWS Glue

**正確答案**
AWS Glue

**為什麼正確**
**AWS Glue** 是無伺服器資料整合與 ETL 服務，可探索、轉換和準備資料，以供分析、查詢或機器學習使用。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Redshift | ❌ 錯誤 | Redshift 是資料倉儲，用於分析查詢，不是主要的 ETL 準備服務。 |
| Amazon Athena | ❌ 錯誤 | Athena 用 SQL 查詢 S3 資料，不是資料準備 ETL 服務。 |
| Amazon EMR | ❌ 錯誤 | EMR 是大數據叢集服務，不是題目強調的無伺服器資料準備首選。 |
| AWS Glue | ✅ 正確 | Glue 是無伺服器 ETL，可為分析準備資料。 |

---

## 問題 21

**題目**
An e-commerce company would like to build a chatbot for its customer service using Natural Language Understanding (NLU). Which AWS service would you use?
一家電子商務公司希望使用自然語言理解（NLU）為其客戶服務建立聊天機器人。您會使用哪個 AWS 服務？

**[選項]**
- A. Amazon SageMaker
- B. Amazon Comprehend
- C. Amazon Rekognition
- D. Amazon Lex

**正確答案**
Amazon Lex

**為什麼正確**
**Amazon Lex** 提供語音與文字的對話式介面建置能力，支援自然語言理解，常用於建立聊天機器人。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon SageMaker | ❌ 錯誤 | SageMaker 是通用 ML 平台，不是專門的聊天機器人服務。 |
| Amazon Comprehend | ❌ 錯誤 | Comprehend 做文字分析與 NLP，但不直接建立對話式聊天機器人。 |
| Amazon Rekognition | ❌ 錯誤 | Rekognition 用於影像與影片分析。 |
| Amazon Lex | ✅ 正確 | Lex 用於建立具 NLU 能力的聊天機器人。 |

---

## 問題 22

**題目**
Which of the following services are provided by Amazon Route 53? (Select Two)
Amazon Route 53 提供以下哪些服務？（選兩項）

**[選項]**
- A. Load balancing／負載平衡
- B. IP routing／IP 路由
- C. Transfer acceleration／傳輸加速
- D. Domain registration／網域註冊
- E. Health checks and monitoring／健康檢查與監控

**正確答案**
Domain registration／網域註冊；Health checks and monitoring／健康檢查與監控

**為什麼正確**
**Amazon Route 53** 是 DNS 與網域服務，提供網域註冊、DNS 路由、健康檢查與監控等功能。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Load balancing／負載平衡 | ❌ 錯誤 | 負載平衡是 Elastic Load Balancing 的主要功能。 |
| IP routing／IP 路由 | ❌ 錯誤 | Route 53 是 DNS 服務，不是網路層 IP 路由設備。 |
| Transfer acceleration／傳輸加速 | ❌ 錯誤 | Transfer Acceleration 是 Amazon S3 的功能。 |
| Domain registration／網域註冊 | ✅ 正確 | Route 53 可註冊與管理網域。 |
| Health checks and monitoring／健康檢查與監控 | ✅ 正確 | Route 53 可設定健康檢查並搭配 DNS 路由使用。 |

---

## 問題 23

**題目**
A company would like to reserve Amazon EC2 compute capacity for three years to reduce costs. The company also plans to increase their workloads during this period. Which Amazon EC2 reserved instance (RI) type would you recommend?
一家公司希望預留 Amazon EC2 運算容量三年以降低成本，且計劃在此期間增加工作負載。您會推薦哪種保留執行個體（RI）類型？

**[選項]**
- A. Adaptable reserved instances (RI)
- B. Standard reserved instance (RI)／標準保留執行個體
- C. Scheduled reserved instance (RI)／排程保留執行個體
- D. Convertible reserved instance (RI)／可轉換保留執行個體

**正確答案**
Convertible reserved instance (RI)／可轉換保留執行個體

**為什麼正確**
**Convertible RI** 允許在合約期間變更執行個體家族、作業系統或租用等屬性，適合預期工作負載會增加或改變的情境。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Adaptable reserved instances (RI) | ❌ 錯誤 | 這不是標準 EC2 RI 類型名稱。 |
| Standard reserved instance (RI)／標準保留執行個體 | ❌ 錯誤 | Standard RI 折扣高但彈性低，不適合工作負載可能改變。 |
| Scheduled reserved instance (RI)／排程保留執行個體 | ❌ 錯誤 | Scheduled RI 不是目前常用選項，且不符合增加工作負載的彈性需求。 |
| Convertible reserved instance (RI)／可轉換保留執行個體 | ✅ 正確 | Convertible RI 提供較高彈性，適合需求會變動的長期工作負載。 |

---

## 問題 24

**題目**
Which of the following length terms are available for Amazon EC2 reserved instances (RI)? (Select Two)
Amazon EC2 保留執行個體（RI）有哪些可用的期限？（選兩項）

**[選項]**
- A. 6 months／6 個月
- B. 2 years／2 年
- C. 5 years／5 年
- D. 1 year／1 年
- E. 3 years／3 年

**正確答案**
1 year／1 年；3 years／3 年

**為什麼正確**
Amazon EC2 Reserved Instances 的標準承諾期限為 **1 年** 或 **3 年**，通常 3 年承諾可取得更高折扣。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| 6 months／6 個月 | ❌ 錯誤 | EC2 RI 沒有 6 個月標準期限。 |
| 2 years／2 年 | ❌ 錯誤 | EC2 RI 沒有 2 年標準期限。 |
| 5 years／5 年 | ❌ 錯誤 | EC2 RI 沒有 5 年標準期限。 |
| 1 year／1 年 | ✅ 正確 | 1 年是 EC2 RI 的標準期限之一。 |
| 3 years／3 年 | ✅ 正確 | 3 年是 EC2 RI 的標準期限之一。 |

---

## 問題 25

**題目**
According to the AWS Shared Responsibility Model, which of the following is both the responsibility of AWS and the customer? (Select two)
根據 AWS 共同責任模型，以下哪些是 AWS 和客戶共同負責的？（選兩項）

**[選項]**
- A. Data center security／資料中心安全
- B. Customer data／客戶資料
- C. Disposal of disk drives／磁碟機的處置
- D. Operating system (OS) configuration／作業系統設定
- E. Configuration management／設定管理

**正確答案**
Operating system (OS) configuration／作業系統設定；Configuration management／設定管理

**為什麼正確**
共同責任模型中，某些領域 AWS 與客戶各自負責不同層面。例如 AWS 管理基礎設施與主機層，客戶管理客體作業系統、應用程式與自己資源的設定。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Data center security／資料中心安全 | ❌ 錯誤 | 資料中心實體安全屬於 AWS 責任。 |
| Customer data／客戶資料 | ❌ 錯誤 | 客戶資料的保護與分類主要是客戶責任。 |
| Disposal of disk drives／磁碟機的處置 | ❌ 錯誤 | 基礎設施硬碟處置屬於 AWS 責任。 |
| Operating system (OS) configuration／作業系統設定 | ✅ 正確 | AWS 負責主機層，客戶負責客體 OS 設定，因此屬共同責任範圍。 |
| Configuration management／設定管理 | ✅ 正確 | AWS 與客戶分別負責雲端基礎設施與客戶資源的設定管理。 |

---

## 問題 26

**題目**
Which AWS service can be used to subscribe to an RSS feed to be notified of the status of all AWS service interruptions?
哪個 AWS 服務可用於訂閱 RSS feed，以接收所有 AWS 服務中斷狀態的通知？

**[選項]**
- A. AWS Lambda
- B. Amazon Simple Notification Service (Amazon SNS)
- C. AWS Health Dashboard - Your Account Health
- D. AWS Health Dashboard - Service Health

**正確答案**
AWS Health Dashboard - Service Health

**為什麼正確**
**AWS Health Dashboard - Service Health** 顯示所有 AWS 服務的公開健康狀態，並可透過 RSS 訂閱服務中斷與狀態更新。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Lambda | ❌ 錯誤 | Lambda 是無伺服器運算服務，不提供 AWS 服務健康 RSS 狀態頁。 |
| Amazon Simple Notification Service (Amazon SNS) | ❌ 錯誤 | SNS 可傳送通知，但不是 AWS 公開服務健康 RSS 來源。 |
| AWS Health Dashboard - Your Account Health | ❌ 錯誤 | Your Account Health 提供帳戶個人化事件，不是所有服務公開 RSS 狀態。 |
| AWS Health Dashboard - Service Health | ✅ 正確 | Service Health 提供 AWS 服務整體狀態與 RSS 訂閱。 |

---

## 問題 27

**題目**
A corporation would like to simplify access management to multiple AWS accounts as well as facilitate AWS Single Sign-On (AWS SSO) access to its AWS accounts. Which AWS service would you use for this task?
一家公司希望簡化多個 AWS 帳戶的存取管理，並促進 AWS Single Sign-On 存取。您會使用哪個 AWS 服務？

**[選項]**
- A. AWS Identity and Access Management (AWS IAM)
- B. AWS Cognito
- C. AWS Command Line Interface (CLI)
- D. AWS IAM Identity Center

**正確答案**
AWS IAM Identity Center

**為什麼正確**
**AWS IAM Identity Center**（AWS SSO 的後續服務）用於集中管理多個 AWS 帳戶與應用程式的單一登入存取。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Identity and Access Management (AWS IAM) | ❌ 錯誤 | IAM 管理 AWS 身分與權限，但不主打多帳戶 SSO 使用者入口。 |
| AWS Cognito | ❌ 錯誤 | Cognito 適合 Web/行動 App 的終端使用者登入。 |
| AWS Command Line Interface (CLI) | ❌ 錯誤 | CLI 是命令列工具，不是 SSO 存取管理服務。 |
| AWS IAM Identity Center | ✅ 正確 | IAM Identity Center 可集中管理多帳戶 SSO。 |

---

## 問題 28

**題目**
Which AWS tool/service will help you define your cloud infrastructure using popular programming languages such as Python and JavaScript?
哪個 AWS 工具/服務可讓您使用 Python 和 JavaScript 等常見程式語言定義雲端基礎設施？

**[選項]**
- A. AWS CodeBuild
- B. AWS Elastic Beanstalk
- C. AWS CloudFormation
- D. AWS Cloud Development Kit (AWS CDK)

**正確答案**
AWS Cloud Development Kit (AWS CDK)

**為什麼正確**
**AWS CDK** 讓開發者使用 Python、JavaScript、TypeScript、Java、C# 等程式語言定義雲端基礎設施，並合成 CloudFormation 範本部署。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS CodeBuild | ❌ 錯誤 | CodeBuild 是持續整合建置服務，不是 IaC 程式語言框架。 |
| AWS Elastic Beanstalk | ❌ 錯誤 | Beanstalk 是 PaaS 應用部署服務，不是用程式語言定義基礎設施的工具。 |
| AWS CloudFormation | ❌ 錯誤 | CloudFormation 使用 JSON/YAML 範本，不是題目所說的 Python/JavaScript。 |
| AWS Cloud Development Kit (AWS CDK) | ✅ 正確 | CDK 可用常見程式語言定義雲端基礎設施。 |

---

## 問題 29

**題目**
According to the AWS Shared Responsibility Model, which of the following are the responsibilities of AWS? (Select two)
根據 AWS 共同責任模型，以下哪些是 AWS 的責任？（選兩項）

**[選項]**
- A. Installing security patches of the guest operating system (OS)／安裝客體作業系統的安全修補程式
- B. Encrypting application data／加密應用程式資料
- C. Configuring IAM Roles／設定 IAM 角色
- D. Network operability／網路可操作性
- E. Data center security／資料中心安全

**正確答案**
Network operability／網路可操作性；Data center security／資料中心安全

**為什麼正確**
AWS 負責「雲端本身的安全」，包含資料中心、硬體、基礎網路與雲端基礎設施的營運可用性。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Installing security patches of the guest operating system (OS)／安裝客體作業系統的安全修補程式 | ❌ 錯誤 | EC2 客體作業系統修補通常是客戶責任。 |
| Encrypting application data／加密應用程式資料 | ❌ 錯誤 | 應用程式資料加密策略與設定由客戶負責。 |
| Configuring IAM Roles／設定 IAM 角色 | ❌ 錯誤 | IAM 權限與角色設定屬於客戶責任。 |
| Network operability／網路可操作性 | ✅ 正確 | AWS 負責雲端基礎網路的可操作性。 |
| Data center security／資料中心安全 | ✅ 正確 | AWS 負責資料中心實體安全。 |

---

## 問題 30

**題目**
The development team at a company manages 300 microservices and it is now trying to automate the code reviews to improve the code quality. Which tool/service is the right fit for this requirement?
一家公司的開發團隊管理 300 個微服務，現在嘗試自動化程式碼審查以提升程式碼品質。哪個工具/服務最適合此需求？

**[選項]**
- A. AWS CodeBuild
- B. AWS Trusted Advisor
- C. AWS X-Ray
- D. Amazon CodeGuru

**正確答案**
Amazon CodeGuru

**為什麼正確**
**Amazon CodeGuru Reviewer** 使用機器學習協助自動化程式碼審查，找出潛在問題、安全弱點與改善建議，適合提升程式碼品質。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS CodeBuild | ❌ 錯誤 | CodeBuild 負責建置與測試，不是自動化程式碼審查服務。 |
| AWS Trusted Advisor | ❌ 錯誤 | Trusted Advisor 檢查 AWS 帳戶最佳實務，不審查程式碼。 |
| AWS X-Ray | ❌ 錯誤 | X-Ray 用於追蹤與分析分散式應用程式效能。 |
| Amazon CodeGuru | ✅ 正確 | CodeGuru 可自動化程式碼審查並提供品質建議。 |

---

## 問題 31

**題目**
A multinational company has just moved its infrastructure to AWS Cloud and has employees traveling to different offices around the world. How should the company set the AWS accounts?
一家跨國公司剛將基礎設施遷移至 AWS 雲端，員工會前往全球不同辦公室。公司應如何設定 AWS 帳戶？

**[選項]**
- A. As employees travel, they can use other employees' accounts／員工出差時可使用其他員工的帳戶
- B. Create an IAM user for each user in each AWS region／在每個 AWS 區域為每位使用者建立 IAM 使用者
- C. Create global permissions so users can access resources from all around the world／建立全域權限使使用者可存取全球資源
- D. There is nothing to do, AWS IAM is a global service／無需任何操作，AWS IAM 是全球服務

**正確答案**
There is nothing to do, AWS IAM is a global service／無需任何操作，AWS IAM 是全球服務

**為什麼正確**
**AWS IAM 是全球服務**，IAM 使用者與權限不需要依照每個 Region 分開建立；員工可以從全球地點存取同一 AWS 帳戶。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| As employees travel, they can use other employees' accounts／員工出差時可使用其他員工的帳戶 | ❌ 錯誤 | 共用帳號違反安全與稽核最佳實務。 |
| Create an IAM user for each user in each AWS region／在每個 AWS 區域為每位使用者建立 IAM 使用者 | ❌ 錯誤 | IAM 是全球服務，不需每個 Region 建立使用者。 |
| Create global permissions so users can access resources from all around the world／建立全域權限使使用者可存取全球資源 | ❌ 錯誤 | 不應為了地理移動而建立過寬權限。 |
| There is nothing to do, AWS IAM is a global service／無需任何操作，AWS IAM 是全球服務 | ✅ 正確 | IAM 使用者與權限本身不綁定 Region。 |

---

## 問題 32

**題目**
Which AWS service can inspect Amazon CloudFront distributions running on any HTTP web server?
哪個 AWS 服務可以檢查在任何 HTTP Web 伺服器上執行的 Amazon CloudFront 發佈？

**[選項]**
- A. AWS GuardDuty
- B. Amazon Inspector
- C. Elastic Load Balancing (ELB)
- D. AWS Web Application Firewall (AWS WAF)

**正確答案**
AWS Web Application Firewall (AWS WAF)

**為什麼正確**
**AWS WAF** 可保護 CloudFront 發佈、ALB、API Gateway 等 Web 流量，檢查 HTTP/HTTPS 請求並依規則允許、封鎖或計數。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS GuardDuty | ❌ 錯誤 | GuardDuty 偵測帳戶與工作負載威脅，不檢查 CloudFront HTTP 請求規則。 |
| Amazon Inspector | ❌ 錯誤 | Inspector 做漏洞評估，不是 Web 應用防火牆。 |
| Elastic Load Balancing (ELB) | ❌ 錯誤 | ELB 分配流量，不提供 CloudFront WAF 規則檢查。 |
| AWS Web Application Firewall (AWS WAF) | ✅ 正確 | WAF 可搭配 CloudFront 檢查和過濾 Web 請求。 |

---

## 問題 33

**題目**
According to the AWS Well-Architected Framework, which of the following action is recommended in the Security pillar?
根據 AWS Well-Architected Framework，以下哪項行動是安全支柱的建議？

**[選項]**
- A. Use AWS Cost Explorer to view and track your usage in detail／使用 AWS Cost Explorer 詳細檢視和追蹤使用情況
- B. Use AWS CloudFormation to automate security best practices／使用 AWS CloudFormation 自動化安全最佳實務
- C. Use Amazon CloudWatch to measure overall efficiency／使用 Amazon CloudWatch 衡量整體效率
- D. Use AWS Key Management Service (AWS KMS) to encrypt data／使用 AWS KMS 加密資料

**正確答案**
Use AWS Key Management Service (AWS KMS) to encrypt data／使用 AWS KMS 加密資料

**為什麼正確**
AWS Well-Architected 的安全支柱強調保護資料、管理身分與偵測安全事件。使用 **AWS KMS** 加密資料符合資料保護的安全最佳實務。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Use AWS Cost Explorer to view and track your usage in detail／使用 AWS Cost Explorer 詳細檢視和追蹤使用情況 | ❌ 錯誤 | Cost Explorer 屬於成本管理與成本最佳化。 |
| Use AWS CloudFormation to automate security best practices／使用 AWS CloudFormation 自動化安全最佳實務 | ❌ 錯誤 | CloudFormation 是 IaC 工具，本選項不如 KMS 加密資料直接對應安全支柱。 |
| Use Amazon CloudWatch to measure overall efficiency／使用 Amazon CloudWatch 衡量整體效率 | ❌ 錯誤 | CloudWatch 主要是監控與營運觀測。 |
| Use AWS Key Management Service (AWS KMS) to encrypt data／使用 AWS KMS 加密資料 | ✅ 正確 | KMS 加密資料是安全支柱中的資料保護作法。 |

---

## 問題 34

**題目**
A research lab needs to be notified in case of a configuration change for security and compliance reasons. Which AWS service can assist with this task?
一個研究實驗室需要在設定變更時收到通知以符合安全和合規要求。哪個 AWS 服務可以協助完成此任務？

**[選項]**
- A. AWS Trusted Advisor
- B. AWS Secrets Manager
- C. Amazon Inspector
- D. AWS Config

**正確答案**
AWS Config

**為什麼正確**
**AWS Config** 可持續記錄 AWS 資源設定與變更歷史，並可針對設定變更進行評估與通知，適合安全與合規稽核。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Trusted Advisor | ❌ 錯誤 | Trusted Advisor 提供最佳實務建議，不是設定變更追蹤系統。 |
| AWS Secrets Manager | ❌ 錯誤 | Secrets Manager 管理機密，不追蹤所有資源設定變更。 |
| Amazon Inspector | ❌ 錯誤 | Inspector 做漏洞評估，不記錄設定變更。 |
| AWS Config | ✅ 正確 | Config 可追蹤資源設定變更並支援合規檢查。 |

---

## 問題 35

**題目**
Which Amazon EC2 Auto Scaling feature can help with fault tolerance?
哪個 Amazon EC2 Auto Scaling 功能可以幫助提升容錯能力？

**[選項]**
- A. Distributing load to Amazon EC2 instances／將負載分配至 EC2 執行個體
- B. Lower cost by adjusting the number of EC2 instances／透過調整 EC2 執行個體數量降低成本
- C. Having the right amount of computing capacity／擁有適當的運算容量
- D. Replacing unhealthy Amazon EC2 instances／替換不健康的 EC2 執行個體

**正確答案**
Replacing unhealthy Amazon EC2 instances／替換不健康的 EC2 執行個體

**為什麼正確**
EC2 Auto Scaling 可監控執行個體健康狀態，當執行個體不健康時自動終止並啟動替代執行個體，有助於維持容錯能力。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Distributing load to Amazon EC2 instances／將負載分配至 EC2 執行個體 | ❌ 錯誤 | 分配流量是 ELB 的功能，不是 Auto Scaling 的核心容錯功能。 |
| Lower cost by adjusting the number of EC2 instances／透過調整 EC2 執行個體數量降低成本 | ❌ 錯誤 | 這是成本最佳化效果，不是容錯重點。 |
| Having the right amount of computing capacity／擁有適當的運算容量 | ❌ 錯誤 | 這是容量管理與可用性，不是本題問的容錯功能。 |
| Replacing unhealthy Amazon EC2 instances／替換不健康的 EC2 執行個體 | ✅ 正確 | 自動替換不健康執行個體可提升容錯。 |

---

## 問題 36

**題目**
An engineering team is new to the AWS Cloud and it would like to launch a dev/test environment with low monthly pricing. Which AWS service can address this use case?
一個工程團隊是 AWS 雲端新手，希望以低月費啟動開發/測試環境。哪個 AWS 服務可以滿足此使用案例？

**[選項]**
- A. Amazon EC2
- B. AWS CloudFormation
- C. Amazon Elastic Container Service (Amazon ECS)
- D. Amazon LightSail

**正確答案**
Amazon LightSail

**為什麼正確**
**Amazon Lightsail** 提供簡化的 VPS、固定月費、預先包裝的運算、儲存、網路與 DNS 功能，適合新手或簡單 dev/test 環境。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon EC2 | ❌ 錯誤 | EC2 彈性高但設定較多，對新手低月費 dev/test 不是最簡單選擇。 |
| AWS CloudFormation | ❌ 錯誤 | CloudFormation 是 IaC 佈建工具，不是低月費開發環境服務。 |
| Amazon Elastic Container Service (Amazon ECS) | ❌ 錯誤 | ECS 是容器編排服務，對此新手情境較複雜。 |
| Amazon LightSail | ✅ 正確 | Lightsail 以簡單、低且可預測的月費啟動環境。 |

---

## 問題 37

**題目**
A company would like to define a set of rules to manage objects cost-effectively between Amazon S3 storage classes. Which Amazon S3 feature would you use?
一家公司希望定義一組規則，在 Amazon S3 儲存類別之間有效管理物件成本。您會使用哪個 Amazon S3 功能？

**[選項]**
- A. Amazon S3 Transfer Acceleration (Amazon S3TA)
- B. Amazon S3 Bucket policies／S3 儲存貯體政策
- C. S3 Cross-Region Replication (S3 CRR)／S3 跨區域複寫
- D. Amazon S3 Lifecycle configuration／Amazon S3 生命週期設定

**正確答案**
Amazon S3 Lifecycle configuration／Amazon S3 生命週期設定

**為什麼正確**
**S3 Lifecycle configuration** 可定義規則，依物件年齡或條件自動轉換到較低成本儲存類別，或在到期時刪除物件。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3 Transfer Acceleration (Amazon S3TA) | ❌ 錯誤 | S3TA 加速長距離上傳下載，不管理儲存類別成本。 |
| Amazon S3 Bucket policies／S3 儲存貯體政策 | ❌ 錯誤 | Bucket policy 控制存取權限，不做儲存類別轉換。 |
| S3 Cross-Region Replication (S3 CRR)／S3 跨區域複寫 | ❌ 錯誤 | CRR 跨 Region 複製物件，不是生命週期成本管理。 |
| Amazon S3 Lifecycle configuration／Amazon S3 生命週期設定 | ✅ 正確 | Lifecycle 可自動轉移或刪除物件以控制成本。 |

---

## 問題 38

**題目**
A company using a hybrid cloud would like to store secondary backup copies of the on-premises data. Which Amazon S3 Storage Class would you use for a cost-optimal yet rapid access solution?
一家使用混合雲的公司希望儲存本地資料的次要備份副本。哪個 Amazon S3 儲存類別提供最佳成本且能快速存取？

**[選項]**
- A. Amazon S3 Standard
- B. Amazon S3 Standard-Infrequent Access (S3 Standard-IA)
- C. Amazon S3 Glacier Deep Archive
- D. Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)

**正確答案**
Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)

**為什麼正確**
**S3 One Zone-IA** 成本低於 Standard-IA，仍提供毫秒級快速存取。因題目是本地資料的次要備份副本，可接受單一 AZ 儲存的較低可用性。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3 Standard | ❌ 錯誤 | S3 Standard 適合頻繁存取，但成本較高。 |
| Amazon S3 Standard-Infrequent Access (S3 Standard-IA) | ❌ 錯誤 | Standard-IA 多 AZ 儲存，較 One Zone-IA 貴。 |
| Amazon S3 Glacier Deep Archive | ❌ 錯誤 | Deep Archive 成本低但取回慢，不符合快速存取。 |
| Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA) | ✅ 正確 | One Zone-IA 適合可重建的次要備份且需要快速存取。 |

---

## 問題 39

**題目**
Which of the following statements is CORRECT regarding the scope of an Amazon Virtual Private Cloud (VPC)?
以下哪項陳述對 Amazon VPC 的範圍描述正確？

**[選項]**
- A. A VPC spans all AWS regions within an Availability Zone (AZ)／VPC 跨越一個 AZ 內的所有 AWS 區域
- B. A VPC spans all Availability Zones (AZs) in all AWS regions／VPC 跨越所有 AWS 區域的所有 AZ
- C. Amazon VPC spans all subnets in all AWS regions／Amazon VPC 跨越所有 AWS 區域的所有子網路
- D. A VPC spans all Availability Zones (AZs) within an AWS region／VPC 跨越一個 AWS 區域內的所有可用區域

**正確答案**
A VPC spans all Availability Zones (AZs) within an AWS region／VPC 跨越一個 AWS 區域內的所有可用區域

**為什麼正確**
Amazon VPC 是 Region 範圍的資源，可橫跨同一 AWS Region 內的多個 AZ；Subnet 則只位於單一 AZ。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| A VPC spans all AWS regions within an Availability Zone (AZ)／VPC 跨越一個 AZ 內的所有 AWS 區域 | ❌ 錯誤 | AZ 屬於 Region 內部，這個說法邏輯錯誤。 |
| A VPC spans all Availability Zones (AZs) in all AWS regions／VPC 跨越所有 AWS 區域的所有 AZ | ❌ 錯誤 | VPC 不會跨所有 Region。 |
| Amazon VPC spans all subnets in all AWS regions／Amazon VPC 跨越所有 AWS 區域的所有子網路 | ❌ 錯誤 | VPC 只在單一 Region 內，不跨所有 Region。 |
| A VPC spans all Availability Zones (AZs) within an AWS region／VPC 跨越一個 AWS 區域內的所有可用區域 | ✅ 正確 | VPC 是 Region 範圍，可跨該 Region 的 AZ。 |

---

## 問題 40

**題目**
Which service/tool will you use to create and provide trusted users with temporary security credentials that can control access to your AWS resources?
您會使用哪個服務/工具來建立並提供受信任使用者臨時安全憑證，以控制對 AWS 資源的存取？

**[選項]**
- A. Amazon Cognito
- B. AWS Web Application Firewall (AWS WAF)
- C. AWS IAM Identity Center
- D. AWS Security Token Service (AWS STS)

**正確答案**
AWS Security Token Service (AWS STS)

**為什麼正確**
**AWS STS** 可簽發短期、臨時安全憑證，讓受信任使用者或角色在有限時間內存取 AWS 資源。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Cognito | ❌ 錯誤 | Cognito 管理應用程式使用者身分，底層可搭配臨時憑證，但題目直接問建立臨時安全憑證的是 STS。 |
| AWS Web Application Firewall (AWS WAF) | ❌ 錯誤 | WAF 保護 Web 應用，不提供安全憑證。 |
| AWS IAM Identity Center | ❌ 錯誤 | IAM Identity Center 管理多帳戶 SSO，不是發行臨時憑證的核心服務。 |
| AWS Security Token Service (AWS STS) | ✅ 正確 | STS 用於建立和提供臨時安全憑證。 |

---

## 問題 41

**題目**
Which of the following statements is INCORRECT regarding Amazon EBS Elastic Volumes?
以下哪項關於 Amazon EBS 彈性磁碟區的陳述是錯誤的？

**[選項]**
- A. Amazon EBS Elastic Volumes are bound to a specific AZ／EBS 彈性磁碟區綁定至特定 AZ
- B. Amazon EBS Elastic Volumes can be mounted to one instance at a time／EBS 彈性磁碟區一次只能掛載至一個執行個體
- C. Amazon EBS Elastic Volumes can persist data after their termination／EBS 彈性磁碟區可在終止後保留資料
- D. Amazon EBS Elastic Volumes can be bound to several Availability Zones (AZs)／EBS 彈性磁碟區可綁定至多個 AZ（此陳述錯誤）

**正確答案**
Amazon EBS Elastic Volumes can be bound to several Availability Zones (AZs)／EBS 彈性磁碟區可綁定至多個 AZ（此陳述錯誤）

**為什麼正確**
EBS Volume 是 AZ 範圍資源，必須位於特定 AZ，不能同時綁定多個 AZ。因此「可綁定至多個 AZ」是錯誤陳述。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon EBS Elastic Volumes are bound to a specific AZ／EBS 彈性磁碟區綁定至特定 AZ | ❌ 錯誤 | 這是正確陳述，不是本題要找的錯誤說法。 |
| Amazon EBS Elastic Volumes can be mounted to one instance at a time／EBS 彈性磁碟區一次只能掛載至一個執行個體 | ❌ 錯誤 | CCP 考試層級通常視為正確特性。 |
| Amazon EBS Elastic Volumes can persist data after their termination／EBS 彈性磁碟區可在終止後保留資料 | ❌ 錯誤 | EBS 可獨立於 EC2 保留資料，這是正確陳述。 |
| Amazon EBS Elastic Volumes can be bound to several Availability Zones (AZs)／EBS 彈性磁碟區可綁定至多個 AZ（此陳述錯誤） | ✅ 正確 | 這是錯誤陳述，EBS Volume 不能跨多個 AZ。 |

---

## 問題 42

**題目**
A university's IT infrastructure is experiencing a read-intensive workload. Which AWS service would you use to take the load off databases?
一所大學的 IT 基礎設施遭遇讀取密集型工作負載。您會使用哪個 AWS 服務來減輕資料庫的負擔？

**[選項]**
- A. AWS Glue
- B. Amazon RDS
- C. Amazon EMR
- D. Amazon ElastiCache

**正確答案**
Amazon ElastiCache

**為什麼正確**
**Amazon ElastiCache** 是受管記憶體快取服務，可將常用讀取資料放在 Redis 或 Memcached 快取中，減少資料庫讀取壓力。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Glue | ❌ 錯誤 | Glue 是 ETL 服務，不用來替資料庫承擔即時讀取流量。 |
| Amazon RDS | ❌ 錯誤 | RDS 是關聯式資料庫服務本身，不是快取層。 |
| Amazon EMR | ❌ 錯誤 | EMR 是大數據處理叢集，不是資料庫讀取快取。 |
| Amazon ElastiCache | ✅ 正確 | ElastiCache 可快取熱資料，降低資料庫讀取負載。 |

---

## 問題 43

**題目**
A start-up would like to monitor its cost on the AWS Cloud and would like to choose an optimal Savings Plan. Which AWS service would you use?
一家新創公司希望監控 AWS 雲端成本並選擇最佳 Savings Plan。您會使用哪個 AWS 服務？

**[選項]**
- A. AWS Budgets
- B. AWS Pricing Calculator
- C. AWS Cost & Usage Report (AWS CUR)
- D. AWS Cost Explorer

**正確答案**
AWS Cost Explorer

**為什麼正確**
**AWS Cost Explorer** 可視覺化分析成本與用量，並提供 Savings Plans 建議，協助選擇適合的承諾方案。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Budgets | ❌ 錯誤 | Budgets 用於設定預算與告警，不主要用來選 Savings Plan。 |
| AWS Pricing Calculator | ❌ 錯誤 | Pricing Calculator 用於事前估算，不分析實際用量與 Savings Plan 建議。 |
| AWS Cost & Usage Report (AWS CUR) | ❌ 錯誤 | CUR 提供最詳細成本資料，但不是最直接的 Savings Plan 建議工具。 |
| AWS Cost Explorer | ✅ 正確 | Cost Explorer 可監控成本並提供 Savings Plans 建議。 |

---

## 問題 44

**題目**
Which of the following AWS IAM Security Tools allows you to review permissions granted to an IAM user?
以下哪個 AWS IAM 安全工具可讓您審查授予 IAM 使用者的權限？

**[選項]**
- A. IAM policy／IAM 政策
- B. Multi-Factor Authentication (MFA)／多重要素驗證
- C. IAM credentials report／IAM 憑證報告
- D. AWS IAM access advisor／AWS IAM 存取顧問

**正確答案**
AWS IAM access advisor／AWS IAM 存取顧問

**為什麼正確**
**IAM Access Advisor** 顯示授予 IAM 使用者或角色的服務權限，以及這些服務最後一次被存取的時間，可用於審查與收斂權限。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| IAM policy／IAM 政策 | ❌ 錯誤 | IAM policy 是權限定義，不是審查使用狀況的工具。 |
| Multi-Factor Authentication (MFA)／多重要素驗證 | ❌ 錯誤 | MFA 強化登入安全，不用來審查已授予權限。 |
| IAM credentials report／IAM 憑證報告 | ❌ 錯誤 | Credentials report 檢視密碼、存取金鑰、MFA 等憑證狀態。 |
| AWS IAM access advisor／AWS IAM 存取顧問 | ✅ 正確 | Access Advisor 可審查服務權限與最後存取時間。 |

---

## 問題 45

**題目**
Which AWS tool can provide best practice recommendations for performance, service limits, and cost optimization?
哪個 AWS 工具可以提供效能、服務限制和成本優化的最佳實務建議？

**[選項]**
- A. Amazon Inspector
- B. Amazon CloudWatch
- C. AWS Health Dashboard - Service health
- D. AWS Trusted Advisor

**正確答案**
AWS Trusted Advisor

**為什麼正確**
**AWS Trusted Advisor** 會依照 AWS 最佳實務檢查帳戶，提供成本最佳化、效能、服務限制、安全與容錯等建議。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Inspector | ❌ 錯誤 | Inspector 著重漏洞與安全評估。 |
| Amazon CloudWatch | ❌ 錯誤 | CloudWatch 監控指標與日誌，不提供整體最佳實務建議。 |
| AWS Health Dashboard - Service health | ❌ 錯誤 | Service Health 顯示 AWS 服務狀態，不分析成本或效能最佳化。 |
| AWS Trusted Advisor | ✅ 正確 | Trusted Advisor 提供效能、限制與成本最佳化等建議。 |

---

## 問題 46

**題目**
An engineering team would like to cost-effectively run hundreds of thousands of batch computing workloads on AWS. Which AWS service would you use for this task?
一個工程團隊希望在 AWS 上以具成本效益的方式執行數十萬個批次運算工作負載。您會使用哪個 AWS 服務？

**[選項]**
- A. Amazon Lightsail
- B. AWS Lambda
- C. AWS Fargate
- D. AWS Batch

**正確答案**
AWS Batch

**為什麼正確**
**AWS Batch** 是全受管批次運算服務，可依工作需求動態佈建合適運算資源，適合大規模且具成本效益地執行大量批次工作。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Lightsail | ❌ 錯誤 | Lightsail 是簡化 VPS，不適合數十萬批次工作。 |
| AWS Lambda | ❌ 錯誤 | Lambda 可跑短時間事件驅動工作，但有執行時間與資源限制。 |
| AWS Fargate | ❌ 錯誤 | Fargate 執行容器，不是專門的批次工作排程與資源最佳化服務。 |
| AWS Batch | ✅ 正確 | AWS Batch 專為大規模批次運算工作負載設計。 |

---

## 問題 47

**題目**
A company would like to optimize Amazon EC2 costs. Which of the following actions can help with this task? (Select TWO)
一家公司希望優化 Amazon EC2 成本。以下哪些行動可以幫助實現此目標？（選兩項）

**[選項]**
- A. Opt for a higher AWS Support plan／選擇更高的 AWS Support 方案
- B. Vertically scale the EC2 instances／垂直擴展 EC2 執行個體
- C. Build its own servers／自建伺服器
- D. Set up Auto Scaling groups to align the number of instances with the demand／設定 Auto Scaling 群組以使執行個體數量符合需求
- E. Purchase Amazon EC2 Reserved instances (RIs)／購買 Amazon EC2 保留執行個體

**正確答案**
Set up Auto Scaling groups to align the number of instances with the demand／設定 Auto Scaling 群組以使執行個體數量符合需求；Purchase Amazon EC2 Reserved instances (RIs)／購買 Amazon EC2 保留執行個體

**為什麼正確**
Auto Scaling 可讓執行個體數量隨需求調整，避免過度佈建；Reserved Instances 則適合長期穩定用量，可用承諾換取折扣。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Opt for a higher AWS Support plan／選擇更高的 AWS Support 方案 | ❌ 錯誤 | 支援方案升級通常增加成本，不能直接最佳化 EC2 費用。 |
| Vertically scale the EC2 instances／垂直擴展 EC2 執行個體 | ❌ 錯誤 | 垂直擴展可能提高規格與成本，不是成本最佳化的典型答案。 |
| Build its own servers／自建伺服器 | ❌ 錯誤 | 自建伺服器違背雲端彈性與成本最佳化方向。 |
| Set up Auto Scaling groups to align the number of instances with the demand／設定 Auto Scaling 群組以使執行個體數量符合需求 | ✅ 正確 | Auto Scaling 可避免閒置容量並符合實際需求。 |
| Purchase Amazon EC2 Reserved instances (RIs)／購買 Amazon EC2 保留執行個體 | ✅ 正確 | RI 適合穩定工作負載，可降低 EC2 成本。 |

---

## 問題 48

**題目**
An enterprise is planning to move one of its older applications from its local data center to AWS. The IT team wants the fastest migration path and has decided not to update the application code or make any architectural changes. Which migration strategy is the most appropriate?
一家企業計劃將一個舊應用程式從本地資料中心遷移至 AWS。IT 團隊希望最快的遷移路徑，並決定不更新應用程式程式碼或進行任何架構變更。哪種遷移策略最合適？

**[選項]**
- A. Repurchase／重新購買
- B. Replatform／重新平台化
- C. Refactor／重構
- D. Rehost／重新託管（Lift and Shift）

**正確答案**
Rehost／重新託管（Lift and Shift）

**為什麼正確**
**Rehost** 又稱 Lift and Shift，是將應用程式直接搬到雲端，通常不修改程式碼或架構，因此是最快的遷移方式。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Repurchase／重新購買 | ❌ 錯誤 | Repurchase 是改用新的 SaaS 或產品，通常需要流程變更。 |
| Replatform／重新平台化 | ❌ 錯誤 | Replatform 會做少量平台調整，不是完全不改。 |
| Refactor／重構 | ❌ 錯誤 | Refactor 需要重新設計或修改程式碼，最耗時。 |
| Rehost／重新託管（Lift and Shift） | ✅ 正確 | Rehost 不改程式碼或架構，適合最快搬遷。 |

---

## 問題 49

**題目**
A company based in Sydney hosts its application on an EC2 instance in ap-southeast-2. They would like to deploy the same EC2 instances in eu-south-1. Which AWS entity can address this use case?
一家位於雪梨的公司在 ap-southeast-2 的 EC2 執行個體上託管其應用程式。他們希望在 eu-south-1 部署相同的 EC2 執行個體。哪個 AWS 實體可以解決此使用案例？

**[選項]**
- A. Elastic Load Balancing (ELB)
- B. AWS Lambda
- C. Amazon EBS Elastic Volume snapshots
- D. Amazon Machine Image (AMI)

**正確答案**
Amazon Machine Image (AMI)

**為什麼正確**
**AMI** 包含啟動 EC2 執行個體所需的作業系統、應用程式與設定。可將 AMI 複製到另一個 Region，再用它啟動相同配置的 EC2。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Elastic Load Balancing (ELB) | ❌ 錯誤 | ELB 分配流量，不複製 EC2 配置到其他 Region。 |
| AWS Lambda | ❌ 錯誤 | Lambda 是無伺服器運算，不是 EC2 映像。 |
| Amazon EBS Elastic Volume snapshots | ❌ 錯誤 | EBS 快照備份磁碟資料，但完整 EC2 啟動範本應使用 AMI。 |
| Amazon Machine Image (AMI) | ✅ 正確 | AMI 可用來在其他 Region 部署相同 EC2 執行個體。 |

---

## 問題 50

**題目**
Which of the following are the best practices when using AWS Organizations? (Select TWO)
以下哪些是使用 AWS Organizations 的最佳實務？（選兩項）

**[選項]**
- A. Disable AWS CloudTrail on several accounts／在部分帳戶上停用 AWS CloudTrail
- B. Never use tags for billing／從不使用標籤進行計費
- C. Do not use AWS Organizations to automate AWS account creation／不使用 AWS Organizations 自動建立 AWS 帳戶
- D. Restrict account privileges using Service Control Policies (SCP)／使用 SCP 限制帳戶權限
- E. Create AWS accounts per department／按部門建立 AWS 帳戶

**正確答案**
Restrict account privileges using Service Control Policies (SCP)／使用 SCP 限制帳戶權限；Create AWS accounts per department／按部門建立 AWS 帳戶

**為什麼正確**
AWS Organizations 的最佳實務包含用 SCP 建立治理護欄，並依部門、工作負載或環境拆分帳戶以提升隔離、治理與成本管理。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Disable AWS CloudTrail on several accounts／在部分帳戶上停用 AWS CloudTrail | ❌ 錯誤 | 停用 CloudTrail 會降低稽核與安全可見性。 |
| Never use tags for billing／從不使用標籤進行計費 | ❌ 錯誤 | 成本分配標籤是計費管理最佳實務之一。 |
| Do not use AWS Organizations to automate AWS account creation／不使用 AWS Organizations 自動建立 AWS 帳戶 | ❌ 錯誤 | 自動化帳戶建立與治理是 Organizations 的常見用途。 |
| Restrict account privileges using Service Control Policies (SCP)／使用 SCP 限制帳戶權限 | ✅ 正確 | SCP 可集中限制成員帳戶可用的服務與動作。 |
| Create AWS accounts per department／按部門建立 AWS 帳戶 | ✅ 正確 | 依部門拆分帳戶有助於隔離、治理與成本追蹤。 |

---

## 問題 51

**題目**
Which of the following are the advantages of using the AWS Cloud? (Select TWO)
以下哪些是使用 AWS 雲端的優勢？（選兩項）

**[選項]**
- A. Limited scaling／有限的擴展性
- B. AWS is responsible for security in the cloud／AWS 負責雲端中的安全
- C. Trade operational expense for capital expense／以資本支出換取營運支出
- D. Stop guessing about capacity／停止猜測容量需求
- E. Increase speed and agility／提升速度和敏捷性

**正確答案**
Stop guessing about capacity／停止猜測容量需求；Increase speed and agility／提升速度和敏捷性

**為什麼正確**
AWS 雲端的優勢包含避免事前猜測容量，並能快速佈建資源，提高創新速度與敏捷性。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Limited scaling／有限的擴展性 | ❌ 錯誤 | 雲端優勢是彈性擴展，不是有限擴展。 |
| AWS is responsible for security in the cloud／AWS 負責雲端中的安全 | ❌ 錯誤 | AWS 負責雲端本身的安全，客戶負責雲端中的安全。 |
| Trade operational expense for capital expense／以資本支出換取營運支出 | ❌ 錯誤 | 正確概念是以營運支出取代大量前期資本支出。 |
| Stop guessing about capacity／停止猜測容量需求 | ✅ 正確 | 雲端可依需求調整容量，降低容量預估風險。 |
| Increase speed and agility／提升速度和敏捷性 | ✅ 正確 | AWS 可快速取得資源，加速實驗與交付。 |

---

## 問題 52

**題目**
Which of the following options are the benefits of using AWS Elastic Load Balancing (ELB)? (Select TWO)
以下哪些是使用 AWS Elastic Load Balancing（ELB）的優點？（選兩項）

**[選項]**
- A. Less costly／成本較低
- B. Storage／儲存
- C. Agility／敏捷性
- D. Fault tolerance／容錯能力
- E. High availability／高可用性

**正確答案**
Fault tolerance／容錯能力；High availability／高可用性

**為什麼正確**
**Elastic Load Balancing** 可將流量分散到多個目標與多個 AZ，避免單一節點故障造成服務中斷，因此提升高可用性與容錯能力。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Less costly／成本較低 | ❌ 錯誤 | ELB 本身會產生成本，不是主要考點。 |
| Storage／儲存 | ❌ 錯誤 | ELB 不提供儲存功能。 |
| Agility／敏捷性 | ❌ 錯誤 | 敏捷性是雲端整體優勢，不是 ELB 的核心功能。 |
| Fault tolerance／容錯能力 | ✅ 正確 | ELB 可避開不健康目標，提升容錯。 |
| High availability／高可用性 | ✅ 正確 | ELB 跨目標分配流量，提高可用性。 |

---

## 問題 53

**題目**
A company would like to create a private, high bandwidth network connection between its on-premises data centers and AWS Cloud. Which option would you recommend?
一家公司希望在其本地資料中心與 AWS 雲端之間建立私有、高頻寬的網路連線。您會推薦哪個選項？

**[選項]**
- A. AWS Site-to-Site VPN
- B. VPC Endpoints／VPC 端點
- C. VPC peering connection／VPC 對等連線
- D. AWS Direct Connect

**正確答案**
AWS Direct Connect

**為什麼正確**
**AWS Direct Connect** 提供從本地資料中心到 AWS 的專用私有網路連線，適合需要高頻寬、低延遲與穩定連線的混合雲場景。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Site-to-Site VPN | ❌ 錯誤 | VPN 透過公網加密連線，通常不如 Direct Connect 高頻寬與穩定。 |
| VPC Endpoints／VPC 端點 | ❌ 錯誤 | VPC Endpoint 用於私有存取 AWS 服務，不連接本地資料中心。 |
| VPC peering connection／VPC 對等連線 | ❌ 錯誤 | VPC Peering 連接 VPC 與 VPC，不是本地資料中心到 AWS。 |
| AWS Direct Connect | ✅ 正確 | Direct Connect 是私有高頻寬連線的最佳選項。 |

---

## 問題 54

**題目**
A Cloud Practitioner would like to deploy identical resources across all AWS regions and accounts using templates while estimating costs. Which AWS service can assist with this task?
一位 Cloud Practitioner 希望使用範本在所有 AWS 區域和帳戶中部署相同資源，同時估算成本。哪個 AWS 服務可以協助完成此任務？

**[選項]**
- A. Amazon LightSail
- B. AWS Directory Service for Microsoft Active Directory
- C. AWS CodeDeploy
- D. AWS CloudFormation

**正確答案**
AWS CloudFormation

**為什麼正確**
**AWS CloudFormation** 使用範本定義與佈建基礎設施，可搭配 StackSets 跨帳戶與跨 Region 部署，並可在建立前估算資源成本。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon LightSail | ❌ 錯誤 | Lightsail 是簡化 VPS 服務，不用範本跨帳戶部署整套基礎設施。 |
| AWS Directory Service for Microsoft Active Directory | ❌ 錯誤 | Directory Service 提供目錄服務，不是 IaC 佈建工具。 |
| AWS CodeDeploy | ❌ 錯誤 | CodeDeploy 部署應用程式程式碼，不佈建基礎設施範本。 |
| AWS CloudFormation | ✅ 正確 | CloudFormation 可用範本部署資源並支援成本估算。 |

---

## 問題 55

**題目**
According to the AWS Shared Responsibility Model, which of the following is the responsibility of the customer?
根據 AWS 共同責任模型，以下哪項是客戶的責任？

**[選項]**
- A. Protecting hardware infrastructure／保護硬體基礎設施
- B. Edge locations security／邊緣位置安全
- C. Managing Amazon DynamoDB／管理 Amazon DynamoDB
- D. Firewall & networking configuration of Amazon EC2／Amazon EC2 的防火牆和網路設定

**正確答案**
Firewall & networking configuration of Amazon EC2／Amazon EC2 的防火牆和網路設定

**為什麼正確**
在 EC2 這類 IaaS 服務中，客戶負責安全群組、網路 ACL、作業系統與應用程式等設定；AWS 負責底層基礎設施。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Protecting hardware infrastructure／保護硬體基礎設施 | ❌ 錯誤 | 硬體基礎設施由 AWS 保護。 |
| Edge locations security／邊緣位置安全 | ❌ 錯誤 | 邊緣節點的實體安全是 AWS 責任。 |
| Managing Amazon DynamoDB／管理 Amazon DynamoDB | ❌ 錯誤 | DynamoDB 是受管服務，AWS 負責底層管理。 |
| Firewall & networking configuration of Amazon EC2／Amazon EC2 的防火牆和網路設定 | ✅ 正確 | EC2 的安全群組與網路設定由客戶管理。 |

---

## 問題 56

**題目**
Which types of monitoring can be provided by Amazon CloudWatch? (Select TWO)
Amazon CloudWatch 可以提供哪些類型的監控？（選兩項）

**[選項]**
- A. API access／API 存取
- B. Performance and availability of AWS services／AWS 服務的效能和可用性
- C. Account management／帳戶管理
- D. Application performance／應用程式效能
- E. Resource utilization／資源使用率

**正確答案**
Application performance／應用程式效能；Resource utilization／資源使用率

**為什麼正確**
**Amazon CloudWatch** 收集指標、日誌與事件，可監控 AWS 資源使用率與應用程式效能，並可設定警示。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| API access／API 存取 | ❌ 錯誤 | API 呼叫稽核主要由 AWS CloudTrail 記錄。 |
| Performance and availability of AWS services／AWS 服務的效能和可用性 | ❌ 錯誤 | AWS 服務整體健康狀態由 AWS Health Dashboard 提供。 |
| Account management／帳戶管理 | ❌ 錯誤 | 帳戶與身分管理不是 CloudWatch 的監控類型。 |
| Application performance／應用程式效能 | ✅ 正確 | CloudWatch 可透過指標與日誌監控應用程式效能。 |
| Resource utilization／資源使用率 | ✅ 正確 | CloudWatch 可監控 CPU、網路、磁碟等資源使用率。 |

---

## 問題 57

**題目**
A company would like to audit requests made to an Amazon S3 bucket. Which Amazon S3 feature would you recommend?
一家公司希望稽核對 Amazon S3 儲存貯體發出的請求。您會推薦哪個 Amazon S3 功能？

**[選項]**
- A. Amazon S3 Bucket Policies／S3 儲存貯體政策
- B. S3 Versioning／S3 版本控制
- C. S3 Cross-Region Replication (S3 CRR)／S3 跨區域複寫
- D. Amazon S3 Access Logs／Amazon S3 存取日誌

**正確答案**
Amazon S3 Access Logs／Amazon S3 存取日誌

**為什麼正確**
**Amazon S3 Server Access Logging** 可記錄對 S3 bucket 發出的請求細節，適合安全稽核、存取分析與成本理解。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3 Bucket Policies／S3 儲存貯體政策 | ❌ 錯誤 | Bucket policy 控制存取權限，不記錄請求。 |
| S3 Versioning／S3 版本控制 | ❌ 錯誤 | Versioning 保留物件多版本，不稽核請求。 |
| S3 Cross-Region Replication (S3 CRR)／S3 跨區域複寫 | ❌ 錯誤 | CRR 複製物件到其他 Region，不記錄請求稽核。 |
| Amazon S3 Access Logs／Amazon S3 存取日誌 | ✅ 正確 | S3 Access Logs 可記錄 bucket 請求，適合稽核。 |

---

## 問題 58

**題目**
Which AWS service can be used to view the most comprehensive billing details for the past month?
哪個 AWS 服務可用於檢視上個月最全面的帳單詳細資訊？

**[選項]**
- A. AWS Budgets
- B. AWS Pricing Calculator
- C. AWS Cost Explorer
- D. AWS Cost & Usage Report (AWS CUR)

**正確答案**
AWS Cost & Usage Report (AWS CUR)

**為什麼正確**
**AWS Cost & Usage Report** 提供最完整、最細的 AWS 成本與用量資料，可輸出到 S3 並供分析工具查詢。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Budgets | ❌ 錯誤 | Budgets 用於預算與告警，不提供最完整帳單明細。 |
| AWS Pricing Calculator | ❌ 錯誤 | Pricing Calculator 用於預估未來費用，不看過去帳單明細。 |
| AWS Cost Explorer | ❌ 錯誤 | Cost Explorer 提供視覺化成本分析，但不是最完整明細資料來源。 |
| AWS Cost & Usage Report (AWS CUR) | ✅ 正確 | CUR 是最全面的成本與用量報告。 |

---

## 問題 59

**題目**
A start-up would like to quickly deploy a popular technology on AWS. Which AWS tool would you use for this task?
一家新創公司希望在 AWS 上快速部署一項熱門技術。您會使用哪個 AWS 工具？

**[選項]**
- A. AWS Forums
- B. AWS CodeDeploy
- C. AWS Whitepapers
- D. AWS Partner Solutions (formerly Quick Starts)

**正確答案**
AWS Partner Solutions (formerly Quick Starts)

**為什麼正確**
**AWS Partner Solutions**（原 Quick Starts）提供由 AWS 與合作夥伴建立的自動化參考部署，可快速依最佳實務部署常見技術。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Forums | ❌ 錯誤 | Forums 是社群討論與支援資源，不是部署工具。 |
| AWS CodeDeploy | ❌ 錯誤 | CodeDeploy 用於應用程式程式碼部署，不是熱門技術參考部署集合。 |
| AWS Whitepapers | ❌ 錯誤 | Whitepapers 是技術文件，不會自動部署資源。 |
| AWS Partner Solutions (formerly Quick Starts) | ✅ 正確 | Partner Solutions 可快速部署常見技術與參考架構。 |

---

## 問題 60

**題目**
A data science team would like to build Machine Learning models for its projects. Which AWS service can it use?
一個資料科學團隊希望為其專案建立機器學習模型。可以使用哪個 AWS 服務？

**[選項]**
- A. Amazon Comprehend
- B. Amazon Connect
- C. Amazon Polly
- D. Amazon SageMaker

**正確答案**
Amazon SageMaker

**為什麼正確**
**Amazon SageMaker** 是完整的機器學習平台，可建立、訓練、調整與部署 ML 模型，適合資料科學團隊使用。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Comprehend | ❌ 錯誤 | Comprehend 是自然語言處理服務，不是完整 ML 建模平台。 |
| Amazon Connect | ❌ 錯誤 | Connect 是雲端客服中心服務。 |
| Amazon Polly | ❌ 錯誤 | Polly 是文字轉語音服務。 |
| Amazon SageMaker | ✅ 正確 | SageMaker 用於建立、訓練與部署機器學習模型。 |

---

## 問題 61

**題目**
A Cloud Practitioner would like to centrally view, manage, and operate nodes to quickly identify any issues that might impact applications. Which AWS service can help with this task?
一位 Cloud Practitioner 希望集中查看、管理和操作節點，以快速識別可能影響應用程式的問題。哪個 AWS 服務可以幫助完成此任務？

**[選項]**
- A. AWS Trusted Advisor
- B. AWS Health Dashboard - Your Account Health
- C. Amazon Inspector
- D. AWS Systems Manager

**正確答案**
AWS Systems Manager

**為什麼正確**
**AWS Systems Manager** 可集中檢視、管理與操作 EC2、混合雲節點和其他受管節點，支援修補、命令執行、Session Manager 與營運管理。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Trusted Advisor | ❌ 錯誤 | Trusted Advisor 提供最佳實務建議，不集中操作節點。 |
| AWS Health Dashboard - Your Account Health | ❌ 錯誤 | Account Health 顯示帳戶相關 AWS 事件，不管理節點。 |
| Amazon Inspector | ❌ 錯誤 | Inspector 做漏洞掃描，不是節點操作管理中心。 |
| AWS Systems Manager | ✅ 正確 | Systems Manager 可集中管理與操作節點。 |

---

## 問題 62

**題目**
Adding more CPU/RAM to an Amazon EC2 instance represents which of the following?
向 Amazon EC2 執行個體新增更多 CPU/RAM 代表以下哪種情況？

**[選項]**
- A. Horizontal scaling／水平擴展
- B. Managing increasing volumes of data／管理不斷增加的資料量
- C. Loose coupling／鬆耦合
- D. Vertical scaling／垂直擴展

**正確答案**
Vertical scaling／垂直擴展

**為什麼正確**
**Vertical scaling** 指增加單一資源的規格，例如為同一台 EC2 換成更多 CPU 或 RAM 的執行個體類型。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Horizontal scaling／水平擴展 | ❌ 錯誤 | 水平擴展是增加更多執行個體或節點。 |
| Managing increasing volumes of data／管理不斷增加的資料量 | ❌ 錯誤 | 這描述資料管理，不是擴展型態。 |
| Loose coupling／鬆耦合 | ❌ 錯誤 | 鬆耦合是架構設計原則，不是增加 CPU/RAM。 |
| Vertical scaling／垂直擴展 | ✅ 正確 | 增加單一 EC2 的 CPU/RAM 屬於垂直擴展。 |

---

## 問題 63

**題目**
Which of the following statements is the MOST accurate when describing AWS Elastic Beanstalk?
以下哪項陳述對 AWS Elastic Beanstalk 的描述最準確？

**[選項]**
- A. It is a PaaS that allows you to model and provision resources needed for an application／它是一種 PaaS，允許您為應用程式建模和佈建所需資源
- B. It is an IaC that allows you to model and provision resources needed for an application／它是一種 IaC，允許您為應用程式建模和佈建所需資源
- C. It is an IaaS that allows you to deploy and scale web applications and services／它是一種 IaaS，允許您部署和擴展 Web 應用程式和服務
- D. It is a PaaS that allows you to deploy and scale web applications and services／它是一種 PaaS，允許您部署和擴展 Web 應用程式和服務

**正確答案**
It is a PaaS that allows you to deploy and scale web applications and services／它是一種 PaaS，允許您部署和擴展 Web 應用程式和服務

**為什麼正確**
**AWS Elastic Beanstalk** 是 PaaS 型服務，讓開發者上傳程式碼後，由服務協助處理容量佈建、負載平衡、自動擴展與應用程式監控。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| It is a PaaS that allows you to model and provision resources needed for an application／它是一種 PaaS，允許您為應用程式建模和佈建所需資源 | ❌ 錯誤 | 「建模和佈建資源」更接近 CloudFormation，不是 Beanstalk 的最佳描述。 |
| It is an IaC that allows you to model and provision resources needed for an application／它是一種 IaC，允許您為應用程式建模和佈建所需資源 | ❌ 錯誤 | IaC 工具是 CloudFormation/CDK，不是 Elastic Beanstalk。 |
| It is an IaaS that allows you to deploy and scale web applications and services／它是一種 IaaS，允許您部署和擴展 Web 應用程式和服務 | ❌ 錯誤 | Beanstalk 是 PaaS，不是 IaaS。 |
| It is a PaaS that allows you to deploy and scale web applications and services／它是一種 PaaS，允許您部署和擴展 Web 應用程式和服務 | ✅ 正確 | Beanstalk 的定位是部署與擴展 Web 應用程式的 PaaS。 |

---

## 問題 64

**題目**
A brand-new startup would like to remove its need to manage the underlying infrastructure and focus on the deployment and management of its applications. Which type of cloud computing does this refer to?
一家全新的新創公司希望不再需要管理底層基礎設施，專注於應用程式的部署和管理。這是指哪種雲端運算類型？

**[選項]**
- A. On-premises／地端
- B. Infrastructure as a Service (IaaS)／基礎設施即服務
- C. Software as a Service (SaaS)／軟體即服務
- D. Platform as a Service (PaaS)／平台即服務

**正確答案**
Platform as a Service (PaaS)／平台即服務

**為什麼正確**
**PaaS** 讓使用者專注於應用程式部署與管理，而底層基礎設施、作業系統與平台運維由服務提供者處理。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| On-premises／地端 | ❌ 錯誤 | 地端需要自行管理基礎設施。 |
| Infrastructure as a Service (IaaS)／基礎設施即服務 | ❌ 錯誤 | IaaS 仍需要客戶管理 OS、Runtime 與應用等層面。 |
| Software as a Service (SaaS)／軟體即服務 | ❌ 錯誤 | SaaS 是直接使用完整軟體，不是自行部署與管理應用程式。 |
| Platform as a Service (PaaS)／平台即服務 | ✅ 正確 | PaaS 免管底層基礎設施，專注應用程式。 |

---

## 問題 65

**題目**
A company would like to separate cost for AWS services by the department for cost allocation. Which of the following is the simplest way to achieve this task?
一家公司希望按部門分離 AWS 服務成本以進行成本分配。以下哪種方式最簡單？

**[選項]**
- A. Create one account for all departments and share this account／為所有部門建立一個帳戶並共用
- B. Create different VPCs for different departments／為不同部門建立不同的 VPC
- C. Create different accounts for different departments／為不同部門建立不同帳戶
- D. Create tags for each department／為每個部門建立標籤

**正確答案**
Create tags for each department／為每個部門建立標籤

**為什麼正確**
AWS 成本分配標籤可用部門、專案、成本中心等鍵值標記資源，搭配成本報告與成本分析工具按標籤拆分費用，是最簡單的成本分攤方式。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Create one account for all departments and share this account／為所有部門建立一個帳戶並共用 | ❌ 錯誤 | 共用同一帳戶難以精準分攤，也不利安全與稽核。 |
| Create different VPCs for different departments／為不同部門建立不同的 VPC | ❌ 錯誤 | VPC 不是成本分配的主要維度。 |
| Create different accounts for different departments／為不同部門建立不同帳戶 | ❌ 錯誤 | 多帳戶可做成本隔離，但比標籤更複雜，不是最簡單。 |
| Create tags for each department／為每個部門建立標籤 | ✅ 正確 | 以部門標籤標記資源是最簡單的成本分配方法。 |

---

