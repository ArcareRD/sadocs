### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/13

### <div id="trac">TRAC</div>
* 待開 

## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_copybtnannotation]
    * RWD
        * 同STD
    * MAE</br>
        * 同STD

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

* ![pic][image_copybtnannotation_Block1]
    * `(1) 規格項目`
        * 用途說明
        * 規格說明
            * 依目的表單設計類型，部份行為的除致能、隱藏，參照下表
                * 表單設計類型=傳統表單、RWD，未勾選者除能
                * 表單設計類型=APP，未勾選者隱藏
                |    |WEB |RWD |APP |
                | -- |--- |--- |--- |
                |p.推播通知  |V |V |V |
    * `(2) 頁籤`
        * 用途說明
        * 規格說明
            * 增加顯示項目: P.推播通知
    * `(3) 功能`
        * 用途說明
        * 規格說明
            * 當`(2)頁籤`顯示項目=P.推播通知, 取得下列欄位名稱資料顯示
                * 顯示 [按鍵加註-推播通知][link_MAENotice]的推播內容、通知對象、推播通知中, 加註中有使用表單元件、表單接收參數的元件
                * 顯示 [超連結表單][link_linkform]、[超連結按鍵][link_linkbutton]、[超連結Google行事曆][link_linkgooglecalendar]、[超連結網址][link_linkurl]、[儲存連結資訊][link_savelinkinfo]、[儲存推播資訊][link_savenoticeinfo], 加註中有使用表單元件、表單接收參數的元件

<!-- 圖片 -->
[image_copybtnannotation]:attachment/CopyButtonAnnotationForm.png
[image_copybtnannotation_Block1]:attachment/CopyButtonAnnotationForm-Block1.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本區塊"

[link_MAENotice]:BAMAENotice.md "按鍵加註-推播通知"
[link_linkform]:MAENotice-Link-Form.md "連結內容_超連結表單"
[link_linkbutton]:MAENotice-Link-Button.md "連結內容_超連結按鍵"
[link_linkgooglecalendar]:MAENotice-Link-GoogleCalendar.md "連結內容_超連結Google行事曆"
[link_linkurl]:MAENotice-Link-URL.md "連結內容_超連結網址"
[link_savelinkinfo]:BAMAENotice.md#MAENotice-SaveLinkInfo.md "儲存連結資訊"
[link_savenoticeinfo]:BAMAENotice.md#MAENotice-SaveNoticeInfo.md "儲存推播資訊"
``