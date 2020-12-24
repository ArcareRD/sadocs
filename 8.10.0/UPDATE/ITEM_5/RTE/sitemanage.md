### <div id="user">規劃人員</div>
* Ivan

### <div id="updatedate">規劃日期</div>
* 2020/12/18

### <div id="trac">TRAC</div>
* #8264

### <div id="sitemanage_2">Site管理首頁畫面 <path>(Site管理首頁)</path></div>
* 異動
* 規格說明
    * Site管理人員角色以及相關表單如下
        * Site管理員 : 增加以下表單
            * 表單.稽核紀錄環境設定
        * 企業管理員 : 增加以下表單
            * 表單.稽核紀錄查詢
        * Site稽核員 : 可用表單如下
            * 表單.企業稽核員指定
            * 表單.稽核紀錄查詢
                * 表單.稽核紀錄內容
        * 企業稽核員 : 可用表單如下
            * 表單.稽核紀錄查詢
                * 表單.稽核紀錄內容

    * 作廢表單.稽核Log設定

* 表單畫面
    * Site管理員
        | 原畫面 | 新畫面 | 
        | :---: | :---: |
        |![SiteManage_SiteManager(old)]|![SiteManage_SiteManager]|

    * 企業管理員
        | 原畫面 | 新畫面 | 
        | :---: | :---: |
        |![SiteManage_EnterpriseManager(old)]|![SiteManage_EnterpriseManager]|

    * Site稽核員

        ![SiteManage_SiteAuditor]

    * 企業稽核員
        
        ![SiteManage_EnterpriseAuditor]


    
* 畫面規格說明
    * 左側樹狀選單
        * 若為Site管理員 :
            * 增加表單.稽核紀錄環境設定
        * 若為企業管理員 :
            * 增加表單.稽核紀錄查詢
        * 若為Site稽核員 :
            * 僅能看到表單.企業稽核員指定、表單.稽核紀錄查詢
        * 若為企業稽核員 :
            * 僅能看到表單.稽核紀錄查詢
        * 刪除表單.稽核Log設定

* 作業流程
    * 開啟Site管理首頁畫面

    ![SiteManage_sa1]


<!--超連結引用ps.畫面上看不到-->
[SiteManage_SiteManager(old)]:img/SiteManage_SiteManager(old).jpg
[SiteManage_SiteManager]:img/SiteManage_SiteManager.jpg
[SiteManage_EnterpriseManager(old)]:img/SiteManage_EnterpriseManager(old).jpg
[SiteManage_EnterpriseManager]:img/SiteManage_EnterpriseManager.jpg
[SiteManage_SiteAuditor]:img/SiteManage_SiteAuditor.jpg
[SiteManage_EnterpriseAuditor]:img/SiteManage_EnterpriseAuditor.jpg
[SiteManage_sa1]:img/SiteManage_sa1.jpg