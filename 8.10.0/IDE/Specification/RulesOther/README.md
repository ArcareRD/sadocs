## <p id="ruleother1">版面資訊通則</p>
* 語系: 依登入的平台語系顯示版面多語
* 資料: 依指定的專案語系顯示資料多語

## <p id="ruleother2">OnlineHelp通則</p>
* 依登入之平台語系, 開啟對應語系的OnlineHelp檔案
* 依指定錨點, 駐留至該錨點下的內容

## <p id="ruleother4">挑選表單檔區通則</p>
* ...

## <p id="ruleother5">MAE加註儲存通則</p>
* 當 [新增表單/報表][link_AddFormReport]的`設計類型`為APP, 介面上被隱藏的欄位, 若存在以下條件, 亦必須寫入資料庫
    * 對應的實體欄位不允空白
    * 第一次進入編輯模式, 有給初始值者
    * 被連動更新者 (例：[元件加註_基本設定][link_ObjectAnnotation]的`僅供顯示`有勾選，則`游標可駐留`須寫入勾選、`可駐留之狀態`為瀏覽)

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
        ![pic][image_nodeAuthority] <!-- 原始檔案: 架構節點權限 -->

## <p id="ruleother7">存回不允空白檢控通則</p>
* 不允空白檢控, 符合條件時, 顯示訊息盒, 並以紅框線標註錯誤的欄位
    * 訊息盒:【標題: 執行存回，發生下列錯誤 / 訊息內容: 以下資料未填寫正確 *錯誤欄位名* / 按鍵: 確定】
        * 確定: 關閉訊息盒
    * 作業流程    
        * <ps>待補</ps>

## <p id="ruleother8">存回其它檢控通則</p>
* 其它檢控, 符合條件時, 顯示訊息盒, 並以紅框線標註錯誤的欄位
    * 訊息盒:【標題: 執行存回，發生下列錯誤 / 訊息內容: 以下資料未通過驗證 *錯誤訊息內容* / 按鍵: 確定】
        * 確定: 關閉訊息盒
    * 作業流程    
        * <ps>待補</ps>

<!-- 圖示 -->
[image_editAuthority1]:attachment/editAuthority1.png
[image_editAuthority2]:attachment/editAuthority2.png
[image_nodeAuthority]:attachment/nodeAuthority.png

<!-- 超連結 -->
[link_AddFormReport]:../AddFormReport/README "新增表單/報表"
[link_ObjectAnnotation]:../ObjectAnnotation/README "元件加註_基本設定"