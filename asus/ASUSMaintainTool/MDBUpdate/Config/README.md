# 華碩行動辦公雲-更新MDB檔案程式

### <div id="installStep">安裝步驟</div>
* 作業目的：安裝MDB更新檔程式
* 安裝檔案：MDBUpdate_版本.zip
* 操作說明
    * 在目錄下(示範範例為C:\ArcareRobot)，直接解壓縮檔案【MDBUpdate_版本.zip】可產生 MDBUpdate 資料夾
        * ![image_install_step1]
    * 請編輯 config 資料夾下的檔案【config.properties】並儲存
        * ![image_install_step2]
        * 以下說明各參數用途及注意事項
            * db.connection.count
                * 用途說明：資料庫連線數上限
            * SQL.Server
                * 用途說明：資料庫伺服器名稱，預設 localhost
            * SQL.Port
                * 用途說明：資料庫連線port，預設 1433
            * SQL.Account
                * 用途說明：資料庫連線帳號
            * SQL.Password
                * 用途說明：資料庫連線密碼(明碼)
            * Database.Site
                * 用途說明：站台資料庫名稱，預設 WellWareProject
            * Database.Share
                * 用途說明：共用資料庫名稱，預設 PJ000200000012_ShareClass
            * UpdateDBBackupPath
                * 用途說明：更新時資料庫的備份檔存放位置路徑
                * 注意事項：資料夾路徑需存在於DB Server上，且資料夾分隔符號須注意逃脫字元，路徑格式範例: D:\\mdbupdate\\bak 或 .\\mdbupdate\\bak
            * LogFileKeepDay
                * 用途說明：log歷史記錄檔保留天數(單位=天)，當產生log歷史記錄檔時，即判斷log歷史記錄檔若超過保留天數則自動刪除，預設 365
            * AccessLogPath
                * 用途說明：accesslog檔案的存放位置路徑
                * 注意事項：資料夾路徑需存在於DB Server上，且資料夾分隔符號須注意逃脫字元，路徑格式範例: D:\\logs 或 .\\logs
    * 執行【run.bat】啟動程式
        ![image_install_step3]
   
* <ps>【改版更新程式的注意事項】</ps> 
    ```
    當程式改版更新時，只需覆蓋檔案: ArcareMDBUpdate.jar、ArcareMDBUpdate_lib 即可
    ```

### <div id="message">accesslog 訊息說明</div>
* 執行成功說明
|執行API |代碼 |代碼說明 |
| --- | --- | --- |
|MDBUpdate/Open |0 |開啟介面，執行成功 |
|MDBUpdate/ImportObject/Import |0 |系統更新，執行成功 |
|MDBUpdate/RestoreCorpDB/RestoreCorpDB |0 |還原組織資料庫，執行成功 |

* 執行錯誤說明
|代碼 |代碼說明 |
| --- | --- |
|130001 |尚未設定資料庫備份路徑為空，請檢查檔案 config.properties 的參數.UpdateDBBackupPath 是否有設定。 |
|300001	|連線資料庫發生錯誤 |
|300001	|取得Site資料庫連線失敗 |
|300002	|取得共用資料庫連線失敗 |
|300003	|取得組織資料庫連線物件失敗 |
|400001	|[行動辦公雲]尚未開啟維護模式。 | 
|400001	|取得資料庫清單資料(SYS_DBMAINTAINCHECKLIST)失敗 |
|400002	|挑選的系統檔案不存在。 路徑: import file location |
|400002	|系統檔無法開啟！ (import file location) |
|400002	|取得安裝資訊失敗！ (import file location) |
|400002	|查無安裝資訊！ (import file location) |
|400002	|取得安裝物件清單失敗！ (import file location) |
|400002	|查無安裝物件清單！ (import file location) |
|400002	|取得安裝檔資訊失敗。 【Exception 訊息】 |
|400007	|共用資料庫[show database name]的備份檔案不存在 |
|400007	|沒有任何資料庫備份檔案 |
|400007	|備份資料庫失敗。 |
|400007	|取得物件資訊失敗。 [OBJDto] 為空。 |
|400007	|取得物件資訊失敗。 [OBJInfoDto] 為空值 |
|400007	|物件 [ (物件類型)物件名稱 ] 解析失敗 |
|400007	|匯入物件到組織資料庫[show database name]失敗！ |
|400008	|匯入資料表失敗。show TableManage Error |
|400008	|物件匯入失敗。 主鍵索引不存在。 |
|400008	|已引用專案[extend project material id]的資料表[extend table material id]，但結構不一致 |
|400008	|已引用專案[extend project material id]的資料表[extend table material id]，但有觸發程序 |
|400008	|取得實體表格資訊物件(object id), 在物件檔中的物件內容解析失敗。 |
|400008	|歸屬資料庫有異動,但目的資料庫已存在相同資料 [(old Table Type)old Table Name] |
|400008	|取得資料表的欄位結構失敗。Info[oldTableNm: old Table Name] |
|400008	|備份資料表失敗 |
|400008	|取得備份的資料表名稱失敗 |
|400008	|舊資料表的欄位[fiel name](get field type and length)還原至新資料表的欄位[fiel name](get field type and length)發生錯誤:不支援轉換型態 |
|400008	|還原資料發生錯誤[Exception訊息] |
|400008	|建立索引發生錯誤[Exception訊息] |
|400008	|建立初始記錄[#record Pos]發生錯誤[Exception訊息] |
|400008	|建立初始記錄[#record Pos]發生錯誤[Exception訊息] |
|400009	|建立語言包失敗。【Exception訊息】 |
|400003	|資料檔無法開啟！ (data file location) |
|400003	|寫入權限資料到組織資料庫[show database name]失敗！ |
|400003	|取得權限資料實體清單數量失敗 |
|400003	|寫入權限資料失敗 【Exception訊息】 |
|400003	|寫入權限資料取消交易失敗 【Exception訊息】 |
|400003	|無法讀取MDB檔案中指定的實體資料 (Table Name) |
|400003	|無法讀取目的資料庫中指定的實體資料 (Table Name) |
|400004	|將組織資料庫[show database name]更新為不可服務失敗 |
|400005	|沒有任何資料庫備份檔案 |
|400005	|組織資料庫[show database name]的備份檔案不存在 |
|400005	|還原組織資料庫[show database name]失敗 |
|400006	|密鑰資訊未設定 |
|400006	|載入密鑰發生錯誤。【Exception訊息】 |




[image_install_step1]:attachment/install_step01.png "安裝步驟1"
[image_install_step2]:attachment/install_step02.png "安裝步驟1"
[image_install_step3]:attachment/install_step03.png "安裝步驟1"