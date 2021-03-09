---
title: OverrideScope Enumeration

Id: amfOverrideScopeEnumeration
TocParent: amfMonarchNamespaceEnumerations
TocOrder: 50

keywords: enumerations [ASNA.Monarch], OverrideScope
keywords: OverrideScope enumeration
keywords: CallLvl enumeration member
keywords: Job enumeration member
keywords: file overrides, levels

---

The **OverrideScope** enumerated constant defines values for the level of override. Used by [ Job.OverrideFile](amfJobClassOverrideFileMethod2.html), [ Job.DeleteOverride](amfJobClassDeleteOverrideMethod2.html), [ CLProgram.OverrideFile](amfCLProgramClassOverrideFileMethod2.html), and [ CLProgram.DeleteOverride](amfCLProgramClassDeleteOverrideMethod2.html) methods. 

#### Syntax
<pre class="prettyprint"> **BegEnum OverrideScope Access(*Public)** </pre>

#### Remarks
**OverrideScope** denote values that classify the level of override.
<!--mine -->

#### Enumerators
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="15%" />
            <col width="80%" />
            <col width="5%" align="center" />
          </colgroup>
          <tr>
            <th>Member</th>
            <th>Description</th>
            <th>Value</th>
          </tr>
<tr><td>Job</td><td>Job level.</td><td>0</td></tr><tr><td>CallLvl</td><td>Call level.</td><td>1</td></tr>
</table>

<!-- -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](amfMonarchNamespace.html)</td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
<dl><dd>[ASNA.Monarch
    Namespace](amfMonarchNamespace.html)</dd></dl>

