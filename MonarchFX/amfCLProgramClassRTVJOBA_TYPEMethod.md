---
title: CLProgram.RTVJOBA_TYPE Method

Id: amfCLProgramClassRTVJOBA_TYPEMethod
TocParent: amfCLProgramClassMethods
TocOrder: 230

keywords: RTVJOBA_TYPE method
keywords: CLProgram.RTVJOBA_TYPE method
keywords: batch job environment
keywords: interactive job environment
keywords: job attributes, batch job environment
keywords: job attributes, interactive job environment
keywords: CLProgram, get job type environment from job attributes
keywords: how to, get job type environment from CLProgram job attributes

---

Reference to the environment type from the job attributes for the job in which this CLProgram is used.

#### Syntax
<pre class="syntax"> **BegSr RTVJOBA_TYPE Access(*Public) Type(Void)
   DclSrParm *type*  Type(*String) Len(1)**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *type* </code>
        </dt>
        <dd>

A string variable containing the value representing the environment of the job. Environment values are:

- <code>0</code> - Batch job.
- <code>1</code> - Interactive job.

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
