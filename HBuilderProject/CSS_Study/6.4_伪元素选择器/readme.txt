(四) 伪元素选择器
1. CSS 提供的伪元素选择器
 	(1)	:first-letter:	该选择器对应的 CSS 样式对指定对象内的【第一个字符】起作用；				<first-letter.html>
 	(2)	:first-line:		该选择器对应的 CSS 样式对指定对象内的【第一行内容】起作用；				<first-line.html>
 	(3)	:before:			该选择器与内容相关的属性结合使用，用于在指定对象内部的【前端】插入内容；	<content.html>
 	(4)	:after:			该选择器与内容相关的属性结合使用，用于在指定对象内部的【尾端】添加内容；	<after.html>
	【tips】伪元素选择器只针对 CSS 中已有的【伪元素】起作用

2. CSS 支持的内容相关的属性<content.html>
	(1)	include-source:	该属性的值应为 url(url)，插入绝对或相对 URL 地址所对应的文档。（目前还没有浏览器支持该属性）； 
	(2)	content:			该属性的值可以是字符串、url(url)、attr(alt)、counter(name)、counter(name,list-style-type)、open-quote、close-quote 等格式；
						该属性用于向指定元素之前、或之后插入指定内容；
	(3)	quotes:			该属性用于为 content 属性定义 open-quote 和 close-quote，该属性的值可以是两个以空格分隔的字符串，其中前面的字符串是 open-quote，后面的字符串是 close-quote；
	(4) counter-increment:
						该属性用于定义一个计数器；
						该属性的值就是计数器的名称；
	(5)	counter-reset:	该属性用于对指定的技术值复位。
	【tips】content 属性是核心
	
3. 只插入部分元素<partAppend.html>
	格式：[E]>[E]Selector2:after	/* [E] ：表示要插入内容的元素； */
	指定该属性为在 class 值为 Selector2 的元素 [E] 后面插入内容。可扩展，在前面插入内容等同
	
4. 配合 quotes 属性执行插入<quote.html>

5. 配合 counter-increment 属性添加编号<counter.html>

6. 使用自定义编号<CustomCounter.html>
	decimal:			阿拉伯数字。默认值。
	disc:			实心圆
	circle:			空心圆
	square:			实心方块
	lower-roman:		小写罗马数字
	upper-roman:		大写罗马数字
	none:			不使用项目符号
	cjk-ideographic:	浅白的表意数字
	georgian:		传统的乔治数字
	lower-greek:		基本的希腊小写字母
	hebrew:			传统的希伯来数字
	hiragana:		日文平假名字符	
	hiragana-iroha:	日文平假名序号
	katakana:		日文片假名字符
	katakana-iroha:	日文片假名序号
	lower-latin:		小写拉丁字母
	upper-latin:		大写拉丁字母

7. 添加多级编号<multiCounter.html>
	【原理】通过 CSS 定义多个编号计数器，然后为不同的选择器插入不同的计数器即可。