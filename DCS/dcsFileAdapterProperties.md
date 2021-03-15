---
title: FileAdapter Properties

Id: dcsFileAdapterProperties
TocParent: dcsFileAdapterClass
TocOrder: 3

keywords: properties DCS 16.0 FileAdapter class
keywords: FileAdapter class, properties

---

[FileAdapter Overview](dcsFileAdapterClass.html) 
Public Properties

<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [ AccessMode](dcsFileAdapterClassAccessModeProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The declared mode of access enforced by the database when the file is open.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [ Connection](dcsFileAdapterClassConnectionProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The current [AdgConnection](dcsAdgConnectionClass.html) associated with this **FileAdapter** . 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [ CurrentFormatIndex](dcsFileAdapterClassCurrentFormatIndexProperty.html) 
</td>
            <td colspan="1" rowspan="1">

An integer containing the index for the record format of the record most recently accessed by the **FileAdapter** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [ ExactSeek](dcsFileAdapterClassExactSeekProperty.html) 
</td>
            <td colspan="1" rowspan="1">

This property is **True** if the seek operation resulted in an exact match.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [ ExtendedResults](dcsFileAdapterClassExtendedResultsProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Specialized collection of status information associated with the file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [ FileLength](dcsFileAdapterClassFileLengthProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The number of deleted and non-deleted records in the open database file. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [ FileName](dcsFileAdapterClassFileNameProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The file path name of the database file excluding the member name (see **MemberName** ).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [FormatRequested](dcsFileAdapterClassFormatRequestedProperty.html)
</td>
            <td colspan="1" rowspan="1">

Reflects the most recent format specified in a **SetFormat** or **ResetFormat** method call.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [ MemberName](dcsFileAdapterClassMemberNameProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The name of the database member of the currently-opened file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [ OpenAttributes](dcsFileAdapterClassOpenAttributesProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Contains a set of file properties which influence the way a file is opened.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [RecordCount](dcsFileAdapterClassRecordCountProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The number of non-deleted records in the open database file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [ RRN](dcsFileAdapterClassRRNProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The relative record number of the member of the currently-opened file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1" style="height: 47px">

<img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [ Status](dcsFileAdapterClassStatusProperty.html) 
</td>
            <td colspan="1" rowspan="1" style="height: 47px">

Indicates the status of the file; whether it is open or closed.
</td>
          </tr>
</table>

See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)

