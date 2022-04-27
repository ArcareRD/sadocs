## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_form_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_form_MAE]
* [版面資訊通則][link_ruleother1]
		
## <div id="form-action">動作說明</div>
* 依規格關聯-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格關聯-主畫面 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本區塊</p>

    * STD</br>
        ![pic][image_fieldbreak1_STD]
    * MAE</br>
        ![pic][image_fieldbreak1_MAE]
    * `(1)表單名稱`
        * 用途說明
        * 規格說明
            * [使用多語詞庫通則][link_ruledialog2], 回傳:表單多語料號, 顯示:多語詞彙
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示傳入的表單料號
    * `(3)表單類型`
        * 用途說明
        * 規格說明
            * 選項 一頁單筆(單筆)/一頁多筆(多筆)/單頭一身多筆型(雙檔)/多頭單身多筆型(雙多筆)/過濾條件查詢(條件多筆)/指定條件執行(單改)/指定條件修改(雙改)/樞紐表單
            * 當 [新增表單/報表][link_AddFormReport_fieldbreak1](n)設計類型=RWD, 選項 指定條件修改(雙改)/樞紐表單 隱藏
            * 當 [新增表單/報表][link_AddFormReport_fieldbreak1](n)設計類型=APP, 選項 單頭一身多筆型(雙檔)/多頭單身多筆型(雙多筆)/指定條件修改(雙改)/樞紐表單 隱藏
    * `(4)記錄內容`
        * 用途說明
        * 規格說明
            * 選項 最首筆/最末筆/空白頁, 預設: 最首筆
    * `(5)資料重顯時間`
        * 用途說明
        * 規格說明
            * 當 [新增表單/報表][link_AddFormReport_fieldbreak1](n)設計類型=APP, 隱藏
    * `(6)資料重顯時間_分`
        * 用途說明
        * 規格說明
            * `(5)資料重顯時間`為未勾選, 除能
            * 選項 00~60; `(5)資料重顯時間`為已勾選, 預設 00
            * 當 [新增表單/報表][link_AddFormReport_fieldbreak1](n)設計類型=APP, 隱藏
    * `(7)資料重顯時間_秒`
        * 用途說明
        * 規格說明
            * `(5)資料重顯時間`為未勾選, 除能
            * 選項 00~60; `(5)資料重顯時間`為已勾選, 預設 01
            * 當 [新增表單/報表][link_AddFormReport_fieldbreak1](n)設計類型=APP, 隱藏
    * `(8)獨立開啟`
        * 用途說明
            * 表示運行時是否顯示於選單中
        * 規格說明    
            * 預設打勾
    * `(9)連續異動`
        * 用途說明
        * 規格說明     
            * 當`(3)表單類型`= 一頁多筆(多筆)/過濾條件查詢(條件多筆) 時 才致能
            * 當 [新增表單/報表][link_AddFormReport_fieldbreak1](n)設計類型=APP, 隱藏
    * `(10)首頁選單`
        * 用途說明
        * 規格說明
            * 選項 強制開啟/強制關閉
            * 當 [新增表單/報表][link_AddFormReport_fieldbreak1](n)設計類型=APP, 隱藏
    * `(11)錯誤訊息指定元件`
        * 用途說明
        * 規格說明
    * `(12)錯誤訊息元件`
        * 用途說明
        * 規格說明
            * 當`(11)錯誤訊息指定元件`為未勾選, 除能
            * [挑選表單元件通則][link_ruledialog7], 限定:條件如下說明 回傳:表單元件料號, 顯示:表單元件
                * 本表單元件
                * 元件類型=多行文字
                * 僅供顯示為勾選
                * 不可為容器(wCtnr)、多筆表格(wGrd)、多筆瀏覽(wGrdLite)的子元件
    * `(13)記錄異動立即過重載`
        * 用途說明
        * 規格說明
            * 預設為勾選
            * 當 [新增表單/報表][link_AddFormReport_fieldbreak1](n)設計類型=APP, 隱藏
    * `(14)接收參數表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
    * `(15)項次`
        * 用途說明
        * 規格說明
            * 依序給流水號
    * `(16)參數`
        * 用途說明
        * 規格說明
            * 自行輸入
    * `(17)型態`
        * 用途說明
        * 規格說明
            * 選項 文字/數字/日期/邏輯, 預設: 文字
    * `(18)說明`
        * 用途說明
        * 規格說明
            * 自行輸入
    * `(19)料號`
        * 用途說明
        * 規格說明
            * 顯示參數料號
    * `(20)使用時機`
        * 用途說明
        * 規格說明
            * 自行輸入

## <div id="save-action">儲存檢控</div>
* 不允空白，以紅框線標註錯誤的欄位
    * 當 [基本區塊][link_fieldbreak1]`錯誤訊息指定元件`為勾選, 則`錯誤訊息元件`, 不允空白
    * 當 [基本區塊][link_fieldbreak1]`接收參數表格`有記錄, 則`參數`、`型態`, 不允空白
* 其它檢控
    * [基本區塊][link_fieldbreak1]`接收參數表格`記錄中, `參數`, 不允重複

## <div id="other-desc">其它</div>
* 儲存後檢查
    * 當異動表單類型時，需檢查是否需要刪除角色條件表格
        * [基本區塊][link_fieldbreak1]`表單類型`= 過濾條件查詢(條件多筆), 角色條件需附屬於表身1下, 其餘表單類型則附屬於表頭下
* [MAE加註儲存通則][link_ruleother5]

<!-- 圖片 -->
[image_form_STD]:attachment/FormAnnotation_STD.png
[image_form_MAE]:attachment/FormAnnotation_MAE.png
[image_fieldbreak1_STD]:attachment/fieldbreak1_STD.png
[image_fieldbreak1_MAE]:attachment/fieldbreak1_MAE.png

<!-- 超連結 -->
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruledialog2]:../RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruledialog7]:../RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_rulebutton2]:../RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
[link_rulebutton3]:../RulesButton/README#rulebutton3 "共用通則_按鍵操作/操作表格記錄通則"
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本區塊"
[link_ruleother5]:../RulesOther/README#ruleother5 "共用通則_其它/MAE加註儲存通則"
[link_AddFormReport_fieldbreak1]:../AddFormReport/README#fieldbreak1 "新增表單/報表/區塊1"