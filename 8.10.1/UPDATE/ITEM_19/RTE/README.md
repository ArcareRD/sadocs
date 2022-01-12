# 系統函數擴充

### <div id="user">規劃人員</div>
* 正傑

### <div id="updatedate">規劃日期</div>
* 2021/12/09

### <div id="trac">TRAC</div>
* #8731,#5209

### <div id="requirement">需求展開</div>
* RTE 擴充以下系統函數
    * 系統函數.身份證字號驗證(SF000000000102)
    * 函數說明 : 驗證傳入的身分證字號是否合法，合法回傳true，不合法回傳false，僅支援運算式 / 引擎語法
        * 參數.身分證字號
            * 參數類型 : 0.Script用
                * 型別：1.字串
        * 回傳型態:4.布林
    * 系統函數.統一編號驗證(SF000000000103)
    * 函數說明 : 驗證傳入的統一編號是否合法，合法回傳true，不合法回傳false，僅支援運算式 / 引擎語法
        * 參數.統一編號
            * 參數類型 : 0.Script用
                * 型別：1.字串
        * 回傳型態:4.布林
    * 系統函數.EAN-13商品條碼驗證(SF000000000104)
    * 函數說明 : 驗證傳入的條碼是否符合EAN-13的編碼，合法回傳true，不合法回傳false，僅支援運算式 / 引擎語法
        * 參數.條碼
            * 參數類型 : 0.Script用
                * 型別：1.字串
        * 回傳型態:4.布林
    * 系統函數.EAN-13商品條碼驗證(SF000000000104)
    * 函數說明 : 將傳入的值依據指定的小數位數進行無條件進位，僅支援運算式 / 引擎語法
        * 參數.值
            * 參數類型 : 0.Script用
                * 型別：2.數字
        * 回傳型態:2.數字