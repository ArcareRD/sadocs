## <div id="layout">版面相關</div>
* 版面
    ![pic][image_radatasource]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>

* 依報表規格定義, 結構清單駐留節點:資料來源, 顯示本單內容
* 依報表規格定義, 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能
* 動作流程
    * ![pic][image_flow_open]

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_radatasource_block1]
    * `(1)報表名稱`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示前單傳入的報表料號
            * 本欄位除能, 不提供編輯
    * `(3)資料來源_類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 請選擇 / 資料表 / 檢視表
            * 系統預設: 請選擇
            * 當切換`(3)資料來源_類別`時，清空 `(4)資料來源_名稱`、`(5)參數`、`(7)過濾條件`、`(10)欄位名`
        * 動作流程
            * ![pic][image_flow_raSourKind]
    * `(4)資料來源_名稱`
        * 用途說明
        * 規格說明
            * 當`(3)資料來源_類別`=檢視表時, 參照 [挑選檢視表通則][link_ruledialog4], 從駐留專案中, 進行檢視表挑選, 回傳並顯示: 檢視表名
            * 當`(3)資料來源_類別`=資料表時, 參照 [挑選資料表通則][link_ruledialog3], 從駐留專案中, 進行資料表挑選, 回傳並顯示: 資料表名
            * 當內容異動時, 清空`(5)參數`、`(7)過濾條件`、`(10)欄位名`
        * 動作流程
            * ![pic][image_flow_raSourCode]
    * `(6)元件對應`
        * 用途說明
        * 規格說明
            * 編輯狀態下, 除能, 否則 致能
            * 致能時, 可開啟[報表元件對應][]
    * `(7)過濾條件`
        * 用途說明
        * 規格說明
            * 參照 [操作條件式通則][link_ruledialog1], 限定: 使用`(4)資料來源_名稱`, 且不提供使用個資加密及密碼處理欄位, 回傳並顯示: 條件說明
        * 動作流程
            * ![pic][image_flow_raFilterID]
    * `(8)來源排序表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
            * 表格列數最高顯示**7**列, 超過出現垂直捲軸
    * `(9)欄位名`
        * 用途說明
        * 規格說明
            * 當`(3)資料來源_類別`=檢視表: 參照 [挑選檢視表元件通則][link_ruledialog8], 從`(4)資料來源_名稱`中, 進行檢視表元件挑選, 限定: 不為密碼處理, 且不為個資加密的欄位, 回傳:檢視表元件.
            * 當`(3)資料來源_類別`=資料表: 參照 [挑選資料表元件通則][link_ruledialog5], 從`(4)資料來源_名稱`中, 進行資料表元件挑選, 限定: 不為密碼處理, 且不為個資加密未解密的欄位, 回傳:資料表元件.
            * 變色顯示, 請參照 [個資加密提示通則][link_ruleother11]
        * 動作流程
            * ![pic][image_flow_rasCode]
    * `(10)排序`
        * 用途說明
        * 規格說明
            * 下拉選項: 請選擇 / 升冪 / 降冪
            * 系統預設: 請選擇
    * `(11)輸出LOG`
        * 用途說明
        * 規格說明
            * 系統預設: 不勾選
    * `(12)記錄鍵值`
        * 用途說明
        * 規格說明
            * 當`(12)輸出LOG`為未勾選時, 除能, 否則 致能
            * 致能時, 下拉選項: 報表接收參數清單, 限定: 目前駐留報表
    * `(13)檔案加密`
        * 用途說明
        * 規格說明
            * 系統預設: 不勾選
    * `(14)加密鍵值`
        * 用途說明
        * 規格說明
            * 當`(14)檔案加密`為未勾選時, 除能, 否則 致能
            * 致能時, 下拉選項: 報表接收參數清單, 限定: 目前駐留報表 且 欄位資料型態=文字



## <div id="save-action">儲存檢控</div>

* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回不允空白檢控通則][link_ruleother7]
    * 當`(3)資料來源_類別`=請選擇
    * 當`(4)資料來源_名稱`=空值
    * 當`(8)來源排序表格`存在記錄, 且`(9)欄位名`=空值
    * 當`(8)來源排序表格`存在記錄, 且`(10)排序`=請選擇
    * 當`(11)輸出LOG`已勾選, 且`(12)記錄鍵值`=空值
    * 當`(13)檔案加密`已勾選, 且`(14)加密鍵值`=空值
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
    * 當`(9)欄位名`為個資加密且未解密或密碼處理欄位時, 錯誤訊息內容: 排序欄位: `(9)欄位名`內容, 不允為個資加密且未解密或密碼處理欄位

<!-- 圖片 -->
[image_radatasource]:attachment/ReportAnnotation_DataSource.png
[image_radatasource_block1]:attachment/ReportAnnotation_DataSource_block1.png

[image_flow_open]:attachment/RADataSoruceFlow_open.png
[image_flow_raSourKind]:attachment/RADataSoruceFlow_raSourKind.png
[image_flow_raSourCode]:attachment/RADataSoruceFlow_raSourCode.png
[image_flow_raFilterID]:attachment/RADataSoruceFlow_raFilterID.png
[image_flow_rasCode]:attachment/RADataSoruceFlow_rasCode.png

 <!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother1]:/8.10.1/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:/8.10.0/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"

[link_ruledialog1]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog2]:/8.10.1/IDE/Specification/RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_ruledialog4]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"
[link_ruledialog5]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog5 "共用通則_開啟單據/挑選資料表元件通則"
[link_ruledialog8]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"

[link_rulebutton2]:/8.10.1/IDE/Specification/RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
[link_rulebutton3]:/8.10.1/IDE/Specification/RulesButton/README#rulebutton3 "共用通則_按鍵/操作表格記錄通則"

