# AWS CCP 06 選項解析

來源：
- 題目與選項：[AWS_CCP_Practice_Test6.md](AWS_CCP_Practice_Test6.md)
- 原詳解：[AWS_CCP_06.md](AWS_CCP_06.md)

這份檔案針對每題列出中英對照題目與選項，並用中文說明正確答案與其他選項的差異。

---

## 問題 1

**題目**
A company provides you with a completed product that is run and managed by the company itself. As a customer, you only use the product without worrying about maintaining or managing the product. Which cloud computing model does this kind of product belong to?
一家公司提供給你一個由該公司自行運行和管理的完整產品。作為客戶，你只需使用該產品，無需擔心維護或管理。這種產品屬於哪種雲端運算模型？

**[選項]**
A. Product as a Service (Paas)／產品即服務
B. Infrastructure as a Service (IaaS)／基礎設施即服務
C. Platform as a Service (PaaS)／平台即服務
D. Software as a Service (SaaS)／軟體即服務

**正確答案**
Software as a Service (SaaS)／軟體即服務

**為什麼正確**
**SaaS** 是由供應商提供完整且已運行的產品，客戶只需要使用軟體，不需要管理底層基礎設施、平台或應用維護。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Product as a Service (Paas)／產品即服務 | ❌ 錯誤 | 這不是標準雲端服務模型，且 Paas 拼法也容易和 PaaS 混淆。 |
| Infrastructure as a Service (IaaS)／基礎設施即服務 | ❌ 錯誤 | IaaS 仍需客戶管理作業系統、應用程式與資料。 |
| Platform as a Service (PaaS)／平台即服務 | ❌ 錯誤 | PaaS 讓客戶部署與管理自己的應用程式，不是只使用完整產品。 |
| Software as a Service (SaaS)／軟體即服務 | ✅ 正確 | SaaS 由供應商管理完整產品，客戶只負責使用。 |

---

## 問題 2

**題目**
As part of a flexible pricing model, AWS offers two types of Savings Plans. Which of the following are the Savings Plans from AWS?
作為彈性定價模型的一部分，AWS 提供兩種 Savings Plans。以下哪項是 AWS 的 Savings Plans？

**[選項]**
A. Compute Savings Plans, Storage Savings Plans／運算節省計畫、儲存節省計畫
B. Reserved Instances (RI) Savings Plans, EC2 Instance Savings Plans／預留執行個體節省計畫、EC2 執行個體節省計畫
C. Instance Savings Plans, Storage Savings Plans／執行個體節省計畫、儲存節省計畫
D. Compute Savings Plans, EC2 Instance Savings Plans／運算節省計畫、EC2 執行個體節省計畫

**正確答案**
Compute Savings Plans, EC2 Instance Savings Plans／運算節省計畫、EC2 執行個體節省計畫

**為什麼正確**
AWS Savings Plans 主要分為 **Compute Savings Plans** 與 **EC2 Instance Savings Plans**。前者彈性較高，可涵蓋 EC2、Fargate、Lambda；後者針對特定 Region 與 EC2 執行個體家族。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Compute Savings Plans, Storage Savings Plans／運算節省計畫、儲存節省計畫 | ❌ 錯誤 | Compute Savings Plans 正確，但 Storage Savings Plans 不是此題所問的標準類型。 |
| Reserved Instances (RI) Savings Plans, EC2 Instance Savings Plans／預留執行個體節省計畫、EC2 執行個體節省計畫 | ❌ 錯誤 | Reserved Instances 是另一種折扣模型，不是 Savings Plans 類型。 |
| Instance Savings Plans, Storage Savings Plans／執行個體節省計畫、儲存節省計畫 | ❌ 錯誤 | 名稱不完整，且 Storage Savings Plans 不符合題目。 |
| Compute Savings Plans, EC2 Instance Savings Plans／運算節省計畫、EC2 執行個體節省計畫 | ✅ 正確 | 這是 AWS Savings Plans 的兩種主要類型。 |

---

## 問題 3

**題目**
A company is looking for ways to make its desktop applications available to the employees from browsers on their devices/laptops. Which AWS service will help achieve this requirement without having to procure servers or maintain infrastructure?
一家公司希望讓員工能透過裝置/筆電的瀏覽器存取桌面應用程式。哪項 AWS 服務可在無需採購伺服器或維護基礎設施的情況下實現此需求？

**[選項]**
A. Amazon WorkSpaces
B. AWS Outposts
C. AWS Snowball
D. Amazon AppStream 2.0

**正確答案**
Amazon AppStream 2.0

**為什麼正確**
**Amazon AppStream 2.0** 是全受管應用程式串流服務，可將桌面應用程式安全串流到使用者瀏覽器，無需自行採購或維護串流基礎設施。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon WorkSpaces | ❌ 錯誤 | WorkSpaces 提供完整虛擬桌面，不是只將特定桌面應用串流到瀏覽器的最佳答案。 |
| AWS Outposts | ❌ 錯誤 | Outposts 將 AWS 基礎設施延伸到本地資料中心。 |
| AWS Snowball | ❌ 錯誤 | Snowball 用於離線資料遷移與邊緣運算，不是應用程式串流。 |
| Amazon AppStream 2.0 | ✅ 正確 | AppStream 2.0 將桌面應用程式串流到瀏覽器。 |

---

## 問題 4

**題目**
Which of the following points have to be considered when choosing an AWS Region for a service? (Select two)
選擇 AWS 區域時，需考慮以下哪些因素？（選兩項）

**[選項]**
A. The AWS Region with high availability index should be considered for your business／應選擇高可用性指數的 AWS 區域
B. The AWS Region should have 5G networks／AWS 區域應具備 5G 網路
C. The AWS Region chosen should have all its AZs within 100 Kms radius／所選區域的所有 AZ 應在 100 公里半徑內
D. Compliance and Data Residency guidelines of the AWS Region should match your business requirements／AWS 區域的合規及資料駐留規定應符合業務需求
E. AWS Region chosen should be geographically closer to the user base／所選 AWS 區域應在地理位置上靠近使用者群

**正確答案**
Compliance and Data Residency guidelines of the AWS Region should match your business requirements／AWS 區域的合規及資料駐留規定應符合業務需求；AWS Region chosen should be geographically closer to the user base／所選 AWS 區域應在地理位置上靠近使用者群

**為什麼正確**
選擇 AWS Region 時，常見考量包含合規與資料駐留、服務可用性、成本，以及與使用者的地理距離。資料所在地要求與低延遲需求是本題最直接的兩個因素。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| The AWS Region with high availability index should be considered for your business／應選擇高可用性指數的 AWS 區域 | ❌ 錯誤 | AWS 不用「高可用性指數」作為正式選 Region 標準。 |
| The AWS Region should have 5G networks／AWS 區域應具備 5G 網路 | ❌ 錯誤 | 5G 不是一般選擇 AWS Region 的必要條件。 |
| The AWS Region chosen should have all its AZs within 100 Kms radius／所選區域的所有 AZ 應在 100 公里半徑內 | ❌ 錯誤 | 這不是客戶選 Region 時需檢查的標準。 |
| Compliance and Data Residency guidelines of the AWS Region should match your business requirements／AWS 區域的合規及資料駐留規定應符合業務需求 | ✅ 正確 | 法規與資料駐留要求常決定資料必須放在哪個 Region。 |
| AWS Region chosen should be geographically closer to the user base／所選 AWS 區域應在地理位置上靠近使用者群 | ✅ 正確 | 靠近使用者可降低延遲並改善體驗。 |

---

## 問題 5

**題目**
A company is planning to move their traditional CRM application running on MySQL to an AWS database service. Which database service is the right fit for this requirement?
一家公司計畫將其運行在 MySQL 上的傳統 CRM 應用程式遷移至 AWS 資料庫服務。哪項資料庫服務最適合此需求？

**[選項]**
A. Amazon DynamoDB
B. Amazon ElastiCache
C. Amazon Neptune
D. Amazon Aurora

**正確答案**
Amazon Aurora

**為什麼正確**
**Amazon Aurora** 是相容 MySQL 與 PostgreSQL 的關聯式資料庫服務。傳統 MySQL CRM 遷移到 AWS 時，Aurora MySQL 相容性與受管能力很符合需求。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon DynamoDB | ❌ 錯誤 | DynamoDB 是 NoSQL 鍵值/文件資料庫，不是 MySQL 相容關聯式資料庫。 |
| Amazon ElastiCache | ❌ 錯誤 | ElastiCache 是快取服務，不是 CRM 主資料庫。 |
| Amazon Neptune | ❌ 錯誤 | Neptune 是圖形資料庫，適合關聯圖譜資料。 |
| Amazon Aurora | ✅ 正確 | Aurora 支援 MySQL 相容引擎，適合 MySQL 應用遷移。 |

---

## 問題 6

**題目**
A team manager needs data about the changes that have taken place for AWS resources in his account during the past two weeks. Which AWS service can help get this data?
一位團隊經理需要了解其帳戶中 AWS 資源在過去兩週內所發生的變更資料。哪項 AWS 服務可提供此資料？

**[選項]**
A. Amazon CloudWatch
B. AWS CloudTrail
C. Amazon Inspector
D. AWS Config

**正確答案**
AWS Config

**為什麼正確**
**AWS Config** 會記錄 AWS 資源的組態歷史與變更時間線，可用來查詢過去一段時間資源「變成什麼樣子」以及何時變更。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon CloudWatch | ❌ 錯誤 | CloudWatch 主要監控指標、日誌與告警，不是資源組態歷史服務。 |
| AWS CloudTrail | ❌ 錯誤 | CloudTrail 記錄 API 呼叫與使用者活動，重點是「誰做了什麼」。 |
| Amazon Inspector | ❌ 錯誤 | Inspector 做漏洞與安全評估。 |
| AWS Config | ✅ 正確 | Config 可追蹤 AWS 資源設定變更與歷史。 |

---

## 問題 7

**題目**
Which of the following services/tools offers a user-friendly graphical user interface to manage AWS Snowball devices without a need for command-line interface or REST APIs?
以下哪項服務/工具提供友善的圖形使用者介面，無需命令列或 REST API 即可管理 AWS Snowball 裝置？

**[選項]**
A. AppStream 2.0
B. AWS Config
C. AWS Transfer Family
D. AWS OpsHub

**正確答案**
AWS OpsHub

**為什麼正確**
**AWS OpsHub** 是用來管理 Snowball 裝置的圖形化工具，可協助解鎖、設定、拖放資料、監控裝置與啟動應用程式。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AppStream 2.0 | ❌ 錯誤 | AppStream 2.0 是應用程式串流服務。 |
| AWS Config | ❌ 錯誤 | Config 追蹤資源組態變更，不管理 Snowball 裝置。 |
| AWS Transfer Family | ❌ 錯誤 | Transfer Family 提供 SFTP/FTPS/FTP 等檔案傳輸端點。 |
| AWS OpsHub | ✅ 正確 | OpsHub 提供 Snowball 裝置的圖形化管理介面。 |

---

## 問題 8

**題目**
An e-commerce company needs to generate custom reports and graphs every week for analyzing the product sales data. The company is looking at a tool/service that will help them analyze this data using interactive dashboards with minimal effort. The dashboards also need to be accessible from any device. Which AWS tool/service will you recommend for this use-case?
一家電商公司每週需要生成自訂報表和圖表來分析產品銷售資料，希望以最少的工作量透過互動式儀表板分析資料，且儀表板需可從任何裝置存取。你推薦哪項 AWS 工具/服務？

**[選項]**
A. Amazon SageMaker
B. Amazon Athena
C. AWS Glue
D. Amazon QuickSight

**正確答案**
Amazon QuickSight

**為什麼正確**
**Amazon QuickSight** 是雲端商業智慧服務，可建立互動式儀表板、報表與圖表，並可從多種裝置存取。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon SageMaker | ❌ 錯誤 | SageMaker 是機器學習建模平台，不是 BI 儀表板工具。 |
| Amazon Athena | ❌ 錯誤 | Athena 用 SQL 查詢 S3 資料，不負責建立互動式商業儀表板。 |
| AWS Glue | ❌ 錯誤 | Glue 是 ETL/資料整合服務，用於準備資料。 |
| Amazon QuickSight | ✅ 正確 | QuickSight 可用最少工作量建立互動式報表與儀表板。 |

---

## 問題 9

**題目**
A company is looking at real-time processing of streaming big data for their ad-tech platform. Which of the following AWS services is the right choice for this requirement?
一家公司希望對其廣告技術平台的串流大數據進行即時處理。以下哪項 AWS 服務最適合此需求？

**[選項]**
A. Amazon Redshift
B. Amazon Simple Queue Service (Amazon SQS)
C. Amazon EMR
D. Amazon Kinesis Data Streams

**正確答案**
Amazon Kinesis Data Streams

