### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2021/06/01

### <div id="trac">TRAC</div>
* #8523

### <div id="requirement">需求展開</div>

* 1. 元件類型=多筆瀏覽時，異動元件加註_更新給值 同 多筆表格的做法
    * 1-1. 呼叫按鈕功能，增加呼叫時機: 滑鼠雙擊
    * 1-2. 呼叫按鈕功能，取消 依附檔區為 單筆表頭、條件多筆的表頭、單改表頭 的限制
* 2. 按鍵加註_開啟表單，當表單設計類型=STD、RWD，
    * 2-1. 增加欄位: 開單模式，Radio，選項: 分頁/視窗，型態: tinyint
    * 2-2. 原已存在資料，選項=分頁

* 因8.10.0已發行，請至完整文件查看本次異動規格:
    * [按鍵加註_開啟它單][open_dialog]
    * [元件加註_更新給值][open_update]


[open_dialog]:../../../IDE/Specification/BADialog/README.md "按鍵加註_開啟它單"
[open_update]:../../../IDE/Specification/OAUpdate/README.md "元件加註_更新給值"