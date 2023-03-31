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
        clientVersion : (String)MAE APP版本
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
        account : (String)使用者帳號,
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
### <div id="appchangesystem">MAE切換系統</div>
* 說明 : 提供給MAE APP呼叫，用來切換系統。
* 限制 : 無
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppChangeSystem)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},
        onlineId : (String)上線唯一號,
        nowProjectId : (String)要登出的專案代號,
        projectId : (String)登入專案代號 ,	
        companyId : (String)登入分公司代號,						
        languageId : (String)語系,
        clientVersion : (String)MAE APP版本						
    }						
```
* Response
    * Body (JSON)
```Json
    {							
        result : (boolean)執行結果,						
        error : (String)錯誤訊息,
    #回傳資訊_start								
        projectVersion : (String)專案版本,						
        userNo : (String)使用者代號,						
        userAccessRoleType : (String)是否為系統管理員(1.是 2.否),						
        userAccessType : (String)是否為最高權限否(1.是 2.否),						
        userMail : (String)登入人員聯絡信箱,						
        menu : (JSONArray)選單						
            [					
                {				
                    id : (String)節點代號,			
                    fid : (String)父節點代號,			
                    name : (String)名稱,
                    objGns : (String)流程表單OBJECTID,
                    rightCount : (int)表單數量,
                    count : (int)子節點數量,
                    newyn : (String)新增的節點 (1.是 / 2.否),		
                    rightNodes : 表單清單
                        [
                            [null, (String)表單OBJECTID, (String)表單名, (String)Hint, (String)新增的表單(1.是/2.否), (String)表單成品料號]
                        ]				
                }, …				
            ],
        sysAndUtcTimeDiff_Corp : (long)格林威治與分公司的時間差(分),
        sysAndUtcTimeDiff_GLC : (long)格林威治與總公司的時間差(分),
        bwId : (String)BWID (註.執行內鍵，須傳入),
        autoCompleteCnt : (int)下拉元件的自動完成查詢筆數,						
        currencyMapping : (JSONObject)貨幣對照表 { 貨幣代號 : 貨幣符號 }  ex.{HKD: "$", TWD: "$", EUR: "€", MYR: "RM", USD: "$", …},
        defaultCurrencyId : (String)預設貨幣代號,
        prototypingCount : (int)打樣記錄上限筆數,
        multiSystem : (JSONObject)Server端現在系統日期時間
            {							
  				sysDateTime_UTC : (String)格林威治日期時間 (格式:yyyy/MM/dd HH:mm:ss.SSS)						
  				sysDateTime : (String)日期時間 (格式:yyyy/MM/dd HH:mm:ss.SSS)						
  			}
        expires : (Int) : APP從背景回到前景未動作需重新登入的時間限制，單位為分鐘
    #回傳資訊_end
        upgrade : (Boolean) : 是否正在更新維護中
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
        deviceType : (Integer)裝置類型 1.ios / 2.android,
        deviceName : (String)手機裝置名稱(提供給華碩API參數.x-asc-device-name),
        deviceModel : (String)裝置作業系統版本,(提供給華碩API參數.x-asc-device-model)
        clientVersion : (String)MAE APP版本
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
        deviceModel : (String)裝置作業系統版本,(提供給華碩API參數.x-asc-device-model),
        clientVersion : (String)MAE APP版本
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
        deviceModel : (String)裝置作業系統版本,(提供給華碩API參數.x-asc-device-model),
        clientVersion : (String)MAE APP版本
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
        commercialId : (Long)組織編號,
        clientVersion : (String)MAE APP版本
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

### <div id="appdeletetempdata">MAE 刪除資料表的暫存資料</div>
* 說明 : 提供給MAE APP呼叫，用來刪除資料表的暫存資料。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppDeleteTempData)
    * Body(JSON)
```Json
    {	
        csrf : (String)cookie[csrf],
        projectId : (String)專案代號 ,
        companyId : (String)分公司代號,
        languageId : (String)登入語系,
        srlid : (String)執行唯一號,
        clientVersion : (String)MAE APP版本
    }	
```
* Response
    * Body (JSON)
```Json
    {	
        result : (boolean)執行結果,
        error : (String)錯誤訊息,
        upgrade : (Boolean) : 是否正在更新維護中
    }	
```

### <div id="appgps">MAE GPS相關</div>
* 說明 : 提供給MAE APP呼叫，用來執行與GPS相關的功能。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGPS)
    * Body(JSON)
```Json
    {								
        csrf : (String)cookie[csrf],							
        projectId : (String)專案代號 ,							
        companyId : (String)分公司代號,							
        languageId : (String)登入語系,							
        bpsId : (String)BPS唯一號,							
        method : (String)查詢類型(getMapsDistance1:差異距離運算_直徑 / getMapsDistance2:差異距離運算_行徑 /  transMapsPosition:位置轉換)							
    #if method = getMapsDistance1								
        getMapsDistance1 : (JSONObject) 差異距離運算_直徑							
            {						
                orgin : (String) 起點					
                destination : (String) 終點					
                unitType : (int) 回傳單位 (1.公尺 / 2.公里 / 3.英里)					
                positionType : (int) 地址類別(1.經緯度 / 2.地址) ex.經緯度 = 25°3'55.31"N 121°31'32.65"E
            }						
    #endif								
    #if method = getMapsDistance2								
        getMapsDistance2 : (JSONObject) 差異距離運算_行徑 (若有多條路線，取最短的那條路線)							
            {						
                orgin : (String) 起點					
                destination : (String) 終點					
                travelMode : (int) 交通工具 (1.行走 / 2.開車)					
                unitType : (int) 回傳單位 (1.公尺 / 2.公里 / 3.英里)					
                positionType : (int) 地址類別(1.經緯度 / 2.地址) ex.經緯度 = 25°3'55.31"N 121°31'32.65"E
            }						
    #endif								
    #if method = transMapsPosition								
        transMapsPosition : (JSONObject) 位置轉換							
            {						
                position : (文字) 位置					
                positionType1 : (數字) 轉換前類別 (1.經緯度 / 2.地址)					
                positionType2 : (數字) 轉換後類別 (1.經緯度 / 2.地址)					
            }						
    #endif	
        clientVersion : (String)MAE APP版本							
    }	
```
* Response
    * Body (JSON)
```Json
    {								
        result : (boolean)執行結果,							
        error : (String)錯誤訊息							
    #if method = getMapsDistance1								
        value : (數字) 差異距離(四捨五入至小數一位)							
    #endif								
    #if method = getMapsDistance2								
        value : (數字) 差異距離(四捨五入至小數一位)							
    #endif								
    #if method = transMapsPosition								
        value : (字串) 轉換後結果							
    #endif	
        upgrade : (Boolean) : 是否正在更新維護中							
    }	
```

### <div id="apprunfunckeyitem">MAE 執行按鍵</div>
* 說明 : 提供給MAE APP呼叫，用來執行按鍵功能。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppRunFunckeyItem)
    * Body(JSON)
```Json
    {					
        csrf : (String)cookie[csrf],				
        projectId : (String)專案代號 ,				
        companyId : (String)分公司代號,				
        languageId : (String)登入語系,				
        bpsId : (String)BPS唯一號  (#7543)				
        formNo : (String)表單成品料號,				
        funckeyNo : (String)功能鍵料號,				
        funckeyItem : (int)DKS優先序				
        srlid : (String)執行唯一號				
        lockHandle : (long)Lock Handle (預留，不須傳入)				
        bwId : (String)BWID				
        refer : (JSONObject)引用到的資訊				
            {			
                formParam : (JSONArray)有引用到的表單傳入參數 [{ key:(String)參數名, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]		
                alias : (JSONArray)有引用到的檔區資料 [ { alias : (String)DKS檔區, fieldvalue : {欄位名 : 欄位值1, …} }, … ]		
                globalVar : (JSONArray)全域變數(全部) [{ key:(String)全域變數料號, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]		
                ctrl : (JSONArray)有引用到的元件資料(元件若有套用模板則提供套用模板後的資料)  [{ mtid:(String)元件料號, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林/5.字串陣列), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]  (#7724)		
            },
        clientVersion : (String)MAE APP版本			
    }
```
* Response
    * Body (JSON)
