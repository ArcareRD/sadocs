### <div id="tag">IDE介面 <path>(一般規則\關鍵字)</path></div>
        `關鍵字`
關鍵字，之後可用來搜尋。
* 介面名

    ex.預設給值、資料交易、....

* 介面裡的欄位名、下拉選項、RADIO選項、...

    ex.新增前、修改前、新增存回前、...

* 範例
        * `新增前` 會因預設給值的加註個數，決定在client端/server端執行。所以為了測試在Client端的部份，建議一張表單一個`預設給值`的加註，來測試於Client端的部份。

    * `新增前` 會因預設給值的加註個數，決定在client端/server端執行。所以為了測試在Client端的部份，建議一張表單一個`預設給值`的加註，來測試於Client端的部份。

### <div id="tag">RTE常用語 <path>(一般規則\關鍵字)</path></div>
        <rte>關鍵字</rte>
關鍵字，之後可用來搜尋。

<ps>注意</ps> 請至[RTE常用語-清單](tag.md) 搜尋。

<ps>注意</ps> 若不存在於清單時，請 skype 通知 rita 登冊。


* 範例
        * <rte>欄位型態</rte>須為<rte>數字</rte>。

    * <rte>欄位型態</rte>須為<rte>數字</rte>。


### <div id="html_tag_ps">注意事項 <path>(一般規則\特殊html tag)</path></div>

    <ps>注意</ps> 內容 

* 範例
        <ps>注意</ps> 當`多根節點`未勾選時，才可設定。

    <ps>注意</ps> 當`多根節點`未勾選時，才可設定。

### <div id="html_tag_ic">開關標示 <path>(一般規則\特殊html tag)</path></div>

    <ic>(開關代號)</ic> 

* 範例
        <ic>(FW0000004555)</ic>

    <ic>(FW0000004555)</ic>

### <div id="html_tag_test">測試注意事項 <path>(一般規則\特殊html tag)</path></div>

    <test>測試</test>

* 範例
        <test>測試</test>
        * `新增前` 會因預設給值的加註個數，決定在client端/server端執行。所以為了測試在Client端的部份，建議一張表單一個`預設給值`的加註，來測試於Client端的部份。
        * `修改前` 會因預設給值的加註個數，決定在client端/server端執行。所以為了測試在Client端的部份，建議一張表單一個`預設給值`的加註，來測試於Client端的部份。

    <test>測試</test>
    * `新增前` 會因預設給值的加註個數，決定在client端/server端執行。所以為了測試在Client端的部份，建議一張表單一個`預設給值`的加註，來測試於Client端的部份。
    * `修改前` 會因預設給值的加註個數，決定在client端/server端執行。所以為了測試在Client端的部份，建議一張表單一個`預設給值`的加註，來測試於Client端的部份。


### <div id="html_tag_path">來源路徑 <path>(一般規則\特殊html tag)</path></div>

    <path>(xx\xxx\...)</path>

* 範例
        #### <div id="expand-level-level">階數 <path>(外觀\預設展開\展開類別\展開階數)</path></div>
        指定展開層數。

    #### <div id="expand-level-level">階數 <path>(外觀\預設展開\展開類別\展開階數)</path></div>
    指定展開層數。

### <div id="ide">撰寫規範 <path>(IDE)</path></div>
* 側邊導覽欄
    * 所有欄位都會出現。
    * 例外狀況，不出現
        * Radio : 沒有子項目要設定。
    * 不支援時，使用刪除線標示。        

* 頁面
    * 固定只有一階。
    * 項目 
        一個欄位。

        * 格式
                ### 欄位名 <path>(位置\位置\...)</path>


### <div id="ide_valid">條件式 <path>(IDE)</path></div>
<ps>注意</ps> 要標示是否可以查表。

<ps>注意</ps> 不支援的話，請用刪除線表示。
* `處理類別`<path>(條件式)</path>
	* `無關資料庫`
	* ~~`資料表`~~
	* ~~`檢視表`~~


### <div id="ide_valid">運算式 <path>(IDE)</path></div>
<ps>注意</ps> 要標示是否可以查表。

<ps>注意</ps> 不支援的話，請用刪除線表示。
* `對應資料庫` <path>(運算式)</path>
    * `無`
    * ~~`資料表`~~
    * ~~`檢視表`~~

