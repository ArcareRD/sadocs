# 元件類型-圖片

* ## Web支援版本
  
      8.9.2

* ## APP 支援版本

      008.009.000.001 以上(含)

* __圖片__
  * __元件代碼__
    * wImg
  * __相依性__
    * 獨立元件
  * __版面相關__
    * 元件寬高
      * 高度(px)
        * 當變動高度＝是時，表示最小高度。
        * 不含<外邊距>的上邊距/下邊距：(DKS_單元樣式_外邊距_上邊距/下邊距)
      * 變動高度
        * 當變動高度＝否時
          * 圖片依<寛度/高度>比例縮放
          * [元件高度不足](../general/rule)
        * 當變動高度＝是時
          * 元件可能因<標題區>或<內容區>撐高，但會有最小高度
          * 圖片內容依<寛度>比例縮放
      * 寬度(%)
        不含 <外邊距>的左邊距/右邊距：(DKS_單元樣式_外邊距_左邊距/右邊距)
      * 當裝置的大小不同時，可能導致元件寬高會改變
    * 元件示意圖
      * Android
          ![image](./image/android/componentImage.png)
      * IOS
          ![image](./image/ios/componentImage.png)
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
    * 錯誤顯示：顯示在元件下方
      - [x] 支援
      - [ ] 不支援
    * 資料過濾：
      - [ ] 支援
      - [x] 不支援
    * 資料搜尋：
      - [ ] 支援
      - [x] 不支援
    * 編輯模式：
      - [ ] 支援
      - [x] 不支援
    * 瀏覧模式：
      * 樣式
        * 無資料時
        * 有資料時
      * 內容：對應欄位
      * 顯示樣式：不支援
      * 比例縮放：不支援
      * [超連結](../affix/component/basicSettings) #圖片_超連結
        * 是否點擊過，無法從外觀看出
        * 點擊
          * 執行<超連結>：(DKS_表單元件_基本設定_引用功能)
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
    * 操作：
      * 點擊 (有引用功能時)
