# AWS 相似名詞差異填空練習

整理來源：[AWS填空練習_白話文版.md](AWS填空練習_白話文版.md)。

這份是從「相似名詞差異整理」改成的填空題版本。先根據提示猜 `___` 裡是哪個 AWS 名詞，再展開答案看差異重點與關鍵字。

使用方式：

1. 先看題目提示，猜正確名詞。
2. 再展開每章的「答案與差異」。
3. 如果答錯，優先記「它解決什麼問題」和「題目關鍵字」。

---

## 0. 雲端模型與基本概念

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：直接使用現成軟體。差異提示：使用者幾乎只管使用，不管平台和基礎設施。關鍵字：軟體即服務、CRM、Email。
2. `___`：使用平台部署程式。差異提示：主要管程式碼，平台由供應商管理。關鍵字：平台、部署應用。
3. `___`：使用底層運算、儲存、網路。差異提示：控制最多，但作業系統和軟體也要自己管。關鍵字：虛擬伺服器、硬碟、網路。
4. `___`：使用雲端供應商環境。差異提示：資源在 AWS 這類公有雲中。關鍵字：公有雲。
5. `___`：單一組織專用雲端環境。差異提示：通常在公司資料中心或專用環境。關鍵字：私有雲。
6. `___`：本地機房和雲端一起使用。差異提示：連接 On-premises 和 AWS。關鍵字：混合雲。
7. `___`：快速取得資源。差異提示：強調速度與彈性嘗試。關鍵字：快速開資源。
8. `___`：依需求自動增減資源。差異提示：強調流量變動時自動伸縮。關鍵字：流量高加、流量低減。
9. `___`：系統能隨需求變大。差異提示：可以靠水平或垂直擴展。關鍵字：可擴展。
10. `___`：系統穩定運作與故障恢復。差異提示：強調不容易故障，故障後能恢復。關鍵字：可靠、容錯。
11. `___`：服務盡量保持可用。差異提示：強調使用者持續可使用。關鍵字：多 AZ、不中斷。
12. `___`：增加更多機器。差異提示：向外擴展，多台一起分擔。關鍵字：Scale out。
13. `___`：升級單台機器規格。差異提示：向上擴展，CPU 或記憶體變大。關鍵字：Scale up。
14. `___`：元件不要綁太死。差異提示：常用 API、佇列、事件降低互相影響。關鍵字：解耦。
15. `___`：用程式碼管理資源。差異提示：不是手動點選，而是用模板或程式建立。關鍵字：IaC、自動化。
16. `___`：總持有成本。差異提示：不只算伺服器，也算人力、機房、電力等。關鍵字：TCO。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | SaaS | 直接使用現成軟體 | 使用者幾乎只管使用，不管平台和基礎設施 | 軟體即服務、CRM、Email |
| 2 | PaaS | 使用平台部署程式 | 主要管程式碼，平台由供應商管理 | 平台、部署應用 |
| 3 | IaaS | 使用底層運算、儲存、網路 | 控制最多，但作業系統和軟體也要自己管 | 虛擬伺服器、硬碟、網路 |
| 4 | Public Cloud | 使用雲端供應商環境 | 資源在 AWS 這類公有雲中 | 公有雲 |
| 5 | Private Cloud | 單一組織專用雲端環境 | 通常在公司資料中心或專用環境 | 私有雲 |
| 6 | Hybrid Cloud | 本地機房和雲端一起使用 | 連接 On-premises 和 AWS | 混合雲 |
| 7 | Agility | 快速取得資源 | 強調速度與彈性嘗試 | 快速開資源 |
| 8 | Elasticity | 依需求自動增減資源 | 強調流量變動時自動伸縮 | 流量高加、流量低減 |
| 9 | Scalability | 系統能隨需求變大 | 可以靠水平或垂直擴展 | 可擴展 |
| 10 | Reliability | 系統穩定運作與故障恢復 | 強調不容易故障，故障後能恢復 | 可靠、容錯 |
| 11 | High Availability | 服務盡量保持可用 | 強調使用者持續可使用 | 多 AZ、不中斷 |
| 12 | Horizontal Scaling | 增加更多機器 | 向外擴展，多台一起分擔 | Scale out |
| 13 | Vertical Scaling | 升級單台機器規格 | 向上擴展，CPU 或記憶體變大 | Scale up |
| 14 | Loose Coupling | 元件不要綁太死 | 常用 API、佇列、事件降低互相影響 | 解耦 |
| 15 | Infrastructure as Code | 用程式碼管理資源 | 不是手動點選，而是用模板或程式建立 | IaC、自動化 |
| 16 | Total Cost of Ownership | 總持有成本 | 不只算伺服器，也算人力、機房、電力等 | TCO |

</details>

---

## 1. Gateway 系列

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：讓 VPC 內的公開資源連上網際網路，也讓網際網路可連入公開資源。差異提示：是 VPC 對外公開上網的入口，常搭配 Public Subnet、公有 IP、路由表。關鍵字：Public Subnet、公開上網、0.0.0.0/0。
2. `___`：讓 Private Subnet 裡的資源可以主動連出去上網，但外部不能主動連進來。差異提示：解決私有子網路「出得去、進不來」的需求，不是公開入口。關鍵字：Private Subnet、只出不進、更新套件。
3. `___`：Site-to-Site VPN 在 AWS 端的閘道。差異提示：是 VPN 的 AWS 端，不是客戶機房設備。關鍵字：VGW、AWS 端、VPN。
4. `___`：Site-to-Site VPN 在客戶機房端的設備或 AWS 中的對應設定。差異提示：是 VPN 的客戶端，通常代表公司機房的路由器或防火牆。關鍵字：CGW、On-premises、客戶端。
5. `___`：多個 VPC、VPN、Direct Connect 之間的中心轉運站。差異提示：適合連線很多時集中管理，不用每兩個 VPC 都各自 Peering。關鍵字：Hub、集中連接、多 VPC。
6. `___`：建立、發布和管理 REST API、HTTP API、WebSocket API。差異提示：名字有 Gateway，但它是應用層 API 入口，不是 VPC 網路閘道。關鍵字：API、REST、WebSocket、後端入口。
7. `___`：把公司機房儲存和 AWS 雲端儲存接起來。差異提示：名字有 Gateway，但重點是混合雲儲存，不是網路路由。關鍵字：Hybrid Storage、File Gateway、Volume Gateway、Tape Gateway。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Internet Gateway | 讓 VPC 內的公開資源連上網際網路，也讓網際網路可連入公開資源 | 是 VPC 對外公開上網的入口，常搭配 Public Subnet、公有 IP、路由表 | Public Subnet、公開上網、0.0.0.0/0 |
| 2 | NAT Gateway | 讓 Private Subnet 裡的資源可以主動連出去上網，但外部不能主動連進來 | 解決私有子網路「出得去、進不來」的需求，不是公開入口 | Private Subnet、只出不進、更新套件 |
| 3 | Virtual Private Gateway | Site-to-Site VPN 在 AWS 端的閘道 | 是 VPN 的 AWS 端，不是客戶機房設備 | VGW、AWS 端、VPN |
| 4 | Customer Gateway | Site-to-Site VPN 在客戶機房端的設備或 AWS 中的對應設定 | 是 VPN 的客戶端，通常代表公司機房的路由器或防火牆 | CGW、On-premises、客戶端 |
| 5 | AWS Transit Gateway | 多個 VPC、VPN、Direct Connect 之間的中心轉運站 | 適合連線很多時集中管理，不用每兩個 VPC 都各自 Peering | Hub、集中連接、多 VPC |
| 6 | Amazon API Gateway | 建立、發布和管理 REST API、HTTP API、WebSocket API | 名字有 Gateway，但它是應用層 API 入口，不是 VPC 網路閘道 | API、REST、WebSocket、後端入口 |
| 7 | AWS Storage Gateway | 把公司機房儲存和 AWS 雲端儲存接起來 | 名字有 Gateway，但重點是混合雲儲存，不是網路路由 | Hybrid Storage、File Gateway、Volume Gateway、Tape Gateway |

記憶法：`Internet/NAT/VGW/CGW/Transit` 偏網路連線，`API Gateway` 偏應用程式 API，`Storage Gateway` 偏本地儲存接雲端。

</details>

---

## 2. VPC 連線與私有存取

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：讓兩個 VPC 私下互通。差異提示：點對點連線，VPC 數量多時管理會變複雜。關鍵字：兩個 VPC、私下互連。
2. `___`：集中連接多個 VPC 和本地網路。差異提示：多對多中心化連線，像雲端網路轉運中心。關鍵字：多 VPC、Hub、集中管理。
3. `___`：讓 VPC 私下連到 AWS 服務，不走公開網際網路。差異提示：常用於 S3、DynamoDB 或 PrivateLink 型服務。關鍵字：私下連 AWS 服務。
4. `___`：透過私有連線提供或使用服務。差異提示：常用於私下存取第三方服務、SaaS 或跨帳戶服務。關鍵字：私有服務、第三方服務。
5. `___`：公司機房到 AWS 的專線。差異提示：比 VPN 更穩定，通常成本較高，需要實體線路。關鍵字：專線、穩定、高頻寬。
6. `___`：透過網際網路建立加密通道連到 AWS。差異提示：比 Direct Connect 快速建立，但走公網。關鍵字：加密通道、VPN、公網。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | VPC Peering Connection | 讓兩個 VPC 私下互通 | 點對點連線，VPC 數量多時管理會變複雜 | 兩個 VPC、私下互連 |
| 2 | AWS Transit Gateway | 集中連接多個 VPC 和本地網路 | 多對多中心化連線，像雲端網路轉運中心 | 多 VPC、Hub、集中管理 |
| 3 | VPC Endpoint | 讓 VPC 私下連到 AWS 服務，不走公開網際網路 | 常用於 S3、DynamoDB 或 PrivateLink 型服務 | 私下連 AWS 服務 |
| 4 | AWS PrivateLink | 透過私有連線提供或使用服務 | 常用於私下存取第三方服務、SaaS 或跨帳戶服務 | 私有服務、第三方服務 |
| 5 | AWS Direct Connect | 公司機房到 AWS 的專線 | 比 VPN 更穩定，通常成本較高，需要實體線路 | 專線、穩定、高頻寬 |
| 6 | AWS Site-to-Site VPN | 透過網際網路建立加密通道連到 AWS | 比 Direct Connect 快速建立，但走公網 | 加密通道、VPN、公網 |

