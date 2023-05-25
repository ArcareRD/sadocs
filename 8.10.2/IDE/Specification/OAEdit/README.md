## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_OAEdit_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_OAEdit_APP]

* [版面資訊通則][link_ruleother1]
		
## <div id="form-action">動作說明</div>
* 依規格關聯-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格關聯-主畫面 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本區塊</p>

    ![pic][image_fieldbreak1]
    * `(1)元件名稱`
        * 用途說明
        * 規格說明
            * 依專案語系, 顯示元件多語名稱
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示元件料號
    * `(3)執行條件`
        * 用途說明
        * 規格說明
            * 參照 [操作條件式通則][link_ruledialog1], 回傳並顯示: 條件說明
    * `(4)控制類別選項`
        * 用途說明
        * 規格說明
            * 選項 可編欄位/頁籤失能/網格資料行
            * 依本元件的元件類型, 給不同預設值, 且不允異動
                * 元件類型=頁籤區塊，控制類別選項=頁籤失能
                * 元件類型=多筆表格，控制類別選項=網格資料行
                * 非上述二項元件類型者, 控制類別選項=可編欄位
            * 當 `表單設計類型`=APP, 則 選項 頁籤失能/網格資料行 隱藏

* <p id="fieldbreak2" style="color:blue;font-weight:bold">可編欄位</p>

    ![pic][image_fieldbreak2]
    * `(1)可編欄位`
        * 用途說明
        * 規格說明
            * 當 `控制類別選項`=可編欄位, 致能
            * 選項 唯讀/勿駐/資料隱藏/資料隱藏; 除致能控制與預設, 請參照下列表(粗體為預設)
                * ![pic][image_fieldbreak2_1]

* <p id="fieldbreak3" style="color:blue;font-weight:bold">頁籤失能</p>

    ![pic][image_fieldbreak3]
    * `(1)頁籤失能`
        * 用途說明
        * 規格說明
            * 當 `表單設計類型`=APP時, 隱藏
    * `(2)失能頁籤序`
        * 用途說明
        * 規格說明
            * 當 `控制類別選項`=頁籤失能, 致能
            * 當 `表單設計類型`=APP時, 隱藏
            * 選項 為本元件頁籤區塊的頁籤內容

* <p id="fieldbreak4" style="color:blue;font-weight:bold">網格資料行</p>

    ![pic][image_fieldbreak4]
    * `(1)網格資料行`
        * 用途說明
        * 規格說明
            * 當 `表單設計類型`=APP時, 隱藏
    * `(2)新增`
        * 用途說明
        * 規格說明
            * 當 `控制類別選項`=網格資料行, 致能
            * 當 `表單設計類型`=APP時, 隱藏
            * 預設 未勾選
    * `(3)新增限制`
        * 用途說明
        * 規格說明
            * 當`(2)新增`為勾選, 才致能
            * 當 `表單設計類型`=APP時, 隱藏
            * 選項 致能/除能
    * `(4)刪除`
        * 用途說明
        * 規格說明
            * 當 `控制類別選項`=網格資料行, 致能
            * 當 `表單設計類型`=APP時, 隱藏
            * 預設 未勾選
    * `(5)刪除限制`
        * 用途說明
        * 規格說明
            * 當`(4)刪除`為勾選, 才致能
            * 當 `表單設計類型`=APP時, 隱藏
            * 選項 致能/除能
    * `(6)矛盾提示`
        * 用途說明
        * 規格說明
            * 當 `控制類別選項`=網格資料行, 致能
            * 當 `表單設計類型`=APP時, 隱藏
    * `(7)訊息內容`
        * 用途說明
        * 規格說明
            * 當`(6)矛盾提示`為勾選, 才致能
            * 當 `表單設計類型`=APP時, 隱藏
            * 參照 [操作多語訊息及替代通則][link_ruledialog17], 依駐留專案, 進行訊息內容挑選, 回傳並顯示: 多語名稱

## <div id="save-action">儲存檢控</div>
* 不允空白檢控, 規則參照 [存回不允空白檢控通則][link_ruleother7]
    * [可編欄位][link_fieldbreak2]
        * 當 `控制類別選項`=可編欄位, `可編欄位`, 需擇一, 不允空白
    * [頁籤失能][link_fieldbreak3]
        * 當 `控制類別選項`=頁籤失能, `失能頁籤序`, 不允空白
    * [網格資料行][link_fieldbreak4]
        * 當 `控制類別選項`=網格資料行, `禁止鍵入字元_例外符號`勾選時, `例外符號內容`, 不允空白


## <div id="other-desc">其它</div>
* [MAE加註儲存通則][link_ruleother5]

<!-- 圖片 -->
[image_OAEdit_STD]:attachment/OAEdit_STD.png
[image_OAEdit_APP]:attachment/OAEdit_APP.png
[image_fieldbreak1]:attachment/OAEdit_fieldbreak1.png
[image_fieldbreak2]:attachment/OAEdit_fieldbreak2.png
[image_fieldbreak2_1]:attachment/OAEdit_fieldbreak2-1.png
[image_fieldbreak3]:attachment/OAEdit_fieldbreak3.png
[image_fieldbreak4]:attachment/OAEdit_fieldbreak4.png

<!-- 超連結 -->
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_rulebutton2]:../RulesButton/README#rulebutton2 "共用通則_按鍵操作/單據異動資料按鍵操作通則"
[link_ruledialog1]:../RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog17]:../RulesDialog/README#ruledialog2 "共用通則_開啟單據/操作多語訊息及替代通則"
[link_ruleother5]:../RulesOther/README#ruleother5 "共用通則_其它/MAE加註儲存通則"
[link_ruleother7]:../RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_fieldbreak2]:#fieldbreak2 "欄位說明/可編欄位"
[link_fieldbreak3]:#fieldbreak3 "欄位說明/頁籤失能"
[link_fieldbreak4]:#fieldbreak4 "欄位說明/網格資料行"