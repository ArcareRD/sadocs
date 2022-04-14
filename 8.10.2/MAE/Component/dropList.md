# 元件類型-下拉選項

* ## Web支援版本
  
      8.9.2

* ## APP 支援版本

      008.010.001062 以上(含)

* __下拉選項__
  * __元件代碼__
    * wDL
  * __相依性__
    * 獨立元件
  * __版面相關__
    * 元件寬高
      * 高度(px)
        * 當變動高度＝是時，表示最小高度。
        * 不含<外邊距>的上邊距/下邊距：(DKS_單元樣式_外邊距_上邊距/下邊距)
      * 變動高度
        * 當變動高度＝否時
          * 內容永遠為一行
          * 內容超出顯示...
          * [元件高度不足](../general/rule)
        * 當變動高度＝是時
          * 元件可能因<標題區>或<內容區>撐高，但會有最小高度
          * [內容超出折行](../general/rule)
      * 寬度(%)
        不含 <外邊距>的左邊距/右邊距：(DKS_單元樣式_外邊距_左邊距/右邊距)
      * 當裝置的大小不同時，可能導致元件寬高會改變
    * 元件示意圖
      * 單選
        * Android
        
          ![AndroidDropListSearchDisplay]
        
          ![AndroidDropListSearchEditing]
        
          ![AndroidDropListSearchFilter]
        
        * IOS

          ![IosDropListSearchDisplay]

          ![IosDropListSearchEditing]

          ![IosDropListSearchFilter]
      * 多選
        * Android
        
          ![AndroidDropListMultiSearchDisplay]
        
          ![AndroidDropListMultiSearchEditing]
        
          ![AndroidDropListMultiSearchFilter]
        
        * IOS

          ![IosDropListMultiSearchDisplay]

          ![IosDropListMultiSearchEditing]

          ![IosDropListMultiSearchFilter]
    * 工作流程
      * 單選
        ![workflow_droplist]
      * 多選
        ![workflow_droplist_multi]
    * [樣式](../general/style)
      * 致能(Enable)
      * 顯示致能(Display Enable)
      * 標題(Title)
      * 光棒：下拉清單選取的元件
  * __加註__
    * - [x] [基本設定](../Addition/Component/basicSettings)
    * - [x] [預設給值](../Addition/Component/defaultValue)
    * - [x] [更新給值](../Addition/Component/updateValue)
    * - [x] [被動更新](../Addition/Component/passiveUpdate)
    * - [x] [編輯能力](../Addition/Component/editing)
    * - [x] [顯示設定](../Addition/Component/display)
    * - [x] [檢控限制](../Addition/Component/prosecutionRestrictions)
    * - [ ] [嵌入物件](../Addition/Component/embedded)
    * - [x] [選項清單](../Addition/Component/optionalList) (必要項)
  * __行為__
    * 受權限保護元件
      - [x] [支援](../general/rule)
      - [ ] 不支援
    * 對應檔區：
      * DKS_表單元件_基本設定_存在檔區
    * 對應欄位：
      * DKS_表單元件_基本設定_檢視表對應欄位
      * 支援欄位型態：文字/整數/數字/日期/日期時間/全唯碼
    * 顯示巨集：
      - [ ] 支援
      - [x] 不支援
    * [模版](../general/model)：
      - [x] 支援
      - [ ] 不支援
    * 提示：
      - [ ] 支援
      - [x] 不支援
    * 錯誤顯示：顯示在元件下方
      - [x] 支援
      - [ ] 不支援
    * 資料過濾：對應欄位
    * 資料搜尋：對應欄位
    * 編輯模式：
      * 樣式
        * 變動高度＝否
        * 變動高度＝是
      * 元件唯讀：(DKS_資料元件_編輯能力_可編欄位_唯讀)
        * 不允許開啟<下拉清單>
      * 內容
      * 開啟下拉清單：(DKS_表單元件_選項清單)
        * 畫面
        * 規則
              當元件於<瀏覧模式>時，無法開啟
              當元件唯讀時，無法開啟
              不能有<執行條件>不成立的狀況：<DKS_選項清單_執行條件>
              下拉選項出現後，點選其他區域，會自動關閉下拉選項
        * 下拉選項的組成
          * 固定選項：(DKS_表單元件_選項清單_固定項次)
            | 類型 | 格式 |
            | --- | --- |
            | 有代號、名稱 | 代號.名稱(以點(.)分隔) |
            | 只有代號 | 代號 |
          * 變動選項：(DKS_表單元件_選項清單_變動項次)
            * 有代號、名稱：(DKS_表單元件_選項清單_帶回對應元件：存在<要顯示＝是 且帶回對應元件<>本元件>)
              * 格式：<對應欄位>對應的<來源欄位>(會套<顯示模版>)+點(.)+DKS_選項清單_來源欄位(要顯示＝Y + 帶回對應元件<>本元件)
                * 帶回對應元件<>本元件：
                  * 若有多個會用底線(_)分隔
                  * 顯示格式
                    | 欄位型態 | 去空白 | 特殊格式 |
                    | --- | --- | --- |
                    | 字串 | 是 | |
                    | 日期/日期時間 | 是 | `yyyy/MM/dd hh:mm:ss.SSS` (yyyy：西元(4碼)/MM：月(2碼)/dd：日(2碼)/hh：時(2碼)/mm：分(2碼)/ss：秒(2碼)/SSS：毫秒(3碼)) |
                    | 數字 | 是 | 轉文字 |
                    | 邏輯 | 是 | 當為true，顯示1。否則顯示0 |
            * 只有代號：(DKS_表單元件_選項清單_帶回對應元件：不存在<要顯示＝是 且帶回對應元件＝不含本欄位>)
              * 格式：<對應欄位>對應的<來源欄位>(會套<顯示模版>)
        * 強制重顯：(DKS_表單元件_選項清單_強制重新載入)
          * 時機：開啟下拉清單
                1. 若有設定時，會每次重新查詢下拉選項
                2. 若沒設定時，若之前已經查過的話不會重新查詢，當SELECT子句改變才會重新查詢。
    * 瀏覧模式：
      * 樣式
        * 變動高度＝否
        * 變動高度＝是
      * 內容：同下拉選項的組成
      * 顯示樣式：(DKS_表單元件_顯示設定_顏色)
        * 字體顏色、背景顏色
    * 開單隱藏：
      - [ ] 支援
      - [x] 不支援
    * 資料隱藏：
      - [x] 支援
      - [ ] 不支援
    * 元件隱藏：
      - [x] 支援
      - [ ] 不支援
    * 元件除能：
      - [ ] 支援
      - [x] 不支援
    * 元件駐留：
      - [ ] 支援
      - [x] 不支援
        * 元件跳離 (選項值異動時)
          1. 若輸入內容與原值相同時，不會再執行後續的動作
          2. 檢查資料的正確性
             * 若條件不成立時，顯示[錯誤訊息](../general/rule)，並回復原值，駐留在該元件上
             1. 系統檢查
               * [空白檢查](../Addition/component/basicSettings)
               * 各種欄位型態的檢查
                 | 組裝欄位型態 | 檢查項目 |
                 | --- | --- |
                 | 01.Unicode字串(固定長度) | 無 |
                 | 13.Unicode字串(可變長度) | |
                 | 14.字串(固定長度) | |
                 | 15.字串(可變長度) | |
                 | 10.Unicode備註 | 無 |
                 | 17.備註 | |
                 | 04.int | 無|
                 | 05.smallint | |
                 | 06.tinyint | |
                 | 16.bigint | |
                 | 07.數字 | |
                 | 08.金額 | |
                 | 02.日期 | 符合日期格式：※輸入有誤※日期輸入不合法！ |
                 | 03.日期時間 | 日期須大於1900/01/01且小於2079/06/06：※輸入有誤※日期超出範圍！ |
                 | 11.全唯碼 | 符合全唯碼格式：※輸入有誤※輸入格式不合法！ |
             2. 設計者定義的檢查
               * [檢控限制](../Addition/component/prosecutionRestrictions)
               * 錯誤訊息類型：(DKS_表單元件_檢控限制_異常類別)
                 * 錯誤：(DKS_表單元件_檢控限制_異常類別_錯誤)
                 * 警告：(DKS_表單元件_檢控限制_異常類別_警告)
                 * 詢問：(DKS_表單元件_檢控限制_異常類別_操作者決定)
          3. 寫入對應欄位
          4. [更新相關值](../Addition/component/updateValue)
          5. [它欄更新](../Addition/component/passiveUpdate)
          6. 存後：(DKS_表單元件_更新給值：ENG.存後)
          7. 重顯相關元件
          8. 跳至另一元件
    * 操作：
    
      * 編輯狀態下
        * 點擊
              開啟下拉清單
        * 點擊空白
              關閉下拉清單
        * 點擊確定按鈕
              異動下拉內容
        * 點擊取消按鈕
              關閉下拉清單
        * <p id="search_filter">關鍵字過濾</p>
        
              可依輸入字為關鍵字來和伺服器再查詢目前下拉選項(單選/多選)的資料
              過濾規則依設定分為 開頭是/結尾是/相似於，預設：開頭是
              若有設定模版的限定大寫則輸入格式會限定在大寫

