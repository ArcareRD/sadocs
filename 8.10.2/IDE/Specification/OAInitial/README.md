## <div id="layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_OAInitial_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_OAInitial_MAE]
* [版面資訊通則][link_ruleother1]
		
## <div id="form-action">動作說明</div>
* 依規格關聯-主畫面 結構清單駐留元件及指定加註條件, 顯示本單內容
* 依規格關聯-主畫面 工具列.編修鍵, 進入本單的編輯模式
* 參照 [單據異動資料按鍵操作通則][link_rulebutton2]
    * 下列欄位, 除規格說明中有額外說明, 否則所有欄位在瀏覽狀態: 除能 ; 編輯狀態: 致能

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本區塊</p>

    ![pic][image_fieldbreak1]
    * `(1)欄位名稱`
        * 用途說明
        * 規格說明
            * 依專案語系, 顯示元件多語名稱
    * `(2)料號`
        * 用途說明
        * 規格說明
            * 顯示元件料號
    * `(3)執行條件`
        * 用途說明
        * 規格說明
            * 參照 [操作條件式通則][link_ruledialog1], 回傳並顯示: 條件說明
    * `(4)給值時間點`
        * 用途說明
        * 規格說明
            * 選項: 新增前/修改前/新增存回前/修改存回前
            * 當 表單設計類型不為APP, 新增前 預設勾選
            * 當 表單設計類型=APP, 新增前 預設未勾選, 並隱藏
    * `(5)資料來源`
        * 用途說明
        * 規格說明
            * 單一選項: 系統資訊/登入資訊/固定給值/查表給值/流水編碼/單據編碼
            * 當 表單設計類型=APP, 選項 流水編碼 隱藏
                * `(5)資料來源`=系統資訊/登入資訊/固定給值/查表給值, 則 `(4)給值時間點`新增前, 預設勾選
                * `(5)資料來源`=單據編碼, 則 `(4)給值時間點`新增存回時, 預設勾選

* <p id="fieldbreak2" style="color:blue;font-weight:bold">系統資訊</p>

    ![pic][image_fieldbreak2]
    * `(1)系統資訊`
        * 用途說明
        * 規格說明
            * 當`資料來源`=系統資訊, 則致能, 否則除能
            * 單一選項: 系統日期/系統日期時間/全唯碼
    * `(2)系統日期類別`
        * 用途說明
        * 規格說明
            * 當`(1)系統資訊`=系統日期, 則致能, 否則除能
            * 下拉選項: 系統日期/當月首日/當月末日

* <p id="fieldbreak3" style="color:blue;font-weight:bold">登入資訊</p>

    ![pic][image_fieldbreak3]
    * `(1)登入資訊`
        * 用途說明
        * 規格說明
            * 當`資料來源`=登入資訊, 則致能, 否則除能
            * 單一選項: 使用者帳號/使用者序號/使用者姓名/用戶代號/組織序號/企業代號

* <p id="fieldbreak4" style="color:blue;font-weight:bold">固定給值</p>

    ![pic][image_fieldbreak4]
    * `(1)固定給值`
        * 用途說明
        * 規格說明
            * 當`資料來源`=固定給值, 則致能, 否則除能
            * 單一選項: 固定值/複寫同欄上列內容/表單參數/複製其它表單欄位/運算給值/編輯提示
            * 當 表單設計類型=APP, 選項 複寫同欄上列內容 隱藏
    * `(2)固定值`
        * 用途說明
        * 規格說明
            * 當`(1)固定給值`=固定值, 則致能, 否則除能
            * 自行輸入
    * `(3)複寫同欄上列內容`
        * 用途說明
        * 規格說明
            * 當`(1)固定給值`=複寫同欄上列內容, 則致能, 否則除能
            * 參照 [挑選表單元件通則][link_ruledialog7], 限定: 本表單下的元件, 進行挑選, 回傳: 表單元件
            * 參照 [個資加密提示通則][link_ruleother11]
            * 當 表單設計類型=APP, 隱藏
    * `(4)表單參數`
        * 用途說明
        * 規格說明
            * 當`(1)固定給值`=表單參數, 則致能, 否則除能
            * 下拉選項內容, 至[表單加註_基本設定][link_FormAnnotation]中, 查詢接收參數取得
    * `(5)複製其它表單欄位`
        * 用途說明
        * 規格說明
            * 當`(1)固定給值`=複製其它表單欄位, 則致能, 否則除能
            * 參照 [挑選表單元件通則][link_ruledialog7], 限定: 本表單下的元件, 進行挑選, 回傳: 表單元件
            * 參照 [個資加密提示通則][link_ruleother11]
    * `(6)運算給值`
        * 用途說明
        * 規格說明
            * 當`(1)固定給值`=運算給值, 則致能, 否則除能
            * 參照 [操作運算式通則][link_ruledialog18], 限定: 無查表功能
    * `(7)編輯提示`
        * 用途說明
        * 規格說明
            * 當`(1)固定給值`=編輯提示, 則致能, 否則除能
            * [使用多語詞庫通則][link_ruledialog2], 回傳:多語料號, 顯示:多語詞彙

