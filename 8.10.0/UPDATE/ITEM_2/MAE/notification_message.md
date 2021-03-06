#### <div id="notification_detail">功能項目名稱</div>
  * 推播訊息顯示

#### <div id="user">規劃人員</div>
  * Andy

#### <div id="version">版本記錄</div>
  |日期|版本|備註|
  |---|---|---|
  |2020/11/06|v1|初始化|

#### <div id="trac">TRAC</div>
  * [#8191](http://trac.uneec.com/trac/neco/ticket/8191)

#### <div id="specification">規格說明</div>
  * 推播訊息顯示
  * 功能
    * 點擊關閉
      * 關閉訊息
    * 點擊遮罩處
      * 關閉訊息
    * 點擊超連結
      * [開啟表單](notification_formlink.md)/[執行按鍵](notification_buttonlink.md)/[內含連結](notification_hyperlink.md)/[加入行事曆](notification_hyperlink.md)
    * 重覆顯示訊息
      * 一次只顯示一個，後單會關閉前單，包含前單開啟的提示訊息
      * 在開啟表單連結的表單情形時可多開啟一個訊息
        * 在點擊第二筆訊息的表單連結後顯示"表單連結不能重覆執行，請關閉前單再至側拉功能項「推播記錄」中開啟"

#### <div id="photo">畫面</div>

  * 表單畫面
    
    ![Notification message](./image/notification_detail.png)

#### <div id="workflow">作業流程</div>

  ![Notification Hyperlink](./image/workflow_hyperlink.png)