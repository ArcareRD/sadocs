### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/06

### <div id="trac">TRAC</div>
* #8213

## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_button_STD]
    * RWD
        * 同STD
    * MAE</br>
        * 同STD

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>

* 依規格定義-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格定義-主畫面 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_ruleother2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能
* 作業流程
    * ![pic][image_Open]


## <div id="other-desc">設計注意事項說明</div>
* 推播訊息所有資料大小合計不可超過4k bytes (含系統保留大小: 500 bytes)，若超過此大小，可能造成發送失敗 

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_Annotation_Notice_Block1]
    * `(1)按鈕名稱`
        * 用途說明
        * 規格說明
            * 參照 [使用多語詞庫通則][link_ruledialog2], 回傳:按鍵多語內容並顯示
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示前單傳入的按鍵料號
    * `(3)優先序`
        * 用途說明
        * 規格說明
            * 自行輸入, 1~999
    * `(4)執行條件`
        * 用途說明
        * 規格說明
            * 參照 [設定按鍵執行條件表格通則][link_ruledialog11]

* <p id="fieldbreak2" style="color:blue;font-weight:bold">推播人</p>  

    * ![pic][image_Annotation_Notice_Block2]
    * <t id="sender">(1)推播人</t>
        * 用途說明
            * 意指 發送推播的人員
        * 規格說明
            * 單選選項: 管理者 / 使用者
            * 系統預設: 管理者

