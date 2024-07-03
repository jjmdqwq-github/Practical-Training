# 文本属性

### 颜色属性

1. 英文单词

   ​	一般情况下常见的颜色都有对应的英文单词，但是英文单词能够表达的颜色是有限制的，也就是说不是所有的颜色都能够通过英文单词来表达

2. rgb

   rgb其实就是三原色, 其中r(red 红色) g(green 绿色) b(blue 蓝色)，格式: rgb(0,0,0)

3. rgba

   rgba中的rgb和前面讲解的一样, 只不过多了一个a，那么这个a呢代表透明度, 取值是0-1, 取值越小就越透明，例如: rgba(255,0,0,0.2)

4. 十六进制

​	在前端开发中通过十六进制来表示颜色, 其实本质就是RGB，十六进制中是通过每两位表示一个颜色，例如: #FFEE00

### - font-style 用于打开和关闭斜体文本

格式：font-style: italic;

取值：

normal：正常的，默认就是正常的

italic：倾斜的

### - font-weight 为字体设置粗细程度

格式：font-weight: bold;

取值：

bold 加粗

bolder 比加粗还要粗

lighter 细线，默认就是细线

### - font-size 为文字指定大小

格式：font-size: 30px;

通过font-size设置大小一定要带单位，也就是一定要写px快捷键

### - font-family 为文字指定特殊的字体，浏览器只会使用浏览器可以访问到的的字体

格式：font-family: "楷体";

通用字体 (直接使用，不需要加引号)

1. serif: 有衬线的字体,笔画结尾有特殊的装饰线或衬线

2. sans-serif: 无衬线的字体，笔画结尾是平滑的字体

3. monospace: 等宽字体，用于代码，字体中每个字宽度相同

4. cursive: 草书，这种字体有的有连笔，有的还有特殊的斜体效果。

5. fantasy: 装饰字体 ，具有特殊艺术效果的字体

### - 缩写格式

缩写格式: font:style weight size family;

例如: font:italic bold 10px "楷体";

### - 文本装饰的作用

格式：text-decoration: underline;

取值：

1. underline 下划线

2. line-through 删除线

3. overline 上划线
4. none 什么都没有

### - 文本水平对齐的属性

格式：text-align：right;

取值：

1. left 左
2. right 右
3. center 中

### - 文本缩进的属性

格式：text-indent：2em

取值：2em，其中是em单位, 一个em代表缩进一个文字的宽度

### - 设置或者取消字体改变

格式：text-transform：capitalize 

取值：

1. none 防止任何改变
2. uppercase 将文本转换为大写
3. lowercase 将文本转换为小写
4. capitalize 将所有单词第一个字母转为大写
5. full-width 转换为类似于一个等宽字体

### - 字体阴影

格式：text-shadow: h-shadow v-shadow blur color;

取值：

1. none 取消所有阴影
2. h-shadow 必需，水平阴影的位置，允许负值
3. v-shadow 必需，垂直阴影的位置，允许负值
4. blur 可选，模糊的距离
5. color 可选，阴影的颜色

# 列表样式

### - list-style-type 设置列表项标志类型

取值：

1. none 不显示列表项的标记
2. disc 实心圆点 (默认值)
3. circle 空心圆点
4. square 实心方块
5. decimal 十进制阿拉伯数字
6. cjk-decimal 中日韩十进制数

### - list-style-position 设置列表项标志出现的位置

取值：

1. outside：列表项标志出现在主块框的外部
2. inside：列表项标志出现在主块框的内部

### - list-style-image 自定义设置列表项标志

取值：url(): 指定图标位置

### - list-style

我们最常用的就是list-style:none; 设置没有任何样式，通过CSS去自定义样式

# 其他样式

### - line-height

设置文本的行高 取值为绝对单位或者相对单位

### - display

取值：

1. inline 行内显示，宽高无效

2. block 块级显示，宽高无效

3. inline-block 为了能够让元素既能够不独占一行, 又可以设置宽度和高度, 那么就出现了行内块级元素， 行内显示同时宽高有效

4. none 不显示，不占据屏幕空间

5. flex 伸缩盒布局

### - visibilty

取值：

1. hidden 隐藏，占据屏幕空间
2. visible 显示

### - opacity

透明度，0-1之间的取值，取值为0的时候隐藏，占据屏幕空间

### - overflow 溢出处理

取值：

1. 超出内容隐藏
2. auto 超出产生滚动条
3. scroll 滚动条

### - cursor

指定光标的样式

取值在此不做记录