</details>

---

## 3. 防火牆與流量控制

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：綁在 EC2、ENI、RDS 等資源上。差異提示：Stateful，只要允許進站，回應流量會自動允許。關鍵字：執行個體層級、Stateful。
2. `___`：套在 Subnet 上。差異提示：Stateless，進站和出站規則都要分別允許。關鍵字：子網路層級、Stateless。
3. `___`：保護 Web 應用程式。差異提示：防 SQL Injection、XSS 等第 7 層 Web 攻擊。關鍵字：Web、防 SQL Injection、XSS。
4. `___`：基本 DDoS 防護。差異提示：免費、自動提供。關鍵字：免費 DDoS。
5. `___`：進階 DDoS 防護。差異提示：付費，提供更完整保護、專家支援和成本保護。關鍵字：付費 DDoS、專家支援。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Security Group | 綁在 EC2、ENI、RDS 等資源上 | Stateful，只要允許進站，回應流量會自動允許 | 執行個體層級、Stateful |
| 2 | Network ACL | 套在 Subnet 上 | Stateless，進站和出站規則都要分別允許 | 子網路層級、Stateless |
| 3 | AWS WAF | 保護 Web 應用程式 | 防 SQL Injection、XSS 等第 7 層 Web 攻擊 | Web、防 SQL Injection、XSS |
| 4 | AWS Shield Standard | 基本 DDoS 防護 | 免費、自動提供 | 免費 DDoS |
| 5 | AWS Shield Advanced | 進階 DDoS 防護 | 付費，提供更完整保護、專家支援和成本保護 | 付費 DDoS、專家支援 |

</details>

---

## 4. Load Balancer 與流量加速

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：AWS 負載平衡的總稱。差異提示：包含 ALB、NLB 等類型。關鍵字：負載平衡總稱。
2. `___`：依 HTTP/HTTPS 內容分流。差異提示：第 7 層，可依 Path、Host、Header 等規則導流。關鍵字：網站、API、HTTP/HTTPS。
3. `___`：依 TCP/UDP 連線分流。差異提示：第 4 層，適合高效能、低延遲、固定 IP 類需求。關鍵字：TCP、UDP、低延遲。
4. `___`：用 AWS 全球網路加速到應用端點。差異提示：提供固定入口 IP，把使用者導到較佳端點，不是 CDN 快取。關鍵字：固定 IP、全球加速。
5. `___`：CDN，把內容快取到 Edge Location。差異提示：靠近使用者快取內容，適合靜態內容、影片、網站加速。關鍵字：CDN、快取、Edge Location。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Elastic Load Balancing | AWS 負載平衡的總稱 | 包含 ALB、NLB 等類型 | 負載平衡總稱 |
| 2 | Application Load Balancer | 依 HTTP/HTTPS 內容分流 | 第 7 層，可依 Path、Host、Header 等規則導流 | 網站、API、HTTP/HTTPS |
| 3 | Network Load Balancer | 依 TCP/UDP 連線分流 | 第 4 層，適合高效能、低延遲、固定 IP 類需求 | TCP、UDP、低延遲 |
| 4 | AWS Global Accelerator | 用 AWS 全球網路加速到應用端點 | 提供固定入口 IP，把使用者導到較佳端點，不是 CDN 快取 | 固定 IP、全球加速 |
| 5 | Amazon CloudFront | CDN，把內容快取到 Edge Location | 靠近使用者快取內容，適合靜態內容、影片、網站加速 | CDN、快取、Edge Location |

</details>

---

## 5. DNS 與 Route 53 路由策略

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：AWS DNS 與路由服務。差異提示：管網域解析、健康檢查、路由策略。關鍵字：DNS、網域。
2. `___`：導到指定目標。差異提示：最單純，沒有流量比例或健康切換邏輯。關鍵字：單一目標。
3. `___`：依比例分配流量。差異提示：可做新版 20%、舊版 80% 這類流量控制。關鍵字：比例、A/B、Canary。
4. `___`：導到延遲最低的區域或端點。差異提示：目標是降低使用者延遲。關鍵字：最低延遲。
5. `___`：主站壞掉時切到備援站。差異提示：需要搭配健康檢查。關鍵字：主備、災備、故障切換。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Amazon Route 53 | AWS DNS 與路由服務 | 管網域解析、健康檢查、路由策略 | DNS、網域 |
| 2 | Simple Routing | 導到指定目標 | 最單純，沒有流量比例或健康切換邏輯 | 單一目標 |
| 3 | Weighted Routing | 依比例分配流量 | 可做新版 20%、舊版 80% 這類流量控制 | 比例、A/B、Canary |
| 4 | Latency-based Routing | 導到延遲最低的區域或端點 | 目標是降低使用者延遲 | 最低延遲 |
| 5 | Failover Routing | 主站壞掉時切到備援站 | 需要搭配健康檢查 | 主備、災備、故障切換 |

</details>

---

## 6. 儲存型態：S3、EBS、EFS、FSx

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：物件儲存。差異提示：適合圖片、影片、備份、日誌等物件檔案，不是掛載成硬碟。關鍵字：Object Storage、Bucket。
2. `___`：區塊儲存。差異提示：像接在 EC2 上的雲端硬碟，通常給單台 EC2 使用。關鍵字：Block Storage、EC2 硬碟。
3. `___`：Linux 共享檔案系統。差異提示：多台 EC2 可同時掛載，使用 NFS。關鍵字：Linux、NFS、共享資料夾。
4. `___`：Windows 受管檔案伺服器。差異提示：適合 Windows 應用與 SMB 檔案共享。關鍵字：Windows、SMB。
5. `___`：高效能檔案系統。差異提示：適合 HPC、機器學習、大量高速檔案處理。關鍵字：高效能、HPC、Lustre。
6. `___`：混合雲儲存。差異提示：讓本地應用用熟悉的檔案、磁碟或磁帶方式接 AWS 儲存。關鍵字：本地機房、混合雲。
7. `___`：資料搬遷與同步。差異提示：用來快速同步本地或雲端之間的資料，不是長期掛載介面。關鍵字：資料同步、搬遷。
8. `___`：EBS 備份。差異提示：用來備份和還原 EBS Volume。關鍵字：快照、備份、還原。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Amazon S3 | 物件儲存 | 適合圖片、影片、備份、日誌等物件檔案，不是掛載成硬碟 | Object Storage、Bucket |
| 2 | Amazon EBS | 區塊儲存 | 像接在 EC2 上的雲端硬碟，通常給單台 EC2 使用 | Block Storage、EC2 硬碟 |
| 3 | Amazon EFS | Linux 共享檔案系統 | 多台 EC2 可同時掛載，使用 NFS | Linux、NFS、共享資料夾 |
| 4 | Amazon FSx for Windows File Server | Windows 受管檔案伺服器 | 適合 Windows 應用與 SMB 檔案共享 | Windows、SMB |
| 5 | Amazon FSx for Lustre | 高效能檔案系統 | 適合 HPC、機器學習、大量高速檔案處理 | 高效能、HPC、Lustre |
| 6 | AWS Storage Gateway | 混合雲儲存 | 讓本地應用用熟悉的檔案、磁碟或磁帶方式接 AWS 儲存 | 本地機房、混合雲 |
| 7 | AWS DataSync | 資料搬遷與同步 | 用來快速同步本地或雲端之間的資料，不是長期掛載介面 | 資料同步、搬遷 |
| 8 | Amazon EBS Snapshots | EBS 備份 | 用來備份和還原 EBS Volume | 快照、備份、還原 |

</details>

---

## 7. S3 儲存類別

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：常常讀取的資料。差異提示：預設通用類別，存取快但成本較高。關鍵字：頻繁存取。
2. `___`：存取模式不確定的資料。差異提示：AWS 會依使用情況自動調整儲存層。關鍵字：自動分層、不確定。
3. `___`：不常讀但需要快速取回。差異提示：跨多 AZ，適合重要但低頻存取資料。關鍵字：不頻繁、快速取回。
4. `___`：可重建、不常讀的資料。差異提示：只存在單一 AZ，較便宜但耐受性較低。關鍵字：單一 AZ、可重建。
5. `___`：封存資料。差異提示：取回可能幾分鐘到幾小時。關鍵字：封存、偶爾取回。
6. `___`：長期深度封存。差異提示：最便宜之一，適合多年保存、極少取回。關鍵字：長期保存、極少取回。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | S3 Standard | 常常讀取的資料 | 預設通用類別，存取快但成本較高 | 頻繁存取 |
| 2 | S3 Intelligent-Tiering | 存取模式不確定的資料 | AWS 會依使用情況自動調整儲存層 | 自動分層、不確定 |
| 3 | S3 Standard-IA | 不常讀但需要快速取回 | 跨多 AZ，適合重要但低頻存取資料 | 不頻繁、快速取回 |
| 4 | S3 One Zone-IA | 可重建、不常讀的資料 | 只存在單一 AZ，較便宜但耐受性較低 | 單一 AZ、可重建 |
| 5 | S3 Glacier Flexible Retrieval | 封存資料 | 取回可能幾分鐘到幾小時 | 封存、偶爾取回 |
| 6 | S3 Glacier Deep Archive | 長期深度封存 | 最便宜之一，適合多年保存、極少取回 | 長期保存、極少取回 |

