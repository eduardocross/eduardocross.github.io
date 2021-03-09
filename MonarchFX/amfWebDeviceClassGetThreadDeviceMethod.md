---
title: WebDevice.GetThreadDevice Method

Id: amfWebDeviceClassGetThreadDeviceMethod
TocParent: amfWebDeviceClassMethods
TocOrder: 70

keywords: GetThreadDevice method
keywords: WebDevice.GetThreadDevice method
keywords: device control, getting
keywords: display files, getting device for thread
keywords: shared files, getting for device
keywords: how to, getting shared file for device

---

Returns an instance of a **WebDevice** thread object.

#### Syntax
<pre class="prettyprint"> **BegFunc GetThreadDevice Access(*Public) Type(WebDevice)** </pre>  

<!--mine -->

#### Return Value
An instance of the **WebDevice** thread object containing application instructions.

#### Remarks
A thread can execute a part of an application's code, including code that is currently being executed by another thread. Threads share the virtual address space, global variables, and operating-system resources of their respective processes.
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

#### See Also
[WebDevice Class](amfWebDeviceClass.html) <br /> [ WebDevice Class Members](amfWebDeviceClassMembers.html) <br /> [WebDevice Class](amfWebDeviceClass.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
