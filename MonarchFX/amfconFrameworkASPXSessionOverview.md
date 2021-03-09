---
title: Monarch Framework ASPX Session Overview

Id: amfconFrameworkASPXSessionOverview
TocParent: amfASNAMonarchFrameworkConceptsMain
TocOrder: 160

keywords: Monarch framework ASPX session overview
keywords: concepts, Monarch framework ASPX session overview
keywords: ASNA.Monarch, ASP.NET model
keywords: ASPX sessions, workstation files
keywords: ASP.NET model, concepts
keywords: ASPX sessions, display files
keywords: ASPX sessions, Procedural Display File Model
keywords: ASPX sessions, Request/Response Model
keywords: ASPX sessions, lifecyle
keywords: ASPX sessions, about
keywords: ASPX sessions, starting
keywords: ASPX sessions, ending
keywords: ASPX sessions, thread concepts
keywords: global.asax file, about
keywords: global.asax file, session_start
keywords: global.asax file, session_end
keywords: session_start, about
keywords: session_end, about
keywords: lifecycle of ASPX sessions
keywords: ending ASPX sessions, about
keywords: ending ASPX sessions, manually
keywords: ending ASPX sessions, programmatically
keywords: shutdown function, calling
keywords: common.js file, about
keywords: workstation files, about
keywords: workstation files, using DCLWORKSTNFILE
keywords: display files, about
keywords: DCLWORKSTNFILE, about
keywords: concepts, ASNA.Monarch, workstation files
keywords: concepts, ASNA.Monarch, display files
keywords: ASNA.Monarch.WebDspF.Page class, using
keywords: procedural programs, about
keywords: WebJob class, concepts
keywords: WebDevice class, concepts

---

This document deals with the mechanisms available in **ASP.NET** and the **Monarch** Framework to maintain an environment similar enough to the original that migrated interactive programs can produce identical results. On of Monarch's goals is to keep the great majority of migrated code in exactly the same form as the original program. In order to achieve this, it is necessary to have the construct of a **workstation** file with the same semantics as on the IBM i. The basic challenge the Monarch Framework faces is marrying the Procedural Display File Model to the Request / Response Model.

#### Procedural Display File Model
The fact that the original program is built using a procedural top-down design and that a Display File is used for user input brings special challenges when the migrated program is to run in a browser-based environment. In particular, as the program executes, it reaches a point where it needs information from the user and prompts for it via <code> **EXFMT** </code> or a <code> **READ** </code>. The program waits, maintaining the full state of the program, until the user inputs the data and then continues its procedural execution. The program is in control of the execution path and the user simply provides data at the will of the program.

#### Request/Response Model
Browser based applications (formally the HTTP protocol) have a different approach to the way a user interacts with an application. In browser applications, the user requests a particular page and waits until the server sends it in the form of a response. Once the response is sent back, the web server forgets all about the request and the response, therefore it is **stateless** .

Creating applications under a pure HTTP model is hard because here is no connection between sequential requests from a user since each request is isolated.

#### ASP .NET Model
When you are working with an application, you open it, make some changes, and then close it. This is much like a **Session** . The computer knows who you are. It knows when you start the application and when you end. However, on the internet there is one problem: the web server does not know who you are and what you do because the HTTP address does not maintain state.

ASP solves this problem by creating a unique cookie for each user. The cookie is sent to the client and contains information that identifies the user. This interface is called the Session object.

The **Session** object is used to store information about, or change settings for a user session. Variables stored in the Session object are available to all pages in one application. Common information stored in typical session variables is user name, id, and preferences. The server creates a new Session object for each new user and destroys the Session object when the session expires.

#### Monarch Interactive Model
Monarch uses the **ASP.NET** session object to keep track of user jobs. There is a Monarch Job associated with each user in an ASP.NET application; actually, there is a job with each session kept by ASP.NET. As part of the session startup, a new job ([ASNA.Monarch.WebJob](amfWebJobClass.html)) is created, a thread is allocated, and the job is started in this thread. The Job object is stored as part of the ASP.NET session collection.

The **WebJob** class, which extends [ASNA.Monarch.Job](amfJobClass.html), provides specialized support for interactive applications by creating a new thread every time a job is started and executing the startup program in it. WebJob also creates a [WebDevice](amfWebDeviceClass.html) to assist in the implementation of Web Display Files. By creating a Monarch Job *and* a thread for each user, the full state of the migrated program is kept on a per user basis that includes the next point of execution in the program.

