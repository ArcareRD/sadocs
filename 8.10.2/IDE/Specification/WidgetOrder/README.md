## <div id="layout">版面相關</div>
* 版面<br>
    ![pic][image_widget_order]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 由表單版面、報表版面 以Dailog on Top 的方式開啟
* 開啟時, 即進入編修狀態

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_widget_order_Block1]
    * `(1)元件清單`
        * 用途說明
        * 規格說明
            * 顯示可供設定駐留排序的元件清單
                * 表單: wTP.文字標題, wTF.文字方塊, wTA.多行文字, wDL.下拉選項, wLB.清單選項, wCB.核取方塊, wGrd.多筆表格, wImg.圖片, wTree.樹狀清單, wTab.頁籤區塊, wFrame.框線, wPW.彈出視窗, wPT.2D樞紐, wTBtn.連結框線, wObj.嵌入物件, wCtnr.元件容器, wCanvas.畫布, wDpanel.動態面板, wRBGroup.按鈕群組, wTBBtn.功能按鈕, wTBMenu.功能選單, wGrdLite.多筆瀏覽, wHObj.隱藏元件
                    * 由後端取得元件清單後, 並依"表單Tab順序"、"Y座標"、"X座標"遞增排序顯示於畫面上
                * 報表: rTP.文字標題, rTF.文字方塊, rTA.多行文字, rCB.核取方塊, rFrame.框線, rBC.條碼, rEChart.嵌入圖表, rImg.圖片, rLogo.企業標誌, rGrid.表格, 且無父階元件者
                    * 由後端取得元件清單後, 並依"駐序"遞增排序顯示於畫面上
    * `(2)駐留順序`
        * 用途說明
        * 規格說明
            * 顯示元件駐留順序
    * `(3)元件`
        * 用途說明
        * 規格說明
            * 顯示 "(表單元件/隱藏元件/功能按鍵)元件/按鍵名稱"
            * 滑鼠滑入時指標改為(move ![pic][image_residency_order_cursor] ), 區塊增加藍色陰影並hint顯示元件類型; 移出後恢復原本樣式<br>
                ![pic][image_residency_order_mouse_in]
            * 鎖定/解鎖鍵: (顯示在元件名稱前方)
                * ![pic][image_residency_order_onlock] 未鎖定圖示
                * ![pic][image_residency_order_lock] 已鎖定圖示
                * 單擊元件名稱區塊，改變鎖定/解鎖鍵狀態, 並將區塊底色改為灰色(#e6e6e6)
                    * 已鎖定: 將圖示改為未鎖定
                    * 未鎖定: 將圖示改為已鎖定<br>
                    ![pic][image_residency_order_lock_img]
            * 滑鼠長按, 可將元件拖動到新位置, 若有多個鎖定元件, 則鎖定元件依順序排列至新位置
    * `(4)移至頂端`
        * 用途說明
        * 規格說明
            * 將目前鎖定的元件移至最頂端
            * 若有多個鎖定元件, 則鎖定元件依順序排序後, 移至最頂端
    * `(5)向上移動`
        * 用途說明
        * 規格說明
            * 將目前鎖定的元件向上移一個元件
            * 若有多個鎖定元件, 則鎖定元件依順序排序後, 取得鎖定元件中最小順序向上移一個元件(若最小順序已是第一個元件則不再變動順序)
    * `(6)向下移動`
        * 用途說明
        * 規格說明
            * 將目前鎖定的元件向下移一個元件
            * 若有多個鎖定元件，則鎖定元件依順序排序後, 取得鎖定元件中最大順序向下移一個元件(若最大順序已是第後一個元件則不再變動順序)
    * `(7)移至最後`
        * 用途說明
        * 規格說明
            * 將目前鎖定的元件移至最底端
            * 若有多個鎖定元件, 則鎖定元件依順序排序後, 移至最底端
    * `(8)解除鎖定`
        * 用途說明
        * 規格說明
            * 將所有已鎖定的元件, 圖示變動為未鎖定
    * `(9)重新載入`
        * 用途說明
        * 規格說明
            * 恢復至異動前順序
    * `(10)儲存`
        * 用途說明: 將駐留順序儲存
        * 規格說明
            * 鎖定表單資料 [使用頁面鎖定通則][link_ruleother10]
            * 依下列儲存邏輯, 進行資料存回
                * [權限驗証通則][link_ruleother6]
                * 依`(1)元件清單`中所排列的順序存回
                * 若設定的駐留元件順序有子階順序比父階順序還小者, 會先依對應父階先排, 再排該父階下的子階順序
                    * 擁有子階的元件類型: wGrd.多筆表格, wTab.頁籤區塊, wTabItem.單一頁籤, wDpanel.動態面板, wDpanelItem.單一面版, wRBGroup.按鈕群組, wCtnr.元件容器, wTBMenu.功能選單, wGrdLite.多筆瀏覽, rGrid.表格
                * 元件有子項元件, 寫入顯示順序(DisplayOrder)
                    * 擁有子項的元件類型: wGrd.多筆表格, wRBGroup.按鈕群組, wTab.頁籤區塊, wDpanel.動態面板, wTBMenu.功能選單, wGrdLite.多筆瀏覽
                * 工具列按鍵, 排在最後面
                * 參考範例如下
                    |頁面調整順序|	元件名稱|	父階元件|	計算後順序|
                    |-----------|---------|----------|-------------|                    
                    |1	|多筆表格	|頁籤耳朵1	|2  |
                    |2	|頁籤耳朵1  |		|1  |
                    |3	|文字方塊1	|頁籤耳朵1	|3  |
                    |4	|文字方塊2	|頁籤耳朵1	|4  |
                    |5	|自訂鍵1	|	    |5  |
                    |6	|自訂鍵2    |		|6  |
    * `(11)OnlineHelp`
        * 用途說明
        * 規格說明
            * [OnlineHelp通則][link_ruleother2]
                
<!-- 圖片 -->
[image_widget_order]:attachment/WidgetOrder.png
[image_widget_order_Block1]:attachment/WidgetOrder_Block1.png
[image_residency_order_cursor]:attachment/residency_order_cursor.png
[image_residency_order_mouse_in]:attachment/residency_order_mouse_in.png
[image_residency_order_onlock]:attachment/residency_order_onlock.png
[image_residency_order_lock]:attachment/residency_order_lock.png
[image_residency_order_lock_img]:attachment/residency_order_lock_img.png

<!-- 超連結 -->
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother10]:../RulesOther/README#ruleother10 "共用通則_其它/使用頁面鎖定通則"
[link_ruleother2]:../RulesOther/README#ruleother2 "共用通則_其它/OnlineHelp通則"
[link_ruleother6]:../RulesOther/README#ruleother6 "共用通則_其它/權限驗証通則"