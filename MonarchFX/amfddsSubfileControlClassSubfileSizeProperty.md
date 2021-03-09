---
title: DdsSubfileControl.SubfileSize Property

Id: amfddsSubfileControlClassSubfileSizeProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 240

keywords: SubfileSize property
keywords: DdsSubfileControl.SubfileSize property
keywords: SFLSIZ
keywords: how to, set number of subfile records
keywords: how to, get number of subfile records
keywords: subfiles, maximum number of subfile records
keywords: subfiles, setting number of subfile records
keywords: subfiles, getting number of subfile records
keywords: subfile records, maximum number of subfile records
keywords: subfile records, number of subfile records
keywords: subfile records, setting number of subfile records
keywords: subfile records, getting number of subfile records
keywords: subfile controls, maximum number of subfile records
keywords: subfile controls, number of subfile records
keywords: subfile controls, setting number of subfile records
keywords: subfile controls, getting number of subfile records
keywords: web controls, maximum number of subfile records
keywords: web controls, number of subfile records
keywords: number of subfile records
keywords: display files, number of subfile records
keywords: display files, maximum number of subfile records

---

Gets or sets the number of records in the Subfile (SFLSIZ).

#### Syntax
<pre class="prettyprint"> **BegProp SubfileSize Access(*Public) Type(*Integer)
   BegGet;  BegSet** </pre>

#### Property Values
Integer. Specifies the number of records in the Subfile.

#### Remarks
The **SubfileSize** property works similarly to the **SubfileSize** keyword to specify the number of records in the Subfile.

The default value is **0** . The maximum number of records allowed is 9999.

**SubfileSize equals SubfilePage:** 

If you specify the same values for the **SubfileSize** and [ SubfilePage](amfddsSubfileControlClassSubfilePageProperty.html) properties, you can specify option indicators for fields in the Subfile record format. (This is called field selection.)

When the Subfile is built, the records can vary in length depending upon which fields are selected, and each output operation places records into successive positions within the Subfile. Each record in the Subfile can require a different number of display lines. The number of records that actually fit into the Subfile depends upon the fields selected for each record written to the Subfile.

The **SubfilePage** property value is increased to equal the maximum number of records that fit on the display if the number of Subfile records to be displayed do not occupy a full display.

**SubfileSize does not equal SubfilePage:** 

When you specify different values for the **SubfilePage** and **SubfileSize** properties, the **SubfileSize** value specifies the number of records that can be placed into the Subfile. If your program places a record with a relative record number larger than the **SubfileSize** value into the Subfile, the Subfile is automatically extended to contain it (up to a maximum of 9999 records). The value you specify should be large enough to accommodate the maximum number of records you would normally have in the Subfile.

To set this property at design-time, click on the right of the **SubfileSize** property and enter the number of records in the subfile.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ SubfilePage Property](amfddsSubfileControlClassSubfilePageProperty.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
