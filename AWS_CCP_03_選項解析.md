# AWS CCP 03 選項解析

來源：
- 題目與選項：[AWS_CCP_Practice_Test3.md](AWS_CCP_Practice_Test3.md)
- 原詳解：[AWS_CCP_03.md](AWS_CCP_03.md)

這份檔案針對每題列出中英對照題目與選項，並用中文說明正確答案與其他選項的差異。

---

## 問題 1

**題目**
A multi-national company has its business-critical data stored on a fleet of Amazon EC2 instances, in various countries, configured in region-specific compliance rules. To demonstrate compliance, the company needs to submit historical configurations on a regular basis. Which AWS service is best suited for this requirement?
一家跨國公司將業務關鍵資料儲存在各國的 Amazon EC2 執行個體上，並設定了特定區域的合規規則。為了展示合規性，公司需要定期提交歷史設定。哪個 AWS 服務最適合此需求？

**[選項]**
- A. Amazon Macie／敏感資料探索
- B. Amazon GuardDuty／威脅偵測
- C. AWS CloudTrail／活動稽核記錄
- D. AWS Config／資源組態追蹤

**正確答案**
AWS Config／資源組態追蹤

**為什麼正確**
**AWS Config** 會持續記錄 AWS 資源的組態、組態變更歷史與資源關聯，可用來定期提交歷史配置並證明合規狀態。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Macie／敏感資料探索 | ❌ 錯誤 | Macie 用於探索和保護 S3 中的敏感資料，不是資源歷史組態追蹤服務。 |
| Amazon GuardDuty／威脅偵測 | ❌ 錯誤 | GuardDuty 用於偵測惡意活動與威脅，不提供資源配置歷史。 |
| AWS CloudTrail／活動稽核記錄 | ❌ 錯誤 | CloudTrail 記錄 API 活動與帳戶操作，不是提交資源歷史配置的主要服務。 |
| AWS Config／資源組態追蹤 | ✅ 正確 | Config 追蹤資源配置變更與合規狀態，符合題目要求。 |

---

## 問題 2

**題目**
Which AWS service can be used to automate code deployment to Amazon EC2 instances as well as on-premises instances?
哪個 AWS 服務可用於自動化將程式碼部署至 Amazon EC2 執行個體以及本地執行個體？

**[選項]**
- A. AWS CodePipeline／持續交付管道
- B. AWS CloudFormation／基礎設施即程式碼
- C. AWS CodeCommit／原始碼儲存庫
- D. AWS CodeDeploy／程式碼部署服務

**正確答案**
AWS CodeDeploy／程式碼部署服務

**為什麼正確**
**AWS CodeDeploy** 可自動將應用程式部署到 Amazon EC2、AWS Lambda、ECS，以及本地伺服器。題目關鍵字是「部署到 EC2 和 on-premises instances」。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS CodePipeline／持續交付管道 | ❌ 錯誤 | CodePipeline 用於編排整個 CI/CD 流程，本身不是實際執行部署的服務。 |
| AWS CloudFormation／基礎設施即程式碼 | ❌ 錯誤 | CloudFormation 用範本佈建 AWS 資源，不是應用程式碼部署工具。 |
| AWS CodeCommit／原始碼儲存庫 | ❌ 錯誤 | CodeCommit 是受管 Git 儲存庫，用於保存程式碼。 |
| AWS CodeDeploy／程式碼部署服務 | ✅ 正確 | CodeDeploy 可自動部署程式碼到 EC2 與本地執行個體。 |

---

## 問題 3

**題目**
An IT company has a hybrid cloud architecture and it wants to centralize the server logs for its Amazon EC2 instances and on-premises servers. Which of the following is the MOST effective for this use-case?
一家 IT 公司擁有混合雲架構，希望集中管理 Amazon EC2 執行個體和本地伺服器的伺服器日誌。以下哪個最有效？

**[選項]**
- A. Use AWS CloudTrail for the EC2 instance and Amazon CloudWatch Logs for the on-premises servers／EC2 使用 CloudTrail，本地伺服器使用 CloudWatch Logs
- B. Use Amazon CloudWatch Logs for the EC2 instance and AWS CloudTrail for the on-premises servers／EC2 使用 CloudWatch Logs，本地伺服器使用 CloudTrail
- C. Use AWS Lambda to send log data from EC2 instance and on-premises servers to Amazon CloudWatch Logs／使用 Lambda 將日誌送到 CloudWatch Logs
- D. Use Amazon CloudWatch Logs for both the EC2 instance and the on-premises servers／EC2 和本地伺服器都使用 CloudWatch Logs

**正確答案**
Use Amazon CloudWatch Logs for both the EC2 instance and the on-premises servers／EC2 和本地伺服器都使用 CloudWatch Logs

**為什麼正確**
**Amazon CloudWatch Logs** 可集中收集、儲存和查詢 EC2、本地伺服器與應用程式日誌，是混合雲集中化伺服器日誌的直接方案。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Use AWS CloudTrail for the EC2 instance and Amazon CloudWatch Logs for the on-premises servers／EC2 使用 CloudTrail，本地伺服器使用 CloudWatch Logs | ❌ 錯誤 | CloudTrail 記錄 AWS API 活動，不是 EC2 伺服器作業系統或應用日誌。 |
| Use Amazon CloudWatch Logs for the EC2 instance and AWS CloudTrail for the on-premises servers／EC2 使用 CloudWatch Logs，本地伺服器使用 CloudTrail | ❌ 錯誤 | CloudTrail 不適合收集本地伺服器日誌。 |
| Use AWS Lambda to send log data from EC2 instance and on-premises servers to Amazon CloudWatch Logs／使用 Lambda 將日誌送到 CloudWatch Logs | ❌ 錯誤 | Lambda 不是必要的集中日誌代理；直接使用 CloudWatch Logs 更有效。 |
| Use Amazon CloudWatch Logs for both the EC2 instance and the on-premises servers／EC2 和本地伺服器都使用 CloudWatch Logs | ✅ 正確 | CloudWatch Logs 可集中管理 EC2 與本地伺服器日誌。 |

---

## 問題 4

**題目**
A financial services enterprise plans to enable Multi-Factor Authentication (MFA) for its employees. For ease of travel, they prefer not to use any physical devices to implement MFA. Which of the below options is best suited for this use case?
一家金融服務企業計劃為員工啟用 MFA。為了出行方便，他們傾向不使用任何實體裝置來實施 MFA。以下哪個選項最適合此使用案例？

**[選項]**
- A. Hardware Multi-Factor Authentication (MFA) device／硬體 MFA 裝置
- B. U2F security key／U2F 安全金鑰
- C. Soft Token Multi-Factor Authentication (MFA) device／軟體令牌 MFA 裝置
- D. Virtual Multi-Factor Authentication (MFA) device／虛擬 MFA 裝置

**正確答案**
Virtual Multi-Factor Authentication (MFA) device／虛擬 MFA 裝置

**為什麼正確**
**Virtual MFA device** 通常是手機 App 產生一次性驗證碼，不需要攜帶額外的實體硬體裝置，符合「不使用 physical devices」的需求。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Hardware Multi-Factor Authentication (MFA) device／硬體 MFA 裝置 | ❌ 錯誤 | 需要實體硬體裝置，不符合題目需求。 |
| U2F security key／U2F 安全金鑰 | ❌ 錯誤 | U2F 是實體安全金鑰。 |
| Soft Token Multi-Factor Authentication (MFA) device／軟體令牌 MFA 裝置 | ❌ 錯誤 | AWS IAM 的常見正式選項是 Virtual MFA device；此題以其為正確名稱。 |
| Virtual Multi-Factor Authentication (MFA) device／虛擬 MFA 裝置 | ✅ 正確 | 虛擬 MFA 可用手機 App，不需額外實體 MFA 硬體。 |

---

## 問題 5

**題目**
Which of the following AWS services offer block-level storage? (Select two)
以下哪些 AWS 服務提供區塊層級儲存？（選兩項）

**[選項]**
- A. Amazon Simple Storage Service (Amazon S3)／物件儲存
- B. Amazon Elastic File System (Amazon EFS)／檔案儲存
- C. Amazon Elastic Container Service (Amazon ECS)／容器服務
- D. Instance Store／執行個體存放區
- E. Amazon Elastic Block Store (Amazon EBS)／彈性區塊儲存

**正確答案**
Instance Store／執行個體存放區；Amazon Elastic Block Store (Amazon EBS)／彈性區塊儲存

**為什麼正確**
**Amazon EBS** 是持久性區塊儲存；**Instance Store** 是直接附加在 EC2 主機上的暫時性區塊儲存。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Simple Storage Service (Amazon S3)／物件儲存 | ❌ 錯誤 | S3 是物件儲存，不是區塊儲存。 |
| Amazon Elastic File System (Amazon EFS)／檔案儲存 | ❌ 錯誤 | EFS 是 NFS 檔案系統。 |
| Amazon Elastic Container Service (Amazon ECS)／容器服務 | ❌ 錯誤 | ECS 是容器編排服務，不是儲存服務。 |
| Instance Store／執行個體存放區 | ✅ 正確 | Instance Store 提供暫時性區塊層級儲存。 |
| Amazon Elastic Block Store (Amazon EBS)／彈性區塊儲存 | ✅ 正確 | EBS 是 EC2 常用的持久性區塊儲存。 |

---

## 問題 6

**題目**
Which of the following statements are CORRECT about the AWS Auto Scaling group? (Select two)
以下哪些陳述關於 AWS Auto Scaling 群組是正確的？（選兩項）

**[選項]**
- A. Auto Scaling group scales up and upgrades to a more powerful EC2 instance to match an increase in demand／升級到更強大的 EC2
- B. Auto Scaling group scales down and reduces the number of EC2 instances to match a decrease in demand／向下擴展並減少 EC2 數量
- C. Auto Scaling group scales down and downgrades to a less powerful EC2 instance to match a decrease in demand／降級到較弱的 EC2
- D. Auto Scaling group scales out and adds more number of EC2 instances to match an increase in demand／向外擴展並增加 EC2 數量
- E. Auto Scaling group scales in and reduces the number of EC2 instances to match a decrease in demand／向內縮減並減少 EC2 數量

**正確答案**
Auto Scaling group scales out and adds more number of EC2 instances／向外擴展增加 EC2；Auto Scaling group scales in and reduces the number of EC2 instances／向內縮減減少 EC2

**為什麼正確**
Auto Scaling 群組做的是水平擴展：需求增加時 **scale out** 新增執行個體；需求降低時 **scale in** 減少執行個體。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Auto Scaling group scales up and upgrades to a more powerful EC2 instance／升級到更強大的 EC2 | ❌ 錯誤 | Scale up 是垂直擴展，Auto Scaling 群組通常不自動升級現有執行個體規格。 |
| Auto Scaling group scales down and reduces the number of EC2 instances／向下擴展並減少 EC2 數量 | ❌ 錯誤 | 減少數量的正確術語是 scale in，不是 scale down。 |
| Auto Scaling group scales down and downgrades to a less powerful EC2 instance／降級到較弱的 EC2 | ❌ 錯誤 | Scale down 是垂直降級，不是 ASG 的主要動作。 |
| Auto Scaling group scales out and adds more number of EC2 instances／向外擴展並增加 EC2 數量 | ✅ 正確 | Scale out 是新增更多執行個體。 |
| Auto Scaling group scales in and reduces the number of EC2 instances／向內縮減並減少 EC2 數量 | ✅ 正確 | Scale in 是移除執行個體以符合較低需求。 |

---

## 問題 7

**題目**
A research group wants to provision an Amazon EC2 instance for a flexible application that can be interrupted. Which of the following would you recommend as the MOST cost-optimal option?
一個研究群組希望為可被中斷的彈性應用程式佈建 Amazon EC2 執行個體。以下哪個是最具成本效益的選項？

**[選項]**
- A. On-Demand Instance／隨需執行個體
- B. Dedicated Host／專用主機
- C. Reserved Instance (RI)／保留執行個體
- D. Spot Instance／Spot 執行個體

**正確答案**
Spot Instance／Spot 執行個體

**為什麼正確**
**Spot Instance** 使用 AWS 閒置 EC2 容量，價格可大幅低於隨需，但可能被中斷。題目明確說應用程式可被中斷，因此 Spot 最具成本效益。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| On-Demand Instance／隨需執行個體 | ❌ 錯誤 | On-Demand 靈活且不中斷，但成本高於 Spot。 |
| Dedicated Host／專用主機 | ❌ 錯誤 | Dedicated Host 適合授權與合規，不是最低成本選項。 |
| Reserved Instance (RI)／保留執行個體 | ❌ 錯誤 | RI 適合長期穩定工作負載，需要承諾期。 |
| Spot Instance／Spot 執行個體 | ✅ 正確 | Spot 適合可中斷、彈性、容錯的低成本工作負載。 |

