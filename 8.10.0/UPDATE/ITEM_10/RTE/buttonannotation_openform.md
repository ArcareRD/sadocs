### <div id="user">規劃人員</div>
* 正傑

### <div id="updatedate">規劃日期</div>
* 2021/06/04

### <div id="trac">TRAC</div>
* #8520

### <div id="openform">開啟它單 <path>(按鍵加註)</path></div>
* 異動
* 規格說明
    * #8520
        * 增加按鍵開啟視窗表單
        * 當開啟視窗表單，視窗出現位置:表單編輯區向右靠50px，上方貼齊表單編輯區。

### <div id="workflow">作業流程</div>

 ![作業流程]

### <div id="openform_condition">執行條件 <path>(按鍵加註\開啟它單)</path></div>
以`執行內容`的結果來決定是否要執行該開啟它單

### <div id="openform_condition_content">執行內容 <path>(按鍵加註\開啟它單\執行條件)</path></div>
若`執行內容`結果未通過，表示該開啟它單不執行。

### <div id="openform_condition_message">訊息處理 <path>(按鍵加註\開啟它單\執行條件)</path></div>
若`執行內容`結果未通過時需彈出的錯誤訊息。

### <div id="openform_form">表單名稱 <path>(按鍵加註\開啟它單\開單內容)</path></div>
執行按鍵時要開啟的表單

### <div id="openform_source">資料來源 <path>(按鍵加註\開啟它單\開單內容)</path></div>
顯示`表單名稱`指定的表單資料來源

### <div id="openform_source_filter">資料過濾 <path>(按鍵加註\開啟它單\開單內容)</path></div>
開啟指定表單時要執行的表單過濾條件

### <div id="openform_focus_filter">駐留條件 <path>(按鍵加註\開啟它單\開單內容)</path></div>
開啟指定表單後，會駐留於此條件過濾出的第一筆資料

### <div id="openform_treeroot_filter">樹根指定 <path>(按鍵加註\開啟它單\開單內容)</path></div>
是開啟的表單，有樹元件時，要駐留哪一筆

### <div id="openform_formmode">限定 <path>(按鍵加註\開啟它單\推播內容\表單異動)</path></div>
開啟的表單，限定僅能執行的能力
* `新增`
* `修改`
* `刪除`

備註:限定的優先權大於表單本身的設計，例如:開啟的表單，限定只能新增，即使該表單有增刪修的功能，被開啟後也只能新增

### <div id="openform_formstatus">進入模式 <path>(按鍵加註\開啟它單\推播內容\進入模式)</path></div>
指定表單開單後的表單狀態
* `瀏覽` : 開啟表單後在瀏覽狀態
* `新增` : 開啟表單後進入新增
* `修`改 : 開啟表單後進入修改

### <div id="openform_type">開單模式 <path>(按鍵加註\開啟它單\開單模式)</path></div>
開啟表單的方式
* `分頁` : 以首頁的頁簽開啟表單
* `視窗` : 以視窗開啟表單，僅支援被動表單開啟，行動裝置執行此功能還是會以分頁方式開啟。若在新版首頁上開啟視窗表單，視窗位置如下 :
    * left : 表單編輯區向右靠50px
    * top : 上方貼齊表單編輯區

### <div id="openform_interaction">互動模式 <path>(按鍵加註\開啟它單\互動模式)</path></div>
* `主動` : 開啟子表單後還是可以駐留回父表單，不須先關閉子表單
* `被動` : 開啟子表單後若想駐留回父表單，需先將子表單關閉
* `互動` : 同主動表單，且子表單與父表單可透過訊息傳遞進行呼叫功能

### <div id="openform_parameter_name">參數名 <path>(按鍵加註\開啟它單\傳遞參數)</path></div>
開啟表單時要傳遞的參數名稱

### <div id="openform_parameter_type">給值類別 <path>(按鍵加註\開啟它單\傳遞參數)</path></div>
開啟表單傳遞參數的類別，共有以下幾種 :
* `元件`
* `固定值`
* `參數`
* `運算式`

### <div id="openform_parameter_content">來源欄位 <path>(按鍵加註\開啟它單\傳遞參數)</path></div>
替換字變數的替換值
* 依照`類別`
    * `固定值` : 指定的固定字串或數字。
    * `元件` : `表單元件` / `隱藏表單元件`。
    * `參數` : `表單`的`接收參數`。
    * `運算式` : 指定的運算結果。


[作業流程]:attachment/buttonannotation_openform.png "作業流程"