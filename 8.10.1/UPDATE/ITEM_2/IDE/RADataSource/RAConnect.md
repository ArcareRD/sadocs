## <div id="layout">版面相關</div>
* 版面
    * ![pic][image_raconnect]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 駐留報表_資料來源, 執行按鍵: 對應元件開啟並顯示本單內容

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_raconnect_block1]
    * `(1)報表名稱`
        * 用途說明
        * 規格說明
            * 本欄位除能
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示前單傳入的報表料號
            * 本欄位除能
    * `(3)報表元件清單_標題顯示`
        * 用途說明
        * 規格說明
            * 當存在尚未對應報表元件的筆數時, 顯示: 未對應:XX
            * 當存在重複對應檔案資料的元件筆數時, 顯示: 重複:XX
    * `(4)報表元件清單_內容`
        * 用途說明
        * 規格說明
            * 顯示報表元件清單，過濾: 駐留報表, 且報表元件類型不存在於【rTP.文字標題、rFrame.框線、rEChart.嵌入圖表、rGrid.表格】
            * 當報表元件有對應到檔案資料的元件時, 以 ←→ 表示連結, 並顯示: 檔案資料的元件名稱 (ex: *報表元件名稱*←→*檔案資料的元件名稱* )
            * 當存在重複對應時, 字體變成粗體
            * 變色顯示, 請參照 [個資加密提示通則][link_ruleother11]
            * 清單列數最高顯示**20**列, 超過出現垂直捲軸
    * `(5)輸出欄位清單`
        * 用途說明
        * 規格說明
            * 顯示 [報表_資料來源][raport_radatasource] 中`資料來源_名稱`的欄位清單
            * 變色顯示, 請參照 [個資加密提示通則][link_ruleother11]
            * 清單列數最高顯示**20**列, 超過出現垂直捲軸
    * `(6)自動對應鍵`
        * 用途說明
        * 規格說明
            * 執行前彈出訊息盒【標題: 系統訊息 / 內容: 確認自動對應"報表元件"與"輸出欄位"相同名稱的項目? / 按鍵: 確認、取消】
                * 確定: 系統執行自動對應，規則如下:
                    * 報表元件已對應到檔案資料的元件時, 不再進行對應
                    * 當[報表_資料來源][raport_radatasource]的`資料來源_類別`=資料表, 查詢同報表元件名稱的輸出欄位名, 且不為個資加密及密碼處理的欄位, 進行連結
                    * 當[報表_資料來源][raport_radatasource]的`資料來源_類別`=檢視表，查詢同報表元件名稱的輸出欄位名, 且不為個資加密且未解密及密碼處理的欄位, 進行連結
                    * 連結完畢, 將結果依`(4)報表元件清單_內容`規格顯示
                * 取消: 關閉訊息盒
        * 動作流程
            * ![pic][image_flow_auto_mapping]
    * `(7)單一連結對應`
        * 用途說明
        * 規格說明
            * 在`(4)報表元件清單_內容`指定駐留任一報表元件, 並同時在`(5)輸出欄位清單`指定駐留任一欄位, 則 致能, 否則 除能
            * 致能時, 執行按鍵進行連結
        * 動作流程
            * ![pic][image_flow_single_mapping]
    * `(8)取消連結對應`
        * 用途說明
        * 規格說明
            * 在`(4)報表元件清單_內容`指定駐留任一報表元件, 且該元件已進行連結, 則 致能, 否則 除能
            * 致能時, 執行按鍵取消已指定的連結
        * 動作流程
            * ![pic][image_flow_calcel_mapping]
    * `(9)儲存`
        * 用途說明
        * 規格說明
            * 將對應結果儲存, 儲存後顯示訊息盒【標題: 系統訊息 / 內容: [元件對應] 儲存完成。】限時顯示: 3秒
            * 訊息盒關閉後，再關閉本單
        * 動作流程
            * ![pic][image_flow_save]
    * `(10)取消`
        * 用途說明
        * 規格說明
            * 關閉本單
        * 動作流程
            * ![pic][image_flow_cancel]

<!-- 圖片 -->
[image_raconnect]:attachment/ReportAnnotation_RAConnect.png
[image_raconnect_block1]:attachment/ReportAnnotation_RAConnect_block1.png

[image_flow_save]:attachment/RAConnectFlow_Save.png
[image_flow_cancel]:attachment/RAConnectFlow_Cancel.png
[image_flow_auto_mapping]:attachment/RAConnectFlow_auto_mapping.png
[image_flow_single_mapping]:attachment/RAConnectFlow_single_mapping.png
[image_flow_calcel_mapping]:attachment/RAConnectFlow_cancel_mapping.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother1]:/8.10.1/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother11]:/8.10.0/IDE/Specification/RulesOther/README#ruleother11 "共用通則_其它/個資加密提示通則"

[raport_radatasource]:README.md
