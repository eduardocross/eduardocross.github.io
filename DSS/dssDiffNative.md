---
title: Native SQL Server Field Interpretation

Id: dssDiffNative
TocParent: dssDifferencesMain
TocOrder: 40

---

<table>
			    <tr>

			       <td><span class="OH_MultiViewContainerPanelDhtmlTable"> DataGate&#174; 16.0 for SQL Server Reference Guide
				   </span><br />
				   </td>
			    </tr>
</table>

# Native SQL Server Considerations
The following table details important considerations for Native SQL Server field interpretation when converting or communicating between DataGate&#174; for IBM i, DataGate&#174; for SQL Server, and the core DataGate&#174; program.
<table id="table7" cellspacing="0" style="width: 100%;" width="754">
					<tr style="x-cell-content-align: top; height: 32px;" valign="top">
						<td bgcolor="#ffffdd" colspan="2" style="width: 226px;" width="226">

**Numerics** 
</td>
						<td bgcolor="#ffffdd" colspan="2" style="width: 226px;" width="226">

**Date/Time** 
</td>
						<td bgcolor="#ffffdd" colspan="2" style="width: 226px;" width="226">

**Char/Other** 
</td>
					</tr>
					<tr style="x-cell-content-align: top;" valign="top">
						<td style="width: 113px;" width="113">

Float 
</td>
						<td style="width: 113px;" width="113">

*Float(4) 
</td>
						<td width="113">

DateTime 
</td>
						<td style="width: 113px;" width="113">

*Timestamp 
</td>
						<td width="113">

Bit 
</td>
						<td style="width: 113px;" width="113">

*Boolean 
</td>
					</tr>
					<tr style="x-cell-content-align: top;" valign="top">
						<td style="width: 113px;" width="113">

Real 
</td>
						<td style="width: 113px;" width="113">

*Float (8) 
</td>
						<td width="113">

SmallDateTime 
</td>
						<td style="width: 113px;" width="113">

*Timestamp 
</td>
						<td width="113">

Char 
</td>
						<td style="width: 113px;" width="113">

*Char 
</td>
					</tr>
					<tr style="x-cell-content-align: top;" valign="top">
						<td style="width: 113px;" width="113">

Int 
</td>
						<td style="width: 113px;" width="113">

*Integer (4) 
</td>
						<td width="113">

</td>
						<td style="width: 113px;" width="113">

</td>
						<td width="113">

VarChar 
</td>
						<td style="width: 113px;" width="113">

*Char (VarLen) 
</td>
					</tr>
					<tr style="x-cell-content-align: top;" valign="top">
						<td style="width: 113px;" width="113">

SmallInt 
</td>
						<td style="width: 113px;" width="113">

*Integer (2) 
</td>
						<td width="113">

</td>
						<td style="width: 113px;" width="113">

</td>
						<td width="113">

NChar 
</td>
						<td style="width: 113px;" width="113">

*Unicode 
</td>
					</tr>
					<tr style="x-cell-content-align: top;" valign="top">
						<td style="width: 113px;" width="113">

TinyInt 
</td>
						<td style="width: 113px;" width="113">

*Integer (2) 
</td>
						<td width="113">

</td>
						<td style="width: 113px;" width="113">

</td>
						<td width="113">

NVarChar 
</td>
						<td style="width: 113px;" width="113">

*Unicode (VarLen) 
</td>
					</tr>
					<tr style="x-cell-content-align: top;" valign="top">
						<td style="width: 113px;" width="113">

Decimal 
</td>
						<td style="width: 113px;" width="113">

*Packed 
</td>
						<td  width="113">

</td>
						<td style="width: 113px;" width="113">

</td>
						<td  width="113">

Binary 
</td>
						<td style="width: 113px;" width="113">

*Hex 
</td>
					</tr>
					<tr style="x-cell-content-align: top;" valign="top">
						<td style="width: 113px;" width="113">

BigInt 
</td>
						<td style="width: 113px;" width="113">

*Zoned (19,0) 
</td>
						<td width="113">

</td>
						<td style="width: 113px;" width="113">

</td>
						<td  width="113">

VarBinary 
</td>
						<td style="width: 113px;" width="113">

*Hex (VarLen) 
</td>
					</tr>
					<tr style="x-cell-content-align: top;" valign="top">
						<td style="width: 113px;" width="113">

Money 
</td>
						<td style="width: 113px;" width="113">

*Zoned (19,4) 
</td>
						<td  width="113">

</td>
						<td style="width: 113px;" width="113">

</td>
						<td  width="113">

UniqueIdentifier 
</td>
						<td style="width: 113px;" width="113">

*Hex (16) 
</td>
					</tr>
					<tr style="x-cell-content-align: top;" valign="top">
						<td style="width: 113px;" width="113">

Numeric 
</td>
						<td style="width: 113px;" width="113">

*Zoned 
</td>
						<td width="113">

</td>
						<td style="width: 113px;" width="113">

</td>
						<td width="113">

</td>
						<td style="width: 113px;" width="113">

</td>
					</tr>
					<tr style="x-cell-content-align: top;" valign="top">
						<td style="width: 113px;" width="113">

SmallMoney 
</td>
						<td style="width: 113px;" width="113">

*Zoned (9,4) 
</td>
						<td style="width: 113px;" width="113">

</td>
						<td style="width: 113px;" width="113">

</td>
						<td style="width: 113px;" width="113">

</td>
						<td style="width: 113px;" width="113">

</td>
					</tr>
</table>

The types **Image, Text, and NText** are not supported. Fields of these types are hidden from the file definition. You will be able to display the file definition in Database Manager but will not be able to open the file. To ensure future application compatibility, you should not use files containing these field types. Instead, you should create logical files naming the individual fields that your application will manipulate. That way, if in a future release the fields 'appear', your application will not break 
