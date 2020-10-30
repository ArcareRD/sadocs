# 樹元件

## <div id="layout-std">版面相關_STD表單(傳統表單)</div>
* 元件位置寬高				
    * X軸 : (px)			
    * Y軸 : (px)			
    * 寬度 : (px)			
    * 高度 : (px)			
* [標題](../common/README.md#std-ctrl_title)
* 套用樣式				
    * 支援狀態 : [( [表單設計類型] = [傳統表單] 且 [元件類型代碼] = [wTree] )]()
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

    * 光棒 : <駐留節點>會套上光棒樣式        
        * 駐留樣式

            ![](attachment/lightbar_stype_focus.png)
        * 未駐留樣式            

            ![](attachment/lightbar_stype_enable.png)        

## <div id="behavior-alias">對應檔區</div>
* IDE : 元件加註_基本設定_存在檔區

## <div id="behavior-field">對應欄位</div>
* IDE : 元件加註_基本設定_檢視表對應欄位
* 可不設
* 用途 : 節點顯示的內容。
* 支援欄位型態
    * 文字

## <div id="behavior-show">顯示巨集</div>
* IDE
    * 元件加註_顯示設定_內容處理_欄位組合
    * 元件加註_樹狀控制_指定顯示
* 用途 : 節點顯示的內容。
* 支援欄位型態
    * 文字

## <div id="behavior-hint">提示</div>
* IDE : 元件加註_基本設定_欄位提示訊息

## <div id="behavior-browse">瀏覽模式</div>
* 樣式
    * 呈現
        * 無checkbox / 無節點圖示

            ![](attachment/browse_style_base.png)

        * 有checkbox

            ![](attachment/browse_style_checkbox.png)

        * 有checkbox / 有節點圖示

            ![](attachment/browse_style_checkbox_icon.png)

    * checkbox
        * IDE : 元件加註_樹狀控制_資料控制_致能勾選
        * 圖示

            ![](attachment/checkbox_enable_x.png) 致能，未勾選

            ![](attachment/checkbox_enable_v.png) 致能，已勾選

            ![](attachment/checkbox_disable_x.png) 除能，未勾選

            ![](attachment/checkbox_disable_v.png) 除能，已勾選
        * 致能條件
            * IDE
                * 元件加註_樹狀控制_資料控制_致能勾選_限制條件
    * <div id="icon">節點圖示</div>
        * IDE 
            * 元件加註_樹狀控制_外觀_節點圖示
        * 每組2個圖示(未駐留圖示,駐留圖示)。每個圖示寬高固定為w19 * h23。
        * 第一組固定為根節點使用。

        * ex1.

            ![](attachment/node_icon_ex1.png)