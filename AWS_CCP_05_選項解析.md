# AWS CCP 04 選項解析

來源：
- 題目與選項：[AWS_CCP_Practice_Test4.md](AWS_CCP_Practice_Test4.md)
- 原詳解：[AWS_CCP_04.md](AWS_CCP_04.md)

這份檔案針對每題列出中英對照題目與選項，並用中文說明正確答案與其他選項的差異。

---

## 問題 1

**題目**
Which AWS service would you use to create a logically isolated section of the AWS Cloud where you can launch AWS resources in your virtual network?
您會使用哪個 AWS 服務來建立 AWS 雲端的邏輯隔離區段，以便在您的虛擬網路中啟動 AWS 資源？

**[選項]**
- A. Virtual Private Network (VPN)／虛擬私有網路
- B. Network Access Control List (Network ACL)／網路存取控制清單
- C. Subnet／子網路
- D. Virtual Private Cloud (VPC)／虛擬私有雲

**正確答案**
Virtual Private Cloud (VPC)／虛擬私有雲

**為什麼正確**
**Amazon VPC** 可在 AWS 雲端中建立邏輯隔離的虛擬網路，讓您控制 IP 位址範圍、子網路、路由表、網路閘道與安全設定，並在其中啟動 AWS 資源。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Virtual Private Network (VPN)／虛擬私有網路 | ❌ 錯誤 | VPN 是加密連線，用於連接本地網路與 AWS，不是建立 AWS 邏輯隔離網路區段的服務。 |
| Network Access Control List (Network ACL)／網路存取控制清單 | ❌ 錯誤 | Network ACL 是子網路層級的安全控制，不是建立虛擬網路本身。 |
| Subnet／子網路 | ❌ 錯誤 | Subnet 是 VPC 內的 IP 範圍，不是建立整個隔離區段的服務。 |
| Virtual Private Cloud (VPC)／虛擬私有雲 | ✅ 正確 | VPC 是 AWS 中邏輯隔離的虛擬網路。 |

---

## 問題 2

**題目**
An organization maintains a separate Virtual Private Cloud (VPC) for each of its business units. Two units need to privately share data. Which is the most optimal way of privately sharing data between the two VPCs?
一個組織為每個業務單位維護獨立的 VPC。兩個單位需要私下共享資料。在兩個 VPC 之間私下共享資料的最佳方式是什麼？

**[選項]**
- A. VPC Endpoint／VPC 端點
- B. AWS Direct Connect／專用網路連線
- C. AWS Site-to-Site VPN／站台對站台 VPN
- D. VPC peering connection／VPC 對等連線

**正確答案**
VPC peering connection／VPC 對等連線

**為什麼正確**
**VPC Peering** 可在兩個 VPC 之間建立私有網路連線，讓兩邊資源使用私有 IP 通訊，適合兩個 VPC 之間的直接私有共享。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| VPC Endpoint／VPC 端點 | ❌ 錯誤 | VPC Endpoint 用於私下連接 VPC 與 AWS 服務，不是連接兩個 VPC。 |
| AWS Direct Connect／專用網路連線 | ❌ 錯誤 | Direct Connect 用於本地資料中心到 AWS 的專線。 |
| AWS Site-to-Site VPN／站台對站台 VPN | ❌ 錯誤 | Site-to-Site VPN 主要連接本地網路與 AWS VPC。 |
| VPC peering connection／VPC 對等連線 | ✅ 正確 | VPC Peering 是兩個 VPC 私有互連的最佳直接方案。 |

---

## 問題 3

**題目**
A financial services company wants to ensure that all customer data uploaded on its data lake on Amazon S3 always stays private. Which of the following is the MOST efficient solution to address this compliance requirement?
一家金融服務公司希望確保上傳至 Amazon S3 資料湖的所有客戶資料始終保持私有。以下哪個解決方案最有效率地滿足此合規要求？

**[選項]**
- A. Trigger a Lambda function every time an object is uploaded on S3 to change the object settings to make sure it stays private／每次上傳物件時觸發 Lambda 修改設定
- B. Use Amazon CloudWatch to ensure that all S3 resources stay private／使用 CloudWatch 確保 S3 保持私有
- C. Set up a high-level advisory committee to review the privacy settings of each object uploaded into S3／設立委員會審查每個物件隱私設定
- D. Use Amazon S3 Block Public Access to ensure that all S3 resources stay private／使用 S3 封鎖公開存取

**正確答案**
Use Amazon S3 Block Public Access to ensure that all S3 resources stay private／使用 S3 封鎖公開存取

**為什麼正確**
**Amazon S3 Block Public Access** 可在帳戶、儲存貯體或存取點層級封鎖公開存取設定，能有效防止 S3 資料因 ACL 或 bucket policy 而公開。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Trigger a Lambda function every time an object is uploaded／每次上傳觸發 Lambda | ❌ 錯誤 | 可以自訂修正，但反應式且複雜，效率不如 S3 Block Public Access。 |
| Use Amazon CloudWatch／使用 CloudWatch | ❌ 錯誤 | CloudWatch 用於監控與警示，不能直接保證 S3 資源私有。 |
| Set up a high-level advisory committee／設立委員會 | ❌ 錯誤 | 人工審查不即時也不具擴展性。 |
| Use Amazon S3 Block Public Access／使用 S3 封鎖公開存取 | ✅ 正確 | 可集中封鎖公開存取，最有效滿足合規要求。 |

---

## 問題 4

**題目**
Which of the following types are free under the Amazon S3 pricing model? (Select two)
以下哪些類型在 Amazon S3 定價模型下是免費的？（選兩項）

**[選項]**
- A. Data storage fee for objects stored in S3 Standard／S3 Standard 物件儲存費
- B. Data storage fee for objects stored in S3 Glacier／S3 Glacier 物件儲存費
- C. Data transferred out to an EC2 instance in any AWS Region／傳出到任何區域 EC2 的資料
- D. Data transferred in from the internet／從網際網路傳入的資料
- E. Data transferred out to an EC2 instance when the instance is in the same AWS Region as the S3 bucket／傳出到同區域 EC2 的資料

**正確答案**
Data transferred in from the internet／從網際網路傳入的資料；Data transferred out to an EC2 instance when the instance is in the same AWS Region as the S3 bucket／傳出到同區域 EC2 的資料

**為什麼正確**
S3 通常不收取從網際網路傳入 AWS 的資料傳輸費；S3 傳出到同一 AWS Region 的 EC2 也通常免費。儲存本身與跨區域/網際網路傳出則會收費。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Data storage fee for objects stored in S3 Standard／S3 Standard 儲存費 | ❌ 錯誤 | S3 Standard 會依儲存量收費。 |
| Data storage fee for objects stored in S3 Glacier／S3 Glacier 儲存費 | ❌ 錯誤 | Glacier 類儲存也會依儲存量收費。 |
| Data transferred out to an EC2 instance in any AWS Region／傳出到任何區域 EC2 | ❌ 錯誤 | 傳到不同 Region 的 EC2 可能產生資料傳輸費。 |
| Data transferred in from the internet／從網際網路傳入資料 | ✅ 正確 | 傳入 AWS 的資料通常免費。 |
| Data transferred out to an EC2 instance in the same Region／傳出到同區域 EC2 | ✅ 正確 | S3 到同 Region EC2 的資料傳輸通常免費。 |

---

## 問題 5

**題目**
An e-commerce company wants to review the Payment Card Industry (PCI) reports on AWS Cloud. Which AWS resource can be used to address this use-case?
一家電子商務公司希望審查 AWS 雲端上的 PCI 報告。哪個 AWS 資源可以滿足此使用案例？

**[選項]**
- A. AWS Trusted Advisor／最佳實務建議
- B. AWS Cost & Usage Report (AWS CUR)／成本與用量報告
- C. AWS Secrets Manager／機密管理
- D. AWS Artifact／合規報告入口

**正確答案**
AWS Artifact／合規報告入口

**為什麼正確**
**AWS Artifact** 是 AWS 合規報告與合約文件的自助式入口，可下載 PCI、SOC 等安全與合規報告。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Trusted Advisor／最佳實務建議 | ❌ 錯誤 | Trusted Advisor 提供最佳實務檢查，不提供 PCI 合規報告下載。 |
| AWS Cost & Usage Report (AWS CUR)／成本與用量報告 | ❌ 錯誤 | CUR 是成本與用量明細報告。 |
| AWS Secrets Manager／機密管理 | ❌ 錯誤 | Secrets Manager 用於管理密碼與機密。 |
| AWS Artifact／合規報告入口 | ✅ 正確 | Artifact 可取得 AWS PCI 等合規報告。 |

---

## 問題 6

**題目**
How is Amazon EC2 different from traditional hosting systems? (Select two)
Amazon EC2 與傳統託管系統有何不同？（選兩項）

**[選項]**
- A. With Amazon EC2, users risk overbuying resources／使用 EC2 有超購資源風險
- B. Amazon EC2 caters more towards groups of users with similar system requirements so that resources are shared and cost is reduced／EC2 偏向共享資源降低成本
- C. Amazon EC2 provides a pre-configured instance for a fixed monthly cost／EC2 固定月費提供預先設定執行個體
- D. With Amazon EC2, developers can launch and terminate the instances anytime they need to／可隨時啟動和終止執行個體
- E. Amazon EC2 can scale with changing computing requirements／可隨運算需求變化擴展

**正確答案**
With Amazon EC2, developers can launch and terminate the instances anytime they need to／可隨時啟動和終止執行個體；Amazon EC2 can scale with changing computing requirements／可隨需求擴展

**為什麼正確**
EC2 的核心優勢是按需啟動/終止執行個體、彈性擴展與按使用量付費，降低傳統託管中預先購買與容量不足/過剩的問題。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| With Amazon EC2, users risk overbuying resources／有超購資源風險 | ❌ 錯誤 | EC2 可按需啟停，降低超購風險。 |
| EC2 caters more towards groups of users with similar requirements／偏向共享資源 | ❌ 錯誤 | 這較像傳統共享主機描述，不是 EC2 的差異重點。 |
| EC2 provides a pre-configured instance for a fixed monthly cost／固定月費預設執行個體 | ❌ 錯誤 | EC2 主要是彈性配置與按量計費，不是固定月費託管。 |
| Developers can launch and terminate instances anytime／可隨時啟動和終止 | ✅ 正確 | EC2 可按需求建立和終止執行個體。 |
| EC2 can scale with changing requirements／可隨需求擴展 | ✅ 正確 | EC2 可因應運算需求彈性擴展。 |

---

## 問題 7

**題目**
Which AWS service would you choose for a data processing project that needs a schemaless database?
對於需要無結構描述資料庫的資料處理專案，您會選擇哪個 AWS 服務？

**[選項]**
- A. Amazon Aurora／雲端關聯式資料庫
- B. Amazon Relational Database Service (Amazon RDS)／關聯式資料庫
- C. Amazon RedShift／資料倉儲
- D. Amazon DynamoDB／NoSQL 資料庫

**正確答案**
Amazon DynamoDB／NoSQL 資料庫

**為什麼正確**
**Amazon DynamoDB** 是 NoSQL 鍵值與文件資料庫，支援彈性 schema，適合不需要固定表格結構的資料處理專案。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Aurora／雲端關聯式資料庫 | ❌ 錯誤 | Aurora 是關聯式資料庫，需要固定 schema。 |
| Amazon RDS／關聯式資料庫 | ❌ 錯誤 | RDS 是關聯式資料庫服務，非 schemaless。 |
| Amazon RedShift／資料倉儲 | ❌ 錯誤 | Redshift 是資料倉儲，使用結構化表格。 |
| Amazon DynamoDB／NoSQL 資料庫 | ✅ 正確 | DynamoDB 是 schemaless NoSQL 資料庫。 |

---

## 問題 8

**題目**
Which of the following statements are true regarding Amazon S3? (Select two)
以下哪些陳述關於 Amazon S3 是正確的？（選兩項）

