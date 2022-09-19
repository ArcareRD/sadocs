## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_badialog_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_badialog_APP]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>

* 依規格定義-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格定義-主畫面 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能


## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_badialog_block1]
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
            * 同一按鍵下的執行項目有多筆時, 可利用本欄位, 排定執行的順序
        * 規格說明
            * 自行輸入, 1~999
    * `(4)執行條件`
        * 用途說明
            * 依指定條件決定是否執行本次設定的開單內容
        * 規格說明
            * 參照 [設定按鍵執行條件表格通則][link_ruledialog11]

* <p id="fieldbreak2" style="color:blue;font-weight:bold">開單內容</p>

    * ![pic][image_badialog_block2]
     * `(1)表單名稱`
        * 用途說明
            * 指定要開啟的表單
        * 規格說明
            *  參照 [挑選表單通則][link_ruledialog6], 從駐留專案中, 進行表單挑選, 回傳並顯示: 表單名、表單主要資料來源
                * 限定: 當設計類型=傳統表單/自適應, 不允挑選APP表單, 反之, 設計類型=APP，只允挑選APP表單
            * 異動表單時, 清空欄位:`(2)資料來源`、`(3)資料過濾`、`(4)駐留條件`、`(5)樹根指定`
    * `(2)資料來源`
        * 用途說明
            * 開啟表單後, 可依指定條件決定本次可查看的記錄筆數範圍
        * 規格說明
            * 依`(1)表單名稱`的表單種類，取得主要資料來源的檢視表名稱顯示
                * 表單種類=過濾條件查詢（條件多筆）, 取得表身1資料區的資料來源, 其餘取得表頭資料區的資料來源
    * `(3)資料過濾`
        * 用途說明
        * 規格說明
            * 當`(1)表單名稱`有值, 則 致能, 否則 除能
            * 致能時, 參照 [操作條件式通則][link_ruledialog1], 限定: 使用`(2)資料來源`, 回傳並顯示: 條件說明
    * `(4)駐留條件`
        * 用途說明
            * 開啟表單後，可依指定條件決定駐留至哪一筆記錄
        * 規格說明
            * 當`(1)表單名稱`有值, 則 致能, 否則 除能
            * 參照 [操作條件式通則][link_ruledialog1], 限定: 使用`(2)資料來源`, 回傳並顯示: 條件說明
    * `(5)樹根指定`
        * 用途說明
            * 當開啟為樹狀表單時, 可依指定條件決定樹節點的駐留位置
        * 規格說明
            * 當表單設計類型=APP, 則 顯示, 否則 隱藏
            * 當本欄顯示時, 且`(1)表單名稱`有值, 則 致能, 否則 除能
            * 致能時, 參照 [操作條件式通則][link_ruledialog1], 限定: 使用`(2)資料來源`, 回傳並顯示: 條件說明
    * `(6)表單異動_限定`
        * 用途說明
            * 是否限定表單異動模式
        * 規格說明
            * 當表單設計類型=APP, 則 顯示, 否則 隱藏
            * 系統預設: 不勾選
    * `(7)表單異動_模式`
        * 用途說明
            * 開啟表單後, 依勾選模式限定使用者可操作的表單異動方式
        * 規格說明
            * 當表單設計類型=APP, 則 顯示, 否則 隱藏
            * 複選選項: 新增 / 修改 / 刪除
            * 當`(6)表單異動_限定`勾選時，本區塊選項致能, 否則 除能
    * `(8)進入模式`
        * 用途說明
            * 開啟表單後, 預設進入的表單異動方式
        * 規格說明
            * 當表單設計類型=APP, 則 顯示, 否則 隱藏
            * 單一選項: 瀏覽 / 新增 / 修改
            * 系統預設: 瀏覽
    * `(9)開單模式`
        * 用途說明
            * 開啟的表單呈現方式
                * 分頁: 以分頁(即頁籤)開啟表單
                * 視窗: 以另一個視窗開啟表單. 此開啟方式, 系統要求`(10)互動模式`只允為被動
        * 規格說明
            * 當表單設計類型=APP, 則 顯示, 否則 隱藏
            * 單一選項: 分頁 / 視窗
            * 系統預設: 分頁
    * `(10)互動模式`
        * 用途說明
            * 設定開啟的表單與本單的互動
                * 主動: 表示開啟的表單具獨立性與本單沒有關連
                * 被動: 表示開啟的表單必須依附在本單的條件之下, 必須操作結束才可回本單
                * 互動: 表示可個自操作, 但可利用表單的溝通訊息做到關聯, 互相影響顯示內容
                * 斷離: 表示開啟表單後, 立即關閉本單
        * 規格說明
            * 當表單設計類型=APP, 則 顯示, 否則 隱藏
            * 單一選項: 主動 / 互動 / 被動 / 斷離
            * 系統預設: 被動
            * 當`(9)開單模式`=視窗, 預設選項: 被動, 且將選項除能

