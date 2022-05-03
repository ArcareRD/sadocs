## <div id="layout">版面相關</div>
* 版面</br>
    ![pic][image_OADisplayEmbed]
* [版面資訊通則][link_ruleother1]
		
## <div id="form-action">動作說明</div>
* 依規格關聯-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格關聯-主畫面 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;">主畫面區塊</p>

    ![pic](attachment/OADisplayEmbed.png)
    * `(1)物件類別`
        * 用途說明
        * 規格說明
            * 選項 網頁/地圖/影片/圖表/系統內表單/檔案櫃圖檔/檔案容器控制/行事曆
                * 依據表單類型顯示不同選項
                    * [新增表單/報表][link_AddFormReport_fieldbreak1]`設計類型`=STD, 選項 網頁/地圖/影片/圖表/系統內表單/檔案櫃圖檔
                    * [新增表單/報表][link_AddFormReport_fieldbreak1]`設計類型`=RWD, 選項 網頁/地圖/影片/圖表/系統內表單/檔案櫃圖檔/檔案容器控制/行事曆
                    * [新增表單/報表][link_AddFormReport_fieldbreak1]`設計類型`=APP, 選項 網頁/檔案容器控制/行事曆
            * 選項為 [網頁](WebPage)
            * 選項為 [地圖](Map)
            * 選項為 [影片](Movie)
            * 選項為 [圖表](Chart)
            * 選項為 [系統內表單](InSystemForm)
            * 選項為 [檔案櫃圖檔](FileCabinetImage)
            * 選項為 [檔案容器控制](FileContainerControl)
            * 選項為 [行事曆](Calendar)

<!-- 圖片 -->
[image_OADisplayEmbed]:attachment/OADisplayEmbed.png
[image_OADisplayEmbed_block1]:attachment/fieldbreak1_STD.png

<!-- 超連結 -->
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_rulebutton2]:../RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
[link_AddFormReport_fieldbreak1]:../AddFormReport/README#fieldbreak1 "新增表單/報表/區塊1"