```Json
    {					
        result : (boolean)執行結果,				
        error : (String)錯誤訊息				
        globalVar : (JSONArray)有異動的全域變數				
            [			
                {		
                    status : (String)狀態(A.新增/U.修改/D.刪除), 	
                    key : (String)全域變數料號, 	
                    valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林)	
                    value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS)	
                }, …		
            ]			
    #if 行為選項=H.外部執行 且 過濾來源=執行程式 (#7916 擴充)
        value : (JSONObject) 資料				
            {			
                apiResult : (boolean) API的執行結果		
            }			
                        
        註.APP 須提供以下函數.取得API的執行結果。讓設計者可於下一個內鍵判斷。				
            [函數] FunctionApi_IsSuccess			
            [傳入] 無			
            [回傳] (boolean) API的執行結果			
    #endif			
            upgrade : (Boolean) : 是否正在更新維護中		
    }
```

### <div id="appgetfilecontainerdata">MAE 嵌入物件_檔案容器控制_讀取資料</div>
* 說明 : 提供給MAE APP呼叫，用來執行嵌入物件檔案容器控制的讀取資料。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetFileContainerData)
    * Body(JSON)
```Json
    {									
        csrf : (String)cookie[csrf],								
        projectId : (String)專案代號 ,								
        companyId : (String)分公司代號,								
        languageId : (String)登入語系,								
        bpsId : (String)BPS唯一號								
        formNo : (String)表單成品料號,								
        queryId : (String)查詢結構ID								
        fileIdFieldNm : (String) 檔案唯一號欄位名								
        maxCount : (int) 最大筆數 (0 : 無限制)								
        fieldId : (String) (可空白)檔案唯一號 (當有設定時，只會回傳該筆資料)								
        refer : (JSONObject)引用到的資訊								
            {							
                formParam : (JSONArray)有引用到的表單傳入參數 [{ key:(String)參數名, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]						
                alias : (JSONArray)有引用到的檔區資料 [ { alias : (String)DKS檔區, fieldvalue : {欄位名 : 欄位值1, …} }, … ]						
                globalVar : (JSONArray)全域變數(全部) [{ key:(String)全域變數料號, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]						
            },
        clientVersion : (String)MAE APP版本							
    }	
```
* Response
    * Body (JSON)
```Json
    {									
        result : (boolean)執行結果,								
        error : (String)錯誤訊息								
        fieldStruct : (JSONArray)欄位結構								
            [							
                { 						
                    field : (String)欄位名					
                    type : (String)組裝欄位型態					
                    length : (int)長度					
                    afterDot : (int)小數位					
                    encryptType : (String)1.密碼 / 2.個資加密 (當有加密時，才會給)					
                    pdpDecrypt : (boolean)個資解密 (當為個資料密，才會給)					
                },…						
                註.會多回傳下列欄位:						
                    M_FILEPATH : 檔案所在位置					
                    M_FILENAME : 檔名					
                    M_UPLOADDATE : 上傳日期時間					
                    M_LASTUPDATEDATE : 最後異動日期時間					
                    M_PHOTOTAKEDATE : 照片拍攝日期時間					
                    M_PHOTOPOSITION : 照片GPS位置					
            ]							
        count : (long)總筆數 (固定回傳-1)								
        record: (JSONArray)記錄  註.欄位值的順序以欄位結構的順序 / 二進位欄位永遠給NULL /  (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS)								
            [							
                {						
                    recNo : (long)位居第n筆 (固定回傳-1)					
                    value : (JSONArray)欄位值 [欄位值1, …]  註.欄位值的順序以欄位結構的順序 / 二進位欄位永遠給空字串 /  (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS)					
                }						
            ],
        upgrade : (Boolean) : 是否正在更新維護中
    }
```

### <div id="appsavefilecontainerdata">MAE 嵌入物件_檔案容器控制_儲存資料</div>
* 說明 : 提供給MAE APP呼叫，用來執行嵌入物件檔案容器控制的儲存。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppSaveFileContainerData)
    * Body(JSON)
```Json
    {			
        csrf : (String)cookie[csrf],		
        projectId : (String)專案代號 ,		
        companyId : (String)分公司代號,		
        languageId : (String)登入語系,		
        bpsId : (String)BPS唯一號		
        formNo : (String)表單成品料號,		
        srlid : (String)執行唯一號		
        lockHandle : (long)Lock Handle (預留，不須傳入)		
        bwId : (String)BWID		
        queryId : (String)查詢結構ID		
        fileIdFieldNm : (String) 檔案唯一號欄位名		
        tblType : (int) 表格類型 (1.實體表格(正式) 2.實體表格(暫存))		
        updateData : (JSONArray) 異動檔案清單		
                [	
                {	
                type : (String) 異動類型(A:新增/D:刪除), 
            #if 異動類型=A.新增	
                file : (String)於Server檔案位置,
                otherField : (JSONArray)其它欄位 [ { fieldNm : (String)欄位名,  valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]
            #else if 異動類型=D.刪除	
                pkey : (JSONArray) PKEY資訊 [ { fieldNm : (String)欄位名, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)欄位值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, ... ]
            #endif	
                }, …	
            ]	
        deleteSrcFile : (boolean) 執行後是否刪除於Server的暫存檔案		
        refer : (JSONObject)引用到的資訊		
            {	
                formParam : (JSONArray)有引用到的表單傳入參數 [{ key:(String)參數名, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]
                alias : (JSONArray)有引用到的檔區資料 [ { alias : (String)DKS檔區, fieldvalue : {欄位名 : 欄位值1, …} }, … ]
                globalVar : (JSONArray)全域變數(全部) [{ key:(String)全域變數料號, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]
            },
        clientVersion : (String)MAE APP版本	
    }	
```
* Response
    * Body (JSON)
```Json
    {			
        result : (boolean)執行結果,		
        error : (String)錯誤訊息,
        upgrade : (Boolean) : 是否正在更新維護中		
    }	
```

### <div id="appgetfiletransfer">MAE 取得<檔案傳輸>的檔案</div>
* 說明 : 提供給MAE APP呼叫，用來取得<檔案傳輸>的檔案。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetFileTransfer)
    * Body(JSON)
```Json
    {										
        csrf : (String)cookie[csrf],									
        projectId : (String)專案代號 ,									
        companyId : (String)分公司代號,									
        languageId : (String)登入語系,									
        bpsId : (String)BPS唯一號,									
        formNo : (String)表單成品料號,									
        queryId : (String)查詢結構ID									
        method : (String)來源位置(database:資料庫 / fileCabinet:檔案櫃 / fileSystem:檔案系統)
    #if method = database										
        database : (JSONObject)資料庫									
            {								
                fileNmFieldNm : (String) 記錄<檔名>的欄位名							
                fileCttFieldNm : (String) 記錄<檔案內容>的欄位名							
            }								
    #else if method = fileCabinet										
        fileCabinet : (JSONObject)檔案櫃									
            {								
                fileNmFieldNm : (String) 記錄<檔名>的欄位名							
                fileCabinetFieldNm : (String) 記錄<檔案櫃料號>的欄位名							
            }								
    #else if method = fileSystem										
        fileSystem : (JSONObject)檔案系統									
            {								
                fileIdFieldNm : (String) 記錄<檔案唯一號>的欄位名							
            }								
    #endif										
        refer : (JSONObject)引用到的資訊									
            {								
                formParam : (JSONArray)有引用到的表單傳入參數 [{ key:(String)參數名, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]							
                alias : (JSONArray)有引用到的檔區資料 [ { alias : (String)DKS檔區, fieldvalue : {欄位名 : 欄位值1, …} }, … ]							
                globalVar : (JSONArray)全域變數(全部) [{ key:(String)全域變數料號, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]							
            },
        clientVersion : (String)MAE APP版本								
    }		
```
* Response
    * Body (JSON)
