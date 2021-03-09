---
title: WebDevice Class

Id: amfWebDeviceClass
TocParent: amfMonarchNamespaceClasses
TocOrder: 230

keywords: WebDevice class
keywords: WebDevice class, about WebDevice class
keywords: classes [ASNA.Monarch], WebDevice class
keywords: device control

---

The **WebDevice** class is responsible for coordinating the job's thread with the one assigned by ASP.NET to produce the response to the browser's request by providing for device control for web display files.

For a list of all members of this type, see [WebDevice Members](amfWebDeviceClassMembers.html).
<!--mine -->

#### Inheritance Hierarchy
<pre> [ASNA.Monarch](amfMonarchNamespace.html)
 **ASNA.Monarch.WebDevice**       </pre>

<!--mine -->

#### Syntax 
<pre class="prettyprint"> **public class WebDevice Inherits System.Object**      </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
The **WebDevice** class provides the device controls.

- [ WebDevice](amfWebDeviceClassWebDeviceConstructors.html) creates an instance of a **WebDevice** object for a **WebJob** object.
- <code>[ Attach](amfWebDeviceClassAttachMethod.html)</code> attaches a **WebDisplayFile** file to a device.
- <code>[ Detach](amfWebDeviceClassDetachMethod.html)</code> is used to remove the device from a file.
- <code>[ SignalDataReadyForProgram](amfWebDeviceClassSignalDataReadyForProgramMethod.html)</code> is used to indicate the device is ready for data from a program event.
- <code>[ SignalDataReadyForUser](amfWebDeviceClassSignalDataReadyForUserMethod.html)</code> is used to indicate the device is ready for data from a user event.
- <code>[ WaitForDataForProgram](amfWebDeviceClassWaitForDataForProgramMethod.html)</code> is used to indicate the device is to wait for data from a program event.
- <code>[ WaitForDataForUser](amfWebDeviceClassWaitForDataForUserMethod.html)</code> is used to indicate the device is to wait for data from a user event.

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
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ASNA.Monarch Namespace](amfMonarchNamespace.html) <br /> [ WebDevice Class Members](amfWebDeviceClassMembers.html) 
