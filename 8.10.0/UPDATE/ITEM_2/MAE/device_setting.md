#### 功能項目名稱
  * <div id="device_setting">推播通知問題需知</div>

#### <div id="user">規劃人員</div>
  * Andy

#### <div id="version">版本記錄</div>
  |日期|版本|備註|
  |---|---|---|
  |2021/02/26|v1|初始化|

#### <div id="specification">問題說明</div>
  * 問題 1：APP安裝完後無法收到通知
    * APP在安裝完後需要先執行過一次，且需要正常登入後才能接到通知
  * 問題 2：APP在背景時無法收到通知
    * APP未收到通知時可以先確認是否有在背景執行
      * 確認範例
        * 裝置：ASUS ZenFone 3 ZE552KL
        * Android 版本：8.0.0
        * <p id="asus_searching">Step 1: 開啟所有應該程式頁面 - 桌面往上滑</p>
        
        * <p id="asus_searching_all_setting">Step 2: 搜查設定 - 點擊查尋功能</p>
          
          ![Asus Searching all setting](./image/asus_all_apps.jpg)
        * <p id="asus_searching_setting">Step 3: 搜查設定 - 點擊查尋功能</p>
          
          ![Asus Searching Setting](./image/asus_searching_setting.jpg)
        * <p id="asus_setting_app">Step 4: 設定 - 點擊"應用程式與通知"</p>
          
          ![Asus Setting app](./image/asus_setting_app.jpg)
        * <p id="asus_app_info_settings">Step 5: 應用程式與通知 - 點擊"應用程式資訊"</p>
          
          ![Asus app info settings](./image/asus_app_info_settings.jpg)
        * <p id="asus_app_info">Step 6: 應用程式資訊 - 點擊"ruRU MAE"</p>
          
          ![Asus app info](./image/asus_app_info.jpg)
        * <p id="asus_app_service_running">Step 7: 應用程式資訊 ruRU MAE - 背景已執行</p>
          
          ![Asus app service running](./image/asus_app_service_running.jpg)
          * <p id="asus_app_service_closed">背景未執行時會無法接收通知</p>
          
            ![Asus app service closed](./image/asus_app_service_closed.jpg)
  * 問題 3：APP未執行時無法收到通知
    * 部份裝置若有電源管理設定，需手動設定APP為自啟動，否則在APP未執行時無法接收到通知
    * 設定範例：
      * 裝置：ASUS ZenFone 3 ZE552KL
      * Android 版本：8.0.0
      * <p id="asus_all">Step 1: 開啟所有應該程式頁面 - 桌面往上滑</p>
      * <p id="asus_all_apps">Step 2: 搜查電源管理程式 - 點擊查尋功能</p>
          
        ![Asus all apps](./image/asus_all_apps.jpg)
      * <p id="asus_clever">Step 3: 查找並開啟 - 智能管家</p>
          
        ![Asus clever](./image/asus_searching_app.jpg)
      * <p id="asus_clever_power">Step 4: 打開電力設定 - 電力逹人</p>
          
        ![Asus clever power](./image/asus_clever_power.jpg)
      * <p id="asus_clever_power_battery">Step 5: 打開自啟動設定 - 自啟動管理</p>

        ![Asus clever power battery](./image/asus_clever_power_battery.jpg)
      * <p id="asus_clever_power_battery_restart">Step 6: 開啟APP的自啟動 - ruRU MAE</p>

        ![Asus clever power battery restart](./image/asus_clever_power_battery_restart.jpg)

