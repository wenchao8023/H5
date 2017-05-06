(五) 伪类选择器
	伪类选择器主要是对已有的选择器做进一步的限制。主要有：
		结构性伪类选择器
		UI 元素状态伪类选择器
		其他伪类选择器
		
1. 结构性伪类选择器
	(1)	Selector:root:					匹配文档的根元素。在 HTML 文档中，根元素永远是<html.../>元素
	(2)	Selector:first-child:			匹配符合 Selector 选择器，而且必须是其父元素的第一个子节点的元素
	(3)	Selector:last-child:				匹配符合 Selector 选择器，而且必须是其父元素的最后一个子节点的元素
	(4)	Selector:nth-child(n):			匹配符合 Selector 选择器，而且必须是其父元素的第 n 个子节点的元素
	(5)	Selector:nth-last-child(n): 		匹配符合 Selector 选择器，而且必须是其父元素的倒数第 n 个子节点的元素
	(6)	Selector:only-child:				匹配符合 Selector 选择器，而且必须是其父元素的唯一子节点的元素
	(7) Selector:first-of-type:			匹配符合 Selector 选择器，要求与它同类型、同级的兄弟元素中的第一个元素	
	(8)	Selector:last-of-type:			匹配符合 Selector 选择器，要求与它同类型、同级的兄弟元素中的最后一个元素
	(9)	Selector:nth-of-type(n):			匹配符合 Selector 选择器，要求与它同类型、同级的兄弟元素中的第 n 个元素
	(10)Selector:nth-last-of-type(n):	匹配符合 Selector 选择器，要求与它同类型、同级的兄弟元素中的倒数第 n 个元素
	(11)Selector:only-of-type:			匹配符合 Selector 选择器，要求与它同类型、同级的兄弟元素中的唯一一个元素
	(12)Selector:empty:					匹配符合 Selector 选择器，而且其内部没有任何子元素（包括文本节点）的元素