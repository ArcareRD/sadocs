### <div id="view">畫面說明</div>

![表單畫面]

* 本單主要在定義各項流程的程序及內容

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * <ps>待補</ps>


* <p id="fieldbreak1" style="color:blue;font-weight:bold">簽核人員</p>

* ![pic][image_signoff_flow_setting_user]
    * 欄位.項次
        * 依序取得流水編碼: 2碼
    * 欄位.簽核類別
        * 下拉選項: 會簽 / 知會 / 會辦
    * 欄位.簽核對象
        * 當`簽核類別`=會簽 且 `流程類型`=組織編制，下拉選項: 單位主管 / 上階主管 / 指定單位 / 特定對象 
        * 當`簽核類別`=會簽 且 `流程類型`=專案編制，下拉選項: 編制主管 / 上階主管 / 指定單位 / 特定對象 
        * 當`簽核類別`=知會 或 會辦，下拉選項: 指定單位 / 特定對象
        * 當`簽核對象`<>指定單位，清空指定單位
        * 當`簽核對象`<>特定對象，清空特定對象
    * 欄位.指定單位
        * 當`簽核對象`<>指定單位，則 本欄勿駐
        * 開啟<簽核組織單位清單>，挑選組織單位，顯示: 組織單位簡稱
        * 檢控: 可自行輸入的組織單位代號，若代號不存在，顯示訊息: ※輸入錯誤※ 組織單位代號不存在!        
    * 欄位.單位窗口
        * 當`簽核對象`<>指定單位，則 本欄勿駐
        * 下拉選項: 單位主管 / 交辦窗口
    * 欄位.特定對象
        * 當`簽核對象`<>特定對象，則 本欄勿駐
        * 開啟<簽核人員設定>，挑選簽核人員，顯示: 人員姓名
        * 檢控: 可自行輸入的人員代號，若代號不存在，顯示訊息: ※輸入錯誤※ 人員代號不存在!        
    * 欄位.摘要說明
        * 自行輸入

* <p id="fieldbreak1" style="color:blue;font-weight:bold">簽核通知</p>

* ![pic][image_signoff_flow_setting_notice]

    * 欄位.受文者附件按鈕選項
        * 核取選項: 附件夾檔、插入物件
    * 欄位.附件夾檔
        * 預設: 未勾選
    * 欄位.插入物件 
        * 預設: 未勾選
    * 欄位.發文者郵件_核取選項
        * 預設: 未勾選
    * 欄位.發文者郵件_內容
        * 使用郵件模版(編輯器)
        * `發文者郵件_核取選項` 未勾選，則 本欄勿駐
    * 欄位.簽核者郵件_核取選項
        * 預設: 勾選
        * 本欄勿駐
    * 欄位.簽核者郵件_內容
        * 使用郵件模版(編輯器)
    * 欄位.知會者郵件_核取選項
        * 預設: 勾選
    * 欄位.簽核者




### <div id="action">動作流程</div>
* <ps>待補</ps>


[表單畫面]:attachment/signoff_flow_setting.png "表單畫面"
[image_signoff_flow_setting_user]:attachment/signoff_flow_setting_user.png "簽核人員"
[image_signoff_flow_setting_notice]:attachment/signoff_flow_setting_notice.png "簽核通知"
