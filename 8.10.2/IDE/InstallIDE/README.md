# IDE 平台基礎套件安裝

## 版本：

|日期|版號|備註|
|:--:|:--:|:--:|
|2022-03-01|8.10.2.0 (含)以上|改版|


## <P id='job_purpose'>作業目的：</P>

    在安裝IDE前，請先確認環境需求是否符合。

## <P id="environmental_requirements">環境需求：</P>

|項目|內容|備註|
|--|--|--|
|作業系統|Windows 2008 R2 (含) 以上| 因IDE目前須搭配打樣台，故作業系統只能使用win server等級，否則無法打樣|
|資料庫版本|MS SQL 2008R2 (含) 以上||
|瀏覽器|Chromium 80 (含) 以上||
| |Internet Information Services (IIS) 版本依作業系統 | |
| |Tomcat 8 |因產出規格書程式是由JAVA撰寫，故運行機台需安裝 Tomcat |

----
## 前置環境準備：

### <P id="net_frame">.NET框架 </P>

`※注意※ 若為開發環境，請在Vistual Studio 安裝過程中選取安裝 .NET Framewor 4.8`

1-1. 下載 .NET Framework 4.8，網址: https://docs.microsoft.com/zh-tw/dotnet/framework/install/on-windows-10#net-framework-48

1-2. 同意條款並安裝，安裝完成後，關閉介面即可 <br>
![alt .NET Frmaework安裝_1](attachment/net_framework_1.png)


### <P id="iis">Internet Information Services (IIS) 環境設定 </P>

`※注意1※ 請先確認該機台已安裝IIS，再依下列步驟設定`
`※注意2※ win 10機台，請由程式與功能->開啟或關閉windows功能, 進入設定`
        ![alt IIS設定_1](attachment/IIS_win10.png)    

1-1. 進入伺服器管理員/IIS，駐留選取新增角色及功能 <br>
![alt IIS設定_1](attachment/IIS_1.png)

1-2. 執行下一步 <br>
![alt IIS設定_2](attachment/IIS_2.png)

1-3. 選取安裝類型=角色型或功能型安裝 <br>
![alt IIS設定_3](attachment/IIS_3.png)

1-4. 選取本次要設定的伺服器 <br>
![alt IIS設定_4](attachment/IIS_4.png)

1-5. 設定角色 <br>
![alt IIS設定_5](attachment/IIS_5.png)

1-5-1. 需設定的角色項目，請找到下圖的項目，並選取 <br>
![alt IIS設定_5_1](attachment/IIS_5_1.png)

1-6. 設定功能 <br>
![alt IIS設定_6](attachment/IIS_6.png)

1-6-1. 需設定的功能項目，請找到下圖的項目，並選取 <br>
![alt IIS設定_6_1](attachment/IIS_6_1.png)

1-7. 先確認安裝項目是否正確，確認後再執行安裝 <br>
![alt IIS設定_7](attachment/IIS_7.png)

1-8. 查詢安裝進度條，安裝完後，再執行關閉 <br>
![alt IIS設定_8](attachment/IIS_8.png)


### <P id="ad_credentials">設定自簽憑證 </P>

1-1. 開啟IIS，選取伺服器憑證，並開啟功能
![alt 自簽憑證_1](attachment/Https_1.png)

1-2. 建立自我簽屬憑證要求
![alt 自簽憑證_2](attachment/Https_2.png)

1-3. 駐留站台，進行擊結
![alt 自簽憑證_3](attachment/Https_3.png)

1-4. 擊結自我簽屬憑證設定
![alt 自簽憑證_4](attachment/Https_4.png)

