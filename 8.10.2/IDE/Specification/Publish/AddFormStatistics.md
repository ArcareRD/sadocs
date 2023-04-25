## <div id="layout">版面相關</div>
* 版面
    * ![pic][image_AddFormStatistics]
* [版面資訊通則][link_ruleother1]
		
## <div id="form-action">動作說明</div>
* 由[版本發行][link_Publish]的`新增統計`, 點擊超連結進入本單, 顯示本版本已打樣或已發行的表單/報表明細及統計數量
* 依`表報類別`及`新增日期`降冪排列

## <div id="object-desc">欄位說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

    * ![pic][image_AddFormStatistics_block1]
    * `(1)新增表單數`
        * 用途說明
        * 規格說明
            * 顯示本版本新增的表單總數
    * `(2)新增報表數`
        * 用途說明
        * 規格說明
            * 顯示本版本新增的報表總數
    * `(3)新增總數`
        * 用途說明
        * 規格說明
            * 顯示本版本新增表單/報表總數
    * `(4)表報類別`
        * 用途說明
        * 規格說明
            * 顯示表單/報表
    * `(5)成品料號`
        * 用途說明
        * 規格說明
            * 顯示表單/報表成品料號
    * `(6)表報名稱`
        * 用途說明
        * 規格說明
            * 顯示表單/報表名稱
    * `(7)新增人員`
        * 用途說明
        * 規格說明
            * 顯示本表報新增建立人員
    * `(8)新增日期`
        * 用途說明
        * 規格說明
            * 顯示本表報新增建立日期時間
    * `(9)打樣人員`
        * 用途說明
        * 規格說明
            * 顯示本表報在本版本中最後的打樣人員
    * `(10)打樣日期`
        * 用途說明
        * 規格說明
            * 顯示本表報在本版本中最後打樣日期時間
    * `(11)發行人員`
        * 用途說明
        * 規格說明
            * 顯示本表報在本版本中最後的發行人員
    * `(12)發行日期`
        * 用途說明
        * 規格說明
            * 顯示本表報在本版本中最後發行日期時間

## <div id="other-desc">其它</div>
* 以下模擬寫入本單據的操作記錄
<table>
    <tr style="background-color:#F3F3FA">
        <td colspan="2">操作流程</td>
        <td colspan="5">UI_PublishUseLog(版本發行單據使用記錄)</td>
		<td>說明</td>
		<td colspan="3">UI_MaterialChangeLog(料件變更記錄)</td>
    </tr>
    <tr style="background-color:#F3F3FA">
        <td>單據</td>
		<td>操作</td>
		<td>表報</td>
		<td>版本</td>
		<td>異動類別</td>
		<td>打樣</td>
		<td>發行</td>
		<td>一但產生xml，打樣、發行即成立</td>
		<td>表報</td>
		<td>版本</td>
		<td>狀態</td>
    </tr>
    <tr>
        <td colspan="11">未發行</td>
    </tr>
    <tr>
        <td colspan="11">↓</td>
    </tr>
    <tr>
        <td>A單</td>
		<td>新增 → 刪除</td>
		<td style="text-decoration:line-through;color:grey">A單</td>
		<td style="text-decoration:line-through;color:grey">000000</td>
		<td style="text-decoration:line-through;color:grey">新增</td>
		<td></td>
		<td></td>
		<td>單據未有發行、打樣記錄，故於清單中刪除</td>
		<td style="text-decoration:line-through;color:grey">A單</td>
		<td style="text-decoration:line-through;color:grey">000000</td>
		<td style="text-decoration:line-through;color:grey">新增</td>
    </tr>
    <tr>
        <td>B單</td>
		<td>新增 → 打樣 → 刪除</td>
		<td>B單</td>
		<td>000000</td>
		<td>新增</td>
		<td>V</td>
		<td></td>
		<td>單據打樣後再刪除，則清單保留記錄</td>
		<td style="text-decoration:line-through;color:grey">B單</td>
		<td style="text-decoration:line-through;color:grey">000000</td>
		<td style="text-decoration:line-through;color:grey">新增</td>
    </tr>
    <tr>
        <td>C單</td>
		<td>新增 → 打樣 → 發行</td>
		<td>C單</td>
		<td>000000</td>
		<td>新增</td>
		<td>V</td>
		<td>V</td>
		<td></td>
		<td>C單</td>
		<td>000000</td>
		<td>新增</td>
    </tr>
    <tr>
        <td>D單</td>
		<td>新增 → 發行</td>
		<td>D單</td>
		<td>000000</td>
		<td>新增</td>
		<td></td>
		<td>V</td>
		<td></td>
		<td>D單</td>
		<td>000000</td>
		<td>新增</td>
    </tr>
    <tr>
        <td colspan="11">↓</td>
    </tr>
    <tr>
        <td colspan="11">發行，版本 = 232001，表報新增數量 = 3</td>
    </tr>
    <tr>
        <td colspan="11">↓</td>
    </tr>
    <tr>
        <td>C單</td>
		<td>刪除</td>
		<td>C單</td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td>C單</td>
		<td>232001</td>
		<td>刪除</td>
    </tr>
    <tr>
        <td>D單</td>
		<td>修改 → 發行</td>
		<td>D單</td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
		<td>D單</td>
		<td>232001</td>
		<td>修改</td>
    </tr>
    <tr>
        <td>E單</td>
		<td>新增 → 刪除</td>
		<td style="text-decoration:line-through;color:grey">E單</td>
		<td style="text-decoration:line-through;color:grey">232001</td>
		<td style="text-decoration:line-through;color:grey">新增</td>
		<td></td>
		<td></td>
		<td>單據未有發行、打樣記錄，故於清單中刪除</td>
		<td style="text-decoration:line-through;color:grey">E單</td>
		<td style="text-decoration:line-through;color:grey">232001</td>
		<td style="text-decoration:line-through;color:grey">新增</td>
    </tr>
    <tr>
        <td>F單</td>
		<td>新增 → 打樣 → 刪除</td>
		<td>F單</td>
		<td>232001</td>
		<td>新增</td>
		<td>V</td>
		<td></td>
		<td>單據打樣後再刪除，則清單保留記錄</td>
		<td style="text-decoration:line-through;color:grey">F單</td>
		<td style="text-decoration:line-through;color:grey">232001</td>
		<td style="text-decoration:line-through;color:grey">新增</td>
    </tr>
    <tr>
        <td>G單</td>
		<td>新增 → 打樣 → 發行</td>
		<td>G單</td>
		<td>232001</td>
		<td>新增</td>
		<td>V</td>
		<td>V</td>
		<td></td>
		<td>G單</td>
		<td>232001</td>
		<td>新增</td>
    </tr>
    <tr>
        <td>H單</td>
		<td>新增 → 發行</td>
		<td>H單</td>
		<td>232001</td>
		<td>新增</td>
		<td></td>
		<td>V</td>
		<td></td>
		<td>H單</td>
		<td>232001</td>
		<td>新增</td>
    </tr>
    <tr>
        <td colspan="11">↓</td>
    </tr>
    <tr>
        <td colspan="11">發行，版本 = 235001，表報新增數量 = 3</td>
    </tr>
</table>


<!-- 圖片 -->
[image_AddFormStatistics]:attachment/AddFormStatistics.png
[image_AddFormStatistics_block1]:attachment/AddFormStatistics_block1.png

<!-- 超連結 -->
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_Publish]:README "版本發行"