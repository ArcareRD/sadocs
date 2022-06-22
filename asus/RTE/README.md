### <div id="login">RTE登入</div>
* 說明 : 檢查是否已登入RTE系統，若尚未登入則檢查是否由ASUS Account Service轉向而來，若不是則將頁面導向至未登入的畫面
* 限制 : 無
* Request : (HTTP GET; https:// {{ RTE Host }} /ArcareEng/login.jsp)
    * Parameter
        * code : type string，授權碼，由ASUS Account Service轉向時傳入，RTE會使用此授權碼向ASUS Account Service取得以下資訊
            * token type
            * access token
            * refresh token
            * 使用者帳號
    * Example
        * https:// {{ RTE Host }} /ArcareEng/login.jsp?code=012f956d-e925-4139-b227-db0373b4b52e
* Response
    * Redirect
        * 若code不存在則導向 unlogin.jsp (未登入畫面)
        * 若登入失敗則顯示錯誤訊息
* 登入流程圖

    ![登入流程圖]

### <div id="logout">RTE登出</div>
* 說明 : 執行RTE的登出以及呼叫ASUS Account Service Logout API
* 限制 : 無
* Request : (HTTP GET; https:// {{ RTE Host }} /ArcareEng/logout.jsp)
    * Parameter : 無
    * Example
        * https:// {{ RTE Host }} /ArcareEng/logout.jsp
* Response
    * Redirect
        * unlogin.jsp (未登入畫面)
* 登出流程圖

    ![登出流程圖]

### <div id="applogin">MAE登入</div>
* 說明 : 提供給MAE APP呼叫，用來登入。
* 限制 : 無
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppRuntimeLogin)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},						
        languageId : (String)語系,						
        deviceId : (String)手機MAC IMEI,
        deviceName : (String)手機裝置名稱(提供給華碩API參數.x-asc-device-name),
        tokenType : (String)token type,
        accessToken : (String)access token,						
        refreshToken : (String)refresh token,
        deviceType : (Integer)裝置類型 1.ios / 2.android
        deviceModel : (String)裝置作業系統版本,(提供給華碩API參數.x-asc-device-model)
    }						
```
* Response
    * Body (JSON)
```Json
    {							
        result : (boolean)執行結果,						
        error : (String)錯誤訊息,
    #回傳資訊_start								
        userId : (Long)使用者序號,						
        enterpriseId : (String)企業唯一號,						
        enterpriseNo : (String)企業代碼(result=true or isactive=false 會回傳),						
        enterpriseName : (String)企業名稱,						
        userName : (String)使用者姓名,						
        project : (JOSNArray)系統、組織、語系						
            [					
                {				
                    id : (String)系統代號			
                    name : (String)系統名稱			
                    makeId : (String)組裝代號
                    icon : (String)圖示料號 (預留)			
                    corp : (JSONArray)組織清單			
                        [		
                            {	
                                id : (String)組織代號,
                                name : (String)組織名稱,
                                corpId : (int)組織序號,
                            }, …	
                        ]		
                    language : (JSONArray)語系清單			
                        [		
                            {	
                                id : (String)代碼
                                name : (String)名稱
                            }, …	
                        ]		
                }, …				
            ],					
        onlineId : (String)使用者上線唯一號, (#7934),
        mainDeviceId : (String) 使用者主裝置代號，若未設定則給null,
        tokenType : (String)token type,
        accessToken : (String)access token,						
        refreshToken : (String)refresh token,
        maintain : {
            action : (String)該使用者所屬的雲端寶盒組織正在執行的維護動作(新增組織=new/刪除組織=delete/帳號同步=sync)
            areaId : (Int) 服務區，用來取得系統初始化狀態的參數,
            commercialId : (Long) 組織編號，用來取得系統初始化狀態的參數,
        }
        
    #回傳資訊_end								
    }
```

### <div id="applogout">MAE登出</div>
* 說明 : 提供給MAE APP呼叫，用來登出。
* 限制 : 無
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppRuntimeLogout)
    * Body(JSON)
```Json
    {	
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},
        userId : 使用者代號
        onlineId : (String)使用者上線唯一號,
        languageId : (String)語系,
        tokenType : (String)token type,
        accessToken : (String)access token,						
        refreshToken : (String)refresh token,
        deviceType : (Integer)裝置類型 1.ios / 2.android
    }							
```
* Response
    * Body (JSON)
```Json
    {	
        result : (boolean)執行結果,
        error : (String)錯誤訊息
    }														
```

### <div id="appgettoken">MAE使用驗證碼取得Token</div>
* 說明 : 提供給MAE APP呼叫，用來取得華碩AccountService的Token。
* 限制 : 無
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetToken)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},						
        languageId : (String)語系,						
        code : (String)華碩提供的授權碼,
        deviceType : (Integer)裝置類型 1.ios / 2.android,
        deviceName : (String)裝置名稱,(提供給華碩API參數.x-asc-device-name),
        deviceModel : (String)裝置作業系統版本,(提供給華碩API參數.x-asc-device-model)
    }						
```
* Response
    * Body (JSON)
