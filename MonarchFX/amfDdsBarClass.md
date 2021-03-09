---
title: DdsBar Class

Id: amfDdsBarClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 99

keywords: DdsBar class, about DdsBar class
keywords: classes [ASNA.Monarch.WebDspF], DdsBar class
keywords: field controls, date field

---

**DdsBar** is a container class that defines a bar on the web display file.

For a list of all members of this type, see [ DdsBar Members](amfDdsBarClassMembers.html).

For a short explanation of this class in use, see the [DdsBar Description](amfUnderstandingBars.html).

#### Applicable Products:
**Mobile RPG** 
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
 **ASNA.Monarch.WebDspF.DdsBar** 
                </pre>

<!--mine -->

#### Inheritance Hierarchy
<pre class="syntax"> **public class DdsBar** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
An instance of **DdsBar** represents an on-screen bar such as those often found at the top and bottom of mobile apps.

DdsBars are only useful when divided into BarSegments; the DdsBar cannot itself contain any buttons or fields.

This class was introduced with Monarch Framework 6.1, and is featured in Mobile RPG and Wings Mobile Support.

DdsBars have their positioning on the screen determined by the DdsRecord properties [NavigationBarControlID](amfDdsRecordClassNavigationBarControlIDProperty.html) and [FooterBarControlID](amfDdsRecordClassNavigationBarControlIDProperty.html). Navigation Bars are locked to the top of the screen, Footer bars to the bottom.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ DdsBar Members](amfDdsBarClassMembers.html)<br /> [DdsBar Description](amfUnderstandingBars.html) 
