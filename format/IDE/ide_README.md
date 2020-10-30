單據名稱
===

## <div id="layout">版面相關</div>
* 版面
    * 分類</br>
        ![pic][desc1]

* 說明內容

## <div id="form-action">動作說明</div>
* 說明內容

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">區塊名稱</p>

    * 分類</br>
        ![pic][desc1]
    * (編碼)欄位名稱 
        * 用途說明
            * 說明內容
        * 規格說明
            * 說明內容

## <div id="save-action">儲存檢控</div>
* 檢控分類
    * 內容說明

## <div id="">其它</div>
* 內容說明

***
以下說明文件規格及原則

* 單據名稱</br>
    ![pic][desc2]
    * 子單據才會標示
        * 例: 元件加註_嵌入物件 的 網頁、地圖、影片...等, 標示 "網頁"、"地圖"、"影片"
* 版面相關</br>
    ![pic][desc3]
    * 錨點: layout
    * 分類
        * 例: 部份 元件加註、按鍵加註 的單據, 可分為 STD、RWD、MAE
        * 若無分類, 不須呈現分類標題
    * 圖示
        * 單據全圖, 須將所有欄位按鍵儘量全部呈現出來
            * 例: grid的欄位, 須顯示1行</br>
                ![pic][desc_exp1]
            * 例: 主檔單據的勾選回傳鍵，須顯示</br>
                ![pic][desc_exp2]
            * 若有較複雜的變化, 可多張圖呈現
                * 例: 部份 元件加註、按鍵加註 的單據, 會因設計類型呈現不同變化, 切多張圖呈現
    * 規格內容說明
        * 針對版面說明規格
        * [註1](#tag1)
* 動作說明</br>
    ![pic][desc4]
    * 錨點: form-action
    * 開單或開單後的行為規格說明
    * [註1](#tag1)
    * 部份md檔不須要有
        * 例: 元件加註_嵌入物件/網頁、地圖、影片...等    
* 欄位說明</br>
    ![pic][desc5]
    * 錨點: object-desc
    * 區塊名稱
        * 須埋錨點

                <p id="fieldbreak1" style="color:blue;font-weight:bold">區塊名稱<>
            * id由fieldbreak1依序往下編
            * 藍字、粗體
    * 分類
        * 例: 部份 元件加註、按鍵加註 的單據, 可分為 STD、RWD、MAE
        * 若無分類, 不須呈現分類標題
    * 區塊圖示
        * 呈現須規格說明的區塊圖示, 並標記編號
            * 以下範例</br>
                ![pic][desc_exp4]
        * 標記
            * 使用PicPick/圖章
            * 編碼最大只到100, 超過須拆圖
            * 針對欲描述規格者設定標記編號
    * 欄位名稱
        * 針對標記編號的欄位、按鍵、區塊, 描述規格
        * 指定欄位, 寫法為 "(標記編號)欄位名稱"
    * 用途說明
        * 說明該欄位於IDE上的用途
    * 規格說明
        * 說明該欄位的規格
        * [註1](#tag1)
* 儲存檢控</br>
    ![pic][desc6]
    * 錨點: save-action
    * 檢控分類
        * 可分為不允空白、其它檢控...等, 依各單據規格進行分類
    * 規格內容說明
        * [註1](#tag1)
* 其它</br>
    ![pic][desc7]
    * 錨點: 自行設定
    * 依各單據規格可能有特殊規格須描述, 例: 儲存後的作動...等
    * 標題自行調整, 不一定要叫 "其它"
    * [註1](#tag1)

* <p id="tag1">註1: 說明內容</p>

    * 若有規格描述到跨區塊欄位時, 寫法為 "區塊名稱(標記編號)欄位名稱"
        * 例: 當 [檔案設定區塊]()(1)檔案類型=Excel 且 [檔案設定區塊]()(5)範本附件=範本，才可點選表格型，否則除能
        * 須超連結至該區塊
    * 若有規格描述到共用通則時, 須連結至該通則
        * 例: [版面資訊通則]()
        * 須完全符合該通則才可連結
    * 若有規格描述到其它單據或其它頁面時, 須連結至該單據、頁面規格
        * 例: 開啟[版本資訊]()
    * 若有規格描述到其它單據或其它頁面的欄位時, 須連結至該區塊
        * 寫法為 "單據名稱(標記編號)欄位名稱"
        * 例: 當 [使用者設定]()(n)新手教學選項=是, 則...
    * 若有規格描述到複雜案例時, 可至excel上編輯並截圖
        * excel原始檔案(檔名: attachment.xlsx)置於 (資料夾)attachment 中
        * 該單據若有多個, 置於同一個excel檔中，切頁籤存放
        * 圖示呈現至規格文件中
        * 圖示旁標註檔案頁籤
        * 例:</br>
            ![pic][desc_exp5]

                <!-- 原始檔案: 頁籤名稱 -->
    * 說明內文皆可使用圖文
    * 除非有統一的標記定義, 否則, 說明內容請不要有特殊標記, 例: 粗體、斜體、字體顏色...等

* 註2: 圖示、超連結說明
    * 置於文件最下方, 圖示、超連結, 分區置放</br>

<!-- 圖示 -->
[desc_exp1]:attachment/desc_exp1.png
[desc_exp2]:attachment/desc_exp2.png
[desc_exp4]:attachment/desc_exp4.png
[desc_exp5]:attachment/desc_exp5.png
[desc1]:attachment/desc1.png
[desc2]:attachment/desc2.png
[desc3]:attachment/desc3.png
[desc4]:attachment/desc4.png
[desc5]:attachment/desc5.png
[desc6]:attachment/desc6.png
[desc7]:attachment/desc7.png

<!-- 超連結 -->