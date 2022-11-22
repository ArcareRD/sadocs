### <div id="view">畫面說明</div>

![pic][image_signoffprojectorganize]

## <div id="object-desc">欄位說明</div>
* <p id="fieldbreak1" style="color:blue;font-weight:bold">基本</p>

* ![pic][image_block1]
    * 欄位.專案代號
        * 可自行輸入, 不允重複
    * 欄位.專案名稱
        * 可自行輸入, 不允重複
    * 欄位.開案日期
        * 新增預設 系統日期
    * 欄位.專案目的
        * 可自行輸入
    * 欄位.異動日期
        * 僅供顯示, 新增、修改、存回預設 系統日期時間
    * 欄位.異動人員
        * 僅供顯示, 新增、修改、存回預設 使用者姓名
    * 欄位.樹狀結構
        * 預設 全展
        * 檢控 專案編制類別 不為 02:任務, 才可執行新增子階
    * 欄位.專案編制類別
        * 單選下拉 01:編制/02:任務
        * 有子階節點, 勿駐
    * 欄位.專案編制名稱
        * 可自行輸入
    * 欄位.主管人員代號
        * 顯示 本階節點中 主管否 為勾選的人員代號
    * 欄位.主管姓名
        * 顯示 本階節點中 主管否 為勾選的人員姓名
    * 欄位.項次
        * 依序取得流水編碼: 2碼
    * 欄位.人員代號
        * 開窗[簽核人員清單][link_SignoffUserList], 可複選勾回人員代號、人員姓名
        * 檢控 人員代號須存在[簽核人員清單][link_SignoffUserList]
            * 若不存在則顯示訊息 "※輸入有誤※ 人員代號不存在！"
        * 至[簽核人員清單][link_SignoffUserList], 依所輸入的人員代號取得人員姓名 
    * 欄位.人員姓名
        * 顯示 人員姓名
    * 欄位.主管否
        * 可自行輸入
    * 按鍵.開啟
    * 按鍵.退出
    * 按鍵.新增
    * 按鍵.新增存回
        * 檢控 一個節點下, 須勾選 且 只允存在一筆主管否為勾選的人員
            * 若上述條件不成立, 則顯示訊息 "※執行有誤※ 必須指定單一主管！"
    * 按鍵.修改
    * 按鍵.修改存回
        * 檢控 一個節點下, 須勾選 且 只允存在一筆主管否為勾選的人員
            * 若上述條件不成立, 則顯示訊息 "※執行有誤※ 必須指定單一主管！"
    * 按鍵.刪除

### <div id="action">動作流程</div>
* <ps>待補</ps>

<!-- 圖片 -->
[image_signoffprojectorganize]:attachment/SignoffProjectOrganize.png "表單畫面"
[image_block1]:attachment/SignoffProjectOrganize_block1.png "基本"

<!-- 超連結 -->
[link_SignoffUserList]:../SignoffUserList/README.md "共用通則_其它/版面資訊通則"