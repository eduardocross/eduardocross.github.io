---
title: WebDevice.WaitForDataForProgram Method

Id: amfWebDeviceClassWaitForDataForProgramMethod
TocParent: amfWebDeviceClassMethods
TocOrder: 140

keywords: WaitForDataForProgram method
keywords: WebDevice.WaitForDataForProgram method
keywords: wait state
keywords: web device, wait for data from program event
keywords: display files, signal the webdevice thread to wait for data from program event
keywords: how to, signal the webdevice thread to wait for data from program event

---

Signals the **WebDevice** object thread the device is to wait for data from a program event.

#### Syntax
<pre class="prettyprint"> **BegSr WaitForDataForProgram() Access(*Public) Type(Void)**       </pre>  

#### Remarks
This method is used to signal to the **WebDevice** object the device is to wait for data from a program event. The thread state of the current program will be changed from "running" or "ready" to "waiting".

This **WaitForDataForProgram** method returns when the WebDevice object is in the signaled state, or when the time-out interval elapses. This function does not return if there is unread input in the queue. It returns only when new input arrives. Use [ SignalDataReadyForProgram](amfWebDeviceClassSignalDataReadyForProgramMethod.html) when the data is available and to remove the wait state.
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
[WebDevice Class](amfWebDeviceClass.html) <br /> [ WebDevice Class Members](amfWebDeviceClassMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