<!-- 圖示_介面 -->
[AndroidDropListSearchDisplay]:image/android/componentDropListSearchDisplay.jpg "Android 下拉選項-單選"
[AndroidDropListSearchEditing]:image/android/componentDropListSearchEditing.jpg "Android 下拉選項-單選 關鍵字輸入"
[AndroidDropListSearchFilter]:image/android/componentDropListSearchFilter.jpg "Android 下拉選項-單選 關鍵字過濾"
[IosDropListSearchDisplay]:image/IOS/componentDropListSearchDisplay.PNG "IOS 下拉選項-單選"
[IosDropListSearchEditing]:image/IOS/componentDropListSearchEditing.PNG "IOS 下拉選項-單選 關鍵字輸入"
[IosDropListSearchFilter]:image/IOS/componentDropListSearchFilter.PNG "IOS 下拉選項-單選 關鍵字過濾"

[AndroidDropListMultiSearchDisplay]:image/android/componentDropListMultiSearchDisplay.png "Android 下拉選項-多選"
[AndroidDropListMultiSearchEditing]:image/android/componentDropListMultiSearchEditing.png "Android 下拉選項-多選 關鍵字輸入"
[AndroidDropListMultiSearchFilter]:image/android/componentDropListMultiSearchFilter.png "Android 下拉選項-多選 關鍵字過濾"
[IosDropListMultiSearchDisplay]:image/IOS/componentDropListMultiSearchDisplay.PNG "IOS 下拉選項-多選"
[IosDropListMultiSearchEditing]:image/IOS/componentDropListMultiSearchEditing.PNG "IOS 下拉選項-多選 關鍵字輸入"
[IosDropListMultiSearchFilter]:image/IOS/componentDropListMultiSearchFilter.PNG "IOS 下拉選項-多選 關鍵字過濾"

[workflow_droplist]: image/workflow_droplist.png "下拉選項-單選 工作流程"
[workflow_droplist_multi]: image/workflow_droplist_multi.png "下拉選項-多選 工作流程"

<!-- 超連結 -->
