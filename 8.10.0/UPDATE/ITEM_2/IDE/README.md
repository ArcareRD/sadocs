### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/04

### <div id="trac">TRAC</div>
* #8193 

### <div id="requirement">需求展開</path></div>
* 規格說明
    * 提供STD、RWD及非離線用APP表單, 推播通知設計介面
    * 通知內容, 不支援 HTML語法、插入圖片、連結字變數
    * 加註方式參考<按鍵加註-郵件發送>, 無夾檔附件、無副本、無密件副本
    * 推播通知支援連結項目: 開啟MAE表單、執行開放按鍵、連結Google行事曆、連結網址
    * 因應連結網址需求, <運算式>需增加上層表格加註方式
* 規劃項目展開
    * 按鍵加註
        * IDE_按鍵行為選項, 新增行為選項: 推播通知
        * IDE_按鍵加註, 新增<推播通知>
    * 運算式, 增加上層表格加註方式
    * 開放按鍵, 增加支援按鍵行為:推播通知 (2020-12-01 擴增項目, 尚未規劃)
    * 影響修改
        * 發行檢錯
        * 加註複製
        * 規格書
		* 傳遞參數
		* 替代訊息
		* 條件式
* 作業流程
    * ![pic][imAge_Workflow]

<!-- 圖片 -->
[image_Workflow]:attachment/IDE_MAENotice.png