* <p id="fieldbreak3" style="color:blue;font-weight:bold">推播內容</p>  

    * ![pic][image_Annotation_Notice_Block3]
    * <t id="replacetype">(1)來源</t>
        * 用途說明
            * 意指 推播來源類別
        * 規格說明
            * 下拉選項: 無 / 查表
            * 系統預設: 無
            * 當切換為無時, 顯示訊息盒【標題: 系統訊息 / 異動推播來源類別將清除[相關欄位]，是否繼續。 / 按鍵:確定、取消】
                * 確定: 清除欄位:`(3)推播來源檢視表參數`、加註中引用類別為 **推播來源欄位** 的欄位, 並關閉訊息盒
                * 取消: 關閉訊息盒
        * 作業流程
            * ![pic][image_NoticeSourceType]
    * <t id="conentviewno">(2)檢視表</t>
        * 用途說明
            * 意指 推播來源檢視表
        * 規格說明
            * 當`(1)來源`=查表時 致能
            * 參照 [指定檢視表通則][link_ruledialog4], 從本專案中, 挑選檢視表, 回傳並顯示:檢視表名稱
            * 內容異動時, 顯示訊息盒【標題: 系統訊息 / 異動推播來源類別將清除[相關欄位]，是否繼續。 / 按鍵:確定、取消】
                * 確定: 清除欄位:`(3)推播來源檢視表參數`及加註中引用類別的選項為 **推播來源欄位** 的欄位, 並關閉訊息盒
                * 取消: 關閉訊息盒
    * <t id="contentparameterid">(4)過濾</t>
        * 用途說明
            * 意指 推播來源檢視表過濾條件
        * 規格說明
            * 當`(1)來源`=查表時, 致能
            * 參照 [操作條件式通則][link_ruledialog1], 限定:檢視表須同`(2)檢視表`已設定的檢視表, 回傳並顯示:條件說明
    * <t id="keynote">(5)主旨</t>
        * 用途說明
            * 請參考設計案例 [主旨內文(含引用替換字)][link_case1]
        * 規格說
            * 當內容為空值，系統顯示提醒(Placeholder): 主旨, 輸入內容後, 自動消失
            * 自行輸入
    * <t id="content">(6)內文</t>
        * 用途說明
            * 請參考設計案例 [主旨內文(含引用替換字)][link_case1]
        * 規格說明
            * 當內容為空值，系統顯示提醒(Placeholder): 內文, 輸入內容後, 自動消失
            * 自行輸入
    * `(7)替換變數表格`
        * 用途說明
            * 運行時, 發送通知的內容中, 存在需要替換內容值時, 須使用替換變數定義替換內容
            * 請參考設計案例 [主旨內文(含引用替換字)][link_case1]
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
    * `(9)替換字變數`
        * 用途說明
            * 須輸入存在`(5)主旨`或`(6)內文`, 帶有 % 符號的替換字
        * 規格說明
            * 自行輸入
    * `(10)類別`
        * 用途說明
            * 意指 替換字的來源類別
        * 規格說明
            * 下拉選項: 推播來源欄位 / 表單元件 / 表單參數 / 全域變數 / 通知來源欄位 / 推播人
            * 當`(1)來源`=無時, 選項:推播來源欄位, 隱藏
            * 當 [通知對象]`(1)來源`<>查表時, 選項:通知來源欄位, 隱藏
            * 異動時清除欄位:`(11)來源欄位`
        * 作業流程
            * <ps>待補</ps>
    * `(11)來源欄位`
        * 用途說明
        * 規格說明
            * 當`(9)類別`=表單元件: 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體
            * 當`(9)類別`=推播來源欄位: 參照 [挑選檢視表元件通則][link_ruledialog8], 從`(2)檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(9)類別`=表單參數: 參照 [挑選表單參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳:表單參數
            * 當`(9)類別`=全域變數: 參照 [挑選全域變數通則][link_ruledialog10], 從駐留專案中, 進行全域變數挑選, 回傳:全域變數
            * 當`(9)類別`=通知來源欄位: 參照 [挑選檢視表元件通則][link_ruledialog8], 從 [通知對象][link_fieldbreak4]的`(2)檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件料號. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(9)類別`=推播人: 設計者無須輸入內容, 運行時由系統依據 [推播通知_推播人][link_MAENotice_fieldbreak1] 設定的選項內容寫入
        * 作業流程
            * <ps>待補</ps>
    * `(12)連結類別`
        * 用途說明
            * 在裝置上點擊推播訊息時, 要進行的超連結動作, 各選項說明如下:
                * 超連結表單: 點擊後開啟一張指定的MAE表單
                * 超連結按鍵: 點擊後執行一個指定的功能按鍵
                * 超連結Google行事曆: 點擊後開啟Google行事曆網頁
                * 超連結網址: 點擊後開啟網頁網址
        * 規格說明
            * 下拉選項: 超連結表單 / 超連結按鍵 / 超連結Google行事曆 / 超連結網址
            * 異動時, 清除欄位:`(13)連結內容`
        * 作業流程
            * <ps>待補</ps>
    * `(13)連結內容`
        * 用途說明
        * 規格說明
            * 欄位於編輯狀態 或 單據於瀏覽狀態 且連結內容區塊存在內容值 時, 致能
            * 當未設定時顯示: 尚未設定 灰色字體(#aaa)
            * 依下列規則超連結開啟對應的連結內容設定介面, 該單關閉後須依規則顯示內容
                * 當`(12)連結類別`=超連結表單: 開啟 [超連結表單][link_linkform] ; 顯示: *表單名稱*【過濾條件:*條件內容*】
                * 當`(12)連結類別`=超連結按鍵: 開啟 [超連結按鍵][link_linkbutton] ; 顯示: *表單名稱* 按鍵.*按鍵名稱*
                * 當`(12)連結類別`=超連結Google行事曆: 開啟 [超連結Google行事曆][link_linkgooglecalendar] ; 顯示: 建立行事曆活動
                * 當`(12)連結類別`=超連結網址:  開啟 [超連結網址][link_linkurl] ; 顯示: *網址元件名稱*【網址參數:*運算式名稱*】
        * 作業流程
            * <ps>待補</ps>
    * `(14)儲存連結資訊`
        * 用途說明
        * 規格說明
            * 欄位於編輯狀態 或 單據於瀏覽狀態 且儲存連結資訊區塊存在內容值 時, 致能
            * 系統預設:未勾選
            * 當未勾選時, 儲存連結資訊區塊 隱藏
            * 當`(12)連結類別`=超連結表單或超連結按鍵時, 才致能 ; 否則除能
            * 當有勾選時,
                * 儲存連結資訊區塊 未設定時, 顯示:尚未設定 灰色字體(#aaa)
                * 可超連結開啟[儲存連結資訊][link_savelinkinfo], 關單後顯示: *資料表名稱*
        * 作業流程
            * ![pic][image_OpenSaveLinkInfo]

* <p id="fieldbreak4" style="color:blue;font-weight:bold">通知對象</p>  

    * ![pic][image_Annotation_Notice_Block4]
    * <t id="noticetype">(1)來源</t>
        * 用途說明
            * 意指 通知對象來源
        * 規格說明
            * 下拉選項: 表單元件 / 查表 / 推播來源欄位 / 表單參數 / 全域變數
            * 系統預設: 查表
            * 當 [推播內容][link_fieldbreak3]的`(1)來源`=無時, 選項:推播來源欄位 隱藏
    * `(2)檢視表`
        * 用途說明
            * 意指 通知對象來源檢視表
        * 規格說明
            * 當`(1)來源`=查表時, 致能
            * 參照 [挑選檢視表通則][link_ruledialog4], 從駐留專案中, 進行檢視表挑選, 回傳並顯示: 檢視表名稱
            * 當內容異動時, 清空 `(3)檢視表參數`
    * `(4)過濾`
        * 用途說明
            * 意指 通知對象來源檢視表過濾條件
        * 規格說明
            * 當`(1)來源`=查表時, 致能
            * 參照 [操作條件式通則][link_ruledialog1], 限定: 使用`(2)檢視表`、上層表格=郵件來源、上層來源類別=1.郵件, 回傳並顯示: 條件說明
    * <t id="useraccount">(5)使用者帳號</t>
        * 用途說明
        * 規格說明
            * 當`(1)來源`=表單元件: 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳:表單元件 ; 若元件為 個資加密且已解密欄位 或 密碼欄位, 則該元件顯示紅色字體
            * 當`(1)來源`=查表: 參照 [挑選檢視表元件通則][link_ruledialog8], 從`(2)檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(1)來源`=推播來源欄位: 參照 [挑選檢視表元件通則][link_ruledialog8], 從 [推播內容][link_fieldbreak3]的`(2)檢視表`中, 進行檢視表元件挑選, 回傳:檢視表元件. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(1)來源`=表單參數: [挑選表單參數通則][link_ruledialog9], 從駐留表單中, 進行表單參數挑選, 回傳:表單參數
            * 當`(1)來源`=全域變數: [挑選全域變數通則][link_ruledialog10], 從駐留專案中, 進行全域變數挑選, 回傳:全域變數
    
* <p id="fieldbreak5" style="color:blue;font-weight:bold">推播資訊</p>  

    * ![pic][image_Annotation_Notice_Block5]
    * `(1)另存推播記錄`
        * 用途說明
        * 規格說明
            * 欄位於編輯狀態 或 單據於瀏覽狀態 且推播資訊區塊存在內容 時, 致能
            * 系統預設: 未勾選
            * 當未勾選時, 推播資訊區塊 隱藏
            * 當有勾選時,
                * 推播資訊區塊 未設定時, 顯示:尚未設定 灰色字體(#aaa)
                * 可超連結開啟[儲存推播資訊][link_savenoticeinfo], 關單後顯示:*表格名稱* 結果欄位.*通知發送結果欄位*


## <div id="save-action">儲存檢控</div>
* 不允空白檢控, 符合條件時, 顯示訊息盒, 並以紅框線標註錯誤的欄位
    * 訊息盒:【標題: 執行存回，發生下列錯誤 / 訊息內容: 以下資料未填寫正確 *錯誤欄位名* / 按鍵: 確定】
        * 確定: 關閉訊息盒 
    * [推播內容][link_fieldbreak3]
        * `主旨`、`內文`、`連結字變數`、`連結類別`、`連結內容`, 不允空白
        * 當`替換字變數`有值時,
            * 內容值中間不能出現空白格
            * `類別`、`來源欄位`, 不允空白
    * [通知對象][link_fieldbreak4]
        * `來源`, 不允空白
        * 當`來源`=查表時, 則`檢視表`, 不允空白
* 其它檢控
    * [基本][link_fieldbreak1]的`優先序`: 同一按鍵的各加註內容順序不允重複; 錯誤時提示訊息
    * [推播人][link_fieldbreak2]的`推播人`: 選項必須有值
    * 檢查下列加註介面中引用推播來源是否與本單推播來源不同
        * 連結內容
            * [連結內容_超連結表單][link_linkform]
            * [連結內容_超連結按鍵][link_linkbutton]
            * [連結內容_超連結Google行事曆][link_linkgooglecalendar]
        * [儲存推播資訊][link_savenoticeinfo]
        * [儲存連結資訊][link_savelinkinfo]
    * [推播內容][link_fieldbreak3]
        * 若`連結類別`不等於超連結表單或超連結按鍵 且 `儲存連結資訊`有設定時, 跳出詢問盒【標題: 系統訊息 / 訊息內容: 當未設定超連結表單與超連結資訊不支援寫入儲存連結資訊，是否清除? / 按鍵: 確定、取消】
            * 確定: 清除欄位:`儲存連結資訊`, 並關閉訊息盒
            * 取消: 關閉訊息盒
        * 若`類別`=推播來源欄位 且`檢視表`未設定時, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 請選擇"推播來源未設定查表"。 / 按鍵:確定】
            * 確定: 關閉訊息盒
        * 若`類別`=通知來源欄位 且`檢視表`未設定時, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 請選擇"通知來源未設定查表"。 / 按鍵:確定】
            * 確定: 關閉訊息盒
* 作業流程
    * <ps>待補</ps>

## <div id="save-desc">儲存說明</div>
* 規格說明
    * 當下列[條件式]來源與引用條件式的來源檢視表不同時，於後端覆寫條件式來源表格，條件式明細不異動
    * 當下列[條件式]上層表格與郵件來源表格不同時，於後端覆寫條件式上層表格，條件式明細不異動
* 作業流程
    * ![pic][image_Save]



<!-- 圖片 -->
[image_button_STD]:attachment/Annotation_Notice.png
[image_Annotation_Notice_Block1]:attachment/Annotation_Notice_Block1.png "基本"
[image_Annotation_Notice_Block2]:attachment/Annotation_Notice_Block2.png "推播人"
[image_Annotation_Notice_Block3]:attachment/Annotation_Notice_Block3.png "推播內容"
[image_Annotation_Notice_Block4]:attachment/Annotation_Notice_Block4.png "通知對象"
[image_Annotation_Notice_Block5]:attachment/Annotation_Notice_Block5.png "推播資訊"
[image_Open]:attachment/BAMAENotice-Open.png "推播通知-開啟"
[image_NoticeSourceType]:attachment/BAMAENotice-NoticeSourceType.png "推播通知-推播內容.來源"
[image_OpenSaveLinkInfo]:attachment/BAMAENotice-OpenSaveLinkInfo.png "推播通知-推播內容.儲存連結資訊"
[image_Save]:attachment/BAMAENotice-Save.png "推播通知-儲存"



<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_fieldbreak2]: #fieldbreak2 "欄位說明/推播人"
[link_fieldbreak3]: #fieldbreak3 "欄位說明/推播內容"
[link_fieldbreak4]: #fieldbreak4 "欄位說明/通知對象"
[link_savelinkinfo]:MAENotice-SaveLinkInfo.md "儲存連結資訊"
[link_savenoticeinfo]:MAENotice-SaveNoticeInfo.md "儲存推播資訊"
[link_linkform]:MAENotice-Link-Form.md "連結內容_超連結表單"
[link_linkbutton]:MAENotice-Link-Button.md "連結內容_超連結按鍵"
[link_linkgooglecalendar]:MAENotice-Link-GoogleCalendar.md "連結內容_超連結Google行事曆"
[link_linkurl]:MAENotice-Link-URL.md "連結內容_超連結網址"
[link_parameter]:/8.10.0/IDE/Specification/Parameter/README.md "共用通則_開啟單據/設定表單參數通則"
  
[link_rulebutton3]:/8.10.0/IDE/Specification/RulesButton/README#rulebutton3 "共用通則_按鍵/操作表格記錄通則"
[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother2]:/8.10.0/IDE/Specification/RulesDialog/README#ruleother7 "共用通則_其它/按鍵加註-執行條件表格通則"
[link_ruledialog1]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog2]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruledialog4]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/挑選檢視表通則"
[link_ruledialog7]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruledialog8]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_ruledialog9]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog9 "共用通則_開啟單據/挑選表單參數通則"
[link_ruledialog10]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog10 "共用通則_開啟單據/挑選全域變數通則"
[link_ruledialog11]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog11 "共用通則_開啟單據/設定按鍵執行條件表格通則"

[link_case1]:DesignCaseDes.md#case1