### <div id="user">規劃人員</div>
* how

### <div id="updatedate">規劃日期</div>
* 2020/11/27

### <div id="trac">TRAC</div>
* <ps>待補</ps> 

## <div id="layout">版面</div>
![pic][image_OAList]

## <div id="object-desc">欄位說明</div>
* `(1)條件式`
    * 用途說明
    * 規格說明
        * [操作條件式通則][link_ruledialog1]
            * 操作單據, 依[新增表單/報表][link_AddFormReport]的`離線用`是否勾選, 影響條件式的相關操作
* `(3)表格名稱`
    * 用途說明
    * 規格說明
        * `(2)對應資料庫`=暫存表格, [挑選資料表通則][link_ruledialog3], 取得`離線資料上傳用`未勾選的資料表
        * `(2)對應資料庫`=檢視表, [挑選檢視表通則][link_ruledialog4]
            * 操作單據, 依[新增表單/報表][link_AddFormReport]的`離線用`為勾選, 則取得`離線用`為勾選的檢視表
            * 否則, 則為未勾選的檢視表

<!-- 圖片 -->
[image_OAList]:attachment/OAList.png

<!-- 超連結 -->
[link_ruledialog1]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_ruledialog4]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"
[link_AddFormReport]:../Home/AddFormReport "新增表單/報表"
