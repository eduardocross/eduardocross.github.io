---
title: Configuring Datagate for Bidi

Id: dgConfiguringDataGateforBidi
TocParent: dgBidirectionalSupport
TocOrder: 64

keywords: DataGate Studio, bidirectional support
keywords: bidirectional text support
keywords: bidirectional text support, about
keywords: hebrew text support
keywords: Configuring the iSeries for Bidi-enabled DataGate Connections
keywords: Configuring DataGate for Bidi-enabled Connections
keywords: Implementing and Configuring an Alternate Server Text Translation Provider

---

To enable the client for bidi support, you must configure the DataGate connection profile, using the source profile configuration dialog window in DataGate Studio. This dialog, shown, is accessible via the DataGate Explorer tool, with the [Modify Connection](dgModifyingaConnection.html) command on a Connections node, or the **Edit Properties.** command on a Database Names node.

In this example, the user "dwarner" is selected as the iSeries user profile configured to use a bidi CCSID. Here we assume that this profile will be used to configure the DataGate/400 job CCSID (as outlined in the previous section).

The bidi configuration properties for a connection are accessed by clicking the "Advanced…" button on the dialog. This will display a second dialog ([Advanced Connection Properties](dgAdvancedConnectionProperties.html)), containing a property grid control which includes the bidi configuration properties, as shown in Figure 1.
![" align="middle](../images/dgCustomTextTrans.bmp)

*Figure 1. By default, no alternate text conversion is configured, as shown by the "Unicode" property value for the "Server Text Encoding" property.* 

To select the text encoding representing the bidi CCSID of the DataGate/400 job, click the drop-down button on the cell to the right of the Server Text Encoding property. This will display the encodings available from the provider assembly. The ASNA bidi provider will provide the encodings listed in Table 1, and these will be shown in the drop-down list. Select the encoding name from Table 1 that matches the DataGate/400 job CCSID shown in the table's CCSID column.

As an example, suppose that the "dwarner" user profile we're working with is configured to use CCSID 424. We would therefore select "EBCDIC-CP424" for the Server Text Encoding property. Selecting a valid encoding name will enable the Decoder and Encoder properties.

After selecting the encoding, you should review and update the properties effecting the interpretation of bidi data stored in the database. The Decoder and Encoder fields contain these properties. Expand the properties by clicking the "+" widget to the left of the fields. The Decoder properties effect the translation from EBCDIC to Unicode (that is, the translation of text stored in the database to Unicode as used in DataGate programs). Encoder properties effect translations in the opposite direction: Unicode to EBCDIC.

You can enlarge the dialog to show all the properties for Decoder by clicking and dragging the "size grip" control in the lower-right corner of the dialog window).

In our example, two properties are changed: String Type and Insert Marks (for a complete explanation of the properties of the ASNA bidi provider's Decoder and Encoder, see [ Implementing and Configuring an Alternate Server Text Translation Provider](dgAlternateServerTextTranslationProvider.html)). The String Type has been changed from "DEFAULT" to ST4, and the Insert Marks property is enabled.

Likewise, the Encoder must be configured. The properties of Encoder are identical to those of Decoder, but the values are not. In some cases, a characteristic of a transformation result of Decoder should be accounted for by the Encoder. In this example, text transformed by Decoder's enabled Insert Marks property may include special Unicode characters called "direction marks". So the configuration in Figure 2 enables the Remove Marks property so that direction mark characters affected the transformation from Unicode to EBCDIC, but are not included in the result.
![" align="middle](../images/dgRemovemarks.bmp)

*Figure 2. Remove Marks is enabled in the Encoder, so that text obtained through the Decoder will have the direction marks removed when converting back to EBCDIC.* 

#### Section summary:

- [Alternate Server Text Translation Interface](dgAlternateServerTextTrans.html)
- [Bidi Text Translation](dgBidiTextTranslation.html)
- [Configuring the iSeries for Bidi-enabled DataGate Connections](dgConfiguringiSeriesforBidi.html)
- [Configuring DataGate for Bidi-enabled DataGate Connections](dgConfiguringDataGateforBidi.html)
- [Implementing and Configuring an Alternate Server Text 
	  		Translation Provider](dgAlternateServerTextTranslationProvider.html)

