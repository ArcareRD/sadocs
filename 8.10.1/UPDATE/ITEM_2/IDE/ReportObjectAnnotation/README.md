## <div id="layout">版面相關</div>
* 版面
    ![pic][image_basic]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>

* 依報表規格定義, 結構清單駐留節點: 報表元件名稱, 顯示本單內容
* 依報表規格定義, 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能
* 動作流程
    * ![pic][image_flow_open]

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_basic_block1]
    * `(1)元件名`
        * 用途說明
        * 規格說明
			* 本欄位唯讀
            * 參照 [使用多語詞庫通則][link_ruledialog2], 回傳:按鍵多語內容並顯示
        * 動作流程
            * ![pic][image_flow_widget_name]
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示前單傳入的報表元件料號
			* 新增存回時, 由系統依編碼原則: 固定值(RI) + Site no + 流水8碼給值. (ex. RI999500000001)
            * 本欄位除能, 不提供編輯
    * `(3)元件類型`
        * 用途說明
        * 規格說明
            * 依平台語系顯示報表元件類型
            * 本欄位除能, 不提供編輯
    * `(4)資料區`
        * 用途說明
        * 規格說明
            * 依平台語系顯示報表階層名稱
            * 本欄位除能, 不提供編輯
    * `(5)規格定義區塊`
        * 用途說明
        * 規格說明
            * 依報表元件類型，將對應的規格頁面顯示在本區塊內
                * 報表元件類型存在【rEChart.嵌入圖表】, 顯示: [圖表介面](rEchart)
                * 報表元件類型存在【rTP.文字標題、rTF.文字方塊、rTA.多行文字、rCB.核取方塊、rBC.條碼、rImg.圖片、rLogo.企業標誌】, 顯示: [非圖表介面](OtherWidget)
            * 當顯示內容高於本區塊最大高度, 則出現垂直捲軸

## <div id="save-action">儲存檢控</div>

* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回不允空白檢控通則][link_ruleother7]
    * [資料呈現][link_otherwidget_fieldbreak1]
        * 當`長度`=空值
        * 當`資料超長`=折行固定行數, 且`折行固定行數`=空值
    * [數值處理][link_otherwidget_fieldbreak2]
        * 當`初始值`已勾選, 且`初始值_類別`未選取任何選項
        * 當`初始值_類別`已選取選項, 且`初始值_內容`=空值
    * [給值內容][link_otherwidget_fieldbreak3]
        * 當`給值內容`未選取任何選項
        * 當`給值內容`=系統資訊, 且系統資訊選項區塊未選取任何選項
        * 當`給值內容`=頁面資訊, 且頁面資訊選項區塊未選取任何選項
            * 頁面資訊選項=條文, 且`頁面資訊_條文`=空值
        * 當`給值內容`=公司LOGO, 且`公司LOGO`=空值
        * 當`給值內容`=操作者資料, 且操作者資料選項區塊未選取任何選項
        * 當`給值內容`=來源給值, 且`指定給值`=空值
        * 當`給值內容`=來源給值, 且`指定給值_內容`=空值
        * 當`給值內容`=欄位組合，`欄位組合`=空值
        * 當`給值內容`=查表給值, 且`檔案篩選`=空值
        * 當`給值內容`=查表給值, 且`給值欄位`=空值
        * 當`給值內容`=代碼轉換, 且`檔案篩選`=空值
        * 當`給值內容`=代碼轉換, 且`代碼轉換表格`表格存在記錄, 且`資料值`=空值
        * 當`給值內容`=代碼轉換, 且`代碼轉換表格`表格存在記錄, 且`對應詞庫碼`=空值
    * [附加條件][link_otherwidget_fieldbreak4]
        * 當`變色條件表格`存在記錄, 且`條件內容`=空值
    * [圖表類型區塊][link_rEchart_fieldbreak1]
        * 當[基本][link_fieldbreak1]的`元件類型`=rEChart.嵌入圖表, 且`圖表類型`=空值
        * 當`可空白`為未勾選, 且`來源型態`=空值
        * 當`來源型態`<>空值, 且`來源內容`=空值
	
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
    * 當[資料呈現][link_otherwidget_fieldbreak1]的`長度`內容不為數值, 顯示錯誤訊息內容: 長度須入為數值
    * 當[附加條件][link_otherwidget_fieldbreak4]的`變色條件表格`存在記錄, 且`前景字顏色`、`背景顏色`皆為空, 顯示錯誤訊息內容: 前景字顏色跟背景顏色，不可同時空白
    * 當[給值內容][link_otherwidget_fieldbreak3]的`給值內容`=代碼轉換, 且`代碼轉換表格`無任何記錄, 顯示錯誤訊息內容: 給值內容等於代碼轉換時, 則代碼轉換表格至少存在一筆記錄
    * 圖示用途, 必須是LOGO
    * 當[基本][link_fieldbreak1]的`元件類型`=rLogo.企業標誌, 且[給值內容][link_otherwidget_fieldbreak3]的給值內容<>公司LOGO, 顯示錯誤訊息內容: 當報表元件類型='LOGO' 時, 加註時限定資料來源選項只能是公司LOGO
    * 當[基本][link_fieldbreak1]的`元件類型`<>rLogo.企業標誌, 且[給值內容][link_otherwidget_fieldbreak3]的給值內容=公司LOGO, 顯示錯誤訊息內容: 當報表元件類型<>'LOGO' 時, 加註時限定資料來源選項不可以是公司LOGO
    * 當[給值內容][link_otherwidget_fieldbreak3]的`給值內容`=來源給值, 依`指定給值_內容`取得對應的資料型態, 若為數值型態, 且[資料呈現][link_otherwidget_fieldbreak1]`模版`的`模版組成`不為數字或貨幣, 顯示錯誤訊息內容: 當元件加註有指定模版時, 模版的型態與對應欄位的型態必須對應一致  
    * 當[數值處理][link_otherwidget_fieldbreak2]的`數據累計`為勾選時, 則[給值內容][link_otherwidget_fieldbreak3]的`給值內容`<>來源給值或欄位組合, 顯示錯誤訊息內容: 加註內容含有查表，系統暫不提供查表欄位的累計，請重新設定加註內容
    
    

<!-- 圖片 -->
[image_basic]:attachment/ReportObjectAnnotation_Basic.png
[image_basic_block1]:attachment/ReportObjectAnnotation_Basic_block1.png
[image_flow_open]:attachment/ReportWidgetAnnotationFlow_open.png
[image_flow_widget_name]:attachment/ReportWidgetAnnotationFlow_widget_name.png



<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_otherwidget_fieldbreak1]:OtherWidget#fieldbreak1 "欄位說明/資料呈現"
[link_otherwidget_fieldbreak2]:OtherWidget#fieldbreak2 "欄位說明/數值處理"
[link_otherwidget_fieldbreak3]:OtherWidget#fieldbreak3 "欄位說明/給值內容"
[link_otherwidget_fieldbreak4]:OtherWidget#fieldbreak4 "欄位說明/附加條件"
[link_rEchart_fieldbreak1]:rEchart#fieldbreak1 "欄位說明/圖表類型區塊"
[link_ruleother1]:{4}/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:{4}/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:{4}/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"

[link_rulebutton2]:{4}/IDE/Specification/RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
[link_rulebutton3]:{4}/IDE/Specification/RulesButton/README#rulebutton3 "共用通則_按鍵/操作表格記錄通則"

[link_ruledialog2]:{4}/IDE/Specification/RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"