### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2020/12/7

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">專案架構樹</p>

    * ![pic][image_Structure_workflow]
    * `(1)工具列_新增`
        * 用途說明
        * 規格說明
            * 駐留節點存在【作業流程、模組、流程】致能, 否則 除能. 單擊按鍵時, 依下列條件決定按鍵選單
                * 任務: 駐留節點存在【作業流程】顯示. 同右鍵功能.`(5)新增任務`
    * `(2)工具列_刪除`
        * 用途說明
        * 規格說明
            * 駐留節點存在【模組、流程、表單、報表、任務】致能, 否則 除能. 參考各節點右鍵功能.`刪除`
    * `(3)工具列_重新命名`
        * 用途說明
        * 規格說明
            * 駐留節點存在【模組、流程、表單、報表、任務】致能, 否則 除能. 參考各節點右鍵功能.`重新命名`
    * `(4)架構樹內容`
        * 用途說明
        * 規格說明
            * 本版新增節點類別說明, 請看紅框線部份【完整版本請參閱附件, 工作表:專案架構樹 (<a href="/8.10.0/UPDATE/ITEM_1/IDE/Home/attachment/Home.xlsx" download>下載</a>)】
            * ![pic][image_StructureTree]
    * `(5)新增任務`
        * 用途說明
        * 規格說明
            * 駐留節點存在【作業流程】顯示, 否則 隱藏
            * 執行開啟 [新增任務][link_addofflinetask], 關單後, 參考`(4)架構樹內容`節點位置, 回傳並顯示 **離線任務名稱**


* <p id="fieldbreak1" style="color:blue;font-weight:bold">離線任務節點</p>

    * ![pic][image_Structure_Offlinetask_ContextMenu]
    * `(1)重新命名`
        * 用途說明
        * 規格說明
            * 駐留節點類別存在【模組、流程、表單、報表】顯示, 否則 隱藏
            * 執行時, 駐留節點變更為可修改的文字方塊，並依駐留的專案語系修改該節點類別對應的多語名稱
    * `(2)刪除`
        * 用途說明
        * 規格說明
            * 駐留節點類別存在【模組、流程、表單、報表、任務】顯示, 否則 隱藏, 每次執行顯示訊息盒【標題:系統訊息 / 訊息內容:請確認是否執行刪除 「(*單元類別名*) *節點名稱* 」? / 按鍵: 刪除、取消】
                * 刪除: 依刪除類別刪除相對應的資料
                    * 節點類別=任務，刪除該任務，若子階含有表單 且 表單未存在其它任務中，則將表單歸屬到作業流程的子階節點
                * 取消: 關閉訊息視窗
    * `(3)規格備註`
        * 用途說明
        * 規格說明
            * 開啟 [規格備註][link_specificationsremarks]


<!-- 圖片 -->
[image_StructureTree]:attachment/StructureTree.png
[image_Structure_workflow]:attachment/Structure_WorkFlow.png
[image_Structure_Offlinetask_ContextMenu]:attachment/Structure_OfflineTask_ContextMenu.png


<!--超連結 -->
[link_specificationsremarks]:/8.10.0/IDE/Specification/SpecificationsRemarks.md
[link_addofflinetask]:AddOfflineTask.md