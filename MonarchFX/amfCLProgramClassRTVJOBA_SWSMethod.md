---
title: CLProgram.RTVJOBA_SWS Method

Id: amfCLProgramClassRTVJOBA_SWSMethod
TocParent: amfCLProgramClassMethods
TocOrder: 220

keywords: RTVJOBA_SWS method
keywords: CLProgram.RTVJOBA_SWS method
keywords: job switches
keywords: job attributes, job switches
keywords: CLProgram, get job switches from job attributes
keywords: how to, get job switches from CLProgram job attributes

---

Reference to the eight switches from the job attributes for the job in which this CLProgram is used.

#### Syntax
<pre class="syntax"> **BegSr RTVJOBA_SWS Access(*Public) Type(void)
   DclSrParm *sws*  Type(*String) Len(8)**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *sws* </code>
        </dt>
        <dd>

A string variable containing the status value of the eight switches used by the job. Each position within <code> *sws* </code> corresponds to a given switch i.e. position 1 is switch 1. Job switch status values are:

- <code>'0'</code> - Off.
- <code>'1'</code> - On.

</dd>
</dl>

<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->      

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [ Job.GetSwitch Method](amfJobClassGetSwitchMethod.html) <br clear="none" /> [ Job.GetSwitches Method](amfJobClassGetSwitchesMethod.html) <br clear="none" /> [ Job.SetSwitch Method](amfJobClassSetSwitchMethod.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
