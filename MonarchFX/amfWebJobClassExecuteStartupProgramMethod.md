---
title: WebJob.ExecuteStartupProgram Method

Id: amfWebJobClassExecuteStartupProgramMethod
TocParent: amfWebJobClassMethods
TocOrder: 30

keywords: how to, startup web job program
keywords: startup web job program
keywords: web job, startup program
keywords: ExecuteStartupProgram method
keywords: WebJob.ExecuteStartupProgram method

---

Executes the startup command-processing program.

#### Syntax
<pre class="prettyprint"><code class="avr"> **BegSr ExecuteStartupProgram Access(*Protected)**  </code></pre>

#### Remarks
This method connects to your database, calls the program, and disconnects from the database.

#### Examples
<pre class="example"><span style="color:blue">BegClass</span> MyJob <span style="color:blue">Extends</span>(ASNA.Monarch.WebJob) <span style="color:blue">Access</span>(<span style="color:gray">*Public</span>)
   <span style="color:blue">DclDB</span><span style="color:blue">Name</span>(MyDatabase) 
   <span style="color:blue">DBName</span>("MonarchDB") <span style="color:blue">Access</span>(<span style="color:gray">*Public</span>)
   <span style="color:blue">BegFunc</span> getDatabase <span style="color:blue">Type</span>(ASNA.VisualRPG.Runtime.Database) <span style="color:blue">Access</span>(<span style="color:gray">*Protected</span>) <span style="color:blue">Modifier</span>(<span style="color:gray">*Overrides</span>)
      <span style="color:blue">LeaveSR</span> MyDatabase
   <span style="color:blue">EndFunc</span>
   <span style="color:#0000ff">BegSr</span>
 **ExecuteStartupProgram**  <span style="color:blue">Access</span>(<span style="color:gray">*Protected</span>) <span style="color:blue">Modifier</span>(<span style="color:gray">*Overrides</span>)
      <span style="color:#0000ff">Connect</span> MyDatabase
      <span style="color:#0000ff">CallD</span> 'MyCompany.MyApplication.Custingc'
      <span style="color:#0000ff">Disconnect</span> MyDataBase
   <span style="color:#0000ff">EndSr</span>
<span style="color:#0000ff">EndClass</span></pre>

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
