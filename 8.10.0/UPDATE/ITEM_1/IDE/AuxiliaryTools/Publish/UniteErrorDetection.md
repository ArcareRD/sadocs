### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/12/3


## <div id="layout">版面相關</div>
* 版面
    ![pic][image_UniteErrorDetection]


## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

* ![pic][image_Annotation_Notice_Block1]
    * `(1)檢錯類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 表單 / 報表 / 資料交易 / 離線資料交易 / 資料表 / 檢視表
    * `(2)檢錯項目`
        * 用途說明
        * 規格說明
    * `(3)全階展開`
        * 用途說明
        * 規格說明
            * 依`(2)檢錯項目`為父階, 展開所有跟檢錯有關的單元階層, 並以樹狀方式回傳展開結果寫入`(5)展開內容`
    * `(4)執行`
        * 用途說明
        * 規格說明
            * 依`(2)檢錯項目`為父階, 展開所有跟檢錯有關的單元階層, 進行檢錯. 將檢錯結果寫入`(6)結果`, 並針對錯誤的內容, 提供超連結的功能
    * `(5)展開內容`
        * 用途說明
        * 規格說明
            * 顯示`(3)全階展開`的結果
    * `(6)結果`
        * 用途說明
        * 規格說明
            * 顯示`(4)執行`的結果





<!-- 圖片 -->
[image_UniteErrorDetection]:attachment/UniteErrorDetection.png


<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"