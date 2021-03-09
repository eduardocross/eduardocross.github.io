---
title: DdsLink Class

Id: amfDdsLinkClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 260

keywords: DdsLink class, about DdsLink class
keywords: classes [ASNA.Monarch.WebDspF], DdsLink class
keywords: Hyperlink control
keywords: Hyperlink
keywords: Link
keywords: Link Control
keywords: Hyperlink, about

---

The **DdsLink** class defines a hyperlink field.

For a list of all members of this type, see [DdsLink Members](amfDdsLinkClassMembers.html).

For a short explanation of this class in use, see the [DdsLink Description](amfUnderstandingLinks.html).

#### Applicable Products:
**Monarch, Wings, Mobile RPG** 
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
 **ASNA.Monarch.WebDspF.DdsLink** </pre>

#### Syntax
<pre class="prettyprint"> **Public class DdsLink Inherits System.Web.UI.WebControls.WebControl** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
**DdsLink** facilitates adding html links to a Display File. When rendered it displays as a hyperlink that when clicked, opens a new browser window and requests the given page.

The **DdsLink** control is similar to the web hyperlink control where you display text describing the link and a URL that the browser will request when the text is clicked (see ASP.NET help: Hypelink Web Server Control). The advantage of the hyperlink control is that the Text and URL can be specified in the aspx code behind from the web server. A hyperLink control allows you to specify the frame or window to display the linked page.

Similarly, the **DdsLink** control allows the Text and URL to be specified in the Visual RPG logic programs as externally described data fields. The **DdsLink** control always displays the linked page in a new window.

The required properties of the **DdsLink** control define the Text and URL character fields that will be referenced by the logic program. These are [ TextFieldName](amfDdsLinkClassTextFieldNameProperty.html), [ TextFieldLength](amfDdsLinkClassTextFieldLengthProperty.html), [ UrlFieldName](amfDdsLinkClassUrlFieldNameProperty.html), and [ UrlFieldLength](amfDdsLinkClassUrlFieldLengthProperty.html).

Example: The following design time property settings of a **DdsLink** control defines two character fields:
<pre class="example">myLinkText Len(50)
myLinkURL Len(250)</pre>

The following Visual RPG code sets the text and the link values before writing the WebDisplayFile record:
<pre class="example">myLinkText = "Go to ASNA.ome page" 
myLinkURL = "http://www.ASNA.com"
Exfmt myFormat</pre>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro.

#### See Also
[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br clear="none" /> [DdsLink Class Members](amfDdsLinkClassMembers.html) <br />[DdsLink Description](amfUnderstandingLinks.html)
