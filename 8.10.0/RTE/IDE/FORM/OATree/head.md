### <div id="alias">檔區 <path>(檔區座落\單一檔區)</path></div>
樹的資料來源。

### <div id="alias-parent">父階 <path>(檔區座落\單一檔區)</path></div>
記錄【父階】欄位。

### <div id="alias-self">子階 <path>(檔區座落\單一檔區)</path></div>
記錄【本階】欄位。

### <div id="alias-seq">順序 <path>(檔區座落\單一檔區)</path></div>
記錄【同階節點順序】欄位。
* 可空白
* <rte>欄位型態</rte>須為<rte>數字</rte>。

### <div id="alias-level">階層 <path>(檔區座落\單一檔區)</path></div>
記錄【節點所在階層】欄位。
* 可空白
* 內容值從0開啟
* <rte>欄位型態</rte>須為<rte>數字</rte>。

### <div id="alias-childqty">數量 <path>(檔區座落\單一檔區)</path></div>
記錄【子階節點數量】欄位。
* 可空白
* <rte>欄位型態</rte>須為<rte>數字</rte>。

### <div id="multiroot">多根節點 <path>(外觀)</path></div>
根節點是否有多個節點，而不是虛擬節點。
* 是 : 第一層為父階為空白的節點，可以有多筆記錄。
* 否 : 根節點為虛擬節點，不會對到記錄。

### <div id="expand">預設展開 <path>(外觀)</path></div>
是否自訂預設展開的階層。

若未勾選時，RTE預設展開一層。

### <div id="expandtype">展開類別 <path>(外觀\預設展開)</path></div>
預設展開的階層。

### <div id="expand-all">全展 <path>(外觀\預設展開\展開類別)</path></div>
展開所有階層。

### <div id="expand-level">展開階數 <path>(外觀\預設展開\展開類別)</path></div>
展開指定的層數。

### <div id="expand-level-level">階數 <path>(外觀\預設展開\展開類別\展開階數)</path></div>
指定展開層數。

### <div id="nodename">指定顯示 <path>(外觀)</path></div>
是否定義節點名稱顯示的內容。<ic>(FW0000004555)</ic>

* 若未勾選時，則依下列其它加註，顯示內容 :
	* 若(`表單元件` \ `顯示設定` \ `欄位組合`)有設定時，顯示其內容。
	* 否則若(`表單元件` \ `基本設定` \ `檢視表對應欄位`)有設定時，顯示其內容。

### <div id="nodename-root">根節點 <path>(外觀\指定顯示)</path></div>
根節點要顯示的節點名稱。
* 當`多根節點`未勾選時，才可設定。
* `對應資料庫` <path>(運算式)</path>
    * `無`
    * ~~`資料表`~~
    * ~~`檢視表`~~

### <div id="nodename-self">子節點 <path>(外觀\指定顯示)</path></div>
除了根節點外，要顯示的節點名稱。

### <div id="icon">節點圖示 <path>(外觀)</path></div>
是否有節點圖示。

### <div id="icon-icon">圖示內容 <path>(外觀\節點圖示)</path></div>
顯示圖示。
* [圖示格式]

### <div id="icon-sourcefield">判斷欄位 <path>(外觀\節點圖示)</path></div>
顯示哪個圖示，依據指定欄位顯示。
* <rte>欄位型態</rte>須為<rte>數字</rte>。
* 根節點為0。


### <div id="checkbox">致能勾選 <path>(資料控制)</path></div>
樹節點是否出現checkbox。

<ps>注意</ps> 虛擬節點不會出現checkbox。

### <div id="checkbox-enable">限制條件 <path>(資料控制\致能勾選)</path></div>
checkbox致能條件。
* 可空白
* `處理類別` <path>(條件式)</path>
	* `無關資料庫` <ic>(FW0000006303)</ic>
	* ~~`資料表`~~
	* ~~`檢視表`~~


