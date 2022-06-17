
#### <div id="item_name">功能項目名稱</div>
  * 元件容器新增屬性-滑動區域

### <div id="user">規劃人員</div>
* Andy

#### <div id="version">支援版本</div>
  |日期|版本|備註|
  |---|---|---|
  |2022/06/17|008.010.002022|MAE|

### <div id="trac">TRAC</div>
* [#9068](http://trac.arcare.com.tw/trac/neco/ticket/9068)

### <div id="specification">規格說明</div>
  * 需求展開
    * [元件容器][container]
      * 新增屬性
        * 滑動區域
          * 全螢幕
            * 滑動範圍為整個表單，元件容器無法滑動
          * 元件容器
            * 滑動範圍為元件容器內容，表單無法滑動
            * 僅支援
              * 滑動方向=上下滑動
              * 區塊模式=單列式
            * 表單只能設定一個
            * 元件容器為變動高度，顯示高度範圍為扣除元件容器以上及以下的顯示元件區域後的剩餘空間(橫屏時的顯示範圍會更小)

<!-- 連結 -->
[container]:../../../MAE/Component/container.md "元件容器"