---

## 問題 8

**題目**
Which Amazon Route 53 routing policy would you use when you want to route your traffic in an active-passive configuration?
當您想以主動-被動設定路由流量時，您會使用哪個 Amazon Route 53 路由政策？

**[選項]**
- A. Weighted routing／加權路由
- B. Latency-based routing／延遲型路由
- C. Simple routing／簡單路由
- D. Failover routing／容錯移轉路由

**正確答案**
Failover routing／容錯移轉路由

**為什麼正確**
**Failover routing** 用於主動-被動架構，主要端點健康時走主端點，主端點不健康時切換到備援端點。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Weighted routing／加權路由 | ❌ 錯誤 | Weighted routing 依權重分配流量，適合 A/B 測試或比例分流。 |
| Latency-based routing／延遲型路由 | ❌ 錯誤 | Latency-based routing 依最低延遲選擇端點。 |
| Simple routing／簡單路由 | ❌ 錯誤 | Simple routing 是基本 DNS 回應，不支援主備健康切換邏輯。 |
| Failover routing／容錯移轉路由 | ✅ 正確 | Failover routing 專門用於 active-passive 容錯移轉。 |

---

## 問題 9

**題目**
Which AWS service protects your AWS account by monitoring malicious activity and detecting threats?
哪個 AWS 服務透過監控惡意活動和偵測威脅來保護您的 AWS 帳戶？

**[選項]**
- A. Amazon CloudWatch／監控服務
- B. AWS Trusted Advisor／最佳實務建議
- C. AWS CloudTrail／活動稽核記錄
- D. Amazon GuardDuty／威脅偵測

**正確答案**
Amazon GuardDuty／威脅偵測

**為什麼正確**
**Amazon GuardDuty** 是威脅偵測服務，會分析 CloudTrail、VPC Flow Logs、DNS 日誌等資料來源，找出惡意活動和未授權行為。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon CloudWatch／監控服務 | ❌ 錯誤 | CloudWatch 監控指標與日誌，不是威脅偵測服務。 |
| AWS Trusted Advisor／最佳實務建議 | ❌ 錯誤 | Trusted Advisor 提供最佳實務建議，不主動偵測威脅。 |
| AWS CloudTrail／活動稽核記錄 | ❌ 錯誤 | CloudTrail 記錄 API 活動，是 GuardDuty 的資料來源之一，但本身不是威脅偵測服務。 |
| Amazon GuardDuty／威脅偵測 | ✅ 正確 | GuardDuty 專門監控惡意活動並偵測威脅。 |

---

## 問題 10

**題目**
As a Cloud Practitioner, which Amazon S3 storage class would you recommend for data archival?
作為 Cloud Practitioner，您會推薦哪個 Amazon S3 儲存類別用於資料封存？

**[選項]**
- A. Amazon S3 Standard／標準儲存
- B. Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)／單區低頻存取
- C. Amazon S3 Intelligent-Tiering／智慧分層
- D. Amazon S3 Glacier Flexible Retrieval／Glacier 彈性取回

**正確答案**
Amazon S3 Glacier Flexible Retrieval／Glacier 彈性取回

**為什麼正確**
**S3 Glacier Flexible Retrieval** 適合封存與備份資料，成本低，取回時間通常為數分鐘到數小時，符合一般資料 archival 場景。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3 Standard／標準儲存 | ❌ 錯誤 | S3 Standard 適合頻繁存取，封存成本較高。 |
| Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)／單區低頻存取 | ❌ 錯誤 | One Zone-IA 適合可重建、低頻但需快速存取的資料，不是封存首選。 |
| Amazon S3 Intelligent-Tiering／智慧分層 | ❌ 錯誤 | Intelligent-Tiering 適合存取模式不確定的資料。 |
| Amazon S3 Glacier Flexible Retrieval／Glacier 彈性取回 | ✅ 正確 | Glacier Flexible Retrieval 是低成本封存儲存類別。 |

---

## 問題 11

**題目**
Which of the following AWS entities provides the information required to launch an Amazon EC2 instance?
以下哪個 AWS 實體提供啟動 Amazon EC2 執行個體所需的資訊？

**[選項]**
- A. Amazon Elastic Block Store (Amazon EBS)／彈性區塊儲存
- B. AWS Lambda／無伺服器函數
- C. Amazon Elastic File System (Amazon EFS)／檔案系統
- D. Amazon Machine Image (AMI)／Amazon 機器映像

**正確答案**
Amazon Machine Image (AMI)／Amazon 機器映像

**為什麼正確**
**AMI** 包含啟動 EC2 執行個體所需的作業系統、根磁碟區範本、啟動權限與區塊設備映射等資訊。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic Block Store (Amazon EBS)／彈性區塊儲存 | ❌ 錯誤 | EBS 是 EC2 可掛載的區塊儲存，不是啟動範本映像。 |
| AWS Lambda／無伺服器函數 | ❌ 錯誤 | Lambda 是函數運算服務，與 EC2 啟動資訊無關。 |
| Amazon Elastic File System (Amazon EFS)／檔案系統 | ❌ 錯誤 | EFS 是共享檔案系統。 |
| Amazon Machine Image (AMI)／Amazon 機器映像 | ✅ 正確 | AMI 提供啟動 EC2 執行個體所需資訊。 |

---

## 問題 12

**題目**
Which of the following improves the availability for a fleet of Amazon EC2 instances?
以下哪項可提升 Amazon EC2 執行個體群的可用性？

**[選項]**
- A. Deploy the EC2 instances in the same AZ across two different AWS Regions／在兩個不同區域的同一 AZ 部署
- B. Deploy the EC2 instances in the same AZ of an AWS Region／在同一區域的同一 AZ 部署
- C. Deploy the EC2 instances across different AWS Regions of the same AZ／在同一 AZ 的不同區域部署
- D. Deploy the EC2 instances across different Availability Zones (AZ) in the same AWS Region／在同一區域的不同 AZ 部署

**正確答案**
Deploy the EC2 instances across different Availability Zones (AZ) in the same AWS Region／在同一區域的不同 AZ 部署

**為什麼正確**
將 EC2 執行個體分散到同一 AWS Region 的多個 AZ，可避免單一 AZ 故障造成全部服務中斷，是提升可用性的常見做法。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Deploy the EC2 instances in the same AZ across two different AWS Regions／在兩個不同區域的同一 AZ 部署 | ❌ 錯誤 | AZ 名稱在不同區域中不具這種跨區域「同一 AZ」意義。 |
| Deploy the EC2 instances in the same AZ of an AWS Region／在同一區域的同一 AZ 部署 | ❌ 錯誤 | 同一 AZ 仍有單點故障風險。 |
| Deploy the EC2 instances across different AWS Regions of the same AZ／在同一 AZ 的不同區域部署 | ❌ 錯誤 | Region 與 AZ 的層級描述不正確。 |
| Deploy the EC2 instances across different Availability Zones (AZ) in the same AWS Region／在同一區域的不同 AZ 部署 | ✅ 正確 | 跨多 AZ 部署可提升高可用性。 |

---

## 問題 13

**題目**
An enterprise is developing a roadmap for its cloud adoption journey and wants to ensure its IT investments align with business objectives and deliver measurable value. Which perspective of the AWS Cloud Adoption Framework (CAF) addresses the strategy management capability?
一家企業正在制定雲端採用之旅的路線圖，並希望確保其 IT 投資與業務目標保持一致並創造可衡量的價值。AWS CAF 的哪個觀點涉及策略管理能力？

**[選項]**
- A. Operations Perspective／營運觀點
- B. Platform Perspective／平台觀點
- C. Governance Perspective／治理觀點
- D. Business Perspective／業務觀點

**正確答案**
Business Perspective／業務觀點

**為什麼正確**
AWS CAF 的 **Business Perspective** 聚焦業務成果、策略管理、投資與價值實現，協助 IT 投資與業務目標對齊。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Operations Perspective／營運觀點 | ❌ 錯誤 | 營運觀點關注日常營運、事件、問題、變更和容量管理。 |
| Platform Perspective／平台觀點 | ❌ 錯誤 | 平台觀點關注雲端平台架構與實作。 |
| Governance Perspective／治理觀點 | ❌ 錯誤 | 治理觀點偏風險、合規、投資組合與財務管理。 |
| Business Perspective／業務觀點 | ✅ 正確 | 業務觀點涵蓋策略管理與業務價值對齊。 |

---

## 問題 14

**題目**
Which of the following AWS services specialize in data migration from on-premises to AWS Cloud? (Select two)
以下哪些 AWS 服務專門用於從本地到 AWS 雲端的資料遷移？（選兩項）

**[選項]**
- A. AWS Direct Connect／專用網路連線
- B. AWS Transit Gateway／網路中樞
- C. AWS Site-to-Site VPN／站台對站台 VPN
- D. AWS Snowball／實體資料遷移設備
- E. AWS Database Migration Service (AWS DMS)／資料庫遷移服務

**正確答案**
AWS Snowball／實體資料遷移設備；AWS Database Migration Service (AWS DMS)／資料庫遷移服務

**為什麼正確**
**AWS Snowball** 用於大量本地資料離線遷移；**AWS DMS** 專門用於資料庫遷移，支援同質或異質資料庫移轉到 AWS。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Direct Connect／專用網路連線 | ❌ 錯誤 | Direct Connect 是網路連線服務，不是資料遷移專用服務。 |
| AWS Transit Gateway／網路中樞 | ❌ 錯誤 | Transit Gateway 用於連接 VPC 與網路，不搬遷資料本身。 |
| AWS Site-to-Site VPN／站台對站台 VPN | ❌ 錯誤 | VPN 是加密網路連線，不是資料遷移服務。 |
| AWS Snowball／實體資料遷移設備 | ✅ 正確 | Snowball 可用實體設備搬移大量本地資料到 AWS。 |
| AWS Database Migration Service (AWS DMS)／資料庫遷移服務 | ✅ 正確 | DMS 專門用於資料庫遷移。 |

---

## 問題 15

**題目**
A development team is looking for a forum where the most frequent questions and requests from AWS customers are listed along with AWS provided solutions. Which AWS forum/service can be used for troubleshooting an issue or checking for a solution?
一個開發團隊正在尋找一個論壇，其中列出了 AWS 客戶最常見的問題和請求以及 AWS 提供的解決方案。哪個 AWS 論壇/服務可用於疑難排解或查找解決方案？

**[選項]**
- A. AWS Support Center／支援中心
- B. AWS Health Dashboard - service health／服務健康儀表板
- C. AWS Marketplace／軟體市集
- D. AWS Knowledge Center／知識中心

**正確答案**
AWS Knowledge Center／知識中心

**為什麼正確**
**AWS Knowledge Center** 收集常見問題、疑難排解文章與 AWS 提供的解決方案，適合查找已知問題與解法。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Support Center／支援中心 | ❌ 錯誤 | Support Center 用於建立和管理支援案例，不是常見問題知識庫。 |
| AWS Health Dashboard - service health／服務健康儀表板 | ❌ 錯誤 | Service Health 顯示 AWS 服務狀態。 |
| AWS Marketplace／軟體市集 | ❌ 錯誤 | Marketplace 用於尋找和購買軟體。 |
| AWS Knowledge Center／知識中心 | ✅ 正確 | Knowledge Center 提供常見問題與 AWS 解法。 |

---

## 問題 16

**題目**
A financial services company must meet compliance requirements that mandate storing multiple copies of data in geographically distant locations. Which of the following represents the MOST resource-efficient solution?
一家金融服務公司必須符合要求在地理位置遙遠的地點儲存多個資料副本的合規要求。以下哪個代表最有效率的解決方案？

**[選項]**
- A. Use S3 same-region replication (S3 SRR) to replicate data between distant AWS Regions／使用 S3 SRR 在遙遠區域間複寫
- B. For every new object, trigger an AWS Lambda function to write data into a bucket in another AWS Region／每個新物件觸發 Lambda 寫入另一區域
- C. Run a daily job on an EC2 instance to copy objects into another Region／用 EC2 每日複製到另一區域
- D. Use S3 cross-region replication (S3 CRR) to replicate data between distant AWS Regions／使用 S3 CRR 在遙遠區域間複寫

**正確答案**
Use S3 cross-region replication (S3 CRR) to replicate data between distant AWS Regions／使用 S3 跨區域複寫

