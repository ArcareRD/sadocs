# 授權管理

* #### 登入站台

  * RTE站台的站台授權期間，登入時會跳出提示訊息
    * 授權到期日為30天內時顯示<span style="color:blue">"站台授權剩餘XX天將到期，請儘速聯絡系統管理員!"</span>
    * 授權到期但還在為30天內的寬限期內時顯示<span style="color:blue">"站台授權已到期，寬限期剩餘XX天，請儘速聯絡系統管理員!"</span>
    * 授權到期後則顯示<span style="color:blue">"站台授權已到期，無法登入，請聯絡系統管理員!"</span><span style="color:red">且無法登入該站台</span>
  * 流程圖

    ![image](../Image/authorization_login_platform.jpg)

* #### 登入系統

  * RTE站台的系統授權期間，登入時會跳出提示訊息
    * 授權到期日為30天內時顯示<span style="color:blue">"系統授權剩餘XX天將到期，請儘速聯絡系統管理員!"</span>
    * 授權到期但還在為30天內的寬限期內時顯示<span style="color:blue">"系統授權已到期，寬限期剩餘XX天，請儘速聯絡系統管理員!"</span>
    * 授權到期後則顯示<span style="color:blue">"系統授權已到期，無法登入，請聯絡系統管理員!"</span><span style="color:red">且無法登入該系統</span>
  * 流程圖

    ![image](../Image/authorization_login_system.jpg)

* #### 背景返回前景

  * 依RTE站台的授權期限來判斷顯示提示訊息
    * 當<span style="color:red">站台</span>授權到期日為30天內時
      * 當<span style="color:red">系統</span>授權到期日為30天內時
        * 顯示<span style="color:blue">"站台授權剩餘XX天將到期且系統授權剩餘XX天將到期，請儘速聯絡系統管理員!"</span>
      * 當<span style="color:red">系統</span>到期後但還在30天內的寬限期內時
        * 顯示<span style="color:blue">"站台授權剩餘XX天將到期且系統授權已到期，寬限期剩餘XX天，請儘速聯絡系統管理員!"</span>
      * 當<span style="color:red">系統</span>授權到期後
        * 顯示<span style="color:blue">"系統授權已到期，無法登入，請聯絡系統管理員!"</span><span style="color:red">且返回系統登入畫面</span>
    * 當<span style="color:red">站台</span>到期後但還在30天內的寬限期內時
      * 當<span style="color:red">系統</span>授權到期日為30天內時
        * 顯示<span style="color:blue">"站台授權已到期，寬限期剩餘XX天且系統授權剩餘XX天將到期，請儘速聯絡系統管理員!"</span>
      * 當<span style="color:red">系統</span>到期後但還在30天內的寬限期內時
        * 顯示<span style="color:blue">"站台授權已到期，寬限期剩餘XX天且系統授權已到期，寬限期剩餘XX天，請儘速聯絡系統管理員!"</span>
      * 當<span style="color:red">系統</span>授權到期後
        * 顯示<span style="color:blue">"系統授權已到期，無法登入，請聯絡系統管理員!"</span><span style="color:red">且返回系統登入畫面</span>
    * 當<span style="color:red">站台</span>授權到期後
      * 顯示<span style="color:blue">"站台已過期，請聯絡系統管理員!"</span><span style="color:red">且返回站台登入畫面</span>
  * 流程圖

    ![image](../Image/authorization_background_to_foreground.jpg)

* 完整網站規劃連結 : [授權中心網站](../../../LICENSE/README.md)
