### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/16

## <div id="layout">版面相關</div>
* 版面
    * ![pic][image_physical]

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">資料表主頁</p>

    * ![pic][image_physical_block1]
    * `(1)離線資料上傳用`
        * 用途說明
            * 恢復連線時，MAE上傳用的資料表
        * 規格說明
            * 本欄永久除能
            * 當資料表來源為系統產生的離線資料上傳用資料表，則系統顯示為已勾選

* <p id="fieldbreak2" style="color:blue;font-weight:bold">外檔關聯</p>

    * ![pic][image_physical_block2]
    * `(1)被關聯表格名`
        * 用途說明
        * 規格說明
            * [指定資料表通則][link_ruledialog3], 從本專案中, 挑選資料表, 限定: 取得`離線資料上傳用`未勾選的資料表, 回傳並顯示:資料表名稱


* <p id="fieldbreak3" style="color:blue;font-weight:bold">主動更新</p>

    * ![pic][image_physical_block3]
    * `(1)標的資料表`
        * 用途說明
        * 規格說明
            * [指定資料表通則][link_ruledialog3], 從本專案中, 挑選資料表, 限定: 取得`離線資料上傳用`未勾選的資料表, 回傳並顯示:資料表名稱


## <div id="other-desc">其它說明</div>
* 當 [資料表主頁][link_fieldbreak1] 的`離線資料上傳用`為已勾選, 則下列頁籤所在的功能按鈕 除能, 否則 致能
    * 資料表主頁: 修改、刪除、儲存、取消、結構匯入
    * 欄位清單: 新增、修改、刪除、儲存、取消
    * 外檔關聯: 新增、儲存、刪除、參考來源_新增
    * 索引定義:
        * 主鍵索引清單: 新增鍵值、刪除鍵值、上移、下移、修改排序方式
        * 一般索引清單: 新增、修改、刪除、新增索引、刪除索引、上移、下移、修改排序方式
    * 初始資料行: 新增、修改、刪除、儲存、取消、複製
    * 主動更新: 新增、修改、刪除、儲存、取消、複製

<!-- 圖片 -->
[image_physical]:attachment/physical.png
[image_physical_block1]:attachment/physical-Block1.png
[image_physical_block2]:attachment/physical-Block2.png
[image_physical_block3]:attachment/physical-Block3.png


<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本區塊"

[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"

[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog3 "共用通知_開啟單據/挑選資料表通則"