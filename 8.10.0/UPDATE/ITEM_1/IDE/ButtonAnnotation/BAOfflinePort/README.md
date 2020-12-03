### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/12/3

## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        * 未提供
    * RWD
        * 未提供
    * MAE</br>
        * ![pic][image_BAOfflinePort]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 依規格定義-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格定義-主畫面 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_BAOfflinePort_block1]
    * `(1)按鈕名稱`
        * 用途說明
        * 規格說明
            * 參照 [使用多語詞庫通則][link_ruledialog2], 回傳:按鍵多語內容並顯示
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

* <p id="fieldbreak2" style="color:blue;font-weight:bold">交易內容</p>

   * ![pic][image_BAOfflinePort_block2]
    * `(1)交易名稱`
        * 用途說明
        * 規格說明
            * 單據於編輯狀態 或 單據於瀏覽狀態 且`(1)交易名稱`欄位有值 時, 致能
            * 開啟[離線資料交易][link_offlinePosting], 依駐留專案, 進行離線資料交易挑選, 異動時, 依下列條件決定回傳方式
                * 當`(2)傳遞參數`不存在記錄時, 回傳並顯示: 交易名稱
                * 當`(2)傳遞參數`存在記錄時, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 交易名稱變動將會清空傳遞參數，是否繼續？ / 按鍵: 確定、取消】
                    * 確定: 關閉訊息盒, 回傳並顯示: 交易名稱, 並清空`(3)參數名`
                    * 取消: 關閉訊息盒, 回到本單
    * `(2)傳遞參數`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
    * `(3)參數載入鍵`
        * 用途說明
        * 規格說明
            * 依`(1)交易名稱`內容取得 [離線資料交易_接收參數][link_offlinePosting_fieldbreak5] 的參數清單, 並依下列條件載入`參數名`及`型態`
                * [離線資料交易_接收參數][link_offlinePosting_fieldbreak5] 的`參數名`不存在表格內: 新增資料列
                * [離線資料交易_接收參數][link_offlinePosting_fieldbreak5] 的`參數名`已存在表格內: 保留資料列
                * 表格內存在無效的`參數名`: 刪除資料列
    * `(4)參數名`
        * 用途說明
        * 規格說明
            * 參照 [挑選參數通則][link_ruledialog9], 從`(1)交易名稱`中, 進行離線資料交易參數挑選, 回傳並顯示: 參數名
    * `(5)資料型態`
        * 用途說明
        * 規格說明
            * 依`(4)參數名`, 取得 [離線資料交易_接收參數][link_offlinePosting_fieldbreak5] 的`型態`顯示
    * `(6)給值類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 元件 / 固定值 / 參數 / 運算值
    * `(7)給值內容`
        * 用途說明
        * 規格說明
            * `(6)給值類別`=元件: 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳並顯示:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體
            * `(6)給值類別`=固定值: 自行輸入
            * `(6)給值類別`=參數: 參照 [挑選參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳並顯示:表單參數
            * `(6)給值類別`=運算式: 參照 [操作運算式通知][link_ruledialog18], 回傳並顯示: 運算式說明
    * `(8)失敗訊息`
        * 用途說明
        * 規格說明
            * 系統預設: 未勾選
            * 當有勾選時, 訊息內容致能, 並參照 [操作多語訊息及替代通則][link_ruledialog17], 否則 除能

## <div id="save-action">儲存檢控</div>
* 參照 [存回不允空白檢控通則][link_ruleother7]
    * [基本][link_fieldbreak1]
        * `優先序`, 不允空白
    * [交易內容][link_fieldbreak2]
        * `交易名稱`, 不允空白
        * 當`傳虒參數`有記錄時
            * `參數名`、`給值類別`, 不允空白
            * 當`給值類別`為元件、參數、運算值時, ` 給值內容`, 不允空白
* 參照 [存回其它檢控通則][link_ruleother8]
    * 同一按鍵的各加註內容的`優先序`是否有重複, 若重複, 顯示訊息
        訊息內容: 同一按鍵的各加註內容順序不允重複

<!-- 圖片 -->
[image_BAOfflinePort]:attachment/BAOfflinePort.png
[image_BAOfflinePort_block1]:attachment/BAOfflinePort_Block1.png
[image_BAOfflinePort_block2]:attachment/BAOfflinePort_Block2.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_fieldbreak2]:#fieldbreak2 "欄位說明/交易內容"

[link_offlinePosting]:/8.10.0/UPDATE/ITEM_1/IDE/DataTable/OfflinePosting/README.md
[link_offlinePosting_fieldbreak5]:/8.10.0/UPDATE/ITEM_1/IDE/DataTable/OfflinePosting/README#fieldbreak5


[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:/8.10.0/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
[link_rulebutton2]:/8.10.0/IDE/Specification/RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
[link_rulebutton3]:/8.10.0/IDE/Specification/RulesButton/README#rulebutton3 "共用通則_按鍵/操作表格記錄通則"

[link_ruledialog2]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruledialog7]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruledialog9]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog9 "共用通則_開啟單據/挑選參數通則"
[link_ruledialog11]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog11 "共用通則_開啟單據/設定按鍵執行條件表格通則"
[link_ruledialog17]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog17 "共用通則_開啟單據/操作多語訊息及替代通則"
[link_ruledialog18]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog18 "共用通則_開啟單據/操作運算式通則"




