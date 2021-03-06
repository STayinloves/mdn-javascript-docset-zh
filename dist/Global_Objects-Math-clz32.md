
                
                  
                    <div><section class="Quick_links" id="Quick_Links"><!-- --></section> <div class="overheadIndicator" style="background: #9CF49C;"> 
    <p><strong>&#x8BE5;&#x7279;&#x6027;&#x5904;&#x4E8E; ECMAScript 6 &#x89C4;&#x8303;&#x8349;&#x6848;&#x4E2D;&#xFF0C;&#x76EE;&#x524D;&#x7684;&#x5B9E;&#x73B0;&#x5728;&#x672A;&#x6765;&#x53EF;&#x80FD;&#x4F1A;&#x53D1;&#x751F;&#x5FAE;&#x8C03;&#xFF0C;&#x8BF7;&#x8C28;&#x614E;&#x4F7F;&#x7528;&#x3002;</strong></p> 
</div></div>

<h2 id="Summary" name="Summary">&#x6982;&#x8FF0;</h2>

<p><code><strong>Math.clz32() </strong></code>&#x51FD;&#x6570;&#x8FD4;&#x56DE;&#x4E00;&#x4E2A;&#x6570;&#x5B57;&#x5728;&#x8F6C;&#x6362;&#x6210; 32 &#x65E0;&#x7B26;&#x53F7;&#x6574;&#x5F62;&#x6570;&#x5B57;&#x7684;&#x4E8C;&#x8FDB;&#x5236;&#x5F62;&#x5F0F;&#x540E;, &#x5F00;&#x5934;&#x7684; 0 &#x7684;&#x4E2A;&#x6570;, &#x6BD4;&#x5982; <code>1000000</code> &#x8F6C;&#x6362;&#x6210; 32 &#x4F4D;&#x65E0;&#x7B26;&#x53F7;&#x6574;&#x5F62;&#x6570;&#x5B57;&#x7684;&#x4E8C;&#x8FDB;&#x5236;&#x5F62;&#x5F0F;&#x540E;&#x662F; <code>00000000000011110100001001000000</code>, &#x5F00;&#x5934;&#x7684; 0 &#x7684;&#x4E2A;&#x6570;&#x662F; 12 &#x4E2A;, &#x5219;&#xA0;<code>Math.clz32(1000000)</code> &#x8FD4;&#x56DE; <code>12</code>.</p>

<h2 id="Syntax" name="Syntax">&#x8BED;&#x6CD5;</h2>

<pre class="syntaxbox"><code>Math.clz32 (x)
</code></pre>

<h3 id="Parameters" name="Parameters">&#x53C2;&#x6570;</h3>

<dl>
 <dt>x</dt>
 <dd>&#x4E00;&#x4E2A;&#x6570;&#x5B57;.</dd>
</dl>

<h2 id=".E6.8F.8F.E8.BF.B0" style="line-height: 30px;">&#x63CF;&#x8FF0;</h2>

<p>&quot;clz32&quot; &#x662F; CountLeadingZeroes32 &#x7684;&#x7F29;&#x5199;.</p>

<p>&#x5982;&#x679C;&#xA0;<code>x</code>&#xA0;&#x4E0D;&#x662F;&#x6570;&#x5B57;&#x7C7B;&#x578B;, &#x5219;&#x5B83;&#x9996;&#x5148;&#x4F1A;&#x88AB;&#x8F6C;&#x6362;&#x6210;&#x6570;&#x5B57;&#x7C7B;&#x578B;, &#x7136;&#x540E;&#x518D;&#x8F6C;&#x6210; 32 &#x4F4D;&#x65E0;&#x7B26;&#x53F7;&#x6574;&#x5F62;&#x6570;&#x5B57;.&#xA0;</p>

<p>&#x5982;&#x679C;&#x8F6C;&#x6362;&#x540E;&#x7684; 32 &#x4F4D;&#x65E0;&#x7B26;&#x53F7;&#x6574;&#x5F62;&#x6570;&#x5B57;&#x662F;&#xA0;<code>0</code>, &#x5219;&#x8FD4;&#x56DE; <code>32</code>, &#x56E0;&#x4E3A;&#x6B64;&#x65F6;&#x6240;&#x6709;&#x4F4D;&#x4E0A;&#x90FD;&#x662F;&#xA0;<code>0</code>.</p>