</details>

---

## 8. S3 功能容易混淆組

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：防止 Bucket 或物件被公開。差異提示：是安全保護設定。關鍵字：防公開。
2. `___`：保留同一物件的多個版本。差異提示：防誤刪、誤覆蓋。關鍵字：版本、誤刪。
3. `___`：自動轉儲存層或刪除。差異提示：管生命週期和成本。關鍵字：到期轉層、刪除。
4. `___`：自動複製物件到同區或跨區。差異提示：強調複製資料。關鍵字：跨區複寫、備援。
5. `___`：加速遠端使用者上傳到 S3。差異提示：透過 CloudFront Edge 加速傳輸。關鍵字：上傳加速、遠距離。
6. `___`：記錄 Bucket 存取請求。差異提示：用於稽核和分析存取。關鍵字：存取日誌。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | S3 Block Public Access | 防止 Bucket 或物件被公開 | 是安全保護設定 | 防公開 |
| 2 | S3 Versioning | 保留同一物件的多個版本 | 防誤刪、誤覆蓋 | 版本、誤刪 |
| 3 | S3 Lifecycle Configuration | 自動轉儲存層或刪除 | 管生命週期和成本 | 到期轉層、刪除 |
| 4 | S3 Replication | 自動複製物件到同區或跨區 | 強調複製資料 | 跨區複寫、備援 |
| 5 | S3 Transfer Acceleration | 加速遠端使用者上傳到 S3 | 透過 CloudFront Edge 加速傳輸 | 上傳加速、遠距離 |
| 6 | S3 Access Logs | 記錄 Bucket 存取請求 | 用於稽核和分析存取 | 存取日誌 |

</details>

---

## 9. EC2 付費與容量選項

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：用多少付多少。差異提示：沒有承諾，適合短期、需求不固定。關鍵字：隨需、無承諾。
2. `___`：承諾 1 或 3 年換折扣。差異提示：適合穩定 EC2 使用量。關鍵字：保留、長期。
3. `___`：折扣較高。差異提示：彈性較低，適合固定需求。關鍵字：固定、最高折扣。
4. `___`：可轉換機型等屬性。差異提示：折扣通常較 Standard RI 低，但比較彈性。關鍵字：可轉換。
5. `___`：使用 AWS 閒置容量。差異提示：很便宜但可能被中斷。關鍵字：最便宜、可中斷。
6. `___`：整台實體主機給你用。差異提示：常用於自帶授權、合規需求。關鍵字：實體主機、BYOL。
7. `___`：跑在專用硬體上。差異提示：不指定固定哪一台實體主機。關鍵字：專用硬體。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | On-Demand Instance | 用多少付多少 | 沒有承諾，適合短期、需求不固定 | 隨需、無承諾 |
| 2 | Reserved Instance | 承諾 1 或 3 年換折扣 | 適合穩定 EC2 使用量 | 保留、長期 |
| 3 | Standard RI | 折扣較高 | 彈性較低，適合固定需求 | 固定、最高折扣 |
| 4 | Convertible RI | 可轉換機型等屬性 | 折扣通常較 Standard RI 低，但比較彈性 | 可轉換 |
| 5 | Spot Instance | 使用 AWS 閒置容量 | 很便宜但可能被中斷 | 最便宜、可中斷 |
| 6 | Dedicated Host | 整台實體主機給你用 | 常用於自帶授權、合規需求 | 實體主機、BYOL |
| 7 | Dedicated Instance | 跑在專用硬體上 | 不指定固定哪一台實體主機 | 專用硬體 |

</details>

---

## 10. Savings Plans 與 RI

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：承諾每小時花費金額。差異提示：不是保留特定執行個體，而是用量折扣模型。關鍵字：每小時用量承諾。
2. `___`：EC2、Fargate、Lambda 等運算用量。差異提示：彈性最高，可跨多種運算服務。關鍵字：最彈性、運算服務。
3. `___`：指定 EC2 執行個體家族與區域。差異提示：折扣較高但彈性較低。關鍵字：EC2 家族、區域。
4. `___`：承諾特定 EC2 使用方式。差異提示：偏 EC2 執行個體購買選項。關鍵字：RI、EC2 折扣。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Savings Plans | 承諾每小時花費金額 | 不是保留特定執行個體，而是用量折扣模型 | 每小時用量承諾 |
| 2 | Compute Savings Plans | EC2、Fargate、Lambda 等運算用量 | 彈性最高，可跨多種運算服務 | 最彈性、運算服務 |
| 3 | EC2 Instance Savings Plans | 指定 EC2 執行個體家族與區域 | 折扣較高但彈性較低 | EC2 家族、區域 |
| 4 | Reserved Instance | 承諾特定 EC2 使用方式 | 偏 EC2 執行個體購買選項 | RI、EC2 折扣 |

</details>

---

## 11. 成本工具

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：建立資源前估算費用。差異提示：事前估價。關鍵字：還沒建立、估算。
2. `___`：看歷史花費和預測。差異提示：互動式圖表分析成本。關鍵字：看花費、預測。
3. `___`：設預算與警示。差異提示：快超支時通知。關鍵字：預算、通知。
4. `___`：最詳細成本與用量報告。差異提示：通常輸出到 S3，適合細部分析。關鍵字：CUR、詳細報告。
5. `___`：用標籤分攤成本。差異提示：分部門、專案、環境看花費。關鍵字：標籤、分攤。
6. `___`：分析資源規格是否合適。差異提示：建議調大、調小、換規格。關鍵字：Rightsizing、最佳化。
7. `___`：合併多帳戶帳單。差異提示：AWS Organizations 的集中帳單能力。關鍵字：多帳戶、合併帳單。
8. `___`：AWS 抵用金。差異提示：折抵符合條件費用，不是成本分析工具。關鍵字：抵用金。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | AWS Pricing Calculator | 建立資源前估算費用 | 事前估價 | 還沒建立、估算 |
| 2 | AWS Cost Explorer | 看歷史花費和預測 | 互動式圖表分析成本 | 看花費、預測 |
| 3 | AWS Budgets | 設預算與警示 | 快超支時通知 | 預算、通知 |
| 4 | Cost and Usage Report | 最詳細成本與用量報告 | 通常輸出到 S3，適合細部分析 | CUR、詳細報告 |
| 5 | Cost Allocation Tags | 用標籤分攤成本 | 分部門、專案、環境看花費 | 標籤、分攤 |
| 6 | AWS Compute Optimizer | 分析資源規格是否合適 | 建議調大、調小、換規格 | Rightsizing、最佳化 |
| 7 | Consolidated Billing | 合併多帳戶帳單 | AWS Organizations 的集中帳單能力 | 多帳戶、合併帳單 |
| 8 | AWS Credits | AWS 抵用金 | 折抵符合條件費用，不是成本分析工具 | 抵用金 |

</details>

---

## 12. 運算服務

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：虛擬伺服器。差異提示：控制最多，也要自己管理作業系統和軟體。關鍵字：VM、伺服器。
2. `___`：只上傳程式碼，事件觸發執行。差異提示：不管理伺服器，適合短時間函數。關鍵字：Serverless、Function。
3. `___`：部署應用程式的平台。差異提示：AWS 幫你處理部署、擴展、負載平衡，但底層仍可見。關鍵字：PaaS、部署 Web App。
4. `___`：無伺服器容器運算引擎。差異提示：跑容器但不用管 EC2。關鍵字：Serverless Container。
5. `___`：容器管理服務。差異提示：管 Docker 容器叢集與任務。關鍵字：Container Orchestration。
6. `___`：容器映像檔倉庫。差異提示：存 Docker Image，不負責執行容器。關鍵字：Image Registry。
7. `___`：簡化版雲端主機。差異提示：適合小網站、WordPress、簡單資料庫。關鍵字：新手、小網站。
8. `___`：批次運算。差異提示：適合大量工作排程與批次處理。關鍵字：Batch、批次工作。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Amazon EC2 | 虛擬伺服器 | 控制最多，也要自己管理作業系統和軟體 | VM、伺服器 |
| 2 | AWS Lambda | 只上傳程式碼，事件觸發執行 | 不管理伺服器，適合短時間函數 | Serverless、Function |
| 3 | AWS Elastic Beanstalk | 部署應用程式的平台 | AWS 幫你處理部署、擴展、負載平衡，但底層仍可見 | PaaS、部署 Web App |
| 4 | AWS Fargate | 無伺服器容器運算引擎 | 跑容器但不用管 EC2 | Serverless Container |
| 5 | Amazon ECS | 容器管理服務 | 管 Docker 容器叢集與任務 | Container Orchestration |
| 6 | Amazon ECR | 容器映像檔倉庫 | 存 Docker Image，不負責執行容器 | Image Registry |
| 7 | Amazon Lightsail | 簡化版雲端主機 | 適合小網站、WordPress、簡單資料庫 | 新手、小網站 |
| 8 | AWS Batch | 批次運算 | 適合大量工作排程與批次處理 | Batch、批次工作 |

</details>

---

