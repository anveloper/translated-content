---
title: window.document
slug: Web/API/Window/document
---
<p>{{ ApiRef() }}</p>

<p><strong><code>window.document</code></strong>返回当前窗口内的文档节点（{{domxref("document")}}）</p>

<div class="note"><strong>注：</strong> 从 Firefox 3 和 IE7 开始，访问其他页面内的文档节点会受到同源策略的影响。</div>

<h2 id="Syntax">语法</h2>

<pre class="eval notranslate"><em>doc</em> = window.document
</pre>

<h2 id="Parameters">参数</h2>

<ul>
 <li><code>doc</code>是一个指向{{domxref("document")}}对象的引用</li>
</ul>

<h2 id="Example">例子</h2>

<pre class="brush:html notranslate">&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
   &lt;title&gt;Hello, World!&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;

&lt;script type="text/javascript"&gt;
   var doc = window.document;
   alert( doc.title);    // 弹出: Hello, World!
&lt;/script&gt;

&lt;/body&gt;
&lt;/html&gt;</pre>

<h2 id="Specification">规范</h2>

{{Specifications}}


<h2 id="浏览器兼容性">浏览器兼容性</h2>



<p>{{Compat("api.Window.document")}}</p>