
# markdown简介

## 前言
写这个算不上教程的文档说明，只是因为在我的小白进阶之路——学习github时，发现每个项目都会有一个readme.md。很好奇这.md后缀的是什么玩意，一探究竟之下，发现又学了点知识~，这里算是我的笔记吧~

md就是markdown缩写，GitHub 上每个项目要求提供Markdown格式的README.md文件，作为项目首页的说明文档。

## 宗旨
Markdown是一种轻量级标记语言，创始人为John Gruber。<br />
Markdown是为了更简单方便地书写 HTML ，使我们更加专注于内容写作本身。

# 兼容HTML
在markdown文本里可以直接加HTML标签，只要不是markdown本身的标签，都可以直接在文档里使用。

## 块状元素
需要注意的是一些块状元素，如`<div>`,`<table>`,`<pre>`,`<p>`等标签。必须在前后加上空行，与其他内容隔离开来，还需要要求他们的开始标签和与结尾标签不能用制表符或空格缩进。markdown的生成器很智能，不会在HTML区块标签外再加`<p>`标签。

例子如下，在markdown文档里加上一段HTML代码：

<ul>
    <li>这里是html标签语法</li>
    <li># 大标题</li>
    <li>## 二级标题</li>
    <li>### 三级标题</li>
    <li>#### 四级标题</li>
    <li>##### 五级标题</li>
    <li>###### 六级标题</li>
</ul>

以上代码要显示出来，该代码块上下都有一个空行，要注意的是，HTML模块化标签之间的markdown格式的语法将不会被处理，例如上例中markdown的标题语法标签并未被转译成标题文本。<br />

## 行内元素
HTML 的行内标签如 `<span>`、`<cite>`、`<del>` 可以在 Markdown 的段落、列表或是标题里随意使用。依照个人习惯，甚至可以不用 Markdown 格式，而直接采用 HTML 标签来格式化。举例说明：如果比较喜欢 HTML 的 <a> 或 <img> 标签，可以直接使用这些标签，而不用 Markdown 提供的链接或是图像标签语法。

和处在 HTML 块状元素标签间不同，Markdown 语法在 HTML 行内元素标签间是有效的。

示例代码：
```
我是<del>**删除线**</del>，我在行内，且我不需要进行转义。也不需要想块元素那样需要在标签前后加空行
```
示例效果：

我是<del>**删除线**</del>，我在行内，且我不需要进行转义。也不需要想块元素那样需要在标签前后加空行

此示例中html标签`<del>`在行内直接起作用，而且markdown语法中的强调语法也是有效的。

***

# 分割线
*** 、--- 、___ 可以显示横线效果
你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：

示例语法：
```
***
* * *
---
- - -
___
_ _ _
```
示例效果：

***
* * *
---
- - -
___
_ _ _

# 源代码显示及高亮

那么如果是程序和标签相关的写作，你不希望你写的一段代码以列表或者段落的方式去排版，而是想要直接以源代码的形式显示，那么markdown会用 `<pre>` 和 `<code>` 标签把代码区块包起来。

markdown语法需要我们在代码的上一行和下一行用三个反引号来标记代码区块。反引号就是数字1左边，Tab键上面的键(注意使用英文输入法)。要实现语法高亮只要在三个反引号之后加上你的编程语言即可（忽略大小写）。如html代码只需在开头三个反引号之后加上html即可，c++语言可以写成c++也可以是cpp。看代码：

```html
<ul>
    <li>这里是html标签语法</li>
    <li># 大标题</li>
    <li>## 二级标题</li>
    <li>### 三级标题</li>
    <li>#### 四级标题</li>
    <li>##### 五级标题</li>
    <li>###### 六级标题</li>
</ul>
```

```java
public static void main(String[]args){} //Java
```

```c
int main(void)
{
    printf("Hello, world!");
    return 0;
} //C
```

```Bash
echo "hello GitHub" #Bash
```

```javascript
document.write("Hello World!") //javascript
```