**為什麼正確**
**Amazon Kinesis Data Streams** 用於即時擷取與處理串流資料，適合廣告技術、點擊流、日誌與即時分析等大數據串流場景。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Redshift | ❌ 錯誤 | Redshift 是資料倉儲，主要用於分析查詢，不是即時串流擷取服務。 |
| Amazon Simple Queue Service (Amazon SQS) | ❌ 錯誤 | SQS 是訊息佇列，用於解耦，不是串流大數據處理平台。 |
| Amazon EMR | ❌ 錯誤 | EMR 可處理大數據，但題目強調即時串流，Kinesis 更適合。 |
| Amazon Kinesis Data Streams | ✅ 正確 | Kinesis Data Streams 專為即時串流資料處理設計。 |

---

## 問題 10

**題目**
Which AWS service is used to store and commit code privately and also offer features for version control?
哪項 AWS 服務用於私密地儲存和提交程式碼，並提供版本控制功能？

**[選項]**
A. AWS CodePipeline
B. AWS CodeBuild
C. AWS CodeStar
D. AWS CodeCommit

**正確答案**
AWS CodeCommit

**為什麼正確**
**AWS CodeCommit** 是全受管原始碼控制服務，可私密儲存 Git 儲存庫並提供版本控制。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS CodePipeline | ❌ 錯誤 | CodePipeline 編排 CI/CD 流程，不是原始碼儲存庫。 |
| AWS CodeBuild | ❌ 錯誤 | CodeBuild 負責建置與測試程式碼。 |
| AWS CodeStar | ❌ 錯誤 | CodeStar 是整合開發專案管理工具，不是版本控制儲存庫本身。 |
| AWS CodeCommit | ✅ 正確 | CodeCommit 提供私有 Git 儲存庫與版本控制。 |

---

## 問題 11

**題目**
Which of the following statements are true about AWS Regions and Availability Zones (AZ)? (Select two)
以下哪些關於 AWS 區域和可用區（AZ）的陳述是正確的？（選兩項）

**[選項]**
A. AWS calls each group of logical data centers as AWS Regions／AWS 將每組邏輯資料中心稱為 AWS 區域
B. Traffic between AZs is not encrypted by default, but can be configured／AZ 之間的流量預設未加密，但可設定
C. An AZ is a physical location where AWS clusters the data centers／AZ 是 AWS 集群資料中心的實體位置
D. Each AWS Region consists of multiple, isolated, and physically separate AZs within a geographic area／每個 AWS 區域由地理區域內多個隔離且實體分開的 AZ 組成
E. All traffic between Availability Zones (AZ) is encrypted／所有 AZ 之間的流量均已加密

**正確答案**
Each AWS Region consists of multiple, isolated, and physically separate AZs within a geographic area／每個 AWS 區域由地理區域內多個隔離且實體分開的 AZ 組成；All traffic between Availability Zones (AZ) is encrypted／所有 AZ 之間的流量均已加密

**為什麼正確**
AWS Region 是地理區域，內含多個彼此隔離且實體分離的 AZ；AWS 也會對 AZ 之間的流量進行加密。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS calls each group of logical data centers as AWS Regions／AWS 將每組邏輯資料中心稱為 AWS 區域 | ❌ 錯誤 | 一組資料中心通常對應 AZ；Region 是包含多個 AZ 的地理區域。 |
| Traffic between AZs is not encrypted by default, but can be configured／AZ 之間的流量預設未加密，但可設定 | ❌ 錯誤 | 題目來源指出 AZ 之間流量會加密。 |
| An AZ is a physical location where AWS clusters the data centers／AZ 是 AWS 集群資料中心的實體位置 | ❌ 錯誤 | AZ 是一個或多個資料中心組成的邏輯區域，不只是單一實體位置描述。 |
| Each AWS Region consists of multiple, isolated, and physically separate AZs within a geographic area／每個 AWS 區域由地理區域內多個隔離且實體分開的 AZ 組成 | ✅ 正確 | 這是 Region 與 AZ 的正確關係。 |
| All traffic between Availability Zones (AZ) is encrypted／所有 AZ 之間的流量均已加密 | ✅ 正確 | AZ 之間的流量會經過加密。 |

---

## 問題 12

**題目**
Which of the following data sources are used by Amazon Detective to analyze events and identify potential security issues?
Amazon Detective 使用以下哪些資料來源來分析事件並識別潛在安全問題？

**[選項]**
A. Amazon CloudWatch Logs, Amazon VPC Flow Logs and Amazon GuardDuty findings
B. Amazon CloudWatch Logs, AWS CloudTrail logs and Amazon S3 Access Logs
C. Amazon CloudWatch Logs, AWS CloudTrail logs and Amazon Inspector logs
D. AWS CloudTrail logs, Amazon VPC Flow Logs, and Amazon GuardDuty findings／AWS CloudTrail 日誌、Amazon VPC 流量日誌和 Amazon GuardDuty 調查結果

**正確答案**
AWS CloudTrail logs, Amazon VPC Flow Logs, and Amazon GuardDuty findings／AWS CloudTrail 日誌、Amazon VPC 流量日誌和 Amazon GuardDuty 調查結果

**為什麼正確**
**Amazon Detective** 會從 CloudTrail、VPC Flow Logs 與 GuardDuty findings 建立安全調查圖譜，協助分析事件與找出潛在安全問題。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon CloudWatch Logs, Amazon VPC Flow Logs and Amazon GuardDuty findings | ❌ 錯誤 | 缺少 CloudTrail，且 CloudWatch Logs 不是本題正確來源組合。 |
| Amazon CloudWatch Logs, AWS CloudTrail logs and Amazon S3 Access Logs | ❌ 錯誤 | 包含錯誤來源，缺少 VPC Flow Logs 與 GuardDuty findings。 |
| Amazon CloudWatch Logs, AWS CloudTrail logs and Amazon Inspector logs | ❌ 錯誤 | Inspector logs 不是本題對應的 Detective 資料來源組合。 |
| AWS CloudTrail logs, Amazon VPC Flow Logs, and Amazon GuardDuty findings／AWS CloudTrail 日誌、Amazon VPC 流量日誌和 Amazon GuardDuty 調查結果 | ✅ 正確 | Detective 使用這些資料來源進行安全調查分析。 |

---

## 問題 13

**題目**
Which of the following statements are correct regarding the AWS Shared Responsibility Model? (Select two)
以下哪些關於 AWS 共同責任模型的陳述是正確的？（選兩項）

**[選項]**
A. For abstracted services such as Amazon S3, AWS operates encryption options and appropriate permissions for accessing S3 resources／對於 S3 等抽象化服務，AWS 負責加密選項及存取 S3 資源的適當權限
B. AWS maintains the configuration of its infrastructure devices and is responsible for configuring the guest operating systems, databases, and applications／AWS 負責設定訪客作業系統、資料庫和應用程式
C. Amazon EC2 is categorized as IaaS and hence AWS will perform all of the necessary security configuration and management tasks／EC2 屬於 IaaS，因此 AWS 負責所有安全設定和管理工作
D. AWS trains AWS employees, but a customer must train their own employees／AWS 訓練 AWS 員工，但客戶必須訓練自己的員工
E. AWS is responsible for patching and fixing flaws within the infrastructure, but customers are responsible for patching their guest OS and applications／AWS 負責修補基礎設施缺陷，但客戶負責修補其訪客作業系統和應用程式

**正確答案**
AWS trains AWS employees, but a customer must train their own employees／AWS 訓練 AWS 員工，但客戶必須訓練自己的員工；AWS is responsible for patching and fixing flaws within the infrastructure, but customers are responsible for patching their guest OS and applications／AWS 負責修補基礎設施缺陷，但客戶負責修補其訪客作業系統和應用程式

**為什麼正確**
共同責任模型中，AWS 負責雲端本身，例如基礎設施修補與 AWS 員工訓練；客戶負責雲端中的安全，例如員工訓練、客體 OS 與應用程式修補。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| For abstracted services such as Amazon S3, AWS operates encryption options and appropriate permissions for accessing S3 resources／對於 S3 等抽象化服務，AWS 負責加密選項及存取 S3 資源的適當權限 | ❌ 錯誤 | S3 的資料、加密選項與存取權限由客戶設定與管理。 |
| AWS maintains the configuration of its infrastructure devices and is responsible for configuring the guest operating systems, databases, and applications／AWS 負責設定訪客作業系統、資料庫和應用程式 | ❌ 錯誤 | Guest OS、資料庫與應用程式設定通常是客戶責任。 |
| Amazon EC2 is categorized as IaaS and hence AWS will perform all of the necessary security configuration and management tasks／EC2 屬於 IaaS，因此 AWS 負責所有安全設定和管理工作 | ❌ 錯誤 | EC2 是 IaaS，因此客戶仍需管理 OS、應用與安全設定。 |
| AWS trains AWS employees, but a customer must train their own employees／AWS 訓練 AWS 員工，但客戶必須訓練自己的員工 | ✅ 正確 | 人員訓練依各自組織負責。 |
| AWS is responsible for patching and fixing flaws within the infrastructure, but customers are responsible for patching their guest OS and applications／AWS 負責修補基礎設施缺陷，但客戶負責修補其訪客作業系統和應用程式 | ✅ 正確 | AWS 修補底層基礎設施，客戶修補自己管理的 OS 與應用。 |

---

## 問題 14

**題目**
Which of the below services are encrypted by default and need no user intervention to enable encryption?
以下哪些服務預設已加密，無需使用者介入即可啟用加密？

**[選項]**
A. Amazon CloudWatch logs, Application Load Balancer (ALB), Amazon S3 Glacier
B. AWS Storage Gateway, Application Load Balancer (ALB), Amazon CloudFront
C. AWS Organizations, Amazon EC2, AWS CloudTrail Logs
D. AWS CloudTrail Logs, Amazon S3 Glacier, AWS Storage Gateway

**正確答案**
AWS CloudTrail Logs, Amazon S3 Glacier, AWS Storage Gateway

**為什麼正確**
題目來源指出 **AWS CloudTrail Logs、Amazon S3 Glacier、AWS Storage Gateway** 都具備預設加密，使用者不需要額外介入即可啟用基本加密。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon CloudWatch logs, Application Load Balancer (ALB), Amazon S3 Glacier | ❌ 錯誤 | ALB 不是此題列出的預設加密服務組合。 |
| AWS Storage Gateway, Application Load Balancer (ALB), Amazon CloudFront | ❌ 錯誤 | 包含 ALB 與 CloudFront，不符合題目正確組合。 |
| AWS Organizations, Amazon EC2, AWS CloudTrail Logs | ❌ 錯誤 | EC2 的資料加密需要客戶依儲存服務設定。 |
| AWS CloudTrail Logs, Amazon S3 Glacier, AWS Storage Gateway | ✅ 正確 | 這三者符合題目所問預設加密且無需使用者介入的組合。 |

---

## 問題 15

**題目**
An e-commerce company has its on-premises data storage on an NFS file system that is accessed in parallel by multiple applications. Which storage service should the company use to move their files to AWS Cloud seamlessly if the application is hosted on Amazon EC2 instances?
一家電商公司的本地資料儲存在 NFS 檔案系統上，可被多個應用程式並行存取。若應用程式託管於 EC2，應使用哪項儲存服務將檔案無縫遷移至 AWS 雲端？

**[選項]**
A. Amazon Elastic Block Store (Amazon EBS)
B. Amazon Simple Storage Service (Amazon S3)
C. AWS Storage Gateway
D. Amazon Elastic File System (Amazon EFS)

**正確答案**
Amazon Elastic File System (Amazon EFS)

**為什麼正確**
**Amazon EFS** 是受管 NFS 檔案系統，可供多個 EC2 執行個體同時掛載與存取，符合 NFS 與多應用平行存取需求。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Elastic Block Store (Amazon EBS) | ❌ 錯誤 | EBS 是區塊儲存，通常掛載到單一 EC2，不是共享 NFS 檔案系統。 |
| Amazon Simple Storage Service (Amazon S3) | ❌ 錯誤 | S3 是物件儲存，不是原生 NFS 檔案系統。 |
| AWS Storage Gateway | ❌ 錯誤 | Storage Gateway 做混合雲儲存整合，但題目 EC2 上共享 NFS 檔案服務更適合 EFS。 |
| Amazon Elastic File System (Amazon EFS) | ✅ 正確 | EFS 支援 NFS 與多個 EC2 並行存取。 |

---

## 問題 16

**題目**
A university provides access to AWS services for its students to submit their research data for analysis. The university is looking at the most cost-effective approach for recovering from disasters and it can tolerate data loss of a few hours. Which disaster recovery strategy is well-suited for this use case?
一所大學為學生提供 AWS 服務存取以提交研究資料進行分析，正在尋找最具成本效益的災難復原方案，且可承受數小時的資料損失。哪種災難復原策略最適合此使用案例？

**[選項]**
A. Warm standby strategy／暖備策略
B. Multi-site active/active strategy／多站點主動/主動策略
C. Pilot light strategy／導引燈策略
D. Backup and restore strategy／備份與還原策略

**正確答案**
Backup and restore strategy／備份與還原策略

