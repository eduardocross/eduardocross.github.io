---
title: WebJob Class Members

Id: amfWebJobClassMembers
TocParent: amfWebJobClass
TocOrder: 5

keywords: WebJob class, all members
keywords: members [ASNA.Monarch], WebJob class

---

[WebJob Class Overview](amfWebJobClass.html) 

#### Constructors
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Method</th>
            <th>Description</th>
          </tr>
          <tr valign="top">
            <td><img  id="IMG1" alt="public property" src="../Images/Constructor.bmp" x-maintain-ratio="TRUE" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [
              WebJob](amfWebJobClassWebJobConstructors.html)
            </td>
            <td>Constructs a new instance
            of 
 **WebJob** .</td>
          </tr>
</table>

<!-- start public properties table -->	

#### Public Properties
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Property</th>
            <th>Description</th>
          </tr>

          <tr valign="top">
            <td><img class="hcp4" alt="public property" src="../Images/property.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              <code>[
              CurrentWebJob](amfWebJobClassCurrentWebJobProperty.html)</code>
            </td>
            <td>Gets a reference to
            the currently running 
 **WebJob**  object.</td>
          </tr><tr>
            <td><img  id="Img8" alt="public property" src="../Images/
property.bmp" x-maintain-ratio="TRUE" width="16" height="16" border="0" />
              <code>[
              Device](amfWebJobClassDeviceProperty.html)</code>
            </td>
            <td>The name of the 
            [
            ASNA.Monarch.WebDevice](amfWebDeviceClass.html) used by the 
 **WebJob** .</td>
          </tr>

</table>

<!--mine -->

#### Public Methods
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Method</th>
            <th>Description</th>
          </tr>
          <tr>
            <td><img  id="Img5" alt="public property" src="../Images/Methods.bmp" x-maintain-ratio="TRUE" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [
              AcceptCommands](amfWebJobClassAcceptCommandsMethod.html)
            </td>
            <td>Prepares a job to accept
            commands.</td>
          </tr>
          <tr>
            <td><img  id="IMG2" alt="public property" src="../Images/Methods.bmp" x-maintain-ratio="TRUE" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [
              EndProgram](amfWebJobClassEndProgramsMethod.html)
            </td>
            <td>Terminates the current 
 **WebJob**  program.</td>
          </tr>
          <tr>
            <td><img  id="Img7" alt="public property" src="../Images/Methods.bmp" x-maintain-ratio="TRUE" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [
              RequestShutDown](amfWebJobClassRequestShutDownMethod.html)
            </td>
            <td>Initiates a timed shut down
            request for the web job.</td>
          </tr>
          <tr>
            <td><img  id="Img6" alt="public property" src="../Images/Methods.bmp" x-maintain-ratio="TRUE" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [ShowPage](amfWebJobClassShowPageMethod.html)
            </td>
            <td>Prepares a job to accept
            commands by presenting an ASPX page to initiate the
            conversation with the user.</td>
          </tr>
          <tr>
            <td><img  id="Img3" alt="public property" src="../Images/Methods.bmp" x-maintain-ratio="TRUE" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [ShutDown](amfWebJobClassShutDownMethod.html)
            </td>
            <td>Ends all active programs,
            closes the database connections for disk and printer
            files, and then aborts the thread assigned to the
            job.</td>
          </tr>
          <tr>
            <td><img  id="Img4" alt="public method" src="../Images/Methods.bmp" x-maintain-ratio="TRUE" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" />
              [
              Start](amfWebJobClassStartMethod.html)
            </td>
            <td>Creates an instance of an 
 **ASNA.Monarch.WebDevice**  object and
            starts the job name specified.</td>
          </tr>
</table>

#### Protected Methods
<table class="dtTABLE" id="table3" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td style="width: 173px"><img alt="public property" src="../Images/promethod.bmp" x-maintain-ratio="TRUE" border="0" />
              [
              ExecuteStartupProgram](amfWebJobClassExecuteStartupProgramMethod.html)
            </td>
            <td>Executes the startup
            command processing program.</td>
          </tr>
</table>

#### See Also
[ASNA.Monarch Namespace](amfMonarchNamespace.html) <br /> [WebJob Class](amfWebJobClass.html) <br /> [ ASNA.Monarch.WebDevice Class](amfWebDeviceClass.html)
