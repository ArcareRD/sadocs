### <div id="trac">TRAC</div>

* [#8195]
* [#8197]

### <div id="projectadd">開案 </div>

* 開案時增加傳遞多語系的系統名稱申請開案, 用來建立測試運行台的系統名稱 `(多語)系統名稱 + "_運行台"`

### <div id="publish">發行 </div>

* 發行時將專案多語資訊傳遞至發行對應的測試運行台, 若系統名稱有未建立的語系, 須以該語系建立名稱, 名稱來源以IDE傳遞內容依語系取得 `專案名稱 + "_運行台"`, 已存在的語系將不覆蓋。



<!--超連結-->
[#8195]:http://trac.uneec.com/trac/neco/ticket/8195 "IDE_開案多語規格擴充"
[#8197]:http://trac.uneec.com/trac/neco/ticket/8197 "IDE_發行多語規格修改"