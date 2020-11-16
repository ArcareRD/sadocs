## <div id="user">規劃人員</div>
  * Andy

## <div id="updatedate">規劃日期</div>
  * 2020/11/09

## <div id="trac">TRAC</div>
  * 待補

#### <div id="offline_mode_data_transfer">資料傳輸<path>(資料處理)</path></div>
* 規格說明
  * 下載離線資料
    * 顯示下載進度[(表單畫面 下載)](#data_transfer_download)
    * 目前無續傳
    * 成功下載後即為離線模式
  * 上傳離線資料
    * 顯示上傳進度[(表單畫面 上傳)](#data_transfer_upload)
    * 目前無續傳
    * 失敗可選擇重新傳送
    * 成功上傳後即為連線模式
* 表單畫面
  * <p id=data_transfer_download>下載</p>
  
    ![Offline Mode Download](./image/offlinemodedownload.png)

  * 下載錯誤
  
    ![Offline Mode Download Error](./image/offlinemodedownloaderror.png)

  * <p id=data_transfer_upload>上傳</p>
  
    ![Offline Mode Download](./image/offlinemodeupload.png)

  * 上傳錯誤
  
    ![Offline Mode Download](./image/offlinemodeuploaderror.png)
  
  * 上傳中斷
  
    ![Offline Mode Download](./image/offlinemodeuploadinterrupt.png)

* 作業流程
  * 下載

    ![Offline Mode Workflow Download](./image/workflow_download.png)
  
  * 上傳

    ![Offline Mode Workflow Upload](./image/workflow_upload.png)

