## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_OAValidate_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_OAValidate_APP]

* [版面資訊通則][link_ruleother1]
		
## <div id="form-action">動作說明</div>
* 依規格關聯-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格關聯-主畫面 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本區塊</p>

    ![pic][image_fieldbreak1]
    * `(1)欄位名稱`
        * 用途說明
        * 規格說明
            * 依專案語系, 顯示元件多語名稱
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示元件料號
    * `(3)執行條件`
        * 用途說明
        * 規格說明
            * 參照 [操作條件式通則][link_ruledialog1], 回傳並顯示: 條件說明
    * `(4)自行輸入才有效`
        * 用途說明
        * 規格說明
            * 當`表單設計類型`=APP, 隱藏
            * 以下條件成立, 則致能, 否則除能
                * 當元件類型=wTF.文字方塊、wDL.下拉選項、wPW.彈出視窗、text.文字方塊(欄位資料)、select.下拉選項(欄位資料)、popupwindow.彈出視窗(欄位資料)
                * 元件非僅供顯示
                * 若有設定元件加註_選項勾選 且 選項種類=變動項次 且 可自行輸入
    * `(5)驗證方法`
        * 用途說明
        * 規格說明
            * 選項 運算判斷/查表比對/鍵入控制/自定函數
            * 當`表單設計類型`=APP, 選項 自定函數 隱藏

* <p id="fieldbreak2" style="color:blue;font-weight:bold">運算判斷</p>

    ![pic][image_fieldbreak2]
    * `(1)運算內容`
        * 用途說明
        * 規格說明
            * 當`驗證方法`為運算判斷, 才致能
            * 參照 [操作運算式通則][link_ruledialog18]

* <p id="fieldbreak3" style="color:blue;font-weight:bold">查表比對</p>

    ![pic][image_fieldbreak3]
    * `(1)查表比對內容`
        * 用途說明
        * 規格說明
            * 當`驗證方法`為查表比對, 才致能
            * 參照 [操作條件式通則][link_ruledialog1], 回傳並顯示: 條件說明
            * 當查表表格料號有異動, 且`替代來源`為查表 時, 則清空訊息替代中, `來源類型`為查表欄位的`來源欄位`

* <p id="fieldbreak4" style="color:blue;font-weight:bold">鍵入控制</p>

    ![pic][image_fieldbreak4]
    * `(1)禁止鍵入字元_中文字`
        * 用途說明
        * 規格說明
            * 當`驗證方法`為鍵入控制, 才致能
            * 預設 未勾選
    * `(2)禁止鍵入字元_數字`
        * 用途說明
        * 規格說明
            * 當`驗證方法`為鍵入控制, 才致能
            * 預設 未勾選
    * `(3)禁止鍵入字元_英文字`
        * 用途說明
        * 規格說明
            * 當`驗證方法`為鍵入控制, 才致能
            * 預設 未勾選
    * `(4)禁止鍵入字元_特殊符號`
        * 用途說明
        * 規格說明
            * 當`驗證方法`為鍵入控制, 才致能
            * 預設 未勾選
    * `(5)禁止鍵入字元_例外符號`
        * 用途說明
        * 規格說明
            * 當`驗證方法`為鍵入控制, 才致能
            * 預設 未勾選
    * `(6)例外符號內容`
        * 用途說明
        * 規格說明
            * 當`驗證方法`為鍵入控制 且 `(5)禁止鍵入字元_例外符號`為勾選, 才致能

* <p id="fieldbreak5" style="color:blue;font-weight:bold">自定函數</p>

    ![pic][image_fieldbreak5]
    * `(1)自定函數`
        * 用途說明
        * 規格說明
            * 當 `表單設計類型`=APP, 則 隱藏
    * `(2)自定函數區塊`
        * 用途說明
        * 規格說明
            * 當 `表單設計類型`=APP, 則 隱藏
            * `(1)自定函數`為勾選, 則 致能, 否則 除能
            * 參照 [挑選自定函數通則][link_ruledialog21]
    * `(3)判斷邏輯式`
        * 用途說明
        * 規格說明
            * 選項 大於/小於/等於/大於等於/小於等於/不等於
    * `(4)判斷類別`
        * 用途說明
        * 規格說明
            * 選項 表單元件/固定值/函數; 預設 表單元件
    * `(5)判斷內容`
        * 用途說明
        * 規格說明
            * `(4)判斷類別`=固定值, 由使用者自行輸入
            * `(4)判斷類別`=表單元件, 參照 [挑選表單元件通則][link_ruledialog7], 限定: 本表單下的元件, 進行挑選, 回傳: 表單元件
                * 參照 [個資加密提示通則][link_ruleother11]
            * `(4)判斷類別`=函數, 下拉系統函數挑選, 過濾: 適用等式右邊且無參數

* <p id="fieldbreak6" style="color:blue;font-weight:bold">異常處理</p>

    ![pic][image_fieldbreak6]
    * `(1)異常判斷`
        * 用途說明
        * 規格說明
            * 選項 通過驗証/未通過驗証; 預設 未通過驗証
    * `(2)異常類別`
        * 用途說明
        * 規格說明
            * 當 `表單設計類型`=APP, 則 隱藏
            * 當 `表單設計類型`=RWD, 則 除能
            * 選項 錯誤/警告/操作者決定; 預設 錯誤
    * `(3)按鍵駐留預設`
        * 用途說明
        * 規格說明
            * 當 `表單設計類型`=APP, 則 隱藏
            * 當 `表單設計類型`=RWD, 則 除能
            * 當 `(2)異常類別`=操作者決定, 致能
            * 選項 是/否; 預設=是
    * `(3)異常訊息`
        * 用途說明
        * 規格說明
            * 當 `驗證方法`=鍵入控制 時, 除能
            * 參照 [操作多語訊息及替代通則][link_ruledialog17], 依駐留專案, 進行訊息內容挑選, 回傳並顯示: 多語名稱