**為什麼正確**
**S3 Cross-Region Replication (CRR)** 可自動將物件複寫到不同 AWS Region，符合地理位置分散與合規需求，且比自行用 Lambda 或 EC2 複製更省管理成本。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Use S3 same-region replication (S3 SRR) to replicate data between distant AWS Regions／使用 S3 SRR 在遙遠區域間複寫 | ❌ 錯誤 | SRR 是同區域複寫，不能跨遙遠 Region。 |
| For every new object, trigger an AWS Lambda function to write data into a bucket in another AWS Region／每個新物件觸發 Lambda 寫入另一區域 | ❌ 錯誤 | 可自行實作，但管理與錯誤處理成本較高。 |
| Run a daily job on an EC2 instance to copy objects into another Region／用 EC2 每日複製到另一區域 | ❌ 錯誤 | 需要管理 EC2、排程與複製邏輯，不是最資源有效。 |
| Use S3 cross-region replication (S3 CRR) to replicate data between distant AWS Regions／使用 S3 CRR 在遙遠區域間複寫 | ✅ 正確 | CRR 是 S3 跨區域資料副本的受管方案。 |

---

## 問題 17

**題目**
Which of the following AWS services are regional in scope? (Select two)
以下哪些 AWS 服務的範圍是區域性的？（選兩項）

**[選項]**
- A. AWS Identity and Access Management (AWS IAM)／身分與存取管理
- B. AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆
- C. Amazon CloudFront／內容交付網路
- D. Amazon Rekognition／影像與影片分析
- E. AWS Lambda／無伺服器函數

**正確答案**
Amazon Rekognition／影像與影片分析；AWS Lambda／無伺服器函數

**為什麼正確**
**Amazon Rekognition** 和 **AWS Lambda** 都是在特定 AWS Region 中使用與部署的區域型服務。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Identity and Access Management (AWS IAM)／身分與存取管理 | ❌ 錯誤 | IAM 是全球服務。 |
| AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆 | ❌ 錯誤 | WAF 常作為全球/區域資源使用，但本題正確區域型選項是 Rekognition 與 Lambda。 |
| Amazon CloudFront／內容交付網路 | ❌ 錯誤 | CloudFront 是全球 CDN。 |
| Amazon Rekognition／影像與影片分析 | ✅ 正確 | Rekognition 是區域型 AI 服務。 |
| AWS Lambda／無伺服器函數 | ✅ 正確 | Lambda 函數建立在特定 Region。 |

---

## 問題 18

**題目**
A leading research firm needs to access information available in old patents and documents (such as PDFs, Text Files, Word documents, etc) present in its huge knowledge base. Which of the following is the correct service to address this requirement?
一家研究公司需要存取其龐大知識庫中舊專利和文件（如 PDF、文字檔案、Word 文件等）中的資訊。哪個服務適合解決此需求？

**[選項]**
- A. Amazon Comprehend／自然語言處理
- B. Amazon Lex／對話式介面
- C. Amazon Personalize／個人化推薦
- D. Amazon Kendra／企業智慧搜尋

**正確答案**
Amazon Kendra／企業智慧搜尋

**為什麼正確**
**Amazon Kendra** 是機器學習驅動的企業搜尋服務，可從 PDF、Word、文字檔等非結構化文件中搜尋相關資訊。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Comprehend／自然語言處理 | ❌ 錯誤 | Comprehend 用於文字情緒、實體、語言等 NLP 分析，不是企業文件搜尋服務。 |
| Amazon Lex／對話式介面 | ❌ 錯誤 | Lex 用於建立聊天機器人與語音/文字對話介面。 |
| Amazon Personalize／個人化推薦 | ❌ 錯誤 | Personalize 用於推薦系統，不是文件知識庫搜尋。 |
| Amazon Kendra／企業智慧搜尋 | ✅ 正確 | Kendra 專門用於企業知識庫與文件搜尋。 |

---

## 問題 19

**題目**
Under the AWS Shared Responsibility Model, which of the following is the responsibility of a customer regarding AWS Lambda?
根據 AWS 共同責任模型，以下哪項是客戶對 AWS Lambda 的責任？

**[選項]**
- A. Maintain all runtime environments for AWS Lambda functions／維護所有 Lambda 執行環境
- B. Configure networking infrastructure for the AWS Lambda functions／設定 Lambda 網路基礎設施
- C. Patch underlying OS for the AWS Lambda function infrastructure／修補 Lambda 底層作業系統
- D. Maintain versions of an AWS Lambda function／維護 Lambda 函數版本

**正確答案**
Maintain versions of an AWS Lambda function／維護 Lambda 函數版本

**為什麼正確**
Lambda 是高度抽象的無伺服器服務，AWS 管理底層作業系統、執行環境和基礎設施；客戶負責自己的程式碼、設定、權限與函數版本。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Maintain all runtime environments for AWS Lambda functions／維護所有 Lambda 執行環境 | ❌ 錯誤 | Lambda 執行環境由 AWS 管理。 |
| Configure networking infrastructure for the AWS Lambda functions／設定 Lambda 網路基礎設施 | ❌ 錯誤 | 底層網路基礎設施由 AWS 管理；客戶只設定 VPC 連接等函數層設定。 |
| Patch underlying OS for the AWS Lambda function infrastructure／修補 Lambda 底層作業系統 | ❌ 錯誤 | Lambda 底層 OS 修補由 AWS 負責。 |
| Maintain versions of an AWS Lambda function／維護 Lambda 函數版本 | ✅ 正確 | 函數版本與程式碼生命週期屬於客戶責任。 |

---

## 問題 20

**題目**
Which of the following AWS services have data encryption automatically enabled? (Select two)
以下哪些 AWS 服務預設自動啟用資料加密？（選兩項）

**[選項]**
- A. Amazon Redshift／資料倉儲
- B. Amazon Elastic File System (Amazon EFS)／檔案系統
- C. Amazon Elastic Block Store (Amazon EBS)／區塊儲存
- D. AWS Storage Gateway／儲存閘道
- E. Amazon Simple Storage Service (Amazon S3)／物件儲存

**正確答案**
AWS Storage Gateway／儲存閘道；Amazon Simple Storage Service (Amazon S3)／物件儲存

**為什麼正確**
**Amazon S3** 預設啟用伺服器端加密；**AWS Storage Gateway** 預設使用加密連線傳輸資料，符合題庫對自動加密的考點。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Redshift／資料倉儲 | ❌ 錯誤 | Redshift 加密可設定啟用，但不是此題的預設自動加密答案。 |
| Amazon Elastic File System (Amazon EFS)／檔案系統 | ❌ 錯誤 | EFS 的靜態/傳輸中加密需要建立時或設定中啟用。 |
| Amazon Elastic Block Store (Amazon EBS)／區塊儲存 | ❌ 錯誤 | EBS 可啟用帳戶預設加密，但服務本身不是此題所指自動啟用。 |
| AWS Storage Gateway／儲存閘道 | ✅ 正確 | Storage Gateway 預設使用加密通訊保護資料傳輸。 |
| Amazon Simple Storage Service (Amazon S3)／物件儲存 | ✅ 正確 | S3 新物件預設套用伺服器端加密。 |

---

## 問題 21

**題目**
Which of the following statements is correct regarding the Amazon Elastic File System (Amazon EFS) storage service?
以下哪項陳述關於 Amazon EFS 儲存服務是正確的？

**[選項]**
- A. EC2 instances can access files on an Amazon EFS file system only in one Availability Zone (AZ)／只能在一個 AZ 存取 EFS
- B. EC2 instances can access files on an Amazon EFS file system across many AZs and VPCs but not across Regions／可跨多 AZ 和 VPC，但不能跨 Region
- C. EC2 instances can access files on an Amazon EFS file system across many AZs but not across VPCs and Regions／可跨多 AZ，但不能跨 VPC 和 Region
- D. EC2 instances can access files on an Amazon EFS file system across many Availability Zones (AZ), Regions and VPCs／可跨多 AZ、Region 和 VPC 存取 EFS

**正確答案**
EC2 instances can access files on an Amazon EFS file system across many Availability Zones (AZ), Regions and VPCs／可跨多 AZ、Region 和 VPC 存取 EFS

**為什麼正確**
**Amazon EFS** 是區域型檔案系統，可在多個 AZ 中提供高可用檔案存取，並可透過適當網路連線讓其他 VPC 或環境中的 EC2 存取。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| EC2 instances can access files on an Amazon EFS file system only in one Availability Zone (AZ)／只能在一個 AZ 存取 EFS | ❌ 錯誤 | EFS 支援多 AZ 存取。 |
| EC2 instances can access files on an Amazon EFS file system across many AZs and VPCs but not across Regions／可跨多 AZ 和 VPC，但不能跨 Region | ❌ 錯誤 | 題庫將跨 Region/VPC 存取能力列為完整正確描述。 |
| EC2 instances can access files on an Amazon EFS file system across many AZs but not across VPCs and Regions／可跨多 AZ，但不能跨 VPC 和 Region | ❌ 錯誤 | 描述過度限制 EFS 的可存取範圍。 |
| EC2 instances can access files on an Amazon EFS file system across many Availability Zones (AZ), Regions and VPCs／可跨多 AZ、Region 和 VPC 存取 EFS | ✅ 正確 | EFS 支援多 AZ，並可透過網路設計支援跨 VPC/其他環境存取。 |

---

## 問題 22

**題目**
A cyber-security agency uses AWS Cloud and wants to carry out security assessments on its own AWS infrastructure without any prior approval from AWS. Which of the following describes/facilitates this practice?
一家網路安全機構使用 AWS 雲端，希望在無需事先獲得 AWS 批准的情況下對其自己的 AWS 基礎設施進行安全評估。以下哪項描述/促進了此實踐？

**[選項]**
- A. AWS Secrets Manager／機密管理
- B. Network Stress Testing／網路壓力測試
- C. Amazon Inspector／弱點評估
- D. Penetration Testing／滲透測試

**正確答案**
Penetration Testing／滲透測試

**為什麼正確**
AWS 允許客戶對自己帳戶中的特定 AWS 資源進行安全評估或滲透測試，常見服務不需事先申請 AWS 批准；但不得測試 AWS 底層基礎設施本身。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Secrets Manager／機密管理 | ❌ 錯誤 | Secrets Manager 管理機密，不描述安全評估做法。 |
| Network Stress Testing／網路壓力測試 | ❌ 錯誤 | 網路壓力測試和滲透測試不同，通常限制更多。 |
| Amazon Inspector／弱點評估 | ❌ 錯誤 | Inspector 是 AWS 自動化弱點評估服務，不是題目所描述的自行安全評估實踐。 |
| Penetration Testing／滲透測試 | ✅ 正確 | 滲透測試描述客戶對自身 AWS 資源進行安全評估。 |

---

## 問題 23

**題目**
Which of the following is a part of the AWS Global Infrastructure?
以下哪項是 AWS 全球基礎設施的一部分？

**[選項]**
- A. Virtual Private Network (VPN)／虛擬私有網路
- B. Virtual Private Cloud (VPC)／虛擬私有雲
- C. Subnet／子網路
- D. AWS Region／AWS 區域

**正確答案**
AWS Region／AWS 區域

**為什麼正確**
AWS 全球基礎設施由 **Regions**、Availability Zones、Local Zones、Wavelength Zones 和 Edge Locations 等組成。Region 是全球基礎設施的一部分。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Virtual Private Network (VPN)／虛擬私有網路 | ❌ 錯誤 | VPN 是網路連線方案，不是全球基礎設施單元。 |
| Virtual Private Cloud (VPC)／虛擬私有雲 | ❌ 錯誤 | VPC 是客戶在 Region 中建立的虛擬網路。 |
| Subnet／子網路 | ❌ 錯誤 | Subnet 是 VPC 內的子網段，位於單一 AZ。 |
| AWS Region／AWS 區域 | ✅ 正確 | Region 是 AWS 全球基礎設施的核心組成。 |

---

## 問題 24

**題目**
An IT company has deployed a static website on Amazon S3, but the website is still inaccessible. Which of the following solutions would you suggest to address this issue?
一家 IT 公司在 Amazon S3 上部署了靜態網站，但網站仍無法存取。您建議哪個解決方案來解決此問題？

**[選項]**
- A. Enable Amazon S3 versioning／啟用 S3 版本控制
- B. Enable Amazon S3 replication／啟用 S3 複寫
- C. Disable Amazon S3 encryption／停用 S3 加密
- D. Fix the Amazon S3 bucket policy／修正 S3 儲存貯體政策

**正確答案**
Fix the Amazon S3 bucket policy／修正 S3 儲存貯體政策