**[選項]**
- A. Amazon S3 is a block storage service designed for a broad range of workloads／S3 是區塊儲存
- B. You can install databases on Amazon S3／可以在 S3 上安裝資料庫
- C. Amazon S3 is a fully managed, elastic file system storage service used as database backup／S3 是彈性檔案系統
- D. Amazon S3 stores data in a flat non-hierarchical structure／S3 以扁平非階層式結構儲存
- E. Amazon S3 is a key value based object storage service／S3 是鍵值型物件儲存

**正確答案**
Amazon S3 stores data in a flat non-hierarchical structure／S3 以扁平非階層式結構儲存；Amazon S3 is a key value based object storage service／S3 是鍵值型物件儲存

**為什麼正確**
S3 是物件儲存服務，物件以 key-value 形式存在 bucket 中。雖然可用前綴模擬資料夾，但底層是扁平命名空間。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3 is a block storage service／S3 是區塊儲存 | ❌ 錯誤 | 區塊儲存是 EBS，S3 是物件儲存。 |
| You can install databases on Amazon S3／可在 S3 安裝資料庫 | ❌ 錯誤 | S3 不是可安裝軟體的檔案系統或伺服器。 |
| Amazon S3 is an elastic file system／S3 是彈性檔案系統 | ❌ 錯誤 | EFS 才是彈性檔案系統。 |
| Amazon S3 stores data in a flat non-hierarchical structure／S3 以扁平結構儲存 | ✅ 正確 | S3 的物件命名空間是扁平的。 |
| Amazon S3 is a key value based object storage service／S3 是鍵值型物件儲存 | ✅ 正確 | S3 以物件 key 對應物件資料。 |

---

## 問題 9

**題目**
Which of the following describes an Availability Zone (AZ) in the AWS Cloud?
以下哪項描述了 AWS 雲端中的可用區域（AZ）？

**[選項]**
- A. One or more data centers in multiple locations／多個位置中的一個或多個資料中心
- B. One or more server racks in multiple locations／多個位置中的一個或多個伺服器機架
- C. One or more server racks in the same location／同一位置中的一個或多個伺服器機架
- D. One or more data centers in the same location／同一位置中的一個或多個資料中心

**正確答案**
One or more data centers in the same location／同一位置中的一個或多個資料中心

**為什麼正確**
**Availability Zone** 是一個或多個離散資料中心，具備獨立電力、網路與連線，位於同一區域內的相對獨立位置。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| One or more data centers in multiple locations／多個位置資料中心 | ❌ 錯誤 | 多個地理位置較接近 Region/多 AZ 概念，不是單一 AZ 定義。 |
| One or more server racks in multiple locations／多地伺服器機架 | ❌ 錯誤 | AZ 不是以伺服器機架定義。 |
| One or more server racks in the same location／同一位置伺服器機架 | ❌ 錯誤 | AZ 是資料中心層級，不是機架層級。 |
| One or more data centers in the same location／同一位置資料中心 | ✅ 正確 | AZ 由同一位置的一個或多個資料中心組成。 |

---

## 問題 10

**題目**
Which of the following statements are CORRECT regarding AWS Global Accelerator? (Select two)
以下哪些陳述關於 AWS Global Accelerator 是正確的？（選兩項）

**[選項]**
- A. AWS Global Accelerator can be used to host static websites／可託管靜態網站
- B. AWS Global Accelerator cannot be configured with an Elastic Load Balancer (ELB)／無法與 ELB 設定
- C. AWS Global Accelerator uses edge locations different from Amazon CloudFront edge locations／使用與 CloudFront 不同的邊緣位置
- D. AWS Global Accelerator provides static IP addresses that act as a fixed entry point to your applications／提供靜態 IP 作為固定入口
- E. AWS Global Accelerator is a good fit for non-HTTP use cases／適合非 HTTP 使用案例

**正確答案**
AWS Global Accelerator provides static IP addresses that act as a fixed entry point to your applications／提供靜態 IP 作為固定入口；AWS Global Accelerator is a good fit for non-HTTP use cases／適合非 HTTP 使用案例

**為什麼正確**
**Global Accelerator** 提供靜態 Anycast IP 作為全球固定入口，透過 AWS 全球網路改善 TCP/UDP 應用效能，特別適合遊戲、IoT、VoIP 等非 HTTP 場景。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Can be used to host static websites／可託管靜態網站 | ❌ 錯誤 | 靜態網站託管可用 S3，內容加速可用 CloudFront。 |
| Cannot be configured with ELB／無法與 ELB 設定 | ❌ 錯誤 | Global Accelerator 可以指向 ALB/NLB 等端點。 |
| Uses edge locations different from CloudFront／使用不同邊緣位置 | ❌ 錯誤 | Global Accelerator 使用 AWS 全球邊緣網路，與 CloudFront 共享全球基礎設施。 |
| Provides static IP addresses／提供靜態 IP 固定入口 | ✅ 正確 | 靜態 IP 是 Global Accelerator 重要特性。 |
| Good fit for non-HTTP use cases／適合非 HTTP | ✅ 正確 | Global Accelerator 支援 TCP/UDP，適合非 HTTP 應用。 |

---

## 問題 11

**題目**
Which of the following are benefits of the AWS Web Application Firewall (AWS WAF)? (Select two)
以下哪些是 AWS WAF 的優點？（選兩項）

**[選項]**
- A. AWS WAF offers dedicated support from the DDoS Response Team (DRT) and advanced reporting／提供 DRT 支援與進階報告
- B. AWS WAF offers protection against all known infrastructure (Layer 3 and 4) attacks／防護所有第 3/4 層攻擊
- C. AWS WAF lets you monitor HTTP and HTTPS requests forwarded to Amazon Route 53／監控轉發到 Route 53 的 HTTP/HTTPS
- D. AWS WAF can block all requests except the ones that you allow／可封鎖除允許外的所有請求
- E. AWS WAF can check for the presence of SQL code that is likely to be malicious (known as SQL injection)／可檢查 SQL injection

**正確答案**
AWS WAF can block all requests except the ones that you allow／可封鎖除允許外的所有請求；AWS WAF can check for SQL injection／可檢查 SQL injection

**為什麼正確**
**AWS WAF** 是第 7 層 Web 應用程式防火牆，可用 Web ACL 規則允許/封鎖請求，並可偵測 SQL injection、XSS 等常見 Web 攻擊模式。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Offers DRT support and advanced reporting／提供 DRT 支援 | ❌ 錯誤 | DRT 支援是 AWS Shield Advanced 的能力。 |
| Protection against all Layer 3 and 4 attacks／防護第 3/4 層攻擊 | ❌ 錯誤 | 第 3/4 層 DDoS 防護主要由 AWS Shield 提供。 |
| Monitor requests forwarded to Route 53／監控 Route 53 請求 | ❌ 錯誤 | WAF 通常關聯 CloudFront、ALB、API Gateway 等，不是 Route 53。 |
| Block all requests except allowed ones／只允許白名單請求 | ✅ 正確 | WAF 可建立白名單式規則。 |
| Check for SQL injection／檢查 SQL injection | ✅ 正確 | WAF 可偵測並封鎖 SQL injection。 |

---

## 問題 12

**題目**
The DevOps team at an IT company wants to centrally manage its servers on AWS Cloud as well as on-premise data center so that it can collect software inventory, run commands, configure and patch servers at scale. Which AWS service would you recommend?
一家 IT 公司的 DevOps 團隊希望集中管理 AWS 雲端及本地資料中心的伺服器，以便大規模收集軟體庫存、執行命令、設定和修補伺服器。您會推薦哪個 AWS 服務？

**[選項]**
- A. AWS Config／資源組態追蹤
- B. AWS Service Catalog／服務目錄
- C. AWS CloudFormation／基礎設施即程式碼
- D. AWS Systems Manager／系統管理

**正確答案**
AWS Systems Manager／系統管理

**為什麼正確**
**AWS Systems Manager** 可跨 AWS 與本地環境管理伺服器，支援 Inventory、Run Command、Patch Manager、Session Manager 等營運管理能力。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Config／資源組態追蹤 | ❌ 錯誤 | Config 追蹤 AWS 資源組態與合規，不執行命令或修補伺服器。 |
| AWS Service Catalog／服務目錄 | ❌ 錯誤 | Service Catalog 管理已核准服務目錄。 |
| AWS CloudFormation／基礎設施即程式碼 | ❌ 錯誤 | CloudFormation 用於佈建資源，不做伺服器日常管理。 |
| AWS Systems Manager／系統管理 | ✅ 正確 | Systems Manager 可集中管理、盤點、執行命令與修補 AWS/本地伺服器。 |

---

## 問題 13

**題目**
Which AWS services can be used together to send alerts whenever the AWS account root user signs in? (Select two)
哪些 AWS 服務可以結合使用，在 AWS 帳戶根使用者登入時發送警報？（選兩項）

**[選項]**
- A. AWS Step Functions／工作流程編排
- B. Amazon Simple Queue Service (Amazon SQS)／訊息佇列
- C. AWS Lambda／無伺服器函數
- D. Amazon CloudWatch／監控與事件
- E. Amazon Simple Notification Service (Amazon SNS)／通知服務

**正確答案**
Amazon CloudWatch／監控與事件；Amazon Simple Notification Service (Amazon SNS)／通知服務

**為什麼正確**
可使用 **CloudWatch Events/EventBridge** 偵測 root 使用者登入事件，再透過 **SNS** 發送電子郵件或簡訊通知。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Step Functions／工作流程編排 | ❌ 錯誤 | Step Functions 用於編排流程，不是登入事件偵測與通知核心服務。 |
| Amazon SQS／訊息佇列 | ❌ 錯誤 | SQS 是佇列，不會直接發送警報給管理員。 |
| AWS Lambda／無伺服器函數 | ❌ 錯誤 | Lambda 可被事件觸發執行邏輯，但本題標準組合是 CloudWatch + SNS。 |
| Amazon CloudWatch／監控與事件 | ✅ 正確 | CloudWatch 可偵測 root 登入事件或建立事件規則。 |
| Amazon SNS／通知服務 | ✅ 正確 | SNS 可發送登入告警通知。 |

---

## 問題 14

**題目**
A multi-national organization wants to connect its on-premises data center with different VPCs for better collaboration. Which AWS services can be combined to build the MOST efficient solution? (Select two)
一家跨國組織希望將其本地資料中心與不同的 VPC 連接以促進協作。哪些 AWS 服務可以結合使用以建立最有效率的解決方案？（選兩項）

**[選項]**
- A. VPC peering connection／VPC 對等連線
- B. AWS Storage Gateway／儲存閘道
- C. Internet Gateway／網際網路閘道
- D. AWS Direct Connect／專用連線
- E. AWS Transit Gateway／轉接閘道

**正確答案**
AWS Direct Connect／專用連線；AWS Transit Gateway／轉接閘道

**為什麼正確**
**Direct Connect** 可提供本地資料中心到 AWS 的專用網路連線；**Transit Gateway** 作為中央樞紐連接多個 VPC，兩者結合適合本地到多 VPC 的高效架構。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| VPC peering connection／VPC 對等連線 | ❌ 錯誤 | Peering 適合少量 VPC 點對點互連，不適合本地到多 VPC 中央化連線。 |
| AWS Storage Gateway／儲存閘道 | ❌ 錯誤 | Storage Gateway 是混合雲儲存服務，不是網路中樞。 |
| Internet Gateway／網際網路閘道 | ❌ 錯誤 | Internet Gateway 讓 VPC 連網際網路，不是本地私有專線。 |
| AWS Direct Connect／專用連線 | ✅ 正確 | Direct Connect 建立本地到 AWS 的專用連線。 |
| AWS Transit Gateway／轉接閘道 | ✅ 正確 | Transit Gateway 集中連接多個 VPC 與本地網路。 |

---

## 問題 15

**題目**
Which of the following is the best practice for application architecture on AWS Cloud?
以下哪項是 AWS 雲端應用程式架構的最佳實務？

**[選項]**
- A. Use synchronous communication between components／元件間使用同步通訊
- B. Build tightly coupled components／建立緊耦合元件
- C. Build monolithic applications／建立單體式應用程式
- D. Build loosely coupled components／建立鬆耦合元件

**正確答案**
Build loosely coupled components／建立鬆耦合元件

