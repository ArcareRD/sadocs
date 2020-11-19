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
  * 系統功能
    * [離線](offlinemodeoffline.md)
      * 在連線模式下預載離線資料
    * [登入](offlinemodelogin.md)
      * 在離線模式下核對登入的使用者相同
    * [連線](offlinemodeonline.md)
      * 在離線模式下恢復連線並上傳離線模式時所異動的資料
  * 資料處理
    * [資料傳輸](offlinemodedatatransfer.md)
      * 下載離線模式時會使用的資料
      * 上傳離線模式時異動的資料
    * [表單處理](offlinemodeform.md)
      * 離線模式下的 表單資料 處理
      * 需連線使用的資料或設定皆不可使用
    * [加註處理](offlinemodeattach.md)
      * 離線模式下的 元件加註/按鍵加註 處理
      * 需連線使用的加註或設定皆不可使用
    * [資料交易](offlinemodedatabase.md)
      * 離線模式下的 資料處理
      * 所有異動皆使用本地資料庫
      * 
  * 注意事項
    * 裝置唯一號 IMEI
      * 用來記錄裝置未重覆
      * 只有包含ＳＩＭ卡的裝置才有
      * WIFI版處理方式
        * IOS 使用 identifier，APP移除後會被再安裝會取到不同的唯一碼，因此會視為不同裝置
        * Android 使用 mar address，必需要取得網路授權且必需要連接wifi後才能取得
  * <font style="color:red;">限制</font>
    1. <font style="color:red;">需先下載離線用表單及資料</font>
    2. <font style="color:red;">所有和網路有關的加註及動作和資料均無法使用(例如開網頁或地圖)</font>
    3. <font style="color:red;">離線時所新增的資料在上傳後需手動同步(表單)後才能在連線後使用</font>
