# 功能元素

---

## 列表标签

### HTML中列表标签的分类

无序列表

有序列表

定义列表

### - 无序列表

无前后之分

```html
<ul>
	<li>需要显示的条目内容</li>
</ul>

<ul type="value"></ul>
```

disc       默认值 实心圆
circle     空心圆
square  实心方块

### - 有序列表

有前后之分

```html
<ol>
	<li></li>
</ol>

<ol type="A"></ol>
1 默认值。数字有序列表。（1、2、3、4）
a 按字母顺序排列的有序列表，小写。（a、b、c、d）
A 按字母顺序排列的有序列表，大写。（A、B、C、D）
i 罗⻢字母，小写。（i, ii, iii, iv）
I 罗⻢字母，大写。（I, II, III, IV）
```

### - 定义列表

不常用

```html
<dl>
	<dt></dt>
	<dd></dd>
	<dt></dt>
	<dd></dd>
</dl>
```

### - 表格标签

用来给一堆数据添加表格语义

```html
<table>
    <tr>
        <td>姓名</td>
        <td>年龄</td>
        <td>身⾼</td>
    </tr>
    <tr>
        <td>张三</td>
        <td>19</td>
        <td>1.78</td>
    </tr>
</table>
```

#### - 宽度和高度的属性

width/height可以给table标签和td标签使用

#### -水平对齐和垂直对齐的属性

水平对齐align可以给table标签和td标签使用

垂直对齐valign只能给tr标签和td标签使用

align: left center right

valign: top mid bottom

#### - 外边距和内边距的属性

只能给table标签使用

**cellspacing**外边距就是单元格和单元格之间的距离,

**cellpadding**内边距就是单元格的边框和文字之间的间隙

#### - 细线表格

1. 给table标签设置`bgcolor="black" cellspacing = "1px"`

2. 给tr标签设置`bgcolor="white"`

#### - 单元格合并

1. 水平方向上的单元格合并`<td colspan="2"></td>`

2. 垂直方向上的单元格合并`<td rowspan="2"></td>`

#### - 表格的完整结构

```html
<table>
    <caption>表格的标题</caption>
    <thead>
        <tr>
            <th>每一列的标题</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>数据</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>数据</td>
        </tr>
    </tfoot>
</table>
```

caption作用：指定表格的标题

thead作用：指定表格的表头信息

tbody作用：指定表格的主体信息

tfoot作用：指定表格的附加信息

### - form表单

专门用于收集用户信息

```html
<form action="提交的服务器接口地址">
	<表单元素>
</form>
```

#### 常用的表单元素

**- fieldset组件**

用于在⼀个web表单中对多个控件和标签进行分组

```html
<form action="">
    <fieldset>
        <legend>请登录</legend>
        账号:<input type="text"><br>
        密码:<input type="password">
        <input type="submit">
    </fieldset>
</form>
```

**- input标签**

1. 明文输入框

```html
<input type="text" name="account" placeholder="请输入用户名">
```

2. 暗文输入框

```html
<input type="password" name="password" placeholder="请输入密码">
```

3. 输入框设置默认值

```HTML
<input type="xxx" value="xxx">
```

4. 单选框

```html
<input type="radio" name="xx" value="xxx">
```

5. 多选框

```html
<input type="checkbox" name="xxx" value="xxx">
```

6. 提交按钮

```html
<input type="submit">
```

7. 重置按钮

```html
<input type="reset" value="xx">
```

8. 隐藏域

```html
<input type="hidden" name="xx" value="xxx">
```

等，不做过多记录

**- select标签**

用于定义下拉列表

```html
<select>
    <optgroup label="分组名称">
        <option>列表数据</option>
    </optgroup>
</select>
```

**- textarea标签**

定义一个多行输入框

```html
<textarea></textarea>
```

**- datalist标签**

给输入框绑定待选项

```html
<input type="text" list="xxx">
<datalist id="xxx">
    <option>xxx</option>
</datalist>
```

**- 邮箱** `<input type="email">`

可以自动校验输入的内容是否符合邮箱的格式

**- 域名** `<input type="url">`

可以自动校验输入的内容是否是URL地址

**- 数字** `<input type="number">`

输入框中只能输入数字

**- 时间** `<input type="date">`

可以通过日历来选择时间

**- 颜色** `<input type="color">`

可以通过取色板来选择颜色
