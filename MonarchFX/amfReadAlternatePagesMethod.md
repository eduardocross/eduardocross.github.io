---
title: The ReadAlternatePagesConfig Method

Id: amfReadAlternatePagesMethod
TocParent: amfASNAMobileSupport
TocOrder: 03

keywords: Mobile Support

---

**Warning &#8211;** This feature is deprecated as of version 8.0.18.0. When new websites are generated the <code>App_Data/AlternatePages.Config</code> file is no longer created, nor is the code to process such files included in **Global.asax** .

When a 5250 Terminal (Emulation) page is displayed, and the device running the browser (or AsnaGo) is a Tablet (identified by the <code>window.navigator.userAgent</code> DOM property having a value that contains the words "iPad", "iPhone", "iPod", "Android" or "Touch"), the page will be replaced with a version in the "Tablet" folder of the same name. This remains the default behavior of the "Alternate Pages" feature, concerning the 5250 Terminal Emulation. 

If the developer must refine the logic that determines when will the Tablet version of the 5250 Terminal Emulation should be used, it is now necessary to change the following global JavaScript function:
<table>
				<tr><td>File</td><td>..\Themes\Current\Asna5250Terminal.aspx </td></tr>
				<tr><td>Function</td><td>checkTabletRedirect()</td></tr>
				<tr><td>Parameters</td><td>none</td></tr>
				<tr><td>Return Value</td><td>(Boolean) true if the current page should be replaced with the Tablet version, 
				false if the page should not be replaced.</td></tr>
</table>

Developers often have no control over the devices their web pages will be viewed on, and with the ascension of smart phones and tablets, it can be extremely difficult to design a page that looks and functions ideally on all likely form factors. To help handle this issue, the Monarch Framework includes a system that allows developers to create distinct (although usually very similar) pages for various devices. 

Instead of trying to design pages that will look good in all devices, the application designer may want to provide "Alternative Pages" for some devices. For example, if the device can be identified as a Phone, then the alternative page may hide some (non-essential) information and use a different layout.

The way in which the Monarch Framework allows different Web Pages to be loaded, given the **same name** of the Web Page (since the display file the application is requesting remains the same), is through the use of folders. These folders all share the same root (the Website "Views" -- "MobileDFs" in MobileRPG -- folder). The syntax of the configuration table refers to them as "subfolders".

The <code>ReadAlternatePagesConfig()</code> method **loads into memory** a "folder-lookup table" keyed by an expression based on the "UserAgent" (which is the way a browser identifies itself) - see [ASNA Monarch Language Reference
        Library](http://en.wikipedia.org/wiki/User_agent" target="_blank"> http://en.wikipedia.org/wiki/User_agent</a>.

The "folder-lookup table" is an xml file stored in 
<pre>
							..\App_Data\AlternatePages.config</pre>

The following is an example of such a file:
<pre class="prettyprint">&lt;?xmlversion="1.0"encoding="utf-8"standalone="yes"?&gt;
&lt;RedirectRules&gt;

&lt;agentcontains="iPad"subfolder="Tablet"/&gt;
&lt;!--Apple iPad: Mozilla/5.0 (iPad; U; CPU OS 3_2 like Mac OS X; en-us) AppleWebKit/531.21.10 (KHTML, like Gecko) Version/4.0.4 Mobile/7B334b Safari/531.21.10 --&gt;

&lt;agentcontains="Android"subfolder="Tablet"/&gt;
&lt;!--ASUS Tablet: Mozilla/5.0 (Linux; U; Android 2.1-update1; en-us;) AppleWebKit/530.17 (KHTML, like Gecko) Version/4.0 Mobile Safari/530.17 --&gt;

&lt;agentcontains="Touch"subfolder="Tablet"/&gt;
&lt;!--Windows Phone 8: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; Touch; .NET4.0C; .NET CLR 3.0.30729; .NET CLR 2.0.50727) --&gt;

&lt;agentcontains="iPhone"subfolder="SmartPhone"/&gt;
&lt;!--Apple iPhone: Mozilla/5.0 (iPhone; U; CPU iPhone OS 4_0 like Mac OS X; en-us) AppleWebKit/532.9 (KHTML, like Gecko) Version/4.0.5 Mobile/8A293 Safari/6531.22.7 --&gt;
&lt;/RedirectRules&gt;</pre>

Where each "Redirect rule" uses the Browser User-Agent <a href="http://en.wikipedia.org/wiki/User_agent" target="_blank"> http://en.wikipedia.org/wiki/User_agent</a> with the string expression "contains", such that if the result is **true** , then Wings will attempt to find the page in the subfolder indicated. If an aspx file is found in the subfolder, that page will be used. If no such file is found, then the page in the root ( ~/Views ) will be used instead.

Notice how the User-Agent <a href="http://en.wikipedia.org/wiki/User_agent" target="_blank"> http://en.wikipedia.org/wiki/User_agent</a> string is rather long and cryptic. It is supposed to be unique, but normally just a few pieces are necessary to identify the device in question. The file above shows, as comments, a typical value of the User-Agent string for different devices. (Comments are of course ignored by XML.)

For example, the first rule:
<pre class="prettyprint">&lt;agentcontains="iPad"subfolder="Tablet"/&gt;
&lt;!--Apple iPad: Mozilla/5.0 (iPad; U; CPU OS 3_2 like Mac OS X; en-us) AppleWebKit/531.21.10 (KHTML, like Gecko) Version/4.0.4 Mobile/7B334b Safari/531.21.10 --&gt;
</pre>

Will be true, if the User-Agent string contains the word "<code>iPad</code>". If the browser requesting the page is a Windows PC, the value may be "Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.1; Trident/6.0)" and the expression <code>contains="iPad"</code> evaluates to <code>false</code>, therefore the subfolder "Tablet" will not be used while searching for the requested Page. In contrast, if the device requesting the page is an Apple iPad, then the value of the User-Agent will likely be <code>"Apple iPad: Mozilla/5.0 (iPad; U; CPU OS 3_2 like Mac OS X; en-us) AppleWebKit/531.21.10 (KHTML, like Gecko) Version/4.0.4 Mobile/7B334b Safari/531.21.10"</code>, and the expression <code>contains="iPad"</code> evaluates to **<code>true</code>,** therefore the subfolder "Tablet" will be used (i.e. Wings will look in ~/Views/Tablet" first for the requested page.

Note: The ..\App_Data\AlternatePages.config should be adjusted to the Application needs. The implementation of <code>ReadAlternatePagesConfig()</code> should not be changed.

#### See Also
<dl>
        <dd><a href="amfReferenceMain.html)</dd>
        <dd>[ASNA Monarch Framework Concepts](amfASNAMonarchFrameworkConceptsMain.html)</dd>

</dl>

