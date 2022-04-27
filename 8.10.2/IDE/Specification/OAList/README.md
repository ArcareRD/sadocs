## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_oalist_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_oalist_APP]
    * [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 依規格關聯-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格關聯-主畫面 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_oalist_block1]
    * `(1)呈現方式`
        * 用途說明
        * 規格說明
            * 單選選項: 下拉式 / 清單式
            * 系統預設: 下拉式
            * 當表單設計類型=標準, 且`(1)呈現方式`=下拉式, 異動欄位: `(2)選擇筆數`=單選
    * `(2)選擇筆數`
        * 用途說明
        * 規格說明
            * 單選選項: 單選 / 多選
            * 系統預設: 單選
            * 當表單設計類型=標準, 且`(1)呈現方式`=下拉式, 則 除能, 否則 致能
    * `(3)查詢轉換欄位`
        * 用途說明
        * 規格說明
            * 當表單設計類型=RWD或APP 且`(1)呈現方式`=下拉式 且`(2)選擇筆數`=多選, 則 致能, 否則 除能
            * 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 限定: 檔區必須同駐留元件的檔區, 且不為密碼處理及個資加密未解密的元件, 且元件對應欄位型態須為文字或備註, 回傳: 表單元件
    * `(4)元件名稱`
        * 用途說明
        * 規格說明
            * 依專案語系, 顯示元件多語名稱
    * `(5)料號`
        * 用途說明
        * 規格說明
            * 顯示傳入的元件料號
    * `(6)執行條件`
        * 用途說明
        * 規格說明
            * 參照 [操作條件式通則][link_ruledialog1], 回傳並顯示:條件說明
            
* <p id="fieldbreak1" style="color:blue;font-weight:bold">選項種類</p>

    * STD</br>
        ![pic][image_oalist_block2_STD]
    * MAE</br>
        ![pic][image_oalist_block2_APP]
    * `(1)選項種類`
        * 用途說明
        * 規格說明
            * 單選選項: 固定項次 / 變動項次
            * 系統預設: 固定項次            
    * `(2)固定項次表格`
        * 用途說明
        * 規格說明
            * 表格操作, 參照 [表格記錄操作通則][link_rulebutton3]
            * 當`(1)選項種類`=固定項次, 則 致能, 否則 除能    
            * 限制: 本表格最多只允設定32筆記錄        
    * `(3)選項內容`
        * 用途說明
        * 規格說明
            * 參照 [使用多語詞庫通則][link_ruledialog2], 回傳:多語料號, 顯示:多語詞彙
    * `(4)強制重新載入`
        * 用途說明
        * 規格說明
            * 當表單設計類型=STD、RWD, 預設: 勾選
            * 當表單設計類型=APP, 預設: 未勾選    
    * `(5)可自行輸入`
        * 用途說明
        * 規格說明  
            * 當表單設計類型=STD、RWD 且 `(1)選項種類`=變動項次, 預設: 未勾選, 且 本欄致能
            * 當表單設計類型=APP 且 `(1)選項種類`=變動項次, 預設:勾選, 且 本欄除能
    * `(6)比對類型`
        * 用途說明
            * 選項元件可自行輸入時，使用輸入內容過濾的方式。共有以下類型:
                * 開頭是: 選項資料開頭符合元件輸入內容
                * 結尾是: 選項資料結尾符合元件輸入內容
                * 相似於: 選項資料相似於元件輸入內
        * 規格說明            
            * 單選選項: 開頭是 / 結尾是 / 相似於
            * 系統預設: 開頭是
            * 當`(5)可自行輸入`為勾選時, 則 致能, 否則 除能
    * `(7)錯誤檢核與訊息`
        * 用途說明
            * 若元件已選項目已不存在資料中會跳出的錯誤訊息
        * 規格說明            
            * 當表單設計類型=APP, 則 隱藏, 否則 顯示
            * 當符合下列條件時, 則 除能, 否則 致能
                * 當`(5)可自行輸入`為未勾選 且 `(8)對應資料庫`=暫存表格
                * 當表單設計類型=RWD 且 [基本][link_fieldbreak1]的`呈現方式`=下拉式 且 [基本][link_fieldbreak1]的`選擇筆數`=多選
            * 當為勾選時, 參照 [使用多語詞庫通則][link_ruledialog2], 回傳:多語料號, 顯示:多語詞彙
    * `(8)對應資料庫`
        * 用途說明
        * 規格說明  
            * 單選選項: 檢視表 / 暫存表格
            * 系統預設: 檢視表
            * 當`(5)可自行輸入`為勾選時, 則 除能, 否則 致能
            * 當表單設計類型=APP, 隱藏選項: 暫存表格, 否則 顯示全部選項
            * 切換選項時, 清空欄位: `(9)表格名稱`、`(10)過濾條件說明`、`(12)來源欄位`
    * `(9)表格名稱`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
            * 當`(5)可自行輸入`為勾選時, 則 致能, 否則 除能
            * 當`(8)對應資料庫`=檢視表, 參照 [挑選檢視表通則][link_ruledialog4], 從駐留專案中, 進行檢視表挑選, 回傳並顯示: 檢視表名
            * 當`(8)對應資料庫`=暫存表格, 參照 [挑選資料表通則][link_ruledialog3], 從駐留專案中, 進行資料表挑選, 限定: 資料表的永久保存為未勾選, 回傳並顯示: 資料表名
            * 當內容異動時, 清空欄位: `(10)過濾條件說明`、`(12)來源欄位`
    * `(10)過濾條件說明`
        * 用途說明
        * 規格說明
            * 本欄位唯讀 
            * 當`(5)可自行輸入`為勾選時, 則 致能, 否則 除能       
            * 當`(8)對應資料庫`=暫存表格, 則 除能, 否則 致能
            * 參照 [操作條件式通則][link_ruledialog1], 限定: 使用`(9)表格名稱`, 且不提供使用密碼處理欄位, 回傳並顯示: 條件說明
    * `(11)變動項次表格`
        * 用途說明
        * 規格說明
            * 當`(5)可自行輸入`為勾選時, 則 致能, 否則 除能        
            * 表格操作, 參照 [表格記錄操作通則][link_rulebutton3]
            * 限制: 本表格最多只允設定11筆記錄 
    * `(12)來源欄位`
        * 用途說明
        * 規格說明            
            * 當`(8)對應資料庫`=檢視表, 參照 [挑選檢視表元件通則][link_ruledialog8], 從`(9)表格名稱`中, 進行檢視表元件挑選, 限定: 不為密碼處理及個資加密的欄位, 回傳:檢視表元件.
                * 當[基本][link_fieldbreak1]的`呈現方式`=下拉式 且 [基本][link_fieldbreak1]的`選擇筆數`=多選, 增加限定: 且元件對應欄位型態須為文字或備註
            * 當`(8)對應資料庫`=暫存表格, 參照 [挑選資料表元件通則][link_ruledialog5]，從`(9)表格名稱`中, 進行資料表元件挑選, 限定: 不為密碼處理及個資加密的欄位, 回傳: 資料表元件.
                * 當[基本][link_fieldbreak1]的`呈現方式`=下拉式 且 [基本][link_fieldbreak1]的`選擇筆數`=多選, 增加限定: 且元件對應欄位型態須為文字或備註
            * 變色顯示, 請參照 [個資加密提示通則][link_ruleother11]
    * `(13)要顯示`
        * 用途說明
        * 規格說明
            * 系統預設: 勾選
    * `(14)帶回值`
        * 用途說明
        * 規格說明
            * 系統預設: 勾選
    * `(15)帶回對應元件`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 限定: 不為密碼處理及個資加密未解密的欄位, 回傳: 表單元件
                * 當[基本][link_fieldbreak1]的`呈現方式`=下拉式 且 [基本][link_fieldbreak1]的`選擇筆數`=多選, 增加限定: 且元件對應欄位型態須為文字或備註
            * 變色顯示, 請參照 [個資加密提示通則][link_ruleother11]
    * `(16)排序方式`
        * 用途說明
        * 規格說明
            * 下拉選項: 升冪 / 升冪
            * 當`(8)對應資料庫`=暫存表格, 則 清空本欄 且 除能 , 否則 致能        

