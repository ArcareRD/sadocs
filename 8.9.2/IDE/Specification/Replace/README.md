## <div id="layout">版面相關</div>
* 版面</br>
    ![pic][image_replace]
* 參照 [版面資訊通則][link_ruleother1]
		
## <div id="form-action">動作說明</div>
* 由各呼叫端開啟 以Dailog on Top 的方式開啟			    

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    ![pic][image_fieldbreak1]
    * `(1)替代來源`
        * 用途說明
        * 規格說明
            * 選項 表單欄位/資料表/檢視表
            * 當前單未限定來源, 選項致能
            * 當前單有限定來源, 該選項點選, 除能
            * 切換選項時, 顯示詢問訊息盒【標題: 系統訊息 / 訊息內容: 不同來源將清空替代來源內容 / 按鍵: 確認、取消】
            * 確認: 關閉訊息, 清除`(2)表格名稱`、`(3)過濾條件`、`(4)替代表格`內容
            * 取消: 關閉訊息, 保留原內容
        * 作業流程    
            * <ps>待補</ps>
    * `(2)表格名稱`
        * 用途說明
        * 規格說明
            * 當前單有限定來源, 顯示限定表格名稱, 除能
            * 當前單無限定來源
                * `(1)替代來源`=表單: 除能
                * `(1)替代來源`=資料表: 參照 [挑選資料表通則][link_ruledialog3], 進行資料表挑選
                * `(1)替代來源`=檢視表: 參照 [挑選檢視表通則][link_ruledialog4], 進行資料表挑選
    * `(3)傳遞參數`
        * 用途說明
        * 規格說明
            * 當前單有限定來源, 除能
            * 當前單無限定來源
                * `(1)替代來源`=表單: 除能
                * `(1)替代來源`=資料表: 除能
    * `(4)過濾條件`
        * 用途說明
        * 規格說明
            * 當前單有限定來源, 顯示限定過濾條件, 除能
            * 當前單無限定來源
                * `(1)替代來源`=表單: 除能
                * `(1)替代來源`=資料表、檢視表: 參照[操作條件式通則][link_ruledialog1], 限定: `(1)替代來源`、`(2)表格名稱`, 進行條件設定
    * `(5)上層表格`
        * 用途說明
        * 規格說明    
            * 顯示依前單限定的上層檢視表名稱
            * 前單未限定上層檢視表, 隱藏
    * `(6)替換字表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton1]
    * `(7)載入`
        * 用途說明
        * 規格說明
            * 取得的前單訊息內容, 依空格區分字中, 擷取有 % 開頭的文字內容, 載入`(6)替換字表格`的`(8)替換字變數`中
                * 當擷取文字不存在`(8)替換字變數`中, 則新增資料列
        * 作業流程    
            * <ps>待補</ps>
    * `(8)替換字變數`
        * 用途說明
        * 規格說明
            * 自行輸入
    * `(9)來源類型`
        * 用途說明
        * 規格說明
            * 選項 參數/表單元件/查表欄位/全域變數/上層欄位/回傳參數
            * `(1)替代來源`=表單, 選項 查表欄位, 隱藏
            * `(1)替代來源`=資料表、檢視表, 選項 表單元件, 隱藏
            * 當`(5)上層表格`有值, 選項 上層欄位, 才顯示
            * 由[超連結內容_超連結按鍵]開啟, 才顯示
        * 作業流程    
            * <ps>待補</ps>
    * `(10)來源欄位`
        * 用途說明
        * 規格說明
            * `(9)來源類型`=參數: 參照 [挑選參數通則][link_ruledialog9], 從駐留表單中, 進行參數挑選
            * `(9)來源類型`=表單元件: 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 過濾不為隱藏元件 及 元件類型為 [註1][link_tag1], 進行元件挑選; 若元件為 個資加密且未解密欄位 或 密碼欄位, 則該元件顯示紅色字體
            * `(9)來源類型`=查表欄位
                * 當`(1)替代來源`=資料表, 
                參照 [挑選資料表元件通則][link_ruledialog5], 從`(2)表格名稱`中, 過濾型態不為二進位、備註, 進行元件挑選
                * 當`(1)替代來源`=檢視表, 
                參照 [挑選檢視表元件通則][link_ruledialog8], 從`(2)表格名稱`中, 過濾型態不為二進位、備註, 進行元件挑選
            * `(9)來源類型`=全域變數: 參照 [挑選全域變數通則][link_ruledialog10], 進行全域變數挑選
            * `(9)來源類型`=上層欄位: 參照 [挑選檢視表元件通則][link_ruledialog8], 從`(5)上層表格`中, 進行元件挑選
            * `(9)來源類型`=回傳參數: 參照 [挑選開放按鍵回傳參數通則][link_ruledialog16], 從前單按鍵中, 過濾型態不為二進位、備註, 進行參數挑選
        * 作業流程    
            * <ps>待補</ps>
    * `(11)儲存`
        * 用途說明
        * 規格說明
            * 前單為瀏覽狀態開啟本單, 除能
            * 參照 [權限驗証通則][link_ruleother6]
        * 作業流程    
            * <ps>待補</ps>

## <div id="save-action">儲存檢控</div>
* [存回不允空白檢控通則][link_ruleother7]
    * 檢控範圍
        * [基本][link_fieldbreak1]
            * `(8)替換字變數`、`(9)來源類型`、`(10)來源欄位`, 不允空白

<!-- 圖片 -->
[image_replace]:attachment/Replace.png
[image_fieldbreak1]:attachment/fieldbreak1.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "基本"
[link_tag1]:#tag1 "註1"
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_rulebutton1]:../RulesButton/README#rulebutton3 "共用通則_操作按鍵/操作表格記錄通則"
[link_ruleother6]:../RulesOther/README#ruleother6 "共用通則_其它/權限驗証通則"
[link_ruledialog3]:../RulesDialog/README#ruledialog3 "共用通則_開單操作/挑選資料表通則"
[link_ruledialog4]:../RulesDialog/README#ruledialog4 "共用通則_開單操作/挑選檢視表通則"
[link_ruledialog1]:../RulesDialog/README#ruledialog1 "共用通則_開單操作/操作條件式通則"
[link_ruledialog9]:../RulesDialog/README#ruledialog9 "共用通則_開單操作/挑選參數通則"
[link_ruledialog7]:../RulesDialog/README#ruledialog7 "共用通則_開單操作/挑選表單元件通則"
[link_ruledialog10]:../RulesDialog/README#ruledialog10 "共用通則_開單操作/挑選全域變數通則"
[link_ruledialog5]:../RulesDialog/README#ruledialog5 "共用通則_開單操作/挑選資料表元件通則"
[link_ruledialog8]:../RulesDialog/README#ruledialog8 "共用通則_開單操作/挑選檢視表元件通則"
[link_ruledialog16]:../RulesDialog/README#ruledialog16 "共用通則_開單操作/挑選開放按鍵回傳參數通則"
[link_ruleother7]:../RulesOther/README#ruleother7 "共用通則_開單操作/存回不允空白檢控通則"