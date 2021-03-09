---
title: XmlInfoEventType Enumeration

Id: dcsXmlInfoEventTypeEnumeration
TocParent: dcsDataGateClientEnumerations
TocOrder: 3

keywords: InfoL1 enumeration member
keywords: InfoL2 enumeration member
keywords: InfoDebug enumeration member
keywords: XmlInfoEventType enumeration
keywords: enumerations [DCS 16.0 XmlInfoEventType
keywords: XML [DCS 16.0 events, feedback type constants
keywords: XML [DCS 16.0 event handler, feedback type constants
keywords: event handlers, feedback type constants

---

<span> **XmlInfoEventType** </span> defines values for the level of information provided when using [ AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethod2.html) and [ IAdgObject.WriteXml](dcsIAdgObjectClassWriteXmlMethod2.html). 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public enum XmlInfoEventType;** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Enum XmlInfoEventType** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegEnum XmlInfoEventType Access(*Public)** 
      </pre>

Remarks

The [XmlInfoEventHandler](dcsXmlInfoEventHandlerDelegate.html) delegate is passed a value of this type, as a field of the [ XmlInfoEventArgs](dcsXmlInfoEventArgsClass.html) object. A program can use this value to discriminate the information provided by **IAdgObject.WriteXml** and **AdgFactory.ReadXml** . 
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col span="1" width="10%" style="FONT-WEIGHT: bold; TEXT-ALIGN: left" />
            <col span="1" width="60%" />
            <col span="1" width="10%" style="TEXT-ALIGN: center" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Member</th>
            <th colspan="1" rowspan="1">
							Description</th>
            <th colspan="1" rowspan="1">
							Value</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

InfoL1 
</td>
            <td colspan="1" rowspan="1">

The information provided is of the most critical level. Events in this class include the verification of XML elements describing the object, database object creation, and skipped duplicate object exceptions. 
</td>
            <td colspan="1" rowspan="1">

1 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

InfoL2 
</td>
            <td colspan="1" rowspan="1">

The information provided is non-critical. Events such as completion of element processing and enumeration of container contents are given at this level. 
</td>
            <td colspan="1" rowspan="1">

2
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

InfoDebug 
</td>
            <td colspan="1" rowspan="1">

The information provided is for system debugging only. This value denotes information useful for development debugging sessions. 
</td>
            <td colspan="1" rowspan="1">

4
</td>
          </tr>
</table>

### Requirements
**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016,Windows 7, Windows 8 Pro, Windows 8.1 Pro Pro

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [AdgFactory.ReadXml Method](dcsAdgFactoryClassReadXmlMethod2.html)
      <br />
      [IAdgObject.WriteXml Method](dcsIAdgObjectClassWriteXmlMethod2.html)
      <br />
      [XmlInfoEventHandler Delegate](dcsXmlInfoEventHandlerDelegate.html)
      <br />
      [XmlInfoEventArgs Class](dcsXmlInfoEventArgsClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

