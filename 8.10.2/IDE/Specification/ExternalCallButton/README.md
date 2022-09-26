## <div id="layout">版面相關</div>
* 版面</br>
    ![pic][image_ExternalCallButton]
* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 開啟 以Dailog on Top 的方式開啟

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">搜尋與其它操作區塊</p>

    ![pic][image_fieldbreak1]
    * `(1)OnlineHelp`
        * 用途說明
        * 規格說明
            * [OnlineHelp通則][link_ruleother2]
    * `(2)搜尋區塊`
        * 用途說明
        * 規格說明
            * [搜尋區塊操作通則][link_rulebutton1]
    * `(5)搜尋鍵`
        * 用途說明
        * 規格說明
            * 由 架構/系統資源/SR06.圖示設定 開啟, 過濾共用資料庫的資料
            * 其餘, 過濾專案資料庫下的資料
    * `(3)單據異動記錄按鍵群`
        * 用途說明
        * 規格說明
            * [單據異動資料按鍵操作通則][link_rulebutton2]
    * `(4)刪除鍵`
        * 用途說明
        * 規格說明    
            * 用途類別=2:Wizard用, 跳訊息"該圖示為表單精靈使用，不允刪除"

* <p id="fieldbreak2" style="color:blue;font-weight:bold">基本區塊</p>

    ![pic][image_fieldbreak2]
    * `(1)表單名稱`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單通則][link_ruledialog6], 從駐留專案中, 進行表單挑選, 回傳並顯示: 表單名、表單料號
            * 當切換不同表單, 顯示訊息盒【標題: 系統訊息 / 變更表單將會清除按鍵名稱、傳入參數表格、回傳參數表格，是否繼續? / 按鍵:確定、取消】
                * 確定: 清除欄位:`(3)按鍵名稱`、`傳入參數表格`、`回傳參數表格`, 並關閉訊息盒
                * 取消: 關閉訊息盒
    * `(2)表單料號`
        * 用途說明
        * 規格說明
            * 由`(1)表單名稱`帶入並顯示料號
    * `(3)按鍵名稱`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單按鍵通則][link_ruledialog13], 限定: `(1)表單名稱`及下列條件, 進行按鍵挑選, 回傳並顯示: 按鍵名、按鍵料號
            * 以下列出支援條件
                * 支援加註
                    |加註行為 |進階條件 |
                    |--------|--------|
                    |[按鍵加註_資料交易][link_BAPort] |RSD開關類型=遠端 |
                    |[按鍵加註_邏輯函數][link_BALogicalFunction] | |
                    |[按鍵加註_郵件發送][link_BAMail] | |
                    |[按鍵加註_外部執行][link_BAExecute] |檔案合併: 須內含交換格式/匯出 且 郵件夾檔皆為勾選<br>執行程式 |
                    |[按鍵加註_資料交換][link_BAExchange] |匯出 且 郵件夾檔為勾選 |
                    |[按鍵加註_開啟報表][link_BAReport] |開啟方式=郵件夾檔、存入資料庫 |
                    |[按鍵加註_預存程序][link_BAStoreProcedure] | |
                    |[按鍵加註_推播通知][link_BANotice] | |
                * 全域變數不允存在以下設定
                    |加註頁面 |設定欄位 |
                    |--------|--------|
                    |[按鍵加註_資料交易][link_BAPort] |回傳參數/`全域變數` |
                    |[按鍵加註_外部執行][link_BAExecute] |成功接收/`接收內容` (接收類型=全域變數)<br>失敗接收/`接收內容` (接收類型=全域變數) |
                    |[按鍵加註_預存程序][link_BAStoreProcedure] |參數設定/`回傳內容` |
                * 不支援所有系統鍵、wTBMenu.功能選單
                    * wMBExport.匯出(選單列): 非系統匯出除外
    * `(4)按鍵料號`
        * 用途說明
        * 規格說明
            * 由`(3)按鍵名稱`帶入並顯示料號
    * `(5)功能說明`
        * 用途說明
        * 規格說明
            * 自行輸入

