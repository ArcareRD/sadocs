## <div id="layout-std">STD表單 <path>(版面相關)</path></div>
* 元件畫面
    * 畫面結構

        ![STD元件畫面結構]

    * 在多筆表格中的畫面結構

        ![STD元件畫面結構_多筆表格內]
    
    * 下拉清單畫面結構

        ![STD下拉清單畫面結構]

## <div id="layout-rwd">RWD表單 <path>(版面相關)</path></div>
* 元件畫面
    * 畫面結構

        ![RWD元件畫面結構]

    * 下拉清單畫面結構

        ![RWD下拉清單畫面結構]

## <div id="behavior-protect">受權限保護元件 <path>(行為)</path></div>
* 內容區會顯示(***)的字樣(#7477)
* 無法駐留

## <div id="behavior-alias">對應檔區 <path>(行為)</path></div>
* 下拉選項的資料檔區設定
* 設定於[元件加註/基本設定/存在檔區]()

## <div id="behavior-field">對應欄位 <path>(行為)</path></div>
* 下拉選項的資料檔區欄位設定
* 設定於[元件加註/基本設定/檢視表對應欄位]()

## <div id="behavior-show">顯示巨集 <path>(行為)</path></div>
* 支援變色

## <div id="behavior-format">模版 <path>(行為)</path></div>    
* 支援	

## <div id="behavior-hint">提示 <path>(行為)</path></div>    
* 滑鼠移入下拉選項時顯示`提示`內容，設定地點 : [元件加註/基本設定/欄位提示訊息]()

## <div id="behavior-filter">資料過濾 <path>(行為)</path></div>    
* 支援

## <div id="behavior-find">資料搜尋 <path>(行為)</path></div>    
* 支援

## <div id="behavior-query">查詢視窗 <path>(行為)</path></div>
* 支援，執行後顯示下拉清單	

## <div id="edit">編輯模式 <path>(行為)</path></div>
* 可自行輸入，輸入後，會依據輸入內容自動篩選並跳出符合的選項，如下模擬畫面 :
    * STD : 

        ![STD編輯模式駐留]
    
    * RWD :

        ![RWD編輯模式駐留]

    * 點擊X按鈕，可清空欄位內容

* 元件勿駐 : 
    * 設定地點 : [元件加註/編輯能力/勿駐]()
    * 當勿駐時，不可駐留
    * 元件在編輯狀態下不出現下拉按鈕(#8270)，且已選擇的項目不出現X按鈕

* 元件唯讀 :
    * 設定地點 : [元件加註/編輯能力/唯讀]()
    * 不允開啟下拉選項的清單
    * 元件在編輯狀態下不出現下拉按鈕(#8270)，且已選擇的項目不出現X按鈕

## <div id="browse">瀏覽模式 <path>(行為)</path></div>
* 內容 :
    * 非駐留時的模擬畫面如下 :
        * STD

            ![STD瀏覽模式非駐留]

        * RWD

            ![RWD瀏覽模式非駐留]

    * 駐留時的模擬畫面如下 :
        * STD
        
            ![STD瀏覽模式駐留]
        
        * RWD
        
            ![RWD瀏覽模式駐留]

## <div id="light">連動燈號 <path>(行為)</path></div>
* 支援

## <div id="hide">元件隱藏 <path>(行為)</path></div>
* 支援資料隱藏
* 支援整個元件隱藏

## <div id="focus">元件駐留 <path>(行為)</path></div>
* 除了預設處理外，會再多執行下列項目:
    * 自動出現<下拉清單> (限RWD表單)

## <div id="hotkey">鍵盤熱鍵 <path>(行為\元件駐留)</path></div>
* Esc : 
    * 編輯狀態下
        * 有開啟下拉清單，關閉下拉清單，不接續後面的動作。
    * 觸發表單熱鍵.Esc
    * 動作流程圖如下 :

        ![熱鍵Esc]

* Enter :
    * 編輯狀態下
        * 有開啟下拉清單，關閉下拉清單，勾選駐留筆到元件，不接續後面的動作。
    * 觸發表單熱鍵.Enter
    * 動作流程圖如下 :

        ![熱鍵Enter]

* Tab :
    * 編輯狀態下
       * 有開啟下拉清單，關閉下拉清單
    * 觸發表單熱鍵.Tab
    * 動作流程圖如下 :

        ![熱鍵Tab]

* Shift + Tab :
    * 編輯狀態下
        * 有開啟下拉清單，關閉下拉清單
    * 觸發表單熱鍵.Shift + Tab
    * 動作流程圖如下 :

        ![熱鍵ShiftTab]
* F6 :
    * 編輯狀態下，開啟下拉清單 。若元件為唯讀或勿駐則該熱鍵失效(#8270)
    * 動作流程圖如下 :

        ![熱鍵F6]
* ↑ :
    * 編輯狀態下
        * 若有開啟下拉清單 : 從目前駐留筆往上移動一筆，若已經到第一筆則無移動效果。
        * 若沒有開啟下拉清單 : 此動作無效果。
    * 瀏覽模式下，觸發表單熱鍵.↑
    * 動作流程圖如下 :

        ![熱鍵↑]

* ↓ :
    * 編輯狀態下
        * 若有開啟下拉清單 : 從目前駐留筆往下移動一筆，若已經到最後一筆則依據元件輸入框內容載入下一批資料並顯示到下拉清單。
        * 若沒有開啟下拉清單 : 開啟下拉清單並停在第一筆。
    * 瀏覽模式下，觸發表單熱鍵.↓
    * 動作流程圖如下 :

        ![熱鍵↓]

* ← :
    * 編輯狀態下，輸入游標往左移動一個字。
    * 瀏覽模式下，觸發表單熱鍵.←
    * 動作流程圖如下 :

        ![熱鍵←]

* → :
    * 編輯狀態下，輸入游標往右移動一個字。
    * 瀏覽模式下，觸發表單熱鍵.→
    * 動作流程圖如下 :

        ![熱鍵→]

* CTRL + M : 
    * 編輯模式下，開啟編輯文字視窗，並呈現元件內容值
    * 瀏覽模式下，開啟瀏覽文字視窗，並呈現元件內容值
    
## <div id="blur">元件跳離 <path>(行為)</path></div>
* 同<文字方塊>，但多了下列動作 :
    * 若有設定[元件加註/選項清單/錯誤檢核與訊息]()，會檢查挑選的選項是否存在，若不存在則彈出指定訊息。 

## <div id="mouse">滑鼠操作 <path>(行為)</path></div>
* 左鍵點擊元件 : 
    * 檢查是否勿駐
    * 執行元件駐留
    * 動作流程圖如下 :

        ![左鍵點擊]

* 滾輪捲動下拉清單至最下方 :
    * 依據元件輸入框的內容作為過濾條件，繼續載入下一批選項資料並顯示在下拉清單上
    * 動作流程圖如下 :

        ![滾輪捲動下拉清單至最下方]

## <div id="mobile">行動裝置操作 `(限RWD表單)` <path>(行為)</path></div>
* 同滑鼠操作

[RWD元件畫面結構]:attachment/rwd_wDL_struct.png "RWD元件畫面結構"
[RWD下拉清單畫面結構]:attachment/rwd_listitem_struct.png "RWD下拉清單畫面結構"
[STD元件畫面結構]:attachment/std_wDL_struct.png "STD元件畫面結構"
[STD元件畫面結構_多筆表格內]:attachment/std_combo_struct.png "STD元件畫面結構_多筆表格內"
[STD下拉清單畫面結構]:attachment/std_listitem_struct.png "STD下拉清單畫面結構"
[STD瀏覽模式非駐留]:attachment/std_combo_browse.png "STD瀏覽模式非駐留"
[RWD瀏覽模式非駐留]:attachment/rwd_combo_browse.png "RWD瀏覽模式非駐留"
[STD瀏覽模式駐留]:attachment/std_combo_browse_focus.png "STD瀏覽模式駐留"
[RWD瀏覽模式駐留]:attachment/rwd_combo_browse_focus.png "RWD瀏覽模式駐留"
[STD編輯模式駐留]:attachment/std_combo_edit_focus.png "STD編輯模式駐留"
[RWD編輯模式駐留]:attachment/rwd_combo_edit_focus.png "RWD編輯模式駐留"
[熱鍵Esc]:attachment/dropdown_esc.png "熱鍵Esc"
[熱鍵Enter]:attachment/dropdown_enter.png "熱鍵Enter"
[熱鍵Tab]:attachment/dropdown_tab.png "熱鍵Tab"
[熱鍵ShiftTab]:attachment/dropdown_shift_tab.png "熱鍵ShiftTab"
[熱鍵F6]:attachment/dropdown_F6.png "熱鍵F6"
[熱鍵↑]:attachment/dropdown_↑.png "熱鍵↑"
[熱鍵↓]:attachment/dropdown_↓.png "熱鍵↓"
[熱鍵←]:attachment/dropdown_←.png "熱鍵←"
[熱鍵→]:attachment/dropdown_→.png "熱鍵→"
[左鍵點擊]:attachment/dropdown_click.png "左鍵點擊"
[元件駐留]:attachment/dropdown_focus.png "元件駐留"
[滾輪捲動下拉清單至最下方]:attachment/dropdown_scroll_down.png "滾輪捲動下拉清單至最下方"