
# markdown简介

## 前言
写这个算不上教程的文档说明，只是因为在我的小白进阶之路——学习github时，发现每个项目都会有一个readme.md。很好奇这.md后缀的是什么玩意，一探究竟之下，发现又学了点知识~，这里算是我的笔记吧~<br />

md就是markdown缩写，GitHub 上每个项目要求提供Markdown格式的README.md文件，作为项目首页的说明文档。<br />

## 宗旨
Markdown是一种轻量级标记语言，创始人为John Gruber。<br />
Markdown是为了更简单方便地书写 HTML ，使我们更加专注于内容写作本身。<br />

# 兼容HTML
在markdown文本里可以直接加HTML标签，只要不是markdown本身的标签，都可以直接在文档里使用。<br />

需要注意的是一些块状元素，如&lt;div&gt;,&lt;table&gt;,&lt;pre&gt;,&lt;p&gt;等标签。必须在前后加上空行，与其他内容隔离开来，还需要要求他们的开始标签和与结尾标签不能用制表符或空格缩进。markdown的生成器很智能，不会在HTML区块标签外再加&lt;p&gt;标签<br/>

例子如下，在markdown文档里加上一段HTML代码：

<ul>
    <li>这里是html标签显示会显示ul,li标签</li>
    <li># 大标题</li>
    <li>## 二级标题</li>
    <li>### 三级标题</li>
    <li>#### 四级标题</li>
    <li>##### 五级标题</li>
    <li>###### 六级标题</li>
</ul>

要注意的是，HTML模块化标签之间的markdown格式的语法将不会被处理，例如上例中markdown的标题语法标签并未被转译成标题文本。<br />
