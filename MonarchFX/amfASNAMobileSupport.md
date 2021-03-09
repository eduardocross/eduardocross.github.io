---
title: ASNA Mobile Support

Id: amfASNAMobileSupport
TocParent: welcome
TocOrder: 44

keywords: concepts, ASNA Monarch, about
keywords: ASNA Monarch
keywords: concepts, ASNA Monarch
keywords: ASNA Monarch, concepts

---

The ASNA Monarch Framework has a number of options, primarily in the form of controls, that are specially targeted to developing pages for mobile environments. These controls are available to all members of the Monarch Family of products (ASNA Monarch, ASNA Wings, and ASNA Mobile RPG). Several other controls were updated and expanded to optimize their function for a mobile environment.

These controls were introduced beginning with Monarch Framework v 6.1, and have been expanded in subsequent versions.

Certain controls introduced in Monarch Framework v 6.2 and later use features of mobile hardware that are unavailable to standard browsers. Pages which use these controls are best accessed via the [ASNA Go](amfNativeMobileApplication.html) native application.

### Mobile Controls
- Bar Controls &#8211; Mobile-style bars that may appear at the top or bottom of the screen.
		  	  They contain and are divided by Bar Segments.
		  	<ul><li>[Bar Control Description](amfUnderstandingBarControls.html)
- [DdsBar Documentation](amfDdsBarClass.html)
- [DdsBarSegment  Documentation](amfDdsBarSegmentClass.html)

</li></ul>
- Chart Controls &#8211; Interactive charts that display data gathered from specified subfiles.
		  	<ul><li>[Chart Control Description](amfUnderstandingCharts.html)
- [DdsChart Documentation](amfDdsChartClass.html)

</li></ul>
- ExpandingList Controls &#8211; Lists that allow the user to add and peruse additional entries.
		  	<ul><li>[ExpandingList Control Description](amfUnderstandingExpandingLists.html)
- [DdsExpandingList Documentation](amfDdsExpandingListClass.html)

</li></ul>
- Geolocation Controls - Controls that use the mobile hardware to return 
	 the GPS location of the device.
		  	<ul><li>[Geolocation Control Description](amfUnderstandingGeoloc.html)
- [DdsGeolocation Documentation](amfDdsGeolocationClass.html)

</li></ul>
- GMap Controls - Maps created using the GoogleMaps API.
		  	<ul><li>[GoogleMap Control Description](amfUnderstandingMaps.html)
- [DdsGMap Documentation](amfDdsGMapClass.html)

</li></ul>

- HostFile Controls &#8211; File hosting controls that access files on the IFS or Windows file system.
 		  	<ul><li>[HostFile Control Description](amfUnderstandingHostFiles.html)
- [DdsHostFile Documentation](amfDdsHostFileClass.html)

</li></ul>
- Icon Controls - Non interactive icons chosen from the [Icon selection](amfIconSelection.html) array.
		   <ul><li>[Icon Control Description](amfUnderstandingIcons.html)
- [DdsIcon Documentation](amfDdsIconClass.html)

</li>
			</ul>
- Image Controls - Images pulled from any of a number of sources 
	 (including the IFS)<ul><li>[Image Control Description](amfUnderstandingImageControls.html)
- [DdsImage Documentation](amfDdsImageClass.html)

</li></ul>
- List Controls - Multi-featured lists created based on subfile data.
		  	<ul><li>[Lists Control Description](amfUnderstandingLists.html)
- [DdsList Documentation](amfDdsListClass.html)

</li></ul>

- Signature Controls - Intuitive controls that
                  allow users to draw and record their signatures.                  <ul>
                      <li>
                          [Signature Control Description](amfUnderstandingSignatures.html)
- [DdsSignature Documentation](amfDdsSignatureClass.html)

</li>
          </ul>

- Switch Controls - Simple controls that can present users with either mobile-friendly on-off switches or checkboxes                  
				  <ul>
                      <li>
                          [Switch Control Description](amfUnderstandingSwitches.html)
