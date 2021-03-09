---
title: Command.PushKeyFocus Method

Id: amfCommandClassPushKeyFocusMethod
TocParent: amfCommandClassMethods
TocOrder: 60

keywords: PushKeyFocus method
keywords: Command.PushKeyFocus method
keywords: non-display file aspx.vr, PushKeyFocus command
keywords: aspx.vr, non-display file, PushKeyFocus command
keywords: how to, set display file field focus after silent call

---

Invoked from the yellow thread to provide input to the blue thread program waiting for input. Sets parameter values and returns a WebDisplayFile with the focus set as dictated by those parameters.

#### Syntax
<pre class="syntax"> **BegFunc PushKeyFocus Access(*Public) Type(ASNA.Monarch.WebDisplayFile)
   DclSrParm key           Type(ASNA.Monarch.Command.AidKey)
   DclSrParm virtualRowCol Type(*short)
   DclSrParm fieldname     Type(*String)** 
          </pre>

<!--mine -->

#### Parameters
<dl>
            <dt>
              <code> *key* </code>
            </dt>
            <dd>ASNA.Monarch.Command.AidKey. The enumeration value
        defining the key the program would think was "pressed" by
        the user.</dd>
            <dt>
              <code> *virtualRowCol* </code>
            </dt>
            <dd>Short integer. The virtual row and column of
        the control with focus when the key was "pressed".</dd>
            <dt>
              <code> *fieldname* </code>
            </dt>
            <dd>String. The field name of the control with focus
        when the key was "pressed".</dd>
</dl>

<!--mine -->

#### Returns
<a shape="rect" href="amfWebDisplayFileClass.htm"> ASNA.Monarch.WebDisplayFile</a> with the focus set as dictated by the parameters.
<!--mine -->

#### Remarks
This method does not affect the indicators that would normally be set/reset if the display file would have gone to the browser. In particular, no numeric indicator will be set based on the key "pressed". The waiting program must base its actions on the feedback AID or the INxx indicators.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html) 

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

          <!--mine -->

#### See Also
<dl>
            <dd>
              <a shape="rect" href="amfCommandClass.htm">Command Class</a>
            </dd>
            <dd>
              <a shape="rect" href="amfCommandClassMembers.htm">Command Class Members</a>
            </dd>
            <dd>
              <a shape="rect" href="amfWebDspFASNAMonarchNamespace.htm">ASNA.Monarch Namespace</a>
            </dd>
            <dd>
              <a shape="rect" href="amfFunctionsMainOverview.htm">Web Functions Overview</a>
            </dd>
</dl>

