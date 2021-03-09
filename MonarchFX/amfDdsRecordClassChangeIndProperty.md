---
title: DdsRecord.ChangeInd Property

Id: amfDdsRecordClassChangeIndProperty
TocParent: amfDdsRecordClassPropertiesMain
TocOrder: 30

keywords: IndicatorException
keywords: ChangeInd property
keywords: DdsRecord.ChangeInd property
keywords: how to, set response indicator for dds record changes
keywords: how to, get response indicator for dds record changes
keywords: response indicators, setting for dds record changes
keywords: response indicators, getting for dds record changes
keywords: web controls, setting response indicator for dds record changes
keywords: web controls, getting response indicator for dds record changes
keywords: subfiles, setting response indicator for dds record changes
keywords: subfiles, getting response indicator for dds record changes
keywords: subfile controls, setting response indicator for dds record changes
keywords: subfile controls, getting response indicator for dds record changes
keywords: subfile records, setting response indicator for dds record changes
keywords: subfile records, getting response indicator for dds record changes
keywords: records, setting response indicator for dds record changes
keywords: records, getting response indicator for dds record changes
keywords: display files, response indicator for record changes

---

Gets or sets the response indicator to set 'on' when this record changes.

#### Syntax
<pre class="prettyprint"> **BegProp ChangeInd Access(*Public) Type(*Integer)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Specifies which indicator to set on when the DdsRecord changes.
<!--mine -->

#### Exceptions
The following exceptions may be encountered with this property setting.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="50%" /><col width="50%" />
          </colgroup>
          <tr><th>Value</th>
           <th>Condition</th>
          </tr>
          <tr>
            <td>IndicatorException</td>
            <td>An indicator outside the
            01-99 range has been provided.</td>
          </tr>
</table>

#### Remarks
To set the **ChangeInd** property at design-time, click on the far right side of the property and enter the response indicator to set *ON when this record changes. The default value is 0.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsRecord Class](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
