# 元件類型-畫布

* ## Web支援版本
  
      8.9.2

* ## APP 支援版本

      008.009.000069 以上(含)

* __畫布__
  * __元件代碼__
    * wCanvas
  * __相依性__
    * 獨立元件
  * __版面相關__
    * 元件寬高
      * 高度(px)
        * 當變動高度＝是時，表示最小高度。
        * 不含<外邊距>的上邊距/下邊距：(DKS_單元樣式_外邊距_上邊距/下邊距)
      * 變動高度
        * 當變動高度＝否時
          * [元件高度不足](../general/rule)
        * 當變動高度＝是時
          * 元件可能因<標題區>或<內容區>撐高，但會有最小高度
      * 寬度(%)
        不含 <外邊距>的左邊距/右邊距：(DKS_單元樣式_外邊距_左邊距/右邊距)
      * 當裝置的大小不同時，可能導致元件寬高會改變
    * 元件示意圖
      * Android
            ![image](./image/android/componentTextEditing.png)
      * IOS
            ![image](./image/ios/componentTextEditing.png)
    * [樣式](../general/style)
      * 致能(Enable)
      * 標題(Title)
  * __加註__
    * - [x] [基本設定](../Addition/component/basicSettings)
    * - [x] [預設給值](../Addition/component/defaultValue)
    * - [x] [更新給值](../Addition/component/updateValue)
    * - [x] [被動更新](../Addition/component/passiveUpdate)
    * - [x] [編輯能力](../Addition/component/editting)
    * - [x] [顯示設定](../Addition/component/display)
    * - [x] [檢控限制](../Addition/component/prosecutionResstrucson)
    * - [ ] [嵌入物件](../Addition/component/embedded)
    * - [ ] [選項清單](../Addition/component/optionList)
  * __行為__
    * 受權限保護元件：內容區會顯示(受保護元件)的字樣(Trac #7477)
      - [x] [支援](../general/rule)
      - [ ] 不支援
    * 對應檔區：
      * DKS_表單元件_基本設定_存在檔區
    * 對應欄位：
      * DKS_表單元件_基本設定_檢視表對應欄位
      * 支援欄位型態：二進位
    * 顯示巨集：
      - [ ] 支援
      - [x] 不支援
    * 模版：
      - [ ] 支援
      - [x] 不支援
    * 提示：
      - [ ] 支援
      - [x] 不支援
    * 錯誤顯示：
      - [ ] 支援
      - [x] 不支援
    * 資料過濾：
      - [ ] 支援
      - [x] 不支援
    * 資料搜尋：
      - [ ] 支援
      - [x] 不支援
    * 編輯模式：
      * 樣式
        * 右上方會有X：清空內容
        * 內容依<寛度/高度>比例縮放
      * 內容：對應欄位
      * 元件唯讀：不支援
    * 瀏覧模式：
      * 樣式
        * 內容依<寛度/高度>比例縮放
      * 內容：對應欄位
      * ~顯示樣式：(DKS_表單元件_顯示設定_顏色)~ 不支援
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
      - [x] 支援
      - [ ] 不支援
        * 元件駐留
          * 除了預設處理外，會再多執行下列項目：當在編輯模式下，會清空內容。
        * 元件跳離
          1. 檢查資料的正確性
             * 檢查值：byte[](若沒有畫的話，為null)
             * 若條件不成立時，顯示錯誤訊息，共回復原值，駐留在該元件上
             * 系統檢查
               * [空白檢查](../Addition/component/basicSettings)
             * 設計者定義的檢查
               * [檢控限制](../Addition/component/prosecutionRestrictions)
               * [不可重複](../Addition/component/basicSettings)
               * [不可負值](../Addition/component/basicSettings)
          2. 寫入對應欄位
          3. [更新相關值](../Addition/component/updateValue)
          4. [它欄更新](../Addition/component/passiveUpdate)
          5. [存後](../Addition/component/updateValue)
          6. 重顯相關元件
          7.  跳至另一元件
    * 操作：
      * 點擊並移動 (編輯狀態下)
    * 橫直屏轉換：
      * 放編輯模式下，依照原本的畫的內容進行旋轉，不進行任何縮放，由使用者自行確認是否需要重新
