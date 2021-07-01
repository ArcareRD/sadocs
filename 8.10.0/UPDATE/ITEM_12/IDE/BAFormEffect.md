## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_BAFormEffect_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_BAFormEffect_MAE]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 依規格定義, 結構清單駐留節點: 表單特效, 顯示本單內容
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能
* 動作流程
    * ![pic][image_flow_open]


## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_BAFormEffect_block1]
    * `(1)按鈕名稱`
        * 用途說明
        * 規格說明
            * 顯示前單傳入按鍵名稱
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示前單傳入的按鍵料號
    * `(3)優先序`
        * 用途說明
        * 規格說明
            * 自行輸入, 1~999
    * `(4)執行條件`
        * 用途說明
        * 規格說明
            * 參照 [設定按鍵執行條件表格通則][link_ruledialog11]

* <p id="fieldbreak2" style="color:blue;font-weight:bold">處理內容</p>

    * ![pic][image_BAFormEffect_block2]
    * `(1)處理內容`
        * 用途說明
        * 規格說明
            * 當表單設計類型=STD、RWD, 畫面顯示單一選項: 關閉表單 / 切換頁籤 / 更新欄位 / 啟動按鍵 / 移動記錄 / 更新變數
            * 當表單設計類型=APP, 畫面顯示單一選項: 關閉表單 / 更新欄位 / 啟動按鍵 / 更新變數
    * `(2)關閉表單`
        * 用途說明
        * 規格說明

* <p id="fieldbreak3" style="color:blue;font-weight:bold">切換頁籤</p>

    * ![pic][image_BAFormEffect_block3]
    * `(1)切換頁籤`
        * 用途說明
        * 規格說明
            * 當表單設計類型=STD、RWD, 顯示本區塊, 否則 隱藏
            * 當[處理內容][link_fieldbreak2]的`處理內容`=切換頁籤, 本區塊 致能, 否則 除能
    * `(2)頁籤元件`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行頁籤元件挑選, 限定: 元件類型=wTab.頁籤區塊, 回傳: 表單元件
            * 變更內容時, 清空欄位: `(3)頁籤名稱`
        * 動作流程
            * ![pic][image_flow_baaSwitchingTabNo]
    * `(3)頁籤名稱`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 參照 [挑選表單元件通則][link_ruledialog7], 從`(2)頁籤元件`中, 挑選本次要切換的頁籤名稱, 限定: 元件類型=wTabItem.頁籤內容, 回傳: 表單元件

