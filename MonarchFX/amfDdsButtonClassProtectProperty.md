---
title: DdsButton.Protect Property

Id: amfDdsButtonClassProtectProperty
TocParent: amfDdsButtonClassProperties
TocOrder: 70

keywords: Protect property
keywords: DdsButton.Protect property
keywords: web controls, setting button control as read-only
keywords: web controls, determine if read-only button control
keywords: how to, set button control as read only
keywords: how to, determine if read-only button control
keywords: display files, setting button control as read-only
keywords: display files, determine if read-only button control
keywords: Web server controls [ASNA.Monarch], read-only button control
keywords: button controls, read-only

---

Gets or sets the *RPG indicator* expression that when evaluated, determines if the field is output-only (read-only).

#### Syntax
<pre class="syntax"> **BegProp Protect Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String containing the *RPG indicator* expression that when evaluated, determines if the field is output-only (read-only).

#### Remarks
Setting this property has no affect for Hidden fields. ( **DspAtr(PR)** )

To set this property at design-time, click on the right hand side of the property window and enter the conditional indicators for the control.

Special case insensitive string values may be used to set the condition to either TRUE or FALSE. "*True" means to make the control read-only. "*False" means the control is not read-only.

#### Inheritance Hierarchy
<pre class="example">ControlName.Protect = "(46 &amp; !47)"
ControlName.Protect = "!(13 | !15)"
ControlName.Protect = "*true"
ControlName.Protect = *false"</pre>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsButton Description](amfUnderstandingButtons.html)<br /> [DdsButton Class](amfDdsButtonClass.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
