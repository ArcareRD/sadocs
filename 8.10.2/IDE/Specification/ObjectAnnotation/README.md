## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_object_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_object_MAE]
* [版面資訊通則][link_ruleother1]
		
## <div id="form-action">動作說明</div>
* 依規格關聯-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格關聯-主畫面 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本區塊</p>

    ![pic][image_fieldbreak1]
    * `(1)表單元件`
        * 用途說明
        * 規格說明
            * [使用多語詞庫通則][link_ruledialog2], 回傳:多語料號, 顯示:多語詞彙
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示元件料號
    * `(3)元件類型`
        * 用途說明
        * 規格說明
            * 顯示本元件的元件類型
    * `(4)存在檔區`
        * 用途說明
        * 規格說明
            * [挑選表單檔區通則][link_ruleother4], 限定: 本單的檔區
            * 變更檔區後, 清空`(9)檢視表對應欄位`、`(10)資料型態`、`(11)資料長度`
    * `(5)資料模版`
        * 用途說明
        * 規格說明
            * 下拉選項內容, 至[資料模版][link_Commodule]中, 查詢取得
            * 當 表單設計類型=APP, 則限定: `模版組成`不為編輯器
    * `(6)資料長度`
        * 用途說明
        * 規格說明
            * 自行輸入數字0~999
    * `(7)幣別元件`
        * 用途說明
        * 規格說明
            * 當`(5)資料模版`的`模版組成`為貨幣, 則致能, 否則除能
            * 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳: 表單元件
            * [個資加密提示通則][link_ruleother11]
    * `(8)清空幣別元件`
        * 用途說明
        * 規格說明
            * 清空`(7)幣別元件`
    * `(9)檢視表對應欄位`
        * 用途說明
        * 規格說明
            * 參照 [挑選檢視表元件通則][link_ruledialog8], 限定: `(4)存在檔區`所指定的`檢視表`, 進行檢視表元件挑選, 回傳:檢視表元件 並將`資料型態`、`長度`帶入`(10)資料型態`、`(11)欄位資料長度`
            * [個資加密提示通則][link_ruleother11]
    * `(10)資料型態`
        * 用途說明
        * 規格說明
            * 由`(9)檢視表對應欄位`帶入顯示 位元/文字/整數(bigint)/整數(int)/整數(smallint)/整數(tinyint)/數字/日期/日期時間/備註/二進位/全唯碼
    * `(11)欄位資料長度`
        * 用途說明
        * 規格說明
            * 由`(9)檢視表對應欄位`帶入顯示 
    * `(12)選項群組`
        * 用途說明
        * 規格說明
            * 僅顯示, 當`(3)元件類型`=wRB.按鈕選項, 則顯示對應父階元件名稱
    * `(13)選項給值`
        * 用途說明
        * 規格說明
            * 當`(3)元件類型`=wRB.按鈕選項, 則致能, 否則除能
            * 自行輸入數字1~99
    * `(14)引用功能`
        * 用途說明
        * 規格說明
            * 以下條件致能, 否則除能
                * 當`(3)元件類型`為 wTBtn.連結框線、wTP.文字標題、wImg.圖片
                * 當`(3)元件類型`為 wTF.文字方塊、text.文字方塊(多筆表格)、liteText.文字方塊(多筆瀏覽) 且 [操作規則][link_fieldbreak2]`僅供顯示`為勾選 且 `(16)撥號功能`不為勾選
            * 參照 [挑選表單按鍵通則][link_ruledialog13], 限定: 駐留筆表單, 進行表單按鍵挑選, 回傳: 按鍵名稱
    * `(15)清空引用功能`
        * 用途說明
        * 規格說明
            * 清空`(14)引用功能`
    * `(16)撥號功能`
        * 用途說明
        * 規格說明
            * 預設未勾選
            * 當 表單設計類型=STD, 則除能
            * 當`(3)元件類型`為 wTF.文字方塊、liteText.文字方塊(多筆瀏覽), 則致能
    * `(17)關閉執行中的提示訊息`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則隱藏
    * `(18)欄位提示訊息`
        * 用途說明
        * 規格說明
            * [使用多語詞庫通則][link_ruledialog2], 回傳:多語料號, 顯示:多語詞彙
            * 當 表單設計類型=APP, 則隱藏
    * `(19)補充說明`
        * 用途說明
        * 規格說明
            * 自行輸入