```Json
    {										
        result : (boolean)執行結果,									
        error : (String)錯誤訊息									
        filePath : (JSONArray) 多個檔案所在位置,
        upgrade : (Boolean) : 是否正在更新維護中									
    }										
```

### <div id="appgetform">MAE 取得表單資訊</div>
* 說明 : 提供給MAE APP呼叫，用來取得表單資訊。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetForm)
    * Body(JSON)
```Json
    {											
        csrf : (String)cookie[csrf],										
        projectId : (String)專案代號 ,										
        companyId : (String)分公司代號,										
        languageId : (String)登入語系,										
        bpsId : (String)BPS唯一號  (#7543)										
        formNo : (String)表單成品料號,										
        makeVer : (String)目前App Cache的表單噴碼版本 (可不帶),
        clientVersion : (String)MAE APP版本										
    }	
```
* Response
    * Body (JSON)
```Json
    {											
        result : (boolean)執行結果,										
        error : (String)錯誤訊息										
        update : (boolean)是否有新版本,										
        defaultLanguageId : (int) 所屬專案的預設語系 (當表單不存在<登入語系>時，使用<預設語系>開啟表單)										
        makeVer : (String)表單噴碼版本 (當bUpdate = true時，才會有), 										
        formData : (String)表單JSON資料 (當bUpdate = true時，才會有), 										
        funcData : (JSONArray)按鍵JSON資料 [(String)按鍵1,…]  (當bUpdate = true時，才會有), 										
        componentData : (JSONArray)元件JSON資料 [(String)元件1,…]  (當bUpdate = true時，才會有), 										
        alias : (JSONArray)檔區資訊 (當bUpdate = true時，才會有), 										
            [									
                {								
                    alias : (String)DKS的檔區名,							
                    parentAlias : (String)父檔區DKS的檔區名  (當有父檔區時，才會有),							
                    relation : (JSONArray)與父檔區的關聯  [ [ 欄位名,  父檔區欄位名 ], … ]  (當有父檔區時，才會有),							
                    sort : (String)排序  ex.PDNO DESC, INDATE							
                    fieldStruct : [							
                        { 						
                            field : (String)欄位名					
                            type : (String)組裝欄位型態					
                            length : (int)長度					
                            afterDot : (int)小數位					
                            encryptType : (String)1.密碼 / 2.個資加密 (當有加密時，才會給)					
                            pdpDecrypt : (boolean)個資解密 (當為個資料密，才會給)					
                        },…						
                    ]							
                }								
            ]									
        funcLimit : (JSONArray) 沒有執行權限的功能鍵清單 [ 功能鍵料號, … ]										
        componentLimit : (JSONArray) 受保護的元件清單 [ 元件料號, … ]										
        picture : (JSONObject)模版資料										
            {									
                模版料號 : {								
                    text: (JSONObject)文字 {							
                        format : (String)特殊格式						
                        upCase : (boolean)限定大寫						
                        fill: (String)填滿符號   ex.XXXX=>AB**						
                    },							
                    number : (JSONObject)數值 {							
                        db: (int)小數位						
                        tp: (boolean)千分位						
                        percent: (boolean)百分比						
                        symbol: (boolean)貨幣符號						
                        fill: (String)填滿符號						
                        trans: (String)金額轉換(1.國字金額 / 2.英文金額)						
                    },							
                    date : (JSONObject)日期 {							
                        year : (String)年度 (1.西元年/2.民國年)						
                        month: (String)月份 (1.英文⽉份 /2.數字月份)						
                        dateFormat : (String)日期格式 (1.年月日 / 2.月日年 / 3.日月年 / 4.年月 / 5.月年 / 6.月日 / 7.日月)						
                        dateSeparate : (String)分隔符號 (1.斜線(/) / 2.減號(-) / 3.點(.))						
                        time : (String)時間 (1.12時制 / 2.24時制)						
                        timeFormat : (String)時間格式 (1.HH:MM / 2.HH:MM:SS)						
                    },							
                    time : (JSONObject)時間 {							
                        time : (String)時間 (1.12時制 / 2.24時制)						
                        timeFormat : (String)時間格式 (1.HH:MM / 2.HH:MM:SS)						
                    },							
                    mask : (JSONObject)遮罩 {							
                        替換字元 : [						
                            { 					
                                start : (int)起始位置				
                                end : (int)終止位置				
                            }, …					
                        ]						
                    }							
                }, …								
            },
        upgrade : (Boolean) : 是否正在更新維護中								
    }	
```

### <div id="appgetformdsdata">MAE 查詢表單資料來源資料</div>
* 說明 : 提供給MAE APP呼叫，用來查詢表單資料來源資料。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetFormDSData)
    * Body(JSON)
```Json
    {														
        csrf : (String)cookie[csrf],													
        projectId : (String)專案代號 ,													
        companyId : (String)分公司代號,													
        languageId : (String)登入語系,													
        bpsId : (String)BPS唯一號  (#7543)													
        formNo : (String)表單成品料號,													
        alias : (String)DKS檔區,													
        sort : (String)排序欄位(可不傳，不傳時依原設定) (ex. FLD1, FLD2 DESC, FLD3) 													
        relation : (JSONObject)關聯欄位值 (沒有父檔區時，不須傳入)													
            {												
                父階欄位名 : 父階欄位值   (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS),											
                …											
            }												
        filterId : (String) 資料過濾結構ID (可不傳)													
        preForm : (JSONObject) 前單傳入資訊 (可不傳)													
            {												
                formNo : (String)前單的表單成品料號,											
                filterId : (String)前單傳入過濾式的結構ID (可不傳),											
                focusId : (String)前單駐留過濾式的結構ID (可不傳)(只有開單第一次查詢可以傳) (且method須設為readTop),											
                refer : (JSONObject)引用到的資訊											
                    {										
                        formParam : (JSONArray)有引用到的前單表單傳入參數 [{ key:(String)參數名, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]									
                        alias : (JSONArray)有引用到的前單檔區資料 [ { alias : (String)DKS檔區, fieldvalue : {欄位名 : 欄位值1, …} }, … ]									
                    }										
            }												
        method : (String)查詢類型(readTop:從第一筆讀取 / readBottom:從最後一筆讀取) / read:從指定記錄讀取)													
        hyperlinkId : (String)超連結唯一號(可不傳),
    #if method = readTop														
        readTop : (JSONObject)從第一筆讀取													
            {												
                readCount : (int)讀取筆數											
                returnRecNo : (boolean)要回傳總筆數/位居第n筆											
            }												
    #else if method = readBottom														
        readBottom : (JSONObject)從最後一筆讀取													
            {												
                readCount : (int)讀取筆數											
                returnRecNo : (boolean)要回傳總筆數/位居第n筆											
            }												
    #else if method = read														
        read : (JSONObject)從指定記錄讀取													
            {												
                readCount : (int)讀取筆數											
                returnRecNo : (boolean)要回傳總筆數/位居第n筆											
                sortValue : (JSONArray)目前駐留記錄的排序欄位值  [欄位值1, 欄位值2, 欄位值3, ...] (註.順序要與strSort相同)											
                sortType : (int)讀取方向(0.往上查詢 / 1.往下查詢)											
                converType : (int)是否包含本筆 (0.不含本筆 / 1.包含本筆)											
            }												
    #endif														
        refer : (JSONObject)引用到的資訊													
            {												
                formParam : (JSONArray)有引用到的表單傳入參數 [{ key:(String)參數名, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]											
                alias : (JSONArray)有引用到的檔區資料 [ { alias : (String)DKS檔區, fieldvalue : {欄位名 : 欄位值1, …} }, … ]											
                globalVar : (JSONArray)全域變數(全部) [{ key:(String)全域變數料號, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]											
            },
        clientVersion : (String)MAE APP版本												
    }
```
* Response
    * Body (JSON)
