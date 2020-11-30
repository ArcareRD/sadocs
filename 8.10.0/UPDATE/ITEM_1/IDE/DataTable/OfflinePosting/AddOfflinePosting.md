### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/26

## <div id="layout">版面相關</div>
* 版面
    * ![pic][image_AddOfflinePosting]


* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 由專案_首頁架構樹, DB08.離線資料交易, 執行右鍵.新增離線資料交易, 或由 [離線資料交易][link_offlineposting] 呼叫開啟, 開啟本單
* 參照 [離線資料交易_搜尋區塊][link_offlineposting_fieldbreak1]的`新增鍵`作業流程

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_AddOfflinePosting_block1]
    * `(1) 資料交易名稱`
        * 用途說明
        * 規格說明
            * 自行輸入
    * `(2) 儲存`
        * 用途說明
        * 規格說明
            * 新增一筆資料交易後, 關閉本單, 並回傳: 資料交易名稱
        * 作業流程
            * ![pig][image_flow_Save]
    * `(3) 關閉`
        * 用途說明
        * 規格說明
            * 關閉本單


## <div id="save-action">儲存檢控</div>
* 參照 [存回不允空白檢控通則][link_ruleother7]
    * `資料交易名稱`, 不允空白

* 參照 [存回其它檢控通則][link_ruleother8]
    * 同一專案下, `資料交易名稱`不可重覆
        * 訊息內容: 資料交易名稱不可重覆


<!--圖片-->
[image_AddOfflinePosting]:attachment/AddOfflinePosting.png
[image_AddOfflinePosting_block1]:attachment/AddOfflinePosting-Block1.png
[image_flow_Save]:attachment/AddOfflinePosting-Save.png


<!--超連結 -->
[link_offlineposting]:README.md
[link_offlineposting_fieldbreak1]:README.md#fieldbreak1

[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:/8.10.0/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