* <p id="fieldbreak2" style="color:blue;font-weight:bold">操作規則</p>

    ![pic][image_fieldbreak2]
    * `(1)僅供顯示`
        * 用途說明
        * 規格說明
            * 預設未勾選
            * 以下條件, 預設為勾選 並 除能
                * 當 表單種類 不為 指定條件執行(單改) 且 `檢視表對應欄位` 為 密碼處理
                * `元件類型`為 liteText.文字方塊(多覽欄位資料)、liteFunckey.功能按鍵(多覽欄位資料)、liteTextarea.多行文字(多覽欄位資料)、liteImage.圖片(多覽欄位資料)
                * 為 wCtnr.元件容器 下的子元件
    * `(2)全文顯示`
        * 用途說明
        * 規格說明
            * 預設未勾選
            * 當 `元件類型`=wTA.多行文字 且 `(1)僅供顯示`為勾選 時, 致能
            * 當 `元件類型`為 liteText.文字方塊(多覽欄位資料)、liteCheckbox.核取方塊(多覽欄位資料)、liteFunckey.功能按鍵(多覽欄位資料)、liteTextarea.多行文字(多覽欄位資料)、liteImage.圖片(多覽欄位資料), 除能
            * 當 表單設計類型=APP, 則隱藏
    * `(3)游標可駐留`
        * 用途說明
        * 規格說明
            * 預設未勾選
            * `(1)僅供顯示`勾選時, 則致能, 且本欄位預設勾選
            * 當 表單設計類型=APP, 則隱藏
    * `(4)可駐留之狀態`
        * 用途說明
        * 規格說明
            * 選項 新增/修改/瀏覽
            * `(3)游標可駐留`勾選時, 則致能, 且 瀏覽預設勾選, 否則除能
            * 當 表單設計類型=APP, 則隱藏
    * `(5)資料複製致能`
        * 用途說明
        * 規格說明
            * 預設未勾選
            * 當`元件類型`為 liteText.文字方塊(多覽欄位資料)、liteCheckbox.核取方塊(多覽欄位資料)、liteFunckey.功能按鍵(多覽欄位資料)、liteTextarea.多行文字(多覽欄位資料)、liteImage.圖片(多覽欄位資料), 則除能
            * 當 表單設計類型=APP, 則隱藏
    * `(6)資料複製致能項目`
        * 用途說明
        * 規格說明
            * 選項 至檔尾/至頁尾/至遇到相同值/到固定筆數
            * `(5)資料複製致能`勾選時, 則致能, 否則除能
            * 當`元件類型`為 liteText.文字方塊(多覽欄位資料)、liteCheckbox.核取方塊(多覽欄位資料)、liteFunckey.功能按鍵(多覽欄位資料)、liteTextarea.多行文字(多覽欄位資料)、liteImage.圖片(多覽欄位資料), 則除能
            * 當 表單設計類型=APP, 則隱藏
    * `(7)固定筆數`
        * 用途說明
        * 規格說明
            * `(6)資料複製致能項目`=到固定筆數, 則致能, 否則除能
            * 當`元件類型`為 liteText.文字方塊(多覽欄位資料)、liteCheckbox.核取方塊(多覽欄位資料)、liteFunckey.功能按鍵(多覽欄位資料)、liteTextarea.多行文字(多覽欄位資料)、liteImage.圖片(多覽欄位資料), 則除能
            * 自行輸入1~99
            * 當 表單設計類型=APP, 則隱藏
    * `(8)不可重複`
        * 用途說明
        * 規格說明
            * 預設未勾選
            * 當`元件類型`為 liteText.文字方塊(多覽欄位資料)、liteCheckbox.核取方塊(多覽欄位資料)、liteFunckey.功能按鍵(多覽欄位資料)、liteTextarea.多行文字(多覽欄位資料)、liteImage.圖片(多覽欄位資料), 則除能
            * 當 表單設計類型=APP, 則隱藏
    * `(9)不可負數`
        * 用途說明
        * 規格說明
            * 預設未勾選
            * 當`元件類型`為 liteText.文字方塊(多覽欄位資料)、liteCheckbox.核取方塊(多覽欄位資料)、liteFunckey.功能按鍵(多覽欄位資料)、liteTextarea.多行文字(多覽欄位資料)、liteImage.圖片(多覽欄位資料), 則除能
    * `(10)密碼顯示`
        * 用途說明
        * 規格說明
            * 當 `檢視表對應欄位` 為 密碼處理, 預設為勾選 且 除能, 其餘預設為未勾選
    * `(11)內容`
        * 用途說明
        * 規格說明
            * 選項 必要項/選擇項
            * 當`元件類型`為 liteText.文字方塊(多覽欄位資料)、liteCheckbox.核取方塊(多覽欄位資料)、liteFunckey.功能按鍵(多覽欄位資料)、liteTextarea.多行文字(多覽欄位資料)、liteImage.圖片(多覽欄位資料), 則除能            
    * `(12)選擇項檢錯`
        * 用途說明
        * 規格說明
            * 選項 空值不檢錯/空值要檢錯
            * 當 `(11)內容`=選擇項, 則致能, 預設 空值不檢錯, 否則除能
            * 當`元件類型`為 liteText.文字方塊(多覽欄位資料)、liteCheckbox.核取方塊(多覽欄位資料)、liteFunckey.功能按鍵(多覽欄位資料)、liteTextarea.多行文字(多覽欄位資料)、liteImage.圖片(多覽欄位資料), 則除能   
    * `(13)駐留原欄位`
        * 用途說明
        * 規格說明
            * 預設未勾選
            * 當`元件類型`為 liteText.文字方塊(多覽欄位資料)、liteCheckbox.核取方塊(多覽欄位資料)、liteFunckey.功能按鍵(多覽欄位資料)、liteTextarea.多行文字(多覽欄位資料)、liteImage.圖片(多覽欄位資料), 則除能
            * 當 表單設計類型=APP, 則隱藏
    * `(14)清空原值`
        * 用途說明
        * 規格說明
            * 預設未勾選
            * 當`元件類型`為 liteText.文字方塊(多覽欄位資料)、liteCheckbox.核取方塊(多覽欄位資料)、liteFunckey.功能按鍵(多覽欄位資料)、liteTextarea.多行文字(多覽欄位資料)、liteImage.圖片(多覽欄位資料), 則除能
            * `(13)駐留原欄位`勾選時, 則致能, 否則除能
            * 當 表單設計類型=APP, 則隱藏

