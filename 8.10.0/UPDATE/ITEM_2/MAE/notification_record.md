#### <div id="notification">功能項目名稱</div>
  * 推播記錄

#### <div id="user">規劃人員</div>
  * Andy

#### <div id="version">版本記錄</div>
  |日期|版本|備註|
  |---|---|---|
  |2020/11/06|v1|初始化|

#### <div id="trac">TRAC</div>
  * [#8191](http://trac.uneec.com/trac/neco/ticket/8191)

#### <div id="specification">規格說明</div>
  * 列入系統功能
  * 畫面顯示[(表單畫面 推播記錄)](#image_record)
    * 上方工具列
      * 功能名稱
      * 全選未讀/取消全選
    * 過濾工具列
      * 系統名稱
      * 過濾條件
        * 顯示目前選擇的系統過濾條件
        * 進階過濾條件
      * 已讀xx/全部已讀
    * 訊息清單
  * 讀取狀態[(表單畫面 推播記錄)](#image_record)
    * 已讀：淺色顯示
    * 未讀：深色顯示
  * 傳送狀態[(表單畫面 推播記錄)](#image_record)
    * 失敗
      * 顯示傳送失敗及原因同時在主旨後會加上紅色三角警示圖示
  * 功能
    * 上方工具列
      * 全選[(表單畫面 推播記錄)](#image_record)
        * 勾選全部未讀訊息並進入多選模式
        * 過濾條件處顯示全部已讀按鈕
          * 點擊後修改已勾選訊息的狀態為已讀
        * 全選未讀改為取消全選[(表單畫面 選取模式)](#image_selected)
    * 過濾工具列
      * 過濾條件[( 表單畫面 過濾條件 )](#image_filter)
        * 顯示/收起 可設定的過濾條件
          * 系統：全部(預設)/系統清單
          * 發送人：全部(預設)/發送人清單
          * 傳送狀態：全部(預設)/成功/失敗
          * 讀取狀態：全部/已讀(預設)/未讀
          * 日期區間
            * 預設: 全部
            * 自訂
              * 起始日期：未設定時為當日
              * 結束日期：未設定時為當日
        * 確認
          * 依當下所選的過濾條件顯示訊息記錄
      * 已讀xx/全部已讀
        * 點擊
          * 將已勾選的未讀訊息資料傳送給後台
    * [訊息清單](#workflow)
      * 點擊
        * 查看訊息內文
      * 長按
        * 未讀
          * 勾選或取消勾選未讀訊息並進入多選模式或取消多選模式
        * 已讀
          * 無作用

#### <div id="photo">畫面</div>
  * 表單畫面
    * <p id="image_record">推播記錄</p>
    
      ![Notification](./image/notification.jpg)

    * <p id="image_selected">選取模式</p>
    
      ![Notification selected](./image/notification_filter_selected.png)
      ![Notification selected all](./image/notification_filter_selected_all.jpg)
    * <p id="image_filter">過濾條件</p>
    
      ![Notification Filter](./image/notification_filter.png)
  
  * 系統推播記錄查看功能

    ![Notification Record button](./image/notification_record_button.png)

#### <div id="workflow">作業流程</div>

  ![Notification Record](./image/workflow_record.png)

#### <div id="attachment">附件</div>
  * [注意事項](Warning.md)