### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/16

## <div id="layout">版面相關</div>
* 版面
    * ![pic][image_OfflinePosting]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 由專案_首頁架構樹, DB08.離線資料交易, 或由它單呼叫開啟, 開啟本單
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能
* 作業流程
    * ![pic][img_flow_Open]

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">搜尋區塊</p>

    * ![pic][image_OfflinePosting_Block1]
    * `(1)關鍵字`
        * 用途說明
        * 規格說明
            * 自行輸入
    * `(2)搜尋鍵`
        * 用途說明
        * 規格說明
            * 可依指定關鍵字, 搜索 相似於(like) 的資料交易名稱, 並顯示於`(5)清單`內
        * 作業流程
            * ![pic][img_flow_Block1Search]
    * `(3)回傳鍵`
        * 用途說明
        * 規格說明
            * 依`(5)清單`中駐留的資料交易, 回傳並顯示: 資料交易名稱給呼叫端. 並關閉表單. `(5)清單`內無記錄者, 隱藏
            * 由其它單據開啟, 且它單為編輯狀態, 則 致能, 否則 除能
        * 作業流程
            * ![pic][img_flow_Block1Return]
    * `(4)新增鍵`
        * 用途說明
        * 規格說明
            * 開啟 [新增離線資料交易][link_addofflineposting]
                * 當接收的資料交易名稱不為空時, 在右方表格內容區塊中, 新增頁籤並將其排序在第一筆後, 駐留至該頁籤
        * 作業流程
            * ![pic][img_flow_Block1Insert]
    * `(5)清單`
        * 用途說明
        * 規格說明
            * 顯示: *資料交易名稱*
            * 駐留任一筆資料交易記錄, 並執行滑鼠雙擊, 於右方表格內容區塊, 以頁籤方式開啟, 並駐留該頁籤
                * 若指定的資料交易未被開啟, 新增的頁籤, 排序須在第1個
                * 若指定的資料交易已開啟, 則直接駐留至該頁籤
            * 當清單中，任一名稱長度超過顯示區時, 系統自動出現 橫向捲軸
            * 當清單中，記錄筆數超過顯示區時, 系統自動出現 垂直捲軸
        * 作業流程
            * ![pic][img_flow_Block1List]
    * `(6)隱藏/顯示搜尋區塊`
        * 用途說明
        * 規格說明
            * 當搜尋區塊顯示時, 單擊隱藏 搜尋區塊
            * 當搜尋區塊隱藏時, 單擊顯示 搜尋區塊
        * 作業流程
            * ![pic][img_flow_Block1HideShowSearch]

* <p id="fieldbreak2" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_OfflinePosting_Block2]
    * `(1)頁籤`
        * 用途說明
        * 規格說明
            * 頁籤標題: 顯示: *資料交易名稱*, 並提供 X 鍵, 關閉單一頁籤內容
                * 當畫面只存在一個頁籤時，該頁籤隱藏 X 鍵. 請參照下圖畫面
                * ![pic][img_block2_bookmark]
    * `(2)資料交易名稱`
        * 用途說明
        * 規格說明
            * 自行輸入
    * `(3)料號`
        * 用途說明
        * 規格說明
            * 本欄唯讀
            * 顯示 系統產生的料號(料號識別碼: OD 離線資料交易: OD)
    * `(4)修改`
        * 用途說明
        * 規格說明
            * 當為瀏覽狀態, 則 致能, 否則 除能
            * 點擊時, 進入編輯狀態
    * `(5)儲存`
        * 用途說明
        * 規格說明
            * 當為編輯狀態, 則 致能, 否則 除能
            * 點擊時, 儲存駐留頁籤的資料交易規格定義內容
        * 作業流程
            * ![pic][img_flow_Block2Save]
    * `(6)刪除`
        * 用途說明
        * 規格說明
            * 執行後, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 請確認刪除 / 按鍵: 確認、取消】
                * 確認: 刪除駐留頁籤的資料交易相關記錄, 並關閉相對應的頁籤; 關閉訊息盒
                * 取消: 關閉訊息盒
        * 作業流程
            * ![pic][img_flow_Block2Delete]
    * `(7)取消`
        * 用途說明
        * 規格說明
            * 當為編輯狀態, 則 致能, 否則 除能
            * 點擊時, 回到瀏覽狀態
    * `(9)單元檢錯`
        * 用途說明
        * 規格說明
            * 開啟 [單元檢錯], 傳入: 目前駐留的資料交易名稱
        * 作業流程
            * ![pic][img_flow_Block2UnitDetection]
    * `(10)描述`
        * 用途說明
        * 規格說明
            * 開啟 [規格備註], 傳入: 目前駐留的資料交易名稱
        * 作業流程
            * ![pic][img_flow_Block2SpecNote]
    * `(11)目的表格清單`
        * 用途說明
        * 規格說明
            * 顯示該交易已設定的目的表格清單, 內容: *目的表格名稱*
            * 當清單中，任一名稱長度超過顯示區時, 系統自動出現 橫向捲軸
            * 當清單中，記錄筆數超過顯示區時, 系統自動出現 垂直捲軸

