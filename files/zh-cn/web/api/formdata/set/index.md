---
title: FormData.set()
slug: Web/API/FormData/set
---
<p>{{APIRef("XMLHttpRequest")}}</p>

<p><code><strong>set()</strong></code> 方法会对 <code>FormData</code> <code>对象里的某个</code> <code>key</code> <code>设置一个新的值，如果该</code> <code>key</code> <code>不存在，则添加。</code></p>

<p><code>set()</code> 和 {{domxref("FormData.append")}} 不同之处在于：如果某个 key 已经存在，<code>set()</code> 会直接覆盖所有该 key 对应的值，而 {{domxref("FormData.append")}} 则是在该 key 的最后位置再追加一个值。</p>

<div class="note">
<p><strong>注意</strong>: 该方法在 <a href="/zh-CN/docs/Web/API/Web_Workers_API">Web Workers</a> 可用。</p>
</div>

<h2 id="语法">语法</h2>

<p>该方法有两种使用方式，一个是传入两个参数，一个是传入三个参数。</p>

<pre class="brush: js">formData.set(name, value);
formData.set(name, value, filename);</pre>

<h4 id="append()_Parameters">参数</h4>

<dl>
 <dt><code>name</code></dt>
 <dd>字段名称。</dd>
 <dt><code>value</code></dt>
 <dd>字段的值，该值可以是一个 {{domxref("USVString")}} 或 {{domxref("Blob")}}（包括其子类，例如 {{domxref("File")}}），如果不是这两个指定的类型，其将被转成一个字符串。</dd>
 <dt><code>filename</code> {{optional_inline}}</dt>
 <dd>当第二个参数传递的是一个 blob 对象（{{domxref("Blob")}}）或者 file 对象（{{domxref("File")}}），filename 参数就代表传给服务端的文件名（一个 {{domxref("USVString")}}）。
  {{domxref("Blob")}} 对象的默认文件名是 "blob"，{{domxref("File")}} 对象的默认文件名则为其“name”属性</dd>
</dl>

<div class="note">
<p><strong>注意：</strong> 如果对 FormData 对象插入一个 blob 对象（ {{domxref("Blob")}}），那么发送给服务器的请求头部（header）里的“Content-Disposition”里的文件名称将会根据浏览器的不同而不同。</p>
</div>

<h2 id="示例">示例</h2>

<p>先创建一个空的 <code>FormData</code> <code>对象：</code></p>

<pre class="brush: js">var formData = new FormData(); // Currently empty</pre>

<p>使用 {{domxref("FormData.set")}} 设置键/值 ：</p>

<pre class="brush: js">formData.set('username', 'Chris');
formData.set('userpic', myFileInput.files[0], 'chris.jpg');</pre>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器兼容性">浏览器兼容性</h2>

{{Compat("api.FormData.set")}}

<h2 id="相关链接">相关链接</h2>

<ul>
 <li>{{domxref("XMLHTTPRequest")}}</li>
 <li><a href="/zh-CN/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest">Using XMLHttpRequest</a></li>
 <li><a href="/zh-CN/docs/Web/API/FormData/Using_FormData_Objects">Using FormData objects</a></li>
 <li>{{HTMLElement("Form")}}</li>
</ul>