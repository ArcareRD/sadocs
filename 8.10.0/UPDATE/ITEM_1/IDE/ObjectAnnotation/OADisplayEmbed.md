### <div id="user">規劃人員</div>
* how

### <div id="updatedate">規劃日期</div>
* 2020/11/27

### <div id="trac">TRAC</div>
* <ps>待補</ps> 

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本設定</p>

    * ![pic][image_OADisplayEmbed]
    * `(1)條件式`
        * 用途說明
        * 規格說明
            * [操作條件式通則][link_ruledialog1]
                * 操作單據, 依[新增表單/報表][link_AddFormReport]的`離線用`是否勾選, 影響條件式的相關操作
    * `(2)物件類別`
        * 用途說明
        * 規格說明
             * 操作單據, [新增表單/報表][link_AddFormReport]的`離線用`為勾選, 選項 網頁, 隱藏

* <p id="fieldbreak2" style="color:blue;font-weight:bold">地圖</p>

    * ![pic][image_OADisplayEmbed_map]
    * `(1)來源檢視表`
        * 用途說明
        * 規格說明
            * [挑選檢視表通則][link_ruledialog4], 取得`離線用`為未勾選的檢視表

* <p id="fieldbreak3" style="color:blue;font-weight:bold">圖表</p>

    * ![pic][image_OADisplayEmbed_chart]
    * `(2)來源內容`
        * 用途說明
        * 規格說明    
            * `(1)來源類型`=資料表, [挑選資料表通則][link_ruledialog3], 取得`離線資料上傳用`未勾選的資料表
            * `(1)來源類型`=檢視表, [挑選檢視表通則][link_ruledialog4], 取得`離線用`為未勾選的檢視表

* <p id="fieldbreak4" style="color:blue;font-weight:bold">系統內表單</p>

    * ![pic][image_OADisplayEmbed_form]
    * `(1)表單名稱`
        * 用途說明
        * 規格說明
            * [挑選表單通則][link_ruledialog6], 取得[新增表單/報表][link_AddFormReport]的`設計類型`不為APP的表單
    * `(2)來源檢視表`
        * 用途說明
        * 規格說明
            * [挑選檢視表通則][link_ruledialog4], 取得`離線用`為未勾選的檢視表

* <p id="fieldbreak5" style="color:blue;font-weight:bold">檔案容器控制</p>

    * ![pic][image_OADisplayEmbed_fileContainer]
    * `(2)來源表格`
        * 用途說明
        * 規格說明
            * `(1)查表類別`=資料表, [挑選資料表通則][link_ruledialog3], 取得`離線資料上傳用`未勾選的資料表
            * `(1)查表類別`=檢視表, [挑選檢視表通則][link_ruledialog4]
                * 操作單據, 依[新增表單/報表][link_AddFormReport]的`離線用`為勾選, 則取得`離線用`為勾選的檢視表
                * 否則, 則為未勾選的檢視表
    * `(3)條件式`
        * 用途說明
        * 規格說明
            * [操作條件式通則][link_ruledialog1]
                * 操作單據, 依[新增表單/報表][link_AddFormReport]的`離線用`是否勾選, 影響條件式的相關操作
    * `(4)表格類型`
        * 用途說明
        * 規格說明
            * 操作單據, [新增表單/報表][link_AddFormReport]的`離線用`為勾選, 選項 資料表, 隱藏; 預設選項 資料表暫存

* <p id="fieldbreak6" style="color:blue;font-weight:bold">行事曆</p>

    * ![pic][image_OADisplayEmbed_fileContainer]
    * `(2)來源表格`
        * 用途說明
        * 規格說明
            * `(1)查表類別`=資料表, [挑選資料表通則][link_ruledialog3], 取得`離線資料上傳用`未勾選的資料表
            * `(1)查表類別`=檢視表, [挑選檢視表通則][link_ruledialog4]
                * 操作單據, 依[新增表單/報表][link_AddFormReport]的`離線用`為勾選, 則取得`離線用`為勾選的檢視表
                * 否則, 則為未勾選的檢視表
    * `(3)條件式`
        * 用途說明
        * 規格說明
            * [操作條件式通則][link_ruledialog1]
                * 操作單據, 依[新增表單/報表][link_AddFormReport]的`離線用`是否勾選, 影響條件式的相關操作                

<!-- 圖片 -->
[image_OADisplayEmbed]:attachment/OADisplayEmbed.png
[image_OADisplayEmbed_map]:attachment/OADisplayEmbed_map.png
[image_OADisplayEmbed_chart]:attachment/OADisplayEmbed_chart.png
[image_OADisplayEmbed_form]:attachment/OADisplayEmbed_form.png
[image_OADisplayEmbed_fileContainer]:attachment/OADisplayEmbed_fileContainer.png
[image_OADisplayEmbed_calendar]:attachment/OADisplayEmbed_calendar.png

<!-- 超連結 -->
[link_ruledialog1]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_ruledialog4]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"
[link_ruledialog6]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog6 "共用通則_開啟單據/挑選表單通則"
[link_AddFormReport]:../Home/AddFormReport "新增表單/報表"
