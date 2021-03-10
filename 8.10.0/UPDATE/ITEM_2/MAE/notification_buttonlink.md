#### <div id="notification_form_link">功能項目名稱</div>
  * 按鍵連結

## <div id="user">規劃人員</div>
  * Andy

#### <div id="version">版本記錄</div>
  |日期|版本|備註|
  |---|---|---|
  |2020/11/06|v1|初始化|

## <div id="trac">TRAC</div>
  * [#8191](http://trac.uneec.com/trac/neco/ticket/8191)

#### <div id="specification">規格說明</div>
  * 以推播資料所包含的唯一號，和伺服器取得按鍵資訊，再經過驗證使用者無誤後，呼叫相關API取得結果並顯示
  * 執行結果
    * 成功
      * 有設定成功訊息
        * 顯示成功訊息
      * 未設定成功訊息
        * 顯示"按鍵執行成功"
    * 失敗
      * 有設定失敗訊息
        * 顯示失敗訊息
      * 未設定失敗訊息
        * 顯示"執行失敗"

#### <div id="workflow">作業流程</div>

  * 超連結處理
  
  ![Notification form link](./image/workflow_hyperlink.png)

  * 超連結按鍵處理
  
  ![Notification button link](./image/workflow_buttonlink.png)