### <div id="checkbox-sourcefield">單項資料傳遞 <path>(資料控制\致能勾選)</path></div>
checkbox顯示的內容為對應檔區裡的欄位。

### <div id="checkbox-sourcefield-field">對應欄位 <path>(資料控制\致能勾選\單項資料傳遞)</path></div>
樹節點上的checkbox對應的欄位。

* <rte>欄位型態</rte>須為<rte>數字</rte>。

### <div id="checkbox-sourcefield-click">呼叫按鈕 <path>(資料控制\致能勾選\單項資料傳遞)</path></div>
* 無設定 : 於<rte>編輯狀態</rte>下，點選節點上checkbox會改變`對應欄位`的值。
* 有設定 : 於<rte>瀏覽狀態</rte>下，點選節點上checkbox會執行指定的按鍵。

### <div id="checkbox-mutitag">多項資料傳遞 <path>(資料控制\致能勾選)</path></div>
checkbox用來做<rte>多筆勾選</rte>。

### <div id="checkbox-mutitag-field">資料行欄位 <path>(資料控制\致能勾選\多項資料傳遞)</path></div>
<rte>多筆勾選</rte>時，要記錄的欄位。

### <div id="edit-type">項目 <path>(操作性)</path></div>
操作類型。
* `新增子階`
* `插入同階`
* `刪除節點`
	* 當`順序` <path>(檔區座落\單一檔區)</path>有設定時，才可設定。
* `移動節點`
* `複製`
* `剪下`
* `複製貼上`
* `剪下貼上`

### <div id="edit-valid">執行條件 <path>(操作性)</path></div>
 若`不成立訊息`無設定時，為致能條件。

 若`不成立訊息`有設定時，為執行條件。當條件不成立時，會彈出錯誤訊息盒，顯示`不成立訊息`。

* 可空白
* `處理類別` <path>(條件式)</path>
	* `無關資料庫`
	* ~~`資料表`~~
	* ~~`檢視表`~~
* 支援的`項目`
	* `新增子階`
		* 致能條件 <ic>(FW0000004183)</ic>
		* 執行條件 <ic>(FW0000004188)</ic>
	* `插入同階`
		* 致能條件 <ic>(FW0000004184)</ic>
		* 執行條件 <ic>(FW0000004189)</ic>
	* `刪除節點`
		* 致能條件 <ic>(FW0000004185)</ic>
		* 執行條件 <ic>(FW0000004190)</ic>
	* `移動節點`
		* 致能條件 <ic>(FW0000004308)</ic>
		* 執行條件 <ic>(FW0000003429)</ic>
	* `複製`
		* 致能條件 <ic>(FW0000003497)</ic>
		* 執行條件 <ic>(FW0000003428)</ic>
	* `剪下`
		* 致能條件 <ic>(FW0000003498)</ic>
		* 執行條件 <ic>(FW0000003467)</ic>
	* `複製貼上`
		* 致能條件 <ic>(FW0000004186)</ic>
		* 執行條件 <ic>(FW0000004191)</ic>
	* `剪下貼上`
		* 致能條件 <ic>(FW0000004187)</ic>
		* 執行條件 <ic>(FW0000004192)</ic>

### <div id="edit-btn">呼叫按鈕 <path>(操作性)</path></div>
是否自訂動作，取代系統的預設動作。
* 可空白
* 支援的`項目`
	* ~~`新增子階`~~
	* ~~`插入同階`~~
	* ~~`刪除節點`~~
	* ~~`移動節點`~~
	* ~~`複製`~~
	* ~~`剪下`~~
	* `複製貼上` <ic>(FW0000004059)</ic>
	* ~~`剪下貼上`~~

### <div id="edit-errmsg">不成立訊息 <path>(操作性)</path></div>	
當`執行條件`不成立時，要顯示的訊息。
* 當`執行條件`有設定時，才可設定。


[圖示格式]:../../../SYSTEM/FORM/ctrl_tree/README.md#icon "圖示格式"