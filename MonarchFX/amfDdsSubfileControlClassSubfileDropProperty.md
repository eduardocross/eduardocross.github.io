---
title: DdsSubfileControl.SubfileDrop Property

Id: amfDdsSubfileControlClassSubfileDropProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 150

keywords: SubfileDrop property
keywords: DdsSubfileControl.SubfileDrop property
keywords: subfiles, conditional indicator expression controlling truncated display
keywords: web controls, conditional indicator expression controlling truncated display
keywords: how to, set conditional indicator expression to control truncated display
keywords: how to, get conditional indicator expression controlling truncated display
keywords: subfile records, conditional indicator expression controlling truncated display
keywords: subfile usage, conditional indicator expression controlling truncated display

---

Gets or sets a set of conditional indicators that determine when the display of the subfile records is in truncated form. 

#### Syntax
<pre class="prettyprint"> **BegProp SubfileDrop Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Conditional indicators used to control when the display of the subfile records is in truncated form. When the evaluation of the expression is true, the display of the subfile records will be in truncated form.

#### Remarks
To set this property at design-time, click on the right of the **SubfileDrop** property and enter the conditional indicators. <br /><br />Notice that the property [ VirtualRowCol](amfDdsDataFieldClassVirtualRowColProperty.html), on every field in the subfile controls the visibility of the field when the subfile is in **Drop** mode. Only rows in the VirtualRowCol pair that are equal to "1" will be shown in the **Drop** mode. That is, a property value of VirtualRowCol="1,10" for a field in the subfile, will make it visible, while in **Drop** mode, where a property value of VirtualRowCol="2,40" will not.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
