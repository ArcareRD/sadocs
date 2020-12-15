### <div id="user">規劃人員</div>
* Ivan

### <div id="updatedate">規劃日期</div>
* 2020/12/15

### <div id="trac">TRAC</div>
* #8264

### <div id="sitemanage_2">表單.激活 <path>(Site管理)</path></div>
* 擴充
* 規格說明
    * 增加表單.稽核紀錄環境設定到激活步驟中

* 表單畫面

    ![SiteAuthorize]
* 畫面規格說明
    * 新增頁籤.稽核紀錄環境設定
        * 嵌入表單.稽核紀錄環境設定
        * 原按鈕.儲存 : 名稱替換為"下一步"
        * 原按鈕.放棄 : 名稱替換為"取消"
    * 按鈕.下一步 : 
        * 保留原有功能
            * 檢查欄位.資料庫、月份檔保留份數 、備份執行時間 不允空白，當內容值為空白時顯示紅框
            * 當欄位.資料庫 挑選的資料庫不存在於SQL Server，則建立新的資料庫
            * 將設定內容回寫至系統實體
        * 切換至下個頁籤
    * 按鈕.取消 : 關閉彈出視窗

* 作業流程
    * 開啟稽核紀錄環境設定畫面

    ![SiteAuthorize_sa1]
    * 設定稽核紀錄資料庫(建立新的資料庫)

    ![SiteAuthorize_sa2]
    * 設定稽核紀錄資料庫(挑選已存在的資料庫)

    ![SiteAuthorize_sa3]
    * 設定稽核紀錄備份執行時間

    ![SiteAuthorize_sa4]
    * 點擊按鈕.下一步

    ![SiteAuthorize_sa5]
    * 點擊按鈕.取消

    ![SiteAuthorize_sa6]

<!--超連結引用ps.畫面上看不到-->
[SiteAuthorize]:img/SiteAuthorize.jpg
[SiteAuthorize_sa1]:img/SiteAuthorize_sa1.jpg
[SiteAuthorize_sa2]:img/SiteAuthorize_sa2.jpg
[SiteAuthorize_sa3]:img/SiteAuthorize_sa3.jpg
[SiteAuthorize_sa4]:img/SiteAuthorize_sa4.jpg
[SiteAuthorize_sa5]:img/SiteAuthorize_sa5.jpg
[SiteAuthorize_sa6]:img/SiteAuthorize_sa6.jpg