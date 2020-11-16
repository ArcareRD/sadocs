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
    | 依資料排序  | *按鍵名稱*  | 取得該按鍵 [規格備註: 規格描述][link_SpecificationsRemarks] 的內容 | (推播通知)【推播人：`推播人選項`】【郵件來源：(`推播來源類別`)`推播來源檢視表名稱` (過濾)`推播來源條件說明`】【主旨內文：(`主旨`)`內文`】【通知對象：(`通知來源類別`)`通知使用者帳號元件`】 |

    * <t id="1">推播人選項</t>: 取得 [按鍵加註_推播通知][link_sender]的`推播人`中, 已勾選的選項內容
    * <t id="2">推播來源類別</t>: 取得 [按鍵加註_主旨內文][link_replacetype]的`來源`中, 已選取的選項內容
    * <t id="3">推播來源檢視表名稱</t>: 取得 [按鍵加註_主旨內文][link_conentviewno]的`檢視表`名稱
    * <t id="4">推播來源條件說明</t>: 取得 [按鍵加註_主旨內文][link_contentparameterid]的`過濾`條件說明
    * <t id="5">主旨</t>: 取得 [按鍵加註_主旨內文][link_keynote]的`主旨`內容
    * <t id="6">內文</t>: 取得 [按鍵加註_主旨內文][link_content]的`內文`內容
    * <t id="7">通知來源類別</t>: 取得 [按鍵加註_通知對象][link_noticertype]的`來源`中, 已選取的內容
    * <t id="8">通知使用者帳號元件</t>: 取得 [按鍵加註_通知對象][link_useraccount]的`使用者帳號`內容


<!-- 超連結 -->
[link_MAENotice_fieldbreak3]:BAMAENotice.md#fieldbreak3 "欄位說明/主旨內文"
[link_conentviewno]:BAMAENotice.md#conentviewno "按鍵加註-推播通知/主旨內文/檢視表"
[link_replacetype]:BAMAENotice.md#replacetype "按鍵加註-推播通知/主旨內文/來源"
[link_contentparameterid]:BAMAENotice.md#contentparameterid "按鍵加註-推播通知/主旨內文/過濾"
[link_keynote]:BAMAENotice.md#keynote "按鍵加註-推播通知/主旨內文/主旨"
[link_content]:BAMAENotice.md#content "按鍵加註-推播通知/主旨內文/內容"

[link_MAENotice_fieldbreak4]: BAMAENotice.md#fieldbreak4 "按鍵加註-推播通知/通知對象"
[link_noticertype]:BAMAENotice.md#noticertype "按鍵加註-推播通知/通知對象/來源"
[link_useraccount]:BAMAENotice.md#useraccount "按鍵加註-推播通知/通知對象/使用者帳號"
[link_sender]:BAMAENotice.md#sender "按鍵加註-推播通知/推播人"

[link_SpecificationsRemarks]:/8.10.0/IDE/Specification/SpecificationsRemarks/README.md "規格備註"