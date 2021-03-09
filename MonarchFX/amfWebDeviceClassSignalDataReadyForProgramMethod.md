---
title: WebDevice.SignalDataReadyForProgram Method

Id: amfWebDeviceClassSignalDataReadyForProgramMethod
TocParent: amfWebDeviceClassMethods
TocOrder: 120

keywords: SignalDataReadyForProgram method
keywords: WebDevice.SignalDataReadyForProgram method
keywords: run state
keywords: ready state
keywords: web device, ready for data from program event
keywords: display files, signal the webdevice thread ready for data from program event
keywords: how to, signals the webdevice thread ready for data from program event

---

Signals the **WebDevice** object thread that the device is ready for data from a program event.

#### Syntax
<pre class="prettyprint"> **BegSr SignalDataReadyForProgram() Access(*Public) Type(Void)**       </pre>  

#### Remarks
This method is used to signal to the **WebDevice** object program thread that the device is ready for data from a program event. The thread state of the current program will be changed from "waiting" to "running" or "ready". Use [ WaitForDataForProgram](amfWebDeviceClassWaitForDataForProgramMethod.html) to place the thread in the 'wait' state.
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
