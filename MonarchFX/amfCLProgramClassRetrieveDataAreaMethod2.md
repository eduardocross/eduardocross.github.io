---
title: CLProgram.RetrieveDataArea(string, integer, integer)

Id: amfCLProgramClassRetrieveDataAreaMethod2
TocParent: amfCLProgramClassRetrieveDataAreaMethods
TocOrder: 20

---

Retrieves selected portion of the local data area associated with the job.

#### Syntax
<pre class="syntax"> **BegFunc RetrieveDataArea Access(*Protected) Type(*String)
   DclSrParm *dataArea*   Type(*String) 
   DclSrParm *start*  Type(*Integer)
   DclSrParm *length*  Type(*Integer)**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *dataArea* </code>
        </dt>
        <dd>

String. The path to the data area to retrieve.
</dd>
        <dt>
          <code> *start* </code>
        </dt>
        <dd>

Integer. The starting point within the data area to be retrieved.
</dd>
        <dt>
         <code> *length* </code>
        </dt>
        <dd>

Integer. The length of the data area to be retrieved.
</dd>
</dl>

#### Return Value
String. Variable containing the partial contents from local *dataArea* as specified by the *start* position and *length* .
<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows Vista Business Edition, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
<a shape="rect" href="amfCLProgramClass.htm">CLProgram Class</a> <br clear="none" /> <a shape="rect" href="amfCLProgramClassMembers.htm"> CLProgram Class Members</a> <br clear="none" /> <a shape="rect" href="amfMonarchNamespace.htm">ASNA.Monarch Namespace</a> 