```Json
#if method = ReadTop / ReadBottom / ReadPage															
	{														
		result : (boolean)執行結果,													
		error : (String)錯誤訊息													
		count : (long)總筆數													
		focusPos : (int)指定駐留記錄在回傳資料的第n筆 (當有設定preForm.focusId時，才會給)													
		record: (JSONArray)記錄  註.欄位值的順序以欄位結構的順序 / 二進位欄位永遠給NULL /  (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS)													
			[												
				{											
					recNo : (long)位居第n筆										
					value : (JSONArray)欄位值 [欄位值1, …]  註.欄位值的順序以欄位結構的順序 / 二進位欄位永遠給空字串 /  (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS)										
				}											
			],
        upgrade : (Boolean) : 是否正在更新維護中												
	}														
#endif
```

### <div id="appgetformquery">MAE 查詢資料</div>
* 說明 : 提供給MAE APP呼叫，用來查詢資料。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetFormQuery)
    * Body(JSON)
```Json
    {									
        csrf : (String)cookie[csrf],								
        projectId : (String)專案代號 ,								
        companyId : (String)分公司代號,								
        languageId : (String)登入語系,								
        bpsId : (String)BPS唯一號  (#7543)								
        formNo : (String)表單成品料號,								
        queryId : (String)查詢結構ID								
        extrQuery : (JSONObject) 額外查詢資訊 (只支援method=multiple:多筆) (可不傳)(#7724)								
            {							
                extrFilter : (JSONArray) 過濾 (可不傳)						
                    [					
                        {				
                            andOr : (int) 0.無 / 1.AND / 2.OR,			
                            bracketsLeft : (int) 左括號數,			
                            bracketsRight : (int) 右括號數,			
                            fieldNm : (String) 欄位名,			
                            operator : (int) 運算子 (1.大於 2.小於 3.等於 4.大於等於 5.小於等於 6.不等於 7.開頭是 8.結尾是 9.相似於),
                            valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), 			
                            value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) 			
                        }, …				
                    ]					
                extrGroupby : (JSONObject) Group by (可不傳)						
                    [					
                        {				
                            fieldNm : (String) 欄位名			
                        }, …				
                    ]					
                extrOutput : (JSONArray) 輸出欄位 (可不傳)						
                    [					
                        {				
                            fieldNm : (String) 輸出欄位名			
                            calcType : (int) 彙總類型(1.count(*))			
                        }, …				
                    ]					
                extrOrderby : (JSONArray) Order by (可不傳)						
                    [					
                        {				
                            fieldNm : (String) 欄位名			
                            sortType : (int) 排序方式 (1.升冪 / 2.降冪)			
                        }, …				
                    ]					
            }							
        method : (String)查詢類型(single:單筆 / multiple:多筆)								
    #if method = single									
        single : (JSONObject)單筆								
            {							
                returnFieldValue : (boolean)是否回傳欄位值						
            }							
    #else if method = multiple									
        multiple : (JSONObject)多筆								
            {							
                method : (String)查詢類型(readTop:從第一筆讀取 / read:從指定記錄讀取)						
                returnFieldStruct : (boolean)是否回傳欄位結構						
            #if method = readTop							
                readTop : (JSONObject)從第一筆讀取						
                    {					
                        readCount : (int)讀取筆數				
                        returnRecNo : (boolean)要回傳總筆數/位居第n筆				
                    }					
            #else if method = readPage							
                readPage : (JSONObject)從指定記錄讀取						
                    {					
                        readCount : (int)讀取筆數				
                        returnRecNo : (boolean)要回傳總筆數/位居第n筆				
                        sortValue : (JSONArray)目前駐留記錄的排序欄位值  [欄位值1, 欄位值2, 欄位值3, ...] (註.順序要與strSort相同)				
                        sortType : (int)讀取方向(0.往上查詢 / 1.往下查詢)				
                        converType : (int)是否包含本筆 (0.不含本筆 / 1.包含本筆)				
                    }					
            #endif							
            }							
    #endif									
        refer : (JSONObject)引用到的資訊								
            {							
                formParam : (JSONArray)有引用到的表單傳入參數 [{ key:(String)參數名, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]						
                alias : (JSONArray)有引用到的檔區資料 [ { alias : (String)DKS檔區, fieldvalue : {欄位名 : 欄位值1, …} }, … ]						
                globalVar : (JSONArray)全域變數(全部) [{ key:(String)全域變數料號, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]						
            },
        clientVersion : (String)MAE APP版本							
    }	
```
* Response
    * Body (JSON)
```Json
#if method = Single									
	{								
		result : (boolean)執行結果,							
		error : (String)錯誤訊息							
		find : (boolean)是否有找到符合的記錄							
	#if retunFieldValue = true								
		fieldStruct : (JSONArray)欄位結構							
			[						
				{ 					
					field : (String)欄位名				
					type : (String)組裝欄位型態				
					length : (int)長度				
					afterDot : (int)小數位				
					encryptType : (String)1.密碼 / 2.個資加密 (當有加密時，才會給)				
					pdpDecrypt : (boolean)個資解密 (當為個資料密，才會給)				
				},…					
			]						
		fieldValue : (JSONArray)欄位值 [ 欄位值1, … ] 註.欄位值的順序以欄位結構的順序 / 二進位欄位永遠給空字串 /  (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS)		
	#endif
        upgrade : (Boolean) : 是否正在更新維護中									
	}								
#elseif method = Multiple									
	{								
		result : (boolean)執行結果,							
		error : (String)錯誤訊息							
	#if returnFieldStruct = true								
		sort : (String)排序  ex.PDNO DESC, INDATE							
		fieldStruct : (JSONArray)欄位結構							
			[						
				{ 					
					field : (String)欄位名				
					type : (String)組裝欄位型態				
					length : (int)長度				
					afterDot : (int)小數位				
					encryptType : (String)1.密碼 / 2.個資加密 (當有加密時，才會給)				
					pdpDecrypt : (boolean)個資解密 (當為個資料密，才會給)				
				},…					
			]
	#endif								
		count : (long)總筆數							
		record: (JSONArray)記錄  註.欄位值的順序以欄位結構的順序 / 二進位欄位永遠給NULL /  (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS)							
			[						
				{					
					recNo : (long)位居第n筆				
					value : (JSONArray)欄位值 [欄位值1, …]  註.欄位值的順序以欄位結構的順序 / 二進位欄位永遠給空字串 /  (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS)				
				}					
			],
        upgrade : (Boolean) : 是否正在更新維護中						
	}								
#endif
```

### <div id="appgetimage">MAE 查詢圖示主檔資料</div>
* 說明 : 提供給MAE APP呼叫，用來查詢圖示主檔資料。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetImage)
    * Body(JSON)
```Json
    {		
        csrf : (String)cookie[csrf],	
        projectId : (String)專案代號 ,	
        languageId : (String)登入語系,	
        iconNo: (String)圖示料號,
        clientVersion : (String)MAE APP版本	
    }
```
* Response
    * Body
```Json
#if 沒錯誤		
	byte[]	
#else		
	{	
		error : (String)錯誤訊息,
        upgrade : (Boolean) : 是否正在更新維護中
	}	
#endif
```

### <div id="appdeviceregistered">MAE 設定主要裝置</div>
* 說明 : 提供給MAE APP呼叫，用來設定主要裝置。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppDeviceRegistered)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},						
        languageId : (String)語系,						
        userId : (long)使用者代號,						
        deviceId : (String)裝置代號,
        deviceName : (String)裝置名稱,
        clientVersion : (String)MAE APP版本
    }
```
* Response
    * Body(JSON)
```Json
    {							
        result : (boolean)執行結果,						
        error : (String)錯誤訊息,
        upgrade : (Boolean) : 是否正在更新維護中
    }
