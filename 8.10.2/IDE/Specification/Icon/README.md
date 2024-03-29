## <div id="layout">版面相關</div>
* 版面</br>
    ![pic][image_icon]
* [版面資訊通則][link_ruleother1]
		
## <div id="form-action">動作說明</div>
* 由各呼叫端開啟 以Dailog on Top 的方式開啟		
* 由 架構節點 開啟, 直接開單, 不執行任何動作		
* [開單搜尋挑選單據動作通則][link_ruleother13]

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">搜尋與其它操作區塊</p>

    ![pic][image_fieldbreak1]
    * `(1)OnlineHelp`
        * 用途說明
        * 規格說明
            * [OnlineHelp通則][link_ruleother2]
    * `(2)搜尋區塊`
        * 用途說明
        * 規格說明
            * [搜尋區塊操作通則][link_rulebutton1]
    * `(3)清單`
        * 用途說明
        * 規格說明
            * 顯示 "表單名稱(按鍵名稱)"
    * `(4)單據異動記錄按鍵群`
        * 用途說明
        * 規格說明
            * [單據異動資料按鍵操作通則][link_rulebutton2]

* <p id="fieldbreak2" style="color:blue;font-weight:bold">設定內容區塊</p>

    ![pic][image_fieldbreak2]
    * `(1)圖示名稱`
        * 用途說明
        * 規格說明
            * [使用多語詞庫通則][link_ruledialog2]
    * `(2)圖示料號`
        * 用途說明
        * 規格說明
            * 顯示系統產生的料號
    * `(3)圖示用途`
        * 用途說明
        * 規格說明
            * 選項 按鍵/樹節點/公司LOGO/表單    
    * `(4)寬度`
        * 用途說明
        * 規格說明
            * 當 (3)圖示用途=樹節點, 預設23, 除能; 其餘可自行輸入
    * `(5)高度`
        * 用途說明
        * 規格說明
            * 當 (3)圖示用途=樹節點, 預設19, 除能; 其餘可自行輸入
    * `(6)圖檔名稱`
        * 用途說明
        * 規格說明
            * 顯示已上傳的檔案名稱
    * `(7)選擇檔案`
        * 用途說明
        * 規格說明
            * 開啟檔案總管挑選圖檔
    * `(8)檢視圖檔`
        * 用途說明
        * 規格說明
            * 當 `(6)圖檔名稱` 不為空白, 才顯示, 否則隱藏
            * 開啟視窗可檢視圖片
    * `(9)檔案下載`
        * 用途說明
        * 規格說明
            * 當 `(6)圖檔名稱` 不為空白, 才顯示, 否則隱藏
            * 可下載圖檔

## <div id="save-action">儲存檢控</div>
* 不允空白, 以紅框線標註錯誤的欄位
    * [設定內容區塊][link_fieldbreak2] `(1)圖示名稱`、`(3)圖示用途`、`(4)寬度`、`(5)高度`
    * [設定內容區塊][link_fieldbreak2] `(7)選擇檔案`、`(6)圖檔名稱`, 則一不允空白
* 其它檢控
    * 檢控圖示寬度的設定與上傳圖檔大小是否符合
        * [設定內容區塊][link_fieldbreak2]`(3)圖示用途`=按鍵
            * 判斷圖檔高度與[設定內容區塊][link_fieldbreak2]`(5)高度`是否相等
            * 判斷圖檔寬度與([設定內容區塊][link_fieldbreak2]`(4)寬度` * 4 是否相同
            * 顯示訊息 "上傳圖檔大小與圖示寬高設定不符(依按鍵圖示原則)"
        * [設定內容區塊][link_fieldbreak2]`(3)圖示用途`=樹節點
            * 判斷圖檔高度與[設定內容區塊][link_fieldbreak2]`(5)高度`是否相等
            * 判斷圖檔寬度是否為38的倍數
            * 顯示訊息 "上傳圖檔大小與圖示寬高設定不符(依樹節點圖示原則)"

<!-- 圖片 -->
[image_icon]:attachment/Icon.png
[image_fieldbreak1]:attachment/fieldbreak1.png
[image_fieldbreak2]:attachment/fieldbreak2.png

<!-- 超連結 -->
[link_fieldbreak2]:#fieldbreak2 "設定內容區塊"
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother2]:../RulesOther/README#ruleother2 "共用通則_其它/OnlineHelp通則"
[link_rulebutton1]:../RulesButton/README#rulebutton1 "共用通則_操作按鍵/搜尋區塊操作通則"
[link_rulebutton2]:../RulesButton/README#rulebutton2 "共用通則_操作按鍵/單據異動資料按鍵操作通則"
[link_ruledialog2]:../RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruleother13]:../RulesOther/README#ruleother13 "共用通則_其它/開單搜尋挑選單據動作通則"