**為什麼正確**
**Backup and Restore** 成本最低，但 RTO/RPO 較高。題目可接受數小時資料遺失並追求最具成本效益，因此最適合。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Warm standby strategy／暖備策略 | ❌ 錯誤 | Warm standby 成本較高，適合更低 RTO/RPO。 |
| Multi-site active/active strategy／多站點主動/主動策略 | ❌ 錯誤 | Active/active 成本最高，適合最嚴格可用性需求。 |
| Pilot light strategy／導引燈策略 | ❌ 錯誤 | Pilot light 保留核心系統，恢復比備份還原快但成本較高。 |
| Backup and restore strategy／備份與還原策略 | ✅ 正確 | 成本最低，適合可接受數小時資料遺失的場景。 |

---

## 問題 17

**題目**
An organization in the US plans to launch a new product line and needs additional IT infrastructure to support the workload. They want a solution that enables rapid deployment of resources and minimizes setup time. Which advantages of cloud computing can help the organization achieve this goal? (Select two)
美國一家機構計畫推出新產品線，需要額外的 IT 基礎設施來支援工作負載，並希望快速部署資源並最小化設定時間。哪些雲端運算優勢可幫助實現此目標？（選兩項）

**[選項]**
A. Benefit from massive economies of scale／受益於大規模經濟效益
B. Trade fixed expense for variable expense／將固定費用轉為可變費用
C. Go global in minutes／幾分鐘內實現全球化
D. Enable automatic scaling of resources based on demand／根據需求自動擴展資源
E. Increase speed and agility／提升速度和敏捷性

**正確答案**
Enable automatic scaling of resources based on demand／根據需求自動擴展資源；Increase speed and agility／提升速度和敏捷性

**為什麼正確**
題目強調快速部署與最少設定時間，對應雲端的速度與敏捷性；同時可依需求自動擴展，快速支援新產品線工作負載。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Benefit from massive economies of scale／受益於大規模經濟效益 | ❌ 錯誤 | 這是雲端優勢之一，但不直接對應快速部署與自動擴展。 |
| Trade fixed expense for variable expense／將固定費用轉為可變費用 | ❌ 錯誤 | 這是成本模型優勢，不是題目重點。 |
| Go global in minutes／幾分鐘內實現全球化 | ❌ 錯誤 | 題目沒有強調全球部署。 |
| Enable automatic scaling of resources based on demand／根據需求自動擴展資源 | ✅ 正確 | 自動擴展可快速配合新工作負載需求。 |
| Increase speed and agility／提升速度和敏捷性 | ✅ 正確 | 雲端能快速佈建資源並減少設定時間。 |

---

## 問題 18

**題目**
Which of the following are the security best practices suggested by AWS for IAM? (Select two)
以下哪些是 AWS 針對 IAM 建議的安全最佳實務？（選兩項）

**[選項]**
A. Do not change passwords and access keys once created／密碼和存取金鑰一旦建立就不要更改
B. Share your AWS account root user credentials only if absolutely necessary／僅在絕對必要時共享根使用者憑證
C. Enable MFA on your root user account to give root access to multiple users without sharing credentials／啟用 MFA 讓多個使用者無需共享憑證即可獲得根存取權限
D. Do not share security credentials between accounts, use IAM roles instead／不要在帳戶之間共享安全憑證，改用 IAM 角色
E. When you create IAM policies, grant the least privileges required to perform a task／建立 IAM 政策時，授予執行任務所需的最少權限

**正確答案**
Do not share security credentials between accounts, use IAM roles instead／不要在帳戶之間共享安全憑證，改用 IAM 角色；When you create IAM policies, grant the least privileges required to perform a task／建立 IAM 政策時，授予執行任務所需的最少權限

**為什麼正確**
IAM 最佳實務包含避免共享長期憑證、改用角色取得臨時憑證，以及依最小權限原則授予完成任務所需的最低權限。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Do not change passwords and access keys once created／密碼和存取金鑰一旦建立就不要更改 | ❌ 錯誤 | 應定期輪替與管理憑證，而不是永不變更。 |
| Share your AWS account root user credentials only if absolutely necessary／僅在絕對必要時共享根使用者憑證 | ❌ 錯誤 | 根使用者憑證不應共享，應建立 IAM 使用者或角色。 |
| Enable MFA on your root user account to give root access to multiple users without sharing credentials／啟用 MFA 讓多個使用者無需共享憑證即可獲得根存取權限 | ❌ 錯誤 | MFA 是保護根使用者，不是讓多人取得 root access。 |
| Do not share security credentials between accounts, use IAM roles instead／不要在帳戶之間共享安全憑證，改用 IAM 角色 | ✅ 正確 | 跨帳戶存取應使用 IAM role。 |
| When you create IAM policies, grant the least privileges required to perform a task／建立 IAM 政策時，授予執行任務所需的最少權限 | ✅ 正確 | 最小權限是 IAM 核心安全最佳實務。 |

---

## 問題 19

**題目**
Which feature of the AWS Cloud refers to right-sizing the resources?
AWS 雲端的哪項特性是指對資源進行合理調整（right-sizing）？

**[選項]**
A. Resiliency／韌性
B. Reliability／可靠性
C. Horizontal scaling／水平擴展
D. Elasticity／彈性

**正確答案**
Elasticity／彈性

**為什麼正確**
**Elasticity** 指依需求取得、調整並釋放資源，避免過度佈建或資源不足，也就是讓資源大小更貼近實際需求。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Resiliency／韌性 | ❌ 錯誤 | 韌性著重在從故障或中斷中恢復。 |
| Reliability／可靠性 | ❌ 錯誤 | 可靠性指工作負載穩定執行預期功能。 |
| Horizontal scaling／水平擴展 | ❌ 錯誤 | 水平擴展是增加更多節點，不等同整體 right-sizing 特性。 |
| Elasticity／彈性 | ✅ 正確 | 彈性代表依需求調整資源大小。 |

---

## 問題 20

**題目**
Per the AWS Shared Responsibility Model, management of which of the following AWS services is the responsibility of the customer?
根據 AWS 共同責任模型，以下哪項 AWS 服務的管理是客戶的責任？

**[選項]**
A. Amazon DynamoDB
B. AWS Elastic Beanstalk
C. Amazon Simple Storage Service (Amazon S3)
D. Amazon Elastic Compute Cloud (Amazon EC2)

**正確答案**
Amazon Elastic Compute Cloud (Amazon EC2)

**為什麼正確**
**Amazon EC2** 是 IaaS，客戶需要管理客體作業系統、應用程式、修補、網路與安全設定；其他選項多為更高階受管或抽象服務。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon DynamoDB | ❌ 錯誤 | DynamoDB 是受管 NoSQL 資料庫，底層管理由 AWS 負責。 |
| AWS Elastic Beanstalk | ❌ 錯誤 | Beanstalk 是 PaaS，AWS 協助管理多數平台基礎設施。 |
| Amazon Simple Storage Service (Amazon S3) | ❌ 錯誤 | S3 是抽象化儲存服務，客戶管理資料與權限但不管理服務本身。 |
| Amazon Elastic Compute Cloud (Amazon EC2) | ✅ 正確 | EC2 需要客戶管理 OS、應用程式與相關安全設定。 |

---

## 問題 21

**題目**
As part of log analysis, you have realized that one or more AWS-owned IP addresses are being used for port scanning your on-premises server. Which service/team should you connect to resolve this issue?
在日誌分析過程中，你發現一個或多個 AWS 擁有的 IP 位址正在對你的本地伺服器進行連接埠掃描。你應聯繫哪個服務/團隊來解決此問題？

**[選項]**
A. Reach out to Werner Vogels, the CTO of Amazon／聯繫 Amazon CTO Werner Vogels
B. Use AWS Trusted Advisor to log a complaint／使用 AWS Trusted Advisor 提出投訴
C. Contact AWS Support／聯繫 AWS Support
D. Contact AWS Abuse team／聯繫 AWS 濫用團隊

**正確答案**
Contact AWS Abuse team／聯繫 AWS 濫用團隊

**為什麼正確**
若發現 AWS-owned IP 涉及 port scanning、DDoS、垃圾郵件、惡意軟體等濫用行為，應聯繫 **AWS Abuse team** 處理。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Reach out to Werner Vogels, the CTO of Amazon／聯繫 Amazon CTO Werner Vogels | ❌ 錯誤 | 這不是正式通報 AWS 濫用事件的管道。 |
| Use AWS Trusted Advisor to log a complaint／使用 AWS Trusted Advisor 提出投訴 | ❌ 錯誤 | Trusted Advisor 提供最佳實務建議，不處理濫用投訴。 |
| Contact AWS Support／聯繫 AWS Support | ❌ 錯誤 | 一般支援不是處理 AWS IP 濫用回報的最佳指定團隊。 |
| Contact AWS Abuse team／聯繫 AWS 濫用團隊 | ✅ 正確 | AWS Abuse team 負責處理濫用與惡意行為回報。 |

---

## 問題 22

**題目**
An organization is looking to break down its AWS spending so that each department and project can be accurately charged for the resources they consume. Which AWS feature or service is the best fit for this use-case?
一家機構希望細分其 AWS 支出，以便每個部門和專案能夠準確地為其消耗的資源計費。哪項 AWS 功能或服務最適合此使用案例？

**[選項]**
A. AWS Cost and Usage Report (CUR)
B. AWS Marketplace
C. AWS Budgets
D. AWS cost allocation tags／AWS 成本分配標籤

**正確答案**
AWS cost allocation tags／AWS 成本分配標籤

**為什麼正確**
**成本分配標籤** 可用部門、專案、成本中心等鍵值標記資源，讓成本報表依業務維度拆分支出。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Cost and Usage Report (CUR) | ❌ 錯誤 | CUR 提供詳細成本資料，但通常需搭配標籤才能按部門/專案歸屬。 |
| AWS Marketplace | ❌ 錯誤 | Marketplace 用於購買第三方軟體與服務。 |
| AWS Budgets | ❌ 錯誤 | Budgets 用於預算與告警，不是成本歸屬標記本身。 |
| AWS cost allocation tags／AWS 成本分配標籤 | ✅ 正確 | 成本分配標籤最適合按部門與專案拆分成本。 |

---

## 問題 23

**題目**
A company wants to establish a private, dedicated connection between AWS and its on-premises data center. Which AWS service is the right choice for this requirement?
一家公司希望在 AWS 和其本地資料中心之間建立私有的專用連接。哪項 AWS 服務是正確選擇？

**[選項]**
A. Amazon CloudFront
B. AWS Site-to-Site VPN
C. Amazon API Gateway
D. AWS Direct Connect

**正確答案**
AWS Direct Connect

**為什麼正確**
**AWS Direct Connect** 提供從本地資料中心到 AWS 的專用私有網路連線，適合需要穩定、高頻寬與不經公網的連接。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon CloudFront | ❌ 錯誤 | CloudFront 是 CDN，不是本地到 AWS 的專線。 |
| AWS Site-to-Site VPN | ❌ 錯誤 | VPN 透過公網建立加密連線，不是專用私有連接。 |
| Amazon API Gateway | ❌ 錯誤 | API Gateway 用於建立與管理 API。 |
| AWS Direct Connect | ✅ 正確 | Direct Connect 提供私有、專用的本地到 AWS 連線。 |

---

## 問題 24

**題目**
Which of the following is the least effort way to encrypt data for AWS services only in your AWS account using AWS KMS?
使用 AWS KMS 為 AWS 帳戶中的 AWS 服務加密資料，以下哪種方式最省力？

**[選項]**
A. Create your own customer managed keys (CMKs) in AWS KMS／在 AWS KMS 中建立自己的客戶管理金鑰
B. Use AWS owned CMK in the service you wish to use encryption／在要使用加密的服務中使用 AWS 擁有的 CMK
C. Use AWS KMS APIs to encrypt data within your own application by using the AWS Encryption SDK／使用 AWS 加密 SDK 透過 KMS API 在應用程式中加密資料
D. Use AWS managed master keys that are automatically created in your account for each service／使用為每項服務自動在帳戶中建立的 AWS 受管主金鑰

**正確答案**
Use AWS managed master keys that are automatically created in your account for each service／使用為每項服務自動在帳戶中建立的 AWS 受管主金鑰

**為什麼正確**
**AWS managed keys** 由 AWS 代客戶在帳戶中為各服務建立與管理，適合想用 KMS 加密 AWS 服務資料、但不想自行建立與維護金鑰的最省力方式。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Create your own customer managed keys (CMKs) in AWS KMS／在 AWS KMS 中建立自己的客戶管理金鑰 | ❌ 錯誤 | 客戶管理金鑰控制力高，但需要自行管理，工作量較大。 |
| Use AWS owned CMK in the service you wish to use encryption／在要使用加密的服務中使用 AWS 擁有的 CMK | ❌ 錯誤 | AWS owned keys 不在客戶帳戶中，客戶不可見也不可管理。 |
| Use AWS KMS APIs to encrypt data within your own application by using the AWS Encryption SDK／使用 AWS 加密 SDK 透過 KMS API 在應用程式中加密資料 | ❌ 錯誤 | 這需要應用程式整合與開發工作，不是最省力。 |
| Use AWS managed master keys that are automatically created in your account for each service／使用為每項服務自動在帳戶中建立的 AWS 受管主金鑰 | ✅ 正確 | AWS 受管金鑰會自動建立並由 AWS 管理，最省力。 |

