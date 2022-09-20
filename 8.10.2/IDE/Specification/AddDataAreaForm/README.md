## <div id="layout">版面相關</div>
* 版面</br>
    ![pic][image_addDataAreaForm]
* [版面資訊通則][link_ruleother1]
		
## <div id="form-action">動作說明</div>
* 依規格定義-主畫面 結構清單駐留節點 資料來源, 執行按鍵.新增, 進入本單
* 依規格定義-主畫面 結構清單駐留節點 資料區, 執行滑鼠右鍵.新增, 進入本單 

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本區塊</p>

    ![pic][image_fieldbreak1]
    * `(1)資料區`
        * 用途說明
        * 規格說明
            * 下拉選項 表身1/表身2/.../表身9
            * 若單據已有該資料區, 則不顯示該資料區的選項
            * 預設 最小資料區
    * `(2)儲存`
        * 用途說明
        * 規格說明
            * 存回時, 新增本次選取的資料區
            * [權限驗証通則][link_ruleother6]
    * `(3)重設`
        * 用途說明
        * 規格說明
            * `(1)資料區`重新設定為最小資料區

## <div id="save-action">儲存檢控</div>
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
    * 若`(1)資料區`已存在本單, 則顯示訊息 "「資料區」已被使用。"

<!-- 圖片 -->
[image_addDataAreaForm]:attachment/AddDataAreaForm.png
[image_fieldbreak1]:attachment/AddDataAreaForm_block1.png

<!-- 超連結 -->
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother8]:../RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
[link_ruleother6]:../RulesOther/README#ruleother6 "共用通則_其它/權限驗証通則"