### HTML5标签列表 
- **根元素**
```<html>: 代表HTML或者XHTML文档的根。其他所有元素必须是这个元素的子节点。```

- **HTML标签是分等级的HTML将所有的标签分为两种：**

```
1. 文本级标签：p、span、a、b、i、u、em。文本级标签里只能放文字、图片、表单元素。（a标签里不能放a和input）

2. 容器级标签：div、h系列、li、dt、dd。容器级标签里可以放置任何东西
```

**p标签是一个文本级标签，p里面只能放文字、图片、表单元素。其他的一律不能放。**

- **块级标签``<div>``和``<span>``**

*div和span是非常重要的标签，div的语义是division“分割”； span的语义就是span“范围、跨度”。*

*CSS课程中你将知道，这两个东西，都是最最重要的“盒子”。*

div：把标签中的内容作为一个块儿来对待(division)。必须单独占据一行

`<span>`和`<div>`唯一的区别在于：`<span>`是不换行的，而`<div>`是换行的。

如果单独在网页中插入这两个元素，不会对页面产生任何的影响。这两个元素是专门为定义CSS样式而生的。或者说，DIV+CSS来实现各种样式。

div在浏览器中，默认是不会增加任何的效果的，但是语义变了，div中的所有元素是一个小区域。 div标签是一个容器级标签，里面什么都能放，甚至可以放div自己。

span也是表达“小区域、小跨度”的标签，但是是一个文本级的标签。 就是说，span里面只能放置文字、图片、表单元素。 span里面不能放p、h、ul、dl、ol、div。

span里面是放置小元素的，div里面放置大东西的。

**div标签负责布局，负责结构，负责分块。css负责样式。**

- **特殊字符（转义字符）**

要求背诵的特殊字符有：`&nbsp;`、`&lt;`、`&gt;`、`&copy;`。

`&nbsp;`：空格 （non-breaking spacing，不断打空格）

`&lt;`：小于号（less than）

`&gt;`：大于号（greater than）

`&copy;`：版权©


- **超链接**

1, 外部链接：链接到外部文件。

```
<a href="02页面.html">点击进入另外一个文件</a>
<a href="http://www.baidu.com" target="_blank">点我点我</a>
```

a是英语anchor“锚”的意思，就好像这个页面往另一个页面扔出了一个锚。是一个文本级的标签。
href是英语hypertext reference超文本地址的缩写。


**超链接的属性**

`href`：目标URL

`title`：悬停文本。

`name`：主要用于设置一个锚点的名称。

`target`：告诉浏览器用什么方式来打开目标页面。target属性有以下几个值：

_self：在同一个网页中显示（默认值）

_blank：在新的窗口中打开。

_parent：在父窗口中显示

_top：在顶级窗口中显示
title属性举例：

```<a href="09_img.html" title="很好看哦">结婚照</a>```



target属性举例：

```<a href="1.html" title="悬停文本" target="_blank">链接的内容</a>```
blank就是“空白”的意思，就表示新建一个空白窗口。为啥有一个_ ，就是规定，没啥好解释的。 也就是说，如果不写target=”_blank”那么就是在相同的标签页打开，如果写了target=”_blank”，就是在新的空白标签页中打开。


## 列表标签

列表标签分为三种。

### 1、无序列表`<ul>`，无序列表中的每一项是`<li>`

### [代码效果](https://irwenjing.github.io/web2019/web2019/01-html/demo.html)

**注意**：

>li不能单独存在，必须包裹在ul里面；反过来说，ul的“儿子”不能是别的东西，只能有li。

>我们这里再次强调，ul的作用，并不是给文字增加小圆点的，而是增加无序列表的“语义”的

**属性:**

type="属性值"。属性值可以选： disc(实心原点，默认)，square(实心方点)，circle(空心圆)。 效果如下：
### [代码效果](https://irwenjing.github.io/web2019/web2019/01-html/demo.html)

不光是`<ul>`标签有type属性，`<ul>`里面的`<li>`标签也有type属性（虽然说这种写法很少见）。效果如下：

### [代码效果](https://irwenjing.github.io/web2019/web2019/01-html/demo.html)

注意：项目符号可以是图片，但是通过CSS设置.

当然了，列表之间是可以**嵌套**的。我们来举个例子： 代码

### [代码](https://github.com/irwenjing/web2019/blob/master/web2019/01-html/demo.html)

### [代码效果](https://irwenjing.github.io/web2019/web2019/01-html/demo.html)

声明：ul的儿子，只能是li。但是li是一个容器级标签，**li里面什么都能放，甚至可以再放一个ul**。

## 2、有序列表`<Ol>`，里面的每一项是`<li>`

### [代码](https://github.com/irwenjing/web2019/blob/master/web2019/01-html/demo.html)

### [代码效果](https://irwenjing.github.io/web2019/web2019/01-html/demo.html)

**属性**

type="属性值"。属性值可以是：1(阿拉伯数字，默认)、a、A、i、I。结合start属性表示从几开始。