```Json
    {							
        result : (boolean)執行結果,						
        error : (String)錯誤訊息(result = false時才有)						
     #回傳資訊_start	(當result = true時才有)							
        tokenType : (String)token type,
        accessToken : (String)access token,						
        refreshToken : (String)refresh token
    #回傳資訊_end									
    }
```

### <div id="apprefreshtoken">MAE Refresh Token</div>
* 說明 : 提供給MAE APP呼叫，用來重新取得華碩access token。
* 限制 : 無
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppRefreshToken)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},						
        languageId : (String)語系,						
        refreshToken : (String)refresh token,
        deviceType : (Integer)裝置類型 1.ios / 2.android,
        deviceName : (String)裝置名稱,(提供給華碩API參數.x-asc-device-name),
        deviceModel : (String)裝置作業系統版本,(提供給華碩API參數.x-asc-device-model)
    }
```
* Response
    * Body (JSON)
```Json
    {							
        result : (boolean)執行結果,						
        error : (String)錯誤訊息(result = false時才有)						
    #回傳資訊_start	(當result = true時才有)							
        tokenType : (String)token type,
        accessToken : (String)access token,						
        refreshToken : (String)refresh token
    #回傳資訊_end								
    }
```

### <div id="appgetinitstatus">MAE 取得系統初始化狀態</div>
* 說明 : 提供給MAE APP呼叫，用來查詢指定的企業組織資料庫是否已初始化完成。
* 限制 : 無
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetInitStatus)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},						
        languageId : (String)語系,						
        areaId : (Int)服務區,
        commercialId : (Long)組織編號
    }
```
* Response
    * Body (JSON)
```Json
    {							
        finish : (boolean)執行完成否,
        success : (boolean)執行成功否,
        error : (String)錯誤訊息,當success=false時出現
    }
```

### <div id="brainworknew">首頁畫面修正</div>
* 如下圖所示為首頁畫面須修正的部分

    ![首頁畫面修正]

### <div id="enterprise">企業組織資料維護</div>
* 說明 : 提供給ASUS Account Service呼叫，用來進行企業組織資料維護
    * 新增企業組織
        * 功能說明 : 
            * 建立指定的企業組織資料庫
            * 呼叫ASUS Account Service取得企業組織相關成員並自動新增帳號以及相關權限
            * 依據參數設定建立[資料庫備份維護計畫](README.md#dbbackup)
            * 建立資料庫備份檔案
    * 刪除企業組織
        * 功能說明 : 
            * 刪除指定的企業組織資料庫 / 該企業組織下所有成員帳號
            * 刪除已建立的[資料庫備份維護計畫](README.md#dbbackup)
            * 此處無法刪除資料庫備份檔案，檔案須由人工手動搬遷或刪除
    * 帳號資料同步
        * 功能說明 : 
            * 呼叫ASUS Account Service取得企業組織相關成員帳號資料
                * 帳號存在於企業組織資料庫，依據資料進行更新帳號
                * 帳號不存在於企業組織資料庫，依據資料進行新增帳號
                * 企業組織資料庫有不存在於ASUS Account Service的帳號，刪除帳號

* 備註 : 採非同步方式呼叫，API僅回傳已接收給ASUS Account Service，背景執行資料維護的動作。

### <div id="addenterpriseflow">新增企業組織 <path>(企業組織資料維護)</div>
* 說明 : 採非同步方式提供給ASUS Account Service呼叫，用來新增企業組織，並依據token取得管理員帳號資料新增至該企業組織，再將該管理員下的memberlist作為使用者帳號加入企業組織。
* 支援以下兩種模式
    * 使用Token呼叫
    * Server to Server呼叫

### <div id="addenterprisetokenflow">Token認證 <path>(企業組織資料維護/新增企業組織)</div>
* 限制 : 透過token向ASUS Account Service取得User Info，User Info內的type=admin 且 supportRuru=1
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance)
    * Body(encoded body)
        * token_type : token的格式， type string
        * token : access token， type string
        * action : 固定字串 new
    * Example
        * URL : https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance
        * Body : token_type=BEARER&token=1234567898asdasdasd&action=new


* Response
    * Body (JSON)
        * { receive : true }

* 新增企業組織(Token)流程圖

    ![新增企業組織(Token)流程圖]

### <div id="addenterpriseserverflow">Server to server <path>(企業組織資料維護/新增企業組織)</div>
* 限制 : 呼叫端的IP須在信任的IP清單中
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/ServerMaintenance)
    * Body
        * areaId : 服務區，type int
        * commercialId : 組織編號，type long
        * action : 固定字串 new
    * Example
        * URL : https:// {{ RTE Host }} /ArcareEng/ServerMaintenance
        * Body : areaId=1&commercialId=123456789&action=new
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
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/ServerMaintenance)
    * Body
        * areaId : 服務區，type int
        * commercialId : 組織編號，type long
        * action : 固定字串 delete
    * Example
        * URL : https:// {{ RTE Host }} /ArcareEng/ServerMaintenance
        * Body : areaId=1&commercialId=123456789&action=delete
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
* 限制 : 透過token向ASUS Account Service取得User Info，User Info內的type=admin 且 supportRuru=1
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance)
    * Body
        * token_type : token的格式， type string
        * token : access token， type string
        * action : 固定字串 sync
    * Example
        * URL : https:// {{ RTE Host }} /ArcareEng/enterprise/sync/token
        * Body : token_type=BEARER&token=1234567898asdasdasd&action=sync
