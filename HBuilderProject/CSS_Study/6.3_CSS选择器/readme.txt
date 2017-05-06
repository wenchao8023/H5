(三) CSS 选择器
	格式：
	Selector{
		property1: value1;
		property2: value2;
	}
	解释：
	Selector(选择器)：决定改样式定义对哪些元素起作用。
	{property1: value1;property2: value2;}(属性定义)：属性定义部分决定这些样式起怎样的作用（字体、颜色、布局等）。

1. 元素选择器<Element.html>
	格式：
	E {...} （E 代表有效的 HTML 元素名）
	
2. 属性选择器<attr.html>
	【元素选择器】也属于【属性选择器】的一个特例
	格式1：E{...}	指定该 CSS 样式对所有 E 元素起作用；
	格式2：E[attr]{...}	指定该 CSS 样式对具有 attr 属性的 E 元素起作用；
	格式3：E[attr  =value]{...}	指定该 CSS 样式对所有包含 attr 属性，且 attr 属性为 value 的 E 元素起作用；
	格式4：E[attr ~=value]{...}	指定该 CSS 样式对所有包含 attr 属性，且 attr 属性的值为以【空格】隔开的系列值，其中某个值为 value 的 E 元素起作用；
	格式5：E[attr |=value]{...}	指定该 CSS 样式对所有包含 attr 属性，且 attr 属性的值为以【字符】分割的系列值，其中第一个值为 value 的 E(Tag) 元素起作用；
	格式6：E[att^="value"]{...}	指定该 CSS 样式对所有包含 attr 属性，且 attr 属性的值为以 value 开头的字符串的 E 元素起作用；
	格式7：E[att$="value"]{...}	指定该 CSS 样式对所有包含 attr 属性，且 attr 属性的值为以 value 结尾的字符串的 E 元素起作用；
	格式8：E[att*="value"]{...}	指定该 CSS 样式对所有包含 attr 属性，且 attr 属性的值为以包含 value 的字符串的 E 元素起作用；
	【注意】：只有第一种形式可以在所有浏览器中运行良好，最后3种 CSS选择器 是 CSS3.0 新增的选择器；
			 定义范围更小的优先级越高
			 多个 CSS 样式定义对同一个 HTML 元素起作用时，该 HTML 元素的显示外观是多个 CSS 样式“迭加”作用的效果，对于冲突属性以优先级更高的 CSS 样式定义起作用；
			 
3. ID选择器<idSelector.html>
	格式1：#idValue: {...}	指定该 CSS 样式对 id 为 idValue 的 HTML 元素起作用。
	格式2：E#idValue: {...}	指定该 CSS 样式仅对 id 为 idValue 的 E 元素起作用
	
4. class选择器<classSelector.html>
	格式：[E].classValue {...}	/* 其中 E 是有效的 HTML 元素 */
	指定该 CSS 定义对 class 属性值为 classValue 的 E 元素起作用；
	如果 E 省略，则指定该 CSS 对所有的 class 属性为 classValue 的元素都起作用。
	【tips】为了让 HTML 页面支持 class 选择器，W3C组织规定几乎所有的 HTML 元素都可以指定 class 属性，该属性的唯一作用就是让 class 选择器起作用。

5. 包含选择器<descendant.html>
	格式：Selector1 Selector2 {...}	/* 其中Selector1 Selector2都是有效的选择器 */
	指定【目标选择器】必须处于【某个选择器对应的元素内部】。

6. 子选择器<child.html>
	格式：Selector1>Selector2 {...}	/* 其中Selector1 Selector2都是有效的选择器 */
	指定【目标选择器】必须是【某个选择器对应的元素的子元素】。
	【tips】与 包含选择器 的不同是
	包含选择器：只要【目标选择器】位于【外部选择器】对应的元素【内部】，即使是“孙子元素”也可；
	子选择器  ：要求【目标选择器】必须作为【外部选择器】对应的元素的【直接子元素】才行
	
7. CSS3.0 新增的兄弟选择器<sibling.html>
	格式：Selector1 ~ Selector2 {...}	/* 其中Selector1 Selector2都是有效的选择器 */
	兄弟选择器匹配与 Selector1 对应的元素后面、能匹配 Selector2 的兄弟节点。
	【tips】出现 Selector1 之后的地方 再出现 Selector2，该 CSS 才会起作用
	条件1：Selector1 必须要出现；
	条件2：Selector1 必须要在 Selector2 之前出现；
	如果 Selector1 在 Selector2 之后出现，那么在 Selector1 之前的 Selector2 就没起作用

8. 选择器组合<group.html>
	格式：Selector1,Selector2,Selector3,... {...}	/* 其中Selector1 Selector2 Selector3 都是有效的选择器 */
