---
title: DdsTable.SelectedKey Property

Id: amfDdsTableClassSelectedKeyProperty
TocParent: amfDdsTableClassPropertiesMain

keywords: SelectedKey property
keywords: DdsTable.SelectedKey property
keywords: Web server controls [ASNA MobileRPG], setting DdsTable SelectedKey
keywords: how to, set DdsTable SelectedKey
keywords: how to, get DdsTable SelectedKey

---

Defines the key press to be triggered when the icon is clicked using the [AidKeyIBMi](amfAidKeyIBMEnumeration.html) enumeration.

#### Syntax
<pre class="prettyprint"> **BegProp SelectedKey Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enum. The [AidKeyIBMi](amfAidKeyIBMEnumeration.html) enumeration is used to define the key to be pressed when the icon is clicked..

#### Remarks
This property applies only to each <code>IconColumn</code>. The [AidKeyIBMi](amfAidKeyIBMiEnumeration.html) will be pressed immediately when the icon is clicked or tapped.

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

