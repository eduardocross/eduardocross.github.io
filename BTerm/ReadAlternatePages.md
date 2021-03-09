---
title: Configuring Device-Specific Alternate Pages

Id: ReadAlternatePages
TocParent: HowTos
TocOrder: 65

keywords: ASNA Browser Terminal
keywords: ASNA Browser Terminal, Walkthroughs
keywords: Modernization
keywords: Display files
keywords: Mobile
keywords: Alternate Pages
keywords: Device Specific
keywords: ReadAlternatePagesConfig
keywords: Controls
keywords: Changing controls

---

<table>
			    <tr>
			       <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA 
				   MobileRPG&#8482; Reference Manual<br />
				   </span>
				    </td>
			    </tr>
</table>

Developers often have no control over the devices their web pages will be viewed on, and with the ascension of smart phones and tablets, it can be extremely difficult to design a page that looks and functions ideally on all likely form factors. To help handle this issue, the Monarch Framework includes a system that allows developers to create distinct (although usually very similar) pages for various devices. 

Instead of trying to design pages that will look good in all devices, the Mobile application developer may want to provide “Alternative” “Pages” pages for some devices. For example, if the device can be identified as a Phone, then the alternative page may hide some (non-essential) information and use a different layout.

The way in which BTerm (via the Monarch Framework) allows different Web Pages to be loaded, given the **same name** of the Web Page (since the display file the application is requesting remains the same), is through the use of folders. These folders all share the same root (the Website “Views”). The syntax of the configuration table refers to them as “subfolders”.

The ReadAlternatePagesConfig() method in Global.asax **loads into memory** a “folder-lookup table” keyed by an expression based on the “UserAgent” (which is the way a browser identifies itself) – see <a href="http://en.wikipedia.org/wiki/User_agent" target="_blank"> http://en.wikipedia.org/wiki/User_agent</a>.

The “folder-lookup table” is an xml file stored in <code>..\App_Data\AlternatePages.config</code>

An AlternatePages.config file might look like the following:
<span style="font-size: 11pt;">
 <span style="font-size: 9.5pt; background-color: white;">
							&lt;?</span> <span style="font-size: 9.5pt; background-color: white;">xml</span> <span style="font-size: 9.5pt; background-color: white;">version</span> <span style="font-size: 9.5pt; background-color: white;">=</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">1.0</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">encoding</span> <span style="font-size: 9.5pt; background-color: white;">=</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">utf-8</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">standalone</span> <span style="font-size: 9.5pt; background-color: white;">=</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">yes</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">?&gt;</span> </span> <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt; background-color: white;">
							&lt;</span> <span style="font-size: 9.5pt; background-color: white;">RedirectRules</span> <span style="font-size: 9.5pt; background-color: white;">&gt;</span> </span> <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt; background-color: white;">
							&lt;</span> <span style="font-size: 9.5pt; background-color: white;">agent</span> <span style="font-size: 9.5pt; background-color: white;">contains</span> <span style="font-size: 9.5pt; background-color: white;">=</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">iPad</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">subfolder</span> <span style="font-size: 9.5pt; background-color: white;">=</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">Tablet</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">/&gt;</span> </span> <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt; background-color: white;">
							&lt;!--</span> <span style="font-size: 9.5pt; background-color: white;">Apple 
							iPad: Mozilla/5.0 (iPad; U; CPU OS 3_2 like Mac OS 
							X; en-us) AppleWebKit/531.21.10 (KHTML, like Gecko) 
							Version/4.0.4 Mobile/7B334b Safari/531.21.10 </span>
 <span style="font-size: 9.5pt; background-color: white;">
							--&gt;</span> </span> <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt; background-color: white;">
							&lt;</span> <span style="font-size: 9.5pt; background-color: white;">agent</span> <span style="font-size: 9.5pt; background-color: white;">contains</span> <span style="font-size: 9.5pt; background-color: white;">=</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">Android</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">subfolder</span> <span style="font-size: 9.5pt; background-color: white;">=</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">Tablet</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">/&gt;</span> </span> <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt; background-color: white;">
							&lt;!--</span> <span style="font-size: 9.5pt; background-color: white;">ASUS 
							Tablet: Mozilla/5.0 (Linux; U; Android 2.1-update1; 
							en-us;) AppleWebKit/530.17 (KHTML, like Gecko) 
							Version/4.0 Mobile Safari/530.17 </span> <span style="font-size: 9.5pt; background-color: white;">
							--&gt;</span> </span> <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt; background-color: white;">
							&lt;</span> <span style="font-size: 9.5pt; background-color: white;">agent</span> <span style="font-size: 9.5pt; background-color: white;">contains</span> <span style="font-size: 9.5pt; background-color: white;">=</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">Touch</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">subfolder</span> <span style="font-size: 9.5pt; background-color: white;">=</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">Tablet</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">/&gt;</span> </span> <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt; background-color: white;">
							&lt;!--</span> <span style="font-size: 9.5pt; background-color: white;">Windows 
							Phone 8: Mozilla/5.0 (compatible; MSIE 10.0; Windows 
							NT 6.2; Win64; x64; Trident/6.0; Touch; .NET4.0C; 
							.NET CLR 3.0.30729; .NET CLR 2.0.50727) </span>
 <span style="font-size: 9.5pt; background-color: white;">
							--&gt;</span> </span> <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt; background-color: white;">
							&lt;</span> <span style="font-size: 9.5pt; background-color: white;">agent</span> <span style="font-size: 9.5pt; background-color: white;">contains</span> <span style="font-size: 9.5pt; background-color: white;">=</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">iPhone</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">subfolder</span> <span style="font-size: 9.5pt; background-color: white;">=</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">SmartPhone</span> <span style="font-size: 9.5pt; background-color: white;">"</span> <span style="font-size: 9.5pt; background-color: white;">/&gt;</span> </span> <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt; background-color: white;">
							&lt;!--</span> <span style="font-size: 9.5pt; background-color: white;">Apple 
							iPhone: Mozilla/5.0 (iPhone; U; CPU iPhone OS 4_0 
							like Mac OS X; en-us) AppleWebKit/532.9 (KHTML, like 
							Gecko) Version/4.0.5 Mobile/8A293 Safari/6531.22.7
							</span> <span style="font-size: 9.5pt; background-color: white;">
							--&gt;</span> </span> <span style="font-size: 11pt;">
 <span style="font-size: 9.5pt; background-color: white;">
							&lt;/</span> <span style="font-size: 9.5pt; background-color: white;">RedirectRules</span> <span style="font-size: 9.5pt; background-color: white;">&gt;</span> </span>
