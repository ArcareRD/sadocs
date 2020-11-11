### <div id="user">規劃人員</div>
* Lucky

### <div id="updatedate">規劃日期</div>
* 2020/11/11

### <div id="trac">TRAC</div>
* <ps>待開</ps>

### <div id="index">檢視表主頁<path>(需求展開\檢視表)</path></div>
* 版面
  * ![open_logical]

* 欄位說明
  * `(1)修改檢視表`
    * 用途說明: 改變單據狀態
    * 規格說明
      * 執行後表單進入編輯模式
      | 單據狀態 | 控制 | 預設值 |
      | ------- | ---- | ----- |
      | 瀏覽模式 | 致能 | -- |
      | 編輯模式 | 除能 | -- | 
  * `(2)DISTINCT`
    * 用途說明: 去重覆
    * 規格說明
      | 單據狀態 | 控制 | 預設值 |
      | ------- | ---- | ----- |
      | 瀏覽模式 | 除能 | 依據資料 |
      | 編輯模式 | 致能 | 不勾選 |   
  * `(3)TOP`
    * 用途說明: 限制筆數
    * 規格說明    
      | 單據狀態 | 控制 | 預設值 |
      | ------- | ---- | ----- |
      | 瀏覽模式 | 除能 | 依據資料 |
      | 編輯模式 | 致能 | 不勾選 |    
  * `(4)筆數`
    * 預設 0
    | 單據狀態 | 控制 | 預設值 |
    | ------- | ---- | ----- |
    | 瀏覽模式 | 除能 | 依據資料 |
    | 編輯模式 | 當`(3)TOP`勾選時致能 | 0 |
  * `(5)SubSelect`
    * 用途說明: 子查詢
    * 規格說明
      | 單據狀態 | 控制 | 預設值 |
      | ------- | ---- | ----- |
      | 瀏覽模式 | 除能 | 依據資料 |
      | 編輯模式 | 致能 | 不勾選 |  
  * `(6)XML PATH`
    * 用途說明: 多筆資料合併
    * 規格說明
      | 單據狀態 | 控制 | 預設值 |
      | ------- | ---- | ----- |
      | 瀏覽模式 | 除能 | 依據資料 |
      | 編輯模式 | 致能 | 不勾選 |  
  * `(7)排序依據`
    * 用途說明
    * 規格說明
      * 開啟[排序依據]
  * `(8)接收參數`
    * 用途說明 
    * 規格說明: 
      * 開啟[接收參數]
  * `(9)結構展開`
    * 用途說明
    * 規格說明: 
      * 開啟檢視表預設駐留該頁籤

* 作業流程
  * 執行按鈕.開啟檢視表
  * ![open_logical_io]

### <div id="joinlist">結構展開<path>(需求展開\檢視表)</path></div>
* 版面
  * ![join_logicallist]