* <p id="fieldbreak3" style="color:blue;font-weight:bold">傳入參數區塊</p>

    ![pic][image_fieldbreak3]
    * `(1)類別`
        * 用途說明
        * 規格說明
            * 下拉選項 Json, 預設 Json
    * `(2)傳入參數表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
    * `(3)項次`
        * 用途說明
        * 規格說明
            * 依序給流水號
    * `(4)設定類型`
        * 用途說明
        * 規格說明
            * 依參數載入內容顯示 檔區欄位/表單元件/表單接收參數/全域變數
    * `(5)傳入參數載入`
        * 用途說明
        * 規格說明
            * 載入[基本][link_fieldbreak2]`按鍵名稱`所設定的加註中, 有設定本單的檔區欄位、元件、接收參數、全域變數者，範圍如下
                * [按鍵加註_執行限制][link_BALimitation]: `前置條件`、`判斷條件`、`訊息替代`
                * [按鍵加註_資料交易][link_BAPort]: `執行條件`、傳遞參數/`給值內容`、`訊息替代`
                * [按鍵加註_資料交換][link_BAExchange]: 
                    * `執行條件`
                    * 匯入: `指定檔案元件`
                    * 匯出: `過濾條件`、`傳遞參數`
                    * 表格對應: `過濾條件`、`傳遞參數`
                * [按鍵加註_郵件發送][link_BAMail]
                    * `執行條件`
                    * 主旨內文
                        * `過濾條件`、`傳遞參數`、替代/`來源欄位`
                        * 連結/超連結表單: `過濾條件`、`傳遞參數`
                        * 連結/元件插圖: `插圖檔名`、`插圖欄位`
                        * 連結/資料表插圖: `過濾條件`
                        * 連結/檢視表插圖: `過濾條件`、`傳遞參數`
                        * 連結/超連結按鍵: `成功訊息替代`、`失敗訊息替代`、傳遞/`傳遞內容`
                        * 連結/超連結Google行事曆: `標題`、`內容`、`欄位`、`日期起`、`日期迄`、`時間起`、`時間迄`
                        * 儲存連結資訊: `給值內容`
                    * 收件對象
                        * `過濾條件`、`傳遞參數`、`姓名`、`信箱`、`使用者序號`
                        * 副本: `過濾條件`、`傳遞參數`、`姓名`、`信箱`
                        * 密件副本: `過濾條件`、`傳遞參數`、`姓名`、`信箱`
                    * 夾檔附件: `過濾條件`、`傳遞參數`、`夾檔檔名`、`夾檔檔案`、`檔案櫃記錄欄位`、`檔案唯一號欄位`
                    * 郵件資訊: `給值內容`
                * [按鍵加註_外部執行][link_BAExecute]: 
                    * 執行程式: `執行條件`、`URL過濾條件`、`URL傳遞參數`
                        * 傳遞: `過濾條件`、`傳遞參數`、`傳遞內容`
                * [按鍵加註_邏輯函數][link_BALogicalFunction]: `執行條件`、`來源類型`=條件式、元件、參數、運算式 的 `來源內容` 或 `來源類型`=表單、檢視表 中 `來源內容`的傳遞參數
                * [按鍵加註_開啟報表][link_BAReport]: `執行條件`、存入資料庫/`過濾條件`、存入資料庫/`傳遞參數`
                * [按鍵加註_預存程序][link_BAStoreProcedure]: `執行條件`、參數設定/`傳入內容`、`訊息替代`
                * [按鍵加註_推播通知][link_BANotice]: 
                    * `執行條件`
                    * 推播內容
                        * `推播內容過濾條件`、`推播內容傳遞參數`、`替換字來源欄位`
                        * [超連結表單][link_linkform]: `傳遞參數`、`過濾條件`
                        * [超連結按鍵][link_linkbutton]: `成功訊息替代`、`失敗訊息替代`、`傳遞內容`
                        * [超連結Google行事曆][link_linkgooglecalendar]: `標題給值內容`、`內容給值內容`、`地點給值內容`、`日期起`、`日期迄`、`時間起`、`時間迄`
                        * [超連結網址][link_linkurl]: `網址給值內容`、`網址參數`
                        * [儲存連結資訊][link_savelinkinfo]: `給值內容`
                    * 通知對象: `通知對象過濾條件`、`通知對象傳遞參數`、`通知對象帳號`
                    * [儲存推播資訊][link_savenoticeinfo]: `給值內容`
                * 以上, 載入`(2)傳入參數表格`中, 不存在新增, 存在不異動
    * `(6)設定來源`
        * 用途說明
        * 規格說明
            * 依參數載入內容顯示 參數名稱
    * `(7)參數型態`
        * 用途說明
        * 規格說明
            * 載入後, 檔區欄位及元件, 須依其對應轉至對應的參數型態
                * 備註、全唯碼 → 字串
                * bigint、int、smallint、tinyint → 數字
                * 位元 → 布林
            * 顯示 字串/數字/陣列/物件/日期/日期時間/二進位/布林
    * `(8)參數名稱`
        * 用途說明
        * 規格說明
            * 另行定義參數名稱
    * `(9)參數說明`
        * 用途說明
        * 規格說明
            * 自行輸入參數說明

* <p id="fieldbreak4" style="color:blue;font-weight:bold">回傳參數區塊</p>

    ![pic][image_fieldbreak4]
    * `(1)回傳參數表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
    * `(2)項次`
        * 用途說明
        * 規格說明
            * 依序給流水號
    * `(3)料號`
        * 用途說明
        * 規格說明
            * 依參數載入內容顯示 參數料號
    * `(4)回傳參數載入`
        * 用途說明
        * 規格說明
            * 載入[基本][link_fieldbreak2]`按鍵名稱`下[按鍵加註_資料交易][link_BAPort]中所設定的[資料交易][link_Posting], 將所有`回傳參數`, 載入`(1)回傳參數表格`
    * `(5)參數名稱`
        * 用途說明
        * 規格說明
            * 依參數載入內容顯示 參數名稱
    * `(6)參數型態`
        * 用途說明
        * 規格說明
            * 依參數載入內容顯示 參數型態
            * 顯示 文字/數字/日期/邏輯
    * `(7)多筆`
        * 用途說明
        * 規格說明
            * 依參數載入內容顯示 是否為多筆
    * `(8)參數說明`
        * 用途說明
        * 規格說明
            * 依參數載入內容顯示 參數說明

