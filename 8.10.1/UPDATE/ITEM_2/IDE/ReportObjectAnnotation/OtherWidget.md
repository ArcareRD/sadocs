非圖表元件規格定義
===
## 版面相關
* 版面</br>
    ![pic][image_other_widget]

## 欄位設定
* <p id="fieldbreak1" style="color:blue;">資料呈現</p>

    * ![pic][image_other_widget_block1]
    * `(1)模版`
        * 用途說明  
        * 規格說明
            * 當`元件類型`存在【rTF.文字方塊】則 顯示, 否則隱藏
            * 下拉選項: 資料模版清單, 過濾: 駐留筆專案, 顯示: 模版名稱, 排序: 模版名稱(升冪)
            * 系統預設: 專案預設模版的模版名稱 
            * 當本次選取模版的`貨幣符號`未勾選時, 清空: `(2)貨幣欄位`
        * 動作流程
            * ![pic][image_flow_roaModCode]
    * `(2)貨幣欄位`
        * 用途說明
        * 規格說明
            * 當`元件類型`存在【rTF.文字方塊】則 顯示, 否則隱藏
            * 當`(1)模版`的`模版組成`=貨幣, 且`貨幣符號`為已勾選, 則 致能, 否則 除能
            * 參照 [挑選報表元件通則][link_ruledialog15], 從駐留報表中, 進行報表元件挑選, 回傳:報表元件
        * 動作流程
            * ![pic][image_flow_roaCurrencyFieldNo]
    * `(3)長度限制`
        * 用途說明
        * 規格說明
            * 當`元件類型`【rTF.文字方塊】則 顯示, 否則隱藏
            * 自行輸入
    * `(4)與前行同值時`
        * 用途說明
        * 規格說明
            * 當`元件類型`【rTF.文字方塊、rTA.多行文字】則 顯示, 否則隱藏
            * 單一選項: 打印 / 省略
            * 系統預設: 打印
            * 當選項=打印時, 將駐留筆報表元件從[欄位同值不列印排序][object_print_sorting_list]中清除
            * 當選項=省略時, 將駐留筆報表元件新增至[欄位同值不列印排序][object_print_sorting_list]中
        * 動作流程
            * ![pic][image_flow_roaValue]
    * `(5)排序`
        * 用途說明
        * 規格說明
            * 當`元件類型`【rTF.文字方塊、rTA.多行文字】則 顯示, 否則隱藏
            * 當`(4)與前行同值時`=省略, 則 瀏覽及編輯狀態下皆致能, 否則 除能
            * 致能時, 執行開啟[欄位同值不列印排序][object_print_sorting_list]
        * 動作流程
            * ![pic][image_flow_roderby]
    * `(6)資料超長`
        * 用途說明
        * 規格說明
            * 當`元件類型`【rTF.文字方塊、rTA.多行文字】則 顯示, 否則隱藏
            * 單一選項: 不折行 / 折行固定行數 / 折行變動行數
            * 系統預設: 不折行
    * `(7)折行固定行數`
        * 用途說明
        * 規格說明
            * 當`元件類型`【rTF.文字方塊、rTA.多行文字】則 顯示, 否則隱藏
            * 當`(6)資料超長`=折行固定行數, 則 致能, 否則 除能
            * 致能時, 使用者自行輸入

