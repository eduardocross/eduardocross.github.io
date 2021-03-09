---
title: DdsSubfileControl.ClearRecords Property

Id: amfddsSubfileControlClassClearRecordsProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 10

keywords: ClearRecords property
keywords: DdsSubfileControl.ClearRecords property
keywords: conditioning expressions, clearing subfile control records
keywords: indicator expressions, clearing subfile control records
keywords: how to, clear subfile control records
keywords: subfile records, clearing records
keywords: subfiles, clearing records
keywords: SFLCLR

---

Gets or sets a string value containing an indicator expression (condition) that when evaluated **True** , clears the data of the detail records (SFLCLR).

#### Syntax
<pre class="prettyprint"> **BegProp ClearRecords Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string value containing an indicator expression. When the condition evaluates **True** , the data of the detail records is cleared. For example setting this property to "03 &amp; !90" means that if *IN03 is *ON and *IN90 is *OFF, the data will cleared.

#### Remarks
The **ClearRecords** property works similar to the SLFCLR keyword on the subfile control record format so that your program can clear the subfile of all records. This property differs from the [ InitializeRecords](amfddsSubfileControlClassInitializeRecordsProperty.html) property (SFLINZ keyword) in that after being cleared, the subfile contains no data. Clearing the subfile does not affect the display but it does not contain active records.

When active records already exist in the subfile and all are replaced, your program can send an output operation to the subfile control record format after selecting SFLCLR. This clears the subfile and permits your program to write new records to the subfile (by issuing output operations to the subfile record format while incrementing the relative record number). Issuing an output operation to an already active subfile record causes an error message to be returned to your program.

If **ClearRecords** is in effect on an output operation and no records exist in the subfile, **ClearRecords** is ignored.

An indicator expression is required for this property to prevent the OS/400 program from clearing the subfile on every output operation to the SubfileControl record format. See [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) and [ Monarch Web Control Indicator Expression Tester](amfMonarchWebControlIndicatorExpressionTester.html) for more information on setting the conditional indicators and testing your expressions.

To set this property at design-time, click on the right of the **ClearRecords** property and enter the indicator expression.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
