---
title: DdsSubfileControl.SubfileFold Property

Id: amfDdsSubfileControlClassSubfileFoldProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 190

keywords: SubfileFold property
keywords: DdsSubfileControl.SubfileFold property
keywords: subfiles, conditional indicator expression controlling folded display
keywords: web controls, conditional indicator expression controlling folded display
keywords: how to, set conditional indicator expression to control folded display
keywords: how to, get conditional indicator expression controlling folded display
keywords: subfile records, conditional indicator expression controlling folded display
keywords: subfile usage, conditional indicator expression controlling folded display

---

Gets or sets a set of conditional indicators that determine when the display of the subfile records is in folded form. 

#### Syntax
<pre class="prettyprint"> **BegProp SubfileFold Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Conditional indicators used to control when the display of the subfile records is in folded form. When the evaluation of the expression is true, the display of the subfile records will be in folded form.

#### Remarks
To set this property at design-time, click on the right of the **SubfileFold** property and enter the conditional indicators.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
