### <div id="layout">版面相關</div>
### <div id="std">STD表單 <path>(版面相關)</div>
待補
### <div id="rwd">RWD表單 <path>(版面相關)</div>
* 元件畫面
    * 畫面結構
        
        ![元件畫面結構]

* 樣式支援 : 
    * 元件樣式 
        * 多行文字
            * [(RWD)標題](../../../../STYLE/wTA.md#rwd標題title-元件多行文字)
            * [(RWD)致能](../../../../STYLE/wTA.md#rwd致能enable-元件多行文字)
            * [(RWD)駐留](../../../../STYLE/wTA.md#rwd駐留onfocus-元件多行文字)
            * [(RWD)滑鼠移入](../../../../STYLE/wTA.md#rwd滑鼠移入mousein-元件多行文字)

### <div id="action">行為</div>

### <div id="protected">受權限保護元件 <path>(行為)</div>
* 內容區會顯示(***)的字樣
* 無法駐留

### <div id="alias">對應檔區 <path>(行為)</div>
* 元件的資料檔區設定
* 設定於[元件加註/基本設定/存在檔區]()

### <div id="field">對應欄位 <path>(行為)</div>
* 支援欄位型態
    * 文字
    * 備註

### <div id="show">顯示設定 <path>(行為)</div>
* 支援變色 : 僅支援RWD表單，設定於[元件加註/顯示設定/僅變更顏色]()
    * 背景顏色
    * 字體顏色
* 支援燈號顯示 : 設定於[元件加註/顯示設定/被突顯]()

### <div id="picture">模版 <path>(行為)</div>
* 必定為`文件編輯模板`

### <div id="hint">提示 <path>(行為)</div>
* 滑鼠移入元件時顯示`提示`內容，設定地點 : 元件加註/基本設定/欄位提示訊息

### <div id="filter">資料過濾 <path>(行為)</div>
* 支援

### <div id="search">資料搜尋 <path>(行為)</div>
* 不支援

### <div id="edit">編輯模式 <path>(行為)</div>
* 支援，進入編輯後，畫面顯示同瀏覽模式，需滑鼠雙擊開啟編輯器，才能開啟編輯器進行編輯資料，以下為編輯器模擬畫面 :

    ![HTML編輯器]
    
    * 備註 : 若資料單行長度大於編輯器寬度，於RWD表單上，會針對資料自動折行；於STD表單上，會出現水平卷軸

### <div id="browse">瀏覽模式 <path>(行為)</div>
* 未駐留元件畫面

    ![未駐留模擬畫面]

* 駐留元件畫面

    ![駐留模擬畫面]

* 滑鼠雙擊彈出視窗顯示元件內容畫面

    ![瀏覽雙擊元件畫面]

    * 備註 : 若資料單行長度大於視窗寬度，於RWD表單上，會針對資料自動折行；於STD表單上，會出現水平卷軸

### <div id="light">連動燈號 <path>(行為)</div>
* 支援

### <div id="hide">元件隱藏 <path>(行為)</div>
* 隱藏方式分為以下兩種 :
    * 元件隱藏 : 整個元件隱藏
    * 資料隱藏 : 隱藏內容資料
* 僅支援元件隱藏

### <div id="disabled">元件除能 <path>(行為)</div>
* 不支援

### <div id="focus">元件駐留 <path>(行為)</div>
* 顯示駐留樣式，動作流程如下圖所示 :

    ![元件駐留]

### <div id="blur">元件跳離 <path>(行為)</div>
* 執行資料的檢控限制以及更新給值，動作流程如下圖所示 :

    ![元件跳離]

### <div id="mouse">滑鼠操作 <path>(行為)</div>
* 左鍵點擊 : 表示駐留到該筆紀錄上，動作流程如下

    ![滑鼠單擊]

* 左鍵雙擊 : 若元件在瀏覽模式，表示開啟視窗顯示資料內容，若在編輯模式，表示開啟編輯器進行修改資料，動作流程如下

    ![滑鼠雙擊]

### <div id="mobile">行動裝置操作 <path>(行為)</div>
* 同滑鼠操作


[元件畫面結構]:attachment/ctrlhtmledit_struct.png "元件畫面結構"
[HTML編輯器]:attachment/dblclick_edit.png "HTML編輯器"
[未駐留模擬畫面]:attachment/browse_not_focus.png "未駐留模擬畫面"
[駐留模擬畫面]:attachment/browse_focus.png "駐留模擬畫面"
[滑鼠單擊]:attachment/click.png "滑鼠單擊"
[滑鼠雙擊]:attachment/dblclick.png "滑鼠雙擊"
[元件駐留]:attachment/focus.png "元件駐留"
[元件跳離]:attachment/blur.png "元件跳離"