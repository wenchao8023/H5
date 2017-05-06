（二） CSS表单的基本使用
1. 引入外部样式文件
	格式：<link href="CSS 样式文件的路径" rel="stylesheet" type="text/css" />
	例子：<link href="outer.css" rel="stylesheet" type="text/css" /> 引入同目录下的 outer.css 样式文件
	
2. 导入外部样式单
	格式：<style type="text/css">
		    	@import "CSS 样式文件的路径";
		 </style>
	例子：<style type="text/css">
			@import "outer.css";
		 </style>
	使用 @import 的完整语法如下：
	@import url (样式单地址) sMedia;
	url：一般可省略，直接使用 样式单地址 即可
	sMedia：用于指定该延时单仅对某种显示设备有效（目前大部分流浪器都不支持sMedia设置）
	【注意】：尽量使用第一种连接外部样式单

3. 使用内部 CSS 样式单
	只适用于让某些CSS样式仅对某个页面有效，而不会影响整个站点
	格式：	<style type="text/css">
				样式单文件定义
		 	</style>
	例子：	<style type="text/css">
				table {
					background-color: #003366;
				}
				td {
					background-color: #FFFFFF;
					font-family: "¿¬Ìå_GB2312";
					font-size: 20pt;
					text-shadow: -8px 6px 2px #333;
				}
				.title {
					font-size: 18px;
					color: #60C;
					height: 30px;
					width: 200px;
					border-top: 3px solid #CCCCCC;
					border-left: 3px solid #CCCCCC;
					border-bottom: 3px solid #000000;
					border-right: 3px solid #000000;
				}
			</style>

4. 使用内联样式
	内联样式只对单个标签有效；
	多个 CSS 样式定义之间以英文分号隔开；
	格式：style="property1:value1;property2:value2..."