**為什麼正確**
AWS 架構最佳實務鼓勵建構**鬆耦合**元件，讓服務可獨立擴展、部署與故障隔離，常透過 SQS、SNS、EventBridge 等服務解耦。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Use synchronous communication／使用同步通訊 | ❌ 錯誤 | 同步耦合可能造成連鎖故障，非最佳實務。 |
| Build tightly coupled components／緊耦合 | ❌ 錯誤 | 緊耦合降低擴展性與韌性。 |
| Build monolithic applications／單體式應用 | ❌ 錯誤 | 單體式較難獨立擴展與部署。 |
| Build loosely coupled components／鬆耦合元件 | ✅ 正確 | 鬆耦合可提升可擴展性、韌性和維護性。 |

---

## 問題 16

**題目**
AWS Shield Advanced provides expanded DDoS attack protection for web applications running on which of the following resources? (Select two)
AWS Shield Advanced 為在以下哪些資源上執行的 Web 應用程式提供擴展的 DDoS 攻擊防護？（選兩項）

**[選項]**
- A. Amazon Simple Storage Service (Amazon S3)／物件儲存
- B. AWS Elastic Beanstalk／應用部署平台
- C. AWS Identity and Access Management (AWS IAM)／身分與存取管理
- D. Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器
- E. Amazon CloudFront／內容交付網路

**正確答案**
Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器；Amazon CloudFront／內容交付網路

**為什麼正確**
**AWS Shield Advanced** 可保護 CloudFront、Route 53、Global Accelerator、Elastic IP、ELB 和 EC2 等資源上的應用免受進階 DDoS 攻擊。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3／物件儲存 | ❌ 錯誤 | Shield Advanced 的典型受保護資源不包含直接保護 S3 bucket。 |
| AWS Elastic Beanstalk／應用部署平台 | ❌ 錯誤 | Beanstalk 是部署平台，底層可用受保護資源，但不是 Shield Advanced 直接列出的資源類型。 |
| AWS IAM／身分與存取管理 | ❌ 錯誤 | IAM 是身分服務，不是 Web 應用 DDoS 受保護端點。 |
| Amazon EC2／虛擬伺服器 | ✅ 正確 | Shield Advanced 可保護 EC2/Elastic IP 等資源。 |
| Amazon CloudFront／內容交付網路 | ✅ 正確 | CloudFront 是 Shield Advanced 支援的防護資源。 |

---

## 問題 17

**題目**
An e-commerce company has migrated its IT infrastructure from the on-premises data center to AWS Cloud. Which of the following costs is the company responsible for?
一家電子商務公司已將其 IT 基礎設施從本地資料中心遷移至 AWS 雲端。以下哪項成本由公司負責？

**[選項]**
- A. Costs for hardware infrastructure on AWS Cloud／AWS 硬體基礎設施成本
- B. AWS Data Center physical security costs／AWS 資料中心實體安全成本
- C. Costs for powering servers on AWS Cloud／AWS 伺服器電力成本
- D. Application software license costs／應用程式軟體授權成本

**正確答案**
Application software license costs／應用程式軟體授權成本

**為什麼正確**
遷移到 AWS 後，AWS 負責資料中心、硬體、電力與實體安全等底層成本；客戶仍需負責自身應用程式、授權與業務軟體成本。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Hardware infrastructure costs／硬體基礎設施成本 | ❌ 錯誤 | AWS 管理並承擔底層硬體設施。 |
| Data Center physical security costs／資料中心實體安全成本 | ❌ 錯誤 | AWS 負責資料中心實體安全。 |
| Costs for powering servers／伺服器電力成本 | ❌ 錯誤 | AWS 負責資料中心電力與冷卻等設施成本。 |
| Application software license costs／應用程式軟體授權成本 | ✅ 正確 | 客戶仍負責自身使用的應用軟體授權。 |

---

## 問題 18

**題目**
Which of the following are the serverless computing services offered by AWS? (Select two)
以下哪些是 AWS 提供的無伺服器運算服務？（選兩項）

**[選項]**
- A. Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器
- B. Amazon Lightsail／簡化 VPS
- C. AWS Elastic Beanstalk／應用部署平台
- D. AWS Fargate／無伺服器容器運算
- E. AWS Lambda／無伺服器函數

**正確答案**
AWS Fargate／無伺服器容器運算；AWS Lambda／無伺服器函數

**為什麼正確**
**AWS Lambda** 是無伺服器函數運算；**AWS Fargate** 是 ECS/EKS 可用的無伺服器容器運算引擎，兩者都不需要客戶管理伺服器。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon EC2／虛擬伺服器 | ❌ 錯誤 | EC2 需要管理執行個體。 |
| Amazon Lightsail／簡化 VPS | ❌ 錯誤 | Lightsail 是簡化 VPS，仍是伺服器型服務。 |
| AWS Elastic Beanstalk／應用部署平台 | ❌ 錯誤 | Beanstalk 會代管部署，但底層仍使用 EC2 等資源。 |
| AWS Fargate／無伺服器容器運算 | ✅ 正確 | Fargate 讓您執行容器而無需管理伺服器。 |
| AWS Lambda／無伺服器函數 | ✅ 正確 | Lambda 是無伺服器函數運算服務。 |

---

## 問題 19

**題目**
Which of the following Amazon S3 storage classes has NO constraint of a minimum storage duration charge for objects?
以下哪個 Amazon S3 儲存類別對物件沒有最低儲存期限費用的限制？

**[選項]**
- A. Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)／單區低頻存取
- B. Amazon S3 Standard-Infrequent Access (S3 Standard-IA)／標準低頻存取
- C. Amazon S3 Glacier Flexible Retrieval／Glacier 彈性取回
- D. Amazon S3 Standard／標準儲存

**正確答案**
Amazon S3 Standard／標準儲存

**為什麼正確**
**S3 Standard** 沒有最低儲存期限費用限制；IA 與 Glacier 類別通常有 30、90 或 180 天等最低儲存期限。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| S3 One Zone-IA／單區低頻存取 | ❌ 錯誤 | One Zone-IA 有最低儲存期限。 |
| S3 Standard-IA／標準低頻存取 | ❌ 錯誤 | Standard-IA 有最低儲存期限。 |
| S3 Glacier Flexible Retrieval／Glacier 彈性取回 | ❌ 錯誤 | Glacier Flexible Retrieval 有封存類最低儲存期限。 |
| S3 Standard／標準儲存 | ✅ 正確 | S3 Standard 無最低儲存期限費用限制。 |

---

## 問題 20

**題目**
Which of the following is correct regarding the Amazon RDS service?
以下哪項關於 Amazon RDS 服務的陳述是正確的？

**[選項]**
- A. You can use read replicas for improved read performance only and multi-AZ deployment for disaster recovery only／讀取副本只提升讀取效能，Multi-AZ 只做災難恢復
- B. You can use both read replicas and multi-AZ deployment having single standby for improved read performance／讀取副本和單待機 Multi-AZ 都提升讀取效能
- C. You can use read replicas for disaster recovery only and multi-AZ deployment for improved read performance only／讀取副本只做 DR，Multi-AZ 只提升讀取效能
- D. You can use both read replicas and multi-AZ deployment for disaster recovery／讀取副本和 Multi-AZ 都可用於災難恢復

**正確答案**
You can use both read replicas and multi-AZ deployment for disaster recovery／讀取副本和 Multi-AZ 都可用於災難恢復

**為什麼正確**
RDS **Read Replica** 可用於讀取擴展，也可在需要時提升為獨立資料庫協助災難復原；**Multi-AZ** 提供同步備援與自動故障切換，支援高可用與復原。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Read replicas only for read performance, Multi-AZ only for DR／兩者用途過度限定 | ❌ 錯誤 | Read Replica 也可支援 DR；Multi-AZ 主要是高可用。 |
| Both read replicas and single-standby Multi-AZ improve read performance／單待機 Multi-AZ 提升讀取效能 | ❌ 錯誤 | 單待機 Multi-AZ 的 standby 通常不處理讀取。 |
| Read replicas only for DR, Multi-AZ only for read performance／說反 | ❌ 錯誤 | Read Replica 主要提升讀取擴展，Multi-AZ 不是讀取效能方案。 |
| Both read replicas and Multi-AZ for disaster recovery／兩者都可用於復原 | ✅ 正確 | 兩者皆可協助復原策略，但目的與機制不同。 |

---

## 問題 21

**題目**
Which Amazon Route 53 routing policy would you use to route traffic to a single resource such as a web server for your website?
您會使用哪個 Amazon Route 53 路由政策將流量路由至單一資源（例如您網站的 Web 伺服器）？

**[選項]**
- A. Latency-based routing／延遲型路由
- B. Failover routing／容錯移轉路由
- C. Weighted routing／加權路由
- D. Simple routing／簡單路由

**正確答案**
Simple routing／簡單路由

**為什麼正確**
**Simple routing** 適合將 DNS 查詢路由到單一資源，例如一台 Web 伺服器或單一負載平衡器。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Latency-based routing／延遲型路由 | ❌ 錯誤 | 依最低延遲端點路由，不是單一資源基本路由。 |
| Failover routing／容錯移轉路由 | ❌ 錯誤 | 用於主備容錯移轉。 |
| Weighted routing／加權路由 | ❌ 錯誤 | 用於多資源按比例分流。 |
| Simple routing／簡單路由 | ✅ 正確 | Simple routing 適合單一資源。 |

---

## 問題 22

**題目**
Which of the following is available across all AWS Support plans?
以下哪項在所有 AWS Support 方案中都可用？

**[選項]**
- A. Third-Party Software Support／第三方軟體支援
- B. Full set of AWS Trusted Advisor best practice checks／完整 Trusted Advisor 檢查
- C. Enhanced Technical Support with unlimited cases and unlimited contacts／無限案例和聯絡人的增強技術支援
- D. AWS Health Dashboard - Your account health／您的帳戶健康狀態

**正確答案**
AWS Health Dashboard - Your account health／您的帳戶健康狀態

**為什麼正確**
**AWS Health Dashboard - Your account health** 可在所有支援方案中使用，提供與您帳戶和資源相關的個人化健康事件。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Third-Party Software Support／第三方軟體支援 | ❌ 錯誤 | 僅較高階支援方案提供。 |
| Full set of Trusted Advisor checks／完整 TA 檢查 | ❌ 錯誤 | 完整 Trusted Advisor 檢查不是所有方案都有。 |
| Enhanced Technical Support／增強技術支援 | ❌ 錯誤 | Basic 等低階方案不提供此能力。 |
| AWS Health Dashboard - Your account health／您的帳戶健康狀態 | ✅ 正確 | 帳戶健康儀表板所有支援方案可用。 |

---

## 問題 23

**題目**
Which of the following is a container service of AWS?
以下哪個是 AWS 的容器服務？

**[選項]**
- A. Amazon Simple Notification Service (Amazon SNS)／通知服務
- B. AWS Elastic Beanstalk／應用部署平台
- C. Amazon SageMaker／機器學習平台
- D. AWS Fargate／無伺服器容器運算

**正確答案**
AWS Fargate／無伺服器容器運算

**為什麼正確**
**AWS Fargate** 是無伺服器容器運算引擎，可搭配 ECS 或 EKS 執行容器，屬於 AWS 容器服務。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon SNS／通知服務 | ❌ 錯誤 | SNS 是發布/訂閱通知服務，不是容器服務。 |
| AWS Elastic Beanstalk／應用部署平台 | ❌ 錯誤 | Beanstalk 是應用部署平台，不是專門容器服務。 |
| Amazon SageMaker／機器學習平台 | ❌ 錯誤 | SageMaker 是機器學習建置與訓練平台。 |
| AWS Fargate／無伺服器容器運算 | ✅ 正確 | Fargate 是 AWS 容器運算服務。 |

---

## 問題 24

**題目**
Which AWS service can help you analyze your infrastructure to identify unattached or underutilized Amazon EBS Elastic Volumes?
哪個 AWS 服務可以幫助您分析基礎設施，以識別未附加或未充分使用的 Amazon EBS 彈性磁碟區？

**[選項]**
- A. Amazon Inspector／弱點評估
- B. Amazon CloudWatch／監控服務
- C. AWS Config／資源組態追蹤
- D. AWS Trusted Advisor／最佳實務建議