---

## 問題 25

**題目**
An e-learning company wants to build a knowledge graph by leveraging a fully managed database. Which of the following is the best fit for this requirement?
一家電子學習公司希望利用全受管資料庫建立知識圖譜。以下哪項最適合此需求？

**[選項]**
A. Amazon Relational Database Service (Amazon RDS)
B. Amazon DynamoDB
C. Amazon DocumentDB
D. Amazon Neptune

**正確答案**
Amazon Neptune

**為什麼正確**
**Amazon Neptune** 是全受管圖形資料庫，適合知識圖譜、身分圖譜、詐騙偵測、推薦引擎與社群關聯資料。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Relational Database Service (Amazon RDS) | ❌ 錯誤 | RDS 是關聯式資料庫，不是圖形資料庫首選。 |
| Amazon DynamoDB | ❌ 錯誤 | DynamoDB 是鍵值/文件 NoSQL，不是圖形資料庫。 |
| Amazon DocumentDB | ❌ 錯誤 | DocumentDB 是文件資料庫，適合 JSON 文件模型。 |
| Amazon Neptune | ✅ 正確 | Neptune 是全受管圖形資料庫，適合知識圖譜。 |

---

## 問題 26

**題目**
Which of the following statements are correct regarding the health monitoring and reporting capabilities supported by AWS Elastic Beanstalk? (Select two)
以下哪些關於 AWS Elastic Beanstalk 支援的健康監控和報告功能的陳述是正確的？（選兩項）

**[選項]**
A. AWS Elastic Beanstalk provides only basic health reporting system; Combined with ELB, they provide advanced health check features／Elastic Beanstalk 僅提供基本健康報告系統，與 ELB 結合才提供進階健康檢查功能
B. The basic health reporting system does not use health checks performed by ELB／基本健康報告系統不使用 ELB 執行的健康檢查
C. In a single instance environment, Elastic Beanstalk determines the instance's health by monitoring the ELB health settings／在單一執行個體環境中，Elastic Beanstalk 透過監控 ELB 健康設定來確定執行個體健康狀況
D. The Elastic Beanstalk health monitoring can determine that the environment's Auto Scaling group is available and has a minimum of at least one instance／Elastic Beanstalk 健康監控可確定環境的 Auto Scaling 群組可用且至少有一個執行個體
E. With basic health reporting, the Elastic Beanstalk service does not publish any metrics to Amazon CloudWatch／使用基本健康報告時，Elastic Beanstalk 不會將任何指標發布至 Amazon CloudWatch

**正確答案**
The Elastic Beanstalk health monitoring can determine that the environment's Auto Scaling group is available and has a minimum of at least one instance／Elastic Beanstalk 健康監控可確定環境的 Auto Scaling 群組可用且至少有一個執行個體；With basic health reporting, the Elastic Beanstalk service does not publish any metrics to Amazon CloudWatch／使用基本健康報告時，Elastic Beanstalk 不會將任何指標發布至 Amazon CloudWatch

**為什麼正確**
Elastic Beanstalk 健康監控會檢查環境是否有可用執行個體與 Auto Scaling 群組狀態；基本健康報告本身不由 Beanstalk 發布 CloudWatch 指標。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Elastic Beanstalk provides only basic health reporting system; Combined with ELB, they provide advanced health check features／Elastic Beanstalk 僅提供基本健康報告系統，與 ELB 結合才提供進階健康檢查功能 | ❌ 錯誤 | Beanstalk 支援基本與增強健康報告，不是只有基本健康報告。 |
| The basic health reporting system does not use health checks performed by ELB／基本健康報告系統不使用 ELB 執行的健康檢查 | ❌ 錯誤 | 負載平衡環境會使用 ELB 健康檢查資訊。 |
| In a single instance environment, Elastic Beanstalk determines the instance's health by monitoring the ELB health settings／在單一執行個體環境中，Elastic Beanstalk 透過監控 ELB 健康設定來確定執行個體健康狀況 | ❌ 錯誤 | 單一執行個體環境沒有 ELB，通常依 EC2 狀態判斷。 |
| The Elastic Beanstalk health monitoring can determine that the environment's Auto Scaling group is available and has a minimum of at least one instance／Elastic Beanstalk 健康監控可確定環境的 Auto Scaling 群組可用且至少有一個執行個體 | ✅ 正確 | Beanstalk 健康監控可檢查環境容量與 Auto Scaling 狀態。 |
| With basic health reporting, the Elastic Beanstalk service does not publish any metrics to Amazon CloudWatch／使用基本健康報告時，Elastic Beanstalk 不會將任何指標發布至 Amazon CloudWatch | ✅ 正確 | 基本健康報告不由 Beanstalk 服務發布 CloudWatch 指標。 |

---

## 問題 27

**題目**
As a Cloud Practitioner, which of the following credentials would you recommend for signing in to the AWS Management Console to meet security best practices? (Select two)
作為雲端從業人員，你會推薦使用以下哪些憑證登入 AWS 管理主控台以符合安全最佳實務？（選兩項）

**[選項]**
A. Access Key ID／存取金鑰 ID
B. X.509 certificate／X.509 憑證
C. Secret Access Key／秘密存取金鑰
D. IAM Username and password／IAM 使用者名稱和密碼
E. Multi Factor Authentication (MFA)／多重要素驗證

**正確答案**
IAM Username and password／IAM 使用者名稱和密碼；Multi Factor Authentication (MFA)／多重要素驗證

**為什麼正確**
登入 AWS Management Console 需要使用者名稱與密碼；為符合安全最佳實務，應搭配 MFA 強化登入保護。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Access Key ID／存取金鑰 ID | ❌ 錯誤 | Access key 用於程式化/API 存取，不用於主控台登入。 |
| X.509 certificate／X.509 憑證 | ❌ 錯誤 | 這不是一般 AWS Management Console 登入憑證。 |
| Secret Access Key／秘密存取金鑰 | ❌ 錯誤 | Secret access key 與 access key ID 搭配做 API 存取。 |
| IAM Username and password／IAM 使用者名稱和密碼 | ✅ 正確 | IAM 使用者名稱與密碼可用於登入主控台。 |
| Multi Factor Authentication (MFA)／多重要素驗證 | ✅ 正確 | MFA 是登入主控台的安全最佳實務。 |

---

## 問題 28

**題目**
Which of the following statements are correct regarding the AWS Support Plans? (Select two)
以下哪些關於 AWS 支援計畫的陳述是正確的？（選兩項）

**[選項]**
A. AWS Concierge service is available for the AWS Business Support and AWS Enterprise Support plans／AWS Concierge 服務適用於商業和企業支援計畫
B. Infrastructure Event Management is included for free for Business and Enterprise Support plans and can be extended to Developer Support plan for an additional fee／基礎設施事件管理免費包含在商業和企業支援計畫中，可付費延伸至開發人員支援計畫
C. Contextual guidance based on customer use-case, is available only for the AWS Enterprise support plan／基於客戶使用案例的情境指導僅適用於企業支援計畫
D. Both Basic and AWS Developer Support plans have access to the core Trusted Advisor checks only／基本和開發人員支援計畫僅能存取核心 Trusted Advisor 檢查
E. A designated Technical Account Manager is available only for AWS Enterprise Support plan／指定技術客戶經理僅適用於 AWS 企業支援計畫

**正確答案**
Both Basic and AWS Developer Support plans have access to the core Trusted Advisor checks only／基本和開發人員支援計畫僅能存取核心 Trusted Advisor 檢查；A designated Technical Account Manager is available only for AWS Enterprise Support plan／指定技術客戶經理僅適用於 AWS 企業支援計畫

**為什麼正確**
Basic 與 Developer Support 只能使用核心 Trusted Advisor 檢查；專屬 Technical Account Manager 是 Enterprise Support 的特色。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Concierge service is available for the AWS Business Support and AWS Enterprise Support plans／AWS Concierge 服務適用於商業和企業支援計畫 | ❌ 錯誤 | Concierge 服務不是 Business Support 的一般功能。 |
| Infrastructure Event Management is included for free for Business and Enterprise Support plans and can be extended to Developer Support plan for an additional fee／基礎設施事件管理免費包含在商業和企業支援計畫中，可付費延伸至開發人員支援計畫 | ❌ 錯誤 | IEM 的包含與付費方式不符合此敘述，Developer 也不是此延伸對象。 |
| Contextual guidance based on customer use-case, is available only for the AWS Enterprise support plan／基於客戶使用案例的情境指導僅適用於企業支援計畫 | ❌ 錯誤 | Use-case guidance 不是 Enterprise 專屬。 |
| Both Basic and AWS Developer Support plans have access to the core Trusted Advisor checks only／基本和開發人員支援計畫僅能存取核心 Trusted Advisor 檢查 | ✅ 正確 | Basic 與 Developer 只可用核心 Trusted Advisor 檢查。 |
| A designated Technical Account Manager is available only for AWS Enterprise Support plan／指定技術客戶經理僅適用於 AWS 企業支援計畫 | ✅ 正確 | 專屬 TAM 是 Enterprise Support 的重要功能。 |

---

## 問題 29

**題目**
A manufacturing company is looking at a service that can offer AWS infrastructure, AWS services, APIs, and tools to its on-premises data center for running low latency applications. Which of the following service/tool is the best fit for the given requirement?
一家製造公司希望在其本地資料中心提供 AWS 基礎設施、服務、API 和工具，以運行低延遲應用程式。哪項服務/工具最適合此需求？

**[選項]**
A. AWS Wavelength
B. AWS Snow Family
C. AWS Local Zones
D. AWS Outposts

**正確答案**
AWS Outposts

**為什麼正確**
**AWS Outposts** 將 AWS 基礎設施、服務、API 與工具延伸到客戶本地資料中心，適合本地低延遲、資料駐留或應用互依需求。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Wavelength | ❌ 錯誤 | Wavelength 位於電信商 5G 邊緣，用於行動網路超低延遲。 |
| AWS Snow Family | ❌ 錯誤 | Snow Family 用於離線資料遷移與邊緣運算，不提供完整本地 AWS 基礎設施體驗。 |
| AWS Local Zones | ❌ 錯誤 | Local Zones 是靠近大城市的 AWS 延伸區，不是部署到客戶資料中心。 |
| AWS Outposts | ✅ 正確 | Outposts 將 AWS 硬體與服務放到本地資料中心。 |

---

## 問題 30

**題目**
A blogging company is looking at an easy to use solution to host WordPress blogs. The company needs a cost-effective, readily available solution without the need to manage the configurations for servers or the databases. Which AWS service will help you achieve this functionality?
一家部落格公司希望找到一個易於使用的解決方案來託管 WordPress 部落格，需要一個具成本效益、隨時可用的解決方案，且無需管理伺服器或資料庫設定。哪項 AWS 服務可實現此功能？

**[選項]**
A. AWS Fargate
B. Amazon Elastic Compute Cloud (EC2) with Amazon S3 for storage
C. Host the application directly on Amazon S3
D. Amazon Lightsail

**正確答案**
Amazon Lightsail

**為什麼正確**
**Amazon Lightsail** 提供簡單、低且可預測價格的 VPS 方案，包含一鍵啟動 WordPress 等應用，適合不想管理複雜伺服器與資料庫設定的部落格。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Fargate | ❌ 錯誤 | Fargate 是無伺服器容器運算，部署 WordPress 仍需更多架構設定。 |
| Amazon Elastic Compute Cloud (EC2) with Amazon S3 for storage | ❌ 錯誤 | EC2 需要自行管理伺服器與應用環境。 |
| Host the application directly on Amazon S3 | ❌ 錯誤 | S3 可託管靜態網站，但 WordPress 是動態應用。 |
| Amazon Lightsail | ✅ 正確 | Lightsail 提供簡單且可快速啟動的 WordPress 託管方案。 |

---

## 問題 31

**題目**
A healthcare company wants to implement a continuous replication based disaster recovery mechanism and provide fast, reliable recovery of physical, virtual, and cloud-based servers into AWS Cloud. Which of the following represents the best-fit solution for this use case?
一家醫療公司希望實施基於持續複製的災難復原機制，並提供將實體、虛擬和雲端伺服器快速可靠地恢復到 AWS 雲端的能力。哪項解決方案最適合此使用案例？

**[選項]**
A. AWS Storage Gateway
B. AWS Snowball Edge
C. CloudCover Disaster Recovery
D. CloudEndure Disaster Recovery

**正確答案**
CloudEndure Disaster Recovery

**為什麼正確**
**CloudEndure Disaster Recovery** 提供持續區塊級複製與快速恢復，可將實體、虛擬與雲端伺服器復原到 AWS。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Storage Gateway | ❌ 錯誤 | Storage Gateway 是混合雲儲存整合，不是完整持續複製 DR 解決方案。 |
| AWS Snowball Edge | ❌ 錯誤 | Snowball Edge 用於離線搬遷與邊緣運算，不是持續複製 DR。 |
| CloudCover Disaster Recovery | ❌ 錯誤 | 不是此題對應的 AWS DR 解決方案。 |
| CloudEndure Disaster Recovery | ✅ 正確 | CloudEndure DR 支援持續複製與快速復原到 AWS。 |

