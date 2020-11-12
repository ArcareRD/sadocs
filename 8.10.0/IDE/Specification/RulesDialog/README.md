## <p id="ruledialog1">操作條件式通則</p>
![pic][image_ruleDialog1]
* `(1)條件欄位`
    * 用途說明
    * 規格說明
        * 顯示條件式名稱
        * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 單據於編輯狀態 或 單據於瀏覽狀態 且 `(1)條件欄位`有值 時, 致能
        * 開窗[條件式][link_Condoper]
        * 回傳: 條件說明
        * 須指定加註類型
        * 當有限定不可查表, 或來源表格時, 條件式內的來源, 不允變動
    * 作業流程
        * <ps>待補</ps> 
* `(3)清除鍵`
    * 用途說明
    * 規格說明
        * 當有清除鍵, 編輯狀態, 致能
        * 當有清除鍵, 清空`(1)條件欄位`
    * 作業流程    
        * <ps>待補</ps>         
* 其它說明
    * 編輯存回, 當條件清除時, 須連帶刪除該條件式的儲存內容

## <p id="ruledialog2">使用多語詞庫通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 顯示多語名稱
        * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 單據於編輯狀態 或 單據於瀏覽狀態 且 `(1)名稱欄位`有值 時, 致能
        * 開窗[多語詞庫][link_Multilingual]
        * 回傳: 多語名稱
    * 作業流程    
        * <ps>待補</ps>         

## <p id="ruledialog3">挑選資料表通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 顯示資料表名稱
        * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 單據於編輯狀態 或 單據於瀏覽狀態 且 `(1)名稱欄位`有值 時, 致能
        * 開窗[資料表][link_Physical]
        * 過濾: 依各單據需求, 指定過濾條件
        * 回傳: 資料表名稱
        * 當`(1)名稱欄位`有值 且 與回傳的資料表名稱不相同時, 顯示詢問訊息盒【標題: 系統訊息 / 訊息內容: 異動資料表將清除相關欄位, 是否繼續? / 按鍵: 確認、取消】
            * 確認: 關閉訊息, 清除相關的欄位或記錄
                * 清除內容依各單據需求指定
            * 取消: 關閉訊息, 保留原內容
    * 作業流程    
        * <ps>待補</ps>         

## <p id="ruledialog5">挑選資料表元件通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 顯示資料表元件名稱
        * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 編輯狀態 時, 致能
        * 開窗[快顯選單][link_Quick]
        * 過濾: 指定的資料表 及 依各單據需求, 指定其它過濾條件
        * 回傳: 資料表元件名稱
    * 作業流程    
        * <ps>待補</ps>         

## <p id="ruledialog4">挑選檢視表通則</p>
![pic][image_ruleDialog3]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 顯示檢視表名稱
        * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 單據於編輯狀態 或 單據於瀏覽狀態 且 `(1)名稱欄位`有值 時, 致能
        * 開窗[檢視表][link_Logical]
        * 過濾: 依各單據需求, 指定過濾條件
        * 回傳: 檢視表名稱
        * 當`(1)名稱欄位`有值 且 與回傳的檢視表名稱不相同時, 顯示詢問訊息盒【標題: 系統訊息 / 訊息內容: 異動檢視表將清除相關欄位, 是否繼續? / 按鍵: 確認、取消】
            * 確認: 關閉訊息, 清除相關的欄位或記錄
                * 清除內容依各單據需求指定
            * 取消: 關閉訊息, 保留原內容
    * 作業流程    
        * <ps>待補</ps>         
* `(3)參數鍵`
    * 用途說明
    * 規格說明
        * 單據於編輯狀態 或 單據於瀏覽狀態 且 `(1)名稱欄位`有值 時, 致能
        * 當`(1)名稱欄位`無值, 顯示訊息盒【標題: 系統訊息 / 訊息內容: 請先設定 檢視表 / 按鍵: 確認】
            * 確認: 關閉訊息
        * 開窗[傳遞參數][link_Parameter]
        * 傳入: `(1)名稱欄位`
    * 作業流程    
        * <ps>待補</ps>         
* 其它說明
    * 編輯存回, 當參數清除時, 須連帶刪除該傳遞參數的儲存內容

