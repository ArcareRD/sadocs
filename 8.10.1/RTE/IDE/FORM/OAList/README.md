### <div id="logical">執行條件</div>

### <div id="showtype">呈現方式</div>
* 表示元件以何種方式呈現選項清單，共有以下類型 :

### <div id="select">下拉式 <path>(呈現方式)</div>
* 會將元件變為下拉元件，以下拉方式呈顯選項

### <div id="list">固定式 <path>(呈現方式)</div>
* 會將元件變為[清單選項](../../../SYSTEM/FORM/ctrl_listbox/README.md)，以元件設定的高度限制呈現選項清單內容。

### <div id="selectdata">選擇筆數</div>
* 決定勾回選項的方式，一共有以下方式
    * `單選`
    * `複選`

### <div id="single">單選 <path>(選擇筆數)</div>
* 僅能勾選單筆資料

### <div id="multiple">多選 <path>(選擇筆數)</div>
* 能勾選多筆資料

### <div id="sqlfield">查詢轉換欄位 <path>(選擇筆數\多選)</div>
* 當`呈現方式`為`下拉式`且`選擇筆數`為`複選`時可選擇，表示下拉複選元件將勾選選項資料從 key1,key2,key3 格式轉換為 'key1','key2','key3' 並寫入的欄位

### <div id="itemtype">選項種類</div>
* 表示選項清單的來源種類，一共有以下種類:
    * `固定選項`
    * `變動選項`

### <div id="fixitem">固定選項 <path>(選項種類)</div>
* 表示選項數量為固定，由設計者指定

### <div id="fixitemcontent">選項內容 <path>(選項種類\固定選項)</div>
* 每一個選項的內容，可挑選多語詞庫作為選項內容

### <div id="dynamicitem">變動選項 <path>(選項種類)</div>
* 表示選項數量為變動，由查詢表格取得

### <div id="alwaysload">強制重新載入 <path>(選項種類\變動選項)</div>
* 是否每次取得選項清單時都強制重新查詢

### <div id="inputtype">操作方法 <path>(選項種類\變動選項)</div>
* 表示取得選項的操作方式，一共有以下方式 :
    * `僅挑選指定`
    * `可自行輸入`

### <div id="onlyselect">僅挑選指定 <path>(選項種類\變動選項\操作方法)</div>
* 表示選項僅能使用挑選的方式取得，不可自行輸入，配合其他設定會有不同變化
    * 當`呈現方式`為`下拉式`且`選擇筆數`為`單選`時，會產生[不可輸入下拉元件](../../../SYSTEM/FORM/ctrl_dropListCombo/README.md)
    * 當`呈現方式`為`下拉式`且`選擇筆數`為`複選`時，會產生[不可輸入下拉複選元件](../../../SYSTEM/FORM/ctrl_dropListMultiCombo/README.md)

### <div id="input">可自行輸入 <path>(選項種類\變動選項\操作方法)</div>
* 表示選項僅能使用挑選以及自行輸入的方式取得，配合其他設定會有不同變化
    * 當`呈現方式`為`下拉式`且`選擇筆數`為`單選`時，會產生[可輸入下拉元件](../../../SYSTEM/FORM/ctrl_dropDownCombo/README.md)
    * 當`呈現方式`為`下拉式`且`選擇筆數`為`複選`時，會產生[可輸入下拉複選元件](../../../SYSTEM/FORM/ctrl_dropDownMultiCombo/README.md)

### <div id="valid">錯誤檢核與訊息 <path>(選項種類\變動選項\操作方法\可自行輸入)</div>
* 表示在[可輸入下拉複選元件](../../../SYSTEM/FORM/ctrl_dropDownMultiCombo/README.md)針對輸入的內容若未通過`檢控限制`的設定以及元件的預設檢查，則會跳出的訊息內容

### <div id="database">對應資料庫 <path>(選項種類\變動選項)</div>
* 表示查詢表格的類型，共有以下類型:
    * `檢視表`
    * `暫存表格`

### <div id="view">檢視表 <path>(選項種類\變動選項\對應資料庫)</div>
* 表示選項來源由`檢視表`取得

### <div id="tempview">暫存表格 <path>(選項種類\變動選項\對應資料庫)</div>
* 表示選項來源由`暫存表格`取得

### <div id="viewname">表格名稱 <path>(選項種類\變動選項)</div>
* 表示選項來源的表格

### <div id="filter">過濾條件說明 <path>(選項種類\變動選項)</div>
* 表示在選項來源的表格增加過濾條件

### <div id="extra">帶回欄位 <path>(選項種類\變動選項)</div>
* 表示挑選選項後，要從選項帶回的欄位內容並更新到指定的元件上

### <div id="source">來源欄位 <path>(選項種類\變動選項\帶回欄位)</div>
* 挑選選項來源表格內的欄位

### <div id="display">要顯示 <path>(選項種類\變動選項\帶回欄位)</div>
* 是否要將這個欄位的內容顯示在選項上

### <div id="value">帶回值 <path>(選項種類\變動選項\帶回欄位)</div>
* 是否要將這個欄位的內容帶回至`帶回對應元件`

### <div id="object">帶回對應元件 <path>(選項種類\變動選項\帶回欄位)</div>
* 挑選更新帶回值的元件，至少要有一個元件是被加註的元件本身。

### <div id="sort">排序方式 <path>(選項種類\變動選項\帶回欄位)</div>
* 是否將`來源欄位`作為選項清單查詢表格的排序依據，可設定的選項如下:
    * 空白 : 表示不作為排序依據
    * 升冪 : 作為升冪排序
    * 降冪 : 作為降冪排序


