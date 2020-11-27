#### <div id="notification">功能項目名稱</div>
  * 推播通知

#### <div id="user">規劃人員</div>
  * Andy

#### <div id="version">版本記錄</div>
  |日期|版本|備註|
  |---|---|---|
  |2020/11/06|v1|初始化|

#### <div id="trac">TRAC</div>
  * [#8191](http://trac.uneec.com/trac/neco/ticket/8191)

#### <div id="specification">規格說明</div>
  * 需求展開
    * APP ICON Badge
      * 當有未讀訊息時顯示小圓點在APP ICON的右上方
    * 系統管理
      * 利用firebase的推播功能來通知使用者
      * 背景通知
        * 在逹成以下條件後，使用者可在未開啟MAE時接收到通知訊息
          1. 安裝MAE
          2. 使用者第一次登入
          3. 設定成主要裝置
    * 表單連結
      * 依設計者設定可開啟特定表單
    * 按鍵連結
      * 依設計者設定可執行特定表單的按鍵
    * 超連結
      * 依設計者設定可開啟特定網頁(含 google 行事曆)
    * 推播記錄
      * 使用者可以查看所有使用者的推播歷史記錄
    * 推播訊息
      * 使用者在查看訊息頁面可以執行相對應連結
    * 按鍵加註
      * 點擊按鍵後依加註來傳送通知

#### <div id="attachment">附件</div>
  * 注意事項
    * 裝置唯一號 IMEI
      * 用來記錄裝置未重覆
      * 只有能安插ＳＩＭ卡的裝置才有
      * WIFI版處理方式
        * IOS 使用 identifier，APP移除後會被再安裝會取到不同的唯一碼，因此會視為不同裝置
        * Android 使用 mar address，必需要取得網路授權且必需要連接wifi後才能取得
  * 限制
    * 裝置
      * Android：5.0 或更高版本
      * iOS：10.0 或更高版本
<!--  * 大小 * 所有資訊合計不可超過4k bytes -->
