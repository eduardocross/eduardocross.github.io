---
title: BannerStyles Enumeration

Id: amfBannerStylesEnumeration
TocParent: amfWebDspFEnumerations
TocOrder: 20

keywords: enumerations [ASNA.Monarch.WebDspF], BannerStyles
keywords: BannerStyles enumeration
keywords: function keys, banner style values

keywords: Vertical enumeration member
keywords: Horizontal enumeration member
keywords: FullBanner enumeration member
keywords: Hidden enumeration member

---

The 
    <code> **BannerStyles** </code> enumerated constants define how to display function keys
    on the page. 
    <pre class="syntax"> **BegEnum BannerStyles Access(*Public)** </pre>

#### Members
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="15%" /><col width="80%" /><col width="5%" align="center"/>
          </colgroup>
          <tr><th>Member</th>
  <th>Description</th>
  <th>Value</th>
          </tr>
<tr><td>FullBanner</td><td>The display is a full
          display.</td><td >0</td></tr><tr><td>Horizontal</td><td>The display is 
				horizontal. This is the default for Monarch and Wings PC sites.</td><td>1</td></tr><tr><td>Vertical</td>
				<td>The display is vertical.</td>
				<td>2</td></tr>
		 <tr><td>Hidden</td><td>This hides all function keys
          except the "Enter" and "Reset" buttons.</td><td>3</td></tr>
         <tr><td>Invisible</td><td>This hides the entire banner. Most 
			 useful for saving screen space on mobile devices, this is the 
			 default for Wings Tablet sites. </td><td>4</td></tr></table>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl><dd>[
    ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd> 
    <dd>[
    DdsFile.BannerStyle](amfDdsFileClassBannerStyleProperty.html)</dd></dl>