**正確答案**
AWS Trusted Advisor／最佳實務建議

**為什麼正確**
**AWS Trusted Advisor** 的成本最佳化檢查可識別閒置或未充分使用的資源，例如未附加或低使用率的 EBS 磁碟區。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Inspector／弱點評估 | ❌ 錯誤 | Inspector 評估安全漏洞，不分析閒置 EBS 成本。 |
| Amazon CloudWatch／監控服務 | ❌ 錯誤 | CloudWatch 可監控指標，但需自行分析與設定。 |
| AWS Config／資源組態追蹤 | ❌ 錯誤 | Config 追蹤配置與合規，不是成本最佳化建議工具。 |
| AWS Trusted Advisor／最佳實務建議 | ✅ 正確 | Trusted Advisor 可找出未充分使用或未附加的 EBS。 |

---

## 問題 25

**題目**
A media company uploads its media files to a centralized Amazon S3 bucket from geographically dispersed locations. Which solution can the company use to optimize transfer speeds?
一家媒體公司從地理位置分散的地點將媒體檔案上傳至集中的 Amazon S3 儲存貯體。公司可以使用哪個解決方案來優化傳輸速度？

**[選項]**
- A. Amazon CloudFront／內容交付網路
- B. AWS Global Accelerator／全球加速器
- C. AWS Direct Connect／專用連線
- D. Amazon S3 Transfer Acceleration (S3TA)／S3 傳輸加速

**正確答案**
Amazon S3 Transfer Acceleration (S3TA)／S3 傳輸加速

**為什麼正確**
**S3 Transfer Acceleration** 使用 CloudFront 邊緣節點與 AWS 全球網路，加速跨長距離將檔案上傳到 S3 bucket。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon CloudFront／內容交付網路 | ❌ 錯誤 | CloudFront 主要加速內容下載與分發。 |
| AWS Global Accelerator／全球加速器 | ❌ 錯誤 | Global Accelerator 加速應用流量，不是 S3 上傳最佳專用功能。 |
| AWS Direct Connect／專用連線 | ❌ 錯誤 | Direct Connect 需專線，適合本地到 AWS 的持續連線，不是地理分散上傳最佳選項。 |
| Amazon S3 Transfer Acceleration／S3 傳輸加速 | ✅ 正確 | S3TA 專門優化遠距離 S3 傳輸速度。 |

---

## 問題 26

**題目**
Which of the following AWS services offers Lifecycle configuration for cost-optimal storage?
以下哪個 AWS 服務提供生命週期設定以實現成本最佳化儲存？

**[選項]**
- A. Amazon Elastic Block Store (Amazon EBS)／區塊儲存
- B. Amazon EC2 Instance Store／執行個體存放區
- C. AWS Storage Gateway／儲存閘道
- D. Amazon Simple Storage Service (Amazon S3)／物件儲存

**正確答案**
Amazon Simple Storage Service (Amazon S3)／物件儲存

**為什麼正確**
**S3 Lifecycle configuration** 可根據規則自動轉換物件到較低成本儲存類別，或在到期後刪除物件，以最佳化儲存成本。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon EBS／區塊儲存 | ❌ 錯誤 | EBS 不提供 S3 物件生命週期轉層功能。 |
| Amazon EC2 Instance Store／執行個體存放區 | ❌ 錯誤 | Instance Store 是暫時性本機儲存。 |
| AWS Storage Gateway／儲存閘道 | ❌ 錯誤 | Storage Gateway 是混合雲儲存整合服務。 |
| Amazon S3／物件儲存 | ✅ 正確 | S3 提供 Lifecycle 規則以最佳化儲存成本。 |

---

## 問題 27

**題目**
Which of the following AWS authentication mechanisms supports an AWS MFA device that you can plug into a USB port on your computer?
以下哪個 AWS 驗證機制支援可插入電腦 USB 連接埠的 AWS MFA 裝置？

**[選項]**
- A. Hardware Multi-Factor Authentication (MFA) device／硬體 MFA 裝置
- B. Virtual Multi-Factor Authentication (MFA) device／虛擬 MFA 裝置
- C. SMS text message-based Multi-Factor Authentication (MFA)／簡訊 MFA
- D. U2F security key／U2F 安全金鑰

**正確答案**
U2F security key／U2F 安全金鑰

**為什麼正確**
**U2F security key** 是可插入 USB 連接埠的實體安全金鑰，使用者登入時可觸碰裝置完成 MFA。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Hardware MFA device／硬體 MFA 裝置 | ❌ 錯誤 | 硬體 MFA 通常是顯示一次性代碼的裝置，不是插 USB 的 U2F 金鑰。 |
| Virtual MFA device／虛擬 MFA 裝置 | ❌ 錯誤 | Virtual MFA 是手機 App 產生驗證碼。 |
| SMS text message-based MFA／簡訊 MFA | ❌ 錯誤 | 簡訊 MFA 透過手機簡訊，不是 USB 裝置。 |
| U2F security key／U2F 安全金鑰 | ✅ 正確 | U2F 金鑰可插入 USB 連接埠使用。 |

---

## 問題 28

**題目**
Bob and Susan each have an AWS account in AWS Organizations. Susan has five Reserved Instances (RIs) and Bob has none. During one hour, Susan uses three instances and Bob uses six, for a total of nine. Which of the following statements are correct about consolidated billing? (Select two)
Bob 和 Susan 各自在 AWS Organizations 中擁有一個 AWS 帳戶。Susan 有五個保留執行個體，Bob 沒有。在某一小時內，Susan 使用三個執行個體，Bob 使用六個，共九個。以下哪些陳述關於合併計費是正確的？（選兩項）

**[選項]**
- A. AWS bills three instances as Reserved Instances, and the remaining six instances as regular instances／三個算 RI，其餘六個一般計費
- B. Bob receives the cost-benefit from Susan's RI only if he launches his instances in the same AWS Region where Susan purchased her RIs／同 Region 才享 RI 優惠
- C. Bob does not receive any cost-benefit since he hasn't purchased any RI／Bob 未購買 RI 所以無優惠
- D. Bob receives the cost-benefit from Susan's RIs only if he launches his instances in the same Availability Zone (AZ) where Susan purchased her RIs／同 AZ 才享 RI 優惠
- E. AWS bills five instances as Reserved Instances, and the remaining four instances as regular instances／五個算 RI，其餘四個一般計費

**正確答案**
Bob receives the cost-benefit from Susan's RIs only if he launches his instances in the same Availability Zone (AZ) where Susan purchased her RIs／Bob 在同 AZ 才享 RI 優惠；AWS bills five instances as Reserved Instances, and the remaining four instances as regular instances／五個算 RI，其餘四個一般計費

**為什麼正確**
在 AWS Organizations 合併計費下，RI 折扣可在成員帳戶間共享。題庫情境中 Susan 有 5 個 RI，因此總共 9 個執行個體中 5 個享 RI 價格，其餘 4 個按一般價格；折扣套用需符合 RI 的區域/AZ、執行個體類型等條件。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS bills three instances as RI, remaining six regular／三個 RI 六個一般 | ❌ 錯誤 | Susan 有 5 個 RI，組織內可共享使用，不只 Susan 自己使用的 3 個。 |
| Same Region only／只要同 Region | ❌ 錯誤 | 題庫此題強調需符合 Susan RI 購買的同一 AZ 條件。 |
| Bob receives no benefit／Bob 無優惠 | ❌ 錯誤 | 合併計費下 RI 折扣可跨成員帳戶共享。 |
| Same AZ where Susan purchased RI／同 AZ 享優惠 | ✅ 正確 | 題庫指定 RI 優惠需在相同 AZ 條件下套用。 |
| AWS bills five instances as RI, remaining four regular／五個 RI 四個一般 | ✅ 正確 | 共有 5 個 RI 可套用，其餘 4 個以一般價格計費。 |

---

## 問題 29

**題目**
Which AWS service will help you deploy application code automatically to an Amazon EC2 instance?
哪個 AWS 服務可以幫助您將應用程式程式碼自動部署至 Amazon EC2 執行個體？

**[選項]**
- A. AWS CloudFormation／基礎設施即程式碼
- B. AWS Elastic Beanstalk／應用部署平台
- C. AWS CodeBuild／建置服務
- D. AWS CodeDeploy／程式碼部署服務

**正確答案**
AWS CodeDeploy／程式碼部署服務

**為什麼正確**
**AWS CodeDeploy** 可自動將應用程式碼部署到 EC2、Lambda、ECS 和本地伺服器。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS CloudFormation／基礎設施即程式碼 | ❌ 錯誤 | CloudFormation 佈建基礎設施，不是應用程式碼部署服務。 |
| AWS Elastic Beanstalk／應用部署平台 | ❌ 錯誤 | Beanstalk 是更高階的平台服務，但題目問自動部署到 EC2 的服務是 CodeDeploy。 |
| AWS CodeBuild／建置服務 | ❌ 錯誤 | CodeBuild 負責建置和測試程式碼，不負責部署到 EC2。 |
| AWS CodeDeploy／程式碼部署服務 | ✅ 正確 | CodeDeploy 專門自動化部署應用程式碼。 |

---

## 問題 30

**題目**
Which of the following scenarios can be handled by AWS Lambda? (Select two)
以下哪些情境可以由 AWS Lambda 處理？（選兩項）

**[選項]**
- A. You can install Container Services on AWS Lambda／可在 Lambda 安裝容器服務
- B. AWS Lambda can be used to store sensitive environment variables／Lambda 可用於儲存敏感環境變數
- C. You can install low latency databases on AWS Lambda／可在 Lambda 安裝低延遲資料庫
- D. AWS Lambda can be used for preprocessing of data before it is stored in Amazon S3 buckets／資料存入 S3 前可用 Lambda 預處理
- E. AWS Lambda can be used to execute code in response to events such as updates to DynamoDB tables／Lambda 可回應 DynamoDB 更新等事件執行程式碼

**正確答案**
AWS Lambda can be used for preprocessing of data before it is stored in Amazon S3 buckets／資料存入 S3 前可用 Lambda 預處理；AWS Lambda can be used to execute code in response to events such as updates to DynamoDB tables／可回應 DynamoDB 更新等事件執行程式碼

**為什麼正確**
**Lambda** 適合事件驅動運算，可在資料流入 S3 前後進行處理，也可由 DynamoDB Streams、S3、EventBridge 等事件觸發執行程式碼。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Install Container Services on Lambda／安裝容器服務 | ❌ 錯誤 | Lambda 不是用來安裝和管理容器服務的平台。 |
| Store sensitive environment variables／儲存敏感環境變數 | ❌ 錯誤 | Lambda 可設定環境變數，但敏感資料應用 Secrets Manager/Parameter Store/KMS 管理。 |
| Install low latency databases on Lambda／安裝低延遲資料庫 | ❌ 錯誤 | Lambda 不能安裝和管理資料庫服務。 |
| Preprocessing data before S3／S3 前預處理 | ✅ 正確 | Lambda 常用於事件式資料預處理。 |
| Execute code in response to DynamoDB updates／回應 DynamoDB 更新執行程式碼 | ✅ 正確 | Lambda 可由 DynamoDB Streams 等事件觸發。 |

---

## 問題 31

**題目**
Which pillar of AWS Well-Architected Framework is responsible for making sure that you select the right resource types and sizes based on your workload requirements?
AWS Well-Architected Framework 的哪個支柱負責確保根據工作負載需求選擇正確的資源類型和大小？

**[選項]**
- A. Operational Excellence／卓越營運
- B. Cost Optimization／成本優化
- C. Reliability／可靠性
- D. Performance Efficiency／效能效率

**正確答案**
Performance Efficiency／效能效率

**為什麼正確**
**Performance Efficiency** 支柱關注有效使用運算資源，包括根據工作負載需求選擇正確資源類型、大小和服務。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Operational Excellence／卓越營運 | ❌ 錯誤 | 關注營運流程、自動化和持續改進。 |
| Cost Optimization／成本優化 | ❌ 錯誤 | 關注以最低成本交付業務價值。 |
| Reliability／可靠性 | ❌ 錯誤 | 關注系統從故障復原並持續運作。 |
| Performance Efficiency／效能效率 | ✅ 正確 | 負責選擇適合的資源類型與大小。 |

