## <div id="layout">版面相關</div>

* 版面
  * 結構展開

    ![ini_index]

  * 欄位清單

    ![ini_logcols]

## <div id="form-action">動作說明</div>  
* [版面資訊通則](../RulesOther/README.md#ruleother1)
* [單據異動資料按鍵操作通則](../RulesButton/README#rulebutton2)
* 開啟方式
  * 架構:資料表格-> DB03.檢視表
  * 需要挑選檢視表的各加註內容
* 開單後預設駐留結構展開區塊
* 按鈕操作:
  * 單擊執行動作
* 作業流程
  * 建立檢視表操作總覽
    * ![flow_overview]
  * 操作各單據按鍵
    * ![diagram_log_button] 

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">檢視表框架</p>

    ![fieldbreak_m1-1]

    * <t>(1)左側框架</t>
      * 用途說明: 所有檢視表清單區塊
      * 規格說明:
        * 預設顯示
    * <t>(2)右側框架</t>
      * 用途說明: 開啟檢視表加註頁
      * 規格說明:
    * <t>(3)左側框架_顯示隱藏鍵</t>
      * 用途說明: 顯示隱藏左側框架
      * 規格說明:
        * 單擊功能
          * 左側框架狀態為顯示時, 隱藏左側框架
          * 左側框架狀態為隱藏時, 顯示左側框架
      
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
        * 執行限制:
          * 由其他單據開啟時致能
      * 作業流程
        * ![log_return]
    * <t>(3)新增</t>
      * 用途說明: 新增檢視表格
      * 規格說明:
        * 開啟[新增檢視表](#fieldbreak8)
      * 作業流程
        * ![log_create]
    * <t>(4)檢視表清單</t>
      * 用途說明
      * 規格說明
        * 顯示`(15)表格名稱`
        * 滑鼠移入顯示`(16)料號`
        * 雙擊開啟檢視表, 檢查表格是否存在於`(5)檢視表頁籤`
          * 已存在, 則頁籤切換至相對表格中
          * 未存在, 則由頁籤區塊左邊增加頁籤項目
        * 單擊切換駐留選取欄位
    * <t if='field5'>(5)檢視表頁籤</t>
      * 用途說明
      * 規格說明:
        * 頁籤顯示`(15)表格名稱`
        * 頁籤預設載入結構展開頁面
        * 執行限制
          * 多個頁籤, 頁籤刪除鍵顯示
          * 單一頁籤, 頁籤刪除鍵隱藏
    * <t>(6)修改</t>
      * 用途說明: 改變單據狀態
      * 規格說明:[頁面鎖定通則][link_other4]
        * 檢查檢視表是否被鎖定
          * 被鎖定: 彈出詢問訊息:發生多用戶衝突
            * 重試: 再次檢查檢視表是否被鎖定
            * 取消: 關閉訊息盒
          * 無鎖定: 表單進入編輯模式, 並將編輯中檢視表鎖定
      * 作業流程
        * ![log_modify]
    * <t>(7)存回</t>
      * 用途說明: 儲存檢視表主頁資訊
      * 規格說明:[頁面鎖定通則][link_other4]
        * 檢查檢視表是否被鎖定
          * 被鎖定(本次操作): 
            * 執行[儲存檢控](#save-action)
            * 將本次資料儲存
            * 單據進入瀏覽模式並解除檢視表鎖定
          * 無鎖定、被鎖定(非本次操作): 
            * 彈出錯誤訊息:該單據已被解除鎖定，無法執行。
      * 作業流程
        * ![log_save]
    * <t>(8)取消</t>
      * 用途說明
      * 規格說明:[頁面鎖定通則][link_other4]
        * 單據進入瀏覽模式並解除檢視表鎖定
        * 重新載入檢視表資料
      * 作業流程
        * ![log_cancel]
    * <t>(9)刪除</t>
      * 用途說明
      * 規格說明: [頁面鎖定通則][link_other4]
        * 檢查檢視表是否被鎖定
          * 被鎖定: 彈出詢問訊息:發生多用戶衝突
            * 重試: 再次檢查檢視表是否被鎖定
            * 取消: 關閉訊息盒
          * 無鎖定:
            * 跳出詢問訊息:是否刪除檢視表?
              * 確定: 刪除檢視表, 關閉`(5)檢視表頁籤` 並 重顯 `(11)表格欄位清單`
              * 取消: 關閉訊息盒
      * 作業流程
        * ![log_delete]
    * <t>(10)檢錯</t>
      * 用途說明
      * 規格說明: 
        * 開啟[單元檢錯][O1]
        * 開啟後預設載入檢錯類別為檢視表、檢視表名稱
      * 作業流程
        * ![log_debugger]
    * <t>(11)表格欄位清單</t>
      * 用途說明
      * 規格說明: 
        * 開啟[表格欄位清單][O2]
        * 開啟後預設載入類別為檢視表、檢視表名稱
      * 作業流程
        * ![log_tablefieldlist]
    * <t>(12)描述</t>
      * 用途說明
      * 規格說明:
        * 開啟[規格備註][O3]
        * 開啟後預設載入類型為檢視表、檢視表名稱、檢視表料號
      * 作業流程
        * ![log_remarks]
    * <t>(13)打樣</t>
      * 用途說明
      * 規格說明: 
        * 執行限制
          * 若為範本專案除能
        * 執行[打樣][link_other1]
      * 作業流程
        * ![log_prototyping]
    * <t>(14)打樣狀態查詢</t>
      * 用途說明
      * 規格說明: 開啟[打樣狀態查詢][O4]
      * 作業流程
        * ![log_prototypingstatus]
    * <t id="field15">(15)表格名稱</t>
      * 用途說明
      * 規格說明: 顯示檢視表名稱
      * 作業流程
    * <t>(16)料號</t>
      * 用途說明
      * 規格說明: 顯示檢視表料號
    * <t>(17)DISTINCT</t>
      * 用途說明: 去重覆
      * 規格說明:
        * 預設不勾選
    * <t>(18)TOP</t>
      * 用途說明: 限制筆數
      * 規格說明:
        * 預設不勾選
    * <t>(19)TOP筆數</t>
      * 用途說明: 限制筆數值
      * 規格說明
        * 預設 0
        * 執行限制:
          * 當`(3)TOP`勾選時致能
    * <t>(20)SubSelect</t>
      * 用途說明: 子查詢
      * 規格說明
        * 預設不勾選
    * <t>(21)XML PATH</t>
      * 用途說明: 多筆資料合併
      * 規格說明:
        * 預設不勾選
        * 當`(5)SubSelect`勾選時致能
    * <t>(22)排序依據</t>
      * 用途說明
      * 規格說明
        * 開啟[排序依據](#fieldbreak6)
        * 執行限制:
          * 預設除能
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
    * <t>(24)頁籤.欄位清單</t>
      * 用途說明
      * 規格說明
        * 單擊切換頁面[欄位清單][columns]
    * <t>(25)頁籤.結構展開</t>
      * 用途說明
      * 規格說明
        * 單擊切換頁面[結構展開][joinlist]
* <p id="fieldbreak8" style="color:blue;font-weight:bold">新增檢視表</p>
    
    ![fieldbreak_m8]  

    * <t>(1)表格名稱</t>
      * 用途說明: 用於建立檢視表名稱
      * 規格說明: 
        * 檢查控制
          * 不允空白
          * 不允與同專案下檢視表格名稱重覆
    * <t>(2)確定</t>
      * 用途說明
      * 規格說明
        * 單擊後檢查控制
          * 以下欄位不允空白檢控 [動作通則][link_other2]
            * `(1)表格名稱`  
          * 其它檢控
            * `(1)表格名稱` 不允與同專案下檢視表格名稱重覆
              * 錯誤訊息: 此表格名稱已經使用，請重新命名
        * 儲存完成後關閉單據
      * 作業流程
        * <PS>待補</PS>
    * <t>(3)取消</t>
      * 用途說明
      * 規格說明: 關閉單據

## <div id="save-action">儲存檢控</div>
* 以下欄位不允空白檢控 [動作通則][link_other2]
* 其他檢控 [動作通則][link_other3]
  * 當`(18)TOP`勾選時, `(19)TOP筆數`必須大於0
  * `(15)表格名稱` 不允與同專案下檢視表格名稱重覆
      * 錯誤訊息: 此表格名稱已經使用，請重新命名

<!-- 圖示_介面 -->
[ini_index]:attachment/ini_index.png "[介面]檢視表主頁"
[ini_logcols]:attachment/ini_logcols.png "[介面]欄位清單"
[fieldbreak_m1]:attachment/mark_ini_index.png "[欄位說明]檢視表主頁"
[fieldbreak_m1-1]:attachment/mark_ini_index2.png "[欄位說明]檢視表框架"
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
[columns]:columns "欄位清單"
[joinlist]:joinlist "結構展開"
[link_other1]:{4}/IDE/Specification/RulesOther/README?id=ruleother9 "共用通則_其他操作/打樣通則"
[link_other2]:{4}/RulesOther/README?id=ruleother7 "共用通則_其他操作/儲存檢控_不允空白"
[link_other3]:{4}/RulesOther/README?id=ruleother8 "共用通則_其他操作/儲存檢控_其他"
[link_other4]:{4}/RulesOther/README?id=ruleother10 "共用通則_其他操作/鎖定通則"
[link_other5]:{4}/RulesOther/README?id=ruleother11 "共用通則_其他操作/個資加密通則"
[O1]:../README "單元檢錯"
[O2]:../README "表格欄位清單"
[O3]:../README "規格備註"
[O4]:../README "打樣狀態查詢"