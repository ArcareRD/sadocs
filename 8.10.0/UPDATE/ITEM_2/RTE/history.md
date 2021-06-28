變更記錄
===
| 版本 |
| :---: |
| [8.10.0](#v8_10_0) |

***
### <a id='v8_10_0'></a>8.10.0
* Added 正傑 2020/11/4: RTE_因應MAE擴充推播通知功能相關修改 ([Trac#8192])
* Added 正傑 2021/06/28: 推播功能_超連結變更文字 ([Trac#8533])

* Changed 正傑 2020/11/12: 第一版需求確認後，提出規格異動
    |異動內容 | 對應文件 |
    |-------- |--------- |
    |Site管理/表單.其他參數, 增加啟動推播通知以及自訂API金鑰設                 | [表單.其他參數][link_fieldbreak1] |          
    |RTE首頁/表單.個人資料, 頁簽.推播通知紀錄增加欄位發送狀態                  | [表單.個人資料][link_fieldbreak2] | 
    |RTE首頁/表單.推播通知明細, 增加欄位發送狀態                              | [表單.推播通知明細][link_fieldbreak3] | 
    |按鍵加註_推播通知推播資訊, 取消 **發送異常** 設定                        | [按鍵加註_推播通知][link_fieldbreak4] |
    |按鍵加註_推播通知_主旨內文, 增加連結類別: 超連結網址 (做法彷嵌入物件:網頁)  | [按鍵加註_推播通知][link_fieldbreak4] |
    |按鍵加註_推播通知_通知對象, 原挑選使用者序號, 改為 使用者帳號              | [按鍵加註_推播通知][link_fieldbreak4] |
* Changed 正傑 2020/11/19: 規格確認過程中，Tracy提出規格異動。
    |異動內容 | 對應文件 |
    |-------- |--------- |
    |RTE首頁/表單.推播通知明細, 增加欄位.失敗原因                              | [表單.推播通知明細][link_fieldbreak3] | 
* Changed 正傑 2020/11/19: 第二版需求確認後，提出規格異動
    |異動內容 | 對應文件 |
    |-------- |--------- |
    |按鍵加註/推播通知/主旨內文 改名為推播內容                                  | [按鍵加註_推播通知][link_fieldbreak4] |
    |按鍵加註/推播通知/通知對象/使用者帳號 改名為帳號                                  | [按鍵加註_推播通知][link_fieldbreak4] |
    |按鍵加註/推播通知/推播資訊/另存推播紀錄/推播發送結果 改名為儲存結果欄位                                  | [按鍵加註_推播通知][link_fieldbreak4] |
    |按鍵加註/推播通知/推播資訊/連結內容/超連結Google行事曆/日期區間 改名為時段                                  | [按鍵加註_推播通知][link_fieldbreak4] |
    |按鍵加註/推播通知/推播資訊/連結內容/超連結Google行事曆/日期區間/替代類別 改名為給值來源                                  | [按鍵加註_推播通知][link_fieldbreak4] |
    |按鍵加註_推播通知的作業流程圖因項目更名連動修正                                  | [按鍵加註_推播通知][link_fieldbreak4] |
* Added ella 2020/12/15:系統工具增加以下表單:
    * 推播通知作業設定
    * 推播通知設定
* Changed 正傑 2021/06/28: #8533異動內容
    [link_fieldbreak4] |
    |按鍵加註/推播通知/推播內容/ 增加顯示名稱   


<!-- 超連結 -->
[link_fieldbreak1]: otherparameter.md "表單.其他參數"
[link_fieldbreak2]: pushmessagelog.md "表單.個人資料"
[link_fieldbreak3]: pushmessagedetail.md "表單.推播通知明細"
[link_fieldbreak4]: ./buttonannotation/README.md "按鍵加註_推播通知"

[Trac#8192]:http://trac.uneec.com/trac/neco/ticket/8192 "#8192"
[Trac#8533]:http://trac.uneec.com/trac/neco/ticket/8533 "#8533"