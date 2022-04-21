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

### <div id="customer">客戶資料維護</div>
* 說明 : 提供給ASUS Account Service呼叫，用來進行客戶資料維護
    * 新增帳號
    * 修改帳號
    * 停用帳號
    * 啟用帳號
    * 刪除帳號
    * 刪除企業組織

### <div id="adduserflow">新增帳號 <path>(客戶資料維護)</div>
* 說明 : 提供給ASUS Account Service呼叫，用來新增帳號，若新增的帳號為企業的第一個帳號，則需額外建立企業資料以及組織資料庫。
* 限制 : 透過token取得WFB Info，type=admin 且 supportRuru=1
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance)
    * Body(JSON)
        * token_type : token的格式， type string
        * token : access token， type string
        * userid : 使用者帳號，僅英數字，不可重複， type string
        * user_name : 使用者名稱， type string
        * email : 使用者email，符合E-Mail格式、不重複， type string
        * group : 使用者角色，Admin / User， type string
        * enterpriceid : 企業代碼，長度限制20, 僅能英數字, 首字英文, 不重複， type string
        * action : 固定為new, type string
    * Example
        * https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance
        * {
            token_type : "BEARER",
            token : "1234567898asdasdasd",
            userid : "first",
            user_name : "王大明",
            email : "first@gmail.com",
            group : "Admin",
            enterpriseid : "123456789123456789",
            action : "new"
          }
* Response
    * Body (JSON)
        * { status : 狀態碼 }
        * 狀態碼清單
        | 狀態碼        | 代碼說明           |
        | ------------- |:-------------:|
        | 200      | 執行成功 |
        | 400      | 無效的ACCESS TOKEN      |
        | 1002      | 建立資料庫連線失敗      |
        | 1003      | 取得加密金鑰錯誤      |
        | 1004      | 建立組織資料庫失敗      |
        | 1005      | 複製權限資料失敗      |
        | 1006      | 新增帳號資料失敗      |
        | 1013      | WFB Info, type <> admin    |
        | 1014      | WFB Info, support ruRu <> 1|
* 新增帳號流程圖

    ![新增帳號流程圖]

### <div id="updateuserflow">修改帳號 <path>(客戶資料維護)</div>
* 說明 : 提供給ASUS Account Service呼叫，可用來修改以下帳號相關資訊
    * 使用者名稱
    * 電子郵件
    * 使用者角色
* 限制 : 透過token取得WFB Info，type=admin 且 supportRuru=1
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance)
    * Body(JSON)
        * token_type : token的格式， type string
        * token : access token， type string
        * userid : 使用者帳號，僅英數字，不可重複， type string
        * user_name : 使用者名稱， type string
        * email : 使用者email，符合E-Mail格式、不重複， type string
        * group : 使用者角色，Admin / User， type string
        * enterpriceid : 該使用者帳號的企業代碼， type string
        * action : 固定為update, type string
    * Example
        * https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance
        * {
            token_type : "BEARER",
            token : "1234567898asdasdasd",
            userid : "first",
            user_name : "王大明",
            email : "first@gmail.com",
            group : "Admin",
            enterpriseid : "123456789123456789",
            action : "update"
          }
* Response
    * Body (JSON)
        * { status : 狀態碼 }
        * 狀態碼清單
        | 狀態碼        | 代碼說明           |
        | ------------- |:-------------:|
        | 200      | 執行成功 |
        | 400      | 無效的ACCESS TOKEN      |
        | 1002      | 建立資料庫連線失敗      |
        | 1007      | 指定的企業不存在      |
        | 1008      | 指定的帳號不存在      |
        | 1009      | 修改帳號資料失敗      |
        | 1013      | WFB Info, type <> admin    |
        | 1014      | WFB Info, support ruRu <> 1|
* 修改帳號流程圖

    ![修改帳號流程圖]

### <div id="disableuserflow">停用帳號 <path>(客戶資料維護)</div>
* 說明 : 提供給ASUS Account Service呼叫，用來停用帳號，此動作僅讓帳號失效，但不刪除任何帳號相關資料。
* 限制 : 透過token取得WFB Info，type=admin 且 supportRuru=1
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance)
    * Body(JSON)
        * token_type : token的格式， type string
        * token : access token， type string
        * userid : 使用者帳號，僅英數字，不可重複， type string
        * enterpriceid : 該使用者帳號的企業代碼， type string
        * action : 固定為disable, type string
    * Example
        * https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance
        * {
            token_type : "BEARER",
            token : "1234567898asdasdasd",
            userid : "first",
            enterpriseid : "123456789123456789",
            action : "disable"
          }
