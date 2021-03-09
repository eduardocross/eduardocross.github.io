---
title: Page.RunProgram Property

Id: amfPageClassRunProgramProperty
TocParent: amfPageClassPropertiesMain
TocOrder: 1

keywords: ProgramRunException
keywords: RunProgram property
keywords: Page.RunProgram property
keywords: how to, run program
keywords: program controls, setting to run
keywords: ASP.NET pages, setting to run program
keywords: aspx files, setting to run program

---

Gets or sets a boolean value indicating whether to pass control to the AVR program waiting on an .

#### Syntax
<pre class="syntax"> **BegProp RunProgram Access(*Public) Type(*Boolean)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean. **True** to pass control to the AVR program waiting on an **EXFMT** ; otherwise **False** .

#### Exceptions
The following exceptions may be encountered with this property setting.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="50%" /><col width="50%" />
          </colgroup>
          <tr><th>Value</th>
           <th>Condition</th>
          </tr>
          <tr>
            <td>ProgramRunException</td>
            <td>RunProgram property can
            only be reset to false.</td>
          </tr>
</table>

#### Remarks
This property gets set **true** at page Load if the request is in sequence ([OutOfSequence](amfPageClassOutOfSequenceField.html) **false** ) and an attention key was pressed. This property can be set **false** in any phase after page Load and before process-business-rules ([Control Execution Lifecycle](amfconControlExecutionLifecycle.html)).
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
      <dd>[Page Class](amfPageClass.html)</dd>
      <dd>[Page Class Members](amfPageClassMembers.html)</dd>
      <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd></dl>