```cpp
string &operator+(const string& A,const string& B) //cpp
```


# 标题
Markdown 支持两种标题的语法，类 Setext 和类 atx 形式。

类 Setext 形式是用底线的形式，利用 = （最高阶标题）和 - （第二阶标题）

示例代码：
```
这是h1标题显示效果
======

这是h2标题显示效果
------
```

示例效果：

这是h1标题显示效果
======

这是h2标题显示效果
------

任何数量的`=`和`-`都可以有效果。而这种类型的表现形式，也只有这两级标题显示。

***
类 Atx 形式则是在行首插入 1 到 6 个 # ，对应到标题 1 到 6 阶，你可以选择性地「闭合」类 atx 样式的标题，这纯粹只是美观用的，若是觉得这样看起来比较舒适，你就可以在行尾加上 #，而行尾的 # 数量也不用和开头一样（行首的井字符数量决定标题的阶数）

示例代码：
```
# 这是 H1

## 这是 H2

###### 这是 H6
```

示例效果：

# 这是 H1

## 这是 H2

###### 这是 H6




***

# 文本

## 普通文本
直接输入的文字就是普通文本。

## 单行文本
```
我是单行文本
```
## 多行文本
```
我是多行文本，我写在三个反引号的markdown语法中，属于源码输出，目的是让这段话高亮显示，
在这里我可以直接回车换行，
我换行了，文字太多了，我任性直接换行
```
## 文本换行
以上文本是在三个反引号内输出的，为源码输出，所以这段文本可以直接回车换行，<br />
而markdown中直接输入文字，不能回车换行，若想换行有三种办法：  
1.本段文本第二行换行是在第一行后面想要换行处加了`<br />`；

2.本段文本第三行换行是上一行文本后面补两个空格然后回车；

3.本段文本第四行和本行换行是在其上一行下面都直接加了一行空行，这样也能实现换行，只是行间距有点大。

## 文本首行缩进 空格
由于在markdown中空格大部分时候都是起着排版控制作用，因此没法在行首或格式控制符之后输入空格。

en space, U+2002 ISOpub<br />
半方大的空白`&ensp;`或`&#8194;`<br />
em space, U+2003 ISOpub<br />
  全方大的空白`&emsp;`或`&#8195;`<br />
no-break space = non-breaking space, U+00A0 ISOnum<br />
    不断行的空白格`&nbsp;`或`&#160;`<br />
一般行首输入两个全角空格（`&emsp;`）或八个半角空格（`&nbsp;`）进行缩进即可。

语法：
```
&emsp;&emsp;全角空格缩进
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;半角空格缩进
```

效果：<br />
&emsp;&emsp;全角空格缩进<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;半角空格缩进<br />
对比以上两行文本已经缩进两个汉字宽度。

***

## 部分文本高亮
如果你想使一段话中部分文字高亮显示，来起到突出强调的作用，那么可以把它用一对反引号把它包围起来。注意不是单引号，而是Tab上方，数字1左边的按键（注意使用英文输入法）。语法：

```
`markdown`,`<code>`,`文本高亮`,`&lt;div&gt;`,&lt;p&gt;
```
效果：`markdown`,`<code>`,`文本高亮`,`&lt;div&gt;`,&lt;p&gt;

***

## 文本段中显示代码标签

文本段中如果要输出标签，不能直接写标签，markdown会转译为标签加上`<pre>``<code>`标签，并将该标签之后的文本解释到代码区块里，导致文本段显示排版出错。

从上诉`部分文本高亮`示例中的语法及效果中，可以看出要在文本段中正常显示标签，需要用一对反引号将标签包围起来，注意不是单引号，而是Tab上方，数字1左边的按键（注意使用英文输入法），这种方法不仅可以在文本段中正常显示标签，而且标签是高亮显示，为常用显示方法。

