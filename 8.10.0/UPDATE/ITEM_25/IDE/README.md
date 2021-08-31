### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2021/08/23

### <div id="trac">TRAC</div>
* #8627 

### <div id="requirement">需求展開</div>
* 元件加註_選項清單: 當設計類型=RWD、APP時, 擴充下列項目
    * (修)選擇筆數: 原固定式下拉的單選、複選, 改為下拉式也支援
        * 固定式更名為清單式
        * 原專案存在下拉式, 轉資料: 選擇筆數=單選, 並產生changelog
    * (增)查詢轉換欄位: 只允挑選同駐留元件檔區的元件, 可空值, 須為文字型態
    * (修)變動選項表格: 來源欄位及帶回對應元件須為文字型態
    * (修)駐留筆元件, 若為固定式下拉須為文字型態
* 單元樣式、主題樣式: 元件類型=wDL.下拉選項, 增加多選狀態樣式, 如下:
    * RWD: 
        * (RWD)多選致能Enable_Multi【狀態代碼: mobile_Enable_Multi】
            * 主題樣式轉資料: 
                * 框線: mobile_ItemList 光棒的框線
                * 底色: mobile_ItemList 光棒的底色
                * 內容: mobile_Enable 內容
        * (RWD)多選顯示致能DisplayEnable_Multi【狀態代碼: mobile_DisplayEnable_Multi】
            * 主題樣式轉資料: 
                * 框線: mobile_ItemList 光棒的框線
                * 底色: mobile_ItemList 光棒的底色
                * 內容: mobile_DisplayEnable 內容
    * APP:  
        * (APP)多選致能Enable_Multi【狀態代碼: Apps_Enable_Multi】
        * (APP)多選顯示致能DisplayEnable_Multi【狀態代碼: Apps_DisplayEnable_Multi】
        * (APP)選項清單ItemList【狀態代碼: Apps_ItemList】
* 複製本次擴充的欄位
    * 規格複製
    * 跨專案複製
* 單元檢錯
* 規格書產出
    


