# 加註類型-元件加註-更新給值

* ## Web支援版本
  
      8.10.1

* ## APP 支援版本

      008.010.001000 以上(含)

### 執行條件

      當條件成立時，才會執行。

* 處理類別
  * 無關資料庫
  * 資料表
  * 檢視表

### 固定式更新

    固定格式更新單筆資料

* 目的欄位

      寫入資料的欄位

* 給值來源

      資料來源的對像

### 查表式更新

    查詢資料庫的資料，回傳欄位的內容值

* 查表條件

      來源表格及過濾條件

  * 查無資料行時清空目的欄位

        查詢資料庫後無資料的處理

* 給值內容

  * 目的欄位

        寫入資料的欄位

  * 給值來源

        資料來源的對像

* 來源排序

      來源表格欄位的排序設定

  * 欄位名稱

            查表的排序欄位

  * 升/降冪

            查表的排序方式

### 呼叫按鈕功能

    依據<呼叫時機>來決定指定的元件操作行為，可執行指定的功能鍵

* 按鈕功能名

      當<呼叫時機>成立時，要執行的功能鍵

* 呼叫時機

  * 資料行移動 : 表示移動駐留筆資料時成立，支援的元件類型如下:
    * [元件容器](../../../Component/container.md)
      * 駐留筆資料異動時觸發(資料相同時不觸發)

  * 雙擊 : 表示雙擊資料列時成立，支援的元件類型如下:
    * [元件容器](../../../Component/container.md)

### 變數更新

      更新全域變數

* 全域變數

      寫入全域變數的欄位

* 給值來源

      資料來源的對像

### 密碼更新

    更新資料為明碼或密碼

### 作業流程

### 附件

* [注意事項](Warning.md)
