### <div id="view">畫面說明</div>
* 表單畫面

    ![表單畫面]

* 本表單主要在在設定企業相關資料，有以下兩種開啟方式
    * 站台管理員在表單.企業設定，點擊按鈕.新增企業或點擊按鈕.修改企業進行開啟本表單。
    * 企業管理員在站台管理首頁的表單選單可看到本表單並點擊開啟。

### <div id="basic">企業基本資料 <path>(畫面說明)</path></div>
* 企業資料
    * 欄位.企業代碼 : 不可空白，表示該企業的代碼。
    * 欄位.公司名稱(當地) : 不可空白，表示該企業的名稱。
    * 欄位.統一編號/稅籍碼 : 可空白，表示該企業的統一編號或稅籍碼。
    * 欄位.國別代碼 : 不可空白，為下拉選項，選項內容為表單.國別設定之內容。
    * 欄位.公司電話代表號 : 可空白，為該企業的電話代表號。
    * 欄位.電話國碼 : 可空白，為該企業的電話國別代碼。
    * 欄位.收費聯絡人姓名 : 不可空白，為該企業的收費聯絡人姓名。
    * 欄位.負責人姓名 : 可空白，為該企業的負責人姓名。
    * 欄位.公司地址 : 可空白，為該企業的公司地址。
    * 欄位.公司英文名 : 不可空白，為該企業的公司英文名。
    * 欄位.企業Manager : 可空白，開窗挑選企業帳號，為該企業的企業管理員。
    * 欄位.同時最大上線人數 : 不可空白，為該企業可同時上線最大人數，預設給0，表示無上限。
    * 欄位.Google API Key : 可空白，為該企業內使用系統若有呼叫Google地圖，則會使用這把Google API Key進行開啟地圖的動作。
    * 欄位.郵件驗證碼等待時間(秒) : 
        * 不可空白
        * 本欄只允輸入數字
        * 系統預設: **300** 
        * 檢控: 最小輸入值 **60**
    * 按鈕.儲存 : 點擊後將依據各欄位可空白否進行檢控，檢控失敗顯示錯誤訊息，若檢控成功則將表單所有資料進行儲存的動作。
    * 按鈕.放棄 : 點擊後關閉表單.企業資料。

### <div id="style">企業LOGO相關 <path>(畫面說明)</path></div>
* 企業LOGO : 使用者登入首頁後，依據設定顯示於首頁的左上角。
    * 欄位.LOGO檔案：
        * 唯讀
        * 有上傳圖檔時，顯示圖片檔案名稱(含副檔名)
    * 功能鍵.上傳：
        * 開啟檔案總管挑選圖片
        * 上傳後欄位.LOGO顯示圖片檔案名稱(含副檔名)
        * 上傳後欄位.預覽結果顯示圖片縮圖
    * 功能鍵.下載：
        * 未上傳LOGO檔案 時除能
        * 下載已上傳的LOGO檔案
    * 功能鍵.恢復系統預設：
        * 未上傳LOGO檔案 時除能
        * 刪除已上傳的LOGO檔案
        * 刪除後清空欄位.LOGO
        * 刪除後清空欄位.預覽結果

### <div id="homepage">企業首頁樣式 <path>(畫面說明)</path></div>
* 新版首頁樣式
    * 欄位.新版首頁壓縮檔：
        * 唯讀
        * 有上傳新版首頁壓縮檔時，顯示檔案名稱(含副檔名)
    * 按鈕.恢復系統預設
        * 當已有上傳自訂新版首頁時致能，否則除能。
        * 執行後，移除自訂的新版首頁，恢復成預設新版首頁。
    * 按鈕.下載
        * 無除致能條件
        * 執行後，若已有自訂新版首頁，則下載自訂新版首頁，若無則下載預設新版首頁。
            * 若為預設新版首頁，則下載的ZIP檔案中包含以下項目:
                * homepage.css : 首頁css樣式檔
                * account-circle.png : 帳號資料圖示
                * sysbtn.png : 系統功能鍵列圖示
            * 若為自訂新版首頁，則下載企業管理員上傳的自訂樣式ZIP檔案。
    * 按鈕.上傳
        * 無除致能條件
        * 執行後，跳出上傳檔案的視窗，讓使用者進行上傳自訂樣式的ZIP檔案。

