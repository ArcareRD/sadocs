### <div id="user">規劃人員</div>
* Lucky

### <div id="updatedate">規劃日期</div>
* 2020/11/11

### <div id="trac">TRAC</div>
* <ps>待開</ps>

### <div id="index">檢視表主頁<path>(需求展開\檢視表)</path></div>
* 版面  
  ![open_logical]
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
      * 開啟[排序依據](#orderby)
  * `(8)接收參數`
    * 用途說明 
    * 規格說明: 
      * 超連結開啟[接收參數](#parameter)
      * 未設定時顯示: 尚未設定
      * 已設定時顯示: (參數型態)參數名稱1、(參數型態)參數名稱2...
  * `(9)結構展開`
    * 用途說明
    * 規格說明: 
      * 開啟檢視表預設駐留該頁籤

* 作業流程
  * 執行按鈕.開啟檢視表
  * ![open_logical_io]
  * 建立檢視表操作流程
  * ![logical_overview_io]

### <div id="joinlist">結構展開<path>(需求展開\檢視表)</path></div>
* 版面
  ![join_logicallist]
* 欄位說明
  * <t id="logaliaslist">(1)結構展開清單</t>
    * 用途說明
    * 規格說明:
      * 顯示 `(2)主檢視表` 下的參考來源表格
      * <ps>注意</ps> 原參考來源若為檢視表者, 還需要再往下展開, 本版本取消該動作
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
        * 雙擊: 重載`結構展開清單`
        * 右鍵: 開啟右鍵選單`(4)主檢視表右鍵選單`
  * <t id="logalias_astbl">(3)參考來源表格</t>
    * 用途說明
    * 規格說明:
      * 顯示方式為: 關聯類型對應圖示 + (來源代號.來源型態) + 來源表格名稱 + (別名) + [(暫存資料表)] +  [(需傳入參數)]
        * 暫存資料表: 若[關聯條件_暫存資料表](#logalias_astemp)有設定過帳前暫存檔時顯示
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
        * <ps>注意</ps> 圖示先暫由網路截圖, 待申請
      * 圖示
        * 單擊: 開啟[關聯條件](#join)
        * 雙擊: 無作用
        * 右鍵: 開啟右鍵選單`(5)參考來源表格右鍵選單`
      * 名稱
        * 單擊: 重載 `(6)關聯條件區塊` 、`(7)過濾條件區塊`
        * 雙擊: 重載`結構展開清單`
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
        * 產生彙總表
          * 開啟[自動彙總](#autogroupby)
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
  * <t id="area_join">(6)關聯條件區塊</t>
    * 用途說明
    * 規格說明:顯示目前 `(1)結構展開清單` 中駐留參考來源表格的關聯條件
  * <t id="area_where">(7)過濾條件區塊</t>
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
  * <t id="logalias_astemp">(8)暫存資料表</t>
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
      * 過帳前暫存檔已改變: 重顯[結構展開_參考來源表格](#logalias_astbl)
        * 勾選: 關聯類型對應圖示 + (來源代號.來源型態) + 來源表格名稱 + (別名) + (過帳前暫存檔) +  [(需傳入參數)]
        * 未勾選: 關聯類型對應圖示 + (來源代號.來源型態) + 來源表格名稱 + (別名) + [(需傳入參數)]
  
* 作業流程
  * 執行按鈕.開啟來源表格
  
  ![join_sourcetable_io]

  * 執行按鈕.開啟傳遞參數

  ![join_param_io]
  
  * 執行按鈕.執行儲存
   
  ![join_save_io]

### <div id="logcols">欄位清單<path>(需求展開\檢視表)</path></div>
* 版面(非UNION) 
  ![logcols]
* 欄位說明
  * <t>(1)資料型態</t>
    * 用途說明:
    * 規格說明: 
      | 單據狀態 | 控制 | 預設值 |
      | ------- | ---- | ----- |
      | 瀏覽模式 | 致能 | 依據資料 |
      | 編輯模式 | 除能 | 文字 |
      * 切換資料型態, 改變`(2)IsNull`可設定狀態
    | 型態 | 控制 | 資料 |
    | ---- | --- | --- |
    |位元 | 致能 | 不異動 |
    |文字 | 致能 | 不異動 |
    |整數 | 致能 | 不異動 |
    |數字 | 致能 | 不異動 |
    |日期 | 致能 | 不異動 |
    |日期時間 | 致能 | 不異動 |
    |備註 | 致能 | 不異動 |
    |二進位 | 致能 | 不異動 |
    |全唯碼 | 除能 | 清空 |
  * <t>(2)IsNull</t>
    * 用途說明: 快速建立IsNull函數
    * 規格說明:
      | 單據狀態 | 控制 | 預設值 |
      | ------- | ---- | ----- |
      | 瀏覽模式 | 致能 | 依據資料 |
      | 編輯模式 | 除能 | 不勾選 |
  * <t id="colsspecific">(3)特定處理</t>
    * 用途說明
    * 規格說明:
      * 擴充群組彙總(GROUP BY)、平均值(AVG)
      | 單據狀態 | 控制 | 預設值 |
      | ------- | ---- | ----- |
      | 瀏覽模式 | 致能 | 依據資料 |
      | 編輯模式 | 除能 | 無 |

      | 特定處理 | 對應圖示 |
      | --- | --- |
      | 無 | -- |
      | 計數(COUNT) | ![icon_other] |
      | 總和(SUM) | ![icon_other] |
      | 最大值(MAX) | ![icon_other] |
      | 最小值(MIN) | ![icon_other] |
      | 平均值(AVG) | ![icon_other] |
      | 群組彙總(GROUP BY) | ![icon_group] |
      | 特殊語法 | -- |
  * <t>(4)輸出欄位清單</t>
    * 用途說明
    * 規格說明:
      * 顯示方式為: [特定處理圖示] + 欄位名
      * 特定處理對應圖示<ps>(對應圖是為示意圖 待補)</ps>
      | 特定處理 | 對應圖示 |
      | --- | --- |
      | 無 | -- |
      | 計數(COUNT) | ![icon_other] |
      | 總和(SUM) | ![icon_other] |
      | 最大值(MAX) | ![icon_other] |
      | 最小值(MIN) | ![icon_other] |
      | 平均值(AVG) | ![icon_other] |
      | 群組彙總(GROUP BY) | ![icon_group] |
      | 特殊語法 | -- |
  * <t>(5)新增</t>
    * 用途說明: 
    * 規格說明:
      * 執行後[欄位清單](#欄位清單)進入編輯模式(空白頁)
      | 單據狀態 | 控制 |
      | ------- | ---- |
      | 瀏覽模式 | 除能 |
      | 編輯模式 | 致能 |
  * <t>(6)修改</t>
    * 用途說明
    * 規格說明:
      * 執行後[欄位清單](#欄位清單)進入編輯模式(駐留欄位)
      | 單據狀態 | 控制 |
      | ------- | ---- |
      | 瀏覽模式 | 除能 |
      | 編輯模式 | 致能 |
  * <t>(7)儲存</t>
    * 用途說明
    * 規格說明:
      * 執行後[欄位清單](#欄位清單)進入瀏覽模式
      | 單據狀態 | 控制 |
      | ------- | ---- |
      | 瀏覽模式 | 除能 |
      | 編輯模式 | 致能 |
      * 重顯欄位清單      
*  版面(UNION)  
  
  ![logcols_union]
* 欄位說明
  * <t id="logcols_union_data">(1)資料內容區塊</t>
    * 用途說明
    * 規格說明:
      * 依據[結構展開](#logaliaslist) `結構展開清單`中, UNION表格數自動產生n筆資料
  * <t>(2)別名</t>
    * 用途說明: 顯示別名資訊
    * 規格說明:
  * <t>(3)資料內容</t>
    * 用途說明
    * 規格說明: 開啟開窗[運算式][link_expression], 限定:無查表功能
  * <t>(4)儲存</t>
    * 用途說明
    * 規格說明:
      * 檢查資料內容都必須有值
* 作業流程
  * 執行按鈕.新增
  
  ![logcols_add_io]

  * 執行按鈕.修改

  ![logcols_modi_io]

  * 執行按鈕.儲存

  ![logcols_save_io]

### <div id="parameter">接收參數<path>(需求展開\檢視表)</path></div>
* 版面

  ![parameter]

* 說明:原頁簽設定改為彈出視窗
* 欄位說明
  * <t>(1)接收參數表格區塊</t>
    * 用途說明
    * 規格說明:  
  * <t>(3)儲存</t>
    * 用途說明
    * 規格說明:
* 作業流程
  * 執行按鈕.儲存
  
  ![parameter_save_io]

### <div id="orderby">排序依據<path>(需求展開\檢視表)</path></div>
* 版面

  ![orderby]

* 說明:原頁簽設定改為彈出視窗
* 欄位說明
  * <t>(1)儲存</t>
    * 用途說明
    * 規格說明:
      * 點擊執行排序順序存回。
  * <t>(2)取消</t>
    * 用途說明
    * 規格說明:
      * 關閉排序依據單據
      * 檢視表單據狀態為瀏覽狀態時，除能
  * <t>(3)新增</t>
    * 用途說明
    * 規格說明:
      * 開啟[挑選檢視表元件通則][link_ruledialog8] 過濾:已挑選順序欄位, 帶回欄位名稱並附加到`(9)排序欄位清單`最後一筆
  * <t>(4)移至頂端</t>
    * 用途說明
    * 規格說明:
      * 將目前鎖定的欄位移至最頂端；若有多個鎖定欄位，依鎖定欄位順序排序後，移至最頂端
  * <t>(5)向上移動</t>
    * 用途說明
    * 規格說明:
      * 將目前鎖定的欄位向上移一個元件；若有多個鎖定欄位，依鎖定欄位順序排序後，取得鎖定欄位中最小順序向上移一個欄位(若最小順序已是第一個欄位則不再變動順序)
  * <t>(6)向下移動</t>
    * 用途說明
    * 規格說明:
      * 將目前鎖定的欄位向下移一個元件；若有多個鎖定欄位，依鎖定欄位順序排序後，取得鎖定欄位中最大順序向下移一個欄位(若最大順序已是第後一個欄位則不再變動順序)
  * <t>(7)移至最後</t>
    * 用途說明
    * 規格說明:
      * 將目前鎖定的欄位移至最底端；若有多個鎖定欄位，依鎖定欄位順序排序後，移至最底端
  * <t>(8)取消鎖定</t>
    * 用途說明
    * 規格說明: 
      * 將所有已鎖定的圖示，變動為未鎖定圖示
  * <t>(9)排序欄位清單</t>
    * 用途說明
    * 規格說明:
      * 顯示排序欄位清單資訊
  * <t>(10)順序</t>
    * 用途說明
    * 規格說明:
      * 顯示排序順序
  * <t>(11)鎖定/解鎖鍵</t>
    * 用途說明
    * 規格說明:
      * 顯示在欄位名稱前方
      * 未鎖定圖示: ![orderby_unlock]
      * 已鎖定圖示: ![orderby_lock]
  * <t>(12)欄位名稱區塊</t>
    * 用途說明
    * 規格說明: 
      * 單擊欄位名稱區塊，改變鎖定/解鎖鍵狀態，並將區塊底色改為灰色
      * 已鎖定:將圖示改為未鎖定
      * 未鎖定:將圖示改為已鎖定
      * 滑鼠滑入時指標改為(move ![orderby_move])，框線顏色改為藍色, 移出後恢復原本設定
      * 滑鼠單擊可將欄位名稱區塊拖動到新位置；若有多個鎖定欄位，依鎖定欄位順序排序後移至新位置
  * <t>(13)刪除</t>
    * 用途說明
    * 規格說明:
      * 刪除指定欄位
  * <t>(14)排序類型</t>
    * 用途說明: 設定昇冪/降冪
    * 規格說明:
      * 預設:昇冪
      * 昇冪:將圖示改為降冪 ↓
      * 降冪:將圖示改為昇冪 ↑
* 作業流程
  * 執行按鍵.新增

  ![orderby_add_io]

  * 執行按鍵.刪除

  ![orderby_remove_io]

  * 執行按鍵.儲存

  ![orderby_save_io]

  * 執行按鍵.取消

  ![orderby_cancel_io]

### <div id="autogroupby">自動彙總<path>(需求展開\檢視表)</path></div>
* 版面

  ![autogroupby]
* 欄位說明
  * <t>(1)確定</t>
    * 用途說明
    * 規格說明:
      * 檢查欄位清單中`(5)特定處理` 必須設定
      * 顯示訊息盒【標題: 系統訊息 / 將自動產生群組彙總檢視表，是否繼續。 / 按鍵:確定、取消】
      * 依據設定產生群組彙總檢視表。
      * 檢視表命名: `來源檢視表名稱 + "_彙總" + [流水號]`
        * 流水號:如有檢視表名稱重複則依序添加流水號
  * <t>(2)取消</t>
    * 用途說明
    * 規格說明:
      * 關閉自動群組彙總單據
      * 檢視表單據狀態為瀏覽狀態時，除能  
  * <t>(3)欄位清單區塊</t>
    * 用途說明
    * 規格說明:
      * 顯示檢視表所有欄位
  * <t>(4)欄位名稱</t>
    * 用途說明
    * 規格說明: 
      * 顯示欄位名稱
  * <t>(5)特定處理</t>
    * 用途說明: 設定彙總函數類型, 設定為無時則彙總檢視表不產生該欄位
    * 規格說明: 下拉選項: 無 / 計數(COUNT) / 總合(SUM) / 最大值(MAX) / 最小值(MIN) / 平均值(AVG) / 群組彙總(GROUP BY), 預設值:無    
* 作業流程
  * 執行按鍵.確定
  
  ![autogroupby_sent_io]

  * 執行按鍵.取消  
  
  ![autogroupby_cancel_io]

<!-- 圖片-->
[logical_overview_io]:attachment/Logical_overview_Diagram.png "[作業流程]建立檢視表操作概觀"
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
[join_sourcetable_io]:attachment/join_sourcetable_io.png "[作業流程]關聯條件開啟表格"
[join_param_io]:attachment/join_param_io.png "[作業流程]關聯條件開啟傳遞參數"
[join_save_io]:attachment/join_save_io.png "[作業流程]關聯條件存回"
[logcols]:attachment/logcols.png "欄位清單"
[logcols_union]:attachment/logcols_union.png "欄位清單 union"
[icon_group]:attachment/colsspecific_icon_group.png "Group by icon"
[icon_other]:attachment/colsspecific_icon_other.png "彙總函式 by icon"
[logcols_add_io]:attachment/logcols_add_io.png "[作業流程]欄位清單_新增"
[logcols_modi_io]:attachment/logcols_modi_io.png "[作業流程]欄位清單_修改"
[logcols_save_io]:attachment/logcols_save_io.png "[作業流程]欄位清單_儲存"
[parameter]:attachment/parameter.png "接收參數"
[orderby]:attachment/orderby.png "排序依據"
[autogroupby]:attachment/autogroupby.png "自動彙總"
[orderby_unlock]:attachment/orderby_unlock.png "未鎖定圖示"
[orderby_lock]:attachment/orderby_lock.png "已鎖定圖示"
[orderby_move]:attachment/orderby_move.png "移動圖示"
[parameter_save_io]:attachment/parameter_save_io.png "[作業流程]接收參數_儲存"
[orderby_add_io]:attachment/orderby_add_io.png "[作業流程]排序依據_新增"
[orderby_remove_io]:attachment/orderby_remove_io.png "[作業流程]排序依據_刪除"
[orderby_cancel_io]:attachment/orderby_cancel_io.png "[作業流程]排序依據_取消"
[orderby_save_io]:attachment/orderby_save_io.png "[作業流程]排序依據_儲存"
[autogroupby_cancel_io]:attachment/autogroupby_cancel_io.png "[作業流程]自動彙總_取消"
[autogroupby_sent_io]:attachment/autogroupby_sent_io.png "[作業流程]自動彙總_送出"


<!--Link-->
[link_ruledialog4]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"
[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_ruledialog8]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_expression]:/8.10.0/IDE/Specification/運算式 "共用通則_開啟運算式"
[link_Parameter]: "傳遞參數" "共用通則_開啟傳遞參數"