### <div id="view">畫面說明</div>

![表單畫面]

* 本單主要在取得角色的連結URL，日後使用此URL申請帳號，帳號會自動生效並指定到該系統下組織的角色
* 本單由介面.[選單權限建置作業][link_RoleOfPeopleSet]，執行按鈕.取得連結 開啟

## <div id="object-desc">欄位說明</div>

* 欄位.生效系統
    * 本欄唯讀並除能    
    * 顯示 系統名稱
* 欄位.指定組織
    * 本欄唯讀並除能    
    * 顯示 組織名稱
* 欄位.預設角色 
    * 本欄唯讀並除能    
    * 顯示 角色名稱
* 欄位.連結URL
    * 本欄唯讀並除能    
    * 當[組織權限維護作業]未生效，則本欄 不可複製，且執行 Ctrl+V 無效
    * 顯示 網址+參數唯一號。參考下列URL顯示範例:
            https://ide-2.arcare-robot.com/ArcareEng/login.jsp?_=A5CCBF73-A509-42D7-97B0-D6E02DB5363C
* 按鈕.連結失效/連結生效 
    * 當[組織權限維護作業]未生效，則本按鈕 隱藏，否則 顯示
    * 當連結生效，顯示 連結失效，點擊後，將本筆記錄的連結設定為失效
    * 當連結失效，顯示 連結生效，點擊後，將本筆記錄的連結設定為生效  
* 按鈕.複製連結 
    * 當為連結生效，本按鈕致能，反之則除能
    * 點擊後，將欄位.**連結URL**的內容複製到作業系統的剪貼簿中    


### <div id="action">動作流程</div>
* 開啟畫面

    ![link_url_openform]

* 點擊按鈕.連結失效    

    ![link_url_click_invalid]

* 點擊按鈕.連結生效

    ![link_url_click_effective]

* 點擊按鈕.複製連結

    ![link_url_click_copy]


[表單畫面]:attachment/get_role_url.png "表單畫面"
[link_RoleOfPeopleSet]:{3}/RTE/SITE/RoleOfPeopleSet/README

[link_url_openform]:attachment/get_role_url_openform.png "開啟畫面"
[link_url_click_invalid]:attachment/click_url_Invalid.png "點擊連結失效"
[link_url_click_effective]:attachment/click_url_effective.png "點擊連結生效"
[link_url_click_copy]:attachment/click_url_copy.png "點擊複製連結"
