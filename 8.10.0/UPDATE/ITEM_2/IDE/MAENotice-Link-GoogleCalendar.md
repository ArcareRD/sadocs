### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/09

### <div id="trac">TRAC</div>
* #8213

## <div id="savelink-layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_link]
    * RWD
        * 同STD
    * MAE</br>
        * 同STD

* [版面資訊通則][link_ruleother1]

## <div id="savelink-form-action">動作說明</div>
* 依 [按鍵加註-推播通知-主旨內文][link_MAENotice_fieldbreak3]`(13)連結內容`開啟, 顯示本單內容
* 若前單推播通知來源與原設定不同時
    * 須清除引用推播通知來源欄位
    * 覆蓋原設定推播通知來源料號

## <div id="savelink-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

* ![pic][image_link_block1]
    * `(1)標題_類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 推播來源欄位 / 表單元件 / 表單參數 / 全域變數 
            * 系統預設: 表單元件
            * 當 [推播通知-主旨內文][link_MAENotice_fieldbreak3]的`(1)來源`=無時, 選項:推播來源欄位 隱藏
            * 異動時清除欄位: `(2)標題_給值內容`
    * `(2)標題_給值內容`
        * 用途說明
        * 規格說明
            * 當`(1)標題_類別`=表單元件: [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體紅色字體
            * 當`(1)標題_類別`=推播來源欄位: [挑選檢視表元件通則][link_ruledialog8], 從 [推播通知-主旨內文][link_MAENotice_fieldbreak3]的`(2)檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(1)標題_類別`=表單參數: [挑選表單參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳:表單參數
            * 當`(1)標題_類別`=全域變數: [挑選全域變數通則][link_ruledialog10], 從駐留專案中, 進行全域變數挑選, 回傳:全域變數
    * `(3)內容_類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 推播來源欄位 / 表單元件 / 表單參數 / 全域變數 
            * 系統預設: 表單元件
            * 當 [推播通知-主旨內文][link_MAENotice_fieldbreak3]的`(1)來源`=無時, 選項: 推播來源欄位 隱藏
            * 異動時清除欄位: `(4)內容_給值內容`
    * `(4)內容_給值內容`
        * 用途說明
        * 規格說明
            * 當`(3)內容_類別`=表單元件: [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體紅色字體
            * 當`(3)內容_類別`=推播來源欄位: [挑選檢視表元件通則][link_ruledialog8], 從 [推播通知-主旨內文][link_MAENotice_fieldbreak3]的`(2)檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(3)內容_類別`=表單參數: [挑選表單參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳:表單參數
            * 當`(3)內容_類別`=全域變數: [挑選全域變數通則][link_ruledialog10], 從駐留專案中, 進行全域變數挑選, 回傳:全域變數
    * `(5)地點_類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 推播來源欄位 / 表單元件 / 表單參數 / 全域變數 
            * 系統預設: 表單元件
            * 當 [推播通知-主旨內文][link_MAENotice_fieldbreak3]`(1)來源`=無時, 選項: 推播來源欄位 隱藏
            * 異動時清除欄位: `(6)地點_給值內容`
    * `(6)地點_給值內容`
        * 用途說明
        * 規格說明
            * 當`(5)地點_類別`=表單元件: [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體紅色字體
            * 當`(5)地點_類別`=推播來源欄位: [挑選檢視表元件通則][link_ruledialog8], 從 [推播通知-主旨內文][link_MAENotice_fieldbreak3]的`(2)檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(5)地點_類別`=表單參數: [挑選表單參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳:表單參數
            * 當`(5)地點_類別`=全域變數: [挑選全域變數通則][link_ruledialog10], 從駐留專案中, 進行全域變數挑選, 回傳:全域變數
    * `(7)替換類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 推播來源欄位 / 表單元件 / 表單參數 / 全域變數 
            * 系統預設: 表單元件
            * 當 [推播通知-主旨內文][link_MAENotice_fieldbreak3]`(1)來源`=無時, 選項: 推播來源欄位 隱藏
    * `(8)日期含時間`
        * 用途說明
        * 規格說明
            * 系統預設: 未勾選
            * 當有勾選時, 欄位:`(13)時間起`、`(14)時間迄`隱藏
    * `(9)整天`
        * 用途說明
        * 規格說明
            * 系統預設: 未勾選
            * 當為有勾選時, 欄位:`(13)時間起`、`(14)時間迄`隱藏
    * `(10)格林威治時區`
        * 用途說明
        * 規格說明 
            * 系統預設: 未勾選
    * `(11)日期起`
        * 用途說明
        * 規格說明 
            * 當`(7)替換類別`=表單元件: [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體紅色字體
            * 當`(7)替換類別`=推播來源欄位: [挑選檢視表元件通則][link_ruledialog8], 從 [推播通知-主旨內文][link_MAENotice_fieldbreak3]的`(2)檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(7)替換類別`=表單參數: [挑選表單參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳:表單參數
            * 當`(7)替換類別`=全域變數: [挑選全域變數通則][link_ruledialog10], 從駐留專案中, 進行全域變數挑選, 回傳:全域變數
    * `(12)日期迄`
        * 用途說明
        * 規格說明
            * 當`(7)替換類別`=表單元件: [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體紅色字體
            * 當`(7)替換類別`=推播來源欄位: [挑選檢視表元件通則][link_ruledialog8], 從 [推播通知-主旨內文][link_MAENotice_fieldbreak3]的`(2)檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(7)替換類別`=表單參數: [挑選表單參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳:表單參數
            * 當`(7)替換類別`=全域變數: [挑選全域變數通則][link_ruledialog10], 從駐留專案中, 進行全域變數挑選, 回傳:全域變數
    * `(13)時間起`
        * 用途說明
        * 規格說明
            * 當`(7)替換類別`=表單元件: [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體紅色字體
            * 當`(7)替換類別`=推播來源欄位: [挑選檢視表元件通則][link_ruledialog8], 從 [推播通知-主旨內文][link_MAENotice_fieldbreak3]的`(2)檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(7)替換類別`=表單參數: [挑選表單參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳:表單參數
            * 當`(7)替換類別`=全域變數: [挑選全域變數通則][link_ruledialog10], 從駐留專案中, 進行全域變數挑選, 回傳:全域變數
    * `(14)時間迄`
        * 用途說明
        * 規格說明
            * 當`(7)替換類別`=表單元件: [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體紅色字體
            * 當`(7)替換類別`=推播來源欄位: [挑選檢視表元件通則][link_ruledialog8], 從 [推播通知-主旨內文][link_MAENotice_fieldbreak3]的`(2)檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(7)替換類別`=表單參數: [挑選表單參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳:表單參數
            * 當`(7)替換類別`=全域變數: [挑選全域變數通則][link_ruledialog10], 從駐留專案中, 進行全域變數挑選, 回傳:全域變數
    * `(15)確定`
        * 用途說明
        * 規格說明
            * 瀏覽模式下, 隱藏
            * 將本次修改資料回傳前單後關閉本單
    * `(16)取消`
        * 用途說明
        * 規格說明
            * 瀏覽模式下, 隱藏
            * 不做任何修改, 直接關閉本單


## <div id="save-action">確定檢控</div>
* 以下檢控, 符合條件時, 顯示訊息盒, 並以紅框線標註錯誤的欄位
    * 訊息盒:【標題: 執行存回，發生下列錯誤 / 訊息內容: 以下資料未填寫正確 </n> *錯誤欄位名* / 按鍵: 確定】
        * 確定: 關閉訊息盒 
    * [基本][link_fieldbreak1]
        * `(1)標題_類別`、`(3)內容_類別`、`(5)地點_類別`、`(11)日期起`、`(12)日期迄`, 不允空白
        * 當`(1)標題_類別`有設定時, `(2)標題_給值內容`, 不允空白
        * 當`(3)內容_類別`有設定時, `(4)內容_給值內容`, 不允空白
        * 當`(5)地點_類別`有設定時, `(6)地點_給值內容`, 不允空白
        * 當`(8)日期含時間`或`(9)整天`為true時, `(13)時間起`、`(14)時間迄`, 不允空白


<!-- 圖片 -->
[image_link]:attachment/MAENotice-Link-GoogleCalendar.png
[image_link_block1]:attachment/MAENotice-Link-GoogleCalendar-Block1.png      


<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本區塊"
[link_MAENotice_fieldbreak3]:MAENotice.md#fieldbreak3 "按鍵加註-推播通知/主旨內文"

[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruledialog7]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruledialog8]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_ruledialog9]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog9 "共用通則_開啟單據/挑選表單參數通則"
[link_ruledialog10]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog10 "共用通則_開啟單據/挑選全域變數通則"