---
title: AdgFactory.ReadXml Methods

Id: dcsAdgFactoryClassReadXmlMethods
TocParent: dcsAdgFactoryMethods
TocOrder: 3

keywords: AdgFactory.ReadXml methods
keywords: ReadXml methods
keywords: database libraries, create from XML document
keywords: database file members, create from XML document
keywords: database files, create from XML document
keywords: how to, create database libraries from XML document
keywords: how to, create database file members from XML document
keywords: how to, create database files from XML document
keywords: XML [DCS 16.0 documents, create database libraries from
keywords: XML [DCS 16.0 documents, create database file members from
keywords: XML [DCS 16.0 documents, create database files from
keywords: XML [DCS 16.0 database libraries, create from XML document
keywords: XML [DCS 16.0 database file members, create from XML document
keywords: XML [DCS 16.0 database files, create from XML document

---

Creates an instance of [IAdgObject](dcsIAdgObjectClass.html) from an XML document describing a database library, file, or member.
<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 50%" />
            <col span="1" style="WIDTH: 50%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Overload List
						</th>
            <th colspan="1" rowspan="1">
							Description</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[ReadXml(AdgConnection, string, AdgObjectTypes, System.Xml.XmlReader, XmlOptions)](dcsAdgFactoryClassReadXmlMethod1.html).
</td>
            <td colspan="1" rowspan="1">

Returns an instance of an **IAdgObject** (representing a file, library, or member) from an XML document stream based upon the connection, the pathname of a pre-existing database object container for the **IAdgObject** , object type, Xml reader, and output options specified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[ReadXml(AdgConnection, string, AdgObjectTypes, System.Xml.XmlReader, XmlOptions, XmlInfoEventHandler)](dcsAdgFactoryClassReadXmlMethod2.html).
</td>
            <td colspan="1" rowspan="1">

Returns an instance of an **IAdgObject** (representing a file, library, or member) from an XML document stream based upon the connection, the pathname of a pre-existing database object container for the **IAdgObject** , object type, Xml reader, output options, and event handler specified.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[ReadXml(AdgConnection, string, AdgObjectTypes, string, System.Xml.XmlReader, XmlOptions)](dcsAdgFactoryClassReadXmlMethod3.html).
</td>
            <td colspan="1" rowspan="1">

Returns an instance of an **IAdgObject** (representing a file, library, or member) from an XML document stream based upon the connection, the pathname of a pre-existing database object container for the **IAdgObject** , object type, new object name, Xml reader, and output options specified. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[ReadXml (AdgConnection, string, AdgObjectTypes, string, System.Xml.XmlReader, XmlOptions, XmlInfoEventHandler)](dcsAdgFactoryClassReadXmlMethod4.html).
</td>
            <td colspan="1" rowspan="1">

Returns an instance of an **IAdgObject** (representing a file, library, or member) from an XML document stream based upon the connection, the pathname of a pre-existing database object container for the **IAdgObject** , object type, new objectname, Xml reader, output options, and event handler specified.
</td>
          </tr>
</table>

See Also

<dl />
      [AdgFactory Class](dcsAdgFactoryClass.html)
      <br />
      [AdgFactory Members](dcsAdgFactoryMembers.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

