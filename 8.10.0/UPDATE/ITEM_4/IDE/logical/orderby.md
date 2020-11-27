## <div id="layout">排序依據</div>

* 版面
  * ![ini]

## <div id="form-action">動作說明</div>

* 說明內容
  * [版面資訊通則](../RulesOther/README.md#ruleother1)
  * [單據異動資料按鍵操作通則](../RulesButton/README#rulebutton2) 
  * 單據編輯狀態請參照[檢視表][index]
## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak6" style="color:blue;font-weight:bold">排序依據</p>
    
    ![fieldbreak_m6]  

    * <t>(1)新增</t>
      * 用途說明
      * 規格說明: 
        * 開啟[挑選檢視表元件通則][link_ruledialog8] 取得:未挑選順序、非個資加密、非密碼處理欄位, 帶回欄位名稱並附加到`(9)排序欄位清單`最後一筆
      * 作業流程
    * <t>(2)移至頂端</t>
      * 用途說明
      * 規格說明:
        * 將目前鎖定的欄位移至最頂端；若有多個鎖定欄位，依鎖定欄位順序排序後，移至最頂端
      * 作業流程
    * <t>(3)向上移動</t>
      * 用途說明
      * 規格說明:
        * 將目前鎖定的欄位向上移一個元件；若有多個鎖定欄位，依鎖定欄位順序排序後，取得鎖定欄位中最小順序向上移一個欄位(若最小順序已是第一個欄位則不再變動順序)
      * 作業流程
    * <t>(4)向下移動</t>
      * 用途說明
      * 規格說明:
        * 將目前鎖定的欄位向下移一個元件；若有多個鎖定欄位，依鎖定欄位順序排序後，取得鎖定欄位中最大順序向下移一個欄位(若最大順序已是第後一個欄位則不再變動順序)
      * 作業流程
    * <t>(5)移至最後</t>
      * 用途說明
      * 規格說明:
        * 將目前鎖定的欄位移至最底端；若有多個鎖定欄位，依鎖定欄位順序排序後，移至最底端
      * 作業流程
    * <t>(6)取消鎖定</t>
      * 用途說明
      * 規格說明:
        * 將所有已鎖定的圖示，變動為未鎖定圖示
      * 作業流程
    * <t>(7)排序欄位清單</t>
      * 用途說明
      * 規格說明:
        * 顯示排序欄位清單資訊
        * 排序資料依據排序順序顯示 
      * 作業流程
    * <t>(8)順序</t>
      * 用途說明
      * 規格說明:
        * 顯示排序順序
      * 作業流程
    * <t>(9)鎖定/解鎖鍵</t>
      * 用途說明
      * 規格說明:
        * 顯示在欄位名稱前方
        * 未鎖定圖示: ![orderby_unlock]
        * 已鎖定圖示: ![orderby_lock]
      * 作業流程
    * <t>(10)欄位名稱區塊</t>
      * 用途說明
      * 規格說明:
        * 單擊欄位名稱區塊，改變鎖定/解鎖鍵狀態，並將區塊底色改為灰色
        * 已鎖定:將圖示改為未鎖定
        * 未鎖定:將圖示改為已鎖定
        * 滑鼠滑入時指標改為(move ![orderby_move])，框線顏色改為藍色, 移出後恢復原本設定
        * 滑鼠單擊可將欄位名稱區塊拖動到新位置；若有多個鎖定欄位，依鎖定欄位順序排序後移至新位置
        * 當欄位為個資加密或密碼處理欄位時, 須依據[加密規則][link_other5]顯示。
      * 作業流程
    * <t>(11)排序類型</t>
      * 用途說明: order by desc / asc
      * 規格說明:
        * 預設:昇冪
        * 昇冪:將圖示改為降冪 ↓
        * 降冪:將圖示改為昇冪 ↑
      * 作業流程
    * <t>(12)刪除</t>
      * 用途說明
      * 規格說明:
        * 刪除指定欄位
      * 作業流程
    * <t>(13)儲存</t>
      * 用途說明
      * 規格說明: [頁面鎖定通則][link_other4]
        * 檢查檢視表是否被鎖定
          * 被鎖定(本次操作):               
              * 將本次資料儲存
              * 關閉單據
            * 無鎖定、被鎖定(非本次操作):
              * 彈出錯誤訊息:該單據已被解除鎖定，無法存回。
      * 作業流程
    * <t>(14)取消</t>
      * 用途說明
      * 規格說明:
        * 關閉單據
      * 作業流程
      
## <div id="save-action">儲存檢控</div>
* 以下欄位不允空白檢控 [動作通則][link_other2]
* 其他檢控 [動作通則][link_other3]
    
<!-- 圖示_介面 -->
[ini]:attachment/ini_orderby.png "[介面]排序依據"
[fieldbreak_m6]:attachment/mark_ini_orderby.png "[欄位說明]排序依據"
[orderby_unlock]:attachment/orderby_unlock.png "未鎖定圖示"
[orderby_lock]:attachment/orderby_lock.png "已鎖定圖示"
[orderby_move]:attachment/orderby_move.png "移動圖示"

<!-- 超連結 -->
[link_other1]:{4}/IDE/Specification/RulesOther/README?id=ruleother9 "共用通則_其他操作/打樣通則"
[link_other2]:{4}/IDE/Specification/RulesOther/README?id=ruleother7 "共用通則_其他操作/儲存檢控_不允空白"
[link_other3]:{4}/IDE/Specification/RulesOther/README?id=ruleother8 "共用通則_其他操作/儲存檢控_其他"
[link_other4]:{4}/IDE/Specification/RulesOther/README?id=ruleother10 "共用通則_其他操作/鎖定通則"
[link_other5]:{4}/IDE/Specification/RulesOther/README?id=ruleother11 "共用通則_其他操作/個資加密通則"

[link_ruledialog8]:{4}/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"

[index]:./README "檢視表主頁"