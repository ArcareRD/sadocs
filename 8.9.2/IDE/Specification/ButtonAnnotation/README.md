## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][button_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][button_MAE]
* [版面資訊通則][rule_Other_1]
		
## <div id="form-action">動作說明</div>
* 依規格關聯-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格關聯-主畫面 工具列.編修鍵, 進入本單的編輯模式

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本區塊</p>

    * STD</br>
        ![pic][fieldbreak1_STD]
    * MAE</br>
        ![pic][fieldbreak1_MAE]
    * (1)按鈕名稱
        * 用途說明
        * 規格說明
            * [使用多語詞庫通則][rule_dialog_2], 回傳:按鍵多語料號, 顯示:多語詞彙
    * (2)料號
        * 用途說明
        * 規格說明
            * 顯示傳入的按鍵料號
    * (3)按鈕類型
        * 用途說明
        * 規格說明
            * 選項 系統按鈕/工具列選單/工具列按鈕/選單內選項/傳統按鈕
            * 顯示按鍵的類型; 當 [新增表單/報表][AddFormReport_fieldbreak1](n)設計類型=APP，隱藏
    * (4)對應熱鍵
        * 用途說明
        * 規格說明
            * (3)按鈕類型=工具列選單/工具列按鈕 時, 下拉: [按鍵熱鍵通則][rule_Other_3], 過濾: 功能類別=1.自定鍵
            * (3)按鈕類型=選單內選項 時, 下拉: [按鍵熱鍵通則][rule_Other_3], 過濾: 功能類別=2.小選單_選項
            * (3)按鈕類型=工具列選單/工具列按鈕 and (3)按鈕類型<>選單內選項 時, 本欄位, 除能;
            * 當 [新增表單/報表][AddFormReport_fieldbreak1](n)設計類型=APP，隱藏
    * (17)系統按鈕
        * 用途說明
        * 規格說明
            * (3)按鈕類型=系統按鈕 時, 致能
            * 當 [新增表單/報表][AddFormReport_fieldbreak1](n)設計類型=APP，本區皆隱藏
    * (5)保留系統按鈕功能
        * 用途說明
        * 規格說明
            * 預設=true
            * (3)按鈕類型=系統按鈕 時, 致能
    * (6)使用系統提示訊息盒
        * 用途說明
        * 規格說明
            * 預設=true
            * (3)按鈕類型=系統按鈕 時, 致能
    * (7)隱藏按鈕類別
        * 用途說明
        * 規格說明
            * 選項 被動運作處理/控制記錄移動
            * 當 (3)按鈕類型=隱藏按鈕時, 致能
            * 當 (3)按鈕類型=隱藏按鈕 且 [新增表單/報表][AddFormReport_fieldbreak1](n)設計類型=APP，預設為 被動運作處理 且 隱藏
    * (8)歸屬工具列選單
        * 用途說明
            * 顯示子選單所屬的按鈕名稱; 只有在(3)按鈕類型=選單內選項 時, 有值
        * 規格說明    
            * 當 [新增表單/報表][AddFormReport_fieldbreak1](n)設計類型=APP，隱藏
    * (9)順序
        * 用途說明
            * 顯示子選單所屬的按鈕出現的順序; 只有在 (3)按鈕類型=選單內選項 時, 有值
        * 規格說明     
            * 當 [新增表單/報表][AddFormReport_fieldbreak1](n)設計類型=APP，隱藏
    * (10)致能時機
        * 用途說明
        * 規格說明
            * 選項 新增/修改/瀏覽
            * 當 [新增表單/報表][AddFormReport_fieldbreak1](n)設計類型=APP，本區皆隱藏  
    * (11)新增
        * 用途說明
        * 規格說明
            * 預設=false
    * (12)修改
        * 用途說明
        * 規格說明
            * 預設=false
    * (13)瀏覽
        * 用途說明
        * 規格說明
            * 預設=true
    * (14)遊標可駐留
        * 用途說明
        * 規格說明
            * 預設=false
            * 當 [新增表單/報表][AddFormReport_fieldbreak1](n)設計類型=APP，隱藏
    * (15)操作提示
        * 用途說明
        * 規格說明
            * [使用多語詞庫通則][rule_dialog_2], 回傳:多語料號, 顯示:多語詞彙
            * 當 [新增表單/報表][AddFormReport_fieldbreak1](n)設計類型=APP，隱藏
    * (16)功能描述: 
        * 用途說明
        * 規格說明
            * 顯示本按鍵於[規格描述]()的簡述內容
* <p id="fieldbreak2" style="color:blue;font-weight:bold">勾選記錄區塊</p>

    * STD</br>
        ![pic][fieldbreak2_STD]
    * MAE
        * 不支援, 區塊隱藏
    * (6)勾選記錄
        * 用途說明
        * 規格說明
            * 當 [新增表單/報表][AddFormReport_fieldbreak1](n)設計類型=APP，隱藏
    * (1)檔區
        * 用途說明
        * 規格說明
            * [挑選表單檔區通則][rule_Other_4], 過濾: 表單料號
    * (2)使用前存入資料表
        * 用途說明
        * 規格說明
    * (3)使用後清空資料表
        * 用途說明
        * 規格說明
            * 預設=false, 當 檔區 有值時, 才致能
    * (4)同時清空勾選紀錄
        * 用途說明
        * 規格說明
            * 預設=false, 當 檔區 有值時, 才致能    
    * (5)編修使用前存入暫存表格
        * 用途說明
        * 規格說明
            * 當 使用後清空資料表=true 才致能; 預設為true
