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
    * 欄位.同時最大上線人數 標題改為 同時登入人數
    * 欄位.使用者維持登入時間(分鐘) 標題改為 閒置登出時間(分鐘)

* 表單畫面

    * 由Site管理員開啟

    ![EnterpriseDetail_SA1]

    * 由企業管理員開啟

    ![EnterpriseDetail_SA2]

* 畫面規格說明

    * 欄位.同時最大上線人數：標題改為 同時登入人數

    * 欄位.使用者維持登入時間(分鐘)：標題改為 閒置登出時間(分鐘)

    * 欄位.LOGO檔案：有上傳圖檔時，顯示圖片檔案名稱(含副檔名)

    * 功能鍵.上傳：
        * 登入者為企業管理員時除能
        * 開啟檔案總管挑選圖片
        * 上傳後欄位.LOGO顯示圖片檔案名稱(含副檔名)
        * 上傳後欄位.預覽結果顯示圖片縮圖

    * 功能鍵.下載：
        * 登入者為企業管理員 或 未上傳LOGO檔案 時除能
        * 下載已上傳的LOGO檔案

    * 功能鍵.恢復系統預設：
        * 登入者為企業管理員 或 未上傳LOGO檔案 時除能
        * 刪除已上傳的LOGO檔案
        * 刪除後清空欄位.LOGO
        * 刪除後清空欄位.預覽結果

    * 欄位.設計規則：
        * 上傳的圖片格式需依照此規格

    * 多筆表格：
        * 表格寬度、欄位寬度縮小
        * 欄位.同時最大上線人數：標題改為 同時登入人數
        * 欄位.使用者維持登入時間(分鐘)：標題改為 閒置登出時間(分鐘)

<!--超連結引用ps.畫面上看不到-->
[EnterpriseDetail_SA1]:attachment/enterprisedetail_sa1.jpg
[EnterpriseDetail_SA2]:attachment/enterprisedetail_sa2.jpg