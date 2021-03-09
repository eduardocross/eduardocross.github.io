---
title: DdsPanel.GroupingTextField Property

Id: amfDdsPanelClassGroupingTextFieldProperty
TocParent: amfDdsPanelClassProperties
TocOrder: 17

keywords: GroupingTextField property
keywords: DdsPanel.GroupingTextField property

---

Gets or sets an IFS field to draw the data for the grouping text from.

#### Syntax
<pre class="prettyprint"> **BegProp GroupingTextField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the IFS location of the IBM i CharField that the grouping text is drawn from. Requires [DdsPanel.GroupingTextFieldLength](amfDdsPanelClassGroupingTextFieldLengthProperty.html).

#### Remarks
This sets a CharField in an IBM i record to draw the data for the grouping text from. It must be used with [GroupingTextFieldLength](amfDdsPanelClassGroupingTextFieldLengthProperty.html) in order to avoid throwing an error. This property is very useful if the grouping text is likely to be changed or updated frequently, or if it will be used in multiple places throughout the site. Overrides [ASNA.Monarch.WebDspF](amfDdsPanelClassGroupingTextProperty">GroupingText</a>.

#### Requirements
**Namespace:** <a href="amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsPanel Description](amfUnderstandingPanels.html)<br /> [ DdsPanel Class](amfDdsPanelClass.html) <br /> [ DdsPanel Class Members](amfDdsPanelClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