## <div id="save-action">儲存檢控</div>
* 不允空白，以紅框線標註錯誤的欄位
    * 當 [基本][link_fieldbreak1]`(2)選擇筆數`=多選, 則`(3)查詢轉換欄位`, 不允空白
    * 當 [選項種類][link_fieldbreak2]`(2)固定項次表格`有記錄, 則`(3)選項內容`, 不允空白
    * 當 [選項種類][link_fieldbreak2]`(7)錯誤檢核與訊息`為勾選, 則訊息內容, 不允空白
    * 當 [選項種類][link_fieldbreak2]`(1)選項種類`=變動項次, 則`(9)表格名稱`, 不允空白
    * 當 [選項種類][link_fieldbreak2]`(11)變動項次表格`有記錄, 則`(12)來源欄位`、`(15)帶回對應元件`, 不允空白
* 其它檢控
    * 當 [選項種類][link_fieldbreak2]`(1)選項種類`=固定項次, 則`(2)固定項次表格`, 至少要有一筆記錄
    * 當 [選項種類][link_fieldbreak2]`(1)選項種類`=變動項次, 則`(11)變動項次表格`, 至少要有一筆記錄
    * 當 [選項種類][link_fieldbreak2]`(1)選項種類`=變動項次, 則至少要有一筆`(14)帶回值`為勾選的`(15)帶回對應元件`為本元件
    * 當 [選項種類][link_fieldbreak2]`(1)選項種類`=變動項次, 則至少要有一筆記錄設定`(16)排序方式`

## <div id="other-desc">其它</div>
* [MAE加註儲存通則][link_ruleother5]

<!-- 圖片 -->
[image_oalist_STD]:attachment/OAList_STD.png
[image_oalist_APP]:attachment/OAList_APP.png
[image_oalist_block1]:attachment/OAList_block1.png
[image_oalist_block2_STD]:attachment/OAList_block2_STD.png  
[image_oalist_block2_APP]:attachment/OAList_block2_APP.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_fieldbreak2]:#fieldbreak2 "欄位說明/選項種類"
[link_ruleother1]:../Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruledialog7]:../Specification/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_rulebutton2]:../RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
[link_ruledialog1]:../RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_rulebutton3]:{3}/IDE/Specification/RulesButton/README?id=rulebutton3 "共用通則_按鍵操作/操作表格記錄通則"
[link_ruleother11]:{3}/IDE/Specification/RulesOther/README#ruleother11 "共用通則_其它/個資加密提示通則"
[link_ruledialog2]:{3}/IDE/Specification/RulesDialog/README?id=ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruledialog3]:{3}/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_ruledialog4]:{3}/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"
[link_ruledialog5]:{4}/IDE/Specification/RulesDialog/README#ruledialog5 "共用通則_開啟單據/挑選資料表元件通則"
[link_ruledialog8]:{4}/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_ruleother7]:{4}/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:{4}/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
[link_ruleother5]:../RulesOther/README#ruleother5 "共用通則_其它/MAE加註儲存通則"