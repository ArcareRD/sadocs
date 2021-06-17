## <div id="layout">版面相關</div>
* 版面
    ![pic][image_spec_form]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 開啟後視窗寬高預設為 1300 * 750, 並提供使用者調整寬高
* 動作流程
    * ![pic][image_flow_open]


## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_spec_form_block1]
    * `(1)視窗標題`
        * 用途說明
        * 規格說明
            * 依專案語系顯示: 表單名稱_表單料號
    * `(2)新增子節點`
        * 用途說明
        * 規格說明
            * 當駐留節點為【隱藏表單元件、隱藏按鍵】按鈕致能, 否則 除能
            * 當駐留節點=隱藏表單元件, 開啟[新增隱藏元件][link_AddHiddenObject]
            * 當駐留節點=隱藏按鍵, 開啟[新增隱藏按鍵][link_AddHiddenButton]
            * 關閉新增子節點的介面後, 重新顯示`(8)規格描述區塊`
        * 動作流程
            * ![pic][image_flow_add_children_node]
    * `(3)刪除子節點`
        * 用途說明
        * 規格說明
            * 當駐留節點為【資料區-表頭、資料區-表身n、隱藏元件名_元件料號、隱藏按鍵名_按鍵料號、加註行為選項名、執行限制】按鈕致能, 否則 除能
            * 執行後, 刪除單元及所引用的加註資料, 判重新顯示`(8)規格描述區塊`, 駐留筆節點下的行為選項
        * 動作流程
            * ![pic][image_flow_delete_children_node]
    * `(4)設定`
        * 用途說明
        * 規格說明
            * 當駐留節點為【元件名_元件料號、隱藏元件名_元件料號、按鍵名_按鍵料號、隱藏按鍵名_按鍵料號】按鈕致能, 否則 除能
            * 當駐留節點為【元件名_元件料號、隱藏元件名_元件料號】, 開啟[元件行為選項][link_ObjectBehavior]
            * 當駐留節點為【按鍵名_按鍵料號、隱藏按鍵名_按鍵料號】, 開啟[按鍵行為選項][link_ButtonBehavior]
            * 關閉設定的介面後, 重新顯示`(8)規格描述區塊`, 駐留筆節點下的行為選項
        * 動作流程
            * ![pic][image_flow_behavior]
    * `(5)複製`
        * 用途說明
        * 規格說明
            * 當駐留節點為【元件名_元件料號、隱藏元件名_元件料號、按鍵名_按鍵料號、隱藏按鍵名_按鍵料號】按鈕致能, 否則 除能
            * 當駐留節點為【元件名_元件料號、隱藏元件名_元件料號】, 開啟[元件加註複製][link_CopyObjectAnnotationForm]
            * 當駐留節點為【按鍵名_按鍵料號、隱藏按鍵名_按鍵料號】, 開啟[按鍵加註複製][link_CopyButtonAnnotationForm]
            * 關閉設定的介面後, 重新顯示`(8)規格描述區塊`, 駐留筆節點下的行為選項
        * 動作流程
            * ![pic][image_flow_copy_annotation]
    * `(6)規格備註`
        * 用途說明
        * 規格說明
            * 當駐留節點為【報表名稱_報表成品料號、基本設定、資料區、元件名_元件料號、隱藏元件名_元件料號、按鍵名_按鍵料號、隱藏按鍵名_按鍵料號】按鈕致能, 否則 除能
            * 當致能時, 執行按鈕, 依駐留節點開啟對應的[規格備註][link_specification], 開啟後傳入單元名稱、單元料號
        * 動作流程
            * ![pic][image_flow_open_spec]
    * `(7)檢錯`
        * 用途說明
            * 檢查表單及表單元件已完成的規格, 進行語法及完成度的檢查
        * 規格說明
            * 當檢查完成, 且無錯誤時, 顯示訊息盒【標題: 系統訊息 / 內容: 檢錯完成。 / 按鍵: 確定】
                * 執行確定, 關閉表單
            * 當檢查完成, 且存在錯誤時, 展開所有節點, 錯誤單元以紅字顯示, 並以Hint方式顯示第一筆錯誤資訊
        * 動作流程
            * ![pic][image_flow_error_detection]
    * `(8)重新整理`
        * 用途說明
        * 規格說明
            * 重新顯示`(8)規格描述區塊`, 若已駐留節點, 重整後駐留節點須為原駐留節點
        * 動作流程
            * ![pic][image_flow_reflash]
    * `(9)線上說明`
        * 用途說明
        * 規格說明
            * 當駐留節點為【資料來源、表單元件、隱藏表單元件、按鍵、隱藏按鍵】按鈕除能, 否則 致能
            * 依駐留節點開啟對應的線上說明文件
        * 動作流程
            * ![pic][image_flow_online_help]
    * `(10)相關元件`
        * 用途說明
        * 規格說明
            * 當駐留節點為【元件名_元件料號、隱藏元件名_元件料號】按鈕致能, 否則 除能
            * 依駐留報表元件單元, 開啟[元件欄位清單][], 傳入: 報表名稱、報表元件名稱
        * 動作流程
            * ![pic][image_flow_components]
    * `(11)加註狀態`
        * 用途說明
            * 記錄該表單是否加註完成的標記
        * 規格說明
            * 當狀態為**開工**時, 執行按鍵將狀態改為**完工**, 顯示完成圖示: ![pic][image_form_annotation_finish]
            * 當狀態為**完工**時, 執行按鍵將狀態改為**開工**, 顯示開工圖示: ![pic][image_form_annotation_start]
        * 動作流程
            * ![pic][image_flow_annotation_state]
    * `(12)規格描述區塊`
        * 用途說明
        * 規格說明
            * 節點顯示方式, 請參考畫面及下列規則 (<font style='color:blue;'>藍色字體為變動內容</font>)
                * 節點內有子階時, 節點圖示為資料夾, 並可展開/關閉子階內容
                * 節點內無子階時, 節點圖示為文件
                * 各階層顯示內容如下
                    <table>
                        <tr>
                            <td colspan='4' style='font-weight:bolder;'>節點內容 </td>
                            <td style='font-weight:bolder;'>筆數 </td>
                            <td style='font-weight:bolder;'>支援雙擊</td>
                            <td style='font-weight:bolder;'>同階排序方式</td>
                            <td style='font-weight:bolder;'>顯示語系來源</td>
                        </tr>
                        <tr>
                            <td colspan='4'>表單名稱 </td>
                            <td>1 </td>
                            <td>V </td>
                            <td> </td>
                            <td>專案 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td colspan='3'>資料來源 </td>
                            <td>1 </td>
                            <td> </td>
                            <td> </td>
                            <td>平台 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td colspan='2'>基本設定 </td>
                            <td>1 </td>
                            <td>V </td>
                            <td> </td>
                            <td>平台 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td colspan='2'>資料區-表頭 </td>
                            <td>1 </td>
                            <td>V </td>
                            <td> </td>
                            <td>平台 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td colspan='2' style='color:blue;'>資料區-表身n </td>
                            <td>n </td>
                            <td>V </td>
                            <td> </td>
                            <td>平台 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td colspan='3'>表單元件 </td>
                            <td>1 </td>
                            <td> </td>
                            <td> </td>
                            <td>平台 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td colspan='2' style='color:blue;'>(加註數)元件名_元件料號 </td>
                            <td>n </td>
                            <td>V </td>
                            <td>依元件料號排序 </td>
                            <td>專案 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td> </td>
                            <td>基本設定 </td>
                            <td>1 </td>
                            <td>V </td>
                            <td> </td>
                            <td>平台 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td> </td>
                            <td style='color:blue;'>加註行為選項名【執行條件名】</td>
                            <td>n </td>
                            <td>V </td>
                            <td>依元件行為選項次序排序 </td>
                            <td>平台, 執行條件名:顯示多語庫的詞彙說明 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td colspan='3'>隱藏表單元件 </td>
                            <td>1 </td>
                            <td> </td>
                            <td> </td>
                            <td>平台 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td colspan='2' style='color:blue;'>(加註數)隱藏元件名_元件料號 </td>
                            <td>n </td>
                            <td>V </td>
                            <td>依元件料號排序 </td>
                            <td>專案 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td> </td>
                            <td>基本設定 </td>
                            <td>1 </td>
                            <td>V </td>
                            <td> </td>
                            <td>平台 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td> </td>
                            <td style='color:blue;'>加註行為選項名【執行條件名】</td>
                            <td>n </td>
                            <td>V </td>
                            <td>依元件行為選項次序排序 </td>
                            <td>平台, 執行條件名:顯示多語庫的詞彙說明 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td colspan='3'>按鍵 </td>
                            <td>1 </td>
                            <td> </td>
                            <td> </td>
                            <td>平台 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td colspan='2' style='color:blue;'>(加註數)按鍵名_按鍵料號 </td>
                            <td>n </td>
                            <td>V </td>
                            <td>依按鍵料號排序 </td>
                            <td>專案 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td> </td>
                            <td>基本設定 </td>
                            <td>1 </td>
                            <td>V </td>
                            <td> </td>
                            <td>平台 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td> </td>
                            <td style='color:blue;'>執行限制(執行序)【判斷條件名】</td>
                            <td>n </td>
                            <td>V </td>
                            <td>依執行序排序 </td>
                            <td>平台, 判斷條件名:顯示多語庫的詞彙說明 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td> </td>
                            <td style='color:blue;'>加註行為選項名(優先序)【執行條件名1,執行條件名2...】</td>
                            <td>n </td>
                            <td>V </td>
                            <td>依優先序排序 </td>
                            <td>平台, 執行條件名:顯示多語庫的詞彙說明 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td colspan='3'>隱藏按鍵 </td>
                            <td>1 </td>
                            <td> </td>
                            <td> </td>
                            <td>平台 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td colspan='2' style='color:blue;'>(加註數)隱藏按鍵名_按鍵料號 </td>
                            <td>n </td>
                            <td>V </td>
                            <td>依按鍵料號排序 </td>
                            <td>專案 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td> </td>
                            <td>基本設定 </td>
                            <td>1 </td>
                            <td>V </td>
                            <td> </td>
                            <td>平台 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td> </td>
                            <td style='color:blue;'>執行限制(執行序)【判斷條件名】</td>
                            <td>n </td>
                            <td>V </td>
                            <td>依執行序排序 </td>
                            <td>平台, 判斷條件名:顯示多語庫的詞彙說明 </td>
                        </tr>
                        <tr>
                            <td> </td>
                            <td> </td>
                            <td> </td>
                            <td style='color:blue;'>加註行為選項名(優先序)【執行條件名1,執行條件名2...】</td>
                            <td>n </td>
                            <td>V </td>
                            <td>依優先序排序 </td>
                            <td>平台, 執行條件名:顯示多語庫的詞彙說</td>
                        </tr>
                    </table>
            * 駐留節點為【元件名_元件料號、隱藏元件名_元件料號】請參照 [個資加密提示通則][link_ruleother11] 顯示變色效果
            * 當駐留節點支援雙擊, 則執行滑鼠雙擊時, 可開啟[規格備註][link_specification], 開啟後傳入單元名稱、單元料號
            * 駐留節點不為【表單名稱、資料來源、表單元件、隱藏表單元件、按鍵、隱藏按鍵】, 單擊開啟對應加註頁面, 顯示於`(9)加註頁面區塊`
            * 駐留節點為【元件名_元件料號】, 取得駐留筆表單, 且表單元件類型不為【wTabItem.頁籤內容、wDpanelItem.單一面版】的報表元件清單顯示
            * 滑鼠移入右邊框, 可調整區塊寬度, 規則如下:
                * 調整後最小寬度不得低於**280px**; 最大寬度不得高於**500px**
                * 規格定義視窗的寬度, 在調整過程中同比例增加寬度
            * <font style='color:red;text-decoration:line-through;'>當表單設計類型=APP，則隱藏按鍵類型:開啟、退出 </font>
        * 動作流程
            * ![pic][image_flow_annotation]
    * `(13)加註頁面區塊`
        * 用途說明
        * 規格說明
            * 顯示規格定義內容


