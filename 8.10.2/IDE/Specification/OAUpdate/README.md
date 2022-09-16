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
    * `(1)元件名稱`
        * 用途說明
        * 規格說明
            * 參照 [使用多語詞庫通則][link_ruledialog2], 回傳:元件多語內容並顯示
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示前單傳入的元件料號
    * `(3)執行條件`
        * 用途說明
        * 規格說明
            * 參照 [操作條件式通則][link_ruledialog1], 回傳並顯示: 條件說明
    * `(4)自行輸入才有效`
        * 用途說明
        * 規格說明
            * 當表單設計類型=APP, 則 顯示, 否則 隱藏
            * 系統預設: 不勾選

* <p id="fieldbreak2" style="color:blue;font-weight:bold">固定式更新</p>

    * ![pic][image_oaudate_block2]
    * `(1)固定式更新`
        * 用途說明
        * 規格說明
            * 當 元件類型=wGrdLite.多筆瀏覽 或 為wCtnr.元件容器下的wCB.核取方塊, 則 除能
    * `(2)固定式更新表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
            * `(1)固定式更新`未勾選, 則 除能, 否則 致能
    * `(3)項次`
        * 用途說明
        * 規格說明
            * 依序給流水號
    * `(4)目的欄位`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單元件通則][link_ruledialog7], 限定: 本表單下的元件, 進行挑選, 回傳: 表單元件
                * 當表單設計類型=RWD, 限定: 元件須存在 表單種類=1.一頁單筆(單筆)/6.過濾條件查詢(條件多筆)/7.指定條件執行(單改) 且 檔區=表頭 者
            * 參照 [個資加密提示通則][link_ruleother11]
    * `(5)給值來源`
        * 用途說明
        * 規格說明
            * 參照 [操作運算式通則][link_ruledialog18], 限定: 無查表功能

* <p id="fieldbreak3" style="color:blue;font-weight:bold">查表式更新</p>

    * ![pic][image_oaudate_block3]
    * `(1)查表式更新`
        * 用途說明
        * 規格說明
            * 當 元件類型=wGrdLite.多筆瀏覽 或 為wCtnr.元件容器下的wCB.核取方塊, 則 除能
    * `(2)查表條件`
        * 用途說明
        * 規格說明
            * 參照 [操作條件式通則][link_ruledialog1], 回傳: 查表類別、表格料號、是否載入個資加密欄位=true、是否載入密碼處理欄位=false、條件ID
            * `(1)查表式更新`未勾選, 則 除能, 否則 致能
    * `(3)無符合記錄時清空目的欄位`
        * 用途說明
        * 規格說明
            * `(2)查表條件`為空 或 `(2)查表條件`未挑選表格, 顯示訊息 "請選擇查表帶值內容-條件式[條件式來源表格]"
            * `(1)查表式更新`未勾選, 則 除能, 否則 致能
    * `(4)給值內容表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
            * `(1)查表式更新`未勾選, 則 除能, 否則 致能
    * `(5)項次`
        * 用途說明
        * 規格說明
            * 依序給流水號
    * `(6)目的欄位`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單元件通則][link_ruledialog7], 限定: 本表單下的元件, 進行挑選, 回傳: 表單元件
                * 當表單設計類型=RWD, 限定: 元件須存在 表單種類=1.一頁單筆(單筆)/6.過濾條件查詢(條件多筆)/7.指定條件執行(單改) 且 檔區=表頭 者
            * 參照 [個資加密提示通則][link_ruleother11]
    * `(7)給值來源`
        * 用途說明
        * 規格說明
            * `(2)查表條件`為空 或 `(2)查表條件`未挑選表格, 顯示訊息 "請選擇查表帶值內容-條件式[條件式來源表格]"
            * `(2)查表條件`的查表類別=資料表, 則參照 [挑選資料表元件通則][link_ruledialog5], 限定: `(2)查表條件`的表格料號, 挑選並回傳資料表元件
            * `(2)查表條件`的查表類別=檢視表, 則參照 [挑選檢視表元件通則][link_ruledialog8], 限定: `(2)查表條件`的表格料號, 挑選並回傳檢視表元件
            * 暫不支援個資解密，故不提供變色處理
    * `(8)來源排序表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
            * `(1)查表式更新`未勾選, 則 除能, 否則 致能
    * `(9)欄位名稱`
        * 用途說明
        * 規格說明
            * `(2)查表條件`的查表類別=資料表, 則參照 [挑選資料表元件通則][link_ruledialog5], 限定: `(2)查表條件`的表格料號, 挑選並回傳資料表元件
            * `(2)查表條件`的查表類別=檢視表, 則參照 [挑選檢視表元件通則][link_ruledialog8], 限定: `(2)查表條件`的表格料號, 挑選並回傳檢視表元件
            * 暫不支援個資解密，故不提供變色處理
    * `(10)升/降冪`
        * 用途說明
        * 規格說明
            * 選項 升冪/降冪, 預設:升冪

* <p id="fieldbreak4" style="color:blue;font-weight:bold">表身欄位更新</p>

    * ![pic][image_oaudate_block4]
    * `(1)表身欄位更新`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則 隱藏; 當 表單設計類型=RWD, 則 除能
            * 當 為wCtnr.元件容器下的wCB.核取方塊, 則 除能
    * `(2)檔區`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則 隱藏
            * `(1)表身欄位更新`未勾選, 則 除能, 否則 致能
            * 參照 [挑選表單檔區通則][link_ruleother4], 限定: 本單資料區 且 不為表頭
    * `(3)執行條件`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則 隱藏
            * `(1)表身欄位更新`未勾選, 則 除能, 否則 致能
            * 參照 [操作條件式通則][link_ruledialog1], 限定: 無查表功能
    * `(4)欄位更新類別`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則 隱藏
            * `(1)表身欄位更新`未勾選, 則 除能, 否則 致能
            * 選項 連結全刪除/欄位值更新
    * `(5)需要確認`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則 隱藏
            * `(4)欄位更新類別`=連結全刪除, 則 致能, 否則 除能
            * 若本元件的僅供顯示為勾選, 則本欄位取消勾選 並 除能
    * `(6)確認訊息`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則 隱藏
            * `(5)需要確認`為勾選, 則 致能, 否則 除能
            * 參照 [使用多語詞庫通則][link_ruledialog2], 回傳並顯示多語內容
    * `(7)目的欄位`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則 隱藏
            * `(4)欄位更新類別`=欄位值更新, 則 致能, 否則 除能
            * 參照 [挑選表單元件通則][link_ruledialog7], 限定: 本表單下 且 為同`(2)檔區`的元件, 進行挑選, 回傳: 表單元件
            * 參照 [個資加密提示通則][link_ruleother11]
    * `(8)給值來源`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則 隱藏
            * `(4)欄位更新類別`=欄位值更新, 則 致能, 否則 除能
            * 參照 [操作運算式通則][[link_ruledialog18]], 限定: 無查表功能

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

* <p id="fieldbreak6" style="color:blue;font-weight:bold">網格更新</p>

    * ![pic][image_oaudate_block6]
    * `(1)網格更新`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則 隱藏; 當 表單設計類型=RWD, 則 除能
            * 當 為wCtnr.元件容器下的wCB.核取方塊, 則 除能
    * `(2)網格元件`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則 隱藏
            * `(1)網格更新`為勾選, 則 致能, 否則 除能
            * 參照 [挑選表單元件通則][link_ruledialog7], 限定: 本表單下 且 元件類別=wGrd.多筆表格、wGrdLite.多筆瀏覽的元件, 進行挑選, 回傳: 表單元件

* <p id="fieldbreak7" style="color:blue;font-weight:bold">變數更新</p>

    * ![pic][image_oaudate_block7]
    * `(1)變數更新`
        * 用途說明
        * 規格說明
            * 當 元件類型=wGrdLite.多筆瀏覽 或 為wCtnr.元件容器下的wCB.核取方塊, 則 除能
    * `(2)變數更新表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
            * `(1)變數更新`未勾選, 則 除能, 否則 致能
    * `(3)項次`
        * 用途說明
        * 規格說明
            * 依序給流水號
    * `(4)全域變數`
        * 用途說明
        * 規格說明
            * 參照 [挑選全域變數通則][link_ruledialog10], 回傳: 全域變數
    * `(5)給值來源`
        * 用途說明
        * 規格說明
            * 參照 [操作運算式通則][[link_ruledialog18]]

