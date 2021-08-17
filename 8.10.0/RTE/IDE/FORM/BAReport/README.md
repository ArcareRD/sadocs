### <div id="logical">執行條件</div>

當條件成立時，才會執行。

* `處理類別` <path>(條件式)</path>
    * `無關資料庫`
    * `資料表`
    * `檢視表`

### <div id="report">報表內容</div>
* 挑選指定的報表

### <div id="opentype">開啟方式</div>
* 開啟報表的方式，共有以下幾種
    * `預覽`
	* `郵件夾檔`
	* `直接下載`
	* `直接列印`
	* `存入資料庫`

### <div id="preview">預覽 <path>(開啟方式)</path></div>
* 以網頁的方式開啟報表

### <div id="mail">郵件夾檔 <path>(開啟方式)</div>
* 將報表輸出為PDF，與`郵件發送`一起使用時，作為郵件夾檔使用

### <div id="download">直接下載 <path>(開啟方式)</path></div>
* 將報表以檔案方式輸出，可指定以下檔案類型
    * `PDF`
    * `XLS`
    * `ODT`
    * `ODS`
    * `DOCX`

### <div id="print">直接列印 <path>(開啟方式)</path></div>
* 將報表以PDF輸出並回傳前端畫面後，呼叫瀏覽器執行列印功能

### <div id="database">存入資料庫 <path>(開啟方式)</path></div>
* 將報表以PDF輸出並存入指定的資料庫紀錄中

### <div id="table">資料表 <path>(開啟方式\存入資料庫)</path></div>
* 輸出的報表檔案要存入的資料表

### <div id="filter">過濾條件 <path>(開啟方式\存入資料庫)</path></div>
* 透過過濾條件找到要更新的紀錄

### <div id="filefield">存入欄位 <path>(查表式更新)</path></div>
* 輸出的報表檔案要存入的欄位

### <div id="filenamefield">檔名欄位 <path>(查表式更新\來源排序)</path></div>
* 輸出的報表檔案名稱要存入的欄位

### <div id="param">傳遞參數</div>
* 依據`報表內容`取得該報表的傳遞參數，可針對每一個報表傳遞參數設定內容值，在開啟報表時將參數傳入報表執行運算

### <div id="paramname">參數名 <path>(傳遞參數)</path></div>
* 可挑選`報表內容`所指定的報表，其設定的傳遞參數

### <div id="paramname">給值類別 <path>(傳遞參數)</path></div>
* 要設定至`參數名`的內容值類別，共有以下項目
    * `元件`
    * `固定值`
    * `參數`
    * `運算式`

### <div id="paramname">給值內容 <path>(傳遞參數)</path></div>
* 依據`給值類別`挑選對應的內容值，設定到`參數名`所指定的報表傳遞參數中