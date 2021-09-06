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
依據`呼叫時機`來決定指定的元件操作行為可執行指定的功能鍵

### <div id="btnup_funkey">按鈕功能名 <path>(元件加註\更新給值\呼叫按鈕功能)</path></div>
當`呼叫時機`成立時，要執行的功能鍵

### <div id="btnup_time">呼叫時機 <path>(元件加註\更新給值\呼叫按鈕功能)</path></div>
* 內容異動 : 表示元件對應的檔區欄位內容值異動時成立(非紀錄移動)，支援的元件類型如下:
    * 文字方塊(wTF)
    * 文字方塊(多筆表格)(text)
    * 多行文字(wTA)
    * 多行文字(多筆表格)(textarea)
    * 按鈕選項(wRB)
    * 核取方塊(wCB)
    * 核取方塊(多筆表格)(checkbox)
    * 下拉選項(wDL)
    * 下拉選項(多筆表格)(select)
    * 彈出視窗(wPW)
    * 彈出視窗(多筆表格)(popupwindow)
    * 清單選項(wLB)
    * 畫布(wCanvas)
    * 隱藏元件(wHObj)
    * 備註 : 若元件為僅供顯示，若元件對應的檔區欄位內容值異動也會視同成立

* 資料行移動 : 表示移動駐留筆資料時成立，支援的元件類型如下:
    * 多筆表格(wGrd)
    * 多筆瀏覽(wGrdLite)
    * 樹狀清單(wTree)
    * 元件容器(wCtnr)

* 滑鼠雙擊 : 表示滑鼠左鍵雙擊資料列時成立，支援的元件類型如下:
    * 多筆表格(wGrd)
    * 多筆瀏覽(wGrdLite)
    * 元件容器(wCtnr)

* 滑鼠單擊 : 表示滑鼠單擊元件時成立，支援的元件類型如下:
    * 核取方塊(wCB)
    * 核取方塊(多筆表格)(checkbox)
    * 核取方塊(多筆瀏覽)(liteCheckbox)
    * 備註 : 目前僅提供給元件容器/多筆表格/多筆瀏覽中的核取方塊使用

* 滑鼠離開 : 表示元件在編輯狀態下異動內容值後跳離且通過檢控限制時成立，支援的元件類型如下:
    * 文字方塊(wTF)
    * 多行文字(wTA)
    * 按鈕選項(wRB)
    * 核取方塊(wCB)
    * 下拉選項(wDL)
    * 彈出視窗(wPW)
    * 清單選項(wLB)

* 自動完成 : 表示元件在編輯狀態下輸入內容值，輸入的間隔時間若超過系統參數中的停滯時間設定時成立，支援的元件類型如下
    * 文字方塊(wTF)
    * 文字方塊(多筆表格)(text)

### <div id="multipleup">網格更新</div>

### <div id="variableup">變數更新</div>

### <div id="customup">自定函數更新</div>

### <div id="passwordup">密碼更新</div>