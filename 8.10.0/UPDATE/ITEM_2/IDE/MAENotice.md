### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/06

### <div id="trac">TRAC</div>
* 待開 

## <div id="notice-layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_button_STD]
    * RWD
        * 同STD
    * MAE</br>
        * 同STD

* [版面資訊通則][link_ruleother1]

## <div id="notice-form-action">動作說明</div>

* 依規格定義-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格定義-主畫面 工具列.編修鍵, 進入本單的編輯模式

## <div id="notice-object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_Annotation_Notice_Block1]
    * `(1)按鈕名稱`
        * 用途說明
        * 規格說明
            * 參照 [使用多語詞庫通則][link_ruledialog2], 回傳:按鍵多語料號, 顯示:多語詞彙
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示傳入的按鍵料號
    * `(3)優先序`
        * 用途說明
        * 規格說明
            * 自行輸入, 1~999
    * `(4)執行條件`
        * 用途說明
        * 規格說明
            * 參照 [使用按鍵加註-執行條件表格通則][link_ruleother2]

* <p id="fieldbreak2" style="color:blue;font-weight:bold">推播人</p>  

    * ![pic][image_Annotation_Notice_Block2]
    * `(1)推播人`
        * 用途說明
        * 規格說明
            * 單選選項: 管理者 / 使用者
            * 系統預設: 管理者        

