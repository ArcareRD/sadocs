### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/12/4

## <div id="behavior-layout">版面</div>
* STD
    * ![pic][image_fieldbreak1_STD]
* MAE
    * ![pic][image_fieldbreak1_MAE]

## <div id="behavior-object-desc">欄位說明</div>

* `(1)行為選項`
    * 用途說明
    * 規格說明
        * 選項:1.基本設定, 預設為true, 除能
        * 依表單設計類型, 決定是否支援行為選項, 請參照下表規則決定畫面結果:
            * 表單設計類型=STD、RWD, 不支援的行為選項, 畫面以除能方式表示
            * 表單設計類型=APP, 不支援的行選項, 畫面以隱藏方式表示
            |     |STD | RWD | APP | 離線APP |
            |---- |----|---- |---- |-------- |
            |1.基本設定    | v | v | v | v |
            |2.執行限制    | v | v | v | v |
            |A.開啟它單    | v | v | v | v |
            |B.開啟報表    | v | v |   |   |
            |C.資料交易    | v | v | v | v |
            |D.資料交換    | v | v |   |   |
            |E.郵件發送    | v | v |   |   |
            |F.資料載入    | v |   |   |   |
            |G.資料過濾    | v | v | v | v |
            |H.外部執行    | v | v | v |   |
            |J.溝通訊息    | v | v |   |   |
            |K1.表單特效   | v | v |   |   |
            |K2.動態表格   | v |   |   |   |
            |K3.帳號同步   | v | v |   |   |
            |K4.系統複製   | v | v |   |   |
            |K5.邏輯函數   | v | v |   |   |
            |K6.連結物件   | v | v | v |   |
            |K7.檔案傳輸   | v | v | v |   |
            |M.預存程序    | v | v |   |   |
            |N.裝置支援    |   |   | v | v |
            |P.推播通知    | v | v | v |   |
* `(2)儲存`
    * 用途說明
    * 規格說明
        * 當表單設計類別=APP, 且離線用為已勾選, 且`(1)行為選項`的C.資料交易為已勾選, 則 新增行為選項為[離線資料交易][link_baofflineport], 否則 新增行為選項為[資料交易][lin_baport]


<!-- 圖片 -->
[image_fieldbreak1_STD]:attachment/ButtonBehavior_STD.png
[image_fieldbreak1_MAE]:attachment/ButtonBehavior_MAE.png
[image_ButtonBehavior_Supper]:attachment/ButtonBehavior_Supper.png


<!-- 超連結 -->
[link_baofflineport]:/BAOfflinePort/README
[lin_baport]:BAPort
