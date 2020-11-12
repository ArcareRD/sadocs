## <div id="user">規劃人員</div>
  * Andy

## <div id="updatedate">規劃日期</div>
  * 2020/11/06

## <div id="trac">TRAC</div>
  * 待補

#### <div id="notification_system">系統管理<path>(推播通知)</path></div>
* 擴充
* 規格說明
    * 裝置在背景/前景或未開啟的狀態下可接收系統收到的通知
    * 在點擊系統通知時處理相對應功能
      1. [表單連結](notification_formlink.md)
        * 開啟對應表單(需登入)
      2. [按鍵連結](notification_buttonlink.md)
        * 執行特定表單的按鍵功能
      3. [超連結](notification_hyperlink.md)
        * 開啟對應網址
        * 連結 google 行事曆(需登入 google 帳號)
      4. [推播記錄](notification_record.md)
        * 顯示所有推播訊息
      5. [推播訊息](notification_message.md)
        * 顯示推播訊息
* 通知畫面(系統)
  * Android

    ![Notification android](./image/notification_android.jpg)
  
  * iOS
  
    ![Notification ios](./image/notification_ios.png)

* 畫面說明
  * 標題(藍色框表示)：通知的標題。
    * 超過長度則顯示省略符號...
      * ios約34個字以上
      * android約41個字以上
      * 實際長度依裝置不同會有不同字數
  * 內容(紅色框表示)：通知的內容。
    * 超過長度則顯示省略符號...
      * ios約147個字以上
      * android
        * 未展開約43個字以上
        * 展開約611個字以上
      * 實際長度依裝置不同會有不同字數
  * 點擊
    * 點擊系統通知會呼叫MAE APP，APP啟動後會顯示通知內容及連結類型，點擊連結會依連結類型來處理相對應事件。

* 作業流程

  ![Notification System](./image/workflow_system.png)
