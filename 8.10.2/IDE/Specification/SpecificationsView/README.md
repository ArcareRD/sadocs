## <div id="layout">版面相關</div>
* 版面
    ![pic][image_spec_form]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 開啟後視窗寬高預設為 1300 * 750, 並提供使用者調整寬高

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_fieldbreak1]
    * `(1)視窗標題`
        * 用途說明
        * 規格說明
            * 依專案語系顯示: 表單名稱_表單料號
    * `(2)加註頁面區塊`
        * 用途說明
        * 規格說明
            * 依駐留節點類別, 顯示對應的規格定義內容

* <p id="fieldbreak2" style="color:blue;font-weight:bold">規格描述區塊</p>

    * ![pic][image_fieldbreak2]
    * `(1)規格描述區塊`
        * 用途說明
        * 規格說明
            * 顯示表單相關分類、單元、加註，依樹狀方式呈現
                * 樹狀分階為 `(2)根節點`、`(3)單元分類`、`(4)單元`、`(5)加註行為`
            * 節點圖示顯示
                * 節點內有子階時, 節點圖示為資料夾, 並可展開/關閉子階內容
                * 節點內無子階時, 節點圖示為文件
            * 可調整區塊寬度, 規則如下:
                * 調整後最小寬度不得低於**280px**; 最大寬度不得高於**500px**
                * 規格定義視窗的寬度, 在調整過程中同比例增加寬度
    * `(2)根節點`
        * 用途說明
        * 規格說明
            * 顯示 "表單名稱 _ 成品料號"
            * 駐留節點, `加註頁面區塊`清空
            * `(6)滑鼠右鍵選單`: 重新載入
    * `(3)單元分類`
        * 用途說明
        * 規格說明
            * 節點顯示固定文字, 分別為
                * 資料來源
                    * `(6)滑鼠右鍵選單`: 新增/重新載入
                * 表單元件
                    * `(6)滑鼠右鍵選單`: 重新載入
                * 隱藏表單元件
                    * `(6)滑鼠右鍵選單`: 新增/重新載入
                * 按鍵
                    * `(6)滑鼠右鍵選單`: 重新載入
                * 隱藏按鍵
                    * `(6)滑鼠右鍵選單`: 新增/重新載入                
            * 駐留節點, `加註頁面區塊`清空
    * `(4)單元`
        * 用途說明
        * 規格說明
            * 顯示 "(加註數量) 單元名稱 _ 單元料號"
            * 駐留節點, `加註頁面區塊`清空
            * `(6)滑鼠右鍵選單`
                * 元件單元: 行為選項/複製其他元件/重新載入
                * 隱藏元件單元: 行為選項/刪除/重新命名/複製其他元件/重新載入
                * 按鍵單元: 行為選項/複製其他按鍵/重新載入
                * 隱藏按鍵單元: 行為選項/刪除/重新命名/複製其他按鍵/重新載入
            * 執行滑鼠雙擊時, 可開啟[規格備註][link_specification]
    * `(5)加註行為`
        * 用途說明
        * 規格說明
            * 資料來源下的加註行為
                * 基本設定
                    * 顯示行為名稱
                    * `(6)滑鼠右鍵選單`: 重新載入
                    * 執行滑鼠雙擊時, 可開啟[規格備註][link_specification]
                * 資料區
                    * 顯示 "資料區_檔區"
                    * `(6)滑鼠右鍵選單`: 新增/刪除/元件對應/重新載入
            * 元件加註行為
                * 基本設定
                    * 顯示行為名稱
                    * `(6)滑鼠右鍵選單`: 行為選項/重新載入
                * 樹狀控制、樞紐設定
                    * 顯示行為名稱
                    * `(6)滑鼠右鍵選單`: 行為選項/刪除/重新載入
                * 其它加註行為
                    * 若加註有設定執行條件, 則顯示 "行為名稱【執行條件說明】", 若無設定, 則顯示行為名稱
                    * `(6)滑鼠右鍵選單`: 行為選項/刪除/複製本筆/重新載入
            * 按鍵加註行為
                * 基本設定
                    * 顯示行為名稱
                    * `(6)滑鼠右鍵選單`: 行為選項/重新載入
                * 執行限制
                    * 若加註有設定前置條件、判斷條件, 則顯示 "執行限制【前置條件說明, 判斷條件說明】", 若無設定, 則顯示行為名稱
                    * `(6)滑鼠右鍵選單`: 行為選項/刪除/複製本筆/重新載入
                * 其它加註行為
                    * 若加註有設定執行條件, 則顯示 "行為名稱【執行條件說明1, 執行條件說明2, ...】", 若無設定, 則顯示行為名稱
                    * `(6)滑鼠右鍵選單`: 行為選項/刪除/複製本筆/重新載入
            * 駐留節點, 將對應的加註行為設定頁面載入`加註頁面區塊`中

