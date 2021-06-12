# HTML-Summary
web应用技术HTML总结
# HTML总结

[TOC]



### 1.HTML简介：

HTML全称为HyperText Markup Language，意为超文本编辑语言，HTML是用来构建web页面的。

> "超文本"（hypertext）是指连接单个网站内或多个网站间的网页的链接

HTML负责构建网页的内容的含义与结构，CSS负责描述网页的表现和展示结果，JavaScript或者typescript负责网站的功能和行为。

HTML不是一门编程语言，而是用于定义内容结构的标记语言。

可以通过F12或者右键查看源代码的方式查看任何一个网页的HTML文档。

### 2.HTML文档结构

演示代码：

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
  <title>页面标题</title>
</head>
<body>
  <h1>我的第一个Web页</h1>
  <p>当前有点丑：)</p>
</body>
</html>
```

HTML 使用"标记"（markup）来注明文本、图片和其他内容，以便于在浏览器中显示。HTML 标记包含一些规定的"元素"如 <head>，<title>，<body>，<header>，<footer>，<article>，<section>，<p>,<div>，<span>，<img>，<aside>，<audio>，<canvas>，<datalist>，<details>，<embed>，<nav>，<output>，<progress>，<video> 等等。

![element](https://qige.io/web/brief-html/img/f63738cc51ebfa14.png)

如图是一个元素(element)的剖析：

1. 开始标签（Opening tag）：包含元素的名称（本例为 p），被左、右角括号所包围。表示元素从这里开始或者开始起作用 —— 在本例中即段落由此开始。
2. 结束标签（Closing tag）：与开始标签相似，只是其在元素名之前包含了一个斜杠。这表示着元素的结尾 —— 在本例中即段落在此结束。初学者常常会犯忘记包含结束标签的错误，这可能会产生一些奇怪的结果。
3. 内容（Content）：元素的内容，本例中就是所输入的文本本身。
4. 元素（Element）：开始标签、结束标签与内容相结合，便是一个完整的元素。

HTML文档的结构：

1. `<!DOCTYPE html>`: 声明文档类型。出于历史原因需要，现在可有可无。
2. `<html></html>`: `<html>`元素。这个元素包裹了整个完整的页面，是一个根元素，**其它元素都嵌套到其中**。
3. `<head></head>`: `<head>`元素。 这个元素是一个容器，它包含了所有你想包含在HTML页面中但不想在HTML页面中显示的内容。这些内容包括你想在搜索结果中出现的关键字和页面描述，CSS样式，字符集声明等等。
4. `<meta charset="utf-8">`: 这个元素设置文档使用utf-8字符集编码，utf-8字符集包含了人类大部分的文字。基本上他能识别你放上去的所有文本内容。毫无疑问要使用它，并且它能在以后避免很多其他问题。
5. `<link rel="shortcut icon" href="favicon.ico" type="image/x-icon">`: 指定页面的图标，出现在浏览器标签上。(注意图标文件放置的目录)
6. `<title></title>`: 设置页面标题，出现在浏览器标签上，当你标记/收藏页面时它可用来描述页面。
7. `<body></body>`: `<body>`元素。 包含你能在页面看到的所有内容，包括文本，图片，音频，游戏等等。

### 3.HTML文档相关说明：

#### 注释：

演示代码：

```
<p>我在注释外，可以显示！</p>
<!-- <p>我在注释内！浏览器将忽略我</p> -->
```

注释快捷键： ctrl+/

注：HTML文件不区分大小写标签，但建议全部使用小写。

#### 空元素：只有一个开始标签

一般标签拥有开始标签、内容、结束标签。但有一些只有一个开始标签，比如

`<br>换行<hr>水平分割线<input>输入框<img>图片<a>超链接`等等

> 元素之间是可以嵌套使用的,比如说可以将图片嵌入到超链接中,表现出来就是点击图片跳转

#### 元素的属性:

元素是可以有相关属性的。属性包含元素的额外信息，这些信息不会在浏览器中显示出来。

演示代码:

```
<!-- 带属性的段落输入框 -->
<p title="这是个title属性">鼠标移上来试试！</p>
<!-- 带属性的输入框 -->
<input type="text">
<input type="password">
```

> 一个属性必须包含如下内容：
>
> 1. 一个空格，在属性和元素名称之间。(如果已经有一个或多个属性，就与前一个属性之间有一个空格。)
> 2. 属性名称，后面跟着一个 = 号。
> 3. 一个属性值，由一对引号 "" 引起来。

### 4.HTML文档的标题(heading)

HTML提供的一到六级标题,分别对应`<h1><h2>~<h6>`.

```
<h1>This is heading 1</h1>
<p>This is some text.</p>
<hr>
<h2>This is heading 2</h2>
<p>This is some other text.</p>
<hr>
```

### 5.文本格式

需要知道的文本格式如下:

`<mark>标记/高光<del>删除线<s>删除线<ins><u>下划线<small>小字显示<strong>加粗<em>斜体`

演示代码:

```
<p>You can use the mark tag to <mark>highlight</mark> text.</p>
<p><del>This line of text is meant to be treated as deleted text.</del></p>
<p><s>This line of text is meant to be treated as no longer accurate.</s></p>
<p><ins>This line of text is meant to be treated as an addition to the document.</ins></p>
<p><u>This line of text will render as underlined</u></p>
<p><small>This line of text is meant to be treated as fine print.</small></p>
<p><strong>This line rendered as bold text.</strong></p>
<p><em>This line rendered as italicized text.</em></p>
```

VScode运行效果:

![image-20210330202355405](C:\Users\Admin\AppData\Roaming\Typora\typora-user-images\image-20210330202355405.png)

### 6.超链接

#### 超链接

语法示例:

```
<a href="https://www.baidu.com/" target="_blank">百度一下</a>
```

> 1. `href`即为要跳转去的地址 URL（Uniform Resorce Locator)
> 2. `target`属性为`_blank`表示在新的页面打开超链接（默认是在当前页面打开即`_self`）
> 3. 超链接标签包含的内容（当前为文字"百度一下"）即为显示在页面上供用户点击的,修改成图片的话变为超链接图片

#### 锚点

锚点，也称为书签，用于标记页面的某个元素或位置。通过锚点，我们可以轻易的在长页面内实现跳转。

先使用`id`属性生成某元素的锚点，然后再使用超链接指向该锚点即可。

示例代码:

```
<!-- 文档其余部分 -->
<h2 id="C4">第四章 论零号病人的重要性</h2>
<!-- 文档其余部分 -->
<a href="#C4">跳到第四章</a>
<!-- 文档其余部分 -->
...
```

> 1. 元素的`id`值必须是唯一的，也即页面不能再有其它元素的`id`值为`C4`
> 2. 超链接中的地址需要有`#`符号

