# 樣式

* ## Web支援版本

        8.10.1

* ## APP 支援版本

        008.010.001049 以上(含)

* ### 支援類型

  * [致能](#致能Apps_Enable)
  * [除能](#除能Apps_Disable)
  * [顯示致能](#顯示致能Apps_DisplayEnable)
  * [駐留](#駐留Apps_OnFocus)
  * [標題](#標題Apps_Title)
  * [點擊](#點擊Apps_OnClick)
  * [區塊](#區塊Apps_Block)
  * [選項清單](#選項清單Apps_Item_List)

* #### 致能(Apps_Enable)

  * 元件類型
    * [文字標題](../Component/label.md)
    * [文字方塊](../Component/text.md)
    * [多行文字](../Component/mulitText.md)
    * [下拉選項](../Component/dropList.md)
    * [清單選項](../Component/list.md)
    * [按鈕群組](../Component/radioGroup.md)
    * [按鈕選項](../Component/radioButton.md)
    * [核取方塊](../Component/checkedBox.md)
    * [框線](../Component/border.md)
    * [圖片](../Component/image.md)
    * [元件容器](../Component/container.md)
    * [畫布](../Component/canvas.md)
    * [嵌入物件](../Component/embed.md)
    * [功能按鈕](../Component/button.md)

* #### 除能(Apps_Disable)

  * 元件類型
    * [功能按鈕](../Component/button.md)
  
* ##### 顯示致能(Apps_DisplayEnable)

  * 元件類型
    * [文字方塊](../Component/text.md)
    * [多行文字](../Component/mulitText.md)
    * [按鈕選項](../Component/radioButton.md)
    * [下拉選項](../Component/dropList.md)
    * [清單選項](../Component/list.md)
    * [嵌入物件](../Component/embed.md)
    * [核取方塊](../Component/checkedBox.md)

* #### 駐留(Apps_OnFocus)

  * 目前暫只支援駐留樣式的顏色，和字型及大小相關的設定因為更新需要重繪，會導至鍵盤連續開關或不顯示
  * 元件類型
    * [文字方塊](../Component/text.md)
    * [多行文字](../Component/mulitText.md)

* #### 標題(Apps_Title)

  * 元件類型
    * [文字方塊](../Component/text.md)
    * [多行文字](../Component/mulitText.md)
    * [按鈕群組](../Component/radioGroup.md)
    * [按鈕選項](../Component/radioButton.md)
    * [下拉選項](../Component/dropList.md)
    * [清單選項](../Component/list.md)
    * [嵌入物件](../Component/embed.md)
    * [圖片](../Component/image.md)
    * [畫布](../Component/canvas.md)
    * [核取方塊](../Component/checkedBox.md)

* #### 點擊(Apps_OnClick)

  * 元件類型
    * [功能按鈕](../Component/button.md)

* #### 區塊(Apps_Block)

  * 元件類型
    * [元件容器](../Component/container.md)

* #### 選項清單(Apps_Item_List)

  * 元件類型
    * [下拉選項](../Component/dropList.md)
    * [清單選項](../Component/list.md)

* ### 常用樣式

  * __背景(底色)__
    * 顏色
            RGB格式
    * 透明度
            數字格式，0~100(不透明)
    * 漸層色
            RGB格式
    * 漸層方向
      * 無
      * 上
      * 下
      * 左
      * 右
      * 垂直
      * 水平
      * 往內
      * 往外
    * `當漸層色有設定但不成立或漸層方向＝無時，若顏色有設定時，則以顏色來顯示`
  * __內容__
    * 文字顏色
            RGB格式
    * 透明度
            數字格式，0~100(不透明)
    * _~~字型~~(不支援)_
    * 大小
            數字格式, px
    * 水平
      * 靠左
      * 置中
      * 靠右
    * 垂直
      * 靠上
      * 置中
      * 靠下
    * 字型樣式
      * 粗體
      * 斜體
      * 底線
      * 刪除線
    * 超連結
      * 點擊前
            RGB格式
      * 點擊後
            RGB格式
  * __框線__
    * 線條
      * 無
      * 實線
      * 虛線
      * 嵌入線
      * 浮出線
    * 圓角
      * `當圓角<寬度且線條=虛線時，會強制設定圓角=寬度`
    * 上框線
      * 寬度
            數字格式, px
      * 顏色
            RGB格式
    * 下框線
      * 寬度
            數字格式, px
      * 顏色
            RGB格式
    * 左框線
      * 寬度
            數字格式, px
      * 顏色
            RGB格式
    * 右框線
      * 寬度
            數字格式, px
      * 顏色
            RGB格式
  * __邊界__
    * 內邊距
      * 上
            數字格式, px
      * 下
            數字格式, px
      * 左
            數字格式, px
      * 右
            數字格式, px
    * 外邊距
      * 上
            數字格式, px
      * 下
            數字格式, px
      * 左
            數字格式, px
      * 右
            數字格式, px
* __進階樣式__
  * 光棒
    * 線條
      * 無
      * 實線
      * 虛線
      * 嵌入線
      * 浮出線
    * 上框線
      * 寬度
            數字格式, px
      * 顏色
            RGB格式
    * 下框線
      * 寬度
            數字格式, px
      * 顏色
            RGB格式
    * 左框線
      * 寬度
            數字格式, px
      * 顏色
            RGB格式
    * 右框線
      * 寬度
            數字格式, px
      * 顏色
            RGB格式
    * 顏色
        RGB格式
    * 透明度
        數字格式，0~100(不透明)
    * 漸層色
        RGB格式
    * 漸層方向
      * 無
      * 上
      * 下
      * 左
      * 右
      * 垂直
      * 水平
      * 往內
      * 往外
    * `當漸層色有設定但不成立或漸層方向＝無時，若顏色有設定時，則以顏色來顯示`
