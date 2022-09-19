## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_AddHiddenObject_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_AddHiddenObject_APP]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 依規格定義-主畫面 結構清單駐留節點 表單隱藏元件
    * 執行按鍵.新增, 進入本單
    * 執行滑鼠右鍵.新增, 進入本單

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_AddHiddenObject_Block1]
    * `(1)元件名稱`
        * 用途說明
        * 規格說明
            * 自行輸入
    * `(2)行為選項`
        * 用途說明
        * 規格說明
            * 選項: 1.基本設定, 預設為已勾選, 並 除能
            * 依表單設計類型及駐留元件類型, 決定是否支援行為選項, 請參照下表規則決定畫面結果:
                * 表單設計類型=STD, 不支援的行為選項 除能, 否則 致能
                * 表單設計類型=RWD, 不支援的行為選項 除能, 否則 致能
                * 表單設計類型=APP 且 所有元件類型皆不支援的行為選項 隱藏; 若存在一個(含)以上的元件類型支援, 則不支援的元件類型, 選項 除能, 否則 致能<br>                
                ![pic][image_AddHiddenObject_Suppert]
    * `(3)儲存`
        * 用途說明
        * 規格說明
            * 存回時, 元件名稱, 新增多語詞庫
            * 存回時, 新增本次選取的行為選項
            * 判斷隱藏元件是存否在[駐留及執行順序][link_WidgetOrder]
                * 不存在, 則 取得專案語系清單, 及表單駐留及執行順序最大號+1, 將隱藏元件新增[駐留及執行順序][link_WidgetOrder] 
            * [權限驗証通則][link_ruleother6]
    * `(4)重設`
        * 用途說明
        * 規格說明
            * 除了基本設定, 清除所有已勾選行為選項

## <div id="save-action">儲存檢控</div>
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
	* 當`元件名稱`的內容已存在表單中, 錯誤訊息內容: 參數名:同表單下, 元件名稱不允重複

<!-- 圖片 -->
[image_AddHiddenObject_STD]:attachment/AddHiddenObject_STD.png
[image_AddHiddenObject_APP]:attachment/AddHiddenObject_APP.png
[image_AddHiddenObject_Block1]:attachment/AddHiddenObject_Block1.png
[image_AddHiddenObject_Suppert]:attachment/AddHiddenObject_Suppert.png

<!-- 超連結 -->
[link_WidgetOrder]:../WidgetOrder/README "版面設計/駐留順序"
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:../RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:../RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
[link_ruleother6]:../RulesOther/README#ruleother6 "共用通則_其它/權限驗証通則"