流程表單
===
## 版面相關
* 版面</br>
    ![pic][image_flowForm]
    * [版面資訊通則][link_ruleother1]

## 動作說明
* 以Dailog on Top 的方式開啟

## 欄位設定
* <p id="fieldbreak1" style="color:blue;">基本</p>

    ![pic][image_fieldbreak1]
    * `(1)傳統/RWD表單`
        * 用途說明
        * 規格說明
            * 依專案多語顯示表單名稱
            * 不須輸入, 唯讀
    * `(2)傳統/RWD表單開窗`
        * 用途說明
        * 規格說明
            * 開窗[單據報表清單][link_ListFormReport], 限定: 挑選非APP表單,  回傳並顯示: 表單名稱
    * `(3)傳統/RWD表單清除`
        * 用途說明
        * 規格說明
            * 清空`(1)傳統/RWD表單`
    * `(4)APP表單名稱`
        * 用途說明
        * 規格說明
            * 依專案多語顯示表單名稱
            * 不須輸入, 唯讀
    * `(5)APP表單開窗`
        * 用途說明
        * 規格說明
            * 開窗[單據清單][link_ListFormReport], 限定: 挑選APP表單,  回傳並顯示: 表單名稱
    * `(6)APP表單清除`
        * 用途說明
        * 規格說明
            * 清空`(4)APP表單名稱`
    * `(7)確定`
        * 用途說明
        * 規格說明
            * 參照[權限驗證通則][link_ruleother6]
            * 寫入資料, 並關閉表單
    * `(8)取消`
        * 用途說明
        * 規格說明
            * 關閉表單

<!-- 圖片 -->
[image_flowForm]:attachment/flowForm.png
[image_fieldbreak1]:attachment/fieldbreak1.png

<!-- 超連結 -->
[link_ListFormReport]:../FlowItem/ListFormReport.md "單據報表清單"
[link_ruleother1]:../RulesOther/README#ruleother1 "共用通則_其它/版面資訊通則"
[link_ruleother6]:../RulesOther/README#ruleother6 "共用通則_其它/權限驗證通則"