* <p id="fieldbreak2" style="color:blue;">數值處理</p>

    * ![pic][image_other_widget_block2]
    * `(1)數據累計`
        * 用途說明
        * 規格說明
            * 當`(1)模版`的`模版組成`=貨幣或數字時, 則 致能, 否則 除能
            * 系統預設: 未勾選
    * `(2)換階重算`
        * 用途說明
        * 規格說明
            * 當`(1)數據累計`為勾選時, 且`資料區`=階尾N, 則 致能, 否則 除能
    * `(3)初始值`
        * 用途說明
        * 規格說明
            * 當`(2)換階重算`為勾選時, 則致能, 否則 除能
     * `(4)初始值_類別`
        * 用途說明
        * 規格說明
            * 當`(3)初始值`為勾選時, 則致能, 否則 除能
            * 下拉選項: 自訂 / 欄位 / 元件 / 參數
    * `(5)初始值_內容`
        * 用途說明
        * 規格說明
            * 當`(3)初始值_類別`=自訂, 由使用者自行輸入
            * 當`(3)初始值_類別`=欄位, 且[報表_資料來源][link_RADataSouce]`資料來源_類別`=檢視表, 參照 [挑選檢視表元件通則][link_ruledialog8], 從`資料來源_內容`中, 進行檢視表元件挑選, 限定: 不為密碼處理, 且不為個資加密未解密的欄位, 回傳:檢視表元件.
            * 當`(3)初始值_類別`=欄位, 且[報表_資料來源][link_RADataSouce]`資料來源_類別`=資料表, 參照 [挑選資料表元件通則][link_ruledialog5], 從`資料來源_內容`中, 進行資料表元件挑選, 限定: 不為密碼處理, 且不為個資加密的欄位, 回傳:資料表元件.
            * 當`(3)初始值_類別`=元件, 參照 [挑選報表元件通則][link_ruledialog15], 從駐留報表中, 進行報表元件挑選, 回傳:報表元件
            * 當`(3)初始值_類別`=參數, 參照[挑選報表參數通則][link_ruledialog9], 從駐留報表中, 進行報表參數挑選, 回傳:報表參數
            * 變色顯示, 請參照 [個資加密提示通則][link_ruleother11]
        * 動作流程
            * ![pic][image_flow_roaStartValue]
    * `(6)零值顯示`
        * 用途說明
        * 規格說明
            * 系統預設: 未勾選
    * `(7)數值加密`
        * 用途說明
        * 規格說明
            * 當`(1)模版`的`模版組成`=貨幣或數字時, 則 致能, 否則 除能
            * 系統預設: 未勾選

