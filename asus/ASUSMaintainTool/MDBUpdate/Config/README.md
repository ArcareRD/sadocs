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
        * ![image_install_step3]


### <div id="message">訊息說明</div>
* 啟動失敗可能原因說明

* accesslog說明



[image_install_step1]:attachment/install_step01.png "安裝步驟1"
[image_install_step2]:attachment/install_step02.png "安裝步驟1"
[image_install_step3]:attachment/install_step03.png "安裝步驟1"