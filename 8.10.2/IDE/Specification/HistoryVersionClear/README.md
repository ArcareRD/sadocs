## <div id="layout">版面相關</div>
* 版面 <br>
    ![pic][image_historyVersionClear]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 由 架構/輔助工具/AT05.歷史版本資料清除 開啟, 直接開單, 不執行任何動作

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_historyVersionClear_block1]
    * `(1)保留版本數`
        * 用途說明
            * 指定需要保留的版本數量
            * 將發行版號依發行日期降冪排序後，依`(1)保留版本數`取得最近發行的版號，即為本次要保留的版本資料
        * 規格說明
            * 系統預設: 1
            * 數字欄位，系統選取值，最小為 **1**，最大為 **99**
    * `(2)清除`
        * 用途說明
            * 除了要保留的版本數外，刪除其餘版本的發行記錄及歷史規格資料
        * 規格說明
            * 當`(1)保留版本數` 小於 1，顯示訊息盒【標題: 系統訊息 / 內容: 須最少保留1版的歷史資料 / 按鍵: 確定】
                * 確定: 關閉訊息盒
            * 當`(1)保留版本數`留版本數 大於 99，顯示訊息盒【標題: 系統訊息 / 內容: 最多只允許保留99版的歷史資料 / 按鍵: 確定】
                * 確定: 關閉訊息盒
            * 當`(1)保留版本數` 小於等於 目前已發行的版本數時，顯示訊息盒【標題: 系統訊息 / 內容: 專案目前已發行的版本數已小於或等於保留版本數。 / 按鍵: 確定】
                * 確定: 關閉訊息盒
            * 當專案正在發行中，顯示訊息盒【標題: 系統訊息 / 內容: 本專案目前正在進行 [專案發行作業]，作業期間所有相關資料將無法進行異動。不便之處，敬請見諒。 / 按鍵: 確定】
                * 確定: 關閉訊息盒



<!-- 圖片 -->
[image_historyVersionClear]:attachment/historyVersionClear.png
[image_historyVersionClear_block1]:attachment/historyVersionClear_block1.png

<!-- 超連結 -->
[link_ruleother1]:{4}/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
