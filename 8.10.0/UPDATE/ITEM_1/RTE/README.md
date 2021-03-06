### <div id="user">規劃人員</div>
* Rita

### <div id="updatedate">規劃日期</div>
* 2020/11/04

### <div id="trac">TRAC</div>
* #8189

### <div id="requirement">需求展開</div>
* 規格說明
    * 主要提供客戶執行資料蒐集，功能以資料蒐集為主、資料查詢為輔，並且協助客戶擴大資料蒐集作業範圍，當使用者超出RTE服務範圍區域時，仍然能完成預定資料蒐集工作。

* 規劃項目展開
    * 系統工具擴充以下項目 :
        * 新增表單.MAE離線管理 : 管理MAE離線。

### <div id="utl_1">表單.MAE離線管理 <path>(需求展開\系統工具)</path></div>
* 擴充
* 規格說明
    * 該表單用來管理下列項目
        * 哪些使用者正在離線狀態。
        * 強制中斷離線使用者不能上傳資料。
        * 哪些使用者正在上傳資料。
        * 等待同步資料。
        * 放棄同步資料。

* 表單畫面
    * 設計類型 : RWD表單
    * 表單種類 : 條件多筆 

    ![表單_MAE離線管理_表單畫面]

* 畫面規格說明

    * 欄位.離線任務名稱 
        * 不可空白
        * 選項清單 : 任務清單

    * 按鈕.過濾

        依條件過濾出符合的資料。

	    * 執行限制
		    * 致能條件 : 欄位.離線任務名稱不可空白。

    * 欄位.離線批號

        離線唯一批號。

    * 欄位.離線使用者

        離線使用者姓名。

    * 欄位.離線日期時間

        開始離線的日期時間。

    * 欄位.上傳日期時間

        上傳完成的日期時間。

    * 欄位.狀態 

        目前的狀態。

        * 狀態的類別
            | 狀態 | 狀態改變時，影響的欄位 | 時機 |
            | ---- | ---- | ---- | 
            | 01.下載資料中 | 狀態異動使用者 = 登入使用者, 狀態異動日期時間 = 系統日期時間, 離線使用者=登入使用者, 離線日期時間=系統日期時間 | 於MAE按下[設定離線範圍]後 |
            | 01.進入離線 | 狀態異動使用者 = 登入使用者, 狀態異動日期時間 = 系統日期時間 | 資料下載完成後 |
            | 02.取消離線 |	狀態異動使用者 = 登入使用者, 狀態異動日期時間 = 系統日期時間 | 狀況1.於MAE按下[放棄離線] <br> 狀況2.已經進入離線後，有錯誤時系統自動放棄離線 | 
            | 03.強制斷線 |	狀態異動使用者 = 登入使用者 狀態異動日期時間 = 系統日期時間 | 於本單按下[按鈕.強制斷線] |
            | 04.上傳資料中 | 狀態異動使用者 = 登入使用者, 狀態異動日期時間 = 系統日期時間, 上傳日期時間=空白 | 於MAE按下[恢復連線]，上傳資料前 |
            | 05.上傳成功 | 狀態異動使用者 = 登入使用者, 狀態異動日期時間 = 系統日期時間, 上傳日期時間=系統日期時間 | 於MAE按下[恢復連線]，上傳資料完成後(開啟同步表單前) |
            | 06.上傳失敗 |	狀態異動使用者 = 登入使用者, 狀態異動日期時間 = 系統日期時間 | 於MAE按下[恢復連線]，上傳資料失敗 |
            | 07.上傳取消 | 狀態異動使用者 = 登入使用者, 狀態異動日期時間 = 系統日期時間 | 於MAE按下[恢復連線]，上傳資料中，使用者自行取消 |
            | 08.同步完成 | 狀態異動使用者 = 登入使用者, 狀態異動日期時間 = 系統日期時間 | 於同步完成後 |
            | 09.放棄同步 | 狀態異動使用者 = 登入使用者, 狀態異動日期時間 = 系統日期時間 | 於本單按下[按鈕.放棄同步] |

    * 欄位.狀態異動使用者

        目前狀態的異動使用者姓名。

    * 欄位.狀態異動日期時間	

        目前狀態的異動日期時間。

    * 按鈕.放棄同步

        放棄同步，刪除所有上傳資料。

	    * 執行限制
		    * 致能條件 : 欄位.狀態 = 上傳成功。

        * 執行
            * 異動駐留記錄的欄位
                * 欄位.狀態 = 放棄同步
                * 欄位.狀態異動使用者 = 登入使用者
                * 欄位.狀態異動日期時間 = 系統日期時間
            * 刪除所有上傳資料。
														
    * 按鈕.強制斷線

        當設為強制斷線後，恢復連線時，將會無法上傳資料。

	    * 執行限制													
		    * 致能條件 : 欄位.狀態 = 進入離線。

        * 執行
            * 異動駐留記錄的欄位
                * 欄位.狀態 = 強制斷線
                * 欄位.狀態異動使用者 = 登入使用者
                * 欄位.狀態異動日期時間 = 系統日期時間

    * 按鈕.取消強制斷線

        取消強制斷線。

	    * 執行限制
		    * 致能條件 : 欄位.狀態 = 強制斷線。
														
	    * 執行
            * 異動駐留記錄的欄位
                * 欄位.狀態 = 進入離線
                * 欄位.狀態異動使用者 = 登入使用者
                * 欄位.狀態異動日期時間 = 系統日期時間

    * 欄位.狀態說明

        目前狀態的說明。


* 作業流程
    * 開啟畫面

        ![表單_MAE離線管理_開啟畫面]

    * 過濾

        ![表單_MAE離線管理_過濾]

    * 放棄同步

        ![表單_MAE離線管理_放棄同步]

    * 強制斷線

        ![表單_MAE離線管理_強制斷線]

    * 取消強制斷線

        ![表單_MAE離線管理_取消強制斷線]


[表單_MAE離線管理_表單畫面]:attachment/表單_MAE離線管理_表單畫面.png "表單_MAE離線管理_表單畫面"
[表單_MAE離線管理_開啟畫面]:attachment/表單_MAE離線管理_開啟畫面.png "表單_MAE離線管理_開啟畫面"
[表單_MAE離線管理_過濾]:attachment/表單_MAE離線管理_過濾.png "表單_MAE離線管理_過濾"
[表單_MAE離線管理_放棄同步]:attachment/表單_MAE離線管理_放棄同步.png "表單_MAE離線管理_放棄同步"
[表單_MAE離線管理_強制斷線]:attachment/表單_MAE離線管理_強制斷線.png "表單_MAE離線管理_強制斷線"
[表單_MAE離線管理_取消強制斷線]:attachment/表單_MAE離線管理_取消強制斷線.png "表單_MAE離線管理_取消強制斷線"

