### <div id="logical">執行條件</div>

當條件成立時，才會執行。

* `處理類別` <path>(條件式)</path>
    * `無關資料庫`
    * `資料表`
    * `檢視表`

### <div id="fixedup">固定式更新</div>

固定格式更新單筆資料
* 支援 
    * `元件類型`=`多筆表格` <ic>(FW0000001321)</ic>
    * 其餘 <ic>(FW0000001235)</ic>

### <div id="fixedup_fld">目的欄位 <path>(固定式更新)</path></div>

固定的給值欄位

### <div id="fixedup_src">給值來源 <path>(固定式更新)</path></div>

寫入資料的格式

### <div id="queryup">查表式更新</div>

查詢資料庫的資料，回傳欄位的內容值

* 支援 <ic>(FW0000001257)</ic>

### <div id="queryup_tbl">查表條件 <path>(查表式更新)</path></div>

來源表格及過濾條件

### <div id="queryup_clear">查無資料行時清空目的欄位 <path>(查表式更新)</path></div>

查詢資料庫後無資料的處理

### <div id="queryup_fld">給值內容 <path>(查表式更新)</path></div>

目的及來源欄位

### <div id="queryup_fld_pur">目的欄位 <path>(查表式更新\給值內容)</path></div>

目的元件

### <div id="queryup_fld_src">給值來源 <path>(查表式更新\給值內容)</path></div>

來源表格欄位

### <div id="queryup_order">來源排序 <path>(查表式更新)</path></div>

來源表格欄位的排序設定

### <div id="queryup_order">欄位名稱 <path>(查表式更新\來源排序)</path></div>

查表的排序欄位

### <div id="queryup_order">升/降冪 <path>(查表式更新\來源排序)</path></div>

查表的排序方式

### <div id="bodyup">表身欄位更新</div>

|檔區|執行條件|連結全刪除|需要確認|欄位值更新|
|--|--|--|--|--|
|表頭|X|X|X|X|
|表身|X|V|

* 檔區 = `主檔區`
* 檔區 <>`主檔區`

執行條件
連結全刪除 = '是'
連結全刪除 = '否'
需要確認
確認訊息
欄位值更新 = '是'
欄位值更新 = '否'
目的欄位
給值來源

### <div id="btnup">呼叫按鈕功能</div>

### <div id="multipleup">網格更新</div>

### <div id="variableup">變數更新</div>

### <div id="customup">自定函數更新</div>

### <div id="passwordup">密碼更新</div>