* <p id="fieldbreak4" style="color:blue;font-weight:bold">更新欄位</p>

    * ![pic][image_BAFormEffect_block4]
    * `(1)更新欄位`
        * 用途說明
        * 規格說明
            * 當[處理內容][link_fieldbreak2]的`處理內容`=更新欄位, 本區塊 致能, 否則 除能
    * `(2)影響筆數`
        * 用途說明
        * 規格說明
            * 單一選項: 單筆 / 多筆
            * 系統預設: 單筆
            * 當表單設計類型=RWD, 本欄位除能, 預設: 單筆, 否則 致能
            * 當表單設計類型=APP, 隱藏選項: 多筆, 否則 顯示
    * `(3)指定檔區`
        * 用途說明
        * 規格說明
            * 下拉選項: 表單檔區清單, 顯示: 檔區名稱, 過濾: 駐留筆表單
            * 當表單設計類型=RWD, 本欄位除能, 否則 致能
            * 當表單設計類型=APP, 本欄位隱藏, 否則 顯示
    * `(4)查表來源`
        * 用途說明
        * 規格說明
            * 單一選項: 無 / 資料表 / 檢視表
            * 系統預設: 無
            * 切換選項時, 清空欄位: `(5)來源表格`、`(6)檢視表參數`、`(7)過濾條件`
        * 動作流程
            * ![pic][image_flow_3_baaftDownQueryType]
    * `(5)來源表格`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 當`(4)查表來源`=資料表, 參照 [挑選資料表通則][link_ruledialog3], 從駐留專案中, 進行資料表挑選, 回傳並顯示: 資料表名
            * 當`(4)查表來源`=檢視表, 參照 [挑選檢視表通則][link_ruledialog4], 從駐留專案中, 進行檢視表挑選, 回傳並顯示: 檢視表名
            * 切換內容時, 清空欄位: `(6)檢視表參數`、`(7)過濾條件`
        * 動作流程
            * ![pic][image_flow_3_baaSourceTableNo]
    * `(6)檢視表參數`
        * 用途說明
        * 規格說明 
    * `(7)過濾條件`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 參照 [操作條件式通則][link_ruledialog1], 限定: 使用`(5)來源表格`, 且不提供使用個資加密未解密及密碼處理欄位, 回傳並顯示: 條件說明
                * 當表單設計類型=APP, 增加限定: 條件式運算元類別不允使用自定
    * `(8)更新欄位表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
			* 表格列數最高顯示**3**列, 超過出現垂直捲軸
    * `(9)目的欄位`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳: 表單元件
                * 當`(2)影響筆數`=單筆 且 表單設計類型=STD, 不限定表單元件檔區
                * 當`(2)影響筆數`=單筆 且 表單設計類型=RWD、APP, 限定: 表單元件檔區須為表頭
                * 當`(2)影響筆數`=多筆, 限定: 表單元件檔區=`(3)指定檔區`
            * 變色顯示, 請參照 [個資加密提示通則][link_ruleother11]
    * `(10)給值內容`
        * 用途說明
        * 規格說明 
            * 本欄位唯讀
		    * 參照 [操作運算式通則][link_ruledialog18], 限定: 使用`(5)來源表格`, 回傳: 運算式說明 
                * 當表單設計類型=APP, 增加限定: 運算式編輯方法只允使用函數

* <p id="fieldbreak5" style="color:blue;font-weight:bold">啟動按鍵</p>

    * ![pic][image_BAFormEffect_block5]
    * `(1)啟動按鍵`
        * 用途說明
        * 規格說明
            * 當[處理內容][link_fieldbreak2]的`處理內容`=啟動按鍵, 本區塊 致能, 否則 除能
    * `(2)按鈕名稱`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單按鍵通則][link_ruledialog13], 從駐留表單中, 進行元件挑選, 回傳: 表單元件
    * `(3)呼叫次數`
        * 用途說明
        * 規格說明
            * 單一選項: 單次 / 多次
            * 系統預設: 單次
    * `(4)多次設定區塊`
        * 用途說明
        * 規格說明
            * 當`(3)呼叫次數`=多次, 此區塊 致能, 否則 除能
    * `(5)表格元件`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 限定: 元件類型須存在【wGrd.多筆表格、wCtnr.元件容器、wGrdLite.多筆瀏覽】, 回傳: 表單元件
    * `(6)起始記錄`
        * 用途說明
        * 規格說明
            * 單一選項: 首筆 / 末筆 / 駐留筆
            * 系統預設: 首筆
    * `(7)依序方式`
        * 用途說明
        * 規格說明
            * 單一選項: 往後移動 / 往前移動
            * 系統預設選項及欄位除致能，請依下列條件
                * 當`(6)起始記錄`=首筆, 系統預設: 往後移動, 且本欄 除能
                * 當`(6)起始記錄`=末筆, 系統預設: 往前移動, 且本欄 除能
                * 其餘，系統預設: 往後移動, 且本欄 致能

* <p id="fieldbreak6" style="color:blue;font-weight:bold">移動記錄</p>

    * ![pic][image_BAFormEffect_block6]
    * `(1)移動記錄`
        * 用途說明
        * 規格說明
            * 當表單設計類型=STD、RWD, 顯示本區塊, 否則 隱藏
            * 當[處理內容][link_fieldbreak2]的`處理內容`=移動記錄, 本區塊 致能, 否則 除能
    * `(2)指定檔區`
        * 用途說明
        * 規格說明
            * 下拉選項: 表單檔區清單, 顯示: 檔區名稱, 過濾: 駐留筆表單
    * `(3)移動方式`
        * 用途說明
        * 規格說明
            * 單一選項: 末筆 / 首筆
            * 系統預設: 末筆
    
* <p id="fieldbreak7" style="color:blue;font-weight:bold">更新變數</p>

    * ![pic][image_BAFormEffect_block7]
    * `(1)更新變數`
        * 用途說明
        * 規格說明
            * 當[處理內容][link_fieldbreak2]的`處理內容`=更新變數, 本區塊 致能, 否則 除能
    * `(2)查表來源`
        * 用途說明
        * 規格說明
            * 單一選項: 無 / 資料表 / 檢視表
            * 系統預設: 無
            * 切換選項時, 清空欄位: `(3)來源表格`、`(4)檢視表參數`、`(5)過濾條件`
        * 動作流程
            * ![pic][image_flow_6_baaftDownQueryType]
    * `(3)來源表格`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 當`(2)查表來源`=資料表, 參照 [挑選資料表通則][link_ruledialog3], 從駐留專案中, 進行資料表挑選, 回傳並顯示: 資料表名
            * 當`(2)查表來源`=檢視表, 參照 [挑選檢視表通則][link_ruledialog4], 從駐留專案中, 進行檢視表挑選, 回傳並顯示: 檢視表名
            * 切換內容時, 清空欄位: `(4)檢視表參數`、`(5)過濾條件` 
        * 動作流程
            * ![pic][image_flow_6_baaSourceTableNo]
    * `(5)過濾條件`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 參照 [操作條件式通則][link_ruledialog1], 限定: 使用`(3)來源表格`, 且不提供使用個資加密未解密及密碼處理欄位, 回傳並顯示: 條件說明
                * 當表單設計類型=APP, 增加限定: 條件式運算元類別不允使用自定
    * `(6)更新變數表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
			* 表格列數最高顯示**3**列, 超過出現垂直捲軸
    * `(7)全域變數`
        * 用途說明
        * 規格說明
            * 開啟 [全域變數][link_GlobalVariable], 從駐留專案中, 進行全域變挑選, 回傳並顯示: 全域變數名
    * `(8)給值來源`
        * 用途說明
        * 規格說明 
            * 本欄位唯讀
		    * 參照 [操作運算式通則][link_ruledialog18], 限定: 使用`(3)來源表格`, 回傳: 運算式說明 
                * 當表單設計類型=APP, 增加限定: 運算式編輯方法不允使用自定


