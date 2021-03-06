# 前端开发校招面试问题整理【2】——HTML

## 1、HTML 元素（element）

### Q：简单介绍下常用的 HTML 元素？

块状标签：元素独占一行，可指定宽、高。
常用的块状元素有：

```
<div>、<p>、<h1>-<h6>、<ol>、<ul>、<dl>、<table>、<form>
```

内联元素：元素在一行内，宽度与高度由内容决定，只有在内容超过 HTML 的宽度时，才会换行。
常用的内联元素有：

```
<a>、<span>、<i>、<em>、<strong>、<label>
```

内联块状元素同时具备内联元素、块状元素的特点，它和其他元素都在一行，但元素的高度、宽度、行高以及顶和底边距都可设置。常用的内联块状元素有：

```
<img>、<input>
```

### Q：语义化元素是指？

语义化元素是指元素本身传达了关于其内容类型的一些信息。这些元素让页面的内容结构化，结构更清晰，便于 SEO，容易阅读和维护。

常见的语义化元素：

```
<header>
<footer>
<nav>
<article>
<section>
<aside>

<h1>
<h2>
<h3>
<h4>
<h5>
<h6>

<strong>
<em>
```

### Q：HTML5 新增了哪些元素？

| 标签        | 说明                                                             |
| ----------- | ---------------------------------------------------------------- |
| `<header>`  | 定义 section 或 document 的页眉。                                |
| `<footer>`  | 定义 section 或 document 的页脚。                                |
| `<nav>`     | 定义导航链接的部分。                                             |
| `<article>` | 定义文章的内容。                                                 |
| `<section>` | 定义文档中的段落。比如章节、页眉、页脚或文档中的其他部分。       |
| `<aside>`   | 定义 article 以外的内容。aside 的内容应该与 article 的内容相关。 |
| `<audio>`   | 定义声音。                                                       |
| `<canvas>`  | 定义图形。                                                       |
| `<video>`   | 定义视频，比如电影片段或其他视频流。                             |
| `<source>`  | 为媒介元素（比如 `<video>` 和 `<audio>`）定义媒介资源。          |

## 2、HTML 事件

### Q：描述一下 HTML 的事件模型？事件捕获/事件冒泡指的是？
![事件模型](http://www.shadowingszy.top/images/event.png)

当页面触发一个事件的时候，浏览器主要做了三个阶段的事情，分别是：
1、捕获事件阶段
2、目标处理阶段
3、后续事件处理阶段

当事件被触发，从根节点传递事件对象到目标节点的过程，就是事件捕获。
当处理完成事件后，从目标节点反向的传递到根节点的过程，就是事件冒泡。

### Q：如何阻止事件冒泡？如何阻止元素默认行为？

```javascript
event.stopPropagation() // 阻止事件冒泡
event.preventDefault() // 阻止元素默认行为
```
