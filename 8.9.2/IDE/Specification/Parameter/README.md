## <div id="layout">版面相關</div>
* 版面</br>
    ![pic][image_parameter]
* 參照 [版面資訊通則][link_ruleother1]
		
## <div id="form-action">動作說明</div>
* 由各呼叫端開啟 以Dailog on Top 的方式開啟			    

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    ![pic][image_fieldbreak1]
    * `(1)OnlineHelp`
        * 用途說明
        * 規格說明
            * 參照 [OnlineHelp通則][link_ruleother2]
            * 錨點: PassParameters
    * `(2)參數類別`
        * 用途說明
        * 規格說明
            * 依前單限定類別顯示 檢視表 或 表單
    * `(3)類別名稱`
        * 用途說明
        * 規格說明
            * 顯示依前單限定的檢視表或表單名稱
    * `(4)上層表格`
        * 用途說明
        * 規格說明    
            * 顯示依前單限定的上層檢視表名稱
            * 前單未限定上層檢視表, 隱藏
    * `(5)載入`
        * 用途說明
        * 規格說明
            * 顯示依前單限定的檢視表或表單, 在[檢視表][link_Logical]或[表單加註_基本設定][link_FormAnnotation]中設定的接收參數, 載入 `(6)參數表格`
                * 當接收參數不存在`(7)參數名稱`中, 則新增資料列
                * 當接收參數已存在`(7)參數名稱`中, 則保留資料列
                * 當`(7)參數名稱`, 存在無效的接收參數, 則刪除資料列
        * 作業流程    
            * <ps>待補</ps>
    * `(6)參數表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton1]
    * `(7)參數名稱`
        * 用途說明
        * 規格說明
            * 參照 [挑選參數通則][link_ruledialog9], 依`(3)類別名稱`指定的表單中, 進行參數挑選, 回傳: 參數型態
    * `(8)資料型態`
        * 用途說明
        * 規格說明
            * 選項 文字/數字/日期/邏輯; 除能
            * 由`(7)參數名稱`回傳給值
    * `(9)給值類型`
        * 用途說明
        * 規格說明
            * 選項 固定值/參數/表單元件/隱藏元件/報表元件/函數/上層欄位/全域變數
            * 依前單, 決定呈現上述選項
                * 固定值: 皆可呈現
                * 函數: 皆可呈現
                * 參數: 由啟動表單開啟, 隱藏
                * 表單元件: 非元件加註、按鍵加註開啟, 隱藏
                * 隱藏元件: 非元件加註、按鍵加註開啟, 隱藏
                * 報表元件: 非報表加註、報表元件加註開啟, 隱藏
                * 全域變數: 非表單加註_資料來源開啟, 隱藏
                * 上層欄位: 當`(4)上層表格`有值, 才顯示
        * 作業流程    
            * <ps>待補</ps>
    * `(10)給值內容`
        * 用途說明
        * 規格說明
            * `(9)給值類型`=固定值: 自行輸入
            * `(9)給值類型`=函數: 參照 [挑選函數通則][link_ruledialog16], 過濾檢視表使用, 進行參數挑選
            * `(9)給值類型`=參數: 參照 [挑選參數通則][link_ruledialog9], 從駐留單元, 進行參數挑選
            * `(9)給值類型`=表單元件: 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 過濾不為隱藏元件 及 元件類型為 [註1][link_tag1], 進行元件挑選; 若元件為 個資加密且未解密欄位 或 密碼欄位, 則該元件顯示紅色字體
            * `(9)給值類型`=隱藏元件: 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 過濾為隱藏元件, 進行元件挑選; 若元件為 個資加密且未解密欄位 或 密碼欄位, 則該元件顯示紅色字體
            * `(9)給值類型`=報表元件: 參照 [挑選報表元件通則][link_ruledialog15], 從駐留報表中, 進行元件挑選 
            * `(9)給值類型`=全域變數: 參照 [挑選全域變數通則][link_ruledialog10], 進行全域變數挑選
            * `(9)給值類型`=上層欄位: 參照 [挑選檢視表元件通則][link_ruledialog8], 從`(4)上層表格`中, 進行元件挑選
    * `(11)儲存`
        * 用途說明
        * 規格說明
            * 前單為瀏覽狀態開啟本單, 除能
            * 參照 [權限驗証通則][link_ruleother6]
        * 作業流程    
            * <ps>待補</ps>

## <div id="save-action">儲存檢控</div>
* [存回不允空白檢控通則][link_ruleother7]
    * 檢控範圍
        * [基本][link_fieldbreak1]
            * `(7)參數名稱`、`(10)給值內容`, 不允空白
* [存回其它檢控通則][link_ruleother8]
    * 檢控範圍
        * [基本][link_fieldbreak1]
            * `(7)參數名稱`, 不允重複
                * 訊息內容: 參數不可重覆

## <div id="tag-desc">註解說明</div>
* <div id="tag1">註1</div>

    |元件類型 |
    |--------|
	|wTF.文字方塊 |
	|wTA.多行文字 |
	|wRB.按鈕選項 |
	|wDL.下拉選項 |
	|wLB.清單選項 |
	|wCB.核取方塊 |
	|wImg.圖片 |
	|wTree.樹狀清單 |
	|wPW.彈出視窗 |
	|wPT.2D樞紐 |
	|wCanvas.畫布 |
	|text.文字方塊(欄位資料) |
	|checkbox.核取方塊(欄位資料) |
	|select.下拉選項(欄位資料) |
	|popupwindow.彈出視窗(欄位資料) |
	|textarea.多行文字(欄位資料) |
	|image.圖片(欄位資料) |
	|liteText.文字方塊(多覽欄位資料) |
	|liteCheckbox.核取方塊(多覽欄位資料) |
	|liteTextarea.多行文字(多覽欄位資料) |
	|liteImage.圖片(多覽欄位資料) |
	|wHObj.隱藏元件 |

<!-- 圖片 -->
[image_parameter]:attachment/Parameter.png
[image_fieldbreak1]:attachment/fieldbreak1.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "基本"
[link_tag1]:#tag1 "註1"
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother2]:../RulesOther/README#ruleother2 "共用通則_其它/OnlineHelp通則"
[link_rulebutton1]:../RulesButton/README#rulebutton3 "共用通則_操作按鍵/操作表格記錄通則"
[link_ruleother6]:../RulesOther/README#ruleother6 "共用通則_其它/權限驗証通則"
[link_ruledialog9]:../RulesDialog/README#ruledialog9 "共用通則_開單操作/挑選參數通則"
[link_ruledialog7]:../RulesDialog/README#ruledialog7 "共用通則_開單操作/挑選表單元件通則"
[link_ruledialog15]:../RulesDialog/README#ruledialog15 "共用通則_開單操作/挑選報表元件通則"
[link_ruledialog10]:../RulesDialog/README#ruledialog10 "共用通則_開單操作/挑選全域變數通則"
[link_ruledialog8]:../RulesDialog/README#ruledialog8 "共用通則_開單操作/挑選檢視表元件通則"
[link_ruledialog16]:../RulesDialog/README#ruledialog16 "共用通則_開單操作/挑選函數通則"
[link_ruleother7]:../RulesOther/README#ruleother7 "共用通則_開單操作/存回不允空白檢控通則"
[link_ruleother8]:../RulesOther/README#ruleother8 "共用通則_開單操作/存回其它檢控通則"
[link_Logical]:../Logical/README "檢視表"
[link_FormAnnotation]:../FormAnnotation/README "表單加註_基本設定"
