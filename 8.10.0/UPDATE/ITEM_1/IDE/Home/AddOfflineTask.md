### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/12/10


## <div id="layout">版面相關</div>
* 版面
    * ![pic][image_AddOfflineTask]

    
## <div id="form-action">動作說明</div>
* 由 [專案架構樹][link_struceure] `工具列_新增`的按鍵選單: 任務, 開啟本單
* 由 [專案架構樹][link_struceure] 駐留節點: 作業流程, 右鍵功能: 新增任務, 開啟本單
* 本單所有欄位, 開單即致能

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

* ![pic][image_AddOfflineTask_Block1]
    * `(1)任務名稱`
        * 用途說明
        * 規格說明
            * 自行輸入
    * `(2)確定`
        * 用途說明
        * 規格說明
            * 新增一筆離線任務後
            * 執行成功後關閉本單, 並回傳`(1)任務名稱`至呼叫端
    * `(3)取消`
        * 用途說明
        * 規格說明
            * 關閉本單


## <div id="save-action">儲存檢控</div>
* 參照 [存回不允空白檢控通則][link_ruleother7]
    * `任務名稱`, 不允空白
* 參照 [存回其它檢控通則][link_ruleother8]
    * 同一專案下, `任務名稱`不允重複
        * 訊息內容: 任務名稱已存在, 請重新命名


<!--圖片 -->
[image_AddOfflineTask]:attachment/AddOfflineTask.png
[image_AddOfflineTask_Block1]:attachment/AddOfflineTask_Block1.png

<!--超連結-->
[link_struceure]:Structure.md
[link_ruleother7]:/8.10.0/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
