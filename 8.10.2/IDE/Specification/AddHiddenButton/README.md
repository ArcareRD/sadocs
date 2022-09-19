## <div id="behavior-layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_button_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_button_MAE]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 依規格定義-主畫面 結構清單駐留節點 隱藏按鍵
    * 執行按鍵.新增, 進入本單
    * 執行滑鼠右鍵.新增, 進入本單

## <div id="behavior-object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本區塊</p>

    * ![pic][image_fieldbreak1]
    * `(1)按鍵名稱`
        * 用途說明
        * 規格說明
            * 自行輸入
    * `(2)行為選項`    
        * 用途說明
        * 規格說明        
            * 選項:1.基本設定, 預設為勾選, 除能
            * 依表單設計類型, 決定是否支援行為選項, 請參照下表規則決定畫面結果:
                * 表單設計類型=STD、RWD, 不支援的行為選項, 畫面以除能方式表示
                * 表單設計類型=APP, 不支援的行選項, 畫面以隱藏方式表示
                |   | STD | RWD | APP |
                |-- |-----|-----|-----|
                |1.基本設定 | V | V | V |
                |2.執行限制 | V | V | V |
                |A.開啟它單 | V | V | V |
                |B.開啟報表 | V | V |  |
                |C.資料交易 | V | V | V |
                |D.資料交換 | V | V |  |
                |E.郵件發送 | V | V |  |
                |F.資料載入 | V |  |  |	
                |G.資料過濾 | V | V | V |
                |H.外部執行 | V | V | V |
                |J.溝通訊息 | V | V |  |
                |K1.表單特效 | V | V | V |
                |K2.動態表格 | V |  |  |	
                |K3.帳號同步 | V | V |  |	
                |K4.系統複製 | V | V |  |	
                |K5.邏輯函數 | V | V |  |	
                |K6.連結物件 | V | V | V |
                |K7.檔案傳輸 | V | V | V |
                |M.預存程序 | V | V |  |	
                |N.裝置支援 |  |  | V |
                |P.推播通知 | V | V | V |
    * `(3)儲存`
        * 用途說明
        * 規格說明
            * 存回時, 按鍵名稱, 新增多語詞庫
            * 存回時, 新增本次選取的行為選項
            * [權限驗証通則][link_ruleother6]
    * `(4)重設`
        * 用途說明
        * 規格說明
            * 除了基本設定, 清除所有已勾選行為選項

## <div id="save-action">儲存檢控</div>	
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
	* 當`按鍵名稱`的內容已存在表單中, 錯誤訊息內容: 參數名:同表單下, 按鍵名稱不允重複

<!-- 圖片 -->
[image_button_STD]:attachment/AddHiddenButton_STD.png
[image_button_MAE]:attachment/AddHiddenButton_MAE.png
[image_fieldbreak1]:attachment/AddHiddenButton_STD_block1.png

<!-- 超連結 -->
[link_WidgetOrder]:../WidgetOrder/README "版面設計/駐留順序"
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:../RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:../RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
[link_ruleother6]:../RulesOther/README#ruleother6 "共用通則_其它/權限驗証通則"