* <p id="fieldbreak3" style="color:blue;font-weight:bold">顯示規則</p>

    ![pic][image_fieldbreak3]
    * `(1)顯示規則`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則隱藏
    * `(2)重顯週期`
        * 用途說明
        * 規格說明
            * 預設未勾選
    * `(3)時間分`
        * 用途說明
        * 規格說明
            * 當 `(2)重顯週期`勾選時, 則致能, 否則除能
            * 下拉選項 00~60
    * `(4)時間秒`
        * 用途說明
        * 規格說明
            * 當 `(2)重顯週期`勾選時, 則致能, 否則除能
            * 下拉選項 00~59

* <p id="fieldbreak4" style="color:blue;font-weight:bold">複選框</p>

    ![pic][image_fieldbreak4]
    * `(1)複選框`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則隱藏
    * `(2)資料行勾選`
        * 用途說明
        * 規格說明
            * 預設未勾選
            * 當`元件類型`為 checkbox.核取方塊(欄位資料)時, 則致能, 否則除能
    * `(3)資料行勾選項目`
        * 用途說明
        * 規格說明
            * `(2)資料行勾選`勾選時, 則致能, 否則除能
            * 選項 傳回呼叫表單/傳給按鈕, 預設 傳回呼叫表單
    * `(4)傳給按鈕表格`
        * 用途說明
        * 規格說明
            * [操作表格記錄通則][link_rulebutton3]
            * `(3)資料行勾選項目`=傳給按鈕, 則致能, 否則除能
            * 最多可以新增**5**筆, 若超過筆數, 顯示訊息盒【標題: 系統訊息 / 不得超出5個 / 按鍵:確定】
                * 確定: 關閉訊息盒
			* 表格列數最高顯示**2**列, 超過出現垂直捲軸            
    * `(5)順序`
        * 用途說明
        * 規格說明
            * 依序給流水號
    * `(4)挑選欄位`
        * 用途說明
        * 規格說明
            * 參照 [挑選檢視表元件通則][link_ruledialog8], 限定: `(4)存在檔區`所指定的`檢視表`, 進行檢視表元件挑選, 回傳:檢視表元件
            * [個資加密提示通則][link_ruleother11]

