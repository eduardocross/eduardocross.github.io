---
title: Instructions to Add Web.config Manually

Id: amfconWebConfigMissingInstructions
TocParent: amfconWebConfigConsiderations
TocOrder: 10

keywords: ASNA.Monarch, webroot
keywords: ASNA.Monarch, web.config considerations
keywords: ASNA.Monarch, configuration files
keywords: ASNA.Monarch, web.config when no IIS
keywords: ASNA.Monarch, creating web.config manually
keywords: concepts, ASNA.Monarch.Webroot
keywords: concepts, ASNA.Monarch.Web.config
keywords: concepts, ASNA.Monarch.Web.config without IIS
keywords: concepts, ASNA.Monarch creating Web.config manually
keywords: concepts, ASNA.Monarch appSettings.config
keywords: concepts, ASNA.Monarch.Webroot
keywords: concepts, Web.config
keywords: concepts, Web.config without IIS
keywords: concepts, creating Web.config manually
keywords: concepts, appSettings.config
keywords: IIS, and ASNA Monarch
keywords: how to, add web.config without IIS
keywords: webroot
keywords: web.config
keywords: web.config configuration file
keywords: web.config, without IIS
keywords: web.config, creating
keywords: web.config, adding manually
keywords: web.config, missing
keywords: creating web.config manually
keywords: application settings
keywords: appSettings.config
keywords: appSettings.config, considerations
keywords: appSettings.config, adding reference manually
keywords: considerations for web.config
keywords: considerations, appSettings.config
keywords: considerations, web.config
keywords: considerations, webroot

---

This topic provides the basic instructions on how to add the Web.config file to your WebSite projects. This topic covers the configuration settings as needed ONLY for ASNA Monarch. 

When migrating a GamePlan and IIS is **not** installed, you will receive the message shown below in your Log Panel. When this occurs you will need to manually add the Web.config file to your solution.
<pre class="syntax"> PM Writing Web.Config
6:33:28 PM **Failed to write Web.Config: IIS is not installed; Cocoon is not able to generate
Web.Config file automatically. Please refer to Help on how to add it manually.** 
6:33:30 PM ** End Task ** Migrating GamePlan</pre>

#### Add the Web.config File
**Start the Debugger** 

Start the application debugger by selecting ***Debugger** --&gt; **Start Debugging*** from the toolbar menu or pressing ** *F5* ** . Visual Studio will notice that there is not a Web.config associated with the web site and will ask if you want to add a default file. Respond &quot;yes&quot;.

**Use ASP.NET Configuration Manager** 

Select &quot; ***ASP.NET Configuration*** &quot; from the Website drop-down menu to add the Web.config file. (If *Website* does not appear on the toolbar, select any file or node in the &quot;Web&quot; section in the solution explorer window.) More detail can be found within Visual Studio while using this tool.

**Use standardized Web.config file** 

Your systems administrator may want to ensure standardized settings to support Monarch as well as other settings that may be unique to your web environment that are not addressed here. Creating a standard Web.config file for ASNA Monarch applications would support standards and eliminate the necessity of creating this file from scratch for each application.

If a standard Web.config is used, you still need to add this file to your solution. Select &quot; ** *Add Existing Item* ** &quot; from the solution explorer menu, browse to the location of your standard Web.config and select the file.

**Add ASNA Monarch References:** 

You will need to add references for the ASNA Monarch assemblies. Select &quot; ** *Add Reference* ** &quot; from the solution explorer window.

**Select .NET Components** 

The **Select Component** dialog will display. From the .NET tab, ** *Add* ** the three ASNA components highlighted in the image below, then select ** *OK* ** . This will update the &lt;assemblies&gt; section of the Web.config file.
<dl><dd>![](images/zzwebaddrefimage2.bmp)</dd></dl>

#### Update Application Settings
If the <code> **AppSettings.Config** </code> file is used to establish function key settings, the &lt;appSettings&gt; section of the Web.config file needs to be updated as follows:
<pre class="example">&lt;appSettings **file=&quot;AppSettings.Config&quot;**  &gt;</pre>

If Message files are used in the website, then the location of these files must be established as the value for the MonarchMessageFileFolder key in appSettings.
<pre class="example"> **&lt;add key=&quot;MonarchMessageFileFolder&quot; value=&quot;C:\Monarch\MsgFiles\&quot; /&gt;** </pre>

**Note:** The value for **&quot;MonarchMessageFileFolder&quot;** allows the use of the symbol &quot;~&quot;, as in **value=&quot;~\Monarch\MsgFiles\&quot;** to specify the website &quot;root&quot; and make this a relative reference instead of an absolute path location.

#### Add Monarch File Overrides
If you use file overrides on the job level, you&#39;ll need to update the <code>&lt;MonarchFileOverrides&gt;</code>. During execution of the application, these entries will direct Monarch Framework to locate the aspx in the given folder.
<pre class="example">&lt;MonarchFileOverrides&gt;
	&lt;add key=&quot;LOGONDF&quot; value=&quot;ToFile=./pages/Logondf.aspx&quot;/&gt;
&lt;/MonarchFileOverrides&gt;</pre>

**Save the <code>Web.config</code> File** 

Save all files in the solution and then close and re-open the solution to activate the settings.

#### <code>Web.config</code> File Sample
A partial sample of a Web.config file is provided below with the red text shown as it pertains to this topic. Note in the &lt;assemblies&gt; section that the **Version** and **PublicKeyToken** values will vary depending on your installed versions of those three assemblies.

#### Using WebRoot
This special folder is provided as a method to allow any files and sub-folders it contains to be copied directly into the web root of your Visual Studio solutions. This folder may contain master pages, images, cascading style sheets, site map pages. 

The WebRoot folder is set up similarly to templates in that you create a new WebRoot folder paralleling the originally installed WebRoot folder and also set the *Agent&#39;s templates root path* in the migration directive to your templates location.

However, there is one major exception. **The installed WebRoot folder and your new WebRoot folder are mutually exclusive** . If there is a WebRoot folder in the *Agent&#39;s templates root path* , the **entire contents** are copied to the web root of your solution; otherwise, the WebRoot installation folder contents are copied. The contents are **NOT** combined.

If you want to use WebRoot:

- Optionally, copy the entire contents of the installed 
					WebRoot folder to the *Agent&#39;s templates root path* 
					location if you want to use any of the installed files.
- Add any additional files.
- Make any changes to any existing templates and/or master pages 
				files you may have copied from those installed.
- Set the *Agent&#39;s templates root path*  in the 
					migration directive to the location of the templates as 
					previously noted above.

**Example:** 

The following figure shows the *MyTemplates\WebRoot* folder to be copied into the web root of the Visual Studio solution provided *Agent&#39;s templates root path* is set to *C:\MyTemplates* .
<dl><dd>![](Images/zzimage6.jpg)</dd></dl>

#### Next: [Web Server Controls Overview](amfWebServerControlsOverview.html)

#### Previous: [Web.config Considerations](amfconWebConfigConsiderations.html)

#### See Also
<dl><dd>[Monarch Migration Style 
			Sheets and Templates](amfMoreAboutStyleSheets.html)</dd>
</dl>