```

### <div id="appgethyperlinkdata">MAE 取得超連結資訊</div>
* 說明 : 提供給MAE APP呼叫，用來取得超連結資訊。
* 限制 : 無
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetHyperlinkData)
    * Body(JSON)
```Json
    {
        csrf : (String)cookie[csrf],
        deviceId : (String)手機MAC IMEI,
        deviceName : (String)手機裝置名稱,
        projectId : (String)專案代號,
        companyId : (String)分公司代號,
        languageId : (String)登入語系,
        srlid : (String)超連結唯一號,
        type : (String)類型(get:取得超連結資訊,returnSuccess:回報執行成功)(註.無傳入時，表示get),
        clientVersion : (String)MAE APP版本
    }
```
* Response
    * Body(JSON)
```Json
    {							
        result : (boolean)執行結果,
        error : (String)錯誤訊息,
    #if 傳入參數.type=get
        data : (JSONObject)資訊,
        {
                needLogin  : (boolean)需要驗證(若為true時,MAE須轉至登入頁面，要求使用者登入),
        #if needLogin=false                
                type : (String)類型(prototyping:打樣預覽,openForm:開啟表單,runFunckeyApi:呼叫開放按鍵),
            #if type=prototyping
                prototyping :
                {
                    prototypingType : (String)打樣類型(form:表單 / event:事件),
                #if prototypingType=form
                    prototypingMTID : (String)表單成品料號,
                #else prototypingType=event
                    prototypingMTID :  (String)事件料號,
                #endif
                #if 執行系統=自動登入 && 登入狀態=未登入
                    login : {
                        內容同【AppRuntimeLogin(登入)】回傳
                    },
                    註.因api會自動登入，所以關閉預覽時，MAE須執行【AppRuntimeLogout(登出)】
                #endif
                    loginSystem : {
                        內容同【AppChangeSystem(登入系統)】回傳
                    }
                }
            #else if type=openForm
                openForm : 
                {
                    formMTID : (String)表單成品料號,
                    formParam : (JSONArray)表單傳入參數 [{ key:(String)參數名, valueType : (String)值的型態(0.Null/1.字串/2.日期時間/3.數值/4.布林), value : (Object)值 (日期時間以字串表示，格式:yyyy/MM/dd HH:mm:ss.SSS) }, … ]	,
                #if 執行系統=自動登入 && 登入狀態=未登入
                    login : {
                        內容同【AppRuntimeLogin(登入)】回傳
                    },
                    註.因api會自動登入，所以關閉預覽時，MAE須執行【AppRuntimeLogout(登出)】
                #endif    
                    loginSystem : {
                        內容同【AppChangeSystem(登入系統)】回傳
                    }
                }
            #else if type=runFunckeyApi
                runFunckeyApi : 
                {
                    successMsg : (String)成功訊息(執行成功時，才會有此參數)
                }
            #endif
        #endif    
        }
    #endif
    }
```

### <div id="appgetpushmessagedata">MAE 取得推撥通知資料</div>
* 說明 : 提供給MAE APP呼叫，使用者在通知列點擊訊息時呼叫用，不登入可使用，僅驗證該訊息以及裝置是否歸屬同一個使用者，若是則回傳訊息資料。
* 限制 : 無
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetPushMessageData)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},						
        languageId : (String)語系,						
        messageId : 訊息ID,
        deviceId : 裝置代號,
        clientVersion : (String)MAE APP版本
    }
```
* Response
    * Body(JSON)
```Json
    {							
        result : (boolean)執行結果,						
        error : (String)錯誤訊息，result=false才有,
        message : result=true才有
            {
                exist : (boolean)訊息存在否,
                projName : (String)系統名稱,
                sender : (String)推播人,
                sendDate : (String)發送日期, 以 yyyy/MM/dd hh:mm:ss 格式,
                sendStatus : (boolean)發送狀態,
                readStatus : (boolean)讀取狀態,
                error : (String)發送失敗原因,
                title : (String)訊息主旨,
                content : (String)訊息內文,
                data : { 超連結相關資訊
                    messageid : 訊息代號,
                    linktype :　超連結類型 1.超連結表單/2.超連結按鍵/3.超連結Google行事曆/4.超連結網址,
                    srlid : 超連結唯一號,
                    url : 超連結網址 / google行事曆網址
                }
            }
    }
```

### <div id="appgetpushmessagedatalist">MAE 查詢推播通知紀錄資料清單</div>
* 說明 : 提供給MAE APP呼叫，用來查詢推播通知紀錄資料清單。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetPushMessageDataList)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},						
        languageId : (String)語系,						
        messages : [訊息ID陣列],
        clientVersion : (String)MAE APP版本
    }
```
* Response
    * Body(JSON)
```Json
    {							
        result : (boolean)執行結果,						
        error : (String)錯誤訊息，result=false才有,
        messages : result=true才有
            {
                訊息代號 : {
                    exsit : (boolean)訊息存在否,
                    projName : (String)系統名稱,
                    sender : (String)推播人,
                    sendDate : (String)發送日期, 以 yyyy/MM/dd hh:mm:ss 格式,
                    sendStatus : (boolean)發送狀態,
                    readStatus : (boolean)讀取狀態,
                    error : (String)發送失敗原因,
                    title : (String)訊息主旨,
                    content : (String)訊息內文,
                    data : { 超連結相關資訊
                        messageid : 訊息代號,
                        linktype :　超連結類型 1.超連結表單/2.超連結按鍵/3.超連結Google行事曆/4.超連結網址,
                        srlid : 超連結唯一號,
                        url : 超連結網址 / google行事曆網址
                    }
                }
            },
        upgrade : (Boolean) : 是否正在更新維護中
    }
```

### <div id="appgetpushmessageidlist">MAE 查詢推播通知紀錄代號清單</div>
* 說明 : 提供給MAE APP呼叫，用來查詢推播通知紀錄代號清單。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetPushMessageIdList)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},						
        languageId : (String)語系,						
        userId : (long)使用者代號,
        filter : 以下為查詢的過濾條件，若不需要過濾條件可不帶參數
            {
                startDate : (String)起始日期,請將日期以 yyyy/mm/dd 格式轉為字串(包含當天，引擎自動補上時間內容 00:00:00),
                endDate : (String)結束日期,請將日期以 yyyy/mm/dd 格式轉為字串(包含當天，引擎自動補上時間內容 23:59:59),
                sender : (String)推播人,
                projId : (String)發出推播通知的系統代號,
                sendStatus : (int) 發送狀態(-1=全部 / 0=失敗 / 1=成功),
                readStatus : (int) 讀取狀態(-1=全部 / 0=未讀 / 1=已讀)
            },
        clientVersion : (String)MAE APP版本
    }
```
* Response
    * Body(JSON)
```Json
    {							
        result : (boolean)執行結果,						
        error : (String)錯誤訊息，result=false才有,
        messages : result=true才有
            {
                ids : [訊息ID陣列],
                read : 已讀筆數,
                unread : 未讀筆數
            },
        upgrade : (Boolean) : 是否正在更新維護中
    }
```

### <div id="appgetpushmessagesenderlist">MAE 查詢推播通知紀錄所屬推播人清單</div>
* 說明 : 提供給MAE APP呼叫，用來查詢推播通知紀錄所屬推播人清單。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetPushMessageSenderList)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},						
        languageId : (String)語系,						
        userId : (long)使用者代號,
        clientVersion : (String)MAE APP版本
    }
```
* Response
    * Body(JSON)
```Json
    {							
        result : (boolean)執行結果,						
        error : (String)錯誤訊息，result=false才有,
        senders : result=true才有
            [
                推播人名稱, 
                ...
            ],
        upgrade : (Boolean) : 是否正在更新維護中
    }
```

### <div id="appgetpushmessagesystemlist">MAE 查詢推播通知紀錄所屬系統清單</div>
* 說明 : 提供給MAE APP呼叫，用來查詢推播通知紀錄所屬系統清單。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetPushMessageSystemList)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},						
        languageId : (String)語系,						
        userId : (long)使用者代號,
        clientVersion : (String)MAE APP版本
    }
```
* Response
    * Body(JSON)
