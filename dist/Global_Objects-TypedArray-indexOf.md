
                
                  
                    <div><section class="Quick_links" id="Quick_Links"><!-- --></section></div>

<p><code><strong>indexOf()</strong></code> &#x65B9;&#x6CD5;&#x8FD4;&#x56DE;&#x5728;&#x7C7B;&#x578B;&#x6570;&#x7EC4;&#x4E2D;&#x53EF;&#x4EE5;&#x627E;&#x5230;&#x7ED9;&#x5B9A;&#x5143;&#x7D20;&#x7684;&#x7B2C;&#x4E00;&#x4E2A;&#x7D22;&#x5F15;&#xFF0C;&#x5982;&#x679C;&#x4E0D;&#x5B58;&#x5728;&#xFF0C;&#x5219;&#x8FD4;&#x56DE;-1&#x3002; &#x65B9;&#x6CD5;&#x5177;&#x6709;&#x4E0E; <a href="/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf" title="indexOf()&#x65B9;&#x6CD5;&#x8FD4;&#x56DE;&#x5728;&#x6570;&#x7EC4;&#x4E2D;&#x53EF;&#x4EE5;&#x627E;&#x5230;&#x7ED9;&#x5B9A;&#x5143;&#x7D20;&#x7684;&#x7B2C;&#x4E00;&#x4E2A;&#x7D22;&#x5F15;&#xFF0C;&#x5982;&#x679C;&#x4E0D;&#x5B58;&#x5728;&#xFF0C;&#x5219;&#x8FD4;&#x56DE;-1&#x3002;"><code>Array.prototype.indexOf()</code></a> &#x76F8;&#x540C;&#x7684;&#x7B97;&#x6CD5;&#x3002; TypedArray&#x662F;&#x8FD9;&#x91CC;&#x7684;<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/TypedArray#TypedArray_objects">&#x7C7B;&#x578B;&#x5316;&#x6570;&#x7EC4;&#x7C7B;&#x578B;</a>&#x4E4B;&#x4E00;&#x3002;</p>

<h2 id="&#x8BED;&#x6CD5;">&#x8BED;&#x6CD5;</h2>

<pre class="syntaxbox"><code><var>typedarray</var>.<var>i<code>ndexOf(<var>searchElement</var>[, <var>fromIndex</var> = 0])</code></var></code></pre>

<h3 id="&#x53C2;&#x6570;">&#x53C2;&#x6570;</h3>

<dl>
 <dt><code>searchElement</code></dt>
 <dd>&#x9700;&#x8981;&#x5728;&#x7C7B;&#x578B;&#x5316;&#x6570;&#x7EC4;&#x4E2D;&#x5B9A;&#x4F4D;&#x7684;&#x5143;&#x7D20;</dd>
 <dt><code>fromIndex</code></dt>
 <dd>&#x641C;&#x7D22;&#x7684;&#x8D77;&#x59CB;&#x4E0B;&#x6807;&#x3002;&#x5982;&#x679C;&#x4E0B;&#x6807;&#x5927;&#x4E8E;&#x7B49;&#x4E8E;&#x7C7B;&#x578B;&#x5316;&#x6570;&#x7EC4;&#x957F;&#x5EA6;&#xFF0C;&#x5219;&#x8FD4;&#x56DE; -1&#xFF0C;&#x610F;&#x601D;&#x662F;&#x7C7B;&#x578B;&#x5316;&#x6570;&#x7EC4;&#x4E0D;&#x4F1A;&#x88AB;&#x641C;&#x7D22;&#x3002;&#x5982;&#x679C;&#x63D0;&#x4F9B;&#x7684;&#x4E0B;&#x6807;&#x503C;&#x662F;&#x8D1F;&#x6570;&#xFF0C;&#x5219;&#x88AB;&#x5F53;&#x505A;&#x8DDD;&#x79BB;&#x7C7B;&#x578B;&#x5316;&#x6570;&#x7EC4;&#x5C3E;&#x90E8;&#x7684;&#x504F;&#x79FB;&#x3002;&#x6CE8;&#xFF1A;&#x5982;&#x679C;&#x63D0;&#x4F9B;&#x7684;&#x4E0B;&#x6807;&#x662F;&#x8D1F;&#x6570;&#xFF0C;&#x7C7B;&#x578B;&#x5316;&#x6570;&#x7EC4;&#x4ECD;&#x7136;&#x4ECE;&#x524D;&#x5230;&#x540E;&#x641C;&#x7D22;&#x3002;&#x5982;&#x679C;&#x8BA1;&#x7B97;&#x51FA;&#x6765;&#x7684;&#x4E0B;&#x6807;&#x5C0F;&#x4E8E; 0&#xFF0C;&#x5219;&#x4F1A;&#x641C;&#x7D22;&#x6574;&#x4E2A;&#x7C7B;&#x578B;&#x5316;&#x6570;&#x7EC4;&#x3002;&#x9ED8;&#x8BA4;&#x4E3A; 0&#xFF08;&#x641C;&#x7D22;&#x6574;&#x4E2A;&#x7C7B;&#x578B;&#x5316;&#x6570;&#x7EC4;&#xFF09;&#x3002;</dd>
</dl>

<h3 id="&#x8FD4;&#x56DE;&#x503C;">&#x8FD4;&#x56DE;&#x503C;</h3>

<p>&#x6570;&#x7EC4;&#x4E2D;&#x5143;&#x7D20;&#x7684;&#x7B2C;&#x4E00;&#x4E2A;&#x4E0B;&#x6807;&#xFF1B;&#x6CA1;&#x6709;&#x627E;&#x5230;&#x5219;&#x8FD4;&#x56DE;<strong>-1</strong> &#x3002;</p>