---

## 問題 32

**題目**
A digital media company wants to convert English language subtitles into Spanish language subtitles. Which AWS service would you recommend?
一家數位媒體公司希望將英文字幕轉換為西班牙文字幕。您會推薦哪個 AWS 服務？

**[選項]**
- A. Amazon Polly／文字轉語音
- B. Amazon Rekognition／影像與影片分析
- C. Amazon Transcribe／語音轉文字
- D. Amazon Translate／翻譯服務

**正確答案**
Amazon Translate／翻譯服務

**為什麼正確**
**Amazon Translate** 是神經機器翻譯服務，可將文字從一種語言翻譯成另一種語言，例如英文字幕翻成西班牙文字幕。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Polly／文字轉語音 | ❌ 錯誤 | Polly 將文字轉為語音。 |
| Amazon Rekognition／影像與影片分析 | ❌ 錯誤 | Rekognition 分析圖片和影片，不翻譯字幕。 |
| Amazon Transcribe／語音轉文字 | ❌ 錯誤 | Transcribe 將語音轉為文字，不做語言翻譯。 |
| Amazon Translate／翻譯服務 | ✅ 正確 | Translate 可將英文文字翻譯為西班牙文。 |

---

## 問題 33

**題目**
Which of the following is best-suited for load-balancing HTTP and HTTPS traffic?
以下哪個最適合用於 HTTP 和 HTTPS 流量的負載平衡？

**[選項]**
- A. AWS Auto Scaling／自動擴展
- B. Network Load Balancer／網路負載平衡器
- C. System Load Balancer／系統負載平衡器
- D. Application Load Balancer／應用程式負載平衡器

**正確答案**
Application Load Balancer／應用程式負載平衡器

**為什麼正確**
**Application Load Balancer (ALB)** 運作於第 7 層，最適合 HTTP/HTTPS 流量，可根據路徑、主機標頭等內容路由。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Auto Scaling／自動擴展 | ❌ 錯誤 | Auto Scaling 調整容量，不負責 HTTP/HTTPS 負載平衡。 |
| Network Load Balancer／網路負載平衡器 | ❌ 錯誤 | NLB 適合 TCP/UDP/TLS 等第 4 層高效能流量。 |
| System Load Balancer／系統負載平衡器 | ❌ 錯誤 | 不是 AWS ELB 類型。 |
| Application Load Balancer／應用程式負載平衡器 | ✅ 正確 | ALB 專為 HTTP/HTTPS 應用流量設計。 |

---

## 問題 34

**題目**
As per the AWS Shared Responsibility Model, which of the following is a responsibility of AWS from a security and compliance point of view?
根據 AWS 共同責任模型，以下哪項是 AWS 從安全和合規角度的責任？

**[選項]**
- A. Patching guest OS and applications／修補客體作業系統和應用程式
- B. Service and Communications Protection／服務和通訊保護
- C. Identity and Access Management／身分和存取管理
- D. Patching networking infrastructure／修補網路基礎設施

**正確答案**
Patching networking infrastructure／修補網路基礎設施

**為什麼正確**
AWS 負責雲端本身的安全，包括底層網路、硬體、軟體與基礎設施的修補與維護。客戶負責 guest OS、應用程式與 IAM 設定。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Patching guest OS and applications／修補客體 OS 和應用 | ❌ 錯誤 | EC2 guest OS 和應用程式修補通常是客戶責任。 |
| Service and Communications Protection／服務和通訊保護 | ❌ 錯誤 | 題目考 AWS 明確基礎設施責任；通訊保護設定常有客戶責任成分。 |
| Identity and Access Management／身分和存取管理 | ❌ 錯誤 | IAM 使用者、角色與權限配置是客戶責任。 |
| Patching networking infrastructure／修補網路基礎設施 | ✅ 正確 | AWS 負責底層網路基礎設施修補。 |

---

## 問題 35

**題目**
According to the AWS Shared Responsibility Model, which of the following are responsibilities of the customer for AWS IAM? (Select two)
根據 AWS 共同責任模型，以下哪些是客戶對 AWS IAM 的責任？（選兩項）

**[選項]**
- A. Manage global network security infrastructure／管理全球網路安全基礎設施
- B. Compliance validation for the underlying software infrastructure／底層軟體基礎設施合規驗證
- C. Configuration and vulnerability analysis for the underlying software infrastructure／底層軟體基礎設施設定和漏洞分析
- D. Analyze user access patterns and review AWS IAM permissions／分析使用者存取模式並審查 IAM 權限
- E. Enable multi-factor authentication (MFA) on all accounts／為所有帳戶啟用 MFA

**正確答案**
Analyze user access patterns and review AWS IAM permissions／分析使用者存取模式並審查 IAM 權限；Enable multi-factor authentication (MFA) on all accounts／為所有帳戶啟用 MFA

**為什麼正確**
IAM 是客戶設定與治理的核心服務。客戶需審查使用者權限、落實最小權限、分析存取模式並啟用 MFA。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Manage global network security infrastructure／管理全球網路安全基礎設施 | ❌ 錯誤 | AWS 全球網路基礎設施由 AWS 管理。 |
| Compliance validation for underlying software infrastructure／底層軟體合規驗證 | ❌ 錯誤 | AWS 負責底層基礎設施合規驗證。 |
| Configuration and vulnerability analysis for underlying software infrastructure／底層軟體設定和漏洞分析 | ❌ 錯誤 | AWS 負責底層軟體基礎設施。 |
| Analyze user access patterns and review IAM permissions／分析存取模式並審查 IAM 權限 | ✅ 正確 | 客戶負責 IAM 權限與存取治理。 |
| Enable MFA on all accounts／啟用 MFA | ✅ 正確 | MFA 是客戶應落實的 IAM 安全最佳實務。 |

---

## 問題 36

**題目**
Amazon EC2 Spot instances are a best-fit for which of the following scenarios?
Amazon EC2 Spot 執行個體最適合以下哪種情境？

**[選項]**
- A. To run scheduled jobs (jobs that run at the same time every day)／執行每日固定時間排程作業
- B. To install cost-effective Amazon RDS database／安裝具成本效益的 RDS 資料庫
- C. To run batch processes for critical workloads／執行關鍵工作負載批次處理
- D. To run any containerized workload with Amazon ECS that can be interrupted／執行可被中斷的 ECS 容器化工作負載

**正確答案**
To run any containerized workload with Amazon ECS that can be interrupted／執行可被中斷的 ECS 容器化工作負載

**為什麼正確**
**Spot Instances** 最適合可中斷、容錯、彈性的工作負載，例如批次、資料處理或可中斷的容器任務。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Scheduled jobs at same time every day／固定排程作業 | ❌ 錯誤 | 固定排程不代表可中斷，若時間要求嚴格不一定適合 Spot。 |
| Install cost-effective RDS database／安裝 RDS | ❌ 錯誤 | RDS 是受管資料庫，不在 Spot 執行個體上安裝。 |
| Batch processes for critical workloads／關鍵批次工作 | ❌ 錯誤 | 關鍵工作負載不應依賴可能中斷的 Spot。 |
| Interruptible ECS containerized workload／可中斷 ECS 容器工作 | ✅ 正確 | Spot 適合可容忍中斷的容器化工作負載。 |

---

## 問題 37

**題目**
The DevOps team at a Big Data consultancy has set up Amazon EC2 instances across two AWS Regions. Which of the following characterizes this application architecture?
一家大數據諮詢公司的 DevOps 團隊在兩個 AWS 區域設定了 Amazon EC2 執行個體。以下哪項描述了此應用程式架構的特點？

**[選項]**
- A. Deploying the application across two AWS Regions improves security／跨兩個區域提升安全性
- B. Deploying the application across two AWS Regions improves agility／跨兩個區域提升敏捷性
- C. Deploying the application across two AWS Regions improves scalability／跨兩個區域提升可擴展性
- D. Deploying the application across two AWS Regions improves availability／跨兩個區域提升可用性

**正確答案**
Deploying the application across two AWS Regions improves availability／跨兩個區域提升可用性

**為什麼正確**
跨多個 AWS Region 部署可降低單一區域故障造成的影響，提升應用程式可用性和災難復原能力。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Improves security／提升安全性 | ❌ 錯誤 | 多區域部署主要提升可用性，不直接代表安全提升。 |
| Improves agility／提升敏捷性 | ❌ 錯誤 | 敏捷性是快速創新與部署能力，不是此架構主要特徵。 |
| Improves scalability／提升可擴展性 | ❌ 錯誤 | 可擴展性可由 Auto Scaling 等達成，跨 Region 主要是可用性/DR。 |
| Improves availability／提升可用性 | ✅ 正確 | 跨 Region 可提升可用性與容災能力。 |

---

## 問題 38

**題目**
A cargo shipping company runs CRM applications that need to be accessible 24*7 but can be managed on fewer instances during a disaster for some time. Which disaster recovery strategy is well-suited and cost-effective?
一家貨運公司執行需要全天候存取的 CRM 應用程式，但在災難期間可以暫時在較少的執行個體上管理。哪種災難恢復策略既適合又具成本效益？

**[選項]**
- A. Multi-site active-active strategy／多站點主動-主動
- B. Pilot Light strategy／試點燈
- C. Backup & Restore strategy／備份與還原
- D. Warm Standby strategy／暖待機

**正確答案**
Warm Standby strategy／暖待機

**為什麼正確**
**Warm Standby** 會在備援環境中維持縮小版可運作系統，災難時可快速擴大容量。題目說災難期間可用較少執行個體暫時服務，正符合暖待機。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Multi-site active-active／多站點主動-主動 | ❌ 錯誤 | 成本最高，兩邊都完整運作，不符合成本效益要求。 |
| Pilot Light／試點燈 | ❌ 錯誤 | Pilot Light 只保留核心元件，需要更多啟動步驟才可服務。 |
| Backup & Restore／備份與還原 | ❌ 錯誤 | 成本最低但恢復時間最長，不符合 24/7 可存取需求。 |
| Warm Standby／暖待機 | ✅ 正確 | 縮小版環境持續運作，災難時可較快服務且成本較 active-active 低。 |

---

## 問題 39

**題目**
AWS Marketplace facilitates which of the following use-cases? (Select two)
AWS Marketplace 促進以下哪些使用案例？（選兩項）

**[選項]**
- A. Purchase compliance documents from third-party vendors／購買合規文件
- B. Buy Amazon EC2 Standard Reserved Instances (RI)／購買 EC2 標準 RI
- C. Raise request for purchasing AWS Direct Connect connection／提出購買 Direct Connect 請求
- D. Sell Software as a Service (SaaS) solutions to AWS customers／向 AWS 客戶銷售 SaaS 解決方案
- E. AWS customer can buy software bundled into customized AMIs by AWS Marketplace sellers／購買 Marketplace 賣家自訂 AMI 內含軟體

**正確答案**
Sell Software as a Service (SaaS) solutions to AWS customers／銷售 SaaS 解決方案；AWS customer can buy software bundled into customized AMIs by AWS Marketplace sellers／購買自訂 AMI 軟體

**為什麼正確**
**AWS Marketplace** 是第三方軟體與 SaaS 解決方案的數位目錄，賣家可銷售 SaaS 或 AMI 型軟體，客戶可搜尋、購買並部署。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Purchase compliance documents／購買合規文件 | ❌ 錯誤 | AWS 合規報告主要透過 AWS Artifact 取得。 |
| Buy EC2 Standard RI／購買 EC2 標準 RI | ❌ 錯誤 | RI 透過 EC2/計費相關頁面購買，不是 Marketplace 核心用途。 |
| Raise Direct Connect request／提出 Direct Connect 請求 | ❌ 錯誤 | Direct Connect 不是透過 Marketplace 請求購買的軟體商品。 |
| Sell SaaS solutions／銷售 SaaS 解決方案 | ✅ 正確 | Marketplace 支援 SaaS 解決方案銷售。 |
| Buy software bundled into customized AMIs／購買自訂 AMI 軟體 | ✅ 正確 | Marketplace 提供 AMI 型軟體產品。 |