## <p id="ruledialog8">挑選檢視表元件通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 編輯狀態
            * 顯示檢視表元件名稱
            * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 編輯狀態 時, 致能
        * 開窗[快顯選單][link_Quick]
        * 過濾: 指定的檢視表 及 依各單據需求, 指定其它過濾條件
        * 回傳: 檢視表元件名稱
    * 作業流程    
        * <ps>待補</ps>

## <p id="ruledialog6">挑選表單通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 編輯狀態
            * 依專案多語顯示表單名稱
            * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 編輯狀態 時, 致能
        * 開窗[快顯選單][link_Quick]
        * 過濾: 依各單據需求, 指定過濾條件
        * 回傳: 表單名稱
        * 當`(1)名稱欄位`有值 且 與回傳的表單名稱不相同時, 顯示詢問訊息盒【標題: 系統訊息 / 訊息內容: 異動表單將清除相關欄位, 是否繼續? / 按鍵: 確認、取消】
            * 確認: 關閉訊息, 清除相關的欄位或記錄
                * 清除內容依各單據需求指定
            * 取消: 關閉訊息, 保留原內容
    * 作業流程    
        * <ps>待補</ps>         

## <p id="ruledialog7">挑選表單元件通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 依專案多語顯示表單元件名稱
        * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 編輯狀態 時, 致能
        * 開窗[快顯選單][link_Quick]
        * 過濾: 依下列條件過濾
            * 指定的表單
            * 元件類型不為按鍵(以下列出按鍵的元件類型)
                |元件類型 |
                |--------|
                |wMBOpen.開啟(選單列) |
                |wMBExit.退出(選單列) |
                |wMBAdd.新增(選單列) |
                |wMBEdit.修改(選單列) |
                |wMBASave.新增存回(選單列) |
                |wMBESave.修改存回(選單列) |
                |wMBDelete.刪除(選單列) |
                |wMBExport.匯出(選單列) |
                |wMBImport.匯入(選單列) |
                |wMBPrint.列印(選單列) |
                |wMBCopy.複製(選單列) |
                |wMBList.清單(選單列) |
                |wTBMenu.功能選單 |
                |wTBBtn.功能按鈕 |
                |funckey.功能按鍵(欄位資料) |
                |liteFunckey.功能按鍵(多覽欄位資料) |
                |wTBMenuItem.功能選單項目 |
                |wHBtn.隱藏按鍵) |
            * 依各單據需求, 指定其它過濾條件
        * 回傳: 表單元件名稱
    * 作業流程    
        * <ps>待補</ps>         

## <p id="ruledialog13">挑選表單按鍵通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 依專案多語顯示表單按鍵名稱
        * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 編輯狀態 時, 致能
        * 開窗[快顯選單][link_Quick]
        * 過濾: 依下列條件過濾
            * 指定的表單
            * 元件類型須為按鍵
                |元件類型 |
                |--------|
                |wMBOpen.開啟(選單列) |
                |wMBExit.退出(選單列) |
                |wMBAdd.新增(選單列) |
                |wMBEdit.修改(選單列) |
                |wMBASave.新增存回(選單列) |
                |wMBESave.修改存回(選單列) |
                |wMBDelete.刪除(選單列) |
                |wMBExport.匯出(選單列) |
                |wMBImport.匯入(選單列) |
                |wMBPrint.列印(選單列) |
                |wMBCopy.複製(選單列) |
                |wMBList.清單(選單列) |
                |wTBMenu.功能選單 |
                |wTBBtn.功能按鈕 |
                |funckey.功能按鍵(欄位資料) |
                |liteFunckey.功能按鍵(多覽欄位資料) |
                |wTBMenuItem.功能選單項目 |
                |wHBtn.隱藏按鍵) |
            * 依各單據需求, 指定其它過濾條件
        * 回傳: 表單按鍵名稱
    * 作業流程    
        * <ps>待補</ps>         

## <p id="ruledialog9">挑選參數通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 顯示參數名稱
        * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 編輯狀態 時, 致能
        * 開窗[快顯選單][link_Quick]
        * 過濾: 依下列條件過濾
            * 指定的檢視表 或 資料交易 或 表單 或 報表
            * 依各單據需求, 指定其它過濾條件
        * 回傳: 表單參數名稱
    * 作業流程    
        * <ps>待補</ps>         

