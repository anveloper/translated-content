---
title: dragend
slug: Web/API/Document/dragend_event
---
<div>拖放事件在拖放操作结束时触发 (通过释放鼠标按钮或单击 escape 键)。</div>

<h2 id="基本信息">基本信息</h2>

<table class="properties">
 <tbody>
  <tr>
   <td>Bubbles</td>
   <td>Yes</td>
  </tr>
  <tr>
   <td>Cancelable</td>
   <td>No</td>
  </tr>
  <tr>
   <td>Target objects</td>
   <td>{{domxref("Document")}}, {{domxref("Element")}}</td>
  </tr>
  <tr>
   <td>Interface</td>
   <td>{{domxref("DragEvent")}}</td>
  </tr>
  <tr>
   <td>Default Action</td>
   <td>Varies.</td>
  </tr>
 </tbody>
</table>

<h2 id="属性">属性</h2>

<table>
 <thead>
  <tr>
   <th scope="col">Property</th>
   <th scope="col">Type</th>
   <th scope="col">Description</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>target</code> {{readonlyInline}}</td>
   <td><a href="/en-US/docs/Web/API/EventTarget"><code>EventTarget</code></a></td>
   <td>The element that was underneath the element being dragged.</td>
  </tr>
  <tr>
   <td><code>type</code> {{readonlyInline}}</td>
   <td><a href="/en-US/docs/Web/API/DOMString"><code>DOMString</code></a></td>
   <td>事件类型。</td>
  </tr>
  <tr>
   <td><code>bubbles</code> {{readonlyInline}}</td>
   <td><a href="/en-US/docs/Web/API/Boolean"><code>Boolean</code></a></td>
   <td>是否允许冒泡</td>
  </tr>
  <tr>
   <td><code>cancelable</code> {{readonlyInline}}</td>
   <td><a href="/en-US/docs/Web/API/Boolean"><code>Boolean</code></a></td>
   <td>默认行为是否可以取消</td>
  </tr>
  <tr>
   <td><code>view</code> {{readonlyInline}}</td>
   <td><a href="/en-US/docs/Web/API/WindowProxy"><code>WindowProxy</code></a></td>
   <td><a href="/en-US/docs/Web/API/Document/defaultView"><code>document.defaultView</code></a> (<code>window</code> of the document)</td>
  </tr>
  <tr>
   <td><code>detail</code> {{readonlyInline}}</td>
   <td><code>long</code> (<code>float</code>)</td>
   <td>0.</td>
  </tr>
  <tr>
   <td><code>dataTransfer</code></td>
   <td>DataTransfer</td>
   <td>The data that underlies a drag-and-drop operation, known as the <a href="/en-US/docs/Web/API/DataTransfer">drag data store</a>. Protected mode.</td>
  </tr>
  <tr>
   <td><code>currentTarget</code> {{readonlyInline}}</td>
   <td>EventTarget</td>
   <td>绑定事件监听的 DOM 结点</td>
  </tr>
  <tr>
   <td><code>relatedTarget</code> {{readonlyInline}}</td>
   <td>EventTarget</td>
   <td>For <code>mouseover</code>, <code>mouseout</code>, <code>mouseenter</code> and <code>mouseleave</code> events: the target of the complementary event (the <code>mouseleave</code> target in the case of a <code>mouseenter</code> event). <code>null</code> otherwise.</td>
  </tr>
  <tr>
   <td><code>screenX</code> {{readonlyInline}}</td>
   <td>long</td>
   <td>The X coordinate of the mouse pointer in global (screen) coordinates.</td>
  </tr>
  <tr>
   <td><code>screenY</code> {{readonlyInline}}</td>
   <td>long</td>
   <td>The Y coordinate of the mouse pointer in global (screen) coordinates.</td>
  </tr>
  <tr>
   <td><code>clientX</code> {{readonlyInline}}</td>
   <td>long</td>
   <td>The X coordinate of the mouse pointer in local (DOM content) coordinates.</td>
  </tr>
  <tr>
   <td><code>clientY</code> {{readonlyInline}}</td>
   <td>long</td>
   <td>The Y coordinate of the mouse pointer in local (DOM content) coordinates.</td>
  </tr>
  <tr>
   <td><code>button</code> {{readonlyInline}}</td>
   <td>unsigned short</td>
   <td>The button number that was pressed when the mouse event was fired: Left button=0, middle button=1 (if present), right button=2. For mice configured for left handed use in which the button actions are reversed the values are instead read from right to left.</td>
  </tr>
  <tr>
   <td><code>buttons</code> {{readonlyInline}}</td>
   <td>unsigned short</td>
   <td>The buttons being pressed when the mouse event was fired: Left button=1, Right button=2, Middle (wheel) button=4, 4th button (typically, "Browser Back" button)=8, 5th button (typically, "Browser Forward" button)=16. If two or more buttons are pressed, returns the logical sum of the values. E.g., if Left button and Right button are pressed, returns 3 (=1 | 2). <a href="/en-US/docs/Web/API/MouseEvent">More info</a>.</td>
  </tr>
  <tr>
   <td><code>mozPressure</code> {{readonlyInline}}</td>
   <td>float</td>
   <td>The amount of pressure applied to a touch or tabdevice when generating the event; this value ranges between 0.0 (minimum pressure) and 1.0 (maximum pressure).</td>
  </tr>
  <tr>
   <td><code>ctrlKey</code> {{readonlyInline}}</td>
   <td>boolean</td>
   <td>
    <p>当事件触发的时候，如果<strong>Ctrl</strong>键是按下的，这个值就是<strong>true</strong>,否则就是<strong>false</strong></p>
   </td>
  </tr>
  <tr>
   <td><code>shiftKey</code> {{readonlyInline}}</td>
   <td>boolean</td>
   <td>
    <p>当事件触发的时候，如果<strong>Shift</strong>键是按下的，这个值就是<strong>true</strong>,否则就是<strong>false</strong></p>
   </td>
  </tr>
  <tr>
   <td><code>altKey</code> {{readonlyInline}}</td>
   <td>boolean</td>
   <td>当事件触发的时候，如果<strong>Alt</strong>键是按下的，这个值就是<strong>true</strong>,否则就是<strong>false</strong></td>
  </tr>
  <tr>
   <td><code>metaKey</code> {{readonlyInline}}</td>
   <td>boolean</td>
   <td>当事件触发的时候，如果<strong>M</strong><strong>eta</strong>键是按下的，这个值就是<strong>true</strong>,否则就是<strong>false</strong></td>
  </tr>
 </tbody>
</table>

<h2 id="示例：dropzone">示例：dropzone</h2>

<p>{{page('/zh-CN/docs/Web/Events/dragstart', '示例：dropzone')}}</p>

<h2 id="规范">规范</h2>

{{Specifications}}

<h2 id="浏览器支持">浏览器支持</h2>

{{Compat("api.Document.dragend_event")}}

<h2 id="相关">相关</h2>

<ul>
 <li>{{event("drag")}}</li>
 <li>{{event("dragstart")}}</li>
 <li>{{event("dragend")}}</li>
 <li>{{event("dragover")}}</li>
 <li>{{event("dragenter")}}</li>
 <li>{{event("dragleave")}}</li>
 <li>{{event("dragexit")}}</li>
 <li>{{event("drop")}}</li>
</ul>