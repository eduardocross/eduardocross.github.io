---
title: FileAdapter Members

Id: dcsFileAdapterMembers
TocParent: dcsFileAdapterClass
TocOrder: 0

keywords: members [DCS 16.0 FileAdapter class

---

[FileAdapter Overview](dcsFileAdapterClass.html) 
Public Constructors

<br />

<table class="dtTABLE" id="table4" style="border-spacing: 0px" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ FileAdapter](dcsFileAdapterClassFileAdapterMethodMain.html) <span style="MARGIN-TOP: 0pt; MARGIN-BOTTOM: 0pt" /> 
</td>
            <td colspan="1" rowspan="1">

Constructs an instance of the **FileAdapter** object.
</td>
          </tr>
</table>

Public Properties

<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ AccessMode](dcsFileAdapterClassAccessModeProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The declared mode of access enforced by the database when the file is open.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ Connection](dcsFileAdapterClassConnectionProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The current [AdgConnection](dcsAdgConnectionClass.html) associated with this **FileAdapter** . 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ CurrentFormatIndex](dcsFileAdapterClassCurrentFormatIndexProperty.html) 
</td>
            <td colspan="1" rowspan="1">

An integer containing the index for the record format of the record most recently accessed by the **FileAdapter** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ ExactSeek](dcsFileAdapterClassExactSeekProperty.html) 
</td>
            <td colspan="1" rowspan="1">

This property is **True** if the seek operation resulted in an exact match.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ ExtendedResults](dcsFileAdapterClassExtendedResultsProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Specialized collection of status information associated with the file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ FileLength](dcsFileAdapterClassFileLengthProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The number of deleted and non-deleted records in the open database file. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ FileName](dcsFileAdapterClassFileNameProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The file path name of the database file excluding the member name (see **MemberName** ).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [FormatRequested](dcsFileAdapterClassFormatRequestedProperty.html)
</td>
            <td colspan="1" rowspan="1">

Reflects the most recent format specified in a **SetFormat** or **ResetFormat** method call.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ MemberName](dcsFileAdapterClassMemberNameProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The name of the database member of the currently-opened file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ OpenAttributes](dcsFileAdapterClassOpenAttributesProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Contains a set of file properties which influence the way a file is opened.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ RecordCount](dcsFileAdapterClassRecordCountProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The number of non-deleted records in the open database file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ RRN](dcsFileAdapterClassRRNProperty.html) 
</td>
            <td colspan="1" rowspan="1">

The relative record number of the member of the currently-opened file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [ Status](dcsFileAdapterClassStatusProperty.html) 
</td>
            <td colspan="1" rowspan="1">

Indicates the status of the file; whether it is open or closed.
</td>
          </tr>
</table>

<br />

Public Methods

<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ AddRecord](dcsFileAdapterClassAddRecordMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Adds a record to a file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ ChangeCurrent](dcsFileAdapterClassChangeCurrentMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Updates the current database file record with the contents of the specified [ AdgDataSet.ActiveRow](dcsAdgDataSetClassActiveRowProperty.html) property.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ ChangeRRN](dcsFileAdapterClassChangeRRNMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Updates the database file record specified by relative record number with the contents of the specified **AdgDataSet’s ActiveRow** property.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [Close](dcsFileAdapterClassCloseMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Closes the currently open file (synonymous with **Dispose** ).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [DeleteAllRecords](dcsFileAdapterClassDeleteAllRecordsMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Deletes all records in the file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [DeleteCurrent](dcsFileAdapterClassDeleteCurrentMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Deletes the current record associated with an open file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [DeleteKey](dcsFileAdapterClassDeleteKeyMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Deletes a database file record containing the specified key, if any.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [DeleteRange](dcsFileAdapterClassDeleteRangeMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Deletes a range of records in an open file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ DeleteRRN](dcsFileAdapterClassDeleteRRNMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Deletes the database file record at the specified position.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ Dispose](dcsFileAdapterClassDisposeMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Closes the currently open file (synonymous with **Close** ).
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ ForceEOD](dcsFileAdapterClassForceEODMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Synchronizes the state of the **FileAdapter** object with the open database file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ GetPrintProperties](dcsFileAdapterClassGetPrintPropertiesMethod.html) 
</td>
            <td colspan="1" rowspan="1">

The [IPrintProperties](dcsIPrintPropertiesClass.html) associated with the open file.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ Open](dcsFileAdapterClassOpenMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Open a database file for access with the specified **AdgDataSet** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ OpenNewAdgDataSet](dcsFileAdapterClassOpenNewAdgDataSetMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Opens a database file for access and returns a new **AdgDataSet** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ OpenSimpleQuery](dcsFileAdapterClassOpenSimpleQueryMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Open a database file for access using the specified query and the specified **AdgDataSet** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ ReadRandomKey](dcsFileAdapterClassReadRandomKeyMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Read a database file record using the specified key.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ ReadRandomRRN](dcsFileAdapterClassReadRandomRRNMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Read the database file record specified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ ReadRange](dcsFileAdapterClassReadRangeMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Read a database file record containing a key within a given range of values.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ ReadSequential](dcsFileAdapterClassReadSequentialMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Read a single record from the file in sequential order. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ ReadSequentialEqual](dcsFileAdapterClassReadSequentialEqualMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Read a database file record adjacent to the current position with a key equal to the key of the current record, or optionally, a key equal to the specified key.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ ReleaseCurrent](dcsFileAdapterClassReleaseCurrentMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Release the currently locked record.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ ReleaseRRN](dcsFileAdapterClassReleaseRRNMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Release the specified record.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ ResetFormat](dcsFileAdapterClassResetFormatMethod.html) 
</td>
            <td colspan="1" rowspan="1">

For multi-format file access, reset the file to access a record of any format in subsequent operations (see **SetFormat** ). 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ ResetPrintAttr](dcsFileAdapterClassResetPrintAttrMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Complete the current printer job, change device-related parameters associated with the open print file, then start a new printer job.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ ReuseRRN](dcsFileAdapterClassReUseRRNMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Change the status of a deleted record to undeleted and update its contents.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ SeekKey](dcsFileAdapterClassSeekKeyMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Moves the record pointer associated with the currently open file without reading records to within a range of key values.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ SeekRange](dcsFileAdapterClassSeekRangeMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Moves the record pointer associated with the currently open file without reading records to within a range of key values.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ SeekRRN](dcsFileAdapterClassSeekRRNMethod.html) 
</td>
            <td colspan="1" rowspan="1">

Moves the record pointer associated with the currently open file without reading records by RRN.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

<img height="11" alt="public property" src="../Images/PUBLIC%20METHOD.GIF" width="15" border="0" x-maintain-ratio="TRUE" /> [ SetFormat](dcsFileAdapterClassSetFormatMethod.html) 
</td>
            <td colspan="1" rowspan="1">

For multiformat read access, calling this method causes the read methods to fetch only those records with the given format.
</td>
          </tr>
</table>

See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [ActiveRow Property](dcsAdgDataSetClassActiveRowProperty.html)
      <br />
      [IPrintProperties Class](dcsIPrintPropertiesClass.html)

