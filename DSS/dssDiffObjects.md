---
title: Object Considerations

Id: dssDiffObjects
TocParent: dssDifferencesMain
TocOrder: 05

---

<table>
			    <tr>

			       <td><span class="OH_MultiViewContainerPanelDhtmlTable"> DataGate&#174; 16.0 for SQL Server Reference Guide
				   </span><br />
				   </td>
			    </tr>
</table>

# Object Considerations
The following table details important object considerations when converting or communicating between DataGate&#174; for IBM i, DataGate&#174; for SQL Server, and the core DataGate&#174; program.

#### Considerations
<table id="table2" cellspacing="0" class="NormalTable-Heading" style="border-width: 1px; border-style: solid; left: 0px; top: 96px; margin-right: 6.75pt; margin-left: 0.15in; border-spacing: 0px;" width="754">
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td bgcolor="#ffffdd" style="x-cell-content-align: top; width: 3.846in;" valign="top">

** Item ** 
</td>
						<td bgcolor="#ffffdd" style="x-cell-content-align: top; width: 315.8pt;" valign="top">

<b style="font-weight: bold;"> DG/400 </b> 
</td>
						<td bgcolor="#ffffdd" style="x-cell-content-align: top; width: 334.3pt;" valign="top" width="237">

** DSS ** 
</td>
						<td bgcolor="#ffffdd" style="x-cell-content-align: top; width: 334.3pt;" valign="top" width="237">

** DataGate ** 7 
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="x-cell-content-align: top; width: 3.846in;" valign="top" width="188">

Library &amp; file name length 
</td>
						<td  style="x-cell-content-align: top; width: 315.8pt;" valign="top" width="222">

10 characters
</td>
						<td  style="x-cell-content-align: top; width: 334.3pt;" valign="top" width="237">

31 characters
</td>
						<td  style="x-cell-content-align: top; width: 359.7pt;" valign="top" width="167">

31 characters
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="x-cell-content-align: top; width: 3.846in;" valign="top" width="188">

Members per file
</td>
						<td  style="x-cell-content-align: top; width: 315.8pt;" valign="top" width="222">

0 ® *NoMax
</td>
						<td  style="x-cell-content-align: top; width: 334.3pt;" valign="top" width="237">

Exactly 1
</td>
						<td  style="x-cell-content-align: top; width: 359.7pt;" valign="top" width="167">

0 ® *NoMax,
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="x-cell-content-align: top; width: 3.846in;" valign="top" width="188">

File types
</td>
						<td  style="x-cell-content-align: top; width: 315.8pt;" valign="top" width="222">

Physical

Simple logical

Join logical

Multiformat logical

Print
</td>
						<td  style="x-cell-content-align: top; width: 334.3pt;" valign="top" width="237">

Physical

SqlLogical

Simple logical

Join logical

Print
</td>
						<td  style="x-cell-content-align: top; width: 359.7pt;" valign="top" width="167">

Physical

Simple logical

Join logical

Multiformat logical

Print
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="x-cell-content-align: top; width: 3.846in;" valign="top" width="188">

Max record length
</td>
						<td  style="x-cell-content-align: top; width: 315.8pt;" valign="top" width="222">

32,000 bytes
</td>
						<td  style="x-cell-content-align: top; width: 334.3pt;" valign="top" width="237">

8,060 bytes (Not counting Text and Image fields that are not accessible yet by DSS).
</td>
						<td  style="x-cell-content-align: top; width: 359.7pt;" valign="top" width="167">

32,000 bytes
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="x-cell-content-align: top; width: 3.846in;" valign="top" width="188">

Max number of records per member
</td>
						<td  style="x-cell-content-align: top; width: 315.8pt;" valign="top" width="222">

</td>
						<td  style="x-cell-content-align: top; width: 334.3pt;" valign="top" width="237">

Limit defined by SQL Server instance
</td>
						<td  style="x-cell-content-align: top; width: 359.7pt;" valign="top" width="167">

2,147,483,646*
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="x-cell-content-align: top; width: 3.846in;" valign="top" width="188">

Library implemented as:
</td>
						<td  style="x-cell-content-align: top; width: 315.8pt;" valign="top" width="222">

Library
</td>
						<td  style="x-cell-content-align: top; width: 334.3pt;" valign="top" width="237">

Database
</td>
						<td  style="x-cell-content-align: top; width: 359.7pt;" valign="top" width="167">

Illusion
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="x-cell-content-align: top; width: 3.846in;" valign="top" width="188">

Object text (description)
</td>
						<td  style="x-cell-content-align: top; width: 315.8pt;" valign="top" width="222">

49 characters
</td>
						<td  style="x-cell-content-align: top; width: 334.3pt;" valign="top" width="237">

49 characters
</td>
						<td  style="x-cell-content-align: top; width: 359.7pt;" valign="top" width="167">

49 characters
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="x-cell-content-align: top; width: 3.846in;" valign="top" width="188">

Stored Procedures
</td>
						<td  style="x-cell-content-align: top; width: 315.8pt;" valign="top" width="222">

Any AS/400 language
</td>
						<td  style="x-cell-content-align: top; width: 334.3pt;" valign="top" width="237">

Programmed in SQL-Transact
</td>
						<td  style="x-cell-content-align: top; width: 359.7pt;" valign="top" width="167">

None
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="x-cell-content-align: top; width: 3.846in;" valign="top" width="188">

Triggers
</td>
						<td  style="x-cell-content-align: top; width: 315.8pt;" valign="top" width="222">

Any AS/400 language
</td>
						<td  style="x-cell-content-align: top; width: 334.3pt;" valign="top" width="237">

Programmed in SQL-Transact
</td>
						<td  style="x-cell-content-align: top; width: 359.7pt;" valign="top" width="167">

None
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="x-cell-content-align: top; width: 3.846in;" valign="top" width="188">

Field Reference File (FRF)
</td>
						<td  style="x-cell-content-align: top; width: 315.8pt;" valign="top" width="222">

A physical file can refer to any number of FRF, which are any physical file in any library. However, DG/400 will report only those coming from the file stated in the DDS REF keyword.
</td>
						<td  style="x-cell-content-align: top; width: 334.3pt;" valign="top" width="237">

Refers to the collection of 'User Defined Data Types', which is one per Database (i.e.: Library). This collection is surfaced via the special file '*FieldRef' which is the ** *ONLY* ** file usable as a FRF.
</td>
						<td  style="x-cell-content-align: top; width: 359.7pt;" valign="top" width="167">

A physical file can refer to only ** *ONE* ** FRF, which FRF, which can be any physical file in any library
</td>
					</tr>
</table>

Note: For Max number of records per member, DataGate&#174; for Windows and Desktop Servers Release 7.2, Version 7.255 and higher support member/file sizes limit of 16 exabytes ( 2^4 * 2^60). 
