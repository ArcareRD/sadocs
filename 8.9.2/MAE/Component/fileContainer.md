* # 元件類型-檔案容器

* ## Web支援版本
  
      8.9.2

* ## APP 支援版本

      008.009.000072 以上(含)

* __檔案容器__
  * __元件代碼__
    * 顯示加註
  * __相依性__
    * 嵌入物件
  * __版面相關__
    * 元件寬高
      * 固定高度
      * 變動高度
      * 當裝置的大小不同時，可能導致元件寬高會改變
    * 元件示意圖
      * 編輯狀態
        * Android
              ![image](./image/android/componentTextEditing.png)
        * IOS
              ![image](./image/ios/componentTextEditing.png)
      * 瀏覧狀態
        * Android
              ![image](./image/android/componentTextEditing.png)
        * IOS
              ![image](./image/ios/componentTextEditing.png)
  * __支援檔案類型__
    * 照片：顯示原圖/GPS/時間(支援格式：bmp/jpg/jpeg/git/png)
    * 音檔：顯示固定圖片(支援音檔格式：mp3)
    * 影片：顯示固定圖片(支援影片格式：mp4)
    * 一般檔案：顯示固定圖片
  * __工具列設定按鈕__：點擊後出現設定畫面，顯示排序方式切換/顯示排序類型切換
    * 圖示大小設定(DKS_表單元件_嵌入物件_內容處理_瀏覧狀態_顯示縮圖大小)：依設定決定顯示圖示大小、一列可顯示檔案數量，每列剩餘空白以平均分散到顯示圖示之間的間距
      * 大：400*400
      * 中：200*200
      * 小：100*100
    * 排序方式設定(DKS_表單元件_嵌入物件_內容處理_瀏覧狀態_顯示排序方式)：依設定決定檔案排序方式的預設值
      * 檔案：使用檔案名稱進行排序
      * 時間：使用檔案最後異動時間進行排序
      * 類型：使用副檔案(不分大小寫)進行排序
    * 排序類型設定(DKS_表單元件_嵌入物件_內容處理_瀏覧狀態_排序類型)：依設定決定檔案排序類型的預設值
      * 升冪：由小到大
      * 降冪：由大到小
  * __每個檔案__
    * 編輯狀態：
      * 單擊：預覧
        * 檔案類型：
          * 照片：顯示原圖/GPS/時間
            * 畫面
              * Android
                    ![image](./image/android/componentTextEditing.png)
              * IOS
                    ![image](./image/ios/componentTextEditing.png)
            * 顯示圖片資訊
              * 顯示位置：
                * 無
                * 照片內
                * 照片外
              * 顯示項目
                * GPS：照片顯示GPS
                * 時間：照片顯示拍攝時間
                      * 註：在相同位置時，GPS位置先顯示
                      * 當上中/下中有放置資訊，且同行的左右右有放置其他資訊時，layout切為三等份
                      * 當同行的左以及右有放置資訊時，layout為二等份
                      * 當同行僅放置一項資訊，layout為100%，依據放置位置將資訊靠左/置中/靠右
                      * 當layout放不下文字時折行
          * 音檔：
            * 工具列(播放/暫停/重播)
            * 畫面
              * Android
                    ![image](./image/android/componentTextEditing.png)
              * IOS
                    ![image](./image/ios/componentTextEditing.png)
          * 影片：
            * 工具列(播放/暫停/重播)
            * 畫面
              * Android
                    ![image](./image/android/componentTextEditing.png)
              * IOS
                    ![image](./image/ios/componentTextEditing.png)
      * 雙擊(長按)：
        1. 刪除功能
           1. 有檔案ID時顯示移除
           2. 無檔案ID且已上傳時顯示重整或不可刪除
           3. 無檔案ID也未上傳時顯示刪除
    * 瀏覧狀態：
      * 單擊：
        * 檔案類型＝一般檔案：直接下載
        * 檔案類型<>一般檔案：開啟播放畫面
          * 照片：顯示原圖/GPS/時間
            * 工具列(下載)
            * 畫面
              * Android
                    ![image](./image/android/componentTextEditing.png)
              * IOS
                    ![image](./image/ios/componentTextEditing.png)
            * 顯示圖片資訊
              * 顯示位置：
                * 無
                * 照片內
                * 照片外
              * 顯示項目
                * GPS：照片顯示GPS
                * 時間：照片顯示拍攝時間
                      * 註：在相同位置時，GPS位置先顯示
                      * 當上中/下中有放置資訊，且同行的左右右有放置其他資訊時，layout切為三等份
                      * 當同行的左以及右有放置資訊時，layout為二等份
                      * 當同行僅放置一項資訊，layout為100%，依據放置位置將資訊靠左/置中/靠右
                      * 當layout放不下文字時折行
          * 音檔：(邊載邊播)
            * 工具列(播放/暫停/重播/下載)
            * 畫面
              * Android
                    ![image](./image/android/componentTextEditing.png)
              * IOS
                    ![image](./image/ios/componentTextEditing.png)
          * 影片：(邊載邊播)
            * 工具列(播放/暫停/重播/下載)
            * 畫面
              * Android
                    ![image](./image/android/componentTextEditing.png)
              * IOS
                    ![image](./image/ios/componentTextEditing.png)
      * 雙擊(長按)：
        1. 將檔案資訊寫入全域變數
        2. 出現選單<干涉.檔案雙擊呼叫功能鍵_項目名稱1~5/檔案雙擊呼叫功能鍵_指定按鍵1~5>
           1. 依照<干涉.檔案資訊_資訊欄位1~12/檔案資訊_寫入全域變數1~12>
        3. 執行選項後：
           1. 註：若只有一個選單項目時，不出現選單
        4. 檢查檔案是否存在，若不存在，則刪除畫面上的該檔案。若存在，則重顯該檔案的資訊。
