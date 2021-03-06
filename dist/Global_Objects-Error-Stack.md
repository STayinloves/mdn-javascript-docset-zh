
                
                  <div><section class="Quick_links" id="Quick_Links"><!-- --></section> <div class="overheadIndicator nonStandard nonStandardHeader"> 
      <p><strong><span title="This API has not been standardized."><i class="icon-warning-sign"> </i></span> Non-standard</strong><br> 
      This feature is non-standard and is not on a standards track. Do not use it on production sites facing the Web: it will not work for every user. There may also be large incompatibilities between implementations and the behavior may change in the future.</p> 
      </div></div>

<p>The non-standard <strong><code>stack</code></strong> property of <a title="The Error constructor creates an error object. Instances of Error objects are thrown when runtime errors occur. The Error object can also be used as a base object&#xA0;for user-defined exceptions. See below for standard built-in error types." href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error"><code>Error</code></a> objects offer a trace of which functions were called, in what order, from which line and file, and with what arguments. The stack string proceeds from the most recent calls to earlier ones, leading back to the original global scope call.</p>

<h2 id="Description">Description</h2>

<p>Each step will be separated by a newline, with the first part of the line being the function name (if not a call from the global scope), then by an at (@) sign, the file location (except when the function is the error constructor as the error is being thrown), a colon, and, if there is a file location, the line number. (Note that the <a title="The Error constructor creates an error object. Instances of Error objects are thrown when runtime errors occur. The Error object can also be used as a base object&#xA0;for user-defined exceptions. See below for standard built-in error types." href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error"><code>Error</code></a> object also possesses the <code>fileName</code>, <code>lineNumber</code> and <code>columnNumber</code> properties for retrieving these from the error thrown (but only the error, and not its trace).)</p>

<p>Note that this is the format used by Firefox. There is no standard formatting. However, Safari 6+ and Opera 12- use a very similar format. Browsers using the V8 JavaScript engine (such as Chrome, Opera 15+, Android Browser) and IE10+, on the other hand, uses a different format (see these MSDN <a href="http://msdn.microsoft.com/en-us/library/windows/apps/hh699850.aspx" class="external">error.stack</a> docs).</p>

<p><strong>Argument values in the stack</strong>: Prior to Firefox 14 (<a title="FIXED: don&apos;t include actual args in error.stack.toString()" href="https://bugzilla.mozilla.org/show_bug.cgi?id=744842" class="external">bug&#xA0;744842</a>), the function name would be followed by the argument values converted to string in parentheses immediately before the at (<code>@</code>) sign. While an object (or array, etc.) would appear in the converted form <code>&quot;[object Object]&quot;</code>, and as such could not be evaluated back into the actual objects, scalar values could be retrieved (though it may be &#x2014; it is still possible in Firefox 14 &#x2014; easier to use <code>arguments.callee.caller.arguments</code>, as could the function name be retrieved by <code>arguments.callee.caller.name</code>). <code>&quot;undefined&quot;</code> is listed as <code>&quot;(void 0)&quot;</code>. Note that if string arguments were passed in with values such as <code>&quot;@&quot;</code>, <code>&quot;(&quot;</code>, <code>&quot;)&quot;</code> (or if in file names), you could not easily rely on these for breaking the line into its component parts. Thus, in Firefox 14 and later this is less of an issue.</p>

<p>Different browsers set this value at different times. For example, Firefox sets it when creating an <a title="The Error constructor creates an error object. Instances of Error objects are thrown when runtime errors occur. The Error object can also be used as a base object&#xA0;for user-defined exceptions. See below for standard built-in error types." href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error"><code>Error</code></a> object, while PhantomJS sets it only when throwing the <a title="The Error constructor creates an error object. Instances of Error objects are thrown when runtime errors occur. The Error object can also be used as a base object&#xA0;for user-defined exceptions. See below for standard built-in error types." href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error"><code>Error</code></a>, and <a href="http://msdn.microsoft.com/en-us/library/windows/apps/hh699850.aspx" class="external">MSDN docs</a> also seem to match the PhantomJS implementation.</p>

<h2 id="Example">Example</h2>

<p>The following HTML markup demonstrates the use of <code>stack</code> property.</p>

<pre class="brush: html">&lt;!DOCTYPE HTML&gt;
&lt;meta charset=&quot;UTF-8&quot;&gt;
&lt;title&gt;Stack Trace Example&lt;/title&gt;
&lt;body&gt;
&lt;script&gt;
function trace() {
  try {
    throw new Error(&apos;myError&apos;);
  }
  catch(e) {
    alert(e.stack);
  }
}
function b() {
  trace();
}
function a() {
  b(3, 4, &apos;\n\n&apos;, undefined, {});
}
a(&apos;first call, firstarg&apos;);
&lt;/script&gt;
</pre>

<p>Assuming the above markup is saved as <code>C:\example.html</code> on a Windows file system it produces an alert message box with the following text:</p>

<p>Starting with Firefox 30 and later containing the column number (<a title="FIXED: Error stack should contain column number" href="https://bugzilla.mozilla.org/show_bug.cgi?id=762556" class="external">bug&#xA0;762556</a>):</p>

<pre><samp>trace@file:///C:/example.html:9:17
b@file:///C:/example.html:16:13
a@file:///C:/example.html:19:13
@file:///C:/example.html:21:9</samp></pre>

<p>Firefox 14 to Firefox 29:</p>

<pre><samp>trace@file:///C:/example.html:9
b@file:///C:/example.html:16
a@file:///C:/example.html:19
@file:///C:/example.html:21</samp></pre>

<p>Firefox 13 and earlier would instead produce the following text:</p>

<pre><samp>Error(&quot;myError&quot;)@:0
trace()@file:///C:/example.html:9
b(3,4,&quot;\n\n&quot;,(void 0),[object Object])@file:///C:/example.html:16
a(&quot;first call, firstarg&quot;)@file:///C:/example.html:19
@file:///C:/example.html:21</samp></pre>

<h3 id="Stack_of_eval&apos;ed_code">Stack of eval&apos;ed code</h3>

<p>Starting with Firefox 30 (Firefox 30 / Thunderbird 30 / SeaMonkey 2.27 / Firefox OS 1.4), the error stack of code in <code>Function()</code> and <code>eval()</code> calls, now produces stacks with more detailed information about the line and column numbers inside these calls. Function calls are indicated with <code>&quot;&gt; Function&quot;</code> and eval calls with <code>&quot;&gt; eval&quot;</code>. See <a title="FIXED: eval still uses call site line number as offset for eval&apos;ed code in the year 2014" href="https://bugzilla.mozilla.org/show_bug.cgi?id=332176" class="external">bug&#xA0;332176</a>.</p>

<pre class="brush: js">try {
  new Function(&apos;throw new Error()&apos;)();
} catch (e) {
  console.log(e.stack);
}

// anonymous@file:///C:/example.html line 7 &gt; Function:1:1
// @file:///C:/example.html:7:6


try {
  eval(&quot;eval(&apos;FAIL&apos;)&quot;);
} catch (x) {
  console.log(x.stack);
}

// @file:///C:/example.html line 7 &gt; eval line 1 &gt; eval:1:1
// @file:///C:/example.html line 7 &gt; eval:1:1
// @file:///C:/example.html:7:6
</pre>

<p>You can also use the <code>//# sourceURL</code> directive to name an eval source. See also <a href="/en-US/docs/Tools/Debugger/How_to/Debug_eval_sources">Debug eval sources</a> in the <a href="/en-US/docs/Tools/Debugger">Debugger</a> docs and this <a href="http://fitzgeraldnick.com/weblog/59/" class="external">blog post</a>.</p>

<h2 id="Specifications">Specifications</h2>

<p>Not part of any specification. Non-standard.</p>

<h2 id="Browser_compatibility">Browser compatibility</h2>

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
   <td><span title="Please update this with the earliest version of support." style="color: #888;">(Yes)</span></td>
   <td><span title="Please update this with the earliest version of support." style="color: #888;">(Yes)</span></td>
   <td><span title="Please update this with the earliest version of support." style="color: #888;">(Yes)</span></td>
   <td>10</td>
   <td><span title="Please update this with the earliest version of support." style="color: #888;">(Yes)</span></td>
   <td>6</td>
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
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td><span title="Compatibility unknown; please update this." style="color: rgb(255, 153, 0);">?</span></td>
   <td>6</td>
  </tr>
 </tbody>
</table>
</div>

<h2 id="See_also">See also</h2>

<ul>
 <li><a href="/en-US/docs/Components.stack">Components.stack</a></li>
 <li>External projects: <a href="https://github.com/csnover/TraceKit/" class="external link-https">TraceKit</a> and <a href="https://github.com/eriwen/javascript-stacktrace" class="external link-https">javascript-stacktrace</a></li>
 <li>MSDN: <a title="http://msdn.microsoft.com/en-us/library/windows/apps/hh699850.aspx" href="http://msdn.microsoft.com/en-us/library/windows/apps/hh699850.aspx" class="external">error.stack</a> docs</li>
 <li><a href="https://github.com/v8/v8/wiki/Stack%20Trace%20API" class="external">Overview of the V8 JavaScript stack trace API</a></li>
</ul>
                
              