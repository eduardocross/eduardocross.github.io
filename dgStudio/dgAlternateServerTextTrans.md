---
title: Alternate Server Text Translation Interface

Id: dgAlternateServerTextTrans
TocParent: dgBidirectionalSupport
TocOrder: 61

keywords: DataGate Studio, bidirectional support
keywords: bidirectional text support
keywords: bidirectional text support, about
keywords: Alternate server text
keywords: Alternate Server Text Translation Interface
keywords: Configuring DataGate for Bidi-enabled Connections
keywords: Implementing and Configuring an Alternate Server Text Translation Provider

---

This release of DataGate for .NET will feature a new library interface, which is designed to allow ASNA and its users create custom server text translators, by implementing subclasses of the .NET Framework's **System.Text.Encoding** class and associated classes. Currently, DataGate relies on the database server to provide a reasonable translation of character fields to and from Unicode.

In extraordinary cases, such as iSeries-based bidirectional text, the database server is not able to evoke reliable translations. For these cases, the server text translation interfaces provide an alternative, client-based, plug-in capability to replace the standard DataGate Unicode translation.

These custom text translators will be loaded, via application configuration, by the **ASNA.DataGate.Client** library. Users will be able to associate a text encoding name, and other custom translator settings, with a registered [database name](dgWorkingwithDatabaseNamesMain.html), or SourceProfile object. DataGate Studio will support the configuration of the custom translator in the [Advanced connections properties](dgAdvancedConnectionProperties.html) dialog of the DataGate Explorer tool. The section on [Implementing and Configuring an Alternate Server Text Translation Provider](dgAlternateServerTextTranslationProvider.html) explains the interface in full detail.

#### Section summary:

- [Alternate Server Text Translation Interface](dgAlternateServerTextTrans.html)
- [Bidi Text Translation](dgBidiTextTranslation.html)
- [Configuring the iSeries for Bidi-enabled DataGate Connections](dgConfiguringiSeriesforBidi.html)
- [Configuring DataGate for Bidi-enabled DataGate Connections](dgConfiguringDataGateforBidi.html)
- [Implementing and Configuring an Alternate Server Text 
	  		Translation Provider](dgAlternateServerTextTranslationProvider.html)

