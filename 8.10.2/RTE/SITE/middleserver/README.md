# RTE Site 服務中間台

### <div id="view">畫面</div>

![畫面]

* 上述畫面各欄位說明如下 :
  * 表格.中間台清單
    * 按鈕.新增 : 點擊後，於表格新增一筆紀錄，並將該筆紀錄進入修改狀態，如下圖所示
      * ![新增畫面]
    * 欄位.伺服器 : 表示中間台位置，建議填寫主機電腦名稱
      * 文字類型欄位
      * 必要欄位
    * 欄位.連接埠 : 表示該中間台開放連接埠，依據該主機安裝的Tomcat連接埠
      * 文字型態欄位
      * 必要欄位
    * 欄位.處理排程 : 表示該中間台為處理排程的機台，當有多台中間台時，僅設定處理排程的中間台會執行排程
      * 單選欄位
      * 非必要欄位
    * 按鈕.修改 : 
      * 點擊後，執行以下動作
        * 將該筆中間台資料進入修改狀態
        * 將其他筆中間台資料的所有按鈕除能
      * 除致能條件 :
        * 當紀錄為瀏覽狀態時致能
        * 當紀錄為修改狀態時除能
    * 按鈕.刪除 : 點擊後，執行以下動作
      * 該筆中間台資料是否設定為處理排程
        * 若是則跳出訊息【當處理排程=Y時，不允執行刪除】
      * 跳出詢問訊息【是否確定刪除該筆中間台資訊?】
        * 確定刪除則刪除該筆中間台資訊並重顯表格畫面
      * 除致能條件 :
        * 當紀錄為瀏覽狀態時致能
        * 當紀錄為修改狀態時除能
    * 按鈕.儲存
      * 檢查上述必要欄位是否不為空
        * 若為空則顯示錯誤訊息
      * 儲存該筆中間台資訊後重新顯示表格畫面
      * 除致能條件 :
        * 當紀錄為修改狀態時致能
        * 當紀錄為瀏覽狀態時除能
    * 按鈕.取消
      * 點擊後，取消修改狀態，回到瀏覽狀態
      * 除致能條件 :
        * 當紀錄為修改狀態時致能
        * 當紀錄為瀏覽狀態時除能

### <div id="flow">動作流程</div>

* 點擊按鈕.新增
  * ![點擊按鈕.新增]
* 點擊按鈕.修改
  * ![點擊按鈕.修改]
* 點擊按鈕.刪除
  * ![點擊按鈕.刪除]
* 點擊按鈕.儲存
  * ![點擊按鈕.儲存]
* 點擊按鈕.放棄
  * ![點擊按鈕.放棄]

[畫面]:attachment/view.png "畫面"
[新增畫面]:attachment/view1.png "新增畫面"
[點擊按鈕.新增]:attachment/click_add.png "點擊按鈕.新增"
[點擊按鈕.修改]:attachment/click_update.png "點擊按鈕.修改"
[點擊按鈕.刪除]:attachment/click_delete.png "點擊按鈕.刪除"
[點擊按鈕.儲存]:attachment/click_save.png "點擊按鈕.儲存"
[點擊按鈕.放棄]:attachment/click_cancel.png "點擊按鈕.放棄"