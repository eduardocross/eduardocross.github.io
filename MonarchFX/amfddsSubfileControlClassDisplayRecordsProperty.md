---
title: DdsSubfileControl.DisplayRecords Property

Id: amfddsSubfileControlClassDisplayRecordsProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 30

keywords: DisplayRecords property
keywords: DdsSubfileControl.DisplayRecords property
keywords: display subfile records
keywords: how to, control display of subfile records
keywords: subfiles, controlling records display
keywords: subfile records, displaying
keywords: displaying, subfile control records
keywords: how to, control display of subfile records
keywords: conditioning expressions, controlling subfile control record display
keywords: indicator expressions, controlling subfile control record display
keywords: SFLDSP

---

Gets or sets a string value containing an indicator expression (condition) that when evaluated indicates **True** , causes the records in the subfile to display (SFLDSP).

#### Syntax
<pre class="prettyprint"> **BegProp DisplayRecords Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. A string value containing an indicator expression or the special value ***True** or ***False.** When the condition evaluates **True** , the records in the subfile are displayed. For example setting this property to "03 &amp; !90" means that if *IN03 is *ON and *IN90 is *OFF (condition true), the records in the subfile will display.

#### Remarks
The **DisplayRecords** property works similar to the **SFLDSP** keyword so that the program displays the subfile when your program sends an output operation to the SubfileControl record format.

Use the [ SubfilePage](amfddsSubfileControlClassDisplayRecordsProperty.html) property to specify the number of records in the Subfile to be displayed at the same time.

If your program sends an output operation to the record format when the DisplayRecords indicator is in effect and the subfile is not activated (by adding records to it or by using SFLINZ), an error message is sent to your program.

To set this property at design-time, click on the right of the **DisplayRecords** property and enter the indicator expression.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