## 13. EC2 相關名詞

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：自動建立和更新映像檔。差異提示：是製作 AMI 或容器映像的服務。關鍵字：建置映像。
2. `___`：EC2 開機範本。差異提示：包含 OS、套件、設定，用來啟動 EC2。關鍵字：AMI、開機模板。
3. `___`：EC2 第一次啟動時執行的腳本。差異提示：用來做初始化安裝和設定。關鍵字：開機腳本。
4. `___`：EC2 自己的資訊。差異提示：可查執行個體 ID、IP、角色憑證等。關鍵字：Metadata。
5. `___`：安全連線到 EC2。差異提示：不用自己長期管理 SSH 公鑰。關鍵字：SSH、瀏覽器連線。
6. `___`：EC2 主機本機暫存磁碟。差異提示：快但不持久，EC2 停止或終止後資料可能消失。關鍵字：暫存、本機磁碟。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Amazon EC2 Image Builder | 自動建立和更新映像檔 | 是製作 AMI 或容器映像的服務 | 建置映像 |
| 2 | Amazon Machine Image | EC2 開機範本 | 包含 OS、套件、設定，用來啟動 EC2 | AMI、開機模板 |
| 3 | EC2 User Data | EC2 第一次啟動時執行的腳本 | 用來做初始化安裝和設定 | 開機腳本 |
| 4 | EC2 Instance Metadata | EC2 自己的資訊 | 可查執行個體 ID、IP、角色憑證等 | Metadata |
| 5 | EC2 Instance Connect | 安全連線到 EC2 | 不用自己長期管理 SSH 公鑰 | SSH、瀏覽器連線 |
| 6 | EC2 Instance Store | EC2 主機本機暫存磁碟 | 快但不持久，EC2 停止或終止後資料可能消失 | 暫存、本機磁碟 |

</details>

---

## 14. 自動擴展

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：自動調整多種 AWS 資源。差異提示：是自動擴展的總概念或服務。關鍵字：自動增減資源。
2. `___`：管一群 EC2 的數量。差異提示：設定最小、最大、期望台數。關鍵字：EC2 群組、Min/Max/Desired。
3. `___`：依歷史模式預先擴展。差異提示：提前加資源，不是等指標超標才反應。關鍵字：預測、提前。
4. `___`：隨需求增減資源的能力。差異提示：是雲端概念，不是單一服務。關鍵字：流量高加、流量低減。
5. `___`：系統可隨需求變大。差異提示：可以是水平或垂直擴展。關鍵字：可擴展。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | AWS Auto Scaling | 自動調整多種 AWS 資源 | 是自動擴展的總概念或服務 | 自動增減資源 |
| 2 | Auto Scaling Group | 管一群 EC2 的數量 | 設定最小、最大、期望台數 | EC2 群組、Min/Max/Desired |
| 3 | Predictive Scaling | 依歷史模式預先擴展 | 提前加資源，不是等指標超標才反應 | 預測、提前 |
| 4 | Elasticity | 隨需求增減資源的能力 | 是雲端概念，不是單一服務 | 流量高加、流量低減 |
| 5 | Scalability | 系統可隨需求變大 | 可以是水平或垂直擴展 | 可擴展 |

</details>

---

## 15. EC2 執行個體類型

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：大型資料庫、快取。差異提示：記憶體需求高。關鍵字：RAM、記憶體。
2. `___`：高 CPU 運算、批次處理。差異提示：CPU 需求高。關鍵字：CPU、計算。
3. `___`：大量本機磁碟讀寫。差異提示：本機儲存 I/O 高。關鍵字：IOPS、資料倉儲。
4. `___`：ML、GPU、3D、影像處理。差異提示：使用 GPU、FPGA 等加速器。關鍵字：GPU、ML、渲染。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Memory Optimized | 大型資料庫、快取 | 記憶體需求高 | RAM、記憶體 |
| 2 | Compute Optimized | 高 CPU 運算、批次處理 | CPU 需求高 | CPU、計算 |
| 3 | Storage Optimized | 大量本機磁碟讀寫 | 本機儲存 I/O 高 | IOPS、資料倉儲 |
| 4 | Accelerated Computing | ML、GPU、3D、影像處理 | 使用 GPU、FPGA 等加速器 | GPU、ML、渲染 |

</details>

---

## 16. 資料庫服務

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：關聯式資料庫。差異提示：AWS 代管 MySQL、PostgreSQL、SQL Server 等。關鍵字：SQL、關聯式。
2. `___`：AWS 自家關聯式資料庫。差異提示：相容 MySQL/PostgreSQL，效能與雲端整合較強。關鍵字：Aurora、MySQL、PostgreSQL。
3. `___`：NoSQL 鍵值或文件資料庫。差異提示：高擴展、低延遲，不是 SQL 關聯式。關鍵字：NoSQL、Key-Value。
4. `___`：記憶體快取。差異提示：Redis 或 Memcached，降低資料庫讀取壓力。關鍵字：Cache、Redis。
5. `___`：圖形資料庫。差異提示：處理節點和關係。關鍵字：Graph、關係網。
6. `___`：文件資料庫。差異提示：相容 MongoDB 工作負載。關鍵字：Document、MongoDB。
7. `___`：資料倉儲。差異提示：做大量分析和商業報表，不是交易型資料庫。關鍵字：Data Warehouse、BI。
8. `___`：資料庫遷移。差異提示：搬資料庫到 AWS 或不同資料庫間遷移。關鍵字：Migration、遷移。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Amazon RDS | 關聯式資料庫 | AWS 代管 MySQL、PostgreSQL、SQL Server 等 | SQL、關聯式 |
| 2 | Amazon Aurora | AWS 自家關聯式資料庫 | 相容 MySQL/PostgreSQL，效能與雲端整合較強 | Aurora、MySQL、PostgreSQL |
| 3 | Amazon DynamoDB | NoSQL 鍵值或文件資料庫 | 高擴展、低延遲，不是 SQL 關聯式 | NoSQL、Key-Value |
| 4 | Amazon ElastiCache | 記憶體快取 | Redis 或 Memcached，降低資料庫讀取壓力 | Cache、Redis |
| 5 | Amazon Neptune | 圖形資料庫 | 處理節點和關係 | Graph、關係網 |
| 6 | Amazon DocumentDB | 文件資料庫 | 相容 MongoDB 工作負載 | Document、MongoDB |
| 7 | Amazon Redshift | 資料倉儲 | 做大量分析和商業報表，不是交易型資料庫 | Data Warehouse、BI |
| 8 | AWS DMS | 資料庫遷移 | 搬資料庫到 AWS 或不同資料庫間遷移 | Migration、遷移 |

</details>

---

## 17. RDS 與 DynamoDB 延伸功能

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：高可用與故障切換。差異提示：備援用，主庫壞掉自動切換，不是用來分擔讀取。關鍵字：HA、Failover。
2. `___`：分擔讀取壓力。差異提示：讀取擴展用，可讓查詢流量去副本。關鍵字：Read Scaling。
3. `___`：跨區域多主資料表。差異提示：多 Region 都能讀寫。關鍵字：全球、多區域。
4. `___`：DynamoDB 快取加速器。差異提示：用記憶體快取降低 DynamoDB 讀取延遲。關鍵字：DAX、快取。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | RDS Multi-AZ | 高可用與故障切換 | 備援用，主庫壞掉自動切換，不是用來分擔讀取 | HA、Failover |
| 2 | RDS Read Replica | 分擔讀取壓力 | 讀取擴展用，可讓查詢流量去副本 | Read Scaling |
| 3 | DynamoDB Global Tables | 跨區域多主資料表 | 多 Region 都能讀寫 | 全球、多區域 |
| 4 | DynamoDB Accelerator | DynamoDB 快取加速器 | 用記憶體快取降低 DynamoDB 讀取延遲 | DAX、快取 |

</details>

---

## 18. 身分、權限與登入

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：管理 AWS 身分與權限。差異提示：AWS 帳戶內的權限核心服務。關鍵字：權限、身份。
2. `___`：長期身分。差異提示：代表一個人或程式，可有長期憑證。關鍵字：使用者、長期。
3. `___`：可被暫時扮演的身分。差異提示：常給 EC2、Lambda 或跨帳戶使用，使用臨時憑證。關鍵字：Role、臨時。
4. `___`：權限規則文件。差異提示：定義 Allow 或 Deny 哪些動作。關鍵字：JSON、權限規則。
5. `___`：程式呼叫 AWS API 的長期金鑰。差異提示：不等於登入密碼，應避免長期暴露。關鍵字：CLI、SDK、API Key。
6. `___`：發臨時安全憑證。差異提示：Role 背後常用 STS 產生短期憑證。關鍵字：Temporary Credential。
7. `___`：多帳戶單一登入。差異提示：給員工集中登入多個 AWS 帳戶。關鍵字：SSO、多帳戶。
8. `___`：App 或網站使用者登入。差異提示：給你的應用程式使用者，不是管理 AWS 員工權限。關鍵字：App Login、使用者池。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | AWS IAM | 管理 AWS 身分與權限 | AWS 帳戶內的權限核心服務 | 權限、身份 |
| 2 | IAM User | 長期身分 | 代表一個人或程式，可有長期憑證 | 使用者、長期 |
| 3 | IAM Role | 可被暫時扮演的身分 | 常給 EC2、Lambda 或跨帳戶使用，使用臨時憑證 | Role、臨時 |
| 4 | IAM Policy | 權限規則文件 | 定義 Allow 或 Deny 哪些動作 | JSON、權限規則 |
| 5 | Access Key ID & Secret Access Key | 程式呼叫 AWS API 的長期金鑰 | 不等於登入密碼，應避免長期暴露 | CLI、SDK、API Key |
| 6 | AWS STS | 發臨時安全憑證 | Role 背後常用 STS 產生短期憑證 | Temporary Credential |
| 7 | IAM Identity Center | 多帳戶單一登入 | 給員工集中登入多個 AWS 帳戶 | SSO、多帳戶 |
| 8 | Amazon Cognito | App 或網站使用者登入 | 給你的應用程式使用者，不是管理 AWS 員工權限 | App Login、使用者池 |

</details>

---