**為什麼正確**
S3 靜態網站若無法存取，常見原因是物件或儲存貯體沒有正確公開讀取權限。修正 **bucket policy** 可允許網站內容被公開讀取。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Enable Amazon S3 versioning／啟用 S3 版本控制 | ❌ 錯誤 | 版本控制保護物件版本，不解決網站存取權限。 |
| Enable Amazon S3 replication／啟用 S3 複寫 | ❌ 錯誤 | 複寫用於資料副本，不處理公開網站存取問題。 |
| Disable Amazon S3 encryption／停用 S3 加密 | ❌ 錯誤 | S3 加密通常不會造成網站無法公開讀取的核心問題。 |
| Fix the Amazon S3 bucket policy／修正 S3 儲存貯體政策 | ✅ 正確 | Bucket policy 可授權公開讀取靜態網站物件。 |

---

## 問題 25

**題目**
An e-commerce company uses AWS Cloud and would like to receive separate invoices for development and production environments. Which of the following solutions would you recommend?
一家電子商務公司使用 AWS 雲端，希望收到開發和生產環境的獨立發票。您會推薦以下哪個解決方案？

**[選項]**
- A. Use AWS Cost Explorer to create separate invoices for development and production environments／使用 Cost Explorer 建立獨立發票
- B. Tag all resources as either development or production, then use the tags to create separate invoices／用標籤建立獨立發票
- C. Use AWS Organizations to create separate invoices for development and production environments／使用 Organizations 建立獨立發票
- D. Create separate AWS accounts for development and production environments to receive separate invoices／為開發和生產建立獨立 AWS 帳戶

**正確答案**
Create separate AWS accounts for development and production environments to receive separate invoices／為開發和生產建立獨立 AWS 帳戶

**為什麼正確**
若需要真正分開發票，應建立獨立 AWS 帳戶。標籤、Cost Explorer 或 Organizations 可協助成本分析與整合管理，但不等同於為同一帳戶資源產生獨立發票。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Use AWS Cost Explorer to create separate invoices／使用 Cost Explorer 建立獨立發票 | ❌ 錯誤 | Cost Explorer 用於分析成本，不建立發票。 |
| Tag all resources as either development or production, then use the tags to create separate invoices／用標籤建立獨立發票 | ❌ 錯誤 | 標籤可分攤成本，但不產生獨立 AWS 發票。 |
| Use AWS Organizations to create separate invoices／使用 Organizations 建立獨立發票 | ❌ 錯誤 | Organizations 常用於整合帳單，不是讓同一帳戶資源分開發票的工具。 |
| Create separate AWS accounts for development and production environments／為開發和生產建立獨立 AWS 帳戶 | ✅ 正確 | 不同 AWS 帳戶可接收獨立發票。 |

---

## 問題 26

**題目**
An AWS hardware failure has impacted one of your Amazon EBS volumes. Which AWS service will alert you of the affected resources and provide a remedial action?
AWS 硬體故障影響了您的一個 Amazon EBS 磁碟區。哪個 AWS 服務會通知您受影響的資源並提供補救措施？

**[選項]**
- A. Amazon GuardDuty／威脅偵測
- B. AWS Trusted Advisor／最佳實務建議
- C. AWS Config／資源組態追蹤
- D. AWS Health Dashboard - Your account health／您的帳戶健康狀態

**正確答案**
AWS Health Dashboard - Your account health／您的帳戶健康狀態

**為什麼正確**
**AWS Health Dashboard - Your account health** 會提供與您帳戶資源相關的個人化事件、受影響資源和建議補救動作，例如特定 EBS 磁碟區受到 AWS 硬體事件影響。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon GuardDuty／威脅偵測 | ❌ 錯誤 | GuardDuty 偵測安全威脅，不通知硬體故障補救。 |
| AWS Trusted Advisor／最佳實務建議 | ❌ 錯誤 | Trusted Advisor 提供最佳實務檢查，不是資源事件通知中心。 |
| AWS Config／資源組態追蹤 | ❌ 錯誤 | Config 追蹤配置歷史與合規，不提供 AWS 健康事件補救通知。 |
| AWS Health Dashboard - Your account health／您的帳戶健康狀態 | ✅ 正確 | Account Health 會提供個人化受影響資源與補救建議。 |

---

## 問題 27

**題目**
Which AWS service will you use to privately connect your VPC to Amazon S3?
您會使用哪個 AWS 服務將您的 VPC 私下連接至 Amazon S3？

**[選項]**
- A. AWS Direct Connect／專用網路連線
- B. Amazon API Gateway／API 閘道
- C. AWS Transit Gateway／網路中樞
- D. VPC Endpoint／VPC 端點

**正確答案**
VPC Endpoint／VPC 端點

**為什麼正確**
**VPC Endpoint** 讓 VPC 私下連接到支援的 AWS 服務，例如 Amazon S3，流量不需經過公有網際網路。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Direct Connect／專用網路連線 | ❌ 錯誤 | Direct Connect 連接本地網路與 AWS，不是 VPC 到 S3 的私有端點。 |
| Amazon API Gateway／API 閘道 | ❌ 錯誤 | API Gateway 用於建立和管理 API。 |
| AWS Transit Gateway／網路中樞 | ❌ 錯誤 | Transit Gateway 用於連接 VPC 和本地網路，不是直接私連 S3 的服務。 |
| VPC Endpoint／VPC 端點 | ✅ 正確 | VPC Endpoint 可私下連接 VPC 與 S3。 |

---

## 問題 28

**題目**
Compared to the on-demand instance prices, what is the highest possible discount offered for reserved instances (RI)?
與隨需執行個體價格相比，保留執行個體（RI）提供的最高折扣是多少？

**[選項]**
- A. 40%
- B. 90%
- C. 50%
- D. 72%

**正確答案**
72%

**為什麼正確**
EC2 Reserved Instances 相較於 On-Demand 可提供最高約 **72%** 折扣。Spot 才常見最高約 90% 折扣。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| 40% | ❌ 錯誤 | 低於 RI 可達的最高折扣。 |
| 90% | ❌ 錯誤 | 90% 常見於 Spot Instance，不是 RI。 |
| 50% | ❌ 錯誤 | 低於題庫所考 RI 最高折扣。 |
| 72% | ✅ 正確 | Reserved Instances 相較 On-Demand 最高可節省約 72%。 |

---

## 問題 29

**題目**
Which of the following use cases is best suited for Amazon EFS Standard-Infrequent Access (EFS Standard-IA) storage class?
以下哪個使用案例最適合 Amazon EFS Standard-Infrequent Access（EFS Standard-IA）儲存類別？

**[選項]**
- A. Object storage for workloads that need sub-second latency speeds for accessing the data／需要亞秒延遲的物件儲存
- B. Use as boot volume for highly available Amazon EC2 instances／作為高可用 EC2 開機磁碟
- C. Storing data in a single AWS Availability Zone (AZ)／將資料儲存在單一 AZ
- D. Storing files in an accessible location to satisfy audit requirements／將檔案儲存在可存取位置以滿足稽核要求

**正確答案**
Storing files in an accessible location to satisfy audit requirements／將檔案儲存在可存取位置以滿足稽核要求

**為什麼正確**
**EFS Standard-IA** 適合不常存取但需要在需要時可存取的檔案資料，例如為稽核或合規保留的共享檔案。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Object storage for workloads that need sub-second latency speeds／需要亞秒延遲的物件儲存 | ❌ 錯誤 | EFS 是檔案儲存，不是物件儲存。 |
| Use as boot volume for highly available Amazon EC2 instances／作為 EC2 開機磁碟 | ❌ 錯誤 | EC2 開機磁碟通常使用 EBS。 |
| Storing data in a single AWS Availability Zone (AZ)／將資料儲存在單一 AZ | ❌ 錯誤 | EFS Standard-IA 是區域級檔案儲存，非單 AZ 使用案例。 |
| Storing files in an accessible location to satisfy audit requirements／將檔案儲存在可存取位置以滿足稽核要求 | ✅ 正確 | 低頻但需可存取的檔案保留適合 EFS Standard-IA。 |

---

## 問題 30

**題目**
An IT company would like to move its IT resources from an AWS Region in the US to another AWS Region in Europe. Which of the following represents the correct solution?
一家 IT 公司希望將其 IT 資源從美國的 AWS 區域遷移至歐洲的另一個 AWS 區域。以下哪個代表正確的解決方案？

**[選項]**
- A. Use AWS CloudFormation to move the resources from source AWS Region to destination AWS Region／使用 CloudFormation 移動資源
- B. Use AWS Database Migration Service (AWS DMS) to move all resources from source to destination AWS Region／使用 DMS 移動所有資源
- C. Raise a ticket with AWS Support for this resource migration／向 AWS Support 提交工單
- D. The company should just start creating new resources in the destination AWS Region and then migrate the relevant data and applications into this new AWS Region／在目標區域建立新資源，再遷移資料和應用

**正確答案**
The company should just start creating new resources in the destination AWS Region and then migrate the relevant data and applications into this new AWS Region／在目標區域建立新資源，再遷移資料和應用

**為什麼正確**
AWS 資源通常是區域性的，不能直接「搬移」整個 Region 的資源。正確做法是在目標 Region 重新建立所需資源，並遷移相關資料與應用程式。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Use AWS CloudFormation to move the resources／使用 CloudFormation 移動資源 | ❌ 錯誤 | CloudFormation 可在目標區域重新佈建資源，但不會直接搬移既有資源。 |
| Use AWS DMS to move all resources／使用 DMS 移動所有資源 | ❌ 錯誤 | DMS 用於資料庫遷移，不會移動所有 AWS 資源。 |
| Raise a ticket with AWS Support／向 AWS Support 提交工單 | ❌ 錯誤 | AWS Support 不會代替客戶跨 Region 搬移所有資源。 |
| Start creating new resources in the destination Region and migrate data/applications／在目標區域建立新資源再遷移 | ✅ 正確 | 跨區域遷移通常需要在新 Region 建置資源並搬遷資料與應用。 |

---

## 問題 31

**題目**
Which of the following are recommended best practices for AWS IAM service? (Select two)
以下哪些是 AWS IAM 服務的推薦最佳實務？（選兩項）

**[選項]**
- A. Share AWS account root user access keys with other administrators／與管理員共享 root 存取金鑰
- B. Grant maximum privileges to avoid assigning privileges again／授予最大權限以避免再次分配
- C. Create a minimum number of accounts and share these account credentials among employees／建立少量帳戶並共享
- D. Rotate credentials regularly／定期輪換憑證
- E. Enable multi-factor authentication (MFA) for all users／為所有使用者啟用 MFA

**正確答案**
Rotate credentials regularly／定期輪換憑證；Enable MFA for all users／為所有使用者啟用 MFA

**為什麼正確**
IAM 最佳實務包括使用最小權限、不要共享憑證、定期輪換憑證，以及為高權限和一般使用者啟用 MFA。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Share AWS account root user access keys with other administrators／共享 root 金鑰 | ❌ 錯誤 | root 憑證不應共享，應避免使用 root 日常操作。 |
| Grant maximum privileges to avoid assigning privileges again／授予最大權限 | ❌ 錯誤 | 違反最小權限原則。 |
| Create a minimum number of accounts and share credentials／共享帳戶憑證 | ❌ 錯誤 | 應為人員建立個別身分，不共享憑證。 |
| Rotate credentials regularly／定期輪換憑證 | ✅ 正確 | 定期輪換降低長期憑證外洩風險。 |
| Enable multi-factor authentication (MFA) for all users／為所有使用者啟用 MFA | ✅ 正確 | MFA 可大幅提升帳戶安全性。 |

---

## 問題 32

**題目**
Which AWS service can be used for online analytical processing?
哪個 AWS 服務可用於線上分析處理？

**[選項]**
- A. Amazon ElastiCache／記憶體快取
- B. Amazon Relational Database Service (Amazon RDS)／關聯式資料庫
- C. Amazon DynamoDB／NoSQL 資料庫
- D. Amazon Redshift／資料倉儲

**正確答案**
Amazon Redshift／資料倉儲

**為什麼正確**
**Amazon Redshift** 是雲端資料倉儲服務，適合 OLAP、報表與大規模分析查詢。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon ElastiCache／記憶體快取 | ❌ 錯誤 | ElastiCache 用於記憶體快取與低延遲資料存取。 |
| Amazon RDS／關聯式資料庫 | ❌ 錯誤 | RDS 通常用於 OLTP 交易型工作負載。 |
| Amazon DynamoDB／NoSQL 資料庫 | ❌ 錯誤 | DynamoDB 是高擴展 NoSQL 鍵值/文件資料庫。 |
| Amazon Redshift／資料倉儲 | ✅ 正確 | Redshift 專為線上分析處理與資料倉儲設計。 |

