## <div id="layout">接收參數</div>

* 版面
  * ![ini]

## <div id="form-action">動作說明</div>

* 說明內容
  * [版面資訊通則](../RulesOther/README.md#ruleother1)
  * [單據異動資料按鍵操作通則](../RulesButton/README#rulebutton2)
  * 單據編輯狀態請參照[檢視表][index]
## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak3" style="color:blue;font-weight:bold">接收參數</p>

    ![fieldbreak_m7]  

    * <t>(1)接收參數區塊</t>
      * 用途說明
      * 規格說明:
        * 一頁最多十筆
    * <t>(2)項次</t>
      * 用途說明
      * 規格說明:
        * 依序顯示流水號, 不可輸入內容
    * <t>(3)料號</t>
      * 用途說明
      * 規格說明:
        * 顯示料號, 不可輸入內容
    * <t>(4)參數名</t>
      * 用途說明
      * 規格說明:
        * 自行輸入
    * <t>(5)型態</t>
      * 用途說明
      * 規格說明:
        * 下拉選項: 文字/ 數字/ 日期/ 邏輯      
    * <t>(6)說明</t>
      * 用途說明
      * 規格說明:
        * 自行輸入      
    * <t>(7)新增</t>
      * 用途說明
      * 規格說明:
        * 新增一筆空白紀錄於最末筆
      * 作業流程
    * <t>(8)刪除</t>
      * 用途說明
      * 規格說明:
        * 刪除目前駐留筆紀錄
      * 作業流程
    * <t>(9)儲存</t>
      * 用途說明
      * 規格說明:[頁面鎖定通則][link_other4]
        * 瀏覽模式下開啟本單, 除能
        * 檢查檢視表是否被鎖定
          * 被鎖定(本次操作): 
              * 執行[儲存檢控](#save-action)
              * 將本次資料儲存
              * 關閉單據
            * 無鎖定、被鎖定(非本次操作):
              * 彈出錯誤訊息:該單據已被解除鎖定，無法執行。
      * 作業流程
    * <t>(10)取消</t>
      * 用途說明
      * 規格說明:
        * 關閉單據
      * 作業流程
      
## <div id="save-action">儲存檢控</div>
* 以下欄位不允空白檢控 [動作通則][link_other2]
  * `(4)參數名`、`(5)型態`
* 其他檢控 [動作通則][link_other3]
  * `(4)參數名`不可重覆
  * `(4)參數名`不可有空白字元
    
<!-- 圖示_介面 -->
[ini]:attachment/ini_parameter.png "[介面]接收參數"
[fieldbreak_m7]:attachment/mark_ini_parameter.png "[欄位說明]接收參數"

<!-- 超連結 -->
[link_other1]:{4}/IDE/Specification/RulesOther/README?id=ruleother9 "共用通則_其他操作/打樣通則"
[link_other2]:{4}/IDE/Specification/RulesOther/README?id=ruleother7 "共用通則_其他操作/儲存檢控_不允空白"
[link_other3]:{4}/IDE/Specification/RulesOther/README?id=ruleother8 "共用通則_其他操作/儲存檢控_其他"
[link_other4]:{4}/IDE/Specification/RulesOther/README?id=ruleother10 "共用通則_其他操作/鎖定通則"
[link_other5]:{4}/IDE/Specification/RulesOther/README?id=ruleother11 "共用通則_其他操作/個資加密通則"

[index]:./README "檢視表主頁"