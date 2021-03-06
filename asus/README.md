# 版本說明

此版本為與華碩雲端整合之客製版本，目前以雲端寶盒專案當作唯一專案。
企業/帳號/組織等維護以API方式提供給華碩呼叫，而引擎功能需和最新版引擎功能同步。
MAE除了登入登出改以華碩的流程，其他功能則需同步

# 服務流程

## 服務初始化
![服務初始化]

## 管理員執行成員清單同步
![管理員成員清單同步]

### 帳號同步標準
1. RTE不存在新增
2. 狀態更新(啟用、停用、nikename)
3. Member List不存在刪除

## 成員執行自己資訊同步
![成員執行自己資訊同步]

## 服務刪除
![服務刪除]

## 架構說明
![環境架構]

* 上述為雲端寶盒環境架構圖，根據上圖可得到以下角色:
    * Web user : 使用Web瀏覽器進入ASUS Web Storage以及使用雲端寶盒的使用者。
    * App user : 使用App進入ASUS Web Storage以及使用雲端寶盒的使用者。
    * ASUS WebStorage : 負責以下工作
        * 呼叫master ruRu RTE執行企業資料維護
        * Web user以及App user的帳號認證
        * 將雲端寶盒使用者導向至 slave ruRu RTE
        * 接受master ruRu RTE / slave ruRu RTE呼叫，取得企業相關資料以及帳號相關資料
    * master ruRu RTE : 負責以下工作
        * 執行雲端寶盒系統排程
        * 其餘工作同slave ruRu RTE
    * slave ruRu RTE : 負責以下工作
        * 作為Web user / App user使用雲端寶盒系統的AP Server
        * 接受ASUS WebStorage執行以下工作
            * 新增企業組織
            * 刪除企業組織
            * 同步企業組織帳號
    * SQL Server database : 雲端寶盒系統的資料庫

[服務初始化]:image/ASUS-SERVICE-FLOW-INIT.png "服務初始化"
[管理員成員清單同步]:image/ASUS-SERVICE-FLOW-AD.png "管理員成員清單同步"
[成員執行自己資訊同步]:image/ASUS-SERVICE-FLOW-MB.png "成員執行自己資訊同步"
[服務刪除]:image/ASUS-SERVICE-FLOW-DELETE.png "服務刪除"
[環境架構]:image/architecture.png "環境架構"