* <p id="fieldbreak3" style="color:blue;">給值內容</p>

    * ![pic][image_other_widget_block3]
    * `(1)給值內容`
        * 用途說明
        * 規格說明
            * 單一選項: 系統資訊 / 頁面資訊 / 公司LOGO / 操作者資料 / 來源給值 / 欄位組合 / 查表給值 / 代碼轉換
    * `(2)系統資訊`
        * 用途說明
        * 規格說明
            * 當`(1)給值內容`=系統資訊, 則 致能, 否則 除能
            * 單一選項: 系統日期 / 系統日期時間 / 系統時間
    * `(3)頁面資訊`
        * 用途說明
        * 規格說明
            * 當`(1)給值內容`=頁面資訊, 則 致能, 否則 除能
            * 單一選項: 頁次 / 總頁數 / 條文
    * `(4)頁面資訊_條文`
        * 用途說明
        * 規格說明
            * 當`(3)頁面資訊`=條文, 則 致能, 否則 除能
    * `(5)公司LOGO`
        * 用途說明
        * 規格說明
            * 當[基本][link_basic_fieldbreak1]的`元件類型`=rLogo.企業標誌, 則 顯示, 否則 隱藏 
            * 開啟[圖示設定][link_icon], 回傳: 圖示名稱
        * 動作流程
            * ![pic][image_flow_roaIconCode]      
    * `(6)操作者資料`
        * 用途說明
        * 規格說明
            * 當`(1)給值內容`=操作者資料, 則 致能, 否則 除能
            * 單一選項: 帳號 / 姓名 / 公司名稱 / 公司英文名稱
    * `(7)來源給值`
        * 用途說明
        * 規格說明
    * `(8)指定給值`
        * 用途說明
        * 規格說明
            * 當`(1)給值內容`=來源給值, 則 致能, 否則 除能
            * 下拉選項: 檔案資料 / 輸入參數 / 報表元件 
    * `(9)指定給值_內容`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 當`(1)給值內容`=來源給值, 則 致能, 否則 除能
            * 當`(7)指定給值`=檔案資料, 且[報表_資料來源][link_RADataSouce]`資料來源_類別`=檢視表, 參照 [挑選檢視表元件通則][link_ruledialog8], 從`資料來源_內容`中, 進行檢視表元件挑選, 限定: 不為密碼處理, 且不為個資加密未解密的欄位, 回傳: 檢視表元件.
            * 當`(7)指定給值`=檔案資料, 且[報表_資料來源][link_RADataSouce]`資料來源_類別`=資料表, 參照 [挑選資料表元件通則][link_ruledialog5]，從`資料來源_內容`中, 進行資料表元件挑選, 限定: 不為密碼處理, 且不為個資加密的欄位, 回傳: 資料表元件.
            * 當`(7)指定給值`=輸入參數, 參照 [挑選報表參數通則][link_ruledialog9], 從駐留報表中, 進行報表參數挑選, 回傳: 報表參數
            * 當`(7)指定給值`=報表元件, 參照 [挑選報表元件通則][link_ruledialog15], 從駐留報表中, 進行報表元件挑選, 回傳: 報表元件
            * 變色顯示, 請參照 [個資加密提示通則][link_ruleother11]
        * 動作流程
            * ![pic][image_flow_roaAsignedValue]
    * `(10)欄位組合`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 當`(1)給值內容`=欄位組合, 則 致能, 否則 除能
            * 參照 [操作運算式通則][link_ruledialog18], 限定: 不允查表, 回傳: 運算式說明
        * 動作流程
            * ![pic][image_flow_roaExpressionID]
    * `(11)查表給值`
        * 用途說明
        * 規格說明
    * `(12)檔案篩選`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 當`(1)給值內容`=查表給值, 則 致能, 否則 除能
            * 參照 [操作條件式通則][link_ruledialog1], 回傳: 條件說明
        * 動作流程
            * ![pic][image_flow_roaCondID]
    * `(13)給值欄位`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 當`(1)給值內容`=查表給值, 則 致能, 否則 除能
            * 當`(12)檔案篩選`無值, 或`(12)檔案篩選`的處理類別=無, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 請選擇檔案篩選-來源表格 / 按鍵: 確定】
                * 確定: 關閉訊息盒
            * 當`(12)檔案篩選`的處理類別=資料表, 參照 [挑選檢視表元件通則][link_ruledialog8], 從`(12)檔案篩選`對應的資料表中, 進行資料表元件挑選, 限定: 不為密碼處理, 且不為個資加密的欄位, 回傳: 資料表元件.
            * 當`(12)檔案篩選`的處理類別=檢視表, 參照 [挑選檢視表元件通則][link_ruledialog8], 從`(12)檔案篩選`對應的檢視表中, 進行檢視表元件挑選, 限定: 不為密碼處理, 且不為個資加密未解密的欄位, 回傳: 檢視表元件.
        * 動作流程
            * ![pic][image_flow_7_roaSourceCode]
    * `(14)代碼轉換`
        * 用途說明
        * 規格說明
    * `(15)檔案篩選`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 當`(1)給值內容`=代碼轉換, 則 致能, 否則 除能
            * 當[報表_資料來源][link_RADataSouce]`資料來源_類別`=檢視表, 參照 [挑選檢視表元件通則][link_ruledialog8], 從`資料來源_內容`中, 進行檢視表元件挑選, 限定: 不為密碼處理, 且不為個資加密未解密的欄位, 回傳: 檢視表元件.
            * 當[報表_資料來源][link_RADataSouce]`資料來源_類別`=資料表, 參照 [挑選資料表元件通則][link_ruledialog5]，從`資料來源_內容`中, 進行資料表元件挑選, 限定: 不為密碼處理, 且不為個資加密的欄位, 回傳: 資料表元件.
        * 動作流程
            * ![pic][image_flow_8_roaSourceCode]
    * `(16)代碼轉換表格`
        * 用途說明
        * 規格說明
            * 當`(1)給值內容`=代碼轉換, 則 致能, 否則 除能
            * 參照 [操作表格記錄通則][link_rulebutton3]
			* 表格列數最高顯示**3**列, 超過出現垂直捲軸
    * `(17)資料值`
        * 用途說明
        * 規格說明
            * 使用者自行輸入
    * `(18)對應詞庫碼`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 參照 [使用多語詞庫通則][link_ruledialog2], 回傳:按鍵多語內容並顯示
        * 動作流程
            * ![pic][image_flow_roapThesaurusID]	
    
