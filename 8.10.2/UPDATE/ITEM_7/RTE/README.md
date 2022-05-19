### <div id="user">規劃人員</div>
* 正傑、ella

### <div id="updatedate">規劃日期</div>
* 2022/05/19

### <div id="trac">TRAC</div>
* #9045

### <div id="requirement">需求展開</div>
* 因RTE引擎在CentOS上發送郵件會出現發送失敗的狀況，經debug確認後，是因作業系統在SSL認證上需強制採用TLSv1.2進行加密連線。討論後，考量到現有客戶機台不一定有支援TLSv1.2，因此在站台管理表單.郵件伺服器增加一個套用TLSv1.2的設定，當有勾選需要使用安全密碼驗證(SPA)登入時致能，引擎執行轉資料時也依據此欄位來決定是否勾選。
* 請至完整文件查看本次異動規格
  * 站台管理
    * [郵件伺服器](../../../RTE/SITE/parametermailsetting/README.md)
  * 系統工具(系統參數設定)