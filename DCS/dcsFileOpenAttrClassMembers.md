---
title: FileOpenAttr Members

Id: dcsFileOpenAttrClassMembers
TocParent: dcsFileOpenAttrClass
TocOrder: 0

keywords: FileOpenAttr class, all members
keywords: members [DCS 16.0 FileOpenAttr class

---

[FileOpenAttr Overview](dcsFileOpenAttrClass.html) 
Public Constructors

<br />

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/PUBLIC%20METHOD.GIF" x-maintain-ratio="TRUE" width="15" height="11" border="0" /> [ FileOpenAttr](dcsFileOpenAttrClassConstructors.html) 
</td>
            <td colspan="1" rowspan="1">

The attributes of a file. The constructor of **FileOpenAttr** should not be called directly, since the class is abstract. Rather it must be called by a class that inherits and implements the abstract methods of the class.
</td>
          </tr>
</table>

Public Fields

<br />

<table class="dtTABLE" id="table3" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" src="Images/field.bmp" width="8" border="0" x-maintain-ratio="TRUE" /> [ OmitBlocking](dcsFileOpenAttrClassOmitBlockingField.html) 
</td>
            <td colspan="1" rowspan="1">

This constant, when assigned to the **BlockingFactor** property, causes DataGate to omit the record blocking feature in the [ FileAdapter.Open](dcsFileAdapterClassOpenMethod.html) method.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" src="Images/field.bmp" width="8" border="0" x-maintain-ratio="TRUE" /> [ OptimalBlockingFactor](dcsFileOpenAttrClassOptimalBlockingFactorField.html) 
</td>
            <td colspan="1" rowspan="1">

This constant, when assigned to the **BlockingFactor** property, requests that DataGate calculate the best-fit size of the network blocking record buffer.
</td>
          </tr>
</table>

Public Properties

<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" /> [ BlockingFactor](dcsFileOpenAttrClassBlockingFactorProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Specify network blocking feature in the open file. 
</td>
          </tr>
          <tr valign="top">
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" /> [ FileLocks](dcsFileOpenAttrClassFileLocksProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Specify record locking mechanisms in opened files.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" /> [ FormatIDs](dcsFileOpenAttrClassFormatIDsProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The set of binary format identifiers associated with the set of formats available from the [AdgDataSet.FormatIDs](dcsAdgDataSetClassFormatIDsProperty.html) property. Set to engage 'level checking' on the DataGate file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" /> [ InhibitWrites](dcsFileOpenAttrClassInhibitWriteProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Specify write-access enabling on the open file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" /> [ ShareTypes](dcsFileOpenAttrClassShareTypesProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Specify concurrent access on the open file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" /> [ WaitForEOF](dcsFileOpenAttrClassWaitForEOFProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Time, in seconds, that a process will wait for more records at end of file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" /> [ WaitForFile](dcsFileOpenAttrClassWaitForFileProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Time, in seconds, that a process will wait to access a file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img alt="public property" src="Images/property.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" height="16" border="0" /> [ WaitForRecord](dscFileOpenAttrClassWaitForRecordProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Time, in seconds, that a process will wait for access to a record.
</td>
          </tr>
</table>

See Also

<dl />
      [FileOpenAttr Class](dcsFileOpenAttrClass.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [AdgDataSet.FormatIDs Property](dcsAdgDataSetClassFormatIDsProperty.html)

