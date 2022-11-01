### <div id="view">畫面說明</div>

![表單畫面]

* 本單主要在設定各系統下組織的選單、表單及角色權限，並依角色設定保密欄位

## <div id="object-desc">欄位說明</div>

* 按鈕.刪除
    * 刪除權限時，須依 **系統+組織+角色** 將對應的 [取得連結][link_getRoleURL] 資料一併刪除
* 按鈕.生效
    * 取得目前生效的權限，進行 **失效**，並執行下列動作:    
        * <ps>待補原規格</ps>
        * 當權限失效時，須依 **系統+組織+角色** 將對應的 [取得連結][link_getRoleURL] 資料進行連結失效 
    * 取得駐留筆權限，進行 **生效**，並執行下列動作:
        * <ps>待補原規格</ps>
        * 權限生效時，須依 **系統+組織+角色** 將對應的 [取得連結][link_getRoleURL] 資料進行連結生效
    

## <div id="schedule">排程說明</div>

* 每日00時00分00秒，檢查是否有各系統下的組織，是否有權限到期要進行生效
* 排程工作內容如下:
    * 查詢目前生效的權限，進行 **失效**，並執行下列動作:    
        * <ps>待補原規格</ps>
        * 當權限失效時，須依 **系統+組織+角色** 將對應的 [取得連結][link_getRoleURL] 資料進行連結失效 
    * 今日即將生效的權限，進行 **生效**，並執行下列動作:
        * <ps>待補原規格</ps>
        * 權限生效時，須依 **系統+組織+角色** 將對應的 [取得連結][link_getRoleURL] 資料進行連結生效    

### <div id="action">動作流程</div>
* <ps>待補</ps>


[表單畫面]:attachment/list_of_permissions.png "表單畫面"
[link_getRoleURL]:{3}/RTE/SITE/getRoleURL/README