## <div id="save-action">儲存檢控</div>
* 不允空白檢控, 規則參照 [存回不允空白檢控通則][link_ruleother7]
    * [基本][link_fieldbreak2]
        * `表單名稱`、`按鍵名稱` 不允空白
    * [傳入參數][link_fieldbreak3]
        * `傳入參數表格`有記錄時, `參數名稱` 不允空白

* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
    * `表單名稱`+`按鍵名稱`, 不允重複存在

<!-- 圖片 -->
[image_ExternalCallButton]:attachment/ExternalCallButton.png
[image_fieldbreak1]:attachment/ExternalCallButton_block1.png
[image_fieldbreak2]:attachment/ExternalCallButton_block2.png
[image_fieldbreak3]:attachment/ExternalCallButton_block3.png
[image_fieldbreak4]:attachment/ExternalCallButton_block4.png

<!-- 超連結 -->
[link_fieldbreak2]:#fieldbreak2 "基本區塊"
[link_fieldbreak3]:#fieldbreak3 "傳入參數區塊"
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother2]:../RulesOther/README#ruleother2 "共用通則_其它/OnlineHelp通則"
[link_rulebutton1]:../RulesButton/README#rulebutton1 "共用通則_操作按鍵/搜尋區塊操作通則"
[link_rulebutton2]:../RulesButton/README#rulebutton2 "共用通則_操作按鍵/單據異動資料按鍵操作通則"
[link_ruleother13]:../RulesOther/README#ruleother13 "共用通則_其它/開單搜尋挑選單據動作通則"
[link_ruledialog6]:../RulesDialog/README#ruledialog6 "共用通則_開啟單據/挑選表單通則"
[link_ruledialog13]:../RulesDialog/README#ruledialog13 "共用通則_開啟單據/挑選表單按鍵通則"
[link_rulebutton3]:../RulesButton/README#rulebutton3 "共用通則_按鍵操作/操作表格記錄通則"
[link_BALimitation]:../BALimitation/README "按鍵加註_執行限制"
[link_BAPort]:../BAPort/README "按鍵加註_資料交易"
[link_BAMail]:../BAMail/README "按鍵加註_郵件發送"
[link_BAExecute]:../BAExecute/README "按鍵加註_外部執行"
[link_BAExchange]:../BAExchange/README "按鍵加註_資料交換"
[link_BAReport]:../BAReport/README "按鍵加註_開啟報表"
[link_BALogicalFunction]:../BALogicalFunction/README "按鍵加註_邏輯函數"
[link_BAStoreProcedure]:../BAStoreProcedure/README "按鍵加註_預存程序"
[link_BANotice]:../BANotice/README "按鍵加註_推播通知"
[link_linkform]:../BANotice/MAENotice-Link-Form.md "連結內容_超連結表單"
[link_linkbutton]:../BANotice/MAENotice-Link-Button.md "連結內容_超連結按鍵"
[link_linkgooglecalendar]:../BANotice/MAENotice-Link-GoogleCalendar.md "連結內容_超連結Google行事曆"
[link_linkurl]:../BANotice/MAENotice-Link-URL.md "連結內容_超連結網址"
[link_savelinkinfo]:../BANotice/MAENotice-SaveLinkInfo.md "儲存連結資訊"
[link_savenoticeinfo]:../BANotice/MAENotice-SaveNoticeInfo.md "儲存推播資訊"
[link_Posting]:../Posting/README "資料交易"
[link_ruleother7]:../RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:../RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"