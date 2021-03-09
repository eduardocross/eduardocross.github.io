---
title: EraseProperty Class

Id: amfErasePropertyClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 350

keywords: EraseProperty class, about EraseProperty
keywords: classes [ASNA.Monarch.WebDspF], EraseProperty class
keywords: EraseFormats Property Editor, container

---

The <span> **EraseProperty** </span> is a derived class that is a container for the **EraseFormats Property Editor** values.

For a list of all members of this type, see [ EraseProperty Members](amfErasePropertyClassMembers.html).
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
    [ASNA.Monarch.WebDspF.ConditionalProperty](amfConditionalPropertyClass.html)
 **ASNA.Monarch.WebDspF.EraseProperty** </pre>

#### Syntax
<pre class="prettyprint"> **Public class EraseProperty Inherits ConditionalProperty** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
An instance of <span> **EraseProperty** </span> represents a collection of value/condition values for a control when the [ EraseFormats](amfDdsRecordClassEraseFormatsProperty.html) property is selected causing the **EraseFormats Property Editor** dialog to display as shown below. Enter the format names and any condition for those records to be erased from the display when this record is written. The default condition is ***ALL** , which indicates to remove all records.

![](Images/zzEraseFormatsPropertyEditor.jpg) 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br clear="none" /> [ EraseProperty Class Members](amfErasePropertyClassMembers.html) <br clear="none" /> [ ConditionalProperty Class](amfConditionalPropertyClass.html) <br clear="none" /> [ DdsRecord.EraseFormat Property](amfDdsRecordClassEraseFormatsProperty.html) 