## <p id="ruledialog10">挑選全域變數通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 顯示全域變數名稱
        * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 單據於編輯狀態 或 單據於瀏覽狀態 且 `(1)名稱欄位`有值 時, 致能
        * 開窗[全域變數][link_GlobalVariable]
        * 過濾: 依各單據需求, 指定其它過濾條件
        * 回傳: 全域變數名稱
    * 作業流程    
        * <ps>待補</ps>         

## <p id="ruledialog11">設定按鍵執行條件表格通則</p>
![pic][image_ruleDialog4]
* `(1)條件內容`
    * 用途說明
    * 規格說明
        * [操作條件式通則][link_ruledialog1]
* `(2)訊息處理`
    * 用途說明
    * 規格說明
        * [操作按鍵執行條件訊息通則][link_ruledialog12]
* `(3)表格操作`
    * 用途說明
    * 規格說明
        * [操作表格記錄通則][link_rulebutton3]
* 其它說明
    * 編輯存回, 當記錄刪除時, 須連帶刪除該`(1)條件內容`、`(2)訊息處理`的儲存內容

## <p id="ruledialog12">操作按鍵執行條件訊息通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 顯示訊息內容
        * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 單據於編輯狀態 或 單據於瀏覽狀態 且 `(1)名稱欄位`有值 時, 致能
        * 開窗[按鍵執行條件訊息][link_BAXCondition]
        * 回傳: 錯誤訊息名稱
    * 作業流程    
        * <ps>待補</ps>         

## <p id="ruledialog14">挑選開放按鍵傳入參數通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 顯示開放按鍵傳入參數名稱
        * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 編輯狀態 時, 致能
        * 開窗[快顯選單][link_Quick]
        * 過濾: 指定的開放按鍵 及 依各單據需求, 指定其它過濾條件
        * 回傳: 參數名稱
    * 作業流程    
        * <ps>待補</ps>

## <p id="ruledialog15">挑選報表元件通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 編輯狀態
            * 顯示報表元件名稱
            * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 編輯狀態 時, 致能
        * 開窗[快顯選單][link_Quick]
        * 過濾: 指定的報表 及 依各單據需求, 指定其它過濾條件
        * 回傳: 報表元件名稱
    * 作業流程    
        * <ps>待補</ps>

## <p id="ruledialog16">挑選函數通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 編輯狀態
            * 顯示函數元件名稱
            * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 編輯狀態 時, 致能
        * 開窗[快顯選單][link_Quick]
        * 過濾: 依各單據需求, 指定過濾條件
        * 回傳: 函數名稱
    * 作業流程    
        * <ps>待補</ps>        

## <p id="ruledialog16">挑選開放按鍵回傳參數通則</p>
![pic][image_ruleDialog2]
* `(1)名稱欄位`
    * 用途說明
    * 規格說明
        * 顯示開放按鍵回傳參數名稱
        * 不須輸入, 唯讀
* `(2)開窗鍵`
    * 用途說明
    * 規格說明
        * 編輯狀態 時, 致能
        * 開窗[快顯選單][link_Quick]
        * 過濾: 指定的開放按鍵 及 依各單據需求, 指定其它過濾條件
        * 回傳: 參數名稱
    * 作業流程    
        * <ps>待補</ps>

<!-- 圖示 -->
[image_ruleDialog1]:attachment/ruleDialog1.png
[image_ruleDialog2]:attachment/ruleDialog2.png
[image_ruleDialog3]:attachment/ruleDialog3.png
[image_ruleDialog4]:attachment/ruleDialog4.png

<!-- 超連結 -->
[link_Condoper]:../Condoper/README "條件式"
[link_Multilingual]:../Multilingual/README "多語詞庫"
[link_Quick]:../Quick/README "快顯選單"
[link_Physical]:../Physical/README "資料表"
[link_Logical]:../Logical/README "檢視表"
[link_Parameter]:../Parameter/README "傳遞參數"
[link_GlobalVariable]:../GlobalVariable/README "全域變數"
[link_BAXCondition]:../BAXCondition/README "按鍵執行條件訊息"
[link_ruledialog1]:#ruledialog1 "操作條件式通則"
[link_ruledialog12]:#ruledialog12 "操作按鍵執行條件訊息通則"
[link_rulebutton3]:../RulesButton/README#rulebutton3 "共用通則_按鍵操作/操作表格記錄通則"