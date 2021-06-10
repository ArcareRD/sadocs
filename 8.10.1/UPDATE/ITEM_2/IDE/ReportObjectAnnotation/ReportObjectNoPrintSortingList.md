欄位同值不列印排序
===
## 版面相關
* 版面</br>
    ![pic][image_ReportObjectNoPrintSortingList]

## 動作說明
* 開啟後視窗寬高預設為 400 * 450, 不提供調整寬高

## 欄位設定
* <p id="fieldbreak1" style="color:blue;">基本</p>

    * ![pic][image_ReportObjectNoPrintSortingList_block1]
    * `(1)儲存`
        * 用途說明  
        * 規格說明
            * 執行時, 將本次駐留順序設定結果存回
    * `(2)重載`
        * 用途說明  
        * 規格說明
            * 執行後, 將畫面恢復至上一次儲存的結果
    * `(3)移至頂端`
        * 用途說明  
        * 規格說明
            * 執行後, 將目前鎖定的元件移至最頂端; 若有多個鎖定元件, 依鎖定元件順序排序後, 移至最頂端
    * `(4)向上移動`
        * 用途說明  
        * 規格說明
            * 執行後, 將目前鎖定的元件向上移一個元件; 若有多個鎖定元件, 依鎖定元件順序排序後, 取得鎖定元件中最小順序向上移一個元件(若最小順序已是第一個元件則不再變動順序)
    * `(5)向下移動`
        * 用途說明  
        * 規格說明
            * 執行後, 將目前鎖定的元件向下移一個元件; 若有多個鎖定元件, 依鎖定元件順序排序後, 取得鎖定元件中最大順序向下移一個元件(若最大順序已是第後一個元件則不再變動順序)
    * `(6)移至尾端`
        * 用途說明  
        * 規格說明
            * 執行後, 將目前鎖定的元件移至最底端; 若有多個鎖定元件, 依鎖定元件順序排序後, 移至最底端
    * `(7)解除鎖定`
        * 用途說明  
        * 規格說明
            * 執行後, 將所有已鎖定的元件，變動為未鎖定
    * `(8)排序元件區塊`
        * 用途說明  
        * 規格說明
            * 區塊列數依視窗高度顯示列數, 超過出現垂直捲軸
    * `(9)順序`
        * 用途說明  
        * 規格說明
            * 依序顯示流水號
    * `(10)報表元件名稱`
        * 用途說明  
        * 規格說明
            * 顯示: 報表元件名稱; 當報表元件名稱超過區塊寬度時, 不折行
            * 滑鼠移入時, 將該筆報表元件修改為滑鼠移入樣式(參考下圖); 滑鼠移出, 則恢復原樣式
                * 修改滑鼠指標; 並將邊框增加藍色陰影; Hint顯示: 報表元件類型 <br>
                    ![pic][image_ReportObjectNoPrintSortingList_MoveIn]
            * 滑鼠單擊時, 增加鎖定狀態樣式
                * 當該筆報表元件未在鎖定狀態, 單擊後, 將該筆報表元件修改為鎖定樣式(參考下圖) <br>
                    ![pic][image_ReportObjectNoPrintSortingList_Click]
                * 當該筆報表元件已在鎖定狀態, 單擊後, 恢復原樣式
            * 滑鼠移動時, 依駐留筆移動報表元件的順序
                * 當駐留筆未在鎖定狀態，僅移動駐留筆
                * 當駐留筆在鎖定狀態, 移動時, 需連同目前所有鎖定的報表元件，依鎖定元件順序排序後移至新位置



<!-- 圖片 -->
[image_ReportObjectNoPrintSortingList]:attachment/ReportObjectNoPrintSortingList.png
[image_ReportObjectNoPrintSortingList_block1]:attachment/ReportObjectNoPrintSortingList_block1.png
[image_ReportObjectNoPrintSortingList_MoveIn]:attachment/ReportObjectNoPrintSortingList_MouseIn.png
[image_ReportObjectNoPrintSortingList_Click]:attachment/ReportObjectNoPrintSortingList_Locking.png