也可以通过特殊符号转义来显示标签，例如`部分文本高亮`示例中最后的div和p标签的写法，加反引号就不需要特殊字符再转义，因为反引号内的内容会直接输出，而不用反引号，则需要将标签的尖括号通过特殊字符转义。

***

## 强调语法
Markdown 使用星号（`*`）和底线（`_`）作为标记强调字词的符号，被 `*` 或 `_` 包围的字词会被转成用 `<em>` 标签包围，用两个 `*` 或 `_` 包起来的话，则会被转成 `<strong>`，用三个 `*` 或 `_` 包起来的话，则会被转成 `<strong><em></em></strong>`，而用两个 `~`包起来的话，则会被转成 `<del>`删除线。

示例语法：
```
*斜体*      |     _斜体_<br />
**粗体**    |   __粗体__<br />
***粗斜体*** | ___粗斜体___<br />
~~删除线~~    |<br />
***~~粗斜体删除线~~***  |  ___~~粗斜体删除线~~___<br />
~~***粗斜体删除线***~~  |  ~~___粗斜体删除线___~~
```

示例效果：

*斜体*      |     _斜体_<br />
**粗体**    |   __粗体__<br />
***粗斜体*** | ___粗斜体___<br />
~~删除线~~    |<br />
***~~粗斜体删除线~~***  |  ___~~粗斜体删除线~~___<br />
~~***粗斜体删除线***~~  |  ~~___粗斜体删除线___~~


斜体、粗体、删除线可混合使用

***

但是如果你的*和_两边都有空白的话，它们就只会被当成普通的符号。

示例语法：
```
 _ 斜体 _ <br />
 ** 粗体 **   __ 粗体 __ <br />
 ~~ 删除线 ~~ <br />
 *** ~~ 粗斜体删除线 ~~ ***
```
示例效果：

 _ 斜体 _ <br />
 ** 粗体 **   __ 粗体 __ <br />
 ~~ 删除线 ~~ <br />
 *** ~~ 粗斜体删除线 ~~ ***

 ***

如果要在文字前后直接插入普通的星号或底线，你可以用反斜线：

示例语法：
```
\*这里的星号不起任何作用，只是普通符号\*
```
示例效果：

\*这里的星号不起任何作用，只是普通符号\*

***

# 特殊字符转义
语法：
```
© ， &copy; ， AT&T ，  AT&amp;T ，  4 < 5  ，   4 &lt; 5  ，  &lt; ，  &amp;  ，  &gt;
```
效果：

© ， &copy; ，  AT&T ，  AT&amp;T ，  4 < 5  ，   4 &lt; 5  ，  &lt; ，  &amp;  ，  &gt;

当`<`，`>`用于标签的起始和结束标签且在文本段内显示时，在不让其高亮显示的情况下，需要对这两个符号进行转义`&lt;`，`&gt;`。

***

# 图片
Markdown 插入图片有两种格式：行内式和参考式。

## 行内式

基本语法：
```
![alt](URL title)
```
行内式详细解释如下：

* 一个惊叹号 `!`<br />
* 接着一个方括号，alt表示图片显示失败时的替换文本,对应html中的alt属性（可省略）<br />
* 接着一个小括号，url放图片的存放地址，title表示鼠标悬停在图片时的显示文本，对应html中的title属性，title需要加双引号或者单引号（title可省略）

## 参考式
基本语法：
```
![alt][ID]
[ID]:URL title
```
* 参考式与行内式不同之处就是第一个方括号之后跟着的又是一个方括号、以及此语法分为两句，第一句写在用到此句的地方，而第二句通常与其他使用参考式的第二句集中在一起放在文章末尾。
* ID是图片参考的名称，使用图片参考可以达到复用的目的，一般把全文所有的URL链接通过ID匹配，统一放在文章末尾，哪里需要用这个链接，直接通过`![alt][ID]`调用这个链接的ID即可。
* 此语法第二行第一个中括号与第一行第二个中括号是相匹配的，两个中括号内的ID必须一致，才能调用该ID语法冒号后的链接地址，不过这里的ID不区分大小写，。
* 冒号后的写法与行内式小括号内写法一样，前者URL，URL可用尖括号包围起来，如`<https://github.com>`后者为title，需加双引号或者单引号以及小括号，title可以放在第二行。

