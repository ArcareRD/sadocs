### <div id="user">規劃人員</div>
* Ivan

### <div id="updatedate">規劃日期</div>
* 2020/12/18

### <div id="trac">TRAC</div>
* #8264

### <div id="sitemanage_2">系統排程.備份稽核紀錄 <path>(RTE啟動停止)</path></div>
* 異動
* 規格說明
    * 搬移異動LOG檔資料由日->周->月->月份備份 改為 月->年度月份備份
    * 把異動LOG檔(記錄最近30天)裡的資料, 將超過30天的記錄, 複製到對應的年度月份檔
    * 刪除異動LOG檔超出30天的紀錄
    * 依據【稽核紀錄環境設定】上【月份檔保留份數】的刪除超出保留份數的月份紀錄擋
    * 排程執行時間由預設的00:00，改為依據【稽核紀錄環境設定】上【備份執行時間】的設定指定排程執行時間

* 作業流程
    * 引擎啟動

    ![BackUpAuditLog_sa1]
    * 排程執行

    ![BackUpAuditLog_sa2]


<!--超連結引用ps.畫面上看不到-->
[BackUpAuditLog_sa1]:img/BackUpAuditLog_sa1.jpg
[BackUpAuditLog_sa2]:img/BackUpAuditLog_sa2.jpg