## <div id="layout">版面相關</div>
* 版面
    ![pic][image_report]

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">主畫面_工具列說明</p>

    * ![pic][image_report_block1]
    * `(1)規格定義`
        * 用途說明
        * 規格說明
            * Hint: 規格定義
            * 執行開啟[報表規格定義][link_report_annotation], 開啟後, 固定駐留節點:基本設定
        * 動作流程
            * ![pic][image_reportflow_toolbar_open_annotation]
    * `(2)儲存`
        * 用途說明
        * 規格說明
            * 將畫面已設定完成的內容進行儲存
            * 執行完成，重載報表版面，載入完成後顯示訊息盒【標題: 系統訊息 / 訊息內容: 儲存完成 若已開啟該報表規定義, 請至規格定義執行重新整理】，限時: 3秒，系統自動關閉訊息盒
                * 版面區塊 XY軸位置不變
        * 動作流程
            * ![pic][image_reportflow_save_report]

* <p id="fieldbreak2" style="color:blue;font-weight:bold">主畫面_版面區塊說明</p>

    * ![pic][image_report_block2]
    * **版面物件操作說明**
        * 駐留物件=報表元件, 執行右鍵, 顯示右鍵選單 (樣式如上圖所示)
            * 選單順序: 規格定義、規格描述
    * `(1)規格定義`
        * 用途說明
        * 規格說明
            * 當駐留物件執行右鍵, 且 報表元件類型存在【rTP.文字標題、rTF.文字方塊、rTA.多行文字、rCB.核取方塊、rFrame.框線、rBC.條碼、rEChart.嵌入圖表、rImg.圖片、rLogo.企業標誌】顯示, 否則 隱藏
            * 執行開啟[報表規格定義][link_report_annotation], 開啟後, 駐留節點=目前駐留的報表元件
        * 動作流程
            * ![pic][image_reportflow_object_open_annotation]
    * `(2)規格備註`
        * 用途說明
        * 規格說明
            * 開啟[規格備註][link_specification], 傳入: 報表元件名稱、報表料號
        * 動作流程
            * ![pic][image_reportflow_object_open_spec]


<!-- 圖片 -->
[image_report]:attachment/Report.png
[image_report_block1]:attachment/Report_block1.png
[image_report_block2]:attachment/Report_block2.png
[image_reportflow_toolbar_open_annotation]:attachment/ReportFlow_toolbar_open_annotation.png
[image_reportflow_save_report]:attachment/ReportFlow_save_report.png
[image_reportflow_object_open_annotation]:attachment/ReportFlow_object_open_annotation.png
[image_reportflow_object_open_spec]:attachment/ReportFlow_object_open_spec.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"

[link_report_annotation]:../ReportAnnotation/README "報表規格定義"
[link_ruleother1]:/8.10.1/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_specification]:/8.10.1/IDE/Specification/SpecificationRemarks/README "規格備註"
