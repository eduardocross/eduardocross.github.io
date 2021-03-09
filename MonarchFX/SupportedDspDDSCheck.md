---
title: Check Keyword Support

Id: SupportedDspDDSCheck
TocParent: SupportedDspDDS
TocOrder: 30

keywords: ASNA Monarch
keywords: ASNA Wings display files
keywords: ASNA Monarch display files DDS keywords
keywords: ASNA Monarch display files field level DDS keywords
keywords: ASNA Monarch display files record level DDS keywords Check
keywords: ASNA Monarch CHECK Keyword support
keywords: ASNA Monarch display attributes for CHECK keyword
keywords: Monarch

---

<table>
			    <tr>
			       <td> <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0
				   </span><br /></td>
			    </tr>
</table>

# CHECK Keyword Support
The following tables specify the level of support provided by ASNA Monarch Framework for the functions of the <code>CHECK</code> keyword. 

## Unsupported Functions
<table  class="members" >
                    <colgroup>
                    <col width="30%" /> 
                    </colgroup>
                        <tr><th>Function Name</th><th>Function Effect</th></tr>
                        <tr><td>CHECK(FE)</td>
							<td>Field Exit Check</td></tr>
</table>

## Supported Keywords
<table  class="members" >
                    <colgroup >
                    <col width="20%" /> 

                    </colgroup>
                        <tr><th>Function Name</th><th>Function Effect</th></tr>
                        <tr><td>CHECK(ER)</td><td>Auto Record Advance</td></tr>
                        <tr><td>CHECK(LC)</td><td>Allow Lower Case</td></tr>
                        <tr><td>CHECK(AB)</td><td>Allow Blanks</td></tr>
                        <tr><td>CHECK(RB)</td><td>Right-aligned with Blank Fill</td></tr>
                        <tr><td>CHECK(RZ)</td><td>Right-aligned with Zero Fill</td></tr>
						<tr><td style="height: 23px">CHECK(ME)</td>
							<td style="height: 23px">Mandatory Enter</td></tr>
						<tr><td style="height: 25px">CHECK(MF)</td>
							<td style="height: 25px">Mandatory Fill</td></tr>	
                        <tr><td style="height: 23px">CHECK(M10), CHECK(M10F)</td>
							<td style="height: 23px">IBM Modulus 10 Algorithm</td></tr>
                        <tr><td>CHECK(M11), CHECK(M11F)</td><td>IBM Modulus 11 Algorithm</td></tr>
</table>

**CHECK(FE)** -- [Force Exit] is redundant in a browser-based UI. Web browsers already force users to employ an exit key or interaction (Tab, Shift+Tab, clicking elsewhere) to exit a field.