---

## 問題 33

**題目**
A startup has just moved its IT infrastructure to AWS Cloud. The CTO would like to receive detailed reports that break down the startup's AWS costs by the hour in an Amazon S3 bucket. Which AWS service would you recommend?
一家新創公司剛將其 IT 基礎設施遷移至 AWS 雲端。CTO 希望在 Amazon S3 儲存貯體中收到按小時細分 AWS 成本的詳細報告。您會推薦哪個 AWS 服務？

**[選項]**
- A. AWS Cost Explorer／成本分析
- B. AWS Pricing Calculator／定價試算
- C. AWS Budgets／預算管理
- D. AWS Cost & Usage Report (AWS CUR)／成本與用量報告

**正確答案**
AWS Cost & Usage Report (AWS CUR)／成本與用量報告

**為什麼正確**
**AWS Cost & Usage Report (CUR)** 提供最詳細的成本與用量資料，可設定以小時粒度交付到 Amazon S3。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Cost Explorer／成本分析 | ❌ 錯誤 | Cost Explorer 用於互動式視覺化與分析成本，不是交付詳細 S3 報告的服務。 |
| AWS Pricing Calculator／定價試算 | ❌ 錯誤 | Pricing Calculator 用於事前估算成本。 |
| AWS Budgets／預算管理 | ❌ 錯誤 | Budgets 用於設定預算與告警。 |
| AWS Cost & Usage Report (AWS CUR)／成本與用量報告 | ✅ 正確 | CUR 可將詳細成本用量報告交付到 S3，支援小時粒度。 |

---

## 問題 34

**題目**
Which pillar of the AWS Well-Architected Framework recommends maintaining infrastructure as code (IaC)?
AWS Well-Architected Framework 的哪個支柱建議將基礎設施作為程式碼（IaC）維護？

**[選項]**
- A. Cost Optimization／成本優化
- B. Security／安全性
- C. Performance Efficiency／效能效率
- D. Operational Excellence／卓越營運

**正確答案**
Operational Excellence／卓越營運

**為什麼正確**
**Operational Excellence** 支柱強調以程式碼執行操作、頻繁小型可逆變更、改善流程和自動化。Infrastructure as Code 是卓越營運的重要實踐。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Cost Optimization／成本優化 | ❌ 錯誤 | 成本優化關注以最低成本交付業務價值。 |
| Security／安全性 | ❌ 錯誤 | 安全性支柱關注保護資料、系統和資產。 |
| Performance Efficiency／效能效率 | ❌ 錯誤 | 效能效率關注資源選型與高效使用。 |
| Operational Excellence／卓越營運 | ✅ 正確 | IaC 和自動化營運是 Operational Excellence 的核心建議。 |

---

## 問題 35

**題目**
Which Amazon S3 storage class offers the lowest availability?
哪個 Amazon S3 儲存類別提供最低的可用性？

**[選項]**
- A. Amazon S3 Intelligent-Tiering／智慧分層
- B. Amazon S3 Standard／標準儲存
- C. Amazon S3 Glacier Flexible Retrieval／Glacier 彈性取回
- D. Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)／單區低頻存取

**正確答案**
Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)／單區低頻存取

**為什麼正確**
**S3 One Zone-IA** 只將資料儲存在單一 AZ，成本較低，但可用性低於跨多 AZ 儲存的 S3 類別。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3 Intelligent-Tiering／智慧分層 | ❌ 錯誤 | Intelligent-Tiering 跨多 AZ，適合不確定存取模式。 |
| Amazon S3 Standard／標準儲存 | ❌ 錯誤 | Standard 提供高可用性，適合頻繁存取。 |
| Amazon S3 Glacier Flexible Retrieval／Glacier 彈性取回 | ❌ 錯誤 | Glacier 類是封存儲存，重點是低成本與取回時間，不是最低可用性選項。 |
| Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)／單區低頻存取 | ✅ 正確 | One Zone-IA 單 AZ 儲存，可用性最低。 |

---

## 問題 36

**題目**
A startup runs its proprietary application on docker containers. Which AWS service would you recommend so that the startup can run containers and still have access to the underlying servers?
一家新創公司在 Docker 容器上執行其專有應用程式。您會推薦哪個 AWS 服務，使新創公司可以執行容器並仍然可以存取底層伺服器？

**[選項]**
- A. Amazon Elastic Container Registry (Amazon ECR)／容器映像倉庫
- B. AWS Fargate／無伺服器容器運算
- C. AWS Lambda／無伺服器函數
- D. Amazon Elastic Container Service (Amazon ECS)／容器編排服務

**正確答案**
Amazon Elastic Container Service (Amazon ECS)／容器編排服務

**為什麼正確**
**Amazon ECS** 使用 EC2 啟動類型時，可執行 Docker 容器並保留對底層 EC2 伺服器的存取與控制。Fargate 則隱藏底層伺服器。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic Container Registry (Amazon ECR)／容器映像倉庫 | ❌ 錯誤 | ECR 儲存容器映像，不執行容器。 |
| AWS Fargate／無伺服器容器運算 | ❌ 錯誤 | Fargate 無需管理伺服器，也不能存取底層伺服器。 |
| AWS Lambda／無伺服器函數 | ❌ 錯誤 | Lambda 是函數服務，不是保留底層伺服器存取的容器編排平台。 |
| Amazon Elastic Container Service (Amazon ECS)／容器編排服務 | ✅ 正確 | ECS EC2 啟動類型可執行容器並存取底層 EC2。 |

---

## 問題 37

**題目**
A global e-commerce platform wants to restrict access to its website from specific countries to comply with regional regulations. Which AWS service is best suited to implement this restriction?
一個全球電子商務平台希望限制特定國家/地區對其網站的存取，以符合地區法規。哪個 AWS 服務最適合實施此限制？

**[選項]**
- A. Amazon Fraud Detector／詐欺偵測
- B. AWS Shield／DDoS 防護
- C. Amazon Pinpoint／使用者互動訊息
- D. Amazon WAF／Web 應用程式防火牆

**正確答案**
Amazon WAF／Web 應用程式防火牆

**為什麼正確**
**AWS WAF** 可使用地理比對條件封鎖或允許特定國家/地區的 Web 請求，適合網站地區存取限制。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Fraud Detector／詐欺偵測 | ❌ 錯誤 | Fraud Detector 用於識別線上詐欺風險，不做網站地理封鎖。 |
| AWS Shield／DDoS 防護 | ❌ 錯誤 | Shield 用於 DDoS 防護，不是地理位置存取控制。 |
| Amazon Pinpoint／使用者互動訊息 | ❌ 錯誤 | Pinpoint 用於行銷、推播與使用者互動。 |
| Amazon WAF／Web 應用程式防火牆 | ✅ 正確 | WAF 可根據地理位置限制網站存取。 |

---

## 問題 38

**題目**
Which of the following are components of an AWS Site-to-Site VPN? (Select two)
以下哪些是 AWS Site-to-Site VPN 的元件？（選兩項）

**[選項]**
- A. Network Address Translation gateway (NAT gateway)／NAT 閘道
- B. AWS storage gateway／AWS 儲存閘道
- C. Internet gateway／網際網路閘道
- D. Virtual private gateway (VGW)／虛擬私有閘道
- E. Customer gateway／客戶閘道

**正確答案**
Virtual private gateway (VGW)／虛擬私有閘道；Customer gateway／客戶閘道

**為什麼正確**
AWS Site-to-Site VPN 典型由 AWS 端的 **Virtual Private Gateway** 或 Transit Gateway，以及客戶端的 **Customer Gateway** 建立加密 VPN 連線。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Network Address Translation gateway (NAT gateway)／NAT 閘道 | ❌ 錯誤 | NAT Gateway 讓私有子網路出站連網，不是 Site-to-Site VPN 元件。 |
| AWS storage gateway／AWS 儲存閘道 | ❌ 錯誤 | Storage Gateway 是混合雲儲存服務。 |
| Internet gateway／網際網路閘道 | ❌ 錯誤 | Internet Gateway 讓 VPC 連接網際網路，不是 VPN 兩端元件。 |
| Virtual private gateway (VGW)／虛擬私有閘道 | ✅ 正確 | VGW 是 VPC 端的 VPN 閘道。 |
| Customer gateway／客戶閘道 | ✅ 正確 | Customer Gateway 代表客戶端 VPN 裝置或軟體。 |

---

## 問題 39

**題目**
AWS Lambda pricing is based on which of the following criteria? (Select two)
AWS Lambda 定價基於以下哪些標準？（選兩項）

**[選項]**
- A. The number of lines of code for the AWS Lambda function／程式碼行數
- B. The language runtime of the AWS Lambda function／語言執行環境
- C. The size of the deployment package for the AWS Lambda function／部署套件大小
- D. Number of requests for the AWS Lambda function／請求數量
- E. The time it takes for the AWS Lambda function to execute／函數執行時間

**正確答案**
Number of requests for the AWS Lambda function／請求數量；The time it takes for the AWS Lambda function to execute／函數執行時間

**為什麼正確**
Lambda 主要依 **請求次數** 與 **執行時間**（搭配配置記憶體計算 GB-seconds）收費，不依程式碼行數或語言 runtime 收費。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| The number of lines of code／程式碼行數 | ❌ 錯誤 | Lambda 不按程式碼行數計費。 |
| The language runtime／語言執行環境 | ❌ 錯誤 | 不因 Node.js、Python 等 runtime 類型直接計費。 |
| The size of the deployment package／部署套件大小 | ❌ 錯誤 | 部署套件大小不是主要計費依據。 |
| Number of requests／請求數量 | ✅ 正確 | Lambda 會依請求次數計費。 |
| The time it takes to execute／執行時間 | ✅ 正確 | Lambda 會依執行時間與記憶體配置計費。 |

---

## 問題 40

**題目**
Which budget types can be created under AWS Budgets? (Select three)
在 AWS Budgets 下可以建立哪些預算類型？（選三項）

**[選項]**
- A. Software budget／軟體預算
- B. Resource budget／資源預算
- C. Hardware budget／硬體預算
- D. Reservation budget／預留預算
- E. Usage budget／使用量預算
- F. Cost budget／成本預算

**正確答案**
Reservation budget／預留預算；Usage budget／使用量預算；Cost budget／成本預算

**為什麼正確**
AWS Budgets 支援建立成本預算、使用量預算、預留相關預算，以及 Savings Plans 相關預算。題目中的正確類型是 Cost、Usage、Reservation。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Software budget／軟體預算 | ❌ 錯誤 | 不是 AWS Budgets 的標準預算類型。 |
| Resource budget／資源預算 | ❌ 錯誤 | 不是題目所列 AWS Budgets 標準類型。 |
| Hardware budget／硬體預算 | ❌ 錯誤 | AWS Budgets 沒有硬體預算類型。 |
| Reservation budget／預留預算 | ✅ 正確 | 可建立預留使用率或覆蓋率相關預算。 |
| Usage budget／使用量預算 | ✅ 正確 | 可針對服務用量設定預算。 |
| Cost budget／成本預算 | ✅ 正確 | 可針對成本設定預算與告警。 |

---

## 問題 41

**題目**
Which feature of AWS Cloud offers the ability to innovate faster and rapidly develop, test and launch software applications?
AWS 雲端的哪項功能提供了更快創新以及快速開發、測試和啟動軟體應用程式的能力？

**[選項]**
- A. Cost savings／成本節省
- B. Ability to deploy globally in minutes／幾分鐘內全球部署
- C. Elasticity／彈性
- D. Agility／敏捷性

**正確答案**
Agility／敏捷性

**為什麼正確**
**Agility** 指雲端讓團隊快速取得資源、快速試驗、開發、測試和推出應用，加速創新週期。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Cost savings／成本節省 | ❌ 錯誤 | 成本節省是雲端優勢，但題目重點是快速創新與開發。 |
| Ability to deploy globally in minutes／幾分鐘內全球部署 | ❌ 錯誤 | 這是全球化部署能力，不是題目所問的創新速度特性。 |
| Elasticity／彈性 | ❌ 錯誤 | 彈性是按需取得與釋放資源。 |
| Agility／敏捷性 | ✅ 正確 | 敏捷性直接對應快速開發、測試、推出和創新。 |

---

## 問題 42

**題目**
Which of the following is correct regarding the AWS Shield Advanced pricing?
以下哪項關於 AWS Shield Advanced 定價的陳述是正確的？

