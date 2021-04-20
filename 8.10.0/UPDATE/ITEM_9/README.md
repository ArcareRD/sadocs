# 擴充MAE伺服器清單列表

### <div id="user">規劃人員</div>
* Andy

#### <div id="version">版本記錄</div>
  |日期|版本|備註|
  |---|---|---|
  |2021/4/12|v1|初始化|

### <div id="trac">TRAC</div>

#### <div id="specification">規格說明</div>

* 可記錄多筆伺服器設定及各伺服器的名稱和各伺服器的登入帳密

### <div id="specification">功能說明</div>
  * 需求展開  
    * 新增伺服器
      * 新增可連線的伺服器
      * 預設名稱"未命名"
      * 預設網址"https://xxxx.arcare-robot.com"
        * 可手動輸入/QRCode輸入
      * 預設未勾選"設定為使用中"
      * 無使用中的伺服器的狀態下會直接顯示新增伺服器畫面
    * 設定(修改伺服器)
      * 可修改名稱/網址/使用中
      * 正在使用中的伺服器不可取消使用中
    * 更換伺服器/設定伺服器
      * 可切換伺服器
      * 正在使用中的伺服器無須切換
    * 刪除伺服器
      * 可刪除列表中的伺服器
      * 正在使用中的伺服器不可刪除
    * 登入狀態記錄
      * 可記錄登入帳密及記錄勾選設定，一個伺服器只記錄一組

#### <div id="photo">畫面</div>
  * 伺服器清單
  
    ![Servrer List](./image/server_list.jpg)

  * 新增伺服器
  
    ![Servrer Add](./image/server_add.jpg)

  * 設定伺服器(修改伺服器)
  
    ![Servrer Edit](./image/server_edit.jpg)

  * 更換伺服器
  
    ![Servrer Change](./image/server_change.jpg)

  * 刪除伺服器
  
    ![Servrer Delete](./image/server_delete.jpg)

  * 功能項目(無設定伺服器)
  
    ![Servrer List Menu Not Set](./image/server_list_menu_not_set.jpg)

  * 功能項目(已設定伺服器)
  
    ![Servrer List Menu Set](./image/server_list_menu_set.jpg)

  * 功能項目(未設定伺服器)
  
    ![Servrer List Menu Unset](./image/server_list_menu_unset.jpg)

  * 返回(無伺服器)
  
    ![Servrer List no data](./image/server_list_no_data.jpg)

  * 返回(未設定伺服器)
  
    ![Servrer List not set](./image/server_list_not_set.jpg)

  * 記錄登入帳密(紅框處)

    ![Servrer Account Password](./image/server_account_password.jpg)

#### <div id="workflow">作業流程</div>
  * 伺服器清單
  
    ![Servrer List](./image/workflow_server_list.png)

  * 伺服器清單功能
  
    ![Servrer List Function](./image/workflow_server_list_function.png)