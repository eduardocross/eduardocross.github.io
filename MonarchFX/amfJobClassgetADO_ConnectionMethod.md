---
title: Job.getADO_Connection Method

Id: amfJobClassgetADO_ConnectionMethod
TocParent: amfJobMethods
TocOrder: 60

keywords: getADO_Connection method
keywords: Job.getADO_Connection method
keywords: how to, assign ADO database connection for job
keywords: jobs, assigning ADO database connection
keywords: SQL, assigning database connection
keywords: database connection, assigning for job

---

The **getADO_Connection** method returns a new instance of a [ASNA.Monarch](http://msdn2.microsoft.com/en-us/library/system.data.common.dbconnection.aspx"> System.Data.Common.DbConnection</a> object representing an ADO connection to a database.

#### Syntax
<pre class="prettyprint"> **BegFunc getADO_Connection Access(*Protected) Type(System.Data.Common.DbConnection)**       </pre>

#### Return Value
<a href="http://msdn2.microsoft.com/en-us/library/system.data.common.dbconnection.aspx"> System.Data.Common.DbConnection</a> representing an ADO connection to a database.

#### Examples
<pre class="prettyprint"> <code class="language-avr">BegClass MyJob Extends(ASNA.Monarch.WebJob) Access(*Public)
  DclDBName(MyADOConnection) DBName("MonarchtargetDB") Access (*Public)

  BegFunc  getADO_Connection Type(System.Data.Common.DbConnection) Access(*Protected)Modifier(*Overrides)
     LeaveSR MyADOConnection
  EndFunc
EndClass</code></pre>

<!-- start -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td><a href="amfMonarchNamespace.html)</td>
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
[Job Class](amfJobClass.html) <br clear="none" /> [Job Class Members](amfJobMembers.html) <br clear="none" /> [ Job.PrinterDB Property](amfJobClassPrinterDBProperty.html) <br clear="none" /> [ASNA.Monarch Namespace](http://msdn2.microsoft.com/en-us/library/system.data.common.dbconnection.aspx"> System.Data.Common.DbConnection</a> <br clear="none" /> <a href="amfMonarchNamespace.html) 
