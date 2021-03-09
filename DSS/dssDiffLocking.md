---
title: Locking Considerations

Id: dssDiffLocking
TocParent: dssDifferencesMain
TocOrder: 25

---

<table>
			    <tr>

			       <td><span class="OH_MultiViewContainerPanelDhtmlTable"> DataGate&#174; 16.0 for SQL Server Reference Guide
				   </span><br />
				   </td>
			    </tr>
</table>

# Locking Considerations
The following table details important data access considerations when converting or communicating between DataGate&#174; for IBM i, DataGate&#174; for SQL Server, and the core DataGate&#174; program.

#####  **Record Locking** 
### <span style="font-size: 10pt;">DG/400</span> 
DB2/400 determines the type and duration of records locks depending on how the file was opened. 

For read-only files, when a record is read, there is no lock requested on it, and if some other application has the record lock, the reading application does not block on the lock, that is, the record is read in spite of being locked by somebody else. 

For files open for update, every time a record is read it is write-locked so that other updating applications cannot read it. The write lock is held until the record is updated or explicitly unlocked by the application or when another record is read or positioned to. 

### <span style="font-size: 10pt;">DSS</span> 
DSS (using server cursors) determines the locking characteristics based on how the file is opened. 

For read-only files DSS behaves like DG/400, that is, locks are neither placed nor considered on records being read. 

The behavior of DSS when the file is opened for update is similar to DG/400 but with <span style="color: rgb(255, 0, 0);"> two significant differences </span>: updating a record does not release the lock on the record and explicitly unlocking a record causes the 'current record position' to be lost. These differences bear the following considerations. 
<table id="table5" cellspacing="0" style="left: 0px; top: 1772px; width: 100%; border-spacing: 0px;" width="754">
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td bgcolor="#ffffdd" style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

**Item** 
</td>
						<td bgcolor="#ffffdd" style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

**DG/400** 
</td>
						<td bgcolor="#ffffdd" style="x-cell-content-align: top; width: 448px;" valign="top" width="448">

**DSS** 
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

Unlock Record 
</td>
						<td style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

Cursor position is unchanged. 
</td>
						<td style="x-cell-content-align: top; width: 387px;" valign="top" width="387">

The file has no 'current' position after the *Unlock.* 
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

Update Record 
</td>
						<td style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

The record just updated is released. 
</td>
						<td style="x-cell-content-align: top; width: 387px;" valign="top" width="387">

The record just updated is kept locked. 
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

**NoLock* option on *Read* operations 
</td>
						<td style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

Supported but deprecated. 
</td>
						<td style="x-cell-content-align: top; width: 387px;" valign="top" width="387">

Unsupported. 

The better way to achieve this is to open the file twice, once for input only and the other for update. Where the read appears with the *NoLock option, the file should be substituted with the one open for input only. By doing this, the application can take advantage of network blocking - yielding better performance. 
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

Range operations 
</td>
						<td style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

When the end of the range is reached, the file has no 'current' position. 
</td>
						<td style="x-cell-content-align: top; width: 387px;" valign="top" width="387">

When the end of the range is reached, the file has no 'current' position. 
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

Hit EOF on a ReadE (P) 
</td>
						<td style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

Lose Record position. 
</td>
						<td style="x-cell-content-align: top; width: 387px;" valign="top" width="387">

Lose Record position. 
</td>
					</tr>
					<tr style="x-cell-content-align: center; height: 32px" valign="middle">
						<td style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

Other Operations like SetLL 
</td>
						<td style="width: 177px; x-cell-content-align: top;" valign="top" width="177">

Unlock Record. 
</td>
						<td valign="top" width="387">

Unlock Record. 
</td>
					</tr>
</table>

Loops involving SetLL/SetGT and Read/ReadE/ReadPE should be re-coded to use the Range operations. 

The most demanding change is the one requiring segments of code involving CHAIN-UPDATE. Combinations have to be studied and possibly modified. 

- If the CHAIN-UPDATE happens in a tight loop, then at the 
					end of the loop an UNLOCK should be issued to release the 
					last record updated. Note however that the record position 
					will be lost after the UNLOCK.
- If the CHAIN-UPDATE is sprinkled throughout the code, 
					then each case has to be closely studied.

#####  Object Locking 
For DSS, object locking is implemented only for Data Area objects. 