* <p id="fieldbreak8" style="color:blue;font-weight:bold">自定函數更新</p>

    * ![pic][image_oaudate_block8]
    * `(1)自定函數更新`
        * 用途說明
        * 規格說明
            * 當 表單設計類型=APP, 則 隱藏; 當 表單設計類型=RWD, 則 除能
            * 當 為wCtnr.元件容器下的wCB.核取方塊, 則 除能
    * `(2)自定函數`
        * 用途說明
        * 規格說明
            * `(1)自定函數更新`為勾選, 則 致能, 否則 除能
            * 顯示自定函數名稱
            * 不須輸入, 唯讀
    * `(11)自定函數鍵`
        * 用途說明
        * 規格說明
            * 單據於編輯狀態 或 單據於瀏覽狀態 且 `(2)自定函數`有值 時, 致能
            * 開窗[自定函數][link_CustomFunction], 回傳: 自定函數, 並寫入`(2)自定函數`
            * 異動時執行`(6)參數載入鍵`
    * `(3)目的欄位`
        * 用途說明
        * 規格說明
            * `(1)自定函數更新`為勾選, 則 致能, 否則 除能
            * 參照 [挑選表單元件通則][link_ruledialog7], 限定: 本表單下的元件, 進行挑選, 回傳: 表單元件
                * 當表單設計類型=RWD, 限定: 元件須存在 表單種類=1.一頁單筆(單筆)/6.過濾條件查詢(條件多筆)/7.指定條件執行(單改) 且 檔區=表頭 者
            * 參照 [個資加密提示通則][link_ruleother11]
    * `(4)給值內容表格`
        * 用途說明
        * 規格說明
            * `(1)自定函數更新功能`為勾選, 則 致能, 否則 除能
    * `(5)項次`
        * 用途說明
        * 規格說明
            * 依序給流水號
    * `(6)參數載入鍵`
        * 用途說明
        * 規格說明
            * 依`(2)自定函數`取得[自定函數][link_CustomFunction]中的傳遞參數載入`(4)給值內容表格`中的`(7)參數名稱`、`(8)參數型態`
            * 依`(2)自定函數`及`(7)參數名稱`至[自定函數][link_CustomFunction]判斷, 不存在`(4)給值內容表格`中, 則新增
            * 依`(2)自定函數`及`(7)參數名稱`至[自定函數][link_CustomFunction]判斷, 於`(4)給值內容表格`中存在無效參數, 則刪除
    * `(7)參數名稱`
        * 用途說明
        * 規格說明
            * 顯示[自定函數][link_CustomFunction]中的傳遞參數名稱
    * `(8)參數型態`
        * 用途說明
        * 規格說明
            * 顯示[自定函數][link_CustomFunction]中的傳遞參數型態
            * 型態選項 字串/數字/陣列/日期/布林
    * `(9)傳遞型態`
        * 用途說明
        * 規格說明
            * 選項 表單元件/固定值/表單參數/全域變數
    * `(10)傳遞內容`
        * 用途說明
        * 規格說明
            * `(9)傳遞型態`=固定值, 由使用者自行輸入
            * `(9)傳遞型態`=表單元件, 參照 [挑選表單元件通則][link_ruledialog7], 限定: 本表單下的元件, 進行挑選, 回傳: 表單元件
            * `(9)傳遞型態`=表單參數, 參照 [挑選參數通則][link_ruledialog9], 限定: 本表單下的參數, 進行挑選, 回傳: 表單參數
            * `(9)傳遞型態`=全域變數, 參照 [挑選全域變數通則][link_ruledialog10], 回傳: 全域變數
    * `(12)同名對應鍵`
        * 用途說明
        * 規格說明
            * 依`(7)參數名稱`比對元件名稱, 預設給同名元件
            * 無同名元件 或 `(10)傳遞內容`不為空值, `(9)傳遞型態`、`(10)傳遞內容`皆不異動
            * 有同名元件 且 `(10)傳遞內容`為空值, `(9)傳遞型態`給值表單元件、`(10)傳遞內容`給值同名元件