* <p id="fieldbreak3" style="color:blue;font-weight:bold">目的表格</p>

    * ![pic][image_OfflinePosting_Block3]
    * 切換頁籤說明
        * 當資料交易尚未設定目的表格, 或在 [基本][link_fieldbreak2] 的`目的表格清單`未駐留任一筆記錄時, 顯示: 初始畫面
        * 當本頁籤為新增狀態, 或在 [基本][link_fieldbreak2] 的`目的表格清單`已駐留任一筆記錄時, 顯示: 編輯畫面
    * `(1)新增`
        * 用途說明
        * 規格說明
            * 當為瀏覽狀態, 則 致能, 否則 除能
            * 點擊時, 進入本頁籤新增狀態
    * `(2)修改`
        * 用途說明
        * 規格說明
            * 當駐留 [基本][link_fieldbreak2] 的`目的表格清單`記錄時, 且為瀏覽狀態, 則 致能, 否則 除能
            * 點擊時, 進入駐留筆目的表格的編輯狀態
    * `(3)刪除`
        * 用途說明
        * 規格說明
            * 當駐留 [基本][link_fieldbreak2] 的`目的表格清單`記錄時, 且為瀏覽狀態, 則 致能, 否則 除能
            * 點擊時, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 請確認刪除 / 按鍵: 確認、取消】
                * 確認: 刪除駐留筆目的表格 ; 關閉訊息盒
                * 取消: 關閉訊息盒
        * 作業流程
            * ![pic][img_flow_Block3Delete]
    * `(4)儲存`
        * 用途說明
        * 規格說明
            * 當為編輯狀態時, 則 致能, 否則 致能
            * 點擊時, 儲存駐留筆目的表格規格定義內容
        * 作業流程
            * ![pic][img_flow_Block3Save]
    * `(5)取消`
        * 用途說明
        * 規格說明
            * 當為編輯狀態時, 則 致能, 否則 致能
            * 點擊時, 畫面回到瀏覽狀態
    * `(7)目的表格`
        * 用途說明
        * 規格說明
            * 參照 [挑選檢視表通則][link_ruledialog4], 限定: 離線用為已勾選 ; 回傳並顯示: 檢視表名稱
    * `(8)異動方式`
        * 用途說明
            * 意指 本次設定的目的表格，其資料的異動方式
            * 各選項說明如下:
                * 無條件新增: 新增記錄
                * 條件成立者修改: 依`(9)判斷條件`至`(7)目的表格`尋找符合的記錄，若有符合記錄，則修改欄位值。
                * 條件成立者修改，不成立者新增 : 依`(9)判斷條件`至`(7)目的表格`尋找符合的記錄，若有符合記錄，則修改欄位值。若沒有符合記錄，則新增記錄。
                * 條件成立者保留，不成立者新增 : 依`(9)判斷條件`至`(7)目的表格`尋找符合的記錄，若沒有符合記錄，則新增記錄。
                * 條件成立者刪除 : 依`(9)判斷條件`至`(7)目的表格`尋找符合的記錄，若有符合記錄，則刪除記錄。
        * 規格說明
            * 下拉選項: 無條件新增 / 條件成立者修改 / 條件成立者修改，不成立者新增 / 條件成立者保留，不成立者新增 / 條件成立者刪除
            * 系統預設: 無條件新增
            * 當為無條件新增時, `(9)判斷條件`表格除能, 並清空表格中已設定的內容
    * `(9)判斷條件`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
    * `(10)比對欄位`
        * 用途說明
        * 規格說明
            * 參照 [挑選檢視表元件通則][link_ruledialog8], 限定: 來源參照欄位為個資加密且已在檢視表解密, 或來源參照欄位的密碼處理為未勾選 ; 回傳並顯示: 欄位名稱
    * `(11)類別`
        * 用途說明
        * 規格說明
            * 下拉選項: 參數 / 系統資訊 / 固定值 / 運算式
            * 系統預設: 參數
            * 當異動內容時, 清空欄位: `(12)來源欄位`
    * `(12)來源欄位`
        * 用途說明
        * 規格說明
            * 當`(11)類別`=參數, 參照 [挑選參數通則][link_ruledialog9], 從駐留的資料交易中挑選參數, 回傳並顯示: 參數名稱
            * 當`(11)類別`=系統資訊, 下拉選項: 1.系統日期 / 2.系統日期時間 / 3.唯一序號碼 / 4.使用者序號 / 5.使用者帳號 / 6.使用者姓名 / 7.簽入組織序號
            * 當`(11)類別`=固定值, 自行輸入
            * 當`(11)類別`=運算式, 開啟 [運算式][link_expression], 限定使用頁籤: 參數、函數、全域變數, 且編輯方式限定只能為引用函數, 回傳並顯示: 運算式說明