---

## 問題 32

**題目**
A company is looking at a service/tool to automate and minimize the time spent on keeping the server images up-to-date. These server images are used by Amazon EC2 instances as well as the on-premises systems. Which AWS service will help achieve the company's need?
一家公司希望自動化並最小化保持伺服器映像更新所花費的時間，這些伺服器映像供 EC2 執行個體和本地系統使用。哪項 AWS 服務可滿足此需求？

**[選項]**
A. Amazon EC2 Amazon Machine Image (AMI)
B. AWS CloudFormation templates
C. AWS Systems Manager (SSM)
D. Amazon EC2 Image Builder

**正確答案**
Amazon EC2 Image Builder

**為什麼正確**
**Amazon EC2 Image Builder** 可自動化建立、測試與發佈伺服器映像，支援 AWS 與本地系統使用，降低手動維護 AMI 或映像的時間。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon EC2 Amazon Machine Image (AMI) | ❌ 錯誤 | AMI 是映像本身，不是自動化維護映像流程的服務。 |
| AWS CloudFormation templates | ❌ 錯誤 | CloudFormation 佈建資源，不專門維護伺服器映像。 |
| AWS Systems Manager (SSM) | ❌ 錯誤 | Systems Manager 可管理節點與修補，但題目問自動化映像建立與更新。 |
| Amazon EC2 Image Builder | ✅ 正確 | Image Builder 專門自動化映像建立、測試與更新。 |

---

## 問題 33

**題目**
AWS Support offers five support plans for its customers. Which of the following features are covered as part of the AWS Basic Support Plan? (Select two)
AWS Support 為客戶提供五種支援計畫。以下哪些功能包含在 AWS 基本支援計畫中？（選兩項）

**[選項]**
A. Infrastructure event management／基礎設施事件管理
B. Use-case guidance／使用案例指導
C. Client-side diagnostic tools／客戶端診斷工具
D. One-on-one responses to account and billing questions／一對一回答帳戶和帳單問題
E. Service health checks／服務健康檢查

**正確答案**
One-on-one responses to account and billing questions／一對一回答帳戶和帳單問題；Service health checks／服務健康檢查

**為什麼正確**
AWS Basic Support 免費提供帳戶與帳單問題支援，以及服務健康檢查等基本支援能力。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Infrastructure event management／基礎設施事件管理 | ❌ 錯誤 | IEM 屬於較高階支援或付費項目，不包含在 Basic。 |
| Use-case guidance／使用案例指導 | ❌ 錯誤 | 使用案例指導不屬於 Basic Support。 |
| Client-side diagnostic tools／客戶端診斷工具 | ❌ 錯誤 | 這不是 Basic Support 的主要包含項目。 |
| One-on-one responses to account and billing questions／一對一回答帳戶和帳單問題 | ✅ 正確 | Basic Support 包含帳戶與帳單問題支援。 |
| Service health checks／服務健康檢查 | ✅ 正確 | Basic Support 可取得服務健康狀態資訊。 |

---

## 問題 34

**題目**
Which of the following statements are correct regarding the AWS Control Tower and Service Control Policies? (Select two)
以下哪些關於 AWS Control Tower 和服務控制政策（SCP）的陳述是正確的？（選兩項）

**[選項]**
A. SCPs, by default, affect all the users in the AWS Organization. They have to be configured to effect only the member accounts, if needed／SCP 預設影響 AWS 組織中的所有使用者，需設定才能僅影響成員帳戶
B. SCPs can help grant permissions to the accounts in your organization／SCP 可以幫助授予組織中帳戶的權限
C. AWS Control Tower helps you deploy a multi-account AWS environment and operate it with day-to-day reminders and recommendations／AWS Control Tower 幫助部署多帳戶環境並以每日提醒和建議來運作
D. AWS Control Tower is an AWS native service providing a pre-defined set of blueprints and guardrails to help customers implement a landing zone for new AWS accounts／AWS Control Tower 是 AWS 原生服務，提供預定義的藍圖和護欄，幫助客戶為新 AWS 帳戶實施登陸區
E. Service Control Policies (SCPs) are a type of organization policy that you can use to manage permissions in your organization／SCP 是一種組織政策，可用於管理組織中的權限

**正確答案**
AWS Control Tower is an AWS native service providing a pre-defined set of blueprints and guardrails to help customers implement a landing zone for new AWS accounts／AWS Control Tower 是 AWS 原生服務，提供預定義的藍圖和護欄，幫助客戶為新 AWS 帳戶實施登陸區；Service Control Policies (SCPs) are a type of organization policy that you can use to manage permissions in your organization／SCP 是一種組織政策，可用於管理組織中的權限

**為什麼正確**
AWS Control Tower 可用藍圖與護欄建立多帳戶 landing zone；SCP 是 AWS Organizations 的政策類型，用來設定成員帳戶的權限上限與治理限制。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| SCPs, by default, affect all the users in the AWS Organization. They have to be configured to effect only the member accounts, if needed／SCP 預設影響 AWS 組織中的所有使用者，需設定才能僅影響成員帳戶 | ❌ 錯誤 | SCP 套用在 root、OU 或帳戶層級，不是單純「所有使用者」概念。 |
| SCPs can help grant permissions to the accounts in your organization／SCP 可以幫助授予組織中帳戶的權限 | ❌ 錯誤 | SCP 不授予權限，只設定最大可用權限邊界。 |
| AWS Control Tower helps you deploy a multi-account AWS environment and operate it with day-to-day reminders and recommendations／AWS Control Tower 幫助部署多帳戶環境並以每日提醒和建議來運作 | ❌ 錯誤 | Control Tower 重點是 landing zone、藍圖與護欄，不是每日提醒建議。 |
| AWS Control Tower is an AWS native service providing a pre-defined set of blueprints and guardrails to help customers implement a landing zone for new AWS accounts／AWS Control Tower 是 AWS 原生服務，提供預定義的藍圖和護欄，幫助客戶為新 AWS 帳戶實施登陸區 | ✅ 正確 | 這是 Control Tower 的核心定位。 |
| Service Control Policies (SCPs) are a type of organization policy that you can use to manage permissions in your organization／SCP 是一種組織政策，可用於管理組織中的權限 | ✅ 正確 | SCP 是 AWS Organizations 中管理權限邊界的組織政策。 |

---

## 問題 35

**題目**
Which AWS service allows you to connect any number of IoT devices to the cloud without requiring you to provision or manage servers?
哪項 AWS 服務允許你將任意數量的 IoT 裝置連接到雲端，而無需佈建或管理伺服器？

**[選項]**
A. AWS Control Tower
B. Amazon Connect
C. AWS IoT Gateway
D. AWS IoT Core

**正確答案**
AWS IoT Core

**為什麼正確**
**AWS IoT Core** 可安全地將大量 IoT 裝置連接到 AWS 雲端，並在無需佈建或管理伺服器的情況下處理裝置訊息與路由。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Control Tower | ❌ 錯誤 | Control Tower 管理多帳戶 landing zone。 |
| Amazon Connect | ❌ 錯誤 | Amazon Connect 是雲端客服中心服務。 |
| AWS IoT Gateway | ❌ 錯誤 | 這不是本題對應的標準 AWS 服務名稱。 |
| AWS IoT Core | ✅ 正確 | IoT Core 可連接與管理大量 IoT 裝置通訊。 |

---

## 問題 36

**題目**
Which tool/service will help you get a forecast of your spending for the next 12 months?
哪項工具/服務可幫助你獲得未來 12 個月支出的預測？

**[選項]**
A. AWS Pricing Calculator
B. AWS Marketplace
C. Consolidated Billing of AWS Organizations
D. AWS Cost Explorer

**正確答案**
AWS Cost Explorer

**為什麼正確**
**AWS Cost Explorer** 可分析歷史成本與用量，並提供未來支出預測，包含未來 12 個月的成本趨勢。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Pricing Calculator | ❌ 錯誤 | Pricing Calculator 用於事前估算特定架構成本，不基於實際用量預測未來 12 個月支出。 |
| AWS Marketplace | ❌ 錯誤 | Marketplace 用於尋找與購買軟體。 |
| Consolidated Billing of AWS Organizations | ❌ 錯誤 | Consolidated Billing 合併多帳戶帳單，不提供成本預測功能。 |
| AWS Cost Explorer | ✅ 正確 | Cost Explorer 可提供成本分析與未來支出預測。 |

---

## 問題 37

**題目**
Which of the following AWS services is delivered globally rather than regionally?
以下哪項 AWS 服務是全球性交付而非區域性交付？

**[選項]**
A. AWS Snowball
B. Amazon Elastic File System (Amazon EFS)
C. Amazon Simple Storage Service (Amazon S3) buckets
D. Amazon WorkSpaces

**正確答案**
Amazon WorkSpaces

**為什麼正確**
在本題來源分類中，**Amazon WorkSpaces** 被列為全球性交付服務；其他選項如 EFS、S3 bucket 與 Snowball 都和特定 Region 或實體位置相關。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Snowball | ❌ 錯誤 | Snowball 是實體資料遷移裝置，與特定地理與區域流程相關。 |
| Amazon Elastic File System (Amazon EFS) | ❌ 錯誤 | EFS 是區域型檔案系統服務。 |
| Amazon Simple Storage Service (Amazon S3) buckets | ❌ 錯誤 | S3 bucket 建立時會選定 Region。 |
| Amazon WorkSpaces | ✅ 正確 | 題目來源將 WorkSpaces 歸為全球性交付服務。 |

---

## 問題 38

**題目**
Which of the following AWS services can be used to continuously monitor both malicious activities as well as unauthorized behavior to protect your AWS accounts and workloads?
以下哪項 AWS 服務可用於持續監控惡意活動和未授權行為，以保護你的 AWS 帳戶和工作負載？

**[選項]**
A. Amazon Inspector
B. AWS Security Hub
C. Amazon Detective
D. Amazon GuardDuty

**正確答案**
Amazon GuardDuty

**為什麼正確**
**Amazon GuardDuty** 是威脅偵測服務，會持續分析 CloudTrail、VPC Flow Logs、DNS logs 等資料，偵測惡意活動與未授權行為。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Inspector | ❌ 錯誤 | Inspector 主要做漏洞與軟體弱點評估。 |
| AWS Security Hub | ❌ 錯誤 | Security Hub 彙總安全發現並提供安全狀態視圖。 |
| Amazon Detective | ❌ 錯誤 | Detective 用於調查安全發現與根因分析。 |
| Amazon GuardDuty | ✅ 正確 | GuardDuty 持續偵測威脅與未授權行為。 |

---

## 問題 39

**題目**
A gaming company needs compute and storage services close to edge locations in order to ensure ultra-low latency for end-users and devices that connect through mobile networks. Which AWS service is the best fit for this requirement?
一家遊戲公司需要靠近邊緣位置的運算和儲存服務，以確保透過行動網路連接的終端使用者和裝置的超低延遲。哪項 AWS 服務最適合此需求？

**[選項]**
A. AWS Snowball Edge
B. AWS Snowball
C. AWS Outposts
D. AWS Wavelength

**正確答案**
AWS Wavelength

**為什麼正確**
**AWS Wavelength** 將 AWS 運算與儲存服務部署在電信商 5G 網路邊緣，適合行動網路裝置的超低延遲應用。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Snowball Edge | ❌ 錯誤 | Snowball Edge 用於離線資料搬遷與邊緣運算，不是 5G 電信邊緣服務。 |
| AWS Snowball | ❌ 錯誤 | Snowball 主要是資料遷移裝置。 |
| AWS Outposts | ❌ 錯誤 | Outposts 部署在客戶本地資料中心，不是行動網路邊緣。 |
| AWS Wavelength | ✅ 正確 | Wavelength 專為 5G/mobile edge 超低延遲場景設計。 |

---

## 問題 40

**題目**
Which pillar of AWS Well-Architected Framework focuses on using IT and computing resources efficiently, while considering the right resource types and sizes based on workload requirements?
AWS Well-Architected Framework 的哪個支柱著重於有效率地使用 IT 和運算資源，同時根據工作負載需求考慮正確的資源類型和大小？

**[選項]**
A. Cost Optimization Pillar／成本最佳化支柱
B. Reliability Pillar／可靠性支柱
C. Operational Excellence Pillar／卓越營運支柱
D. Performance Efficiency Pillar／效能效率支柱

**正確答案**
Performance Efficiency Pillar／效能效率支柱

**為什麼正確**
**Performance Efficiency** 支柱強調有效率使用運算資源，並依工作負載選擇正確資源類型、大小與架構模式。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Cost Optimization Pillar／成本最佳化支柱 | ❌ 錯誤 | 成本最佳化著重避免不必要成本與提升成本效率。 |
| Reliability Pillar／可靠性支柱 | ❌ 錯誤 | 可靠性著重故障復原與持續正確運作。 |
| Operational Excellence Pillar／卓越營運支柱 | ❌ 錯誤 | 卓越營運著重營運流程、觀測、改進與自動化。 |
| Performance Efficiency Pillar／效能效率支柱 | ✅ 正確 | 效能效率關注資源類型、大小與高效使用。 |

