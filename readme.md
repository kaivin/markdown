
# markdown简介

## 前言
写这个算不上教程的文档说明，只是因为在我的小白进阶之路——学习github时，发现每个项目都会有一个readme.md。很好奇这.md后缀的是什么玩意，一探究竟之下，发现又学了点知识~，这里算是我的笔记吧~<br />

md就是markdown缩写，GitHub 上每个项目要求提供Markdown格式的README.md文件，作为项目首页的说明文档。<br />

## 宗旨
Markdown是一种轻量级标记语言，创始人为John Gruber。<br />
Markdown是为了更简单方便地书写 HTML ，使我们更加专注于内容写作本身。<br />

# 兼容HTML
在markdown文本里可以直接加HTML标签，只要不是markdown本身的标签，都可以直接在文档里使用。<br />

## 块状元素
需要注意的是一些块状元素，如&lt;div&gt;,&lt;table&gt;,&lt;pre&gt;,&lt;p&gt;等标签。必须在前后加上空行，与其他内容隔离开来，还需要要求他们的开始标签和与结尾标签不能用制表符或空格缩进。markdown的生成器很智能，不会在HTML区块标签外再加&lt;p&gt;标签<br/>

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

### 源代码显示及高亮

那么如果是程序和标签相关的写作，你不希望你写的一段代码以列表或者段落的方式去排版，而是想要直接以源代码的形式显示，那么markdown会用 &lt;pre&gt; 和 &lt;code&gt; 标签把代码区块包起来。<br />

markdown语法需要我们在代码的上一行和下一行用三个反引号来标记代码区块。反引号就是数字1左边，Tab键上面的键。要实现语法高亮那么只要在  三个反引号之后加上你的编程语言即可（忽略大小写）。c++语言可以写成c++也可以是cpp。看代码：

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
