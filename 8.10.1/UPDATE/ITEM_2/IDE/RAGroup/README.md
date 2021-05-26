## <div id="layout">版面相關</div>
* 版面
    ![pic][image_report_ragroup]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能


## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_report_ragroup_block1]
    * `(1)報表名稱`
        * 用途說明
        * 規格說明
            * 本欄位唯讀
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示前單傳入的報表料號
            * 本欄位除能, 不提供編輯
    * `(3)階層別`
        * 用途說明
        * 規格說明
            * 顯示報表階層清單, 過濾: 駐留筆報表
    * `(4)資料欄位`
        * 用途說明
        * 規格說明
            * 顯示報表元件清單，過濾: 駐留筆報表, 且報表元件類型不存在【rTP.文字標題、rFrame.框線、rEChart.嵌入圖表、rImg.圖片、rLogo.企業標誌、rGrid.表格】
    * `(5)分群項目`
        * 用途說明
        * 規格說明
            * 顯示方式: *階層名稱*.*資料欄位名稱*
    * `(6)加入_分群項目`
        * 用途說明
        * 規格說明
            * 在`(3)階層別`指定駐留任一報表階層, 並同時在`(4)資料欄位`指定駐留任一欄位, 且駐留的階層+資料欄位不存在`(5)分群項目`中, 則 致能, 否則 除能
            * 執行按鍵時, 將指定的階層及資料欄位加入至`(5)分群項目`中
    * `(7)清除_分群項目`
        * 用途說明
        * 規格說明
            * 在`(5)分群項目`指定駐留任一記錄, 則 致能, 否則 除能
            * 執行按鍵, 將駐留筆從`(5)分群項目`中清除
    * `(8)上移`
        * 用途說明
        * 規格說明
            * 在`(5)分群項目`指定駐留任一記錄, 且`(5)分群項目`記錄筆數>1, 且駐留筆非第一筆時, 則 致能, 否則 除能
            * 執行按鍵，將駐留筆往上移
    * `(9)下移`
        * 用途說明
        * 規格說明
            * 在`(5)分群項目`指定駐留任一記錄, 且`(5)分群項目`記錄筆數>1, 且駐留筆非最後一筆時, 則 致能, 否則 除能
            * 執行按鍵，將駐留筆往下移
    * `(10)分頁模式`
        * 用途說明
            * 報表分頁的基礎
                * 依版面空間：即版面已滿時才會換頁
                * 依階層別：挑選依據階層，依上述設定階層群組依據異動而分頁
        * 規格說明
            * 單一選項: 依版面空間 / 依資料行數/ 依階層別
    * `(11)依階層別`
        * 用途說明
        * 規格說明
            * 下拉選項: 報表階層名稱, 過濾: 駐留筆報表
    * `(12)換頁重印`
        * 用途說明
            * 指報表換頁時，頁首內容是否於次頁中顯示
        * 規格說明
    * `(12)頁尾位置`
        * 用途說明
            * 指定頁尾的資訊出現的位置
                * 固定版面底部，即將頁尾內容固定置於報表最下方
                * 跟隨資料列，即將頁尾資料內容，置於頁身或階尾內容的下方顯示
        * 規格說明

## <div id="save-action">儲存檢控</div>
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回不允空白檢控通則][link_ruleother7]
    * 當`(5)參數名`=空值
    * 當`(6)型態`=請選擇

	
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
	* 當`(5)參數名`存在空白字元, 錯誤訊息內容: 參數名:`(5)參數名`, 不允有空白字元


<!-- 圖片 -->
[image_report_ragroup]:attachment/ReportAnnotation_RAGroup.png
[image_report_ragroup_block1]:attachment/ReportAnnotation_RAGroup_block1.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:/8.10.0/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"

[link_rulebutton2]:/8.10.1/IDE/Specification/RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
