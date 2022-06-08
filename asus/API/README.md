### <div id="enterprise">企業組織資料維護</div>
* 說明 : 提供給ASUS Account Service呼叫，用來進行企業組織資料維護
    * 新增企業組織
    * 刪除企業組織
    * 帳號資料同步
* 備註 : 採非同步方式呼叫，API僅回傳已接收給ASUS Account Service，背景執行資料維護的動作。

### <div id="addenterpriseflow">新增企業組織 <path>(企業組織資料維護)</div>
* 說明 : 採非同步方式提供給ASUS Account Service呼叫，用來新增企業組織，並依據token取得管理員帳號資料新增至該企業組織，再將該管理員下的memberlist作為使用者帳號加入企業組織。
* 支援以下兩種模式
    * 使用Token呼叫
    * Server to Server呼叫

### <div id="addenterprisetokenflow">Token認證 <path>(企業組織資料維護/新增企業組織)</div>
* 限制 : 透過token取得WFB Info，type=admin 且 supportRuru=1
* Request : (HTTP POST; https:// {{ API Host }} /maintain/enterprise/add/token)
    * Body
        * token_type : token的格式， type string
        * token : access token， type string
    * Example
        * URL : https:// {{ API Host }} /maintain/enterprise/add/token
        * Body : token_type=BEARER&token=1234567898asdasdasd

* Response
    * Body (JSON)
        * { receive : true }

* 新增企業組織(Token)流程圖

    ![新增企業組織(Token)流程圖]

### <div id="addenterpriseserverflow">Server to server <path>(企業組織資料維護/新增企業組織)</div>
* 限制 : 呼叫端的IP須在信任的IP清單中
* Request : (HTTP POST; https:// {{ API Host }} /maintain/enterprise/add/server)
    * Body
        * areaId : 服務區，type int
        * commercialId : 組織編號，type long
    * Example
        * URL : https:// {{ API Host }} /maintain/enterprise/add/server
        * Body : areaId=1&commercialId=123456789
* Response
    * Body (JSON)
        * { receive : true }
* 新增企業組織(ServerToServer)流程圖

    ![新增企業組織(ServerToServer)流程圖]

### <div id="deleteenterpriseflow">刪除企業組織 <path>(企業組織資料維護)</div>
* 說明 : 提供給ASUS Account Service呼叫，用來刪除企業組織，當呼叫此API時，會刪除該企業組織下所有企業資料、帳號資料以及組織資料庫。
* 僅支援Server to Server呼叫

### <div id="deleteenterpriseserverflow">Server to server <path>(企業組織資料維護/刪除企業組織)</div>
* 限制 : 呼叫端的IP須在信任的IP清單中
* Request : (HTTP POST; https:// {{ API Host }} /maintain/enterprise/delete/server)
    * Body
        * areaId : 服務區，type int
        * commercialId : 組織編號，type long
    * Example
        * URL : https:// {{ API Host }} /maintain/enterprise/delete/server
        * Body : areaId=1&commercialId=123456789
* Response
    * Body (JSON)
        * { receive : true }
* 刪除企業組織流程圖

    ![刪除企業組織流程圖]

### <div id="syncaccountflow">帳號資料同步 <path>(企業組織資料維護)</div>
* 說明 : 提供給ASUS Account Service呼叫，用來執行帳號資料同步，當呼叫此API時，會依據WFB Member list資料進行帳號同步。
* 支援以下兩種模式
    * 使用Token呼叫
    * Server to Server呼叫

### <div id="syncaccounttokenflow">Token驗證 <path>(企業組織資料維護/帳號資料同步)</div>
* 限制 : 透過token取得WFB Info，type=admin 且 supportRuru=1
* Request : (HTTP POST; https:// {{ API Host }} /maintain/enterprise/sync/token)
    * Body
        * token_type : token的格式， type string
        * token : access token， type string
    * Example
        * URL : https:// {{ API Host }} /maintain/enterprise/sync/token
        * Body : token_type=BEARER&token=1234567898asdasdasd
* Response
    * Body (JSON)
        * { receive : true }
* 帳號資料同步(Token)流程圖

    ![帳號資料同步(Token)流程圖]

### <div id="syncaccountserverflow">Server to server <path>(企業組織資料維護/帳號資料同步)</div>
* 限制 : 呼叫端的IP須在信任的IP清單中
* Request : (HTTP POST; https:// {{ API Host }} /maintain/enterprise/sync/server)
    * Body
        * areaId : 服務區，type int
        * commercialId : 組織編號，type long
    * Example
        * URL : https:// {{ API Host }} /maintain/enterprise/sync/server
        * Body : areaId=1&commercialId=123456789
* Response
    * Body (JSON)
        * { receive : true }
* 帳號資料同步(ServerToServer)流程圖

    ![帳號資料同步(ServerToServer)流程圖]

### <div id="service">系統狀態查詢</div>
* 說明 : 提供給ASUS Account Service呼叫，用來確認AP Server是否可正常連線
* Server to Server呼叫
* 採同步呼叫，確認資料庫連線狀態後回傳給ASUS Account Service。

### <div id="serviceflow">Server to server <path>(系統狀態查詢)</div>
* 限制 : 呼叫端的IP須在信任的IP清單中
* Request : (HTTP GET; https:// {{ API Host }} /maintain/status)
    * Parameter
        * 無
* Response
    * Body (JSON)
        * { status : 狀態碼 }
        * 狀態碼清單
        | 狀態碼        | 代碼說明           |
        | ------------- |:-------------:|
        | 200      | 執行成功 |
        | 1002      | 建立資料庫連線失敗      |
* 系統狀態查詢流程圖

    ![系統狀態查詢流程圖]

### <div id="asusconfig">API設定</div>
* 設定檔案路徑 : {Tomcat Path}\conf\asus_api.properties
* 參數清單
| 參數名稱        | 參數說明           |
| ------------- |:-------------:|
| rteClientId      | RTE向ASUS Account Service 申請的 Client ID |
| rteClientIdVersion      | RTE向ASUS Account Service 申請的 Client ID Version|
| rteClientSecret      | RTE向ASUS Account Service 申請的 Client Secret      |
| maeIosClientId      | MAE向ASUS Account Service 申請的 IOS 版 Client ID      |
| maeIosClientIdVersion      | MAE向ASUS Account Service 申請的 IOS 版 Client ID Version|
| maeIosClientSecret      | MAE向ASUS Account Service 申請的 IOS 版 Client Secret |
| maeAndroidClientId      | MAE向ASUS Account Service 申請的 Android 版 Client ID |
| maeAndroidClientIdVersion      | MAE向ASUS Account Service 申請的 Android 版 Client ID Version|
| maeAndroidClientSecret      | MAE向ASUS Account Service 申請的 Android 版 Client Secret |
| asusAccountServiceLoginUrl      | ASUS Account Service Login Page URL|
| asusAccountServiceLogoutUrl      | ASUS Account Service Logout API URL |
| asusAccountServiceAccessTokenUrl      | ASUS Account Service Get/Refresh Access Token API URL |
| asusAccountServiceUserInfoUrl      | ASUS Account Service Get User Info API URL |
| asusAccountServiceWFBInfoUrl      | ASUS Account Service Get WFB Info API URL |
| projectId      | 雲端寶盒-系統代號 |
| companyId      | 雲端寶盒-範本組織代號 |
| adminGroupNo      | 雲端寶盒系統-權限管理者角色代號 |
| userGroupNo      | 雲端寶盒系統-權限使用者角色代號 |
| orgPlanNo      | 雲端寶盒系統-權限組織編制計畫代號 |
| whiteList      | 信任的IP來源，可接受多組位置以,連接在一起。如: 192.168.1.1,192.168.22.11 |

* 注意事項 : 需在API程式啟動前將此設定檔案填寫完畢並放到{Tomcat Path}\conf，否則當API啟動時，讀不到此設定檔案會將服務停止。

[新增企業組織(Token)流程圖]:attachment/sd_addenterprise(Token).png "新增企業組織(Token)流程圖"
[新增企業組織(ServerToServer)流程圖]:attachment/sd_syncaccount(ServertoServer).png "新增企業組織(ServerToServer)流程圖"
[刪除企業組織流程圖]:attachment/sd_deleteenterprise.png "刪除企業組織流程圖"
[帳號資料同步(Token)流程圖]:attachment/sd_syncaccount(Token).png "帳號資料同步(Token)流程圖"
[帳號資料同步(ServerToServer)流程圖]:attachment/sd_syncaccount(ServertoServer).png "帳號資料同步(ServerToServer)流程圖"
[系統狀態查詢流程圖]:attachment/sd_service.png "系統狀態查詢流程圖"
