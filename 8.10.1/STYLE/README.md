### <div id="stylename">樣式名稱 <path>(IDE介面)</path></div>

### <div id="styletype">元件類型 <path>(IDE介面)</path></div>
### <div id="statustype">狀態樣式 <path>(IDE介面)</path></div>
### <div id="background">底色 <path>(IDE介面\常用樣式)</path></div>
底色。

<ps>注意</ps> 背景圖 > 顏色 (顏色、透明度) > 漸層色(漸層色、漸層方向)。

<ps>注意</ps> 當<顏色>有設定時，<透明度>才可以設定。

<ps>注意</ps> 當<顏色>有設定時，<漸層色 / 漸層方向> 無效。

<ps>注意</ps> 漸層色 + 漸層方向 : 兩個都要設定才會生效。

<ps>注意</ps> 當設定為漸層色時，若線條=虛線，則虛線內看到的底色會與漸層相反，以下圖畫面為例:

![背景漸層色]

元件容器區塊設定漸層色=藍色，漸層方向=下，表示由上往下為白色->藍色進行漸層，此時線條=虛線，上框線顏色=紫色。上框線此時應為白色(底色)與紫色(框線顏色)相間的虛線線條，但卻呈現藍色(底色)與紫色(框線顏色)，經確認後，此為目前CSS3的呈現方式，討論後不做修改。

### <div id="background_color">顏色 <path>(IDE介面\常用樣式\底色)</path></div>
底色的顏色。

### <div id="background_transparent">透明度 <path>(IDE介面\常用樣式\底色)</path></div>
底色的透明度。(0~100)(0:透明)

### <div id="background_gradient_color">漸層色 <path>(IDE介面\常用樣式\底色)</path></div>
底色的漸層色。

### <div id="background_gradient_direction">漸層方向 <path>(IDE介面\常用樣式\底色)</path></div>
底色的漸層方向。
* 無
* 1.上
* 2.下
* 3.左
* 4.右
* 5.垂直
* 6.水平
* 7.往內
* 8.往外            

### <div id="content">內容 <path>(IDE介面\常用樣式)</path></div>


### <div id="content_color">文字顏色 <path>(IDE介面\常用樣式\內容)</path></div>
內容的文字顏色。

### <div id="content_transparent">透明度 <path>(IDE介面\常用樣式\內容)</path></div>
內容的文字透明度。

### <div id="content_font">字型 <path>(IDE介面\常用樣式\內容)</path></div>
內容的文字字型。

### <div id="content_fontsize">字型大小 <path>(IDE介面\常用樣式\內容)</path></div>
內容的文字字型大小。

### <div id="content_horz">水平 <path>(IDE介面\常用樣式\內容)</path></div>
內容的水平對齊方式。
* 0.靠左
* 1.置中
* 2.靠右

### <div id="content_vert">垂直 <path>(IDE介面\常用樣式\內容)</path></div>
內容的垂直對齊方式。
* 0.靠上
* 1.置中
* 2.靠下

### <div id="content_bold">粗體 <path>(IDE介面\常用樣式\內容\字型樣式)</path></div>
內容的文字是否粗體。

### <div id="content_italic">斜體 <path>(IDE介面\常用樣式\內容\字型樣式)</path></div>
內容的文字是否斜體。

### <div id="content_underline">底線 <path>(IDE介面\常用樣式\內容\字型樣式)</path></div>
內容的文字是否加上底線。

### <div id="content_linethrough">刪除線 <path>(IDE介面\常用樣式\內容\字型樣式)</path></div>
內容的文字是否加上刪除線。


           * 字型樣式
                * 粗體
                * 斜體
                * 底線
                * 刪除線        
                * 字型大小
			* 超連結
				* 點擊前
				* 點擊後
### <div id="border">框線 <path>(IDE介面\常用樣式)</path></div>                            			
		* 框線
			* 線條
                0.實線 / 1.虛線 / 2.嵌入線 / 3.浮出線
                註. 只要<線條>有設定，上線寬度、上線顏色、下線寬度、下線顏色、左線寬度、左線顏色、右線寬度、右線顏色都一定要設定            
			* 圓角
			* 上框線
				* 寬度
				* 顏色
			* 下框線
				* 寬度
				* 顏色
			* 左框線
				* 寬度
				* 顏色
			* 右框線
				* 寬度
				* 顏色
### <div id="padding">內間距 <path>(IDE介面\常用樣式\邊界)</path></div>
			* 內間距
				* 上
				* 下
				* 左
				* 右
### <div id="margin">外邊距 <path>(IDE介面\常用樣式\邊界)</path></div>
			* 外邊距
				* 上
				* 下
				* 左
				* 右
### <div id="grid_row_background">列底色 <path>(IDE介面\進階樣式)</path></div>
		* 列底色
			* 標題列
			* 資料列
				* 單數
				* 雙數

### <div id="content_border">內框線 <path>(IDE介面\進階樣式)</path></div>                
		* 內框線
			* 線條
                0.實線 / 1.虛線 / 2.嵌入線 / 3.浮出線
                註. 只要<線條>有設定，上線寬度、上線顏色、下線寬度、下線顏色、左線寬度、左線顏色、右線寬度、右線顏色都一定要設定            
			* 圓角
			* 上框線
				* 寬度
				* 顏色
			* 下框線
				* 寬度
				* 顏色
			* 左框線
				* 寬度
				* 顏色
			* 右框線
				* 寬度
				* 顏色

### <div id="focusbar">光棒 <path>(IDE介面\進階樣式)</path></div>
		* 光棒
			* 線條
                實線 / 虛線 / 嵌入線 / 浮出線
                註. 只要<線條>有設定，上線寬度、上線顏色、下線寬度、下線顏色、左線寬度、左線顏色、右線寬度、右線顏色都一定要設定            
			* 上框線
				* 寬度
				* 顏色
			* 下框線
				* 寬度
				* 顏色
			* 左框線
				* 寬度
				* 顏色
			* 右框線
				* 寬度
				* 顏色
			* 底色
                註. 背景圖 > 顏色 (顏色、透明度) > 漸層色(漸層色、漸層方向)
                註. 當<顏色>有設定時，<透明度>才可以設定
                註. 當<顏色>有設定時，<漸層色 / 漸層方向> 無效
                註. 漸層色 + 漸層方向 : 兩個都要設定才會生效            
				* 顏色
				* 透明度
				* 漸層色
				* 漸層方向
                    無 / 1.上 / 2.下 / 3.左 / 4.右 / 5.垂直 / 6.水平 / 7.往內 / 8.往外
### <div id="icon">圖示設定 <path>(IDE介面\進階樣式)</path></div>

		* 圖示設定



[背景漸層色]:attachment/linear_gradient.png "背景漸層色"