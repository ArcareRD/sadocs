檔案櫃圖檔
===
## 版面相關
* 版面</br>
    ![pic][image_fileCabinetImage]

## 欄位設定
* <p id="fieldbreak1" style="color:blue;">檔案櫃圖檔區塊</p>

    ![pic][image_block1]
    * `(1)櫃名欄位`
        * 用途說明
        * 規格說明
            * 開窗[檔案櫃][link_FileCabinet], 進行檔案櫃挑選, 回傳: 檔案櫃名稱
    * `(2)檔名欄位`
        * 用途說明
        * 規格說明
            * 參照 [挑選表單元件通則][link_ruledialog7], 從駐留表單中, 進行元件挑選, 回傳: 表單元件
            * 參照 [個資加密提示通則][link_ruleother11]

## <div id="save-action">儲存檢控</div>
* 不允空白檢控, 規則參照 [存回不允空白檢控通則][link_ruleother7]
    * `櫃名欄位`、`檔名欄位` 不允空白

<!-- 圖片 -->
[image_fileCabinetImage]:attachment/fileCabinetImage.png
[image_block1]:attachment/fileCabinetImage_block1.png

<!-- 超連結 -->
[link_FileCabinet]:../FileCabinet/README "檔案櫃"
[link_ruledialog7]:../RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruleother11]:../RulesOther/README#ruleother11 "共用通則_其它/個資加密提示通則"
[link_ruleother7]:../RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"