* Response
    * Body (JSON)
        * { receive : true }
* 帳號資料同步(Token)流程圖

    ![帳號資料同步(Token)流程圖]

### <div id="syncaccountserverflow">Server to server <path>(企業組織資料維護/帳號資料同步)</div>
* 限制 : 呼叫端的IP須在信任的IP清單中
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/ServerMaintenance)
    * Body
        * areaId : 服務區，type int
        * commercialId : 組織編號，type long
        * action : 固定字串 sync
    * Example
        * URL : https:// {{ RTE Host }} /ArcareEng/ServerMaintenance
        * Body : areaId=1&commercialId=123456789&action=sync
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
* Request : (HTTP GET; https:// {{ RTE Host }} /ArcareEng/ServiceStatus)
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

### <div id="asusconfig">RTE設定</div>
* 設定檔案路徑 : { Tomcat Path } \conf\asus_api.properties
* 參數清單
| 參數名稱        | 參數說明           |
| ------------- |:-------------|
| rteRedirectUri   | RTE呼叫ASUS Account Service 指定的 redirect_uri |
| rteClientId      | RTE向ASUS Account Service 申請的 Client ID |
| rteClientIdVersion      | RTE向ASUS Account Service 申請的 Client ID Version|
| rteClientSecret      | RTE向ASUS Account Service 申請的 Client Secret      |
| maeIosRedirectUri   | MAE呼叫ASUS Account Service 指定的 IOS 版 redirect_uri |
| maeIosClientId      | MAE向ASUS Account Service 申請的 IOS 版 Client ID      |
| maeIosClientIdVersion      | MAE向ASUS Account Service 申請的 IOS 版 Client ID Version|
| maeIosClientSecret      | MAE向ASUS Account Service 申請的 IOS 版 Client Secret |
| maeAndroidRedirectUri   | MAE呼叫ASUS Account Service 指定的 Android 版 redirect_uri |
| maeAndroidClientId      | MAE向ASUS Account Service 申請的 Android 版 Client ID |
| maeAndroidClientIdVersion      | MAE向ASUS Account Service 申請的 Android 版 Client ID Version|
| maeAndroidClientSecret      | MAE向ASUS Account Service 申請的 Android 版 Client Secret |
| asusAccountServiceLoginUrl      | ASUS Account Service Login Page URL|
| asusAccountServiceLogoutUrl      | ASUS Account Service Logout API URL |
| asusAccountServiceAccessTokenUrl      | ASUS Account Service Get/Refresh Access Token API URL |
| asusAccountServiceUserInfoUrl      | ASUS Account Service Get User Info API URL |
| asusAccountServiceWFBMemberListUrl      | ASUS Account Service Get WFB MemberList API URL |
| projectId      | 雲端寶盒-系統代號 |
| companyId      | 雲端寶盒-範本組織代號 |
| adminGroupNo      | 雲端寶盒系統-權限管理者角色代號 |
| userGroupNo      | 雲端寶盒系統-權限使用者角色代號 |
| orgPlanNo      | 雲端寶盒系統-權限組織編制計畫代號 |
| maintainWorkerCount      | 同時可執行維護動作的執行緒數量，請填入比0大的數字 |
| whiteList      | 信任的IP來源，可接受多組位置以,連接在一起。如: 192.168.1.1,192.168.22.11 |
| newDBFilePath      | 新增的企業組織資料庫檔案資料夾路徑 |
| newDBFileInitSize      | 新增的企業組織資料庫檔案初始化大小，單位為MB。範例: 1024 |
| newDBFileGrowthSize      | 新增的企業組織資料庫檔案自動成長大小，單位為MB。範例: 10 |
| newDBFileMaxSize      | 新增的企業組織資料庫檔案限制大小，單位為MB。範例: 10240 |
| newDBLogPath      | 新增的企業組織資料庫交易紀錄檔資料夾路徑 |
| newDBLogInitSize      | 新增的企業組織資料庫交易紀錄檔初始化大小，單位為MB。範例: 1024 |
| newDBLogGrowthSize      | 新增的企業組織資料庫交易紀錄檔自動成長大小，單位為MB。範例: 10 |
| newDBLogMaxSize      | 新增的企業組織資料庫交易紀錄檔限制大小，單位為MB。範例: 10240 |
| newDBBackupPath      | 新增的企業組織資料庫備份檔案路徑 |
| newDBFullBackupType      | 新增的企業組織資料庫備份方式，1.僅初始系統後完整備份一次，後續由差異備份定時執行 / 2.週期性備份(覆蓋原完整備份檔案) |
| newDBFullBackupCircle      | 備份週期當備份類型=2時有效，以每週為單位，填入數字，表示週數(幾週執行一次完整備份並覆蓋原完整備份檔案) |
| newDBFullBackupDay      | 備份週期當備份類型=2時有效，當備份類型=2時有效，表示週幾進行備份，1.週一 / 2.週二 / 3.週三 / 4.週四 / 5.週五 / 6.週六 / 7.週日 |
| newDBFullBackupStartTime      | 當備份類型=2時有效，完整備份的開始時間，格式為 hhmmss |
| newDBDiffBackupCircle  | 填入數字，表示每隔多少小時進行差異備份 |
| newDBDiffBackupStartTimeOnFullBackupDay | 當備份類型=2時有效，表示完整備份日的差異備份起始時間，格式為 hhmmss |

### <div id="dbbackup">資料庫備份維護排程</div>
* 僅透過企業組織資料維護所產生的資料庫才會自動套用此項功能
* 執行限制條件 : 
    * SQL Server 必須啟用 Agent XPs 伺服器組態選項
    * 修改參數僅影響後續新建立的資料庫，已建立的資料庫請由人工手動修改
* 採循環備份機制 : 依據參數newDBFullBackupType來決定備份機制，共有以下兩種
    * 1.僅初始系統後完整備份一次，後續由差異備份定時執行 : 僅建立差異備份排程，一直附加到資料庫備份檔案中。
        * 差異備份會以附加方式加入到備份檔案
            *  每日從 00:00 - 11:59 執行，依據以下參數建立
                * newDBDiffBackupCircle : 以小時為單位，表示幾小時執行一次 
                * 資料庫備份排程名稱為【資料庫名稱_Diff_Backup】
    * 2.週期性備份 : 會自動產生完整備份以及差異備份排程
        * 完整備份排程執行時會覆蓋原本的備份檔案。
            * 依據下列參數建立 :
                * newDBBackupPath : 指定備份檔案路徑
                * newDBFullBackupCircle : 以週為單位，表示幾週執行一次
                * newDBFullBackupDay : 指定星期幾為完整備份日
                * newDBFullBackupStartTime : 指定完整備份日的開始時間
                * 資料庫備份排程名稱為【資料庫名稱_Diff_Backup】
        * 差異備份共有兩個，各自會以附加方式加入到備份檔案
            * 非完整備份日 : 從 00:00 - 11:59 執行， 依據以下參數建立
                * newDBFullBackupDay : 一週當中除了這一天，都會執行差異備份
                * newDBDiffBackupCircle : 以小時為單位，表示幾小時執行一次
                * 資料庫備份排程名稱為【資料庫名稱_Diff_Backup】
            * 完整備份日 : 依據以下參數建立
                * newDBDiffBackupStartTimeOnFullBackupDay : 差異備份執行的開始時間，用來接續完整備份。
                * newDBDiffBackupCircle : 以小時為單位，表示幾小時執行一次
                * 資料庫備份排程名稱為【資料庫名稱_Diff_Backup_OnFullBackupDay】

[登入流程圖]:attachment/sd_login.png "登入流程圖"
[登出流程圖]:attachment/sd_logout.png "登出流程圖"
[首頁畫面修正]:attachment/sa_brainworkNew.png "首頁畫面修正"
[新增企業組織(Token)流程圖]:attachment/sd_addenterprise(Token).png "新增企業組織(Token)流程圖"
[新增企業組織(ServerToServer)流程圖]:attachment/sd_syncaccount(ServertoServer).png "新增企業組織(ServerToServer)流程圖"
[刪除企業組織流程圖]:attachment/sd_deleteenterprise.png "刪除企業組織流程圖"
[帳號資料同步(Token)流程圖]:attachment/sd_syncaccount(Token).png "帳號資料同步(Token)流程圖"
[帳號資料同步(ServerToServer)流程圖]:attachment/sd_syncaccount(ServertoServer).png "帳號資料同步(ServerToServer)流程圖"
[系統狀態查詢流程圖]:attachment/sd_service.png "系統狀態查詢流程圖"