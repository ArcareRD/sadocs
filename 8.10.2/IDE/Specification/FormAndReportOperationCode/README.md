## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_FormAndReportOperationCode]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 由 架構/專案管理/PM10.表報作業代號 開啟, 直接開單, 不執行任何動作
* 預設開單角色權限: PM、Site Administrator

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_FormAndReportOperationCode_block1]
    * `(1)作業名稱`
        * 用途說明
        * 規格說明
            * 下拉選項: 專案作業清單, 顯示: 作業名稱, 過濾: 駐留專案
    * `(2)載入`
        * 用途說明
        * 規格說明
            * 當`(1)作業名稱`不為空，過濾: `(1)作業名稱`，載入`(1)作業名稱`下的表單及報表清單至`(4)表報作業代號表格`內
            * 當`(1)作業名稱`為空，過濾: 駐留專案，載入專案下的表單及報表清單至`(4)表報作業代號表格`內
    * `(3)儲存`
        * 用途說明
            * 依目前載入的表報清單且作業代號不為空者，進行儲存
        * 規格說明
            * 當同 `(5)表報類別` 下的作業代號重複時，顯示訊息盒【標題: 系統訊息 / 內容: 下列 <font color=blue>表單/報表</font> 的作業代號 [<font color=blue>作業代號內容</font>] 重覆。<font color=blue>換行顯示重複的表報名稱</font> / 按鍵: 確定】
                * 確定: 關閉訊息盒
                * 訊息盒示意圖<br>
                    ![pic][image_saveErrorMsg]
    * `(4)表報作業代號表格`
        * 用途說明
        * 規格說明
            * 依`(5)表報類別`+`(6)表報名稱`，升冪排序顯示內容
    * `(5)表報類別`
        * 用途說明
        * 規格說明
            * 本欄唯讀
            * 當`(6)表報名稱`來源為表單，顯示 **表單**
            * 當`(6)表報名稱`來源為報表，顯示 **報表**
    * `(6)表報名稱`
        * 用途說明
        * 規格說明
            * 本欄唯讀
            * 顯示表單或報表的單元名稱
    * `(7)作業代號`
        * 用途說明
        * 規格說明
            * 預設顯示表單或報表的作業代號，可修改




<!-- 圖片 -->
[image_FormAndReportOperationCode]:attachment/FormAndReportOperationCode.png
[image_FormAndReportOperationCode_block1]:attachment/FormAndReportOperationCode_block1.png
[image_saveErrorMsg]:attachment/FormAndReportOperationCode_saveErrorMsg.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:/8.10.0/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
