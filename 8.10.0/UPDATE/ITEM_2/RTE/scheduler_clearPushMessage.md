### <div id="user">規劃人員</div>
* Rita

### <div id="updatedate">規劃日期</div>
* 2020/12/22

### <div id="trac">TRAC</div>
* #8192

### <div id="sitemanage_2">系統排程.清除推播通知訊息 <path>(RTE啟動停止)</path></div>
* 擴充
* 規格說明
    * 依據【表單.其他參數】的【欄位.清除訊息時間 / 欄位.訊息保留天數】,定時執行自發送日期起算，每日系統排程會將超過保留天數的推播通知以及相關超連結資料刪除。

* 作業流程
    * 引擎啟動

    ![scheduler_clearPushMessage_start]
    * 排程執行

    ![scheduler_clearPushMessage_run]


<!--超連結引用ps.畫面上看不到-->
[scheduler_clearPushMessage_start]:img/scheduler_clearPushMessage_start.png
[scheduler_clearPushMessage_run]:img/scheduler_clearPushMessage_run.png