---
title: Configuring iSeries for Bidi

Id: dgConfiguringiSeriesforBidi
TocParent: dgBidirectionalSupport
TocOrder: 63

keywords: DataGate Studio, bidirectional support
keywords: bidirectional text support
keywords: bidirectional text support, iSeries configuration
keywords: iSeries Bidi support
keywords: Configuring the iSeries for Bidi-enabled DataGate Connections
keywords: Configuring DataGate for Bidi-enabled Connections
keywords: Implementing and Configuring an Alternate Server Text Translation Provider

---

By default, DataGate connections do not have bidi support. To enable bidi text transformations, you must select an appropriate bidi "encoding", based on the text to be accessed on the iSeries. On the iSeries, the following factors should influence your selection:

- The CCSID of the file data to be accessed.
- The CCSID of the DataGate/400 job.

Note that on the iSeries, the database implicitly converts character data from the CCSID in which it is stored to the CCSID of the job. If the CCSIDs are the same, or the job CCSID is the special CCSID 65535, no implicit conversion occurs. DataGate/400 cannot control this conversion; therefore **it is the responsibility of the user to ensure that the implicit conversion is valid.** 

Usually, the validity of the database's implicit conversion can be verified by using a "greenscreen" iSeries session to access and render the data. If the data is rendered correctly in the greenscreen, you should use the session's CCSID in the DataGate/400 connection job, unless the session's CCSID is 65535. If the session job's CCSID is 65535, use the CCSID of the stored data for the DataGate/400 connection job.

There are many ways to configure the CCSID of a DataGate/400 job, and enumerating them all is beyond scope here. However, the most common way to specify a DataGate job CCSID is to set the CCSID of the user profile specified in the DataGate database name. The user profile CCSID can be set with the iSeries **CHGUSRPRF** command.

Make note of your selection for the DataGate job CCSID and user profile, since these will be used to configure the bidi encoding of the client connection with DataGate Explorer.

#### Section summary:

- [Alternate Server Text Translation Interface](dgAlternateServerTextTrans.html)
- [Bidi Text Translation](dgBidiTextTranslation.html)
- [Configuring the iSeries for Bidi-enabled DataGate Connections](dgConfiguringiSeriesforBidi.html)
- [Configuring DataGate for Bidi-enabled DataGate Connections](dgConfiguringDataGateforBidi.html)
- [Implementing and Configuring an Alternate Server Text 
	  		Translation Provider](dgAlternateServerTextTranslationProvider.html)

