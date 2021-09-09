## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_oalist_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_oalist_APP]



## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_oalist_block1]
    * `(1)呈現方式`
        * 用途說明
        * 規格說明
            * 單選選項: 下拉式 / 清單式
            * 系統預設: 下拉式
            * 當表單設計類型=標準, 且`(1)呈現方式`=下拉式, 異動欄位: `(2)選擇筆數`=單選
            * <delLine>固定式: 選項 單選/複選; 呈現方式=固定式，致能; 預設單選<delLine>
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
            
* <p id="fieldbreak1" style="color:blue;font-weight:bold">變動項次</p>

    * ![pic][image_oalist_block2]
    * `(2)錯誤檢核與訊息`
        * 用途說明
        * 規格說明            
            * 當表單設計類型=APP, 則 隱藏, 否則 顯示
            * 當符合下列條件時, 則 除能, 否則 致能
                * 當`(1)操作方式`=僅挑選指定 且 `(3)對應資料庫`=暫存表格
                * 當表單設計類型=RWD 且 [基本][link_fieldbreak1]的`呈現方式`=下拉式 且 [基本][link_fieldbreak1]的`選擇筆數`=多選
    * `(3)對應資料庫`
        * 用途說明
        * 規格說明
            * 單選選項: 檢視表 / 暫存表格
            * 系統預設: 檢視表
            * 當`(1)操作方式`=可自行輸入, 則 除能, 否則 致能
            * 當表單設計類型=APP, 隱藏選項: 暫存表格, 否則 顯示全部選項
            * 切換選項時, 清空欄位: `(4)表格名稱`、`(7)過濾條件說明`、`(5)來源欄位`
    * `(5)來源欄位`
        * 用途說明
        * 規格說明            
            * 當`(3)對應資料庫`=檢視表, 參照 [挑選檢視表元件通則][link_ruledialog8], 從`(4)表格名稱`中, 進行檢視表元件挑選, 限定: 不為密碼處理及個資加密的欄位, 回傳:檢視表元件.
                * 當[基本][link_fieldbreak1]的`呈現方式`=下拉式 且 [基本][link_fieldbreak1]的`選擇筆數`=多選, 增加限定: 且元件對應欄位型態須為文字或備註
            * 當`(3)對應資料庫`=暫存表格, 參照 [挑選資料表元件通則][link_ruledialog5]，從`(4)表格名稱`中, 進行資料表元件挑選, 限定: 不為密碼處理及個資加密的欄位, 回傳: 資料表元件.
                * 當[基本][link_fieldbreak1]的`呈現方式`=下拉式 且 [基本][link_fieldbreak1]的`選擇筆數`=多選, 增加限定: 且元件對應欄位型態須為文字或備註
            * 變色顯示, 請參照 [個資加密提示通則][link_ruleother11]
    * `(6)帶回對應元件`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 限定: 不為密碼處理及個資加密未解密的欄位, 回傳: 表單元件
                * 當[基本][link_fieldbreak1]的`呈現方式`=下拉式 且 [基本][link_fieldbreak1]的`選擇筆數`=多選, 增加限定: 且元件對應欄位型態須為文字或備註
            * 變色顯示, 請參照 [個資加密提示通則][link_ruleother11]



<!-- 圖片 -->
[image_oalist_STD]:attachment/OAList_STD.png
[image_oalist_APP]:attachment/OAList_APP.png
[image_oalist_block1]:attachment/OAList_block1.png
[image_oalist_block2]:attachment/OAList_block2.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"

[link_ruledialog7]:{4}/IDE/Specification/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruledialog5]:{4}/IDE/Specification/RulesDialog/README#ruledialog5 "共用通則_開啟單據/挑選資料表元件通則"
[link_ruledialog8]:{4}/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"

[link_ruleother11]:{4}/IDE/Specification/RulesOther/README#ruleother11 "共用通則_其它/個資加密提示通則"
