---
title: WebJob.ShutDown Method

Id: amfWebJobClassShutDownMethod
TocParent: amfWebJobClassMethods
TocOrder: 70

keywords: ShutDown method
keywords: WebJob.ShutDown method
keywords: how to, shut down a web job
keywords: shutting down a web job
keywords: web job, shutting down

---

This method ends all active programs, closes the database connections for disk and printer files, and then aborts the thread assigned to the job.

#### Syntax
<pre class="prettyprint"><code class="avr"> **BegSr ShutDown Access(*Public) Type(Void)Modifier(*Overrides)** </code> </pre>

#### Remarks
This method ends all active programs, closes the database connections for disk and printer files and then aborts the thread assigned to the job.
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
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016,  Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[WebJob Class](amfWebJobClass.html) <br /> [WebJob Class Members](amfWebJobClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
