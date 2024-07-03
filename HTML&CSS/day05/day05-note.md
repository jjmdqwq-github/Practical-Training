**- 兄弟选择器**

给指定选择器后面紧跟的那个选择器选中的标签设置属性

```css
选择器1+选择器2 {
	属性:值;
}
```

给指定选择器后面的所有选择器选中的所有标签设置属性

```css
选择器1~选择器2 {
	属性:值;
}
```

**- 序选择器**

**:first-child** 选中同级别中的第一个标签

**:last-child** 选中同级别中的最后一个标签

**:nth-child(n)** 选中同级别中的第n个标签

**:nth-child(odd)** 选中同级别中的所有奇数

**:nth-child(even)** 选中同级别中的所有偶数

**:nth-child(xn+y)** x和y是用户自定义的, 而n是一个计数器，从0开始递增

**- 动态伪类选择器**

**E:link**（链接伪类选择器）：选择匹配的E元素，而且匹配元素被定义了超链接并未被访问过。

**E:visited**（链接伪类选择器 ）：选择匹配的E元素，而且匹配元素被定义了超链接并已被访问过。

**E:active**（用户行为选择器）：选择匹配的E元素，且匹配元素被激活。

**E:hover** （用户行为选择器）： 选择匹配的E元素，且用户鼠标停留在元素E上。

**- 否定伪类**

可以从已选中的元素中剔除出某些元素

```css
p:not(.hello) {
	background-color: yellow;
}
```

**- 为元素选择器**

使用伪元素来表示元素中的一些特殊的位置

**::after**

表示元素的最后边的部分

一般需要结合content这个样式一起使用，

通过content可以向after的位置添加一些内容

 **::before**

表示元素最前边的部分

一般需要结合content这个样式一起使用，

通过content可以向before的位置添加一些内容 

 **::first-letter**

为第一个字符来设置一个样式

 **::first-line** 

为第一行设置一个样式

# CSS三大特性

### - 继承性

给父元素设置一些属性，子元素也可以使用，我们就称之为继承性

1.并不是所有的属性都可以继承, 只有以color/font-/text-/line-开头的属性才可以继承

2.在CSS的继承中不仅仅是儿子可以继承, 只要是后代都可以继承

3.继承性中的特殊性

​	3.1 a标签的文字颜色和下划线是不能继承的，当做子元素

​	3.2 h标签的文字大小是不能继承的，在做子元素

### - 层叠行

层叠性就是CSS处理冲突的⼀种能力

层叠性只有在多个选择器选中"同一个标签", 然后又设置了"相同的属性", 才会发生层叠性

### - 优先级

当多个选择器选中同一个标签, 并且给同一个标签设置相同的属性时, 如何层叠就由优先级来确定

**- !important**

用于提升某个直接选中标签的选择器中的某个属性的优先级的，可以将被指定的属性的优先级提升为最高

**- 优先级权重**

当多个选择器混合在一起使用时, 我们可以通过计算权重来判断谁的优先级最高

**- 权重计算规则**

1. 内联样式，如: style="..."，权值为1000。

2. ID选择器，如：#content，权值为0100。

3. 类，伪类、属性选择器，如.content，权值为0010。

4. 标签选择器、伪元素选择器，如div p，权值为0001。

5. 通配符、复合选择器（+、>、~等）、否定伪类（：not）没有影响，权值为0000。

6. 继承的样式没有权值