* <p id="fieldbreak3" style="color:blue;font-weight:bold">傳遞參數</p>

    * ![pic][image_badialog_block3]
     * `(1)傳遞參數表格`
        * 用途說明
            * 若開啟的表單有接收參數的設定，必須在本表格填入參數內容
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
			* 表格列數最高顯示**5**列, 超過出現垂直捲軸
    * `(2)參數名`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單參數通則][link_ruledialog9], 從[開單內容][link_fieldbreak2]的`表單名稱`中, 進行表單參數挑選, 回傳: 表單參數名、參數型態
    * `(3)載入`
        * 用途說明
        * 規格說明
            * 從[開單內容][link_fieldbreak2]的`表單名稱`中, 載入該表單所有參數清單, 回傳: 表單參數名、參數型態
                * 當參數名不存在表格內: 新增資料列
                * 當參數名已存在表格內: 保留資料列
                * `(1)傳遞參數表格`內存在無效的參數名: 刪除資料列     
    * `(4)資料型態`
        * 用途說明
        * 規格說明
            * 依`(2)參數名`取得對應的型態顯示
    * `(5)給值類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 元件 / 固定值 / 參數 / 運算
    * `(6)給值內容`
        * 用途說明
        * 規格說明
            * 當`(4)給值類別`=表單元件: 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳: 表單元件
            * 當`(4)給值類別`=固定值: 由使用者自行輸入
            * 當`(4)給值類別`=參數: 參照 [挑選表單參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳: 表單參數
            * 當`(4)給值類別`=運算式: 參照 [操作運算式通則][link_ruledialog8], 限定: 不可查表, 回傳: 運算式說明
    * `(7)同名對應鍵`
        * 用途說明
        * 規格說明
            * 依`(2)參數名`比對元件名稱, 預設給同名元件
            * 無同名元件 或 `(6)給值內容`不為空值, `(5)給值類別`、`(6)給值內容`皆不異動
            * 有同名元件 且 `(6)給值內容`為空值, `(5)給值類別`給值表單元件、`(6)給值內容`給值同名元件

## <div id="save-action">儲存檢控</div>
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回不允空白檢控通則][link_ruleother7]
    * 當[基本][link_fieldbreak1]的`優先序`=空值
    * 當[開單內容][link_fieldbreak2]的`表單名稱`=空值
    * 當[開單內容][link_fieldbreak2]的`資料來源`=空值
    * 當[傳遞參教][link_fieldbreak3]的`傳遞參數表格`存在記錄時, 增加下列檢控
        * 當[傳遞參教][link_fieldbreak3]的`參數名`=空值
        * 當[傳遞參教][link_fieldbreak3]的`給值類別`=空值
        * 當[傳遞參教][link_fieldbreak3]的`給值類別`<>空值, 且`給值內容`=空值

* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
    * [基本][link_fieldbreak1]的`優先序`在同一按鍵下的各加註行為順序不允重複, 錯誤訊息內容: 同一按鍵的各加註內容順序不允重複

## <div id="other-desc">其它</div>
* [MAE加註儲存通則][link_ruleother5]

<!-- 圖片 -->
[image_badialog_STD]:attachment/BADialog_STD.png
[image_badialog_APP]:attachment/BADialog_APP.png
[image_badialog_block1]:attachment/BADialog_block1.png
[image_badialog_block2]:attachment/BADialog_block2.png
[image_badialog_block3]:attachment/BADialog_block3.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "基本"
[link_fieldbreak2]:#fieldbreak2 "開單內容"
[link_fieldbreak3]:#fieldbreak3 "傳遞參數"
[link_ruleother1]:{1}/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruledialog2]:{1}/RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruleother7]:{1}/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:{1}/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
[link_rulebutton2]:{1}/RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
[link_rulebutton3]:{1}/RulesButton/README#rulebutton3 "共用通則_按鍵/操作表格記錄通則"
[link_ruledialog1]:{1}/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog6]:{1}/RulesDialog/README#ruledialog6 "共用通則_開啟單據/挑選表單通則"
[link_ruledialog7]:{1}/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruledialog8]:{1}/RulesDialog/README#ruledialog8 "共用通則_開啟單據/操作運算式通則"
[link_ruledialog9]:{1}/RulesDialog/README#ruledialog9 "共用通則_開啟單據/挑選表單參數通則"
[link_ruledialog11]:{1}/RulesDialog/README#ruledialog11 "共用通則_開啟單據/設定按鍵執行條件表格通則"
[link_ruleother5]:../RulesOther/README#ruleother5 "共用通則_其它/MAE加註儲存通則"