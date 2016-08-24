
# markdown简介
&emsp;&emsp;写这个算不上教程的文档说明，只是因为在我的小白进阶之路——学习github时，发现每个项目都会有一个readme.md。很好奇这.md后缀的是什么玩意，一探究竟之下，发现又学了点知识~，这里算是我的笔记吧~<br />

&emsp;&emsp;那么.md后缀文件是什么呢？其实就是一种为了实现“易读易写”，适用于网络的书写语言，这就是markdown! 如果非要深究什么是markdown，那我也只能说，他就是一种语言，更深层次的东西，不必去研究，我们需要的是灵活使用它。<br />

# 兼容HTML
&emsp;&emsp;在markdown文本里可以直接加HTML标签，只要不是markdown本身的标签，都可以直接在文档里使用。<br />

&emsp;&emsp;需要注意的是一些块状元素，如&lt;div&gt;,&lt;table&gt;,&lt;pre&gt;,&lt;p&gt;等标签。必须在前后加上空行，与其他内容隔离开来，还需要要求他们的开始标签和与结尾标签不能用制表符或空格缩进。markdown的生成器很智能，不会在HTML区块标签外再加&lt;p&gt;标签<br/>

&emsp;&emsp;例子如下，在markdown文档里加上一段HTML代码：

    <pre>
        <code>
            <ul>
                <li>这里是html标签显示会显示ul,li标签</li>
                <li>#大标题</li>
                <li>##二级标题</li>
                <li>###三级标题</li>
                <li>####四级标题</li>
                <li>#####五级标题</li>
                <li>######六级标题</li>
            </ul>
        </code>
    </pre>

&emsp;&emsp;要注意的是，HTML模块化标签之间的markdown格式的语法将不会被处理，例如上例中markdown的标题语法标签并未被转译成标题文本。<br />
