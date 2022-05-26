# 元件類型-文字方塊

* ## Web支援版本
  
      8.9.2

* ### APP 支援版本

      008.009.000.001 以上(含)

* #### 元件代碼

      wTF

* #### 相依性

      獨立元件

* #### 版面相關

  * 元件寬高
    * 高度(px)
      * 當變動高度＝是時，表示最小高度。
      * 不含<外邊距>的上邊距/下邊距：(DKS_單元樣式_外邊距_上邊距/下邊距)
    * 變動高度
      * 當變動高度＝否時
        * [元件超出顯示](../general/rule)
        * [元件高度不足](../general/rule)
      * 當變動高度＝是時
        * 元件可能因<標題區>撐高
        * [標題超出折行](../general/rule)
    * 寬度(%)
      * 不含 <外邊距>的左邊距/右邊距：(DKS_單元樣式_外邊距_左邊距/右邊距)
    * 當裝置的大小不同時，可能導致元件寬高會改變

* #### 元件樣式

  * [致能](../general/style#致能Apps_Enable)
  * [顯示致能](../general/style#顯示致能Apps_Display_Enable)
  * ~~[駐留](../general/style#駐留Apps_onFocus)~~
  * [標題](../general/style#標題Apps_Title)
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
  * [ ] [選項清單](../Addition/Component/optionalList)

* #### 行為

  * 受權限保護元件
    * [x] [支援](../general/rule)
    * [ ] 不支援
  * 對應檔區：
    * DKS_表單元件_基本設定_存在檔區
  * 對應欄位：
    * DKS_表單元件_基本設定_檢視表對應欄位
    * 支援欄位型態：文字/整數/數字/日期/日期時間/全唯碼/備註
  * 顯示巨集：
    * [ ] 支援
    * [x] 不支援
  * [模版](../general/model)：
    * [x] 支援
    * [ ] 不支援
  * 提示：
    * [ ] 支援
    * [x] 不支援
  * 錯誤顯示：顯示在元件下方
    * [x] 支援
    * [ ] 不支援
  * 資料過濾：對應欄位
  * 資料搜尋：對應欄位
    * 編輯模式：
      * 樣式
        * 若模版 ＝ 日期模版/日期時間模版/時間
        * 若模版 ＝ 數字
        * 若模版 ＝ 文字
      * 元件唯讀：(DKS_資料元件_編輯能力_可編欄位_唯讀)
        * 當唯讀時，不允許輸入
      * 內容：對應欄位
      * [密碼](../Addition/Component/basicSettings)
    * 瀏覧模式：
      * 樣式
        * 無撥號功能
        * 有撥號功能
          * 元件右邊顯示電話圖示
            * 不會出現圖示的清況
              1. 受保護元件
              2. 勿駐
              3. 於編輯模式下
          * 只有<單擊>電話圖示時，可以播打電話(於元件瀏覧模式下)
            * 檢查電話號碼是否只有 0~9 +#* ，若不符規則或空白時，彈出訊息盒"電話號碼格式不正確，無法撥打電話。"
      * [超連結](../Addition/Component/basicSettings)
        * 點擊前顏色：(DKS_單元樣式_內容_超連結點擊前顏色)
        * 已點擊過的判斷依據：所屬檔區記錄，一直到關閉表單為止
        * 點擊前
        * 點擊後
        * 點擊
          * 字體變更<超連結點擊後顏色>：(DSK_單元樣式_內容_超連結點擊後顏色)
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
      * [x] 支援
      * [ ] 不支援
        * 元件駐留
        * 元件跳離
          1. 調整輸入內容
               * 若套用大寫模版時，系統自動將英文字轉為大寫
               * 若對應欄位的組裝欄位型態＝04.int / 05.smallint / 06.tinyint / 16.bigint / 07.數字 / 08.金額 時，沒輸入資料，預設給0
          2. 若輸入內容與原值相同時，不會再執行後續的動作
          3. 檢查資料的正確性
             * 若條件不成立時，顯示[錯誤訊息](../general/rule)，並回復原值，駐留在該元件上
             * 系統檢查
               * [空白檢查](../Addition/Component/basicSettings)
             * 設計者定義的檢查
               * [檢控限制](../Addition/Component/prosecutionRestrictions)
               * [不可重複](../Addition/Component/basicSettings)
               * [不可負值](../Addition/Component/basicSettings)
          4. 寫入對應欄位
          5. [更新相關值](../Addition/Component/updateValue)
          6. [被動更新](../Addition/Component/passiveUpdate)
          7. 重顯相關元件
          8. 跳至另一元件
    * 操作：
      * 點擊 (編輯狀態下)

* #### 預覧畫面

  * Android

    ![image](./image/android/componentTextEditing.png)

  * IOS

    ![image](./image/ios/componentTextEditing.png)

* #### 作業流程
