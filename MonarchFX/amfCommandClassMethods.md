---
title: Command Methods

Id: amfCommandClassMethods
TocParent: amfCommandClass
TocOrder: 20

keywords: Command class, methods
keywords: methods [ASNA.Monarch], Command class

---

This topic contains a listing of the methods in the [Command Class](amfCommandClass.html). 
<!--mine -->

#### Methods
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Method</th>
            <th>Description</th>
          </tr>

          <tr>
            <td><img class="hcp4" alt="public method" src="Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [<code>Call</code>](amfCommandClassCallMethods.html)
            </td>
            <td>Overloaded. Call allows
            code in non-display file aspx.vr to invoke diverse
            program functions within a Job.</td>
          </tr>
          <tr>
            <td><img class="hcp4" alt="public method" src="Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [
              <code>CallSilent</code>](amfCommandClassCallSilentMethod.html)
            </td>
            <td>Invokes an interactive
            program from a non-display file aspx.vr (yellow thread)
            and prevents the display of the program's display
            file in the browser.</td>
          </tr>
          <tr>
            <td><img class="hcp4" alt="public method" src="Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [
              <code>GetLdaField</code>](amfCommandClassGetLdaFieldMethod.html)
            </td>
            <td>Returns a value from
            a portion of the jobs' LDA (local data
            area).  </td>
          </tr>
          <tr>
            <td><img class="hcp4" alt="public method" src="Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [
              <code>GetLdcObject</code>](amfCommandClassGetLdcObjectMethod.html)
            </td>
            <td>Returns the
            value for an entry from the jobs' LDC
            (local data collection).</td>
          </tr>
          <tr>
            <td><img class="hcp4" alt="public method" src="Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [
              <code>PushKeyFocus</code>](amfCommandClassPushKeyFocusMethod.html)
            </td>
            <td>Invoked from the yellow
            thread to provide input to the blue thread program
            waiting for input.  Sets parameter values and
            returns a WebDisplayFile with the focus set as dictated
            by those parameters.</td>
          </tr>
          <tr>
            <td>  <img class="hcp4" alt="public method" src="Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [
              <code>RemoveLdcObject</code>](amfCommandClassRemoveLdcObjectMethod.html)
            </td>
            <td>Removes an entry
            from the jobs' LDC (local data collection).</td>
          </tr>
          <tr>
            <td>  <img class="hcp4" alt="public method" src="Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [
              <code>RequestShutdown</code>](amfCommandClassRequestShutdownMethod.html)
            </td>
            <td>Requests the job to
            shutdown.  All active programs in the job will be
            ended.</td>
          </tr>
          <tr>
            <td>  <img class="hcp4" alt="public method" src="Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [<code>Return</code>](amfCommandClassReturnMethod.html)
            </td>
            <td>Returns a job to procedural
            processing.</td>
          </tr>
          <tr>
            <td>  <img class="hcp4" alt="public method" src="Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [
              <code>SetLdaField</code>](amfCommandClassSetLdaFieldMethod.html)
            </td>
            <td>Assigns a
            value to a portion of the jobs' LDA (local
            data area).  </td>
          </tr>
          <tr>
            <td>  <img class="hcp4" alt="public method" src="Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [
              <code>SetLdcObject</code>](amfCommandClassSetLdcObjectMethod.html)
            </td>
            <td>Assigns a
            value to an entry in the jobs' LDC
            (local data collection).</td>
          </tr>
</table>

<!--mine -->

#### See Also
<dl>
        <dd>[Command Class](amfCommandClass.html)</dd>
        <dd>[Command Class Members](amfCommandClassMembers.html)</dd>
        <dd>[ASNA.Monarch Namespace](amfWebDspFASNAMonarchNamespace.html)</dd>
</dl>

