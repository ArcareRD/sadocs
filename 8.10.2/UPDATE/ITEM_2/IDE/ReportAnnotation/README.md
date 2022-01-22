## <div id="layout">版面相關</div>
* 版面
    ![pic][image_report_annotation]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>

* 依報表規格定義, 結構清單駐留節點: 基本設定, 顯示本單內容
* 依報表規格定義, 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能
* 動作流程
    * ![pic][image_flow_open]

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_report_annotation_block1]
    * `(1)報表名稱`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 參照 [使用多語詞庫通則][link_ruledialog2], 回傳:報表名稱的多語內容並顯示
        * 動作流程
            * ![pic][image_flow_report_name]
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示前單傳入的報表料號
            * 本欄位除能, 不提供編輯
    * `(3)接收參數表格`
        * 用途說明
            * 當報表接受外部的條件指定時，可利用參數方式接收資訊，做為後續處理的依據。
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
            * 表格列數最高顯示**10**列, 超過出現垂直捲軸
    * `(4)項次`
        * 用途說明
        * 規格說明
            * 依記錄順序顯示流水號
    * `(5)參數名`
        * 用途說明
        * 規格說明
            * 由使用者自行輸入
    * `(6)型態`
        * 用途說明
        * 規格說明
            * 下拉選項: 請選擇 / 文字 / 數字 / 日期 / 邏輯
            * 系統預設: 請選擇
    * `(7)說明`
        * 用途說明
        * 規格說明
            * 由使用者自行輸入
    * `(8)使用時機`
        * 用途說明
            * 輸入本報表的使用時機
        * 規格說明
            * 由使用者自行輸入

## <div id="save-action">儲存檢控</div>

* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回不允空白檢控通則][link_ruleother7]
    * 當`(5)參數名`=空值
    * 當`(6)型態`=請選擇
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
    * 當`(5)參數名`存在空白字元, 錯誤訊息內容: 參數名:`(5)參數名`, 不允有空白字元

<!-- 圖片 -->
[image_report_annotation]:attachment/ReportAnnotation_Basic.png
[image_report_annotation_block1]:attachment/ReportAnnotation_Basic_block1.png

[image_flow_open]:attachment/ReportAnnotationFlow_open.png
[image_flow_report_name]:attachment/ReportAnnotationFlow_report_name.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother1]:/8.10.1/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:/8.10.0/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"

[link_ruledialog2]:/8.10.1/IDE/Specification/RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"

[link_rulebutton2]:/8.10.1/IDE/Specification/RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
[link_rulebutton3]:/8.10.1/IDE/Specification/RulesButton/README#rulebutton3 "共用通則_按鍵/操作表格記錄通則"

