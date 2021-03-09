---
title: GoogleMap Controls

Id: amfUnderstandingMaps
TocParent: amfASNAMobileSupport
TocOrder: 40

keywords: ASNA Mobile RPG
keywords: ASNA Mobile RPG, GMaps
keywords: ASNA Mobile RPG, workstation feedback
keywords: Mobile RPG
keywords: Maps
keywords: Map Control

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# GoogleMap Controls
**Warning -** Users of the DdsGMap (Map) Control must comply with the Google Maps API Terms of Service which now require obtaining a license from Google (generally free for development, although certain commercial sites and applications will eventually require a paid license). See [DdsGMap Control](https://developers.google.com/maps/faq#tos"> https://developers.google.com/maps/faq#tos</a>.

Prior to June 22, 2016 Google rarely enforced the requirement for a key, and sites published before that date will generally not require a license until October of 2016, but new sites must have a key for this control (or any other integration of Google Maps) to function properly. Google allows most sites using a free key up to 25,000 requests per day. After that they require payment (follow the link above for more detail on Google's policies).

A key accquired from Google at: <a href="https://developers.google.com/maps/documentation/javascript/get-api-key">https://developers.google.com/maps/documentation/javascript/get-api-key</a> must be used as the value for the "MonarchGoogleMapKey" attribute in the Web.config file. (A less preferred option is to enter a key into the GoogleKey property for each DdsGMap in the app/site.)

### What is a DdsGMap?
A DdsGMap is a control that allows users to create customized maps from data in a subfile on the IBM i. The subfile contains the addresses to display and order in which to use them (they are shown in the same order as the records). The map control uses the GoogleMaps API, with the familiar GoogleMaps interface, but takes selected data from the subfile on the IBM i and can organize it as routes or individual flags. Similarly, the map control can be configured to display either a road map, a satellite map, or a hybrid displaying roads overlaid on a satellite image. Maps are enabled by the <a href="amfDdsGMapClass.html), a part of the Monarch Framework.

### The Mechanics of a DdsGMap
As with all of the ASNA Mobile support controls, each of the parameters for the map control can be set on the IBM i or through Visual Studio.

**Applicability:** These controls can be used in Monarch, Wings, and Mobile RPG pages/apps.

The IBM i sees the Map as nothing more than a subfile populated with numbers and addresses; this information is fed into the GoogleMaps API in order to generate the map. The way the map displays that data is determined largely by the following properties:
![](Images/DdsGMapTasks.png)

#### DdsGMap Property Tasks
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

**Appearance** 
</td>
			</tr>
				<tr><td><code> **[MapType](amfDdsGMapClassMapTypeProperty.html)** </code></td>
					<td>Used to select which type of map (road, terrain, satellite, or hybrid) to display.</td></tr>
				<tr><td><code> **[Marks](amfDdsGMapClassMarkTypesProperty.html)** </code></td>
					<td>Used to determine what type of marks to display on the map.</td></tr>

			<tr><td><code> **[ShowCurrentLocation](amfDdsGMapClassShowCurrentLocationProperty.html)** </code></td><td>Sets whether or not to display the mobile device's
				current location.</td></tr>
			<tr><td><code> **[UseLocationSensor](amfDdsGMapClassUseLocationSensorProperty.html)** </code></td><td>Used to determine whether to access the location sensor on the 
				mobile device in order to generate the map.</td></tr>
			<tr><td><code> **[PinLabelType](amfDdsGMapClassPinLabelTypeProperty.html)** </code></td>
			<td>Used to determine how the label on the pin is displayed (Options include ToolTip. Opened Pop Up, and Closed 
			Pop Up).</td></tr>
				<tr><td><code> **[PinIcon](amfDdsGMapClassPinIconProperty.html)** </code></td>
					<td>Sets an icon to display for "normal" (unselected)  map pins.</td></tr>
			<tr><td><code> **[SelectedPinIcon](amfDdsGMapClassSelectedPinIconTypeProperty.html)** </code></td>
					<td>Sets an icon to display for selected map pins.</td></tr>
	<tr>				
	<td valign="top" width="169">
		<code> **[AddressField](http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.height(v=vs.110).aspx">Height</a>
		 &amp; <br /><a href="http://msdn.microsoft.com/en-us/library/system.web.ui.webcontrols.webcontrol.width(v=vs.110).aspx">Width</a>** </code>
	</td>
	<td valign="top" width="468">
		These properties set the height and width of the control in whichever unit is specified (pixels, by default).</td>
	</tr>
			<tr>
            <td colspan="2" valign="top">

**Data** 
</td>
			</tr>
			<tr><td><code> **<a href="amfDdsGMapClassAddressFieldProperty.html) &amp; 
				[AddressFieldLength](amfDdsGMapClassAddressFieldLengthProperty.html)** </code></td>
				<td>These properties define a character field whose runtime value is to be used as the file path to the address. </td></tr>
			   <tr><td><code> **[ClearIndicator](amfDdsGMapClassClearIndicatorProperty.html)** </code></td>
					<td>Used to set the clear indicator for the subfile on the IBM i.</td></tr>
			   <tr><td><code> **[GoogleKey](amfDdsGMapClassGoogleKeyProperty.html)** </code></td>
					<td>Used to set the product key for the GoogleMaps API.</td></tr>
			    <tr><td><code> **[SubfileControlName](amfDdsGMapClassSubfileControlNameProperty.html)** </code></td>
					<td>Used to define the name of the subfile control associated with the map.</td></tr>
			    <tr><td><code> **[SubfileName](amfDdsGMapClassSubfileNameProperty.html)** </code></td>
					<td>Used to define the name of the subfile associated with the map.</td></tr>		
			    </tbody>
</table>

#### New Features
A few new features have been added to the DdsGMap since its introduction, mostly related to how the pins created by the [Marks](amfDdsGMapClassMarkTypesProperty.html) Property behave:

- [PinLabelField](amfDdsGMapClassPinLabelFieldProperty.html) 
					and [PinLabelFieldLength](amfDdsGMapClassPinLabelFieldLengthProperty.html) &#8211; 
					 Define a character field whose runtime value is used  as the file path to the labels that are applied to each address pin.
- [PinIconField](amfDdsGMapClassPinIconFieldProperty.html) 
					and [PinIconFieldLength](amfDdsGMapClassPinIconFieldLengthProperty.html) &#8211; 
					 Define a character field whose runtime value is used  as the file path to the icon that is applied to each address pin.
- [PinTagField](amfDdsGMapClassPinTagFieldProperty.html) &#8211; Specifies the name of a subfile field which will be used to add a tag to the marker for the address..
- [SelectPinKey](amfDdsGMapClassSelectPinKeyProperty.html) &#8211; Sets a function key that is entered 
					when a pin is selected.
- [SelectedField](amfDdsGMapClassSelectedFieldProperty.html) &#8211; Sets whether a record or field currently 
					selected, allowing users to select multiple pins.

The Web.config file's <code>&lt;AppSetting&gt;</code> section has been enhanced with a new attribute, <code>MonarchGoogleMapKey</code> which allows the developer to set a single universal key for each instance of a DdsGMap that occurs in the page. The syntax for this is shown below:
<pre>
					&lt;appSettings&gt;
  .  .  .
  &lt;add key="MonarchGoogleMapKey" value="AKeyProvidedByGoogle"/&gt;
&lt;/appSettings&gt;
					</pre>

This is intended to be easier to use than the [GoogleKey](amfDdsGMapClassGoogleKeyProperty.html) Property, although if the GoogleKey property is populste it will override this value.
