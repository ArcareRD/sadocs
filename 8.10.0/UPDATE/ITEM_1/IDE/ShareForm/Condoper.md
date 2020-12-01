### <div id="user">規劃人員</div>
* how

### <div id="updatedate">規劃日期</div>
* 2020/11/27

### <div id="trac">TRAC</div>
* <ps>待補</ps> 

## <div id="layout">版面</div>
![pic][image_Condoper]

## <div id="object-desc">欄位說明</div>
* `(2)查詢表格`
    * 用途說明
    * 規格說明
        * `(1)處理類別`=資料表基礎, [挑選資料表通則][link_ruledialog3], 取得`離線資料上傳用`未勾選的資料表
        * `(1)處理類別`=檢視表基礎, [挑選檢視表通則][link_ruledialog4], 由前單指定, 取得`離線用`勾選或未勾選的檢視表
            * 由表單、元件、按鍵加註單據開啟 且 [新增表單/報表][link_AddFormReport]的`離線用`為勾選, 則取得`離線用`為勾選的檢視表
            * 否則, 則為未勾選的檢視表
* `(3)系統函數名`
    * 用途說明
    * 規格說明
        * 由前單指定, 取得是否支援SQLLite的函數, 請參閱[系統函數][link_SystemFunction]的引用說明
* `(4)運算元名稱`
    * 用途說明
    * 規格說明
        * `(3)運算元類別`=函數, 由前單指定, 取得是否支援SQLLite的函數, 請參閱[系統函數][link_SystemFunction]的引用說明

<!-- 圖片 -->
[image_Condoper]:attachment/Condoper.png

<!-- 超連結 -->
[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog3 "共用通則_開啟單據/挑選資料表通則"
[link_ruledialog4]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"
[link_SystemFunction]:../SystemResource/SystemFunction "系統函數"
[link_AddFormReport]:../Home/AddFormReport "新增表單/報表"