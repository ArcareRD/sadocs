### <div id="user">規劃人員</div>
* Lucky

### <div id="updatedate">規劃日期</div>
* 2020/11/17

### <div id="trac">TRAC</div>
* <ps>待開</ps>

### <div id="index">單元檢錯</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">檢視表</p>

  * [聯結設定][link_logjoin]
    * 當`聯結方式`不為Cross Join、Union, `聯結條件區塊` 須設定
  * [欄位清單][link_logcols]
    * 當[欄位清單](/8.10.0/UPDATE/ITEM_4/IDE/logical/README.md#colsspecific)`特定處理`, 有設定除了無以外的設
    定時, 所有欄位都不可設定為無
    * `資料內容區塊` 必須設定
    * 關聯條件為UNION時, [欄位清單](/8.10.0/UPDATE/ITEM_4/IDE/logical/README.md#logcols_union_data)`資料內容區塊` 需全數設定
  * [排序依據][link_orderby]
    * 當TOP有設定勾選時, 排序依據至少設定一筆

[link_logjoin]:/8.10.0/UPDATE/ITEM_4/IDE/logical/README.md#join "關聯條件"
[link_logcols]:/8.10.0/UPDATE/ITEM_4/IDE/logical/README.md#logcols "欄位清單"
[link_orderby]:/8.10.0/UPDATE/ITEM_4/IDE/logical/README.md#orderby "排序依據"