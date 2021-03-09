---
title: CLProgram.RTVJOBA_USER Method

Id: amfCLProgramClassRTVJOBA_USERMethod
TocParent: amfCLProgramClassMethods
TocOrder: 240

keywords: RTVJOBA_USER method
keywords: CLProgram.RTVJOBA_USER method
keywords: user profile
keywords: job attributes, user profile
keywords: CLProgram, user profile from job attributes
keywords: how to, get user profile from CLProgram job attributes

---

Reference to the user profile name from the job attributes for the job in which this CLProgram is used.

#### Syntax
<pre class="syntax"> **BegSr RTVJOBA_USER Access(*Public) Type(Void)
   DclSrParm *user*  Type(*String) Len(10)**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *user* </code>
        </dt>
        <dd>

A string variable containing the user profile name associated with the job when the job was started. The user name is the second part of the qualified job name. The variable must be a minimum of 10 characters. If the user profile name is less than allowed by the length of the variable, the value will be padded on the right with blanks.
</dd>
</dl>

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