<p><code>NaN</code>, <code>Infinity</code>,<code> -Infinity</code>&#xA0;&#x8FD9;&#x4E09;&#x4E2A;&#x6570;&#x5B57;&#x8F6C;&#x6210; 32 &#x4F4D;&#x65E0;&#x7B26;&#x53F7;&#x6574;&#x5F62;&#x6570;&#x5B57;&#x540E;&#x90FD;&#x662F;&#xA0;<code>0</code>.</p>

<p><span>&#x8FD9;&#x4E2A;&#x51FD;&#x6570;&#x4E3B;&#x8981;&#x7528;&#x4E8E;&#x90A3;&#x4E9B;&#x7F16;&#x8BD1;&#x76EE;&#x6807;&#x4E3A; JS &#x8BED;&#x8A00;&#x7684;&#x7CFB;&#x7EDF;&#x4E2D;, &#x6BD4;&#x5982; Emscripten.</span></p>

<h2 id=".E7.A4.BA.E4.BE.8B">&#x793A;&#x4F8B;</h2>

<pre class="brush: js">Math.clz32(1)                // 31
Math.clz32(1000)             // 22 
Math.clz32()                 // 32
[NaN, Infinity, -Infinity, 0, -0, null, undefined, &quot;foo&quot;, {}, []].filter(function (n) {
  return Math.clz32(n) !== 32
})                           // []
Math.clz32(true)             // 31
Math.clz32(3.5)              // 30
</pre>

<h2 id="Compatibility" name="Compatibility">Polyfill</h2>

<pre class="brush: js">Math.clz32 = Math.clz32 || function(value) {
    var value = Number(value) &gt;&gt;&gt; 0;
    return value ? 32 - value.toString(2).length : 32;
}
</pre>

<h2 id=".E8.A7.84.E8.8C.83">&#x89C4;&#x8303;</h2>

<table class="standard-table">
 <tbody>
  <tr>
   <th scope="col">Specification</th>
   <th scope="col">Status</th>
   <th scope="col">Comment</th>
  </tr>
  <tr>
   <td><a class="external" href="http://people.mozilla.org/~jorendorff/es6-draft.html#sec-Math.clz32" hreflang="en" lang="en">ECMAScript 6 (ECMA-262)<br><small lang="zh-CN">Math.clz32</small></a></td>
   <td><span class="spec-RC">Release Candidate</span></td>
   <td>Initial definition.</td>
  </tr>
 </tbody>
</table>

<h2 id=".E6.B5.8F.E8.A7.88.E5.99.A8.E5.85.BC.E5.AE.B9.E6.80.A7">&#x6D4F;&#x89C8;&#x5668;&#x517C;&#x5BB9;&#x6027;</h2>

<div><div class="htab"> 
    <a id="AutoCompatibilityTable" name="AutoCompatibilityTable"></a> 
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
   <th>Firefox (Gecko)</th>
   <th>Internet Explorer</th>
   <th>Opera</th>
   <th>Safari</th>
  </tr>
  <tr>
   <td>Basic support</td>
   <td>35</td>
   <td><a href="/en-US/Firefox/Releases/31" title="Released on 2014-07-22.">31</a> (31)</td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
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
   <td>31.0 (31)</td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
   <td><span style="color: #f00;">&#x672A;&#x5B9E;&#x73B0;</span></td>
  </tr>
 </tbody>
</table>
</div>

<h2 id="See_also" name="See_also">&#x76F8;&#x5173;&#x94FE;&#x63A5;</h2>

<ul>
 <li><a href="/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math" title="Math&#xA0;&#x4E3A;&#x65B9;&#x4FBF;&#x6570;&#x5B66;&#x8BA1;&#x7B97;&#x6240;&#x9700;&#x7684;&#x5E38;&#x91CF;&#x548C;&#x51FD;&#x6570;&#x63D0;&#x4F9B;&#x4E86;&#x5C5E;&#x6027;&#x548C;&#x65B9;&#x6CD5;.&#x8BE5;&#x5185;&#x7F6E;&#x5BF9;&#x8C61;&#x4E0D;&#x662F;&#x51FD;&#x6570;&#x5BF9;&#x8C61;."><code>Math</code></a></li>
</ul>
                  
                
              