```Json
    {							
        result : (boolean)執行結果,						
        error : (String)錯誤訊息，result=false才有,
        projects : result=true才有
            [{
                strProjectId : (String)系統代號,
                strProjectName : (String)系統名稱
            }],
        upgrade : (Boolean) : 是否正在更新維護中
    }
```

### <div id="appsetpushmessagelistreaded">MAE 設定推播通知清單已讀</div>
* 說明 : 提供給MAE APP呼叫，用來設定推播通知清單已讀。
* 限制 : 需在使用者已登入的狀態下執行
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppSetPushMessageListReaded)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},						
        userId : (long)使用者代號,
        languageId : (String)語系,						
        messages : [訊息ID陣列],
        clientVersion : (String)MAE APP版本
    }
```
* Response
    * Body(JSON)
```Json
    {							
        finish : (boolean)執行結果,						
        error : (String)錯誤訊息，result=false才有,
        upgrade : (Boolean) : 是否正在更新維護中
    }
```

### <div id="appgetcorpupgradestatus">MAE 取得企業組織更新狀態</div>
* 說明 : 提供給MAE APP呼叫，用來取得企業組織更新狀態。
* 限制 : 無
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppGetCorpUpgradeStatus)
    * Body(JSON)
```Json
    {							
        csrf : (String)cookie[csrf] ex.{AAAA1310-83C6-44A3-A6AF-3329F5B44EEE},						
        userId : (Long)使用者序號,
        clientVersion : (String)MAE APP版本
    }
```
* Response
    * Body(JSON)
```Json
    {							
        finish : (boolean)是否完成更新,						
        success : (boolean)api執行成功否,
        error : (String)錯誤訊息,當success=false時出現
    }
```

### <div id="apptestconnection">MAE 測試連線狀態</div>
* 說明 : 提供給MAE APP呼叫，用來測試連線狀態。
* 限制 : 無
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/AppTestConnection)
    * Body(JSON)
```Json
    {							
        clientVersion : (String)MAE APP版本
    }
```
* Response
    * Body(JSON)
```Json
    {							
        showApplyAccount : (boolean)是否啟用帳號申請,						
        version : (String)RTE版本
    }