<h2 id="&#x63CF;&#x8FF0;">&#x63CF;&#x8FF0;</h2>

<p><code>indexOf</code>&#x4F7F;&#x7528;<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators#Using_the_Equality_Operators">&#x4E25;&#x683C;&#x76F8;&#x7B49;</a> &#xFF08;&#x7531; === &#x6216;&#x4E09;&#x7B49;&#x53F7;&#x8FD0;&#x7B97;&#x7B26;&#x4F7F;&#x7528;&#x7684;&#x76F8;&#x540C;&#x65B9;&#x6CD5;&#xFF09;&#x6BD4;&#x8F83;<code>searchElement</code>&#x548C;&#x7C7B;&#x578B;&#x5316;&#x6570;&#x7EC4;&#x7684;&#x5143;&#x7D20;&#x3002;</p>

<h2 id="&#x793A;&#x4F8B;">&#x793A;&#x4F8B;</h2>

<pre class="brush: js">var uint8 = new Uint8Array([2, 5, 9]);
uint8.indexOf(2);     // 0
uint8.indexOf(7);     // -1
uint8.indexOf(9, 2);  // 2
uint8.indexOf(2, -1); // -1
uint8.indexOf(2, -3); // 0
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
   <td><a href="http://www.ecma-international.org/ecma-262/6.0/#sec-%typedarray%.prototype.indexof" class="external" lang="en" hreflang="en">ECMAScript 2015 (6th Edition, ECMA-262)<br><small lang="zh-CN">TypedArray.prototype.indexOf</small></a></td>
   <td><span class="spec-Standard">Standard</span></td>
   <td>&#x521D;&#x59CB;&#x5B9A;&#x4E49;&#x3002;</td>
  </tr>
  <tr>
   <td><a href="https://tc39.github.io/ecma262/#sec-%typedarray%.prototype.indexof" class="external" lang="en" hreflang="en">ECMAScript 2017 Draft (ECMA-262)<br><small lang="zh-CN">TypedArray.prototype.indexOf</small></a></td>
   <td><span class="spec-Draft">Draft</span></td>
   <td>&#xA0;</td>
  </tr>
 </tbody>
</table>

<h2 id="&#x6D4F;&#x89C8;&#x5668;&#x517C;&#x5BB9;&#x6027;">&#x6D4F;&#x89C8;&#x5668;&#x517C;&#x5BB9;&#x6027;</h2>

<div><div class="htab">
    <a name="AutoCompatibilityTable" id="AutoCompatibilityTable"></a>
    <ul>
        <li class="selected"><a>Desktop</a></li>
        <li><a>Mobile</a></li>
    </ul>
</div></div>

<div id="compat-desktop">
<table class="compat-table">
 <tbody>
  <tr>
   <th>Feature</th>
   <th>Chrome</th>
   <th>Edge</th>
   <th>Firefox (Gecko)</th>
   <th>Internet Explorer</th>
   <th>Opera</th>
   <th>Safari</th>
  </tr>
  <tr>
   <td>Basic support</td>
   <td>45</td>
   <td><span title="Please update this with the earliest version of support." style="color: #888;">(Yes)</span></td>
   <td><a href="/en-US/Firefox/Releases/37" title="Released on 2015-04-07.">37</a> (37)</td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
   <td>32</td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
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
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
   <td><a href="/en-US/Firefox/Releases/37" title="Released on 2015-04-07.">37</a> (37)</td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
  </tr>
 </tbody>
</table>
</div>

<h2 id="&#x517C;&#x5BB9;&#x6027;&#x6CE8;&#x89E3;">&#x517C;&#x5BB9;&#x6027;&#x6CE8;&#x89E3;</h2>

<ul>
 <li>&#x81EA; Firefox 47 (Firefox 47 / Thunderbird 47 / SeaMonkey 2.44)&#x8D77;&#xFF0C;&#x8FD9;&#x4E2A;&#x65B9;&#x6CD5;&#x4E0D;&#x518D;&#x8FD4;&#x56DE;<code>-0</code>&#x3002;<br>
  &#x4F8B;&#x5982;&#xFF0C; <code>new Uint8Array([0]).indexOf(0, -0)</code> &#x73B0;&#x5728;&#x59CB;&#x7EC8;&#x8FD4;&#x56DE; <code>+0</code> (<a href="https://bugzilla.mozilla.org/show_bug.cgi?id=1242043" class="external" title="FIXED: {Array,%TypedArray%}.prototype.{i,lastI}ndexOf should never return -0">bug&#xA0;1242043</a>)&#x3002;</li>
</ul>

<h2 id="&#x53E6;&#x89C1;">&#x53E6;&#x89C1;</h2>

<ul>
 <li><a href="/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/TypedArray/lastIndexOf" class="new" title="&#x6B64;&#x9875;&#x9762;&#x4ECD;&#x672A;&#x88AB;&#x672C;&#x5730;&#x5316;, &#x671F;&#x5F85;&#x60A8;&#x7684;&#x7FFB;&#x8BD1;!"><code>TypedArray.prototype.lastIndexOf()</code></a></li>
 <li><a href="/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf" title="indexOf()&#x65B9;&#x6CD5;&#x8FD4;&#x56DE;&#x5728;&#x6570;&#x7EC4;&#x4E2D;&#x53EF;&#x4EE5;&#x627E;&#x5230;&#x7ED9;&#x5B9A;&#x5143;&#x7D20;&#x7684;&#x7B2C;&#x4E00;&#x4E2A;&#x7D22;&#x5F15;&#xFF0C;&#x5982;&#x679C;&#x4E0D;&#x5B58;&#x5728;&#xFF0C;&#x5219;&#x8FD4;&#x56DE;-1&#x3002;"><code>Array.prototype.indexOf()</code></a></li>
</ul>
                  
                
              