**[選項]**
- A. AWS Shield Advanced is a free service for all AWS Support plans／所有支援方案免費
- B. AWS Shield Advanced is a free service for AWS Business Support plan／Business Support 免費
- C. AWS Shield Advanced is a free service for AWS Enterprise Support plan／Enterprise Support 免費
- D. AWS Shield Advanced offers protection against higher fees that could result from a DDoS attack／提供 DDoS 攻擊導致高額費用的保護

**正確答案**
AWS Shield Advanced offers protection against higher fees that could result from a DDoS attack／提供 DDoS 攻擊導致高額費用的保護

**為什麼正確**
**AWS Shield Advanced** 是付費 DDoS 防護服務，提供進階防護、DDoS 成本保護等能力，可協助處理由 DDoS 攻擊造成的流量高峰費用風險。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Shield Advanced is a free service for all AWS Support plans／所有支援方案免費 | ❌ 錯誤 | Shield Standard 才是自動免費；Advanced 是付費服務。 |
| AWS Shield Advanced is a free service for AWS Business Support plan／Business Support 免費 | ❌ 錯誤 | Business Support 不會讓 Shield Advanced 免費。 |
| AWS Shield Advanced is a free service for AWS Enterprise Support plan／Enterprise Support 免費 | ❌ 錯誤 | Enterprise Support 也不代表 Shield Advanced 免費。 |
| AWS Shield Advanced offers protection against higher fees that could result from a DDoS attack／提供 DDoS 攻擊導致高額費用的保護 | ✅ 正確 | Shield Advanced 包含 DDoS 成本保護相關能力。 |

---

## 問題 43

**題目**
Which AWS service can be used to execute code triggered by new files being uploaded to Amazon S3?
哪個 AWS 服務可用於執行由新檔案上傳至 Amazon S3 觸發的程式碼？

**[選項]**
- A. Amazon Simple Queue Service (Amazon SQS)／訊息佇列
- B. Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器
- C. Amazon Elastic Container Service (Amazon ECS)／容器服務
- D. AWS Lambda／無伺服器函數

**正確答案**
AWS Lambda／無伺服器函數

**為什麼正確**
**AWS Lambda** 可被 S3 事件通知觸發，在新物件上傳時自動執行程式碼，常用於影像處理、資料轉換、索引建立等。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Simple Queue Service (Amazon SQS)／訊息佇列 | ❌ 錯誤 | SQS 可接收事件訊息，但不執行程式碼。 |
| Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器 | ❌ 錯誤 | EC2 可執行程式，但需自行管理伺服器與觸發邏輯。 |
| Amazon Elastic Container Service (Amazon ECS)／容器服務 | ❌ 錯誤 | ECS 執行容器，不是 S3 事件最直接的函數觸發服務。 |
| AWS Lambda／無伺服器函數 | ✅ 正確 | Lambda 可由 S3 上傳事件觸發並執行程式碼。 |

---

## 問題 44

**題目**
AWS IAM policies are written as JSON documents. Which of the following are mandatory elements of an IAM policy?
AWS IAM 政策以 JSON 文件形式撰寫。以下哪些是 IAM 政策的必要元素？

**[選項]**
- A. Effect, Sid
- B. Action, Condition
- C. Sid, Principal
- D. Effect, Action

**正確答案**
Effect, Action

**為什麼正確**
IAM 政策陳述中至少需要指定 **Effect**（Allow 或 Deny）和 **Action**（允許或拒絕的動作）。Sid 和 Condition 通常是可選元素。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Effect, Sid | ❌ 錯誤 | Effect 必要，但 Sid 是可選識別字。 |
| Action, Condition | ❌ 錯誤 | Action 必要，但 Condition 是可選條件。 |
| Sid, Principal | ❌ 錯誤 | Sid 可選；Principal 在身分型政策中通常不使用。 |
| Effect, Action | ✅ 正確 | Effect 與 Action 是 IAM policy statement 的必要核心元素。 |

---

## 問題 45

**題目**
A research lab wants to optimize the caching capabilities for its scientific computations application running on Amazon EC2 instances. Which Amazon EC2 storage option is best suited for this use-case?
一個研究實驗室希望優化其在 Amazon EC2 執行個體上執行的科學運算應用程式的快取功能。哪個 Amazon EC2 儲存選項最適合此使用案例？

**[選項]**
- A. Amazon Simple Storage Service (Amazon S3)／物件儲存
- B. Amazon Elastic Block Store (Amazon EBS)／區塊儲存
- C. Amazon Elastic File System (Amazon EFS)／檔案系統
- D. Instance Store／執行個體存放區

**正確答案**
Instance Store／執行個體存放區

**為什麼正確**
**Instance Store** 位於 EC2 實體主機本機，提供非常低延遲和高 I/O，適合暫時性快取、緩衝區和可重建資料。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Simple Storage Service (Amazon S3)／物件儲存 | ❌ 錯誤 | S3 是物件儲存，延遲與存取模式不適合 EC2 本機快取。 |
| Amazon Elastic Block Store (Amazon EBS)／區塊儲存 | ❌ 錯誤 | EBS 是持久性區塊儲存，可用於磁碟，但快取場景不如本機 Instance Store。 |
| Amazon Elastic File System (Amazon EFS)／檔案系統 | ❌ 錯誤 | EFS 是共享檔案系統，不是最低延遲快取選項。 |
| Instance Store／執行個體存放區 | ✅ 正確 | Instance Store 高速、暫時性、本機附加，最適合快取。 |

---

## 問題 46

**題目**
A customer is running a comparative study of pricing models of Amazon EFS and Amazon EBS. Which of the following statements are correct regarding this use-case? (Select two)
一位客戶正在對 Amazon EFS 和 Amazon EBS 的定價模型進行比較研究。以下哪些陳述關於此使用案例是正確的？（選兩項）

**[選項]**
- A. Amazon EBS Snapshot storage pricing is based on the amount of space your data consumes in Amazon EBS／EBS 快照定價基於資料在 EBS 中佔用空間
- B. With AWS Backup, you pay only for the amount of Amazon EFS backup storage you use in a month, you need not pay for restoring this data／EFS 備份只付儲存費，不需付還原費
- C. Amazon EC2 data transfer charges will apply for all Amazon EBS direct APIs for Snapshots／所有 EBS Snapshot direct APIs 都適用 EC2 資料傳輸費
- D. Amazon EBS Snapshots are stored incrementally, which means you are billed only for the changed blocks stored／EBS 快照增量儲存，只為變更區塊付費
- E. You will pay a fee each time you read from or write data stored on the Amazon EFS - Infrequent Access storage class／每次讀寫 EFS-IA 資料都需付費

**正確答案**
Amazon EBS Snapshots are stored incrementally／EBS 快照增量儲存；You will pay a fee each time you read from or write data stored on EFS-IA／EFS-IA 每次讀寫需付費

**為什麼正確**
**EBS Snapshots** 以增量方式儲存，只保存上次快照後變更的區塊；**EFS Infrequent Access** 儲存成本較低，但讀取或寫入低頻層資料會產生存取費用。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon EBS Snapshot storage pricing is based on the amount of space your data consumes in Amazon EBS／EBS 快照定價基於 EBS 中佔用空間 | ❌ 錯誤 | 快照儲存在 S3，依快照實際儲存資料量計費，不是 EBS 磁碟宣告容量。 |
| With AWS Backup... need not pay for restoring this data／EFS 備份還原不需付費 | ❌ 錯誤 | 備份還原可能有還原費用或相關費用。 |
| Amazon EC2 data transfer charges will apply for all Amazon EBS direct APIs for Snapshots／所有 EBS direct APIs 都收 EC2 傳輸費 | ❌ 錯誤 | 此說法過度概括，非本題正確定價重點。 |
| Amazon EBS Snapshots are stored incrementally／EBS 快照增量儲存 | ✅ 正確 | EBS 快照只為儲存的變更區塊計費。 |
| You will pay a fee each time you read from or write data stored on EFS-IA／每次讀寫 EFS-IA 需付費 | ✅ 正確 | EFS-IA 有低儲存費與資料存取費。 |

---

## 問題 47

**題目**
Which of the following is the best way to protect your data from accidental deletion on Amazon S3?
以下哪項是保護 Amazon S3 上資料免遭意外刪除的最佳方式？

**[選項]**
- A. Amazon S3 lifecycle configuration／生命週期設定
- B. Amazon S3 storage classes／儲存類別
- C. Amazon S3 Transfer Acceleration (Amazon S3TA)／傳輸加速
- D. Amazon S3 Versioning／版本控制

**正確答案**
Amazon S3 Versioning／版本控制

**為什麼正確**
**S3 Versioning** 會保留物件的多個版本；刪除物件時會加入刪除標記，舊版本仍可恢復，可防止意外刪除造成資料永久遺失。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3 lifecycle configuration／生命週期設定 | ❌ 錯誤 | Lifecycle 用於自動轉換儲存類別或過期刪除，反而可能刪除資料。 |
| Amazon S3 storage classes／儲存類別 | ❌ 錯誤 | 儲存類別影響成本、可用性與取回方式，不保護版本。 |
| Amazon S3 Transfer Acceleration (Amazon S3TA)／傳輸加速 | ❌ 錯誤 | Transfer Acceleration 加速遠距離上傳/下載。 |
| Amazon S3 Versioning／版本控制 | ✅ 正確 | Versioning 可保留舊版本並復原誤刪。 |

---

## 問題 48

**題目**
What is the primary benefit of deploying an Amazon RDS database in a Read Replica configuration?
在讀取副本設定中部署 Amazon RDS 資料庫的主要優點是什麼？

**[選項]**
- A. Read Replica reduces database usage costs／讀取副本降低資料庫使用成本
- B. Read Replica protects the database from a regional failure／讀取副本保護資料庫免受區域故障影響
- C. Read Replica enhances database availability／讀取副本提升資料庫可用性
- D. Read Replica improves database scalability／讀取副本提升資料庫可擴展性

**正確答案**
Read Replica improves database scalability／讀取副本提升資料庫可擴展性

**為什麼正確**
**RDS Read Replica** 透過非同步複寫建立可處理讀取流量的副本，主要目的是分散讀取請求、提升讀取擴展性。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Read Replica reduces database usage costs／降低資料庫使用成本 | ❌ 錯誤 | 讀取副本會增加資源，不是降成本主要功能。 |
| Read Replica protects the database from a regional failure／保護免受區域故障 | ❌ 錯誤 | 跨區域讀取副本可協助 DR，但 Read Replica 的主要考點是讀取擴展。 |
| Read Replica enhances database availability／提升資料庫可用性 | ❌ 錯誤 | 高可用主要是 Multi-AZ。 |
| Read Replica improves database scalability／提升資料庫可擴展性 | ✅ 正確 | Read Replica 主要改善讀取可擴展性。 |

---

## 問題 49

**題目**
Which AWS services/features support High Availability by default? (Select two)
以下哪些 AWS 服務/功能預設支援高可用性？（選兩項）

**[選項]**
- A. Amazon Elastic Block Store (Amazon EBS)／區塊儲存
- B. Subnet／子網路
- C. Instance Store／執行個體存放區
- D. Amazon Elastic File System (Amazon EFS)／檔案系統
- E. Amazon DynamoDB／NoSQL 資料庫

**正確答案**
Amazon Elastic File System (Amazon EFS)／檔案系統；Amazon DynamoDB／NoSQL 資料庫

**為什麼正確**
**Amazon EFS** 是區域型服務，跨多個 AZ 儲存資料；**DynamoDB** 預設跨多個 AZ 複寫資料，兩者都具備預設高可用特性。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic Block Store (Amazon EBS)／區塊儲存 | ❌ 錯誤 | EBS 磁碟區位於單一 AZ，雖在 AZ 內複寫，但不是跨 AZ 高可用。 |
| Subnet／子網路 | ❌ 錯誤 | Subnet 只存在於單一 AZ。 |
| Instance Store／執行個體存放區 | ❌ 錯誤 | Instance Store 是本機暫時性儲存，不具預設高可用。 |
| Amazon Elastic File System (Amazon EFS)／檔案系統 | ✅ 正確 | EFS 預設跨多 AZ 提供高可用檔案存取。 |
| Amazon DynamoDB／NoSQL 資料庫 | ✅ 正確 | DynamoDB 預設跨多 AZ 複寫以提供高可用。 |

---

## 問題 50

**題目**
An organization maintains separate Amazon VPCs for each of its departments. The organization now wants to connect all VPCs for better departmental collaboration. Which AWS service will help effectively?
一個組織為每個部門維護獨立的 Amazon VPC。組織現在希望連接所有 VPC 以促進部門協作。哪個 AWS 服務可以有效幫助解決此問題？

