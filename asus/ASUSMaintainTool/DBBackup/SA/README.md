# 華碩行動辦公雲-資料庫備份服務程式

### <div id="require">功能說明</div>
* 該程式為作業系統服務程式，需要依據設定執行行動辦公雲各資料庫的定時備份
    * 依據華碩在資料庫維護的需求，備份檔案必須有能力還原至任意指定的時間點，因此備份內容須包含以下兩部分
        * 完整資料庫備份排程
            * 讀取站台資料庫的設定，將資料庫備份清單依據備份路徑分組後，依據分組數量產生執行緒進行各分組的備份作業
                * 執行緒內需做以下工作
                    * 執行一次資料庫交易紀錄的備份
                        * 資料庫名稱_yyyymmddHHMMss.trn
                        * 若該檔案名稱已存在，則不執行此交易紀錄備份，避免重複執行。
                    * 執行一次資料庫完整備份
                        * 資料庫名稱_yyyymmddHHMMss.bak
        * 資料庫交易紀錄備份排程
            * 讀取站台資料庫的設定，將資料庫備份清單依據備份路徑分組後，依據分組數量產生執行緒進行各分組的備份作業
                * 執行緒內需做以下工作
                    * 執行一次資料庫交易紀錄的備份
                        * 資料庫名稱_yyyymmddHHMMss.trn
                        * 若該檔案名稱已存在，則不執行此交易紀錄備份，避免重複執行。
    * 各備份排程須依據RTE引擎對於各組織資料庫的分組來決定同時啟動多少個執行緒
        * 舉例，若查詢站台管理資料庫後，各資料庫的備份路徑共有6組，表示上述兩個備份排程會各自啟動6個執行緒，依據各分組清單循序執行備份。
* 備份執行的結果需要依據[華碩ACCESSLOG的格式](../../../../asus/RTE/README?id=accesslog)寫到LOG檔案中，華碩會有LOG管理的程式將LOG檔案彙整後，針對異常的部分通知維運人員。
* LOG檔案依指定的保留天數保留檔案，超過保留天數自動刪除。
### <div id="flow">作業流程</div>

![DBBackup_before]

![DBBackup_ServiceStart]

![DBBackup_Database]

![DBBackup_DatabaseLog]

[資料庫備份服務-啟動服務]:attachment/資料庫備份服務-啟動服務.png "資料庫備份服務-啟動服務"
[資料庫備份服務-完整備份排程]:attachment/資料庫備份服務-完整備份排程.png "資料庫備份服務-完整備份排程"
[資料庫備份服務-交易紀錄檔備份排程]:attachment/資料庫備份服務-交易紀錄檔備份排程.png "資料庫備份服務-交易紀錄檔備份排程"
[DBBackup_before]:attachment/DBBackup_before.png "資料庫備份服務-維護人員設定"
[DBBackup_ServiceStart]:attachment/DBBackup_ServiceStart.png "資料庫備份服務-服務啟動"
[DBBackup_Database]:attachment/DBBackup_Database.png "資料庫備份服務-完整備份排程"
[DBBackup_DatabaseLog]:attachment/DBBackup_DatabaseLog.png "資料庫備份服務-交易紀錄檔備份排程"