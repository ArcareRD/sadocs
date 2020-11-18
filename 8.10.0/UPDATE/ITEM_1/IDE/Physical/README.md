### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/16


## <div id="layout">版面相關</div>
* 版面
    * ![pic][image_physical]

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_physical_block1]
    * `(1)鏡像表格來源`
        * 用途說明
            * 意指 恢復連線時，要給MAE上傳用的資料表, 其欄位結構的參考來源
        * 規格說明
            * 系統預設: 未勾選
            * 當`系統表格`為已勾選, 或`(3)離線上傳用表格`為已勾選 , 或`永久保存`=否, 或`歸屬資料庫`=其它, 則 本欄改設為未勾選並除能, 否則 致能
    * `(2)鏡像表格`
        * 用途說明
            * 意指 恢復連線時，要給MAE上傳用的資料表
        * 規格說明
            * 本欄永久除能
            * 當資料表來源為系統產生的離線上傳用資料表，則系統顯示為已勾選
    * `(4)修改`
        * 用途說明
        * 規格說明
            * 當`(2)鏡像表格`為已勾選, 則 除能, 否則 致能
    * `(5)儲存`
        * 用途說明
        * 規格說明
            * 當`(2)鏡像表格`為已勾選, 則 除能, 否則 致能
            * 當`(1)鏡像表格來源`為已勾選, 依對應的鏡像表格是否存在 + 欄位結構, 決定是否新增或修改鏡像表格
                * 須符合下列欄位產生條件
                    * 欄位清單中`個資加密`為已勾選, 或`密碼處理`為已勾選的欄位, 不產生
                    * 當`序號`為已勾選, 產生的欄位, 系統改設為未勾選
                    * 當`鍵值`為已勾選, 產生的欄位, 系統改設定未勾選
                * 原存在頁籤:索引定義、初始資料行、主動更新的記錄，皆不產生
                * 因應恢復離線時，需要進行同步資料交易，由系統產生下列欄位
                    |欄位名 |欄位說明 |型態 |長度 |可變長度 |鍵值 |
                    |------ |-------- |--- |--- |------- |--- |
                    |RURU_OT_BATCHNO |離線批號 |only.全唯碼 |38 | |Y |
                    |RURU_OT_SERIALNO |離線記錄流水號 |int.整數(int) |9 | |Y |
                    |RURU_OT_STATUS |離線異動狀態(A:新增 U:修改 D:刪除) |string.文字 |1 |N |N |
            * 當`(1)鏡像表格來源`為未勾選, 且駐留資料表存在相對應的鏡像表格, 則刪除對應的鏡像表格
        * 作業流程
            * ![pic][image_physical_Save]
    * `(6)刪除`
        * 用途說明
        * 規格說明
            * 當`(2)鏡像表格`為已勾選, 則 除能, 否則 致能
            * 當駐留資料表存在相對應的離線上傳用資料表, 則刪除對應的離線上傳用的資料表
        * 作業流程
            * ![pic][image_physical_Delete]
    * `(7)取消`
        * 用途說明
        * 規格說明
            * 當`(2)鏡像表格`為已勾選, 則 除能, 否則 致能

* <p id="fieldbreak1" style="color:blue;font-weight:bold">欄位清單</p>

    * ![pic][image_physical_block2]
    * `(1)儲存`
        * 用途說明
        * 規格說明
            * 當[基本][link_fieldbreak1]的`鏡像表格`為已勾選, 則 除能, 否則 致能
            * 當[基本][link_fieldbreak1]的`鏡像表格來源`為已勾選, 依本次異動的欄位結構, 修改對應的鏡像表格欄位
                * 須符合下列欄位產生條件
                    * 欄位清單中`個資加密`為已勾選, 或`密碼處理`為已勾選的欄位, 不產生 ; 若之前已產生, 則 刪除
                    * 當欄位`序號`為已勾選, 產生的欄位, 系統改設為未勾選
                    * 當欄位`鍵值`為已勾選, 產生的欄位, 系統改設定未勾選
        * 作業流程
            * ![pic][image_physical_FieldSave]
    * `(2)刪除`
        * 用途說明
        * 規格說明
            * 當[基本][link_fieldbreak1]的`鏡像表格`為已勾選, 則 除能, 否則 致能
            * 當[基本][link_fieldbreak1]的`鏡像表格來源`為已勾選, 且對應的離線上傳用資料表中已產生該欄位, 則 刪除
        * 作業流程
            * ![pic][image_physical_FieldDelete]

## <div id="other-desc">其它說明</div>
* 當 [基本][link_fieldbreak1] 的`鏡像表格`為已勾選, 則下列頁籤所在的功能按鈕 除能, 否則 致能
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
[image_physical_Save]:attachment/Physical-Save.png
[image_physical_Delete]:attachment/Physical-Delete.png
[image_physical_FieldSave]:attachment/Physical-FieldSave.png
[image_physical_FieldDelete]:attachment/Physical-FieldDelete.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本區塊"

[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"