﻿### <div id="view">畫面說明</div>
* 新版首頁的畫面功能分布如下圖所示:

    ![新版首頁畫面]

* 須在[站台管理表單.其他參數](../../SITE/otherparameter/README.md)設定啟用新版首頁樣式，使用者登入後才會進入此頁面。
* 已登入過系統的的使用者，再次登入時，會預設依照上次登入的設定，進行自動登入
* 如果使用者僅有一個系統可使用，會預設使用以下設定進行該系統的登入
    * 系統:挑選此系統
    * 分公司:挑選此系統下第一個分公司
    * 語系:
        * 上次登入使用語系
        * 950(繁體中文)
        * 該系統的第一個語系
* 登入系統後，若使用者的帳號在[系統工具表單.用戶帳號維護]()在設定登入執行，則會自動開啟該表單

### <div id="logo">系統自訂版面主畫面圖片<path>(畫面說明)</path></div>
* 該圖片可由[站台管理表單.企業資料設定]()指定，依據登入使用者所屬企業顯示主畫面圖片。，如下圖紅框所示:

    ![企業資料設定LOGO]

### <div id="myfavorite">開啟常用表單<path>(畫面說明)</path></div>
* 與使用者帳號綁定，用來記錄使用者在此系統中常用的表單清單
* 下圖為常用表單畫面，分為兩個區塊
 
    ![常用表單畫面]

* 常用表單 : 依照加入的順序排序，先加入的排前面，僅可記錄10張
    * 畫面樣式
        * 初始化樣式

            ![常用表單初始化樣式]
            
        * 滑鼠移入時的樣式

            ![常用表單初始化樣式]

        * 滑鼠點擊後的樣式

            ![常用表單滑鼠點擊樣式]

        * 滑鼠拖曳時的樣式

            ![常用表單滑鼠拖曳樣式]

    * 開啟常用表單 : 滑鼠雙擊表單可進行開啟表單的動作
    * 設定常用表單 : 待補
    * 移除常用表單 : 點擊按鈕.移除，點擊後跳出以下確認視窗畫面，確定後刪除。

        ![移除常用表單]

* 最近開啟 : 最近開啟的表單清單，依照開啟時間排序，最新排前面，僅可記錄10張
    * 畫面樣式
        * 初始化樣式

            ![最近開啟初始化樣式]

        * 滑鼠移入時的樣式

            ![最近開啟滑鼠移入樣式]

    * 開啟最近開啟 : 滑鼠雙擊最近開啟表單，表示開啟此表單並將常用表單畫面關閉
    * 清除最近開啟 : 點擊按鈕.清除，出現清除紀錄的詢問視窗，點擊確認後清除所有最近開啟的紀錄，如下圖所示:
        
        ![清除最近開啟]

### <div id="mainmenu">系統主選單<path>(畫面說明)</path></div>
* 為使用者在此系統能使用的表單選單
* 選單本身可拖曳改變寬度，最小寬度為260px，最大寬度為螢幕的50%，改變寬度後會依網站記錄在Client端的localStorage中，下次登入會直接以此設定改變選單寬度
* 選單內只會出現RWD/STD的表單
* 若選單節點下的節點沒有表單時，要隱藏該選單節點
* ROOT節點會有表單 : 沒有掛在事件裡的表單，且該表單的獨立開啟=是。(由IDE_表單加註_基本設定_獨立開啟設定)
* 節點裡，同時有子節點以及表單時，先出現子節點，再出現表單。
* 待補

### <div id="search">搜尋表單<path>(畫面說明)</path></div>
* 提供使用者搜尋系統主選單內的表單清單功能
* 搜尋框中沒有任何內容時，顯示提示字串﹝搜尋表單﹞
* 輸入文字後按ENTER或點擊放大鏡表示開始搜尋
* 搜尋方式會以系統主選單中的所有表單進行表單名稱比對，比對成功者出現在搜尋結果中
* 樣式狀態如下
    * 未駐留時樣式

        ![搜尋表單初始化樣式]

    * 駐留時樣式

        ![搜尋表單駐留樣式]
    
    * 搜尋結果樣式

        ![搜尋結果樣式]

* 搜尋結果說明待補

### <div id="hidemenu">隱藏左方選單<path>(畫面說明)</path></div>
* 滑鼠點擊後，左方主選單隱藏並顯示如下圖
    
    ![隱藏左方主選單]


### <div id="changesystem">切換系統<path>(畫面說明)</path></div>
* 待補

### <div id="systemfunction">系統工具列<path>(畫面說明)</path></div>
* 開啟報表時，不依照系統[工具表單.系統參數]()設定勾選隱藏系統工具列，強制顯示系統工具列
* 其餘待補

