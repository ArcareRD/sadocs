### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/12/1

## <div id="layout">版面相關</div>
* 版面
    * ![pic][image_Logical]

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">檢視表主頁</p>

    * ![pic][image_Logical_block1]
    * `(1)離線用`
        * 用途說明
            * MAE在離線模式下使用的檢視表須指定為離線用, 供後續檢控用
        * 規格說明
            * 系統預設: 未勾選
            * 當設定為勾選時, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 檢視表切換為離線用, 將限定參考來源的檢視表, 只能使用離線用的檢視表, 且不可使用接收參數、暫存資料表, 個資加密且未解密欄位、密碼欄位、二進位欄位, . 確定設定為離線用? / 按鍵: 確定、取消】
                * 確定: 修改本欄為已勾選, 並清空已設定的接收參數及暫存資料表後, 關閉訊息盒
                * 取消: 關閉訊息盒, 不做任何修改
    * `(2)離線資料需上傳`
        * 用途說明
            * MAE恢復連線時，若需上傳異動資料, 可使用檢視表的欄位結構產生上傳用的資料表
        * 規格說明
            * 系統預設: 未勾選, 且 除能
            * 當`(1)離線用`為勾選時, 則 致能, 否則 本欄預設不勾選 且 除能
    * `(3)接收參數`
        * 用途說明
        * 規格說明
            * 當`(1)離線用`為已勾選, 則 關閉超連結, 顯示: 不可設定
    * `(4)儲存`
        * 用途說明
        * 規格說明
            * 當`(2)離線資料需上傳`為已勾選, 查詢是否存在離線資料上傳用資料表, 決定是否新增離線資料上傳用資料表
                * 資料表名: `表格名稱` + "_OfflineUploadData"
                * 資料表英文名: `料號` + "_OT"
                * [欄位清單][link_fieldbreak2] 中, 若有符合下列條件的欄位不產生
                    * 來源參照欄位的`個資加密`為已勾選且`個資解密`為未勾選的欄位
                    * 來源參照欄位的`密碼處理`為已勾選的欄位
                    * `資料型態`為二進位的欄位
                * 因應恢復連線時，需要進行同步資料交易，由系統產生下列欄位
                    |欄位名 |欄位說明 |型態 |長度 |可變長度 |鍵值 |
                    |------ |-------- |--- |--- |------- |--- |
                    |RURU_OT_BATCHNO |離線批號 |only.全唯碼 |38 | |Y |
                    |RURU_OT_SERIALNO |離線記錄流水號 |int.整數(int) |9 | |Y |
                    |RURU_OT_STATUS |離線異動狀態(A:新增 U:修改 D:刪除) |string.文字 |1 |N |N |
            * 當`(2)離線資料需上傳`為未勾選, 且駐留資料表存在相對應的離線資料上傳用資料表, 則刪除對應的離線資料上傳用資料表
        * 作業流程
            * ![pic][image_Logical_Save]
    * `(5)刪除`
        * 用途說明
        * 規格說明
            * 當駐留資料表存在相對應的離線資料上傳用資料表, 則刪除對應的離線上傳用的資料表
        * 作業流程
            * ![pic][image_Logical_Delete]

* <p id="fieldbreak3" style="color:blue;font-weight:bold">聯結設定</p>

    * ![pic][image_Logical_block3]
    * `(1)暫存資料表`
        * 用途說明
        * 規格說明
            * 當  [檢視表主頁][link_fieldbreak1] 的`離線用`為已勾選, 本欄預設不勾選 且 除能, 否則 致能
    * `(2)表格名稱`
        * 用途說明
        * 規格說明
            * 依據`類別`
                * 資料表: [指定資料表通則][link_ruledialog3], 從本專案中, 挑選資料表, 回傳並顯示:資料表名稱
                    * 當 [檢視表主頁][link_fieldbreak1] 的`離線用`為已勾選, 增加限定: 取得`離線資料上傳用`未勾選的資料表
                * 檢視表: [指定檢視表通則][link_ruledialog4], 從本專案中, 挑選檢視表, 回傳並顯示:檢視表名稱
                    * 當 [檢視表主頁][link_fieldbreak1] 的`離線用`為已勾選, 增加限定: 取得`離線用`已勾選的檢視表


