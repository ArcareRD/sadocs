### <div id="user">規劃人員</div>
* Ivan

### <div id="updatedate">規劃日期</div>
* 2020/12/11

### <div id="trac">TRAC</div>
* #8264

### <div id="sitemanage_2">表單.稽核紀錄環境設定 <path>(Site管理)</path></div>
* 擴充
* 規格說明
    * 設定稽核紀錄資料庫以及月份檔案備份數量與備份執行時間
    * 僅【Site管理員】可使用。

* 表單畫面

    ![AuditLogEnvSetting]
* 畫面規格說明
    * 欄位.資料庫 : 稽核紀錄存放的資料庫，下拉元件，可選擇以下內容 : 
        * 建立新的資料庫 : 選擇後彈出視窗輸入新資料庫名稱(此時還不會真正建立資料庫)。
        * 所有已存在的資料庫清單。
    * 欄位.月份檔保留份數 : 備份月份檔保留的數量，超出保留份數的月份檔會被刪除，輸入元件，預設值為6，只允輸入數字且不得為0。
    * 欄位.備份執行時間 : 於每天的指定時間進行稽核紀錄的備份，不可輸入，僅能點擊按鈕挑選時間。
    * 按鈕.儲存 : 
        * 檢查欄位.資料庫、月份檔保留份數 、備份執行時間 不允空白，當內容值為空白時顯示紅框
        * 當欄位.資料庫 挑選的資料庫不存在於SQL Server，則建立新的資料庫
        * 將設定內容回寫至系統實體
    * 按鈕.放棄 : 關閉表單

* 作業流程
    * 開啟稽核紀錄環境設定畫面

    ![AuditLogEnvSetting_sa1]
    * 設定稽核紀錄資料庫(建立新的資料庫)

    ![AuditLogEnvSetting_sa2]
    * 設定稽核紀錄資料庫(挑選已存在的資料庫)

    ![AuditLogEnvSetting_sa3]
    * 設定稽核紀錄備份執行時間

    ![AuditLogEnvSetting_sa4]
    * 點擊按鈕.儲存

    ![AuditLogEnvSetting_sa5]
    * 點擊按鈕.放棄

    ![AuditLogEnvSetting_sa6]

<!--超連結引用ps.畫面上看不到-->
[AuditLogEnvSetting]:img/AuditLogEnvSetting.jpg
[AuditLogEnvSetting_sa1]:img/AuditLogEnvSetting_sa1.jpg
[AuditLogEnvSetting_sa2]:img/AuditLogEnvSetting_sa2.jpg
[AuditLogEnvSetting_sa3]:img/AuditLogEnvSetting_sa3.jpg
[AuditLogEnvSetting_sa4]:img/AuditLogEnvSetting_sa4.jpg
[AuditLogEnvSetting_sa5]:img/AuditLogEnvSetting_sa5.jpg
[AuditLogEnvSetting_sa6]:img/AuditLogEnvSetting_sa6.jpg