---

## 問題 40

**題目**
Which AWS service can be used to set up billing alarms to monitor estimated charges on your AWS account?
哪個 AWS 服務可用於設定帳單警報以監控 AWS 帳戶的預估費用？

**[選項]**
- A. AWS Organizations／多帳戶管理
- B. AWS Cost Explorer／成本分析
- C. AWS CloudTrail／活動稽核
- D. Amazon CloudWatch／監控與警示

**正確答案**
Amazon CloudWatch／監控與警示

**為什麼正確**
**CloudWatch Billing Alarms** 可根據估算費用指標設定警示，在費用超過門檻時通知使用者。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Organizations／多帳戶管理 | ❌ 錯誤 | Organizations 管理多帳戶與整合帳單，不設定 CloudWatch billing alarms。 |
| AWS Cost Explorer／成本分析 | ❌ 錯誤 | Cost Explorer 用於分析和預測成本。 |
| AWS CloudTrail／活動稽核 | ❌ 錯誤 | CloudTrail 記錄 API 活動，不監控費用指標。 |
| Amazon CloudWatch／監控與警示 | ✅ 正確 | CloudWatch 可設定帳單警示。 |

---

## 問題 41

**題目**
Which benefit of Cloud Computing allows AWS to offer lower pay-as-you-go prices as usage from hundreds of thousands of customers is aggregated in the cloud?
雲端運算的哪項優勢使 AWS 能夠在數十萬客戶的使用量聚合到雲端時提供更低的隨用隨付價格？

**[選項]**
- A. Increased speed and agility／提升速度和敏捷性
- B. Trade capital expense for variable expense／以資本支出換取可變支出
- C. Go global in minutes／幾分鐘內全球化
- D. Massive economies of scale／大規模規模經濟

**正確答案**
Massive economies of scale／大規模規模經濟

**為什麼正確**
**Massive economies of scale** 指雲端供應商彙整大量客戶需求，因規模採購與營運效率降低單位成本，進而提供較低的隨用隨付價格。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Increased speed and agility／速度和敏捷性 | ❌ 錯誤 | 這描述快速取得資源與創新，不是價格降低原因。 |
| Trade capital expense for variable expense／資本支出轉可變支出 | ❌ 錯誤 | 指不用預先投資資料中心，而是按用量付費。 |
| Go global in minutes／幾分鐘全球化 | ❌ 錯誤 | 指快速部署到全球區域。 |
| Massive economies of scale／大規模規模經濟 | ✅ 正確 | 大規模聚合需求帶來較低單位成本。 |

---

## 問題 42

**題目**
An e-commerce company would like to receive alerts when the Amazon EC2 Reserved Instances (RI) utilization drops below a certain threshold. Which AWS service can be used to address this use-case?
一家電子商務公司希望在 Amazon EC2 保留執行個體（RI）使用率低於某個閾值時收到警報。哪個 AWS 服務可以解決此使用案例？

**[選項]**
- A. AWS Cost Explorer／成本分析
- B. AWS Systems Manager／系統管理
- C. AWS Trusted Advisor／最佳實務建議
- D. AWS Budgets／預算管理

**正確答案**
AWS Budgets／預算管理

**為什麼正確**
**AWS Budgets** 可建立 RI 使用率或 RI 覆蓋率預算，並在使用率低於指定門檻時發送警報。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Cost Explorer／成本分析 | ❌ 錯誤 | Cost Explorer 可分析 RI 使用情況，但題目問警報。 |
| AWS Systems Manager／系統管理 | ❌ 錯誤 | Systems Manager 不監控 RI 使用率。 |
| AWS Trusted Advisor／最佳實務建議 | ❌ 錯誤 | Trusted Advisor 可提供建議，但 Budgets 是設定 RI 使用率警報的服務。 |
| AWS Budgets／預算管理 | ✅ 正確 | Budgets 支援 RI 使用率低於門檻告警。 |

---

## 問題 43

**題目**
Which of the following AWS entities lists all users in your account and the status of their various account aspects such as passwords, access keys, and MFA devices?
以下哪個 AWS 實體列出帳戶中所有使用者及其各種帳戶方面的狀態（如密碼、存取金鑰和 MFA 裝置）？

**[選項]**
- A. AWS Trusted Advisor／最佳實務建議
- B. AWS Cost & Usage Report (AWS CUR)／成本與用量報告
- C. Amazon Inspector／弱點評估
- D. Credentials Report／憑證報告

**正確答案**
Credentials Report／憑證報告

**為什麼正確**
**IAM Credential Report** 會列出帳戶中所有 IAM 使用者及其密碼、存取金鑰、MFA 等憑證狀態，常用於稽核與合規。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Trusted Advisor／最佳實務建議 | ❌ 錯誤 | Trusted Advisor 提供最佳實務檢查，不列出所有使用者憑證明細。 |
| AWS CUR／成本與用量報告 | ❌ 錯誤 | CUR 是費用與用量報告。 |
| Amazon Inspector／弱點評估 | ❌ 錯誤 | Inspector 評估弱點，不產生 IAM 憑證清單。 |
| Credentials Report／憑證報告 | ✅ 正確 | IAM Credential Report 列出使用者密碼、存取金鑰、MFA 等狀態。 |

---

## 問題 44

**題目**
Which of the following entities are part of an Amazon VPC in the AWS Cloud? (Select two)
以下哪些實體是 AWS 雲端中 Amazon VPC 的一部分？（選兩項）

**[選項]**
- A. AWS Storage Gateway／儲存閘道
- B. Object／物件
- C. API Gateway／API 閘道
- D. Subnet／子網路
- E. Internet Gateway／網際網路閘道

**正確答案**
Subnet／子網路；Internet Gateway／網際網路閘道

**為什麼正確**
**Subnet** 是 VPC 中的 IP 範圍；**Internet Gateway** 是可附加到 VPC 的元件，讓 VPC 內資源連接網際網路。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Storage Gateway／儲存閘道 | ❌ 錯誤 | Storage Gateway 是混合雲儲存服務，不是 VPC 元件。 |
| Object／物件 | ❌ 錯誤 | Object 是 S3 儲存概念。 |
| API Gateway／API 閘道 | ❌ 錯誤 | API Gateway 是 API 管理服務，不是 VPC 基礎元件。 |
| Subnet／子網路 | ✅ 正確 | Subnet 是 VPC 的基本組成。 |
| Internet Gateway／網際網路閘道 | ✅ 正確 | Internet Gateway 可附加到 VPC 以連接網際網路。 |

---

## 問題 45

**題目**
Which AWS service will you use to provision the same AWS infrastructure across multiple AWS accounts and regions?
您會使用哪個 AWS 服務在多個 AWS 帳戶和區域中佈建相同的 AWS 基礎設施？

**[選項]**
- A. AWS CodeDeploy／程式碼部署
- B. AWS Systems Manager／系統管理
- C. AWS Config／資源組態
- D. AWS CloudFormation／基礎設施即程式碼

**正確答案**
AWS CloudFormation／基礎設施即程式碼

**為什麼正確**
**AWS CloudFormation StackSets** 可在多個 AWS 帳戶與多個 Region 中建立、更新和刪除同一組基礎設施堆疊。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS CodeDeploy／程式碼部署 | ❌ 錯誤 | CodeDeploy 部署應用程式碼，不佈建基礎設施。 |
| AWS Systems Manager／系統管理 | ❌ 錯誤 | Systems Manager 管理與自動化營運，不是跨帳戶/區域 IaC 佈建主要服務。 |
| AWS Config／資源組態 | ❌ 錯誤 | Config 追蹤組態與合規，不佈建資源。 |
| AWS CloudFormation／基礎設施即程式碼 | ✅ 正確 | CloudFormation StackSets 可跨帳戶和 Region 佈建相同基礎設施。 |

---

## 問題 46

**題目**
Which AWS entity enables you to privately connect your Amazon VPC to an Amazon SQS queue?
哪個 AWS 實體使您能夠將 Amazon VPC 私下連接至 Amazon SQS 佇列？

**[選項]**
- A. AWS Direct Connect／專用網路連線
- B. VPC Gateway Endpoint／VPC 閘道端點
- C. Internet Gateway／網際網路閘道
- D. VPC Interface Endpoint／VPC 介面端點

**正確答案**
VPC Interface Endpoint／VPC 介面端點

**為什麼正確**
**Interface Endpoint** 透過 AWS PrivateLink 在 VPC 中建立私有 IP ENI，用於私下連接多數 AWS 服務，包括 Amazon SQS。Gateway Endpoint 主要支援 S3 和 DynamoDB。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Direct Connect／專用網路連線 | ❌ 錯誤 | Direct Connect 連接本地資料中心與 AWS。 |
| VPC Gateway Endpoint／VPC 閘道端點 | ❌ 錯誤 | Gateway Endpoint 主要支援 S3 和 DynamoDB，不是 SQS。 |
| Internet Gateway／網際網路閘道 | ❌ 錯誤 | Internet Gateway 會走網際網路路徑，不是私有 SQS 連線。 |
| VPC Interface Endpoint／VPC 介面端點 | ✅ 正確 | Interface Endpoint 可私下連接 VPC 與 SQS。 |

---

## 問題 47

**題目**
AWS Organizations provides which of the following benefits? (Select two)
AWS Organizations 提供以下哪些優點？（選兩項）

**[選項]**
- A. Deploy patches on Amazon EC2 instances across the member AWS accounts／跨帳戶部署 EC2 修補程式
- B. Provision Amazon EC2 Spot instances across the member AWS accounts／跨帳戶佈建 Spot 執行個體
- C. Check vulnerabilities on Amazon EC2 instances across the member AWS accounts／跨帳戶檢查 EC2 漏洞
- D. Volume discounts for Amazon EC2 and Amazon S3 aggregated across the member AWS accounts／跨成員帳戶彙總 EC2 和 S3 批量折扣
- E. Share the reserved Amazon EC2 instances amongst the member AWS accounts／在成員帳戶間共享 EC2 RI

**正確答案**
Volume discounts for Amazon EC2 and Amazon S3 aggregated across the member AWS accounts／跨成員帳戶彙總批量折扣；Share the reserved Amazon EC2 instances amongst the member AWS accounts／成員帳戶間共享 EC2 RI

**為什麼正確**
**AWS Organizations** 支援整合帳單，可彙總多帳戶用量以取得批量折扣，並可在成員帳戶間共享 Reserved Instance 折扣。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Deploy patches／部署修補程式 | ❌ 錯誤 | 跨帳戶修補可看 Systems Manager，不是 Organizations 核心功能。 |
| Provision EC2 Spot instances／佈建 Spot | ❌ 錯誤 | Spot 是 EC2 採購選項，不是 Organizations 功能。 |
| Check vulnerabilities／檢查漏洞 | ❌ 錯誤 | 漏洞評估用 Amazon Inspector。 |
| Volume discounts aggregated across accounts／彙總批量折扣 | ✅ 正確 | 整合帳單可彙總用量取得折扣。 |
| Share reserved EC2 instances／共享 RI | ✅ 正確 | Organizations 可在成員帳戶間共享 RI 折扣。 |

---

## 問題 48

**題目**
Which of the following entities can be used to connect to an Amazon EC2 server from a Mac OS, Windows or Linux based computer via a browser-based client?
以下哪個實體可用於透過瀏覽器用戶端從 Mac OS、Windows 或 Linux 電腦連接至 Amazon EC2 伺服器？

**[選項]**
- A. SSH
- B. AWS Direct Connect
- C. Putty
- D. Amazon EC2 Instance Connect

**正確答案**
Amazon EC2 Instance Connect

**為什麼正確**
**EC2 Instance Connect** 可透過瀏覽器型用戶端或 CLI 連接 EC2，支援從 Mac、Windows 或 Linux 電腦使用。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| SSH | ❌ 錯誤 | SSH 是命令列協定，不是瀏覽器型用戶端本身。 |
| AWS Direct Connect | ❌ 錯誤 | Direct Connect 是網路專線服務，不是 EC2 登入工具。 |
| Putty | ❌ 錯誤 | PuTTY 是 Windows SSH 用戶端，不是跨平台瀏覽器型連線。 |
| Amazon EC2 Instance Connect | ✅ 正確 | EC2 Instance Connect 支援瀏覽器連線到 EC2。 |

