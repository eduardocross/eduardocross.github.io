---
title: DdsBar.Segments Property

Id: amfDdsBarClassSegmentsProperty
TocParent: amfDdsBarClassProperties
TocOrder: 10

keywords: Segments property
keywords: dds button, Segments
keywords: field controls, dds button, Segments

---

Gets or sets the IDs of the segments that will hold the content to be shown in the DdsBar.

#### Syntax
<pre class="syntax"> **BegProp Segments Access(*Public) Type(String)
   BegGet:  BegSet** </pre>

#### Property Values
**String.** Contains the ID values for the [DdsBarSegments](amfDdsBarSegmentClass.html) present in the DdsBar.

#### Remarks
This property is required if the bar is to have any contents to present. The Id of each segment must be provided in the order they are intended to be presented.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBar Class](amfDdsBarClass.html) <br /> [DdsBar Class Members](amfDdsBarClassMembers.html) <br />[DdsRecord Class](amfDdsRecordClass.html)<br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
