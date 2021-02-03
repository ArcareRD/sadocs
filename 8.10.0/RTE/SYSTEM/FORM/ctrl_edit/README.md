## <div id="layout-std">STD表單 <path>(版面相關)</path></div>
* 元件位置寬高				
    * X軸 : (px)			
    * Y軸 : (px)			
    * 寬度 : (px)			
    * 高度 : (px)			
* 標題 : [STD_標題]
* 套用樣式				
    * <div id="">不在<rte>多筆表格</rte></div>

        * 支援狀態 : [( [表單設計類型] = [STD表單] 且 [元件類型代碼] = [wTF] 且 [僅供顯示] = [N] )]()
        * 支援狀態 : [( [表單設計類型] = [STD表單] 且 [元件類型代碼] = [wPW] 且 [僅供顯示] = [N] )]()
        * 元件構成

            <div class="ctrl_margin" style="position:relative;box-sizing:border-box;padding:30px;border:1px #ffffff dotted;width:90%;height:360px;">
                <div class="ctrl" style="display:inline-flex;position:relative;box-sizing:border-box;padding:30px;border:1px #FFAC55 dotted;background-color:#add8e6;width:100%;height:100%;">
                    <div style="position:absolute;top:2px;left:2px;">元件</div>
                    <div class="ctrl_title" style="position:relative;box-sizing:border-box;padding:2px;border:1px #808080 dotted;width:30%;height:100%;">標題區
                    </div>
                    <div class="ctrl_ctt" style="position:relative;box-sizing:border-box;margin-left:5%;padding:30px;border:1px #808080 dotted;width:65%;height:100%;">
                        <div style="position:absolute;top:2px;left:2px;">內容區</div>
                        <div class="ctrl_border" style="position:relative;box-sizing:border-box;padding:30px;border:2px #808080 solid;width:100%;height:100%;">
                            <div style="position:absolute;top:2px;left:2px;color:#ff7f50;">框線</div>
                            <div class="ctrl_padding" style="position:relative;box-sizing:border-box;padding:30px;border:1px #808080 dotted;width:100%;height:100%;">
                            <div style="position:absolute;top:2px;left:2px;color:#ff7f50;">內間距 / 底色</div>
                                <div class="ctrl_ctt" style="position:relative;box-sizing:border-box;padding:2px;border:1px #808080 dotted;width:100%;height:100%;color:#ff7f50;">內容
                                </div>                   
                            </div>            
                        </div>
                    </div>
                </div>
            </div>
            註.以 [ 標題位置:左 ] 為例

    * <div id="">在<rte>多筆表格</rte></div>

        * 支援狀態 :  ( [表單設計類型] = [STD表單] 且 [元件類型代碼] = [text] 且 [僅供顯示] = [N] ) 		
        * 支援狀態 :  ( [表單設計類型] = [STD表單] 且 [元件類型代碼] = [popupwindow] 且 [僅供顯示] = [N] )
        * 元件構成

            <div class="ctrl_margin" style="position:relative;box-sizing:border-box;padding:30px;border:1px #ffffff dotted;width:90%;height:360px;">
                <div class="ctrl" style="display:inline-flex;position:relative;box-sizing:border-box;padding:30px;border:1px #FFAC55 dotted;background-color:#add8e6;width:100%;height:100%;">
                    <div style="position:absolute;top:2px;left:2px;">元件</div>
                    <div class="ctrl_ctt" style="position:relative;box-sizing:border-box;padding:30px;border:1px #808080 dotted;width:100%;height:100%;">
                        <div style="position:absolute;top:2px;left:2px;">內容區</div>
                        <div class="ctrl_border" style="position:relative;box-sizing:border-box;padding:30px;border:2px #808080 solid;width:100%;height:100%;">
                            <div style="position:absolute;top:2px;left:2px;color:#ff7f50;">框線</div>
                            <div class="ctrl_padding" style="position:relative;box-sizing:border-box;padding:30px;border:1px #808080 dotted;width:100%;height:100%;">
                            <div style="position:absolute;top:2px;left:2px;color:#ff7f50;">內間距 / 底色</div>
                                <div class="ctrl_ctt" style="position:relative;box-sizing:border-box;padding:2px;border:1px #808080 dotted;width:100%;height:100%;color:#ff7f50;">內容
                                </div>                   
                            </div>            
                        </div>
                    </div>
                </div>
            </div>