**[選項]**
- A. AWS Direct Connect／專用網路連線
- B. AWS Site-to-Site VPN／站台對站台 VPN
- C. VPC peering connection／VPC 對等連線
- D. AWS Transit Gateway／轉接閘道

**正確答案**
AWS Transit Gateway／轉接閘道

**為什麼正確**
**AWS Transit Gateway** 是 Hub-and-Spoke 網路中樞，可集中連接多個 VPC 與本地網路，適合大量 VPC 互連，管理上比多個 VPC Peering 更有效率。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Direct Connect／專用網路連線 | ❌ 錯誤 | Direct Connect 主要連接本地資料中心與 AWS。 |
| AWS Site-to-Site VPN／站台對站台 VPN | ❌ 錯誤 | Site-to-Site VPN 主要用於本地網路與 VPC 連線。 |
| VPC peering connection／VPC 對等連線 | ❌ 錯誤 | VPC Peering 適合少量 VPC 點對點連接，不支援傳遞路由，大量 VPC 管理複雜。 |
| AWS Transit Gateway／轉接閘道 | ✅ 正確 | Transit Gateway 可集中有效連接多個 VPC。 |

---

## 問題 51

**題目**
Which of the following capabilities does Amazon Rekognition provide as a ready-to-use feature?
以下哪些功能是 Amazon Rekognition 提供的即用型功能？

**[選項]**
- A. Resize images quickly／快速調整圖片大小
- B. Convert images into greyscale／將圖片轉換為灰階
- C. Human pose detection／人體姿勢偵測
- D. Identify objects in a photo／識別照片中的物件

**正確答案**
Identify objects in a photo／識別照片中的物件

**為什麼正確**
**Amazon Rekognition** 提供開箱即用的影像與影片分析能力，可識別照片中的物件、人物、文字、場景與活動。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Resize images quickly／快速調整圖片大小 | ❌ 錯誤 | 圖片縮放是影像處理任務，不是 Rekognition 分析能力。 |
| Convert images into greyscale／將圖片轉換為灰階 | ❌ 錯誤 | 轉灰階是影像轉換，不是 Rekognition 功能。 |
| Human pose detection／人體姿勢偵測 | ❌ 錯誤 | 題庫中 Rekognition 的即用功能重點不是人體姿態偵測。 |
| Identify objects in a photo／識別照片中的物件 | ✅ 正確 | Rekognition 可辨識圖片中的物件與場景。 |

---

## 問題 52

**題目**
What is the region-specific constraint that the Amazon Machine Image (AMI) must meet so that it can be used for an Amazon EC2 instance?
Amazon Machine Image（AMI）必須滿足哪些特定區域限制才能用於 Amazon EC2 執行個體？

**[選項]**
- A. You can use an AMI from a different region, but it degrades the performance of the EC2 instance／可使用不同區域 AMI，但會降低效能
- B. An AMI is a global entity, so the region is not applicable／AMI 是全球實體
- C. You should use an AMI from the same region, as it improves the performance of the EC2 instance／應使用相同區域 AMI，因為提升效能
- D. You must use an AMI from the same region as that of the EC2 instance. The region of the AMI has no bearing on the performance of the EC2 instance／必須使用同區域 AMI，AMI 區域不影響效能

**正確答案**
You must use an AMI from the same region as that of the EC2 instance. The region of the AMI has no bearing on the performance of the EC2 instance／必須使用與 EC2 同區域的 AMI，AMI 區域不影響效能

**為什麼正確**
AMI 是區域型資源，啟動 EC2 時必須使用同一 Region 的 AMI。若要跨 Region 使用，需要先複製 AMI；區域限制是可用性限制，不是效能優化。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| You can use an AMI from a different region, but it degrades performance／可使用不同區域 AMI 但降低效能 | ❌ 錯誤 | 不能直接用不同 Region 的 AMI 啟動 EC2。 |
| An AMI is a global entity／AMI 是全球實體 | ❌ 錯誤 | AMI 是區域型資源。 |
| You should use an AMI from the same region, as it improves performance／同區域 AMI 提升效能 | ❌ 錯誤 | 同區域是必要條件，不是效能原因。 |
| You must use an AMI from the same region...／必須使用同區域 AMI | ✅ 正確 | EC2 必須使用同 Region AMI，跨區需先複製。 |

---

## 問題 53

**題目**
Which AWS service can be used as an in-memory database with high-performance and low latency?
哪個 AWS 服務可用作高效能、低延遲的記憶體內資料庫？

**[選項]**
- A. Amazon DynamoDB／NoSQL 資料庫
- B. Amazon Athena／互動式查詢
- C. Amazon Relational Database Service (Amazon RDS)／關聯式資料庫
- D. Amazon ElastiCache／記憶體快取

**正確答案**
Amazon ElastiCache／記憶體快取

**為什麼正確**
**Amazon ElastiCache** 是受管記憶體資料存放服務，支援 Redis 與 Memcached，提供高效能、低延遲的快取與 in-memory database 能力。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon DynamoDB／NoSQL 資料庫 | ❌ 錯誤 | DynamoDB 是 NoSQL 資料庫，但不是 in-memory database。 |
| Amazon Athena／互動式查詢 | ❌ 錯誤 | Athena 用 SQL 查詢 S3 資料，不是記憶體資料庫。 |
| Amazon RDS／關聯式資料庫 | ❌ 錯誤 | RDS 是受管關聯式資料庫，不是記憶體快取。 |
| Amazon ElastiCache／記憶體快取 | ✅ 正確 | ElastiCache 提供 Redis/Memcached 記憶體資料存取。 |

---

## 問題 54

**題目**
Which of the following statements are CORRECT regarding security groups and network access control lists (network ACL)? (Select two)
以下哪些陳述關於安全群組和網路存取控制清單（network ACL）是正確的？（選兩項）

**[選項]**
- A. A network ACL is stateful, that is, it automatically allows the return traffic／NACL 是有狀態
- B. A security group contains a numbered list of rules and evaluates these rules in the increasing order／安全群組按編號順序評估
- C. A security group is stateless, that is, the return traffic must be explicitly allowed／安全群組是無狀態
- D. A network ACL contains a numbered list of rules and evaluates these rules in the increasing order／NACL 有編號規則並按遞增順序評估
- E. A security group is stateful, that is, it automatically allows the return traffic／安全群組是有狀態

**正確答案**
A network ACL contains a numbered list of rules and evaluates these rules in the increasing order／NACL 有編號規則並按遞增順序評估；A security group is stateful／安全群組是有狀態

**為什麼正確**
**Security Group** 是有狀態，回應流量會自動允許；**Network ACL** 是無狀態，使用有編號的規則並按編號由小到大評估。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| A network ACL is stateful／NACL 是有狀態 | ❌ 錯誤 | NACL 是無狀態。 |
| A security group contains a numbered list of rules／安全群組按編號順序評估 | ❌ 錯誤 | 安全群組沒有 NACL 那種編號順序評估規則。 |
| A security group is stateless／安全群組是無狀態 | ❌ 錯誤 | 安全群組是有狀態。 |
| A network ACL contains a numbered list of rules...／NACL 有編號規則並按遞增順序評估 | ✅ 正確 | NACL 規則按編號順序處理。 |
| A security group is stateful...／安全群組是有狀態 | ✅ 正確 | 安全群組會自動允許回傳流量。 |

---

## 問題 55

**題目**
A company has a static website hosted on an Amazon S3 bucket in Asia. It wants to drive growth globally. How can it improve the global performance of its static website?
一家公司在亞洲的 Amazon S3 儲存貯體上託管靜態網站，現在希望推動全球增長。如何提升其靜態網站的全球效能？

**[選項]**
- A. Use AWS Web Application Firewall (AWS WAF) to improve the performance of your website／使用 WAF 提升效能
- B. Use AWS CloudFormation to improve the performance of your website／使用 CloudFormation 提升效能
- C. Use Amazon S3 Transfer Acceleration (Amazon S3TA) to improve the performance of your website／使用 S3TA 提升效能
- D. Use Amazon CloudFront to improve the performance of your website／使用 CloudFront 提升效能

**正確答案**
Use Amazon CloudFront to improve the performance of your website／使用 CloudFront 提升效能

**為什麼正確**
**Amazon CloudFront** 是全球 CDN，可將靜態網站內容快取到靠近使用者的邊緣節點，降低延遲並提升全球讀取效能。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Use AWS WAF／使用 WAF | ❌ 錯誤 | WAF 是安全防護服務，不是效能加速服務。 |
| Use AWS CloudFormation／使用 CloudFormation | ❌ 錯誤 | CloudFormation 用於佈建基礎設施。 |
| Use Amazon S3 Transfer Acceleration／使用 S3TA | ❌ 錯誤 | S3 Transfer Acceleration 主要加速上傳/傳輸到 S3，不是靜態網站全球讀取快取首選。 |
| Use Amazon CloudFront／使用 CloudFront | ✅ 正確 | CloudFront 可透過全球邊緣節點提升靜態網站效能。 |

---

## 問題 56

**題目**
According to the AWS Shared Responsibility Model, which of the following are the responsibilities of the customer? (Select two)
根據 AWS 共同責任模型，以下哪些是客戶的責任？（選兩項）

**[選項]**
- A. Ensuring AWS employees cannot access customer data／確保 AWS 員工無法存取客戶資料
- B. Compliance validation of Cloud infrastructure／雲端基礎設施合規驗證
- C. AWS Global Network Security／AWS 全球網路安全
- D. Operating system patches and updates of an Amazon EC2 instance／EC2 作業系統修補與更新
- E. Managing IAM users and roles／管理 IAM 使用者和角色

**正確答案**
Operating system patches and updates of an Amazon EC2 instance／EC2 作業系統修補與更新；Managing IAM users and roles／管理 IAM 使用者和角色

**為什麼正確**
在共同責任模型中，客戶負責雲端中的安全。對 EC2，客戶負責 guest OS 修補；IAM 使用者、角色與權限管理也屬於客戶責任。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Ensuring AWS employees cannot access customer data／確保 AWS 員工無法存取客戶資料 | ❌ 錯誤 | AWS 負責其員工與基礎設施存取控制。 |
| Compliance validation of Cloud infrastructure／雲端基礎設施合規驗證 | ❌ 錯誤 | AWS 負責雲端基礎設施的合規驗證與控制。 |
| AWS Global Network Security／AWS 全球網路安全 | ❌ 錯誤 | AWS 全球網路安全屬於 AWS 責任。 |
| Operating system patches and updates of an Amazon EC2 instance／EC2 作業系統修補與更新 | ✅ 正確 | EC2 guest OS 修補由客戶負責。 |
| Managing IAM users and roles／管理 IAM 使用者和角色 | ✅ 正確 | IAM 身分與權限配置由客戶負責。 |

---

## 問題 57

**題目**
Which of the following Cloud Computing models does the 'gmail' service represent?
以下哪個雲端運算模型代表了「gmail」服務？

**[選項]**
- A. Infrastructure as a service (IaaS)／基礎設施即服務
- B. Platform as a service (PaaS)／平台即服務
- C. Function as a service (FaaS)／函數即服務
- D. Software as a service (SaaS)／軟體即服務

**正確答案**
Software as a service (SaaS)／軟體即服務

**為什麼正確**
**Gmail** 是使用者直接透過瀏覽器或 App 使用的完整軟體服務，底層平台和基礎設施由供應商管理，屬於 SaaS。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Infrastructure as a service (IaaS)／基礎設施即服務 | ❌ 錯誤 | IaaS 提供虛擬伺服器、網路和儲存等基礎設施。 |
| Platform as a service (PaaS)／平台即服務 | ❌ 錯誤 | PaaS 提供應用開發和部署平台。 |
| Function as a service (FaaS)／函數即服務 | ❌ 錯誤 | FaaS 代表事件驅動函數運算，例如 Lambda。 |
| Software as a service (SaaS)／軟體即服務 | ✅ 正確 | Gmail 是完整應用服務，屬於 SaaS。 |

---

## 問題 58

**題目**
As per the AWS Shared Responsibility Model, which of the following security services/utilities falls under the purview of AWS?
根據 AWS 共同責任模型，以下哪些安全服務/工具屬於 AWS 的管轄範圍？

**[選項]**
- A. Security group／安全群組
- B. AWS Shield Advanced／進階 DDoS 防護
- C. AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆
- D. AWS Shield Standard／標準 DDoS 防護

**正確答案**
AWS Shield Standard／標準 DDoS 防護

