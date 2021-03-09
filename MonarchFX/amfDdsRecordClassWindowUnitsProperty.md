---
title: DdsRecord.WindowUnits Property

Id: amfDdsRecordClassWindowUnitsProperty
TocParent: amfDdsRecordClassPropertiesMain
TocOrder: 196

keywords: WindowUnits property
keywords: DdsRecord.WindowUnits property
keywords: how to, set window top edge x-cooridinate
keywords: how to, get window top edge x-cooridinate
keywords: web controls, setting window top edge x-cooridinate
keywords: web controls, getting window top edge x-cooridinate
keywords: subfiles, setting window top edge x-cooridinate
keywords: subfiles, getting window top edge x-cooridinate
keywords: subfile controls, setting window top edge x-cooridinate
keywords: subfile controls, getting window top edge x-cooridinate
keywords: subfile records, setting window top edge x-cooridinate
keywords: subfile records, getting window top edge x-cooridinate
keywords: records, setting window top edge x-cooridinate
keywords: records, getting window top edge x-cooridinate
keywords: display files, setting window top edge x-cooridinate
keywords: display files, getting window top edge x-cooridinate
keywords: pop-up windows, setting top edge x-cooridinate
keywords: pop-up windows, getting top edge x-cooridinate
keywords: windows, setting top edge x-cooridinate
keywords: windows, getting top edge x-cooridinate

---

Gets or sets the units that the window will be rendered in.

#### Syntax
<pre class="prettyprint">
 **BegProp WindowUnits Access(*Public) Type(*Enum)   BegGet;  BegSet** 
            </pre>

#### Property Values
Enumeration. Possible values are **Pixels** (the default) and **CharacterPositions** (for legacy character units).

#### Remarks
To set this property at design-time, click on the right of the **WindowUnits** property and select the units from the dropdown.

This property is only active if the [Window](amfddsRecordClassWindowProperty.html) property is set to **True** .

If this property is set to **CharacterPositions** the associated DdsFile properties [PixelPerCharHeight](amfddsFileClassPixelPerCharHeightProperty.html) and [PixelPerCharWidth](amfddsFileClassPixelPerCharWidthProperty.html) will be activated. These properties work together to ensure a smooth import process for legacy pop up windows.

#### Requirements
**Namespace:** [ASNA.onarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.onarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsRecordClass](amfDdsRecordClass.html) <br /> [ DdsRecord Class Members](amfDdsRecordClassMembers.html) <br /> [ ASNA.onarch.WebDspF Namespace](amfWebDspFNamespace.html) 
