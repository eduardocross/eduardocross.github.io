---
title: shutDown Function

Id: amfFunctionsShuttingDown
TocParent: amfFunctionsMainOverview
TocOrder: 110

keywords: shutdown client-side function
keywords: client-side functions, simulating key press
keywords: client-side functions, shutdown
keywords: client-side functions, isBrowserClosing
keywords: client-side events, onBrowserClose
keywords: client-side events, onClickEvent
keywords: client-side functions, shutdown
keywords: form control functions, simulating key press
keywords: form control functions, isBrowserClosing
keywords: form control events, onBrowserClose
keywords: form control functions, client-side shutdown
keywords: isBrowserClosing function, client-side
keywords: onBrowserClose event, client-side
keywords: onClientClick event, client-side
keywords: client-side shutdown

---

When MyJob starts, it runs the <code>[ExecuteStartupProgram](amfWebJobClassExecuteStartupProgramMethod.html)</code>, which invokes the startup program. When this program returns to <code> **ExecuteStartupProgram** </code>, it then returns to its caller, which in turn proceeds to end the Job and destroy the thread running the job. You can also decide to end the job programmatically in the procedural code or from the browser.

Programmatically you can use the <code>[ RequestShutdown](amfWebJobClassRequestShutDownMethod.html)</code> or the <code>[ Shutdown](amfWebJobClassShutDownMethod.html)</code> method of WebJob class to shut down the job. This method ends all active programs, closes the database connections for disk and printer files, and then aborts the thread assigned to the job.

From the browser you can use JavaScript to call the <code> ***Shutdown*** </code> function available that requests, in an out-of-band call, the [!EOJ.aspx](amf!Eoj.html) page that abandons the ASP.NET session causing the job to be shut down.

There are two javascript functions that are used for control of a client-side shutdown to provide some programming cleanup if needed. They are <code> **onBrowserClose()** </code> and <code> **isBrowserClosing()** </code>.

### <code>onBrowserClose()</code>
**<code>onBrowserClose()</code>** will check for the existence of function **<code>isBrowserClosing()</code>** and its return value to see if a client-side shutdown has been requested. If the return value is true, the function will call ** *Shutdown* ** terminating the Job on the server, while a return value of false will prevent the shutdown. Be aware that **<code>onBrowserClose()</code>** will do nothing if **<code>isBrowserClosing()</code>** is not defined. If the call does not occur, the user's job will remain active until the time limit specified in the session timeout property is reached.

### <code>isBrowserClosing()</code>
<code> **isBrowserClosing()** </code> can be used to perform any checks and cleanup before returning <code>True</code> to request the shutdown or <code>False</code> to prevent the shutdown. 

### Example 1
In this example, an action is required on the part of the user to initiate the shutdown on the client side when there are certain conditions or cleanup that needs to occur before the shutdown can occurs. **This removes the user's ability to use the browser's Close button** .

Verify that the body tag does NOT have <code> **OnUnload** </code> specified:
<pre class="example">
            <span style="COLOR:blue">&lt;<span style="COLOR:maroon">body</span>&gt;</span>
          </pre>

Add the JavaScript function <code> **isBrowserClosing()** </code> to the display file inside the <code>&lt;head&gt;</code> or <code>&lt;body&gt;</code> tag similar to the following:
<pre class="example">
            <span style="COLOR: blue">&lt;<span style="COLOR: maroon">script</span><span style="COLOR: red">language</span>="javascript" <span style="COLOR: red">type</span>="text/javascript"&gt;</span>
 {         
   <span style="COLOR: blue">function</span> **isBrowserClosing()**    
      <span style="COLOR: green">// programmer can perform desired checks and/or cleanup here</span><span style="COLOR: blue">return true;  
      <span style="COLOR:green">// request shutdown</span></span>
 }  
<span style="COLOR: blue">&lt;/<span style="COLOR: maroon">script</span>&gt;</span></pre>