## <div id="save-action">儲存檢控</div>
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回不允空白檢控通則][link_ruleother7]
    * 當[處理內容內][link_fieldbreak2]的`處理內容`, 未選取任何選項
    * 當[處理內容內][link_fieldbreak2]的`處理內容`=切換頁籤時, 判斷下列欄位是否符合條件
        * [切換頁籤][link_fieldbreak3]的`頁籤元件`=空值
        * [切換頁籤][link_fieldbreak3]的`頁籤名稱`=空值
    * 當[處理內容內][link_fieldbreak2]的`處理內容`=更新欄位時, 判斷下列欄位是否符合條件
        * [更新欄位][link_fieldbreak4]的`影響筆數`=多筆, 且`指定檔區`=空值
        * [更新欄位][link_fieldbreak4]的`查表來源`=資料表或檢視表, 且`來源表格`=空值
        * [更新欄位][link_fieldbreak4]的`更新欄位表格`存在記錄, 且`目的欄位`=空值
        * [更新欄位][link_fieldbreak4]的`更新欄位表格`存在記錄, 且`給值內容`=空值
    * 當[處理內容內][link_fieldbreak2]的`處理內容`=啟動按鍵時, 判斷下列欄位是否符合條件
        * [啟動按鍵][link_fieldbreak5]的`按鈕名稱`=空值
        * [啟動按鍵][link_fieldbreak5]的`呼叫次數`=多次, 且`表格元件`=空值
    * 當[處理內容內][link_fieldbreak2]的`處理內容`=移動記錄時, 判斷下列欄位是否符合條件
        * [移動記錄][link_fieldbreak6]的`指定檔區`=空值
    * 當[處理內容內][link_fieldbreak2]的`處理內容`=更新變數時, 判斷下列欄位是否符合條件
        * [更新變數][link_fieldbreak7]的`查表來源`=資料表或檢視表, 且`來源表格`=空值
        * [更新變數][link_fieldbreak7]的`更新變數表格`存在記錄, 且`全域變數`=空值
        * [更新變數][link_fieldbreak7]的`更新變數表格`存在記錄, 且`給值來源`=空值
	
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
	* 當[基本][link_fieldbreak1]的`優先序`與同一按鍵下的優先序相同, 錯誤訊息內容: 同一按鍵的各加註內容順序不允重複
    * 當[處理內容內][link_fieldbreak2]的`處理內容`=更新欄位, 判斷下列欄位是否符合條件
        * [更新欄位][link_fieldbreak4]的`更新欄位表格`無任何記錄, 錯誤訊息內容: 更新欄位，至少須存在一筆給值記錄
        * [更新欄位][link_fieldbreak4]的`目的欄位`內容重覆, 錯誤訊息內容: 目的欄位不可重覆 
    * 當[處理內容內][link_fieldbreak2]的`處理內容`=更新變數, 判斷下列欄位是否符合條件
        * [更新變數][link_fieldbreak7]的`更新變數表格`無任何記錄, 錯誤訊息內容: 更新變數，至少須存在一筆給值記錄
        * [更新變數][link_fieldbreak7]的`全域變數`內容重覆, 錯誤訊息內容: 全域變數不可重覆
        * [更新變數][link_fieldbreak7]的`更新變數表格`記錄筆數>**8**筆, 錯誤訊息內容: 更新變數，最多只能存在八筆給值紀錄




