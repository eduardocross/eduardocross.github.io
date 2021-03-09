---
title: Index Considerations

Id: dssDiffIndex
TocParent: dssDifferencesMain
TocOrder: 15

---

<table>
			    <tr>

			       <td><span class="OH_MultiViewContainerPanelDhtmlTable"> DataGate&#174; 16.0 for SQL Server Reference Guide
				   </span><br />
				   </td>
			    </tr>
</table>

# Index Considerations
The following table details important index (keys) considerations when converting or communicating between DataGate&#174; for IBM i, DataGate&#174; for SQL Server, and the core DataGate&#174; program.

#### Considerations
<table id="table3" cellspacing="0" class="normal" style="border-width: 1px; border-style: solid; margin-left: 0.15in; border-spacing: 0px;" width="754">
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td bgcolor="#ffffdd" style="width: 239px; x-cell-content-align: top;" valign="top">

**Item** 
</td>
						<td bgcolor="#ffffdd" style="width: 95px; x-cell-content-align: top;" valign="top" width="95">

**DG/400** 
</td>
						<td bgcolor="#ffffdd" style="width: 239px; x-cell-content-align: top;" valign="top" width="212">

**DSS** 
</td>
						<td bgcolor="#ffffdd" style="width: 95px; x-cell-content-align: top;" valign="top" width="161">

<b style="font-weight: bold;"><span>DataGate</span></b> 
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td valign="top" width="239">

Indexed logical files per physical file
</td>
						<td valign="top" width="95">

</td>
						<td valign="top" width="212">

249
</td>
						<td valign="top" width="161">

*NoMax
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td valign="top" width="239">

Imposing 'uniqueness' via select/omit rules in logical files
</td>
						<td style="width: 95px; x-cell-content-align: top;" valign="top" width="95">

Supported
</td>
						<td style="width: 239px; x-cell-content-align: top;" valign="top" width="212">

Not directly supported. See <span style="color: rgb(0, 0, 128); font-weight: bold;"> **work-around** </span><span style="font-weight: bold;"> </span>note below.
</td>
						<td style="width: 95px; x-cell-content-align: top;" valign="top" width="161">

Supported
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td valign="top" width="239">

Logical field used as a key field must be based on a physical field with the same name
</td>
						<td style="width: 95px; x-cell-content-align: top;" valign="top" width="95">

No
</td>
						<td style="width: 239px; x-cell-content-align: top;" valign="top" width="212">

Yes. Notice that this eliminates the possibility of using Renamed, Concatenated and Sub-stringed fields as keys. 
</td>
						<td style="width: 95px; x-cell-content-align: top;" valign="top" width="161">

No
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td valign="top" width="239">

Maximum number of key fields per key
</td>
						<td style="width: 95px; x-cell-content-align: top;" valign="top" width="95">

</td>
						<td style="width: 239px; x-cell-content-align: top;" valign="top" width="212">

16
</td>
						<td style="width: 95px; x-cell-content-align: top;" valign="top" width="161">

250
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td valign="top" width="239">

Maximum length of key in bytes
</td>
						<td style="width: 95px; x-cell-content-align: top;" valign="top" width="95">

2,000
</td>
						<td style="width: 239px; x-cell-content-align: top;" valign="top" width="212">

900
</td>
						<td style="width: 95px; x-cell-content-align: top;" valign="top" width="161">

250
</td>
					</tr>
</table>

**Work-around:** 

As a work-around to support "Imposing 'uniqueness' via select/omit rules in logical files": 

1. Change the logical file definition to 
					allow duplicate keys.
2. Create the logical file.
3. Alter the SQL view with the " **SCHEMABINDING** " 
					attribute.
4. Add a Unique, Clustered Index to the 
					SQL view (logical file).
5. Make sure the " **ARITHABORT** " SET 
					option is on/true for the database.

