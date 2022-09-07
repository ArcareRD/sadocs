## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_OperationCodeList]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 由 架構/輔助/AT13.作業代號清單 開啟, 直接開單, 不執行任何動作
* 預設開單角色權限: PM、Site Administrator

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_OperationCodeList_block1]
    * `(1)流程名稱`
        * 用途說明
        * 規格說明
            * 下拉選項: 專案流程清單, 過濾: 駐留專案 且 作業流程=流程, 顯示: 流程名稱
    * `(2)載入`
        * 用途說明
        * 規格說明
            * 當`(1)流程名稱`不為空，過濾: `(1)流程名稱`內容，載入`(1)流程名稱`下的表單及報表清單至`(6)表報作業代號表格`內
            * 當`(1)流程名稱`為空，過濾: 駐留專案，載入專案下的表單及報表清單至`(6)表報作業代號表格`內
    * `(3)自動編碼`
        * 用途說明
            * 依駐留筆的`(9)作業代號`的內容中，最後一碼為數值時，依序編碼給值
        * 規格說明
            * 偵測是否有駐留在`(6)表報作業代號表格`記錄中，當駐留表格記錄，本按鈕致能；否則 本按鈕除能
            * 當`(9)作業代號`的最後一碼不為數值時，顯示訊息盒【標題: 系統訊息 / 內容: 自動編碼只能處理最後編碼為數值型的作業代號。例如: A001、A002、...  / 按鍵: 確定】
                * 確定: 關閉訊息盒
            * 依下列原則進行自動編碼:
                * 取得駐留筆的`(9)作業代號`右側為數值的碼數，即為可編碼的流水號。例如: A001 => 取得可編碼的流水號為3位數；A1 => 取得可編碼的流水號為1位數
                * 依駐留筆下一筆開始，可編碼流水號 + **1**，依序給值，直到流水號用盡，則不繼續編碼                
                * 當 `(5)自動編碼時，已存在作業代號`=保留 且 需編碼的`(9)作業代號`內容為空，則該欄位不給值，跳下一欄位繼續編碼
    * `(4)儲存`
        * 用途說明
            * 依目前載入的表報清單且作業代號不為空者，進行儲存
        * 規格說明
            * 檢查專案下所有的表報，當作業代號重複時，顯示訊息盒【標題: 系統訊息 / 內容: 下列表報的作業代號 [<font color=blue>作業代號內容</font>] 重覆。<font color=blue>換行顯示重複的表報名稱</font> / 按鍵: 確定】
                * 確定: 關閉訊息盒
                * 訊息盒示意圖<br>
                    ![pic][image_saveErrorMsg]
    * `(5)自動編碼時，已存在作業代號`
        * 用途說明
        * 規格說明
            * 單一選項: 覆蓋 / 保留
            * 系統預設: 覆蓋
    * `(6)表報作業代號表格`
        * 用途說明
        * 規格說明
            * 依`(7)表報名稱`+`(8)表報類別`，升冪排序顯示內容    
            * 畫面最多顯示 **15** 筆記錄；當記錄超過 **15** 筆，出現垂直捲軸
    * `(7)表報名稱` 
        * 用途說明
        * 規格說明
            * 本欄唯讀
            * 顯示表單或報表的單元名稱
    * `(8)表報類別`
        * 用途說明
        * 規格說明
            * 本欄唯讀
            * 當`(7)表報名稱`來源為表單，顯示 **表單**
            * 當`(7)表報名稱`來源為報表，顯示 **報表**            
    * `(9)作業代號`
        * 用途說明
        * 規格說明
            * 預設顯示表單或報表的作業代號，可修改





<!-- 圖片 -->
[image_OperationCodeList]:attachment/OperationCodeList.png
[image_OperationCodeList_block1]:attachment/OperationCodeList_block1.png
[image_saveErrorMsg]:attachment/OperationCodeList_saveErrorMsg.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:/8.10.0/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
