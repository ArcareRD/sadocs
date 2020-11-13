### <div id="user">規劃人員</div>
* Lucky

### <div id="updatedate">規劃日期</div>
* 2020/11/12

### <div id="trac">TRAC</div>
* #8197

### <div id="publish">版本發行<path>(需求展開\輔助工具)</path> </div>
* 版面 
  * ![publish]
* 欄位說明
  * <t id="btnpublish">(1)發行</t>
    * 用途說明: 建立該版本XML資訊並通知匯入程式進行匯入、噴碼
    * 規格說明: 
      * 當[狀態](#ui_publishlog_stage) 等於 8.成品已批次產出, 呼叫API異動測試運行台的系統名稱
      | 語系狀態 | 動作 |
      | ------- | ---- |
      | 已存在 | 不處理 |
      | 不存在 | 新增語系內容 |

      * 測試台建立規則
      | 語系 | 運行台名稱 |
      | --- | --------- |
      | 950(繁體中文) | `對應950的語系內容 + "_運行台"` |
      | 936(簡體中文) | `對應950的語系內容 + "_运行台"` |
      | 437(英文) | `對應950的語系內容 + "_SIT"` |
      | 1145(西班牙) | `對應950的語系內容 + "_SIT"` |

  * <t id="ui_publishlog_stage">(2)狀態</t>
    * 用途說明: 顯示目前發行處理狀態
    * 規格說明: 
* 作業流程
  * ![Publish_Diagram]


<!--圖片-->
[publish]:attachment/Publish.png "版本發行"
[Publish_Diagram]:attachment/Publish_Diagram.png "[作業流程]發行"
