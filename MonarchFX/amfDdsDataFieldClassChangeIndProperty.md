---
title: DdsDataField.ChangeInd Property

Id: amfDdsDataFieldClassChangeIndProperty
TocParent: amfDdsDataFieldClassProperties
TocOrder: 40

keywords: IndicatorException
keywords: ChangeInd property
keywords: DdsDataField.ChangeInd property
keywords: Web server controls [ASNA.Monarch], response indicator for dds field changes
keywords: how to, set response indicator for dds field changes
keywords: how to, get response indicator for dds field changes
keywords: response indicators, setting for dds field changes
keywords: response indicators, getting for dds field changes
keywords: web controls, setting response indicator for dds field changes
keywords: web controls, getting response indicator for dds field changes
keywords: display files, response indicator for field changes
keywords: field controls, response indicator for field changes

---

Gets or sets the response indicator to set 'on' when this field changes. 

#### Syntax
<pre class="prettyprint"> **BegProp ChangeInd Access(*Public) Type(*Integer)
   BegGet;  BegSet** </pre>

#### Property Values
Integer containing the response indicator turned *ON when the field is changed.

#### Exceptions
The following exceptions may be encountered with this property setting.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="50%" /><col width="50%" />
          </colgroup>
          <tr><th>Value</th><th>Condition</th>
          </tr>      
          <tr><td>IndicatorException</td><td>An indicator outside the01-99 range has been provided.</td>
          </tr>
</table>

#### Remarks
The default value is 0. Use this property to set on a response indicator for an input operation when the user keys into this field. When the record is displayed again with an error message, the response indicator set on remains on until all validity checks succeed and the record is passed to your program.

To set this property at design-time, click to the right of the property and enter the indicator to set on when the field changes.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[DdsDataField Class](amfDdsDataFieldClass.html)</dd>
        <dd>[DdsDataField Class Members](amfDdsDataFieldClassMembers.html)</dd>
       <dd>[Derived Classes](amfDdsDataFieldDerivedClasses.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
</dl>

