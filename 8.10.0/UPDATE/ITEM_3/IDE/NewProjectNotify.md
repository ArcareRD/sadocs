### <div id="user">規劃人員</div>
* Lucky

### <div id="updatedate">規劃日期</div>
* 2020/11/12

### <div id="trac">TRAC</div>
* #8195

### <div id="projectadd">工廠開案資訊 <path>(需求展開\專案管理)</path></div>
* 版面
  * ![upnotify]

* 欄位說明
  * <t id="btnUpNotify">(1)開案通知</t>
    * 用途說明: 呼叫API 建立發行測試組裝台、運行台相關資訊
    * 規格說明: 
      * 擴充增加傳遞專案名稱的多語資訊, 用來建立多語系的測試運行台、測試組裝台, 規則如下
      | 語系 | 組裝台名稱 | 運行台名稱 |
      | --- | --------- | ---------- |
      | 950(繁體中文) | `對應950的語系內容 + "_組裝台"` | `對應950的語系內容 + "_運行台"` | 
      | 936(簡體中文) | `對應950的語系內容 + "_组装台"` | `對應950的語系內容 + "_运行台"` | 
      | 437(英文) | `對應950的語系內容 + "_AMS"` | `對應950的語系內容 + "_SIT"` | 
      | 1145(西班牙) | `對應950的語系內容 + "_AMS"` | `對應950的語系內容 + "_SIT"` | 

* 作業流程
  * ![UpNotify_Diagram]



<!--圖片-->
[upnotify]:attachment/NewProjectNotify.png "工廠開案資訊"
[UpNotify_Diagram]:attachment/UpNotify_Diagram.png "[作業流程]開案通知"

