### <div id="user">規劃人員</div>
* 正傑
  
### <div id="updatedate">規劃日期</div>
* 2023/04/19
  
### <div id="trac">TRAC</div>
* #9213 3-1項
  
### <div id="requirement">需求展開</div>
* 因開始鎖定RTE運行的授權人數，因此配合授權中心進行RTE的調整。
  * RTE服務啟動
    * 將授權檔案的驗證寫入Log中
  * RTE站台管理
    * 站台啟用流程
      * 增加向授權中心認證站台授權
      * 當站台授權=同時連線數
        * 驗證站台MAC與授權檔案是否相符
        * 以同時連線數作為站台本身的控制
      * 當站台授權=帳號數
        * 驗證站台MAC與授權檔案是否相符
        * 以增加的帳號數作為站台本身的控制
      * 當站台授權=雲端平台授權
        * 不須驗證站台MAC
        * 不做任何連線數以及帳號數的控制
      * 完整的規格文件請參照[站台啟用](../../../RTE/SITE/active/README.md)
    * 站台授權設定
      * 新增加的表單，用來顯示獲更新站台授權
      * 完整的規格文件請參照[站台授權設定](../../../RTE/SITE/siteauth/README.md)
    * 企業設定系統
      * 增加向授權中心認證系統授權
        * 當站台授權=雲端服務平台
          * 該站台下所有系統不須再經過認證授權
      * 完整的規格文件請參照[企業設定系統](../../../RTE/SITE/enterprisesystem/README.md)
    * 站台線上人數查詢
      * 增加欄位.帳號數
      * 完整的規格文件請參照[站台線上人數查詢](../../../RTE/SITE/siteonlineuser/README.md)
    * 企業線上人數查詢
      * 增加欄位.帳號數
      * 完整的規格文件請參照[企業線上人數查詢](../../../RTE/SITE/enterpriseonlineuser/README.md)
    * 系統線上人數查詢
      * 增加欄位.帳號數
      * 完整的規格文件請參照[系統線上人數查詢](../../../RTE/SITE/systemonlineuser/README.md)
  * RTE運行
    * 登入畫面
      * RTE站台授權到期前一個月，登入畫面顯示提示訊息表示授權快到期了
      * 授權已到期則禁止登入
      * 完整的規格文件請參照[登入畫面](../../../RTE/SYSTEM/LOGIN/README.md)
    * 新版首頁
      * RTE企業下系統授權到期前一個月，當使用者登入系統時，顯示提示訊息表示授權快到期了
      * 授權已到期則禁止登入
      * 當授權類型=同時連線數時
        * 若登入系統Request數量已滿，則顯示人數已滿的訊息
      * 完整的規格文件請參照[新版首頁](../../../RTE/SYSTEM/MAINPAGE/README.md)
    * 舊版首頁
      * RTE企業下系統授權到期前一個月，當使用者登入系統時，顯示提示訊息表示授權快到期了
      * 授權已到期則禁止登入
      * 當授權類型=同時連線數時
        * 若登入系統Request數量已滿，則顯示人數已滿的訊息
      * 完整的規格文件請參照[舊版首頁](../../../RTE/SYSTEM/MAINPAGE_OLD/README.md)
    * 行動裝置版首頁
      * RTE企業下系統授權到期前一個月，當使用者登入系統時，顯示提示訊息表示授權快到期了
      * 授權已到期則禁止登入
      * 當授權類型=同時連線數時
        * 若登入系統Request數量已滿，則顯示人數已滿的訊息
      * 完整的規格文件請參照[行動裝置版首頁](../../../RTE/SYSTEM/MAINPAGE_MOBILE/README.md)
    * MAE API
      * 登入首頁增加回傳站台授權狀態以及授權提示訊息
        * 上述規格紀錄於ShareClass文件中，路徑為 : 8.10.2\RTE\MAE_API\AppRuntimeLogin
      * 登入系統增加回傳系統授權狀態以及授權提示訊息
        * 上述規格紀錄於ShareClass文件中，路徑為 : 8.10.2\RTE\MAE_API\AppChangeSystem
      * 新增API.檢查授權，提供給MAE呼叫用
        * 上述規格紀錄於ShareClass文件中，路徑為 : 8.10.2\RTE\MAE_API\AppGetLicenseStatus
  * 現行客戶站台產生授權資料
    * 完整的規格文件請參照[授權產生程式](../../../RTE/CUSTOM/AUTH/README.md)
  
