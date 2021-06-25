### <div id="user">規劃人員</div>
* 正傑

### <div id="updatedate">規劃日期</div>
* 2021/06/24

### <div id="trac">TRAC</div>
* #8551

### <div id="openform">嵌入物件 <path>(元件加註)</path></div>
* 異動
* 規格說明
    * #8551
        * 嵌入元件Google地圖支援點擊事件並回傳GPS經緯度
        * 位址連結更名為地標功能

### <div id="workflow">作業流程</div>

![作業流程]

### <div id="map-latlng-return">經緯度回傳 <path>(物件類別\地圖)</path></div>
當地圖上任意點被點擊時，會將該點座標的經度寫入`經度變數名`，緯度寫入`緯度變數名`...等所指定的全域變數後，呼叫`觸發按鍵`所指定的功能按鍵

### <div id="map-latlng-return-funckey">觸發按鍵 <path>(物件類別\地圖\經緯度回傳)</path></div>
點擊地圖上任意點時呼叫的功能按鍵

### <div id="map-latlng-return-latparam">經度變數名 <path>(物件類別\地圖\經緯度回傳)</path></div>
點擊地圖上任意時，要寫入【座標經度】的全域變數。

### <div id="map-latlng-return-lngparam">緯度變數名 <path>(物件類別\地圖\經緯度回傳)</path></div>
點擊地圖上任意時，要寫入【座標緯度】的全域變數。

[作業流程]:attachment/objectannotation_embed.png "作業流程"