* <p id="fieldbreak3" style="color:blue;font-weight:bold">主旨內文</p>  

    * ![pic][image_Annotation_Notice_Block3]
    * `(1)來源`
        * 用途說明
            * 意指 推播來源類別
        * 規格說明
            * 下拉選項: 無 / 查表
            * 系統預設: 無
            * 當切換為無時, 清除 推播來源檢視表參數、引用推播來源欄位的替代來源欄位、推播對象使用者序號
        * 作業流程
    * `(2)檢視表`
        * 用途說明
            * 意指 推播來源檢視表
        * 規格說明
            * 當`(1)來源`=查表時 致能
            * 參照 [指定檢視表通則][link_ruledialog3], 回傳:替代檢視表料號
            * 內容異動時, 清空 推播來源檢視表參數、引用推播來源欄位的替代來源欄位、推播對象使用者序號
        * 作業流程
    * `(3)檢視表參數`
        * 用途說明
            * 意指 推播來源檢視表傳虒參數
        * 規格說明
            * 當`(1)來源`=查表時, 致能
            * 參照 [設定檢視表參數通則][link_ruledialog4], 傳遞:郵件來源邏表料號、邏表名稱、檢視狀態、表單料號; 
        * 作業流程
    * `(4)過濾`
        * 用途說明
            * 意指 推播來源檢視表過濾條件
        * 規格說明
            * 當`(1)來源`=查表時, 致能
            * 參照 [操作條件式通則][link_ruledialog5], 限定:來源表格=郵件來源檢視表料號, 回傳:條件ID, 顯示條件說明
            * 執行清除鍵時, 清除 條件ID及過濾條件內容
        * 作業流程
    * `(5)主旨`
        * 用途說明
        * 規格說
            * 自行輸入
    * `(6)內文`
        * 用途說明
        * 規格說明
            * 自行輸入
    * `(7)替代變數表格`
        * 用途說明
        * 規格說明
            * 參照 [操作一般表格通則][link_ruleother3]
    * `(8)項次`
        * 用途說明
        * 規格說明
            * 依流水依資料列顯示
    * `(9)替換字變數`
        * 用途說明
        * 規格說明
            * 自行輸入
    * `(10)類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 推播來源欄位 / 表單元件 / 表單參數 / 全域變數 / 通知來源欄位
            * 當`(1)來源`=無時, 推播來源欄位, 隱藏
            * 當 [通知對象]`(1)來源`<>查表 時, 通知來源欄位, 隱藏
        * 作業流程
    * `(11)來源欄位`
        * 用途說明
        * 規格說明
            * 當`(9)類別`=表單元件: [挑選表單元件通則][link_ruledialog6], 過濾:表單料號 回傳:表單元件料號. 若元件 (個資加密==true 且 個資解密=false ) 或 密碼處理=true, 則該元件顯示紅色字體
            * 當`(9)類別`=推播來源欄位: [挑選檢視表元件通則][link_ruledialog7], 限定:推播來源檢視表料號, 回傳:檢視表元件料號. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(9)類別`=表單參數，[挑選表單參數通則][link_ruledialog8], 過濾:表單料號 回傳:表單參數料號
            * 當`(9)類別`=全域變數，[挑選全域變數通則][link_ruledialog9], 過濾:專案料號 回傳:全域變數料號
            * 當`(9)類別`=通知來源欄位: [挑選檢視表元件通則][link_ruledialog7], 限定:通知來源檢視表料號, 回傳:檢視表元件料號. 因查表來源暫不支援個資解密, 故不提供變色處理
        * 作業流程
    * `(12)連結類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 超連結表單 / 超連結按鍵 / 超連結Google行事曆
        * 作業流程
    * `(13)連結內容`
        * 用途說明
        * 規格說明
            * 依下列規則超連結開啟對應的連結內容設定介面, 關單後帶回JSON Data
                * 當`(12)連結類別`=超連結表單: [連結內容_超連結表單][link_linkform]
                * 當`(12)連結類別`=超連結按鍵: [連結內容_超連結按鍵][link_linkbutton]
                * 當`(12)連結類別`=超連結Google行事曆: [連結內容_超連結Google行事曆][link_linkgooglecalendar]
            * 當未設定時顯示 尚未設定 灰色字體(#aaa)
            * 當已設定時, 依下列規則顯示內容
                * 當`(12)連結類別`=超連結表單: 表單名稱【過濾條件:XXX】
                * 當`(12)連結類別`=超連結按鍵: 表單名稱 按鍵.按鍵名稱
                * 當`(12)連結類別`=超連結Google行事曆: 建立行事曆活動
        * 作業流程 
    * `(14)儲存連結資訊`
        * 用途說明
        * 規格說明
            * 當值為false時, 儲存連結資訊區塊隱藏,預設false 
            * 當值為true時, 可超連結開啟[儲存連結資訊][link_savelinkinfo]，關單後帶回JSON Data
            * 當未設定時, 顯示尚未設定 灰色字體(#aaa)
            * 當已設定時, 顯示表格名稱
            * 當`(12)連結類別`=超連結表單、超連結按鍵時, 才致能 ; 否則除能
        * 作業流程

* <p id="fieldbreak4" style="color:blue;font-weight:bold">通知對象</p>  

    * ![pic][image_Annotation_Notice_Block4]
    * `(1)來源`
        * 用途說明
            * 意指 通知對象來源
        * 規格說明
            * 下拉選項: 固定對象 / 表單元件 / 查表 / 推播來源欄位 / 表單參數 / 全域變數
            * 系統預設: 查表
            * 當[主旨內文][link_fieldbreak3]`(1)來源`=無時, 推播來源欄位隱藏
    * `(2)檢視表`
        * 用途說明
            * 意指 通知對象來源檢視表
        * 規格說明
            * 當`(1)來源`=查表時, 致能
            * 參照 [指定檢視表通則][link_ruledialog3], 回傳:對象檢視表料號
            * 當內容異動時, 清空 通知對象檢視表表參數
    * `(3)檢視表參數`
        * 用途說明
            * 意指 通知對象來源檢視表傳遞參數
        * 規格說明
            * 當`(1)來源`=查表時, 致能
            * 參照 [設定檢視表參數通則][link_ruledialog4], 傳遞:通知對象檢視表料號、檢視表名稱、檢視狀態、表單料號、上層表格=推播來源、上層來源類別=1.郵件
    * `(4)過濾`
        * 用途說明
            * 意指 通知對象來源檢視表過濾條件
        * 規格說明
            * 當`(1)來源`=查表時，致能
            * 參照 [操作條件式通則][link_ruledialog5], 限定:來源表格=通知對象檢視表料號, 上層表格=郵件來源 上層來源類別=1.郵件, 回傳:條件ID
            * 執行清除鍵時, 清除 條件ID及過濾條件內容  
    * `(5)使用者序號`
        * 用途說明
        * 規格說明
            * 當`(1)來源`=固定對象: 自行輸入
            * 當`(1)來源`=表單元件: [挑選表單元件通則][link_ruledialog6], 過濾:表單料號 回傳:表單元件料號. 若元件 (個資加密==true 且 個資解密=false ) 或 密碼處理=true, 則該元件顯示紅色字體
            * 當`(1)來源`=查表: [挑選檢視表元件通則][link_ruledialog7], 限定:通知對象檢視表料號, 回傳:檢視表元件料號. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(1)來源`=郵件來源欄位: [挑選檢視表元件通則][link_ruledialog7], 限定:推播來源檢視表料號, 回傳:檢視表元件料號. 因查表來源暫不支援個資解密, 故不提供變色處理
            * 當`(1)來源`=表單參數: [挑選表單參數通則][link_ruledialog8], 過濾:表單料號 回傳:表單參數料號
            * 當`(1)來源`=全域變數: [挑選全域變數通則][link_ruledialog9], 過濾:專案料號 回傳:全域變數料號
    
