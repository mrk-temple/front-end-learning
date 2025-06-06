# CSS 简介
*什么是CSS?*
**CSS全名是 `Cascading Style Sheets`,中文名`层叠样式表`**
==用于定义网页样式和布局的样式表语言==
- 通过CSS,你可以指定页面中各个元素的颜色、字体、大小、间距、边框、背景等样式,从而实现更精确的页面设计

# CSS 语法
**CSS通常由选择器、属性和属性值组成,多个规则可以组合在一起,以便同时应用多个样式**
```
选择器{
属性1:属性值1;
属性2:属性值2;
}
```
1. 选择器的声明中可以写无数条属性
2. 声明的每一行属性,都需要以英文分号结尾;
3. 声明中的所有属性和值都是以键值对这种形式出现的;

- 示例:
```
/*这是一个 p 标签选择器 */
p {
color: blue;
font-size: 16px;
}
```
# CSS 三种导入方式
*下面是三种常见的CSS导入方式：*

1. `内联样式(Inline Styles)`
2. `内部样式表(Internal Stylesheet)`
3. `外部样式表(External Stylesheet)`

==三种导入方式的优先级:`内联样式`>`内部样式表`>`外部样式表`==

# 选择器
**选择器是CSS中的关键部分,它允许你针对特定元素或一组元素定义样式**
 
 - ==元素选择器==
 - ==类选择器==
 - ==ID选择器==
 - ==通用选择器==
 - ==子元素选择器==
 - ==后代选择器(包含选择器)==
 - ==并集选择器(兄弟选择器)==
 - ==伪类选择器==


# 块、行内、行内块元素

### 块元素(block):
- 块级元素通常会从新行开始,并占据整行的宽度
- 可以包含其他块级元素和行内元素

### 行内元素(inline):
- 行内元素通常在同一行内呈现,不会独占一行
- 它们只占据其内容所需的宽度,而不是整行的宽度
- 行内元素不能包含块级元素,但可以包含其他行内元素

### 行内块元素(Inline-block):
- 水平方向上排列,但可以设置宽度、高度、内外边距等块级元素的属性
- 行内块元素可以包含其他行内元素或块级元素


# 盒子模型
![[屏幕截图 2025-05-25 141030.png]]

# 盒子模型相关属性

| 属性名            | 说明                                       |
| -------------- | ---------------------------------------- |
| `内容(Content)`  | 盒子包含的实际内容，比如文本、图片等。                      |
| `内边距(Padding)` | 围绕在内容的内部,是内容与边框之间的空间。可以使用 padding属性来设置。  |
| `边框(Border)`   | 围绕在内边距的外部,是盒子的边界。可以使用 border`属性来设置。      |
| `外边距(Margin)`  | 围绕在边框的外部,是盒子与其他元素之间的空间。可以使用 margin属性来设置。 |


# 传统网页布局方式
在学习浮动之前,先了解传统的网页布局方式

网页布局方式有以下五种:

- 标准流(普通流、文档流):网页按照元素的书写顺序依次排列
- 浮动
- 定位
- `Flexbox`和`Grid`(自适应布局)
标准流`是由块级元素和行内元素按照默认规定的方式来排列,块级就是占一行,行内元素一行放好多个元素。`

# 浮动
*元素脱离文档流,根据开发者的意愿漂浮到网页的任意方向。*

==浮动定义：**属性用于创建浮动框,将其移动到一边,直到左边缘或右边缘触及包含块或另一个浮动框的边缘,这样即可使得元素进行浮动**==
```
选择器{
	float: left/right/none;
}
```
###### 注意:浮动是相对于父元素浮动,只会在父元素的内部移动


# 浮动的三大特性
*学习浮动要先了解浮动的三大特性:*

- 脱标:脱离标准流
- 一行显示,顶部对齐
- 具备行内块元素特性

# 定位
*定位布局可以精准定位，但缺乏灵活性*
##### 定位方式：
- `相对定位`:相对于元素在文档流中的正常位置进行定位。
- `绝对定位`:相对于其最近的已定位祖先元素进行定位,不占据文档流。
- `固定定位`:相对于浏览器窗口进行定位。不占据文档流,固定在屏幕上的位置,不随滚动而移动。
- 