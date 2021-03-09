---
title: Supported Display File Attributes

Id: SupportedDspATR
TocParent: SupportedDspDDS
TocOrder: 10

keywords: ASNA Wings
keywords: ASNA Monadrch display files
keywords: ASNA Monarch display files DSPATR
keywords: Modernizing DSPATR
keywords: Migrating DSPATR
keywords: ASNA Monarch DSPATR
keywords: Display Attributes
keywords: Wings

---

<table class="bannerparthead" id="Table1" style="border-spacing: 0px" cellspacing="0">
          <tr id="hdr">
            <td colspan="1" nowrap="nowrap" rowspan="1" class="procedureSubHeading">ASNA Monarch&#174; Framework 10.0</td>           
          </tr>
</table>

# Supported Display File DDS Keywords
The following tables specify the level of support provided by ASNA Monarch Framework for DDS keywords. Links from keywords lead to the classes and properties that handle them.

## Display Attributes for DSPATR Keyword
<table  class="members" >
                     <colgroup>
                    <col width="30%" /> 
                    <col width="30%" />  
                    <col width="30%" /> 
                    </colgroup>

                        <tr><th>Supported</th><th>Not Applicable</th></tr>
                        <tr><td>BL-Blinking Field </td><td>MDT-Set Change Data Tag</td></tr>
                        <tr><td style="height: 20px">CS-Column Separator </td>

							<td style="height: 20px">OID-Operator Identification</td></tr>
						 <tr><td>HI-High Intensity</td> 

							<td>SP-Select by Light Pen</td></tr>
                        <tr><td>ND-Non Display </td><td></td></tr>
                        <tr><td> PC-Position Cursor</td> 
							<td></td></tr>
						<tr><td>PR-Protect</td><td></td></tr>
						<tr><td>Program-to-system field </td><td></td></tr>
                        <tr><td>[RI-Reverse Image](amfDdsFieldClassInvertFontColor.html) </td>
							<td></td></tr>
                        <tr><td>[UL-Underline](amfDdsFieldClassUnderlineProperty.html) </td><td></td></tr>

</table>

Wings handles most of the display attributes through directly related properties, such as Underline (for UL). In the case of BL, HI, and CS however Wings uses the following key, provided by IBM i for applying those keyword to color monitors:
<table align="center">
						<tr><th>CS</th><th>HI</th><th>BL</th><th>Converted to Color</th></tr>
						<tr><td>X</td><td></td><td></td><td><span class="color:turqoise">Turquoise</span></td></tr>
						<tr><td></td><td>X</td><td></td><td>White</td></tr>
						<tr><td></td><td></td><td>X</td><td>Red</td></tr>
						<tr><td></td><td>X</td><td>X</td><td>Red*</td></tr>
						<tr><td>X</td><td>X</td><td></td><td>Yellow</td></tr>
						<tr><td>X</td><td></td><td>X</td><td>Pink</td></tr>
						<tr><td>X</td><td>X</td><td>X</td><td>Blue</td></tr>
</table>

*<sub> Blinking is not supported, the text is only recolored red.</sub>

After the conversion, if a COLOR attribute with same option indicators is used and the color is not the same as the resulting (from BL, CS and HI display attributes), a Task is issued.

Since the inroduction of support for mapping legacy colors to Web colors, the actual color used will be the resulting from the conversion as described above, and translated color according to the mapping preferences.
