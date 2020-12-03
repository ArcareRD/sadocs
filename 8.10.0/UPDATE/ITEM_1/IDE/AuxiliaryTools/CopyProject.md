### <div id="user">規劃人員</div>
* how

### <div id="updatedate">規劃日期</div>
* 2020/12/03

### <div id="trac">TRAC</div>
* <ps>待補</ps> 

## <div id="layout">版面</div>
![pic][image_CopyProject]

## <div id="object-desc">欄位說明</div>
* `(1)複製項目`
    * 用途說明
    * 規格說明
        * 選項 專案/流程/表單/報表/資料交易/離線資料交易/檢視表/資料表
* `(2)離線資料交易`
    * 用途說明
    * 規格說明
        * 開窗[快顯選單][link_Quick], 取得離線資料交易清單, 進行挑選, 回傳離線資料交易名稱
* `(3)資料表`
    * 用途說明
    * 規格說明
        * [挑選資料表通則][link_ruledialog3], 取得`離線資料上傳用`未勾選的資料表
* `(4)複製`
    * 用途說明
    * 規格說明
        * 展開複製範圍時, 若為表單, 須展離線交易並往下正展
        * 以下說明, `離線資料需上傳`為勾選的檢視表 及 對應的`離線資料上傳用`為勾選的資料表, 兩者父子關係於複製時的規則
            * 當父子表格不存在目的 且 父表格不存在但子表格存在複製範圍時
                * 判斷子表格名稱(去除"_OfflineUploadData")是否存在目的端, 若存在則引用目的端的表格
                * 承上, 若不存在, 複製表格
                    * 資料表名: 去除"_OfflineUploadData"
                    * 資料表英文名: 去除"_OT"
                    * `離線資料上傳用`不勾選
                    * 系統欄位更名
                    |系統欄位名 |更名 |
                    |--------- |---- |
                    |RURU_OT_BATCHNO |XRURU_OT_BATCHNO |
                    |RURU_OT_SERIALNO |XRURU_OT_SERIALNO |
                    |RURU_OT_STATUS |XRURU_OT_STATUS |
            * 當父子表格不存在目的 且 父子表格皆存在複製範圍
                * 同目前複製原則, 皆複製至目的端
            * 當父子表格存在目的
                * 同目前複製原則, 引用目的端的表格
        * 複製以下本次擴充的單據
            * [資料表][link_Physical]
            * [檢視表][link_Logical]
                * 若`離線資料須上傳`為勾選者, 須連帶產生對應的`離線資料上傳用`為勾選的資料表
            * [離線資料交易][link_OfflinePosting]
            * [新增表單/報表][link_AddFormReport]
            * [按鍵加註_資料交易][link_BAPort]
            * [按鍵加註_資料過濾][link_BAFilter]

<!-- 圖片 -->
[image_CopyProject]:attachment/CopyProject.png

<!-- 超連結 -->
[link_Quick]:/8.10.0/IDE/Specification/Quick/README "快顯選單"
[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_Physical]:../DataTable/Physical/README "資料表"
[link_Logical]:../DataTable/Logical/README "檢視表"
[link_OfflinePosting]:../DataTable/OfflinePosting/README "離線資料交易"
[link_AddFormReport]:../Home/AddFormReport "新增表單/報表"
[link_BAPort]:../ButtonAnnotation/BAPort "按鍵加註_資料交易"
[link_BAFilter]:../ButtonAnnotation/BAFilter "按鍵加註_資料過濾"