---
title: EventSource.onerror
slug: Web/API/EventSource/error_event
---
<div>{{APIRef('WebSockets API')}}</div>

<div> </div>


<p>{{domxref("EventSource")}} 的属性 <code><strong>onerror</strong></code> 是当发生错误且这个错误事件（{{event("error")}} ）被 EventSource 触发时调用的一个事件处理函数（{{event("Event_handlers", "event handler")}}）</p>

<h2 id="语法">语法</h2>

<pre class="syntaxbox">eventSource.onerror = function</pre>

<h2 id="例子">例子</h2>

<pre class="brush: js">evtSource.onerror = function() {
  console.log("EventSource failed.");
};</pre>

<div class="note">
<p><strong>Note</strong>: 你可以在 Github 上查看这个完整例子： <a href="https://github.com/mdn/dom-examples/tree/master/server-sent-events">Simple SSE demo using PHP.</a></p>
</div>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.EventSource.onerror")}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>{{domxref("EventSource")}}</li>
</ul>