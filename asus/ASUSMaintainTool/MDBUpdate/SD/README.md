### <div id="flowchart">更新MDB檔案程式-循序圖</div>

---
## <div id="view">● 視窗介面動作 </div>
![img_mdbupdate_1]

---
## <div id="check-db-in-no-update">● 勾選未完成更新的資料庫 </div>

---
## <div id="execute-import-object">● 執行系統更新 </div>
#### - BtnExecuteImportObjectListener (執行系統更新)
![img_import_object_1]

#### - attachment/ObjectManage.ParserObject(解析LIFF檔)
![img_import_object_2]

#### - ObjectManage.UpdateObject_Share(匯入物件_共用資料庫用)
![img_import_object_3]

#### - DatasManage.UpdateDatas(更新權限資料檔)
![img_import_object_4]

#### - ObjectManage.UpdateObject_Corp(匯入物件_組織資料庫用)
![img_import_object_5]


#### - ImportObject.Backup(備份資料庫)
![img_import_object_6]

#### - ImportObject.Restore(還原資料庫)
![img_import_object_7]



---
## <div id="restore-db">● 還原組織資料庫 </div>











[img_import_object_1]:attachment/BtnExecuteImportObjectListener(執行系統更新).jpg 
[img_import_object_2]:attachment/ObjectManage.ParserObject(解析LIFF檔).jpg
[img_import_object_3]:attachment/ObjectManage.UpdateObject_Share(匯入物件_共用資料庫用).jpg
[img_import_object_4]:attachment/DatasManage.UpdateDatas(更新權限資料檔).jpg
[img_import_object_5]:attachment/ObjectManage.UpdateObject_Corp(匯入物件_組織資料庫用).jpg

[img_import_object_6]:attachment/ImportObject.Backup(備份資料庫).jpg
[img_import_object_7]:attachment/ImportObject.Restore(還原資料庫).jpg

[img_mdbupdate_1]:attachment/MDBUpdate(開啟介面).jpg


