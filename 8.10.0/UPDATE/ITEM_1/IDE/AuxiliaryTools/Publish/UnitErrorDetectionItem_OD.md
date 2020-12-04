### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/12/4

## <div id="desc">離線資料交易</div>
* [目的表格][link_offlineposting_fieldbreak2]
    * `目的表格`須存在專案中
    * `比對欄位`須存在`目的表格`中
    * 當`判斷條件`存在記錄, 增加下列檢控
        * 當`類別`=參數, 則`來源欄位`須存在[接收參數][link_offlineposting_fieldbreak5]中
        * 當`類別`=運算式,替 則`來源欄位`須存在[運算式][link_expression]中, 且符合運算式檢錯
        * `比對欄位`與`來源欄位`, 須符合[型態檢查通則]




<!-- 超連結-->
[link_offlineposting_fieldbreak2]:/8.10.0/UPDATE/ITEM_1/IDE/DataTable/OfflinePosting/README#fieldbreak2
[link_offlineposting_fieldbreak5]:/8.10.0/UPDATE/ITEM_1/IDE/DataTable/OfflinePosting/README#fieldbreak5
[link_expression]:/8.10.0/IDE/Specification/Expression/README