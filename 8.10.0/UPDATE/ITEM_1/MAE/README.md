## <div id="user">規劃人員</div>
  * Andy

## <div id="updatedate">規劃日期</div>
  * 2020/11/09

## <div id="trac">TRAC</div>
  * #8188

### <div id="notification">離線功能</div>
* 目的說明
  * 為了使APP在無法連接到伺服器時可以使用離線表單
* 需求展開
  * 連線功能
    * [離線](offlinemodeoffline.md)
      * 在連線狀態下預載離線資料
  * 離線功能
    * [登入](offlinemodelogin.md)
      * 在離線狀態下確保使用者相同
    * [連線](offlinemodeonline.md)
      * 在離線狀態下恢復連線並上傳離線時所 新增/修改/刪除 的資料
    * [資料傳輸](offlinemodedatatransfer.md)
      * 下載離線資料
      * 上傳離線狀態時 新增/修改/刪除 的資料
    * [表單處理](offlinemodeform.md)
      * 離線模式下顯示表單資料
      * 需連線使用的資料皆不可使用
    * [加註處理](offlinemodeattach.md)
      * 離線模式下執行元件加註/按鍵加註
      * 需連線使用的加註或設定皆不可使用
  * 資料庫功能
    * [資料交易](offlinemodedatabase.md)
      * 離線模式下使用本地資料庫
      * 所有異動皆使用本地資料庫
  * 限制
    1. 需先下載離線用表單及資料
    2. 所有和網路有關的加註及動作和資料均無法使用(例如開網頁或地圖)
    3. 離線時所新增的資料在上傳後需手動同步(表單)後才能在連線後使用