---

## 問題 49

**題目**
Which of the following is the MOST cost-effective Amazon EC2 instance purchasing option for short-term, spiky and critical workloads on AWS Cloud?
以下哪個是 AWS 雲端上短期、突發性和關鍵工作負載最具成本效益的 Amazon EC2 執行個體購買選項？

**[選項]**
- A. Reserved Instance (RI)／保留執行個體
- B. Spot Instance／Spot 執行個體
- C. Dedicated Host／專用主機
- D. On-Demand Instance／隨需執行個體

**正確答案**
On-Demand Instance／隨需執行個體

**為什麼正確**
題目是短期、突發且**關鍵**工作負載，需要不中斷且不需長期承諾。**On-Demand** 雖不是最低單價，但在關鍵不可中斷且短期彈性條件下最合適。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Reserved Instance (RI)／保留執行個體 | ❌ 錯誤 | RI 適合長期穩定可預測工作負載。 |
| Spot Instance／Spot 執行個體 | ❌ 錯誤 | Spot 成本低但可能中斷，不適合關鍵工作負載。 |
| Dedicated Host／專用主機 | ❌ 錯誤 | Dedicated Host 適合授權或合規需求，成本通常較高。 |
| On-Demand Instance／隨需執行個體 | ✅ 正確 | On-Demand 適合短期、突發且不可中斷的工作負載。 |

---

## 問題 50

**題目**
Which of the following Amazon S3 storage classes do not charge any data retrieval fee? (Select two)
以下哪些 Amazon S3 儲存類別不收取任何資料取得費用？（選兩項）

**[選項]**
- A. Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)／單區低頻存取
- B. Amazon S3 Standard-Infrequent Access (S3 Standard-IA)／標準低頻存取
- C. Amazon S3 Glacier Flexible Retrieval／Glacier 彈性取回
- D. Amazon S3 Intelligent-Tiering／智慧分層
- E. Amazon S3 Standard／標準儲存

**正確答案**
Amazon S3 Intelligent-Tiering／智慧分層；Amazon S3 Standard／標準儲存

**為什麼正確**
**S3 Standard** 和 **S3 Intelligent-Tiering** 不收取資料取回費用；IA 和 Glacier 類別通常會收取資料取回費。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| S3 One Zone-IA／單區低頻存取 | ❌ 錯誤 | One Zone-IA 有資料取回費。 |
| S3 Standard-IA／標準低頻存取 | ❌ 錯誤 | Standard-IA 有資料取回費。 |
| S3 Glacier Flexible Retrieval／Glacier 彈性取回 | ❌ 錯誤 | Glacier 類取回通常有費用。 |
| S3 Intelligent-Tiering／智慧分層 | ✅ 正確 | Intelligent-Tiering 不收資料取回費。 |
| S3 Standard／標準儲存 | ✅ 正確 | S3 Standard 不收資料取回費。 |

---

## 問題 51

**題目**
Which of the following AWS services can be used to forecast your AWS account usage and costs?
以下哪個 AWS 服務可用於預測您的 AWS 帳戶使用量和成本？

**[選項]**
- A. AWS Cost & Usage Report (AWS CUR)／成本與用量報告
- B. AWS Pricing Calculator／定價試算
- C. AWS Budgets／預算管理
- D. AWS Cost Explorer／成本分析

**正確答案**
AWS Cost Explorer／成本分析

**為什麼正確**
**AWS Cost Explorer** 可視覺化歷史成本與用量，並根據歷史趨勢預測未來 AWS 成本和使用量。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS CUR／成本與用量報告 | ❌ 錯誤 | CUR 提供詳細歷史資料，不是預測工具。 |
| AWS Pricing Calculator／定價試算 | ❌ 錯誤 | Pricing Calculator 用於建置前估算假設架構成本。 |
| AWS Budgets／預算管理 | ❌ 錯誤 | Budgets 可用預測值觸發告警，但預測分析工具是 Cost Explorer。 |
| AWS Cost Explorer／成本分析 | ✅ 正確 | Cost Explorer 可預測帳戶用量與成本。 |

---

## 問題 52

**題目**
Which of the following AWS storage services can be directly used with on-premises systems?
以下哪個 AWS 儲存服務可直接與本地系統搭配使用？

**[選項]**
- A. Amazon EC2 Instance Store／執行個體存放區
- B. Amazon Simple Storage Service (Amazon S3)／物件儲存
- C. Amazon Elastic Block Store (Amazon EBS)／區塊儲存
- D. Amazon Elastic File System (Amazon EFS)／檔案系統

**正確答案**
Amazon Elastic File System (Amazon EFS)／檔案系統

**為什麼正確**
**Amazon EFS** 可透過 AWS Direct Connect 或 VPN 從本地 Linux 伺服器掛載使用，是可與本地系統直接搭配的 AWS 檔案儲存服務。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon EC2 Instance Store／執行個體存放區 | ❌ 錯誤 | Instance Store 是 EC2 主機本機暫存儲存，不能給本地系統直接使用。 |
| Amazon S3／物件儲存 | ❌ 錯誤 | 本地系統通常需透過 API 或 Storage Gateway 整合，不是直接檔案掛載。 |
| Amazon EBS／區塊儲存 | ❌ 錯誤 | EBS 只能附加到同 AZ 的 EC2 執行個體。 |
| Amazon EFS／檔案系統 | ✅ 正確 | EFS 可透過網路從本地系統掛載使用。 |

---

## 問題 53

**題目**
Which of the following entities should be used for an Amazon EC2 Instance to access a DynamoDB table?
以下哪個實體應用於 Amazon EC2 執行個體存取 DynamoDB 資料表？

**[選項]**
- A. AWS Key Management Service (KMS)／金鑰管理服務
- B. Amazon Cognito／使用者身分服務
- C. AWS IAM user access keys／IAM 使用者存取金鑰
- D. IAM role／IAM 角色

**正確答案**
IAM role／IAM 角色

**為什麼正確**
讓 EC2 存取 DynamoDB 等 AWS 服務的最佳實務是附加 **IAM Role**，由角色提供臨時安全憑證，避免在執行個體中保存長期 access key。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS KMS／金鑰管理服務 | ❌ 錯誤 | KMS 管理加密金鑰，不授予 EC2 存取 DynamoDB 的身分。 |
| Amazon Cognito／使用者身分服務 | ❌ 錯誤 | Cognito 用於應用使用者身分驗證與授權。 |
| IAM user access keys／IAM 使用者存取金鑰 | ❌ 錯誤 | 長期金鑰不建議放在 EC2 上，安全風險較高。 |
| IAM role／IAM 角色 | ✅ 正確 | IAM Role 為 EC2 提供臨時憑證與權限。 |

---

## 問題 54

**題目**
A financial services company wants to compare the cost of running their IT infrastructure on-premises vs AWS Cloud. Which AWS service would you recommend?
一家金融服務公司希望比較在本地與 AWS 雲端執行 IT 基礎設施的成本。您會推薦哪個 AWS 服務？

**[選項]**
- A. AWS Cost Explorer／成本分析
- B. AWS Trusted Advisor／最佳實務建議
- C. AWS Budgets／預算管理
- D. AWS Pricing Calculator／定價試算

**正確答案**
AWS Pricing Calculator／定價試算

**為什麼正確**
**AWS Pricing Calculator** 可根據預期服務、用量與架構建立 AWS 成本估算，適合在遷移或採用前比較本地與 AWS 雲端成本。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Cost Explorer／成本分析 | ❌ 錯誤 | Cost Explorer 分析已在 AWS 上產生的成本。 |
| AWS Trusted Advisor／最佳實務建議 | ❌ 錯誤 | Trusted Advisor 提供成本/安全等最佳實務建議，不做本地 vs AWS 成本試算。 |
| AWS Budgets／預算管理 | ❌ 錯誤 | Budgets 用於設定預算與警報。 |
| AWS Pricing Calculator／定價試算 | ✅ 正確 | Pricing Calculator 可事前估算 AWS 成本並支援比較。 |

---

## 問題 55

**題目**
A social media company wants to have the MOST cost-optimal strategy for deploying Amazon EC2 instances. Which of the following options would you recommend? (Select two)
一家社群媒體公司希望制定最具成本效益的 Amazon EC2 執行個體部署策略。您會推薦以下哪些選項？（選兩項）

**[選項]**
- A. Use On-Demand Instances for ad-hoc jobs that can be interrupted／可中斷臨時作業用 On-Demand
- B. Use On-Demand Instances to run applications with a predictable usage over the next one year／未來一年可預測用量用 On-Demand
- C. Use Reserved Instances (RI) for ad-hoc jobs that can be interrupted／可中斷臨時作業用 RI
- D. Use Spot Instances for ad-hoc jobs that can be interrupted／可中斷臨時作業用 Spot
- E. Use Reserved Instances (RI) to run applications with a predictable usage over the next one year／未來一年可預測用量用 RI

**正確答案**
Use Spot Instances for ad-hoc jobs that can be interrupted／可中斷臨時作業用 Spot；Use Reserved Instances (RI) to run applications with predictable usage over the next one year／可預測一年用量用 RI

**為什麼正確**
可中斷臨時工作最適合 **Spot Instances**，可用較低價格使用閒置容量；長期且可預測的工作負載適合 **Reserved Instances**，用承諾換取折扣。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| On-Demand for interruptible ad-hoc jobs／可中斷臨時作業用 On-Demand | ❌ 錯誤 | 可中斷作業用 Spot 成本更低。 |
| On-Demand for predictable one-year usage／可預測一年用量用 On-Demand | ❌ 錯誤 | 可預測長期用量應用 RI 降成本。 |
| RI for interruptible ad-hoc jobs／可中斷臨時作業用 RI | ❌ 錯誤 | RI 適合長期穩定，不適合臨時可中斷作業。 |
| Spot for interruptible ad-hoc jobs／可中斷臨時作業用 Spot | ✅ 正確 | Spot 是可中斷彈性作業的最低成本選項。 |
| RI for predictable one-year usage／可預測一年用量用 RI | ✅ 正確 | RI 適合一年或三年可預測工作負載。 |

---

## 問題 56

**題目**
AWS Trusted Advisor can provide alerts on which of the following common security misconfigurations? (Select two)
AWS Trusted Advisor 可以針對以下哪些常見安全設定錯誤提供警報？（選兩項）

**[選項]**
- A. When you don't enable data encryption on Amazon S3 Glacier／未啟用 S3 Glacier 加密
- B. When you don't tag objects in Amazon S3 buckets／S3 物件未加標籤
- C. When you share IAM user credentials with others／共享 IAM 使用者憑證
- D. When you don't turn on user activity logging (AWS CloudTrail)／未開啟 CloudTrail
- E. When you allow public access to Amazon S3 buckets／允許 S3 bucket 公開存取

**正確答案**
When you don't turn on user activity logging (AWS CloudTrail)／未開啟 CloudTrail；When you allow public access to Amazon S3 buckets／允許 S3 bucket 公開存取

**為什麼正確**
**AWS Trusted Advisor** 安全檢查可提醒常見安全風險，包括 S3 bucket 公開存取、CloudTrail 未啟用、特定端口暴露、root MFA 等。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| S3 Glacier encryption not enabled／Glacier 未加密 | ❌ 錯誤 | 題庫此題的 TA 常見安全告警不選此項。 |
| S3 objects not tagged／S3 物件未標籤 | ❌ 錯誤 | 標籤是成本/管理用途，非典型安全錯誤告警。 |
| Sharing IAM credentials／共享 IAM 憑證 | ❌ 錯誤 | 這是壞實務，但 Trusted Advisor 無法可靠知道是否「共享」。 |
| CloudTrail not turned on／未開啟 CloudTrail | ✅ 正確 | Trusted Advisor 可提醒未啟用使用者活動記錄。 |
| Public access to S3 buckets／S3 bucket 公開存取 | ✅ 正確 | Trusted Advisor 可提醒 S3 公開存取風險。 |

---

## 問題 57

