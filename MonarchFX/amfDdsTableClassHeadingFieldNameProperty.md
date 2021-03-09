---
title: DdsTable.HeadingFieldName Property

Id: amfDdsTableClassHeadingFieldNameProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: HeadingFieldName property
keywords: DdsTable.HeadingFieldName property
keywords: Web server controls [ASNA MobileRPG], DdsTable HeadingFieldName
keywords: how to, set DdsTable HeadingFieldName
keywords: how to, get DdsTable HeadingFieldName

---

Gets or sets a string containing the name of the heading field.

#### Syntax
<pre class="prettyprint"> **BegProp HeadingFieldName Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the IFS location of the IBM i CharField that the Heading data is drawn from. Requires [DdsTable.HeadingFieldLength](amfDdsTableClassHeadingFieldLengthProperty.html). Defaults to blank.

#### Remarks
This property applies only to one specific column in the DdsTable's column collection, and can be set seperately for each. 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[DdsTable Class](amfDdsTableClass.html)</dd>
        <dd>[DdsTable Class Members](amfDdsTableClassMembers.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
        <dd>[Web.config Considerations](amfconWebConfigConsiderations.html)</dd>
</dl>

