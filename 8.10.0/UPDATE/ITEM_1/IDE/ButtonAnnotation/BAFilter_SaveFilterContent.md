## <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/12/4

## <div id="behavior-layout">版面相關</div>
* 版面
    * ![pic][image_savefiltercontent]

## <div id="behavior-form-action">動作說明</div>
* 依 [按鍵加註-資料過濾-離線過濾][link_BAFilter] 的`儲存過濾內容`開啟, 顯示本單內容
* 下列欄位, 除規格說明中有額外說明, 否則所有欄位須判斷: 若前單為瀏覽狀態: 除能; 編輯狀態: 致能

## <div id="behavior-object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_savefiltercontent_block1]
    * `(1)寫入資料表`
        * 用途說明
        * 規格說明
            * 參照 [挑選資料表通則][link_ruledialog3], 從駐留專案中, 進行資料表挑選, 限定使用`離線資料上傳用`未勾選的資料表,  回傳並顯示: 表格名稱
    * `(2)寫入欄位表格`
        * 用途說明
        * 規格說明
            * 參照 [操作一般表格通則][link_rulebutton3]
    * `(3)目的欄位`
        * 用途說明
        * 規格說明
            * 參照 [挑選資料表元件通則][link_ruledialog5], 限定使用`(1)寫入資料表`
    * `(4)給值類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 離線批號 / 表單元件 / 表單參數 / 全域變數
            * 異動時清除欄位: `(7)給值內容`
    * `(5)給值內容`
        * 用途說明
        * 規格說明
            * 當`(6)給值類別`=離線批號: 設計者無須輸入內容, 運行時由系統回傳離線批號寫入
            * 當`(6)給值類別`=表單元件: [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體紅色字體
            * 當`(6)給值類別`=表單參數: [挑選表單參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳:表單參數
            * 當`(6)給值類別`=全域變數: [挑選全域變數通則][link_ruledialog10], 從駐留專案中, 進行全域變數挑選, 回傳:全域變數
    * `(6)確定`
        * 用途說明
        * 規格說明
            * 若前單為瀏覽狀態: 隱藏; 編輯狀態: 顯示
            * 將本次修改資料回傳前單後關閉本單
    * `(7)取消`
        * 用途說明
        * 規格說明
            * 若前單為瀏覽狀態: 隱藏; 編輯狀態: 顯示
            * 顯示訊息盒【標題: 系統訊息 / 訊息內容: 資料尚未儲存, 是否確定取消? / 按鍵: 確定、取消】
                * 確定: 關閉訊息盒, 直接關閉本單
                * 取消: 關閉訊息盒, 回到本單畫面


## <div id="save-action">確定檢控</div>
* 參照 [存回不允空白檢控通則][link_ruleother7]
    * [基本][link_fieldbreak1]
        * `寫入資料表`, 不允空白
        * 當`寫入欄位表格`存在記錄, `目的欄位`、`給值類別`, 不允空白
        * 當`給值類別`為表單元件/表單參數/全域變數時, `給值內容`不允空白

* 參照 [存回其它檢控通則][link_ruleother8]
    * [基本][link_fieldbreak1]
        * `目的欄位`, 不允重複
            * 訊息內容: 同一按鍵的各加註內容順序不允重複


<!--圖片 -->
[image_savefiltercontent]:attachment/BAFilter_SaveFilterContent.png
[image_savefiltercontent_block1]:attachment/BAFilter_SaveFilterContent_Block1.png


<!--超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_BAFilter]:BAFilter.md
[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother2]:/8.10.0/IDE/Specification/RulesOther/README#ruleother2 "共用通則_其它/單據異動資料按鍵操作通則"
[link_ruleother7]:/8.10.0/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"

[link_rulebutton3]:/8.10.0/IDE/Specification/RulesButton/README#rulebutton3 "共用通則_按鍵/操作表格記錄通則"

[link_ruledialog7]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruledialog9]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog9 "共用通則_開啟單據/挑選表單參數通則"
[link_ruledialog10]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog10 "共用通則_開啟單據/挑選全域變數通則"
[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_ruledialog5]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog5 "共用通則_開啟單據/挑選資料表元件通則"