* <p id="fieldbreak4" style="color:blue;font-weight:bold">目的欄位</p>

    * ![pic][image_OfflinePosting_Block4]
    * 切換頁籤說明
        * 當在[基本][link_fieldbreak2]的`目的表格清單`未駐留任一筆記錄時, 本頁籤不可點選
        * 本頁籤被選取時，預設不駐留`(7)影響欄位清單`任一筆記錄
    * `(1)修改`
        * 用途說明
        * 規格說明
            * 當駐留`(7)影響欄位清單`記錄時, 且為瀏覽模式, 則 致能, 否則 除能
            * 點擊時, 進入駐留筆目的表格的編輯狀態
    * `(2)儲存`
        * 用途說明
        * 規格說明
            * 當為編輯狀態時, 則 致能, 否則 致能
            * 點擊時, 儲存駐留筆目的表格欄位規格定義內容
        * 作業流程
            * ![pic][img_flow_Block4Save]
    * `(3)取消`
        * 用途說明
        * 規格說明
            * 當為編輯狀態時, 則 致能, 否則 致能
            * 點擊時, 畫面回到瀏覽狀態
    * `(4)新增`
        * 用途說明
        * 規格說明
            * 當為瀏覽狀態, 則 致能, 否則 除能
            * 點擊時, 清空畫面上所有欄位, 並進入本頁籤編輯狀態
        * 作業流程
            * ![pic][img_flow_Block4Insert]
    * `(5)刪除`
        * 用途說明
        * 規格說明
            * 當駐留`(7)影響欄位清單`記錄時, 則 致能, 否則 除能
            * 點擊時, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 請確認刪除 / 按鍵: 確認、取消】
                * 確認: 刪除駐留筆目的欄位 ; 關閉訊息盒
                * 取消: 關閉訊息盒
        * 作業流程
            * ![pic][img_flow_Block4Delete]
    * `(6)自動載入`
        * 用途說明
        * 規格說明
            * 依下列欄位載入條件, 取得目前駐留的目的表格, 將其對應的欄位清單載入至`(7)影響欄位清單`
                * 當目的表格欄位名稱已存在`(7)影響欄位清單`, 不處理
                * 當目的表格欄位名稱不存在`(7)影響欄位清單`, 將欄位載入至清單中, `(8)影響欄位`=目的欄位名稱, 並依下列原則給值
                    * 當目的表格欄位名稱存在[接收參數][link_fieldbreak5]的`參數名`, 則`(12)接收參數`設為已勾選, 給值內容: [接收參數][link_fieldbreak5]的`參數名`
                    * 當不符合上述內容者, 則`(10)固定給值`設為已勾選
        * 作業流程
            * ![pic][img_flow_Block4AutoFieldLoad]
    * `(7)影響欄位清單`
        * 用途說明
        * 規格說明
            * 顯示`(8)影響欄位`已設定的欄位名稱
            * 記錄移動時, 若已進入修改或模式, 則欄位不異動, 直接跳離
    * `(8)影響欄位`
        * 用途說明
        * 規格說明
            * 下拉選項來源: 依駐留的目的表格的欄位清單中挑選欄位, 顯示: 欄位名稱
    * `(9)給值條件`
        * 用途說明
        * 規格說明
            * 開啟 [運算式][link_expression], 限定使用頁籤: 參數、函數、全域變數, 且編輯方式限定只能為引用函數, 回傳並顯示: 運算式說明
    * `(11)固定給值`
        * 用途說明
        * 規格說明
            * 系統預設為未勾選
            * 當為已勾選時, 對應內容致能, 否則 除能
                * 自行輸入
    * `(12)系統資訊`
        * 用途說明
        * 規格說明
            * 系統預設為未勾選
            * 當為已勾選時, 對應內容致能, 否則 除能
                * 下拉選項: 1.系統日期 / 2.系統日期時間 / 3.唯一序號碼 / 4.使用者序號 / 5.使用者帳號 / 6.使用者姓名 / 7.簽入組織序號
    * `(13)接收參數`
        * 用途說明
        * 規格說明
            * 系統預設為未勾選
            * 當為已勾選時, 對應內容致能, 否則 除能
               * 參照 [挑選參數通則][link_ruledialog9], 從駐留的資料交易中挑選參數, 回傳並顯示: 參數名稱
    * `(14)運算給值`
        * 用途說明
        * 規格說明
            * 系統預設為未勾選
            * 當為已勾選時，對應內容致能, 否則 除能
                * 開啟 [運算式][link_expression], 限定使用頁籤: 參數、函數、全域變數, 且編輯方式限定只能為引用函數, 回傳並顯示: 運算式說明
    * `(15)重新編碼`
        * 用途說明
            * 若恢復連線後, 須進行同步, 且該欄位為依據單據編碼原則取值, 可設定此選項由系統暫時產生一組不重覆的編號
        * 規格說明
            * 由 ruRU MAE 在背景自動產生一組編號
            * 取號原則: 固定前3碼為 * 字, 後4碼為流水號, 案例如下:
                <div>
                    ***9999 (ex.***0001, ***0002, ***0003, ...)
                <div>
    * `(16)取得序號`
        * 用途說明
            * 若恢復連線後, 須進行同步, 且該欄位為依據流水序號取值, 可設定此選項由系統暫時產生一組流水序號
        * 規格說明
            * 由 ruRU MAE 在背景自動產生流水序號
            * 取號原則: 從-1開始, 案例如下:
                <div>
                    (ex.-1, -2, -3, ...)
                </div>
                
