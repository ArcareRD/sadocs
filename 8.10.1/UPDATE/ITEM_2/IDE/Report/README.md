## <div id="layout">版面相關</div>
* 版面
    ![pic][image_report]

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">主畫面_工具列說明</p>

    * ![pic][image_report_block1]
    * `(1)規格定義`
        * 用途說明
        * 規格說明
            * 執行開啟[報表規格定義][link_report_annotation], 開啟後, 固定駐留節點:基本設定
    * `(2)儲存`
        * 用途說明
        * 規格說明
            * 執行完成，重載報表版面，載入完成後顯示訊息盒【標題: 系統訊息 / 訊息內容: 儲存完成 若已開啟該報表規定義, 請至規格定義執行重新整理】，限時: 3秒，系統自動關閉訊息盒
                * 版面區塊 XY軸位置不變

* <p id="fieldbreak2" style="color:blue;font-weight:bold">主畫面_版面區塊說明</p>

    * ![pic][image_report_block2]
    * `(1)規格定義`
        * 用途說明
        * 規格說明
            * 當駐留物件執行右鍵, 且 報表元件類型存在【rTP.文字標題、rTF.文字方塊、rTA.多行文字、rCB.核取方塊、rFrame.框線、rBC.條碼、rEChart.嵌入圖表、rImg.圖片、rLogo.企業標誌】顯示, 否則 隱藏
            * 執行開啟[報表規格定義][link_report_annotation], 開啟後, 駐留節點=目前駐留的報表元件


<!-- 圖片 -->
[image_report]:attachment/Report.png
[image_report_block1]:attachment/Report_block1.png
[image_report_block2]:attachment/Report_block2.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"

[link_report_annotation]:../ReportAnnotation/README "報表規格定義"
[link_ruleother1]:/8.10.1/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
