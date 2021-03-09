---
title: DdsGMap.MapType Property

Id: amfDdsGMapClassMapTypeProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: MapType property
keywords: DdsGMap.MapType property

---

Gets or sets an enumeration value that defines the type of map to be displayed in a [map control](amfDdsGMapClass.html).

#### Syntax
<pre class="prettyprint"> **BegProp MapType Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Sets the type of the map. Defaults to **Road** .
- **Road**  &#8211; (Default) Presents the map in 
		   traditional roadmap format with the **addresses**  displayed per the Marks property.
- **Hybrid**  &#8211; Presents a satellite map with an overlaid network of named roads.
- **Satellite**  - Presents the map as a satellite map with 
	   no overlay.
- **Terrain**  &#8211; Presents a roadmap with visible 
		   terrain features and elevation.

#### Remarks
The **MapType** property sets the appearance of the map displayed by the map control. The default **Map** setting will load more quickly, and is often less cluttered when looking at a large area or a lot of addresses, while the **Hybrid** option can provide important contextual cues and takes advantage of faster connections and platforms. 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGMap Description](amfUnderstandingMaps.html)<br /> [ DdsGMap Class](amfDdsGMapClass.html) <br /> [ DdsGMap Class Members](amfDdsGMapClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
