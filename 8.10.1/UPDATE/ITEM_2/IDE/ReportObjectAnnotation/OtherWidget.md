非圖表元件規格定義
===
## 版面相關
* 版面</br>
    ![pic][image_other_widget]

## 欄位設定
* <p id="fieldbreak1" style="color:blue;">資料呈現</p>

    * ![pic][image_other_widget_block1]
    * `(1)模版`
        * 用途說明  
        * 規格說明
            * 當`元件類型`存在【rTF.文字方塊】則 顯示, 否則隱藏
            * 下拉選項: 資料模版清單, 過濾: 駐留筆專案, 顯示: 模版名稱, 排序: 模版名稱(升冪)
            * 系統預設: 專案預設模版的模版名稱 
            * 當本次選取模版的`貨幣符號`未勾選時, 清空: `(2)貨幣欄位`
    * `(2)貨幣欄位`
        * 用途說明
        * 規格說明
            * 當`元件類型`存在【rTF.文字方塊】則 顯示, 否則隱藏
            * 當`(1)模版`的`模版組成`=貨幣, 且`貨幣符號`為已勾選, 則 致能, 否則 除能
            * 參照 [挑選報表元件通則][link_ruledialog15], 從駐留報表中, 進行報表元件挑選, 回傳:報表元件
    * `(3)長度限制`
        * 用途說明
        * 規格說明
            * 當`元件類型`【rTF.文字方塊】則 顯示, 否則隱藏
            * 自行輸入
    * `(4)與前行同值時`
        * 用途說明
        * 規格說明
            * 當`元件類型`【rTF.文字方塊、rTA.多行文字】則 顯示, 否則隱藏
            * 單一選項: 打印 / 省略
            * 系統預設: 打印
            * 當選項=打印時, 將駐留筆報表元件從[欄位同值不列印排序][object_print_sorting_list]中清除
            * 當選項=省略時, 將駐留筆報表元件新增至[欄位同值不列印排序][object_print_sorting_list]中
    * `(5)排序`
        * 用途說明
        * 規格說明
            * 當`元件類型`【rTF.文字方塊、rTA.多行文字】則 顯示, 否則隱藏
            * 當`(4)與前行同值時`=省略, 則 致能, 否則 除能
            * 致能時, 執行開啟[欄位同值不列印排序][object_print_sorting_list]
    * `(6)資料超長`
        * 用途說明
        * 規格說明
            * 當`元件類型`【rTF.文字方塊、rTA.多行文字】則 顯示, 否則隱藏
            * 單一選項: 不折行 / 折行固定行數 / 折行變動行數
            * 系統預設: 不折行
    * `(7)折行固定行數`
        * 用途說明
        * 規格說明
            * 當`元件類型`【rTF.文字方塊、rTA.多行文字】則 顯示, 否則隱藏
            * 當`(6)資料超長`=折行固定行數, 則 致能, 否則 除能
            * 致能時, 使用者自行輸入

* <p id="fieldbreak2" style="color:blue;">資料呈現</p>

    * ![pic][image_other_widget_block2]
    * `(1)數據累計`
        * 用途說明
        * 規格說明
            * 當`(1)模版`的`模版組成`=貨幣或數字時, 則 致能, 否則 除能
            * 系統預設: 未勾選
    * `(2)換階重算`
        * 用途說明
        * 規格說明
            * 當`(1)數據累計`為勾選時, 且`資料區`=階尾N, 則 致能, 否則 除能
    * `(3)初始值`
        * 用途說明
        * 規格說明
            * 當`(2)換階重算`為勾選時, 則致能, 否則 除能
     * `(4)初始值_類別`
        * 用途說明
        * 規格說明
            * 當`(3)初始值`為勾選時, 則致能, 否則 除能
            * 下拉選項: 自訂 / 欄位 / 元件 / 參數
    * `(5)初始值_內容`
        * 用途說明
        * 規格說明
            * 當`(3)初始值_類別`=自訂, 由使用者自行輸入
            * 當`(3)初始值_類別`=欄位, 且[報表_資料來源][]`資料來源_類別`=檢視表, 參照 [挑選檢視表元件通則][link_ruledialog8], 從`資料來源_內容`中, 進行檢視表元件挑選, 回傳:檢視表元件.
            * 當`(3)初始值_類別`=欄位, 且[報表_資料來源][]`資料來源_類別`=資料表, 參照 [挑選資料表元件通則][link_ruledialog5]，從`資料來源_內容`中, 進行資料表元件挑選, 回傳:資料表元件.
            * 當`(3)初始值_類別`=元件, 參照 [挑選報表元件通則][link_ruledialog15], 從駐留報表中, 進行報表元件挑選, 回傳:報表元件
            * 當`(3)初始值_類別`=參數, [挑選報表參數通則][link_ruledialog9], 從駐留報表中, 進行報表參數挑選, 回傳:報表參數
    * `(6)零值顯示`
        * 用途說明
        * 規格說明
            * 系統預設: 未勾選
    * `(7)數值加密`
        * 用途說明
        * 規格說明
            * 當`(1)模版`的`模版組成`=貨幣或數字時, 則 致能, 否則 除能
            * 系統預設: 未勾選

* <p id="fieldbreak3" style="color:blue;">給值內容</p>

    * ![pic][image_other_widget_block3]
    * `(1)給值內容`
        * 用途說明
        * 規格說明
            * 單一選項: 系統資訊 / 頁面資訊 / 操作者資料 / 來源給值 / 欄位組合 / 查表給值 / 代碼轉換
    * `(2)系統資訊`
        * 用途說明
        * 規格說明
            * 當`(1)給值內容`=系統資訊, 則 致能, 否則 除能
            * 單一選項: 系統日期 / 系統日期時間 / 系統時間
    * `(3)頁面資訊`
        * 用途說明
        * 規格說明
            * 當`(1)給值內容`=頁面資訊, 則 致能, 否則 除能
            * 單一選項: 頁次 / 總頁數 / 條文
    * `(4)頁面資訊_條文`
        * 用途說明
        * 規格說明

<!-- 圖片 -->
[image_other_widget]:attachment/ReportObjectAnnotation_OtherWidget.png
[image_other_widget_block1]:attachment/ReportObjectAnnotation_OtherWidget_block1.png
[image_other_widget_block2]:attachment/ReportObjectAnnotation_OtherWidget_block2.png
[image_other_widget_block3]:attachment/ReportObjectAnnotation_OtherWidget_block3.png
[image_other_widget_block4]:attachment/ReportObjectAnnotation_OtherWidget_block4.png

<!-- 超連結 -->
[object_print_sorting_list]:ReportObjectNoPrintSortingList.md

[link_ruledialog19]:/8.10.1/IDE/Specification/RulesDialog/README#ruledialog19 "共用通則_開啟單據/操作邏輯函數表格通則"
[link_ruledialog8]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_ruledialog9]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog9 "共用通則_開啟單據/挑選報表參數通則"
[link_ruledialog15]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog15 "共用通則_開啟單據/挑選報表元件通則"