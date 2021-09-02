## <div id="layout">版面相關</div>
* 版面
    * STD <br>
        ![pic][image_wCtnr_STD]
    * RWD <br>
        ![pic][image_wCtnr_RWDAPP]
    * APP <br>
        * 同RWD

## <div id="attributes-object-desc">屬性欄位說明</div>
* ![pic][image_wCtnr_attributes]
* `(1)元件類型`
    * 用途說明
    * 規格說明
        * 依平台語系取得元件類型名稱顯示, 除能, 不可修改
* `(2)元件名稱`
    * 用途說明
    * 規格說明
        * 系統預設: 依平台語系+元件類型, 取得對應的標題名稱顯示, 可修改. Hint: 當使用的多語料號存在, 顯示多語料號
        * 若欄位內容為空值, 跳離欄位後, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 元件名稱不允為空值】, 系統回復上次修改內容
        * 若有修改元件名稱內容, 跳離本欄位後, 異動 標題內容 同 元件名稱內容, 否則 不異動
* `(3)X軸座標`
    * 用途說明
    * 規格說明
        * [座標異動通則][]
* `(4)X軸座標`
    * 用途說明
    * 規格說明
        * [座標異動通則][]
* `(5)高度`
    * 用途說明
    * 規格說明 動通則][link_width_and_height]
        * 若設計類型=APP、RWD, 且元件類型=容器元件(wCtnr), 且`(3)變動高度`=勾選, 則 除能, 否則 致能
* `(6)寬度`
    * 用途說明
    * 規格說明
        * 參照 [元件寬高異動通則][link_width_and_height]
* `(7)滑動方向`
    * 用途說明
    * 規格說明
        * 下拉選項: 上下滑動 / 左右滑動 
        * 系統預設: 上下滑動
* `(8)多欄顯示`
    * 用途說明
    * 規格說明
        * 當設計類型=APP、RWD, 則本欄位隱藏, 否則 顯示
        * checkbox, 系統預設: false
* `(9)資料間距`
    * 用途說明
    * 規格說明
        * 當設計類型=APP、RWD, 則本欄位隱藏, 否則 顯示
        * 系統預設 10, 可修改, 只允輸入數值型態內容, 且不允為負數
        * 若欄位內容為空值, 欄位跳離後, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 資料間距不允為空值】, 系統回復上次修改內容
* `(10)區塊模式`
    * 用途說明
        * 指容器的每一筆記錄為一資料區塊
    * 規格說明
        * 當設計類型=標準, 則 隱藏, 否則 顯示
        * 下拉選項: 磚塊式 / 單列式
        * 系統預設: 單列式
        * 當切換區塊模式=磚塊式時, 異動下列內容:
            * `(11)磚塊寬度`=`(6)寬度`的比率換算成px的值
            * `(12)磚塊高度`=`(5)高度`
            * [樣式欄位說明][link_style_object_desc]的`變動高度`=未勾選
            * 容器下所有子元件對應的`變動高度`=未勾選, 且欄位除能
        * 當切換區塊模式=單列式時, 異動下列內容:
            * [樣式欄位說明][link_style_object_desc]的`變動高度`=勾選
* `(11)磚塊寬度`
    * 用途說明
    * 規格說明
        * 當設計類型=標準, 則 隱藏, 否則 顯示
        * 當`(9)區塊模式`=磚塊式, 則 致能, 否則 除能
* `(12)磚塊高度`
    * 用途說明
    * 規格說明
        * 當設計類型=標準, 則 隱藏, 否則 顯示
        * 當`(9)區塊模式`=磚塊式, 則 致能, 否則 除能
        * 若 異動後磚塊高度 > 原磚塊高度, 異動: 區塊內最後一列的高度 = 原列高 + (異動後磚塊高度-原磚塊高度)
        * 若 異動後磚塊高度 > 原磚塊高度, 且區塊內列的總高度 > 磚塊高度, 顯示 垂直捲軸
        * 若 異動後磚塊高度 > `(5)高度`, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 磚塊高度不得大於容器高度】，系統回復上次修改內容

## <div id="style-object-desc">樣式欄位說明</div>
* ![pic][image_wCtnr_style]
* `(1)自訂樣式`
    * 用途說明
    * 規格說明
        * 參照 [挑選自訂樣式通則][link_style_select], 限定: 元件類型=元件容器, 回傳: 單元樣式名稱
* `(2)變動高度`
    * 用途說明
        * 當為磚塊式, 提供變動高度選擇, 單列式的容器元件一定是變動高度
    * 規格說明
        * 參照 [元件寬高異動通則][link_width_and_height]
        * 當設計類型=APP 或 RWD, 且父階元件類型=元件容器(wCtnr), 且容器的區塊模式=磚塊式, 本欄除能. 系統預設: false
        * 當設計類型=App 或 RWD, 且元件類型=元件容器(wCtnr), 且容器的區塊模式=單列式, 本欄除能. 系統預設: true


## <div id="right-click-function">右鍵功能</div>
* `(1)功能敘述`
    * 用途說明
    * 規格說明
        * 參照 [右鍵功能操作通則][]
* `(2)規格定義`
    * 用途說明
    * 規格說明
        * 參照 [右鍵功能操作通則][]
* `(3)刪除`
    * 用途說明
    * 規格說明
        * 參照 [右鍵功能操作通則][]


<!-- 圖片 -->
[image_wCtnr_STD]:attachment/WidgetBaseProperty_wCtnr_STD.png 
[image_wCtnr_RWDAPP]:attachment/WidgetBaseProperty_wCtnr_RWD&APP.png
[image_wCtnr_attributes]:attachment/WidgetBaseProperty_wCtnr_attributes.png
[image_wCtnr_style]:attachment/WidgetBaseProperty_wCtnr_style.png

<!-- 超連結 -->

[link_attributes_object_desc]:#attributes-object-desc
[link_style_object_desc]:#style-object-desc
[link_style_select]:GeneralRules#style-select
[link_width_and_height]:GeneralRules#width-and-height