* <p id="fieldbreak5" style="color:blue;font-weight:bold">接收參數</p>

    * ![pic][image_OfflinePosting_Block5]
    * `(1)修改`
        * 用途說明
        * 規格說明
            * 當為瀏覽模式, 則 致能, 否則 除能
            * 點擊時, 進入編輯狀態
    * `(2)儲存`
        * 用途說明
        * 規格說明
            * 當為編輯狀態時, 則 致能, 否則 致能
            * 點擊時, 儲存駐留筆接收參數規格定義內容
        * 作業流程
            * ![pic][img_flow_Block5Save]
    * `(3)取消`
        * 用途說明
        * 規格說明
            * 當為編輯狀態時, 則 致能, 否則 致能
            * 點擊時, 畫面回到瀏覽狀態
    * `(4)接收參數表格`
        * 用途說明
        * 規格說明
            * 參照 [操作表格記錄通則][link_rulebutton3]
    * `(5)料號`
        * 用途說明
        * 規格說明
            * 顯示 系統產生的料號(料號識別碼: 9 參數: RV)
    * `(6)參數名`
        * 用途說明
        * 規格說明
            * 自行輸入
    * `(7)型態`
        * 用途說明
        * 規格說明
            * 下拉選項: 文字 / 數字 / 日期 / 邏輯
            * 系統預設: 文字
    * `(8)說明`
        * 用途說明
        * 規格說明
            * 自行輸入



## <div id="save-action">各頁籤儲存檢控</div>
* 參照 [存回不允空白檢控通則][link_ruleother7]
    * [基本][link_fieldbreak2]
        * `資料交易名稱`, 不允空白
    * [目的表格][link_fieldbreak3]
        * `目的表格`、`異動方式`, 不允空白
        * 當`判斷條件`存在記錄時, `比對欄位`、`來源欄位`, 不允空白
    * [目的欄位][link_fieldbreak4]
        * `影響欄位`, 不允空白
        * 給值方式區塊中, 被勾選的選項為`固定給值`、`系統資訊`、`接收參數`、`運算給值`時, 其對應內容, 不允空白
    * [接收參數][link_fieldbreak5]
        * `參數名`, 不允空白

