### <div id="view">畫面說明</div>
* 在PC呈現的畫面如下

    ![登入畫面]

* 在行動裝置呈現的畫面如下

    ![登入畫面行動裝置]

* 登入畫面也可在[站台管理表單.系統自訂版面]()上傳客製的畫面。
* 其餘待補

### <div id="account">帳號 <path>(畫面說明)</path></div>
* 未輸入時顯示提示文字【帳號】，有輸入後提示文字消失。
* 駐留欄位後，按鍵盤ENTER會檢控帳號/密碼不可為空，若有啟用驗證碼，則額外檢控驗證碼不可為空，檢控通過後進行登入流程(等同於點擊按鈕.登入)。

### <div id="password">密碼 <path>(畫面說明)</path></div>
* 未輸入時顯示提示文字【密碼】，有輸入後提示文字消失
* 駐留欄位後，按鍵盤ENTER會檢控帳號/密碼不可為空，若有啟用驗證碼，則額外檢控驗證碼不可為空，檢控通過後進行登入流程(等同於點擊按鈕.登入)。
* 點擊按鈕.顯示會顯示使用者輸入的密碼。

### <div id="captcha">驗證碼 <path>(畫面說明)</path></div>
* 由[站台管理表單.其他參數](../../SITE/otherparameter/README.md)的登入相關設定啟用驗證碼
* 未輸入時顯示提示文字【驗證碼】，有輸入後提示文字消失。
* 駐留欄位後，按鍵盤ENTER會檢控帳號/密碼/驗證碼不可為空，檢控通過後進行登入流程(等同於點擊按鈕.登入)。

### <div id="forgetpassword">忘記密碼 <path>(畫面說明)</path></div>
* 待補

### <div id="applyaccount">申請帳號 <path>(畫面說明)</path></div>
* 當瀏覽器的連結網址存在帳號生效參數設定的唯一號，即使Site系統服務介面.**其他參數**的欄位.**開放帳號申請**未勾選，畫面仍顯示**申請新帳號**的連結
* 開啟表單.[申請帳號](../APPLYACCOUNT/README.md)

### <div id="login">登入 <path>(畫面說明)</path></div>
* 若有啟用驗證碼，當帳號/密碼/驗證碼都有輸入值時，按鈕.登入顯示為致能
* 若未啟用驗證碼，當帳號/密碼都有輸入值時，按鈕.登入顯示為致能
* 點擊按鈕.登入後執行登入驗證
    * 登入成功時依據以下原則決定轉跳的首頁
        * 若為行動裝置，則跳至行動裝置首頁
        * 若為PC，依據由[站台管理表單.其他參數](../../SITE/otherparameter/README.md)的新版首頁樣式來決定跳至新版首頁或舊版首頁
    * 登入失敗則依照錯誤顯示訊息視窗
* 其餘待補

### <div id="action">作業流程</div>
* 顯示登入畫面

    ![開啟畫面]

* 欄位.帳號鍵盤輸入ENTER

    ![欄位.帳號鍵盤輸入ENTER]

* 欄位.密碼鍵盤輸入ENTER

    ![欄位.密碼鍵盤輸入ENTER]

* 欄位.驗證碼鍵盤輸入ENTER

    ![欄位.驗證碼鍵盤輸入ENTER]

* 點擊按鈕.登入

    ![點擊按鈕.登入]

* 登入驗證流程

    ![登入驗證]

* 其餘待補

[登入畫面]:attachment/login.png "登入畫面"
[登入畫面行動裝置]:attachment/loginmobile.png "登入畫面行動裝置"
[開啟畫面]:attachment/login_open.png "開啟畫面"
[欄位.帳號鍵盤輸入ENTER]:attachment/accountenter.png "欄位.帳號鍵盤輸入ENTER"
[欄位.密碼鍵盤輸入ENTER]:attachment/passwordenter.png "欄位.密碼鍵盤輸入ENTER"
[欄位.驗證碼鍵盤輸入ENTER]:attachment/captchaenter.png "欄位.驗證碼鍵盤輸入ENTER"
[點擊按鈕.登入]:attachment/clicklogin.png "點擊按鈕.登入"
[登入驗證]:attachment/loginverify.png "登入驗證"