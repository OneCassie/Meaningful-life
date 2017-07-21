[TOC]
# CATLOG

### 概述
### 应用
### 基本语法

#### 简介
Markdown是一种可以使用普通文本编辑器编写的标记语言，通过简单的标记语法，它可以使普通文本内容具有一定的格式。


#### 兼容HTML
Markdown 的理念是，能让文档更容易读、写和随意改。HTML 是一种发布的格式，Markdown 是一种书写的格式。就这样，Markdown 的格式语法只涵盖纯文本可以涵盖的范围。
不在 Markdown 涵盖范围之内的标签，都可以直接在文档里面用 HTML 撰写。不需要额外标注这是 HTML 或是 Markdown；只要直接加标签就可以了。
要制约的只有一些 HTML 区块元素――比如`<div>`、`<table>`、`<pre>`、`<p>` 等标签，必须在前后加上空行与其它内容区隔开，还要求它们的开始标签与结尾标签不能用制表符或空格来缩进。Markdown 的生成器有足够智能，不会在 HTML 区块标签外加上不必要的`<p>`标签。

>举个栗子，在 Markdown 文件里加上一段 HTML 表格：
>这是一个普通段落。
><table>
>    <tr>
>        <td>Foo</td>
>    </tr>
></table>
>
>这是另一个普通段落。

请注意，在 HTML 区块标签间的 Markdown 格式语法将不会被处理。比如，你在 HTML 区块内使用 Markdown 样式的*强调*会没有效果。
HTML 的区段（行内）标签如 `<span>`、`<cite>`、`<del>` 可以在 Markdown 的段落、列表或是标题里随意使用。依照个人习惯，甚至可以不用 Markdown 格式，而直接采用 HTML 标签来格式化。举例说明：如果比较喜欢 HTML 的 `<a>` 或 `<img>` 标签，可以直接使用这些标签，而不用 Markdown 提供的链接或是图像标签语法。
和处在 HTML 区块标签间不同，Markdown 语法在 HTML 区段标签间是有效的。

### 应用
Markdown的语法简洁明了、学习容易，而且功能比纯文本更强，因此有很多人用它写博客。
还用于编写说明文档，并且以“README.MD”的文件名保存在软件的目录下面


### 基本语法
#### 标题
Markdown 支持两种标题的语法，类 Setext 和类 atx 形式。
类 Setext 形式是用底线的形式，利用 = （最高阶标题）和  - （第二阶标题）
例如：

This is an H1
=============

This is an H2
-------------

任何数量的 = 和 - 都可以有效果。

类 Atx 形式：行首插入1-6个 # ，每增加一个 # 表示更深入层次的内容，即 # 越小标题越大，对应到标题的深度由 1-6 阶。

举例：
# H1 :# Header 1
## H2 :## Header 2
### H3 :### Header 3
#### H4 :#### Header 4
##### H5 :##### Header 5
###### H6 :###### Header 6

#### 区块引用 Blockquotes
Markdown 标记区块引用是使用类似 email 中用 > 的引用方式。如果你还熟悉在 email 信件中的引言部分，你就知道怎么在 Markdown 文件中建立一个区块引用，那会看起来像是你自己先断好行，然后在每行的最前面加上 > 
举例：
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
> 
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

引用的区块内可以继续嵌套区块，也可以使用其他的 Markdown 语法，包括标题、列表、代码区块等：

> ## 这是一个标题。
> 
> >1.   这是第一行列表项。
> >2.   这是第二行列表项。
> 
> 给出一些例子代码：
> 
>     document.writln("Good!");

#### 分割线
可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：
* * *

1.* * *  
2.***  
3.*****  
4.- - - -  
5.--------------------------------------

####  链接
1.要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可：  
`This is [an example](http://www.baidu.com/) inline link.`  
效果：This is [an example](http://www.baidu.com/) inline link.

2.也可以用这种参考式的链接  
`This is [an example][id] reference-style link.`  
接着，可以在文件的任意处，把这个标记的链接内容定义出来：  
`[id]: http://www.baidu.com/  "Optional Title Here"`  
效果和上面一样。



#### 文本样式
注：（带“*”星号的文本样式，在原版Markdown标准中不存在，但在其大部分衍生标准中被添加）
加粗 :**Cassie**
斜体字 :*Italics*
*删除线 :~~Error~~
*高亮 :==Bug==
段落 : 段落之间直接空一行
换行符 : 一行结束时输入两个空格
列表 :* 添加星号成为一个新的列表项。
引用 :> 引用内容
内嵌代码 : `alert('Hello World');`
画水平线 (HR) :--------
