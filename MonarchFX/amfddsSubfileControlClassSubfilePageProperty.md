---
title: DdsSubfileControl.SubfilePage Property

Id: amfddsSubfileControlClassSubfilePageProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 230

keywords: SubfilePage property
keywords: DdsSubfileControl.SubfilePage property
keywords: SFLPAG
keywords: how to, set number of subfile records to display on page
keywords: how to, get number of subfile records to display on page
keywords: subfiles, setting number of subfile records to display on page
keywords: subfiles, getting number of subfile records to display on page
keywords: subfile records, number of subfile records per page
keywords: subfile records, setting number of subfile records to display on page
keywords: subfile records, getting number of subfile records to display on page
keywords: subfile controls, number of subfile records per page
keywords: subfile controls, setting number of subfile records to display on page
keywords: subfile controls, getting number of subfile records to display on page
keywords: web controls, number of subfile records per page
keywords: number of subfile records per page
keywords: display files, number of subfile records per page

---

Gets or sets the number of records in the Subfile to be displayed at the same time (SFLPAG).

#### Syntax
<pre class="prettyprint"> **BegProp SubfilePage Access(*Public) Type(*Integer)
   BegGet;  BegSet** </pre>

#### Property Values
Integer specifying the number of records in the Subfile to be displayed at the same time.

#### Remarks
The **SubfilePage** property works similar to the **SubfilePage** keyword that specifies the number of records in the Subfile to be displayed at the same time.

The default value is **0** .

The **SubfilePage** value and the number of lines required by each Subfile record determine the number of actual lines required to display the page of records. Not all records within a Subfile must be displayed at the same time, and not all lines of the display are required to display a page of Subfile records.

When you specify the same values for the **SubfilePage** and [ SubfileSize](amfddsSubfileControlClassSubfileSizeProperty.html) properties, the maximum number of records that can be contained in the Subfile equals the maximum number of Subfile records that can appear on the display at one time. You can also specify option indicators for fields in the Subfile record format.

To set this property at design-time, click on the right of the **SubfilePage** property and enter the number of records to display at the same time.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ SubfileSize Property](amfddsSubfileControlClassSubfileSizeProperty.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
