---
title: CLProgram.DeleteOverride(string, OverrideScope)

Id: amfCLProgramClassDeleteOverrideMethod2
TocParent: amfCLProgramClassDeleteOverrideMethods
TocOrder: 20

keywords: enumerations [ASNA.Monarch], OverrideScope, used by
keywords: OverrideScope enumeration, used by

---

Removes the database file override previously applied to the CLProgram.

#### Syntax
<pre class="syntax"> **BegSr DeleteOverride Access(*Public) Type(Void)
   DclSrParm *fileName*  Type(*String)
   DclSrParm *scope*     Type([ASNA.Monarch.OverrideScope](amfOverrideScopeEnumeration.html))**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *fileName* </code>
        </dt>
        <dd>

String containing the database file name from which an override is to be removed.
</dd>
        <dt>
          <code> *scope* </code>
        </dt>
        <dd>

[ ASNA.Monarch.OverrideScope](amfOverrideScopeEnumeration.html). The scope for which the override is to be removed (call or job).
</dd>
</dl>

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [ OverrideFile Method](amfCLProgramClassOverrideFileMethods.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
