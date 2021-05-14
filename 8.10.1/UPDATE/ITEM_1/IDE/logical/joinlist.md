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
      * 顯示聯結設定條件
      * 欄位同[聯結設定][logalias]的`聯結條件`
  * <t>(5)資料過濾條件區塊</t>
    * 用途說明
    * 規格說明
      * 顯示過濾條件
      * 欄位同[條件式][O5]

  * <t id="menu1">右鍵選單1</t>
    * ![fieldbreak_m3_1] 

    * <t>(1)新增聯結</t>
      * 用途說明: 開啟聯結設定, 可新增參考來源與聯結條件
      * 規格說明:
        * 關閉選單清單
        * 開啟[聯結設定][join]
    * <t>(2)設定UNION</t>
      * 執行限制:
        * 瀏覽模式 或 已設定UNION, 除能
      * 關聯條件中是否有不是UNION的關聯方式(ex. 有設定Left join、right join、inner join...)
        * 無其他關聯方式:
          * 關閉選單清單, 並鎖定關聯條件僅可設定UNION
          * 重顯`(2)主檢視表` 預設圖示 + (5.檢視表) + 檢視表名稱 + (UNION)
        * 有其他關聯方式:
          * 關閉選單清單
          * 顯示訊息盒【標題: 系統訊息 / 設定UNION將清除所有參考來源，是否繼續。 / 按鍵:確定、取消】
            * 確定: 
              * 清除所有參考來源[`聯結設定`][join]的`聯結條件`, 並鎖定`聯結方式`僅可設定UNION
              * 保留所有[欄位清單][logcols]中的欄位, 清除非UNION的`資料內容`
              * 重顯`(2)主檢視表` 預設圖示 + (5.檢視表) + 檢視表名稱 + (UNION)
            * 取消: 關閉訊息盒
    * <t>(3)解除UNION</t>
      * 執行限制:
        * 瀏覽模式 或 非設定UNION, 除能
      * 關聯條件中是否有UNION的關聯方式
        * 無UNION關聯方式:
          * 關閉選單清單, 並鎖定關聯條件不可設定UNION
          * 重顯`(2)主檢視表` 預設圖示 + (5.檢視表) + 檢視表名稱
        * 有UNION關聯方式:
          * 顯示訊息盒【標題: 系統訊息 / 解除UNION是否一併刪除所有欄位。 / 按鍵:刪除、不刪除、取消】
            * 刪除: 
              * 刪除所有[欄位清單][logcols]中的欄位, 並鎖定[`聯結設定`][join]的`聯結方式`不可設定UNION
              * 重顯`(2)主檢視表` 預設圖示 + (5.檢視表) + 檢視表名稱
            * 不刪除: 
              * 鎖定[`聯結設定`][join]的`聯結方式`預設給值 Left Join
              * 保留所有[欄位清單][logcols]中的欄位, 清除UNION的`資料內容`
              * 承上, 非UNION的`資料內容`預設給值 自訂欄位, 依`資料型態`預設給空值
              * 重顯`(2)主檢視表` 預設圖示 + (5.檢視表) + 檢視表名稱
            * 取消: 關閉訊息盒
    
  * <t id="menu2">右鍵選單2</t>
    * ![fieldbreak_m3_2]
 
    * <t>(1)開啟表格</t>
      * 關閉選單清單
      * [聯結設定 `類別`][logalias_askind]
        * 檢視表: 由[檢視表 `檢視表頁籤`][log_tab]開啟
        * 資料表: 開啟[資料表][link_Physical]
    * <t>(2)設定聯結</t>      
      * 關閉選單清單
      * 開啟[聯結設定][join], 並載入參考來源表格聯結資訊
    * <t>(3)刪除聯結</t>
      * 關閉選單清單
      * 顯示訊息盒【標題: 系統訊息 / 即將刪除參考來源，是否繼續。 / 按鍵:刪除、刪除但保留欄位、取消】
        * 刪除: 刪除聯結設定、過濾條件、參考來源引用該表格的欄位
        * 刪除但保留欄位: 刪除聯結設定、過濾條件；清除參考來源引用該表格的[欄位清單][logcols]`資料內容`
        * 取消: 關閉訊息盒
 
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
[logalias_askind]:./join?id=field2 "類別"
[log_tab]:./README?id=field5 "檢視表頁籤"
[logcols]:./columns.md "欄位清單"
[link_Physical]:../Physical/README "資料表"

[O5]:{4}/IDE/Specification/RulesDialog/README#ruledialog1 "條件式"
[link_other1]:{4}/IDE/Specification/RulesOther/README?id=ruleother9 "共用通則_其他操作/打樣通則"
[link_other2]:{4}/IDE/Specification/RulesOther/README?id=ruleother7 "共用通則_其他操作/儲存檢控_不允空白"
[link_other3]:{4}/IDE/Specification/RulesOther/README?id=ruleother8 "共用通則_其他操作/儲存檢控_其他"
[link_other4]:{4}/IDE/Specification/RulesOther/README?id=ruleother10 "共用通則_其他操作/鎖定通則"
[link_other5]:{4}/IDE/Specification/RulesOther/README?id=ruleother11 "共用通則_其他操作/個資加密通則"