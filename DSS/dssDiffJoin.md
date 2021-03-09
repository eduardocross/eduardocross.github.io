---
title: Join Considerations

Id: dssDiffJoin
TocParent: dssDifferencesMain
TocOrder: 45

---

<table>
			    <tr>

			       <td><span class="OH_MultiViewContainerPanelDhtmlTable"> DataGate&#174; 16.0 for SQL Server Reference Guide
				   </span><br />
				   </td>
			    </tr>
</table>

# Join Considerations
The following table details important considerations for joins when converting or communicating between DataGate&#174; for IBM i, DataGate&#174; for SQL Server, and the core DataGate&#174; program.
<table id="table8" cellspacing="0" class="MsoNormalTable" style="border-width: 1px; border-style: solid; left: 0px; top: 3685px; width: 754px; margin-left: 0.15in; border-spacing: 0px;" width="754">
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td bgcolor="#ffffdd"  style="x-cell-content-align: top; width: 1.506in;" valign="top" width="1">

**Item** 
</td>
						<td bgcolor="#ffffdd" class="auto-style32" style="x-cell-content-align: top; width: 123.6pt;" valign="top" width="123">

**DG/400** 
</td>
						<td bgcolor="#ffffdd" class="auto-style32" style="x-cell-content-align: top; width: 251px;" valign="top" width="251">

**DSS** 
</td>
						<td bgcolor="#ffffdd" class="auto-style32" style="width: 95px; x-cell-content-align: top;" valign="top" width="95">

**DataGate** 
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td class="auto-style33" style="x-cell-content-align: top; width: 1.506in;" valign="top" width="1">

Supports Use Default for Joins by: 
</td>
						<td class="auto-style34" style="x-cell-content-align: top; width: 123.6pt;" valign="top" width="123">

DDS Keyword JOINDFLT?? 

When a record is not found in the secondary file, logical fields whose base is that file will be populated with the default values specified in the physical file definition. 
</td>
						<td class="auto-style34" style="x-cell-content-align: top; width: 251px;" valign="top" width="251">

Creating a Left Outer Join instead of an Inner Join. 

From SQL Docs: 

*LEFT JOIN or LEFT OUTER JOIN* 

<i style="font-style: italic;"> The result set of a left outer join includes all the rows from the left table specified in the LEFT OUTER clause, not just the ones in which the joined columns match. When a row in the left table has no matching rows in the right table, the associated result set row contains null values for all select list columns coming from the right table.</i> 
</td>
						<td class="auto-style34" style="width: 95px; x-cell-content-align: top;" valign="top" width="95">

Yes 
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td class="auto-style33" style="x-cell-content-align: top; width: 1.506in;" valign="top" width="1">

Supports 'Join Duplicates By' 
</td>
						<td class="auto-style34" style="x-cell-content-align: top; width: 123.6pt;" valign="top" width="123">

DDS Keyword JDUP 
</td>
						<td class="auto-style34" style="x-cell-content-align: top; width: 251px;" valign="top" width="251">

Not supported. Duplicate rows in the 'secondary' tables may be returned in random order. 
</td>
						<td class="auto-style34" style="width: 95px; x-cell-content-align: top;" valign="top" width="95">

Yes 
</td>
					</tr>
</table>

