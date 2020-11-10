### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/09

### <div id="trac">TRAC</div>
* 待開 

## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_savelink]
    * RWD
        * 同STD
    * MAE</br>
        * 同STD

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 依 [按鍵加註-推播通知-主旨內文][link_MAENotice_block3]`(14)儲存連結資訊`開啟, 顯示本單內容
* 若前單推播通知來源與原設定不同時
    * 須清除引用推播通知來源欄位
    * 覆蓋原設定推播通知來源料號

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_savelink_block1]
    * `(1)寫入資料表`
        * 用途說明
        * 規格說明
            * 參照 [挑選實表通則], 回傳:表格料號, 顯示: 表格名稱, 除能
    * `(2)通行碼`
        * 用途說明
        * 規格說明
            * 參照 [挑選實表元件通則], 過濾:存入資料表料號 且 資料型態=全唯碼
    * `(3)額外寫入欄位表格`
        * 用途說明
        * 規格說明
            * 參照 [操作一般表格通則]
    * `(4)項次`
        * 用途說明
        * 規格說明
            * 依資料列顯示 
    * `(5)其他目的欄位`
        * 用途說明
        * 規格說明    
            * 參照 [挑選實表元件通則], 過濾:存入資料表料號         
    * `(6)給值類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 推播來源欄位 / 表單元件 / 表單參數 / 全域變數 / 通知者使用序號 / 替換字變數         
            * 當[推播通知-主旨內文]`(1)來源`=無時, 選項:郵件來源欄位 隱藏
            * 異動時清除欄位: `(5)給值內容`
    * `(7)給值內容`
        * 用途說明
        * 規格說明
            * 當`(5)給值類別`=推播來源欄位: [挑選邏表元件通則][link_ruledialog6], 限定:推播來源檢視表料號, 回傳:檢視表元件料號. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(5)給值類別`=表單元件: [挑選表單元件通則][link_ruledialog7], 過濾:表單料號 回傳:表單元件料號. 若元件 (個資加密==true 且 個資解密=false ) 或 密碼處理=true, 則該元件顯示紅色字體
            * 當`(5)給值類別`=表單參數: [挑選表單參數通則][link_ruledialog8], 過濾:表單料號 回傳:表單參數料號
            * 當`(5)給值類別`=全域變數: [挑選全域變數通則][link_ruledialog9], 過濾:專案料號 回傳:全域變數料號
    * `(8)確定`
        * 用途說明
        * 規格說明
            * 瀏覽模式下, 隱藏
            * 將資料回傳前單暫存後關閉本單
    * `(9)取消`
        * 用途說明
        * 規格說明
            * 瀏覽模式下, 隱藏
            * 關閉表單
        

## <div id="save-action">確定檢控</div>
* 不允空白檢控, 符合條件時, 顯示訊息盒, 並以紅框線標註錯誤的欄位
    * 訊息盒:【標題: 執行存回，發生下列錯誤 / 訊息內容: 以下資料未填寫正確 </n> *錯誤欄位名* / 按鍵: 確定】
        * 確定: 關閉訊息盒 
    * [基本][link_fieldbreak1]
        * `(1)寫入資料表`、`(2)通行碼`, 不允空白
        * 當`(3)額外寫入欄位表格`存在記錄, `(5)其他目的欄位`、`(6)給值類別`, 不允空白
        * 當`(6)給值類別`為推播來源欄位/表單元件/表單參數/全域變數時, `(7)給值內容`不允空白

* 其它檢控    
    * `(5)其他目的欄位`, 不允重複, 顯示訊息盒【標題: 系統訊息 / 其他目的欄位, 不允重覆 / 按鍵: 確定】
        * 確定: 關閉訊息盒



<!-- 圖片 -->
[image_savelink]:attachment/MAENotice-SaveLinkInfo.png      
[image_savelink_block1]:attachment/MAENotice-SaveLinkInfo-Block1.png 


<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本區塊"
[link_MAENotice_block3]:MAENotice.md#fieldbreak3 "按鍵加註-推播通知/主旨內文"

[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"

[link_ruledialog6]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruledialog7]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_ruledialog8]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog9 "共用通則_開啟單據/挑選表單參數通則"
[link_ruledialog9]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog10 "共用通則_開啟單據/挑選全域變數通則"