### <div id="user">規劃人員</div>
* 正傑

### <div id="updatedate">規劃日期</div>
* 2020/11/09

### <div id="trac">TRAC</div>
* 待開

### <div id="pushmessage_1">推播通知 <path>(按鍵加註)</path></div>
發送推播通知給MAE

### <div id="pushmessage_condition">執行條件 <path>(按鍵加註\推播通知)</path></div>
以`執行內容`的結果來決定是否要執行該推播通知

### <div id="pushmessage_condition_content">執行內容 <path>(按鍵加註\推播通知\執行條件)</path></div>
若`執行內容`結果未通過，表示該推播通知不執行。

### <div id="pushmessage_condition_message">訊息處理 <path>(按鍵加註\推播通知\執行條件)</path></div>
若`執行內容`結果未通過時需彈出的錯誤訊息。

### <div id="pushmessage_source">推播人 <path>(按鍵加註\推播通知)</path></div>
推播人類型
* `管理者` : 訊息推播時，顯示系統發送 (待討論)
* `使用者` : 訊息推播時，顯示執行使用者名稱

### <div id="pushmessage_content">主旨內文 <path>(按鍵加註\推播通知)</path></div>
推播通知的訊息內文，可在`內文`中撰寫替換字，再設定`替代變數表格`，運行時會將內文進行替換的動作。

### <div id="pushmessage_content_source">來源 <path>(按鍵加註\推播通知\主旨內文)</path></div>
是否需查表，共有以下類型 : 
* `無` : 表示內文無資料來源可供查詢或替換。
* `查表` : 表示內文可依據`檢視表`加上`過濾`後的結果查詢到資料，用來做替換字來源用。

### <div id="pushmessage_content_view">檢視表 <path>(按鍵加註\推播通知\主旨內文)</path></div>
`內文`可指定的資料來源

### <div id="pushmessage_content_filter">過濾 <path>(按鍵加註\推播通知\主旨內文)</path></div>
`檢視表`可指定的過濾條件

### <div id="pushmessage_content_title">主旨 <path>(按鍵加註\推播通知\主旨內文)</path></div>
紀錄推播通知的標題

### <div id="pushmessage_content_body">內文 <path>(按鍵加註\推播通知\主旨內文)</path></div>
紀錄推播通知的內容，可在此寫訊息內容，若內文有需要進行替換字處理，可填寫`替代變數表格`進行替換。

### <div id="pushmessage_content_replace">替代變數表格 <path>(按鍵加註\推播通知\主旨內文)</path></div>
紀錄推播通知針對`內文`的替換字清單。
如 : `內文`中有%AAA%，`替換字變數`也有一個變數叫做AAA，運行時就會將此筆資料的`來源欄位`內容替換掉內文的%AAA%。

### <div id="pushmessage_content_replace_variable">替換字變數 <path>(按鍵加註\推播通知\主旨內文\替代變數表格)</path></div>
紀錄推播通知的替換字變數名稱。

### <div id="pushmessage_content_replace_type">類別 <path>(按鍵加註\推播通知\主旨內文\替代變數表格)</path></div>
替換字變數的替換類別，共有以下幾種 :
* `推播來源欄位`
* `表單元件`
* `表單參數`
* `全域變數`
* `通知來源欄位`

### <div id="pushmessage_content_replace_source">來源欄位 <path>(按鍵加註\推播通知\主旨內文\替代變數表格)</path></div>
替換字變數的替換值
* 依照`類別`
    * `推播來源欄位` : `主旨內文`資料來源的欄位值。
    * `表單元件` : `表單元件` / `隱藏表單元件`。
    * `表單參數` : `表單`的`接收參數`。
    * `全域變數` : `全域變數`。
    * `通知來源欄位` : `通知對象`資料來源的欄位值。

### <div id="pushmessage_content_link-type">連結類別 <path>(按鍵加註\推播通知\主旨內文)</path></div>
推播通知超連結的類型，共有以下幾種 :
* `超連結表單`
* `超連結按鍵`
* `超連結Google行事曆`

### <div id="pushmessage_content_link-body">連結內容 <path>(按鍵加註\推播通知\主旨內文)</path></div>
超連結內容資訊
* 依照`連結類別`
    * `超連結表單` : 點擊後開啟一張指定的MAE表單
    * `超連結按鍵` : 點擊後執行一個指定的功能按鍵
    * `超連結Google行事曆` : 點擊後開啟Google行事曆網頁

### <div id="pushmessage_content_link-save">儲存連結資訊 <path>(按鍵加註\推播通知\主旨內文)</path></div>
推播通知的超連結設定資訊可依此設定在執行此功能按鍵的時候，將超連結資訊儲存至資料表。

### <div id="pushmessage_content_link-save_table">寫入資料表 <path>(按鍵加註\推播通知\主旨內文\儲存連結資訊)</path></div>
存放超連結設定的資料表

