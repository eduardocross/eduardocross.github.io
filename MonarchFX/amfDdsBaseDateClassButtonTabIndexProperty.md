---
title: DdsBaseDate.ButtonTabIndex Property

Id: amfDdsBaseDateClassButtonTabIndexProperty
TocParent: amfDdsBaseDateClassProperties
TocOrder: 70

keywords: ButtonTabIndex property
keywords: DdsBaseDate.ButtonTabIndex property
keywords: Web server controls [ASNA.Monarch], date field button tab order
keywords: how to, set date field button tab order
keywords: how to, get date field button tab order
keywords: display files, setting date field button tab order
keywords: display files, getting date field button tab order
keywords: web controls, setting date field button tab order
keywords: web controls, getting date field button tab order
keywords: field controls, date field button, tab order
keywords: CSS class name

---

Gets or sets the index representing the tab order of the date control button.

#### Syntax
<pre class="syntax"> **BegProp ButtonTabIndex Access(*Public) Type(*Short)
     BegGet;   BegSet** </pre>

#### Property Values
Short. An index representing the tab order of the date control button.

#### Remarks
This property will define the tab stop order of the button/image for the control. It can be set to zero (default) to not be included in the **initial** order of tabbing. The elements in the page that can receive focus and do not have a tabindex property can still be tabbed to after those with a tabindex have been 'consumed'.

To set the **ButtonTabIndex** at design time, click to the right of the property and enter the index value.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBaseDate Class](amfDdsBaseDateClass.html) <br /> [ DdsBaseDate Class Members](amfDdsBaseDateClassMembers.html) <br /> [ Derived Classes](amfDdsBaseDateDerivedClasses.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