ID参考如下：
```
![我的github][github]
[github]:https://github.com/kaivin/ "我的github，欢迎关注"
```
## 图片地址
### 本地图片/同主机资源
图片的url地址，如果引用本图片或是项目本身的资源，直接使用相对路径就可了。
```
行内式：
![我的新浪微博](images/sina.png "我的新浪微博")

参考式：
![我的新浪微博][sina]
[sina]:images/sina.png "我的新浪微博"
```
行内式：
![我的新浪微博](images/sina.png "我的新浪微博")

参考式：
![我的新浪微博][sina]
[sina]:images/sina.png "我的新浪微博"

### 网络图片
如果是网络图片，复制该图片的网络链接地址即可。
```
行内式：
![百度](https://ss0.bdstatic.com/5aV1bjqh_Q23odCf/static/superman/img/logo/bd_logo1_31bdc765.png "百度一下")

参考式：
![百度][baidu]
[baidu]:https://ss0.bdstatic.com/5aV1bjqh_Q23odCf/static/superman/img/logo/bd_logo1_31bdc765.png "百度一下"
```
行内式：
![百度](https://ss0.bdstatic.com/5aV1bjqh_Q23odCf/static/superman/img/logo/bd_logo1_31bdc765.png "百度一下")

参考式：
![百度][baidu]
[baidu]:https://ss0.bdstatic.com/5aV1bjqh_Q23odCf/static/superman/img/logo/bd_logo1_31bdc765.png "百度一下"

### github仓库中的图片
如果引用其他github仓库中的图片要注意格式：https://github.com/ 你的用户名 / 你的项目名 /raw/分支名/存放图片文件夹/图片，如：
```
https://github.com/kaivin/markdown/raw/master/images/github.png
行内式：
![我的github](https://github.com/kaivin/markdown/raw/master/images/github.png "我的github")

参考式：
![我的github][github]
[github]:https://github.com/kaivin/markdown/raw/master/images/github.png "我的github"
```
行内式：
![我的github](https://github.com/kaivin/markdown/raw/master/images/github.png "我的github")

参考式：
![我的github][github]
[github]:https://github.com/kaivin/markdown/raw/master/images/github.png "我的github"

#### tips
* 图片地址的参考式中，其第二句`[ID]:URL title`，可将一个md文件中所有用到此句的集中在一起，写在此文件的任意位置，达到复用及修改方便的目的。
* 图片地址的语法与链接中的文本链接以及图片链接，都属于链接的一种，所以，都可以用行内式及参考式这两种插入链接的方法。只是图片地址与超链接的语法识别有所不同，具体可看本文链接模块。
* 在本例中，新浪图标及github图标调用的就是本仓库的图片，所以即可以使用相对路径，也可以使用调用github仓库中的图片的格式。若调用其他仓库，或其他github使用者仓库的图片，这里就需要做相应的修改。
***


# 链接
语法：
```
行内式：
[content]( URL title)

参考式：
[content][ID]
[ID]:URL title
```
* **超链接语法机构对比图片地址的语法结构，可以发现，不同之处，只在于两种语法的第一个中括号及图片地址多了一个`！`。**
* **图片地址语法内第一个中括号内alt表示图片显示失败的替代文本文字，而超链接这里我给你取名content,主要是因为超链接有文本链接及图片链接，两种链接在这个中括号内的内容不同，但相同的是，都是显示内容的地方。**
* **我将文本链接的此处命名为text,即显示文本，图片链接的此处命名为img,即显示图片。**
* **此处的命名content,text,img均没有实际的意义，只是为了写出这个语法结构，与参考式中ID所在中括号一样，这些命名只代表本人对这个语法理解**

## 文本链接
给一段文字加入超链接的语法如下：

```
行内式：
[text]( URL title)

参考式：
[text][ID]
[ID]:URL title
```
示例代码：
```
行内式：
[我的github](https://github.com/kaivin/ "github")

参考式：
[我的github][githubs]
[githubs]:https://github.com/kaivin/ "github"
```
显示效果：

行内式：
[我的github](https://github.com/kaivin/ "github")

参考式：
[我的github][githubs]
[githubs]:https://github.com/kaivin/ "github"

* **此处我的github的ID换了个名字，这里的ID指向的是github的网址，而在图片地址一节中，有一个ID为github，其指向的是我这个项目在github上的图片路径。指向不同，ID不能冲突。**

## 图片链接
给图片加超链接语法如下：

```
行内式：
[img]( URL title)

参考式：
[img][ID]
[ID]:URL title
```
前文说过，超链接第一个中括号只起显示内容的作用，文本链接，可以直接输入要显示内容，而图片链接这里要显示图片，就需要将图片地址写在这里，所以，进一步语法可分为四类：
```
行内链接行内图片地址式：
[![alt](URL title)]( URL title)

行内链接 图片参考式
[![alt][ID]]( URL title)
[ID]:URL title

参考链接 图片行内式：
[![alt](URL title)][ID]
[ID]:URL title

参考式图片链接
[![alt][ID_IMG]][ID]
[ID_IMG]:URL title
[ID]:URL title
```
示例代码：
```
行内链接行内图片地址式：
[![新浪微博](images/sina.png "我的新浪微博")]( http://weibo.com/kayvon "新浪微博")

行内链接 图片参考式：
[![百度一下][baidu]]( http://www.baidu.com "百度一下")
[baidu]:https://ss0.bdstatic.com/5aV1bjqh_Q23odCf/static/superman/img/logo/bd_logo1_31bdc765.png "百度一下"

参考链接 图片行内式：
[![我的github](https://github.com/kaivin/markdown/raw/master/images/github.png "我的github")][githubs]
[githubs]:https://github.com/kaivin/ "我的github"

参考式图片链接：
[![我的知乎][zhihu_logo]][zhihu]
[zhihu_logo]:https://github.com/kaivin/markdown/raw/master/images/zhihu.png "我的知乎"
[zhihu]:https://www.zhihu.com/people/kay_vin "我的知乎"

删除图片的alt属性：
[![zhihu_logo]][zhihu]
```
行内链接行内图片地址式：
[![新浪微博](images/sina.png "我的新浪微博")]( http://weibo.com/kayvon "新浪微博")

行内链接 图片参考式：
[![百度一下][baidu]]( http://www.baidu.com "百度一下")
[baidu]:https://ss0.bdstatic.com/5aV1bjqh_Q23odCf/static/superman/img/logo/bd_logo1_31bdc765.png "百度一下"

参考链接 图片行内式：
[![我的github](https://github.com/kaivin/markdown/raw/master/images/github.png "我的github")][githubs]
[githubs]:https://github.com/kaivin/ "我的github"

参考式图片链接：
[![我的知乎][zhihu_logo]][zhihu]
[zhihu_logo]:https://github.com/kaivin/markdown/raw/master/images/zhihu.png "我的知乎"
[zhihu]:https://www.zhihu.com/people/kay_vin "我的知乎"

删除图片的alt属性：
[![zhihu_logo]][zhihu]

***
* 由以上示例可看出，在markdown中添加图片及在一段文本中添加链接最方便的便是参考式，其在文件中的语法最简便。而ID指向的链接也都集合在一起，方便修改及调用。
* 所有超链接也和图片地址链接一样，链接到本仓库其他页面可使用相对路径，外部链接，直接复制外部链接即可。


## 自动超链
用尖括号包裹url，这样生成的url就是url本身
示例代码：
```
<kay_vin@qq.com>
```
示例效果：<kay_vin@qq.com> www.baidu.com
## 锚点链接
