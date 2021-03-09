---
title: CLProgram.RTVJOBA_JOB Method

Id: amfCLProgramClassRTVJOBA_JOBMethod
TocParent: amfCLProgramClassMethods
TocOrder: 200

keywords: RTVJOBA_JOB method
keywords: CLProgram.RTVJOBA_JOB method
keywords: job name
keywords: job attributes, job name
keywords: CLProgram, get job name from job attributes
keywords: how to, get job name from CLProgram job attributes

---

Reference to the job name from the job attributes for the job in which this CLProgram is used.

#### Syntax
<pre class="syntax"> **BegSr RTVJOBA_JOB Access(*Public) Type(Void)
   DclSrParm *job*  Type(*String) Len(10)**       </pre>

#### Parameters
<dl>
        <dt>
         <code> *job* </code>
        </dt>
        <dd>A string variable containing the name of the job. The
        variable must be at least 10 characters long. If the
        variable length is longer than the job name, it will be
        padded on the right with blanks.</dd>
</dl>

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->      

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
