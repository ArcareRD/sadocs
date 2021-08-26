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
            * 單選選項: 下拉式 / 固定式
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
            * 當表單設計類型=RWD或APP, 且`(2)選擇筆數`=多選, 則 致能, 否則 除能
            * 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 限定: 須同駐留元件檔區的元件, 回傳: 表單元件
            

<!-- 圖片 -->
[image_oalist_STD]:attachment/OAList_STD.png
[image_oalist_APP]:attachment/OAList_APP.png
[image_oalist_block1]:attachment/OAList_block1.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"

[link_ruledialog7]:{4}/IDE/Specification/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