* <p id="fieldbreak5" style="color:blue;font-weight:bold">查表給值</p>

    ![pic][image_fieldbreak5]
    * `(1)來源資料行`
        * 用途說明
        * 規格說明
            * 當`資料來源`=查表給值, 則致能, 否則除能
            * 參照 [操作條件式通則][link_ruledialog1], 回傳並顯示: 條件說明
    * `(2)來源欄位`
        * 用途說明
        * 規格說明
            * 當`資料來源`=查表給值, 則致能, 否則除能
            * 依`(1)來源資料行`的查表類別=資料表, 則參照 [挑選資料表元件通則][link_ruledialog5], 限定: `(1)來源資料行`的表格料號, 挑選並回傳資料表元件
            * 依`(1)來源資料行`的查表類別=檢視表, 則參照 [挑選檢視表元件通則][link_ruledialog8], 限定: `(1)來源資料行`的表格料號, 挑選並回傳檢視表元件                

* <p id="fieldbreak6" style="color:blue;font-weight:bold">流水編碼</p>

    ![pic][image_fieldbreak6]
    * `(1)英文字母碼數`
        * 用途說明
        * 規格說明
            * 當`資料來源`=流水編碼, 則致能, 否則除能
            * 自行輸入數字 1~9; 輸入後變化`流水編碼格式`欄位
            * 當 表單設計類型=APP, 隱藏
    * `(2)英數字碼數`
        * 用途說明
        * 規格說明
            * 當`資料來源`=流水編碼, 則致能, 否則除能
            * 自行輸入數字 1~9; 輸入後變化`流水編碼格式`欄位
            * 當 表單設計類型=APP, 隱藏
    * `(3)數字碼數`
        * 用途說明
        * 規格說明
            * 當`資料來源`=流水編碼, 則致能, 否則除能
            * 自行輸入數字 1~9; 輸入後變化`流水編碼格式`欄位
            * 當 表單設計類型=APP, 隱藏
    * `(4)流水編碼格式`
        * 用途說明
        * 規格說明
            * 當`資料來源`=流水編碼, 則致能, 否則除能
            * 無條件唯讀, 由`(1)英文字母碼數`、`(2)英數字碼數`、`(3)數字碼數`更新顯示
                * 顯示內容 (A) * `(1)英文字母碼數` + (Z) * `(2)英數字碼數` + (9) * `(3)數字碼數`
                * 例: `(1)英文字母碼數`=1, `(2)英數字碼數`=2, `(3)數字碼數`=5 → "AZZ99999"
            * 當 表單設計類型=APP, 隱藏
    * `(5)重顯流水號`
        * 用途說明
        * 規格說明
            * 當`資料來源`=流水編碼, 則致能, 否則除能
            * 當 表單設計類型=APP, 隱藏
    * `(6)執行條件`
        * 用途說明
        * 規格說明
            * 當`資料來源`=流水編碼, 則致能, 否則除能
            * 參照 [操作條件式通則][link_ruledialog1], 限定: 對應檔區的資料來源表格, 回傳並顯示: 條件說明
            * 當 表單設計類型=APP, 隱藏