## <div id="save-action">儲存檢控</div>
* 不允空白檢控, 規則參照 [存回不允空白檢控通則][link_ruleother7]
    * [基本][link_fieldbreak1]
        * 當 `元件類型`不為 wRB.按鈕選項、wCB.核取方塊、wImg.圖片、wObj.嵌入物件、wHObj.隱藏元件、wTBtn.連結框線、 wTP.文字標題、wGrd.多筆表格、wTab.頁籤區塊、wFrame.框線、checkbox.核取方塊(欄位資料)、wRBGroup.按鈕群組、wGrdLite.多筆殼(瀏覽)、liteCheckbox.核取方塊(多覽欄位資料), `資料模版`、`資料長度` 不允空白, 否則清空
        * 當 `元件類型`不為 wTBtn.連結框線、wTP.文字標題、wGrd.多筆表格、wTab.頁籤區塊、wFrame.框線、wObj.嵌入物件、wRBGroup.按鈕群組、wGrdLite.多筆殼(瀏覽), `(9)檢視表對應欄位` 不允空白; 否則清空
    * [操作規則][link_fieldbreak2]
        * 當 `內容`=選擇項時, `選擇項檢錯` 不允空白
    * [顯示規則][link_fieldbreak3]
        * 當 `重顯週期`為勾選時, `時間分`、`時間秒` 不允空白
    * [複選框][link_fieldbreak4]
        * 當 `資料行勾選`為勾選時, `資料行勾選項目` 不允空白
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
    * [基本][link_fieldbreak1]
        * 當 `元件類型`不為 wRB.按鈕選項、wCB.核取方塊、wImg.圖片、wObj.嵌入物件、wHObj.隱藏元件、wTBtn.連結框線、 wTP.文字標題、wGrd.多筆表格、wTab.頁籤區塊、wFrame.框線、checkbox.核取方塊(欄位資料)、wRBGroup.按鈕群組、wGrdLite.多筆殼(瀏覽)、liteCheckbox.核取方塊(多覽欄位資料), `資料長度` 內容值必須介於0~999之間
        * 當 `元件類型`為 wRB.按鈕選項, `選項給值` 內容值必須介於1~99之間
        * 當 `檢視表對應欄位` 所對應的`欄位型態`若為 整數(int)/整數(smallint)/整數(tinyint)/整數(bigint)/數字(numeric)時, 則`資料模版`的模版組成只能是數字或貨幣
        * 當 `元件類型`=wCanvas.畫布, 則`檢視表對應欄位` 所對應的`欄位型態`, 只允為二進位
    * [操作規則][link_fieldbreak2]
        * 當 `資料複製致能項目`=到固定筆數, 則`固定筆數` 內容值必須介於1~99之間
    * [複選框][link_fieldbreak4]
        * 當 `資料行勾選項目`=傳給按鈕, 則`傳給按鈕表格` 至少要有一筆記錄

## <div id="other-desc">其它</div>
* [MAE加註儲存通則][link_ruleother5]

<!-- 圖片 -->
[image_object_STD]:attachment/ObjectAnnotation_STD.png
[image_object_MAE]:attachment/ObjectAnnotation_MAE.png
[image_fieldbreak1]:attachment/ObjectAnnotation_fieldbreak1.png
[image_fieldbreak2]:attachment/ObjectAnnotation_fieldbreak2.png
[image_fieldbreak3]:attachment/ObjectAnnotation_fieldbreak3.png
[image_fieldbreak4]:attachment/ObjectAnnotation_fieldbreak4.png

<!-- 超連結 -->
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_rulebutton2]:../RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
[link_ruleother5]:../RulesOther/README#ruleother5 "共用通則_其它/MAE加註儲存通則"
[link_ruledialog2]:../RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruleother4]:../RulesOther/README#ruleother4 "共用通則_其它/挑選表單檔區通則"
[link_Commodule]:../Commodule/README "資料模版"
[link_ruledialog7]:../RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruledialog8]:../RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_ruleother11]:../RulesOther/README#ruleother11 "共用通則_其它/個資加密提示通則"
[link_ruledialog13]:../RulesDialog/README#ruledialog13 "共用通則_開啟單據/挑選表單按鍵通則"
[link_rulebutton3]:../RulesButton/README#rulebutton3 "共用通則_按鍵操作/操作表格記錄通則"
[link_ruleother7]:../RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:../RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_fieldbreak2]:#fieldbreak2 "欄位說明/操作規則"
[link_fieldbreak3]:#fieldbreak3 "欄位說明/顯示規則"
[link_fieldbreak4]:#fieldbreak4 "欄位說明/複選框"