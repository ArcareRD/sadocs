### <div id="map-content">地圖 <path>(物件類別)</path></div>
### <div id="map-address-type">位置資訊 <path>(物件類別\地圖)</path></div>
* `地址`

	表示`位置欄位`內存放的是地址資訊。
* `經緯度`

	表示`位置欄位`內存放的是經緯度資訊(度分秒格式)。

	<ps>注意</ps>
	當設定為經緯度時，運行時會先將座標點資料由度分秒格式轉換為經緯度再傳送給Google Map

<test>測試</test>
* `地址`以及`經緯度`都要測試

### <div id="map-address-count">位置點數 <path>(物件類別\地圖)</path></div>	
顯示在地圖上的座標點數量
### <div id="map-single-address">單點位置 <path>(物件類別\地圖\位置點數)</path></div>
僅顯示單一座標點
### <div id="map-single-address-data">位置欄位 <path>(物件類別\地圖\位置點數\單點位置)</path></div>
存放`地址`或`經緯度`的欄位。
### <div id="map-single-address-info">資訊欄位 <path>(物件類別\地圖\位置點數\單點位置)</path></div>
存放座標點說明資訊的欄位。

### <div id="map-multiple-address">多點位置 <path>(物件類別\地圖\位置點數)</path></div>
可顯示多個座標點，並且將座標點依據`群組欄位`分群顯示
### <div id="map-multiple-address-view">來源檢視表 <path>(物件類別\地圖\位置點數\多點位置)</path></div>
存放地圖顯示座標點的資料來源。

<test>測試</test>
* 靜態view
* 動態view & 有參數

### <div id="map-multiple-address-filter">過濾 <path>(物件類別\地圖\位置點數\多點位置)</path></div>
`來源檢視表`過濾條件。

<test>測試</test>
* 有設定以及未設定都要測試

### <div id="map-multiple-address-group">群組 <path>(物件類別\地圖\位置點數\多點位置)</path></div>
### <div id="map-multiple-address-group-field">群組欄位 <path>(物件類別\地圖\位置點數\多點位置\群組)</path></div>
設定座標點分群資訊的欄位。

<test>測試</test>
* 有設定(兩個欄位以上)以及未設定都要測試

### <div id="map-multiple-address-data">位置欄位 <path>(物件類別\地圖\位置點數\多點位置)</path></div>
存放`地址`或`經緯度`的欄位。
### <div id="map-multiple-address-info">資訊欄位 <path>(物件類別\地圖\位置點數\多點位置)</path></div>
存放座標點說明資訊的欄位。

### <div id="map-address-link">位址連結 <path>(物件類別\地圖)</path></div>
當地圖座標點被點擊時，會先取得`鍵值欄位`的欄位內容值並寫到`鍵值變數名`所指定的全域變數後，呼叫`開單按鈕`所指定的功能按鍵
### <div id="map-address-link-funckey">開單按鈕 <path>(物件類別\地圖\位址連結)</path></div>
點擊地圖座標點時，要執行的功能按鍵。

<test>測試</test>
* 有設定以及未設定都要測試

### <div id="map-address-link-variable">鍵值變數名 <path>(物件類別\地圖\位址連結)</path></div>
點擊地圖座標點時，要寫入【座標額外資訊】的全域變數。
### <div id="map-address-link-variable_data">鍵值欄位 <path>(物件類別\地圖\位址連結)</path></div>
點擊地圖座標點時，要讀取【座標額外資訊】的欄位。
