
### <div id="applogin">MAE登入</div>
* 流程圖
  
    ![image][workflow_login]

* 循序圖

    ![image][sequence_login]

### <div id="applogout">MAE登出</div>
* 流程圖
  
    ![image][workflow_logout]

* 循序圖
  
    ![image][sequence_logout]

### <div id="appbacktofront">MAE背景返回前景</div>
* 說明
  * 當系統狀態為 初始化/維護/刪除 時，不執行此判斷
  * 計時時間設定以收至背景後開始，返回前景時結束，若超過30分鐘時會在背景執行登入
* 流程圖
  
    ![image][workflow_back_to_front]

### <div id="appsystemupgrade">系統更新狀態</div>
* 說明
  * 當系統狀態為更新維護時，顯示訊息且無法返回或登出
  * 當APP從背景返回前景時，檢查系統更新狀態，若更新已結束則返首頁，無首頁時則返回清單。
* 流程圖

    ![image][workflow_upgrade]

<!-- 連結 -->
[sequence_login]:image/sequence_login.png "登入循序圖"
[sequence_logout]:image/sequence_logout.png "登出循序圖"
[workflow_login]:image/workflow_login.png "登入流程圖"
[workflow_logout]:image/workflow_logout.png "登出流程圖"
[workflow_back_to_front]:image/workflow_back_to_front.png "背景返回前景"
[workflow_upgrade]:image/workflow_upgrade.jpg "系統更新狀態"
