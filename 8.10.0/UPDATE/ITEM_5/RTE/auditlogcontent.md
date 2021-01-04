### <div id="user">規劃人員</div>
* Ivan

### <div id="updatedate">規劃日期</div>
* 2020/12/31

### <div id="trac">TRAC</div>
* #8264

### <div id="sitemanage_2">表單.稽核紀錄內容 <path>(Site管理)</path></div>
* 擴充
* 規格說明
    * 僅 稽核管理員, 可檢視
    * 顯示Request、Response內容
    * 若Request、Response內容為資料結構，則內容以表格呈現(詳見[附件](https://docs.google.com/spreadsheets/d/1JVLJAa9XyQxCIEuPNR-z6Ex4F39gIEC9/edit#gid=29312194))

* 表單畫面
    |  | 畫面 |
    | :---: | :---: |
    | 內容</br>不為</br>資料</br>結構 | ![AuditLogContent_Memo] |
    | 內容</br>為資</br>料結</br>構 | ![AuditLogContent_Table] |


* 畫面規格說明
    * 欄位.日期時間 : 顯示稽核紀錄的執行時間
        
    * 欄位.使用者 : 顯示稽核紀錄的使用者名稱

    * 欄位.系統名稱 : 顯示稽核紀錄的系統名稱(寫入時給值系統預設語系的多語內容)

    * 欄位.組織編號 : 顯示稽核紀錄的組織編號(寫入時給值系統預設語系的多語內容)

    * 欄位.執行程式 : 顯示稽核紀錄的SERVLETPATH

    * 欄位.動作頁面 : 
        * 顯示稽核紀錄的表單名稱 :
            * 若為Site表單 : 寫入時給值表單英文名稱
            * 若為系統表單 : 寫入時給值系統預設語系的多語內容

    * 欄位.動作代號 : 
        * 顯示稽核紀錄的動作名稱(寫入時依SERVLETPATH判斷給值:異動/查詢)

    * 欄位.Request內容 :
        * 當內容不為資料結構 : 內容以Memo顯示
        * 當內容為資料結構 : 需拆解內容並以表格顯示
            * 欄位.紀錄 : 資料結構內的第幾筆紀錄
            * 欄位.資料表 : 
                * 當動作代號為異動 : 異動的資料表名稱(寫入時給值主表資料表名稱)
                * 當動作代號為查詢 : <ps>查詢時無法得知主表為何，待確認是否需顯示</ps>
            * 欄位.異動類別 : 
                * 當動作代號為異動 : 資料結構內的異動類別
                * 當動作代號為查詢 : 固定顯示"R"
            * 欄位.資料內容 : 資料結構內的資料內容

    * 欄位.Response內容 :
        * 當內容不為資料結構 : 內容以Memo顯示
        * 當內容為資料結構 : 需拆解內容並以表格顯示
            * 欄位.紀錄 : 資料結構內的第幾筆紀錄
            * 欄位.資料表 : 異動的資料表名稱(寫入時給值主表資料表名稱)
            * 欄位.異動類別 : 
                * 當動作代號為異動 : 資料結構內的異動類別
                * 當動作代號為查詢 : 固定顯示"R"
            * 欄位.資料內容 : 資料結構內的資料內容

* 作業流程
    * 開啟稽核紀錄內容畫面

    ![AuditLogContent_sa1]

<!--超連結引用ps.畫面上看不到-->
[AuditLogContent_Memo]:img/AuditLogContent_Memo.jpg
[AuditLogContent_Table]:img/AuditLogContent_Table.jpg
[AuditLogContent_sa1]:img/AuditLogContent_sa1.jpg