### 7.图片及文件路径

#### 图片

在页面插入一张图片如下：

```
<img src="https://mdbootstrap.com/img/logo/mdb192x192.jpg" alt="MDB Logo" width="200" height="200">
```

说明：

1. `src`属性为要显示图片文件的位置 URL，即图片文件的路径
2. `alt`属性当获取图片出现问题时显示的文字（占位符）
3. 可为图片指定高宽度，但不建议（可能导致图片变形）

**提示：** 对于小尺寸的图片，现在可采用 **base64** 编码进行，可提高页面加载速度，提升用户体验。[可前往一试](https://c.runoob.com/front-end/59)。

#### 文件路径

为获取图片文件，我们需要指定该文件位于何处，这称为文件路径。文件路径有相对路径和绝对路径两种。

上面图片的例子即为绝对路径。下面是相对路径的例子：

| 例子                               | 解释                                   |
| ---------------------------------- | -------------------------------------- |
| `<img src="picture.jpg">`          | 该图片文件与当前文档在同一目录中       |
| `<img src="./images/picture.jpg">` | 该图片文件在当前目录下的`images`目录中 |
| `<img src="../picture.jpg">`       | 该图片文件在上一级目录中               |

### 8.表格 table

有时，页面的内容需要用表格来进行呈现。我们使用`<table>`等标签即可：

```
  <table>
    <tr>
      <th>Firstname</th>
      <th>Lastname</th>
      <th>Age</th>
    </tr>
    <tr>
      <td>Jill</td>
      <td>Smith</td>
      <td>50</td>
    </tr>
    <tr>
      <td>Eve</td>
      <td>Jackson</td>
      <td>94</td>
    </tr>
  </table>
```

代码中，`<tr>`表示行, `<td>`表示行中的单元, `<th>`是表头的单元（将会加粗显示）

### 9.列表 List

我们也可以使用列表来呈现内容，分为无序列表和有序列表。

#### 无序列表

```
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

无序列表使用`<ul>`标签，默认使用**实心圆点**作为每项的标志，其它的标志可以是空心圆`circle`，实心方块`square`以及不出现标志。

```
<ul type="square">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

#### 有序列表

```
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

有序列表使用`<ol>`标签，默认使用**数字**作为每项的标志，其它的标志可以是大写字母`A`，小写字母`a`，罗马字母`i`等。

```
<ol type="a">
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

### 10. 表单 Form

当网站需要获取我们的一些信息如：用户名、密码、选择买什么、买多少、提出意见等等时，我们就需要使用表单（form）来让用户填写或选择。

```
<form>
  <!-- 文本框，注意有 placeholder 提示符 -->
  用户名：<br>
  <input type="text" name="name" placeholder="请输入用户名"><br>
  <!-- 密码框 -->
  密码：<br>
  <input type="password" name="ps" placeholder="请输入密码"><br>
  年龄：<br>
  <!-- 数字输入框，注意 min 和 value 属性-->
  <input type="number" name="age" min="18" value="18"><br>
  <!-- 单选按钮, 注意 checked 属性 -->
  性别：<br>
  <input type="radio" name="gender" value="male" checked> 男<br>
  <input type="radio" name="gender" value="female"> 女<br>
  <input type="radio" name="gender" value="other"> 其它<br>
  <!-- 下拉列表，注意 selected 属性 -->
  党派：<br>
  <select name="party">
    <option value="D">民主党</option>
    <option value="R" selected>共和党</option>
    <option value="N">无党派</option>
  </select><br>
  <!-- 多选框 -->
  您有哪些交通工具：<br>
  <input type="checkbox" name="vehicle1" value="Bike"> 自行车<br>
  <input type="checkbox" name="vehicle2" value="Motocycle" checked> 摩托车<br>
  <input type="checkbox" name="vehicle3" value="Car"> 轿车<br>
  <input type="checkbox" name="vehicle4" value="Jet"> 飞机<br>
  <!-- 日期选择器 -->
  您的工作日期：<br>
  <input type="date"><br>
  <!-- 文件选择器 -->
  上传您的照片:<br>
  <input type="file" name="photo"><br>
  <!-- 文本输入区域，注意 rows 和 cols 属性 -->
  您的建议：<br>
  <textarea name="message" rows="5" cols="30">
    The cat was playing in the garden.
  </textarea><br><hr>
  <!-- 表单提交/重置按钮，将表单中的数据取消或传输给服务器端进行处理 -->
  <input type="submit" value="提 交">
  <input type="reset" value="重 置">
</form>
```

## 11.其他

HTML 的元素可以以称为**区块** 或 **内联**的方式进行显示。

#### 区块元素

区块元素在浏览器显示时，通常会以**新行**来开始（和结束）。如：`<h1>, <pre>, <ul>, <table>，<`div> 等。

```
<h2>区块元素</h2>
<div>Hello</div>
<div>World</div>
<p>单独一行</p>
```

#### 内联元素

内联元素相反，他们总是一个接一个进行显示，不会新起一行。如： `<span>, <input>, <td>, <a>, <img>`等。

```
<h3>下面的元素将在一行中显示</h3>
<span>姓名：</span>
<input name="username">
<span>哈哈哈</span>
<a href="https://google.com/">Google</a>
<img src="https://mdbootstrap.com/img/logo/mdb192x192.jpg">
```

#### 预设格式

如果你想在网页中展示一首诗或一些特别格式的文本，那么请使用`pre`标签。

```
<!-- pre标签中的内容将保持格式不变 -->
<pre>
              我如果爱你——
              绝不象攀援的凌霄花，
              借你的高枝炫耀自己；

              我如果爱你——
              绝不学痴情的鸟儿，
              为绿荫重复单调的歌曲；

              也不止像泉源，
              常年送来清凉的慰藉；

              也不止像险峰，
              增加你的高度，衬托你的威仪。

              甚至日光。
              甚至春雨。

              不，这些都还不够！
              我必须是你近旁的一株木棉，
              作为树的形象和你站在一起。

              根，紧握在地下，
              叶，相触在云里。

              每一阵风过，
              我们都互相致意，
              但没有人，
              听懂我们的言语。

              你有你的铜枝铁干，
              像刀，像剑，
              也像戟；

              我有我红硕的花朵，
              像沉重的叹息，
              又像英勇的火炬。

              我们分担寒潮、风雷、霹雳；
              我们共享雾霭、流岚、虹霓。
              仿佛永远分离，
              却又终身相依。

              这才是伟大的爱情，
              坚贞就在这里：
              爱——
              不仅爱你伟岸的身躯，
              也爱你坚持的位置，足下的土地。
</pre>
```

#### 特殊字符

考虑下面的代码将显示成什么？

```
<p>有多          远，滚                         多远！</p>
```

或者你希望在页面显示一段 HTML 的源代码，你打算用标签`<pre>`:

```
<pre>
  <h1>这是个一级标题</h1>
  <p>这是一个段落<p>
  <a href="https://twitter.com/">眼见何事，情系何处，身处何方，心思何人</a>
<pre>
```

以上代码将得不到你想要的结果。
原因是：在 HTML 中，某些字符是预留的。
在 HTML 中不能使用小于号（<）和大于号（>），这是因为浏览器会误认为它们是标签。
如果希望正确地显示预留字符，我们必须在 HTML 源代码中使用字符实体（character entities）

```
<p>有多&nbsp;&nbsp;&nbsp;远，滚&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;多远！</p>
<hr>
<h2>test.html</h2>
<pre>
  &lt;h1&gt;这是个一级标题&lt;/h1&gt;
  &lt;p&gt;这是一个段落&lt;p&gt;
  &lt;a href="https://twitter.com/"&gt;眼见何事，情系何处，身处何方，心思何人&lt;/a&gt;
<pre>
```

特殊字符可参考[ISO-8859-1 字符实体手册](https://www.runoob.com/tags/ref-entities.html)
