### <div id="valid">執行條件</div>

### <div id="query">視窗內容</div>
按下 <rte>系統功能鍵.查詢視窗</rte>，會開啟對應的功能。

### <div id="form">開啟表單 <path>(視窗內容)</path></div>
開啟表單，選取記錄帶回。<ic>(FW0000002946)(ENG.參照勾選)</ic>

### <div id="form_form">表單名稱 <path>(視窗內容\開啟表單)</path></div>
開啟的表單。

### <div id="form_filter">過濾條件 <path>(視窗內容\開啟表單)</path></div>
開啟表單後，是否過濾部份資料。
* 可空白

<ps>注意</ps> 若開啟表單_<rte>主檔區</rte>的資料來源改變時，須重新設定。

### <div id="form_param">傳遞參數 <path>(視窗內容\開啟表單)</path></div>
開啟表單的傳遞參數。<ic>(FW0000002450)(ENG.參照勾選)</ic>
* 可不設 (但開啟表單要控制好，沒傳遞的處理。)

### <div id="form_param_name">參數名 <path>(視窗內容\開啟表單\傳遞參數)</path></div>
傳遞參數名。

<ps>注意</ps> 當`參數名`改變時，本單也要改版。

### <div id="form_param_sourcetype">參數類別 <path>(視窗內容\開啟表單\傳遞參數)</path></div>
傳入值的類別。
* `表單元件`
* `固定值`
* `參數`

### <div id="form_param_source">參數體 <path>(視窗內容\開啟表單\傳遞參數)</path></div>
傳入值。
* 依`參數類別`
    * `表單元件`
        `表單元件` / `隱藏表單元件`。
    * `固定值`
        * 依`接收參數`的`型態`，輸入格式不同
            * 文字
            * 數字
            * 日期
            * 邏輯
    * `參數`
        `表單`的`接收參數`。

### <div id="form_choosetype">筆數 <path>(視窗內容\開啟表單\勾選限制)</path></div>
可帶回的筆數。
* 單選
* 複選 <ic>(FW0000002982)(ENG.參照勾選)</ic>
    * 限為`多筆表格`的子元件，才可設定。
    * 帶回資料時，第一筆會固定覆蓋駐留筆。第二筆以後會插入新的記錄在駐留筆之後。

### <div id="form_onlychoose">限定勾選 <path>(視窗內容\開啟表單\勾選限制)</path></div>
是否只能是開窗挑回，不可自行輸入。
* `筆數`
    * `單選` <ic>(FW0000006440)(ENG.參照勾選)</ic>
    * `複選` <ic>(FW0000002665)(ENG.參照勾選)</ic>
* 若非開窗挑回時，於<rte>元件跳離</rte>時，顯示錯誤訊息"※系統通知※ 不允自行輸入，只能開窗挑回！"

### <div id="form_appendinit">新增初始值 <path>(視窗內容\開啟表單\勾選限制)</path></div>
帶回的資料，於新增`多筆表格`的記錄時，是否執行新增初始值。
* 當`筆數`為`複選`時，才可設定。

### <div id="form_put">勾選帶回 <path>(視窗內容\開啟表單)</path></div>

* 若帶回多個欄位時 <ic>(FW0000006440)(ENG.參照勾選)</ic>

### <div id="form_put_ctrl">接收欄位 <path>(視窗內容\開啟表單\勾選帶回)</path></div>
### <div id="form_put_sourcefield">來源欄位 <path>(視窗內容\開啟表單\勾選帶回)</path></div>
### <div id="form_remove_duplicates">剔除已存 <path>(視窗內容\開啟表單\勾選帶回)</path></div>
若帶回的資料，已存在`多筆表格`時，該筆則不帶回。
* 當`筆數`為`複選`時，才可設定。

### <div id="form_run_relation_update">主動更新 <path>(視窗內容\開啟表單\勾選帶回)</path></div>
是否執行該`元件`的`更新相關值` / `被動更新`。

### <div id="form_copy">複寫資料 <path>(視窗內容\開啟表單)</path></div>
預設是否帶入`多筆表格`駐留筆資料。<ic>(FW0000001821)(ENG.參照勾選)</ic>

### <div id="form_copy_ctrl">欄位 <path>(視窗內容\開啟表單\複寫資料)</path></div>


### <div id="folder">資料夾 <path>(視窗內容\檔案總管\型態)</path></div>

### <div id="file">資料夾 <path>(視窗內容\檔案總管\檔案)</path></div>

### <div id="color">調色盤 <path>(視窗內容)</path></div>

