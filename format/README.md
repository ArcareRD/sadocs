# <div id="folder">資料夾預設檔案</div>
* 每個資料夾都會有下列檔案    

        _sidebar.md (側邊導航欄)
        README.md (頁面)
        history.md (變更記錄)
        attachment (附件資料夾)(可沒有)

# <div id="back-btn">上一頁的連結寫法</div>
* 若檔案會被多個檔案呼叫時的寫法

        * [上一頁]({back})

# <div id="history">History</div>
* 須出現在`側邊導航欄`的`最後一個項目`

    # 基本設定
    * [上一頁](../README.md)
    * 加註項目
        * [對應熱鍵](README.md#hotkey)
        * [系統按鈕](README.md#sysbtn)
        * [隱藏按鈕類別](README.md#hidebtn)
    * 案例
        * [((STD)按鍵加註_基本設定(Rita))](Example/FX999500001767.md)
        * [((RWD)按鍵加註_基本設定(Rita))](Example/FX999500001768.md)
    * [History](history.md)

# 超連結
非`_sidebar.md`的md檔，固定將所有的超連結放在檔案的最後面。

* 格式

    [`超連結顯示文字`]:`超連結` "`hint`"

* 範例

        * Added rita 2019/05/24 :  擴充`游標可駐留` ([Trac#6737])
        * Removed rita 2020/09/01 :  刪除`游標可駐留` ([Trac#9999])

        [Trac#6737]:http://trac.uneec.com/trac/neco/ticket/6737 "#6737"
        [Trac#9999]:http://trac.uneec.com/trac/neco/ticket/9999 "#9999"
