## <div id="layout">版面相關</div>
* 版面
    * ![pic][image_Expression1]
    * ![pic][image_Expression2]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 由各呼叫端開啟 以Dailog on Top 的方式開啟
* 由各呼叫端開啟, 部份欄位的顯示/隱藏、除能/致能, 由欄位說明列出詳給內容

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">搜尋</p>

    * ![pic][image_fieldbreak1]
    * `(1)頁籤`
        * 用途說明
        * 規格說明
            * 分別為 來源/元件/參數/查表/函數/段落/全域變數/上層
            * 依呼叫端判斷頁籤是否隱藏
                * 非檢視表開啟, 來源 隱藏
                * 非資料交易開啟, 段落 隱藏
                * 非加註(元件、按鍵、報表元件)頁面開啟, 元件 隱藏
                * 非以下頁面開啟, 查表 隱藏
                    * 元件加註_檢控限制/運算判斷
                    * 元件加註_更新給值/變數更新/給值來源
                    * 按鍵加註_表單特效/更新欄位/給值內容
                    * 按鍵加註_表單特效/更新變數/給值來源
                * 非按鍵加註_推播通知開啟, 上層 隱藏
    * `(2)搜尋清單區`
        * 用途說明
        * 規格說明
            * 依不同頁籤顯示不同的搜尋清單內容
                * 頁籤為 來源、段落、全域變數, `(3)關鍵字`、`(4)搜尋` 隱藏
                * 頁籤為 函數, `(5)新增` 隱藏
                * 其餘頁籤皆顯示
    * `(4)搜尋`
        * 用途說明
        * 規格說明
            * 以 Like %`(1)關鍵字`% 的語法, 比對名稱
                * 元件, 搜尋範圍為來源端表單(報表)下的元件, 並比對專案語系下的多語內容
                * 參數, 搜尋範圍為來源端表單(報表、檢視表、資料交易)下的參數, 並比對參數名稱
                * 查表, 搜尋範圍為資料(檢視)表格下的欄位, 並比對欄位名稱
                * 函數, 搜尋範圍為所有函數, 依來源端判斷支援語法與類型, 並比對平台語系下的多語內容
                * 上層, 搜尋範圍為來源端 按鍵加註_推播通知/推播內容/來源 下的欄位, 並比對欄位名稱
            * 載入符合條件的記錄, 並以 多語內容 由小到大, 升冪排序
        * 動作流程
            * ![pic][image_flow_search]
    * `(5)新增`
        * 用途說明
        * 規格說明
            * 可將駐留筆依新增至對應自定頁籤的內容中
            * 當`編輯方法`=引用函數, 除能
        * 動作流程
            * ![pic][image_flow_add]
    * `(6)清單`
        * 用途說明
        * 規格說明
            * 搜尋結果依清單方式呈現於此
            * 以下說明清單呈現內容
                * 來源, 顯示 表格別名.欄位名稱 (例: A.客戶代號)
                * 元件、全域變數, 顯示 專案語系下的多語內容
                * 參數, 顯示 參數名稱
                * 查表、上層, 顯示 欄位名稱
                * 函數, 顯示 平台語系下的多語內容
                * 段落, 顯示 段落流水序號.來源欄位名稱 (例: 001.客戶代號)
            * 當`編輯方法`=引用函數, 可駐留項目, 並拖拉至`結果`中
                * 拖拉規則請參閱 <a href="attachment/ExpressionRA.xlsx" donwnload>運算式拖曳規則</a>
        * 動作流程
            * ![pic][image_flow_drag]
            * ![pic][image_flow_reside]

