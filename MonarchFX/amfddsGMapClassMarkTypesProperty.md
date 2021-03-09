---
title: DdsGMap.Marks Property

Id: amfddsGMapClassMarkTypesProperty
TocParent: amfDdsGMapClassPropertiesMain

keywords: Marks property
keywords: DdsGMap.Marks property

---

Gets or sets an enumeration value that defines how the **addresses** will be displayed and/or linked in a [Gmap control](amfDdsGMapClass.html).

#### Syntax
<pre class="prettyprint"> **BegProp Marks Access(*Public) Type(*enum)
   BegGet;  BegSet** </pre>

#### Property Values
Enumeration. Sets the type of the marker. Defaults to **Route** .

- **None**  &#8212; The map will be centered on the **Addresses** , 
	   	 	but individual data points will not be marked
- **Pins**  &#8212; Presents the **Addresses**  as 
		   Points with no special labels: just simple black squares.
- **Route**  &#8212; (Default) Presents the **Addresses**  as Points, joined by a route selected by the.

#### Remarks
The **Marks** property sets the appearance of the address markers displayed by the map control. The default <code>Route</code> option shows a selection of highlighted roadways connecting the <code>Addresses</code> in order; it can be very useful for determining travel times and optimizing navigation. The <code>Pins</code> option displays <code>Addresses</code> without any order, it can be useful for identifying locations and patterns when neither overland route nor order is of particular concern.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsGMap Description](amfUnderstandingMaps.html)<br /> [ DdsGMap Class](amfddsGMapClass.html) <br /> [ DdsGMap Class Members](amfddsGMapClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
