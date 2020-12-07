### <div id="user">規劃人員</div>
* how

### <div id="updatedate">規劃日期</div>
* 2020/12/07

### <div id="trac">TRAC</div>
* <ps>待補</ps> 

## <div id="layout">版面相關</div>
* 版面</br>
    ![pic][image_ExternalCallButton]

## <div id="object-desc">欄位說明</div>
* `(1)按鍵名稱`
    * 用途說明
    * 規格說明
        * 擴充支援加註行為 推播通知
* `(2)傳入參數`
    * 用途說明
    * 規格說明
        * 擴充載入推播通知中有設定表單元件、接收參數、全域變數者, 範圍如下
            * [按鍵加註-推播通知][link_MAENotice]: `執行條件`、`推播內容過濾條件`、`替換字來源欄位`、`通知對象過濾條件`、`通知對象帳號`
            * [超連結表單][link_linkform]: `傳遞參數`、`過濾條件`
            * [超連結按鍵][link_linkbutton]: `成功訊息替代`、`失敗訊息替代`、`傳遞內容`
            * [超連結Google行事曆][link_linkgooglecalendar]: `標題給值內容`、`內容給值內容`、`地點給值內容`、`日期起`、`日期迄`、`時間起`、`時間迄`
            * [超連結網址][link_linkurl]: `網址給值內容`、`網址參數`
            * [儲存連結資訊][link_savelinkinfo]: `給值內容`
            * [儲存推播資訊][link_savenoticeinfo]: `給值內容`
                
<!-- 圖片 -->
[image_ExternalCallButton]:attachment/ExternalCallButton.png

<!-- 超連結 -->
[link_MAENotice]:BAMAENotice.md "按鍵加註-推播通知"
[link_linkform]:MAENotice-Link-Form.md "連結內容_超連結表單"
[link_linkbutton]:MAENotice-Link-Button.md "連結內容_超連結按鍵"
[link_linkgooglecalendar]:MAENotice-Link-GoogleCalendar.md "連結內容_超連結Google行事曆"
[link_linkurl]:MAENotice-Link-URL.md "連結內容_超連結網址"
[link_savelinkinfo]:BAMAENotice.md#MAENotice-SaveLinkInfo.md "儲存連結資訊"
[link_savenoticeinfo]:BAMAENotice.md#MAENotice-SaveNoticeInfo.md "儲存推播資訊"