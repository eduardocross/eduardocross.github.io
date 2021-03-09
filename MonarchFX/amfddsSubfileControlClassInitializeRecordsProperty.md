---
title: DdsSubfileControl.InitializeRecords Property

Id: amfddsSubfileControlClassInitializeRecordsProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 50

keywords: InitializeRecords property
keywords: DdsSubfileControl.InitializeRecords property
keywords: initialize subfile records
keywords: subfiles, controlling record initialization
keywords: subfile records, initializing
keywords: initializing, subfile control records
keywords: how to, initialize subfile records
keywords: how to, control initialization of subfile records
keywords: conditioning expressions, controlling subfile control record initialization
keywords: indicator expressions, controlling subfile control record initialization
keywords: SFLINZ

---

Gets or sets a string value containing an indicator expression that when turned on (*True), all of the records in the Subfile are initialized (SFLINZ).

#### Syntax
<pre class="prettyprint"> **BegProp InitializeRecords Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string value containing an indicator expression that when turned on (*True), initializes all of the records in the Subfile.

#### Remarks
The **InitializeRecords** property works similar to the **SFLINZ** keyword to initialize all records in the subfile on an output operation to the subfile control record format.

When the subfile is displayed (on an output operation to the subfile control record), all records in the subfile are displayed with the same value. Any record previously written is overwritten and no longer has its earlier value.

After your program sends an output operation to the subfile control record with the **InitializeRecords** indicator in effect, all records in the subfile are considered active but not changed. They are considered changed only when the indicator specified with the [ ChangeInd](amfDdsDataFieldClassChangeIndProperty.html) property.

In general, specify **InitializeRecords** with the [ ProgramQ](amfddsSubfileControlClassProgramQProperty.html) property so that your program can build a message subfile with a single output operation.

To set this property at design-time, click on the right of the **InitializeRecords** property and enter the indicator expression.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
