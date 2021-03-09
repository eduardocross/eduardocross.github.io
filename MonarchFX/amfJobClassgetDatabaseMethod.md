---
title: Job.getDatabase Method

Id: amfJobClassgetDatabaseMethod
TocParent: amfJobMethods
TocOrder: 70

keywords: getDatabase method
keywords: Job.getDatabase method
keywords: how to, get job database connection
keywords: jobs, returning database connection
keywords: database connections, job

---

The getDatabase method returns a new instance of ASNA.VisualRPG.Runtime.Database connection object for the job.
<!-- start -->

#### Syntax
<pre class="prettyprint"> **BegFunc getDatabase Access(*Protected) Type(ASNA.VisualRPG.Runtime.Database)**       </pre>

<!-- start -->

#### Return Value
A new instance of ASNA.VisualRPG.Runtime.Database connection for the job.
<!-- start -->

#### Examples
<pre class="prettyprint"><code class="language-avr">BegClass MyJob Extends(ASNA.Monarch.WebJob) Access(*Public)
  DclDB Name(MyDatabase) DBName("MonarchDB") Access(*Public)

  BegFunc getDatabase Type(ASNA.VisualRPG.Runtime.Database) Access(*Protected) Modifier(*Overrides)
     LeaveSR MyDatabase
  EndFunc
EndClass</code>      </pre>

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
            <td>ASNA.VisualRPG.Runtime.</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[Job Class](amfJobClass.html) <br clear="none" /> [Job Class Members](amfJobMembers.html) <br clear="none" /> [ Job.Database Property](amfJobClassDatabaseProperty.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
