# 華碩行動辦公雲-更新MDB檔案程式

### <div id="step">維運人員更新步驟</div>
* 至AP Server，使用CURL呼叫本機RTE的進入維護模式API
* 至DB Server，啟動更新MDB檔案程式
    * 挑選行動辦公雲系統安裝MDB檔
    * 挑選行動辦公雲權限安裝MDB檔
    * 指定要更新的組織資料庫清單
    * 執行更新
* 至AP Server，使用CURL呼叫本機RTE的退出維護模式API


### <div id="notice">注意事項</div>
* 權限資料檔更新，目前只支援更新組織資料庫。
* 資料表匯入物件，暫不處理外部資料庫。


### <div id="flowchart">更新MDB檔案程式-作業流程</div>

#### - 介面
![workflow_01]

#### - 解析系統更新檔
![workflow_02]

#### - Parser OBJECT Info
![workflow_03]

#### - 更新共用資料庫
![workflow_04]

#### - 更新組織資料庫
![workflow_05]

#### - 還原組織資料庫
![workflow_06]


[workflow_01]:attachment/workflow_01.png "介面"
[workflow_02]:attachment/workflow_02.png "解析系統更新檔"
[workflow_03]:attachment/workflow_03.png "Parser OBJECT Info"
[workflow_04]:attachment/workflow_04.png "更新共用資料庫"
[workflow_05]:attachment/workflow_05.png "更新組織資料庫"
[workflow_06]:attachment/workflow_06.png "還原組織資料庫"