- [DdsSwitch Documentation](amfDdsSwitchClass.html)

</li>
          </ul>

- Table Controls - User friendly tables that give subfile data a mobile-ready presentation               
				  <ul>
                      <li>
                          [Table Control Description](amfUnderstandingTables.html)
- [DdsTable Documentation](amfDdsTableClass.html)

</li>
			  </ul>

- <ul>
					  <li>Uploader Controls - Simple drag-and-drop controls that let the user upload files of various types.
- [Uploader Control Description](amfUnderstandingUploaders.html)
- [DdsUploader Class Documentation](amfDdsUploaderClass.html)

</li>
          </ul>

### Enhanced Controls
- Button Controls - Buttons can now present icons from a large selection.
 		  	<ul><li>[Button Control Description](amfUnderstandingButtons.html)
- [DdsButton Documentation](amfDdsButtonClass.html)

</li></ul>
- Link Controls - Links can now be presented as images.
 		<ul><li>[Link Control Description](amfUnderstandingLinks.html)
- [DdsLink Documentation](amfDdsLinkClass.html)

</li></ul>

### Native Controls
- Barcode Controls - Barcode scanning controls using the mobile device's camera.
		<ul><li>[Barcode Control Description](amfUnderstandingBarcodes.html)
- [DdsBarcode Documentation](amfDdsBarcodeClass.html)

</li></ul>

## Controls by Product
Some of the controls implemented as part of Mobile Support are only available to developers who're using particular ASNA products. These are outlined in the table below.
<table>
					<tr><td align="center" bgcolor="4A4FE5" colspan="4"> **DdsControls Restricted by Product** </td></tr>
					<tr><td align="center" bgcolor="BCD3EF"> **Control** </td><td align="center" bgcolor="BCD3EF"> **Monarch** </td><td align="center" bgcolor="BCD3EF"> **Wings** </td><td align="center"  bgcolor="BCD3EF"> **Mobile RPG** </td></tr>
					<tr><td bgcolor="BCD3EF">DdsBar</td><td style="color:red">No</td><td style="color:red">No</td><td style="color:green">Yes</td></tr>
					<tr><td bgcolor="BCD3EF">DdsBarcode</td><td style="color:red">No</td><td style="color:red">No</td><td style="color:green">Yes</td></tr>
					<tr><td bgcolor="BCD3EF">DdsBarSegment</td><td style="color:red">No</td><td style="color:red">No</td><td style="color:green">Yes</td></tr>
					<tr><td bgcolor="BCD3EF">DdsExpandingList</td><td style="color:red">No</td><td style="color:red">No</td><td style="color:green">Yes</td></tr>
					<tr><td bgcolor="BCD3EF">DdsGeolocation</td><td style="color:red">No</td><td style="color:red">No</td><td style="color:green">Yes</td></tr>
					<tr><td bgcolor="BCD3EF">DdsHostFile</td><td style="color:red">No</td><td style="color:green">Yes</td><td style="color:green">Yes</td></tr>
					<tr><td bgcolor="BCD3EF">DdsList</td><td style="color:red">No</td><td style="color:green">Yes*</td><td style="color:green">Yes</td></tr>
					<tr><td bgcolor="BCD3EF">DdsSubfile</td><td style="color:green">Yes</td><td style="color:green">Yes</td><td style="color:red">No</td></tr>
					<tr><td bgcolor="BCD3EF">DdsSubfileControl</td><td style="color:green">Yes</td><td style="color:green">Yes</td><td style="color:red">No</td></tr>
					<tr><td bgcolor="BCD3EF">DdsTable</td><td style="color:red">No</td><td style="color:red">No</td><td style="color:green">Yes</td></tr>
</table>

*The <code>Navigation</code> ListType is exclusive to Mobile RPG.

Any control not included above is shared by all three products.

#### See Also
[What's New](amfWhatsNewin72.html) <br clear="none" /> [Reference Library](amfReferenceMain.html) 