* <p id="fieldbreak2" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_fieldbreak2]
    * `(1)說明`
        * 用途說明
        * 規格說明
            * 自行輸入，不允空白
    * `(2)條件區塊`
        * 用途說明
        * 規格說明
            * 由檢視表開啟時, 標題顯示 "條件運算式n"(n為流水號), 否則 顯示空白
            * 當條件有多個時, 單擊未展開的條件, 則展開點擊的條件, 並將其它的條件收起
        * 動作流程
            * ![pic][image_flow_clickCondition]
    * `(3)新增條件`
        * 用途說明
        * 規格說明
            * 非檢視表開啟時, 隱藏
            * 新增一`(2)條件區塊`並展開, 將其它的條件收起
        * 動作流程
            * ![pic][image_flow_addCondition]
    * `(4)刪除條件`
        * 用途說明
        * 規格說明
            * 非檢視表開啟時, 隱藏
            * 刪除指定的`(2)條件區塊`後, 展開第1個條件區塊
        * 動作流程
            * ![pic][image_flow_deleteCondition]
    * `(5)條件說明`
        * 用途說明
        * 規格說明
            * 非檢視表開啟時, 隱藏
            * 參照 [操作條件式通則][link_ruledialog1], 限定不允查表 且 不為個資加密、密碼處理欄位, 回傳並顯示 條件說明
    * `(6)對應資料庫`
        * 用途說明
        * 規格說明
            * 非以下頁面開啟, 隱藏
                * 元件加註_檢控限制/運算判斷
                * 元件加註_更新給值/變數更新/給值來源
                * 按鍵加註_表單特效/更新欄位/給值內容
                * 按鍵加註_表單特效/更新變數/給值來源
            * 以下頁面開啟, 除能
                * 按鍵加註_表單特效/更新欄位/給值內容
                * 按鍵加註_表單特效/更新變數/給值來源            
            * 選項 無/資料表/檢視表; 預設: 無
            * 內容異動時, 顯示訊息盒【標題: 系統訊息 / 將會移除所有引用表格的欄位，是否繼續? / 按鍵:確定、取消】
                * 確定: 清除以下中, 有引用表格的欄位, 並關閉訊息盒
                    * `(7)表格`、`傳遞參數`、自定、引用函數頁籤
                * 取消: 關閉訊息盒
        * 動作流程
            * ![pic][image_flow_changeQueryType]
    * `(7)表格`
        * 用途說明
        * 規格說明
            * 非以下頁面開啟, 隱藏
                * 元件加註_檢控限制/運算判斷
                * 元件加註_更新給值/變數更新/給值來源
                * 按鍵加註_表單特效/更新欄位/給值內容
                * 按鍵加註_表單特效/更新變數/給值來源
            * 以下頁面開啟, 除能
                * 按鍵加註_表單特效/更新欄位/給值內容
                * 按鍵加註_表單特效/更新變數/給值來源
            * `(6)對應資料庫`=無, 除能(含相關按鍵)
            * 依據`(6)對應資料庫`
                * 資料表: [挑選資料表通則][link_ruledialog3], 從本專案中, 挑選資料表, 回傳並顯示資料表名稱
                * 檢視表: [挑選檢視表通則][link_ruledialog4], 從本專案中, 挑選檢視表, 回傳並顯示檢視表名稱
    * `(8)過濾條件`
        * 用途說明
        * 規格說明
            * 非以下頁面開啟, 隱藏
                * 元件加註_檢控限制/運算判斷
                * 元件加註_更新給值/變數更新/給值來源
                * 按鍵加註_表單特效/更新欄位/給值內容
                * 按鍵加註_表單特效/更新變數/給值來源
            * 以下頁面開啟, 除能
                * 按鍵加註_表單特效/更新欄位/給值內容
                * 按鍵加註_表單特效/更新變數/給值來源
            * `(6)對應資料庫`=無, 除能(含相關按鍵)
            * 參照 [操作條件式通則][link_ruledialog1], 限定查表須同`(7)表格`已設定的來源, 回傳並顯示條件說明

* <p id="fieldbreak3" style="color:blue;font-weight:bold">編輯方式/自定</p>

    * ![pic][image_fieldbreak3]
    * `(1)編輯方法`
        * 用途說明
        * 規格說明
            * 選項 自定/引用函數; 預設 自定
            * 來源端為加註(元件、按鍵) 且 表單類型=APP, 自定 隱藏; 預設 引用函數
            * 改變時, 切換`(2)自定`、`(3)引用函數`頁籤顯示
        * 動作流程
            * ![pic][image_flow_changeEditType]
    * `(2)自定`
        * 用途說明
        * 規格說明
            * 來源端為加註(元件、按鍵) 且 表單類型=APP, 隱藏
    * `(4)內容`
        * 用途說明
        * 規格說明
            * 自行輸入, 可使用清單上的新增鍵將元件、參數...等, 引用至運算內容中

