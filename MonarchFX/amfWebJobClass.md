---
title: WebJob Class

Id: amfWebJobClass
TocParent: amfMonarchNamespaceClasses
TocOrder: 250

keywords: WebJob class, about WebJob class
keywords: WebJob class
keywords: classes [ASNA.Monarch], WebJob class

---

The **WebJob** class, which extends [ASNA.Monarch.Job](amfJobClass.html), provides specialized support for interactive applications. This includes creating a new thread every time a Job is started and executing the startup program in it.

For a list of all members of this type, see [WebJob Class Members](amfWebJobClassMembers.html).

#### Inheritance Hierarchy
<pre>[ASNA.Monarch](amfMonarchNamespace.html)
    [ASNA.Monarch.Job](amfJobClass.html)
 **ASNA.Monarch.WebJob**       </pre>

#### Syntax
<pre class="syntax"> **public class WebJob Inherits ASNA.Monarch.Job** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
One of the first tasks of job initiation is the creation of a Monarch device instance which is stored as part of the ASP.Net session collection. The [ WebJob](amfWebJobClassWebJobConstructors.html) constructor creates a new instance of **WebJob** .

The <code>[ Start](amfWebJobClassStartMethod.html)</code> method creates a new instance of an [ ASNA.Monarch.WebDevice](amfWebDeviceClass.html) object for the job specified.

The <code>[ ExecuteStartupProgram](amfWebJobClassExecuteStartupProgramMethod.html)</code> method executes the startup command-processing program.

The <code>[ EndProgram](amfWebJobClassEndProgramsMethod.html)</code> method terminates the current **WebJob** program.

The [ CurrentWebJob](amfWebJobClassCurrentWebJobProperty.html) property returns the current job running.

The <code>[ Device](amfWebJobClassDeviceField.html)</code> field is the name of the **ASNA.Monarch.WebDevice** used by the **WebJob** .

The <code>[ ShutDown](amfWebJobClassShutDownMethod.html)</code> method ends all active programs, closes the database connections for disk and printer files and then aborts the thread assigned to the job.

There are also two methods, [ AcceptCommands](amfWebJobClassAcceptCommandsMethod.html) and <code>[ ShowPage](amfWebJobClassShowPageMethod.html)</code>, that are used to prepare the job to accept commands in a non-displayfile aspx.vr. <code> **ShowPage** </code> also presents an ASPX page to initiate the conversation with the user.
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
[ASNA.Monarch Namespace](amfMonarchNamespace.html) <br /> [WebJob Class Members](amfWebJobClassMembers.html) <br /> [Job Class](amfJobClass.html) 