## 19. MFA 類型

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：多重要素驗證總稱。差異提示：密碼之外再加一層驗證。關鍵字：第二因素。
2. `___`：手機 App 產生驗證碼。差異提示：軟體式 MFA，例如驗證器 App。關鍵字：Authenticator App。
3. `___`：USB 或裝置上的實體安全金鑰。差異提示：實體插入或感應確認。關鍵字：Security Key。
4. `___`：實體裝置產生一次性驗證碼。差異提示：硬體 Token，不一定是 U2F。關鍵字：Token、一次性密碼。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | MFA | 多重要素驗證總稱 | 密碼之外再加一層驗證 | 第二因素 |
| 2 | Virtual MFA Device | 手機 App 產生驗證碼 | 軟體式 MFA，例如驗證器 App | Authenticator App |
| 3 | U2F Security Key | USB 或裝置上的實體安全金鑰 | 實體插入或感應確認 | Security Key |
| 4 | Hardware MFA Device | 實體裝置產生一次性驗證碼 | 硬體 Token，不一定是 U2F | Token、一次性密碼 |

</details>

---

## 20. 加密與機密管理

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：管理加密金鑰。差異提示：常用於加密 S3、EBS、RDS 等資料。關鍵字：Key Management。
2. `___`：由客戶建立和管理的 KMS Key。差異提示：控制權較高，可自訂政策、輪換等。關鍵字：CMK、客戶管理。
3. `___`：AWS 幫你建立和管理的 KMS Key。差異提示：操作最簡單，控制較少。關鍵字：AWS 管理。
4. `___`：雲端硬體安全模組。差異提示：適合法規或合規要求高、需要專用 HSM。關鍵字：HSM、合規。
5. `___`：保存密碼、API Key、資料庫密碼。差異提示：可自動輪換機密，不是加密金鑰管理主服務。關鍵字：Secret、密碼、自動輪換。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | AWS KMS | 管理加密金鑰 | 常用於加密 S3、EBS、RDS 等資料 | Key Management |
| 2 | Customer Managed Key | 由客戶建立和管理的 KMS Key | 控制權較高，可自訂政策、輪換等 | CMK、客戶管理 |
| 3 | AWS Managed Key | AWS 幫你建立和管理的 KMS Key | 操作最簡單，控制較少 | AWS 管理 |
| 4 | AWS CloudHSM | 雲端硬體安全模組 | 適合法規或合規要求高、需要專用 HSM | HSM、合規 |
| 5 | AWS Secrets Manager | 保存密碼、API Key、資料庫密碼 | 可自動輪換機密，不是加密金鑰管理主服務 | Secret、密碼、自動輪換 |

</details>

---

## 21. 安全偵測與調查

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：偵測可疑或惡意活動。差異提示：分析帳戶、網路與日誌找威脅。關鍵字：威脅偵測。
2. `___`：掃描工作負載弱點。差異提示：檢查 EC2、容器等是否有漏洞。關鍵字：Vulnerability。
3. `___`：找出 S3 敏感資料。差異提示：掃個資、信用卡號等敏感資料。關鍵字：S3、敏感資料。
4. `___`：調查安全事件。差異提示：幫你看事件關聯與原因。關鍵字：Investigation。
5. `___`：集中整理安全警報與狀態。差異提示：彙整多個安全服務，不是單一偵測器。關鍵字：Central Security。
6. `___`：記錄 VPC 網路流量。差異提示：用於網路除錯與安全分析。關鍵字：IP 流量紀錄。
7. `___`：處理 AWS 資源濫用通報。差異提示：是 AWS 團隊，不是客戶設定的安全服務。關鍵字：濫用、通報。
8. `___`：下載合規報告和文件。差異提示：合規文件入口，不是掃描工具。關鍵字：合規報告。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Amazon GuardDuty | 偵測可疑或惡意活動 | 分析帳戶、網路與日誌找威脅 | 威脅偵測 |
| 2 | Amazon Inspector | 掃描工作負載弱點 | 檢查 EC2、容器等是否有漏洞 | Vulnerability |
| 3 | Amazon Macie | 找出 S3 敏感資料 | 掃個資、信用卡號等敏感資料 | S3、敏感資料 |
| 4 | Amazon Detective | 調查安全事件 | 幫你看事件關聯與原因 | Investigation |
| 5 | AWS Security Hub | 集中整理安全警報與狀態 | 彙整多個安全服務，不是單一偵測器 | Central Security |
| 6 | VPC Flow Logs | 記錄 VPC 網路流量 | 用於網路除錯與安全分析 | IP 流量紀錄 |
| 7 | AWS Abuse Team | 處理 AWS 資源濫用通報 | 是 AWS 團隊，不是客戶設定的安全服務 | 濫用、通報 |
| 8 | AWS Artifact | 下載合規報告和文件 | 合規文件入口，不是掃描工具 | 合規報告 |

</details>

---

## 22. 監控、稽核與設定管理

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：監控指標、日誌、警報。差異提示：看系統現在或歷史狀態。關鍵字：Metrics、Logs、Alarm。
2. `___`：記錄 AWS API 操作。差異提示：查誰在帳戶裡做了什麼。關鍵字：API Audit。
3. `___`：偵測異常 API 活動。差異提示：是 CloudTrail 的異常偵測功能。關鍵字：API 異常。
4. `___`：記錄資源設定變更與合規。差異提示：看資源設定是否符合規範。關鍵字：Configuration、Compliance。
5. `___`：追蹤請求流程。差異提示：找微服務或 Lambda 哪裡慢、哪裡錯。關鍵字：Trace、分散式追蹤。
6. `___`：給成本、安全、效能等建議。差異提示：偏帳戶與資源最佳化建議。關鍵字：Best Practice 建議。
7. `___`：用問卷檢查架構。差異提示：偏架構設計審查，不是即時監控。關鍵字：架構評估。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Amazon CloudWatch | 監控指標、日誌、警報 | 看系統現在或歷史狀態 | Metrics、Logs、Alarm |
| 2 | AWS CloudTrail | 記錄 AWS API 操作 | 查誰在帳戶裡做了什麼 | API Audit |
| 3 | CloudTrail Insights | 偵測異常 API 活動 | 是 CloudTrail 的異常偵測功能 | API 異常 |
| 4 | AWS Config | 記錄資源設定變更與合規 | 看資源設定是否符合規範 | Configuration、Compliance |
| 5 | AWS X-Ray | 追蹤請求流程 | 找微服務或 Lambda 哪裡慢、哪裡錯 | Trace、分散式追蹤 |
| 6 | AWS Trusted Advisor | 給成本、安全、效能等建議 | 偏帳戶與資源最佳化建議 | Best Practice 建議 |
| 7 | AWS Well-Architected Tool | 用問卷檢查架構 | 偏架構設計審查，不是即時監控 | 架構評估 |

</details>

---

## 23. Systems Manager 相關

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：集中管理 EC2 或本地伺服器。差異提示：可做派送命令、修補、盤點等。關鍵字：SSM、管理伺服器。
2. `___`：安全連進 EC2。差異提示：不用開 SSH 連接埠，也能從瀏覽器或 CLI 連線。關鍵字：不開 SSH、遠端連線。
3. `___`：連線到 EC2 的另一種方式。差異提示：偏 SSH 金鑰臨時推送，和 SSM Session Manager 不同。關鍵字：SSH、臨時公鑰。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | AWS Systems Manager | 集中管理 EC2 或本地伺服器 | 可做派送命令、修補、盤點等 | SSM、管理伺服器 |
| 2 | AWS Systems Manager Session Manager | 安全連進 EC2 | 不用開 SSH 連接埠，也能從瀏覽器或 CLI 連線；它是 Systems Manager 裡的一項功能 | 不開 SSH、遠端連線 |
| 3 | EC2 Instance Connect | 連線到 EC2 的另一種方式 | 偏 SSH 金鑰臨時推送，和 SSM Session Manager 不同 | SSH、臨時公鑰 |

</details>

---

## 24. IaC 工具

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：用 JSON 或 YAML 描述基礎設施。差異提示：宣告式 IaC，直接寫模板。關鍵字：Template、YAML、JSON。
2. `___`：用程式語言寫基礎設施。差異提示：最後會產生 CloudFormation。關鍵字：Python、TypeScript、程式碼。
3. `___`：用程式碼管理資源的概念。差異提示：是方法論，不是單一服務。關鍵字：IaC、自動化。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | AWS CloudFormation | 用 JSON 或 YAML 描述基礎設施 | 宣告式 IaC，直接寫模板 | Template、YAML、JSON |
| 2 | AWS CDK | 用程式語言寫基礎設施 | 最後會產生 CloudFormation | Python、TypeScript、程式碼 |
| 3 | Infrastructure as Code | 用程式碼管理資源的概念 | 是方法論，不是單一服務 | IaC、自動化 |

</details>

---

