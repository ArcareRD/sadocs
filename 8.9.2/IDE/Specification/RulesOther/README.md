## <p id="ruleother1">版面資訊通則</p>
* 語系:  依登入的平台語系顯示版面多語
* 資料: 依指定的專案語系顯示資料多語

## <p id="ruleother2">OnlineHelp通則</p>
* 依登入之平台語系，開啟對應語系的OnlineHelp檔案
* 依指定錨點，駐留至該錨點下的內容

## <p id="ruleother3">按鍵熱鍵通則</p>
* 依據 UI_Prj_Main.IsUseSystemHotKey
    * true: 取得 HotKeyInfo 所有資料
    * false: 排除 HotKeyInfo.IsSystemUse = true 資料

## <p id="ruleother4">挑選表單檔區通則</p>
* ...

## <p id="ruleother5">MAE加註儲存通則</p>
* 當 設計類型=APP, 介面上被隱藏的欄位, 若存在以下條件, 亦必須寫入資料庫
    * 對應的實體欄位不允空白
    * 第一次進入編輯模式，有給初始值者
    * 被連動更新者 (例：元件加註_基本設定/操作規則/僅供顯示=true，則 游標可駐留=true、可駐留之狀態=瀏覽)

## <p id="ruleother6">權限驗証通則</p>
* 權限控管原則說明
    * 編輯權限(異動資料) / 處理方式 = 按鍵除能
        * 單據無儲存權限, 則按鍵.增、修、刪、存，除能
            * 例：模版 / 按鍵.增、修、刪、存、專案預設</br>
                ![pic][image_editAuthority1]
        * 按鍵會影響資料, 除能
            * 例：規格關聯 / 新增資料區 / 按鍵.儲存</br>
                ![pic][image_editAuthority2]
    * 檢視權限 / 處理方式 = 訊息
        * 單據無檢視檢限, 則執行開單按鍵時, 顯示訊息 "你並未授權執行此功能。"
    * 架構節點, 依登入帳號角色, 判斷顯示 / 隱藏</br>
        ![pic][image_nodeAuthority]

<!-- 圖示 -->
[image_editAuthority1]:attachment/editAuthority1.png
[image_editAuthority2]:attachment/editAuthority2.png
[image_nodeAuthority]:attachment/nodeAuthority.png

<!-- 超連結 -->