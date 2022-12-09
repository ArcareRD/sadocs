## <div id="layout">版面相關</div>
* 版面

    ![pic][image_FADataSource]
* [版面資訊通則][link_ruleother1]
		
## <div id="form-action">動作說明</div>
* 依規格關聯-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格關聯-主畫面 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本區塊</p>

    ![pic][image_fieldbreak1]
    * `(1)表單名稱`
        * 用途說明
        * 規格說明
            * 依專案語系, 顯示表單多語名稱
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示傳入的表單料號
    * `(3)資料區`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單檔區通則][link_ruleother4]
    * `(4)元件對應`
        * 用途說明
        * 規格說明
            * 開啟 [元件對應][link_FAConnect], 限定取得: 本單元件、本單資料區欄位
    * `(5)檢視表`
        * 用途說明
        * 規格說明
            * 參照 [指定檢視表通則][link_ruledialog4], 從本專案中, 挑選檢視表, 回傳並顯示:檢視表名稱
            * 內容異動時, 顯示訊息盒【標題: 系統訊息 / 變動檢視表將清除[相關欄位]，是否繼續。 / 按鍵:確定、取消】
                * 確定: 清除欄位: `(6)參數`、`(7)過濾條件`、`(10)排序欄位`, 並關閉訊息盒
                * 取消: 關閉訊息盒
    * `(6)參數`
        * 用途說明
        * 規格說明
    * `(7)過濾條件`
        * 用途說明
        * 規格說明
            * 參照 [操作條件式通則][link_ruledialog1], 限定:檢視表須同`(2)檢視表`已設定的檢視表, 回傳並顯示:條件說明
    * `(8)排序依據表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
    * `(9)順序`
        * 用途說明
        * 規格說明    
            * 依序給流水號
    * `(10)排序欄位`
        * 用途說明
        * 規格說明
            * 參照 [挑選檢視表元件通則][link_ruledialog8], 限定:檢視表須同`(2)檢視表`中, 進行檢視表元件挑選, 且 不為密碼處理及個資加密的欄位, 回傳:檢視表元件
            * 參照 [個資加密提示通則][link_ruleother11]
    * `(11)排序方式`
        * 用途說明
        * 規格說明
            * 選項 升冪/降冪, 預設:升冪
    * `(12)關聯依據區塊`
        * 用途說明
        * 規格說明
            * 當`(3)資料區`=表頭, 本區塊隱藏
    * `(13)檔區`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單檔區通則][link_ruleother4] 限定: 本表單`(3)資料區` 及 除去本身檔區外
            * 若選項設定為無時. 清空`(15)欄位名稱`、`(16)父階欄位`
    * `(14)關聯依據表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
    * `(15)欄位名稱`
        * 用途說明
        * 規格說明
            * 參照 [挑選檢視表元件通則][link_ruledialog8], 限定:檢視表須同`(2)檢視表`中, 進行檢視表元件挑選, 且 不為密碼處理及個資加密的欄位, 回傳:檢視表元件
            * 參照 [個資加密提示通則][link_ruleother11]
    * `(16)父階欄位`
        * 用途說明
        * 規格說明
            * 參照 [挑選檢視表元件通則][link_ruledialog8], 限定:檢視表須同`(13)檔區`的`(2)檢視表`中, 進行檢視表元件挑選, 且 不為密碼處理及個資加密的欄位, 回傳:檢視表元件
            * 參照 [個資加密提示通則][link_ruleother11]
    * `(17)角色條件表格`
        * 用途說明
            * 作用時機: 運行時，若登入使用者對應的角色不是最高權限，且不是系統管理員時，則增加此表格設計的過濾條件至表單過濾條件中
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
            * 以下條件判斷本區塊顯示或隱藏
                * 當 [表單加註_基本設定][link_FormAnnotation_fieldbreak1]`表單類型`不為過濾條件查詢(條件多筆) 且 `(3)資料區`為表頭 , 則顯示
                * 當 [表單加註_基本設定][link_FormAnnotation_fieldbreak1]`表單類型`為過濾條件查詢(條件多筆) 且 `(3)資料區`為表身1, 則顯示
                * 非上述條件, 一律隱藏
    * `(18)條件說明`
        * 用途說明
        * 規格說明
            * 參照 [使用多語詞庫通則][link_ruledialog2], 回傳:多語料號, 顯示:多語詞彙
    * `(19)條件內容`
        * 用途說明
        * 規格說明
            * 參照 [操作條件式通則][link_ruledialog1], 回傳並顯示:條件說明
    * `(20)料號`
        * 用途說明
        * 規格說明
            * 顯示角色條件料號

## <div id="save-action">儲存檢控</div>
* 不允空白，以紅框線標註錯誤的欄位
    * [基本區塊][link_fieldbreak1]`資料區`、`檢視表`, 不允空白
    * 當 [基本區塊][link_fieldbreak1]`排序依據表格`有記錄, 則`排序欄位`、`排序方式`, 不允空白
    * 當 [基本區塊][link_fieldbreak1]`關聯依據表格`有記錄, 則`參數`、`型態`, 不允空白
    * 當 [基本區塊][link_fieldbreak1]`角色條件表格`有記錄, 則`條件說明`、`條件內容`, 不允空白
* 其它檢控
    * [基本區塊][link_fieldbreak1]`排序依據表格`, 至少要有一筆記錄
    * [基本區塊][link_fieldbreak1] 當`檔區`不為無, 則`關聯依據表格`, 至少要有一筆記錄

## <div id="other-desc">其它</div>
* 儲存後異動
    * 異動`資料區`, 將表單加註、元件加註、按鍵加註(含向下開啟的單據, 如:條件式)下所有引用相同檔區的內容一併修改
    * 異動`檢視表`, 將表單加註、元件加註、按鍵加註(含向下開啟的單據, 如:條件式)下所有引用相同檔區的檔區欄位一併清空
    * 刪除資料區, 將表單加註、元件加註、按鍵加註(含向下開啟的單據, 如:條件式)下所有引用相同檔區的檔區、檔區欄位一併清空
    * 異動`檢視表` 且 元件存在存在PhyEncryptionFieldUsage(資料表加密欄位使用狀況) 欄位.引用加密單元料號, 則 刪除對應的資料
    * 承上, 將規格關聯樹_單元名稱顯示黑色字體
* [MAE加註儲存通則][link_ruleother5]

<!-- 圖片 -->
[image_FADataSource]:attachment/FADataSource.png
[image_fieldbreak1]:attachment/fieldbreak1.png

<!-- 超連結 -->
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother4]:../RulesOther/README#ruleother4 "共用通則_其它/挑選表單檔區通則"
[link_ruledialog2]:../RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruledialog1]:../RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog4]:../RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"
[link_ruledialog8]:../RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_rulebutton2]:../RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
[link_rulebutton3]:../RulesButton/README#rulebutton3 "共用通則_按鍵操作/操作表格記錄通則"
[link_ruleother11]:../RulesOther/README#ruleother11 "共用通則_其它/個資加密提示通則"
[link_ruleother5]:../RulesOther/README#ruleother5 "共用通則_其它/MAE加註儲存通則"
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本區塊"
[link_FAConnect]:../FAConnect/README "元件對應"
[link_FormAnnotation_fieldbreak1]:../FormAnnotation/README#fieldbreak1 "表單加註_基本設定/區塊1"