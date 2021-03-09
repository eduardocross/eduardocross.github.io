---
title: CLProgram.RetrieveDataArea(string)

Id: amfCLProgramClassRetrieveDataAreaMethod1
TocParent: amfCLProgramClassRetrieveDataAreaMethods
TocOrder: 10

---

Returns the local data area associated with the job.

#### Syntax
<pre class="syntax"> **BegFunc RetrieveDataArea Access(*Protected) Type(*String)
   DclSrParm *dataArea*  Type(*String)**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *dataArea* </code>
        </dt>
        <dd>String. The path to the data area to retrieve.</dd>
</dl>

#### Return Value
String. Variable containing the contents of the local *dataArea* .

#### Remarks
If you want to retrieve many subfields, use this method and then use <code>[ Percent_SST](amfCLProgramClassPercent_SSTMethod.html)</code> to extract subfields.
<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [Percent_SST Method](amfCLProgramClassPercent_SSTMethod.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
