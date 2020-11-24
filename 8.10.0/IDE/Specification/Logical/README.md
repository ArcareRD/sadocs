## <div id="layout">版面相關</div>

* 版面
  * 檢視表主頁

    ![ini_index]

  * 欄位清單

    ![ini_logcols]

## <div id="form-action">動作說明</div>

* 說明內容
  * [版面資訊通則](../RulesOther/README.md#ruleother1)
  * [單據異動資料按鍵操作通則](../RulesButton/README#rulebutton2)
  
* 作業流程
  * 建立檢視表操作總覽
    * ![flow_overview]
  * 操作各單據按鍵
    * ![diagram_log_button] 

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">檢視表主頁</p>

    ![fieldbreak_m1]

    * <t>(1)查詢</t>
      * 用途說明: 依據輸入關鍵字查詢並顯示檢視表清單
      * 規格說明
        * 依據輸入關鍵字, 取得相似於`(15)表格名稱`和相似於`(16)料號`, 並顯示於 `(4)檢視表清單` 中
      * 作業流程
        * ![log_search]
    * <t>(2)帶回</t>
      * 用途說明: 用於回傳檢視表資訊至前單中
      * 規格說明:
        * 執行限制: 由其他單據開啟時致能
      * 作業流程
        * ![log_return]
    * <t>(3)新增</t>
      * 用途說明: 新增檢視表格
      * 規格說明:
        * 開啟
      * 作業流程
        * ![log_create]
    * <t>(4)檢視表清單</t>
      * 用途說明
      * 規格說明      
    * <t>(5)檢視表頁籤</t>
      * 用途說明
      * 規格說明
    * <t>(6)修改</t>
      * 用途說明: 改變單據狀態
      * 規格說明
        * 執行後表單進入編輯模式
      * 作業流程
        * ![log_modify]
    * <t>(7)存回</t>
      * 用途說明: 儲存檢視表主頁資訊
      * 規格說明:
        * 
      * 作業流程
        * ![log_save]
    * <t>(8)取消</t>
      * 用途說明
      * 規格說明
      * 作業流程
        * ![log_cancel]
    * <t>(9)刪除</t>
      * 用途說明
      * 規格說明
      * 作業流程
        * ![log_delete]
    * <t>(10)檢錯</t>
      * 用途說明
      * 規格說明
      * 作業流程
        * ![log_debugger]
    * <t>(11)表格欄位清單</t>
      * 用途說明
      * 規格說明
      * 作業流程
        * ![log_tablefieldlist]
    * <t>(12)描述</t>
      * 用途說明
      * 規格說明
      * 作業流程
        * ![log_remarks]
    * <t>(13)打樣</t>
      * 用途說明
      * 規格說明
      * 作業流程
        * ![log_prototyping]
    * <t>(14)打樣狀態查詢</t>
      * 用途說明
      * 規格說明
      * 作業流程
        * ![log_prototypingstatus]
    * <t>(15)表格名稱</t>
      * 用途說明
      * 規格說明
      * 作業流程      
    * <t>(16)料號</t>
      * 用途說明
      * 規格說明
    * <t>(17)DISTINCT</t>
      * 用途說明: 去重覆
      * 規格說明
    * <t>(18)TOP</t>
      * 用途說明: 限制筆數
      * 規格說明
    * <t>(19)TOP筆數</t>
      * 用途說明: 限制筆數值
      * 規格說明
        * 預設 0
        * 執行限制:
          * 當`(3)TOP`勾選時致能
    * <t>(20)SubSelect</t>
      * 用途說明: 子查詢
      * 規格說明
    * <t>(21)XML PATH</t>
      * 用途說明: 多筆資料合併
      * 規格說明:
        * 當`(5)SubSelect`勾選時致能
    * <t>(22)排序依據</t>
      * 用途說明
      * 規格說明
        * 單擊開啟[排序依據](#fieldbreak6)
        * 執行限制: 
          * 當`(3)TOP`勾選時致能
          * 當`(5)SubSelect`勾選時致能
      * 作業流程
        * ![log_orderby]
    * <t>(23)接收參數</t>
      * 用途說明
      * 規格說明
        * 超連結開啟[接收參數](#fieldbreak7)
        * 未設定時顯示: 尚未設定
        * 已設定時顯示: (參數型態)參數名稱1、(參數型態)參數名稱2...
      * 作業流程
        * ![log_param]

* <p id="fieldbreak8" style="color:blue;font-weight:bold">新增檢視表</p>
    
    ![fieldbreak_m8]  

    * <t>(1)表格名稱</t>
      * 用途說明
      * 規格說明
      * 作業流程
    * <t>(2)確定</t>
      * 用途說明
      * 規格說明
      * 作業流程 
    * <t>(3)取消</t>
      * 用途說明
      * 規格說明
      * 作業流程

## <div id="save-action">儲存檢控</div>
* 檢控分類
    * 內容說明

<!-- 圖示_介面 -->
[ini_index]:attachment/ini_index.png "[介面]檢視表主頁"
[ini_logcols]:attachment/ini_logcols.png "[介面]欄位清單"
[fieldbreak_m1]:attachment/mark_ini_index.png "[欄位說明]檢視表主頁"
[fieldbreak_m8]:attachment/mark_ini_create_logical.png "[欄位說明]新增檢視表"
<!-- 圖示_作業流程 -->
[flow_overview]:attachment/Diagram_Logical_overview.png "[作業流程]檢視表操作總覽"
[diagram_log_button]:attachment/Diagram_Log_button.png "[作業流程]檢視表各類按鍵操作"
[log_cancel]:attachment/Diagram_Log_cancel.png "[作業流程]檢視表取消"
[log_create]:attachment/Diagram_Log_create.png "[作業流程]檢視表新增"
[log_debugger]:attachment/Diagram_Log_debugger.png "[作業流程]單元檢錯"
[log_delete]:attachment/Diagram_Log_delete.png "[作業流程]檢視表刪除"
[log_modify]:attachment/Diagram_Log_modify.png "[作業流程]檢視表修改"
[log_orderby]:attachment/Diagram_Log_orderby.png "[作業流程]排序依據"
[log_param]:attachment/Diagram_Log_param.png "[作業流程]接收參數"
[log_prototyping]:attachment/Diagram_Log_Prototyping.png "[作業流程]打樣"
[log_prototypingstatus]:attachment/Diagram_Log_PrototypingStatus.png "[作業流程]打樣狀態查詢"
[log_remarks]:attachment/Diagram_Log_Remarks.png "[作業流程]描述"
[log_return]:attachment/Diagram_Log_return.png "[作業流程]帶回"
[log_save]:attachment/Diagram_Log_save.png "[作業流程]檢視表儲存"
[log_search]:attachment/Diagram_Log_search.png "[作業流程]搜尋"
[log_tablefieldlist]:attachment/Diagram_Log_TableFieldList.png "[作業流程]表單欄位清單"


<!-- 超連結 -->