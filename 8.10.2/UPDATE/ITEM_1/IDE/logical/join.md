## <div id="layout">聯結設定<path>(檢視表/結構展開)</path></div>

* 版面
  * ![ini]

## <div id="form-action">動作說明</div>

* 說明內容
  * [版面資訊通則](../RulesOther/README.md#ruleother1)
  * [單據異動資料按鍵操作通則](../RulesButton/README#rulebutton2)
  * 單據編輯狀態請參照[檢視表][index]

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak3" style="color:blue;font-weight:bold">聯結設定</p>

    ![fieldbreak_m3]

    * <t>(1)聯結方式</t>
      * 用途說明
      * 規格說明:
        * 下拉選項: Left Join / Right Join / Cross Join / Full Join / Inner Join / Union / Sub Select
        * 當檢視表為設定UNION, 則預設Union並除能, 否則預設 Left Join
      * 作業流程
        * ![flow_joinType]
    * <t id="field2">(2)類別</t>
      * 用途說明
      * 規格說明:
        * 單選選項:資料表 / 檢視表
        * 當切換選項時, 顯示訊息盒【標題: 系統訊息 / 異動類別將清除相關欄位，是否繼續？ / 按鍵:確定、取消】
          * 確定: 清除相關欄位, 並關閉訊息盒
            * `(3)暫存資料表`、`(4)來源表格`、`(5)傳遞參數`、`(14)自訂連結`
            * 當`(12)連結類別` 等於本表欄位時, 清除`(13)連結內容`
          * 取消: 關閉訊息盒
      * 作業流程
        * ![flow_tableType]
    * <t id='field3'>(3)暫存資料表</t>
      * 用途說明
      * 規格說明:
        * 預設除能
        * 執行限制:
          * 當`(2)類別`為資料表時致能
        * 預設不勾選
    * <t>(4)表格名稱</t>
      * 用途說明
      * 規格說明
        * 依據`(2)類別`
          * 資料表: [挑選資料表通則][link_ruledialog3], 從本專案中, 挑選資料表, 回傳並顯示:資料表名稱
          * 檢視表: [挑選檢視表通則][link_ruledialog4], 從本專案中, 挑選檢視表, 回傳並顯示:檢視表名稱
        * 當切換表格時, 顯示訊息盒【標題: 系統訊息 / 異動表格將清除相關欄位，是否繼續？ / 按鍵:確定、取消】
          * 確定: 清除相關欄位, 並關閉訊息盒
            * `(5)傳遞參數`、`(14)自訂連結`
            * 當`(12)連結類別` 等於本表欄位時, 清除`(13)連結內容`
          * 取消: 關閉訊息盒
    * <t>(6)別名</t>
      * 用途說明
      * 規格說明
        * 執行限制:
          * 首字必須為英文字母
          * 最大長度4碼
          * 新增聯結預設
            * 依目前聯結表格的別名, 最大字母加1 (例: A->B, B1->C)
            * 若該表格尚無關連資料時, 預設為A
            * 若最大字母為Z時, 則不預設
    * <t>(7)過濾條件</t>
      * 用途說明
      * 規格說明
        * [操作條件式通則][link_ruledialog1], 限定:資料表/檢視表須同(4)表格名稱已設定的資料表/檢視表, 回傳並顯示:條件說明
        * 當`(4)表格名稱`未設定時, 顯示訊息盒【標題: 系統訊息 / 請選擇表格。 / 按鍵:確定】
          * 確定: 關閉訊息盒
    * <t id="field7">(8)聯結條件區塊</t>
      * 用途說明
      * 規格說明
        * 一頁最多五筆
        * [操作表格記錄通則][link_rulebutton3]
        * 當`(1)聯結方式`為Cross Join、Union時, 區塊下所有欄位與按鍵皆除能
    * <t>(9)連結來源表格</t>
      * 用途說明
      * 規格說明:
        * 下拉 聯結設定`(4)來源表格`清單, 顯示 "(別名)表格名稱"
        * 下拉只顯示小於等於本表別名的表格名稱
          * 例: 本表的別名為C, 則下拉清單只有 A、B、C 三項下拉選項
        * 異動則清空`(10)連結欄位`
      * 作業流程
        * ![flow_sourceType]
    * <t>(10)連結欄位</t>
      * 用途說明
      * 規格說明
        * 依各`(9)連結來源表格`的類別, 挑選欄位
          * 資料表: [挑選資料表元件通則][link_ruledialog5], 排除有設定密碼處理的欄位, 挑選資料表元件, 回傳並顯示:元件名稱
          * 檢視表: [挑選檢視表元件通則][link_ruledialog8], 排除有設定密碼處理的欄位, 挑選檢視表元件, 回傳並顯示:元件名稱
        * 若個資加密有設定者, 須依據[加密規則][link_other5]顯示。
        * 當欄位為個資加密時 且 `(11)條件`不為等於、不等於時, 則清空`(11)條件`
    * <t>(11)條件</t>
      * 用途說明
      * 規格說明:
        * 下拉選項: 大於 / 小於 / 等於 / 大於等於 / 小於等於 / 不等於 / 存在於 / 不存在於 / 相似於
        * 當為個資加密欄位, 下拉選項: 等於 / 不等於
      * 作業流程
    * <t>(12)連結類別</t>
      * 用途說明
      * 規格說明
        * 下拉選項: 本表欄位 / 參數 / 函數 / 固定值 / 運算式
        * 當`(10)連結欄位`為個資加密欄位, 下拉選項: 本表欄位
        * 異動則切換`(13)連結內容`
      * 作業流程
        * ![flow_linkType]
    * <t>(13)連結內容</t>
      * 用途說明
      * 規格說明
        * 連結類別=本表欄位, 依`(4)表格`挑選欄位
          * 資料表: [挑選資料表元件通則][link_ruledialog5], 挑選資料表元件, 回傳並顯示:元件名稱
          * 檢視表: [挑選檢視表元件通則][link_ruledialog8], 排除有設定密碼處理的欄位, 挑選檢視表元件, 回傳並顯示:元件名稱
          * 若`(10)連結欄位`挑選欄位無設定個資加密, 則`(4)表格`的欄位清單且欄位的密碼處理須為無設定
          * 若`(10)連結欄位`挑選欄位有設定個資加密, 則`(4)表格`的欄位清單且欄位的個資加密須設定
          * 若欄位的個資加密有設定，須依據[加密規則][link_other5]顯示。
        * 連結類別=參數, [挑選參數通則][link_ruledialog2], 依本檢視表, 進行參數挑選, 回傳:參數
        * 連結類別=固定值, 自行輸入
        * 連結類別=運算式, 開啟[運算式][link_expression], 限定:無查表功能
    * <t>(14)自訂連結</t>
      * 用途說明
      * 規格說明
        * 開啟[運算式][link_expression], 限定:無查表功能
    * <t>(15)儲存</t>
      * 用途說明
      * 規格說明: [頁面鎖定通則][link_other4]
        * 瀏覽模式下開啟本單, 除能
        * 檢查檢視表是否被鎖定
          * 被鎖定(本次操作): 
              * 執行[儲存檢控](#save-action)
              * 處理以下異動
                * `(4)表格`已改變
                  * 清除其他參考來源中有聯結該表格`(8)聯結條件區塊`的`(10)連結欄位`
                  * 清除[欄位清單][columns]中有挑選該表格欄位的`資料內容`
                * `(6)別名`已改變
                  * 清除或替換其他參考來源中有聯結該表格`(8)聯結條件區塊`的`(9)連結來源表格`、`(10)連結欄位`, 以下案例說明
                    * 主副表分別為 A、B、C、D、E, B更新別名為C1
                      * B、D、E: 於`(8)聯結條件區塊`的`(9)連結來源表格`中, 有設定B者, 替換為C1
                      * C: 於`(8)聯結條件區塊`的`(9)連結來源表格`中, 有設定B者, 清除`(9)連結來源表格`、`(10)連結欄位`
                  * 替換[欄位清單][columns]中有挑選該表格欄位的`資料內容`
                * `(3)暫存資料表`已改變: 重顯[結構展開 `參考來源表格`][loglist_as]
                  * 勾選: 關聯類型對應圖示 + (來源代號.來源型態) + 來源表格名稱 + (別名) + (暫存資料表) +  [(需傳入參數)]
                  * 未勾選: 關聯類型對應圖示 + (來源代號.來源型態) + 來源表格名稱 + (別名) + [(需傳入參數)]
              * 將本次資料儲存
              * 關閉單據
            * 無鎖定、被鎖定(非本次操作):
              * 彈出錯誤訊息: 該單據已被解除鎖定，無法執行。
      * 作業流程
        * ![flow_save]
    * <t>(17)取消</t>
      * 用途說明
      * 規格說明:
        * 關閉單據
      * 作業流程
        * ![flow_cancel]
      
## <div id="save-action">儲存檢控</div>
* 以下欄位不允空白檢控 [動作通則][link_other2]
  * `(4)表格`、`(6)別名`
* 其他檢控 [動作通則][link_other3]
  * 當`(9)連結來源表格`、`(10)連結欄位`、`(11)條件`、`(12)連結類別`、`(13)連結內容`任一欄位有設定, 則其餘欄位都不可空白
  * 當`(9)連結來源表格`、`(10)連結欄位`、`(11)條件`、`(12)連結類別`、`(13)連結內容`所有欄位都無設定, 則`(13)自訂連結` 必須設定
  * 若`(9)連結欄位` 為個資加密時
    * `(11)連結類別`必須為本表欄位
    * `(12)連結內容`必須為個資加密
    * `(10)條件` 必須為等於或不等於
  * 若`(9)連結欄位` 不為個資加密時
    * `(12)連結內容`不可為個資加密或密碼處理
  * 過濾條件中的限定表格與`表格`是否相同

<!-- 圖示_介面 -->
[ini]:attachment/ini_logjoin.png "[介面]聯結設定"
[fieldbreak_m3]:attachment/mark_ini_logjoin.png "[欄位說明]聯結設定"
[fieldbreak_m4]:attachment/mark_ini_logjoin_phydata.png "[欄位說明]結構欄位"

[flow_joinType]:attachment/Diagram_Join_joinType.png "聯結方式"
[flow_tableType]:attachment/Diagram_Join_tableType.png "類別"
[flow_sourceType]:attachment/Diagram_Join_sourceType.png "連結來源表格"
[flow_linkType]:attachment/Diagram_Join_linkType.png "連結類別"
[flow_save]:attachment/Diagram_Join_save.png "儲存"
[flow_cancel]:attachment/Diagram_Join_cancel.png "取消"

<!-- 超連結 -->
[link_other1]:{4}/IDE/Specification/RulesOther/README?id=ruleother9 "共用通則_其他操作/打樣通則"
[link_other2]:{4}/IDE/Specification//RulesOther/README?id=ruleother7 "共用通則_其他操作/儲存檢控_不允空白"
[link_other3]:{4}/IDE/Specification//RulesOther/README?id=ruleother8 "共用通則_其他操作/儲存檢控_其他"
[link_other4]:{4}/IDE/Specification//RulesOther/README?id=ruleother10 "共用通則_其他操作/鎖定通則"
[link_other5]:{4}/IDE/Specification//RulesOther/README?id=ruleother11 "共用通則_其他操作/個資加密通則"

[link_ruledialog2]:{4}/IDE/Specification/RulesDialog/README#ruledialog2 "共用通則_開啟單據/挑選參數通則"
[link_ruledialog3]:{4}/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_ruledialog4]:{4}/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"
[link_ruledialog5]:{4}/IDE/Specification/RulesDialog/README#ruledialog5 "共用通則_開啟單據/挑選資料表元件通則"
[link_ruledialog8]:{4}/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_ruledialog1]:{4}/IDE/Specification/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_expression]:{4}/IDE/Specification/運算式 "共用通則_開啟運算式"

[link_rulebutton3]:{4}/IDE/Specification/RulesButton/README#rulebutton3 "共用通則_按鍵操作/操作表格記錄通則"

[index]:./README.md "檢視表主頁"
[O9]: "傳遞參數" "共用通則_開啟傳遞參數"
[log_index]:./README.md?id=field15 "檢視表 表格名稱"
[loglist_as]:./joinlist.md?id=field3 "結構展開 參考來源表格"
[logcols_data]:./columns?id=field31 "資料內容"
[columns]:columns "欄位清單"