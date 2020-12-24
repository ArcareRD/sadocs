### <div id="user">規劃人員</div>
* Ivan

### <div id="updatedate">規劃日期</div>
* 2020/12/14

### <div id="trac">TRAC</div>
* #8264

### <div id="sitemanage_2">表單.Site資料庫設定 <path>(環境設定)</path></div>
* 異動
* 規格說明
    * 刪除欄位.稽核Log資料庫
    * 按鈕.儲存 不須儲存稽核Log資料庫的設定
    * 升級轉資料

* 表單畫面
    | | 畫面 |
    | ------- | :------: |
    | 原</br>畫</br>面 | ![SiteDatabaseSet(old)] |
    | 新</br>畫</br>面 | ![SiteDatabaseSet] |

* 畫面規格說明
    * 欄位.稽核Log資料庫 : 移除該欄位
    * 按鈕.儲存 : 不須儲存稽核Log資料庫的設定
    * 按鈕.重整資料庫 :
        * 執行
            * Site資料庫
                * 若原版本<8.10.0時 (擴充)
                    * 新增系統實體
                        * 稽核紀錄環境設定
                    * 升級轉資料
                        * 新增Site稽核員資料
                        * 新增稽核紀錄環境設定資料
                            * 之前有設定稽核LOG資料庫
                                * 取得原稽核LOG資料庫
                            * 之前未設定稽核LOG資料庫
                                * 建立預設稽核LOG資料庫
                    * 修改系統實體
                        * 參數設定
                            * 刪除欄位.稽核LOG資料庫
                            * 刪除欄位.處理稽核LOG的中間台唯一號
                        * 系統清單
                            * 刪除欄位.稽核LOG開啟
                    * 刪除系統實體
                        * 異動稽核LOG設定LOG
                    
            * 稽核Log資料庫
                * 若原版本<8.10.0時 (擴充)
                    * 新增系統實體.稽核Log資料(記錄最近30天內的Log)
                    * 備份原稽核Log資料
                        * 有找到單日/雙日/週稽核Log資料的實體
                            * 將未備份的單日/雙日/週稽核Log資料備份至系統實體.稽核Log資料
                    * 刪除系統實體
                        * 有找到單日/雙日/週稽核Log資料的實體
                            * 單數日稽核Log資料
                            * 偶數日稽核Log資料
                            * 當月稽核Log資料

* 作業流程
    * 開啟Site資料庫設定畫面

    ![SiteDatabaseSet_sa1]
    * 儲存

    ![SiteDatabaseSet_sa2]
    * 重整資料庫

    ![SiteDatabaseSet_sa3]


<!--超連結引用ps.畫面上看不到-->
[SiteDatabaseSet]:img/SiteDatabaseSet.jpg
[SiteDatabaseSet(old)]:img/SiteDatabaseSet(old).jpg
[SiteDatabaseSet_sa1]:img/SiteDatabaseSet_sa1.jpg
[SiteDatabaseSet_sa2]:img/SiteDatabaseSet_sa2.jpg
[SiteDatabaseSet_sa3]:img/SiteDatabaseSet_sa3.jpg