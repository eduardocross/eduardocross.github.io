---
title: DdsList.SelectItemKey Property

Id: amfDdsListClassSelectItemKeyProperty
TocParent: amfDdsListClassProperties
TocOrder: 92

keywords: SelectItemKey property
keywords: DdsList.SelectItemKey property

---

Gets or sets the key pressed when a list item is selected (clicked or tapped) by the user. As of Mobile RPG 8.0 this defaults to <code>UNKNOWN</code>.

#### Syntax
<pre class="prettyprint"> **BegProp SelectItemKey Access(*Public) Type( **ASNA.Monarch.WebDspF.AidProperty** )
   BegGet;  BegSet** </pre>

#### Property Values
**ASNA.Monarch.WebDspF.AidProperty.** One of the enumeration values from [ AidKeyIBM](amfAidKeyIBMEnumeration.html) containing the function key value assigned to the list Items.

#### Remarks
To set this property at design-time, select it from the Property Tasks list and select the key from the drop-down list, or click on the right hand side of the property window and select the key from the drop-down list. This key must also be defined in either the [FuncKeys](amfDdsRecordClassFuncKeysProperty.html) or, more rarely, [AttnKeys](amfDdsRecordClassAttnKeysProperty.html) property of the [DdsRecord](amfDdsRecordClass.html), [DdsFile](amfDdsFileClass.html), [DdsSubfile](amfDdsSubfileClass.html) or [DdsSubfileControl](amfDdsSubfileClass.html) control that contains it.

This property is only active when the [ListType](amfDdsListClassListTypeProperty.html) of the DdsList is Navigation.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8, Pro, Windows 10 Pro

#### See Also
[DdsList Description](amfUnderstandingLists.html)<br /> [ DdsList Class](amfDdsListClass.html) <br /> [ DdsList Class Members](amfDdsListClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
