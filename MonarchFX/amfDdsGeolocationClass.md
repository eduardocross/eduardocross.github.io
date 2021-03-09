---
title: DdsGeolocation Class

Id: amfDdsGeolocationClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 251

keywords: DdsGeolocation class, about DdsGelocation class
keywords: classes [ASNA.Monarch.WebDspF], DdsGeolocation class
keywords: Geolocation

---

**DdsGeolocation** is a control used to get the geographical position of the user with the device's available location facilities.

For a list of all members of this type, see [ DdsGeolocation Members](amfDdsGeolocationClassMembers.html).

For a short explanation of this class in use, see the [DdsGeolocation Description](amfUnderstandingGeoloc.html).

#### Applicable Products:
**Mobile RPG** 

#### Usage
<pre class="prettyprint"><code class="html">&lt;mdf:DdsGeolocation runat="server" 
    LatitudeField="Lat" LatitudeFieldLength="10" LatitudeFieldDecimals="5"
    LongitudeField="Lon" LongitudeFieldLength="11" LongitudeFieldDecimals="5" 
    AltitudeField="Alt" AltitudeFieldLength="10" AltitudeFieldDecimals="5"
/&gt;</code></pre>

#### Remarks
An instance of **DdsGeolocation** represents an interface by which data derived from a device's location facilities (often the HTML5 Geolocation API) can be transmitted directly to an RPG program. The Geolocation control does not require a specific location information source; it can use whatever the device has available. Most commonly, this invokes the Global Positioning System (GPS), or user input, but it can also draw from inferred locations based on network signals such as IP address, RFID, WiFi and Bluetooth MAC addresses, and GSM/CDMA cell IDs. 

Depending on the source of location resource used the control may or may not return the device's actual position.

This control is designed to enable "one-shot" position requests; it is not intended to provide continuously repeated position updates or the ability to query cached positions.

This class was introduced with Monarch Framework 6.1, and is featured in Mobile RPG.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ DdsGeolocation Members](amfDdsGeoLocationClassMembers.html) <br />[DdsGeolocation Description](amfUnderstandingGeoloc.html)
