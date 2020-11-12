變更記錄
===
| 版本 |
| :---: |
| [8.10.0](#v8_10_0) |

***
### <a id='v8_10_0'></a>8.10.0
* Added Andy 2020/11/6: 擴充推播相關功能 ([Trac#8191])

* Changed Andy 2020/11/12: 第一版需求確認後，修改下列規格異動 
    |異動內容 | 對應文件 |
    |-------- |--------- |
    |推播通知 推播記錄, 新增 **傳送狀態** 的過濾條件 | [推播記錄][link_filter] |          
    |新增 **推播通知 按鍵連結** | [按鍵連結][link_buttonlink] | 
    |推播通知 表單連結/按鍵連結, 加入登入驗證流程 | [表單連結][link_formlink]/[按鍵連結][link_buttonlink] |
    |推播通知 按鍵連結,  加入顯示成功/失敗的訊息流程 | [按鍵連結][link_buttonlink] |
    |推播通知 系統管理,  開啟通知訊息顯示不需登入驗證 | [推播訊息][link_system] |





<!-- 超連結 --> 
[link_filter]: notification_record.md#filter "推播通知/推播記錄"
[link_buttonlink]: notification_buttonlink.md "推播通知/按鍵連結"
[link_formlink]: notification_formlink.md "推播通知/表單連結"   
[link_system]: notification_system.md#workflow "推播通知/系統管理"   

[Trac#8191]:http://trac.uneec.com/trac/neco/ticket/8191 "#8191"