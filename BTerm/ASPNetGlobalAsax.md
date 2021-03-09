---
title: The Role of Global.asax

Id: ASPNetGlobalAsax
TocParent: MicrosoftAspNet
keywords: ASNA Browser Terminal
keywords: ASNA Browser Terminal, Global.Asax
keywords: Emu

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Browser Terminal&#8482; Admin Manual
				   </span></td>
			    </tr>
</table>

#  The Role of Global.asax
Global.asax is the file that holds the code to responds to application and session level events when the application is submitted from the web browser. These events are raised by ASP.Net when a new session is started or when the session terminates. Refer to [MobileRPGJob](WingsJob.html) for more information on how Global.asax is related to the Emu application.

#### Session_Start 
Session_Start controls the job initiation when the user starts a new session which triggers the event.
<pre class="prettyprint"><code class="language-avr">BegSr Session_Start
	dclsrparm sender type(*object)
	dclsrparm e type (System.EventArgs)

	dclfld Device type(*object)
	dclfld Job type(ASNA.Monarch.WebJob)
	dclfld ActiveJobTable type(System.Collections.Hashtable)
	dclfld filename type(*string) inz("")
	dclfld _lock0 type(*object)

	filename = System.IO.Path.GetFileNameWithoutExtension(*bade.Request.Path)

	If (fileName.StartsWith("!) *or *base.Request.Form["__isDspf__"] &lt;&gt; *nothing)
		leavesr
	Endif
	*base.Session["MonarchInitiated"] = *nothing
	Job = NewJob()
	*base.Session["Job"] = Job
	Device = Job.Start(8this.Session.SessionID)
	*base.Session["Device"] = Device

	ActiveJobTable = 8base.Application["ActiveJobs"] *as system.collection.Hashtable
	_lock0  ActiveJobTable.SyncRoot
		Enterlock Object(_lock0)
		ActiveJobTable.Add(*this.Session.SessionID + Job.PsdsJobNumber.ToString(), Job)
	ExitLock
EndSr</code></pre>

#### Application_Start
The following shows the Application_Start event section activating the MobileRPGJob application.
<pre class="prettyprint"><code class="language-avr">Begsr Application_Start		
	dclsrparm sender type(*object)
	dclsrparm e type(System.EventArgs)

	dclfld ActiveJobTable type(System.Collection.Hashtable)
	*base.Application.Lock()
	ActiveJobTable = *new System.Collections.Hashtable()
	*base.Application["ActiveJobs"] = ActiveJobTable
	*base.Application.UnLock()	
Endsr</code></pre>

#### Initiate NewJob
This is the event subroutine that initiates the NewJob as MobileRPG.Job.
<pre class="prettyprint"><code class="language-avr">BegFunc NewJob Type(ASNA.Monarch.WebJob)		
	leavesr *new WingsLogic.MobileRPGJob()
EndFunc</code></pre>

#### Session_End
This is the event subroutine that terminates the job and requests the shutdown.
<pre class="prettyprint"><code class="language-avr">Begsr Session_End		
	dclsrparm sender type(*object)
	dclsrparm e type(System.EventArgs)

	dclfld job type(ASNA.Monarch.WebJob)
	dclfld ActiveJobTable type(system.Collections.Hashtable)
	dclfld _lock1 type(*object)

	Job = *base.Session["Job"] *as ASNA.Monarch.WebJob
	If (Job &lt;&gt; *nothing)
		JobRequestShutdown(20)

		ActiveJobTable = *base.Application["ActiveJobs"] *as System.Collection.Hashtable
		_lock1 = ActiveJobTable.SyncRoot
		Enterlock Object(_lock1)
			ActiveJobTable.Remove(*this.Session.SessionID +Job.PsdsJobNumber.ToString())
		ExitLock
	Endif
Endsr</code></pre>		