* <p id="fieldbreak9" style="color:blue;font-weight:bold">密碼更新</p>

    * ![pic][image_oaudate_block9]
    * `(1)密碼更新`
        * 用途說明
        * 規格說明
            * 當 元件類型=wGrdLite.多筆瀏覽 或 為wCtnr.元件容器下的wCB.核取方塊, 則 除能
    * `(2)更新類型`
        * 用途說明
        * 規格說明
            * `(1)密碼更新`為勾選, 則 致能, 否則 除能
            * 選項 密碼/明碼
    * `(3)更新元件表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
            * `(1)密碼更新`為勾選, 則 致能, 否則 除能
    * `(4)項次`
        * 用途說明
        * 規格說明
            * 依序給流水號
    * `(5)元件名稱`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單元件通則][link_ruledialog7], 限定: 本表單下的元件 且 為密碼顯示, 進行挑選, 回傳: 表單元件
            * 參照 [個資加密提示通則][link_ruleother11]

## <div id="save-action">儲存檢控</div>
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回不允空白檢控通則][link_ruleother7]
    * [固定式更新][link_fieldbreak2]
        * 當`固定式更新表格`有記錄時, `目的欄位`、`給值來源`, 不允空白
    * [查表式更新][link_fieldbreak3]
        * 當`查表式更新`為勾選時, `查表條件`, 不允空白
        * 當`給值內容表格`有記錄時, `目的欄位`、`給值來源`, 不允空白
        * 當`來源排序表格`有記錄時, `欄位名稱`, 不允空白
    * [表身欄位更新][link_fieldbreak4]
        * 當`表身欄位更新`為勾選時, `檔區`、`欄位更新類別`, 不允空白
        * 當`欄位更新類別`=連結全刪除 且 `需要確認`已勾選 時, `確認訊息`, 不允空白
        * 當`欄位更新類別`=欄位值更新 時, `目的欄位`、`給值來源`, 不允空白
    * [呼叫按鈕功能][link_fieldbreak5]
        * `呼叫按鈕功能`為勾選時, `按鈕功能名`、`呼叫時機`, 不允空白
    * [網格更新][link_fieldbreak6]
        * 當`網格更新`為勾選時, `網格元件名`, 不允空白
    * [變數更新][link_fieldbreak7]
        * 當`變數更新表格`有記錄時, `全域變數`、`給值來源`, 不允空白
    * [自定函數更新][link_fieldbreak8]
        * 當`自定函數更新`為勾選時, `自定函數`、`目的欄位`, 不允空白
        * 當`給值內容表格`有記錄時, `參數名稱`、`傳遞型態`、`傳遞內容`, 不允空白
    * [密碼更新][link_fieldbreak9]
        * 當`密碼更新`為勾選時, `更新類型`, 不允空白
        * 當`變數更新表格`有記錄時, `元件名稱`, 不允空白
	
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
    * 以下至少勾選一項更新方式
        * [固定式更新][link_fieldbreak2]的`固定式更新`
        * [查詢式更新][link_fieldbreak3]的`查詢式更新`
        * [表身欄位更新][link_fieldbreak4]的`表身欄位更新`
        * [呼叫按鈕功能][link_fieldbreak5]的`呼叫按鈕功能`
        * [網格更新][link_fieldbreak6]的`網格更新`
        * [變數更新][link_fieldbreak7]的`變數更新`
        * [自動函數更新][link_fieldbreak8]的`自動函數更新`
        * [密碼更新][link_fieldbreak9]的`密碼更新`
    * 當[固定式更新][link_fieldbreak2]的`固定式更新`為勾選, 則`固定式更新表格`至少要有一筆記錄
    * 當[查表式更新][link_fieldbreak2]的`查表式更新`為勾選, 則`給值內容表格`至少要有一筆記錄
    * 當[變數更新][link_fieldbreak7]的`變數更新`為勾選, 則`變數更新表格`至少要有一筆記錄
    * 當[變數更新][link_fieldbreak7]`變數更新表格`有記錄時, 則`全域變數`, 不允重覆
    * 當[密碼更新][link_fieldbreak9]的`密碼更新`為勾選, 則`密碼更新表格`至少要有一筆記錄
    * 當[密碼更新][link_fieldbreak9]`密碼更新`有記錄時, 則`元件名稱`, 不允重覆

## <div id="other-desc">其它</div>
* [MAE加註儲存通則][link_ruleother5]

<!-- 圖片 -->
[image_oaudate_STD]:attachment/OAUpdate_STD.png
[image_oaudate_APP]:attachment/OAUpdate_APP.png
[image_oaudate_block1]:attachment/OAUpdate_block1.png
[image_oaudate_block2]:attachment/OAUpdate_block2.png
[image_oaudate_block3]:attachment/OAUpdate_block3.png
[image_oaudate_block4]:attachment/OAUpdate_block4.png
[image_oaudate_block5]:attachment/OAUpdate_block5.png
[image_oaudate_block6]:attachment/OAUpdate_block6.png
[image_oaudate_block7]:attachment/OAUpdate_block7.png
[image_oaudate_block8]:attachment/OAUpdate_block8.png
[image_oaudate_block9]:attachment/OAUpdate_block9.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_fieldbreak2]:#fieldbreak2 "欄位說明/固定式更新"
[link_fieldbreak3]:#fieldbreak3 "欄位說明/查表式更新"
[link_fieldbreak4]:#fieldbreak4 "欄位說明/表身欄位更新"
[link_fieldbreak5]:#fieldbreak5 "欄位說明/呼叫按鈕功能"
[link_fieldbreak6]:#fieldbreak6 "欄位說明/網格更新"
[link_fieldbreak7]:#fieldbreak7 "欄位說明/變數更新"
[link_fieldbreak8]:#fieldbreak8 "欄位說明/自定函數更新"
[link_fieldbreak9]:#fieldbreak9 "欄位說明/密碼更新"
[link_rulebutton3]:../RulesButton/README#rulebutton3 "共用通則_按鍵操作/操作表格記錄通則"
[link_rulebutton2]:{1}/RulesButton/README#rulebutton2 "共用通則_按鍵操作/單據異動資料按鍵操作通則"
[link_ruledialog1]:{1}/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog13]:{1}/RulesDialog/README#ruledialog13 "共用通則_開啟單據/挑選表單按鍵通則"
[link_ruleother1]:{1}/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruledialog7]:{1}/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruleother11]:../RulesOther/README#ruleother11 "共用通則_其它/個資加密提示通則"
[link_ruledialog18]:{1}/RulesDialog/README#ruledialog18 "共用通則_開啟單據/操作運算式通則"
[link_ruleother7]:{1}/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:{1}/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
[link_ruledialog5]:{1}/RulesDialog/README#ruledialog5 "共用通則_開啟單據/挑選資料表元件通則"
[link_ruledialog8]:{1}/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_ruleother4]:../RulesOther/README#ruleother4 "共用通則_其它/挑選表單檔區通則"
[link_ruledialog2]:../RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruledialog10]:../RulesDialog/README#ruledialog10 "共用通則_開啟單據/挑選全域變數通則"
[link_ruledialog9]:../RulesDialog/README#ruledialog9 "共用通則_開啟單據/挑選參數通則"
[link_CustomFunction]:../CustomFunction/README "自定函數"
[link_ruleother5]:../RulesOther/README#ruleother5 "共用通則_其它/MAE加註儲存通則"