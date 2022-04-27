## <div id="layout">版面相關</div>
* 版面<br>
    ![pic][image_form_design]
    

## <div id="main-block-desc">主畫面_版面區塊說明</div>

* <p id="fieldbreak1" style="color:blue;font-weight:bold">樣式呈現</p>

    * 各元件類型在版面上的樣式呈現, 除非有特別說明或DKS已開放設定的部份, 其它皆以 Client 引擎目前的預設樣式為主(含除致能變化), 本文件不列引擎樣式說明, 若有引擎樣式規格問題, 請洽 Client 引擎負責人
        * 元件類型=wCtnr.元件容器, 增加顯示區塊的狀態樣式: 請洽 client 引擎負責人
        * 元件類型=wCtnr.元件容器, 當空白列或子元件總高度超過磚塊高度, 出現垂直捲軸

* <p id="fieldbreak1" style="color:blue;font-weight:bold">版面物件操作說明</p>

    * 物件拖拉原則
        * 若元件類型存在【<delLine>wCtnr.元件容器</delLine>、wTab.頁籤區塊、wDpanel.動態面板、wRBGroup.按鈕群組、wGrdLite.多筆瀏覽】
            * 若設計類型=自適應 或 APP, 系統預設初始高度:50px, 元件屬性:變動高度, 固定為 True, 元件高度應依子階元件的總高度變動
        * 若元件類型存在【wTab.頁籤區塊、wDpanel.動態面板、wRBGroup.按鈕群組、wGrdLite.多筆瀏覽】或 元件類型=wCtnr.元件容器 且 區塊模式=單列式 或 元件類型=wCtnr.元件容器 且 區塊模式=磚塊式 且容器的變動高度=True
            * 若設計類型=自適應 或 APP, 系統預設初始高度:50px, 元件屬性: 變動高度，固定為 True, 元件高度應依子階元件的總高度變動
                    此處規格不變，省略
        * 若元件類型=wCtnr.元件容器, 且區塊模式=磚塊式, 且容器的變動高度=False
            * 新增列、插入列: 
                * 固定給列高度: 50px
                * 磚塊高度、磚塊寬度: 不變化
            * 子元件時的異動變化
                * 子元件可拖拉區塊, 應限制在磚塊中, 否則 拖拉無效
                * 當新增子元件時, 磚塊高度不變; 子元件的變動高度調整為false, 且除能; 否則 致能
                    * 每次計算子元件總高度，若大於磚塊高度，則出現垂直捲軸 
                * 當刪除子元件時, 
                    * 磚塊高度不變, 重新計算各列高度, 將剩餘高度給最後一列
                    * 若刪除子元件後, 該列各欄已無子元件, 調整列高度: 50px
                * 當修改子元件高度時
                    * 重新計算子元件總高度，若大於磚塊高度，則出現垂直捲軸 
                    * 重新計算該列子元件總高度, 若有多餘的高度，將剩餘的高度給最後一列


<!-- 圖片 -->
[image_form_design]:attachment/FormDesign.png

<!-- 超連結 -->
