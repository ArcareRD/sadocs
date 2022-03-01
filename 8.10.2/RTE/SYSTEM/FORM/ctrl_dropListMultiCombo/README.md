﻿### <div id="layout">版面相關</div>
### <div id="std">STD表單 <path>(版面相關)</div>
* 該元件不支援STD

### <div id="rwd">RWD表單 <path>(版面相關)</div>
* 元件畫面
    * 畫面結構
        
        * 元件部分

            ![元件畫面結構]
        
        * 下拉清單

            ![下拉清單畫面結構]

    * 備註1 : 不判斷高度設定，直接採變動高度，且編輯狀態下，若勾回選項使用的總寬度超過元件寬度則折行顯示並將元件高度撐大。
    * 備註2 : 元件部分結構以 [ 標題位置在左 ] 為例

* 樣式支援 : 
    * 元件樣式 
        * [下拉選項樣式](../../../../STYLE/wDL.md)
        * 備註1 : 下拉選項的按鈕.取消以及按鈕.確定會依據主題樣式的功能按鈕進行套用

### <div id="action">行為</div>

### <div id="protected">受權限保護元件 <path>(行為)</div>
* 內容區會顯示(***)的字樣(#7477)
* 無法駐留

### <div id="alias">對應檔區 <path>(行為)</div>
* 下拉選項的資料檔區設定
* 設定於[元件加註/基本設定/存在檔區]()

### <div id="field">對應欄位 <path>(行為)</div>
* 下拉選項的資料檔區欄位設定
* 設定於[元件加註/基本設定/檢視表對應欄位]()

### <div id="findfield">查詢轉換欄位 <path>(行為)</div>
* 下拉選項提供給設計者做SQL IN查詢的資料欄位設定

### <div id="show">顯示設定 <path>(行為)</div>
* 支援變色

### <div id="picture">模版 <path>(行為)</div>
* 支援欄位型態 : 文字

### <div id="hint">提示 <path>(行為)</div>
* 滑鼠移入下拉選項時顯示`提示`內容，設定地點 : [元件加註/基本設定/欄位提示訊息]()

### <div id="filter">資料過濾 <path>(行為)</div>
* 支援
* 欄位的內容值格式為 key1,key2,key3,key4，可以此作為要過濾的條件，ex:
    * 欄位名稱選擇下拉複選元件的`對應欄位`，判斷式設定 7.開頭是 ，過濾固定值設定 key1，則可過濾到所有開頭是key1的資料
    * 欄位名稱選擇下拉複選元件的`對應欄位`，判斷式設定 8.包含 ，過濾固定值設定 key2，則可過濾到勾選選項中含有key2的資料

### <div id="search">資料搜尋 <path>(行為)</div>
* 支援
* 欄位的內容值格式為 key1,key2,key3,key4，可以此作為要搜尋的條件，ex:
    * 搜尋方式設定 開頭 ，搜尋值設定 key1，則可搜尋到下一筆開頭是key1的資料
    * 搜尋方式設定 包含 ，搜尋值設定 key2，則可搜尋到下一筆含有key2的資料

### <div id="edit">編輯模式 <path>(行為)</div>
* 不允自行輸入
* 元件勿駐 : 
    * 設定地點 : [元件加註/編輯能力/勿駐]()
    * 當勿駐時，不可駐留
    * 元件在編輯狀態下不出現下拉按鈕(#8270)，且已選擇的項目不出現X按鈕
    * 以下為模擬畫面 :

        ![勿駐唯讀]

* 元件唯讀 :
    * 設定地點 : [元件加註/編輯能力/唯讀]()
    * 不允開啟下拉選項的清單
    * 元件在編輯狀態下不出現下拉按鈕(#8270)，且已選擇的項目不出現X按鈕
    * 以下為模擬畫面 :
    
        ![勿駐唯讀]

* 內容 :
    * 駐留時的模擬畫面如下 :
        * 駐留元件自動出現下拉清單 :
        
            ![編輯模式下拉選項]
        
        * 點擊checkbox可勾選選項 :

            ![編輯模式下拉選項勾選]

        * 點擊按鈕.取消表示關閉下拉清單，此次新增加的勾選內容無效，不會新增至元件編輯區

        * 點擊按鈕.下拉表示開啟下拉清單，若已開啟下拉清單，則無任何效果

        * 點擊按鈕.確定後，回傳勾選項目，去除已勾選項目後，新增至元件編輯區 :

            ![編輯模式下拉選項勾選確認]
        
        * 當勾選後的資料長度總和超過`對應欄位`的長度設定，此次新增的勾選內容視為無效，並提示訊息 : 選項勾選長度超過欄位長度，無法異動選項

        * 點擊各選項的X按鈕，可刪除掉此選項
        
    * 非駐留時的模擬畫面如下 :

        * 無內容選項的模擬畫面如下 :

            ![編輯狀態非駐留畫面]

        * 若已有內容選項的模擬畫面如下 :

            ![編輯狀態非駐留畫面有內容值]
        
        * 點擊各選項的X按鈕，會先駐留元件後，刪除此選項

    * 備註1 : 勾回選項的總寬度超過元件寬度時，內容折行自動撐大 :

        ![編輯狀態非駐留畫面有內容值超過寬度]

    * 備註2 : 單一勾回選項的寬度超過元件寬度時，超過的部分出現省略符號 :

        ![編輯狀態非駐留畫面有內容值單一選項超過寬度]

### <div id="browse">瀏覽模式 <path>(行為)</div>
* 瀏覽模式下看到的模擬畫面如下 :
    * 駐留時 :

        ![瀏覽狀態駐留]
    
    * 非駐留時 :

        ![瀏覽狀態非駐留]

    * 備註1 : 勾回選項的總寬度超過元件寬度時，內容折行自動撐大 :

        ![瀏覽狀態非駐留畫面有內容值超過寬度]

    * 備註2 : 單一勾回選項的寬度超過元件寬度時，超過的部分出現省略符號 :

        ![瀏覽狀態非駐留畫面有內容值單一選項超過寬度]

### <div id="light">連動燈號 <path>(行為)</div>
* 支援

### <div id="hide">元件隱藏 <path>(行為)</div>
* 隱藏方式分為以下兩種 :
    * 元件隱藏 : 整個元件隱藏
    * 資料隱藏 : 隱藏內容資料
* 支援元件隱藏 / 資料隱藏

### <div id="disabled">元件除能 <path>(行為)</div>
* 不支援

### <div id="focus">元件駐留 <path>(行為)</div>
* 顯示駐留樣式
* 編輯狀態下
    * 自動出現下拉選項清單
* 動作流程圖如下 :

    ![元件駐留]

### <div id="hotkey">鍵盤熱鍵 <path>(行為\元件駐留)</div>
* Esc : 
    * 編輯狀態下
        * 有開啟下拉清單，關閉下拉清單，不接續後面的動作。
    * 觸發表單熱鍵.Esc
    * 動作流程圖如下 :

        ![熱鍵Esc]

* Enter :
    * 編輯狀態下
        * 若有開啟下拉清單 : 無任何效果，不接續後面的動作。
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
        * 若有開啟下拉清單 : 無任何效果，不接續後面的動作。
    * 觸發表單熱鍵.↑
    * 動作流程圖如下 :

        ![熱鍵↑]

* ↓ :
    * 編輯狀態下
        * 若有開啟下拉清單 : 無任何效果，不接續後面的動作。
    * 觸發表單熱鍵.↓
    * 動作流程圖如下 :

        ![熱鍵↓]

* ← :
    * 編輯狀態下
        * 若有開啟下拉清單 : 無任何效果，不接續後面的動作。
    * 觸發表單熱鍵.←
    * 動作流程圖如下 :

        ![熱鍵←]

* → :
    * 編輯狀態下
        * 若有開啟下拉清單 : 無任何效果，不接續後面的動作。
    * 觸發表單熱鍵.→
    * 動作流程圖如下 :

        ![熱鍵→]
    
### <div id="killfocus">元件跳離 <path>(行為)</div>
* 檢查資料的正確性
    * 若有設定[檢控限制]()，則執行檢控限制確認是正確
    * 通過檢控限制後，將已勾選的選項資料轉換為key1,key2,key3,key4,key5的格式並存到`對應欄位`
    * 若有設定`查詢轉換欄位`，再將已勾選的選項資料轉換為(N'key1',N'key2',N'key3',N'key4',N'key5')並存到`查詢轉換欄位`
    * 觸發[更新給值]()的設定
* 動作流程圖如下 :

    ![元件跳離]

### <div id="mouse">滑鼠操作 <path>(行為)</div>
* 左鍵點擊元件 : 
    * 檢查是否勿駐
    * 執行元件駐留
    * 動作流程圖如下 :

        ![左鍵點擊]

* 左鍵點擊下拉清單按鈕.確定 :
    * 將此次新增或取消勾選的項目與已勾選項目同步
    * 判斷同步後的勾選項目總長度是否超過對應`欄位長度`
        * 若超過則彈出錯誤訊息 : 選項勾選長度超過欄位長度，無法異動選項
    * 顯示已勾選項目
    * 動作流程圖如下 :

        ![左鍵點擊下拉清單按鈕.確定]

* 左鍵點擊下拉清單按鈕.取消 :
    * 關閉下拉視窗
    * 放棄此次新增或取消勾選的項目
    * 動作流程圖如下 :

        ![左鍵點擊下拉清單按鈕.取消]

### <div id="mobile">行動裝置操作 <path>(行為)</div>
* 同滑鼠操作

[元件畫面結構]:attachment/wDL_struct.png "元件畫面結構"
[下拉清單畫面結構]:attachment/wDL_list_struct.png "下拉清單畫面結構"
[編輯模式下拉選項]:attachment/droplist_multi.png "編輯模式下拉選項"
[編輯模式下拉選項勾選]:attachment/droplist_multi_selected.png "編輯模式下拉選項勾選"
[編輯模式下拉選項勾選確認]:attachment/droplist_multi_selected_ok.png "編輯模式下拉選項勾選確認"
[編輯狀態非駐留畫面]:attachment/droplist_multi2.png "編輯狀態非駐留畫面"
[編輯狀態非駐留畫面有內容值]:attachment/droplist_multi2_selected.png "編輯狀態非駐留畫面有內容值"
[編輯狀態非駐留畫面有內容值超過寬度]:attachment/droplist_multi2_selected_overflow.png "編輯狀態非駐留畫面有內容值超過寬度"
[編輯狀態非駐留畫面有內容值單一選項超過寬度]:attachment/droplist_multi2_selected_overflow2.png "編輯狀態非駐留畫面有內容值單一選項超過寬度"
[瀏覽狀態駐留]:attachment/droplist_multi_browse_focus.png "瀏覽狀態駐留"
[瀏覽狀態非駐留]:attachment/droplist_multi_browse.png "瀏覽狀態非駐留"
[瀏覽狀態非駐留畫面有內容值超過寬度]:attachment/droplist_multi_browse_overflow.png "瀏覽狀態非駐留畫面有內容值超過寬度"
[瀏覽狀態非駐留畫面有內容值單一選項超過寬度]:attachment/droplist_multi_browse_overflow2.png "瀏覽狀態非駐留畫面有內容值單一選項超過寬度"
[勿駐唯讀]:attachment/droplist_multi_readonly.png "勿駐唯讀"
[熱鍵Esc]:attachment/droplist_multi_esc.png "熱鍵Esc"
[熱鍵Enter]:attachment/droplist_multi_enter.png "熱鍵Enter"
[熱鍵Tab]:attachment/droplist_multi_tab.png "熱鍵Tab"
[熱鍵ShiftTab]:attachment/droplist_multi_shift_tab.png "熱鍵ShiftTab"
[熱鍵F6]:attachment/droplist_multi_F6.png "熱鍵F6"
[熱鍵↑]:attachment/droplist_multi_↑.png "熱鍵↑"
[熱鍵↓]:attachment/droplist_multi_↓.png "熱鍵↓"
[熱鍵←]:attachment/droplist_multi_←.png "熱鍵←"
[熱鍵→]:attachment/droplist_multi_→.png "熱鍵→"
[左鍵點擊]:attachment/droplist_multi_click.png "左鍵點擊"
[元件駐留]:attachment/droplist_multi_focus.png "元件駐留"
[元件跳離]:attachment/droplist_multi_killfocus.png "元件跳離"
[左鍵點擊下拉清單按鈕.確定]:attachment/droplist_multi_click_ok.png "左鍵點擊下拉清單按鈕.確定"
[左鍵點擊下拉清單按鈕.取消]:attachment/droplist_multi_click_cancel.png "左鍵點擊下拉清單按鈕.取消"