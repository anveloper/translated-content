---
title: SpeechRecognitionResult
slug: Web/API/SpeechRecognitionResult
---
<p>{{APIRef("Web Speech API")}}{{SeeCompatTable}}</p>

<p>The <strong><code>SpeechRecognitionResult</code></strong> interface of the <a href="/en-US/docs/Web/API/Web_Speech_API">Web Speech API</a> represents a single recognition match, which may contain multiple {{domxref("SpeechRecognitionAlternative")}} objects.</p>

<h2 id="Properties">Properties</h2>

<dl>
 <dt>{{domxref("SpeechRecognitionResult.isFinal")}} {{readonlyinline}}</dt>
 <dd>A {{domxref("Boolean")}} that states whether this result is final (true) or not (false) — if so, then this is the final time this result will be returned; if not, then this result is an interim result, and may be updated later on.</dd>
 <dt>{{domxref("SpeechRecognitionResult.length")}} {{readonlyinline}}</dt>
 <dd>Returns <cite>the length of the "array" — the </cite>number of {{domxref("SpeechRecognitionAlternative")}} objects contained in the result (also referred to as "n-best alternatives".)</dd>
</dl>

<h2 id="Methods">Methods</h2>

<dl>
 <dt>{{domxref("SpeechRecognitionResult.item")}}</dt>
 <dd>A standard getter that allows {{domxref("SpeechRecognitionAlternative")}} objects within the result to be accessed via array syntax.</dd>
</dl>

<h2 id="Examples">Examples</h2>

<p>This code is excerpted from our <a href="https://github.com/mdn/web-speech-api/blob/master/speech-color-changer/script.js">Speech color changer</a> example.</p>

<pre class="brush: js">recognition.onresult = function(event) {
  // The SpeechRecognitionEvent results property returns a SpeechRecognitionResultList object
  // The SpeechRecognitionResultList object contains SpeechRecognitionResult objects.
  // It has a getter so it can be accessed like an array
  // The first [0] returns the SpeechRecognitionResult at position 0.
  // Each SpeechRecognitionResult object contains SpeechRecognitionAlternative objects that contain individual results.
  // These also have getters so they can be accessed like arrays.
  // The second [0] returns the SpeechRecognitionAlternative at position 0.
  // We then return the transcript property of the SpeechRecognitionAlternative object
  var color = event.results[0][0].transcript;
  diagnostic.textContent = 'Result received: ' + color + '.';
  bg.style.backgroundColor = color;
}</pre>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

{{Compat("api.SpeechRecognitionResult")}}

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="/en-US/docs/Web/API/Web_Speech_API">Web Speech API</a></li>
</ul>