* Response
    * Body (JSON)
        * { status : 狀態碼 }
        * 狀態碼清單
        | 狀態碼        | 代碼說明           |
        | ------------- |:-------------:|
        | 200      | 執行成功 |
        | 400      | 無效的ACCESS TOKEN      |
        | 1002      | 建立資料庫連線失敗      |
        | 1007      | 指定的企業不存在      |
        | 1008      | 指定的帳號不存在      |
        | 1011      | 停用帳號資料失敗      |
        | 1013      | WFB Info, type <> admin    |
        | 1014      | WFB Info, support ruRu <> 1|
* 停用帳號流程圖

    ![停用帳號流程圖]

### <div id="enableuserflow">啟用帳號 <path>(客戶資料維護)</div>
* 說明 : 提供給ASUS Account Service呼叫，用來啟用帳號，此動作僅讓帳號生效。
* 限制 : 透過token取得WFB Info，type=admin 且 supportRuru=1
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance)
    * Body(JSON)
        * token_type : token的格式， type string
        * token : access token， type string
        * userid : 使用者帳號，僅英數字，不可重複， type string
        * enterpriceid : 該使用者帳號的企業代碼， type string
        * action : 固定為enaable, type string
    * Example
        * https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance
        * {
            token_type : "BEARER",
            token : "1234567898asdasdasd",
            userid : "first",
            enterpriseid : "123456789123456789",
            action : "enaable"
          }
* Response
    * Body (JSON)
        * { status : 狀態碼 }
        * 狀態碼清單
        | 狀態碼        | 代碼說明           |
        | ------------- |:-------------:|
        | 200      | 執行成功 |
        | 400      | 無效的ACCESS TOKEN      |
        | 1002      | 建立資料庫連線失敗      |
        | 1007      | 指定的企業不存在      |
        | 1008      | 指定的帳號不存在      |
        | 1012      | 啟用帳號資料失敗      |
        | 1013      | WFB Info, type <> admin    |
        | 1014      | WFB Info, support ruRu <> 1|
* 啟用帳號流程圖

    ![啟用帳號流程圖]

### <div id="deleteuserflow">刪除帳號 <path>(客戶資料維護)</div>
* 說明 : 提供給ASUS Account Service呼叫，用來刪除帳號，若刪除的帳號為企業最後一個帳號，則需連同企業資料以及組織資料庫一併刪除。
* 限制 : 透過token取得WFB Info，type=admin 且 supportRuru=1
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance)
    * Body(JSON)
        * token_type : token的格式， type string
        * token : access token， type string
        * userid : 使用者帳號，僅英數字，不可重複， type string
        * enterpriceid : 該使用者帳號的企業代碼， type string
        * action : 固定為delete, type string
    * Example
        * https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance
        * {
            token_type : "BEARER",
            token : "1234567898asdasdasd",
            userid : "first",
            enterpriseid : "123456789123456789",
            action : "delete"
          }
* Response
    * Body (JSON)
        * { status : 狀態碼 }
        * 狀態碼清單
        | 狀態碼        | 代碼說明           |
        | ------------- |:-------------:|
        | 200      | 執行成功 |
        | 400      | 無效的ACCESS TOKEN      |
        | 1002      | 建立資料庫連線失敗      |
        | 1007      | 指定的企業不存在      |
        | 1008      | 指定的帳號不存在      |
        | 1010      | 刪除帳號資料失敗      |
        | 1013      | WFB Info, type <> admin    |
        | 1014      | WFB Info, support ruRu <> 1|
* 刪除帳號流程圖

    ![刪除帳號流程圖]

### <div id="deleteenterpriseflow">刪除企業組織 <path>(客戶資料維護)</div>
* 說明 : 提供給ASUS Account Service呼叫，用來刪除企業組織，當呼叫此API時，會刪除該企業組織下所有企業資料、帳號資料以及組織資料庫。
* 限制 : 透過token取得WFB Info，type=admin 且 supportRuru=1
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance)
    * Body(JSON)
        * token_type : token的格式， type string
        * token : access token， type string
        * enterpriceid : 該使用者帳號的企業代碼， type string
        * action : 固定為delete_enterprise, type string
    * Example
        * https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance
        * {
            token_type : "BEARER",
            token : "1234567898asdasdasd",
            enterpriseid : "123456789123456789",
            action : "delete_enterprise"
          }
