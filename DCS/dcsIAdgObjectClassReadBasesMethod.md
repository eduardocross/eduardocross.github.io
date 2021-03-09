---
title: IAdgObject.ReadBases Method

Id: dcsIAdgObjectClassReadBasesMethod
TocParent: dcsIAdgObjectMethods
TocOrder: 5

keywords: ReadBases method
keywords: IAdgObject.ReadBases method
keywords: database objects, XML documents, set base objects path name
keywords: database objects, XML documents, set base objects description
keywords: base objects description from XML document
keywords: base objects path name from XML document
keywords: how to, set base objects description from XML document
keywords: how to, set base objects path names from XML document
keywords: XML [DCS 16.0 documents, set base objects path names from
keywords: XML [DCS 16.0 documents, set base objects description from
keywords: XML [DCS 16.0 database objects, set base objects path names
keywords: XML [DCS 16.0 database objects, set base objects description
keywords: XML [DCS 16.0 set base objects description from XML document

---

**ReadBases** sets base object information for the **IAdgObject** by reading an XML document fragment.
<pre>        <span class="lang">
 **[C#]** 
        </span> **Public void ReadBases(
   System.Xml.XmlReader reader
);** 
      </pre>

      <pre> **<span class="lang">[Visual Basic] </span>
 public Sub ReadBases(_
   ByVal reader As System.Xml.XmlReader<br /> ) As IAdgObject** 
      </pre>

      <pre class="prettyprint">
 **<span class="lang">[Visual RPG]</span>
 BegSr ReadBases Access(*Public) Type(IAdgObject
   DclSrParm reader Type(System.Xml.XmlReader)** 
      </pre>

Parameters

<dl>
        <dt />
</dl>

*reader* 
<dl>
        <dd>
**System.Xml.XmlReader** . The input stream providing the XML document fragment.
</dd>
</dl>

Exceptions

<table class="dtTABLE" id="Table4" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="30%" style="FONT-WEIGHT: bold" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Exception Type</th>
            <th colspan="1" rowspan="1">
							Condition</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

XmlException
</td>
            <td colspan="1" rowspan="1">

An error occurred validating or loading; the supplied XML fragment.
</td>
          </tr>
</table>

Remarks

**ReadBases** is called by the [ AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethods.html) method to set the base objects description of a new **IAdgObject** instance. This method may be called by user programs to change the base objects description of the **IAdgObject** . Any previously set base objects information is discarded and replaced with the new information. The description includes the path names of the base objects. Note that changing the description of the base objects of an **IAdgObject** instance has no effect on the existing database object it represents, if any. To create a new database object with the new base objects information, use the [Create](dcsIAdgObjectClassCreateMethod.html) method.

The state of *reader* should be such that the next XML content node to be read describes the base objects. Intervening non-content nodes, if any, are ignored. *reader* may reference a stream containing multiple current-level elements, but only the first element will be read and interpreted to set the base object description. The XML fragment read by **ReadBases** is assumed to be valid. An invalid XML fragment or invalid base object description changes the **IAdgObject** instance such that it contains no base object information.
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [Create Method](dcsIAdgObjectClassCreateMethod.html)
      <br />
      [AdgFactory.ReadXml Method](dcsAdgFactoryClassReadXmlMethods.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

