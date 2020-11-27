### <div id="user">規劃人員</div>
* how

### <div id="updatedate">規劃日期</div>
* 2020/11/26

### <div id="trac">TRAC</div>
* <ps>待補</ps> 

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本設定</p>

    * ![pic][image_BasicSetting]
    * `(1)檢視表`
        * 用途說明
        * 規格說明    
            * [挑選檢視表通則][link_ruledialog4], 取得`離線用`未勾選的檢視表

* <p id="fieldbreak2" style="color:blue;font-weight:bold">目的表格</p>

    * ![pic][image_TargetTable]
    * `(1)目的類型`
        * 用途說明
        * 規格說明
            * 選項 專案資料表/系統通行碼/離線任務同步完成
            * `(1)目的類型`=離線任務同步完成, 異動以下相關欄位
                * 清空`(2)目的表格`、`(3)異動方式`, 並除能
                * 清除`(4)判斷條件`下所有記錄, 並預設新增1筆記錄
                * `(5)判斷條件按鍵群`, 除能
        * 作業流程
            * ![pic][image_flow_Posting_Block2_1] <!-- 原始檔案: Posting.drawio/目的表格.目的類型 -->
    * `(2)目的表格`
        * 用途說明
        * 規格說明
            * `(1)目的類型`不為離線任務同步完成, [挑選資料表通則][link_ruledialog3], 取得`離線資料上傳用`未勾選的資料表
    * `(6)比對欄位`
        * 用途說明
        * 規格說明
            * `(1)目的類型`=離線任務同步完成, 選項 批號, 預設 批號
    * `(7)類別`
        * 用途說明
        * 規格說明
            * `(1)目的類型`=離線任務同步完成, 隱藏選項 來源/系統資訊/固定值/運算式, 預設 參數
    * `(8)儲存`
        * 用途說明
        * 規格說明
            * `(1)目的類型`=離線任務同步完成, 須連帶清除[目的欄位][link_fieldbreak3]所有設定內容

* <p id="fieldbrea3" style="color:blue;font-weight:bold">目的欄位</p>

    * ![pic][image_TargetField]
    * `(1)資料表`
        * 用途說明
        * 規格說明    
            * [挑選資料表通則][link_ruledialog3], 取得`離線資料上傳用`未勾選的資料表
    * `(2)表單`
        * 用途說明
        * 規格說明    
            * [挑選表單通則][link_ruledialog3], 取得`離線用`未勾選的表單
    * `(3)目的欄位按鍵群`
        * 用途說明
        * 規格說明
            * [目的表格][link_fieldbreak2]的`(1)目的型態`=離線任務同步完成, 除能

* <p id="fieldbreak4" style="color:blue;font-weight:bold">資料鎖定</p>

    * ![pic][image_DataLock]
    * `(1)鑜定表格`
        * 用途說明
        * 規格說明    
            * [挑選資料表通則][link_ruledialog3], 取得`離線資料上傳用`未勾選的資料表


<!-- 圖片 -->
[image_BasicSetting]:attachment/BasicSetting.png
[image_TargetTable]:attachment/TargetTable.png
[image_TargetField]:attachment/TargetField.png
[image_DataLock]:attachment/DataLock.png
[image_flow_Posting_Block2_1]:attachment/flow_Posting_Block2_1.png

<!-- 超連結 -->
[link_fieldbreak2]:#fieldbreak2 "目的表格"
[link_fieldbreak3]:#fieldbreak3 "目的欄位"
[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_ruledialog4]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"
[link_ruledialog6]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog6 "共用通則_開啟單據/挑選表單通則"