
                
                  
                    <div><section class="Quick_links" id="Quick_Links"><!-- --></section></div>

<p><strong><code>buffer</code></strong>&#x8BBF;&#x95EE;&#x5668;&#x5C5E;&#x6027;&#x8868;&#x793A;&#x7531;<em>TypedArray</em>&#x5728;&#x6784;&#x9020;&#x671F;&#x95F4;&#x5F15;&#x7528;&#x7684;<a href="/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/ArrayBuffer" title="&#x4E00;&#x4E2A;&#x65B0;&#x7684;&#x62E5;&#x6709;&#x6307;&#x5B9A;&#x5927;&#x5C0F;&#x7684;ArrayBuffer&#x5BF9;&#x8C61;&#x3002;&#x5B83;&#x7684;&#x5185;&#x5BB9;&#x90FD;&#x88AB;&#x521D;&#x59CB;&#x5316;&#x4E3A;0&#x3002;"><code>ArrayBuffer</code></a>&#x3002;</p>

<h2 id="&#x8BED;&#x6CD5;">&#x8BED;&#x6CD5;</h2>

<pre class="syntaxbox"><var>typedArray</var>.buffer</pre>

<h2 id="&#x63CF;&#x8FF0;">&#x63CF;&#x8FF0;</h2>

<p><code>buffer</code> &#x5C5E;&#x6027;&#x662F;&#x4E00;&#x4E2A;&#x8BBF;&#x95EE;&#x5668;&#x5C5E;&#x6027;&#xFF0C;&#x5B83;&#x7684; set &#x8BBF;&#x95EE;&#x5668;&#x51FD;&#x6570;&#x662F;<code>undefined</code>&#xFF0C;&#x610F;&#x601D;&#x662F;&#x4F60;&#x53EA;&#x80FD;&#x591F;&#x8BFB;&#x53D6;&#x8FD9;&#x4E2A;&#x5C5E;&#x6027;&#x3002;&#x5B83;&#x7684;&#x503C;&#x5728;<em>TypedArray</em>&#x6784;&#x9020;&#x65F6;&#x5EFA;&#x7ACB;&#xFF0C;&#x4E0D;&#x80FD;&#x88AB;&#x4FEE;&#x6539;&#x3002;<em>TypedArray</em>&#x662F;&#x8FD9;&#x91CC;&#x7684;<a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray#TypedArray_objects">&#x7C7B;&#x578B;&#x5316;&#x6570;&#x7EC4;</a>&#x4E4B;&#x4E00;&#x3002;</p>

<h2 id="&#x793A;&#x4F8B;">&#x793A;&#x4F8B;</h2>

<h3 id="&#x4F7F;&#x7528;_buffer_&#x5C5E;&#x6027;">&#x4F7F;&#x7528; <code>buffer</code> &#x5C5E;&#x6027;</h3>

<pre class="brush:js">var buffer = new ArrayBuffer(8);
var uint16 = new Uint16Array(buffer);
uint16.buffer; // ArrayBuffer { byteLength: 8 }
</pre>

<h2 id="&#x89C4;&#x8303;">&#x89C4;&#x8303;</h2>

<table class="standard-table">
 <tbody>
  <tr>
   <th scope="col">Specification</th>
   <th scope="col">Status</th>
   <th scope="col">Comment</th>
  </tr>
  <tr>
   <td><a href="http://www.ecma-international.org/ecma-262/6.0/#sec-get-%typedarray%.prototype.buffer" class="external" lang="en" hreflang="en">ECMAScript 2015 (6th Edition, ECMA-262)<br><small lang="zh-CN">TypedArray.prototype.buffer</small></a></td>
   <td><span class="spec-Standard">Standard</span></td>
   <td>&#x521D;&#x59CB;&#x5B9A;&#x4E49;&#x3002;</td>
  </tr>
  <tr>
   <td><a href="https://tc39.github.io/ecma262/#sec-get-%typedarray%.prototype.buffer" class="external" lang="en" hreflang="en">ECMAScript 2017 Draft (ECMA-262)<br><small lang="zh-CN">TypedArray.prototype.buffer</small></a></td>
   <td><span class="spec-Draft">Draft</span></td>
   <td>&#xA0;</td>
  </tr>
 </tbody>
</table>

<h2 id="&#x6D4F;&#x89C8;&#x5668;&#x517C;&#x5BB9;&#x6027;">&#x6D4F;&#x89C8;&#x5668;&#x517C;&#x5BB9;&#x6027;</h2>

