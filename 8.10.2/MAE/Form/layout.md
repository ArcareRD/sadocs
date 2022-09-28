# 版面

* ## Web支援版本
  
      8.9.2

* ## APP 支援版本

      008.009.000.001 以上(含)

* ### 版面設定

* #### 上方導覧列

  * 元件類型
    * [功能按鈕](../Component/button.md)
  * 高度
        固定30px
  * 寬度
        固定100%
  * 說明
        當存在首頁的上方導覧列且不存在目前表單的上方導覧列時，顯示首頁的上方導覧列

* #### 表單

  * 類型
    * 單筆
    * 多筆
    * 單改
    * 條件多筆
  * 元件類型
    * [文字標題](../Component/label.md)
    * [文字方塊](../Component/text.md)
    * [多行文字](../Component/mulitText.md)
    * [按鈕群組](../Component/radioGroup.md)
    * [按鈕選項](../Component/radioButton.md)
    * [核取方塊](../Component/checkedBox.md)
    * [下拉選項](../Component/dropList.md)
    * [清單選項](../Component/list.md)
    * [圖片](../Component/image.md)
    * [嵌入物件](../Component/embed.md)
    * [元件容器](../Component/container.md)
    * [畫布](../Component/canvas.md)
    * [框線](../Component/border.md)
    * [功能按鈕](../Component/button.md)
  * 高度
    * 標題列位置=上/下時
          固定100%-標題列-上方導覧列(有設定時)-下方導覧列(有設定時)
    * 標題列位置=左/右時
          固定100%-上方導覧列(有設定時)-下方導覧列(有設定時)
  * 寬度
    * 標題列位置=上/下時
          固定100%
    * 標題列位置=左/右時
          固定100%-標題列

* #### 開單模式

  * 分頁
    * 顯示為一般表單
    * 預設為分頁
  * 訊息盒
    * 顯示大小會依寬高比例設定
    * 比例大小相對於裝置螢幕
    * 訊息盒表單範圍外，除系統工具列，其餘區域點擊無效(包含上方工具列)
    * 不會套用首頁的上下方導覧列

* #### 下方導覧列

  * 元件類型
    * [功能按鈕](../Component/button.md)
  * 高度
        固定30px
  * 寬度
        固定100%
  * 說明
        當存在首頁的下方導覧列且不存在目前表單的下方導覧列時，顯示首頁的下方導覧列

* #### 開啟(選單列)

  * 執行時機
          表單預設給值及載入檔區資料後
  * 元件類型
    * [功能按鈕](../Component/button.md)

* #### 退出(選單列)

  * 執行時機
          表單關閉後完全退出前
  * 元件類型
    * [功能按鈕](../Component/button.md)
