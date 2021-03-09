---
title: DdsRecord.CommandKeyInd Property

Id: amfDdsRecordClassCommandKeyIndProperty
TocParent: amfDdsRecordClassPropertiesMain
TocOrder: 40

keywords: IndicatorException
keywords: CommandKeyInd property
keywords: DdsRecord.CommandKeyInd property
keywords: how to, set response indicator for command key
keywords: how to, get response indicator for command key
keywords: response indicators, setting for dds record command key press
keywords: response indicators, getting for dds record command key press
keywords: web controls, setting response indicator for dds record command key press
keywords: web controls, getting response indicator for dds record command key press
keywords: subfiles, setting response indicator for dds record command key press
keywords: subfiles, getting response indicator for dds record command key press
keywords: subfile controls, setting response indicator for dds record command key press
keywords: subfile controls, getting response indicator for dds record command key press
keywords: subfile records, setting response indicator for command key press
keywords: subfile records, getting response indicator for command key press
keywords: records, setting response indicator for command key press
keywords: records, getting response indicator for command key press
keywords: display files, response indicator for command key press

---

Gets or sets the response indicator to set 'on' when the user presses any command key other than "enter".

#### Syntax
<pre class="prettyprint"> **BegProp CommandKeyInd Access(*Public) Type(*Integer)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Specifies which indicator to set on when the user presses any command key other than "enter".
<!--mine -->

#### Exceptions
The following exceptions may be encountered with this property setting.
<table class="mytable" cellspacing="0" cellpadding="4" width="70%">
          <colgroup><col width="20%" /><col width="50%" />
          </colgroup>
          <tr><th>Value</th>
           <th>Condition</th>
          </tr>
          <tr>
            <td style="height: 31px">IndicatorException</td>
            <td style="height: 31px">An indicator outside the
            01-99 range has been provided.</td>
          </tr>
</table>

#### Remarks
To set the **CommandKeyInd** property at design-time, click on the far right side of the property and enter the response indicator to set *ON when this record changes. The default value is 0.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
