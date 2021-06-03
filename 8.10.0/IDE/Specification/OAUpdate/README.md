## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_oaudate_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_oaudate_APP]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 依規格定義-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格定義-主畫面 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能


## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_oaudate_block1]
    * `(1)按鈕名稱`
        * 用途說明
        * 規格說明
            * 參照 [使用多語詞庫通則][link_ruledialog2], 回傳:按鍵多語內容並顯示
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示前單傳入的按鍵料號
    * `(3)執行條件`
        * 用途說明
        * 規格說明
            * 參照 [操作條件式通則][link_ruledialog1], 回傳並顯示: 條件說明
    * `(4)自行輸入才有效`
        * 用途說明
        * 規格說明
            * 當表單設計類型=APP, 則 顯示, 否則 隱藏
            * 系統預設: 不勾選


* <p id="fieldbreak5" style="color:blue;font-weight:bold">呼叫按鈕功能</p>

    * ![pic][image_oaudate_block5]
    * `(1)呼叫按鈕功能`
        * 用途說明
        * 規格說明
            * 當表單設計類型=APP, 則 顯示, 否則 隱藏
            * 系統預設: 不勾選
    * `(2)按鈕功能名`
        * 用途說明
        * 規格說明
            * 當`(1)呼叫按鈕功能`為勾選時, 則 致能, 否則 除能
            * 參照 [挑選表單按鍵通則][link_ruledialog13], 過濾: 駐留筆表單, 且表單按鈕類型須存在【wTBBtn.功能按鈕、wHBtn.隱藏按鍵、funckey.功能按鍵(多筆表格)、liteFunckey.功能按鍵(多筆瀏覽)、wMBASave.新增存回(選單列)、wMBESave.修改存回(選單列)、wMBExport.匯出(選單列)、wMBImport.匯入(選單列)、wMBPrint.列印(選單列)】
    * `(3)呼叫時機`
        * 用途說明
        * 規格說明
            * 當`(1)呼叫按鈕功能`為勾選時, 則 致能, 否則 除能
            * 下拉選項: 內容異動 / 資料行移動 / 滑鼠雙擊 / 滑鼠單擊 / 滑鼠離開 / 自動完成
            * 依駐留筆元件類型決定顯示選項, 如下:
                * 當`元件類型`存在【checkbox.核取方塊(多筆表格)】, 僅顯示選項: 內容異動 / 滑鼠單擊 / 滑鼠離開
                * 當`元件類型`存在【wGrd.多筆表格、wGrdLite.多筆瀏覽】, 僅顯示選項: 資料行移動 / 滑鼠雙擊
                * 當`元件類型`存在【wTree.樹狀清單】, 僅顯示選項: 內容異動 / 資料行移動 / 滑鼠離開
                * 當`元件類型`存在【wTF.文字方塊】, 僅顯示選項: 內容異動 / 滑鼠離開 / 自動完成
                * 其餘元件類型, 顯示選項: 內容異動 / 滑鼠離開



## <div id="save-action">儲存檢控</div>
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回不允空白檢控通則][link_ruleother7]
    * 當[呼叫按鈕功能][link_fieldbreak5]的`呼叫按鈕功能`勾選時,
        * `按鈕功能名`=空值
        * `呼叫時機`=空值
	
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]

<!-- 圖片 -->
[image_oaudate_STD]:attachment/OAUpdate_STD.png
[image_oaudate_APP]:attachment/OAUpdate_APP.png
[image_oaudate_block1]:attachment/OAUpdate_block1.png
[image_oaudate_block5]:attachment/OAUpdate_block5.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_fieldbreak5]:#fieldbreak5 "欄位說明/呼叫按鈕功能"
[link_ruleother1]:{1}/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:{1}/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:{1}/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"

[link_rulebutton2]:{1}/RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"

[link_ruledialog1]:{1}/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog13]:{1}/RulesDialog/README#ruledialog13 "共用通則_開啟單據/挑選表單按鍵通則"