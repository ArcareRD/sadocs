## <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/12/4

## <div id="behavior-layout">版面相關</div>

* 版面
    * STD
        * ![pic][image_bafilter_STD]
    * RWD
        * 同STD
    * 離線用APP
        * 同STD
    * APP
        * ![pic][image_bafilter_MAE]

## <div id="behavior-object-desc">欄位說明</div>

* ![pic][image_bafilter_block1]
* `(1)過濾類別`
    * 用途說明
    * 規格說明
        * 單選選項: 過濾來源 / 離線過濾
        * 系統預設選項: 過濾來源
        * 當表單設計類型=APP, 且`離線用`未勾選時, 顯示 單選選項, 否則隱藏 單選選項
* `(2)過濾來源`
    * 用途說明
        * 依資料區來源檢視表設定過濾條件，進行資料過濾
    * 規格說明
        * 當`(1)過濾類別`=過濾來源時, 過濾來源區塊 致能, 否則 除能
* `(3)離線過濾`
    * 用途說明
        * 過濾離線資料下載範圍用
        * 系統依對應的離線任務若不下載資料，則無須
    * 規格說明
        * 當`(1)過濾類別`=離線過濾時, 離線過濾區塊 致能, 否則 除能
* `(4)離線過濾表格`
    * 用途說明
    * 規格說明
        * 參照 [操作表格記錄通則][link_rulebutton3]
* `(5)表格類別`
    * 用途說明
    * 規格說明
        * 下拉選項: 資料表 / 檢視表
        * 異動時清除欄位:`(6)表格名稱`
* `(6)表格名稱`
    * 用途說明
    * 規格說明
        * 參照 [挑選檢視表通則][link_ruledialog4], 從駐留專案中, 進行檢視表挑選, 並限定使用`離線用`為未勾選的檢視表, 回傳並顯示: 檢視表名稱
        * 參照 [挑選資料表通則][link_ruledialog3], 從駐留專案中, 進行資料表挑選, 回傳並顯示: 表格名稱
* `(7)過濾條件`
    * 用途說明
    * 規格說明
        * 參照 [操作條件式通則][link_ruledialog1], 限定使用`(6)表格名稱`的內容, 回傳並顯示: 條件說明
* `(8)儲存過濾內容`
    * 用途說明
        * 儲存本單設定過濾內容
    * 規格說明
        * 系統預設: 未勾選
        * 當未勾選時, 儲存區塊 隱藏
            * 當有勾選時,
                * 儲存區塊 未設定時, 顯示:尚未設定 灰色字體(#aaa)
                * 可超連結開啟 [儲存過濾內容][link_savefilterContent], 關單後顯示:*表格名稱*


## <div id="save-action">儲存檢控</div>
* 參照 [存回不允空白檢控通則][link_ruleother7]
    * 當`離線過濾表格`存在記錄時
        * `表格類別`、`表格名稱`、`過濾條件`, 不允空白
* 參照 [存回其它檢控通則][link_ruleother8]
    * 當`儲存過濾內容`為已勾選, 對應的儲存區塊須有值
        * 訊息內容: 已設定為儲存過濾內容, 但尚未設定儲存過濾內容


<!--圖片 -->
[image_bafilter_STD]:attachment/BAFilter_STD.png
[image_bafilter_MAE]:attachment/BAFilter_MAE.png
[image_bafilter_block1]:attachment/BAFilter_Block1.png

<!-- 超連結 -->
[link_savefilterContent]:BAFilter_SaveFilterContent.md

[link_ruleother7]:/8.10.0/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"

[link_rulebutton3]:/8.10.0/IDE/Specification/RulesButton/README#rulebutton3 "共用通則_按鍵/操作表格記錄通則"

[link_ruledialog1]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_ruledialog4]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"



