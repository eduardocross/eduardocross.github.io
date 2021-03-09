---
title: Bidi Text Translation

Id: dgBidiTextTranslation
TocParent: dgBidirectionalSupport
TocOrder: 62

keywords: bidirectional support
keywords: bidirectional text translation
keywords: bidirectional text translation, about
keywords: hebrew text translation
keywords: Configuring the iSeries for Bidi-enabled DataGate Connections
keywords: Configuring DataGate for Bidi-enabled Connections
keywords: Implementing and Configuring an Alternate Server Text Translation Provider

---

Right-to-left (RTL) text is most often seen in Middle Eastern languages, such as Arabic and Hebrew. Over the years, iSeries users and IBM have adopted conventions for entering and rendering text data, which collectively are inconsistent and complex to manage in the .NET era of Unicode character processing. Particularly difficult for current DataGate users are iSeries database fields containing a mix of RTL and left-to-right (LTR) text, usually referred to as bidirectional text, or simply, "bidi" text.

The DataGate bidi support enhancement consists of the server text translation interface, to be implemented by a bidi "provider." The provider is loaded by the DataGate run-time assembly to translate iSeries EBCDIC text fields to and from Unicode text. The provider will allow bidi text to be used and rendered in DataGate and Visual RPG programs. The character translators implemented by the provider will be configurable, via traditional DataGate "database name" configuration, to specify EBCDIC bidi conventions such as "String Type", and implicit/visual-style transformations.

As part of the enhancement, ASNA will ship its own bidi provider assembly, which will include Unicode transformations for the most common iSeries bidi CCSIDs, as follows:
<table border="1" align="center">
		<tr>
			<th>CCSID</th>
			<th>BidiEncoding Name</th>
		</tr>
		<tr>
			<td>1255</td>
			<td>EBCDIC-CP1255</td>
		</tr>		
		<tr>
			<td>1256</td>
			<td>EBCDIC-CP1256</td>
		</tr>
		<tr>
			<td>420</td>
			<td>EBCDIC-CP420</td>
		</tr>
		<tr>
			<td>424</td>
			<td>EBCDIC-CP424</td>
		</tr>
		<tr>
			<td>856</td>
			<td>EBCDIC-CP856</td>
		</tr>
		<tr>
			<td>862</td>
			<td>EBCDIC-CP862</td>
		</tr>
		<tr>
			<td>864</td>
			<td>EBCDIC-CP864</td>
		</tr>
		<tr>
			<td>1089</td>
			<td>EBCDIC-ISO_8859-6</td>
		</tr>
		<tr>
			<td>916</td>
			<td>EBCDIC-ISO_8859-8</td>
		</tr>
</table>

*Table 1. CCSIDs supported by the ASNA bidi provider.* 

For the above CCSIDs, all string types currently supported by the iSeries will be supported by the ASNA bidi provider. Additionally, advanced users are able, and are encouraged to implement and/or use an alternate bidi provider for other bidi CCSIDs and special data entry conventions. Please see Appendix B for information on implementing and configuring a bidi provider assembly.

*Note that this DataGate bidi support is offered only for the DataGate .NET client. Also, the only tool currently available for configuring a bidi-enabled client connection is DataGate Studio.* 

#### Section summary:

- [Alternate Server Text Translation Interface](dgAlternateServerTextTrans.html)
- [Bidi Text Translation](dgBidiTextTranslation.html)
- [Configuring the iSeries for Bidi-enabled DataGate Connections](dgConfiguringiSeriesforBidi.html)
- [Configuring DataGate for Bidi-enabled DataGate Connections](dgConfiguringDataGateforBidi.html)
- [Implementing and Configuring an Alternate Server Text 
	  		Translation Provider](dgAlternateServerTextTranslationProvider.html)

