---
title: Command.Call Methods

Id: amfCommandClassCallMethods
TocParent: amfCommandClassMethods
TocOrder: 10

keywords: Call method
keywords: Command.Call method
keywords: MONARCH_CMDPARM
keywords: how to, call interactive program functions from a non-display file aspx.vr
keywords: how to, call non-interactive program functions from a non-display file aspx.vr
keywords: non-display file aspx.vr, calling interactive functions
keywords: non-display file aspx.vr, calling non-interactive functions
keywords: non-display file aspx.vr, Call command
keywords: aspx.vr, non-display file, call commands

---

The <code> **Call** </code> methods can invoke an interactive or process program function. Programs called receive parameters by reference, i.e.: the ASPX code can send and receive data to/from the called program. These parameters are stored in an array of strings. The called program can define its parameters list using fields of type <code>character</code> and <code>decimal</code> (<code>zoned, packed, binary, and decimal</code>).

Interactive calls also require an ASPX page reference where control will be relinquished once the called program finishes execution. Calling interactive programs effectively means a transfer of control, first to the interactive program being called and then to the Callback page reference. Calls that invoke interactive programs can send data into the program via parameters but the output parameter list will be sent to the Callback page by storing the array in the Session under the <code>["MONARCH_CMDPARM"]</code> key.

This overloaded method allows code in non-display file aspx.vr files to invoke interactive or non-interactive program functions within a Job.
<!--mine -->

#### Overloaded List
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="50%" />
            <col width="50%" />
          </colgroup>
          <tr>
            <th>Syntax</th>
            <th>Description</th>
          </tr>
            <tr>
              <td>    <code>[Call ( *string, string, string[ ]* )](amfCommandClassCallMethod1.html)</code>
              </td>
              <td>Calls a non-interactive
              program or function with 
 *assembly name* , 
 *program name* , and the 
 *parameters*  specified.</td>
            </tr>
            <tr>
              <td>    <code>[Call ( *string, string, string[ ], string* )](amfCommandClassCallMethod2.html)</code>
              </td>
              <td>Calls an interactive
              program or function with 
 *assembly name* , 
 *program name* , and 
 *parameters*  specified along with the name of
              the 
 *callback page*  reference where control will be
              relinquished once the called program finishes
              execution.</td>
            </tr>
</table>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!--mine -->

#### See Also
<dl>
        <dd>[Command Class](amfCommandClass.html)</dd>
        <dd>[Command Class Members](amfCommandClassMembers.html)</dd>
        <dd>[ASNA.Monarch Namespace](amfWebDspFASNAMonarchNamespace.html)</dd>
</dl>

