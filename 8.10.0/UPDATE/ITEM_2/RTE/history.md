變更記錄
===
| 版本 |
| :---: |
| [8.10.0](#v8_10_0) |

***
### <a id='v8_10_0'></a>8.10.0
* Added 正傑 2020/11/4: RTE_因應MAE擴充推播通知功能相關修改 ([Trac#8192])

* Changed 正傑 2020/11/12: 第一版需求確認後，提出規格異動
    |異動內容 | 對應文件 |
    |-------- |--------- |
    |Site管理/表單.其他參數, 增加啟動推播通知以及自訂API金鑰設                 | [表單.其他參數][link_fieldbreak1] |          
    |RTE首頁/表單.個人資料, 頁簽.推播通知紀錄增加欄位發送狀態                  | [表單.個人資料][link_fieldbreak2] | 
    |RTE首頁/表單.推播通知明細, 增加欄位發送狀態                              | [表單.推播通知明細][link_fieldbreak3] | 
    |按鍵加註_推播通知推播資訊, 取消 **發送異常** 設定                        | [按鍵加註_推播通知][link_fieldbreak4] |
    |按鍵加註_推播通知_主旨內文, 增加連結類別: 超連結網址 (做法彷嵌入物件:網頁)  | [按鍵加註_推播通知][link_fieldbreak4] |
    |按鍵加註_推播通知_通知對象, 原挑選使用者序號, 改為 使用者帳號              | [按鍵加註_推播通知][link_fieldbreak4] |

<!-- 超連結 -->
[link_fieldbreak1]: otherparameter.md "表單.其他參數"
[link_fieldbreak2]: pushmessagelog.md "表單.個人資料"
[link_fieldbreak3]: pushmessagedetail.md "表單.推播通知明細"
[link_fieldbreak4]: ./buttonannotation/README.md "按鍵加註_推播通知"

[Trac#8192]:http://trac.uneec.com/trac/neco/ticket/8192 "#8192"