* <p id="fieldbreak5" style="color:blue;font-weight:bold">推播資訊</p>  

    * ![pic][image_Annotation_Notice_Block5]
    * `(1)發送異常`
        * 用途說明
        * 規格說明
            * 單選選項: 忽略 / 停止
            * 系統預設: 停止
    * `(2)儲存推播資訊`
        * 用途說明
        * 規格說明
            * 當值為false時, 郵件資訊區塊隱藏, 預設false 
            * 當未設定時, 顯示尚未設定 灰色字體(#aaa)
            * 當已設定時, 顯示 表格名稱 結果欄位.通知發送結果欄位
            * 當值為true時, 可超連結開啟[儲存推播資訊][link_savenoticeinfo], 關單後帶回JSON Data

## <div id="notice-save-action">儲存檢控</div>
* 不允空白檢控, 符合條件時, 顯示訊息盒, 並以紅框線標註錯誤的欄位
    * 訊息盒:【標題: 執行存回，發生下列錯誤 / 訊息內容: 以下資料未填寫正確 </n> *錯誤欄位名* / 按鍵: 確定】
        * 確定: 關閉訊息盒 
    * [通知對象][image_Annotation_Notice_Block4]
        * `(1)來源`, 不允空白
        * 當`(1)來源`=查表時, 則`(2)檢視表`, 不允空白
    * [主旨內文][image_Annotation_Notice_Block3]
        * `(5)主旨`、`(6)內文`、`(12)連結字變數`、`(13)連結類別`、`(14)連結內容`, 不允空白
        * 當`(9)替換字變數` 有值時, 則`(10)類別`、`(11)來源欄位`, 不允空白
* 其它檢控
    * [基本][image_Annotation_Notice_Block1]`(3)優先序`: 同一按鍵的各加註內容順序不允重複; 錯誤時提示訊息
    * [推播人][image_Annotation_Notice_Block2]`(1)推播人`: 選項必須有值
    * 檢查下列加註介面中引用推播來源是否與本單推播來源不同
        * [連結內容]
        * [儲存推播資訊]
        * [儲存連結資訊]
    * 若[主旨內文][image_Annotation_Notice_Block3]`(13)連結類別`不等於超連結表單或超連結按鍵 且 `(15)儲存連結資訊`有設定時, 跳出詢問清除訊息 ; 若選否則返回編輯. 

* 替代類別=查表時, 替代邏表, 不允空白
* 若連結內容有設定帳號驗證時則必須填寫使用者序號


## <div id="notice-button-desc">按鍵說明</div>
* 儲存
    * 用途說明
    * 規格說明
        * 當下列[條件式]來源與引用條件式的來源檢視表不同時，於後端覆寫條件式來源表格，條件式明細不異動
            * [主旨內文][image_Annotation_Notice_Block3]`(4)過濾`
            * [通知對象][image_Annotation_Notice_Block4]`(4)過濾`
            * [主旨內文][image_Annotation_Notice_Block3]`(14)連結內容`
            * [連結內容_超連結表單][link_linkform]`(3)過濾`
            * [連結內容]超連結按鍵過濾條件
         * 當下列[條件式]上層表格與郵件來源表格不同時，於後端覆寫條件式上層表格，條件式明細不異動
    * 作業流程
        * ![pic][動作流程圖]







<!-- 圖片 -->
[image_button_STD]:attachment/Annotation_Notice.png        
[image_Annotation_Notice_Block1]:attachment/Annotation_Notice_Block1.png "基本"
[image_Annotation_Notice_Block2]:attachment/Annotation_Notice_Block2.png "推播人"
[image_Annotation_Notice_Block3]:attachment/Annotation_Notice_Block3.png "主旨內文"
[image_Annotation_Notice_Block4]:attachment/Annotation_Notice_Block4.png "通知對象"
[image_Annotation_Notice_Block5]:attachment/Annotation_Notice_Block5.png "推播資訊"


<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_fieldbreak3]: #fieldbreak3 "欄位說明/主旨內文"
[link_savelinkinfo]:MAENotice-SaveLinkInfo.md "儲存連結資訊"
[link_savenoticeinfo]:MAENotice-SaveNoticeInfo.md "儲存推播資訊"
[link_linkform]:MAENotice-Link-Form.md "連結內容_超連結表單"
[link_linkbutton]:MAENotice-Link-Button.md "連結內容_超連結按鍵"
[link_linkgooglecalendar]:MAENotice-Link-GoogleCalendar.md "連結內容_超連結Google行事曆"
  

[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother2]:/8.10.0/IDE/Specification/RulesDialog/README#ruleother7 "共用通則_其它/按鍵加註-執行條件表格通則"
[link_ruleother3]:/8.10.0/IDE/Specification/RulesDialog/README#ruleother8 "共用通則_其它/操作一般表格通則"

[link_ruledialog2]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開啟單據/指定檢視表通則"
[link_ruledialog4]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog5 "共用通則_開啟單據/設定檢視表參數通則"
[link_ruledialog5]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog6]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruledialog7]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_ruledialog8]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog9 "共用通則_開啟單據/挑選表單參數通則"
[link_ruledialog9]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog10 "共用通則_開啟單據/挑選全域變數通則"