## <div id="layout-rwd">RWD表單 <path>(版面相關)</path></div>
* 切版 : 不支援	
* 元件寬高
    * 高度 : (px)
        * 當變動高度=是時，表示最小高度
		* 不含<外邊距>的上邊距 / 下邊距 : (DKS_單元樣式_外邊距_上邊距 / 下邊距)													
    * 變動高度 : 是 / 否
        * 當變動高度=否時
            * 編輯狀態下
                * 內容永遠為一行
                * 元件高度不足 : [RWD_元件高度不足]
            * 瀏覽狀態下
                * 內容超出顯示… : [RWD_內容超出顯示…]
                * 元件高度不足 : [RWD_元件高度不足]
            * ex1.寬度:50% / 高度:25 / 變動高度:否 / 標題位置:左 / 標題寬度:30% 標題:文字方塊

                ![文字方塊_RWD表單_固定高度ex]

        * 當變動高度=是時
            * 元件可能因<標題區>或<內容區>撐高，但會有最小高度
            * 編輯狀態下
                * 內容永遠為一行
            * 瀏覽狀態下
                * 內容超出折行 : [RWD_內容超出折行]
            * ex1.寬度:50% / 高度:25 / 變動高度:是 / 標題位置:左 / 標題寬度:30% 標題:文字方塊

                ![文字方塊_RWD表單_變動高度ex]

    * 寬度 : (%)														
        * 不含<外邊距>的左邊距 / 右邊距 : (DKS_單元樣式_外邊距_左邊距 / 右邊距)

    > 當瀏覽器視窗的大小改變時，可能導致元件寬高會改變														
