---
title: CLProgram.RTVJOBA_DATE Method

Id: amfCLProgramClassRTVJOBA_DATEMethod
TocParent: amfCLProgramClassMethods
TocOrder: 190

keywords: RTVJOBA_DATE method
keywords: CLProgram.RTVJOBA_DATE method
keywords: CLProgram.RTVJOBA_DATE method
keywords: job date
keywords: job attributes, job date
keywords: CLProgram, get date from job attributes
keywords: how to, get date from CLProgram job attributes

---

Reference to the date from the job attributes for the job in which this CLProgram is used.

#### Syntax
<pre class="syntax"> **BegSr RTVJOBA_DATE Access(*Public) Type(Void)
   DclSrParm *date*  Type(*String) Len(6)**       </pre>      

#### Parameters
<dl>
        <dt>
          <code> *date* </code>
        </dt>
        <dd>A string variable containing the date assigned to the
        job by the system when the job was started.</dd>
</dl>

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
