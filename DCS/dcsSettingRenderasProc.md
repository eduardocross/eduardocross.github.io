---
title: Render-in-Process Options

Id: dcsSettingRenderasProc
TocParent: dcsAccessingaFileMain
TocOrder: 20

keywords: Render In Process
keywords: Render in Proc
keywords: ASP.NET Impersonation bug
keywords: Rendering

---

Occasionally the requirement to run the application with asp.net "impersonation" may arise, and in this case the IIS7 worker process starts a thread which runs under the credentials of the impersonated user. This is similar too, but slightly different than, logging onto the Windows workstation with the same credentials. In particular, when the worker process is running as the "Network Service" identity (as per default IIS7 configuration), the impersonation thread is not allowed to create new processes with the same authority as a logged-on user with its credentials. 

This can create an issue because DataGate client performs Windows printing functions by generating a "meta-file" containing Windows-specific generic printing information. The renderer uses this meta-file to perform the actual printing. By default the client starts the renderer as a separate process. This process must load the print file controls assembly in order to print the contents of the print file's fields. In the scenario described in the previous paragraph however, the renderer fails to load the controls assembly: The load fails because of a requirement for that assembly to access the WinForms subsystem of .NET; the Network Service identity of the parent process is inherited by the renderer's process, and Window2008R2 does not allow that identity to access UI facilities. 

To resolve this issue, DataGate can be instructed to Render-in-Proc, rather than as a seperate process. Doing so involves adding the following code to the .config file for the application, website, or machine (application.config, web.config, or machine.config) where Render-in-Proc is to be used.
<pre>&lt;configuration&gt;
    &lt;configSections&gt;
        &lt;sectionGroup name="applicationSettings" type="System.Configuration.ApplicationSettingsGroup, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" &gt;
            &lt;section name="ASNA.DataGate.Client.Properties.PrintingProps" type="System.Configuration.ClientSettingsSection, System, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" requirePermission="false" /&gt;
        &lt;/sectionGroup&gt;
    &lt;/configSections&gt;
    &lt;applicationSettings&gt;
        &lt;ASNA.DataGate.Client.Properties.PrintingProps&gt;
            &lt;setting name="RenderInProc" serializeAs="String"&gt;
                &lt;value&gt;True&lt;/value&gt;
            &lt;/setting&gt;
        &lt;/ASNA.DataGate.Client.Properties.PrintingProps&gt;
    &lt;/applicationSettings&gt;
&lt;/configuration&gt;
			</pre>

<span style="color: rgb(0, 0, 0); font-family: Verdana, Helvetica, Arial, sans-serif; font-size: 14px; font-style: normal; font-variant: normal; font-weight: normal; letter-spacing: normal; line-height: normal; orphans: 2; text-align: -webkit-auto; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; word-spacing: 0px; -webkit-text-size-adjust: auto; -webkit-text-stroke-width: 0px; background-color: rgb(251, 251, 251); display: inline !important; float: none; "> To disable render-in-process, either remove the above, or change the content of the &lt;setting name="RenderInProc"&gt; element to "&lt;value&gt;False&lt;/value&gt;".</span>
See Also

<dl />
		[AdgDataSet Class](dcsAdgDataSetClass.html)<br />
		[Database File Records and AdgDataSet](dcsDatabaseFileRecordsandAdgDataSet.html)<br />
		[Efficient File Access](dcsEfficientFileAccess.html)<br />
		[FileAdapter Class](dcsFileAdapterClass.html)<br />
		[Reading and Writing to Database Files](dcsReadingandWritingtoDatabaseFiles.html)<br />
		[Using the FileAdapter Class](dcsUsingtheFileAdapterClass.html)   

