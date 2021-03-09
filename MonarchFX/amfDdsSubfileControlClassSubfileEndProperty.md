---
title: DdsSubfileControl.SubfileEnd Property

Id: amfDdsSubfileControlClassSubfileEndProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 160

keywords: SubfileEnd property
keywords: DdsSubfileControl.SubfileEnd property
keywords: SFLEND

---

Gets or sets an indicator expression that when evaluated indicates whether [ SubfileEndTextOn](amfDdsSubfileControlClassSubFileEndTextOnProperty.html) (True) or [ SubfileEndTextOff](amfDdsSubfileControlClassSubFileEndTextOffProperty.html) (False) will be used (SFLEND).

#### Syntax
<pre class="prettyprint">
 **BegProp SubfileEnd Access(*Public) Type(*String)
   BegGet;  BegSet** 
            </pre>

#### Property Values
String. An indicator expression that when the condition evaluates to true, **SubfileEndTextOn** will be used; otherwise **SubfileEndTextOff** will be used.

#### Remarks
This property controls the text to display in the lower right display location occupied by the subfile.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
