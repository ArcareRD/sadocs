### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2022/03/23

### <div id="trac">TRAC</div>
* #8972

### <div id="requirement">需求展開</div>
* 表單設計版面:
    * 工具列按鍵. 駐留順序, 修正下列規格:
        * <delLine> 修改模式 或 設計類型=APP 隱藏，否則 顯示，開啟<駐留順序>，傳入:專案ID、表單料號、專案語系 </delLine>
        * 版面為編輯模式, 則 隱藏, 否則 顯示, 開啟: [駐留及執行順序][link_WidgetOrder], 限定: 同表單料 且 專案語系=主要語系
    * 詳細規格請查看: [表單設計版面][link_FormDesign]
* 駐留順序:
    * 修改介面標題名: 駐留及執行順序
    * 增加元件類型: 隱藏元件, 並可對其調整駐留順序
    * 按鍵.儲存邏輯, 修正下列規格:
        * <delLine> 先由可設定駐留順序元件開始排列，隱藏元件/隱藏按鍵項目不列入排序 </delLine> 
        * 先由可設定駐留順序元件開始排列, 隱藏按鍵項目不列入排序 
    * 已存在資料: 依現有規則, 取得最後的駐留順序, 並依序增加隱藏元件    
    * 詳細規格請查看: [駐留及執行順序][link_WidgetOrder]
* 新增隱藏元件:
    * 執行按鍵.儲存, 取得專案語系清單, 及表單駐留及執行順序最大號+1, 將隱藏元件新增[駐留及執行順序][link_WidgetOrder] 
    * 詳細規格請查看: [新增隱藏元件][link_AddHiddenObject]
* 影響修改範圍:
    * 規格複製
    * 跨專案複製
    * 表單精靈    


<!-- 超連結 -->
[link_FormDesign]:{3}/IDE/Specification/FormDesign/README "版面設計/表單"
[link_WidgetOrder]:{3}/IDE/Specification/WidgetOrder/README "版面設計/駐留順序"
[link_AddHiddenObject]:{3}/IDE/Specification/AddHiddenObject/README "表單/加註功能/新增隱藏元件"