### [代码](https://github.com/irwenjing/web2019/blob/master/web2019/01-html/demo.html)

### [代码效果](https://irwenjing.github.io/web2019/web2019/01-html/demo.html)


和无序列表一样，有序列表也是可以嵌套的哦，这里就不举类似的例子了。

ol和ul就是语义不一样，怎么使用都是一样的。 ol里面只能有li，li必须被ol包裹。li是容器级。

ol这个东西用的不多，如果想表达顺序，大家一般也用ul。举例如下：

### [代码](https://github.com/irwenjing/web2019/blob/master/web2019/01-html/demo.html)

## 3. 定义列表`<dl>`

>定义列表的作用非常大。

`<dl>`英文单词：definition list，没有属性。dl的子元素只能是dt和dd。

`<dt>`：definition title 列表的标题，这个标签是必须的

`<dd>`：definition description 列表的列表项，如果不需要它，可以不加

备注：dt、dd只能在dl里面；dl里面只能有dt、dd。

举例：

### [代码](https://github.com/irwenjing/web2019/blob/master/web2019/01-html/demo.html)

### [代码效果](https://irwenjing.github.io/web2019/web2019/01-html/demo.html)

上图可以看出，定义列表表达的语义是两层：

（1）是一个列表，列出了几个dd项目

（2）每一个词儿都有自己的描述项。

备注：dd是描述dt的。

定义列表用法非常灵活，可以一个dt配很多dd：

### [代码](https://github.com/irwenjing/web2019/blob/master/web2019/01-html/demo.html)

还可以拆开，让每一个dl里面只有一个dt和dd，这样子感觉清晰一些：

### [代码](https://github.com/irwenjing/web2019/blob/master/web2019/01-html/demo.html)

真实案例：（京东最下方）

### [代码效果](https://irwenjing.github.io/web2019/web2019/01-html/demo.html)


dt、dd都是容器级标签，想放什么都可以。所以，现在就应该更加清晰的知道：用什么标签，不是根据样子来决定，而是语义（语义本质上是结构）。











- **文档元数据**
```
<head>: 代表关于文档元数据的一个集合，包括脚本或样式表的链接或内容。
<title>: 定义文档的标题，将显示在浏览器的标题栏或标签页上。该元素只能包含文本，包含的标签不会被解释。
<base>: 定义页面上相对URL的基准URL。
<link>: 用于链接外部的CSS到该文档。
<meta>: 定义其他HTML元素无法描述的元数据。
<style>: 用于内联CSS。
```
- **脚本**
```
<script>: 定义一个内联脚本或链接到外部脚本。脚本语言是JavaScript。
<noscript>: 定义当浏览器不支持脚本时显示的替代文字。
<template>: 通过JavaScript在运行时实例化内容的容器。
```
- **章节**
```
<body>: 代表HTML文档的内容。在文档中只能有一个<body>元素。
<section>: 定义文档中的一个章节。
<nav>: 定义之包含导航链接的章节。
<article>: 定义可以独立于内容其余部分的完整独立内容块。
<aside>: 定义和页面内容关联度较低的内容--如果被删除，剩下的内容仍然很合理。
<h1>,<h2>,<h3>,<h4>,<h5>,<h6>: 标题元素实现了六层文档标题，<h1>是最大的标题，<h6>是最小的标题。标题元素简要地描述章节的主题。
<header>定义页面或章节的头部。它经常包含logo、页面标题和导航性的目录。
<footer>: 定义页面或章节的尾部。它经常包含版权信息、法律信息链接和反馈建议用的地址。
<address>: 定义包含联系信息的一个章节。
<main>: 定义文档中主要或重要的内容。
```
- **组织内容**

