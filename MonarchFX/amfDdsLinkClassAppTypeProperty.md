---
title: DdsLink.AppType Property

Id: amfDdsLinkClassAppTypeProperty
TocParent: amfDdsLinkClassPropertiesMain
TocOrder: 02

keywords: AppType property
keywords: DdsLink.AppType property
keywords: Hyperlink, application type
keywords: hyperlink fields, app type
keywords: hyperlink field apptype
keywords: how to, set hyperlink text app type
keywords: how to, get hyperlink text application type
keywords: web controls, setting hyperlink application type
keywords: web controls, getting hyperlink app type
keywords: display files, setting hyperlink application type
keywords: display files, getting hyperlink app type

---

Gets or sets the type of application that the DdsLink control will interact with.

#### Syntax
<pre class="prettyprint"> **BegProp AppType Access(*Public) Type(*enum)
   BegGet;   BegSet** </pre>

#### Property Values
Enumeration. Defines the type of application that the DdsLink is intended to connect to. Each option sets a URI scheme name for the link address. Options include:
<table><tr><th>Value</th><th>URI scheme name</th><th>Effect</th></tr>
	  	<tr><td>Browser</td><td>http</td><td>(default) Calls the device's default internet browser</td></tr>
	  	<tr><td>Email</td><td>mailto</td><td>Calls the device's default mail application</td></tr>
		<tr><td>Telephone</td><td>tel</td><td>Uses the device's built-in phone call software</td></tr>
		<tr><td>TextMessage</td><td>sms</td><td>Uses the device's built-in text messaging application</td></tr>
		<tr><td>Explicit</td><td>See Remarks</td><td>Calls an explicitly defined application</td></tr>

</table>

#### Remarks
This enumeration controls which type of application the DdsLink will target. By default (and exclusively in older versions of this control) a browser is called, but the additional options help take advantage of the varied means of communication often employed by web sites and mobile applications.

The **Browser** value's behavior (whether it opens a new window, opens a new tab, or replaces the current window) is generally determined by the preferences set in the browser. The exception is when running in full screen on an iOS device using [ASNA.o](amfNativeMobileApp.html) or by accessing the page directly from your homescreen: under those circumstances the link will always open a new browser window so that data and state will not be lost.

The value of **Explicit** instructs the framework not to attach any scheme name prefix to the URL; it is the application's responsibility to form the complete URL. This allows for creating links to any third party target (Facebook or Skype for example). Visit Wikipedia for a list of valid scheme names: [ASNA.Monarch.WebDspF](http://en.wikipedia.org/wiki/URI_scheme#Official_IANA-registered_schemes">http://en.wikipedia.org/wiki/URI_scheme#Official_IANA-registered_schemes</a>, as well as more information on URI formatting.

The Property was added with version 6.1.

#### Requirements
**Namespace:** <a href="amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsLink Description](amfUnderstandingLinks.html)<br /> [DdsLink Class](amfDdsLinkClass.html) <br clear="none" /> [DdsLink Class Members](amfDdsLinkClassMembers.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
