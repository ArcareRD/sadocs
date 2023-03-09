# 華碩行動辦公雲-資料庫備份服務程式

### <div id="installStep">安裝步驟</div>
* 作業目的：安裝資料庫備份服務並啟動
* 安裝檔案：DatabaseBackupService_版本.zip
* 操作說明
    * 在目錄下(示範範例為C:\ArcareRobot)，直接解壓縮檔案【DatabaseBackupService_版本.zip】可產生 DatabaseBackupService 資料夾
        * ![image_install_step1]
    * 至【資料庫.WellWareProject/資料表.SYS_DBMAINTAINCHECKLIST/欄位.BACKUPPATH(備份路徑)】確認備份檔案路徑存在於DB Server上
        * ![image_install_step2]
    * 請編輯 config 資料夾下的檔案【config.properties】並儲存
        * ![image_install_step3]
        * 以下說明各參數用途及注意事項
            * db.connection.count
                * 用途說明：資料庫連線數上限
                * 注意事項：請設定 (資料庫備份路徑數\*2)+5 的連線數 (若 資料庫備份路徑數 = 5，則 連線數 = (5\*2)+5=15
                    * 資料庫備份路徑數 =【資料庫.WellWareProject/資料表.SYS_DBMAINTAINCHECKLIST/欄位.BACKUPPATH(備份路徑)】備份路徑去除重覆後的總數
            * db.port
                * 用途說明：資料庫連線port，預設 1433
            * db.account
                * 用途說明：資料庫連線帳號
            * db.password
                * 用途說明：資料庫連線密碼(明碼)
            * db.WellWareProject.dbname
                * 用途說明：WellWareProject的資料庫名，預設 WellWareProject
            * backup.db.cycle
                * 用途說明：資料庫完整備份週期(單位=小時)，預設 168
            * backup.log.cycle
                * 用途說明：資料庫交易記錄備份週期(單位=分鐘)，預設 10
            * log.keep.day
                * 用途說明：log歷史記錄檔保留天數(單位=天)，當產生log歷史記錄檔時，即判斷log歷史記錄檔若超過保留天數則自動刪除，預設 365
            * log.accesslog.path
                * 用途說明：accesslog檔案路徑
                * 注意事項：資料夾路徑需存在於DB Server上，且資料夾分隔符號須注意逃脫字元，路徑格式範例: D:\\\logs 或 .\\\logs
    * 執行【install.bat】進行安裝 (安裝完成視窗會自動關閉)
        * ![image_install_step4]
    * 執行【DatabaseBackupService.exe】啟動服務
        * ![image_install_step5]

### <div id="message">訊息說明</div>
* 啟動失敗可能原因說明
    * 如何查看訊息：至 DaemonLogs 資料夾下的檔案【databasebackupservice-stdout.日期.log】查看
        * ![image_message_startError]
    * 可能原因：
        * config 資料夾下的檔案【config.properties】參數設定錯誤，以下範例為 db.account、db.password 未設定的錯誤訊息
            * ![image_message_startError1]
        * config 資料夾下的檔案【config.properties】遺失的錯誤訊息
            * ![image_message_startError2]
        * 資料庫連線失敗，以下範例為 db.account、db.password 設定錯誤，而無法連線資料庫
            * ![image_message_startError3]
* accesslog說明
    * 以下為【資料庫完整備份】會產生的ErrorCode說明

    |API |ErrorCode |錯誤說明 |
    | --- | --- | --- |
    |/FullDatabaseBackupSchedule |0 |排程，執行成功 |
    |/FullDatabaseBackupSchedule |110001 |排程，執行失敗 |
    |/FullDatabaseBackupSchedule/GetBackupPath |200001 |取得備份路經清單，查詢失敗 |
    |/FullDatabaseBackupSchedule/GetDBNameList |200001 |取得分組資料庫清單，查詢失敗 |
    |/FullDatabaseBackupThread |0 |備份執行緒，執行成功 |
    |/FullDatabaseBackupThread |110001 |備份執行緒，執行失敗 |
    |/FullDatabaseBackupThread/CheckIsDBNeverBackup |200001 |備份前，查詢資料庫是否從未執行過備份，查詢失敗 |
    |/FullDatabaseBackupThread/backupFullDatabase |200001 |執行完整備份，失敗
    |/FullDatabaseBackupThread/backupTransactionLog |200001 |執行交易記錄備份，失敗 |

    * 以下為【資料庫交易記錄備份】會產生的ErrorCode說明

    |API |ErrorCode |錯誤說明 |
    | --- | --- | --- |
    |/TransactionLogBackupSchedule |0 |排程，執行成功 |
    |/TransactionLogBackupSchedule |110001 |排程，執行失敗 |
    |/TransactionLogBackupSchedule/GetBackupPath |500001 |取得備份路經清單，查詢失敗 |
    |/TransactionLogBackupSchedule/GetDBNameList |500001 |取得分組資料庫清單，查詢失敗 |
    |/TransactionLogBackupThread |0 |備份執行緒，執行成功 |
    |/TransactionLogBackupThread |110001 |備份執行緒，執行失敗 |
    |/TransactionLogBackupThread/CheckIsDBNeverBackup |500001 |備份前，查詢資料庫是否從未執行過備份，查詢失敗 |
    |/TransactionLogBackupThread/backupFullDatabase |500001 |執行完整備份，失敗
    |/TransactionLogBackupThread/backupTransactionLog |500001 |執行交易記錄備份，失敗 |


[image_install_step1]:attachment/install_step1.png "安裝步驟1"
[image_install_step2]:attachment/install_step2.png "安裝步驟2"
[image_install_step3]:attachment/install_step3.png "安裝步驟3"
[image_install_step4]:attachment/install_step4.png "安裝步驟4"
[image_install_step5]:attachment/install_step5.png "安裝步驟5"

[image_message_startError]:attachment/message_startError.png "啟動失敗_查看訊息"
[image_message_startError1]:attachment/message_startError1.png "啟動失敗_錯誤1"
[image_message_startError2]:attachment/message_startError2.png "啟動失敗_錯誤2"
[image_message_startError3]:attachment/message_startError3.png "啟動失敗_錯誤3"