## 25. 開發者工具

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：Git 程式碼倉庫。差異提示：放原始碼。關鍵字：Git、Repo。
2. `___`：編譯、測試、產生建置結果。差異提示：建置階段。關鍵字：Build、Test。
3. `___`：自動部署到 EC2 或本地伺服器。差異提示：部署階段。關鍵字：Deploy。
4. `___`：串起原始碼、建置、測試、部署流程。差異提示：CI/CD 流水線。關鍵字：Pipeline、CI/CD。
5. `___`：套件管理服務。差異提示：放 npm、Maven、Gradle 等套件。關鍵字：Package。
6. `___`：AI 程式碼審查與效能建議。差異提示：找程式碼問題，不是 CI/CD 工具本身。關鍵字：Code Review。
7. `___`：命令列操作 AWS。差異提示：人或腳本下指令。關鍵字：Command Line。
8. `___`：程式呼叫 AWS 服務。差異提示：給應用程式用。關鍵字：程式語言、API。
9. `___`：瀏覽器圖形介面。差異提示：用網頁點選操作。關鍵字：Web Console。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | AWS CodeCommit | Git 程式碼倉庫 | 放原始碼 | Git、Repo |
| 2 | AWS CodeBuild | 編譯、測試、產生建置結果 | 建置階段 | Build、Test |
| 3 | AWS CodeDeploy | 自動部署到 EC2 或本地伺服器 | 部署階段 | Deploy |
| 4 | AWS CodePipeline | 串起原始碼、建置、測試、部署流程 | CI/CD 流水線 | Pipeline、CI/CD |
| 5 | AWS CodeArtifact | 套件管理服務 | 放 npm、Maven、Gradle 等套件 | Package |
| 6 | Amazon CodeGuru | AI 程式碼審查與效能建議 | 找程式碼問題，不是 CI/CD 工具本身 | Code Review |
| 7 | AWS CLI | 命令列操作 AWS | 人或腳本下指令 | Command Line |
| 8 | AWS SDK | 程式呼叫 AWS 服務 | 給應用程式用 | 程式語言、API |
| 9 | AWS Management Console | 瀏覽器圖形介面 | 用網頁點選操作 | Web Console |

</details>

---

## 26. 分析服務

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：即時串流資料。差異提示：收集和處理即時資料流。關鍵字：Streaming。
2. `___`：大數據叢集。差異提示：跑 Hadoop、Spark 等框架。關鍵字：Hadoop、Spark。
3. `___`：直接用 SQL 查 S3。差異提示：不用先架資料庫或載入資料倉儲。關鍵字：SQL on S3。
4. `___`：BI 視覺化報表。差異提示：做儀表板和分析圖表。關鍵字：BI、Dashboard。
5. `___`：ETL 資料整合。差異提示：擷取、轉換、載入資料。關鍵字：ETL。
6. `___`：資料倉儲。差異提示：大量結構化資料分析。關鍵字：Data Warehouse。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Kinesis Data Streams | 即時串流資料 | 收集和處理即時資料流 | Streaming |
| 2 | Amazon EMR | 大數據叢集 | 跑 Hadoop、Spark 等框架 | Hadoop、Spark |
| 3 | Amazon Athena | 直接用 SQL 查 S3 | 不用先架資料庫或載入資料倉儲 | SQL on S3 |
| 4 | Amazon QuickSight | BI 視覺化報表 | 做儀表板和分析圖表 | BI、Dashboard |
| 5 | AWS Glue | ETL 資料整合 | 擷取、轉換、載入資料 | ETL |
| 6 | Amazon Redshift | 資料倉儲 | 大量結構化資料分析 | Data Warehouse |

</details>

---

## 27. AI/ML 服務

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：建立、訓練、部署 ML 模型。差異提示：給資料科學家做完整 ML 流程。關鍵字：ML 平台。
2. `___`：時間序列預測。差異提示：預測銷售量、需求、流量。關鍵字：Forecast、時間序列。
3. `___`：圖片與影片辨識。差異提示：辨識人臉、物件、文字等。關鍵字：Image、Video。
4. `___`：語音轉文字。差異提示：Speech to Text。關鍵字：STT。
5. `___`：文字轉語音。差異提示：Text to Speech。關鍵字：TTS。
6. `___`：文字翻譯。差異提示：翻成其他語言。關鍵字：Translation。
7. `___`：自然語言理解。差異提示：情緒、關鍵字、實體辨識。關鍵字：NLP。
8. `___`：聊天機器人或語音對話。差異提示：建立對話介面。關鍵字：Chatbot。
9. `___`：企業搜尋。差異提示：從文件找答案。關鍵字：Enterprise Search。
10. `___`：個人化推薦。差異提示：依使用者行為推薦內容。關鍵字：Recommendation。
11. `___`：媒體轉碼。差異提示：把影音轉成不同格式。關鍵字：Media Transcode。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Amazon SageMaker | 建立、訓練、部署 ML 模型 | 給資料科學家做完整 ML 流程 | ML 平台 |
| 2 | Amazon Forecast | 時間序列預測 | 預測銷售量、需求、流量 | Forecast、時間序列 |
| 3 | Amazon Rekognition | 圖片與影片辨識 | 辨識人臉、物件、文字等 | Image、Video |
| 4 | Amazon Transcribe | 語音轉文字 | Speech to Text | STT |
| 5 | Amazon Polly | 文字轉語音 | Text to Speech | TTS |
| 6 | Amazon Translate | 文字翻譯 | 翻成其他語言 | Translation |
| 7 | Amazon Comprehend | 自然語言理解 | 情緒、關鍵字、實體辨識 | NLP |
| 8 | Amazon Lex | 聊天機器人或語音對話 | 建立對話介面 | Chatbot |
| 9 | Amazon Kendra | 企業搜尋 | 從文件找答案 | Enterprise Search |
| 10 | Amazon Personalize | 個人化推薦 | 依使用者行為推薦內容 | Recommendation |
| 11 | Amazon Elastic Transcoder | 媒體轉碼 | 把影音轉成不同格式 | Media Transcode |

</details>

---

## 28. 應用程式整合

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：訊息佇列。差異提示：系統 A 放工作，系統 B 慢慢處理。關鍵字：Queue、解耦。
2. `___`：發布通知給多個訂閱者。差異提示：一對多推播，可推 Email、SQS、Lambda。關鍵字：Pub/Sub、通知。
3. `___`：受管訊息代理。差異提示：相容 ActiveMQ、RabbitMQ。關鍵字：Message Broker。
4. `___`：事件匯流排。差異提示：根據事件或排程觸發動作。關鍵字：Event Bus。
5. `___`：工作流程協調。差異提示：把 Lambda 或 AWS 服務串成流程。關鍵字：Workflow、狀態機。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Amazon SQS | 訊息佇列 | 系統 A 放工作，系統 B 慢慢處理 | Queue、解耦 |
| 2 | Amazon SNS | 發布通知給多個訂閱者 | 一對多推播，可推 Email、SQS、Lambda | Pub/Sub、通知 |
| 3 | Amazon MQ | 受管訊息代理 | 相容 ActiveMQ、RabbitMQ | Message Broker |
| 4 | Amazon EventBridge | 事件匯流排 | 根據事件或排程觸發動作 | Event Bus |
| 5 | AWS Step Functions | 工作流程協調 | 把 Lambda 或 AWS 服務串成流程 | Workflow、狀態機 |

</details>

---

## 29. 架構框架與支柱

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：AWS 架構最佳實務框架。差異提示：用六大支柱檢查架構。關鍵字：六大支柱。
2. `___`：卓越營運。差異提示：自動化、可回復小變更、營運流程。關鍵字：運維、自動化。
3. `___`：安全性。差異提示：權限、加密、偵測、資料保護。關鍵字：安全。
4. `___`：可靠性。差異提示：故障恢復、容錯、水平擴展。關鍵字：容錯、恢復。
5. `___`：效能效率。差異提示：選對資源類型與大小。關鍵字：效能。
6. `___`：成本優化。差異提示：正確定價模式、刪除閒置資源。關鍵字：成本。
7. `___`：雲端採用框架。差異提示：協助組織規劃雲端採用，不是檢查單一架構。關鍵字：採用雲端、組織。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | AWS Well-Architected Framework | AWS 架構最佳實務框架 | 用六大支柱檢查架構 | 六大支柱 |
| 2 | Operational Excellence Pillar | 卓越營運 | 自動化、可回復小變更、營運流程 | 運維、自動化 |
| 3 | Security Pillar | 安全性 | 權限、加密、偵測、資料保護 | 安全 |
| 4 | Reliability Pillar | 可靠性 | 故障恢復、容錯、水平擴展 | 容錯、恢復 |
| 5 | Performance Efficiency Pillar | 效能效率 | 選對資源類型與大小 | 效能 |
| 6 | Cost Optimization Pillar | 成本優化 | 正確定價模式、刪除閒置資源 | 成本 |
| 7 | AWS CAF | 雲端採用框架 | 協助組織規劃雲端採用，不是檢查單一架構 | 採用雲端、組織 |

</details>

---

## 30. 多帳戶與治理

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：集中管理多個 AWS 帳戶。差異提示：帳戶、帳單、組織政策管理。關鍵字：多帳戶。
2. `___`：合併帳單。差異提示：Organizations 的帳單整合能力。關鍵字：合併計費。
3. `___`：限制帳戶最大權限。差異提示：SCP 不直接授權，只設上限。關鍵字：權限上限。
4. `___`：快速建立多帳戶環境。差異提示：建 landing zone 和治理護欄。關鍵字：Landing Zone、護欄。
5. `___`：核准的 IT 服務目錄。差異提示：讓使用者照規範部署已核准資源。關鍵字：核准清單。
6. `___`：資源標籤。差異提示：用於分類、搜尋、成本分攤。關鍵字：Key-Value。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | AWS Organizations | 集中管理多個 AWS 帳戶 | 帳戶、帳單、組織政策管理 | 多帳戶 |
| 2 | Consolidated Billing | 合併帳單 | Organizations 的帳單整合能力 | 合併計費 |
| 3 | Service Control Policies | 限制帳戶最大權限 | SCP 不直接授權，只設上限 | 權限上限 |
| 4 | AWS Control Tower | 快速建立多帳戶環境 | 建 landing zone 和治理護欄 | Landing Zone、護欄 |
| 5 | AWS Service Catalog | 核准的 IT 服務目錄 | 讓使用者照規範部署已核准資源 | 核准清單 |
| 6 | Tags | 資源標籤 | 用於分類、搜尋、成本分攤 | Key-Value |

</details>

---