Each “Redirect rule” above uses the Browser User-Agent (<a href="http://en.wikipedia.org/wiki/User_agent" target="_blank">http://en.wikipedia.org/wiki/User_agent</a>) with the string expression “contains”, such that if the result is **true** , BTerm will attempt to find the page in the subfolder indicated. If an aspx file is found in the subfolder, that page will be used. If no such file is found, then the page in the root (~/Views) will be used instead.

The User-Agent string is rather long and cryptic. It is intended to be unique, but normally just a few pieces are necessary to identify the device in question. The file above shows typical values of the User-Agent string for different devices as comments. (Comments are ignored by XML )

### Example
The first rule <code class="prettyprint">(&lt;agentcontains="iPad" . . . )</code> will be **true** if the User-Agent string contains the word “iPad”. If the browser requesting the page is a Windows PC running Mozilla Firefox, the value may be <code>“Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.1; Trident/6.0)“</code> and the expression <code>contains="iPad"</code> evaluates to **false** , therefore the subfolder “Tablet” will not be used while searching for the requested Page.

In contrast, if the device requesting the page is an Apple iPad, then the value of the User-Agent will likely be <code>“Apple iPad: Mozilla/5.0 (iPad; U; CPU OS 3_2 like Mac OS X; en-us) AppleWebKit/531.21.10 (KHTML, like Gecko) Version/4.0.4 Mobile/7B334b Safari/531.21.10”</code> and the expression <code>contains="iPad"</code> evaluates to **true,** therefore the subfolder “Tablet” will be used (i.e. Wings will look in ~/Views/Tablet” first for the requested page.

**Note** : The <code>..\App_Data\AlternatePages.config</code> should be adjusted to the Application needs. The implementation of <code>ReadAlternatePagesConfig()</code> should not be changed.

### Configuring
In order to make use of this system, a developer need only create (or more likely copy, then modify) a version of their web page within each of the desired subfolders. 

Adapting a site to best serve mobile users is beyond the scope of this guide, but helpful resources can be found here: <a href="http://designm.ag/tutorials/21-best-websites-for-teaching-yourself-web-development/"> http://designm.ag/tutorials/21-best-websites-for-teaching-yourself-web-development/</a>
