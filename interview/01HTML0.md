
### __HTML所有标签__

* 基础标签：\<!DOCTYPE>,\<html>,\<title>,\<body>,\<h1>to\<h6>,\<p>,\<br>,\<hr>,\<!---->
* 格式标签：\<acronym>(废弃),\<abbr>,\<address>,\<b>,\<bdi>(New),\<bdo>,\<big>(废弃),\<blockquote>,\<center>(废弃),\<cite>,\<code>,\<del>,\<dfn>,\<em>,\<font>(废弃),\<i>,\<ins>,\<kbd>,\<mark>(New),\<meter>(New),\<pre>,\<progress>(New),\<q>,\<rt>(New),\<ruby>(New),\<s>,\<samp>,\<small>,\<strike>(废弃),\<strong>,\<sub>,\<sup>,\<time>,\<tt>(废弃),\<u>,\<var>,\<wbr>(New)
* 表单标签：\<form>,\<input>,\<textarea>,\<button>,\<select>,\<optgroup>,\<option>,\<label>,\<fieldset>,\<legend>,\<datalist>(New),\<keygen>(New),\<output>(New)
* 框架：\<frame>(废弃),\<frameset>(废弃),\<noframes>(废弃),\<iframe>
* 图像：\<img>,\<map>,\<area>,\<canvas>(New),\<figcaption>(New),\<figure>(New)
* Audio/Video(New)：\<audio>,\<source>,\<track>,\<video>
* 链接：\<a>,\<link>,\<main>,\<nav>(New)
* 列表：\<ul>,\<ol>,\<li>,\<dir>(废弃),\<dl>,\<dt>,\<dd>,\<menu>,\<command>
* 表格：\<table>,\<caption>,\<th>,\<tr>,\<td>,\<thead>,\<tbody>,\<tfoot>,\<col>,\<colgroup>
* 样式/节：\<style>, \<div>, \<span>, \<header>(New),\<footer>(New),\<section>(New),\<article><New>,\<aside>(New),\<dialog>(New),\<summary>(New)
* 元信息：\<head>,\<meta>,\<base>,\<basefont>(废弃)
* 程序：\<script>,\<noscript>,\<applet>(废弃),\<embed>(New),\<object>,\<param>


### __声明__
* \<!DOCTYPE>:html5标准网页声明，且必须声明在HTML文档的第一行。
  * BackCompat：怪异模式(没有声明时默认)--浏览器使用自己的怪异模式解析渲染页面
  * CSS1Compat:标准模式--使用W3C的标准解析渲染页面

### __元素__

* __\<head>__ 元素是所有头部元素的容器,可以添加的标签有：

  * __\<title>__：定义文档的标题--定义在浏览器工具栏中的标题，提供页面被添加到收藏夹时显示的标题--现在在搜素引擎结果中的页面标题
  * __\<base>__：定义页面上所有链接规定默认地址或默认目标(targe)
  * __\<link>__：定义文档与外部资源之间的关系，常用于连接样式表
  * __\<meta>__：元数据--是关于数据的信息，规定页面的描述、关键词、文档的作者、最后修改时间以及其他元数据
    * 属性值：name、http-equiv、content、scheme
      * name:名称/值对中的名称。author、description、keywords、generator、revised、others
      * http-equiv:没有name时，采用此属性的值。content-type、expires、refresh、set-cookie
      * content:名称/值对中的值，可以是任何有效的字符串。始终要和name或者http-equiv属性一起使用
      * scheme:用于指定要用来翻译属性值的方案
    * 
  * __\<style>__
  * __\<script>__
  * __\<noscript>__
* __\<body>__ 定义文档的主体
  * 常用标签 \<h1>-\<h6>,\<hr>,\<p>,\<div>,\<a>,\<img>,\<table>,\<form>,\<ul>\<ol>\<li>

### __行内元素__
> a b span img input select strong em
### __块级元素__
> div ul ol li dl dt dd h1-h6 p

### __自闭合元素(空元素)__
> input img br hr meta link

### __HTML5新特性__

* 新的语义元素：\<header>,\<footer>,\<article>,\<section>,\<nav>
* 新的表单控件：数字，日期，时间，日历和滑块(calendar,date,time,email,url,search)
* 图像支持：\<canvas>,\<svg>
* 多媒体支持：\<video>,\<audio>
* 新的API：本地存储(localStorage,sessionStorage)取代cookie；
* Geolocation：获取用户的位置
* 应用程序缓存：离线浏览--速度--减少服务器负载
* webworker:
* websocket:


### __HTML5移除的元素__
* 纯表现的元素： basefont,big,center,font,s,strike,tt,u
* frame,frameset,noframes


### __重点__

> defer和async的区别
* defer要等到整个页面在内存中正常渲染结束（DOM结构完全生成，以及其他脚本执行完成），才会执行。多个defer脚本会按照它们在页面出现的顺序加载。
* async一旦下载完，渲染引擎就会中断渲染，执行这个脚本以后，再继续渲染。多个async脚本是不能保证加载顺序的。


### __有意思的点__

> 如何在多个标签页之间通信

> 从浏览器地址输入url到显示页面发生的事情

> 渲染优化
* 使用css3代码代替js动画（尽可能避免重绘重排一级回流）
* 页面中空的href和src会阻塞页面其它资源的加载
* 用innerHTML代替DOM操作，减少DOM操作次数
* 当需要设置的样式很多时设置className
* 少用全局变量、缓存DOM阶段查找的结果。减少IO读取操作。
* 图片预加载，将样式表放在顶部，将脚本放在底部加上时间戳

> 如何进行网站性能优化
* 减少HTTP请求：合并文件，css精灵、inline Image
* 将样式表放在页面顶部
* 不使用css表达式
* 使用link不使用@import
* 将脚本放在页面底部
* 将JavaScript和css从外部引入
* 压缩JavaScript和css
