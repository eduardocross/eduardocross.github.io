---
title: Job.PsdsJobNumber Field

Id: amfJobClassPsdsJobNumberField
TocParent: amfJobFields
TocOrder: 60

keywords: PsdsJobNumber field
keywords: Job.PsdsJobNumber field
keywords: jobs, number
keywords: PSDS, job number
keywords: program status data structures, job number
keywords: data structures, program status job number
keywords: how to, determine job number

---

The 6-digits job number field in the program status data structure.

#### Field Value
<pre class="prettyprint"> **BegProp PsdsJobNumber Access(*Public) Type(*Decimal)Len(6,0)**       </pre>

#### Field Value
Six digit numeric containing the job number.

#### Remarks
A program status data structure (PSDS) can be defined to make program exception/error information available to a program. There is only one PSDS per module. The job number is in position 264-269 of the data structure.
<!-- start -->

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
[Job Class](amfJobClass.html) <br /> [Job Class Members](amfJobMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