**題目**
Which of the following is a perspective of the AWS Cloud Adoption Framework (AWS CAF)?
以下哪項是 AWS 雲端採用框架（AWS CAF）的觀點？

**[選項]**
- A. Product／產品
- B. Process／流程
- C. Architecture／架構
- D. Business／業務

**正確答案**
Business／業務

**為什麼正確**
AWS CAF 六大觀點包括 Business、People、Governance、Platform、Security、Operations。**Business** 是其中之一。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Product／產品 | ❌ 錯誤 | Product 不是 AWS CAF 視角名稱。 |
| Process／流程 | ❌ 錯誤 | Process 不是 AWS CAF 視角名稱。 |
| Architecture／架構 | ❌ 錯誤 | Architecture 不是六大 CAF 視角之一。 |
| Business／業務 | ✅ 正確 | Business 是 AWS CAF 視角之一。 |

---

## 問題 58

**題目**
Which AWS service can be used to host a static website with the LEAST effort?
哪個 AWS 服務可以以最少的工作量託管靜態網站？

**[選項]**
- A. AWS Storage Gateway／儲存閘道
- B. Amazon S3 Glacier／封存儲存
- C. Amazon Elastic File System (Amazon EFS)／檔案系統
- D. Amazon Simple Storage Service (Amazon S3)／物件儲存

**正確答案**
Amazon Simple Storage Service (Amazon S3)／物件儲存

**為什麼正確**
**Amazon S3** 支援靜態網站託管，只需將 HTML/CSS/JS 等靜態檔案放入 bucket 並啟用網站託管與權限設定。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Storage Gateway／儲存閘道 | ❌ 錯誤 | Storage Gateway 是混合雲儲存整合，不託管靜態網站。 |
| Amazon S3 Glacier／封存儲存 | ❌ 錯誤 | Glacier 用於封存，不能作為網站託管入口。 |
| Amazon EFS／檔案系統 | ❌ 錯誤 | EFS 需搭配伺服器才能對外提供網站。 |
| Amazon S3／物件儲存 | ✅ 正確 | S3 可最少努力託管靜態網站。 |

---

## 問題 59

**題目**
Which of the following can you use to run a bootstrap script while launching an Amazon EC2 instance?
以下哪項可讓您在啟動 Amazon EC2 執行個體時執行啟動程序腳本？

**[選項]**
- A. Amazon EC2 instance AMI data／AMI 資料
- B. Amazon EC2 instance metadata／執行個體中繼資料
- C. Amazon EC2 instance configuration data／執行個體設定資料
- D. Amazon EC2 instance user data／執行個體使用者資料

**正確答案**
Amazon EC2 instance user data／執行個體使用者資料

**為什麼正確**
**EC2 User Data** 可在執行個體首次啟動時執行 bootstrap script，用於安裝套件、設定服務或初始化應用。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AMI data／AMI 資料 | ❌ 錯誤 | AMI 提供啟動映像，不是啟動腳本輸入。 |
| Instance metadata／執行個體中繼資料 | ❌ 錯誤 | Metadata 用於查詢執行個體自身資訊。 |
| Instance configuration data／執行個體設定資料 | ❌ 錯誤 | 不是 EC2 啟動腳本的正式功能名稱。 |
| Instance user data／執行個體使用者資料 | ✅ 正確 | User Data 可在啟動時執行 bootstrap script。 |

---

## 問題 60

**題目**
Which entity ensures that your application on Amazon EC2 always has the right amount of capacity to handle the current traffic demand?
哪個實體確保您在 Amazon EC2 上的應用程式始終擁有適當的容量來處理當前的流量需求？

**[選項]**
- A. Application Load Balancer／應用程式負載平衡器
- B. Multi-AZ deployment／多 AZ 部署
- C. Network Load Balancer／網路負載平衡器
- D. Amazon EC2 Auto Scaling／EC2 自動擴展

**正確答案**
Amazon EC2 Auto Scaling／EC2 自動擴展

**為什麼正確**
**Amazon EC2 Auto Scaling** 會根據需求自動增加或減少 EC2 執行個體數量，確保應用有適當容量處理目前流量。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Application Load Balancer／應用程式負載平衡器 | ❌ 錯誤 | ALB 分配流量，但不增加或減少 EC2 容量。 |
| Multi-AZ deployment／多 AZ 部署 | ❌ 錯誤 | Multi-AZ 提升可用性，不自動調整容量。 |
| Network Load Balancer／網路負載平衡器 | ❌ 錯誤 | NLB 做第 4 層負載分配，不管理容量。 |
| Amazon EC2 Auto Scaling／EC2 自動擴展 | ✅ 正確 | EC2 Auto Scaling 自動維持所需容量。 |

---

## 問題 61

**題目**
Which of the following are recommended security best practices for the AWS account root user? (Select two)
以下哪些是 AWS 帳戶根使用者的推薦安全最佳實務？（選兩項）

**[選項]**
- A. Keep your AWS account root user access keys in an encrypted file on Amazon S3／將 root access keys 存在 S3 加密檔案
- B. Disable MFA for the root user as it can lock the entire AWS account if the MFA device is lost／停用 root MFA
- C. Share AWS account root user access keys with other administrators／與管理員共享 root access keys
- D. Enable multi-factor authentication (MFA) for the AWS account root user／為 root 啟用 MFA
- E. Set up an IAM user with administrator permissions and do not use AWS account root user for administrative tasks／建立 IAM 管理員，不用 root 做日常管理

**正確答案**
Enable MFA for the AWS account root user／為 root 啟用 MFA；Set up an IAM user with administrator permissions and do not use AWS account root user for administrative tasks／建立 IAM 管理員並避免 root 日常使用

**為什麼正確**
Root 使用者權限極高，最佳實務是啟用 MFA、不要建立或使用 root access keys，並建立具管理權限的 IAM 使用者或角色處理日常管理。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Store root access keys in S3／將 root 金鑰存 S3 | ❌ 錯誤 | 應避免建立 root access keys；若已有應刪除。 |
| Disable MFA for root／停用 root MFA | ❌ 錯誤 | root 應啟用 MFA；MFA 遺失有恢復流程。 |
| Share root access keys／共享 root 金鑰 | ❌ 錯誤 | 不應共享 root 憑證。 |
| Enable MFA for root／為 root 啟用 MFA | ✅ 正確 | MFA 是 root 安全基本要求。 |
| Set up IAM admin and avoid root daily tasks／建立 IAM 管理員不用 root | ✅ 正確 | 日常管理應用 IAM 身分，不用 root。 |

---

## 問題 62

**題目**
Reserved Instance (RI) pricing is available for which of the following AWS services? (Select two)
保留執行個體（RI）定價適用於以下哪些 AWS 服務？（選兩項）

**[選項]**
- A. Amazon Simple Storage Service (Amazon S3)／物件儲存
- B. Amazon CloudFront／內容交付網路
- C. AWS Identity and Access Management (AWS IAM)／身分與存取管理
- D. Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器
- E. Amazon Relational Database Service (Amazon RDS)／關聯式資料庫

**正確答案**
Amazon Elastic Compute Cloud (Amazon EC2)／虛擬伺服器；Amazon Relational Database Service (Amazon RDS)／關聯式資料庫

**為什麼正確**
**EC2** 提供 Reserved Instances；**RDS** 提供 Reserved DB Instances，可用承諾期換取較低價格。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3／物件儲存 | ❌ 錯誤 | S3 沒有 RI 定價，依儲存與請求等用量收費。 |
| Amazon CloudFront／內容交付網路 | ❌ 錯誤 | CloudFront 沒有 EC2/RDS 類型的 RI。 |
| AWS IAM／身分與存取管理 | ❌ 錯誤 | IAM 是免費服務，無 RI。 |
| Amazon EC2／虛擬伺服器 | ✅ 正確 | EC2 支援 RI 定價。 |
| Amazon RDS／關聯式資料庫 | ✅ 正確 | RDS 支援 Reserved DB Instance 定價。 |

---

## 問題 63

**題目**
A firm wants to maintain the same data on Amazon S3 between its production account and multiple test accounts, retaining object metadata. Which technique should you choose?
一家公司希望在其生產帳戶和多個測試帳戶之間在 Amazon S3 上維護相同的資料，同時保留物件中繼資料。您應選擇哪種技術？

**[選項]**
- A. Amazon S3 Bucket Policy／S3 儲存貯體政策
- B. Amazon S3 Storage Classes／S3 儲存類別
- C. Amazon S3 Transfer Acceleration (S3TA)／S3 傳輸加速
- D. Amazon S3 Replication／S3 複寫

**正確答案**
Amazon S3 Replication／S3 複寫

**為什麼正確**
**Amazon S3 Replication** 可自動、非同步地將物件從來源 bucket 複寫到一個或多個目的 bucket，可跨帳戶並保留物件中繼資料。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3 Bucket Policy／S3 儲存貯體政策 | ❌ 錯誤 | Bucket policy 控制存取權，不複製資料。 |
| Amazon S3 Storage Classes／S3 儲存類別 | ❌ 錯誤 | 儲存類別影響成本與存取模式，不同步資料。 |
| Amazon S3 Transfer Acceleration／S3 傳輸加速 | ❌ 錯誤 | S3TA 加速上傳/下載，不維護跨帳戶資料副本。 |
| Amazon S3 Replication／S3 複寫 | ✅ 正確 | S3 Replication 可跨 bucket/帳戶複寫物件並保留 metadata。 |

---

## 問題 64

**題目**
The QA team at a company wants a tool/service that can provide access to different mobile devices with variations in firmware and Operating System versions. Which AWS service can address this use case?
一家公司的 QA 團隊需要一個工具/服務，可以存取具有不同韌體和作業系統版本的各種行動裝置。哪個 AWS 服務可以解決此使用案例？

**[選項]**
- A. AWS Elastic Beanstalk／應用部署平台
- B. AWS Mobile Farm／行動裝置農場
- C. AWS CodePipeline／持續交付管道
- D. AWS Device Farm／裝置測試農場

**正確答案**
AWS Device Farm／裝置測試農場

**為什麼正確**
**AWS Device Farm** 可在多種真實行動裝置、瀏覽器、韌體與作業系統版本上測試應用程式，適合 QA 團隊進行相容性測試。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Elastic Beanstalk／應用部署平台 | ❌ 錯誤 | Beanstalk 用於部署 Web 應用程式。 |
| AWS Mobile Farm／行動裝置農場 | ❌ 錯誤 | 不是正確 AWS 服務名稱。 |
| AWS CodePipeline／持續交付管道 | ❌ 錯誤 | CodePipeline 編排 CI/CD 流程，不提供真實行動裝置測試環境。 |
| AWS Device Farm／裝置測試農場 | ✅ 正確 | Device Farm 提供多裝置與多 OS 版本測試。 |

---

## 問題 65

**題目**
Which of the following AWS Support plans provide programmatic access to AWS Support Center features to create, manage and close your support cases? (Select two)
以下哪些 AWS Support 方案提供對 AWS Support Center 功能的程式化存取，以建立、管理和關閉支援案例？（選兩項）

**[選項]**
- A. AWS Developer Support／開發者支援
- B. AWS Basic Support／基本支援
- C. AWS Corporate Support／企業公司支援
- D. AWS Enterprise Support／企業支援
- E. AWS Business Support／商業支援

**正確答案**
AWS Enterprise Support／企業支援；AWS Business Support／商業支援

**為什麼正確**
**AWS Support API** 提供程式化建立、管理和關閉支援案例的能力，Business Support 與 Enterprise Support 等較高階支援方案可使用。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Developer Support／開發者支援 | ❌ 錯誤 | Developer Support 不提供 Support API 程式化存取。 |
| AWS Basic Support／基本支援 | ❌ 錯誤 | Basic Support 不提供建立技術支援案例的 API 存取。 |
| AWS Corporate Support／企業公司支援 | ❌ 錯誤 | 這不是標準 AWS Support 方案名稱。 |
| AWS Enterprise Support／企業支援 | ✅ 正確 | Enterprise Support 支援程式化存取 Support Center 功能。 |
| AWS Business Support／商業支援 | ✅ 正確 | Business Support 可使用 AWS Support API 管理支援案例。 |

---

