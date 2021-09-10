# 元件類型-下拉選項

* ## Web支援版本
  
      8.10.0

* ## APP 支援版本

      008.010.000049 以上(含)

* __下拉選項__
  * __<div id="code">元件代碼</div>__

    * wDL
  * __<div id="dependency">相依性</div>__

    * 獨立元件
  * __<div id="layout">版面相關</div>__

    * 元件寬高
      * 高度(px)
        * 下拉選項＝單選
          * 當變動高度＝是
            * 表示最小高度。
            * 不含`外邊距`的上邊距/下邊距：(單元樣式/外邊距/(上邊距/下邊距))
            * 元件會因`標題區`或`內容區`撐高
            * [內容超出折行](../general/rule)
          * 當變動高度＝否
            * 內容永遠為一行
            * 內容超出顯示...
            * [元件高度不足](../general/rule)
        * 下拉選項＝多選
          * 一定是變動高度
          * 高度表示最小高度
          * 元件會因`標題區`或`內容區`撐高
      * 寬度(%)
        不含`外邊距`的左邊距/右邊距：(單元樣式/外邊距/(左邊距/右邊距))
        * 下拉選項＝多選
          * [單個選項超過時會顯示省略，多個選項超過時會折行](#photo_over_width)
      * 當裝置的大小不同時，可能導致元件寬高會改變
    * [樣式](../general/style)
      * [<div id="apps_enable">致能(Apps_Enable)</div>](#photo_enabled)

        * 下拉選項=單選
          * 背景
            * 顏色
            * 透明度
            * 漸層色
            * 漸層方向
          * 內容
            * 文字顏色
            * 透明度
            * ~`字型`~
            * 大小
            * 水平
            * 垂直
            * 字型樣式
              * 粗體
              * 斜體
              * 底線
              * 刪除線
            * ~`超連結`~
              * ~`點擊前`~
              * ~`點擊後`~
          * 框線
            * 線條
              * 無
              * 實線
              * 虛線
              * 嵌入線
              * 浮出線
            * 圓角
            * `當圓角<寬度且線條=虛線時，會強制設定圓角=寬度`
            * 左框線
              * 寬度
              * 顏色
            * 上框線
              * 寬度
              * 顏色
            * 右框線
              * 寬度
              * 顏色
            * 下框線
              * 寬度
              * 顏色
          * 邊界
            * 內間距
              * 左
              * 上
              * 右
              * 下
            * 外邊距
              * 左
              * 上
              * 右
              * 下
        * 下拉選項=多選
          * 背景
            * 顏色
            * 透明度
            * 漸層色
            * 漸層方向
          * 內容
            * 文字顏色
            * 透明度
            * ~`字型`~
            * 大小
            * 水平
            * 垂直
            * 字型樣式
              * 粗體
              * 斜體
              * 底線
              * 刪除線
            * ~`超連結`~
              * ~`點擊前`~
              * ~`點擊後`~
          * 框線
            * 線條
              * 無
              * 實線
              * 虛線
              * 嵌入線
              * 浮出線
            * 圓角
            * 左框線
              * 寬度
              * 顏色
            * 上框線
              * 寬度
              * 顏色
            * 右框線
              * 寬度
              * 顏色
            * 下框線
              * 寬度
              * 顏色
          * 邊界
            * 內間距
              * 左
              * 上
              * 右
              * 下
            * 外邊距
              * 左
              * 上
              * 右
              * 下
      * [<div id="apps_enable_multi">多選致能(Apps_Enable_Multi)</div>](#photo_multi_enabled)

        * 下拉選項=多選，選取後的子元件樣式
        * 背景
          * 顏色
          * 透明度
          * 漸層色
          * 漸層方向
        * 內容
          * 文字顏色
          * 透明度
          * 字型
          * 大小
          * ~`水平`~
          * ~`垂直`~
          * 字型樣式
            * 粗體
            * 斜體
            * 底線
            * 刪除線
          * ~`超連結`~
            * ~`點擊前`~
            * ~`點擊後`~
        * 框線
          * 線條
            * 無
            * 實線
            * 虛線
            * 嵌入線
            * 浮出線
          * 圓角
            * `當圓角<寬度且線條=虛線時，會強制設定圓角=寬度`
          
            <!--
            * 當有圓角設定時
              * 邊框的線條樣式只支援`無`及`實線``(虛線/嵌入/浮出皆會設定為實線)`，且依左上右下順序，只有一邊的設定有效`(會套用至四邊)`
            * 當無圓角設定時
              * 支援四邊框線樣式的設定
            -->
          * 左框線
            * 寬度
            * 顏色
          * 上框線
            * 寬度
            * 顏色
          * 右框線
            * 寬度
            * 顏色
          * 下框線
            * 寬度
            * 顏色
        * 邊界
          * 內間距
            * 左
            * 上
            * 右
            * 下
          * 外邊距
            * 左
            * 上
            * 右
            * 下
      * [<div id="apps_display_enable">顯示致能(Apps_DisplayEnable)</div>](#photo_readonly)

        * 下拉選項=單選
          * 背景
            * 顏色
            * 透明度
            * 漸層色
            * 漸層方向
          * 內容
            * 文字顏色
            * 透明度
            * ~`字型`~
            * 大小
            * 水平
            * 垂直
            * 字型樣式
              * 粗體
              * 斜體
              * 底線
              * 刪除線
            * ~`超連結`~
              * ~`點擊前`~
              * ~`點擊後`~
          * 框線
            * 線條
              * 無
              * 實線
              * 虛線
              * 嵌入線
              * 浮出線
            * 圓角
              * `當圓角<寬度且線條=虛線時，會強制設定圓角=寬度`
            * 左框線
              * 寬度
              * 顏色
            * 上框線
              * 寬度
              * 顏色
            * 右框線
              * 寬度
              * 顏色
            * 下框線
              * 寬度
              * 顏色
          * 邊界
            * 內間距
              * 左
              * 上
              * 右
              * 下
            * 外邊距
              * 左
              * 上
              * 右
              * 下
        * 下拉選項=多選
          * 背景
            * 顏色
            * 透明度
            * 漸層色
            * 漸層方向
          * ~`內容`~
          * 框線
            * 線條
              * 無
              * 實線
              * 虛線
              * 嵌入線
              * 浮出線
            * 圓角
              * `當圓角<寬度且線條=虛線時，會強制設定圓角=寬度`
            * 左框線
              * 寬度
              * 顏色
            * 上框線
              * 寬度
              * 顏色
            * 右框線
              * 寬度
              * 顏色
            * 下框線
              * 寬度
              * 顏色
          * 邊界
            * 內間距
              * 左
              * 上
              * 右
              * 下
            * 外邊距
              * 左
              * 上
              * 右
              * 下
      * [<div id="apps_display_enable_multi">多選顯示致能(Apps_DisplayEnable_Multi)</div>](#photo_multi_readonly)

        * 下拉選項=多選，選取後的子元件樣式
        * 背景
          * 顏色
          * 透明度
          * 漸層色
          * 漸層方向
        * 內容
          * 文字顏色
          * 透明度
          * 字型
          * 大小
          * ~`水平`~
          * ~`垂直`~
          * 字型樣式
            * 粗體
            * 斜體
            * 底線
            * 刪除線
          * ~`超連結`~
            * ~`點擊前`~
            * ~`點擊後`~
        * 框線
          * 線條
            * 無
            * 實線
            * 虛線
            * 嵌入線
            * 浮出線
          * 圓角
            * `當圓角<寬度且線條=虛線時，會強制設定圓角=寬度`
            
            <!--
            * 當有圓角設定時
              * 邊框的線條樣式只支援`無`及`實線``(虛線/嵌入/浮出皆會設定為實線)`，且依左上右下順序，只有一邊的設定有效`(會套用至四邊)`
            * 當無圓角設定時
              * 支援四邊框線樣式的設定
            -->
          * 左框線
            * 寬度
            * 顏色
          * 上框線
            * 寬度
            * 顏色
          * 右框線
            * 寬度
            * 顏色
          * 下框線
            * 寬度
            * 顏色
        * 邊界
          * 內間距
            * 左
            * 上
            * 右
            * 下
          * 外邊距
            * 左
            * 上
            * 右
            * 下
      * [<div id="apps_title">標題(Apps_Title)</div>](#photo_title)

        * 下拉選項=單選/多選
          * 背景
            * 顏色
            * 透明度
            * 漸層色
            * 漸層方向
          * 內容
            * 文字顏色
            * 透明度
            * ~`字型`~
            * 大小
            * 水平
            * 垂直
            * 字型樣式
              * 粗體
              * 斜體
              * 底線
              * 刪除線
            * ~`超連結`~
              * ~`點擊前`~
              * ~`點擊後`~
          * 框線
            * 線條
              * 無
              * 實線
              * 虛線
              * 嵌入線
              * 浮出線
            * 圓角
              * `當圓角<寬度且線條=虛線時，會強制設定圓角=寬度`
            * 左框線
              * 寬度
              * 顏色
            * 上框線
              * 寬度
              * 顏色
            * 右框線
              * 寬度
              * 顏色
            * 下框線
              * 寬度
              * 顏色
          * 邊界
            * 內間距
              * 左
              * 上
              * 右
              * 下
            * 外邊距
              * 左
              * 上
              * 右
              * 下
      * [<div id="apps_item_list">選項清單(Apps_Item_List)</div>](#photo_dropdown_list)

        * 下拉選項=單選
          * 背景
            * 顏色
            * 透明度
            * 漸層色
            * 漸層方向
          * 內容
            * 文字顏色
            * 透明度
            * ~`字型`~
            * 大小
            * 水平
            * 垂直
            * 字型樣式
              * 粗體
              * 斜體
              * 底線
              * 刪除線
            * ~`超連結`~
              * ~`點擊前`~
              * ~`點擊後`~
          * 框線
            * 線條
              * 無
              * 實線
              * 虛線
              * 嵌入線
              * 浮出線
            * 圓角
              * `當圓角<寬度且線條=虛線時，會強制設定圓角=寬度`
            * 左框線
              * 寬度
              * 顏色
            * 上框線
              * 寬度
              * 顏色
            * 右框線
              * 寬度
              * 顏色
            * 下框線
              * 寬度
              * 顏色
          * 邊界
            * ~`內間距`~
            * ~`外邊距`~
          * 光棒(lightBar)
            * 樣式設定的順序為 該狀態樣式內的光棒設定->Apps_Item_List的樣式設定->預設光棒設定
              * 輪盤式的選取因為有放大1.2倍的效果，左右邊框在某種程度上是看不到效果
            * 線條
              * 無
              * 實線
              * 虛線
              * 嵌入線
              * 浮出線
            * 上框線
              * 寬度
              * 顏色
            * 下框線
              * 寬度
              * 顏色
            * 左框線
              * 寬度
              * 顏色
            * 右框線
              * 寬度
              * 顏色
            * 顏色
            * 透明度
            * 漸層色
            * 漸層方向
          * `確定`及`消取`的樣式不可設定
        * 下拉選項=多選
          * 背景
            * 顏色
            * 透明度
            * 漸層色
            * 漸層方向
          * 內容
            * 文字顏色
            * 透明度
            * ~`字型`~
            * 大小
            * ~`水平`~
            * ~`垂直`~
            * 字型樣式
              * 粗體
              * 斜體
              * 底線
              * 刪除線
            * ~`超連結`~
              * ~`點擊前`~
              * ~`點擊後`~
          * 框線
            * 線條
              * 無
              * 實線
              * 虛線
              * 嵌入線
              * 浮出線
            * 圓角
              * `當圓角<寬度且線條=虛線時，會強制設定圓角=寬度`
              
              <!--
              * 當有圓角設定時
                * 邊框的線條樣式只支援`無`及`實線``(虛線/嵌入/浮出皆會設定為實線)`，且依左上右下順序，只有一邊的設定有效`(會套用至四邊)`
              * 當無圓角設定時
                * 支援四邊樣式的設定
              -->
            * 左框線
              * 寬度
              * 顏色
            * 上框線
              * 寬度
              * 顏色
            * 右框線
              * 寬度
              * 顏色
            * 下框線
              * 寬度
              * 顏色
          * ~`邊界`~
            * ~`內間距`~
            * ~`外邊距`~
          * `確定`/`消取`/`核取方塊`及`查找`的樣式不可設定
      * <div id="default_style">預設樣式</div>

        * 標題樣式(標題(Apps_Title))
          * 字型
            * 顏色=`[0xFF000000]` [<span style="color: #000000;">▇</span>]
            * 大小＝16
        * 下拉選項=單選
          * 元件樣式(致能(Apps_Enable)/顯示致能(Apps_DisplayEnable))
            * 字型
              * 顏色=`[0xFF000000]` [<span style="color: #000000;">▇</span>]
              * 大小＝16
              * 位置＝靠左置中
            * 背景
              * 顏色＝`[0xFFFFFFFF]` [<span style="color: #FFFFFF;">▇</span>]
            * 邊框
              * 顏色=`[0xFFE0E0E0]` [<span style="color: #E0E0E0;">▇</span>]
              * 線條＝實線
              * 圓角=3
              * 寬度＝1
            * 內邊距
              * 上=下＝2
              * 左＝右＝5
          * 選項清單樣式(選項清單(Apps_Item_List))
            <!--
            * 確定
              * 字型
                * 顏色=`[0xFF2196F3]` [<span style="color: #2196F3;">▇</span>]
                * 大小=18
            * 取消
              * 字型
                * 顏色=`[0xFFF44336]` [<span style="color: #F44336;">▇</span>]
                * 大小=18
            -->
            * 背景
              * 顏色=`[0xFFFFFFFF]` [<span style="color: #FFFFFF;">▇</span>]
            * 邊框
              * 顏色=無
              * 線條＝無
              * 圓角=10
              * 寬度＝0
            * 選項文字
              * 字型
                * 顏色=`[0xFF000000]` [<span style="color: #000000;">▇</span>]
                * 大小=18
                * 位置
                  * 水平=置中
                  * 垂直=置中
            * 光棒
              * 無
        * 下拉選項=多選
          * 元件樣式(致能(Apps_Enable)/顯示致能(Apps_DisplayEnable))
            * 字型
              * 顏色=`[0xFF000000]` [<span style="color: #000000;">▇</span>]
              * 大小＝16
              * 位置
                * 水平=靠左
                * 垂直=置中
              * 字體=粗體
            * 背景
              * 顏色＝`[0xFFFFFFFF]` [<span style="color: #FFFFFF;">▇</span>]
            * 邊框
              * 顏色=`[0xFFE0E0E0]` [<span style="color: #E0E0E0;">▇</span>]
              * 線條＝無
              * 圓角=3
              * 寬度＝1
            * 內邊距
              * 上=2
              * 下＝2
              * 左＝5
              * 右＝5
          * 已選取項目樣式(多選致能(Apps_Enable_Multi)/多選顯示致能(Apps_DisplayEnable_Multi))
            * 背景
              * 顏色=`[0xFF90CAF9]` [<span style="color: #90CAF9;">▇</span>]
            * 字型
              * 顏色=`[0xFF42A5F5]` [<span style="color: #42A5F5;">▇</span>]
              * 大小=18
            * 邊框
              * 顏色=透明
              * 線條＝無
              * 圓角=30
              * 寬度＝2
            * 內間距
              * 上=下=5
              * 左=右=10
            * 外邊距
              * 上=下=2
              * 左=右=3
            
            <!--
            * 取消
              * 顏色=`[0xFF1E88E5]` [<span style="color: #1E88E5;">▇</span>]
            -->
          * 選項清單樣式(選項清單(Apps_Item_List))
          
          <!--
            * 核取方塊
              * 選取=`[0xFFFFFFFF]` [<span style="color: #FFFFFF;">▇</span>]
              * 背景=`[0xFF2196F3]` [<span style="color: #2196F3;">▇</span>]
              * 邊框＝`[0xFFFFFFFF]` [<span style="color: #FFFFFF;">▇</span>]
            * 確定
              * 字型
                * 顏色=`[0xFF2196F3]` [<span style="color: #2196F3;">▇</span>]
                * 大小=18
            * 取消
              * 字型
                * 顏色=`[0xFFF44336]` [<span style="color: #F44336;">▇</span>]
                * 大小=18
          -->
            * 背景
              * 顏色=`[0xFFFFFFFF]` [<span style="color: #FFFFFF;">▇</span>]
            * 選項文字
              * 字型
                * 顏色=`[0xFF000000]` [<span style="color: #000000;">▇</span>]
                * 大小=18
            * 邊框
              * 顏色=無
              * 線條＝無
              * 圓角=30
              * 寬度＝0

  * __<div id="addition">加註</div>__
    * - [x] [基本設定](../Addition/component/basicSettings)
    * - [x] [預設給值](../Addition/component/defaultValue)
    * - [x] [更新給值](../Addition/component/updateValue)
    * - [x] [被動更新](../Addition/component/passiveUpdate)
    * - [x] [編輯能力](../Addition/component/editting)
    * - [x] [顯示設定](../Addition/component/display)
    * - [x] [檢控限制](../Addition/component/prosecutionResstrucson)
    * - [ ] [嵌入物件](../Addition/component/embedded)
    * - [x] [選項清單](../Addition/component/optionList) (必要項)
  * __<div id="behavior">行為</div>__
    * 受權限保護元件
      - [x] [支援](../general/rule)
      - [ ] 不支援
    * 對應檔區：
      * 表單元件/基本設定/存在檔區
    * 對應欄位：
      * 表單元件/基本設定/檢視表對應欄位
      * 支援欄位型態：文字/整數/數字/日期/日期時間/全唯碼
    * 對應查找欄位：
      * 下拉選項-多選
        * 查找資料庫時的條件
    * 顯示巨集：
      - [ ] 支援
      - [x] 不支援
    * [模版](../general/model)：
      - [x] 支援(`下拉選項-單選`)
      - [x] 不支援(`下拉選項-多選`)
    * 提示：
      - [ ] 支援
      - [x] 不支援
    * 錯誤顯示：顯示在元件下方
      - [x] 支援
      - [ ] 不支援
    <!--* 資料過濾：對應欄位-->
    <!--* 資料搜尋：對應欄位-->
    * 瀏覧模式：
      * 內容
        * 顯示所選取資料
        * 不允許點擊
        * `下拉選項＝多選`
          * 多選的資料不顯示取消圖示(X)
    * 編輯模式：
      * 長度限制
        * 依欄位長度限制可顯示字數
          * 下拉選項-單選
            * 長度計算為所有顯示欄位相加的長度
          * 下拉選項-多選
            * 長度計算為所有選擇的資料相加的長度
              * `需加上間隔逗號的長度`
                * Ex.`"key1,key2,key3"=15`
        * 超過時顯示提示
        * 對應查找欄位單獨判斷`(下拉選項-多選)`
          * 長度計算為所有選擇的資料相加的長度
            * `需加上間隔逗號及前後單引號的長度`
              * Ex.`"(N'key1',N'key2',N'key3')"=25`
      * 元件唯讀：(資料元件/編輯能力/可編欄位/唯讀)
        * 不允許點擊
        * `下拉選項＝多選`
          * 多選的資料不顯示取消圖示(X)
      * 內容
        * 顯示所選取資料
        * `下拉選項＝多選`
          * 多選的資料顯示取消圖示(X)
      * 開啟下拉清單：(表單元件/選項清單)
        * 規則
              當元件於`瀏覧模式`時，無法開啟
              當元件唯讀時，無法開啟
              不能有`執行條件`不成立的狀況：`選項清單/執行條件`
              下拉選項出現後，點選其他區域，會自動關閉下拉選項
              點擊`確認`後即為選取，點擊`取消`後即為放棄此次選取
              下拉選項=單選，可上下滑動想選取的資料
              下拉選項=多選，點選為選取，再點選相同項目時為取消
      * 下拉選項的組成
        * 下拉選項=單選
          * 固定選項：(表單元件/選項清單/固定項次)
            | 類型 | 格式 |
            | --- | --- |
            | 有代號、名稱 | 代號.名稱(以點(.)分隔) |
            | 只有代號 | 代號 |
          * 變動選項：(表單元件/選項清單/變動項次)
            * 有代號、名稱：(表單元件/選項清單/帶回對應元件：存在`要顯示＝是 且帶回對應元件<>本元件`)
              * 格式：`對應欄位`對應的`來源欄位`(會套`顯示模版`)+點(.)+選項清單/來源欄位(要顯示＝Y + 帶回對應元件<>本元件)
                * 帶回對應元件<>本元件：
                  * 若有多個會用底線(_)分隔
                  * 顯示格式
                    | 欄位型態 | 去空白 | 特殊格式 |
                    | --- | --- | --- |
                    | 字串 | 是 | |
                    | 日期/日期時間 | 是 | `yyyy/MM/dd hh:mm:ss.SSS` (yyyy：西元(4碼)/MM：月(2碼)/dd：日(2碼)/hh：時(2碼)/mm：分(2碼)/ss：秒(2碼)/SSS：毫秒(3碼)) |
                    | 數字 | 是 | 轉文字 |
                    | 邏輯 | 是 | 當為true，顯示1。否則顯示0 |
            * 只有代號：(表單元件/選項清單/帶回對應元件：不存在`要顯示＝是 且帶回對應元件＝不含本欄位`)
              * 格式：`對應欄位`對應的`來源欄位`(會套`顯示模版`)
            * 帶回值欄位的資料長度超過帶回對應元件的資料長度時
              * 帶回對應元件=本元件
                * 跳錯誤訊息
              * 帶回對應元件<>本元件
                * 跳BPS
        * 下拉選項=多選
          * 可輸入並過濾可選項次`(可關閉)`
          * 會同步輸出至`對應查找欄位`
            * 資料會變成`"'key1', 'key2', 'key3', 'key4'"`
          * 所選取的資料可直接點擊(X)來取消選取
          * 固定選項
            * 同單選
          * 變動選項
            * 同單選
            * 帶回值欄位只能是文字類型`(目前由IDE欄檢)`
      * 強制重顯：(表單元件/選項清單/強制重新載入)
        * 時機：開啟下拉清單
          * 強制重顯=`true`
            * 每次會重新載入選項清單資料
          * 強制重顯=`false`
            * 當查詢條件改變時才會重新載入
            * 表單重顯時才會重新載入
    * 開單隱藏：
      - [ ] 支援
      - [x] 不支援
    * 資料隱藏：
      - [x] 支援
      - [ ] 不支援
    * 元件隱藏：
      - [x] 支援
      - [ ] 不支援
    * 元件除能：
      - [x] 支援
      - [ ] 不支援
    * 元件駐留：
      - [ ] 支援
      - [x] 不支援
        <!--* 元件跳離 (選項值異動時)
          1. 若輸入內容與原值相同時，不會再執行後續的動作
          2. 檢查資料的正確性
             * 若條件不成立時，顯示[錯誤訊息](../general/rule)，並回復原值
             1. 系統檢查
               * [空白檢查](../Addition/component/basicSettings)
               * 各種欄位型態的檢查
                 | 組裝欄位型態 | 檢查項目 |
                 | --- | --- |
                 | 01.Unicode字串(固定長度) | 無 |
                 | 13.Unicode字串(可變長度) | 無 |
                 | 14.字串(固定長度) | 無 |
                 | 15.字串(可變長度) | 無 |
                 | 10.Unicode備註 | 無 |
                 | 17.備註 | 無 |
                 | 04.int | 無|
                 | 05.smallint | 無 |
                 | 06.tinyint | 無 |
                 | 16.bigint | 無 |
                 | 07.數字 | 無 |
                 | 08.金額 | 無 |
                 | 02.日期 | 不符合日期格式：※輸入有誤※日期輸入不合法！ |
                 | 03.日期時間 | 日期須大於1900/01/01且小於2079/06/06：※輸入有誤※日期超出範圍！ |
                 | 11.全唯碼 | 符合全唯碼格式：※輸入有誤※輸入格式不合法！ |
             2. 設計者定義的檢查
               * [檢控限制](../Addition/component/prosecutionRestrictions)
               * 錯誤訊息類型：(表單元件/檢控限制/異常類別)
                 * 錯誤：(表單元件/檢控限制/異常類別/錯誤)
                 * 警告：(表單元件/檢控限制/異常類別/警告)
                 * 詢問：(表單元件/檢控限制/異常類別/操作者決定)
          3. 寫入對應欄位
          4. [更新相關值](../Addition/component/updateValue)
          5. [它欄更新](../Addition/component/passiveUpdate)
          6. 存後：(表單元件/更新給值：ENG.存後)
          7. 重顯相關元件
          8. 跳至另一元件
          9. -->

#### <div id="photo">畫面</div>
* 元件示意圖
  * <div id="photo_dropdown">下拉選項</div>
    
    * <div id="photo_title">標題</div>
    
    ![multi_selected][droplist_title]

    * <div id="photo_enabled">致能</div>

    ![multi_selected][droplist_selected]

    * <div id="photo_readonly">顯示致能(唯讀)</div>
      
      * 下拉選項＝單選
      
        ![image][droplist_selected]

      * 下拉選項＝多選
      
        ![image][droplist_multi_selected_readonly]
  
    * <div id="photo_multi_enabled">多選致能</div>

      ![image][droplist_multi_selected_over_selected]
    
    * <div id="photo_multi_readonly">多選顯示致能(唯讀)</div>

        ![image][droplist_multi_selected_readonly]
    
  * <div id="photo_dropdown_list">選項清單</div>
  
    * 下拉選項＝單選

      ![editing][component_drop_list_editing]

    * 下拉選項＝多選
        
        ![image][droplist_multi_selected_selecting]

      * 選取-查找
          
        ![image][droplist_multi_selected_search]

      * <div id="photo_over_width">超過寬度</div>
          
        ![image][droplist_multi_selected_over_selected]

        ![image][droplist_multi_selected_over_one_selected]
      
      * 欄位資料未包含在選項清單中
      
        ![image][droplist_multi_selected_editable]
      
        ![image][droplist_multi_selected_not_in_list]

      * 選取後的順序
        * 第一次選取
        
          ![image][droplist_multi_selected_first_select]
      
        * 第二次選取
        
          ![image][droplist_multi_selected_second_select]

    * 選項清單無資料時的提示訊息
      
      ![image][droplist_multi_selected_no_list]

#### <div id="workflow">作業流程</div>

* 下拉選項＝單選

  ![image][workflow_droplist_single]

* 下拉選項＝多選

  ![image][workflow_droplist_multi]

<!-- 圖片 -->
[droplist_selected]:./Image/droplist_selected.png
[component_drop_list_editing]:./Image/IOS/component_drop_list_editing.png
[droplist_multi_selected_selecting]:./Image/droplist_multi_selected_selecting.jpg
[droplist_multi_selected_search]:./Image/droplist_multi_selected_search.jpg
[droplist_multi_selected_over_selected]:./Image/droplist_multi_selected_over_selected.png
[droplist_multi_selected_over_one_selected]:./Image/droplist_multi_selected_over_one_selected.png
[droplist_multi_selected_editable]:./Image/droplist_multi_selected_editable.png
[droplist_multi_selected_first_select]:./Image/droplist_multi_selected_first_select.png
[droplist_multi_selected_second_select]:./Image/droplist_multi_selected_second_select.png
[droplist_multi_selected_no_list]:./Image/droplist_multi_selected_no_list.jpg
[droplist_multi_selected_not_in_list]:./Image/droplist_multi_selected_not_in_list.png
[droplist_multi_selected_readonly]:./Image/droplist_multi_selected_readonly.png
[droplist_title]:./Image/droplist_title.png
[workflow_droplist_single]:./Image/workflow_droplist_single.png
[workflow_droplist_multi]:./Image/workflow_droplist_multi.png
