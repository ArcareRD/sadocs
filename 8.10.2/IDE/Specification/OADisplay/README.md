## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_OADisplay_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_OADisplay_MAE]
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
    * `(4)內容處理`
        * 用途說明
        * 規格說明
            * 單一選項: 固定值/欄位組合/被突顯/僅變更顏色/依語系顯示對應內容/填入行號
            * 當 表單設計類型=APP, 選項 固定值/欄位組合/被突顯/依語系顯示對應內容 隱藏
    * `(5)固定值`
        * 用途說明
        * 規格說明
            * `(4)內容處理`=固定值, 則致能, 否則除能
            * [使用多語詞庫通則][link_ruledialog2], 回傳:多語料號, 顯示:多語詞彙
            * 當 表單設計類型=APP, 隱藏
    * `(6)欄位組合`
        * 用途說明
        * 規格說明
            * `(4)內容處理`=欄位組合, 則致能, 否則除能
            * 參照 [操作運算式通則][link_ruledialog18], 限定: 無查表功能
            * 當 表單設計類型=APP, 隱藏
    * `(7)被突顯`
        * 用途說明
        * 規格說明
            * `(4)內容處理`=被突顯, 則致能, 否則除能
            * 下拉選項 左上/左中/左下/右上/右中/右下
            * 當 表單設計類型=APP, 隱藏
    * `(8)字體顏色`
        * 用途說明
        * 規格說明
            * 開窗色盤或可自行輸入色號
    * `(9)背景顏色`
        * 用途說明
        * 規格說明
            * 開窗色盤或可自行輸入色號

## <div id="save-action">儲存檢控</div>
* 不允空白檢控, 規則參照 [存回不允空白檢控通則][link_ruleother7]
    * [基本][link_fieldbreak1]
        * `內容處理`必擇一, 不允空白
        * `內容處理`=固定值, `固定值` 不允空白
        * `內容處理`=欄位組合, `欄位組合` 不允空白
        * `內容處理`=被突顯, `被突顯`、`字體顏色` 不允空白
        * `內容處理`=僅變更顏色, `字體顏色`、`背景顏色` 不允空白

## <div id="other-desc">其它</div>
* 若`內容處理`=固定值、欄位組合、填入行號 且 元件存在表格.PhyEncryptionFieldUsage(資料表加密欄位使用狀況), 則依元件料號, 刪除資料
* [MAE加註儲存通則][link_ruleother5]

<!-- 圖片 -->
[image_OADisplay_STD]:attachment/OADisplay_STD.png
[image_OADisplay_MAE]:attachment/OADisplay_MAE.png
[image_fieldbreak1]:attachment/OADisplay_fieldbreak1.png

<!-- 超連結 -->
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_rulebutton2]:../RulesButton/README#rulebutton2 "共用通則_按鍵操作/單據異動資料按鍵操作通則"
[link_ruledialog1]:../RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog2]:../RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruledialog18]:../RulesDialog/README#ruledialog18 "共用通則_開啟單據/操作運算式通則"
[link_ruleother5]:../RulesOther/README#ruleother5 "共用通則_其它/MAE加註儲存通則"
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother7]:../RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:../RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"