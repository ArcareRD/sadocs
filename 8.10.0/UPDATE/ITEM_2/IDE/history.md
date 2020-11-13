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
    |推播通知_推播資訊, 取消 **發送異常** 設定                             | [推播通知_推播資訊][link_fieldbreak5] |          
    |推播通知_主旨內文, 增加固定訊息告知推播通知的訊息，長度大小限制不可超過4K | [推播通知_主旨內文][link_fieldbreak3] | 
    |推播通知_主旨內文, 增加連結類別: 超連結網址 (做法彷嵌入物件:網頁)        | [推播通知_主旨內文][link_fieldbreak3]、[連結內容_超連結網址][link_linkurl]、[運算式][link_expression] |
    |推播通知_通知對象, 原挑選使用者序號, 改為 使用者帳號                    | [推播通知_通知對象][link_fieldbreak4] |
    





<!-- 超連結 -->
[link_fieldbreak3]:MAENotice.md#fieldbreak3 "欄位說明/主旨內文"
[link_fieldbreak4]:MAENotice.md#fieldbreak4 "欄位說明/通知對象"    
[link_fieldbreak5]:MAENotice.md#fieldbreak5 "欄位說明/推播資訊"
[link_linkurl]:MAENotice-Link-URL.md "連結內容_超連結網址"
[link_expression]:Expression.md "運算式"

[Trac#8193]:http://trac.uneec.com/trac/neco/ticket/8193 "#8193"