In the body section, you then attach <code> **onBrowserClose** </code> to the <code> **onClientClick** </code> event of a control like those shown below for a button that the user presses to initiate the shutdown.
<pre class="example">
            <span style="COLOR:blue">&lt;<span style="COLOR:maroon">asp</span>:<span style="COLOR:maroon">Button</span><span style="COLOR:red">ID</span>="Btn1 <span style="COLOR:red">runat</span>="server" <span style="COLOR:red">onClientClick</span>="onBrowserClose()" <span style="COLOR:red">Text</span>="Bye" /&gt;</span> </pre>

### Example 2
Similar to the above, this example uses the <code> **isBrowserClosing()** </code> function as the <code> **onClientClick** </code> event for the user control button for the shutdown and bypasses <code> **onBrowserClose()** </code>. **This also removes the user's ability to use the browser's close button** .

As above, the <code><span style="COLOR:blue">&lt;<span style="COLOR:maroon">body</span>&gt;</span></code> tag must NOT have <code> **onunload** </code> specified. Add the JavaScript function <code> **isBrowserClosing()** </code> to the display file manually inside the <code>&lt;head&gt;</code> or <code>&lt;body&gt;</code> tag similar to the following:
<pre class="example">
            <span style="COLOR: blue">&lt;<span style="COLOR: macroon">script</span><span style="COLOR: red">language</span>="javascript" <span style="COLOR: red">type</span>="text/javascript"&gt;</span>
{     
      <span style="COLOR: blue">function</span> **isBrowserClosing()**      
      <span style="COLOR: green">// programmer can perform desired checks and/or cleanup here</span><span style="COLOR: blue">Shutdown()</span>;
}
<span style="COLOR: blue">&lt;/<span style="COLOR: maroon">script</span>&gt;</span></pre>

In the body section, set the <code> **onClientClick** </code> event to <code> **isBrowserClosing** </code> for the button that the user presses to initiate the shutdown:
<pre class="example">
            <span style="color:blue">&lt;<span style="color:maroon">asp:Button</span><span style="color:#ff0000">ID</span>="Btn1" <span style="color:#ff0000">runat</span>="server" <span style="color:red">onClientClick</span>="isBrowserClosing()" <span style="color:red">Text</span>="Bye" /&gt;</span>
          </pre>

### Example 3
This example shows how to control the shutdown if you need to retain the early Monarch behaviors that allows the session to terminate when the user clicks on the browser's close button.

Ensure the body tag has <code> **onunload** </code> as shown here:
<pre class="example">
            <span style="color:blue">&lt;<span style="color:maroon">body</span><span style="color:red">onunload</span>="onBrowserClose();" &gt;</span>
          </pre>

Then place the following within the head or body section:
<pre class="example">
            <span style="COLOR: blue">&lt;</span>
            <span style="COLOR: #993300">script</span>
            <span style="COLOR: red">language</span>
            <span style="COLOR: blue">="javascript"</span>
            <span style="COLOR: red">type</span> ="text/javascript"&gt;
   <span style="COLOR: green">// Allow user to use Browser's close button to end session</span><span style="COLOR: blue">function</span> **isBrowserClosing()** 
  {
       <span style="COLOR: blue">If</span>(<span style="COLOR: blue">event</span> &amp;&amp; <span style="COLOR: blue">event</span>.clientX &lt; 0 &amp;&amp; <span style="COLOR: blue">event</span>.clientY &lt; 0)
          <span style="COLOR: green">// programmer can perform desired checks and/or cleanup here</span><span style="COLOR: blue">return true;</span>   
          <span style="COLOR: green">// do shutdown</span><span style="COLOR: blue">else
          return false;</span>  
        <span style="color: green">// do not shutdown</span>
 }
<span style="COLOR: blue">&lt;/<span style="COLOR: maroon">script</span>&gt;</span></pre>

### See Also
<dl>
        <dd>[Web Server Controls Overview](amfWebServerControlsOverview.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Class Library](amfWebDspFClassLibraryMain.html)</dd>
        <dd>[Web Functions Overview](amfFunctionsMainOverview.html)</dd>
</dl>

