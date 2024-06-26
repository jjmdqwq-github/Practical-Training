# 基础标签的使用

---

### - h标签

标题标签

在HTML中，⼀共有六级标题标签，h1~h6，h1最大，h6最小

``<h1>这是⼀个h1标签</h1>``

### - p标签

段落标签

表示内容中的一个自然段，p标签中的文字，会独占一行，并且段与段之间会有⼀个间距

``<p>这是一个p标签<p>``

### - br标签

``<br>``换行



### **-hr**标签

``<hr>``分割线

---



### **-** 字符实体

```
空格 &nbsp;
<	&lt
>	&gt
“	&quot
&	&amp;
'	&apos
```

### - img标签

显示图片

``<img src="图⽚的url或本地路径地址" alt="" width="100px"height="100px" title="">``

src：设置⼀个图片的路径（绝对路径和相对路径，最好使用相对路径）

alt：可以用来设置在图片不能显示的时，对图片的描述

img：标签的其他属性

width：设置图片的宽度

height：设置图片的⾼度

title：用于告诉浏览器，鼠标悬停的时候，需要弹出的描述框中显示什么内容。

### - a标签

超链接，页面与页面之间的跳转

```html
<a href="指定需要跳转的⽬标界⾯">需要展现给⽤户查看的内容</a>
<a href="https://www.baidu.com" target="_blank" title="百度">百度⼀下</a>
```

target：属性用于控制如何跳转

\_self：用于当前的选项卡中进行跳转，也就是不新建页面跳转，默认就是_self

\_blank：用于在新的选项卡中进行跳转，也就是新建页面跳转

title：效果和img标签的title类似

###  - mailto链接

⼀种html链接，能够设置你电脑中邮件的默认发送信息

``<a href="mailto:name@email.com">Email</a>``

### - base标签

统⼀指定当前页面中所有的a标签需要如何打开

1.base标签必须要写在head标签之间

2.如果既在base中指定了target又在a标签中指定了target，那么浏览

器会按照a标签中指定的来执行

### - 假链接

点击之后不需要跳转的链接

1.# 直接回到页面的顶部

2.javascript：不会自动回到页面的顶部

```html
<a href="#">回到顶部</a>
<a href="javascript:">点我啊</a>
```

### **-**  锚点

通过a标签跳转到指定的位置

```html
<a href="#center">跳转</a>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<p id="center">我是中部</p>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
```

a标签除了可以跳转到当前界面的指定位置以外，还可以在跳转到其它界面的时候直接跳转到其它界面的指定位置

```html
//a.html
<a href="b.html#bottom" target="_blank">跳转</a>
```

```html
//b.html
<p id="bottom">找到我</p>
```

### - video(H5新增)

播放视频

``格式:<video src=""></video>``

src：告诉video标签需要播放的视频地址

autoplay：用于告诉video标签是否需要自动播放视频

controls：用于告诉video标签是否需要控制条

poster：用于告诉video标签视频没有播放之前显示的占位图片

loop：一般用于做广告视频，用于告诉video标签视频播放完毕之后是否需要循环播放

muted：静音

width/height：和img标签中的⼀模⼀样

### - audio(H5新增)

播放音频

```html
<audio src=""></audio>
<audio>
	<source src="" type="">
</audio>
```

audio标签的使用和video标签的使用基本⼀样，video中能够使用的属性在audio标签中大部分都能够使用，并且功能都⼀样，只不过有3个属性不能用：height/width/poster