---

## 問題 41

**題目**
Which of the following are NoSQL database services from AWS? (Select two)
以下哪些是 AWS 的 NoSQL 資料庫服務？（選兩項）

**[選項]**
A. AWS Storage Gateway
B. Amazon Aurora
C. Amazon Relational Database Service (Amazon RDS)
D. Amazon DocumentDB
E. Amazon Neptune

**正確答案**
Amazon DocumentDB；Amazon Neptune

**為什麼正確**
**Amazon DocumentDB** 是文件型 NoSQL 資料庫，**Amazon Neptune** 是圖形 NoSQL 資料庫；兩者都不是關聯式資料庫。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Storage Gateway | ❌ 錯誤 | Storage Gateway 是混合雲儲存服務，不是資料庫。 |
| Amazon Aurora | ❌ 錯誤 | Aurora 是關聯式資料庫，支援 MySQL/PostgreSQL 相容引擎。 |
| Amazon Relational Database Service (Amazon RDS) | ❌ 錯誤 | RDS 是關聯式資料庫服務。 |
| Amazon DocumentDB | ✅ 正確 | DocumentDB 是文件型 NoSQL 資料庫。 |
| Amazon Neptune | ✅ 正確 | Neptune 是圖形 NoSQL 資料庫。 |

---

## 問題 42

**題目**
A financial consulting company is looking for automated reference deployments, that will speed up the process of deploying its financial solutions on AWS Cloud. The reference deployment should be able to deploy most of the well-known functions of financial services and leave space for customizations, if necessary. Which AWS service will help achieve this requirement?
一家金融諮詢公司正在尋找自動化的參考部署方案，以加速在 AWS 雲端部署金融解決方案的過程，且需能留有自訂空間。哪項 AWS 服務可滿足此需求？

**[選項]**
A. Amazon QuickSight
B. AWS Elastic Beanstalk
C. AWS CloudFormation
D. AWS Partner Solutions (formerly Quick Starts)／AWS 合作夥伴解決方案（前身為 Quick Starts）

**正確答案**
AWS Partner Solutions (formerly Quick Starts)／AWS 合作夥伴解決方案（前身為 Quick Starts）

**為什麼正確**
**AWS Partner Solutions**（原 Quick Starts）提供自動化參考部署、架構說明與 CloudFormation 範本，可快速部署常見解決方案並保留客製空間。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon QuickSight | ❌ 錯誤 | QuickSight 是 BI 與儀表板服務，不是參考部署集合。 |
| AWS Elastic Beanstalk | ❌ 錯誤 | Beanstalk 部署應用程式，不提供金融方案參考架構集合。 |
| AWS CloudFormation | ❌ 錯誤 | CloudFormation 是底層 IaC 工具，Partner Solutions 會使用它，但題目問參考部署服務。 |
| AWS Partner Solutions (formerly Quick Starts)／AWS 合作夥伴解決方案（前身為 Quick Starts） | ✅ 正確 | Partner Solutions 提供自動化參考部署與實作指南。 |

---

## 問題 43

**題目**
A weather-tracking application is built using Amazon DynamoDB. During holidays and travel seasons, the load is high and the read requests consume most of the database resources, increasing overall application latency. Which feature/service will help resolve this issue?
一個天氣追蹤應用程式使用 Amazon DynamoDB 建構。在假日和旅遊旺季，負載很高，讀取請求消耗大部分資料庫資源，導致應用程式延遲增加。哪項功能/服務可解決此問題？

**[選項]**
A. Amazon CloudFront
B. Amazon DynamoDB Regulator
C. Amazon ElastiCache
D. Amazon DynamoDB Accelerator (DAX)

**正確答案**
Amazon DynamoDB Accelerator (DAX)

**為什麼正確**
**DynamoDB Accelerator (DAX)** 是 DynamoDB 相容的記憶體快取，可將讀取延遲降到微秒等級，適合 DynamoDB 讀取密集型工作負載。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon CloudFront | ❌ 錯誤 | CloudFront 是 CDN，主要快取靜態或動態 Web 內容，不是 DynamoDB 原生讀取快取。 |
| Amazon DynamoDB Regulator | ❌ 錯誤 | 這不是正確 AWS 服務名稱。 |
| Amazon ElastiCache | ❌ 錯誤 | ElastiCache 是通用快取，題目指定 DynamoDB，原生方案是 DAX。 |
| Amazon DynamoDB Accelerator (DAX) | ✅ 正確 | DAX 專為 DynamoDB 讀取效能加速。 |

---

## 問題 44

**題目**
A media company uses Amazon S3 for storing all its data. Which storage class should it consider for cost-optimal storage of the data that has random access patterns?
一家媒體公司使用 Amazon S3 儲存所有資料。對於具有隨機存取模式的資料，應考慮哪種儲存類別以實現最優成本儲存？

**[選項]**
A. Amazon S3 Standard (S3 Standard)
B. Amazon S3 Random Access (S3 Random-Access)
C. Amazon S3 Standard-Infrequent Access (S3 Standard-IA)
D. Amazon S3 Intelligent-Tiering (S3 Intelligent-Tiering)

**正確答案**
Amazon S3 Intelligent-Tiering (S3 Intelligent-Tiering)

**為什麼正確**
**S3 Intelligent-Tiering** 會監控物件存取模式，並自動在不同存取層移動資料，適合存取模式未知、隨機或變動的資料。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3 Standard (S3 Standard) | ❌ 錯誤 | S3 Standard 適合頻繁存取，但若存取模式不固定，成本可能不是最佳。 |
| Amazon S3 Random Access (S3 Random-Access) | ❌ 錯誤 | 這不是有效的 S3 儲存類別。 |
| Amazon S3 Standard-Infrequent Access (S3 Standard-IA) | ❌ 錯誤 | Standard-IA 適合不常存取但仍需快速取回的資料，隨機模式可能產生不理想取回成本。 |
| Amazon S3 Intelligent-Tiering (S3 Intelligent-Tiering) | ✅ 正確 | Intelligent-Tiering 會依實際存取自動最佳化成本。 |

---

## 問題 45

**題目**
A company is moving its on-premises application to AWS Cloud. The application uses in-memory caches for running custom workloads. Which Amazon EC2 instance type is the right choice for the given requirement?
一家公司正在將其本地應用程式遷移至 AWS 雲端，該應用程式使用記憶體快取運行自訂工作負載。哪種 EC2 執行個體類型最適合此需求？

**[選項]**
A. Accelerated computing instance types／加速運算執行個體類型
B. Storage Optimized instance types／儲存最佳化執行個體類型
C. Compute Optimized instance types／運算最佳化執行個體類型
D. Memory Optimized instance types／記憶體最佳化執行個體類型

**正確答案**
Memory Optimized instance types／記憶體最佳化執行個體類型

**為什麼正確**
**Memory Optimized** 執行個體適合記憶體內資料庫、快取與需要大量 RAM 的工作負載，符合題目的 in-memory cache。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Accelerated computing instance types／加速運算執行個體類型 | ❌ 錯誤 | 加速運算適合 GPU、FPGA、ML 推理等。 |
| Storage Optimized instance types／儲存最佳化執行個體類型 | ❌ 錯誤 | 儲存最佳化適合高 I/O、本地儲存密集工作負載。 |
| Compute Optimized instance types／運算最佳化執行個體類型 | ❌ 錯誤 | 運算最佳化適合 CPU 密集工作負載。 |
| Memory Optimized instance types／記憶體最佳化執行個體類型 | ✅ 正確 | 記憶體最佳化適合快取與 in-memory workload。 |

---

## 問題 46

**題目**
Which of the following represents the correct scenario where an Auto Scaling group's (ASG) predictive scaling can be effectively used to maintain the required number of AWS resources?
以下哪種情境最適合使用 Auto Scaling 群組的預測性擴展來維持所需的 AWS 資源數量？

**[選項]**
A. To help configure a CloudWatch SQS metric for scaling the group based on the value of the metric／幫助設定 CloudWatch SQS 指標以根據指標值擴展群組
B. To help configure a scaling policy to keep the average aggregate CPU utilization at 40 percent／幫助設定擴展政策使平均 CPU 使用率保持在 40%
C. To manage a fixed number of resources in the Auto Scaling group／管理 Auto Scaling 群組中固定數量的資源
D. To manage a workload that exhibits recurring load patterns that are specific to the day of the week or the time of day／管理具有週期性負載模式（特定於星期幾或一天中某個時段）的工作負載

**正確答案**
To manage a workload that exhibits recurring load patterns that are specific to the day of the week or the time of day／管理具有週期性負載模式（特定於星期幾或一天中某個時段）的工作負載

**為什麼正確**
**Predictive scaling** 會根據歷史資料預測未來需求，特別適合每天或每週出現固定週期性負載的工作負載。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| To help configure a CloudWatch SQS metric for scaling the group based on the value of the metric／幫助設定 CloudWatch SQS 指標以根據指標值擴展群組 | ❌ 錯誤 | 這較接近依指標動態擴展，不是預測性擴展。 |
| To help configure a scaling policy to keep the average aggregate CPU utilization at 40 percent／幫助設定擴展政策使平均 CPU 使用率保持在 40% | ❌ 錯誤 | 這是 target tracking scaling。 |
| To manage a fixed number of resources in the Auto Scaling group／管理 Auto Scaling 群組中固定數量的資源 | ❌ 錯誤 | 固定數量不需要預測性擴展。 |
| To manage a workload that exhibits recurring load patterns that are specific to the day of the week or the time of day／管理具有週期性負載模式（特定於星期幾或一天中某個時段）的工作負載 | ✅ 正確 | 預測性擴展適合週期性負載。 |

---

## 問題 47

**題目**
A Security Group has been changed in an AWS account and the manager of the account has asked you to find out the details of the user who changed it. As a Cloud Practitioner, which AWS service will you use to fetch the necessary information?
AWS 帳戶中的安全群組被更改，帳戶管理者要求你找出更改者的詳細資訊。作為雲端從業人員，你會使用哪項 AWS 服務獲取必要資訊？

**[選項]**
A. Amazon Inspector
B. AWS X-Ray
C. AWS Trusted Advisor
D. AWS CloudTrail

**正確答案**
AWS CloudTrail

**為什麼正確**
**AWS CloudTrail** 記錄 AWS 帳戶中的 API 呼叫與使用者活動。若要查「誰改了安全群組」，CloudTrail 是正確服務。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Inspector | ❌ 錯誤 | Inspector 用於漏洞與安全評估。 |
| AWS X-Ray | ❌ 錯誤 | X-Ray 用於追蹤分散式應用程式請求與效能。 |
| AWS Trusted Advisor | ❌ 錯誤 | Trusted Advisor 提供最佳實務建議，不記錄使用者 API 操作。 |
| AWS CloudTrail | ✅ 正確 | CloudTrail 可查詢修改安全群組的 API 呼叫與使用者。 |

---

## 問題 48

**題目**
As an AWS Cloud Practitioner, you have been tasked to find examples of AWS Cloud solution designs. Which service/feature would you recommend?
作為 AWS 雲端從業人員，你被要求尋找 AWS 雲端解決方案設計範例。你會推薦哪項服務/功能？

**[選項]**
A. AWS Trusted Advisor
B. APN Consulting Partner
C. AWS Marketplace
D. AWS Architecture Center／AWS 架構中心

**正確答案**
AWS Architecture Center／AWS 架構中心

**為什麼正確**
**AWS Architecture Center** 提供參考架構、設計模式、架構圖與 Well-Architected 最佳實務，是查找雲端解決方案設計範例的合適資源。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Trusted Advisor | ❌ 錯誤 | Trusted Advisor 檢查帳戶最佳實務，不提供解決方案設計範例庫。 |
| APN Consulting Partner | ❌ 錯誤 | 合作夥伴可提供顧問服務，但不是題目問的 AWS 架構範例資源。 |
| AWS Marketplace | ❌ 錯誤 | Marketplace 用於購買軟體與解決方案。 |
| AWS Architecture Center／AWS 架構中心 | ✅ 正確 | Architecture Center 提供 AWS 解決方案設計範例與參考架構。 |

---

## 問題 49

**題目**
A company stores all its media files in Amazon S3 which is accessed by an application hosted on Amazon EC2 instances. The company wants to convert these media files into formats that users can playback on mobile devices. Which AWS service/tool helps you achieve this requirement?
一家公司將所有媒體檔案儲存在 Amazon S3 中，由 EC2 上的應用程式存取。公司希望將這些媒體檔案轉換為使用者可在行動裝置上播放的格式。哪項 AWS 服務/工具可實現此需求？

**[選項]**
A. Amazon Transcribe
B. Amazon Comprehend
C. AWS Glue
D. Amazon Elastic Transcoder

**正確答案**
Amazon Elastic Transcoder

