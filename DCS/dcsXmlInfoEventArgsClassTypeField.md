---
title: XmlInfoEventArgs.Type Field

Id: dcsXmlInfoEventArgsClassTypeField
TocParent: dcsXmlInfoEventArgsFields
TocOrder: 1

keywords: Type field
keywords: XmlInfoEventArgs.Type field
keywords: XmlInfoEventType enumeration, used by
keywords: enumerations [DCS 16.0 XmlInfoEventType, used by
keywords: XML [DCS 16.0 events, feedback type
keywords: XML [DCS 16.0 event handler, feedback type
keywords: event handlers, feedback type

---

The **Type** field denotes the type of event being reported.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public [XmlInfoEventType](dcsXmlInfoEventTypeEnumeration.html) Type** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Shared Property Type As [XmlInfoEventType](dcsXmlInfoEventTypeEnumeration.html)** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp Type Type([XmlInfoEventType](dcsXmlInfoEventTypeEnumeration.html)) Access(*Public) Shared(*Yes)** 
      </pre>

Field Value

[XmlInfoEventType](dcsXmlInfoEventTypeEnumeration.html). The type of event being reported. Valid values are defined by the **XmlInfoEventType** enumeration
Remarks

The **Type** field allows a consumer of XML event information to more easily discriminate that information. For example, a program ciykd produce separate logs of events based on the value of **Type** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [XmlInfoEventArgs Class](dcsXmlInfoEventArgsClass.html)
      <br />
      [XmlInfoEventArgs Members](dcsXmlInfoEventArgsMembers.html)
      <br />
      [XmlInfoEventType Enumeration](dcsXmlInfoEventTypeEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

