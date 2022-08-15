---
title: StorageEvent
slug: Web/API/StorageEvent
---
<p>{{APIRef("Web Storage API")}}</p>

<p>当前页面使用的 storage 被其他页面修改时会触发 StorageEvent 事件. </p>

<p>[译者：事件在同一个域下的不同页面之间触发，即在 A 页面注册了 storge 的监听处理，只有在跟 A 同域名下的 B 页面操作 storage 对象，A 页面才会被触发 storage 事件] </p>

<p>{{InheritanceDiagram}}</p>

<div class="note">
<p><strong>Note:</strong> 尽管这个事件已经早在 {{ Gecko("2.0") }}时就已存在，但是并不符合规范。老的事件模型直到 <code>nsIDOMStorageEventObsolete</code> 确定才被表现出来。</p>
</div>

<h2 id="方法描述">方法描述</h2>

<pre><code>void initStorageEvent(
  in DOMString typeArg,
  in boolean canBubbleArg,
  in boolean cancelableArg,
  in DOMString keyArg,
  in DOMString oldValueArg,
  in DOMString newValueArg,
  in DOMString urlArg,
  in nsIDOMStorage storageAreaArg
);</code>
</pre>

<h2 id="Method_overview">属性</h2>

<table class="standard-table">
 <tbody>
  <tr>
   <td class="header">属性名</td>
   <td class="header">类型</td>
   <td class="header">描述</td>
  </tr>
  <tr>
   <td><code>key</code></td>
   <td><code><a href="/en/DOMString">DOMString</a></code></td>
   <td>该属性代表被修改的键值。当被 clear() 方法清除之后该属性值为 null。<strong>（只读）</strong></td>
  </tr>
  <tr>
   <td><code>newValue</code></td>
   <td><code><a href="/en/DOMString">DOMString</a></code></td>
   <td>该属性代表修改后的新值。当被 clear() 方法清理后或者该键值对被移除，<code>newValue</code> 的值为 <code>null</code> 。<strong>（只读）</strong></td>
  </tr>
  <tr>
   <td><code>oldValue</code></td>
   <td><code><a href="/en/DOMString">DOMString</a></code></td>
   <td>该属性代表修改前的原值。在设置新键值对时由于没有原始值，该属性值为 <code>null</code>。<strong>（只读）</strong></td>
  </tr>
  <tr>
   <td><code>storageArea</code></td>
   <td><code>nsIDOMStorage</code></td>
   <td>被操作的 storage 对象。<strong>（只读）</strong></td>
  </tr>
  <tr>
   <td><code>url</code></td>
   <td><code><a href="/en/DOMString">DOMString</a></code></td>
   <td>
    <p>key 发生改变的对象所在文档的 URL 地址。<strong>（只读）</strong></p>
   </td>
  </tr>
 </tbody>
</table>

<h2 id="Methods">方法</h2>

<h3 id="initStorageEvent()">initStorageEvent()</h3>

<p>类似 DOM 中的初始化事件，即初始化新创建的 Storage 对象的属性。</p>

<pre class="eval">void initStorageEvent(
  in DOMString typeArg,
  in boolean canBubbleArg,
  in boolean cancelableArg,
  in DOMString keyArg,
  in DOMString oldValueArg,
  in DOMString newValueArg,
  in DOMString urlArg,
  in nsIDOMStorage storageAreaArg
);</pre>

<dl>
 <dt>参数：</dt>
 <dt><code>typeArg</code></dt>
 <dd>事件名</dd>
 <dt><code>canBubbleArg</code></dt>
 <dd>布尔值，代表是否可以通过 dom 冒泡</dd>
 <dt><code>cancelableArg</code></dt>
 <dd>布尔值，代表是否可以注销事件</dd>
 <dt><code>keyArg</code></dt>
 <dd>事件结果时被改变的值对应的属性名称</dd>
 <dt><code>oldValueArg</code></dt>
 <dd>旧值</dd>
 <dt><code>newValueArg</code></dt>
 <dd>新值</dd>
 <dt><code>urlArg</code></dt>
 <dd>事件初始化时页面的 url</dd>
 <dt><code>storageAreaArg</code></dt>
 <dd>发生在哪个 storage 对象上</dd>
</dl>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="See_also">参阅</h2>

<ul>
 <li><a href="http://dev.w3.org/html5/webstorage/#the-storage-event">Specification</a></li>
</ul>