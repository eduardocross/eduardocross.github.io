---
title: Job.GetSwitch Method

Id: amfJobClassGetSwitchMethod
TocParent: amfJobMethods
TocOrder: 120

keywords: GetSwitch method
keywords: Job.GetSwitch method
keywords: jobs, getting attribute switches
keywords: job attribute switches
keywords: sws, getting job attribute switches
keywords: how to, set job attribute switch settings

---

Returns a value indicating the 'on'/'off' status of a specific job attribute switch.

#### Syntax
<pre class="prettyprint">
 **BegFunc GetSwitch Access(*Public) Type(*Char)
  DclSrParm *iSwitch*  Type(*Integer2)** 
            </pre>

#### Parameters
<dl>
              <dt>
 *iSwitch* 
              </dt>
              <dd>An integer value between 1 and 8 representing the
        desired switch.</dd>
</dl>

#### Return Value
A '0' if the switch is 'off' or a '1' if the switch is 'on'.

#### Remarks
RPG programs have access to these switches via the *INUx indicators. In order to support applications using these switches, the **Job** class provides a set of methods to access the 8 values. Additional methods to return or set these switches are [ GetSwitches](amfJobClassGetSwitchesMethod.html) and [ SetSwitch](amfJobClassSetSwitchMethod.html). The [ CLProgram](amfCLProgramClass.html) class also provides the method [ RTVJOBA_SWS](amfCLProgramClassRTVJOBA_SWSMethod.html) to facilitate the translation of the RTVJOBA CL command SWS attribute.
<!-- start -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](amfMonarchNamespace.html)</td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.VisualRPG.Runtime.</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[Job Class](amfJobClass.html) <br clear="none" /> [Job Class Members](amfJobMembers.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
