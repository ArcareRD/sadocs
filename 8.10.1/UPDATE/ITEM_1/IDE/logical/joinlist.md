## <div id="layout">結構展開<path>(檢視表)</path></div>

* 版面
  * ![ini]

## <div id="form-action">動作說明</div>

* 說明內容
  * [版面資訊通則](../RulesOther/README.md#ruleother1)
  * [單據異動資料按鍵操作通則](../RulesButton/README#rulebutton2)
  * []內的字串為特定條件下才會顯示
  * 單據編輯狀態請參照[檢視表][index]
## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">結構展開</p>
 
    ![fieldbreak_m2]

  * <t>(1)結構展開清單</t>
    * 用途說明
    * 規格說明:
      * 顯示 `(2)主檢視表` 下的參考來源表格
      * 駐留節點時, 載入`(4)聯結設定區塊`、`(5)資料過濾條件區塊`
  * <t>(2)主檢視表</t>
    * 用途說明:
    * 規格說明:
      * 顯示檢視表名稱
      * 顯示方式為: 預設圖示 + (5.檢視表) + 檢視表名稱 + [(UNION)]
        * UNION: 若鎖定UNION時顯示
        * 解除UNION:![show_logical]
        * 設定UNION:![show_logical_union]
      * 圖示
        * 單擊: 開啟[聯結設定][join]
        * 雙擊: 無作用
        * 右鍵: 開啟右鍵選單`右鍵選單1`
      * 名稱
        * 單擊: 無作用
        * 雙擊: 重載`(1)結構展開清單`
        * 右鍵: 開啟右鍵選單`右鍵選單1`
  * <t id="field3">(3)參考來源表格</t>
    * 用途說明
    * 規格說明: 
      * 顯示方式為: 關聯類型對應圖示 + (來源代號.來源型態) + 來源表格名稱 + (別名) + [(暫存資料表)] +  [(需傳入參數)]
        * 暫存資料表: 若[聯結設定 `暫存資料表`][logalias_astemp]有設定暫存資料表時顯示
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
        * 單擊: 開啟[聯結設定][join]
        * 雙擊: 無作用
        * 右鍵: 開啟右鍵選單`右鍵選單2`
      * 名稱
        * 單擊: 重載 `(4)聯結設定區塊` 、`(5)資料過濾條件區塊`
        * 雙擊: 重載`結構展開清單`
        * 右鍵: 開啟右鍵選單`右鍵選單2`
  * <t>(4)聯結設定區塊</t>
    * 用途說明
    * 規格說明
      * 顯示聯結設定條件, 全唯讀
      * 欄位同[聯結設定 `聯結條件區塊`][logalias_join]
  * <t>(5)資料過濾條件區塊</t>
    * 用途說明
    * 規格說明
      * 顯示過濾條件, 全唯讀
      * 欄位同[條件式][O5]
  * <t>(6)過濾式</t>
    * 用途說明
    * 規格說明
      * 開啟[條件式][O5]
  * <t>(7)刪除過濾式</t>
    * 用途說明
    * 規格說明:[頁面鎖定通則][link_other4]
      * 預設除能
      * 執行限制
        * 當有設定過濾式時致能
      * 檢查檢視表是否被鎖定
        * 被鎖定: 彈出詢問訊息:發生多用戶衝突
          * 重試: 再次檢查檢視表是否被鎖定
          * 取消: 關閉訊息盒
        * 無鎖定:
          * 跳出詢問訊息:是否刪除過濾條件?
            * 確定: 刪除條件式
            * 取消: 關閉訊息盒
    * 作業流程
      * <ps>待補</ps>
  * <t id="menu1">右鍵選單1</t>
    * ![fieldbreak_m3_1] 

    * <t>(1)新增聯結</t>
      * 用途說明: 開啟聯結設定, 可新增參考來源與聯結條件
      * 規格說明:
        * 關閉選單清單
        * 開啟[聯結設定][join]
    * <t>(2)設定UNION</t>
      * 執行限制:
        * 已設定UNION除能
      * 關聯條件中是否有不是UNION的關聯方式(ex. 有設定Left join、right join、inner join...)
        * 無其他關聯方式:
          * 關閉選單清單, 並鎖定關聯條件僅可設定UNION
          * 重顯`(2)主檢視表` 預設圖示 + (5.檢視表) + 檢視表名稱 + (UNION)
        * 有其他關聯方式:
          * 關閉選單清單
          * 顯示訊息盒【標題: 系統訊息 / 設定UNION將清除所有參考來源[`聯結條件`][logalias_join]，是否繼續。 / 按鍵:確定、取消】
            * 確定: 清除所有參考來源[`聯結條件`][logalias_join], 並鎖定聯結條件僅可設定UNION
              * 重顯`(2)主檢視表` 預設圖示 + (5.檢視表) + 檢視表名稱 + (UNION)
            * 取消: 關閉訊息盒
    * <t>(3)解除UNION</t>
      * 執行限制:
        * 已設定UNION致能
      * 關聯條件中是否有UNION的關聯方式
        * 無UNION關聯方式:
          * 關閉選單清單, 並鎖定關聯條件不可設定UNION
          * 重顯`(2)主檢視表` 預設圖示 + (5.檢視表) + 檢視表名稱
        * 有UNION關聯方式:
          * 顯示訊息盒【標題: 系統訊息 / 解除UNION是否一併刪除所有欄位。 / 按鍵:刪除、不刪除、取消】
            * 刪除: 刪除所有欄位並鎖定關聯條件不可設定UNION
              * 重顯`(2)主檢視表` 預設圖示 + (5.檢視表) + 檢視表名稱
            * 不刪除: 保留所有欄位, 清除欄位資料內容並鎖定關聯條件不可設定UNION
              * 重顯`(2)主檢視表` 預設圖示 + (5.檢視表) + 檢視表名稱
            * 取消: 關閉訊息盒
    
  * <t id="menu2">右鍵選單2</t>
    * ![fieldbreak_m3_2]
 
    * <t>(1)開啟表格</t>
      * 關閉選單清單
      * [聯結設定 `類別`][logalias_askind]
        * 檢視表: 由[檢視表 `檢視表頁籤`][log_tab]開啟
        * 資料表: 開啟[欄位結構](#fieldbreak4)
    * <t>(2)設定聯結</t>      
      * 關閉選單清單
      * 開啟[聯結設定][join], 並載入參考來源表格聯結資訊
    * <t>(3)刪除聯結</t>
      * 關閉選單清單
      * 顯示訊息盒【標題: 系統訊息 / 即將刪除參考來源，是否繼續。 / 按鍵:刪除、刪除但保留欄位、取消】
        * 刪除: 刪除聯結設定、過濾條件、參考來源引用該表格的欄位
        * 刪除但保留欄位: 刪除聯結設定、過濾條件；清除參考來源引用該表格的[欄位清單 `資料內容`][logcols_data]
        * 取消: 關閉訊息盒
* <p id="fieldbreak4" style="color:blue;font-weight:bold">欄位結構</p>
    
    ![fieldbreak_m4]  

    * <t>(1)欄位清單區塊</t>
      * 用途說明
      * 規格說明:
        * 僅供顯示無編輯功能
        * 一頁最多十筆
    * <t>(2)欄位名</t>
      * 用途說明
      * 規格說明:
        * 顯示資料表欄位名稱
    * <t>(3)欄位名(DB)</t>
      * 用途說明
      * 規格說明:
        * 顯示資料表結構命名
    * <t>(4)資料型態</t>
      * 用途說明
      * 規格說明
        * 顯示資料表資料型態名稱:位元 / 文字 / 整數 (bigint) / 整數 (int) / 整數 (smallint) / 整數 (tinyint) / 數字/ 日期 / 日期時間 / 備註 / 二進位 / 全唯碼 
    * <t>(5)長度</t>
      * 用途說明
      * 規格說明
        * 顯示資料表欄位長度
          * 有小數位: 長度.小數位數
          * 無小數位: 長度
    * <t>(6)允許空值</t>
      * 用途說明
      * 規格說明:
        * 顯示空值否
    * <t>(7)鍵值否</t>
      * 用途說明
      * 規格說明
        * 顯示鍵值否
    * <t>(8)說明</t>
      * 用途說明
      * 規格說明
        * 顯示 [序號] / [個資加密] / [密碼] / [檔案唯一號]
        * 序號: 當是否為序號有勾選時顯示
        * 個資加密: 當個資加密有勾選時顯示
        * 密碼: 當密碼處理有勾選時顯示
        * 檔案唯一號: 當檔案唯一號有勾選時顯示
 
<!-- 圖示_介面 -->
[ini]:attachment/ini_logjoinList.png "[介面]結構展開"
[fieldbreak_m2]:attachment/mark_ini_logjoinview.png "[欄位說明]結構展開"
[fieldbreak_m3_1]:attachment/mark_ini_logjoin_menu1.png "[欄位說明]聯結設定_右鍵選單1"
[fieldbreak_m3_2]:attachment/mark_ini_logjoin_menu2.png "[欄位說明]聯結設定_右鍵選單2"
[fieldbreak_m4]:attachment/mark_ini_logjoin_phydata.png "[欄位說明]結構欄位"
[show_logical]:attachment/show_logical.png "檢視表無設定UNION"
[show_logical_union]:attachment/show_logical_union.png "檢視表有設定UNION"
[join_type_first]:attachment/join_type_first.png "table source"
[join_type_left]:attachment/join_type_left.png "Left Join"
[join_type_right]:attachment/join_type_left.png "Right Join"
[join_type_inner]:attachment/join_type_left.png "Inner Join"
[join_type_full]:attachment/join_type_fullouter.png "Full Join"
[join_type_subselect]:attachment/join_type_sub.png "SubSelect"
[join_type_cross]:attachment/join_type_cross.png "Cross Join"
[join_type_union]:attachment/join_type_union.png "Union" 
<!--連結-->
[index]:./README.md "檢視表主頁"
[join]:./join.md "聯結設定"
[logalias_astemp]:./join?id=field3 "暫存資料表"
[logalias_join]:./join?id=field7 "聯結條件區塊"
[logalias_askind]:./join?id=field2 "類別"
[log_tab]:./README?id=field5 "檢視表頁籤"
[logcols_data]:./columns?id=field31 "資料內容"

[O5]:{4}/IDE/Specification/RulesDialog/README#ruledialog1 "條件式"
[link_other1]:{4}/IDE/Specification/RulesOther/README?id=ruleother9 "共用通則_其他操作/打樣通則"
[link_other2]:{4}/IDE/Specification/RulesOther/README?id=ruleother7 "共用通則_其他操作/儲存檢控_不允空白"
[link_other3]:{4}/IDE/Specification/RulesOther/README?id=ruleother8 "共用通則_其他操作/儲存檢控_其他"
[link_other4]:{4}/IDE/Specification/RulesOther/README?id=ruleother10 "共用通則_其他操作/鎖定通則"
[link_other5]:{4}/IDE/Specification/RulesOther/README?id=ruleother11 "共用通則_其他操作/個資加密通則"