The **WebDevice** is responsible for coordinating the job's thread with the one assigned by ASP.NET to produce the response to the browser's request. The following figure depicts the area of responsibility for the two threads.
<dl><dd>
        <img alt="image of the yellow thread versus the procedural blue thread" 
		src="../Images/zzASPX_YellowThreadVSProceduralBlueThreat.JPG" /></dd>
</dl>

The thread on the left (Yellow) is called the ASPX Thread; it is responsible for running the code behind the ASPX pages. At each request, this thread might be different and the ASPX engine is responsible for managing it. The thread on the right (Blue) is known as the Procedural Thread; responsible for running the procedural RPG code.

The threads interact through the WebJob, the WebDevice, and the DataSets that serve as buffers for the Display File data.

#### <a name="SessionLifeCycle"></a>Session Lifecycle
A session starts when a user requests a web page from a web application for the first time. You create a web application by creating a virtual directory; an application includes a file called *Global.asax* . *Global.asax* provides two subroutines, <code> ***Session_Start*** </code> and <code> ***Session_End*** </code>, which get invoked by ASP.NET when the session starts and ends.

When a new session starts in ASP.NET, a new job should be created to support the new user of the application. *<code> **Session_Start** </code>* accomplishes this by instantiating a new <code>MyJob</code> and invoking its <code> ***Start*** </code> method. [ Start](amfWebJobClassStartMethod.html) will create a new procedural thread and then run the [ MyJob.ExecuteStartupProgram](amfWebJobClassExecuteStartupProgramMethod.html) subroutine in it.

By the time <code> *Session_Start* </code> finishes running, there will effectively be two threads serving the user. The ASPX thread, which was running <code> *Session_Start* </code>, will now go on to process the requested page while the procedural thread will be running the startup program. The synchronization of these two threads will be clarified below.

While the user stays active in the application by interacting with the browser, the session will be alive. The session has a timeout property that specifies the amount of idle time between browser requests; this time defaults to 20 minutes. If the user ignores the browser for more than these 20 minutes, ASP.NET will deem the session abandoned and will proceed to end it by invoking the <code> ***Session_End*** </code> subroutine in *Global.asax* . <code> *Session_End* </code> requests the job to execute its Shutdown method, which will end the job and destroy the procedural thread.

#### Ending a WebJob
When <code>MyJob</code> starts, it runs the <code>ExecuteStartupProgram</code> that invokes the startup program. When this program returns to <code>ExecuteStartupProgram</code>, the <code>ExecuteStartupProgram</code> returns to its caller which in turn proceeds to end the Job and destroy the thread running the job as noted above. You can also decide to end the job programmatically in the procedural code or from the browser.

**Programmatically:** 

You can use the <code>[ RequestShutdown](amfWebJobClassRequestShutDownMethod.html)</code> or the <code>[ Shutdown](amfWebJobClassShutDownMethod.html)</code> method of WebJob class to shut down the job. This method ends all active programs, closes the database connections for disk and printer files, and then aborts the thread assigned to the job.

**From the browser:** 

You can use JavaScript to call the <code> ***Shutdown*** </code> function included in with every page sent down to the browser. The <code> *Shutdown* </code> function requests, in an out-of-band call, the [!EOJ.aspx](amf!Eoj.html) page that abandons the ASP.NET session causing the job to be shut down.

Additional functions (<code> **onBrowserClose** </code> and <code> **isBrowserClosing** </code>) are also provided to give the ability to control any cleanup necessary prior to the shutdown. See the [Shutdown functions](amfFunctionsShuttingDown.html) for more specific information.

#### Next: [Moving Data between Workstation File and Display File](amfconFrameworkASPXSessionMovingData.html)

#### Previous: [Conditional Properties Overview](amfconConditionalPropertiesOverview.html)

#### See Also
<dl>
       <dd>[Display File Concepts](amfconDisplayFiles.html)</dd>
       <dd>[Web Server Controls Overview](amfWebServerControlsOverview.html)</dd>
       <dd>[WebDevice Class](amfWebDeviceClass.html)</dd>
       <dd>[WebJob Class](amfWebJobClass.html)</dd>
       <dd>[Job Class](amfJobClass.html)</dd>
       <dd>[WebDisplayFile Class](amfWebDisplayFileClass.html)</dd>
</dl>