* Response
    * Body (JSON)
        * { status : 狀態碼 }
        * 狀態碼清單
        | 狀態碼        | 代碼說明           |
        | ------------- |:-------------:|
        | 200      | 執行成功 |
        | 400      | 無效的ACCESS TOKEN      |
        | 1002      | 建立資料庫連線失敗      |
        | 1007      | 指定的企業不存在      |
        | 1015      | 刪除企業資料失敗      |
        | 1013      | WFB Info, type <> admin    |
        | 1014      | WFB Info, support ruRu <> 1|
* 刪除企業組織流程圖

    ![刪除企業組織流程圖]

### <div id="service">系統狀態查詢</div>
* 說明 : 提供給ASUS Account Service呼叫，用來確認AP Server是否可正常連線
* 限制 : 透過token取得WFB Info，type=admin 且 supportRuru=1
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/ServiceStatus)
    * Body(JSON)
        * token_type : token的格式； type string
        * token : access token； type string
    * Example
        * https:// {{ RTE Host }} /ArcareEng/ServiceStatus
        * {
            token_type : "BEARER",
            token : "1234567898asdasdasd"
          }
* Response
    * Body (JSON)
        * { status : 狀態碼 }
        * 狀態碼清單
        | 狀態碼        | 代碼說明           |
        | ------------- |:-------------:|
        | 200      | 執行成功 |
        | 400      | 無效的ACCESS TOKEN      |
        | 1002      | 建立資料庫連線失敗      |
        | 1013      | WFB Info, type <> admin    |
        | 1014      | WFB Info, support ruRu <> 1|
* 系統狀態查詢流程圖

    ![系統狀態查詢流程圖]

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
        deviceName : (String)手機裝置名稱,
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
        error : (String)錯誤訊息,
        isactive : (Boolean)該使用者所屬的雲端寶盒組織資料庫初始化完成否
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
        deviceType : (Integer)裝置類型 1.ios / 2.android
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
        deviceType : (Integer)裝置類型 1.ios / 2.android
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
* 說明 : 提供給MAE APP呼叫，用來重新取得華碩access token。
* 限制 : 無
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetInitStatus)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},						
        languageId : (String)語系,						
        enterpriseNo : (String)企業代碼
    }
```
* Response
    * Body (JSON)
```Json
    {							
        result : (boolean)執行結果,
    }
```

### <div id="brainworknew">首頁畫面修正</div>
* 如下圖所示為首頁畫面須修正的部分

    ![首頁畫面修正]

### <div id="asusconfig">RTE華碩雲端寶盒系統設定檔案說明</div>
* 設定檔案路徑 : {Tomcat Path}\conf\asus.properties
* 參數清單
| 參數名稱        | 參數說明           |
| ------------- |:-------------:|
| rteClientId      | RTE向ASUS Account Service 申請的 Client ID |
| rteClientSecret      | RTE向ASUS Account Service 申請的 Client Secret      |
| maeIosClientId      | MAE向ASUS Account Service 申請的 IOS 版 Client ID      |
| maeIosClientSecret      | MAE向ASUS Account Service 申請的 IOS 版 Client Secret |
| maeAndroidClientId      | MAE向ASUS Account Service 申請的 Android 版 Client ID |
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
| defaultPassword      | 雲端寶盒系統-新增帳號預設密碼(僅預設值存到資料庫，實際登入密碼由ASUS Account Service管理) |

* 注意事項 : 需在RTE引擎啟動前將此設定檔案填寫完畢並放到{Tomcat Path}\conf，否則當RTE引擎啟動時，讀不到此設定檔案會將服務停止。

[登入流程圖]:attachment/sd_login.png "登入流程圖"
[登出流程圖]:attachment/sd_logout.png "登出流程圖"
[新增帳號流程圖]:attachment/sd_adduser.png "新增帳號流程圖"
[修改帳號流程圖]:attachment/sd_updateuser.png "修改帳號流程圖"
[刪除帳號流程圖]:attachment/sd_deleteuser.png "刪除帳號流程圖"
[停用帳號流程圖]:attachment/sd_disableuser.png "停用帳號流程圖"
[啟用帳號流程圖]:attachment/sd_enableuser.png "啟用帳號流程圖"
[刪除企業組織流程圖]:attachment/sd_deleteenterprise.png "刪除企業組織流程圖"
[系統狀態查詢流程圖]:attachment/sd_service.png "系統狀態查詢流程圖"
[首頁畫面修正]:attachment/sa_brainworkNew.png "首頁畫面修正"
