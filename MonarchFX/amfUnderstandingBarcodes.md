---
title: Barcode Reader Controls

Id: amfUnderstandingBarcodes
TocParent: amfASNAMobileSupport
TocOrder: 25

keywords: ASNA Mobile RPG
keywords: ASNA Mobile RPG, Barcodes
keywords: ASNA Mobile RPG, barcode controls
keywords: Mobile RPG

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# Barcode Reader Controls

### What is a DdsBarcode
Introduced in version 6.2, Monarch Framework now includes the [DdsBarcode control](amfDdsBarcodeClass.html) which supports apps capable of reading several types of both classic (UPC) barcodes and "2D" codes such as the Aztec and QR standards. For more on barcode standards, see: [ASNA Go Native Mobile Browser](http://en.wikipedia.org/wiki/Barcode"> http://en.wikipedia.org/wiki/Barcode</a>

**Applicability:** These controls can be used exclusively in Mobile RPG pages/apps.

### The Mechanics of a DdsBarcode
This control is dependent on the ASNA Go native application (see <a href="amfNativeMobileApp.html) for instructions on installing ASNA Go via the Apple Store or [DdsCharField](http://play.google.com">Google Play</a> for the Android edition). Onscreen, this control appears as an input type 'text' HTML element, with a single button associated with it. 

Pressing the button will activate the mobile device's camera, and a heads up display indicating the ideal area to capture the code in. Snapping a picture with the camera (as normal) will translate the data from the barcode. Once the barcode is identified, the code represented by the barcode will be translated into the input field. If the AidKey property is configured, then the key indicated will be submitted to the Mobile RPG application.

Note that the Scan button will not be visible at design time.

The input HTML control behaves very similarly to the <a href="amdDdsCharfieldClass.html) control. If the usage property is set to Both or InputOnly, the user can type in a code directly, but there is no client-side validation of the code format. 

### DdsBarcode Property Tasks
![](Images/DdsBarcodeTasks.png)

<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637">
   						 <tbody>

							 <tr>
           						 <td valign="top" align="center" style="width: 117px">
 **Property** 
								</td>
								<td valign="top" style="width: 468px" align="center">
 **Notes** 
								</td>
							</tr>
						<tr>
            <td colspan="2" valign="top">

**Behavior** 
</td>
        </tr>
				<tr>
					<td style="width: 117px"><code> **[AidKey](amfDdsBarcodeClassAidKeyProperty.html)** </code> </td>
					<td>(Optional - defaults to <code>'Unknown'</code>) A valid IBM AidKey to be submitted to the Mobile application as soon as the barcode is identified. (If user enters a code manually, this property does not take effect).
					</td>
				</tr>
					<tr>
					<td style="width: 117px"><code> **[BarcodeFormat](amfDdsBarcodeClassBarcodeFormatProperty.html)** </code> </td> 
					<td>(Optional - defaults to <code>'Any'</code>) Specifies the expected barcode format. If the value of the property is set to other than "<code>Any</code>" then only 
						the selected format will be identified as valid (all others will be ignored).
					</td>
				</tr> 
						<tr>
					<td style="width: 117px"><code> **[Usage](amfDdsBarcodeClassUsageProperty.html)** </code> </td>
					<td>This enumeration determines the input/output capability of the text field.
					</td>
				</tr>
		<tr>
            <td colspan="2" valign="top">

**External Description** 
</td>
        </tr>

		<tr>
					<td style="width: 117px"><code> **[ValueField](amfDdsBarcodeClassValueFieldProperty.html)** </code> </td>
					<td>(Required Property)Defines the record field used to report the name of the code 
						field.
					</td>
				</tr>	
				<tr>
					<td style="width: 117px"><code> **[ValueFieldLength](amfDdsBarcodeClassValueFieldLengthProperty.html)** </code> </td>
					<td>Defines the length (in characters) of the field that holds the code data.
					</td>
				</tr>
					<tr>
					<td style="width: 117px"><code> **[LimitMaxLength](amfDdsBarcodeClassLimitMaxLengthProperty.html)** </code> </td>
					<td>(Optional - defaults to <code>TRUE</code>) Determines whether or not to set a maximum number of character that can be entered into the Value Field.
					</td>
				</tr>
			<tr>
            <td colspan="2" align="top">

**Style** 
</td>
        </tr>
						<tr>
					<td style="width: 117px"><code> **[subtype](amfDdsBarcodeClassSubTypeProperty.html)** </code> </td>
					<td>(Optional - defaults to 'Unknown') Determines the subtype of the text field.
					</td>
				</tr>

			</tbody>
</table>

Possible Values of <code>Barcodeformat</code> include:
<table> 					
							 <tr>
           						 <td valign="top" align="center" style="width: 117px">
 **Value** 
								</td>
								<td valign="top" style="width: 468px" align="center">
 **Notes** 
								</td>
							</tr>

        		<tr><td><code>"Any"</code></td><td>Accepts all supported code formats</td></tr>
        		<tr><td><code>"OnlyAztec_2D_barcode"</code></td><td>Support may be incomplete</td></tr>
        		<tr><td><code>"OnlyCODABAR_1D"</code></td><td>Fully supported</td></tr>
        		<tr><td><code>"OnlyCode_39_1D"</code></td><td>Fully supported</td></tr>
        		<tr><td><code>"OnlyCode_93_1D"</code></td><td>Fully supported</td></tr>
        		<tr><td><code>"OnlyCode_128_1D"</code></td><td>Fully supported</td></tr>
        		<tr><td><code>"OnlyData_Matrix_2D"</code></td><td>Fully supported</td></tr>
        		<tr><td><code>"OnlyEAN_8_1D"</code></td><td>Fully supported</td></tr>
        		<tr><td><code>"OnlyEAN_13_1D"</code></td><td>Fully supported, includes ISBNs</td></tr>
				<tr><td><code>"OnlyITF_1D"</code></td><td>Interleaved Two of Five</td></tr>
				<tr><td><code>"OnlyMaxiCode_2D"</code></td><td>Fully supported</td></tr>
				<tr><td><code>"OnlyPDF417"</code></td><td>Incomplete support</td></tr>
				<tr><td><code>"OnlyQR_Code_2D"</code></td><td>Fully supported</td></tr>
				<tr><td><code>"OnlyRSS_14"</code></td><td>All variants supported</td></tr>
				<tr><td><code>"OnlyRSS_EXPANDED"</code></td><td>Most variants supported</td></tr>
				<tr><td><code>"OnlyUPC_A_1D"</code></td><td>Fully supported</td></tr>
				<tr><td><code>"OnlyUPC_E_1D"</code></td><td>Fully supported</td></tr>
				<tr><td><code>"OnlyUPC_EAN_Extension"</code></td><td>This is not 
					a stand alone option</td></tr>

</table>

#### Major barcode styles and areas of use
**One Dimensional (1-D) Barcode styles** 
<table>
			<tr>
				<td>UPC-E</td>
				<td align="center">![](Images/BarcodeUPCE.png)</td>
				<td>UPC-E is found on US retail products.</td>
			</tr>
			<tr>
				<td>EAN 8 and EAN 13</td>
				<td align="center">![](Images/BarcodeEAN8EAN13.png)</td>
				<td>EAN 8 and EAN 13 are widely used in Europe.</td>
			</tr>
			<tr>
				<td>Code 39 <br /> (with or without checksum)</td>
				<td align="center">![](Images/BarcodeCode39.png)</td>
				<td>Code 39 is mostly used in non-retail environments.</td>
			</tr>
			<tr>
				<td>Code 93</td>
				<td align="center">![](Images/BarcodeCode93.png)</td>
				<td>Code 93 is used primarliy by the Canadian Postal Service.</td>
			</tr>
			<tr>
				<td>Code 128</td>
				<td align="center">![](Images/BarcodeCode128.png)</td>
				<td>Code 128 is used worldwide by the packaging and shipping industries as product identification codes for the container and pallet
				levels of the supply chain.</td>
			</tr>
</table>

**Two Dimensional (2-D) Barcode styles** 
<table>
			<tr>
				<td>PDF417</td>
				<td align="center">![](Images/BarcodePDF417.png)</td>
				<td>PDF417 is frequently used on airline passes.</td>
			</tr>
			<tr>
				<td>QR</td>
				<td align="center">![](Images/BarcodeQR.png)</td>
				<td>QR codes are often found on buildings, or billboards, commonly linking to informational or advertising websites.</td>
			</tr>
			<tr>
				<td>Aztec</td>
				<td align="center">![](Images/BarcodeAztec.png)</td>
				<td>Aztec codes are often used on personal/businesses shipping packages.</td>
			</tr>
</table>

### Example:
<pre>&lt;mdf:DdsBarcode id="DdsBarcodeJobId" runat="server" CssClass="DdsBarcode" 
ButtonCssClass="DdsBarcodeButton" CodeFieldName="JBID" CodeFieldLength="10" 
Usage="InputOnly" BarcodeFormat="Any"  AidKey ="Enter"  Width="8em" /&gt;</pre>