* 欄位說明
  * `(1)結構展開清單`
    * 用途說明
    * 規格說明:
      * 顯示 `(2)主檢視表` 下的參考來源表格

      <ps>注意</ps> 原參考來源若為檢視表者, 還需要再往下展開, 本版本取消該動作
  * `(2)主檢視表`
    * 用途說明
    * 規格說明: 顯示檢視表名稱
      * 顯示方式為: 預設圖示 + (6.檢視表) + 檢視表名稱 + [(UNION)]
        * UNION: 若鎖定UNION時顯示
        * 解除UNION:![show_logical]
        * 設定UNION:![show_logical_union]
      * 圖示
        * 單擊: 開啟[關聯條件](#join)
        * 雙擊: 無作用
        * 右鍵: 開啟右鍵選單`(4)主檢視表右鍵選單`
      * 名稱
        * 單擊: 無作用
        * 雙擊: 重載結構展開清單
        * 右鍵: 開啟右鍵選單`(4)主檢視表右鍵選單`
  * `(3)參考來源表格`
    * 用途說明
    * 規格說明:
      * 顯示方式為: 關聯類型對應圖示 + (來源代號.來源型態) + 來源表格名稱 + (別名) + [(過帳前暫存檔)] +  [(需傳入參數)]
        * 過帳前暫存檔: 若[關聯條件](#join)`(3)過帳前暫存檔`有設定過帳前暫存檔時顯示
        * 需傳入參數: 若參考來源有設定傳入參數時顯示
      |關聯類型 | 說明 | 對應圖示 |
      | ---- | --- | --- |
      |主表 |第一個表格 | ![join_type_first] |
      |Left Join | 左外部連接 | ![join_type_left] |
      |Right Join | 右外部連接 | ![join_type_right] |
      |Full Join | 全部外部連接 | ![join_type_full] |
      |Inner Join | 內部連接 | ![join_type_inner] | 
      |Cross Join | 交叉連接 | ![join_type_cross] |
      |Union | 聯集 | ![join_type_union] |
      |Sub Select| 子查詢| ![join_type_subselect] |

      <ps>注意</ps> 圖示先暫由網路截圖, 待申請

      * 圖示
        * 單擊: 開啟[關聯條件](#join)
        * 雙擊: 無作用
        * 右鍵: 開啟右鍵選單`(5)參考來源表格右鍵選單`
      * 名稱
        * 單擊: 無作用
        * 雙擊: 重載結構展開清單
        * 右鍵: 開啟右鍵選單`(5)參考來源表格右鍵選單`

  * `(4)主檢視表右鍵選單`
    * 用途說明
    * 規格說明:
      | 單據狀態 | 控制 | 預設值 |
      | ------- | ---- | ----- |
      | 瀏覽模式 | 不開啟選單 | -- |
      | 編輯模式 | 開啟選單 | -- |  
      * 選單項目
        * 新增
          * 開啟[關聯條件](#join)
        * 設定UNION
          * 關聯條件中是否有不是UNION的關聯方式(ex. 有設定Left join、right join、inner join...)
            * 無其他關聯方式:
              * 關閉選單清單, 並鎖定關聯條件僅可設定UNION
              * 重顯`(2)主檢視表` 預設圖示 + (6.檢視表) + 檢視表名稱 + (UNION)
            * 有其他關聯方式:
              * 關閉選單清單
              * 顯示訊息盒【標題: 系統訊息 / 設定UNION將清除所有參考來源[(6)關聯條件區塊]，是否繼續。 / 按鍵:確定、取消】
                * 確定: 清除所有參考來源[(6)關聯條件區塊], 並鎖定關聯條件僅可設定UNION
                  * 重顯`(2)主檢視表` 預設圖示 + (6.檢視表) + 檢視表名稱 + (UNION)
                * 取消: 關閉訊息盒
        * 解除UNION
          * 關聯條件中是否有UNION的關聯方式
            * 無UNION關聯方式:
              * 關閉選單清單, 並鎖定關聯條件不可設定UNION
              * 重顯`(2)主檢視表` 預設圖示 + (6.檢視表) + 檢視表名稱
            * 有UNION關聯方式:
              * 顯示訊息盒【標題: 系統訊息 / 解除UNION是否一併刪除所有欄位。 / 按鍵:刪除、不刪除、取消】
                * 刪除: 刪除所有欄位並鎖定關聯條件不可設定UNION
                  * 重顯`(2)主檢視表` 預設圖示 + (6.檢視表) + 檢視表名稱
                * 不刪除: 保留所有欄位, 清除欄位資料內容並鎖定關聯條件不可設定UNION
                  * 重顯`(2)主檢視表` 預設圖示 + (6.檢視表) + 檢視表名稱
                * 取消: 關閉訊息盒
  * `(5)參考來源表格右鍵選單`
    * 用途說明
    * 規格說明:
      | 單據狀態 | 控制 | 預設值 |
      | ------- | ---- | ----- |
      | 瀏覽模式 | 不開啟選單 | -- |
      | 編輯模式 | 開啟選單 | -- |  
      * 選單項目
        * 開啟
          * 關閉選單清單
          * 參考來源表格類型
            * 檢視表: 由檢視表分頁開啟
            * 資料表: 開啟資料表欄位結構清單
        * 設定
          * 關閉選單清單
          * 開啟[關聯條件](#join), 並載入參考來源表格關聯條件資訊
        * 刪除
          * 關閉選單清單
          * 顯示訊息盒【標題: 系統訊息 / 即將刪除參考來源，是否繼續。 / 按鍵:刪除、刪除但保留欄位、取消】
            * 刪除: 刪除參考來源、關聯條件、過濾條件、參考來源引用該表格的欄位清單
            * 刪除但保留欄位: 刪除參考來源、關聯條件、過濾條件；清除參考來源引用該表格的欄位資料內容
            * 取消: 關閉訊息盒
  * `(6)關聯條件區塊`
    * 用途說明
    * 規格說明:顯示目前 `(1)結構展開清單` 中駐留參考來源表格的關聯條件
  * `(7)過濾條件區塊`
    * 用途說明
    * 規格說明:移除傳遞參數按鈕

* 作業流程
  * 結構展開執行右鍵選單  
  
  ![join_menu_io]

  * 右鍵選單 - 新增
  
  ![menu_add_io]

  * 右鍵選單 - 設定UNION
 
  ![menu_union_io]

  * 右鍵選單 - 解除UNION
 
  ![menu_ununion_io]

  * 右鍵選單 - 開啟
 
  ![menu_open_io]

  * 右鍵選單 - 設定
 
  ![menu_edit_io]

  * 右鍵選單 - 刪除
 
  ![menu_remove_io]

### <div id="join">關聯條件<path>(需求展開\檢視表)</path></div>
* 版面
  * ![join_logical]
  | 單據狀態 | 控制 | 預設值 |
  | ------- | ---- | ----- |
  | 瀏覽模式 | 除了傳遞參數外, 所有按鍵除能 | -- |
  | 編輯模式 | 致能 | -- | 
* 欄位說明
  * `(1)關聯條件`
    * 用途說明
    * 規格說明: 
      * 檢視表類型
        * UNION
        | 關聯條件 | 關聯條件區塊 | 動作 |
        | -------- | ----------- | --- |
        | Left join| 最少一筆 | 關聯條件區塊可新增 | 
        | Right join| 最少一筆 | 關聯條件區塊可新增 | 
        | Full join| 最少一筆 | 關聯條件區塊可新增 | 
        | Inner join| 最少一筆 | 關聯條件區塊可新增 | 
        | Cross join| 不可設定 | 清除關聯條件區塊且不可新增 | 
        | Sub Select| 最少一筆 | 關聯條件區塊可新增 | 

        * 非UNION
        | 關聯條件 | 關聯條件區塊 | 動作 |
        | -------- | ----------- | --- |
        | Union| 不可設定 | 清除關聯條件區塊且不可新增 | 

  * `(2)類別`
    * 用途說明
    * 規格說明: 單選選項 資料表 / 檢視表
      * 切換後需清除`(3)來源表格` 與 `(6)關聯條件區塊`連結內容
  * `(3)來源表格`
    * 用途說明
    * 規格說明: 
      * 依據`(2)類別`
        * 資料表: [指定資料表通則][link_ruledialog3], 從本專案中, 挑選資料表, 回傳並顯示:資料表名稱
        * 檢視表: [指定檢視表通則][link_ruledialog4], 從本專案中, 挑選檢視表, 回傳並顯示:檢視表名稱
      * 改變表格需清除或異動相關設定
        * 需清除`(6)關聯條件區塊`連結內容
  * `(4)傳遞參數`
    * 用途說明
    * 規格說明: 
      * 致能時機: 當`(3)來源表格`有設定接收參數時
      * 開窗[傳遞參數][link_Parameter]
  * `(5)別名`
    * 用途說明
    * 規格說明: 
      * 別名首字必須為英文
  * `(6)關聯條件區塊`  
    * 用途說明
    * 規格說明: 
  * `(8)過帳前暫存檔`
    * 用途說明
    * 規格說明: 
    | 單據狀態 | 控制 | 預設值 |
    | ------- | ---- | ----- |
    | 瀏覽模式 | 除能 | 依據資料 |
    | 編輯模式 | 致能 | 不勾選 |  
  * `(7)儲存`
    * 用途說明
    * 規格說明: 
      * 表格已改變
        * 清除其他參考來源中有連結該表格`(6)關聯條件區塊`的連結欄位
        * 清除[欄位清單]中有挑選該表格欄位的`(n)資料內容`
      * 別名已改變
        * 替換其他參考來源中有連結該表格`(6)關聯條件區塊`的連結來源表格
        * 替換[欄位清單]中有挑選該表格欄位的`(n)資料內容`
      * 過帳前暫存檔已改變: 重顯[結構展開](#joinlist) `(3)參考來源表格`
        * 勾選: 關聯類型對應圖示 + (來源代號.來源型態) + 來源表格名稱 + (別名) + (過帳前暫存檔) +  [(需傳入參數)]
        * 未勾選: 關聯類型對應圖示 + (來源代號.來源型態) + 來源表格名稱 + (別名) + [(需傳入參數)]
  
* 作業流程
  * 執行按鈕.開啟來源表格
  * 執行按鈕.開啟傳遞參數
  * 執行按鈕.執行儲存
  
<!-- 圖片-->
[open_logical]:attachment/open_logical.png "開啟檢視表"
[open_logical_io]:attachment/open_logical_io.png "[作業流程]開啟檢視表"
[join_logicallist]:attachment/join_logicallist.png "結構展開"
[join_menu_io]:attachment/join_menu_io.png "[作業流程]結構展開右鍵選單"
[menu_add_io]:attachment/menu_add_io.png "[作業流程]右鍵選單新增"
[menu_edit_io]:attachment/menu_edit_io.png "[作業流程]右鍵選單設定"
[menu_open_io]:attachment/menu_open_io.png "[作業流程]右鍵選單開啟"
[menu_union_io]:attachment/menu_union_io.png "[作業流程]右鍵選單設定UNION"
[menu_ununion_io]:attachment/menu_ununion_io.png "[作業流程]右鍵選單解除UNION"
[menu_remove_io]:attachment/menu_remove_io.png "[作業流程]右鍵選單刪除"
[join_type_first]:attachment/join_type_first.png "table source"
[join_type_left]:attachment/join_type_left.png "Left Join"
[join_type_right]:attachment/join_type_left.png "Right Join"
[join_type_inner]:attachment/join_type_left.png "Inner Join"
[join_type_full]:attachment/join_type_fullouter.png "Full Join"
[join_type_subselect]:attachment/join_type_sub.png "SubSelect"
[join_type_cross]:attachment/join_type_cross.png "Cross Join"
[join_type_union]:attachment/join_type_union.png "Union" 
[show_logical]:attachment/show_logical.png "檢視表無設定UNION"
[show_logical_union]:attachment/show_logical_union.png "檢視表有設定UNION"
[join_logical]:attachment/join_logical.png "關聯條件"
<!--Link-->
[link_ruledialog4]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"
[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_Parameter]: "傳遞參數" "共用通則_開啟單據/傳遞參數"