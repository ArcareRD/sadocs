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

[登入流程圖]:attachment/sd_login.png "登入流程圖"
[登出流程圖]:attachment/sd_logout.png "登出流程圖"
[首頁畫面修正]:attachment/sa_brainworkNew.png "首頁畫面修正"