* <p id="fieldbreak4" style="color:blue;font-weight:bold">編輯方式/引用函數</p>

    * ![pic][image_fieldbreak4]
    * `(1)結果`
        * 用途說明
        * 規格說明
            * 拖曳及編輯方式的規則請參閱 <a href="attachment/ExpressionRA.xlsx" donwnload>運算式拖曳規則</a>          
            * 駐留函數, 重新載入參數至`(3)參數清單`中
                * 若該參數內放置的是函數, 則表示駐留函數            
            * 駐留參數, 重新載入依附函數的參數至`(3)參數清單`中
                * 若該參數內放置的是非函數, 則表示駐留參數
            * 參數若自行輸入, 依參數型態及來源端判斷是否要使用單雙引號('、")將內容包起來
                * 非數字 且 來源端為檢視表開啟, 使用 單引號(')
                * 非數字 且 來源端非檢視表開啟, 使用 雙引號(")
            * 將元件、參數...等拖曳至`(1)結果`中時, 依下列條件判斷開啟 [引用運算方式](CitationOperation)
                * 滑鼠移入函數上
                * 滑鼠移入參數上 且 參數已有內容值
        * 作業流程
            * ![pic][image_flow_drag]
            * ![pic][image_flow_reside]
            * ![pic][image_flow_rightClickAdd]
            * ![pic][image_flow_rightClickDelete]
    * `(2)前置`
        * 用途說明
        * 規格說明
            * 為最外層函數 且 有前置函數時顯示, 否則清空除能
            * 選項 相加(+) / 相減(-) / 相乘(*) / 相除(/) / 餘數(Mod) / 大於(>) / 小於(<) / 等於(==) / 不等於(!=) / 大於等於(>=) / 小於等於(<=) / 且(&&) / 或(||)
                * 選項 大於(>) / 小於(<) / 等於(==) / 不等於(!=) / 大於等於(>=) / 小於等於(<=) / 且(&&) / 或(||), 非以下來源端開啟時, 隱藏
                    * 檢視表/聯結設定
                    * 資料交易
                    * 元件加註_檢控限制/運算判斷
                * 選項 等於(==) / 不等於(!=) / 且(&&) / 或(||), 若來源端為 檢視表/聯結設定 開啟, 則顯示 等於(=) / 不等於(<>) / 且(AND) / 或(OR)
                * 可切換選項, 即時更新`(1)結果`的顯示, 運算符號依()中的內容呈現 [引用運算方式](CitationOperation)
        * 作業流程
            * ![pic][image_flow_changeOperatingType]
    * `(4)參數名稱`
        * 用途說明
        * 規格說明
            * 顯示參數名稱
    * `(5)參數型態`
        * 用途說明
        * 規格說明
            * 顯示參數型態
    * `(6)運算方式`
        * 用途說明
        * 規格說明
            * 選項 相加(+) / 相減(-) / 相乘(*) / 相除(/) / 餘數(Mod) / 大於(>) / 小於(<) / 等於(==) / 不等於(!=) / 大於等於(>=) / 小於等於(<=) / 且(&&) / 或(||)
                * 選項 大於(>) / 小於(<) / 等於(==) / 不等於(!=) / 大於等於(>=) / 小於等於(<=) / 且(&&) / 或(||), 非以下來源端開啟時, 隱藏
                    * 檢視表/聯結設定
                    * 資料交易
                    * 元件加註_檢控限制/運算判斷
                * 選項 等於(==) / 不等於(!=) / 且(&&) / 或(||), 若來源端為 檢視表/聯結設定 開啟, 則顯示 等於(=) / 不等於(<>) / 且(AND) / 或(OR)
                * 可切換選項, 即時更新`(1)結果`的顯示, 運算符號依()中的內容呈現
        * 作業流程
            * ![pic][image_flow_changeOperatingType]
    * `(7)運算內容`
        * 用途說明
        * 規格說明
            * 當參數有選項時, 顯示下拉選項, 下拉該參數可選取的資料
            * 可自行輸入, 可引用元件、參數...等
            * 語法檢查=✓時, 則將運算內容顯示至`(1)結果`中
        * 作業流程
            * ![pic][image_flow_enter]
    * `(8)語法檢查`
        * 用途說明
        * 規格說明
            * 依參數型態+運算內容, 檢查合法性, 通過檢查打✓, 不通過打✗ (紅色)
            * 參數區塊使用的是函數 或 參數型態為任意, 則不做任何語法檢查
            * 當參數型態為布林時, 檢查輸入値必為true、false 或 1、0 或位元(邏輯)型態欄位 或 NULL (不論大小寫)
            * 當參數型態為日期時, 檢控輸入値必為yyyy/mm/dd 或 yyyy/mm/dd hh:mm:ss 或 yyyy/mm/dd hh:mm或 日期(日期時間)型態欄位 或 NULL(不論大小寫)
            * 當參數型態為全唯碼時, 檢控輸入値必須為全唯碼字串(ex.{471B9A50-6A53-4D37-AC30-EDD332E6175D}) 或 全唯碼型態欄位 或 NULL(不論大小寫)
            * 當參數型態為表單參數陣列, 檢控輸入值須為陣列寫法, 例: ["A","B","C"]、[1,2,3]
            * 當輸入值為元件
                * 表單元件, 判斷對應檔區欄位是何種型態
                * 報表元件, 判斷對應的模板是何種型態

* <p id="fieldbreak5" style="color:blue;font-weight:bold">按鍵區</p>

    * ![pic][image_fieldbreak4]
    * `(1)儲存`
        * 用途說明
        * 規格說明    
            * 若為新增時, 必須產生多語詞庫  
            * 若為修改時, 必須依專案語系異動多語詞庫
            * 儲存完成後, 顯示訊息盒【標題: 系統訊息 / 儲存完成 / 按鍵: 繼續編輯、關閉視窗】
                * 繼續編輯: 關閉訊息盒
                * 關閉視窗: 關閉訊息盒、關閉視窗, 並將運算說明回傳給來源端
        * 作業流程
            * ![pic][image_flow_save]
    * `(2)關閉`
        * 用途說明
        * 規格說明
            * 關閉視窗

## <div id="save-action">儲存檢控</div>
* 不允空白檢控, 符合條件時, 顯示訊息盒, 並以紅框線標註錯誤的欄位
    * 訊息盒:【標題: 執行存回，發生下列錯誤 / 訊息內容: 以下資料未填寫正確 *錯誤欄位名* / 按鍵: 確定】
        * 確定: 關閉訊息盒 
    * 檢控欄位如下
        * `說明`
        * `對應資料庫`不為無, `表格`不允空白
* 其它檢控, 符合條件時, 顯示訊息盒
    * 訊息盒【標題: 執行存回 / 訊息內容: 以下資料未通過驗證 / 按鍵:確定】
        * 確定: 關閉訊息盒
    * 檢控如下
        * 由 檢視表/欄位濾單/資料內容/運算公式 開啟
            * 只有一個條件項時, 不允設`條件式`
            * 有設定`條件式`時, 至少要有一筆空白條件
            * 空白條件者, 不允存在兩筆
        * 編輯方法=自定時, 自定內容, 不允空白
        * 編輯方法=引用函數時
            * `結果`, 不允空白
            * 檢查`運算內容`是否有未填入值或是語法檢查有誤
            * 檢查`運算方式`是否有未填入值
        * 自定內容 或 函數結果內容, 不能為個資加密或密碼處理的欄位
        * 以下頁面開啟, 檢查過濾條件中的限定表格與`表格`是否相同
            * 元件加註_檢控限制/運算判斷
            * 元件加註_更新給值/變數更新/給值來源

<!-- 圖片 -->
[image_Expression1]:attachment/Expression1.png
[image_Expression2]:attachment/Expression2.png
[image_fieldbreak1]:attachment/fieldbreak1.png
[image_fieldbreak2]:attachment/fieldbreak2.png
[image_fieldbreak3]:attachment/fieldbreak3.png
[image_fieldbreak4]:attachment/fieldbreak4.png
[image_fieldbreak5]:attachment/fieldbreak5.png

[image_flow_search]:attachment/flow_search.png
[image_flow_add]:attachment/flow_add.png
[image_flow_drag]:attachment/flow_drag.png
[image_flow_reside]:attachment/flow_reside.png
[image_flow_clickCondition]:attachment/flow_clickCondition.png
[image_flow_addCondition]:attachment/flow_addCondition.png
[image_flow_deleteCondition]:attachment/flow_deleteCondition.png
[image_flow_changeQueryType]:attachment/flow_changeQueryType]:.png
[image_flow_changeEditType]:attachment/flow_changeEditType.png
[image_flow_changeOperatingType]:attachment/flow_changeOperatingType.png
[image_flow_enter]:attachment/flow_enter.png
[image_flow_rightClickAdd]:attachment/flow_rightClickAdd.png
[image_flow_rightClickDelete]:attachment/flow_rightClickDelete.png
[image_flow_save]:attachment/flow_save.png

<!-- 超連結 -->
[link_ruleother1]:/8.10.1/IDE/Specification/RulesOther/README.md#ruleother1 "其他操作通則/版面資訊通則"
[link_ruledialog1]:/8.10.1/IDE/Specification/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog3]:/8.10.1/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_ruledialog4]:/8.10.1/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"
[link_citation_operation]:CitationOperation.md "引用運算方式"