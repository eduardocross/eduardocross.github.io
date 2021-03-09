---
title: XmlInfoEventArgs Class

Id: dcsXmlInfoEventArgsClass
TocParent: dcsASNADataGateClientClasses
TocOrder: 15

keywords: classes [DCS 16.0 XmlInfoEventArgs class
keywords: XmlInfoEventArgs class
keywords: XmlInfoEventArgs class, about XmlInfoEventArgs class
keywords: XML [DCS 16.0 events, about reporting feedback
keywords: XML [DCS 16.0 event handler, object
keywords: event handlers, about using

---

An **XmlInfoEventArgs** object contains the details of events reported by the [ AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethod2.html) and [IAdgObject.WriteXml](dcsIAdgObjectClassWriteXmlMethod2.html) methods, through the **** [XmlInfoEventHandler](dcsXmlInfoEventHandlerDelegate.html) delegate. 

For a list of all members of this type, see [ XmlInfoEventArgs Members](dcsXmlInfoEventArgsMembers.html).

[ASNA.DataGate.Client](dcsDataGateClientNamespace.html) <br /> **ASNA.DataGate.Client.<span>XmlInfoEventArgs</span>** 
<pre class="syntax">
        <span class="lang">[Prototype in C#]</span>
        <span>
public class XmlInfoEventArgs | inherits System.EventArgs</span>
      </pre>

Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
Remarks

**XmlInfoEventArgs** is defined for use as a parameter of the XmlInfoEventHandler delegate. The parameter reports a single event status in a DCS XML method.

The [Message](dcsXmlInfoEventArgsClassMessageField.html) field contains a string message providing some detail of the event. The [ Type](dcsXmlInfoEventArgsClassTypeField.html) field classifies the event (see [ XmlInfoEventType](dcsXmlInfoEventTypeEnumeration.html)).
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [XmlInfoEventArgs Members](dcsXmlInfoEventArgsMembers.html)
      <br />
      [XmlInfoEventType Enumeration](dcsXmlInfoEventTypeEnumeration.html) <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

