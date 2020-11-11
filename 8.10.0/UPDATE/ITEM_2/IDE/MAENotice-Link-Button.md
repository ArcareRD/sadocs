### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/09

### <div id="trac">TRAC</div>
* #8213

## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_linkbutton]
    * RWD
        * 同STD
    * MAE</br>
        * 同STD

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 依 [按鍵加註-推播通知-主旨內文][link_MAENotice_fieldbreak3]`(13)連結內容`開啟, 顯示本單內容
* 若前單推播通知來源與原設定不同時
    * 須清除引用推播通知來源欄位
    * 覆蓋原設定推播通知來源料號

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_linkbutton_block1]
    * `(1)表單名稱`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單通則][link_ruledialog6], 依駐留專案 且 表單須存在[開放按鍵][link_ExternalCallButton]中, 進行表單挑選, 回傳並顯示: 表單名稱
    * `(2)按鍵名稱`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單按鍵通則][link_ruledialog13], 依`(1)表單名稱` 且 按鍵須存在[開放按鍵][link_ExternalCallButton]中, 回傳並顯示: 按鍵名稱
    * `(3)通行碼`
        * 用途說明
        * 規格說明
            * 單選選項: 相同 / 不相同 
            * 系統預設: 相同
    * `(4)有效次數`
        * 用途說明
        * 規格說明
            * 單選選項: 一次性 / 多次性 
            * 系統預設: 多次性 
            * 當設定為多次性時, `(5)執行系統`預設為要求登入, 並唯讀
    * `(5)執行系統`
        * 用途說明
        * 規格說明
            * 單選選項: 要求登入 / 自動登入
            * 帳號驗證: 預設為true
                * 當`(4)有效次數`為一次性 且 `(5)執行系統`為要求登入，則 **帳號驗證** 預設為true，並唯讀
    * `(6)執行後續_成功訊息`
        * 用途說明
        * 規格說明
            * 系統預設: 未勾選
            * 當為有勾選時, 參照 [使用多語詞庫通則][link_ruledialog2], 依駐留專案, 連行訊息內容挑選, 回傳並顯示: 多語名稱
    * `(7)執行後續_成功訊息_替代鍵`
        * 用途說明
        * 規格說明
            * 當`(6)執行後續_成功訊息`未設定時, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 請選擇"成功訊息"。 / 按鍵: 確定】
                * 確定: 關閉訊息盒 
            * 當`(6)執行後續_成功訊息`有設定時, 開啟[訊息替代][link_Replace] , 限定: 替代來源=表單
    * `(8)執行後續_失敗訊息`
        * 用途說明
        * 規格說明
            * 系統預設: 未勾選
            * 當為有勾選時, 參照 [使用多語詞庫通則][link_ruledialog2], 依駐留專案, 進行訊息內容挑選, 回傳並顯示: 多語名稱
    * `(9)執行後續_失敗訊息_替代鍵`
        * 用途說明
        * 規格說明
            * 當`(8)執行後續_失敗訊息`未設定時, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 請選擇"失敗訊息"。 / 按鍵: 確定】
                * 確定: 關閉訊息盒 
            * 當`(8)執行後續_失敗訊息`有設定時, 開啟[訊息替代][link_Replace], 限定: 替代來源=表單
    * `(10)傳遞參數表格`
        * 用途說明
        * 規格說明 
            * [操作表格記錄通則][link_rulesbutton3]
    * `(11)參數名稱`
        * 用途說明
        * 規格說明 
            * 參照 [挑選開放按鍵參數通則], 依`(2)按鍵名稱`中, 進行參數挑選, 回傳並顯示: 參數名稱
            * 可使用參數下載鍵, 依`(2)按鍵名稱`載入開放按鍵參數名稱, 回傳:參數料號
    * `(12)傳遞類型`
        * 用途說明
        * 規格說明
            * 下拉選項: 推播來源欄位 / 表單元件 / 表單參數 / 全域變數 
            * 系統預設: 表單元件
            * 當[推播通知-主旨內文]`(1)來源`=無時, 選項:郵件來源欄位 隱藏
            * 異動時清除欄位: `(13)傳遞內容`
    * `(13)傳遞內容`
        * 用途說明
        * 規格說明 
            * 當`(12)傳遞類型`=表單元件: [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體
            * 當`(12)傳遞類型`=推播來源欄位: [挑選檢視表元件通則][link_ruledialog8], 從 [推播通知-主旨內文][link_MAENotice_fieldbreak3]的`(2)檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(12)傳遞類型`=表單參數: [挑選表單參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳:表單參數
            * 當`(12)傳遞類型`=全域變數: [挑選全域變數通則][link_ruledialog10], 從駐留專案中, 進行全域變數挑選, 回傳:全域變數  
    * `(14)確定`
        * 用途說明
        * 規格說明
            * 瀏覽模式下, 隱藏
            * 將本次修改資料回傳前單後關閉本單
    * `(15)取消`
        * 用途說明
        * 規格說明
            * 瀏覽模式下, 隱藏
            * 不做任何修改, 直接關閉本單


## <div id="save-action">確定檢控</div>
* 以下檢控, 符合條件時, 顯示訊息盒, 並以紅框線標註錯誤的欄位
    * 訊息盒:【標題: 執行存回，發生下列錯誤 / 訊息內容: 以下資料未填寫正確 </n> *錯誤欄位名* / 按鍵: 確定】
        * 確定: 關閉訊息盒 
    * [基本][link_fieldbreak1]
        * `(1)表單名稱`、`(2)按鍵名稱`, 不允空白
        * 當 `(6)執行後續_成功訊息`有勾選時, 成功訊息內容不允為空
        * 當 `(8)執行後續_失敗訊息`有勾選時, 失敗訊息內容不允為空
        * 當`(10)傳遞參數表格`存在記錄時, `(11)參數名稱`、`(12)傳遞類型`, 不允空白
        * 當`(12)傳遞類型`有設定時, `(13)傳遞內容`, 不允空白


<!-- 圖片 -->
[image_linkbutton]:attachment/MAENotice-Link-Button.png
[image_linkbutton_block1]:attachment/MAENotice-Link-Button-Block1.png


<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本區塊"
[link_MAENotice_fieldbreak3]:MAENotice.md#fieldbreak3 "按鍵加註-推播通知/主旨內文"

[link_ExternalCallButton]:/8.10.0/IDE/Specification/ExternalCallButton/README "開放按鍵"
[link_Replace]:/8.10.0/IDE/Specification/Replace/README "訊息替代"

[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"

[link_rulesbutton3]:/8.10.0/IDE/Specification/RulesButton/README#rulebutton3 "共用通則_其它/操作表格記錄通則"

[link_ruledialog2]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruledialog6]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog6 "共用通則_開啟單據/挑選表單通則"
[link_ruledialog7]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruledialog8]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_ruledialog9]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog9 "共用通則_開啟單據/挑選表單參數通則"
[link_ruledialog10]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog10 "共用通則_開啟單據/挑選全域變數通則"
[link_ruledialog13]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog13 "共用通則_開啟單據/挑選表單按鍵通則"