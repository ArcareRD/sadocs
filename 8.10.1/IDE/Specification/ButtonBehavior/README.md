## <div id="behavior-layout">版面相關</div>
* 版面
    * STD</br>
        ![pic][image_button_STD]
    * RWD
        * 同STD
    * MAE</br>
        ![pic][image_button_MAE]
* [版面資訊通則][link_ruleother1]

## <div id="behavior-form-action">動作說明</div>
* 依規格定義-主畫面 結構清單駐留按鍵或隱藏按鍵, 執行按鍵.設定，進入本單
* 作業流程
    * ![pic][image_ButtonBehavior_Open]


## <div id="behavior-object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本區塊</p>

    * STD</br>
        ![pic][image_fieldbreak1_STD]
    * MAE</br>
        ![pic][image_fieldbreak1_MAE]
    * `(1)行為選項`    
        * 用途說明
        * 規格說明        
            * 選項:1.基本設定, 預設為true, 除能
            * 依表單設計類型, 決定是否支援行為選項, 請參照下表規則決定畫面結果:
                * 表單設計類型=STD、RWD, 不支援的行為選項, 畫面以除能方式表示
                * 表單設計類型=APP, 不支援的行選項, 畫面以隱藏方式表示
                * ![pic][image_ButtonBehavior_Supper]
    * (2)`儲存`
        * 用途說明
        * 規格說明
            * 若駐留功能按鈕, 不存在行為選項:1.基本設定, 系統自動新增該行為選項
            * 依駐留功能按鈕, 新增本次選取的行為選項
        * 作業流程
            * ![pic][image_ButtonBehavior_Save]
    * (3)`重設`
        * 用途說明
        * 規格說明
            * 除了基本設定, 清除所有行為選項勾項目
        * 作業流程
            * ![pic][image_ButtonBehavior_Reset]                






<!-- 圖片 -->
[image_button_STD]:attachment/ButtonBehavior_STD.png
[image_button_MAE]:attachment/ButtonBehavior_MAE.png
[image_fieldbreak1_STD]:attachment/ButtonBehavior_MAE_block1.png
[image_fieldbreak1_MAE]:attachment/ButtonBehavior_STD_block1.png
[image_ButtonBehavior_Supper]:attachment/ButtonBehavior_Supper.png
[image_ButtonBehavior_Save]:attachment/ButtonBehavior-Save.png
[image_ButtonBehavior_Reset]:attachment/ButtonBehavior-Reset.png
[image_ButtonBehavior_Open]:attachment/ButtonBehavior-Open.png


<!-- 超連結 -->
[link_ruleother1]:/8.10.0/IDE/Specification/RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"