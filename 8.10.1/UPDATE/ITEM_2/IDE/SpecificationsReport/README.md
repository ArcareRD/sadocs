## <div id="layout">版面相關</div>
* 版面
    ![pic][image_spec_report]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 開啟後視窗寬高預設為 1100 * 700


## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_spec_report_block1]
    * `(1)視窗標題`
        * 用途說明
        * 規格說明
            * 依專案語系顯示: 報表名稱_報表料號
    * `(2)規格描述`
        * 用途說明
        * 規格說明
            * 參考 `(8)規格描述區塊`, 當節點支援雙擊，則致能; 否則 除能
            * 當致能時,  執行動作可開啟[規格備註][link_specification]
    * `(3)檢錯`
        * 用途說明
            * 檢查報表及報表元件已完成的規格, 進行語法及完成度的檢查
        * 規格說明
            * 當檢查完成, 且無錯誤時, 顯示訊息盒【標題: 系統訊息 / 內容: 檢錯完成。 / 按鍵: 確定】
                * 執行確定, 關閉表單
            * 當檢查完成, 且存在錯誤時, 展開所有節點, 錯誤單元以紅字顯示, 並以Hint方式顯示第一筆錯誤資訊
    * `(4)重新整理`
        * 用途說明
        * 規格說明
            * 重新顯示`(8)規格描述區塊`, 若已駐留節點, 重整後駐留節點不變
    * `(5)線上說明`
        * 用途說明
        * 規格說明
            * 依駐留節點開啟對應的線上說明文件
    * `(6)相關元件`
        * 用途說明
        * 規格說明
            * 當駐留節點為**報表元件單元**時, 則 致能, 否則 除能
            * 依駐留報表元件單元, 開啟[元件欄位清單][], 傳入: 報表名稱、報表元件名稱
    * `(7)加註狀態`
        * 用途說明
            * 記錄該表單是否加註完成的標記
        * 規格說明
            * 當狀態為**開工**時, 執行按鍵將狀態改為**完工**, 並顯示完成圖示: ![pic][image_report_annotation_finish]
            * 當狀態為**完工**時, 執行按鍵將狀態改為**開工**, 並顯示開工圖示: ![pic][image_report_annotation_start]
        * 作業流程
    * `(8)規格描述區塊`
        * 用途說明
        * 規格說明
            * 節點顯示方式, 請參考畫面及下列規則
                * 節點內有子階時, 節點圖示為資料夾, 並可展開/關閉子階內容
                * 節點內無子階時, 節點圖示為文件
                * 各階層顯示內容如下
                    |顯示內容 |所屬階層 |筆數 |支援雙擊 |排序方式 |顯示語系來源 |
                    |--------|---------|-----|---------|--------|-----------|
                    |報表名稱_報表成品料號 |0 |1| | |專案 |
                    |基本設定      |1 |1 |v | |平台 |
                    |資料來源      |1 |1 |v | |平台 |
                    |分頁模式      |1 |1 |v | |平台 |
                    |報表元件      |1 |1 | | |平台 |
                    |報表元件名稱_元件料號 |2 |n |v |依單元料號 |專案 |
            * 當駐留節點支援雙擊, 則執行滑鼠雙擊時, 可開啟[規格備註][link_specification]
            * 依駐留節點類別+元件類別, 單擊開啟對應加註頁面, 顯示於`(9)加註頁面區塊`
    * `(9)加註頁面區塊`
        * 用途說明
        * 規格說明



<!-- 圖片 -->
[image_spec_report]:attachment/SpecificationsReport.png
[image_spec_report_block1]:attachment/SpecificationsReport_block1.png
[image_report_annotation_start]:attachment/ReportAnnotation_Start.png
[image_report_annotation_finish]:attachment/ReportAnnotation_Finish.png


<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother1]:/8.10.1/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_specification]:/8.10.1/IDE/Specification/SpecificationRemarks/README "規格備註"