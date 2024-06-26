# HTML与CSS

---

### 什么是HTML？什么是CSS？

HTML是HyperText MArkup Language（超文本标记语言）

CSS（Cascading Style Sheets）

### HTML和CSS之间的关系

HTML是网页内容的载体，CSS样式是表现。

*HTML就像是一个人，而CSS就像是衣服和化妆品，用来装饰HTML*

**结构**：HTML用于描述页面的结构

**表现**：CSS用于控制页面中元素的样式

**行为**：JavaScript用于响应用户操作

### Hello HTML

打开VSCode，新建后缀名为.html的文件，输⼊"!"或"html:5"生成基本的html5结构

### 语法

**注释**

<!-- 注释内容 -->

**元素**

单标签元素，只有一个标签

``<meta />、<img />、<br />``

双标签元素，由开始标签和结束标签组成

``<div></div>、<p></p>``

![image-20240626223619465](C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20240626223619465.png)

**属性**

HTML标签都拥有自己的属性，属性应该出现在元素的开始标签内部，属性名和属性值通过“=”分割，属性与属性之间通过空格分隔，属性名不区分大小写，属性值区分大小写并且属性值可以使用双引号引起来。

核心属性——绝大多数标签都具有的属性：title、id、class、style

title：描述信息

``<div title="div1">div1</div>``

id：唯一标识

``<div id="div1">div1</div>``

class：标识一类元素

``<div class="box1">box1</div>``

style 样式

``<div style="color: red;">我是⼀个div</div>``

### 块级元素

搭建网页结构

特点：

- 独占一行空间
- 默认宽度为100%
- 高度由子元素或内容决定
- 可以通过css指定其宽度

元素：html、body、div、p、h1~h6、ul->li、ol->li、dl->dd/dt、header、footer、nav、article、section、aside、address...

### 行内元素

在结构中填充网页内容

特点：

- 与其他行内元素共享一行空间
- 宽高由自身决定
- 由于不用来搭建网页结构，所以也无需通过css指定其宽度
- 行内元素中不可以嵌套块元素

元素：span、a、img、strong、b、i、em、sub、sup...