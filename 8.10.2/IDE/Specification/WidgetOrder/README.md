## <div id="layout">版面相關</div>
* 版面<br>
    ![pic][image_widget_order]

* [版面資訊通則][link_ruleother1]


## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_widget_order_Block1]
    * `(1)儲存`
        * 用途說明: 將駐留順序儲存
        * 規格說明
            * 鎖定表單資料 [鎖定通則][link_pointLock]
            * 儲存中, 顯示訊息盒【標題: 無 / 訊息內容: 駐留順序]儲存中...。】, 直到儲存完成
            * 儲存完成, 顯示訊息盒【標題: 無 / 誱息內容: [駐留及執行順序資料] 儲存完成。】, 限時: 3秒後自動關閉訊息盒
            * 依下列儲存邏輯, 進行資料存回
                * 先由可設定駐留順序元件開始排列, 隱藏元件/隱藏按鍵項目不列入排序
                * 若設定的駐留元件順序有子階順序比父階順序還小者, 會先依對應父階先排在排該父階下的子階順序
                * 可擁有子階的元件類型
                    * "wGrd", "wTab", "wTabItem", "wDpanel", "wRBGroup", "wCtnr", "wTBMenu", "wDpanelItem", "wGrdLite", "rGrid"
                * 子階元件有子項元件顯示順序(DisplayOrder)的元件類型
                    * "wGrd", "wRBGroup", "wTab", "wDpanel", "wTBMenu", "wGrdLite"
                * 參考範例如下
                    |頁面調整順序|	元件名稱|	父階元件|	計算後順序|
                    |-----------|---------|----------|-------------|                    
                    |1	|多筆表格	|頁籤耳朵1	|2  |
                    |2	|頁籤耳朵1  |		|1  |
                    |3	|文字方塊1	|頁籤耳朵1	|3  |
                    |4	|文字方塊2	|頁籤耳朵1	|4  |
                    |5	|自訂鍵1	|	    |5  |
                    |6	|自訂鍵2    |		|6  |
                    |不在畫面調整	|隱藏元件1  |		|null   |
                    |不在畫面調整	|隱藏按鍵1	|	    |null   |
     * `(2)元件清單`
        * 用途說明
        * 規格說明
            * 取得可供設定駐留排序的元件清單
                * 表單: "wTP", "wTF", "wTA", "wDL", "wLB", "wCB", "wGrd", "wImg", "wTree", "wTab", "wFrame", "wPW", "wPT", "wTBtn", "wObj", "wCtnr", "wCanvas", "wDpanel", "wRBGroup", "wTBBtn", "wTBMenu","wGrdLite"、"wHObj"
                    * 由後端取得元件清單後, 並依"表單Tab順序"、"Y座標"、"X座標"遞增排序顯示於畫面上
                * 報表: rTP.文字標題,rTF.文字方塊,rTA.多行文字,rCB.核取方塊,rFrame.框線,rBC.條碼,rEChart.嵌入圖表,rImg.圖片,rLogo.企業標誌,rGrid.表格, 且無父階元件者
                    * 由後端取得元件清單後, 並依"駐序"遞增排序顯示於畫面上
            * 駐留順序區塊:顯示元件駐留順序
                * 滑鼠滑入時指標改為(move ![pic][image_residency_order_cursor] ), 區塊增加藍色陰影並hint顯示元件類型; 移出後恢復原本樣式
                * ![pic][image_residency_order_mouse_in]
            * 元件名稱區塊:
                * 顯示: (表單元件/元件)元件名稱
                * 鎖定/解鎖鍵: (顯示在元件名稱前方)
                    * ![pic][image_residency_order_onlock] 未鎖定圖示(ui:ui-icon-arrowthick-2-n-s)
                    * ![pic][image_residency_order_lock] 已鎖定圖示(ui:ui-icon-locked)
                * 單擊元件名稱區塊，改變鎖定/解鎖鍵狀態, 並將區塊底色改為灰色(#e6e6e6)
                    * 已鎖定: 將圖示改為未鎖定
                    * 未鎖定: 將圖示改為已鎖定
                * ![pic][image_residency_order_lock_img]
                * 滑鼠滑入時指標改為(move ![pic][image_residency_order_cursor] ), 框線顏色改為藍色(box-shadow:#51a4ff 0 0 6px 0;); 移出後恢復原本設定 
                * ![pic][image_residency_order_mouse_in]
                * 滑鼠單擊可將元件名稱區塊拖動到新位置; 若有多個鎖定元件, 依鎖定元件順序排序後移至新位置
                



<!-- 圖片 -->
[image_widget_order]:attachment/WidgetOrder.png
[image_widget_order_Block1]:attachment/WidgetOrder_Block1.png
[image_residency_order_cursor]:attachment/residency_order_cursor.png
[image_residency_order_mouse_in]:attachment/residency_order_mouse_in.png
[image_residency_order_onlock]:attachment/residency_order_onlock.png
[image_residency_order_lock]:attachment/residency_order_lock.png
[image_residency_order_lock_img]:attachment/residency_order_lock_img.png


<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother1]:{3}/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_pointLock]:{3}/IDE/Specification/RulesOther/README# "共用通則_其它/鎖定通則"