**為什麼正確**
**AWS Shield Standard** 對所有 AWS 客戶自動啟用，無需客戶配置，屬於 AWS 端提供與維護的基礎 DDoS 防護。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Security group／安全群組 | ❌ 錯誤 | Security Group 規則由客戶配置與管理。 |
| AWS Shield Advanced／進階 DDoS 防護 | ❌ 錯誤 | Shield Advanced 需客戶訂閱並配置受保護資源。 |
| AWS Web Application Firewall (AWS WAF)／Web 應用程式防火牆 | ❌ 錯誤 | WAF Web ACL 和規則由客戶配置。 |
| AWS Shield Standard／標準 DDoS 防護 | ✅ 正確 | Shield Standard 自動為 AWS 客戶啟用，由 AWS 管理。 |

---

## 問題 59

**題目**
Which of the following are correct statements regarding the AWS Shared Responsibility Model? (Select two)
以下哪些陳述關於 AWS 共同責任模型是正確的？（選兩項）

**[選項]**
- A. Configuration Management is the responsibility of the customer／設定管理是客戶責任
- B. For a service like Amazon EC2 (IaaS), AWS is responsible for maintaining guest operating system／EC2 的 guest OS 由 AWS 維護
- C. AWS is responsible for training AWS and customer employees on AWS products and services／AWS 負責培訓 AWS 與客戶員工
- D. For abstracted services like Amazon S3, AWS operates the infrastructure layer, the operating system, and platforms／S3 等抽象服務由 AWS 維運基礎設施、OS 和平台
- E. AWS is responsible for Security 'of' the Cloud／AWS 負責雲端的安全性

**正確答案**
For abstracted services like Amazon S3, AWS operates the infrastructure layer, the operating system, and platforms／S3 等抽象服務由 AWS 維運基礎設施、OS 和平台；AWS is responsible for Security 'of' the Cloud／AWS 負責雲端的安全性

**為什麼正確**
AWS 負責 **Security of the Cloud**，也就是底層硬體、軟體、網路與設施。對 S3 這類抽象服務，AWS 也負責基礎設施層、作業系統與平台營運。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Configuration Management is the responsibility of the customer／設定管理是客戶責任 | ❌ 錯誤 | 設定管理是共同責任；AWS 管底層，客戶管自己的資源與應用設定。 |
| For EC2, AWS is responsible for maintaining guest OS／EC2 guest OS 由 AWS 維護 | ❌ 錯誤 | EC2 guest OS 由客戶負責維護和修補。 |
| AWS is responsible for training AWS and customer employees／AWS 負責培訓雙方員工 | ❌ 錯誤 | AWS 訓練 AWS 員工；客戶負責訓練自己的員工。 |
| For abstracted services like S3, AWS operates infrastructure, OS, platforms／S3 抽象服務由 AWS 維運底層 | ✅ 正確 | S3 底層基礎設施、OS 和平台由 AWS 管理。 |
| AWS is responsible for Security 'of' the Cloud／AWS 負責雲端的安全性 | ✅ 正確 | AWS 負責雲端本身的安全。 |

---

## 問題 60

**題目**
An IT company wants to identify all Amazon EC2 instances that are under-utilized. Which AWS services can be used off-the-shelf to address this use-case without needing any manual configurations? (Select two)
一家 IT 公司希望識別所有未充分使用的 Amazon EC2 執行個體。哪些 AWS 服務可以開箱即用地解決此使用案例，無需任何手動設定？（選兩項）

**[選項]**
- A. Amazon CloudWatch／監控服務
- B. AWS Cost & Usage Report (AWS CUR)／成本與用量報告
- C. AWS Budgets／預算管理
- D. AWS Cost Explorer／成本分析
- E. AWS Trusted Advisor／最佳實務建議

**正確答案**
AWS Cost Explorer／成本分析；AWS Trusted Advisor／最佳實務建議

**為什麼正確**
**AWS Trusted Advisor** 可提供低使用率 EC2 檢查；**AWS Cost Explorer** 提供 rightsizing 建議，可找出低使用率 EC2。兩者不需要自行建立 CloudWatch 告警規則。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon CloudWatch／監控服務 | ❌ 錯誤 | CloudWatch 可監控指標，但需要自行設定閾值與告警。 |
| AWS Cost & Usage Report (AWS CUR)／成本與用量報告 | ❌ 錯誤 | CUR 提供詳細成本資料，但不是開箱即用的低使用率 EC2 建議工具。 |
| AWS Budgets／預算管理 | ❌ 錯誤 | Budgets 用於預算與告警，不識別低使用率 EC2。 |
| AWS Cost Explorer／成本分析 | ✅ 正確 | Cost Explorer 可提供 EC2 rightsizing 建議。 |
| AWS Trusted Advisor／最佳實務建議 | ✅ 正確 | Trusted Advisor 可檢查低使用率 EC2 執行個體。 |

---

## 問題 61

**題目**
A medical device company is looking for a durable and cost-effective way of storing their historic data. Due to compliance requirements, the data must be stored for 10 years. Which AWS Storage solution will you suggest?
一家醫療設備公司正在尋找儲存其歷史資料的耐用且具成本效益的方式。由於合規要求，資料必須儲存 10 年。您會建議哪個 AWS 儲存解決方案？

**[選項]**
- A. Amazon Elastic File System (Amazon EFS)／檔案系統
- B. Amazon S3 Glacier Flexible Retrieval／Glacier 彈性取回
- C. AWS Storage Gateway／儲存閘道
- D. Amazon S3 Glacier Deep Archive／Glacier 深度封存

**正確答案**
Amazon S3 Glacier Deep Archive／Glacier 深度封存

**為什麼正確**
**S3 Glacier Deep Archive** 是 AWS 成本最低的 S3 儲存類別之一，專為長期保存和合規封存設計，適合需保存 7 到 10 年以上且很少取回的資料。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic File System (Amazon EFS)／檔案系統 | ❌ 錯誤 | EFS 是共享檔案系統，不是低成本長期封存。 |
| Amazon S3 Glacier Flexible Retrieval／Glacier 彈性取回 | ❌ 錯誤 | 適合一般封存，但 10 年合規長期保存通常 Deep Archive 成本更低。 |
| AWS Storage Gateway／儲存閘道 | ❌ 錯誤 | Storage Gateway 是混合雲儲存整合，不是長期封存儲存類別。 |
| Amazon S3 Glacier Deep Archive／Glacier 深度封存 | ✅ 正確 | Deep Archive 最適合長期、耐用、低成本合規封存。 |

---

## 問題 62

**題目**
Which of the following statements are true about Cost Allocation Tags in AWS Billing? (Select two)
以下哪些陳述關於 AWS 計費中的成本分配標籤是正確的？（選兩項）

**[選項]**
- A. Tags help in organizing resources and are a mandatory configuration item to run reports／標籤是執行報告必要設定
- B. For each resource, each tag key must be unique, but can have multiple values／每個資源的標籤鍵唯一但可多值
- C. Only user-defined tags need to be activated before they can appear in Cost Explorer or on a cost allocation report／只需啟用使用者定義標籤
- D. For each resource, each tag key must be unique, and each tag key can have only one value／每個資源每個標籤鍵唯一且只能有一個值
- E. You must activate both AWS generated tags and user-defined tags separately before they can appear in Cost Explorer or on a cost allocation report／AWS 生成和使用者定義標籤都需分別啟用

**正確答案**
For each resource, each tag key must be unique, and each tag key can have only one value／每個資源每個標籤鍵唯一且只能有一個值；You must activate both AWS generated tags and user-defined tags separately／兩類標籤都需分別啟用

**為什麼正確**
每個資源上的標籤鍵必須唯一，且每個鍵只能有一個值。若要讓成本分配標籤出現在 Cost Explorer 或成本分配報告中，AWS 生成標籤和使用者定義標籤都需要分別啟用。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Tags are mandatory to run reports／標籤是執行報告必要設定 | ❌ 錯誤 | 標籤有助於整理與分攤成本，但不是執行成本報告的必要條件。 |
| Each tag key must be unique, but can have multiple values／標籤鍵可多值 | ❌ 錯誤 | 同一資源上每個標籤鍵只能有一個值。 |
| Only user-defined tags need to be activated／只需啟用使用者定義標籤 | ❌ 錯誤 | AWS 生成標籤也需要分別啟用。 |
| Each tag key must be unique and can have only one value／標籤鍵唯一且單值 | ✅ 正確 | 這是標籤鍵值規則。 |
| Activate both AWS generated tags and user-defined tags separately／兩類標籤都需分別啟用 | ✅ 正確 | 兩類成本分配標籤需分別啟用才會出現在成本工具中。 |

---

## 問題 63

**題目**
AWS Trusted Advisor analyzes your AWS environment and provides best practice recommendations for which of the following categories? (Select two)
AWS Trusted Advisor 分析您的 AWS 環境並為以下哪些類別提供最佳實務建議？（選兩項）

**[選項]**
- A. Change Management／變更管理
- B. Elasticity／彈性
- C. Documentation／文件
- D. Service Limits／服務限制
- E. Cost Optimization／成本優化

**正確答案**
Service Limits／服務限制；Cost Optimization／成本優化

**為什麼正確**
AWS Trusted Advisor 的檢查類別包含成本優化、安全性、容錯、效能和服務限制。題目中的正確類別是 **Service Limits** 與 **Cost Optimization**。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Change Management／變更管理 | ❌ 錯誤 | 不是 Trusted Advisor 的五大建議類別。 |
| Elasticity／彈性 | ❌ 錯誤 | 彈性是雲端設計概念，不是 Trusted Advisor 類別。 |
| Documentation／文件 | ❌ 錯誤 | Documentation 不是 Trusted Advisor 檢查類別。 |
| Service Limits／服務限制 | ✅ 正確 | Trusted Advisor 可提醒服務使用量接近限制。 |
| Cost Optimization／成本優化 | ✅ 正確 | Trusted Advisor 可提供節省成本建議。 |

---

## 問題 64

**題目**
Which AWS service will you use if you have to move large volumes of on-premises data to AWS Cloud from a remote location with limited bandwidth?
如果您必須從頻寬有限的遠端位置將大量本地資料移動至 AWS 雲端，您會使用哪個 AWS 服務？

**[選項]**
- A. AWS Virtual Private Network (VPN)／虛擬私有網路
- B. AWS Direct Connect／專用網路連線
- C. AWS Transit Gateway／轉接閘道
- D. AWS Snowball／資料遷移設備

**正確答案**
AWS Snowball／資料遷移設備

**為什麼正確**
**AWS Snowball** 使用實體設備離線搬移大量資料，適合遠端位置頻寬有限、線上傳輸耗時過長的資料遷移場景。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Virtual Private Network (VPN)／虛擬私有網路 | ❌ 錯誤 | VPN 仍依賴網路頻寬，對大量資料且頻寬受限不理想。 |
| AWS Direct Connect／專用網路連線 | ❌ 錯誤 | Direct Connect 適合長期專線連接，但建置需要時間且仍是線上傳輸。 |
| AWS Transit Gateway／轉接閘道 | ❌ 錯誤 | Transit Gateway 是網路互連中樞，不搬移資料。 |
| AWS Snowball／資料遷移設備 | ✅ 正確 | Snowball 透過實體設備搬移大量資料，適合頻寬受限環境。 |

---

## 問題 65

**題目**
Amazon CloudWatch billing metric data is stored in which AWS Region?
Amazon CloudWatch 帳單指標資料儲存在哪個 AWS 區域？

**[選項]**
- A. In the AWS Region where the AWS resource is provisioned／在佈建資源的區域
- B. In the AWS Region where the AWS account is created／在建立帳戶的區域
- C. US West (N. California) - us-west-1
- D. US East (N. Virginia) - us-east-1

**正確答案**
US East (N. Virginia) - us-east-1

**為什麼正確**
CloudWatch 帳單指標資料一律儲存在 **US East (N. Virginia) - us-east-1**，代表全域 AWS 帳單估算費用資料。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| In the AWS Region where the AWS resource is provisioned／在佈建資源的區域 | ❌ 錯誤 | 帳單指標不是依資源所在區域分散儲存。 |
| In the AWS Region where the AWS account is created／在建立帳戶的區域 | ❌ 錯誤 | AWS 帳戶不以建立區域決定帳單指標位置。 |
| US West (N. California) - us-west-1 | ❌ 錯誤 | CloudWatch billing metrics 不儲存在 us-west-1。 |
| US East (N. Virginia) - us-east-1 | ✅ 正確 | 帳單指標資料儲存在 us-east-1。 |

---