**為什麼正確**
**Amazon Elastic Transcoder** 可將 S3 中的媒體檔轉換為適合手機、平板、瀏覽器等裝置播放的格式。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Transcribe | ❌ 錯誤 | Transcribe 將語音轉文字，不做媒體格式轉碼。 |
| Amazon Comprehend | ❌ 錯誤 | Comprehend 是 NLP 文字分析服務。 |
| AWS Glue | ❌ 錯誤 | Glue 是資料整合/ETL 服務，不是媒體轉碼服務。 |
| Amazon Elastic Transcoder | ✅ 正確 | Elastic Transcoder 將媒體檔轉成不同播放格式。 |

---

## 問題 50

**題目**
Which of the following AWS services are offered free of cost? (Select two)
以下哪些 AWS 服務是免費提供的？（選兩項）

**[選項]**
A. Amazon EC2 Spot Instances／Amazon EC2 Spot 執行個體
B. An Elastic IP address, which is chargeable as long as it is associated with an EC2 instance／Elastic IP 位址，只要與 EC2 執行個體關聯就需收費
C. Amazon CloudWatch facilitated detailed monitoring of EC2 instances／Amazon CloudWatch 促進的 EC2 執行個體詳細監控
D. AWS Elastic Beanstalk
E. AWS Auto Scaling

**正確答案**
AWS Elastic Beanstalk；AWS Auto Scaling

**為什麼正確**
**AWS Elastic Beanstalk** 與 **AWS Auto Scaling** 服務本身不另收服務費，使用者只需支付其建立或管理的底層 AWS 資源費用。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon EC2 Spot Instances／Amazon EC2 Spot 執行個體 | ❌ 錯誤 | Spot Instances 有折扣但不是免費。 |
| An Elastic IP address, which is chargeable as long as it is associated with an EC2 instance／Elastic IP 位址，只要與 EC2 執行個體關聯就需收費 | ❌ 錯誤 | Elastic IP 不是此題的免費 AWS 服務。 |
| Amazon CloudWatch facilitated detailed monitoring of EC2 instances／Amazon CloudWatch 促進的 EC2 執行個體詳細監控 | ❌ 錯誤 | EC2 詳細監控會產生成本。 |
| AWS Elastic Beanstalk | ✅ 正確 | Beanstalk 服務本身免費，支付底層資源費用。 |
| AWS Auto Scaling | ✅ 正確 | Auto Scaling 服務本身免費，支付被擴展的底層資源費用。 |

---

## 問題 51

**題目**
Which of the following statements are correct regarding Amazon API Gateway? (Select two)
以下哪些關於 Amazon API Gateway 的陳述是正確的？（選兩項）

**[選項]**
A. Amazon API Gateway creates RESTful APIs, Storage Gateway creates WebSocket APIs／API Gateway 建立 RESTful API，Storage Gateway 建立 WebSocket API
B. Amazon API Gateway does not yet support API result caching／Amazon API Gateway 尚不支援 API 結果快取
C. If an API response is served by the cached data, it is not considered an API call for billing purposes／若 API 回應由快取資料提供，則不計入計費目的的 API 呼叫
D. Amazon API Gateway can call an AWS Lambda function to create the front door of a serverless application／Amazon API Gateway 可呼叫 Lambda 函數以建立無伺服器應用程式的前門
E. API Gateway can be configured to send data directly to Amazon Kinesis Data Stream／API Gateway 可設定為直接將資料傳送至 Amazon Kinesis Data Stream

**正確答案**
Amazon API Gateway can call an AWS Lambda function to create the front door of a serverless application／Amazon API Gateway 可呼叫 Lambda 函數以建立無伺服器應用程式的前門；API Gateway can be configured to send data directly to Amazon Kinesis Data Stream／API Gateway 可設定為直接將資料傳送至 Amazon Kinesis Data Stream

**為什麼正確**
API Gateway 可作為無伺服器應用的前門並觸發 Lambda，也可透過 AWS 服務整合將資料送到 Kinesis Data Streams。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon API Gateway creates RESTful APIs, Storage Gateway creates WebSocket APIs／API Gateway 建立 RESTful API，Storage Gateway 建立 WebSocket API | ❌ 錯誤 | API Gateway 本身支援 REST、HTTP 與 WebSocket API；Storage Gateway 不建立 WebSocket API。 |
| Amazon API Gateway does not yet support API result caching／Amazon API Gateway 尚不支援 API 結果快取 | ❌ 錯誤 | API Gateway 支援快取。 |
| If an API response is served by the cached data, it is not considered an API call for billing purposes／若 API 回應由快取資料提供，則不計入計費目的的 API 呼叫 | ❌ 錯誤 | 快取回應仍可能涉及 API Gateway 計費，不是本題正確敘述。 |
| Amazon API Gateway can call an AWS Lambda function to create the front door of a serverless application／Amazon API Gateway 可呼叫 Lambda 函數以建立無伺服器應用程式的前門 | ✅ 正確 | API Gateway 常與 Lambda 組成無伺服器 API。 |
| API Gateway can be configured to send data directly to Amazon Kinesis Data Stream／API Gateway 可設定為直接將資料傳送至 Amazon Kinesis Data Stream | ✅ 正確 | API Gateway 可整合 AWS 服務並直接送資料到 Kinesis。 |

---

## 問題 52

**題目**
Which of the following statements are true about AWS Elastic Beanstalk? (Select two)
以下哪些關於 AWS Elastic Beanstalk 的陳述是正確的？（選兩項）

**[選項]**
A. AWS Elastic Beanstalk supports web applications built on different languages. But, Elastic Beanstalk cannot be used for deploying non-web applications／Elastic Beanstalk 支援不同語言的 Web 應用程式，但不能用於部署非 Web 應用程式
B. AWS Elastic Beanstalk supports Java, .NET, PHP, but does not support Docker web applications／Elastic Beanstalk 支援 Java、.NET、PHP，但不支援 Docker Web 應用程式
C. AWS Elastic Beanstalk automates capacity provisioning, load balancing, and application deployment, but auto-scaling functionality cannot be automated／Elastic Beanstalk 自動化容量佈建、負載平衡和應用程式部署，但無法自動化 Auto Scaling
D. There is no additional charge for AWS Elastic Beanstalk. You pay only for the underlying AWS resources that your application consumes／AWS Elastic Beanstalk 無額外費用，你只需為應用程式消耗的底層 AWS 資源付費
E. With AWS Elastic Beanstalk, you can quickly deploy and manage applications in the AWS Cloud without having to learn about the infrastructure that runs those applications／使用 Elastic Beanstalk，你可以快速部署和管理 AWS 雲端中的應用程式，而無需了解運行這些應用程式的基礎設施

**正確答案**
There is no additional charge for AWS Elastic Beanstalk. You pay only for the underlying AWS resources that your application consumes／AWS Elastic Beanstalk 無額外費用，你只需為應用程式消耗的底層 AWS 資源付費；With AWS Elastic Beanstalk, you can quickly deploy and manage applications in the AWS Cloud without having to learn about the infrastructure that runs those applications／使用 Elastic Beanstalk，你可以快速部署和管理 AWS 雲端中的應用程式，而無需了解運行這些應用程式的基礎設施

**為什麼正確**
Elastic Beanstalk 可快速部署與管理應用程式，協助處理底層容量、負載平衡與自動擴展，且服務本身不另收費，只支付底層資源費用。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Elastic Beanstalk supports web applications built on different languages. But, Elastic Beanstalk cannot be used for deploying non-web applications／Elastic Beanstalk 支援不同語言的 Web 應用程式，但不能用於部署非 Web 應用程式 | ❌ 錯誤 | Beanstalk 可支援多種應用部署情境，不限於此敘述。 |
| AWS Elastic Beanstalk supports Java, .NET, PHP, but does not support Docker web applications／Elastic Beanstalk 支援 Java、.NET、PHP，但不支援 Docker Web 應用程式 | ❌ 錯誤 | Elastic Beanstalk 支援 Docker。 |
| AWS Elastic Beanstalk automates capacity provisioning, load balancing, and application deployment, but auto-scaling functionality cannot be automated／Elastic Beanstalk 自動化容量佈建、負載平衡和應用程式部署，但無法自動化 Auto Scaling | ❌ 錯誤 | Beanstalk 可自動化 Auto Scaling。 |
| There is no additional charge for AWS Elastic Beanstalk. You pay only for the underlying AWS resources that your application consumes／AWS Elastic Beanstalk 無額外費用，你只需為應用程式消耗的底層 AWS 資源付費 | ✅ 正確 | Beanstalk 不另收服務費。 |
| With AWS Elastic Beanstalk, you can quickly deploy and manage applications in the AWS Cloud without having to learn about the infrastructure that runs those applications／使用 Elastic Beanstalk，你可以快速部署和管理 AWS 雲端中的應用程式，而無需了解運行這些應用程式的基礎設施 | ✅ 正確 | Beanstalk 簡化應用部署與底層基礎設施管理。 |

---

## 問題 53

**題目**
Which of the following use-cases can be solved using the Amazon Forecast service?
以下哪種使用案例可以使用 Amazon Forecast 服務解決？

**[選項]**
A. To develop and test fully functional machine learning models／開發和測試完整的機器學習模型
B. Document search service that can extract answers from text within documents／可從文件中提取答案的文件搜尋服務
C. To recommend personalized products for users based on their previous purchases／根據使用者過去的購買記錄推薦個人化產品
D. Predict the web traffic of a website for the next few weeks／預測網站未來幾週的網路流量

**正確答案**
Predict the web traffic of a website for the next few weeks／預測網站未來幾週的網路流量

**為什麼正確**
**Amazon Forecast** 是時間序列預測服務，可用於需求、流量、容量、庫存等未來趨勢預測。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| To develop and test fully functional machine learning models／開發和測試完整的機器學習模型 | ❌ 錯誤 | 通用 ML 模型開發應使用 Amazon SageMaker。 |
| Document search service that can extract answers from text within documents／可從文件中提取答案的文件搜尋服務 | ❌ 錯誤 | 文件智慧搜尋更接近 Amazon Kendra。 |
| To recommend personalized products for users based on their previous purchases／根據使用者過去的購買記錄推薦個人化產品 | ❌ 錯誤 | 個人化推薦應使用 Amazon Personalize。 |
| Predict the web traffic of a website for the next few weeks／預測網站未來幾週的網路流量 | ✅ 正確 | Web traffic 是典型時間序列預測場景。 |

---

## 問題 54

**題目**
A financial services company needs to retain its data for 10 years to meet compliance norms. Which Amazon S3 storage class is the best fit for this use case considering that the data has to be stored at a minimal cost?
一家金融服務公司需要將資料保留 10 年以符合合規規範。考慮到資料必須以最低成本儲存，哪種 Amazon S3 儲存類別最適合此使用案例？

**[選項]**
A. Amazon S3 Glacier Flexible Retrieval
B. Amazon S3 Standard-Infrequent Access (S3 Standard-IA)
C. Amazon S3 Intelligent-Tiering
D. Amazon S3 Glacier Deep Archive

**正確答案**
Amazon S3 Glacier Deep Archive

**為什麼正確**
**S3 Glacier Deep Archive** 是 Amazon S3 中最低成本的長期封存儲存類別，適合 7 到 10 年以上的合規保留資料。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon S3 Glacier Flexible Retrieval | ❌ 錯誤 | 適合封存但成本高於 Deep Archive。 |
| Amazon S3 Standard-Infrequent Access (S3 Standard-IA) | ❌ 錯誤 | Standard-IA 適合不常存取但需快速取回的資料，長期最低成本不如 Deep Archive。 |
| Amazon S3 Intelligent-Tiering | ❌ 錯誤 | Intelligent-Tiering 適合未知或變動存取模式，不是最低成本長期封存。 |
| Amazon S3 Glacier Deep Archive | ✅ 正確 | Deep Archive 適合最低成本、長期合規保留。 |

---

## 問題 55

**題目**
A company has defined a baseline that mentions the number of AWS resources to be used for different stages of application testing. However, employees are provisioning additional resources via API calls, resulting in higher testing costs. Which AWS service will help the company raise alarms whenever the baseline resource numbers are crossed?
一家公司定義了應用程式測試不同階段使用的 AWS 資源基準數量，但員工透過 API 呼叫佈建額外資源，導致測試成本增加。哪項 AWS 服務可在超過基準資源數量時發出警報？

**[選項]**
A. Amazon Detective
B. AWS X-Ray
C. AWS Config
D. AWS CloudTrail Insights

**正確答案**
AWS CloudTrail Insights

**為什麼正確**
**AWS CloudTrail Insights** 會分析 CloudTrail 管理事件，偵測 API 呼叫量與行為是否偏離正常基線，並產生 Insights 事件。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Detective | ❌ 錯誤 | Detective 用於安全調查與根因分析，不是 API 呼叫量異常告警基線。 |
| AWS X-Ray | ❌ 錯誤 | X-Ray 追蹤應用程式請求，不監控資源佈建 API 基線。 |
| AWS Config | ❌ 錯誤 | Config 記錄資源組態變更，但題目重點是 API 呼叫行為超出基線。 |
| AWS CloudTrail Insights | ✅ 正確 | CloudTrail Insights 可偵測異常 API 呼叫活動並告警。 |

---

## 問題 56

**題目**
Which of the following AWS services will help provision a logically isolated network for your AWS resources?
以下哪項 AWS 服務可幫助為你的 AWS 資源佈建邏輯隔離的網路？

