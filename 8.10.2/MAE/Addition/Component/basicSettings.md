# 元件加註-基本設定

* ## Web支援版本
  
      8.10.2

* ## APP 支援版本

      008.010.002004 以上(含)

* ## 執行時機

      內容異動

* __基本設定__
  * __存在檔區__
  * __[資料模版](../../General/model.md)__
    * 資料長度
  * __幣別元件__
  * __檢視表對應欄位__
    * [資料型態](../../General/dataFormat.md)
    * 資料長度
  * __選項群組__
    * 元件類型
      * [下拉選項](../../Component/dropList.md)
      * [選項清單](../../Component/list.md)
  * __選項給值__
    * 元件類型
      * [下拉選項](../../Component/dropList.md)
      * [選項清單](../../Component/list.md)
  * __引用功能__
    * 執行時機
          點擊元件時
    * 元件類型
      * [文字標題](../../Component/label.md)
      * [文字方塊](../../Component/text.md)
        * 僅供顯示＝是
        * 撥號功能=否
      * [圖片](../../Component/image.md)
      * [框線](../../Component/border.md)
  * __撥號功能__
    * 執行時機
          點擊電話圖示時
    * 元件類型
      * [文字方塊](../../Component/text.md)
        * 瀏覧模式/僅供顯示＝是
    * 檢查規則
      * 當空資料時顯示"空資料無法撥號。"。
      * 當有資料時，去除0~9+#*之外的資料，若去除後無資料則顯示"電話號碼不符合規則，無法撥打電話。"
  * __操作規則__
    * 執行時機
      * 內容異動時
    * 僅供顯示
      * 元件類型
        1. [文字方塊](../../Component/text.md)
        2. [下拉選項](../../Component/dropList.md)
        3. [清單選項](../../Component/list.md)
        4. [多行文字](../../Component/mulitText.md)
        5. [按鈕群組](../../Component/radioGroup.md)
        6. [按鈕選項](../../Component/radioButton.md)
        7. [核取方塊](../../Component/checkedBox.md)
    * 不可負值 (& 僅供顯示＝否)
      * 元件類型
        1. [文字方塊](../../Component/text.md)
    * 密碼顯示
      * 元件類型
        1. [文字方塊](../../Component/text.md)
    * 內容
      * 必要項 (& 僅供顯示＝否)
        1. [文字方塊](../../Component/text.md)
              在可編輯時，若無預設給值-編輯提示時會顯示提示訊息"請輸入"
        2. [多行文字](../../Component/mulitText.md)
              在可編輯時，若無預設給值-編輯提示時會顯示提示訊息"請輸入"
        3. [下拉選項](../../Component/dropList.md)
              在有必要項設定時，選擇內容不會出現空白資料
      * 選擇項 (& 僅供顯示＝否)
        * 空值不檢錯
              不檢查資料是否為空值或空字串
        * 空值要檢錯
              在 unFocus 時檢查資料是否為空值或空字串，若是則顯示錯誤並不允許跳離
