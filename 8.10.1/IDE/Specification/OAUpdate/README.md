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
            * 當表單設計類型=APP 且 元件類型存在【wTF.文字方塊、wTA.多行文字、wRB.按鈕選項、wCB.核取方塊、wDL.下拉選項、wLB.清單選項、wCanvas.畫布、wHObj.隱藏元件、wCtnr.元件容器】, 則 顯示, 否則 隱藏
            * 當表單設計類型=RWD 且 元件類型存在【wTF.文字方塊、text.文字方塊(多筆表格)、wTA.多行文字、textarea.多行文字(多筆表格)、wRB.按鈕選項、wCB.核取方塊、checkbox.核取方塊(多筆表格)、liteCheckbox.核取方塊(多筆瀏覽)、wDL.下拉選項、select.下拉選項(多筆表格)、wPW.彈出視窗、popupwindow.彈出視窗(多筆表格)、wLB.清單選項、wCanvas.畫布、wGrd.多筆表格、wGrdLite.多筆瀏覽、wTree.樹狀清單、wCtnr.元件容器、wHObj.隱藏元件】, 則 致能, 否則 除能
            * 系統預設: 不勾選
    * `(2)按鈕功能名`
        * 用途說明
        * 規格說明
            * 當`(1)呼叫按鈕功能`為勾選時, 則 致能, 否則 除能
            * 參照 [挑選表單按鍵通則][link_ruledialog13], 過濾: 駐留筆表單, 且表單按鈕類型須存在【wTBBtn.功能按鈕、wHBtn.隱藏按鍵、funckey.功能按鍵(多筆表格)、liteFunckey.功能按鍵(多筆瀏覽)、wMBASave.新增存回(選單列)、wMBESave.修改存回(選單列)、wMBExport.匯出(選單列)、wMBImport.匯入(選單列)、wMBPrint.列印(選單列)】
    * `(3)呼叫時機`
        * 用途說明
            * 內容異動: 表示元件對應的檔區欄位內容值異動時成立(非紀錄移動)
            * 資料行移動: 表示移動駐留筆資料時成立
            * 滑鼠雙擊: 表示滑鼠左鍵雙擊資料列時成立
            * 滑鼠單擊: 表示滑鼠單擊元件時成立
            * 滑鼠離開: 表示元件在編輯狀態下異動內容值後跳離且通過檢控限制時成立
            * 自動完成: 表示元件在編輯狀態下輸入內容值，輸入的間隔時間若超過系統參數中的停滯時間設定時成立
        * 規格說明
            * 當`(1)呼叫按鈕功能`為勾選時, 則 致能, 否則 除能
            * 下拉選項: 內容異動 / 資料行移動 / 滑鼠雙擊 / 滑鼠單擊 / 滑鼠離開 / 自動完成
            * 依表單設計類型+駐留的元件類型決定要顯示的下拉選項, 如下表所示: 
                * 表單設計類型=STD、RWD, 如下表
                    |                   | 內容異動 | 資料行移動 | 滑鼠雙擊 | 滑鼠單擊 | 滑鼠離開 | 自動完成 |
                    |-------------------|:-------:|:---------:|:--------:|:-------:|:-------:|:-------:|
                    |wTF.文字方塊                   | V |  |  |  | V | V |
                    |text.文字方塊(多筆表格)         | V |  |  |  |  | V |
                    |wTA.多行文字                   | V |  |  |  | V |  |
                    |textarea.多行文字(多筆表格)     | V |  |  |  |  |  |
                    |wRB.按鈕選項                   | V |  |  |  | V |  |
                    |wCB.核取方塊                   | V |  |  |  | V |  |
                    |checkbox.核取方塊(多筆表格)     | V |  |  | V |  |  |
                    |liteCheckbox.核取方塊(多筆瀏覽) |  |  |  | V |  |  |
                    |wDL.下拉選項                   | V |  |  |  | V |  |
                    |select.下拉選項(多筆表格)       | V |  |  |  |  |  |
                    |wPW.彈出視窗                   | V |  |  |  | V |  |
                    |popupwindow.彈出視窗(多筆表格)  | V |  |  |  |  |  |
                    |wLB.清單選項                   | V |  |  |  | V |  |
                    |wCanvas.畫布                   | V |  |  |  |  |  |
                    |wGrd.多筆表格                  |  | V | V |  |  |  |
                    |wGrdLite.多筆瀏覽              |  | V | V |  |  |  |
                    |wTree.樹狀清單                 |  | V |  |  |  |  |
                    |wCtnr.元件容器                 |  | V | V |  |  |  |
                    |wHObj隱藏元件                 | V |  |  |  |  |  |
                * 表單設計類型=APP, 如下表
                    |                   | 內容異動 | 資料行移動 | 滑鼠雙擊 | 滑鼠單擊 | 滑鼠離開 | 自動完成 |
                    |-------------------|:-------:|:---------:|:--------:|:-------:|:-------:|:-------:|
                    |wTF.文字方塊                   | V |  |  |  |  |  |
                    |wTA.多行文字                   | V |  |  |  |  |  |
                    |wRB.按鈕選項                   | V |  |  |  |  |  |
                    |wCB.核取方塊                   | V |  |  |  |  |  |
                    |wDL.下拉選項                   | V |  |  |  |  |  |
                    |wPW.彈出視窗                   | V |  |  |  |  |  |
                    |wLB.清單選項                   | V |  |  |  |  |  |
                    |wCanvas.畫布                   | V |  |  |  |  |  |
                    |wCtnr.元件容器                 |  | V | V |  |  |  |
                    |wHObj隱藏元件                 | V |  |  |  |  |  |


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