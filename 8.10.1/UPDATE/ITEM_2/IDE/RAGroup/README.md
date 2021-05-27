## <div id="layout">版面相關</div>
* 版面
    ![pic][image_report_ragroup]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>

* 依報表規格定義, 結構清單駐留節點: 分頁模式, 顯示本單內容
* 依報表規格定義, 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能
* 動作流程
    * ![pic][image_flow_open]

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
            * 顯示報表階層清單, 過濾: 駐留筆報表, 且階層類型存在【lh.階層首、lf.階層尾】
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
        * 動作流程
            * ![pic][image_flow_add_group]
    * `(7)清除_分群項目`
        * 用途說明
        * 規格說明
            * 在`(5)分群項目`指定駐留任一記錄, 則 致能, 否則 除能
            * 執行按鍵, 將駐留筆從`(5)分群項目`中清除
        * 動作流程
            * ![pic][image_flow_cancel_group]
    * `(8)上移`
        * 用途說明
        * 規格說明
            * 在`(5)分群項目`指定駐留任一記錄, 且`(5)分群項目`記錄筆數>1, 且駐留筆非第一筆時, 則 致能, 否則 除能
            * 執行按鍵, 將駐留筆往上移, 與上一筆記錄調換排序位置
        * 動作流程
            * ![pic][image_flow_move_up]
    * `(9)下移`
        * 用途說明
        * 規格說明
            * 在`(5)分群項目`指定駐留任一記錄, 且`(5)分群項目`記錄筆數>1, 且駐留筆非最後一筆時, 則 致能, 否則 除能
            * 執行按鍵, 將駐留筆往下移, 與下一筆記錄調換排序位置
        * 動作流程
            * ![pic][image_flow_move_down]
    * `(10)分頁模式`
        * 用途說明
            * 報表分頁的基礎
                * 依版面空間: 即版面已滿時才會換頁
                * 依階層別: 挑選依據階層, 依上述設定階層群組依據異動而分頁
        * 規格說明
            * 單一選項: 依版面空間/ 依階層別
    * `(11)依階層別`
        * 用途說明
        * 規格說明
            * 下拉選項: 報表階層清單, 顯示: 階層名稱, 過濾: 駐留筆報表, 且階層類型存在【lh.階層首、lf.階層尾】
    * `(12)換頁重印`
        * 用途說明
            * 指報表換頁時, 頁首內容是否於次頁中顯示
        * 規格說明
            * 單一選項: 是 / 否
    * `(13)頁尾位置`
        * 用途說明
            * 指定頁尾的資訊出現的位置
                * 固定版面底部, 即將頁尾內容固定置於報表最下方
                * 跟隨資料列, 即將頁尾資料內容, 置於頁身或階尾內容的下方顯示
        * 規格說明
            * 單一選項: 固定版面底部 / 跟隨資料列

## <div id="save-action">儲存檢控</div>
* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回不允空白檢控通則][link_ruleother7]
    * 當`(10)分頁模式`未選取任何選項
    * 當`(10)分頁模式`=依階層別, 且`(11)依階層別`未選取任何選項
    * 當`(12)換頁重印`未選取任何選項
	* 當`(12)頁尾位置`未選取任何選項


<!-- 圖片 -->
[image_report_ragroup]:attachment/ReportAnnotation_RAGroup.png
[image_report_ragroup_block1]:attachment/ReportAnnotation_RAGroup_block1.png

[image_flow_open]:attachment/RAGroupFlow_open.png
[image_flow_add_group]:attachment/RAGroupFlow_add_group.png
[image_flow_cancel_group]:attachment/RAGroupFlow_cancel_group.png
[image_flow_move_up]:attachment/RAGroupFlow_move_up.png
[image_flow_move_down]:attachment/RAGroupFlow_move_down.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:/8.10.0/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"

[link_rulebutton2]:/8.10.1/IDE/Specification/RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"
