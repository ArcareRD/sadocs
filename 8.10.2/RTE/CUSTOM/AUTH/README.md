# RTE 授權資料產生程式

### <div id="readrte">RTE讀取主機資訊</div>
* 獨立單機程式
* 僅針對目前前已有客戶要更新引擎時產生授權檔案用
* 由客戶端主機資料產生授權資訊，提供給單機授權程式產生RTE授權檔案
  
### <div id="func">功能說明 <path>RTE讀取主機資訊</path></div>
* 執行流程
  * 執行程式
    * 挑選Tomcat安裝目錄
    * 讀取主機資訊
    * 讀取RTE設定資訊
    * 讀取站台資料庫資訊並產生站台授權檔案
    * 取得各企業系統資訊並產生系統授權檔案
    * 將產生的檔案壓縮成zip檔案

### <div id="view">畫面 <path>RTE讀取主機資訊</path></div>
![畫面]

* 上述畫面個欄位說明如下
  * 按鈕.挑選Tomcat安裝目錄
    * 點擊後執行以下動作
      * 跳出檔案總管，挑選Tomcat安裝目錄
      * 偵測挑選的目錄下的 conf 資料夾下是否有 ArcareEng.xml 檔案
        * 若沒有則跳出錯誤訊息【該Tomcat資料夾下並沒有安裝RTE】
    * 除致能條件 = 挑選目錄後可以在 Tomcat安裝目錄/conf 資料夾下讀取到 ArareEng.xml 檔案
      * 有讀取到檔案時，本按鈕除能
      * 尚未讀取到時，本按鈕致能
  * 按鈕.產生RTE主機資訊檔案
    * 點擊後依據讀取到的 ArcareEng.xml 進行以下動作
      * 讀取主機資訊
      * 讀取站台資料庫資訊並產生站台授權檔案
        * 授權類型固定為同時連線數
        * 授權人數固定為300
      * 取得各企業系統資訊並產生系統授權檔案
        * 授權類型固定為同時連線數
        * 授權人數固定為300
      * 將產生的檔案壓縮成zip檔案
    * 除致能條件 = 是否已正確讀取到 ArareEng.xml 檔案
      * 有讀取到檔案時，本按鈕致能
      * 尚未讀取到時，本按鈕除能
  * 按鈕.匯入License檔案
    * 點擊後進行以下動作
      * 跳出檔案總管，挑選授權中心客製程式產生的授權壓縮檔案
      * 更新授權資訊到站台資料庫中
    * 除致能條件 = 是否已正確讀取到 ArareEng.xml 檔案
      * 有讀取到檔案時，本按鈕致能
      * 尚未讀取到時，本按鈕除能
  * 欄位.狀態紀錄備註
    * 文字型態欄位
    * 操作上述兩個按鈕時的狀態紀錄會顯示於本欄位

### <div id="auth">授權中心產生授權資料</div>
* 獨立單機程式
* 僅針對目前前已有客戶要更新引擎時產生授權檔案用
* 讀取RTE讀取主機資訊所產生的站台資料進行以下動作
  * 寫入授權中心資料
  * 產生離線啟動授權檔案
  
### <div id="func">功能說明 <path>授權中心產生授權資料</path></div>
* 執行流程
  * 執行程式
    * 挑選Tomcat安裝目錄
    * 讀取主機資訊
    * 讀取授權中心設定資訊
    * 寫入授權中心資料
    * 產生離線啟動授權檔案

### <div id="view">畫面 <path>授權中心產生授權資料</path></div>
![授權程式畫面]

* 上述畫面個欄位說明如下
  * 按鈕.挑選Tomcat安裝目錄
    * 點擊後執行以下動作
      * 跳出檔案總管，挑選Tomcat安裝目錄
      * 偵測挑選的目錄下的 conf 資料夾下是否有授權中心網站設定檔案
        * 若沒有則跳出錯誤訊息【該Tomcat資料夾下並沒有安裝授權中心網站】
    * 除致能條件 = 挑選目錄後可以在 Tomcat安裝目錄/conf 資料夾下讀取到授權中心網站設定檔案
      * 有讀取到檔案時，本按鈕除能
      * 尚未讀取到時，本按鈕致能
  * 按鈕.挑選RTE主機授權壓縮檔
    * 點擊後執行以下動作
      * 跳出檔案總管，挑選RTE主機授權壓縮檔
    * 除致能條件 = 挑選RTE主機授權壓縮檔
      * 有讀取到檔案時，本按鈕除能
      * 尚未讀取到時，本按鈕致能
  * 欄位.授權類型
    * 單選欄位
    * 除致能條件 = 是否已正確讀取到授權中心網站設定檔案 AND 讀取到RTE主機授權壓縮檔
      * 上述條件成立，本欄位致能
    * 選項如下 :
      * 同時連線 : 該選項為預設值
      * 雲端授權
  * 欄位.客戶統一編號
    * 除致能條件 = 是否已正確讀取到授權中心網站設定檔案 AND 讀取到RTE主機授權壓縮檔
      * 上述條件成立，本欄位致能
  * 按鈕.產生離線授權啟用檔案
    * 點擊後依據讀取到的授權中心網站設定檔案進行以下動作
      * 產生授權紀錄
      * 產生站台離線授權檔案
      * 產生各企業系統離線授權檔案
      * 將上述檔案壓縮成ZIP檔案
    * 除致能條件 = 是否已正確讀取到授權中心網站設定檔案 AND 讀取到RTE主機授權壓縮檔 AND 欄位.客戶統一編號不為空
      * 上述條件成立，本按鈕致能
  * 欄位.狀態紀錄備註
    * 文字型態欄位
    * 操作上述兩個按鈕時的狀態紀錄會顯示於本欄位

[畫面]:attachment/view.png "畫面"
[授權程式畫面]:attachment/auth_view.png "授權程式畫面"