<!-- 圖片 -->
[image_spec_form]:attachment/SpecificationsView.png
[image_spec_form_block1]:attachment/SpecificationsView_block1.png
[image_form_annotation_start]:attachment/FormAnnotation_Start.png
[image_form_annotation_finish]:attachment/FormAnnotation_Finish.png

[image_flow_add_children_node]:attachment/SpecificationsViewFlow_add_children_node.png
[image_flow_annotation]:attachment/SpecificationsViewFlow_annotation.png
[image_flow_annotation_state]:attachment/SpecificationsViewFlow_annotation_state.png
[image_flow_behavior]:attachment/SpecificationsViewFlow_behavior.png
[image_flow_components]:attachment/SpecificationsViewFlow_components.png
[image_flow_copy_annotation]:attachment/SpecificationsViewFlow_copy_annotation.png
[image_flow_delete_children_node]:attachment/SpecificationsViewFlow_delete_children_node.png
[image_flow_error_detection]:attachment/SpecificationsViewFlow_error_detection.png
[image_flow_online_help]:attachment/SpecificationsViewFlow_online_help.png
[image_flow_open]:attachment/SpecificationsViewFlow_open.png
[image_flow_open_spec]:attachment/SpecificationsViewFlow_open_spec.png
[image_flow_reflash]:attachment/SpecificationsViewFlow_reflash.png


<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother1]:{3}/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_specification]:{3}/IDE/Specification/SpecificationRemarks/README "規格備註"
[link_ruleother11]:{3}/IDE/Specification/RulesOther/README#ruleother11 "共用通則_其它/個資加密提示通則"

[link_ButtonBehavior]:{3}/IDE/Specification/ButtonBehavior/README.md "表單規格定義/按鍵行為選項"
[link_ObjectBehavior]:{3}/IDE/Specification/ObjectBehavior/README.md "表單規格定義/元件行為選項"
[link_AddHiddenObject]:{3}/IDE/Specification/AddHiddenObject/README.md "表單規格定義/新增隱藏元件"
[link_AddHiddenButton]:{3}/IDE/Specification/AddHiddenButton/README.md "表單規格定義/新增隱藏按鍵"
[link_CopyObjectAnnotationForm]:{3}/IDE/Specification/CopyObjectAnnotationForm/README.md "表單規格定義/元件加註複製"
[link_CopyButtonAnnotationForm]:{3}/IDE/Specification/CopyButtonAnnotationForm/README.md "表單規格定義/按鍵加註複製"