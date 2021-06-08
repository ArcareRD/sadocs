### <div id="user">規劃人員</div>
* Ivan

### <div id="updatedate">規劃日期</div>
* 2021/6/4

### <div id="trac">TRAC</div>
* #8502

### <div id="enterprisedetail">企業資料<path>(Site管理)</path></div>
* 擴充
* 規格說明
    * 表單.系統自訂版面的Logo設定移至本單
    * 企業管理員權限調整
        * 調整前：
            * 所有欄位唯讀、功能鍵除能
        * 調整後：
            * 欄位.企業同時登入人數 唯讀
            * 功能鍵.企業Manager 除能
            * 其他欄位、功能鍵皆可以異動

* 表單畫面

    * 由Site管理員開啟

    ![EnterpriseDetail_SA1]

    * 由企業管理員開啟

    ![EnterpriseDetail_SA2]

* 畫面規格說明

    * 欄位.使用者維持登入時間(分鐘)：標題改為 閒置登出時間(分鐘)

    * 欄位.LOGO檔案：
        * 唯讀
        * 有上傳圖檔時，顯示圖片檔案名稱(含副檔名)

    * 功能鍵.上傳：
        * 開啟檔案總管挑選圖片
        * 上傳後欄位.LOGO顯示圖片檔案名稱(含副檔名)
        * 上傳後欄位.預覽結果顯示圖片縮圖

    * 功能鍵.下載：
        * 未上傳LOGO檔案 時除能
        * 下載已上傳的LOGO檔案

    * 功能鍵.恢復系統預設：
        * 未上傳LOGO檔案 時除能
        * 刪除已上傳的LOGO檔案
        * 刪除後清空欄位.LOGO
        * 刪除後清空欄位.預覽結果

    * 欄位.預覽結果：顯示上傳圖片的預覽

    * 欄位.設計規則：上傳的圖片格式需依照此規格

    * 多筆表格：
        * 欄位.使用者維持登入時間(分鐘)：標題改為 閒置登出時間(分鐘)

* 作業流程

    * 由Site管理員開啟
    
    ![EnterpriseDetail_SA3]

    * 由企業管理員開啟

    ![EnterpriseDetail_SA4]
    
    * 執行功能鍵.上傳
    
    ![EnterpriseDetail_SA5]
    
    * 執行功能鍵.下載

    ![EnterpriseDetail_SA6]
    
    * 執行功能鍵.恢復系統預設

    ![EnterpriseDetail_SA7]
    
<!--超連結引用ps.畫面上看不到-->
[EnterpriseDetail_SA1]:attachment/enterprisedetail_sa1.jpg
[EnterpriseDetail_SA2]:attachment/enterprisedetail_sa2.jpg
[EnterpriseDetail_SA3]:attachment/enterprisedetail_sa3.jpg
[EnterpriseDetail_SA4]:attachment/enterprisedetail_sa4.jpg
[EnterpriseDetail_SA5]:attachment/enterprisedetail_sa5.jpg
[EnterpriseDetail_SA6]:attachment/enterprisedetail_sa6.jpg
[EnterpriseDetail_SA7]:attachment/enterprisedetail_sa7.jpg