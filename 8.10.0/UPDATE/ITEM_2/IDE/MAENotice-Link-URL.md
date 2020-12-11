### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/12

### <div id="trac">TRAC</div>
* 待開 

## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_linkurl]
    * RWD
        * 同STD
    * MAE</br>
        * 同STD

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>


## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

* ![pic][image_linkurl_block1]
    * `(1)網址欄位_類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 推播來源欄位 / 表單元件 / 表單參數 / 全域變數 
            * 系統預設: 表單元件
            * 異動時清除欄位: `(2)標題_給值內容`
    * `(2)網址欄位_給值內容`
        * 用途說明
        * 規格說明
            * 當`(1)網址欄位_類別`=表單元件: [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體紅色字體
            * 當`(1)網址欄位_類別`=推播來源欄位: [挑選檢視表元件通則][link_ruledialog8], 從 [推播通知_推播內容][link_conentviewno] 的`檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(1)網址欄位_類別`=表單參數: [挑選表單參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳:表單參數
            * 當`(1)網址欄位_類別`=全域變數: [挑選全域變數通則][link_ruledialog10], 從駐留專案中, 進行全域變數挑選, 回傳:全域變數
    * `(3)網址參數`
        * 用途說明
        * 規格說明
            * 開啟 [運算式][link_Expression], 限定: 不可查表

## <div id="save-action">確定檢控</div>
* 不允空白檢控, 符合條件時, 顯示訊息盒, 並以紅框線標註錯誤的欄位
    * 訊息盒:【標題: 執行存回，發生下列錯誤 / 訊息內容: 以下資料未填寫正確 </n> *錯誤欄位名* / 按鍵: 確定】
        * 確定: 關閉訊息盒
    * [基本][link_fieldbreak1]
        * `(2)網址欄位_給值內容`, 不允空白


<!-- 圖片 -->
[image_linkurl]:attachment/MAENotice-Link-URL.png
[image_linkurl_block1]:attachment/MAENotice-Link-URL-Block1.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本區塊"
[link_MAENotice_fieldbreak3]:BAMAENotice.md#fieldbreak3 "按鍵加註-推播通知/推播內容"
[link_conentviewno]:BAMAENotice.md#conentviewno "按鍵加註-推播通知/推播內容/檢視表"
[link_Expression]:Expression.md "運算式"

[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"

[link_ruledialog7]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruledialog8]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_ruledialog9]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog9 "共用通則_開啟單據/挑選表單參數通則"
[link_ruledialog10]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog10 "共用通則_開啟單據/挑選全域變數通則"