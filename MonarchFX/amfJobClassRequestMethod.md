---
title: Job.Request Method

Id: amfJobClassRequestMethod
TocParent: amfJobMethods
TocOrder: 150

keywords: Request method
keywords: Job.Request method
keywords: jobs, closing elegantly switches
keywords: job request
keywords: how to, change force-close delay

---

Sets a value (in seconds) to wait for Monarch (or Wings-related) programs to dispose or shut down elegantly. It has a default value of 20.

#### Syntax
<pre class="prettyprint"> **BegSr Request Access(*Public) Type(Void)
  DclSrParm *Shutdown* (*Integer)** 
      </pre>

#### Parameters
<dl>
        <dt>
 *Shutdown* 
        </dt>
        <dd>An integer value that sets the time (in seconds) that the process 
		should wait for the programs to close before forcibly closing them. Has 
		a default of 20.</dd>
</dl>

#### Remarks
Invoked by default as part of the session_end process in the global.asax file for Monarch and Wings sites.
<!-- start -->

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
[Job Class](amfJobClass.html) <br /> [Job Class Members](amfJobMembers.html) <br /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