* 參照 [存回其它檢控通則][link_ruleother8]
    * [基本][link_fieldbreak2]
        * 同一專案下, `資料交易名稱`不可重覆
            * 訊息內容: 資料交易名稱不可重覆
    * [目的表格][link_fieldbreak3]
        * 當`異動方式`<>無條件新增時, 判斷條件至少須存在一筆記錄
            * 訊息內容: 當異動方式<>無條件新增時, 判斷條件至少須存在一筆記錄
    * [目的欄位][link_fieldbreak4]
        * 當`影響欄位`已存在`影響欄位清單`中, `給值條件`必須有值
            訊息內容: 影響欄位已存在影響欄位清單時, 給值條件必須有值
    * [接收參數][link_fieldbreak5]
        * 同一資料交易下, `參數名`不可重覆
            * 訊息內容: 接收參數名稱不可重覆


<!-- 圖片 -->
[image_OfflinePosting]:attachment/OfflinePosting.png
[image_OfflinePosting_Block1]:attachment/OfflinePosting-Block1.png
[image_OfflinePosting_Block2]:attachment/OfflinePosting-Block2.png
[image_OfflinePosting_Block3]:attachment/OfflinePosting-Block3.png
[image_OfflinePosting_Block4]:attachment/OfflinePosting-Block4.png
[image_OfflinePosting_Block5]:attachment/OfflinePosting-Block5.png

[img_flow_Open]: attachment/OfflinePosting-Open.png
[img_flow_Block1HideShowSearch]: attachment/OfflinePosting-Block1-HideShowSearch.png
[img_flow_Block1Insert]: attachment/OfflinePosting-Block1-Insert.png
[img_flow_Block1List]: attachment/OfflinePosting-Block1-List.png
[img_flow_Block1Return]: attachment/OfflinePosting-Block1-Return.png
[img_flow_Block1Search]: attachment/OfflinePosting-Block1-Search.png
[img_flow_Block2Delete]: attachment/OfflinePosting-Block2-Delete.png
[img_flow_Block2Save]: attachment/OfflinePosting-Block2-Save.png
[img_flow_Block2UnitDetection]: attachment/OfflinePosting-Block2-UnitDetection.png
[img_flow_Block2SpecNote]: attachment/OfflinePosting-Block2-SpecNote.png
[img_block2_bookmark]:attachment/OfflinePosting-Block2_bookmark.png
[img_flow_Block3Save]:attachment/OfflinePosting-Block3-Save.png
[img_flow_Block3Delete]:attachment/OfflinePosting-Block3-Delete.png
[img_flow_Block4Save]:attachment/OfflinePosting-Block4-Save.png
[img_flow_Block4Delete]:attachment/OfflinePosting-Block4-Delete.png
[img_flow_Block4Insert]:attachment/OfflinePosting-Block4-Insert.png
[img_flow_Block4AutoFieldLoad]:attachment/OfflinePosting-Block4-AutoFieldLoad.png
[img_flow_Block5Save]:attachment/OfflinePosting-Block5-Save.png


<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/搜尋區塊"
[link_fieldbreak2]:#fieldbreak2 "欄位說明/基本"
[link_fieldbreak3]:#fieldbreak3 "欄位說明/目的表格"
[link_fieldbreak4]:#fieldbreak4 "欄位說明/目的欄位"
[link_fieldbreak5]:#fieldbreak5 "欄位說明/接收參數"

[link_addofflineposting]:addOfflinePosting.md

[link_expression]:/8.10.0/IDE/Specification/Expression/README.md "運算式"
[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother7]:/8.10.0/IDE/Specification/RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:/8.10.0/IDE/Specification/RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"

[link_rulebutton2]:/8.10.0/IDE/Specification/RulesButton/README#rulebutton2 "共用通則_按鍵/單據異動資料按鍵操作通則"

[link_ruledialog2]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog2 "共用通則_開單/挑選資料表通則"
[link_ruledialog5]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog5 "共用通則_開單/挑選資料表元件通則"
[link_ruledialog4]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog4 "共用通則_開單/挑選檢視表通則"
[link_ruledialog8]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog8 "共用通則_開單/挑選檢視表元件通則"
[link_ruledialog9]:/8.10.0/IDE/Specification/RulesDialog/README#ruledialog9 "共用通則_開單/挑選參數通則"

[link_rulebutton3]:/8.10.0/IDE/Specification/RulesButton/README#rulebutton3 "共用通則_按鍵/操作表格記錄通則"