---
title: DdsImage Class

Id: amfDdsImageClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 255

keywords: DdsImage class, about DdsImage class
keywords: classes [ASNA.Monarch.WebDspF], DdsImage class
keywords: field controls, date field

---

**DdsImage** is a container class that defines a Image on the web display file.

For a list of all members of this type, see [ DdsImage Members](amfDdsImageClassMembers.html).

For a short explanation of this class in use, see the [DdsImage Description](amfUnderstandingImageControls.html).

#### Applicable Products:
**Monarch, Wings, Mobile RPG** 
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
 **ASNA.Monarch.WebDspF.DdsImage** 
                </pre>

<!--mine -->

#### Inheritance Hierarchy
<pre class="syntax"> **public class DdsImage** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
An instance of **DdsImage** represents an image file on the IBM i that is translated into an on-screen Image such as those found on almost all modern web pages. The resulting image is nested in an HTML &lt;img&gt; tag on the output web page.

DdsImages can include files of type .bmp, .jpg, .gif, or .png.

DdsImages are stored in IBM i libraries, on the Web server, or on external servers.

This class was introduced with Monarch Framework 6.1, and is featured in Mobile RPG and Wings Mobile Support. It can also be used with Monarch, but only with images stored on the Web Server or on external locations.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ DdsImage Members](amfDdsImageClassMembers.html) <br />[DdsImage Description](amfUnderstandingImageControls.html)
