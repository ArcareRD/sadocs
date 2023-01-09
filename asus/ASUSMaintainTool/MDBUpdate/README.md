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
* 權限資料檔的更新目前只支援更新組織資料庫。
