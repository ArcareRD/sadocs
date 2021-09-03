### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2021/08/24

### <div id="trac">TRAC</div>
* #8627
 
## <div id="unit-detection">單元檢錯</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">元件加註</p>

    * [元件加註-選項清單][link_OAList] 增加下列檢控:
        * 當`呈現方式`=下拉式, 且`選擇筆數`=多選, 駐留元件的對應欄位型態必須為文字(string)或備註(remark)            
        * 當`查詢轉換欄位`有值, 增加下列檢控:
            * 元件的對應欄位型態必須為(string)或備註(remark)
            * 元件的對應檔區須同駐留元件的檔區
            * 元件必須存在本單
            * 元件須不為密碼處理及個資加密未解密的元件
        * 當`呈現方式`=下拉式, 且`選擇筆數`=多選, 則變動選項表格
            * `來源欄位`
                * 欄位型態必須為文字(string)或備註(remark)            
                * 不為密碼處理及個資加密的欄位
            * `帶回對應元件`的
                * 對應欄位型態文字(string)或備註(remark)           
                * 不為密碼處理及個資加密未解密的欄位

<!--超連結 -->
[link_OAList]:OAList/README.md
