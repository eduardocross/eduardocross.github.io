---
title: Data Access Considerations

Id: dssDiffDataAccess
TocParent: dssDifferencesMain
TocOrder: 20

---

<table>
			    <tr>

			       <td><span class="OH_MultiViewContainerPanelDhtmlTable"> DataGate&#174; 16.0 for SQL Server Reference Guide
				   </span><br />
				   </td>
			    </tr>
</table>

# Data Access Considerations
The following table details important data access considerations when converting or communicating between DataGate&#174; for IBM i, DataGate&#174; for SQL Server, and the core DataGate&#174; program.

#### Considerations
<div>
<table id="table4" cellspacing="0" class="normal" style="border-width: 1px; border-style: solid; left: 0px; top: 1085px; width: 754px; margin-left: 0.15in; border-spacing: 0px;" width="754">
			  <tr valign="middle">
				  <td bgcolor="#ffffdd" style="x-cell-content-align: top; width: 99px;" valign="top" width="99">

<b style="font-weight: bold;"><span>Item</span></b>
</td>
				  <td bgcolor="#ffffdd" style="x-cell-content-align: top; width: 149px;" valign="top" width="149">

**DG/400** 
</td>
				  <td bgcolor="#ffffdd" style="x-cell-content-align: top; width: 274px;" valign="top" width="274">

**DSS** 
</td>
				  <td bgcolor="#ffffdd" style="x-cell-content-align: top; width: 149px;" valign="top" width="149">

**DataGate** 
</td>
			  </tr>
			  <tr style="x-cell-content-align: center; height: 32px" valign="middle">
				  <td valign="top" width="99">

Arrival Access
</td>
				  <td style="x-cell-content-align: top; width: 149px;" valign="top" width="149">

Relative Record Number is used for Sequential and Random access.
</td>
				  <td style="x-cell-content-align: top; width: 274px;" valign="top" width="274">

Only Consecutive access is supported, but there is no guaranteed order of retrieval unless the file is indexed. The only random operation allowed is SetLL and this is only when used with *Start and *End. No other kind of seeking (SetGT,CHAIN) is allowed. 
</td>
				  <td style="width: 149px;" valign="top" width="149">

Relative Record Number is used for Sequential and Random access.
</td>
			  </tr>
			  <tr style="x-cell-content-align: center; height: 32px" valign="middle">
				  <td style="x-cell-content-align: top; width: 99px;" valign="top" width="99">

Format Name (see Note below)
</td>
				  <td style="x-cell-content-align: top; width: 149px;" valign="top" width="149">

Given by file creator.
</td>
				  <td style="x-cell-content-align: top; width: 274px;" valign="top" width="274">

<b style="font-weight: bold;">Always 'R'followed by File Name.</b>

<span style="color: rgb(255, 0, 0);"> Note to AVR Users </span>: The Format can be renamed in the DclDiskFile, using the RNMFMT keyword by providing a new name, it is not necessary to provide the existing Name in the RNMFMT. This allows the creation of single-source apps that can compile against DG/400 and DSS.
</td>
				  <td style="x-cell-content-align: top; width: 149px;" valign="top" width="149">

Given by File creator.
</td>
			  </tr>
			  <tr style="x-cell-content-align: center; height: 32px" valign="middle">
				  <td valign="top" width="99">

Open Query File
</td>
				  <td style="x-cell-content-align: top; width: 149px;" valign="top" width="149">

Implemented with OpenQry.
</td>
				  <td style="x-cell-content-align: top; width: 274px;" valign="top" width="274">

Select expression is used as the WHERE clause of a SELECT. The key field list is used as the ORDER BY clause. 

The SELECT expression is passed directly to the SQL analyzer with no interpretation. The expression must follow valid SQL Server syntax. Pay special attention to uses of logical operators. Use 'AND' and 'OR' not '&amp;' and '|'. 
</td>
				  <td style="x-cell-content-align: top; width: 149px;" valign="top" width="149">

A temporary logical file is created using the SELECT expression as a SELECT/OMIT expression and the key field list to define the new key.
</td>
			  </tr>
</table>

***NOTE:** Multi-format logical files are not supported on SQL Server. The migrated code is normalized for SQL Server especially when I/O commands target single-format record format names instead of the file name but this does **not** change the application's behavior when accessing files on the System i.<br /><br />If the Rename keyword is present in the legacy file description, the migrated RNMFMT keyword will contain the legacy New Format Name. If the Rename keyword is **not** present in the legacy file description, the migrated RNMFMT keyword will contain the files Externally Described Record Format name.* 