1-5. 設定完成，登入AD憑證服務伺服器( http://localhost/certsrv )，確認是否看到下列畫面
![alt 自簽憑證_5](attachment/Https_5.png)


----
## 安裝:

### <P id="wellwaredtstools">WellWareDTSTools </P>

`※注意※ 因該程式是使用32位元撰寫的，故當使用的機台為64位元，需加裝C++ 可轉散發套件，請參考步驟 1-1 ~ 1-2 `

1-1. 依作業系統架構下載可轉散發套件，網址: https://docs.microsoft.com/zh-tw/cpp/windows/latest-supported-vc-redist?view=msvc-170

1-2. 執行安裝檔，選取項目後，執行下一步安裝，安裝完成後，關閉介面即可 <br>
![alt WellWareDTSTools安裝_1](attachment/WellWareDTSTools_1.png)

1-3. 取得 WellWareDTSToolsSetup 安裝檔。 <a href="8.10.2/IDE/InstallIDE/attachment/WellWareDTSToolsSetup.msi" target="_blank">下載安裝檔</a> <br>

1-4. 執行 WellWareDTSToolsSetup.msi 安裝檔，執行下一步 <br>
![alt WellWareDTSTools安裝_2](attachment/WellWareDTSTools_2.png)

1-5. 選擇要安裝的資料夾，並設定為所有使用者，執行下一步 <br>
![alt WellWareDTSTools安裝_3](attachment/WellWareDTSTools_3.png)

1-6. 執行下一步安裝，安裝完成後，關閉介面即可 <br>
![alt WellWareDTSTools安裝_4](attachment/WellWareDTSTools_4.png)


### <P id="ide">IDE </P>

`※注意※ 下列程式的檔案請依版本更新清單上釋出的版本號，至 U:\ 取得版本安裝檔` 

1-1. 建立存放IDE相關程式的資料夾。建議存放位置及資料夾名: C:\ArcareRobot\ <br>

    1-1-1. 資料夾: TEMP；用途: 規格書、資料庫備份檔的暫存位置  
    1-1-2. 資料夾: vhosts；用途: IDE主程式存放位置  
    1-1-3. 資料夾: XML；用途: 發行後XML檔的暫存位置 
    1-1-4. 資料夾: ekfmxsd；用途: XML對應的XSD驗證檔存放位置 

1-2. 開啟IIS介面，將IIS停止 <br>
![alt ide_1](attachment/ide_1.png)

1-3. 於目錄 C:\ArcareRobot\  下，解壓縮XSD驗證檔 (DKS_XSD_版本.zip) 並存放到資料夾【ekfmxsd】。 <br>

1-4. 於目錄 C:\ArcareRobot\vhosts 將主程式安裝檔 (DKS_版本.zip) 解壓縮，產生 Eco 的資料夾 <br>

1-5. 下載檔案: <a href="8.10.2/IDE/InstallIDE/attachment/Authenticate.xml" target="_blank">Authenticate</a> 。將檔案存放於目錄 C:\ArcareRobot\vhosts 下

1-6. 開啟IIS介面，建立IDE應用程式 <br>
![alt ide_2](attachment/ide_2.png)

1-7. 設定應用程式別名及實體路徑 <br>
![alt ide_3](attachment/ide_3.png)

1-7. 設定應用程式資料夾權限為完全控制，設定完成後，啟動IIS <br>
![alt ide_5](attachment/ide_5.png)

1-8. 登入http://localhost/ECO/DKSDatabaseSet/Index ，輸入 資料庫登入名稱、資料庫登入密碼、Tomcat帳號、Tomcat密碼 後執行【儲存】<br>
![alt ide_4](attachment/ide_4.png)

1-9. 開啟工具【WellWareDTSTools】，選取功能.匯入，依序將下列初始值匯入。完成後須再次重新啟動IIS。 <br>

    1-9-1. 載入【InitialDKSOneTime.mdb】填入機台相關資訊，填寫資料庫:DKS，寫入方式為新增並執行【確定】
    1-9-2. 載入【InitialDKS_(版本).mdb】填入機台相關資訊，資料庫為DKS，寫入方式為全刪全增並執行【確定】
![alt ide_6](attachment/ide_6.png)

1-10. 完成後，登入測試是否正常 http://localhost/Eco/Home/Index  。系統預設Site管理者帳號: Admin_DKS 、密碼: abc123 <br>
![alt ide_7](attachment/ide_7.png)

1-11. 登入系統的平台管理，開啟PA03.系統設定，調整該機台的相關資訊 <br>
![alt ide_8](attachment/ide_8.png) 

**必須要調整的項目，請參考下表。若為研發人員的開發機台，則與後端(FMS、AMS、RTE、...)銜接的網址，請改填寫無效的網址即可**

|代碼 |描述 |
|---- |---- |
|DKSSiteNo |DKS設計的唯一號 (通常為4碼) | 
|EcoCenterUrl |FMS網址，若為開發機，請填寫無效的網址 | 
|EcoServerHostName |DKS網址:IP | 
|GenSASpecURL |產出SA規格書API存放目錄 | 
|GenSpecURL |產出規格書API存放目錄 | 
|ProjectAccount_AppendURL |運行台的新增帳號修正API | 
|PrototypingURL |打樣預覽網址 | 
|PrototypingViewURL |打樣邏表預覽網址 | 
|PTURL |打樣API存放目錄 | 
|UserUpdateURL |打樣專案_異動帳戶使用者的API | 
|AuthenticateConfigFile |限定特定帳號的使用日期及時段 | 
|GetSpecTemplatePath |規格書範本檔案路徑 | 
|TempPath |規格文件暫存目錄 |
|XmlTempPath |匯出 XML 的暫存路徑 |

1-12. 請先至 **服務機台記錄** 取得各機台對應的發送郵件帳號資訊。在至下列位置更改發送 SMTP 郵件信箱及密碼，更新後須重啟IIS <br>
![alt ide_9](attachment/ide_9.png) 


### <P id="error_validation">檢錯服務 </P>

1-1. 先在指定硬碟目錄(預設為C:\ArcareRobot)，直接解壓縮檔案【ErrorValidationService_(版本).zip】可產生 ErrorValidationService 資料夾

1-2. 編輯目錄 config 下的 config.properties 並儲存 <br>
![alt ErrorValidation_1](attachment/ErrorValidation_1.png) 

**參數說明如下表**

|參數名稱 |說明 |
|------- |---- |
|server.port |服務監聽http port。預設為8082 |
|ide.db.connection.count |資料庫連線數上限 |
|ide.db.ip |資料庫連線IP。 |
|ide.db.port |資料庫連線port |
|ide.db.account |資料庫連線帳號 |
|ide.db.password |資料庫連線密碼 |
|node.name |群集當中一個服務的名稱。同一群集內，名稱不可重覆 |

1-3. 於目錄 ErrorValidationService 下執行 install.bat，安裝完成視窗會自動關閉 

1-4. 啟動檢錯服務 
    
    服務安裝後會設定為自動啟動，僅首次安裝的啟動需手動執行。機器重開機後不須登入，服務也會自動啟動。
![alt ErrorValidation_2](attachment/ErrorValidation_2.png)

1-5. 登入系統的平台管理，開啟PA03.系統設定，設定IDE檢錯服務的網址及呼叫服務要重試的次數 <br>
![alt ErrorValidation_3](attachment/ErrorValidation_3.png)


### <P id="genspec">規格書 </P>

1-1. 輸入網址 http://機台名:8080/manager/  登入Tomcat <br>
![alt GenSpec_1](attachment/GenSpec_1.png)

1-2. 選取產出規格書的檔案(ECO_GenSpec_版本.war) 上傳，並執行【Deploy】 <br>
![alt GenSpec_2](attachment/GenSpec_2.png)

1-3. 登入網址: http://機台名:8080/ECO_GenSpec/GetVersion.html 查詢版本是否正確 <br>
![alt GenSpec_3](attachment/GenSpec_3.png)

1-4. 編輯目錄 C:\WebServer\TOMCAT\conf\ 下的 config.properties 並儲存 <br>
![alt GenSpec_4](attachment/GenSpec_4.png)

**參數說明如下表**

|參數名稱 |說明 |
|------- |---- |
|Password |登入資料庫的密碼 |
|Server |SQL伺服器的IP	|
|UserName |登入資料庫的帳號 |
|SQLType |資料庫類型(目前僅支援MSSQL) |
|Port |SQL伺服器的Port |

1-5. 登入系統的平台管理，開啟PA03.系統設定，設定規格書相關代碼內容 <br>
![alt GenSpec_5](attachment/GenSpec_5.png)

1-6. 查詢PA03.系統設定，代碼: **GetSpecTemplatePath** 設定的目錄，將規格書範本檔(template_語系.docx) 複製一份存放於此目錄下 <br>
![alt GenSpec_6](attachment/GenSpec_6.png)


------
## 升級/更新:

### <P id="ide_upgrade">IDE升級</P>

1-1. 開啟IIS介面，將IIS停止

1-2. 於目錄 C:\ArcareRobot\vhosts 將主程式的資料夾【Eco】內容清空

1-3. 於目錄 C:\ArcareRobot\vhosts 將主程式安裝檔 (DKS_版本.zip) 解壓縮，覆蓋還原至主程式的資料夾【Eco】

1-4.請先至 **服務機台記錄** 取得各機台對應的發送郵件帳號資訊。在至下列位置更改發送 SMTP 郵件信箱及密碼
![alt ide_9](attachment/ide_9.png)

`※注意※ 下列XSD驗證檔為非每次必要的更新檔，請依版本更新清單釋出的版本決定是步執行步驟 1-5 ~ 1-6`

1-5. 於目錄 C:\ArcareRobot\ 將XSD驗證的資料夾【ekfmxsd】內容清空
    
1-6. 於目錄 C:\ArcareRobot\  將XSD驗證檔 (DKS_XSD_版本.zip) 解壓縮，覆蓋還原至XSD驗證檔的資料夾【ekfmxsd】。

1-6. 開啟IIS介面，將IIS啟動 

1-7. 登入http://localhost/ECO/DKSDatabaseSet/Index ，輸入 資料庫登入名稱、資料庫登入密碼 後執行【重整資料庫】<br>
![alt ide_upgrade_1](attachment/ide_upgrade_1.png)
    
`※注意※ 下列初始值更新為非每次必要的更新檔，請依版本更新清單釋出的版本決定是步執行步驟 1-8`

1-8. 更新初始值：開啟工具【WellWareDTSTools】> 匯入，【InitialDKS_(版本).mdb】填入機台相關資訊，資料庫為DKS，寫入方式為全刪全增並執行【確定】 <br>
![alt ide_upgrade_2](attachment/ide_upgrade_2.png)

1-9. 上述步驟全數完成後，開啟IIS介面，將IIS重新啟動


### <P id="error_validation_upgrade">檢錯服務升級</P>

1-1. 停止檢錯服務 <br>
![alt ErrorValidation_Upgrade_1](attachment/ErrorValidation_Upgrade_1.png)

1-2. 至 指定硬碟目錄(預設為C:\ArcareRobot)，解壓縮檔案【ErrorValidationService_(版本).zip】 <br>
    
    請勿覆蓋原 ErrorValidationService 資料夾

1-3. 至 解壓縮後的資料夾，取得 ErrorValidation.jar，覆蓋原 ErrorValidationService 資料夾中對應的jar檔 <br>

    ErrorValidation.jar 為必要更新的檔案，須配合版本更新清單中的條件，決定各版最後要更新的檔案
![alt ErrorValidation_Upgrade_2](attachment/ErrorValidation_Upgrade_2.png)    

1-4. 重新啟動檢錯服務 <br>


### <P id="genspec_upgrade">規格書升級</P>

請重複[規格書](README#genspec) 安裝步驟 1-1 ~ 1-3