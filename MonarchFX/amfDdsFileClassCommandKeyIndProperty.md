---
title: DdsFile.CommandKeyInd Property

Id: amfDdsFileClassCommandKeyIndProperty
TocParent: amfDdsFileClassPropertiesMain
TocOrder: 50

keywords: IndicatorException
keywords: CommandKeyInd property
keywords: DdsFile.CommandKeyInd property
keywords: function keys, setting command key press indicator
keywords: function keys, getting command key press indicator
keywords: attention keys, setting command key press indicator
keywords: attention keys, getting command key press indicator
keywords: aidkeys, setting command key press indicator
keywords: aidkeys, getting command key press indicator
keywords: web controls, setting command key press indicator
keywords: web controls, getting command key press indicator
keywords: display files, setting command key press indicator
keywords: display files, getting command key press indicator

---

Gets or sets the response indicator to set 'on' when the user presses any command key other than "enter".

#### Syntax
<pre class="prettyprint"> **BegProp CommandKeyInd Access(*Public) Type(*Integer)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Specifies which indicator to set on when the user presses any command key other than "enter".

#### Exceptions
The following exceptions may be encountered with this property setting.
<br clear="none" />

<table class="dtTABLE" id="Table3" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold;WIDTH: 50%" />
            <col span="1" style="WIDTH: 50%" />
          </colgroup>
          <tr>
            <th

>Value</th>
            <th

>Condition</th>
          </tr>
          <tr>
            <td>IndicatorException</td>
            <td>An indicator outside the
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
[DdsFile Class](amfDdsFileClass.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
