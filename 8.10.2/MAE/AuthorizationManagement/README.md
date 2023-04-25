# 授權管理

* #### 登入系統

  * RTE站台的系統授權期間，登入時會跳出提示訊息
    * 前期前一個月間顯示<span style="color:blue">"系統即將過期，請儘速聯絡系統管理員!"</span>
    * 到期後一個月間顯示<span style="color:blue">"系統已過期，請儘速聯絡系統管理員!"</span>
    * 超過期限後則顯示<span style="color:blue">"系統已過期，請聯絡系統管理員!"</span><span style="color:red">且無法登入該站台</span>
  * 流程圖

    ![image](../Image/authorization_login_system.jpg)

* #### 登入站台

  * RTE站台的站台授權期間，登入時會跳出提示訊息
    * 到期前一個月間顯示<span style="color:blue">"站台即將過期，請儘速聯絡系統管理員!"</span>
    * 到期後一個月間顯示<span style="color:blue">"站台已過期，請儘速聯絡系統管理員!"</span>
    * 超過期限後則顯示<span style="color:blue">"站台已過期，請聯絡系統管理員!"</span><span style="color:red">且無法登入該系統</span>
  * 流程圖

    ![image](../Image/authorization_login_platform.jpg)

* #### 背景返回前景

  * 依RTE站台的授權期限來判斷顯示提示訊息
    * 當<span style="color:red">系統</span>到期前一個月間
      * 當<span style="color:red">站台</span>到期前一個月間
        * 顯示<span style="color:blue">"系統與站台即將過期，請儘速聯絡系統管理員!"</span>
      * 當<span style="color:red">站台</span>到期後一個月間
        * 顯示<span style="color:blue">"系統即將過期且站台已過期，請儘速聯絡系統管理員!"</span>
      * 當<span style="color:red">站台</span>超過期限
        * 顯示<span style="color:blue">"站台已過期，請聯絡系統管理員!"</span><span style="color:red">且返回站台登入畫面</span>
    * 當<span style="color:red">系統</span>到期後一個月間
      * 當<span style="color:red">站台</span>到期前一個月間
        * 顯示<span style="color:blue">"系統已過期且站台即將過期，請儘速聯絡系統管理員!"</span>
      * 當<span style="color:red">站台</span>到期後一個月間
        * 顯示<span style="color:blue">"系統與站台已過期，請儘速聯絡系統管理員!"</span>
      * 當<span style="color:red">站台</span>超過期限
        * 顯示<span style="color:blue">"站台已過期，請聯絡系統管理員!"</span><span style="color:red">且返回站台登入畫面</span>
    * 當<span style="color:red">系統</span>超過期限
      * 顯示<span style="color:blue">"系統已過期，請聯絡系統管理員!"</span><span style="color:red">且返回系統登入畫面</span>
  * 流程圖

    ![image](../Image/authorization_background_to_foreground.jpg)

* 完整網站規劃連結 : [授權中心網站](../../../LICENSE/README.md)