* 行動裝置版首頁樣式
    * 欄位.行動裝置首頁壓縮檔：
        * 唯讀
        * 有上傳行動裝置首頁壓縮檔時，顯示檔案名稱(含副檔名)
    * 按鈕.恢復系統預設
        * 當已有上傳自訂行動裝置版首頁時致能，否則除能。
        * 執行後，移除自訂的行動裝置版首頁，恢復成預設行動裝置版首頁。
    * 按鈕.下載
        * 無除致能條件
        * 執行後，若已有自訂行動裝置版首頁，則下載自訂行動裝置版首頁，若無則下載預設行動裝置版首頁。
            * 執行後，若已有自訂行動裝置版首頁，則下載自訂行動裝置版首頁，若無則下載預設行動裝置版首頁。
            * 若為預設行動裝置版首頁，則下載的ZIP檔案中包含以下項目:
                * homepage.css : 首頁css樣式檔
                * sysbtn.png : 系統功能鍵列圖示
            * 若為自訂行動裝置版首頁，則下載企業管理員上傳的自訂樣式ZIP檔案。
    * 按鈕.上傳
        * 無除致能條件
        * 執行後，跳出上傳檔案的視窗，讓使用者進行上傳自訂樣式的ZIP檔案。

### <div id="action">動作流程</div>
* 站台管理員開啟畫面

    ![站台管理員開啟畫面]

* 企業管理員開啟畫面

    ![企業管理員開啟畫面]

* 企業LOGO
    * 點擊按鈕.恢復系統預設

        ![點擊按鈕.恢復系統預設(LOGO檔案)]

    * 點擊按鈕.下載

        ![點擊按鈕.下載(LOGO檔案)]

    * 點擊按鈕.上傳

        ![點擊按鈕.上傳(LOGO檔案)]

* 新版首頁
    * 點擊按鈕.恢復系統預設

        ![點擊按鈕.恢復系統預設(新版首頁)]

    * 點擊按鈕.下載

        ![點擊按鈕.下載目前樣式(新版首頁)]

    * 點擊按鈕.上傳

        ![點擊按鈕.上傳自訂樣式(新版首頁)]

* 行動裝置版首頁
    * 點擊按鈕.恢復系統預設

        ![點擊按鈕.恢復系統預設(行動裝置版首頁)]

    * 點擊按鈕.下載

        ![點擊按鈕.下載目前樣式(行動裝置版首頁)]

    * 點擊按鈕.上傳

        ![點擊按鈕.上傳自訂樣式(行動裝置版首頁)]

* 點擊按鈕.儲存

    ![點擊按鈕.儲存]

* 點擊按鈕.取消

    ![點擊按鈕.取消]

[表單畫面]:attachment/enterprisedetail_view.png "表單畫面"
[企業管理員開啟畫面]:attachment/enterprisemanager_openform.png "企業管理員開啟畫面"
[站台管理員開啟畫面]:attachment/sitemanager_openform.png "站台管理員開啟畫面"
[點擊按鈕.恢復系統預設(新版首頁)]:attachment/click_recover_default_new.png "點擊按鈕.恢復系統預設(新版首頁)"
[點擊按鈕.下載目前樣式(新版首頁)]:attachment/click_download_new.png "點擊按鈕.下載目前樣式(新版首頁)"
[點擊按鈕.上傳自訂樣式(新版首頁)]:attachment/click_upload_new.png "點擊按鈕.上傳自訂樣式(新版首頁)"
[點擊按鈕.恢復系統預設(行動裝置版首頁)]:attachment/click_recover_default_mobile.png "點擊按鈕.恢復系統預設(行動裝置版首頁)"
[點擊按鈕.下載目前樣式(行動裝置版首頁)]:attachment/click_download_mobile.png "點擊按鈕.下載目前樣式(行動裝置版首頁)"
[點擊按鈕.上傳自訂樣式(行動裝置版首頁)]:attachment/click_upload_mobile.png "點擊按鈕.上傳自訂樣式(行動裝置版首頁)"
[點擊按鈕.恢復系統預設(LOGO檔案)]:attachment/click_recover_default_logo.png "點擊按鈕.恢復系統預設(LOGO檔案)"
[點擊按鈕.下載(LOGO檔案)]:attachment/click_download_logo.png "點擊按鈕.下載(LOGO檔案)"
[點擊按鈕.上傳(LOGO檔案)]:attachment/click_upload_logo.png "點擊按鈕.上傳(LOGO檔案)"
[點擊按鈕.儲存]:attachment/click_save.png "點擊按鈕.儲存"
[點擊按鈕.取消]:attachment/click_cancel.png "點擊按鈕.取消"