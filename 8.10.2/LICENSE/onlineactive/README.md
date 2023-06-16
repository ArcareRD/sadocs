# 認證授權中心 線上啟用授權API

### <div id="func">功能說明</div>
* 當客戶端主機具備外部網路連線能力，讓客戶端維護人員在進行啟用RTE站台時，RTE引擎可以自動透過此API完成線上啟用授權

![流程]

### <div id="api">API說明</div>
* HTTP Method : HTTP POST
* URL : /online/activate
* Request :
    * Header : 
        * Authorization：授權中心金鑰對-公鑰
    * Body : 
        * type : 授權類型，目前有以下類型
          * RTE_SITE : RTE站台授權
          * RTE_SYSTEM : RTE系統授權
        * file : 使用RTE金鑰對-私鑰加密過的授權資料，未加密前的啟用授權資訊為JSON格式
          * 當 type = RTE_SITE，資訊內容如下
            * siteid : 該筆站台授權的代號
              * 數字型態
            * ubn : 客戶統一編號
              * 文字型態
            * name : 客戶站台名稱
              * 文字型態
            * type : 授權類型
              * 數字型態
              * 1=同時連線數
              * 2=帳號數
              * 3=雲端平台授權
            * count : 授權數量
              * 數字型態
            * startdate : 授權開始日期
              * 文字型態，格式 = 'yyyy-mm-dd'
            * enddate : 授權結束日期
              * 文字型態，格式 = 'yyyy-mm-dd'
            * mac : 啟用主機電腦的MAC Address
              * 文字型態
            * computername : 啟用主機電腦的電腦名稱
              * 文字型態
          * 當 type = RTE_SYSTEM，資訊內容如下
            * systemid : 該筆系統授權的代號
            * 數字型態
            * projid : 系統全唯碼
              * 文字型態
            * mkpjid : 系統組裝全唯碼
              * 文字型態
            * name : 系統名稱
              * 文字型態
            * type : 授權類型
              * 數字型態
                * 1=同時連線數
                * 2=帳號數
            * count : 授權數量
              * 數字型態
            * startdate : 授權開始日期
              * 文字型態，格式 = 'yyyy-mm-dd'
            * enddate : 授權結束日期
              * 文字型態，格式 = 'yyyy-mm-dd'
            * mac : 啟用主機電腦的MAC Address
              * 文字型態
            * computername : 啟用主機電腦的電腦名稱
              * 文字型態
            * enterpriseid : 啟用該系統授權的企業全唯碼
              * 文字型態
            * enterprise : 啟用該系統授權的企業名稱
              * 文字型態
        * signature : 數位簽章
    * Example :
        * Header : 
            * Authorization：MIICIjANBgkqhkiG9w0BAQEFAAOCAg8AMIICCgKCAgEAmDJhaFXig73c1Ik8j
        * Body : 
            * "type":"RTE_SITE"
            * "file":"RuBzbuK6APPT8ghKlr5E0h31TUdTvXh+L+ox7riSQudNxEe/HM1R0tTNt/ZA0w8T4ukAyG/"+"\r\n"+"ieHRp6vFxIt8cTnzVt4YksCh32Kj7BNMZstZ+sPlRNY5KP4hoo7ULPNzVq5cZXSCjw+jOU+BbH"}
* Response
    * Body
        * 成功會取得認證啟用檔案內容, 包含以下兩部分
            * 使用授權中心金鑰對-私鑰加密後的啟用授權資訊 : 未加密前的啟用授權資訊為JSON格式，內容同傳入參數.source的內容
            * 數位簽章 : 使用未加密前的啟用授權資訊作為原始資料，產生數位簽章
        * 若有錯，則errorcode=500，可取得錯誤原因.

[流程]:attachment/軟體授權碼連線啟用站台.png "流程"