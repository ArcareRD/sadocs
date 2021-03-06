## <div id="layout">版面相關</div>
* 版面</br>
    ![pic][image_Specification]
* [版面資訊通則][link_ruleother1]
		
## <div id="form-action">動作說明</div>
* 由各呼叫端開啟 以Dailog on Top 的方式開啟		

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    ![pic][image_fieldbreak1]
    * `(1)OnlineHelp`
        * 用途說明
        * 規格說明
			* [OnlineHelp通則][link_ruleother2], 錨點: ProduceDocument
	* `(2)文件類型`
        * 用途說明
        * 規格說明
			* 選項 需求規格/設定規格, 預設需求規格
	* `(3)文件格式`
        * 用途說明
        * 規格說明
			* 選項 整合文件/獨立檔案, 預設整合文件
	* `(4)獨立檔案區塊`
        * 用途說明
        * 規格說明
			* 除能, 目前暫不提供
	* `(5)表報版面`
        * 用途說明
        * 規格說明
			* 選項 打樣畫面/上傳圖檔, 預設打樣畫面
	* `(6)圖檔上傳`
        * 用途說明
        * 規格說明
			* `(5)表報版面`=上傳圖檔, 致能
            * 檢查圖檔的副檔名必須為ZIP檔
	* `(7)產出範圍`
        * 用途說明
        * 規格說明
			* 選項 全專案/指定事件, 預設全專案
	* `(8)事件名稱`
        * 用途說明
        * 規格說明
			* 指定事件的部份, 已無維護, 雖然可操作，但有可能會有錯誤 (與tracy確認, 保留畫面上的欄位, 但不維護)
			* `(7)產出範圍`=指定事件, 致能
			* 預設根節點事件
			* 開啟<快顯選單>, 可挑選事件
	* `(9)事件載入`
        * 用途說明
        * 規格說明
			* 指定事件的部份, 已無維護, 雖然可操作，但有可能會有錯誤 (與tracy確認, 保留畫面上的欄位, 但不維護)
			* `(7)產出範圍`=指定事件, 致能
			* 依指定的事件, 將查詢出的表、報載入清單中
	* `(10)以上全選`
        * 用途說明
        * 規格說明
			於清單, 依駐留筆以上(含), 勾選打勾
	* `(11)以上取消`
        * 用途說明
        * 規格說明
			* 於清單, 依駐留筆以上(含), 勾選取消打勾
	* `(12)以下全選`
        * 用途說明
        * 規格說明
			* 於清單, 依駐留筆以下(含), 勾選打勾
	* `(13)以下取消`
        * 用途說明
        * 規格說明
			* 於清單, 依駐留筆以下(含), 勾選取消打勾
	* `(14)反向選取`
        * 用途說明
        * 規格說明
			* 於清單, 將所有記錄, 勾選 做打勾/取消打勾的互調
	* `(15)清單`
        * 用途說明
        * 規格說明
			* 指定事件的部份, 已無維護, 雖然可操作，但有可能會有錯誤 (與tracy確認, 保留畫面上的欄位, 但不維護)
	* `(16)勾選`
        * 用途說明
        * 規格說明
			* 預設false
	* `(17)類別`
        * 用途說明
        * 規格說明
			* 顯示 表單/報表
	* `(18)文件名稱`
        * 用途說明
        * 規格說明
			* 顯示 表報名稱
	* `(19)檔案名稱`
        * 用途說明
        * 規格說明
			* 顯示 成品料號
	* `(20)產出`
        * 用途說明
        * 規格說明
			* `(7)產出範圍`=全專案
				* 依表單版面指定, 取得圖片, 呼叫API.Gen_Spec_Servlet, 產生規格書
				* `(5)表報版面`=打樣畫面
					* 當表單設計類型=傳統表單, 取得打樣後的表單畫面
					* 當表單設計類型=RWD、APP, 取得表單版面畫面
					* 取得版面圖片後, 記入catch資料夾, 當下一次產生規格書時, 判斷若未異動, 則直接取catch資料夾內的圖片
				* `(5)表報版面`=打樣畫面, 產生打樣快照
				* `(5)表報版面`=上傳圖檔, 將上傳的ZIP檔，解壓縮後，取得圖片
				* `(2)文件類型`=需求規格, 產出結果, 可參考範例檔案 (<a href="/8.10.0/IDE/Specification/Specification/attachment/SA_Specification.docx" donwnload>SA附件</a>)
				* `(2)文件類型`=設計規格, 產出結果, 可參考範例檔案 (<a href="/8.10.0/IDE/Specification/Specification/attachment/SD_Specification.docx" donwnload>SD附件</a>)
			* `(7)產出範圍`=指定事件
				* 指定事件的部份, 已無維護, 雖然可操作，但有可能會有錯誤 (與tracy確認, 保留畫面上的欄位, 但不維護)
				* 若表格內無勾選者, 提示訊息: 請勾選產出文件項目!
			* 依產出文件的各項指定, 生成文件
	* `(21)下載文件`
        * 用途說明
        * 規格說明
			* 未執行產出前, 除能
			* 將已產出的檔案打包, 下載
	* `(22)下載圖檔`
        * 用途說明
        * 規格說明
			* `(5)表報版面`=打樣圖檔 且 執行產出後, 致能
			* 將打樣圖檔的所有檔案壓縮後下載, 檔案名稱預設 PJ料號.zip