<p></p><div class="htab">
    <a name="AutoCompatibilityTable" id="AutoCompatibilityTable"></a>
    <ul>
        <li class="selected"><a>Desktop</a></li>
        <li><a>Mobile</a></li>
    </ul>
</div><p></p>

<div id="compat-desktop">
<table class="compat-table">
 <tbody>
  <tr>
   <th>Feature</th>
   <th>Chrome</th>
   <th>Firefox (Gecko)</th>
   <th>Internet Explorer</th>
   <th>Opera</th>
   <th>Safari</th>
  </tr>
  <tr>
   <td>Basic support</td>
   <td>7.0</td>
   <td><a href="/en-US/Firefox/Releases/4" title="Released on 2011-03-22.">4.0</a> (2)</td>
   <td>10</td>
   <td>11.6</td>
   <td>5.1</td>
  </tr>
 </tbody>
</table>
</div>

<div id="compat-mobile">
<table class="compat-table">
 <tbody>
  <tr>
   <th>Feature</th>
   <th>Android</th>
   <th>Chrome for Android</th>
   <th>Firefox Mobile (Gecko)</th>
   <th>IE Mobile</th>
   <th>Opera Mobile</th>
   <th>Safari Mobile</th>
  </tr>
  <tr>
   <td>Basic support</td>
   <td>4.0</td>
   <td><span title="Please update this with the earliest version of support." style="color: #888;">(Yes)</span></td>
   <td>4.0 (2)</td>
   <td>10</td>
   <td>11.6</td>
   <td>4.2</td>
  </tr>
 </tbody>
</table>
</div>

<h2 id="&#x53E6;&#x89C1;">&#x53E6;&#x89C1;</h2>

<ul>
 <li><a href="/en-US/docs/Web/JavaScript/Typed_arrays">JavaScript &#x7C7B;&#x578B;&#x5316;&#x6570;&#x7EC4;</a></li>
 <li><a href="/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/TypedArray" title="&#x4E00;&#x4E2A;TypedArray &#x5BF9;&#x8C61;&#x63CF;&#x8FF0;&#x4E00;&#x4E2A;&#x8868;&#x793A;&#x5E95;&#x5C42;&#x7684;&#x4E8C;&#x8FDB;&#x5236;&#x6570;&#x636E;&#x7F13;&#x5B58;&#x533A;&#x7684;&#x7C7B;&#x4F3C;&#x6570;&#x7EC4;(array-like)&#x89C6;&#x56FE;&#x3002;&#x6CA1;&#x6709;&#x540D;&#x4E3A;TypedArray&#x7684;&#x5168;&#x5C40;&#x5C5E;&#x6027;&#xFF0C;&#x4E5F;&#x6CA1;&#x6709;&#x76F4;&#x63A5;&#x53EF;&#x89C1;&#x7684;TypedArray&#x6784;&#x9020;&#x51FD;&#x6570;&#x3002;&#x76F8;&#x53CD;&#xFF0C;&#x6709;&#x8BB8;&#x591A;&#x4E0D;&#x540C;&#x7684;&#x5168;&#x5C40;&#x5C5E;&#x6027;&#xFF0C;&#x5176;&#x503C;&#x662F;&#x4E0B;&#x9762;&#x5217;&#x51FA;&#x7684;&#x7279;&#x5B9A;&#x5143;&#x7D20;&#x7C7B;&#x578B;&#x7684;&#x7C7B;&#x578B;&#x5316;&#x6570;&#x7EC4;&#x6784;&#x9020;&#x51FD;&#x6570;&#x3002;&#x5728;&#x4E0B;&#x9762;&#x7684;&#x9875;&#x9762;&#x4E2D;&#xFF0C;&#x4F60;&#x4F1A;&#x627E;&#x5230;&#x53EF;&#x7528;&#x4E8E;&#x5305;&#x542B;&#x4EFB;&#x4F55;&#x7C7B;&#x578B;&#x7684;&#x5143;&#x7D20;&#x7684;&#x4EFB;&#x4F55;&#x7C7B;&#x578B;&#x6570;&#x7EC4;&#x7684;&#x5E38;&#x89C1;&#x5C5E;&#x6027;&#x548C;&#x65B9;&#x6CD5;"><code>TypedArray</code></a></li>
</ul>
                  
                
              