* <p id="fieldbreak4" style="color:blue;">附加條件</p>

    * ![pic][image_other_widget_block4]
    * `(1)顯示條件`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 參照 [操作條件式通則][link_ruledialog1], 回傳: 條件說明
        * 動作流程
            * ![pic][image_flow_roaDisplayConID]
    * `(2)變色條件表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
			* 表格列數最高顯示**3**列, 超過出現垂直捲軸
    * `(3)條件內容`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 參照 [操作條件式通則][link_ruledialog1], 回傳: 條件說明
        * 動作流程
            * ![pic][image_flow_DiscolorationCondID]
    * `(4)前景字顏色`
        * 用途說明
        * 規格說明
            * 開啟顏色選擇器(Picker)
    * `(5)背景顏色`
        * 用途說明
        * 規格說明
            * 開啟顏色選擇器(Picker)

<!-- 圖片 -->
[image_other_widget]:attachment/ReportObjectAnnotation_OtherWidget.png
[image_other_widget_block1]:attachment/ReportObjectAnnotation_OtherWidget_block1.png
[image_other_widget_block2]:attachment/ReportObjectAnnotation_OtherWidget_block2.png
[image_other_widget_block3]:attachment/ReportObjectAnnotation_OtherWidget_block3.png
[image_other_widget_block4]:attachment/ReportObjectAnnotation_OtherWidget_block4.png

[image_flow_roaValue]:attachment/OtherWidetFlow_roaValue.png
[image_flow_roaStartValue]:attachment/OtherWidetFlow_roaStartValue.png
[image_flow_roapThesaurusID]:attachment/OtherWidetFlow_roapThesaurusID.png
[image_flow_roaModCode]:attachment/OtherWidetFlow_roaModCode.png
[image_flow_roaIconCode]:attachment/OtherWidetFlow_roaIconCode.png
[image_flow_roaExpressionID]:attachment/OtherWidetFlow_roaExpressionID.png
[image_flow_roaDisplayConID]:attachment/OtherWidetFlow_roaDisplayCondID.png
[image_flow_roaCondID]:attachment/OtherWidetFlow_roaCondID.png
[image_flow_roaAsignedValue]:attachment/OtherWidetFlow_roaAsignedValue.png
[image_flow_roderby]:attachment/OtherWidetFlow_orderby.png
[image_flow_DiscolorationCondID]:attachment/OtherWidetFlow_DiscolorationCondID.png
[image_flow_8_roaSourceCode]:attachment/OtherWidetFlow_8_roaSourceCode.png
[image_flow_7_roaSourceCode]:attachment/OtherWidetFlow_7_roaSourceCode.png
[image_flow_roaCurrencyFieldNo]:attachment/OtherWidetFlow_roaCurrencyFieldNo.png

<!-- 超連結 -->
[link_basic_fieldbreak1]:README#fieldbreak1 "報表元件/基本"
[object_print_sorting_list]:ReportObjectNoPrintSortingList.md
[link_RADataSouce]:{1}/RADataSource/README#fieldbreak1 "報表資料來源"
[link_icon]:{4}/IDE/Specification/Icon/README "圖示設定"

[link_ruledialog1]:{4}/IDE/Specification/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog2]:{4}/IDE/Specification/RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruledialog5]:{4}/IDE/Specification/RulesDialog/README#ruledialog5 "共用通則_開啟單據/挑選資料表元件通則"
[link_ruledialog8]:{4}/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_ruledialog9]:{4}/IDE/Specification/RulesDialog/README#ruledialog9 "共用通則_開啟單據/挑選報表參數通則"
[link_ruledialog15]:{4}/IDE/Specification/RulesDialog/README#ruledialog15 "共用通則_開啟單據/挑選報表元件通則"
[link_ruledialog18]:{4}/IDE/Specification/RulesDialog/README#ruledialog18 "共用通則_開啟單據/操作運算式通則"

[link_rulebutton3]:{4}/IDE/Specification/RulesButton/README#rulebutton3 "共用通則_按鍵/操作表格記錄通則"

[link_ruleother11]:{4}/IDE/Specification/RulesOther/README#ruleother11 "共用通則_其它/個資加密提示通則"