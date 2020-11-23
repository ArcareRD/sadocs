### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/08

### <div id="trac">TRAC</div>
* 待開

## <div id="specification_output">規格書產出</div>
* 支援本次新增加註: [按鍵加註-推播通知][link_MAENotice]
    * 按鍵說明_規格定義中, 增加 **推播通知** 加註內容, 格式範例如下:
    | 順序       | 按鍵名稱    | 規格描述                              | 規格定義  |
    | ---------- |----------- | -----------------------------------  | --------- |
    | 依資料排序  | `按鍵名稱`  | 取得該按鍵 [規格備註: 規格描述][link_SpecificationsRemarks] 的內容 | (推播通知)【推播人：`推播人`】【推播來源：(`來源`)`檢視表` (過濾)`過濾`】【推播內容：(`主旨`)`內文`】【連結：(`連結類別`) `連結內容` 】【通知對象：(`來源`)`帳號`】 |

    * 連結內容
        * 當`連結類別`=超連結表單: 取得 [超連結表單][link_linkform] 以下欄位, 組合顯示
            * `表單名稱`, (過濾) `過濾` , (通行碼) `通行碼`, (有效次數) `有效次數`, (執行系統) `執行系統`, 並進行`帳號驗證` 
        * 當`連結類別`=超連結按鍵: 取得 [連結內容_超連結按鍵][link_linkbutton] 以下欄位, 組合顯示
            * `表單名稱`, (按鍵名) `按鍵名` , (通行碼) `通行碼`, (有效次數) `有效次數`, (執行系統) `執行系統`, 並進行`帳號驗證`, (執行後續) 成功: `成功訊息`, 失敗: `失敗訊息`, 傳遞: `參數名稱1` = `傳遞類型`.`傳遞內容`、`參數名稱2` = `傳遞類型`.`傳遞內容`、`參數名稱3` = `傳遞類型`.`傳遞內容`、...
        * 當`連結類別`=超連結Google行事曆: 取得 [連結內容_超連結Google行事曆][link_linkgooglecalendar] 以下欄位, 組合顯示
            * (標題) `類別`.`給值內容`, (內容) `類別`.`給值內容`, (地點) `類別`.`給值內容`, (時段) 來源: `給值來源`, `日期含時間`.`整天`.`格林威治時區`, 日期: `日期起` `時間起`~`日期迄` `時間迄`
        * 當`連結類別`=超連結網址:  取得 [連結內容_超連結網址][link_linkurl] 以下欄位, 組合顯示
            * (網址): `網址欄位類別`.`網址欄位`, (參數) `網址參數`


<!-- 超連結 -->
[link_MAENotice]:BAMAENotice.md "按鍵加註-推播通知"
[link_MAENotice_fieldbreak3]:BAMAENotice.md#fieldbreak3 "欄位說明/推播內容"
[link_conentviewno]:BAMAENotice.md#conentviewno "按鍵加註-推播通知/推播內容/檢視表"
[link_replacetype]:BAMAENotice.md#replacetype "按鍵加註-推播通知/推播內容/來源"
[link_contentparameterid]:BAMAENotice.md#contentparameterid "按鍵加註-推播通知/推播內容/過濾"
[link_keynote]:BAMAENotice.md#keynote "按鍵加註-推播通知/推播內容/主旨"
[link_content]:BAMAENotice.md#content "按鍵加註-推播通知/推播內容/內容"

[link_MAENotice_fieldbreak4]: BAMAENotice.md#fieldbreak4 "按鍵加註-推播通知/通知對象"
[link_noticertype]:BAMAENotice.md#noticertype "按鍵加註-推播通知/通知對象/來源"
[link_useraccount]:BAMAENotice.md#useraccount "按鍵加註-推播通知/通知對象/使用者帳號"
[link_sender]:BAMAENotice.md#sender "按鍵加註-推播通知/推播人"

[link_linkform]:MAENotice-Link-Form.md "連結內容_超連結表單"
[link_linkbutton]:MAENotice-Link-Button.md "連結內容_超連結按鍵"
[link_linkgooglecalendar]:MAENotice-Link-GoogleCalendar.md "連結內容_超連結Google行事曆"
[link_linkurl]:MAENotice-Link-URL.md "連結內容_超連結網址"


[link_SpecificationsRemarks]:/8.10.0/IDE/Specification/SpecificationsRemarks/README.md "規格備註"