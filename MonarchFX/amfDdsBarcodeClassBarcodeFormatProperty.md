---
title: DdsBarcode.BarcodeFormat Property

Id: amfDdsBarcodeClassBarcodeFormatProperty
TocParent: amfDdsBarcodeClassProperties
TocOrder: 10

keywords: BarcodeFormat property
keywords: available Barcode Formats
keywords: BarcodeFormat, setting values
keywords: BarcodeFormat Property Dialog, setting values
keywords: DdsBarcode.BarcodeFormat property
keywords: dds barcode, aBarcodeFormat
keywords: field controls, dds barcode, BarcodeFormat

---

Property that sets the format or formats of barcode that the barcode control will recognize and accept.

#### Syntax
<pre class="syntax"> **BegProp BarcodeFormat Access(*Public) Type(*Enumeration)
   BegGet:  BegSet** </pre>

#### Property Values
**Enumeration.** One of the enumeration values from the following list:
<table><thead>Value</thead><thead>Notes</thead>
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

#### Remarks
To set the BarcodFormat property at design-time, click on the right hand side of the property window and select the key from the drop-down list.

The list of available barcode formats is drawn from the Zebra Crossing library, version dated Nov 19, 2013. The list can be found at [ASNA.Monarch.WebDspF](https://code.google.com/p/zxing/">https://code.google.com/p/zxing/</a>

#### Requirements
**Namespace:** <a href="amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsBarcode Class](amfDdsBarcodeClass.html) <br /> [DdsBarcode Class Members](amfDdsBarcodeClassMembers.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
