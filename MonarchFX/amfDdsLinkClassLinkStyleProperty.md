---
title: DdsLink.LinkStyle Property

Id: amfDdsLinkClassLinkStyleProperty
TocParent: amfDdsLinkClassPropertiesMain
TocOrder: 95

keywords: LinkStyle property
keywords: DdsLink.LinkStyle property
keywords: Hyperlink, text field length
keywords: hyperlink fields, text field length
keywords: hyperlink field text field length
keywords: how to, set hyperlink text field length
keywords: how to, get hyperlink text field length
keywords: web controls, setting hyperlink text field length
keywords: web controls, getting hyperlink text field length
keywords: display files, setting hyperlink text field length
keywords: display files, getting hyperlink text field length

---

Gets or sets the style of the link.

#### Syntax
<pre class="prettyprint"> **BegProp LinkStyle Access(*Public) Type(*enum)
   BegGet;   BegSet** </pre>

#### Property Values
Enumeration. Options are:

- Link  &#8211; A "blue text" hyperlink.
- Image  &#8211; 
	   		An image that also serves as a link.

#### Remarks
This property sets the DdsLink as either a standard hyperlink or a clickable [ASNA.Monarch.WebDspF](amfDdsLinkClassImageProperty">image</a>. The "Text" properties aren't used if Image is selected.

#### Requirements
**Namespace:** <a href="amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsLink Description](amfUnderstandingLinks.html)<br /> [DdsLink Class](amfDdsLinkClass.html) <br clear="none" /> [DdsLink Class Members](amfDdsLinkClassMembers.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