* <p id="fieldbreak3" style="color:blue;font-weight:bold">執行後續</p>

    * STD</br>
        ![pic][fieldbreak3_STD]
    * MAE</br>
        ![pic][fieldbreak3_MAE]
    * (1)列入排程
        * 用途說明
        * 規格說明
            * 預設=false
    * (2)排程記錄
        * 用途說明
        * 規格說明
            * 開啟[排程設定]() 接收:排程料號, 顯示:排程名稱
            * 當 (1)列入排程否=true, 致能
    * (3)結束訊息
        * 用途說明
        * 規格說明
            * 預設=false
    * (4)訊息內容
        * 用途說明
        * 規格說明
            * [使用多語詞庫通則][rule_dialog_2], 回傳:多語料號, 顯示:多語詞彙
            * 當 (3)結束訊息=true, 致能
    * (6)結束後關閉表單
        * 用途說明
        * 規格說明
            * 預設=false
    * (7)重顯網格
        * 用途說明
        * 規格說明
           * 預設=false
           * 為true, 本區欄位皆除能
    * (8)檔區
        * 用途說明
        * 規格說明
            * [挑選表單檔區通則][rule_Other_4], 過濾: 表單料號
    * (9)資料行更新方式
        * 用途說明
        * 規格說明
            * 選項 駐留筆/全部記錄; 預設=駐留筆
    * (10)關聯檔區
        * 用途說明
        * 規格說明
            * 當 (9)資料行更新方式=駐留筆，則本欄位，致能; 預設=true
    * (11)樹內容重顯
        * 用途說明
        * 規格說明
           * 預設=false
           * 選項 駐留筆/正展/逆展/根節點/整顆樹; 預設:駐留筆
           * 當 [新增表單/報表][AddFormReport_fieldbreak1](n)設計類型=APP，本區皆隱藏
        * 為true，需判斷是否異動重顯網格
            * (7)重顯網格=false, 勾選重顯網格, 並預設檔區為樹元件對應檔區(若有兩個以上的樹元件，則取得第一個樹元件的檔區)
            * 若樹元件未設定檔區/或找不到樹元件, 則給表頭檔區
            * (7)重顯網格=true, 不做任何動作

## <div id="save-action">儲存檢控</div>
* 不允空白，以紅框線標註錯誤的欄位
    * [基本區塊][fieldbreak1](11)新增、[基本區塊][fieldbreak1](12)修改、[基本區塊][fieldbreak1](13)瀏覽, 至少有一筆=true
    * 當 [基本區塊][fieldbreak1](3)按鈕類型=隱藏按鈕, [基本區塊][fieldbreak1](7)隱藏按鈕類型, 不允空白
    * 當 [執行後續區塊][fieldbreak3](1)列入排程=true, 當 [執行後續區塊][fieldbreak3](2)排程記錄, 不允空白
    * 當 [執行後續區塊][fieldbreak3](3)結束訊息=true, [執行後續區塊][fieldbreak3](4)訊息內容, 不允空白
    * 當 [執行後續區塊][fieldbreak3](7)重顯網格=true
        * [執行後續區塊][fieldbreak3](8)檔區, 不允空白
        * [執行後續區塊][fieldbreak3](9)資料行更新方式, 至少有一筆=true
    * 當 [執行後續區塊][fieldbreak3](11)樹內容重顯=true
        * 至少有一筆=true
        * 必須設定 [執行後續區塊][fieldbreak3](7)重顯網格
* 其它檢控
    * 檢查所屬表單之按鍵, 依據 [基本區塊][fieldbreak1](3)按鈕類型=工具列選單/工具列按鈕、選單內選項 是否有相同的熱鍵設定

## <div id="other-desc">其它</div>
* [MAE加註儲存通則][rule_Other_5]

<!-- 圖片 -->
[button_STD]:attachment/ButtonAnnotation_STD.png
[button_MAE]:attachment/ButtonAnnotation_MAE.png
[fieldbreak1_STD]:attachment/fieldbreak1_STD.png
[fieldbreak1_MAE]:attachment/fieldbreak1_MAE.png
[fieldbreak2_STD]:attachment/fieldbreak2_STD.png
[fieldbreak3_STD]:attachment/fieldbreak3_STD.png
[fieldbreak3_MAE]:attachment/fieldbreak3_MAE.png

<!-- 超連結 -->
[fieldbreak1]:#fieldbreak1 "欄位說明/基本區塊"
[fieldbreak3]:#fieldbreak3 "欄位說明/執行後續區塊"
[rule_Other_1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[rule_Other_3]:../RulesOther/README#ruleother3 "共用通則_其它/按鍵熱鍵通則"
[rule_Other_4]:../RulesOther/README#ruleother4 "共用通則_其它/挑選表單檔區通則"
[rule_Other_5]:../RulesOther/README#ruleother5 "共用通則_其它/MAE加註儲存通則"
[rule_dialog_2]:../RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[AddFormReport_fieldbreak1]:../AddFormReport/README#fieldbreak1 "新增表單/報表/區塊1"
[temp]: "排程設定"


