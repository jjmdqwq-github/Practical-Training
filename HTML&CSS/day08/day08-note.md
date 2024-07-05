# CSS布局

### 标准流（文档流/普通流）

**特点：**

块元素：

1. 块元素在标准流中会独占一行，块元素会自上向下排列
2. 块元素在标准流中默认宽度是父元素的100%
3. 块元素在标准流中的高度默认被内容撑开

内联元素：

1. 内联元素在标准流中只占自身的大小，会默认从左向右排列，如果一行中不足以容纳所有的内联元素，则换到下一行，继续自左向右
2. 在标准流中，内联元素的宽度和高度默认都被内容撑开

3. 在标准流中有两种排版方式, 一种是垂直排版, 一种是水平排版

   垂直排版, 如果元素是块级元素, 那么就会垂直排版

   水平排版, 如果元素是行内元素/行内块级元素, 那么就会水平排版

4. 如果希望块元素在页面中水平排列，可以使块元素脱离标准流(文档流/普通流)，使用float来使元素浮动，从而脱离标准流(文档流/普通流)

### 浮动流

**特点：**

1. 在浮动流中是不区分块级元素/行内元素/行内块级元素的，无论是块级元素/行内元素/行内块级元素都可以水平排版
2. 在浮动流中无论是块级元素/行内元素/行内块级元素都可以设置宽高

**- 浮动元素字围现象**

​	浮动元素不会挡住没有浮动元素中的文字, 没有浮动的文字会自动给浮动的元素让位置,这个就是浮动元素字围现象

**- 高度塌陷**

​	为子元素设置浮动以后，子元素会完全脱离文档流，此时将会导致子元素无法撑起父元素的高度，导致父元素的高度塌陷。由于父元素的高度塌陷了，则父元素下的所有元素都会向上移动，这样将会导致页面布局混乱。

**- 解决高度塌陷**

1. 将父元素的高度写死，但是一旦高度写死，父元素的高度将不能自动适应子元素的高度，所以这种方案是不推荐使用的。

2. 可以直接在高度塌陷的父元素的最后，添加⼀个空白的div，由于这个div并没有浮动，所以他是可以撑开父元素的高度的，然后在对其进行清除浮动，这样可以通过这个空白的div来撑开父元素的高度，基本没有副作用。使用这种方式虽然可以解决问题，但是会在页面中添加多余的结构。

   clear属性取值:

   1. none: 默认取值, 按照浮动元素的排序规则来排序(左浮动找左浮动, 右浮动找右浮动)

   2. left: 不要找前面的左浮动元素

   3. right: 不要找前面的右浮动元素

   4. both: 不要找前面的左浮动元素和右浮动元素

3. 通过after伪类

​	可以通过after伪类向元素的最后添加一个空白的块元素，然后对其清除浮动，这样做和添加一个div的原理一样，可以达到一个相同的效果，而且不会在页面中添加多余的div，这是我们最推荐使用的方式，几乎没有副作用。

```css
.clearfix::after {
    /*添加一个内容*/
	content: "";
    /*转换为一个块元素*/
    display: block;
    /*清除两侧的浮动*/
    clear: both;
}
```

### BFC

BFC是一个独立的布局环境，BFC内部的元素布局与外部互不影响

**BFC的布局规则**

1. 内部的Box会在垂直方向一个接着一个地放置。
2. Box垂直方向上的距离由margin决定。属于同一个BFC的两个相邻的Box的margin会发生重叠。
3. 每个盒子的左外边框紧挨着包含块的左边框，即使浮动元素也是如此。
4. BFC的区域不会与float box重叠。
5. BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素，反之亦然。
6. 计算BFC的高度时，浮动子元素也参与计算。

**哪些元素会生成BFC**

1. 根元素
2. float属性不为none
3. position为absolute或fixed
4. display为line-block、table-cell、table-caption、flex、inline-flex
5. overflow不为visible