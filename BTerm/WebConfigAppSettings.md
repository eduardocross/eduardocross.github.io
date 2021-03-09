---
title: Web.config

Id: WebConfigAppSettings
TocParent: emComponents
TocOrder: 25

keywords: ASNA Browser Terminal
keywords: Wings
keywords: ASNA Browser Terminal, import message files runtime location
keywords: ASNA Browser Terminal, _Star_LIBL display file search libraries
keywords: ASNA Browser Terminal, Asna5250Terminal.aspx location
keywords: ASNA Browser Terminal, replacement characters for DDS files names
keywords: how to, set import message files runtime location
keywords: how to, set _Star_LIBL display file search libraries
keywords: how to, set Asna5250Terminal.aspx page location
keywords: how to, set replacement characters for DDS file names invalid in ASP.NET 
keywords: importing message files, runtime location
keywords: setting replacement characters for DDS file names invalid in ASP.NET 
keywords: setting _Star_LIBL display files runtime location
keywords: setting Asna5250Terminal.aspx page location
keywords: ASNA Browser Terminal, web.config appSettings
keywords: web.config
keywords: web.config, appSettings
keywords: appSettings
keywords: appSettings, MonarchDspFileLibl
keywords: appSettings, MonarchMsgFileFolder
keywords: appSettings, MonarchSpecialCharReplacement
keywords: appSettings, Asna5250TerminalFolder
keywords: MonarchDspFileLibl
keywords: MonarchMsgFileFolder
keywords: MonarchSpecialCharReplacement
keywords: Asna5250TerminalFolder
keywords: Asna5250TerminalFolder location
keywords: Asna5250Terminal.aspx
keywords: Asna5250Terminal.aspx, location

---

<table>
                <tr>
                    <td>
                        <span class="OH_MultiViewContainerPanelDhtmlTable">
                            ASNA Browser Terminal&#8482; Admin Manual
                        </span>
                    </td>
                </tr>
</table>

# Web.config
<a name="top"></a>

Much of the Browser Terminal's appearance and behavior is defined in its Web.config file. Web.config is an ASP.NET configuration file; It contains data stored as XML text with nested XML tags and sub-tags with attributes that specify configuration settings entered between the &lt;configuration&gt; and &lt;/configuration&gt; XML tags. These configuration settings encompass two areas: section-handler declarations and configuration settings. This topic deals with configuration settings only. 
<!-- end of introduction -->

**Case-Sensitivity** 

The XML tags, sub-tags, and attributes are **well-formed XML** and therefore are case-sensitive. The tag and attribute names must have a lowercase first letter and uppercase on the first letter of any subsequent word(s) i.e. **a** pp **S** ettings. String attribute values have an uppercase first letter and an uppercase first letter of any subsequent word(s) i.e. **M** onarch **M** essage **F** ile **F** older. The only exceptions are **true** and **false** , which are all lowercase letters. 

**appSettings Usage in ASNA Browser Terminal** 

The appSettings section of the Web.config file has the configuration settings for the following: 

- [Terminal Emulation](#terminalfolder">Setting the location of the Asna5250Terminal.aspx page</a>

#### <a name="terminalfolder">Asna5250Terminal.aspx Folder</a>
Asna5250Terminal.aspx page is required whenever DataGate needs to display a 5250 datastream. Monarch redirects to this page using the folder location specified in the Web.config file &lt;appSettings&gt;<span style="color:red;">key</span> <span style="color:blue;">"Asna5250TerminalFolder"</span> <span style="color:red;">value</span>. An example entry for this key is shown highlighted below showing <span style="color:blue;">&quot;~/Themes/Current&quot;</span> as the location for the Asna5250Terminal.aspx page. 
<pre class="prettyprint"><span style="color:blue">&lt;<span style="color:Maroon">appSettings</span><span style="color:red;"> file</span>=<span style="color:black;">"</span>AppSettings.Config<span style="color:black;">"</span>&gt;
    &lt;<span style="color:Maroon">add</span><span style="color:red;"> key</span>=<span style="color:black">"</span>MonarchMessageFileFolder<span style="color:black;">"</span> <span style="color:red;">value</span>=<span style="color:black;">"</span>~\MessageFiles\<span style="color:black;">"</span> /&gt;        
    &lt;<span style="color:Maroon">add</span><span style="color:red;"> key</span>=<span style="color:black">"</span>MonarchSpecialCharReplacements<span style="color:black;">"</span> <span style="color:red;">value</span>=<span style="color:black;">"</span>@=_at_, #=H_lb_, $=_usd_<span style="color:black;">"</span> /&gt;
    &lt;<span style="color:Maroon">add</span><span style="color:red;"> key</span>=<span style="color:black">"</span>MonarchDspFileLibl<span style="color:black;">"</span> <span style="color:red;">value</span>=<span style="color:black;">"</span>MyLibrary, DspFiles/ARlib, Views/*<span style="color:black;">"</span> /&gt;

 **&lt;<span style="color: maroon">add</span> <span style="color: red">key</span>=<span style="color:black;">"</span>Asna5250TerminalFolder<span style="color:black;">"</span> <span style="color: red">value</span>=<span style="color:black;">"</span>~/Themes/Current"/&gt;** &lt;/<span style="color: maroon">appSettings</span>&gt; </span></pre>

The **value** may be one of the following:
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
                        <colgroup>
                            <col width="15%" />
                            <col width="85%" />
                        </colgroup>

                        <tr>
                            <th>value=</th>
                            <th>Description</th>
                        </tr>

                        <tr>
                            <td> *blank*  (or missing)</td>
                            <td>
                                The default location is
                                <span style="color:Red">~Themes\Current</span> - which is relative to the root of your website.
                            </td>
                        </tr>

                        <tr>
                            <td>~</td>
                            <td>The root of the website.</td>
                        </tr>

                        <tr>
                            <td>~\folder\</td>
                            <td>A folder with a relative location with respect to the root of the website.</td>
                        </tr>

                        <tr>
                            <td>absolute folder\</td>
                            <td>
                                A full path including drive designation where
                                Asna5250Terminal.aspx is located.
                            </td>
                        </tr>
</table>

<a href="#top">Return to the top</a>

#### See Also
<dl>
                    <dd>
                        <a href="TerminalEmulation.html)
                    </dd>
</dl>

