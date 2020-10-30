## <p id="ruleother1">版面資訊通則</p>
* 語系:  依登入的平台語系顯示版面多語
* 資料: 依指定的專案語系顯示資料多語

## <p id="ruleother2">OnlineHelp通則</p>
* 依登入之平台語系，開啟對應語系的OnlineHelp檔案
* 依指定標籤/毛點，駐留至該標籤/毛點下的內容

## <p id="ruleother3">按鍵熱鍵通則</p>
* 依據 UI_Prj_Main.IsUseSystemHotKey
    * true : 取得 HotKeyInfo 所有資料
    * false : 排除 HotKeyInfo.IsSystemUse = true 資料

## <p id="ruleother4">挑選表單檔區通則</p>
* ...

## <p id="ruleother5">MAE加註儲存通則</p>
* 當 設計類型=APPS, 介面上被隱藏的欄位, 若存在以下條件, 亦必須寫入資料庫
    * 對應的實體欄位不允空白
    * 第一次進入編輯模式，有給初始值者
    * 被連動更新者 (例：元件加註_基本設定/操作規則/僅供顯示=true，則 游標可駐留=true、可駐留之狀態=瀏覽)

## <p id="ruleother">權限驗証方法</p> 
* ...