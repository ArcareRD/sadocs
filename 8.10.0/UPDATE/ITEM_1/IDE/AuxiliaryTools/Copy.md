### <div id="user">規劃人員</div>
* how

### <div id="updatedate">規劃日期</div>
* 2020/12/03

### <div id="trac">TRAC</div>
* <ps>待補</ps> 

## <div id="layout">版面</div>
![pic][image_Copy]

## <div id="object-desc">欄位說明</div>
* `(1)複製類別`
    * 用途說明
    * 規格說明
        * 選項 表單/報表/資料交易/離線資料交易/檢視表/資料表
* `(2)複製項目`
    * 用途說明
    * 規格說明
        * `(1)複製類別`=資料表, [挑選資料表通則][link_ruledialog3], 取得`離線資料上傳用`未勾選的資料表
        * `(1)複製類別`=離線資料交易, 開窗[快顯選單][link_Quick], 取得離線資料交易清單, 進行挑選, 回傳離線資料交易名稱
* `(3)全階展開`
    * 用途說明
    * 規格說明
        * `(1)複製類別`=離線資料交易, 展開範圍如下
            * 檢視表 範圍: 來源view、來源view往下正展者
            * 資料表 範圍: 目的實體、鎖定表格、目的欄位中所引用到的實體、上述檢視表往下正展者、排除實體觸發/外檔關聯
        * `(1)複製類別`=表單, 展開範圍如下
            * 資料交易 範圍: 按鍵加註_影響內容所引用到的資料交易
            * 離線資料交易 範圍: 按鍵加註_影響內容所引用到的離線資料交易
            * 檢視表 範圍: 表單加註、元件加註、按鍵加註、資料交易、離線資料交易 所有引用到的檢視表、前者檢視表往下正展者
            * 資料表 範圍: 表單加註、元件加註、按鍵加註、資料交易、離線資料交易 所有引用到的資料表、上述檢視表往下正展者、排除實體觸發/外檔關聯
            * 交換格式 範圍: 按鍵加註_資料交換所引用到的交換格式
* `(4)展開結果`
    * 用途說明
    * 規格說明
        * 若為資料表節點 且 `離線資料上傳用`為勾選的資料表, 則勾選除能
* `(5)複製`
    * 用途說明
    * 規格說明
        * 複製以下本次擴充的單據
            * [資料表][link_Physical]
            * [檢視表][link_Logical]
                * 若`離線資料須上傳`為勾選者, 須連帶產生對應的`離線資料上傳用`為勾選的資料表
            * [離線資料交易][link_OfflinePosting]
            * [新增表單/報表][link_AddFormReport]
            * [按鍵加註_資料交易][link_BAPort]
            * [按鍵加註_資料過濾][link_BAFilter]
* `(6)複製結果`
    * 用途說明
    * 規格說明
        * 擴充呈現離線資料交易複製的結果內容

<!-- 圖片 -->
[image_Copy]:attachment/Copy.png

<!-- 超連結 -->
[link_Quick]:/8.10.0/IDE/Specification/Quick/README "快顯選單"
[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_Physical]:../DataTable/Physical/README "資料表"
[link_Logical]:../DataTable/Logical/README "檢視表"
[link_OfflinePosting]:../DataTable/OfflinePosting/README "離線資料交易"
[link_AddFormReport]:../Home/AddFormReport "新增表單/報表"
[link_BAPort]:../ButtonAnnotation/BAPort "按鍵加註_資料交易"
[link_BAFilter]:../ButtonAnnotation/BAFilter "按鍵加註_資料過濾"