```

### <div id="login">RTE登入</div>
* 說明 : 檢查是否已登入RTE系統，若尚未登入則檢查是否由ASUS WebStorage轉向而來，若不是則將頁面導向至未登入的畫面
* 限制 : 無
* Request : (HTTP GET; https:// {{ RTE Host }} /ArcareEng/login.jsp)
    * Parameter
        * code : type string，授權碼，由ASUS WebStorage轉向時傳入，RTE會使用此授權碼向ASUS WebStorage取得以下資訊
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
* 說明 : 執行RTE的登出以及呼叫ASUS WebStorage Logout API
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

### <div id="brainworknew">首頁畫面修正</div>
* 如下圖所示為首頁畫面須修正的部分

    ![首頁畫面修正]

### <div id="enterprise">企業組織資料維護</div>
* 說明 : 提供給ASUS WebStorage呼叫，用來進行企業組織資料維護
    * 新增企業組織
        * 功能說明 : 
            * 建立指定的企業組織資料庫
            * 呼叫ASUS WebStorage取得企業組織相關成員並自動新增帳號以及相關權限
            * 依據參數設定建立[資料庫備份維護計畫](README.md#dbbackup)
            * 建立資料庫備份檔案
    * 刪除企業組織
        * 功能說明 : 
            * 刪除指定的企業組織資料庫 / 該企業組織下所有成員帳號
            * 刪除已建立的[資料庫備份維護計畫](README.md#dbbackup)
            * 此處無法刪除資料庫備份檔案，檔案須由人工手動搬遷或刪除
    * 帳號資料同步
        * 功能說明 : 
            * 呼叫ASUS WebStorage取得企業組織相關成員帳號資料
                * 帳號存在於企業組織資料庫，依據資料進行更新帳號
                * 帳號不存在於企業組織資料庫，依據資料進行新增帳號
                * 企業組織資料庫有不存在於ASUS WebStorage的帳號，刪除帳號

* 備註 : 採非同步方式呼叫，API僅回傳已接收給ASUS WebStorage，背景執行資料維護的動作。

### <div id="addenterpriseflow">新增企業組織 <path>(企業組織資料維護)</div>
* 說明 : 採非同步方式提供給ASUS WebStorage呼叫，用來新增企業組織，並依據token取得管理員帳號資料新增至該企業組織，再將該管理員下的memberlist作為使用者帳號加入企業組織。
* 支援以下兩種模式
    * 使用Token呼叫
    * Server to Server呼叫

### <div id="addenterprisetokenflow">Token認證 <path>(企業組織資料維護/新增企業組織)</div>
* 限制 : 透過token向ASUS WebStorage取得User Info，User Info內的type=admin 且 supportRuru=1
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance)
    * Content-Type： application/x-www-form-urlencoded
    * Body(encoded body)
        * token_type : token的格式， type string
        * token : access token， type string
        * action : 固定字串 new， type string
        * notifyUrl : 回報執行結果的URL， type string
            * 回傳參數依據 [ASUS Cloud API](https://docs.google.com/document/d/141kCcJeACvJSJC542driaCFVAkcqiEHcFNdlS8xGgO4/edit#heading=h.bnzrgv614wt)
    * Example
        * URL : https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance
        * Body : token_type=BEARER&token=1234567898asdasdasd&action=new&notifyUrl=https%3A%2F%2Ftest.asuswebstorage.com%2F


* Response
    * Body (JSON)
        * { receive : 接收request成功否, errorCode : 錯誤代碼(當receive=false時產生) }

* 新增企業組織(Token)流程圖

    ![新增企業組織(Token)流程圖]

### <div id="addenterpriseserverflow">Server to server <path>(企業組織資料維護/新增企業組織)</div>
* 限制 : 呼叫端的IP須在信任的IP清單中
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/ServerMaintenance)
    * Content-Type： application/x-www-form-urlencoded
    * Body(encoded body)
        * areaId : 服務區，type int
        * commercialId : 組織編號，type long
        * action : 固定字串 new， type string
        * notifyUrl : 回報執行結果的URL， type string
            * 回傳參數依據 [ASUS Cloud API](https://docs.google.com/document/d/141kCcJeACvJSJC542driaCFVAkcqiEHcFNdlS8xGgO4/edit#heading=h.bnzrgv614wt)
    * Example
        * URL : https:// {{ RTE Host }} /ArcareEng/ServerMaintenance
        * Body : areaId=1&commercialId=123456789&action=new&notifyUrl=https%3A%2F%2Ftest.asuswebstorage.com%2F
* Response
    * Body (JSON)
        * { receive : 接收request成功否, errorCode : 錯誤代碼(當receive=false時產生) }
* 新增企業組織(ServerToServer)流程圖

    ![新增企業組織(ServerToServer)流程圖]

### <div id="deleteenterpriseflow">刪除企業組織 <path>(企業組織資料維護)</div>
* 說明 : 提供給ASUS WebStorage呼叫，用來刪除企業組織，當呼叫此API時，會刪除該企業組織下所有企業資料、帳號資料以及組織資料庫。
* 僅支援Server to Server呼叫

### <div id="deleteenterpriseserverflow">Server to server <path>(企業組織資料維護/刪除企業組織)</div>
* 限制 : 
    * 呼叫端的IP須在信任的IP清單中
    * 當呼叫完 get member list api 後，如 administrator state 為 32，才將執行 delete team 
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/ServerMaintenance)
    * Content-Type： application/x-www-form-urlencoded
    * Body(encoded body)
        * areaId : 服務區，type int
        * commercialId : 組織編號，type long
        * action : 固定字串 delete， type string
        * notifyUrl : 回報執行結果的URL， type string
            * 回傳參數依據 [ASUS Cloud API](https://docs.google.com/document/d/141kCcJeACvJSJC542driaCFVAkcqiEHcFNdlS8xGgO4/edit#heading=h.bnzrgv614wt)
    * Example
        * URL : https:// {{ RTE Host }} /ArcareEng/ServerMaintenance
        * Body : areaId=1&commercialId=123456789&action=delete&notifyUrl=https%3A%2F%2Ftest.asuswebstorage.com%2F
* Response
    * Body (JSON)
        * { receive : 接收request成功否, errorCode : 錯誤代碼(當receive=false時產生) }
* 刪除企業組織流程圖

    ![刪除企業組織流程圖]

### <div id="syncaccountflow">帳號資料同步 <path>(企業組織資料維護)</div>
* 說明 : 提供給ASUS WebStorage呼叫，用來執行帳號資料同步，當呼叫此API時，會依據WFB Member list資料進行帳號同步。
* 支援以下兩種模式
    * 使用Token呼叫
    * Server to Server呼叫

### <div id="syncaccounttokenflow">Token驗證 <path>(企業組織資料維護/帳號資料同步)</div>
* 限制 : 透過token向ASUS WebStorage取得User Info，User Info內的type=admin 且 supportRuru=1
* 帳號同步狀態說明 : 當呼叫完 get member list api 後，依據 member state 不同動作
    * 當 member state 為 64 時，即為 停用。
    * 當 member list 清單中未找到已存在 ruRU 資料庫中的 member，即為 刪除。
    * 當 member state 為 2、4、8、16，即為 正常使用，執行啟動狀態並更新會員名稱以及會員郵件
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/CustomerMaintenance)
    * Content-Type： application/x-www-form-urlencoded
    * Body(encoded body)
        * token_type : token的格式， type string
        * token : access token， type string
        * action : 固定字串 sync， type string
        * notifyUrl : 回報執行結果的URL， type string
            * 回傳參數依據 [ASUS Cloud API](https://docs.google.com/document/d/141kCcJeACvJSJC542driaCFVAkcqiEHcFNdlS8xGgO4/edit#heading=h.bnzrgv614wt)
    * Example
        * URL : https:// {{ RTE Host }} /ArcareEng/enterprise/sync/token
        * Body : token_type=BEARER&token=1234567898asdasdasd&action=sync&notifyUrl=https%3A%2F%2Ftest.asuswebstorage.com%2F
* Response
    * Body (JSON)
       * { receive : 接收request成功否, errorCode : 錯誤代碼(當receive=false時產生) }
* 帳號資料同步(Token)流程圖

    ![帳號資料同步(Token)流程圖]

### <div id="syncaccountserverflow">Server to server <path>(企業組織資料維護/帳號資料同步)</div>
* 限制 : 呼叫端的IP須在信任的IP清單中
* 帳號同步狀態說明 : 當呼叫完 get member list api 後，只針對 member 做資料比對。依據 member state 執行不同動作
    * 當 member state 為 64 時，即為 停用。
    * 當 member list 清單中未找到已存在 ruRU 資料庫中的 member，即為 刪除。
    * 當 member state 為 2、4、8、16，即為 正常使用，執行啟用狀態並更新會員名稱以及會員郵件
    * 其餘 member state 同正常使用處理方式
* Request : (HTTP POST; https:// {{ RTE Host }} /ArcareEng/ServerMaintenance)
    * Content-Type： application/x-www-form-urlencoded
    * Body(encoded body)
        * areaId : 服務區，type int
        * commercialId : 組織編號，type long
        * action : 固定字串 sync， type string
        * notifyUrl : 回報執行結果的URL， type string
            * 回傳參數依據 [ASUS Cloud API](https://docs.google.com/document/d/141kCcJeACvJSJC542driaCFVAkcqiEHcFNdlS8xGgO4/edit#heading=h.bnzrgv614wt)
    * Example
        * URL : https:// {{ RTE Host }} /ArcareEng/ServerMaintenance
        * Body : areaId=1&commercialId=123456789&action=sync&notifyUrl=https%3A%2F%2Ftest.asuswebstorage.com%2F
* Response
    * Body (JSON)
        * { receive : 接收request成功否, errorCode : 錯誤代碼(當receive=false時產生) }
* 帳號資料同步(ServerToServer)流程圖

    ![帳號資料同步(ServerToServer)流程圖]

### <div id="service">系統狀態查詢</div>
* 說明 : 提供給ASUS WebStorage呼叫，用來確認AP Server是否可正常連線
* Server to Server呼叫
* 採同步呼叫，確認資料庫連線狀態後回傳給ASUS WebStorage。

### <div id="serviceflow">Server to server <path>(系統狀態查詢)</div>
* 限制 : 呼叫端的IP須在信任的IP清單中
* Request : (HTTP GET; https:// {{ RTE Host }} /ArcareEng/ServiceStatus)
    * Parameter
        * 無
* Response
    * Body (JSON)
        * 若成功則回傳ok,若失敗則回傳錯誤原因
        * 狀態碼清單
        
* 系統狀態查詢流程圖

    ![系統狀態查詢流程圖]

### <div id="maintainstart">進入維護狀態</div>
* 說明 : 提供給維護人員呼叫，呼叫後，RTE引擎進入維護狀態，並將所有共用/企業組織資料庫標示為未更新完成以及刪除 Tomcat安裝路徑\webapps\ArcareEng\Cache\ 整個資料夾的內容。在進入維護狀態期間，RTE引擎增加以下限制:
    * 所有Request都需查表更新確認共用/所屬組織資料庫已維護完成，否則跳轉至提示目前在維護狀態的畫面。
    * 企業組織資料維護的API禁止使用，避免造成更新維護失敗或有資料錯誤問題。
* 限制 : 必須在本機端呼叫
* Request : (HTTP GET; https:// {{ RTE Host }} /ArcareEng/MaintainStart)
    * Parameter
        * 無
* Response
    * Body (JSON)
        * 若成功則回傳ok,若失敗則回傳錯誤原因
        * 狀態碼清單

### <div id="maintainfinish">退出維護狀態</div>
* 說明 : 提供給維護人員呼叫，呼叫後，RTE引擎需檢查是否所有共用/企業組織資料庫標示皆為更新完成，若是則可執行以下動作
    * 退出維護狀態
    * 背景執行CACHE檔案的全刪全增
        * 背景重新產生Cache檔案(請參考 CreateProjectCache_Servlet 執行緒啟動產生Cache的作法)
* 限制 : 必須在本機端呼叫
* Request : (HTTP GET; https:// {{ RTE Host }} /ArcareEng/MaintainFinish)
    * Parameter
        * 無
* Response
    * Body (JSON)
        * 若成功則回傳ok,若失敗則回傳錯誤原因
        * 狀態碼清單

### <div id="asusconfig">RTE設定</div>
* 設定檔案路徑 : { Tomcat Path } \conf\asus_api.properties
* 參數清單
| 參數名稱        | 參數說明    |
| ------------- |:-------------|
| rteRedirectUri   | RTE呼叫ASUS WebStorage 指定的 redirect_uri |
| rteClientId      | RTE向ASUS WebStorage 申請的 Client ID |
| rteClientSecret      | RTE向ASUS WebStorage 申請的 Client Secret      |
| maeIosRedirectUri   | MAE呼叫ASUS WebStorage 指定的 IOS 版 redirect_uri |
| maeIosClientId      | MAE向ASUS WebStorage 申請的 IOS 版 Client ID      |
| maeIosClientSecret      | MAE向ASUS WebStorage 申請的 IOS 版 Client Secret |
| maeAndroidRedirectUri   | MAE呼叫ASUS WebStorage 指定的 Android 版 redirect_uri |
| maeAndroidClientId      | MAE向ASUS WebStorage 申請的 Android 版 Client ID |
| maeAndroidClientSecret      | MAE向ASUS WebStorage 申請的 Android 版 Client Secret |
| asusAccountServiceLoginUrl      | ASUS WebStorage Login Page URL|
| asusAccountServiceLogoutUrl      | ASUS WebStorage Logout API URL |
| asusAccountServiceAccessTokenUrl      | ASUS WebStorage Get/Refresh Access Token API URL |
| asusAccountServiceUserInfoUrl      | ASUS WebStorage Get User Info API URL |
| asusAccountServiceWFBMemberListUrl      | ASUS WebStorage Get WFB MemberList API URL |
| projectId      | 雲端寶盒-系統代號 |
| companyId      | 雲端寶盒-範本組織代號 |
| adminGroupNo      | 雲端寶盒系統-權限管理者角色代號 |
| userGroupNo      | 雲端寶盒系統-權限使用者角色代號 |
| orgPlanNo      | 雲端寶盒系統-權限組織編制計畫代號 |
| maintainWorkerCount      | 同時可執行維護動作的執行緒數量，請填入比0大的數字 |
| whiteList      | 信任的IP來源，可接受多組位置以,連接在一起。如: 192.168.1.1,192.168.22.11 |
| newDBFilePath.流水序號      | 新增的企業組織資料庫檔案資料夾路徑，可多組，依據流水序號由1-100，如:newDBFilePath.1 表示第一組，資料夾路徑需存在於DB Server上，且須用資料夾分隔符號結尾並注意逃脫字元，路徑格式範例: D:\\\\BAK\\\\ |
| newDBFileInitSize      | 新增的企業組織資料庫檔案初始化大小，單位為MB。範例: 1024 |
| newDBFileGrowthSize      | 新增的企業組織資料庫檔案自動成長大小，單位為MB。範例: 10 |
| newDBFileMaxSize      | 新增的企業組織資料庫檔案限制大小，單位為MB。範例: 10240 |
| newDBLogPath      | 新增的企業組織資料庫交易紀錄檔資料夾路徑 |
| newDBLogInitSize      | 新增的企業組織資料庫交易紀錄檔初始化大小，單位為MB。範例: 1024 |
| newDBLogGrowthSize      | 新增的企業組織資料庫交易紀錄檔自動成長大小，單位為MB。範例: 10 |
| newDBLogMaxSize      | 新增的企業組織資料庫交易紀錄檔限制大小，單位為MB。範例: 10240 |
| newDBBackupPath.流水序號      | 新增的企業組織資料庫備份檔案路徑，可多組，依據流水序號由1-100，如:newDBBackupPath.1 表示第一組，資料夾路徑需存在於DB Server上，且須用資料夾分隔符號結尾並注意逃脫字元，路徑格式範例: D:\\\\BAK\\\\ |
| accessLogPath | access log 檔案路徑 |
| osType | AP Server作業系統類型設定，1.windows/2.centos/3.unbutu |
| taskLogPath | 系統排程 log 檔案路徑 |
| tempFileKeepDay | 暫存檔保留天數，請填入比0大的數字 |
| logFileKeepDay | log檔案保留天數，請填入比0大的數字 |

### <div id="accesslog">Access Log 紀錄</div>
* 當API被呼叫時，會留下一筆資料
* 可匯入統計軟體進行分析，各API均輸出到同一個檔案，有一定格式
* 檔案路徑由參數accessLogPath進行設定
* 1小時產生1個檔案
* 若1小時內檔案超過50mb則產生該小時的第2個檔案(1小時內產生檔案上限為20個)
* 檔案保留天數由參數logFileKeepDay決定
* 檔案編碼為UTF-8
* 欄位定義 : DateTime|LogKey|ID|API|ErrorCode|message|Client IP|ServerIP|ClientType|ClientVersion|X_Ver|SID|Manufacturer|ProductName|OS|SKUNumber|LastCommandLength|LastCommandResponseTime||
* 欄位說明 :
| 欄位名稱        | 欄位說明    |
| ------------- |:-------------|
| DateTime   | Log記錄的日期時間 |
| LogKey   | UUID，Log記錄的unique key，跨log檔關聯查詢用的Key |
| ID   | 使用者ID (User ID) |
| API   | 執行的API名稱 |
| ErrorCode   | 執行後回傳給客戶端的Status Code，例：0表示正常執行 |
| Message   | 相關訊息。通常用於發生Exception時記錄錯誤訊息 |
| Client IP   | 呼叫此API之用戶端IP位址 |
| Server IP   | 執行API的伺服器端主機本身IP位址 |
| Client Type   | 此欄位RTE為空 |
| Client Version   | 此欄位RTE為空 |
| X_Ver   | 此欄位RTE為空 |
| SID   | 此欄位RTE為空 |
| Manufacturer   | 此欄位RTE為空 |
| Product Name   | 此欄位RTE為空 |
| OS   | 此欄位RTE為空 |
| SKUNumber   | 此欄位RTE為空 |
| LastCommandLEngth   | 此欄位RTE為空 |
| LastCommandResponseTime   | 此欄位RTE為空 |
* 備註 : 以下為ASUS提供的原始文件以及LOG樣本
    * <a href="asus/RTE/attachment/Accesslog規格20220623.docx" target="_blank">原始文件</a>
    * <a href="asus/RTE/attachment/AccessLog樣本.txt" target="_blank">LOG樣本</a>

### <div id="codelist">狀態碼一覽表</div>
| 狀態碼        | 代碼說明           |
| ------------- |:-------------:|
| 0             | 執行成功 |
| 400          | 無效的REFRESH_TOKEN      |
| 401          | 無效的ACCESS_TOKEN      |
| 500          | 傳遞參數不合法      |
| 501          | 讀取設定檔案失敗      |
| 502          | 來源IP不在信任的白名單中，IP:[xxx.xxx.xxx.xxx]      |
| 503          |  站台已進入維護模式，不可執行企業組織維護      |
| 1000          | 本機台非主要中間台，無法執行維護API功能      |
| 1001          | 作業類型不合法      |
| 1002          | 建立資料庫連線失敗      |
| 1003          | 取得密鑰資訊發生錯誤      |
| 1004          | 建立新帳務失敗      |
| 1005          | 複製權限資料失敗      |
| 1006          | 新增帳號資料失敗      |
| 1007          | 指定的企業不存在      |
| 1008          | 指定的帳號不存在      |
| 1009          | 修改帳號資料失敗      |
| 1010          | 刪除帳號資料失敗      |
| 1011          | 帳號非email格式      |
| 1012          | 刪除企業失敗      |
| 1013          | 同步帳號失敗      |
| 1014          | 企業已存在，無法新增      |
| 1015          | 新增企業組織失敗      |
| 1016          | administrator state 不為 32，停止刪除  |
| 2001          | 查詢UserInfo失敗      |
| 2013          | USER Info, Type <> admin      |
| 2014          | USER Info, unsupport ruRu      |
| 2015          | 取得WFB用戶清單失敗      |

[登入流程圖]:attachment/sd_login.png "登入流程圖"
[登出流程圖]:attachment/sd_logout.png "登出流程圖"
[首頁畫面修正]:attachment/sa_brainworkNew.png "首頁畫面修正"
[新增企業組織(Token)流程圖]:attachment/sd_addenterprise(Token).png "新增企業組織(Token)流程圖"
[新增企業組織(ServerToServer)流程圖]:attachment/sd_addenterprise(ServertoServer).png "新增企業組織(ServerToServer)流程圖"
[刪除企業組織流程圖]:attachment/sd_deleteenterprise.png "刪除企業組織流程圖"
[帳號資料同步(Token)流程圖]:attachment/sd_syncaccount(Token).png "帳號資料同步(Token)流程圖"
[帳號資料同步(ServerToServer)流程圖]:attachment/sd_syncaccount(ServertoServer).png "帳號資料同步(ServerToServer)流程圖"
[系統狀態查詢流程圖]:attachment/sd_service.png "系統狀態查詢流程圖"
