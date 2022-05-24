# 元件類型-多行文字

* ## Web支援版本
  
      8.9.2

* ## APP 支援版本

      008.009.000.001 以上(含)

* __多行文字__
  * __元件代碼__
    * wTA
  * __相依性__
    * 獨立元件
  * __版面相關__
    * 元件寬高
      * 高度(px)
        * 當變動高度＝是時，表示最小高度。
        * 不含<外邊距>的上邊距/下邊距：(DKS_單元樣式_外邊距_上邊距/下邊距)
      * 變動高度
        * 當變動高度＝否時
          * 內容超出，出現Scrollbar
          * [元件高度不足](../general/rule)
        * 當變動高度＝是時
          * 元件可能因<標題區>或<內容區>撐高，但會有最小高度
          * [內容超出折行，Enter也折行](../general/rule)
      * 寬度(%)
        不含 <外邊距>的左邊距/右邊距：(DKS_單元樣式_外邊距_左邊距/右邊距)
      * 當裝置的大小不同時，可能導致元件寬高會改變
    * 元件示意圖
      * Android
          ![image](./image/android/componentMulitTextEditing.png)
      * IOS
          ![image](./image/ios/componentMulitTextEditing.png)
    * [樣式](../general/style)
      * 致能(Enable)
      * 顯示致能(Display Enable)
      * 駐留(On Focus)
      * 標題(Title)
  * __加註__
    * - [x] [基本設定](../Addition/Component/basicSettings)
    * - [x] [預設給值](../Addition/Component/defaultValue)
    * - [x] [更新給值](../Addition/Component/updateValue)
    * - [x] [被動更新](../Addition/Component/passiveUpdate)
    * - [x] [編輯能力](../Addition/Component/editing)
    * - [x] [顯示設定](../Addition/Component/display)
    * - [x] [檢控限制](../Addition/Component/prosecutionRestrictions)
    * - [ ] [嵌入物件](../Addition/Component/embedded)
    * - [ ] [選項清單](../Addition/Component/optionalList)
    </details>
  * __行為__
    * 受權限保護元件
      - [x] [支援](../general/rule)
      - [ ] 不支援
    * 對應檔區：
      * DKS_表單元件_基本設定_存在檔區
    * 對應欄位：
      * DKS_表單元件_基本設定_檢視表對應欄位
      * 支援欄位型態：備註
    * 顯示巨集：
      - [ ] 支援
      - [x] 不支援
    * 模版：
      - [ ] 支援
      - [x] 不支援
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
        * 輸入時
          * 當為變動高度時，邊輸入會邊改變內容框高度，輸入超過一行會直接斷行，因此不會產生垂直/水平scrollbar
      * 內容：對應欄位
        * 換行視為有效資料
      * 元件唯讀：(DKS_資料元件_編輯能力_可編欄位_唯讀)
        * 當唯讀時，不允許輸入
    * 瀏覧模式：
      * 樣式
        * 變動高度＝否
        * 變動高度＝是
      * 內容：顯示<對應欄位>
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
      - [x] 支援
      - [ ] 不支援
        * 元件駐留
        * 元件跳離
          1. 若輸入內容與原值相同時，不會再執行後續的動作
          2. 檢查資料的正確性
             * 若條件不成立時，顯示[錯誤訊息](../general/rule)，並回復原值，駐留在該元件上
             1. 系統檢查
               * [空白檢查](../Addition/component/basicSettings)
             2. 設計者定義的檢查
               * [檢控限制](../Addition/component/prosecutionRestrictions)
               * 錯誤訊息類型：(DKS_表單元件_檢控限制_異常類別)
                 * 錯誤：(DKS_表單元件_檢控限制_異常類別_錯誤)
                 * 警告：(DKS_表單元件_檢控限制_異常類別_警告)
                 * 詢問：(DKS_表單元件_檢控限制_異常類別_操作者決定)
          3. 調整輸入內容
                   1. 若換行符號為\n，改為\r\n
          4. 寫入對應欄位
          5. [更新相關值](../Addition/component/updateValue)
          6. [它欄更新](../Addition/component/passiveUpdate)
          7. 存後：(DKS_表單元件_更新給值：ENG.存後)
          8. 重顯相關元件
          9. 跳至另一元件
    * 操作：
      * 點擊 (編輯狀態下)