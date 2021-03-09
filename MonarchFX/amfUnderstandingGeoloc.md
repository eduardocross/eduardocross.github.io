---
title: Geolocation Controls

Id: amfUnderstandingGeoloc
TocParent: amfASNAMobileSupport
TocOrder: 35

keywords: ASNA Mobile RPG
keywords: ASNA Mobile RPG, Geolocation
keywords: ASNA Mobile RPG, GPS
keywords: Mobile RPG
keywords: GPS
keywords: Geolocation Control

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0</span></td>
			    </tr>
</table>

# Geolocation Control

### What is a DdsGeolocation?
Many mobile Apps take advantage of the built-in ability of mobile devices to pinpoint themselves on the Global Positioning System. ASNA-based Mobile Apps can do the same through the [DdsGeolocation](amfDdsGeolocationClass.html) Control. It allows the program to access the devices' built-in GPS API, and therefore determine the location of the end-user. 

**Applicability:** These controls can be used exclusively in Mobile RPG pages/apps.

### The Mechanics of a DdsGeolocation
This particular control uses a number of "packed" fields, each of which is comprised of three properties. These properties follow the schema: <code>[ *Name* Field](amfDdsGeolocationClassLatitudeFieldProperty.html)</code>, <code>[ *Name* FieldLength](amfDdsGeolocationClassLatitudeFieldLengthProperty.html)</code>, <code>[ *Name* FieldDecimals](amfDdsGeolocationClassLatitudeFieldDecimalsProperty.html)</code>. The runtime values of these three properties define IBM i fields that the program can use to pinpoint the end user's geolocation. 

#### DdsGeolocation Property Tasks 
![](Images/DdsGeolocationTasks.png)

<table class="TaskTable" border="1" cellspacing="0" cellpadding="0" width="637">
    <tbody>
        <tr>
            <td valign="top" width="185">

**Property for Field *Name* ** 
</td>
            <td valign="top" width="452">

**Notes** 
</td>
        </tr>
        <tr>
            <td valign="top" width="185">

<code> **[Latitude](amfDdsGeolocationClassLatitudeFieldProperty.html)** </code> 
</td>
            <td valign="top" width="452">

Expressed in Decimal Degrees. Bounded by +/- 90°. Positive latitudes are north of the equator. Negative latitudes are south of the equator. 
</td>
        </tr>
        <tr>
            <td valign="top" width="185">

<code> **[Longitude](amfDdsGeolocationClassLongitudeFieldProperty.html)** </code> 
</td>
            <td valign="top" width="452">

Expressed in Decimal Degrees. Bounded by +/- 90°. Positive longitudes are east of the Prime Meridian (Greenwich, England). Negative longitudes are west of the Prime Meridian. 
</td>
        </tr>
        <tr>
            <td valign="top" width="185">

<code> **[Accuracy](amfDdsGeolocationClassAccuracyFieldProperty.html)** </code> 
</td>
            <td valign="top" width="452">

This property determines the accuracy to which the Latitude and Longitude are reported. Expressed in Meters. 
</td>
        </tr>
        <tr>
            <td valign="top" width="185">

<code> **[Altitude](amfDdsGeolocationClassAltitudeFieldProperty.html)** </code> 
</td>
            <td valign="top" width="452">

Expressed in Meters. This reports the altitude of the device relative to the WGS84 ellipsoid (roughly sea level), 
</td>
        </tr>
        <tr>
            <td valign="top" width="185">

<code> **[AltitudeAccuracy](amfDdsGeolocationClassAltitudeAccuracyFieldProperty.html)** </code> 
</td>
            <td valign="top" width="452">

Expressed in Meters. 
</td>
        </tr>
		        <tr>
            <td valign="top" width="185">

<code> **[ErrorCode](amfDdsGeolocationClassErrorCodeFieldProperty.html)** </code> 
</td>
            <td valign="top" width="452">

This receives an error code that developers can use for debugging purposes. 
</td>
			</tr>
					        <tr>
            <td valign="top" width="185">

<code> **[ErrorCode](amfDdsGeolocationClassErrorCodeFieldProperty.html)** </code> 
</td>

            <td valign="top" width="452">

This receives an error message that developers can use for debugging purposes. 
</td>
        </tr>
    </tbody>
</table>

