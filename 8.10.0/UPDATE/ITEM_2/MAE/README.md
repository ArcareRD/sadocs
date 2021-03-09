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
    * [APP ICON Badge](notification_icon.md)
      * 當有未讀訊息時顯示小圓點在APP ICON的右上方
    * [系統管理](notification_system.md)
      * 利用firebase的推播功能來通知使用者
      * 推播通知([推播通知問題需知](device_setting.md))
        * 在逹成以下條件後，使用者便可接收到 MAE 的通知訊息
          1. 安裝MAE
          2. 使用者第一次登入
        * 背景通知(未執行或APP被關閉時)
          * 在已可接收到 MAE 的通知訊息下需要設定成主要裝置才可以在背景接收到通知
      * 主裝置設定
        * 設定主裝置
        * 設定主裝置說明
        * 登入時不再詢問
    * [打樣](notification_prototyping.md)
      * 主裝置設定
        * 登入時不再詢問
        * 設定主裝置
    * [表單連結](notification_formlink.md)
      * 依設計者設定可開啟特定表單
    * [按鍵連結](notification_buttonlink.md)
      * 依設計者設定可執行特定表單的按鍵
    * [超連結](notification_hyperlink.md)
      * 依設計者設定可開啟特定網頁(含 google 行事曆)
    * [推播記錄](notification_record.md)
      * 使用者可以查看所有使用者的推播歷史記錄
    * [推播訊息](notification_message.md)
      * 使用者可以查看查看詳細訊息並可以執行相對應連結
    * [按鍵加註](notification_buttonlink.md)
      * 點擊按鍵後依加註來傳送通知