### <div id="pushmessage_content_link-save_passport">通行碼 <path>(按鍵加註\推播通知\主旨內文\儲存連結資訊)</path></div>
挑選存放MAE超連結通行碼的欄位

### <div id="pushmessage_content_link-save_info">額外寫入欄位表格 <path>(按鍵加註\推播通知\主旨內文\儲存連結資訊)</path></div>
若有額外需要寫入的資訊，可透過此表格進行設定。

### <div id="pushmessage_content_link-save_target">其他目的欄位 <path>(按鍵加註\推播通知\主旨內文\儲存連結資訊\額外寫入欄位表格)</path></div>
額外再寫`寫入資料表`包含的欄位

### <div id="pushmessage_content_link-save_type">給值類別 <path>(按鍵加註\推播通知\主旨內文\儲存連結資訊\額外寫入欄位表格)</path></div>
額外寫入`其他目的欄位`的給值類型 :
* `推播來源欄位`
* `表單元件`
* `表單參數`
* `全域變數`
* `通知者使用序號`
* `替換字變數`

### <div id="pushmessage_content_link-save_value">給值內容 <path>(按鍵加註\推播通知\主旨內文\儲存連結資訊\額外寫入欄位表格)</path></div>
額外寫入`其他目的欄位`的給值內容
* 依照`給值類別`
    * `推播來源欄位` : 表示寫入的欄位資料為`主旨內文`資料來源的欄位值。
    * `表單元件` : `表單元件` / `隱藏表單元件`。
    * `表單參數` : `表單`的`接收參數`。
    * `全域變數` : `全域變數`。
    * `通知者使用序號` : `通知對象`的使用者序號。
    * `替換字變數` : `替換字變數`的內容。

### <div id="pushmessage_target">通知對象 <path>(按鍵加註\推播通知)</path></div>
推播訊息發送對象的設定

### <div id="pushmessage_target_source">來源 <path>(按鍵加註\推播通知\通知對象)</path></div>
(待補)

### <div id="pushmessage_target_view">檢視表 <path>(按鍵加註\推播通知\通知對象)</path></div>
(待補)

### <div id="pushmessage_target_filter">過濾 <path>(按鍵加註\推播通知\通知對象)</path></div>
(待補)

### <div id="pushmessage_target_userid">使用者序號 <path>(按鍵加註\推播通知\通知對象)</path></div>
(待補)

### <div id="pushmessage_info">推播資訊 <path>(按鍵加註\推播通知)</path></div>
提供額外寫入推播資訊的功能

### <div id="pushmessage_info_error">發送異常 <path>(按鍵加註\推播通知\推播資訊)</path></div>
發送推播訊息異常時，是否還繼續執行`推播儲存資訊` :
* `忽略` : 忽略發送成功或失敗，繼續執行。
* `停止` : 發送異常時停止執行。

### <div id="pushmessage_info_save">推播儲存資訊 <path>(按鍵加註\推播通知\推播資訊)</path></div>
推播通知的推播資訊可依此設定在執行此功能按鍵的時候，將推播資訊儲存至資料表。

### <div id="pushmessage_info_save_table">寫入資料表 <path>(按鍵加註\推播通知\推播資訊\推播儲存資訊)</path></div>
存放推播資訊的資料表

### <div id="pushmessage_info_save_result">推播發送結果 <path>(按鍵加註\推播通知\推播資訊\推播儲存資訊)</path></div>
寫入推播發送的結果到該欄位

### <div id="pushmessage_info_save_info">額外寫入欄位表格 <path>(按鍵加註\推播通知\推播資訊\推播儲存資訊)</path></div>
若有額外需要寫入的資訊，可透過此表格進行設定。

### <div id="pushmessage_info_save_info_target">其他目的欄位 <path>(按鍵加註\推播通知\推播資訊\推播儲存資訊\額外寫入欄位表格)</path></div>
額外再寫`寫入資料表`包含的欄位

### <div id="pushmessage_info_save_info_type">給值類別 <path>(按鍵加註\推播通知\推播資訊\推播儲存資訊\額外寫入欄位表格)</path></div>
額外寫入`其他目的欄位`的給值類型 :
* `推播來源欄位`
* `表單元件`
* `表單參數`
* `全域變數`
* `推播發送失敗原因`

### <div id="pushmessage_info_save_info_value">給值內容 <path>(按鍵加註\推播通知\推播資訊\推播儲存資訊\額外寫入欄位表格)</path></div>
額外寫入`其他目的欄位`的給值內容
* 依照`給值類別`
    * `推播來源欄位` : 表示寫入的欄位資料為`主旨內文`資料來源的欄位值。
    * `表單元件` : `表單元件` / `隱藏表單元件`。
    * `表單參數` : `表單`的`接收參數`。
    * `全域變數` : `全域變數`。
    * `推播發送失敗原因` : 推播發送失敗的錯誤訊息。