* <p id="fieldbreak2" style="color:blue;font-weight:bold">欄位清單</p>

    * ![pic][image_Logical_block2]
    * `(1)檔案唯一號`
        * 用途說明
        * 規格說明
            * 系統預設為未勾選
            * 當`資料型態`=全唯碼, 則 顯示, 否則 隱藏
            * 當來源參照欄位的`個資加密`為已勾選時, 更新本欄位為未勾選, 並除能
    * `(2)來源參照_欄位`
        * 用途說明
        * 規格說明
            * 下拉選項[結構展開]`參考來源表格`的欄位清單
                * 當 [檢視表主頁][link_fieldbreak1] 的`離線用`為已勾選, 則不輸出須`密碼處理`已勾選及`資料型態`=二進位的欄位
    * `(3)儲存`
        * 用途說明
        * 規格說明
            * 當[檢視表主頁][link_fieldbreak1]的`離線資料需上傳`為已勾選, 依本次異動的欄位結構, 修改離線資料上傳用資料表的欄位
                * 下列符合條件的欄位不產生, 若欄位已存在資料表中, 則必須刪除
                    * 來源參照欄位的`個資加密`為已勾選, 且`個資解密`為未勾選
                    * 來源參照欄位的`密碼處理`為已勾選
                    * `資料型態`為二進位
        * 作業流程
            * ![pic][image_Logical_FieldSave]
    * `(4)刪除`
        * 用途說明
        * 規格說明
            * 當[基本][link_fieldbreak1]的`離線資料需上傳`為已勾選, 且對應的離線上傳用資料表中已產生該欄位, 則 刪除
        * 作業流程
            * ![pic][image_Logical_FieldDelete]
    * `(5)可參考欄位_複製`
        * 用途說明
        * 規格說明
            * 當[檢視表主頁][link_fieldbreak1]的`離線資料需上傳`為已勾選, 依本次複製的欄位結構, 修改離線資料上傳用資料表的欄位
                * 下列符合條件的欄位不產生, 若欄位已存在資料表中, 則必須刪除
                    * 來源參照欄位的`個資加密`為已勾選, 且`個資解密`為未勾選
                    * 來源參照欄位的`密碼處理`為已勾選
                    * `資料型態`為二進位


## <div id="save-action">各頁籤儲存檢控</div>
* 參照 [存回其它檢控通則][link_ruleother8]
    * [檢視表主頁][link_fieldbreak1]
        * 當`離線用`為已勾選, 且[聯結設定][link_fieldbreak3]的`類別`=檢視表, 且來源表格為`離線用`未勾選的檢視表, 則 不允存回
            * 訊息內容: 本表已設定為離線使用的檢視表, 但聯結設定中, 別名[*別名*(ex. A、B、C、....)] 未使用離線用的檢視表
        * 當`離線用`為已勾選, 且[欄位清單][link_fieldbreak2]中, 任一欄位存在下列設定, 則 不允存回
            * 來源參照欄位的`個資加密`為已勾選, 且`個資解密`為未勾選
            * 來源參照欄位的`密碼處理`為已勾選
            * `資料型態`=二進位
            * 訊息內容: 本表已設定為離線使用的檢視表, 但欄位清單中, 欄位[*欄位名*(ex. 欄位名1、欄位名2、欄位名3、....)] 存在個資加密未解密的欄位或密碼欄位或二進位欄位
    * [欄位清單][link_fieldbreak2]
        * 當`離線用`為已勾選, 且欄位存在下列設定, 則 不允存回
            * 來源參照欄位的`個資加密`為已勾選, 且`個資解密`為未勾選
            * 來源參照欄位的`密碼處理`為已勾選
            * `資料型態`=二進位
            * 訊息內容: 本表已設定為離線使用的檢視表, 則欄位不能為個資加密未解密的欄位或密碼欄位或二進位欄位


<!-- 圖片 -->
[image_Logical]:attachment/Logical.png
[image_Logical_block1]:attachment/Logical-Block1.png
[image_Logical_block2]:attachment/Logical-Block2.png
[image_Logical_block3]:attachment/Logical-Block3.png
[image_Logical_Save]:attachment/Logical-Save.png
[image_Logical_Delete]:attachment/Logical-Delete.png
[image_Logical_FieldSave]:attachment/Logical-FieldSave.png
[image_Logical_FieldDelete]:attachment/Logical-FieldDelete.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/檢視表主頁"
[link_fieldbreak2]:#fieldbreak2 "欄位說明/欄位清單"
[link_fieldbreak3]:#fieldbreak3 "欄位說明/聯結設定"

[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
[link_ruledialog4]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog4 "共用通知_開啟單據/挑選檢視表通則"
[link_ruledialog3]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog3 "共用通知_開啟單據/挑選資料表通則"