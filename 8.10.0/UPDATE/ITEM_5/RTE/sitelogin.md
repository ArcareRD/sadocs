### <div id="user">規劃人員</div>
* Ivan 

### <div id="updatedate">規劃日期</div>
* 2020/12/16

### <div id="trac">TRAC</div>
* #8264

### <div id="sitemanage_2">Site管理登入畫面 <path>(Site管理登入畫面)</path></div>
* 擴充
* 規格說明
    * Site稽核員首次登入需強制變更密碼

* 表單畫面
    | | 畫面 |
    |---|:---:|
    |登入畫面|![SiteLogin]|
    |首次登入|![SiteLogin_PasswordChange]|
* 畫面規格說明
    * 按鈕.登入 : 
        * 登入成功時判斷登入人員為Site稽核員且為首次登入 : 
            * 彈出視窗嵌入表單.密碼變更
            * 彈出視窗關閉時需驗證密碼是否變更 : 
                * 密碼已變更 : 登入至Site首頁
                * 密碼未變更 : 不做任何動作

* 作業流程
    * 開啟Site管理登入畫面

    ![SiteLogin_sa1]
    * 點擊功.登入

    ![SiteLogin_sa2]
    * 點擊功.變更

    ![SiteLogin_sa3]
    * 點擊功.放棄

    ![SiteLogin_sa4]
    * 彈出視窗關閉

    ![SiteLogin_sa5]

<!--超連結引用ps.畫面上看不到-->
[SiteLogin]:img/SiteLogin.jpg
[SiteLogin_PasswordChange]:img/SiteLogin_PasswordChange.jpg
[SiteLogin_sa1]:img/SiteLogin_sa1.jpg
[SiteLogin_sa2]:img/SiteLogin_sa2.jpg
[SiteLogin_sa3]:img/SiteLogin_sa3.jpg
[SiteLogin_sa4]:img/SiteLogin_sa4.jpg
[SiteLogin_sa5]:img/SiteLogin_sa5.jpg