## 31. 遷移策略

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：遷移策略總稱。差異提示：常見 6R：Rehost、Replatform、Refactor 等。關鍵字：6R。
2. `___`：幾乎不改直接搬。差異提示：又叫 Lift and Shift。關鍵字：原樣搬。
3. `___`：稍微調整平台。差異提示：例如自管資料庫改用 RDS。關鍵字：小幅改造。
4. `___`：遷移資料庫。差異提示：是資料庫遷移工具，不是整體策略。關鍵字：DB Migration。
5. `___`：搬遷或同步檔案資料。差異提示：偏檔案與儲存資料同步。關鍵字：File Sync。
6. `___`：用實體設備搬大量資料。差異提示：適合網路傳太慢或資料量極大。關鍵字：離線搬遷。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | AWS Migration Strategies | 遷移策略總稱 | 常見 6R：Rehost、Replatform、Refactor 等 | 6R |
| 2 | Rehost | 幾乎不改直接搬 | 又叫 Lift and Shift | 原樣搬 |
| 3 | Replatform | 稍微調整平台 | 例如自管資料庫改用 RDS | 小幅改造 |
| 4 | AWS DMS | 遷移資料庫 | 是資料庫遷移工具，不是整體策略 | DB Migration |
| 5 | AWS DataSync | 搬遷或同步檔案資料 | 偏檔案與儲存資料同步 | File Sync |
| 6 | AWS Snowball | 用實體設備搬大量資料 | 適合網路傳太慢或資料量極大 | 離線搬遷 |

</details>

---

## 32. 邊緣與混合雲

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：把 AWS 硬體和服務放到客戶機房。差異提示：本地也要跑 AWS 服務。關鍵字：On-prem AWS。
2. `___`：把 AWS 放到 5G 電信網路邊緣。差異提示：適合 5G 超低延遲應用。關鍵字：5G、低延遲。
3. `___`：大城市附近的小型 AWS 延伸區域。差異提示：靠近使用者降低延遲。關鍵字：城市、低延遲。
4. `___`：CloudFront 快取節點。差異提示：用於 CDN 快取，不是完整 Region。關鍵字：CDN、快取。
5. `___`：地理區域。差異提示：最大地理單位，內含多個 AZ。關鍵字：區域。
6. `___`：Region 內隔離的資料中心群。差異提示：用於高可用架構。關鍵字：AZ、高可用。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | AWS Outposts | 把 AWS 硬體和服務放到客戶機房 | 本地也要跑 AWS 服務 | On-prem AWS |
| 2 | AWS Wavelength | 把 AWS 放到 5G 電信網路邊緣 | 適合 5G 超低延遲應用 | 5G、低延遲 |
| 3 | AWS Local Zones | 大城市附近的小型 AWS 延伸區域 | 靠近使用者降低延遲 | 城市、低延遲 |
| 4 | Edge Location | CloudFront 快取節點 | 用於 CDN 快取，不是完整 Region | CDN、快取 |
| 5 | AWS Region | 地理區域 | 最大地理單位，內含多個 AZ | 區域 |
| 6 | Availability Zone | Region 內隔離的資料中心群 | 用於高可用架構 | AZ、高可用 |

</details>

---

## 33. Snow 系列

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：Snow 裝置系列總稱。差異提示：包含 Snowball、Snowball Edge 等。關鍵字：Snow 系列。
2. `___`：用實體設備搬大量資料。差異提示：偏資料搬運。關鍵字：離線資料搬遷。
3. `___`：搬資料加上邊緣運算能力。差異提示：可在本地先做一些處理。關鍵字：Edge Compute。
4. `___`：管理 Snow 裝置的圖形工具。差異提示：管理工具，不是搬資料設備本身。關鍵字：GUI 管理。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | AWS Snow Family | Snow 裝置系列總稱 | 包含 Snowball、Snowball Edge 等 | Snow 系列 |
| 2 | AWS Snowball | 用實體設備搬大量資料 | 偏資料搬運 | 離線資料搬遷 |
| 3 | AWS Snowball Edge | 搬資料加上邊緣運算能力 | 可在本地先做一些處理 | Edge Compute |
| 4 | AWS OpsHub | 管理 Snow 裝置的圖形工具 | 管理工具，不是搬資料設備本身 | GUI 管理 |

</details>

---

## 34. 災難復原策略

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：成本 最低，恢復速度 最慢。差異提示：平常只備份，災難時再還原。
2. `___`：成本 低，恢復速度 較慢。差異提示：只保留最小核心系統。
3. `___`：成本 中，恢復速度 較快。差異提示：平常跑縮小版系統，災難時放大。
4. `___`：成本 最高，恢復速度 最快。差異提示：多站點同時完整運作。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 成本 | 恢復速度 | 差異重點 |
|---:|---|---:|---:|---|
| 1 | Backup and Restore | 最低 | 最慢 | 平常只備份，災難時再還原 |
| 2 | Pilot Light | 低 | 較慢 | 只保留最小核心系統 |
| 3 | Warm Standby | 中 | 較快 | 平常跑縮小版系統，災難時放大 |
| 4 | Multi-Site Active/Active | 最高 | 最快 | 多站點同時完整運作 |

記憶法：成本和恢復速度通常一起上升。

</details>

---

## 35. 支援計畫

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：所有 AWS 使用者。差異提示：免費，主要支援帳戶、帳單、基本健康狀態。關鍵字：免費。
2. `___`：開發測試。差異提示：Email 技術支援，支援範圍較有限。關鍵字：開發測試。
3. `___`：正式營運工作負載。差異提示：24/7 技術支援，完整 Trusted Advisor 檢查。關鍵字：Production、24/7。
4. `___`：介於 Business 和 Enterprise。差異提示：有一組 TAM 團隊支援。關鍵字：TAM 團隊。
5. `___`：大型企業關鍵工作負載。差異提示：指定 TAM、Concierge、重大活動支援。關鍵字：最高等級。
6. `___`：企業支援的技術顧問。差異提示：協助規劃和優化 AWS 使用。關鍵字：TAM。
7. `___`：帳務與帳戶協助。差異提示：偏帳務、帳戶、方案問題。關鍵字：帳務禮賓。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Basic Support | 所有 AWS 使用者 | 免費，主要支援帳戶、帳單、基本健康狀態 | 免費 |
| 2 | Developer Support | 開發測試 | Email 技術支援，支援範圍較有限 | 開發測試 |
| 3 | Business Support | 正式營運工作負載 | 24/7 技術支援，完整 Trusted Advisor 檢查 | Production、24/7 |
| 4 | Enterprise On-Ramp Support | 介於 Business 和 Enterprise | 有一組 TAM 團隊支援 | TAM 團隊 |
| 5 | Enterprise Support | 大型企業關鍵工作負載 | 指定 TAM、Concierge、重大活動支援 | 最高等級 |
| 6 | Technical Account Manager | 企業支援的技術顧問 | 協助規劃和優化 AWS 使用 | TAM |
| 7 | AWS Concierge | 帳務與帳戶協助 | 偏帳務、帳戶、方案問題 | 帳務禮賓 |

</details>

---

## 36. Manager 相關容易混淆組

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：安全保存密碼、API Key、資料庫密碼。差異提示：可自動輪換機密，重點是「機密資料管理」，不是伺服器維運。關鍵字：Secret、密碼、自動輪換。
2. `___`：集中管理 EC2 或本地伺服器。差異提示：可做派送命令、修補、盤點、自動化等，是系統管理服務總稱。關鍵字：SSM、修補、盤點、Run Command。
3. `___`：不用開 SSH 連接埠，也能安全連進 EC2。差異提示：它是 Systems Manager 裡的一項功能，重點是「建立安全工作階段」。關鍵字：Session、遠端連線、不開 SSH。
4. `___`：企業支援中的技術顧問。差異提示：這是 AWS Enterprise Support 相關的人員角色，不是 AWS 服務。關鍵字：TAM、Enterprise Support、技術顧問。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | AWS Secrets Manager | 安全保存密碼、API Key、資料庫密碼 | 管「機密資料」，可自動輪換；不是用來管理 EC2 或遠端連線 | Secret、密碼、自動輪換 |
| 2 | AWS Systems Manager | 集中管理 EC2 或本地伺服器 | 管「系統與伺服器維運」，包含修補、命令、盤點、自動化 | SSM、修補、盤點、Run Command |
| 3 | AWS Systems Manager Session Manager | 不用開 SSH 連接埠也能安全連進 EC2 | 是 Systems Manager 的功能之一，專門建立安全互動式連線 | Session、遠端連線、不開 SSH |
| 4 | Technical Account Manager | 企業支援中的技術顧問 | 是 Enterprise Support 裡的人員角色，不是可部署的 AWS 服務 | TAM、Enterprise Support、技術顧問 |

記憶法：看到 `Secrets` 想密碼；看到 `Systems` 想伺服器管理；看到 `Session` 想遠端連線；看到 `Technical Account` 想企業支援顧問。

</details>

---

## 37. 雲端優勢概念 vs Well-Architected 支柱

請根據提示，填入正確的 AWS 名詞或雲端概念。

