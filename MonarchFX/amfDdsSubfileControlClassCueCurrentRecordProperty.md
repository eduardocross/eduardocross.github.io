---
title: DdsSubfileControl.CueCurrentRecord Property

Id: amfddsSubfileControlClassCueCurrentRecordProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 11

keywords: CueCurretnRecords property
keywords: DdsSubfileControl.CueCurrentRecords property
keywords: conditioning expressions, cue the current record
keywords: indicator expressions, setting click styles
keywords: how to, set highlights on current records
keywords: subfile records, setting current
keywords: subfiles, setting the current
keywords: SFLCLR

---

Determines if any of the two CSS styles should be applied when mouse click event fires. 

#### Syntax
<pre class="prettyprint"> **BegProp CueCurrentRecord 
   BegGet;  BegSet** </pre>

#### Property Values
Boolean. If **true** , the two CSS styles (.DdsSubfileCandidateCurrentRecord and .DdssubfileCurrentRecord) for a selected subfile will be applied on the appropriate events.

#### Remarks
The CueCurrentRecord Property determines whether or not the styles that are available to indicate that a subfile is currently selected are applied. If set to **False** then .DdsSubfileCandidateCurrentRecord will not be applied on hover, nor will .DdsSubfileCurrentRecord be applied on a click event. 

To set this property at design-time, right-click the CueCurrentRecord property and enter the conditional indicators. It defaults to **true** on migration, except for the Message Subfile Controller record.

This property was introduced with Monarch and Wings 5.2. 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
