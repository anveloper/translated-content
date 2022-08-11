---
title: target
slug: Web/SVG/Attribute/target
translation_of: Web/SVG/Attribute/target
---
<div>{{SVGRef}}</div>

<p><code><strong>target</strong></code>当结束资源有多个可能的目标时，例如，当父文档嵌入在 HTML 或 XHTML 文档中或使用选项卡式浏览器查看时，应使用该属性。此属性指定激活链接时要在其中打开文档的浏览上下文的名称（例如，浏览器选项卡或（X）HTML iframe 或 object 元素）：</p>

<p>只有一个元素正在使用此属性：{{SVGElement("a")}}</p>

<h2>示例</h2>

<pre class="brush: css hidden">html, body, svg {
    height: 100%;
}

text {
    font: 20px Arial, Helvetica, sans-serif;
    fill: blue;
    text-decoration: underline;
}
</pre>

<pre class="brush: html">&lt;svg viewBox="0 0 300 120" xmlns="http://www.w3.org/2000/svg"&gt;
  &lt;a href="https://developer.mozilla.org" target="_self"&gt;
    &lt;text x="0" y="20"&gt;在 iframe 中打开链接&lt;/text&gt;
    &lt;/a&gt;
  &lt;a href="https://developer.mozilla.org" target="_blank"&gt;
    &lt;text x="0" y="60"&gt;在新标签页或窗口中打开链接&lt;/text&gt;
    &lt;/a&gt;
  &lt;a href="https://developer.mozilla.org" target="_top"&gt;
    &lt;text x="0" y="100"&gt;在此标签或窗口中打开链接&lt;/text&gt;
    &lt;/a&gt;
&lt;/svg&gt;
</pre>

<p>{{EmbedLiveSample("示例", "300", "120")}}</p>

<h2 id="使用说明">使用说明</h2>

<table class="properties">
 <tbody>
  <tr>
   <th scope="row">值</th>
   <td><code>_self</code>| <code>_parent</code>| <code>_top</code>| <code>_blank</code>|<code>&lt;XML-Name&gt;</code></td>
  </tr>
  <tr>
   <th scope="row">默认值</th>
   <td><code>_self</code></td>
  </tr>
  <tr>
   <th scope="row">可动画的</th>
   <td>是</td>
  </tr>
 </tbody>
</table>

<dl>
 <dt><code>_replace</code> {{deprecated_inline}}</dt>
 <dd>
 <p>当前 SVG 图像被与当前 SVG 图像在同一帧中相同矩形区域中的链接内容替换。</p>

 <div class="blockIndicator note">
 <p><strong>备注：</strong> 这个值是从来没有很好的执行，之间的区别<code>_replace</code>，并<code>_self</code>已通过在浏览上下文的 HTML 定义的变化变得多余。使用<code>_self</code>以取代目前的 SVG 文件。</p>
 </div>
 </dd>
 <dt><code>_self</code></dt>
 <dd>在与当前 SVG 图像相同的浏览上下文中，当前 SVG 图像被链接的内容替换。</dd>
 <dt><code>_parent</code></dt>
 <dd>SVG 图像的直接父浏览上下文将被链接的内容替换（如果存在），并且可以从此文档中安全地访问它。</dd>
 <dt><code>_top</code></dt>
 <dd>完整活动窗口或选项卡的内容将由链接的内容替换（如果存在），并且可以从此文档中安全地访问</dd>
 <dt><code>_blank</code></dt>
 <dd>如果此文档可以安全地显示，则需要一个新的未命名窗口或标签来显示链接的内容。如果用户代理不支持多个窗口/选项卡，则结果与_top 相同。</dd>
 <dt><code>&lt;XML-Name&gt;</code></dt>
 <dd>指定用于显示链接内容的浏览上下文的名称（选项卡，内联框架，对象等）。如果具有该名称的上下文已经存在，并且可以从此文档中安全地访问，则可以重新使用该上下文，替换现有内容。如果不存在，则创建它（与'_blank'相同，但现在有了一个名称）。该名称必须是有效的 XML 名称 [XML11]，并且不能以下划线（U + 005F LOW LINE 字符）开头，以满足来自 HTML 的有效浏览上下文名称的要求。</dd>
</dl>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

<p>{{Compat}}</p>