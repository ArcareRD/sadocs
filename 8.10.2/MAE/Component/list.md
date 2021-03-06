# 元件類型-清單選項

* ## Web支援版本
  
      8.9.2

* ### APP 支援版本

      008.009.000.001 以上(含)

* #### 元件代碼

      wLB

* #### 相依性

      獨立元件

* #### 版面相關

  * 元件寬高
    * 高度(px)
      * 當變動高度＝是時，表示最小高度。
      * 不含<外邊距>的上邊距/下邊距：(DKS_單元樣式_外邊距_上邊距/下邊距)
    * 變動高度
      * 當變動高度＝否時
        * 選項超出，出現Scrollbar
        * [元件高度不足](../general/rule)
      * 當變動高度＝是時
        * 元件可能因<標題區>或<內容區>撐高，但會有最小高度
        * 選項超出顯示...
    * 寬度(%)
      * 不含 <外邊距>的左邊距/右邊距：(DKS_單元樣式_外邊距_左邊距/右邊距)
    * 當裝置的大小不同時，可能導致元件寬高會改變

* #### 元件樣式

  * [致能](../general/style#致能Apps_Enable)
  * [顯示致能](../general/style#顯示致能Apps_Display_Enable)
  * [標題](../general/style#標題Apps_Title)
  * 光棒
    * 被選取的選項
  * 預設樣式

* #### 加註

  * [x] [基本設定](../Addition/Component/basicSettings)
  * [x] [預設給值](../Addition/Component/defaultValue)
  * [x] [更新給值](../Addition/Component/updateValue)
  * [x] [被動更新](../Addition/Component/passiveUpdate)
  * [x] [編輯能力](../Addition/Component/editing)
  * [x] [顯示設定](../Addition/Component/display)
  * [x] [檢控限制](../Addition/Component/prosecutionRestrictions)
  * [ ] [嵌入物件](../Addition/Component/embedded)
  * [x] [選項清單](../Addition/Component/optionalList) (必要項)
    * 若無選項清單的加註時，清單選項不會顯示資料

* #### 行為

  * 受權限保護元件 (Trac #7477)
    * [ ] 支援
    * [x] 不支援
  * 對應檔區：
    * DKS_表單元件_基本設定_存在檔區
  * 對應欄位：
    * DKS_表單元件_基本設定_檢視表對應欄位
    * 支援欄位型態：文字/整數/數字/日期/日期時間/全唯碼
  * 顯示巨集：
    * [ ] 支援
    * [x] 不支援
  * 模版
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
  * 單選/複選
    * 單選：(DKS_表單元件_選項清單_固定式_單選)
      * [x] 支援
      * [ ] 不支援
    * 複選：(DKS_表單元件_選項清單_固定式_複選)
      * [ ] 支援
      * [x] 不支援
  * 編輯模式：
    * 樣式
      * 變動高度＝否
      * 變動高度＝是
    * 內容：(DKS_表單元件_選項清單)
      * 被選取元件：對應欄位
      * 選項的組成
        * 固定選項：(DKS_表單元件_選項清單_固定項次)
              格式= 代號.名稱(以點(.)分隔)
              顯示= 名稱
        * 變動選項：(DKS_表單元件_選項清單_變動項次)
          * 顯示= DKS_選項清單_來源欄位(要顯示=Y 且帶回對應元件<>本元件)(只能有一個)
    * 不允許自行輸入
    * 新增若沒給初始值，為空值時，會預設選取第一個選項
    * 元件唯讀：(DKS_表單元件_編輯能力_唯讀)
      * 不允許挑選
  * 瀏覧模式：
    * 樣式
      * 變動高度＝否
      * 變動高度＝是
    * 內容：同編輯模式下的內容
    * ~顯示樣式：(DKS_表單元件_顯示設定_顏色)~
      * ~字體顏色、背景顏色~ 不支援
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
      * 元件跳離 (選項值異動時)
        1. 若輸入內容與原值相同時，不會再執行後續的動作
        2. 檢查資料的正確性
           * 若條件不成立時，顯示[錯誤訊息](../general/rule)，並回復原值，駐留在該元件上
           * 設計者定義的檢查
             * [檢控限制](../Addition/Component/prosecutionRestrictions)
             * 錯誤訊息類型：(DKS_表單元件_檢控限制_異常類別)
             * 錯誤：(DKS_表單元件_檢控限制_異常類別_錯誤)
             * 警告：(DKS_表單元件_檢控限制_異常類別_警告)
             * 詢問：(DKS_表單元件_檢控限制_異常類別_操作者決定)
        3. 寫入對應欄位
        4. [更新相關值](../Addition/Component/updateValue)
        5. [被動更新](../Addition/Component/passiveUpdate)
        6. 重顯相關元件
        7. 跳至另一元件
  * 操作：
          點擊(編輯狀態下)

* #### 預覧畫面

  * Android

    ![image](./image/android/componentListEditing.png)

  * IOS

    ![image](./image/ios/componentListEditing.png)

* #### 作業流程
