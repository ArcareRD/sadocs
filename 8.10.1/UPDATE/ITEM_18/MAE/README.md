
#### <div id="item_name">功能項目名稱</div>
  * 擴充固定下方導覽列，套用在所有表單

### <div id="user">規劃人員</div>
* Andy

#### <div id="version">版本記錄</div>
  |日期|版本|備註|
  |---|---|---|
  |2021/12/7|v1|初始化|

### <div id="trac">TRAC</div>
* [#8775](http://trac.uneec.com/trac/neco/ticket/8775)

### <div id="specification">規格說明</div>
  * 需求展開
    * 固定下方導覽列，套用在所有表單
      * 規則
        * 當表單有下方導航列時
          * 顯示表單的下方導航列
        * 當表單無下方導航列時
          * 當下列條件成立時，顯示首頁的下方導覧列
            * 1. 有首頁時
            * 2. 首頁有下方導覧列時
  * 示意圖
    * android
      * 首頁包含下方導覧列
      
        ![AndroidNavigationMainForm]

      * 表單包含下方導覧列
      
        ![AndroidNavigationFormDown]

      * 表單不包含下方導覧列，以首頁取代
      
        ![AndroidNavigationReplaceDown]
    * ios
      * 首頁包含下方導覧列
      
        ![IOSNavigationMainForm]

      * 表單包含下方導覧列
      
        ![IOSNavigationFormDown]

      * 表單不包含下方導覧列，以首頁取代
      
        ![IOSNavigationReplaceDown]
  * 流程圖
  
    ![workflowNavigation]

<!-- 圖示_介面 -->
[AndroidNavigationMainForm]:image/android/navigation_main_form.jpg "Android 首頁包含下方導覧列"
[AndroidNavigationFormDown]:image/android/navigation_form_down.jpg "Android 下拉選項-單選"
[AndroidNavigationReplaceDown]:image/android/navigation_replace_down.jpg "Android 下拉選項-單選 關鍵字過濾"
[IOSNavigationMainForm]:image/ios/navigation_main_form.PNG "Android 首頁包含下方導覧列"
[IOSNavigationFormDown]:image/ios/navigation_form_down.PNG "Android 下拉選項-單選"
[IOSNavigationReplaceDown]:image/ios/navigation_replace_down.PNG "Android 下拉選項-單選 關鍵字過濾"

[workflowNavigation]: image/workflow_navigation.png "工作流程"

<!-- 超連結 -->