1. `___`：需要新資源時可以很快取得。差異提示：重點是速度與行動力，不用等採購、拉線、進機房。關鍵字：快速開資源、敏捷。
2. `___`：流量多就自動加資源，流量少就縮回來。差異提示：重點是隨需求自動伸縮，避免浪費。關鍵字：自動增減、流量變動。
3. `___`：系統可以隨著使用者或需求變多而撐住。差異提示：可以靠水平擴展或垂直擴展，不一定代表自動。關鍵字：可擴展、Scale。
4. `___`：系統能穩定運作，故障後也能恢復。差異提示：這是雲端架構的品質概念，不是 Well-Architected 裡的支柱名稱。關鍵字：可靠、容錯、恢復。
5. `___`：服務盡量保持可用，即使單一資料中心出問題也不中斷。差異提示：更聚焦在「可用不中斷」，常是 Reliability 的一部分。關鍵字：多 AZ、不中斷、可用。
6. `___`：AWS 的架構最佳實務框架。差異提示：用六大支柱檢查整體架構，不是單一技術服務。關鍵字：六大支柱、架構檢查。
7. `___`：重點是自動化、可回復的小變更、營運流程。差異提示：這是 Well-Architected 的支柱之一，管營運方式。關鍵字：營運、自動化、流程。
8. `___`：重點是權限、加密、偵測、資料與系統保護。差異提示：這是 Well-Architected 的安全支柱。關鍵字：安全、權限、加密。
9. `___`：重點是故障恢復、容錯、水平擴展與高可用設計。差異提示：這是 Well-Architected 的支柱名稱，和一般概念 Reliability 很像但層級不同。關鍵字：支柱、容錯、恢復。
10. `___`：重點是選對資源類型與大小。差異提示：避免效能不足，也避免過度配置。關鍵字：效能、資源規格。
11. `___`：重點是正確定價模式、刪除閒置資源、降低不必要成本。差異提示：這是 Well-Architected 的成本支柱。關鍵字：成本、節省、最佳化。

<details>
<summary>答案與差異</summary>

| 題號 | 答案 | 主要提示 | 差異重點 | 常見關鍵字 |
|---:|---|---|---|---|
| 1 | Agility | 需要新資源時可以很快取得 | 雲端優勢概念，強調速度與行動力 | 快速開資源、敏捷 |
| 2 | Elasticity | 流量多加資源、流量少縮回來 | 雲端優勢概念，強調依需求自動伸縮 | 自動增減、流量變動 |
| 3 | Scalability | 系統能隨需求變大 | 雲端優勢概念，可水平或垂直擴展，不一定自動 | 可擴展、Scale |
| 4 | Reliability | 系統穩定運作並能故障恢復 | 一般架構品質概念，不是 Well-Architected 支柱名稱本身 | 可靠、容錯、恢復 |
| 5 | High Availability | 服務盡量保持可用 | 聚焦「不中斷可用」，通常是可靠性設計的一部分 | 多 AZ、不中斷、可用 |
| 6 | AWS Well-Architected Framework | AWS 架構最佳實務框架 | 用六大支柱檢查整體架構 | 六大支柱、架構檢查 |
| 7 | Operational Excellence Pillar | 自動化、可回復的小變更、營運流程 | Well-Architected 支柱，重點是營運做得好不好 | 營運、自動化、流程 |
| 8 | Security Pillar | 權限、加密、偵測、資料與系統保護 | Well-Architected 支柱，重點是安全設計 | 安全、權限、加密 |
| 9 | Reliability Pillar | 故障恢復、容錯、水平擴展與高可用設計 | Well-Architected 支柱；`Reliability` 是概念，`Reliability Pillar` 是檢查分類 | 支柱、容錯、恢復 |
| 10 | Performance Efficiency Pillar | 選對資源類型與大小 | Well-Architected 支柱，重點是效能與資源效率 | 效能、資源規格 |
| 11 | Cost Optimization Pillar | 正確定價模式、刪除閒置資源、降低成本 | Well-Architected 支柱，重點是成本最佳化 | 成本、節省、最佳化 |

記憶法：`Agility / Elasticity / Scalability / Reliability / High Availability` 是雲端優勢或架構品質概念；`Operational Excellence / Security / Reliability / Performance Efficiency / Cost Optimization Pillar` 是 Well-Architected 的檢查分類。

</details>

---

## 38. 最容易一眼判斷的關鍵字

請根據題目線索，填入最可能對應的 AWS 名詞。

1. 題目說「Private Subnet 要連出去更新套件」時，優先想到 `___`。
2. 題目說「VPC 公開連網」時，優先想到 `___`。
3. 題目說「VPN 在 AWS 端」時，優先想到 `___`。
4. 題目說「VPN 在公司機房端」時，優先想到 `___`。
5. 題目說「多個 VPC 集中互連」時，優先想到 `___`。
6. 題目說「建立 REST 或 WebSocket API」時，優先想到 `___`。
7. 題目說「本地儲存接 AWS 儲存」時，優先想到 `___`。
8. 題目說「網站依網址路徑分流」時，優先想到 `___`。
9. 題目說「TCP/UDP 低延遲分流」時，優先想到 `___`。
10. 題目說「全球 CDN 快取」時，優先想到 `___`。
11. 題目說「固定 IP 全球入口加速」時，優先想到 `___`。
12. 題目說「查誰呼叫了 AWS API」時，優先想到 `___`。
13. 題目說「看 CPU、日誌、警報」時，優先想到 `___`。
14. 題目說「查資源設定是否合規」時，優先想到 `___`。
15. 題目說「S3 敏感資料掃描」時，優先想到 `___`。
16. 題目說「EC2 或容器弱點掃描」時，優先想到 `___`。
17. 題目說「帳戶威脅偵測」時，優先想到 `___`。
18. 題目說「App 使用者註冊登入」時，優先想到 `___`。
19. 題目說「員工多帳戶單一登入」時，優先想到 `___`。
20. 題目說「SQL 關聯式資料庫」時，優先想到 `___`。
21. 題目說「NoSQL 鍵值資料庫」時，優先想到 `___`。
22. 題目說「直接 SQL 查 S3」時，優先想到 `___`。
23. 題目說「ETL 整理資料」時，優先想到 `___`。
24. 題目說「訊息排隊解耦」時，優先想到 `___`。
25. 題目說「一對多通知」時，優先想到 `___`。
26. 題目說「工作流程狀態機」時，優先想到 `___`。
27. 題目說「用 YAML/JSON 建資源」時，優先想到 `___`。
28. 題目說「用 Python/TypeScript 寫雲端架構」時，優先想到 `___`。
29. 題目說「保存密碼、API Key，並可自動輪換」時，優先想到 `___`。
30. 題目說「集中管理 EC2 或本地伺服器、修補、盤點」時，優先想到 `___`。
31. 題目說「不用開 SSH 連接埠也能連進 EC2」時，優先想到 `___`。
32. 題目說「企業支援中的技術顧問」時，優先想到 `___`。
33. 題目說「需要新資源時可以很快取得」時，優先想到 `___`。
34. 題目說「流量多自動加資源，流量少自動縮回」時，優先想到 `___`。
35. 題目說「系統能隨使用者或需求變多而撐住」時，優先想到 `___`。
36. 題目說「服務盡量不中斷、持續可用」時，優先想到 `___`。
37. 題目說「用六大支柱檢查架構」時，優先想到 `___`。
38. 題目說「Well-Architected 裡的可靠性支柱」時，優先想到 `___`。

<details>
<summary>答案</summary>

| 題號 | 題目線索 | 答案 |
|---:|---|---|
| 1 | Private Subnet 要連出去更新套件 | NAT Gateway |
| 2 | VPC 公開連網 | Internet Gateway |
| 3 | VPN 在 AWS 端 | Virtual Private Gateway |
| 4 | VPN 在公司機房端 | Customer Gateway |
| 5 | 多個 VPC 集中互連 | AWS Transit Gateway |
| 6 | 建立 REST 或 WebSocket API | Amazon API Gateway |
| 7 | 本地儲存接 AWS 儲存 | AWS Storage Gateway |
| 8 | 網站依網址路徑分流 | Application Load Balancer |
| 9 | TCP/UDP 低延遲分流 | Network Load Balancer |
| 10 | 全球 CDN 快取 | Amazon CloudFront |
| 11 | 固定 IP 全球入口加速 | AWS Global Accelerator |
| 12 | 查誰呼叫了 AWS API | AWS CloudTrail |
| 13 | 看 CPU、日誌、警報 | Amazon CloudWatch |
| 14 | 查資源設定是否合規 | AWS Config |
| 15 | S3 敏感資料掃描 | Amazon Macie |
| 16 | EC2 或容器弱點掃描 | Amazon Inspector |
| 17 | 帳戶威脅偵測 | Amazon GuardDuty |
| 18 | App 使用者註冊登入 | Amazon Cognito |
| 19 | 員工多帳戶單一登入 | IAM Identity Center |
| 20 | SQL 關聯式資料庫 | Amazon RDS 或 Amazon Aurora |
| 21 | NoSQL 鍵值資料庫 | Amazon DynamoDB |
| 22 | 直接 SQL 查 S3 | Amazon Athena |
| 23 | ETL 整理資料 | AWS Glue |
| 24 | 訊息排隊解耦 | Amazon SQS |
| 25 | 一對多通知 | Amazon SNS |
| 26 | 工作流程狀態機 | AWS Step Functions |
| 27 | 用 YAML/JSON 建資源 | AWS CloudFormation |
| 28 | 用 Python/TypeScript 寫雲端架構 | AWS CDK |
| 29 | 保存密碼、API Key，並可自動輪換 | AWS Secrets Manager |
| 30 | 集中管理 EC2 或本地伺服器、修補、盤點 | AWS Systems Manager |
| 31 | 不用開 SSH 連接埠也能連進 EC2 | AWS Systems Manager Session Manager |
| 32 | 企業支援中的技術顧問 | Technical Account Manager |
| 33 | 需要新資源時可以很快取得 | Agility |
| 34 | 流量多自動加資源，流量少自動縮回 | Elasticity |
| 35 | 系統能隨使用者或需求變多而撐住 | Scalability |
| 36 | 服務盡量不中斷、持續可用 | High Availability |
| 37 | 用六大支柱檢查架構 | AWS Well-Architected Framework |
| 38 | Well-Architected 裡的可靠性支柱 | Reliability Pillar |

</details>

---


