### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/11/16

### <div id="trac">TRAC</div>
* 待開 

## <div id="layout">版面相關</div>
* 版面
    * ![pic][image_OfflinePosting]

* [版面資訊通則][link_ruleother1]

## <div id="form-action">動作說明</div>
* 由專案_首頁架構樹, DB08.離線資料交易, 開啟本單

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
    * `(3)回傳鍵`
        * 用途說明
        * 規格說明
            * 依駐留的資料交易加註記錄, 回傳並顯示: 資料交易名稱給呼叫端. 並關閉表單. `(5)清單`內無記錄者, 隱藏
            * 由其它單據開啟, 且它單為編修模式, 則 致能, 否則 除能
    * `(4)新增鍵`
        * 用途說明
        * 規格說明
            * 開啟 [新增離線資料交易]
    * `(5)清單`
        * 用途說明
        * 規格說明
            * 顯示: 資料交易名稱
            * 當清單中，任一名稱長度超過顯示區時, 系統自動出現 橫向捲軸
            * 當清單中，記錄筆數超過顯示區時, 系統自動出現 垂直捲軸
    * `(6)隱藏/顯示搜尋區塊`
        * 用途說明
        * 規格說明
            * 當搜尋區塊顯示時, 單擊隱藏 搜尋區塊
            * 當搜尋區塊隱藏時, 單擊顯示 搜尋區塊

* <p id="fieldbreak2" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_OfflinePosting_Block2]
    * `(1)頁籤`
        * 用途說明
        * 規格說明
            * 依指定的資料交易, 開啟頁籤內容
                * 若指定的資料交易已開啟, 則駐留至該頁籤
            * 頁籤標題: 顯示: 資料交易名稱, 並提供 X 鍵, 關閉單一頁籤內容
                * 當畫面只存在一個頁籤時，該頁籤隱藏 X 鍵
    * `(2)資料交易名稱`
        * 用途說明
        * 規格說明
            * 自行輸入
    * `(3)料號`
        * 用途說明
        * 規格說明
            * 顯示 系統產生的料號(料號識別碼: OD 離線資料交易: OD)
    * `(4)修改`
        * 用途說明
        * 規格說明
            * 駐留頁籤, 進入修改模式
            * 欄位: (2)資料交易名稱 致能, 否則 除能
    * `(5)儲存`
        * 用途說明
        * 規格說明
            * 修改模式, 致能, 點擊後, 儲存駐留頁籤的資料交易規格定義內容
    * `(6)刪除`
        * 用途說明
        * 規格說明
    * `(7)取消`
        * 用途說明
        * 規格說明
    * `(8)複製`
        * 用途說明
        * 規格說明
    * `(9)單元檢錯`
        * 用途說明
        * 規格說明
    * `(10)描述`
        * 用途說明
        * 規格說明


<!-- 圖片 -->
[image_OfflinePosting]:attachment/OfflinePosting.png
[image_OfflinePosting_Block1]:attachment/OfflinePosting-Block1.png
[image_OfflinePosting_Block2]:attachment/OfflinePosting-Block2.png

<!-- 超連結 -->
[link_fieldbreak1]:#fieldbreak1 "欄位說明/搜尋區塊"
[link_fieldbreak2]:#fieldbreak2 "欄位說明/基本"

[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"