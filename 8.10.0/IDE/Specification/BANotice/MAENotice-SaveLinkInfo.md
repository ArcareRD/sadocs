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
* 依 [按鍵加註-推播通知-推播內容][link_MAENotice_fieldbreak3]`(14)儲存連結資訊`開啟, 顯示本單內容
* 若前單推播通知來源與原設定不同時
    * 須清除引用推播通知來源欄位
    * 覆蓋原設定推播通知來源料號
* 下列欄位, 除規格說明中有額外說明, 否則所有欄位須判斷: 若前單為瀏覽狀態: 除能 ; 編輯狀態: 致能

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_savelink_block1]
    * `(1)寫入資料表`
        * 用途說明
        * 規格說明
            * 參照 [挑選資料表通則][link_ruledialog3], 從駐留專案中, 進行資料表挑選,  回傳並顯示: 表格名稱
    * `(2)通行碼`
        * 用途說明
        * 規格說明
            * 參照 [挑選資料表元件通則][link_ruledialog5], 限定使用`(1)寫入資料表` 且 欄位資料型態須為全唯碼
    * `(3)額外寫入欄位表格`
        * 用途說明
            * 若有額外需要寫入的資訊，可透過此表格進行設定。
        * 規格說明
            * 參照 [操作一般表格通則][link_rulebutton3]
    * `(5)其他目的欄位`
        * 用途說明
        * 規格說明
            * 參照 [挑選資料表元件通則][link_ruledialog5], 限定使用`(1)寫入資料表`
    * `(6)給值類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 推播來源欄位 / 表單元件 / 表單參數 / 全域變數 / 通知者帳號
            * 異動時清除欄位: `(7)給值內容`
    * `(7)給值內容`
        * 用途說明
        * 規格說明
            * 當`(6)給值類別`=表單元件: [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體紅色字體
            * 當`(6)給值類別`=推播來源欄位: [挑選檢視表元件通則][link_ruledialog8], 從 [推播通知_推播內容][link_conentviewno] 的`檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(6)給值類別`=表單參數: [挑選表單參數通則][link_ruledialog8], 從駐留表單中, 進行表單參數挑選, 回傳:表單參數
            * 當`(6)給值類別`=全域變數: [挑選全域變數通則][link_ruledialog9], 從駐留專案中, 進行全域變數挑選, 回傳:全域變數
            * 當`(6)給值類別`=通知者帳號: 設計者無須輸入內容, 運行時由系統依據 [推播通知_推播人][link_MAENotice_fieldbreak1] 設定的選項內容寫入
    * `(8)確定`
        * 用途說明
        * 規格說明
            * 若前單為瀏覽狀態: 隱藏 ; 編輯狀態: 顯示
            * 將本次修改資料回傳前單後關閉本單
    * `(9)取消`
        * 用途說明
        * 規格說明
            * 若前單為瀏覽狀態: 隱藏 ; 編輯狀態: 顯示
            * 顯示訊息盒【標題: 系統訊息 / 訊息內容: 資料尚未儲存, 是否確定取消? / 按鍵: 確定、取消】
                * 確定: 關閉訊息盒後, 直接關閉本單
                * 取消: 關閉訊息盒, 回到本單畫面

## <div id="save-action">確定檢控</div>
* 不允空白檢控, 符合條件時, 顯示訊息盒, 並以紅框線標註錯誤的欄位
    * 訊息盒:【標題: 執行存回，發生下列錯誤 / 訊息內容: 以下資料未填寫正確 </n> *錯誤欄位名* / 按鍵: 確定】
        * 確定: 關閉訊息盒 
    * [基本][link_fieldbreak1]
        * `寫入資料表`、`通行碼`, 不允空白
        * 當`額外寫入欄位表格`存在記錄, `其他目的欄位`、`給值類別`, 不允空白
        * 當`給值類別`為推播來源欄位/表單元件/表單參數/全域變數時, `給值內容`不允空白

* 其它檢控    
    * `(5)其他目的欄位`, 不允重複, 顯示訊息盒【標題: 系統訊息 / 其他目的欄位, 不允重覆 / 按鍵: 確定】
        * 確定: 關閉訊息盒



<!-- 圖片 -->
[image_savelink]:attachment/MAENotice-SaveLinkInfo.png      
[image_savelink_block1]:attachment/MAENotice-SaveLinkInfo-Block1.png 


<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本區塊"
[link_MAENotice_fieldbreak1]:README.md#fieldbreak1 "按鍵加註-推播通知/推播人"
[link_MAENotice_fieldbreak3]:README.md#fieldbreak3 "按鍵加註-推播通知/推播內容"
[link_conentviewno]:README.md#conentviewno "按鍵加註-推播通知/推播內容/檢視表"

[link_ruleother1]:{1}/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_rulebutton3]:{1}/RulesButton/README#rulebutton3 "共用通則_按鍵/操作表格記錄通則"

[link_ruledialog7]:{1}/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruledialog8]:{1}/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_ruledialog9]:{1}/RulesDialog/README#ruledialog9 "共用通則_開啟單據/挑選表單參數通則"
[link_ruledialog10]:{1}/RulesDialog/README#ruledialog10 "共用通則_開啟單據/挑選全域變數通則"
[link_ruledialog3]:{1}/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_ruledialog5]:{1}/RulesDialog/README#ruledialog5 "共用通則_開啟單據/挑選資料表元件通則"