* <p id="fieldbreak7" style="color:blue;font-weight:bold">單據編碼</p>

    ![pic][image_fieldbreak7]
    * `(1)單據編碼`
        * 用途說明
        * 規格說明
            * 當 表單設計類型不為APP, 標題名稱顯示 "單據編碼"; 當 表單設計類型=APP, 標題名稱顯示 "存回編碼"
    * `(2)單據編碼格式`
        * 用途說明
        * 規格說明
            * 當`資料來源`=單據編碼, 則致能, 否則除能
            * 顯示`(6)編碼組合表格`中, 組合的內容
            * 無條件唯讀
    * `(3)直接跳號`
        * 用途說明
        * 規格說明
            * 當`資料來源`=單據編碼, 則致能, 否則除能
            * [基本][link_fieldbreak1]`給值時間點`新增前為勾選, 則除能, 並預設勾選
    * `(4)日期基礎`
        * 用途說明
        * 規格說明
            * 當`資料來源`=單據編碼, 則致能, 否則除能
            * 單一選項: 選項 無關/系統日期/日期元件, 預設 無關
    * `(5)日期元件`
        * 用途說明
        * 規格說明
            * 當`(4)日期基礎`=日期元件, 則致能, 否則除能
            * 下拉查詢本單元件, 限定: 本表單下的元件、資料模版=日期格式, 進行挑選
            * 參照 [個資加密提示通則][link_ruleother11]
    * `(6)編碼組合表格`
        * 用途說明
        * 規格說明
            * 當`資料來源`=單據編碼, 則致能, 否則除能
            * 參照 [操作表格記錄通則][link_rulebutton3]
    * `(7)編碼組合序號`
        * 用途說明
        * 規格說明
            * 當`資料來源`=單據編碼, 則致能, 否則除能
            * 依序給流水號
    * `(8)區段碼類別`
        * 用途說明
        * 規格說明
            * 當`資料來源`=單據編碼, 則致能, 否則除能
            * 下拉選項: 固定值/表單欄位/流水號/年度/月份/日期/週次
            * 當`(4)日期基礎`=無關, 選項 年度/月份/日期/週次 隱藏
    * `(9)內容`
        * 用途說明
        * 規格說明
            * 當`資料來源`=單據編碼, 則致能, 否則除能
            * 當`(8)區段碼類別`=固定值
                * 自行輸入, 並計算內容長度給`(10)編碼長度`
                * 輸入後, 依輸入內容, 影響`(2)單據編碼格式`
            * 當`(8)區段碼類別`=表單欄位
                * 下拉查詢本單元件, 限定: 本表單下的元件, 進行挑選
                * 代碼:K * `(10)編碼長度`, 影響`(2)單據編碼格式`
                * 參照 [個資加密提示通則][link_ruleother11]
            * 當`(8)區段碼類別`=流水號
                * 下拉選項 0~9/0~9 + A~Z/0~9 + A~Z(不含I、O、Z)/A~Z
                * 代碼:9 * `(10)編碼長度`, 影響`(2)單據編碼格式`
            * 當`(8)區段碼類別`=年度
                * 下拉選項 YYYY/YY/CCC
                * `(9)內容`=YYYY, `(10)編碼長度`給值4
                * `(9)內容`=YY, `(10)編碼長度`給值2
                * `(9)內容`=CCC, `(10)編碼長度`給值3
                * 依輸入內容, 影響`(2)單據編碼格式`
            * 當`(8)區段碼類別`=月份
                * 下拉選項 MM/M
                * `(9)內容`=MM, `(10)編碼長度`給值2
                * `(9)內容`=M, `(10)編碼長度`給值1
                * 依輸入內容, 影響`(2)單據編碼格式`
            * 當`(8)區段碼類別`=日期
                * 清空, `(10)編碼長度`給值2
                * 代碼:D * `(10)編碼長度`, 影響`(2)單據編碼格式`
            * 當`(8)區段碼類別`=週次 
                * 清空, `(10)編碼長度`給值2
                * 代碼:W * `(10)編碼長度`, 影響`(2)單據編碼格式`
    * `(10)編碼長度`
        * 用途說明
        * 規格說明
            * 當`資料來源`=單據編碼, 則致能, 否則除能
            * 當`(9)內容`=固定值/年度/月份/日期/週別 則除能
            * 輸入後, 影響 `(2)單據編碼格式`
            * 檢控編碼組合後的長度若超過[元件加註_基本設定][link_ObjectAnnotation]中`欄位資料長度`, 則顯示訊息盒【標題: 系統訊息 / 編碼格式的長度，不可超過基本資料裡的對應欄位長度 / 按鍵:確定】
                * 確定: 關閉訊息盒
    * `(11)延伸編碼表格`
        * 用途說明
        * 規格說明
            * 當`資料來源`=單據編碼, 則致能, 否則除能
            * 參照 [操作表格記錄通則][link_rulebutton3]
    * `(12)延伸編碼序號`
        * 用途說明
        * 規格說明
            * 當`資料來源`=單據編碼, 則致能, 否則除能
            * 依序給流水號
    * `(12)表單欄位`
        * 用途說明
        * 規格說明
            * 當`資料來源`=單據編碼, 則致能, 否則除能
            * 參照 [挑選表單元件通則][link_ruledialog7], 限定: 本表單下的元件, 進行挑選, 回傳: 表單元件
            * 參照 [個資加密提示通則][link_ruleother11]

