---
title: Session Timeouts

Id: emSessionTimeOuts
TocParent: WebConfigAppSettings
TocOrder: 20

keywords: ASNA Browser Terminal
keywords: ASNA Browser Terminal, Sessions
keywords: Session Timeouts

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Browser Terminal&#8482; Reference Manual
				   </span></td>
			    </tr>
</table>

# Session Timeouts
This topic describes Session Timeouts, why they occur, how ASNA Browser Terminal handles them, and how developers can customize how they're handled. 

When a BTerm accesses the IBM i, it starts a session like any 5250 terminal, however since BTerm runs in a web browser instead of a standard terminal session, it is possible to close the browser or navigate to another page without properly ending the session and any jobs attached to it. This may lead to system resources being tied up or files being locked to the user of the abandoned session.

**Warning &#8211;** There is no built-in visual cue that a session timeout has occurred. This means that a timed-out user can still fill in fields, but may not be aware that their session has ended until they attempt to submit information. 

By default BTerm pages use the ASP.NET standard of timing out after 20 minutes of inactivity. Inactivity, in this case, refers strictly to information being passed to the server; only clicking the submit button or otherwise sending messages to the IBM i will reset the timer, mouseclicks and information entered into fields will not. The preferred method of changing this setting is through the Microsoft [web.config](http://msdn.microsoft.com/en-us/library/bb756935.aspx"> Internet Information Services (IIS) Manager</a> GUI. In Windows 7, open the **Start menu &#8211; IIS Manager &#8211; Session State** then locate the **Time-out (minutes)** field under Cookie Settings, then click **Apply** on the right. Whatever number you set will be passed as a parameter of the sessionState Timeout method in the <a href="WebConfigAppSettings.html).
![](images/SessionTimeout.png" height="419" width="591)

**Note &#8211;** In order to access this GUI, you muse have the IIS Manager, as well as its .NET Extensibility and ASP.NET components, installed and active. In Windows 7, you can add all the required components through the **Turn Windows Features on or off** dialog.

The sessionState Timout method can also be applied in the [web.config](WebConfigAppSettings.html) file. 

In the [web.config](WebConfigAppSettings.html) file, the sessionState.timeout method can be set inside the &lt;system.web&gt; tag, as shown below.
<pre class="prettyprint">&lt;configuration&gt;
  &lt;system.web&gt;
    &lt;sessionState 
      mode="InProc"
      cookieless="true"
      timeout="30" /&gt;
  &lt;/system.web&gt;
&lt;/configuration&gt;</pre>

Once the Timeout method is triggered, it will call <code>Session_end</code>, which will trigger code to prepare the application for shutdown (eventually closing the DataGate connection). The default parameter passed is set to 20 which tells the <code>Job.Request</code> process to wait up to 20 seconds for the application to finish cleanup. 

Sessions can also be terminated immediately by guiding the Browser Terminal to the EoJ.aspx script, which calls the abandon method and displays Monarch/!ExpiredSession.html. Developers can modify this (static HTML) file to customize its appearance and the message it displays.