* [標題](../common/README.md#rwd-ctrl-title)
* 套用樣式			#文字方塊_組成_RWD表單
    * 支援狀態 :  ( [表單設計類型] = [RWD表單] 且 [元件類型代碼] = [wTF] 且 [僅供顯示] = [N] )
    * 支援狀態 :  ( [表單設計類型] = [RWD表單] 且 [元件類型代碼] = [wPW] 且 [僅供顯示] = [N] ) 									
    * 元件構成

        <div class="ctrl_margin" style="position:relative;box-sizing:border-box;padding:30px;border:1px #808080 dotted;width:90%;height:360px;">
            <div style="position:absolute;top:2px;left:2px;color:#ff7f50;">外邊距</div>
            <div class="ctrl" style="display:inline-flex;position:relative;box-sizing:border-box;padding:30px;border:1px #FFAC55 dotted;background-color:#add8e6;width:100%;height:100%;">
                <div style="position:absolute;top:2px;left:2px;">元件</div>
                <div class="ctrl_title" style="position:relative;box-sizing:border-box;padding:2px;border:1px #808080 dotted;width:30%;height:100%;">標題區
                </div>
                <div class="ctrl_ctt" style="position:relative;box-sizing:border-box;margin-left:5%;padding:30px;border:1px #808080 dotted;width:65%;height:100%;">
                    <div style="position:absolute;top:2px;left:2px;">內容區</div>
                    <div class="ctrl_border" style="position:relative;box-sizing:border-box;padding:30px;border:2px #808080 solid;width:100%;height:100%;">
                        <div style="position:absolute;top:2px;left:2px;color:#ff7f50;">框線</div>
                        <div class="ctrl_padding" style="position:relative;box-sizing:border-box;padding:30px;border:1px #808080 dotted;width:100%;height:100%;">
                        <div style="position:absolute;top:2px;left:2px;color:#ff7f50;">內間距 / 底色</div>
                            <div class="ctrl_ctt" style="position:relative;box-sizing:border-box;padding:2px;border:1px #808080 dotted;width:100%;height:100%;color:#ff7f50;">內容
                            </div>                   
                        </div>            
                    </div>
                </div>
            </div>
        </div>
        註.以 [ 標題位置:左 ] 為例

## <div id="behavior-protect">受權限保護元件 <path>(行為)</path></div>
* 內容區會顯示(***)的字樣(#7477)
* 無法駐留

## <div id="behavior-alias">對應檔區 <path>(行為)</path></div>
* IDE : 元件加註_基本設定_存在檔區

## <div id="behavior-field">對應欄位 <path>(行為)</path></div>
* IDE : 元件加註_基本設定_檢視表對應欄位
* 支援欄位型態
    * 文字
    * 整數
    * 數字
    * 日期
    * 日期時間
    * 全唯碼
    * 備註

<test>測試</test> 支援的欄位型態都要測試(除了全唯碼外)

## <div id="behavior-show">顯示巨集 <path>(行為)</path></div>
* IDE
    * `元件` \ `顯示設定` \ `內容處理` \ `固定值`
    * `元件` \ `顯示設定` \ `內容處理` \ `欄位組合`
* 支援<rte>欄位型態</rte>
    * <rte>文字</rte>
    * <rte>整數</rte>
    * <rte>數字</rte>
    * <rte>日期</rte>
    * <rte>日期時間</rte>
    * <rte>全唯碼</rte>
    * <rte>備註</rte>

<test>測試</test> 支援的欄位型態都要測試(除了全唯碼外)

## <div id="behavior-format">模版 <path>(行為)</path></div>    
* IDE : 元件加註_基本設定_資料模版

## <div id="behavior-hint">提示 <path>(行為)</path></div>    
* IDE : 元件加註_基本設定_欄位提示訊息

## <div id="behavior-filter">資料過濾 <path>(行為)</path></div>    
* 過濾來源 : 對應欄位

## <div id="behavior-find">資料搜尋 <path>(行為)</path></div>    
* 資料搜尋 : 對應欄位

## <div id="behavior-query">查詢視窗 <path>(行為)</path></div>
* 當元件唯讀時，無法開啟 : (DKS_資料元件_編輯能力_可編欄位_唯讀)
* 當元件勿駐時，無法開啟 : (DKS_資料元件_編輯能力_可編欄位_勿駐)
* 類型
    * 開窗參照 : (DKS_表單元件_開窗參照_視窗內容<>檔案總管)

        * 規格 : [元件加註_開窗參照]

    * 當沒有開窗參照 且 模版 = 日期模版 / 日期時間模版 / 時間
        * <div>日期、日期時間、時間選擇器(#7796異動)</div>

            * 選擇器種類
                * 若模版=日期模版

                    ![文字方塊_RWD表單_日期選擇器] 註.以RWD表單示意。

                * 若模版=日期時間模版 (時間=HH:MM)    

                    ![文字方塊_RWD表單_日期時間選擇器(HHMM)] 註.以RWD表單示意。

                * 若模版=日期時間模版 (時間=HH:MM:SS)

                    ![文字方塊_RWD表單_日期時間選擇器(HHMMSS)] 註.以RWD表單示意。

                * 若模版=時間模版(HH:MM)

                    ![文字方塊_RWD表單_時間選擇器(HHMM)] 註.以RWD表單示意。

                * 若模版=時間模版(HH:MM:SS)

                    ![文字方塊_RWD表單_時間選擇器(HHMMSS)] 註.以RWD表單示意。

            * 選擇器規則
                * 選擇器出現的位置 : 元件<內容區>下方，靠左顯示。但若右邊沒位置顯示不下時，改靠右顯示。
                    * 靠左顯示
                
                        ![文字方塊_RWD表單_選擇器_靠左顯示] 註.以RWD表單示意。

                    * 靠右顯示
                
                        ![文字方塊_RWD表單_選擇器_靠右顯示] 註.以RWD表單示意。

            * 開啟預設帶入<輸入內容>。若輸入內容為空白時，會給預設日期時間。
            * 預設日期 : 日期會標示為[綠底白字]。
            * 今日 : 日期會標示為[灰底藍字]。
            * [年度]的[左右鍵] : 至上年 / 至下年。
            * [月份]的[左右鍵] : 至上月 / 至下月。
            * [時間]的[上下鍵] : 至上一秒 / 至下一秒。
            * 帶回
                * 按右上角的 ^ 鈕
                * 點擊日期
                * F5
            * PC鍵盤操作
                * ESC : 關閉選擇器。
                * F5 : 帶回。


[STD_標題]:../common/README.md#std-ctrl-title "STD_標題"
[RWD_元件高度不足]:../common/README.md#rwd-ctrl-height-notenough "RWD_元件高度不足"
[RWD_內容超出顯示…]:../common/README.md#rwd-ctrl-overflow-ellipsis "RWD_內容超出顯示…"
[RWD_元件高度不足]:../common/README.md#rwd-ctrl-height-notenough "RWD_元件高度不足"
[文字方塊_RWD表單_固定高度ex]:attachment/rwd_fixheight_ex1.png "文字方塊_RWD表單_固定高度ex"
[RWD_內容超出折行]:../common/README.md#rwd-ctrl-overflow-break "RWD_內容超出折行"
[文字方塊_RWD表單_變動高度ex]:attachment/rwd_dynamicheight_ex1.png "文字方塊_RWD表單_變動高度ex"
[文字方塊_RWD表單_日期選擇器]:attachment/rwd_datePicker.png "文字方塊_RWD表單_日期選擇器"
[文字方塊_RWD表單_日期時間選擇器(HHMM)]:attachment/rwd_datetimePicker_hhmm.png "文字方塊_RWD表單_日期時間選擇器(HHMM)"
[文字方塊_RWD表單_日期時間選擇器(HHMMSS)]:attachment/rwd_datetimePicker_hhmmss.png "文字方塊_RWD表單_日期時間選擇器(HHMMSS)"
[文字方塊_RWD表單_時間選擇器(HHMM)]:attachment/rwd_timePicker_hhmm.png "文字方塊_RWD表單_時間選擇器(HHMM)"
[文字方塊_RWD表單_時間選擇器(HHMMSS)]:attachment/rwd_timePicker_hhmmss.png "文字方塊_RWD表單_時間選擇器(HHMMSS)"
[文字方塊_RWD表單_選擇器_靠左顯示]:attachment/rwd_picker_align_left.png "文字方塊_RWD表單_選擇器_靠左顯示"
[文字方塊_RWD表單_選擇器_靠右顯示]:attachment/rwd_picker_align_right.png "文字方塊_RWD表單_選擇器_靠右顯示"
[元件加註_開窗參照]:../../../IDE/FORM/OAPopup/README.md "元件加註_開窗參照"