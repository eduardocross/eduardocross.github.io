---
title: DdsGMap.MapStyle Property

Id: amfDdsGMapClassMapStyleProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: MapStyle property
keywords: DdsGMap.MapStyle property

---

Gets or sets an enumeration value that defines the type of map to be displayed in a [map control](amfDdsGMapClass.html).

#### Syntax
<pre class="prettyprint"> **BegProp MapStyle Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Sets the type of the map. Defaults to Map.
- **Map**  &#8211; (Default) Presents the map in 
		   traditional roadmap format with the **addresses**  displayed per the MarkerStyle property.
- **Satellite**  &#8211; Presents the map as a satellite 
	   map with overlaid roads.

#### Remarks
The **MapStyle** property sets the appearance of the map displayed by the map control. The default **Map** setting will load more quickly, and is often less cluttered when looking at a large area or a lot of addresses, while the **Satellite** option can provide important contextual cues and takes advantage of faster connections and platforms.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsGMap Class](amfDdsGMapClass.html) <br /> [ DdsGMap Class Members](amfDdsGMapClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
