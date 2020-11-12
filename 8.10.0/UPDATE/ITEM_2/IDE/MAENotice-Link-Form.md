### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/08

### <div id="trac">TRAC</div>
* #8213

## <div id="linkform-layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_LinkForm_STD]
    * RWD
        * 同STD
    * MAE</br>
        * 同STD

* [版面資訊通則][link_ruleother1]

## <div id="linkform-form-action">動作說明</div>
* 依 [按鍵加註-推播通知-主旨內文][link_MAENotice_fieldbreak3]`(13)連結內容`開啟, 顯示本單內容
* 若前單推播通知來源與原設定不同時
    * 須清除引用推播通知來源欄位
    * 覆蓋原設定推播通知來源料號

## <div id="linkform-object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_LinkForm_Block1]
    * `(1)表單名稱`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單通則][link_ruledialog6], 限定挑選非離用APP表單,  回傳並顯示: 表單料號
    * `(2)表單參數`
        * 用途說明
        * 規格說明
            * 參照 [設定表單參數通則][link_parameter], 限定: 使用`(1)表單名稱`內容
    * `(3)過濾`
        * 用途說明
        * 規格說明 
            * 參照 [操作條件式通則][link_ruledialog1], 限定: 使用`(1)表單名稱`主資料區資料來源, 回傳並顯示: 條件說明
    * `(4)通行碼`
        * 用途說明
        * 規格說明
            * 單選選項: 相同 / 不相同 
            * 系統預設: 相同
    * `(5)有效次數`
        * 用途說明
        * 規格說明
            * 單選選項: 一次性 / 多次性 
            * 系統預設: 多次性 
            * 當設定為多次性時, `(6)執行系統`預設為要求登入, 並唯讀
    * `(6)執行系統`
        * 用途說明
        * 規格說明
            * 單選選項: 要求登入 / 自動登入
            * 帳號驗證: 預設為有勾選
                * 當`(5)有效次數`為一次性 且 `(6)執行系統`為要求登入，則 **帳號驗證** 預設為有勾選，並唯讀       
    * `(7)確定`
        * 用途說明
        * 規格說明
            * 瀏覽模式下, 隱藏
            * 將本次修改資料回傳前單後關閉本單
    * `(8)取消`
        * 用途說明
        * 規格說明
            * 瀏覽模式下, 隱藏
            * 不做任何修改, 直接關閉本單
  
## <div id="save-action">確定檢控</div>
* 以下檢控, 符合條件時, 顯示訊息盒, 並以紅框線標註錯誤的欄位
    * 訊息盒:【標題: 執行存回，發生下列錯誤 / 訊息內容: 以下資料未填寫正確 </n> *錯誤欄位名* / 按鍵: 確定】
        * 確定: 關閉訊息盒 
    * [基本][link_fieldbreak1]
        * `(1)表單名稱`, 不允空白


<!-- 圖片 -->
[image_LinkForm_STD]:attachment/MAENotice-Link-Form.png
[image_LinkForm_Block1]:attachment/MAENotice-Link-Form-Block1.png "基本"       


<!-- 超連結 -->
[link_MAENotice_fieldbreak3]:MAENotice.md#fieldbreak3 "按鍵加註-推播通知/欄位說明/主旨內容"
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_parameter]:/8.10.0/IDE/Specification/Parameter/README.md "共用通則_開啟單據/設定表單參數通則"
[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"

[link_ruledialog1]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog6]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog6 "共用通則_開啟單據/挑選表單通則"