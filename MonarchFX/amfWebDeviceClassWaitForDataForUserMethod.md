---
title: WebDevice.WaitForDataForUser Method

Id: amfWebDeviceClassWaitForDataForUserMethod
TocParent: amfWebDeviceClassMethods
TocOrder: 150

keywords: WaitForDataForUser method
keywords: WebDevice.WaitForDataForUser method
keywords: wait state
keywords: web device, wait for data from user event
keywords: display files, signal the webdevice thread to wait for data from user event
keywords: how to, signals the webdevice thread to wait for data from user event

---

Signals the **WebDevice** object thread the device is to wait for data from a user event.
<pre class="prettyprint"> **BegSr WaitForDataForUser() Access(*Public) Type(Void)**       </pre> 

#### Remarks
This method is used to signal to the **WebDevice** object program thread to wait for data from a user event. The thread state of the current program will be changed from "running" or "ready" to "waiting".

This **WaitForDataForUser** method returns when the WebDevice object is in the signaled state, or when the time-out interval elapses. This function does not return if there is unread input in the queue. It returns only when new input arrives. Use [ SignalDataReadyForUser](amfWebDeviceClassSignalDataReadyForUserMethod.html) when the user input data is available and to remove the wait state.
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