```
<p>: 定义一个段落。
<hr>: 代表章节、文章或其他长内容中段落之间的分隔符。
<pre>: 代表其内容已经预先排版过，格式应当保留。
<blockquote>: 代表引用其他来源的内容。
<ol>: 定义一个有序列表。
<ul>: 定义一个无序列表。
<li>: 定义列表中的一个列表项。
<dl>: 定义一个定义列表(一系列术语和其定义)。
<dt>: 代表一个由下一个<dd>定义的术语。
<dd>: 代表出现在它之前术语的定义。
<figure>: 代表一个和文档有关的图例。
<figcaption>: 代表一个图例的说明。
<div>: 代表一个通用的容器，没有特殊含义。
```
- **文字形式**
```
<a>: 代表一个链接到其他资源的超链接。
<em>: 代表强调文字。
<strong>: 代表特别重要文字。
<small>: 代表注释，如免责声明、版权声明等，对理解文档不重要。
<s>: 代表不准确或不相关的内容。
<cite>: 代表作品标题。
<q>: 代表内联的引用。
<dfn>: 代表一个术语包含在其最近祖先内容中的定义。
<abbr>: 代表省略或缩写，其完整内容在title属性中。
<data>: 关联一个内容的机器可读的等价形式（该元素只在WHATWG版本的HTML标准中，不在W3C版本的HTML5标准中）。
<time>: 代表日期和时间值；机器可读的等价形式通过datetime属性指定。
<code>: 代表计算机代码。
<var>: 代表代码中的变量。
<samp>: 代表程序或电脑的输出。
<kbd>: 代表用户输入，一般从键盘输出，但也可以代表其他输入，如语音输入。
<sub>,<sup>: 分别代表下标和上标。
<i>: 代表一段不同性质的文字，如技术术语、外交短语等。
<b>: 代表一段需要被关注的文字。
<u>: 代表一段需要下划线呈现的文本注释，如标记出拼写错误的文字等。
<mark>: 代表一段需要被高亮的引用 文字。
<ruby>: 代表被ruby 注释 标记的文本，如中文汉字和它的拼音。
<rt>: 代表ruby 注释 ，如中文拼音。
<rp>: 代表 ruby 注释两边的额外插入文本 ，用于在不支持 ruby 注释显示的浏览器中提供友好的注释显示。
<bdi>: 代表需要脱离 父元素文本方向的一段文本。它允许嵌入一段不同或未知文本方向格式的文本。
<bdo>: 指定子元素的文本方向 ，显式地覆盖默认的文本方向。
<span>: 代表一段没有特殊含义的文本，当其他语义元素都不适合文本时候可以使用该元素。
<br>: 代表换行 。
<wbr>: 代表建议换行 (Word Break Opportunity) ，当文本太长需要换行时将会在此处添加换行符。
```
- **编辑**
```
<ins>:  定义增加到文档的内容。
<del>: 定义从文档移除 的内容。
```
- **嵌入内容**
```
<img>: 代表一张图片 。
<iframe>: 代表一个内联的框架 。
<embed>: 代表一个嵌入的外部资源，如应用程序或交互内容。
<object>: 代表一个外部资源 ，如图片、HTML 子文档、插件等。
<param>: 代表 <object> 元素所指定的插件的参数 。
<video>: 代表一段视频 及其视频文件和字幕，并提供了播放视频的用户界面。
<audio>: 代表一段声音,或音频流 。
<source>: 为 <video> 或 <audio> 这类媒体元素指定媒体源 。
<track>: 为 <video> 或 <audio> 这类媒体元素指定文本轨道（字幕） 。
<canvas>: 代表位图区域 ，可以通过脚本在它上面实时呈现图形，如图表、游戏绘图等。
<map>:  与 <area> 元素共同定义图像映射区域。
<area>: 	与 <map> 元素共同定义图像映射区域。
<svg>: 定义一个嵌入式矢量图。
<math>: 定义一段数学公式 。
```
- **表格**
```
<table>:  定义多维数据。
<caption>: 代表表格的标题 。
<colgroup>: 代表表格中一组单列或多列 。
<col>: 代表表格中的列。
<tbody>: 	代表表格中一块具体数据（表格主体）。
<thead>: 代表表格中一块列标签 （表头）。
<tfoot>: 代表表格中一块列摘要 （表尾）。
<tr>: 代表表格中的行 。
<td>: 代表表格中的单元格 。
<th>: 代表表格中的头部单元格 。
```
- **表单**
```
<form>: 代表一个表单 ，由控件组成。
<fieldset>: 代表控件组 。
<legend>: 代表<fieldset>控件组的标题 。
<label>: 代表表单控件的标题 。
<input>: 代表允许用户编辑数据的数据区 （文本框、单选框、复选框等）。
<button>: 代表按钮 。
<select>:  代表下拉框 。
<datalist>: 代表提供给其他控件的一组预定义选项 。
<optgroup>: 代表一个选项分组 。
<option>: 代表一个 <select> 元素或 <datalist> 元素中的一个选项。
<textarea>: 代表多行文本框 。
<keygen>: 代表一个密钥对生成器 控件。
<output>: 代表计算值 。
<progress>: 代表进度条 。
<meter>: 代表滑动条 。
```
- **交互元素**
```
<details>: 代表一个用户可以(点击)获取额外信息或控件的小部件 。
<summary>: 代表 <details> 元素的综述 或标题 。
<menuitem>: 代表一个用户可以点击的菜单项。
<menu>: 代表菜单。
```
### 空标签
一个空元素可能是HTML,SVG，或者MathML里的一个不可能存在子节点（例如内嵌的元素或者元素内的文本）的element。
在HTML中，许多组合是没有任何语义含义的，比如一个`<audio>`元素嵌套在一个`<hr>`元素里。而且通常在一个空元素上使用一个闭标签是无效的。例如，`<input type="text"></input>`的闭标签是无效的HTML。

在HTML中有一下这些空元素：
`<area>`、`<base>`、`<br>`、`<col>`、`<colgroup>` when the `span` is present 、`<command>`、`<embed>`、`<hr>`、`<img>`、`<input>`、`<keygen>`、`<link>`、`<meta>`、`<param>`、`<source>`、`<track>`、`<wbr>` 。

### 可替换标签
典型的可替换元素有`<img>`、`<object>`、`<video>`和表单元素，如`<textarea>`、`<input>`。