<!-- 圖片 -->
[image_BAFormEffect_STD]:attachment/BAFormEffect_STD.png
[image_BAFormEffect_MAE]:attachment/BAFormEffect_MAE.png
[image_BAFormEffect_block1]:attachment/BAFormEffect_block1.png
[image_BAFormEffect_block2]:attachment/BAFormEffect_block2.png
[image_BAFormEffect_block3]:attachment/BAFormEffect_block3.png
[image_BAFormEffect_block4]:attachment/BAFormEffect_block4.png
[image_BAFormEffect_block5]:attachment/BAFormEffect_block5.png
[image_BAFormEffect_block6]:attachment/BAFormEffect_block6.png
[image_BAFormEffect_block7]:attachment/BAFormEffect_block7.png

[image_flow_open]:attachment/BAFormEffectFlow_open.png
[image_flow_baaSwitchingTabNo]:attachment/BAFormEffectFlow_baaSwitchingTabNo.png
[image_flow_3_baaftDownQueryType]:attachment/BAFormEffectFlow_3_baaftDownQueryType.png
[image_flow_3_baaSourceTableNo]:attachment/BAFormEffectFlow_3_baaSourceTableNo.png
[image_flow_6_baaftDownQueryType]:attachment/BAFormEffectFlow_6_baaftDownQueryType.png
[image_flow_6_baaSourceTableNo]:attachment/BAFormEffectFlow_6_baaSourceTableNo.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_fieldbreak2]:#fieldbreak2 "欄位說明/處理內容"
[link_fieldbreak3]:#fieldbreak3 "欄位說明/處理內容/切換頁籤"
[link_fieldbreak4]:#fieldbreak4 "欄位說明/處理內容/更新欄位"
[link_fieldbreak5]:#fieldbreak5 "欄位說明/處理內容/啟動按鍵"
[link_fieldbreak6]:#fieldbreak6 "欄位說明/處理內容/移動記錄"
[link_fieldbreak7]:#fieldbreak7 "欄位說明/處理內容/更新變數"

[link_GlobalVariable]:{3}/IDE/Specification/GlobalVariable/README.md "全域變數"

[link_ruleother1]:{3}/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:{3}/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:{3}/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
[link_ruleother11]:{3}/IDE/Specification/RulesOther/README#ruleother11 "共用通則_其它/個資加密提示通則"



[link_rulebutton2]:{3}IDE/Specification/RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
[link_rulebutton3]:{3}/IDE/Specification/RulesButton/README#rulebutton3 "共用通則_按鍵/操作表格記錄通則"

[link_ruledialog1]:{3}/IDE/Specification/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog3]:{3}/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_ruledialog4]:{3}/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"
[link_ruledialog7]:{3}/IDE/Specification/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruledialog18]:{3}/IDE/Specification/RulesDialog/README#ruledialog18 "共用通則_開啟單據/操作運算式通則"

[link_ruledialog11]:{3}/IDE/Specification/RulesDialog/README#ruledialog11 "共用通則_開啟單據/設定按鍵執行條件表格通則"
[link_ruledialog13]:{3}/IDE/Specification/RulesDialog/README#ruledialog13 "共用通則_開啟單據/挑選表單按鍵通則"