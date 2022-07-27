### <div id="user">規劃人員</div>
* Prenkt

### <div id="updatedate">規劃日期</div>
* 2022/6/20

### <div id="trac">TRAC</div>
* #9068

### <div id="requirement">需求展開</div>
* 規格說明
    * 表單版面設計: 要做到容器外的欄位可以凍結, 只滑動容器內的記錄
        * 當元件類型=wCtnr.元件容器 且 區塊模式=單列式，屬性設定: 滑動區域，下拉(1.全螢幕 2.元件容器) 致能，否則 除能
        * 增加版面儲存檢控: 表單若有設定容器為滑動區域=2.元件容器時，表單只允存在一個容器元件
    * 元件加註-基本設定: 下列條件成立時，引用功能 致能，否則 除能 :  
        * (類型in(wTBtn.連結框線、wTP.文字標題、wImg.圖片、liteImage.圖片(多筆瀏覽)) 
        * (類型in(wTF.文字方塊、text.文字方塊(多筆表格)、liteText.文字方塊(多筆瀏覽)、wTA.多行文字) 且 欄位能力.僅供顯示=True 且 撥號功能 = false)) 
        * (表單設計類型=3.APP 且 元件類型=wCtnr.元件容器) 
* 文件位置
    * [表單版面設計][link_FormDesign]
    * [元件加註-基本設定][link_ObjectAnnotation]

<!-- 超連結 -->
[link_FormDesign]:{3}/IDE/Specification/FormDesign/README
[link_ObjectAnnotation]:{3}/IDE/Specification/ObjectAnnotation/README