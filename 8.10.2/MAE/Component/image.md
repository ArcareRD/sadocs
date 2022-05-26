# 元件類型-圖片

* ## Web支援版本
  
      8.9.2

* ### APP 支援版本

      008.009.000.001 以上(含)

* #### 元件代碼

      wImg

* #### 相依性

      獨立元件

* #### 版面相關

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
      * 不含 <外邊距>的左邊距/右邊距：(DKS_單元樣式_外邊距_左邊距/右邊距)
    * 當裝置的大小不同時，可能導致元件寬高會改變

* #### 元件樣式

  * [致能](../general/style#致能Apps_Enable)
  * [標題](../general/style#標題Apps_Title)
  * 預設樣式

* #### 加註

  * [x] [基本設定](../Addition/Component/basicSettings)
  * [x] [預設給值](../Addition/Component/defaultValue)
  * [x] [更新給值](../Addition/Component/updateValue)
  * [ ] [被動更新](../Addition/Component/passiveUpdate)
  * [ ] [編輯能力](../Addition/Component/editing)
  * [ ] [顯示設定](../Addition/Component/display)
  * [x] [檢控限制](../Addition/Component/prosecutionRestrictions)
  * [ ] [嵌入物件](../Addition/Component/embedded)
  * [ ] [選項清單](../Addition/Component/optionalList)

* #### 行為

  * 受權限保護元件：內容區會顯示(受保護元件)的字樣(Trac #7477)
    * [x] [支援](../general/rule)
    * [ ] 不支援
  * 對應檔區：
    * DKS_表單元件_基本設定_存在檔區
  * 對應欄位：
    * DKS_表單元件_基本設定_檢視表對應欄位
    * 支援欄位型態：二進位
  * 顯示巨集：
    * [ ] 支援
    * [x] 不支援
  * 模版：
    * [ ] 支援
    * [x] 不支援
  * 提示：
    * [ ] 支援
    * [x] 不支援
  * 錯誤顯示：顯示在元件下方
    * [x] 支援
    * [ ] 不支援
  * 資料過濾：
    * [ ] 支援
    * [x] 不支援
  * 資料搜尋：
    * [ ] 支援
    * [x] 不支援
  * 編輯模式：
    * [ ] 支援
    * [x] 不支援
  * 瀏覧模式：
    * 樣式
      * 無資料時
      * 有資料時
    * 內容：對應欄位
    * 顯示樣式：不支援
    * 比例縮放：不支援
    * [超連結](../Addition/Component/basicSettings) #圖片_超連結
      * 是否點擊過，無法從外觀看出
      * 點擊
        * 執行<超連結>：(DKS_表單元件_基本設定_引用功能)
  * 開單隱藏：
    * [ ] 支援
    * [x] 不支援
  * 資料隱藏：
    * [x] 支援
    * [ ] 不支援
  * 元件隱藏：
    * [x] 支援
    * [ ] 不支援
  * 元件除能：
    * [ ] 支援
    * [x] 不支援
  * 元件駐留：
    * [ ] 支援
    * [x] 不支援
  * 操作：
    * 點擊 (有引用功能時)

* #### 預覧畫面

  * Android

    ![image](./image/android/componentImage.png)

  * IOS

    ![image](./image/ios/componentImage.png)

* #### 作業流程
