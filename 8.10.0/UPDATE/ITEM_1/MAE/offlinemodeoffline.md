#### <div id="offline_mode_offline">功能項目名稱</div>
  * 離線<path>(系統功能)</path>

#### <div id="user">規劃人員</div>
  * Andy

#### <div id="version">版本記錄</div>
  |日期|版本|備註|
  |---|---|---|
  |2020/11/09|v1|初始化|

#### <div id="trac">TRAC</div>
  * [#8188](http://trac.uneec.com/trac/neco/ticket/8188)

#### <div id="specification">規格說明</div>
  * 需求展開
    * 系統功能選項 [(表單畫面 離線功能)](#offline_button)
      * 有離線任務時才顯示
    * 離線任務清單 [(表單畫面 離線任務清單)](#offline_list)
      * 一次只能下載一個任務來使用
    * 離線設定範圍表單 [(表單畫面 離線設定範圍表單)](#offline_range)
      * 需使用者設計(預設為關連資料全部載入)
    * 成功下載資料後即變為離線模式

#### <div id="photo">畫面</div>
  * 表單畫面
    * <p id=offline_button>離線功能</p>
    
      ![Offline Mode offline](./image/offlinemodeoffline.png)

    * <p id=offline_list>離線任務清單</p>
    
      ![Offline Mode offline list](./image/offlinemodeofflinelist.png)

    * <p id=offline_range>離線設定範圍表單(需設計者設計)</p>
    
      ![Offline Mode offline range](./image/offlinemodeofflinerange.png)

    * <p id=offline_range_error>離線設定範圍表單錯誤</p>
    
      ![Offline Mode offline range](./image/offlinemodeofflinerangeerror.png)
    
#### <div id="workflow">作業流程</div>

  ![Offline Mode Workflow Offline](./image/workflow_offline.png)