### <div id="systemmenu">系統選單列<path>(畫面說明)</path></div>
* 可由[系統工具表單.系統參數]()設定系統選單列是否隱藏
    
    ![系統參數設定]

    * 若選擇隱藏，則登入系統時，自動隱藏系統選單列、切換系統等區塊，並將個人資訊移至左側欄顯示，如下圖紅框所示:

        ![關閉系統選單]

        * 當隱藏系統選單列且左側欄收起時，個人資訊移至左側欄小圖示清單，如下圖紅框所示:

            ![左側欄圖示清單]
    
    * 其餘待補

### <div id="formtab">表單頁簽列<path>(畫面說明)</path></div>
* 以頁簽方式顯示目前已開啟的表單
* 頁簽設定在[站台管理表單.企業資料]()中針對企業使用系統進行設定，如下圖所示

    ![頁簽設定]

* 選單開單方式共有三種 :
    * 單頁簽 : 開啟表單時僅留下本表單以及本表單的父階關係表單，設定此方式時，首頁的表單頁簽列隱藏，如下圖所示:

        ![隱藏表單頁簽列]

        * 若表單或子表單已在新增或修改，並已經異動資料，此時點擊系統主選單開啟表單時，需先詢問﹝表單資料已有異動，是否放棄異動資料?﹞若使用者選擇確定，則放棄異動資料並解除鎖定後關閉所有表單再開新表單，選擇取消則不做任何處理。提示畫面如下圖所示:

            ![放棄異動資料]
    * 多頁簽 : 可開啟多個表單，相同的表單也可重複開啟多次，其餘待補。
    * 不重複頁簽 : 可開啟多個表單，但相同的表單不會重複開啟，其餘待補。

### <div id="personaldata">個人資訊<path>(畫面說明)</path></div>
* 依據[站台管理表單.其他參數](../../SITE/otherparameter/README.md)的設定.顯示用戶名稱來決定是否顯示用戶名稱
* 點擊圖示出現小選單，共有以下選項
    * 個人資料 : 點擊後開啟表單.個人資料，如下圖所示:

        ![個人資料]

    * 登出 : 點擊後執行使用者登出。
    
### <div id="form">表單編輯區<path>(畫面說明)</path></div>
* 待補


### <div id="action">作業流程</path></div>
* 登入新版首頁_首頁處理流程

    ![登入新版首頁]

* 登入系統_首頁處理流程

    ![登入系統]

* 系統主選單開啟表單

    ![系統主選單開啟表單]

    ![開啟表單流程]

* 點擊隱藏左方選單

    ![點擊隱藏左方選單]

* 開啟報表

    ![開啟報表]

* 其餘待補

[新版首頁畫面]:attachment/brainworknew.png "新版首頁畫面"
[企業資料設定LOGO]:attachment/enterprisedata_updatelogo.png "企業資料設定LOGO"
[系統參數設定]:attachment/sysparam.png "系統參數設定"
[關閉系統選單]:attachment/hidesystemmenu.png "關閉系統選單"
[左側欄圖示清單]:attachment/leftbarmenu.png "左側欄圖示清單"
[隱藏表單頁簽列]:attachment/hideformtab.png "隱藏表單頁簽列"
[放棄異動資料]:attachment/discarddata.png "放棄異動資料"
[登入新版首頁]:attachment/loginhomepage.png "登入新版首頁"
[登入系統]:attachment/loginsystem.png "登入系統"
[系統主選單開啟表單]:attachment/homepageopenform.png "系統主選單開啟表單"
[開啟表單流程]:attachment/openformflow.png "開啟表單流程"
[點擊隱藏左方選單]:attachment/hideleftframe.png "點擊隱藏左方選單"
[開啟報表]:attachment/openreportnew.png "開啟報表"
[常用表單畫面]:attachment/myfavorite.png "常用表單畫面"
[常用表單初始化樣式]:attachment/myfavorite_style_enable.png "常用表單初始化樣式"
[常用表單滑鼠移入樣式]:attachment/myfavorite_style_mousein.png "常用表單滑鼠移入樣式"
[常用表單滑鼠點擊樣式]:attachment/myfavorite_style_click.png "常用表單滑鼠點擊樣式"
[常用表單滑鼠拖曳樣式]:attachment/myfavorite_style_drag.png "常用表單滑鼠拖曳樣式"
[個人資料]:attachment/personaldata.png "個人資料"
[頁簽設定]:attachment/singleformtab.png "頁簽設定"
[移除常用表單]:attachment/deletemyfavorite.png "移除常用表單"
[最近開啟初始化樣式]:attachment/recentlyopen_style_enable.png "最近開啟初始化樣式"
[最近開啟滑鼠移入樣式]:attachment/recentlyopen_style_mousein.png "最近開啟滑鼠移入樣式"
[清除最近開啟]:attachment/clear_recentlyopen.png "清除最近開啟"
[隱藏左方主選單]:attachment/hideleftmenu.png "隱藏左方主選單"
[搜尋表單初始化樣式]:attachment/searchform_enable.png "搜尋表單初始化樣式"
[搜尋表單駐留樣式]:attachment/searchform_focus.png "搜尋表單駐留樣式"
[搜尋結果樣式]:attachment/searchform_result.png "搜尋結果樣式"