## <div id="other">其它</div>
* 流程相關
    * 若存在流程表單, 則取得流程表單畫面, 若無則不顯示流程表單
        * 顯示順序為, 傳統/RWD表單、APP表單
        * 傳統/RWD流程表單的圖示檔名為 流程料號.png
        * APP流程表單的圖示檔名為 流程料號_APP.png
        * 當 傳統/RWD流程表單、APP流程表單 皆有設定時, 顯示標題 傳統/RWD、APP
        * 有指定流程表單者, 才出現作業流程的章節

* 加註內容, 格式範例如下:
    * 元件加註
        * [元件加註-嵌入物件][] 加註內容
            * 地圖
                * (嵌入物件)【`位置點數` `顯示地標符號` (來源)`檢視表名稱` (過濾)`過濾條件名稱` (位置欄位)`欄位名稱` (資訊欄位)`欄位名稱` (群組)`欄位名稱1`／`欄位名稱2`...】【地標功能 (連結按鍵)`按鍵名稱` (鍵值變數)`變數名稱` (鍵值欄位)`欄位名稱`】【經緯度回傳 (觸發按鍵)`按鍵名稱` (經度變數)`變數名稱` (緯度變數)`變數名稱`】

                * 內容說明
                    * `位置點數`
                        * 顯示 單點位置/多點位置
                    * `顯示地標符號`
                        * `顯示地標符號`有打勾, 才顯示
                    * (來源)`檢視表名稱`
                        * `位置點數`=多點位置, 才顯示
                    * (過濾)`過濾條件名稱`
                        * `過濾條件名稱`有值, 才顯示
                    * 【地標功能 (連結按鍵)`按鍵名稱` (鍵值變數)`變數名稱` (鍵值欄位)`欄位名稱`】
                        * 地標功能區塊有設定才顯示
                    * 【經緯度回傳 (觸發按鍵)`按鍵名稱` (經度變數)`變數名稱` (緯度變數)`變數名稱`】
                        * 經緯度回傳區塊有設定才顯示                
                
    * 按鍵加註
        * [按鍵加註-表單特效][] 加註內容
            | 順序       | 按鍵名稱    | 規格描述                              | 規格定義  |
            | ---------- |----------- | -----------------------------------  | --------- |
            | 依資料排序  | `按鍵名稱`  | (表單特效)【執行條件：`條件名稱1`／`條件名稱2`...】【`處理內容`】 |

            * 執行條件
                * 當執行條件無設定, 則不顯示
            * 處理內容, 依以下說明顯示
                * `處理內容`=關閉表單
                    * 關閉表單
                * `處理內容`=切換頁籤
                    * 【切換頁籤 (頁籤)`元件名稱` (名稱)`頁籤名稱`】
                * `處理內容`=更新欄位
                    * 【更新欄位 (影響筆數)`影響筆數選項` (檔區)`檔區名稱` (`查表來源`)`表格名稱` (過濾)`過濾條件名稱` (給值)`目的欄位名稱` = `給值內容說明`／...】
                * `處理內容`=啟動按鍵
                    * 【啟動按鍵 (按鍵)`按鍵名稱` (次數)`呼叫次數選項` (表格元件)`元件名稱` (起始)`起始記錄選項` (依序)`依序方式選項`】
                * `處理內容`=移動記錄
                    * 【移動記錄 (檔區)`檔區名稱` (移動方式)`移動方式選項`】
                * `處理內容`=更新變數
                    * 【更新變數 (查表來源)`表格名稱` (過濾)`過濾條件名稱` (給值)`全域變數名稱`=`給值內容說明`、...】

        * [按鍵加註-推播通知][link_MAENotice] 加註內容
            | 順序       | 按鍵名稱    | 規格描述                              | 規格定義  |
            | ---------- |----------- | -----------------------------------  | --------- |
            | 依資料排序  | `按鍵名稱`  | 取得該按鍵 [規格備註: 規格描述][link_SpecificationsRemarks] 的內容 | (推播通知)【推播人：`推播人`】【推播來源：(`來源`)`檢視表` (過濾)`過濾`】【推播內容：(`主旨`)`內文`】【連結：(提示文字)`提示文字` (`連結類別`) `連結內容` 】【通知對象：(`來源`)`檢視表` (過濾)`過濾` (帳號)`帳號`】 |

            * 連結內容
                * 當`連結類別`=超連結表單: 取得 [超連結表單][link_linkform] 以下欄位, 組合顯示
                    * `表單名稱`, (過濾) `過濾` , (通行碼) `通行碼`, (有效次數) `有效次數`, (執行系統) `執行系統`, 並進行`帳號驗證` 
                * 當`連結類別`=超連結按鍵: 取得 [連結內容_超連結按鍵][link_linkbutton] 以下欄位, 組合顯示
                    * `表單名稱`, (按鍵名) `按鍵名` , (通行碼) `通行碼`, (有效次數) `有效次數`, (執行系統) `執行系統`, 並進行`帳號驗證`, (執行後續) 成功: `成功訊息`, 失敗: `失敗訊息`, 傳遞: `參數名稱1`=`傳遞類型`.`傳遞內容`／`參數名稱2`=`傳遞類型`.`傳遞內容`／`參數名稱3`=`傳遞類型`.`傳遞內容`／...
                * 當`連結類別`=超連結Google行事曆: 取得 [連結內容_超連結Google行事曆][link_linkgooglecalendar] 以下欄位, 組合顯示
                    * (標題) `類別`.`給值內容`, (內容) `類別`.`給值內容`, (地點) `類別`.`給值內容`, (時段) 來源: `給值來源`, `日期含時間`.`整天`.`格林威治時間`, 日期: `日期起` `時間起`~`日期迄` `時間迄`
                * 當`連結類別`=超連結網址:  取得 [連結內容_超連結網址][link_linkurl] 以下欄位, 組合顯示
                    * (網址): `網址欄位類別`.`網址欄位`, (參數) `網址參數`

<!-- 圖片 -->
[image_Specification]:attachment/Specification.png
[image_fieldbreak1]:attachment/fieldbreak1.png

<!-- 超連結 -->
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother2]:../RulesOther/README#ruleother2 "共用通則_其它/OnlineHelp通則"
[link_MAENotice]:../BANotice/README "按鍵加註-推播通知"
[link_linkform]:../BANotice/MAENotice-Link-Form.md "連結內容_超連結表單"
[link_linkbutton]:../BANotice/MAENotice-Link-Button.md "連結內容_超連結按鍵"
[link_linkgooglecalendar]:../BANotice/MAENotice-Link-GoogleCalendar.md "連結內容_超連結Google行事曆"
[link_linkurl]:../BANotice/MAENotice-Link-URL.md "連結內容_超連結網址"
[link_SpecificationsRemarks]:/8.10.0/IDE/Specification/SpecificationsRemarks/README.md "規格備註"