* <p id="fieldbreak3" style="color:blue;font-weight:bold">按鍵操作區塊</p>

    * ![pic][image_fieldbreak3]
    * `(1)新增節點`
        * 用途說明
        * 規格說明
            * 當駐留節點為 資料來源、隱藏表單元件、隱藏按鍵、資料區 則按鍵致能, 否則 除能
            * 當駐留節點為 資料來源、資料區: 開啟[新增資料區][link_AddDataAreaForm]
            * 當駐留節點為 隱藏表單元件: 開啟[新增隱藏元件][link_AddHiddenObject]
            * 當駐留節點為 隱藏按鍵: 開啟[新增隱藏按鍵][link_AddHiddenButton]
    * `(2)刪除節點`
        * 用途說明
        * 規格說明
            * 當駐留節點為 資料來源/資料區、隱藏元件單元、隱藏按鍵單元、非基本設定的加註行為選項 則按鍵致能, 否則 除能
            * 執行刪除駐留節點、及其下所有子階節點對應的加註資料
    * `(3)行為選項`
        * 用途說明
        * 規格說明
            * 當駐留節點為 元件單元、按鍵單元、隱藏元件單元、隱藏按鍵單元、上述單元的加註行為 則按鍵致能, 否則 除能
            * 當駐留節點為 元件單元、隱藏元件單元, 開啟[元件行為選項][link_ObjectBehavior]
            * 當駐留節點為 按鍵單元、隱藏按鍵單元, 開啟[按鍵行為選項][link_ButtonBehavior]
            * 關閉行為選項, 重新載入節點及單元的加註數量
    * `(4)加註複製`
        * 用途說明
        * 規格說明
            * 當駐留節點為 元件單元、按鍵單元、隱藏元件單元、隱藏按鍵單元 則按鍵致能, 否則 除能
            * 當駐留節點為 元件單元、隱藏元件單元, 開啟[元件加註複製][link_CopyObjectAnnotationForm]
            * 當駐留節點為 按鍵單元、隱藏按鍵單元, 開啟[按鍵加註複製][link_CopyButtonAnnotationForm]
            * 關閉行為選項, 重新載入節點及單元的加註數量   
    * `(5)規格備註`
        * 用途說明
        * 規格說明
            * 當駐留節點為 資料來源、元件單元、按鍵單元、隱藏元件單元、隱藏按鍵單元 則按鍵致能, 否則 除能
            * 依駐留節點開啟對應的[規格備註][link_specification]
    * `(6)檢錯`
        * 用途說明
            * 檢查駐留筆表單及表單元件已完成的規格, 進行語法及完成度的檢查
        * 規格說明
            * 當檢查完成, 且無錯誤時, 顯示訊息盒【標題: 系統訊息 / 內容: 檢錯完成。 / 按鍵: 確定】
                * 執行確定, 關閉表單
            * 當檢查完成, 且存在錯誤時, 展開所有節點, 錯誤單元以紅字顯示, 並以Hint方式顯示第一筆錯誤資訊
    * `(7)重新載入`
        * 用途說明
        * 規格說明
            * 重新載入`(1)規格描述區塊`, 載入後駐留原駐留節點
    * `(8)線上說明`
        * 用途說明
        * 規格說明
            * 當駐留節點為 根節點、元件單元、按鍵單元、隱藏元件單元、隱藏按鍵單元、加註行為 則按鍵致能, 否則 除能
            * [OnlineHelp通則][link_ruleother2]
            * 依駐留節點開啟對應的線上說明文件
    * `(9)相關元件`
        * 用途說明
        * 規格說明
            * 當駐留節點為 元件單元、按鍵單元、隱藏按鍵單元、加註行為 則按鍵致能, 否則 除能
            * 依駐留報表元件單元, 開啟[元件欄位清單][link_FormAndReportComponents], 傳入: 表單名稱、駐留單元名稱
    * `(10)加註狀態`
        * 用途說明
            * 記錄該表單是否加註完成的標記
        * 規格說明
            * 當狀態為開工時, 執行按鍵將狀態改為完工
            * 當狀態為完工時, 執行按鍵將狀態改為開工
    * `(11)元件對應`
        * 用途說明
        * 規格說明
            * 開啟[元件對應][link_FAConnect]
    * `(12)重新命名`
        * 用途說明
        * 規格說明
            * 節點進入編輯狀態, 可修改名稱, 跳離後存回多語內容
    * `(13)複製本筆`
        * 用途說明
        * 規格說明
            * 依駐留加註行為整筆複製
            * 若複製的節點為 按鍵加註_執行限制, 則執行序取最大號+1
            * 若複製的節點為 按鍵加註_其它加註行為, 則優先序取最大號+1
    * `(14)單據異動記錄按鍵群`
        * 用途說明
        * 規格說明
            * [單據異動資料按鍵操作通則][link_rulebutton2]

<!-- 圖片 -->
[image_spec_form]:attachment/SpecificationsView.png
[image_fieldbreak1]:attachment/SpecificationsView_block1.png
[image_fieldbreak2]:attachment/SpecificationsView_block2.png
[image_fieldbreak3]:attachment/SpecificationsView_block3.png

<!-- 超連結 -->
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_specification]:../SpecificationRemarks/README "規格備註"
[link_AddDataAreaForm]:../AddDataAreaForm/README "新增資料區"
[link_AddHiddenObject]:../AddHiddenObject/README "新增隱藏元件"
[link_AddHiddenButton]:../AddHiddenButton/README "新增隱藏按鍵"
[link_ObjectBehavior]:../ObjectBehavior/README "元件行為選項"
[link_ButtonBehavior]:../ButtonBehavior/README "按鍵行為選項"
[link_CopyObjectAnnotationForm]:../CopyObjectAnnotationForm/README "元件加註複製"
[link_CopyButtonAnnotationForm]:../CopyButtonAnnotationForm/README "按鍵加註複製"
[link_FAConnect]:../FAConnect/README "元件對應"
[link_FormAndReportComponents]:../FormAndReportComponents/README "元件欄位清單"
[link_ruleother2]:../RulesOther/README#ruleother2 "共用通則_其它/OnlineHelp通則"
[link_rulebutton2]:../RulesButton/README#rulebutton2 "共用通則_操作按鍵/單據異動資料按鍵操作通則"