---
title: Implementing and Configuring an Alternate Server Text Translation Provider

Id: dgAlternateServerTextTranslationProvider
TocParent: dgBidirectionalSupport
TocOrder: 65

keywords: DataGate Studio, bidirectional support
keywords: bidirectional text support
keywords: bidirectional text support, about
keywords: hebrew text support
keywords: Configuring the iSeries for Bidi-enabled DataGate Connections
keywords: Configuring DataGate for Bidi-enabled Connections
keywords: Implementing and Configuring an Alternate Server Text Translation Provider

---

This document assumes that the reader has at least a basic understanding of XML and the use of .NET configuration files. For a thorough introduction to .NET configuration files, please consult the Configuration Files topics in the .NET framework documentation.

To configure your DataGate application to use the Bidi plug-in (or any other alternate encoding engine), the .NET configuration file must contain an &#60;applicationSettings&#62; element referring to the factory class' assembly-qualified name. For example, the following is a .NET application configuration file containing only the elements required to configure the plug-in.

Note that some of these elements may already be present in an existing configuration, but the &#60;ASNA.DataGate.Client.Properties.AltEncodingProps&#62; element must be unique in the file.
<pre class="prettyprint">
&#60;?xml version ="1.0"?&#62;
&#60;configuration&#62;
	&#60;configSections&#62;
		&#60;sectionGroup name="applicationSettings"
			type="System.Configuration.ApplicationSettingsGroup, System,
			Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" &#62;
			&#60;section
				name="ASNA.DataGate.Client.Properties.AltEncodingProps"
				type="System.Configuration.ClientSettingsSection, System,
				Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"
				requirePermission="false" /&#62;
		&#60;/sectionGroup&#62;
	&#60;/configSections&#62;
	&#60;applicationSettings&#62;
		&#60;ASNA.DataGate.Client.Properties.AltEncodingProps&#62;
			&#60;setting name="EncodingFactoryImpl" serializeAs="String"&#62;
				&#60;value&#62;
					ASNA.DataGate.DataLink.Bidi.EncodingFactory,
					ASNA.DataGate.DataLink.Bidi, Version=9.1.0.0, Culture=neutral,
					PublicKeyToken=f1b0bf4120ba8afa
				&#60;/value&#62;
			&#60;/setting&#62;
		&#60;/ASNA.DataGate.Client.Properties.AltEncodingProps&#62;
	&#60;/applicationSettings&#62;
&#60;/configuration&#62;
</pre>

To apply these settings to all DataGate programs that run on the computer, you can merge the above settings into the " **machine.config** " file. Machine.config can be found in the **%runtime install path%\Config** directory, where %runtime install path% is the directory containing the version of the .NET framework in use. For the .NET 2.0 framework, this directory is typically " **C:\Windows\Microsoft.NET\Framework\v2.0.50727\Config** ".

*Before editing machine.config, make a backup copy. Use **extreme caution** when editing machine.config; as the settings here affect **all .NET applications** on the computer.* 

Note that machine.config already contains a &#60;configSections&#62; element, but that you will probably need to add the &#60;sectionGroup&#62; element above (and its child elements), as a child of &#60;configSections&#62;. If it already exists in machine.config, add the above &#60;section&#62; element to it as a child.

Likewise, add the &#60;applicationSettings&#62; element above (and its children) to the &#60;configuration&#62; element of machine config, unless it already exists as a **System.Configuration.ApplicationSettingsGroup** type. If &#60;applicationSettings&#62; already exists, add the &#60;ASNA.DataGate.Client.Properties.AltEncodingProps&#62; element above (and its children) to it.

If another &#60;applicationSettings&#62; element already exists in machine.config, but does not have 'type="System.Configuration.ApplicationSettingsGroup…', then give the above &#60;applicationSettings&#62; element a different name; such as &#60;applicationSettingsForASNA&#62;.

The following listing is an example of a name collision with a pre-existing &#60;applicationSettings&#62; element that is resolved by renaming the ASNA element. Omitted portions of machine.config are denoted below by the "…" ellipsis:
<!--Exampleimg goes here-->
<pre class="prettyprint">
&#60;?xml version ="1.0"?&#62;
&#60;configuration&#62;
	&#60;configSections&#62;
	…
		&#60;sectionGroup name="applicationSettings"
			type="SomeOtherApp.SettingsGroup, SomeOtherApp, Version=1.0.0.0" &#62;
	…
		&#60;/sectionGroup&#62;
	…
		&#60;sectionGroup name="applicationSettingsForASNA"
			type="System.Configuration.ApplicationSettingsGroup, System,
			Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089" &#62;
			&#60;section
			name="ASNA.DataGate.Client.Properties.AltEncodingProps"
			type="System.Configuration.ClientSettingsSection, System,
			Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"
			requirePermission="false" /&#62;
		&#60;/sectionGroup&#62;
	&#60;/configSections&#62;
	…
	&#60;applicationSettingsForASNA&#62;
		&#60;ASNA.DataGate.Client.Properties.AltEncodingProps&#62;
			&#60;setting name="EncodingFactoryImpl" serializeAs="String"&#62;
				&#60;value&#62;
					ASNA.DataGate.DataLink.Bidi.EncodingFactory,
					ASNA.DataGate.DataLink.Bidi, Version=9.1.0.0, Culture=neutral,
					PublicKeyToken=f1b0bf4120ba8afa
				&#60;/value&#62;
			&#60;/setting&#62;
		&#60;/ASNA.DataGate.Client.Properties.AltEncodingProps&#62;
	&#60;/applicationSettingsForASNA&#62;
	…
&#60;/configuration&#62;
</pre>

To specify that a different encoding engine be used, say for a new version of &#60;b&#62;ASNA.DataGate.DataLink.Bidi&#60;/b&#62;, the only change required to the above configuration is the text content of the &#60;value&#62; element.

#### Section summary:

- [Alternate Server Text Translation Interface](dgAlternateServerTextTrans.html)
- [Bidi Text Translation](dgBidiTextTranslation.html)
- [Configuring the iSeries for Bidi-enabled DataGate Connections](dgConfiguringiSeriesforBidi.html)
- [Configuring DataGate for Bidi-enabled DataGate Connections](dgConfiguringDataGateforBidi.html)
- [Implementing and Configuring an Alternate Server Text 
	  		Translation Provider](dgAlternateServerTextTranslationProvider.html)

