變更記錄
===
| 版本 |
| :---: |
| [8.10.0](#v8_10_0) |

***
### <a id='v8_10_0'></a>8.10.0
* Added Prenkt 2020/11/5: IDE_因應MAE擴充推播功能相關擴充 ([Trac#8193])

* Changed Prenkt 2020/11/12: 第一版需求確認後，提出下列規格異動 
    |異動內容 | 對應文件 |
    |-------- |--------- |
    |按鍵加註/推播通知/推播資訊, 取消 **發送異常** 設定                             | [推播通知_推播資訊][link_fieldbreak5] |          
    |按鍵加註/推播通知/主旨內文, 增加固定訊息告知推播通知的訊息，長度大小限制不可超過4K | [推播通知_主旨內文][link_fieldbreak3] | 
    |按鍵加註/推播通知/主旨內文, 增加連結類別: 超連結網址 (做法彷嵌入物件:網頁)        | [推播通知_主旨內文][link_fieldbreak3]、[連結內容_超連結網址][link_linkurl]、[運算式][link_expression] |
    |按鍵加註/推播通知/通知對象, 原挑選使用者序號, 改為 使用者帳號                    | [推播通知_通知對象][link_fieldbreak4] |
    
* Changed Prenkt 2020/11/20: 第二版需求確認後，提出下列規格異動
    |異動內容 | 對應文件 |
    |-------- |--------- |
    |按鍵加註/推播通知, 增加欄位用途說明、主旨內文及替換字的設計案例                            | [推播通][link_maenotice]、[設計案例][link_case1]|
    |按鍵加註/推播通知/主旨內文, 改名為推播內容 ; 增加內文提醒                                 | [推播通知_推播內容][link_fieldbreak3] |
    |按鍵加註/推播通知/通知對象/使用者帳號, 改名為帳號                                         | [推播通知_通知對象][link_fieldbreak4] |
    |按鍵加註/推播通知/推播資訊/另存推播紀錄/推播發送結果, 改名為儲存結果欄位                    | [儲存推播資訊][link_savenoticeinfo] |
    |按鍵加註/推播通知/推播資訊/連結內容/超連結Google行事曆/日期區間, 改名為時段                 | [超連結Google行事曆][link_linkgooglecalendar] |
    |按鍵加註/推播通知/推播資訊/連結內容/超連結Google行事曆/日期區間/替代類別, 改名為給值來源     | [超連結Google行事曆][link_linkgooglecalendar] |
    |按鍵加註/推播通知/推播資訊/連結內容/超連結表單, 增加欄位用途說明                            | [超連結表單][link_linkform] |
    |按鍵加註/推播通知/推播資訊/連結內容/超連結表單, 增加欄位用途說明                            | [超連結按鍵][link_linkbutton] |
    |規格書, 修正寫法 ; 增加連結內容                                                          | [規格書][link_specification] |

* Changed Prenkt 2021/06/18: #8533 APP:推播功能_超連結變更文字  ([Trac#8533])
    * 異動內容: 增加連結內容的顯示名稱 [異動內容][link_show_name]

* Changed Prenkt 2021/06/21: #8533 APP:推播功能_超連結變更文字  ([Trac#8533])
    * 異體內容: 將 "顯示名稱" 修改為 "提示文字"



<!-- 超連結 -->
[link_maenotice]:BAMAENotice.md "推播通知"
[link_fieldbreak3]:BAMAENotice.md#fieldbreak3 "欄位說明/主旨內文"
[link_fieldbreak4]:BAMAENotice.md#fieldbreak4 "欄位說明/通知對象"
[link_fieldbreak5]:BAMAENotice.md#fieldbreak5 "欄位說明/推播資訊"
[link_linkurl]:MAENotice-Link-URL.md "超連結網址"
[link_savenoticeinfo]:MAENotice-SaveNoticeInfo.md "儲存推播資訊"
[link_linkform]:MAENotice-Link-Form.md "超連結表單"
[link_linkbutton]:MAENotice-Link-Button.md "超連結按鍵"
[link_linkgooglecalendar]:MAENotice-Link-GoogleCalendar.md "連結內容_超連結Google行事曆"

[link_specification]:AffectModify-Specification.md "規格書產出"
[link_expression]:Expression.md "運算式"

[link_case1]:DesignCaseDes.md#case1
[Trac#8193]:http://trac.uneec.com/trac/neco/ticket/8193 "#8193"
[Trac#8533]:http://trac.uneec.com/trac/neco/ticket/8533#comment:2 "#8533"
[link_show_name]:BAMAENotice#link_show_name