**[選項]**
A. AWS PrivateLink
B. AWS Firewall Manager
C. Amazon Route 53
D. Amazon Virtual Private Cloud (Amazon VPC)

**正確答案**
Amazon Virtual Private Cloud (Amazon VPC)

**為什麼正確**
**Amazon VPC** 可在 AWS 中建立邏輯隔離的虛擬網路，讓客戶控制 IP 範圍、子網路、路由與網路閘道。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS PrivateLink | ❌ 錯誤 | PrivateLink 用於私有連線到 AWS 服務或服務供應商，不建立整個隔離網路。 |
| AWS Firewall Manager | ❌ 錯誤 | Firewall Manager 集中管理防火牆與安全規則。 |
| Amazon Route 53 | ❌ 錯誤 | Route 53 是 DNS 與網域服務。 |
| Amazon Virtual Private Cloud (Amazon VPC) | ✅ 正確 | VPC 建立 AWS 資源的邏輯隔離網路。 |

---

## 問題 57

**題目**
Which of the following is the responsibility of the customer when running applications using AWS Lambda?
使用 AWS Lambda 運行應用程式時，以下哪項是客戶的責任？

**[選項]**
A. Configuring the networking infrastructure for the Lambda service／設定 Lambda 服務的網路基礎設施
B. Updating the operating system and runtime environment for Lambda functions／更新 Lambda 函數的作業系統和執行環境
C. Managing the physical servers where the Lambda function runs／管理 Lambda 函數運行的實體伺服器
D. Writing and maintaining the function code and its dependencies／編寫和維護函數程式碼及其相依性

**正確答案**
Writing and maintaining the function code and its dependencies／編寫和維護函數程式碼及其相依性

**為什麼正確**
Lambda 是無伺服器服務，AWS 管理底層伺服器、作業系統與運行環境；客戶負責函數程式碼、依賴套件與應用邏輯。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Configuring the networking infrastructure for the Lambda service／設定 Lambda 服務的網路基礎設施 | ❌ 錯誤 | Lambda 服務底層網路基礎設施由 AWS 管理。 |
| Updating the operating system and runtime environment for Lambda functions／更新 Lambda 函數的作業系統和執行環境 | ❌ 錯誤 | 作業系統與受管 Runtime 更新由 AWS 負責。 |
| Managing the physical servers where the Lambda function runs／管理 Lambda 函數運行的實體伺服器 | ❌ 錯誤 | 實體伺服器由 AWS 管理。 |
| Writing and maintaining the function code and its dependencies／編寫和維護函數程式碼及其相依性 | ✅ 正確 | Lambda 客戶負責自己的程式碼與相依性。 |

---

## 問題 58

**題目**
Which free tool helps to review the state of your workloads and compares them to the latest AWS architectural best practices after you have answered a series of questions about your workload?
哪項免費工具可在你回答一系列關於工作負載的問題後，幫助審查工作負載的狀態並與最新的 AWS 架構最佳實務進行比較？

**[選項]**
A. AWS Trusted Advisor
B. AWS Well-Architected Framework
C. AWS Technical Account Manager (TAM)
D. AWS Well-Architected Tool

**正確答案**
AWS Well-Architected Tool

**為什麼正確**
**AWS Well-Architected Tool** 是免費工具，透過一系列問題審查工作負載，並根據 Well-Architected 最佳實務產生改善建議與行動計畫。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS Trusted Advisor | ❌ 錯誤 | Trusted Advisor 根據實際資源提供建議，不是問卷式工作負載審查工具。 |
| AWS Well-Architected Framework | ❌ 錯誤 | Framework 是架構最佳實務框架本身，不是互動式工具。 |
| AWS Technical Account Manager (TAM) | ❌ 錯誤 | TAM 是 Enterprise Support 中的人員角色，不是免費工具。 |
| AWS Well-Architected Tool | ✅ 正確 | Well-Architected Tool 透過問卷審查工作負載並比較最佳實務。 |

---

## 問題 59

**題目**
AWS Web Application Firewall (AWS WAF) can be deployed on which of the following services?
AWS WAF 可部署在以下哪些服務上？

**[選項]**
A. AWS AppSync, Amazon CloudFront, Application Load Balancer, Amazon EC2
B. Amazon CloudFront, Amazon EC2, Amazon API Gateway, Application Load Balancer
C. Application Load Balancer, Amazon EC2, Amazon API Gateway
D. Amazon CloudFront, Application Load Balancer, Amazon API Gateway, AWS AppSync

**正確答案**
Amazon CloudFront, Application Load Balancer, Amazon API Gateway, AWS AppSync

**為什麼正確**
**AWS WAF** 可部署在 Amazon CloudFront、Application Load Balancer、Amazon API Gateway 與 AWS AppSync 等入口服務上，用來檢查與過濾 Web 請求。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS AppSync, Amazon CloudFront, Application Load Balancer, Amazon EC2 | ❌ 錯誤 | AWS WAF 不能直接部署在 EC2 上，通常需透過 ALB 或 CloudFront。 |
| Amazon CloudFront, Amazon EC2, Amazon API Gateway, Application Load Balancer | ❌ 錯誤 | 包含 EC2，組合不正確。 |
| Application Load Balancer, Amazon EC2, Amazon API Gateway | ❌ 錯誤 | 包含 EC2 且缺少 CloudFront/AppSync。 |
| Amazon CloudFront, Application Load Balancer, Amazon API Gateway, AWS AppSync | ✅ 正確 | 這些是 AWS WAF 支援的部署目標。 |

---

## 問題 60

**題目**
A Cloud Practitioner wants to use CIDR block notation when providing an IP address range. Which of the following AWS network services/utilities allow this feature? (Select two)
一位雲端從業人員希望在提供 IP 位址範圍時使用 CIDR 區塊表示法。以下哪些 AWS 網路服務/工具支援此功能？（選兩項）

**[選項]**
A. Amazon Simple Storage Service (Amazon S3)
B. AWS Cost Explorer
C. AWS Lambda
D. Network access control list (network ACL)／網路存取控制清單
E. Security group／安全群組

**正確答案**
Network access control list (network ACL)／網路存取控制清單；Security group／安全群組

**為什麼正確**
Security Group 與 Network ACL 都能用 CIDR 表示法指定來源或目的地 IP 範圍，以控制允許或拒絕的網路流量。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Simple Storage Service (Amazon S3) | ❌ 錯誤 | S3 是物件儲存服務，不是以 CIDR 設定網路流量規則的工具。 |
| AWS Cost Explorer | ❌ 錯誤 | Cost Explorer 是成本分析工具。 |
| AWS Lambda | ❌ 錯誤 | Lambda 是運算服務，不是設定 CIDR 網路規則的安全控制。 |
| Network access control list (network ACL)／網路存取控制清單 | ✅ 正確 | Network ACL 規則可使用 CIDR 區塊。 |
| Security group／安全群組 | ✅ 正確 | Security Group 規則可使用 CIDR 區塊。 |

---

## 問題 61

**題目**
Which of the following will help you control the incoming traffic to an Amazon EC2 instance?
以下哪項可幫助你控制流向 Amazon EC2 執行個體的傳入流量？

**[選項]**
A. Route Table／路由表
B. AWS Resource Group／AWS 資源群組
C. Network access control list (network ACL)／網路存取控制清單
D. Security Group／安全群組

**正確答案**
Security Group／安全群組

**為什麼正確**
**Security Group** 是 EC2 執行個體層級的虛擬防火牆，可控制執行個體的入站與出站流量。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Route Table／路由表 | ❌ 錯誤 | Route Table 決定流量路由方向，不是 EC2 防火牆。 |
| AWS Resource Group／AWS 資源群組 | ❌ 錯誤 | Resource Group 用於組織和批量管理資源。 |
| Network access control list (network ACL)／網路存取控制清單 | ❌ 錯誤 | Network ACL 在子網路層級控制流量；題目問 EC2 執行個體入站流量，Security Group 更直接。 |
| Security Group／安全群組 | ✅ 正確 | Security Group 控制 EC2 執行個體的傳入流量。 |

---

## 問題 62

**題目**
An e-commerce application sends out messages to a downstream application whenever an order is created. The downstream application processes the messages and updates its own systems. Currently, the two applications directly communicate with each other. Which service will you use to decouple this architecture, without any communication loss between the two systems?
一個電商應用程式在每次建立訂單時向下游應用程式發送消息，下游應用程式處理消息並更新其自身系統。目前兩個應用程式直接通訊。你會使用哪項服務來解耦此架構，且不會造成兩個系統之間的通訊損失？

**[選項]**
A. Amazon Kinesis Data Streams
B. AWS Lambda
C. Amazon Simple Notification Service (Amazon SNS)
D. Amazon Simple Queue Service (SQS)

**正確答案**
Amazon Simple Queue Service (SQS)

**為什麼正確**
**Amazon SQS** 是訊息佇列，可在上游與下游系統之間持久保存訊息，讓系統解耦並避免下游暫時不可用時遺失訊息。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Amazon Kinesis Data Streams | ❌ 錯誤 | Kinesis 適合串流資料處理，不是一般訂單處理的訊息佇列首選。 |
| AWS Lambda | ❌ 錯誤 | Lambda 是運算服務，不提供持久訊息佇列。 |
| Amazon Simple Notification Service (Amazon SNS) | ❌ 錯誤 | SNS 是發布/訂閱推送服務，不如 SQS 適合保證單一下游處理且避免通訊遺失。 |
| Amazon Simple Queue Service (SQS) | ✅ 正確 | SQS 可持久保存訊息並解耦兩個系統。 |

---

## 問題 63

**題目**
By default, which of the following events are logged by AWS CloudTrail?
預設情況下，AWS CloudTrail 記錄以下哪種類型的事件？

**[選項]**
A. AWS CloudTrail Insights events／CloudTrail Insights 事件
B. Data events／資料事件
C. Data events and Insights events／資料事件和 Insights 事件
D. Management events／管理事件

**正確答案**
Management events／管理事件

**為什麼正確**
**CloudTrail** 預設記錄管理事件，例如建立或修改 AWS 資源的控制平面操作；資料事件與 Insights 事件通常需額外啟用。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS CloudTrail Insights events／CloudTrail Insights 事件 | ❌ 錯誤 | Insights events 需另外啟用，不是預設記錄。 |
| Data events／資料事件 | ❌ 錯誤 | Data events 需明確設定，通常也會產生額外費用。 |
| Data events and Insights events／資料事件和 Insights 事件 | ❌ 錯誤 | 兩者都不是 CloudTrail 預設記錄類型。 |
| Management events／管理事件 | ✅ 正確 | CloudTrail 預設記錄管理事件。 |

---

## 問題 64

**題目**
Which of the following is a repository service that helps in maintaining application dependencies via integration with commonly used package managers and build tools like Maven, Gradle, npm, etc?
以下哪項是透過與 Maven、Gradle、npm 等常用套件管理器和建置工具整合來幫助維護應用程式相依性的儲存庫服務？

**[選項]**
A. AWS CodeCommit
B. AWS CodeBuild
C. AWS CodeStar
D. AWS CodeArtifact

**正確答案**
AWS CodeArtifact

**為什麼正確**
**AWS CodeArtifact** 是全受管套件儲存庫服務，可整合 Maven、Gradle、npm、yarn、pip、NuGet 等工具，用於儲存、發布與共享應用程式相依套件。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| AWS CodeCommit | ❌ 錯誤 | CodeCommit 是 Git 原始碼儲存庫，不是套件相依儲存庫。 |
| AWS CodeBuild | ❌ 錯誤 | CodeBuild 是建置與測試服務。 |
| AWS CodeStar | ❌ 錯誤 | CodeStar 是開發專案整合管理服務，不是套件儲存庫。 |
| AWS CodeArtifact | ✅ 正確 | CodeArtifact 用於管理與分享套件相依性。 |

---

## 問題 65

**題目**
Which feature/functionality will help you organize your AWS resources, manage and automate tasks on large numbers of resources at a time?
哪項功能可幫助你組織 AWS 資源，並一次管理和自動化大量資源的任務？

**[選項]**
A. Tags／標籤
B. Amazon WorkSpaces
C. AWS Organizations
D. AWS Resource Groups／AWS 資源群組

**正確答案**
AWS Resource Groups／AWS 資源群組

**為什麼正確**
**AWS Resource Groups** 可依標籤、CloudFormation 堆疊等條件將資源分組，方便一次管理與自動化大量資源上的任務。

**選項解析**

| 選項 | 判斷 | 說明 |
|---|---|---|
| Tags／標籤 | ❌ 錯誤 | 標籤是資源元資料，常用來分組，但本身不是批量管理功能。 |
| Amazon WorkSpaces | ❌ 錯誤 | WorkSpaces 是虛擬桌面服務。 |
| AWS Organizations | ❌ 錯誤 | Organizations 管理多個 AWS 帳戶，不是單次批量管理資源的主要功能。 |
| AWS Resource Groups／AWS 資源群組 | ✅ 正確 | Resource Groups 可組織資源並批量管理或自動化任務。 |

---
