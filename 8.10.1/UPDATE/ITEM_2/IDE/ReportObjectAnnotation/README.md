## <div id="layout">版面相關</div>
* 版面
    ![pic][image_basic]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>

* 依報表規格定義, 結構清單駐留節點: 報表元件名稱, 顯示本單內容
* 依報表規格定義, 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_basic_block1]
    * `(1)元件名`
        * 用途說明
        * 規格說明
			* 本欄位唯讀
            * 參照 [使用多語詞庫通則][link_ruledialog2], 回傳:按鍵多語內容並顯示
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
    * `(4)資料區`
        * 用途說明
        * 規格說明
            * 依平台語系顯示報表階層名稱
    * `(5)規格定義區塊`
        * 用途說明
        * 規格說明
            * 依報表元件類型，將對應的規格頁面顯示在本區塊內
                * 報表元件類型存在【rEChart.嵌入圖表】, 顯示: [圖表介面](rEchart)
                * 報表元件類型存在【rTP.文字標題、rTF.文字方塊、rTA.多行文字、rCB.核取方塊、rBC.條碼、rImg.圖片、rLogo.企業標誌】, 顯示: [非圖表介面](OtherWidget)
            * 當顯示內容高於本區塊最大高度, 則出現垂直捲軸

## <div id="save-action">儲存檢控</div>

* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回不允空白檢控通則][link_ruleother7]
    * 當`(5)參數名`=空值
    * 當`(6)型態`=請選擇
	
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
	* 當`(5)參數名`存在空白字元, 錯誤訊息內容: 參數名:`(5)參數名`, 不允有空白字元

<!-- 圖片 -->
[image_basic]:attachment/ReportObjectAnnotation_Basic.png
[image_basic_block1]:attachment/ReportObjectAnnotation_Basic_block1.png


<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:/8.10.0/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"

[link_rulebutton2]:/8.10.1/IDE/Specification/RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
[link_rulebutton3]:/8.10.1/IDE/Specification/RulesButton/README#rulebutton3 "共用通則_按鍵/操作表格記錄通則"

[link_ruledialog2]:/8.10.1/IDE/Specification/RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"