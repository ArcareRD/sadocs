# 元件加註-嵌入物件

* ## Web支援版本
  
      8.9.2

* ## APP 支援版本

      1. 008.009.000.069 以上(含)
      2. 行事曆 008.009.000.072 以上(含)
      3. 檔案容器 008.009.000.072 以上(含)
      4. 網頁 008.009.000086 以上(含)

* ## 執行時機

      1. 內容異動
      2. 執行條件異動

* __嵌入物件__
  * 執行條件
    * 無設定
    * 有設定
  * __物件類別__
    * 網頁
      * 內容處理
        * 來源欄位 (該欄位內容為網址)
        * 參數 (會將參數連接在網頁的後頁變成完整網址)
          * 無設定
          * 有設定
    * 檔案容器
      * 內容處理
        * 查表類別
          * 資料表
          * 檢視表
            * 靜態VIEW
            * 動態VIEW & 有參數
        * 來源表格: 檔案容器的資料來源類型
        * 過濾條件
          * 無設定
          * 有設定
        * 檔案唯一號 (存放檔案唯一號的欄位)
        * 編輯狀態
          * 表格類型
            * 資料表
            * 資料暫存表
          * 其他欄位
          * 上傳類型
            * 相機
            * 錄音
            * 相簿
            * 一般檔案
          * 上傳限制
            * 限定筆數 (空白表示無限制)
            * 尺寸介於 (空白表示無限制)
              * 起
              * 迄
            * 檔案介於 (空白表示無限制)
              * 起
              * 迄
        * 瀏覧狀態
          * 限定筆數 (空白表示無限制)
          * 說明欄位 (存放檔案說明資訊的欄位)
          * 顯示預設 (檔案容器顯示檔案的畫面設定)
            * 排序
              * 檔名
              * 時間
              * 類型
            * 排序類型
              * 升冪
              * 降冪
            * 縮圖大小
              * 大
              * 中
              * 小
          * 顯示位置 (當檔案為圖片，被點擊後開啟該檔案明細畫面，圖片資訊要顯示的位置)
            * 無
            * 圖內
            * 圖外
          * 圖片資訊
            * GPS (圖片GPS資訊)
              * 無設定
              * 有設定
                * 位置
                  * 上左
                  * 上中
                  * 上右
                  * 下左
                  * 下中
                  * 下右
            * 時間 圖片建立時間
              * 無設定
              * 有設定
                * 位置
                  * 上左
                  * 上中
                  * 上右
                  * 下左
                  * 下中
                  * 下右
          * 雙擊功能
            * 執行按鍵
            * 選單標題
          * 傳遞變數 (執行雙擊所指定的按鍵之前要寫入的全域變數資訊)
            * 全域變數
            * 資訊欄位
    * 行事曆
      * 內容處理
        * 日曆設定
          * 顯示類型 (預設顯示的類型)
            * 月 (預設)
            * 週
          * 一週首日 (一週的第一天)
            * 星期日 (預設)
            * 星期一
          * 非工作日 (非工作日會標示在行事曆上)
            * 星期日  (預設)
            * 星期一
            * 星期二
            * 星期三
            * 星期四
            * 星期五
            * 星期六  (預設)
          * 預設當日 (開啟表單後，預設駐留在哪天)
            * 系統日期  (預設)
            * 表單參數
            * 全域變數
          * 新增功能 (雙擊/長按 <日期>時，要執行的功能鍵)
            * 無設定
            * 有設定
        * 例假日 (依此設定會將查到的日期，標示在行事曆上)
          * 無設定
          * 有設定
            * 查表類型
              * 資料表
              * 檢視表
                * 靜態VIEW
                * 動態VIEW & 有參數
            * 來源表格
            * 過濾條件
              * 無設定
              * 有設定
            * 日期欄位
            * 名稱欄位
        * 事件 (單擊日期時，依此設定顯示該日的事件清單)
          * 無設定
          * 有設定
            * 查表類別
              * 資料表
              * 檢視表
                * 靜態VIEW
                * 動態VIEW & 有參數
            * 來源表格
            * 過濾條件
              * 無設定
              * 有設定
            * 日期欄位
            * 事件名稱欄位 (顯示在事件清單上的內容)
            * 引用功能 (單擊事件時，要執行的功能鍵)
              * 無設定
              * 有設定
                * 傳遞變數 (呼叫功能鍵前，會將事件的資訊放至全域變數內)
                  * 全域變數
                  * 資訊欄位
            * 排序依據
              * 無設定
              * 有設定
            * 傳遞變數
              * 無設定
              * 有設定
