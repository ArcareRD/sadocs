# 流程表單擴充MAE表單設定

### <div id="user">規劃人員</div>
* how

### <div id="updatedate">規劃日期</div>
* 2021/06/15

### <div id="trac">TRAC</div>
* #8548

### <div id="requirement">需求展開</div>
* 1. 流程表單, 分RTE/MAE兩種設定
    * 1-1. 流程表單, 原欄位標題更名為 RTE表單名稱; 新增一欄位為 MAE表單名稱
	* 2-2. 單據報表清單, 由 流程表單/RTE表單名稱 開啟, 新增單據, 則表單類型須寫入app表單
    * 2-3. 單據流程, 移除指定流程表單的欄位

* 因8.10.0已發行，請至完整文件查看本次異動規格:
    * [流程表單][link_FlowForm]
    * [單據報表清單][link_ListFormReport]
    * [單據流程][link_FlowItem]

* 其它
    * [發行檢錯](UnitDetection.md)

[link_FlowForm]:../../../IDE/Specification/Home/FlowForm.md "流程表單"	
[link_ListFormReport]:../../../IDE/Specification/FlowItem/ListFormReport.md "單據報表清單"	
[link_FlowItem]:../../../IDE/Specification/FlowItem/README.md "單據流程"