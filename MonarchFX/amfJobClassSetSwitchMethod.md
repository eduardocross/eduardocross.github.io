---
title: Job.SetSwitch Method

Id: amfJobClassSetSwitchMethod
TocParent: amfJobMethods
TocOrder: 160

keywords: SetSwitch method
keywords: Job.SetSwitch method
keywords: jobs, setting attribute switches
keywords: job attribute switches
keywords: sws, setting job attribute switches
keywords: how to, set job attribute switch settings
keywords: CHGJOB SWS()

---

Set a value indicating the 'on'/'off' status of a specific job attribute switch.

#### Syntax
<pre class="prettyprint"> **BegSr SetSwitch Access(*Public) Type(Void)
  DclSrParm *iSwitch*  Type(*Integer2)
  DclSrParm *value*  Type(*Char)** 
      </pre>

#### Parameters
<dl>
        <dt>
 *iSwitch* 
        </dt>
        <dd>An integer value between 1 and 8 representing the
        desired switch.</dd>
        <dt>
 *value* 
        </dt>
        <dd>A one-character value to indicate the status of 
 *iSwitch* . Set the value '0' to turn the switch
        'off' or '1' to turn the switch 'on'.</dd>
</dl>

#### Remarks
RPG programs have access to these switches via the *INUx indicators. In order to support applications using these switches, the **Job** class provides a set of methods to access the 8 values. Additional methods to return these switches are [ GetSwitches](amfJobClassGetSwitchesMethod.html) and [ GetSwitch](amfJobClassGetSwitchMethod.html). The [ CLProgram](amfCLProgramClass.html) class also provides the method [ RTVJOBA_SWS](amfCLProgramClassRTVJOBA_SWSMethod.html) to facilitate the translation of the RTVJOBA CL command SWS attribute.

In addition, when the CL Command CHGJOB keyword SWS(nnnnnnnn) is encountered, the RPG Agent uses this method to set each switch on or off depending on the values in the SWS keyword. 
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