## <div id="save-action">儲存檢控</div>
* 不允空白檢控, 規則參照 [存回不允空白檢控通則][link_ruleother7]
    * [系統資訊][link_fieldbreak2]
        * 當`資料來源`=系統資訊, 則`系統資訊`必擇一
        * 當`系統資訊`=系統日期, 則`系統日期類別` 不允空白
    * [登入資訊][link_fieldbreak3]
        * 當`資料來源`=登入資訊, 則`登入資訊`必擇一
    * [固定給值][link_fieldbreak4]
        * 當`資料來源`=固定給值, 則`固定給值`必擇一
        * 當`固定給值`=固定值, 則`固定值` 不允空白
        * 當`固定給值`=複寫同欄上列內容, 則`複寫同欄上列內容` 不允空白
        * 當`固定給值`=表單參數, 則`表單參數` 不允空白
        * 當`固定給值`=複寫其它表單欄位, 則`複寫其它表單欄位` 不允空白
        * 當`固定給值`=運算給值, 則`運算給值` 不允空白
        * 當`固定給值`=編輯提示, 則`編輯提示` 不允空白
    * [查表給值][link_fieldbreak5]
        * `來源資料行`、`來源欄位` 不允空白
    * [流水編號][link_fieldbreak6]
        * `流水編碼格式` 不允空白
    * [單據編號][link_fieldbreak7]
        * `單據編碼格式` 不允空白
        * 當`日期基礎`=日期元件, 則`日期元件` 不允空白
        * 當`編碼組合表格`有記錄時, `區段碼類別`、`編碼長度` 不允空白
        * 當`區段碼類別`=固定值/表單欄位/流水號/年度/月份, `內容` 不允空白
        * 當`延伸編碼表格`有記錄時, `表單欄位` 不允空白

* 以下欄位符合條件時, 顯示訊息盒, 顯示規則參照 [存回其它檢控通則][link_ruleother8]
    * [基本][link_fieldbreak1]
        * 當 表單設計類型不為APP, `給值時間點`至少有一項為勾選
    * [單據編號][link_fieldbreak7]
        * `單據編碼格式`內容長度, 必須小於等於[元件加註_基本設定][link_ObjectAnnotation]中`欄位資料長度`
        * 必須設定至少一碼流水號

## <div id="other-desc">其它</div>
* [MAE加註儲存通則][link_ruleother5]

<!-- 圖片 -->
[image_OAInitial_STD]:attachment/OAInitial_STD.png
[image_OAInitial_MAE]:attachment/OAInitial_MAE.png
[image_fieldbreak1]:attachment/OAInitial_fieldbreak1.png
[image_fieldbreak2]:attachment/OAInitial_fieldbreak2.png
[image_fieldbreak3]:attachment/OAInitial_fieldbreak3.png
[image_fieldbreak4]:attachment/OAInitial_fieldbreak4.png
[image_fieldbreak5]:attachment/OAInitial_fieldbreak5.png
[image_fieldbreak6]:attachment/OAInitial_fieldbreak6.png
[image_fieldbreak7]:attachment/OAInitial_fieldbreak7.png

<!-- 超連結 -->
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_rulebutton2]:../RulesButton/README#rulebutton2 "共用通則_按鍵操作/單據異動資料按鍵操作通則"
[link_rulebutton3]:../RulesButton/README#rulebutton3 "共用通則_按鍵操作/操作表格記錄通則"
[link_ruledialog1]:../RulesDialog/README#ruledialog1 "共用通則_開啟單據/操作條件式通則"
[link_ruledialog7]:../RulesDialog/README#ruledialog7 "共用通則_開啟單據/挑選表單元件通則"
[link_ruleother11]:../RulesOther/README#ruleother11 "共用通則_其它/個資加密提示通則"
[link_FormAnnotation]:../FormAnnotation/README "表單加註_基本設定"
[link_ruledialog18]:../RulesDialog/README#ruledialog18 "共用通則_開啟單據/操作運算式通則"
[link_ruledialog2]:../RulesDialog/README#ruledialog2 "共用通則_開啟單據/使用多語詞庫通則"
[link_ruledialog5]:../RulesDialog/README#ruledialog5 "共用通則_開啟單據/挑選資料表元件通則"
[link_ruledialog8]:../RulesDialog/README#ruledialog8 "共用通則_開啟單據/挑選檢視表元件通則"
[link_fieldbreak1]:#fieldbreak1 "欄位說明/基本"
[link_fieldbreak2]:#fieldbreak2 "欄位說明/系統資訊"
[link_fieldbreak3]:#fieldbreak3 "欄位說明/登入資訊"
[link_fieldbreak4]:#fieldbreak4 "欄位說明/固定給值"
[link_fieldbreak5]:#fieldbreak5 "欄位說明/查表給值"
[link_fieldbreak6]:#fieldbreak6 "欄位說明/流水編碼"
[link_fieldbreak7]:#fieldbreak7 "欄位說明/單據編碼"
[link_ruleother5]:../RulesOther/README#ruleother5 "共用通則_其它/MAE加註儲存通則"
[link_ruleother7]:../RulesOther/README#ruleother7 "共用通則_其它/存回不允空白檢控通則"
[link_ruleother8]:../RulesOther/README#ruleother8 "共用通則_其它/存回其它檢控通則"
[link_ObjectAnnotation]:../ObjectAnnotation/README "元件加註_基本設定"