* <p id="fieldbreak7" style="color:blue;font-weight:bold">重複檢控時機</p>

    ![pic][image_fieldbreak7]
    * `(1)新增存回`
        * 用途說明
        * 規格說明
            * 當 `表單設計類型`=APP, 則 隱藏        
            * 當 `驗證方法`=查表比對 時, 致能
    * `(2)修改存回`
        * 用途說明
        * 規格說明
            * 當 `表單設計類型`=APP, 則 隱藏        
            * 當 `驗證方法`=查表比對 時, 致能

## <div id="save-action">儲存檢控</div>
* 不允空白檢控, 規則參照 [存回不允空白檢控通則][link_ruleother7]
    * [基本][link_fieldbreak1]
        * `驗證方法`必擇一, 不允空白
    * [運算判斷][link_fieldbreak2]
        * 當 `驗證方法`=運算判斷, `運算內容`, 不允空白
    * [查表比對][link_fieldbreak3]
        * 當 `驗證方法`=查表比對, `查表比對內容`, 不允空白
    * [鍵入控制][link_fieldbreak4]
        * 當 `驗證方法`=鍵入控制, `禁止鍵入字元_例外符號`勾選時, `例外符號內容`, 不允空白
    * [自定函數][link_fieldbreak5]
        * 當 `驗證方法`=自定函數, `自定函數`、`判斷邏輯式`、`判斷類別`、`判斷內容`, 不允空白
        * 當 `驗證方法`=自定函數 且 `自定函數參數表格`有記錄時, `傳遞型態`、`傳遞內容`, 不允空白
    * [異常處理][link_fieldbreak6]
        * `異常訊息`, 不允空白

* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
    * [鍵入控制][link_fieldbreak4]
        * 當 `驗證方法`=鍵入控制, 則`禁止鍵入的字元`至少要勾選一個
        * 當 `驗證方法`異動時, 檢查是否與 替代訊息 的來源相同, 若不同時則顯示訊息

## <div id="other-desc">其它</div>
* [MAE加註儲存通則][link_ruleother5]
* [重複檢控時機][link_fieldbreak7]
    * 當 `新增存回`勾選, 判斷本單系統按鍵.新增存回/[按鍵加註_執行限制][link_BALimitation], 不存在新增, 存在修改 
    * 當 `修改存回`勾選, 判斷本單系統按鍵.修改存回/[按鍵加註_執行限制][link_BALimitation], 不存在新增, 存在修改 
    * 以下說明寫入[按鍵加註_執行限制][link_BALimitation]的內容
        * [按鍵加註_執行限制][link_BALimitation]/`判斷條件` = `查表比對內容`
        * [按鍵加註_執行限制][link_BALimitation]/`執行時機` = `異常判斷`
            * `異常判斷`=通過驗證, 則勾選 [按鍵加註_執行限制][link_BALimitation]/`執行時機`/`條件成立`=執行、`不條件成立`=訊息
            * `異常判斷`=未通過驗證, 則勾選 [按鍵加註_執行限制][link_BALimitation]/`執行時機`/`條件成立`=訊息、`不條件成立`=執行
            * 當 `異常訊息`有 替代變數 時, 同時複製替代訊息內容

<!-- 圖片 -->
[image_OAValidate_STD]:attachment/OAValidate_STD.png
[image_OAValidate_APP]:attachment/OAValidate_APP.png
[image_fieldbreak1]:attachment/OAValidate_fieldbreak1.png
[image_fieldbreak2]:attachment/OAValidate_fieldbreak2.png
[image_fieldbreak3]:attachment/OAValidate_fieldbreak3.png
[image_fieldbreak4]:attachment/OAValidate_fieldbreak4.png
[image_fieldbreak5]:attachment/OAValidate_fieldbreak5.png
[image_fieldbreak6]:attachment/OAValidate_fieldbreak6.png
[image_fieldbreak7]:attachment/OAValidate_fieldbreak7.png

<!-- 超連結 -->
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_rulebutton2]:../RulesButton/README#rulebutton2 "共用通則_按鍵操作/單據異動資料按鍵操作通則"
[link_ruledialog1]:../RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog18]:../RulesDialog/README#ruledialog18 "共用通則_開啟單據/操作運算式通則"
[link_ruledialog7]:../RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruleother11]:../RulesOther/README#ruleother11 "共用通則_其它/個資加密提示通則"
[link_ruledialog21]:../RulesDialog/README#ruledialog21 "共用通則_開啟單據/挑選自定函數通則"
[link_ruledialog2]:../RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruledialog17]:../RulesDialog/README#ruledialog2 "共用通則_開啟單據/操作多語訊息及替代通則"
[link_ruleother5]:../RulesOther/README#ruleother5 "共用通則_其它/MAE加註儲存通則"
[link_ruleother7]:../RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:../RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_fieldbreak2]:#fieldbreak2 "欄位說明/運算判斷"
[link_fieldbreak3]:#fieldbreak3 "欄位說明/查表比對"
[link_fieldbreak4]:#fieldbreak4 "欄位說明/鍵入控制"
[link_fieldbreak5]:#fieldbreak5 "欄位說明/自定函數"
[link_fieldbreak6]:#fieldbreak6 "欄位說明/異常處理"
[link_fieldbreak7]:#fieldbreak7 "欄位說明/重複檢控時機"
[link_BALimitation]:../BALimitation/README "按鍵加註_執行限制"