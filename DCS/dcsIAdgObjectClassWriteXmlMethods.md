---
title: IAdgObject.WriteXml Methods

Id: dcsIAdgObjectClassWriteXmlMethods
TocParent: dcsIAdgObjectMethods
TocOrder: 12

keywords: IAdgObject.WriteXml methods
keywords: WriteXml method
keywords: how to, create XML document fragment for database objects
keywords: XML [DCS 16.0 documents, create fragment for database objects
keywords: XML [DCS 16.0 database objects, create fragment for

---

**WriteXml** produces an XML document fragment representing the [IAdgObject](dcsIAdgObjectClass.html) instance. Such a document can subsequently be used to create a new **IAdgObject** instance with the [AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethods.html) method. Optionally, the document may also describe a hierarchy of database objects contained by the object (file or library) represented by the **IAdgObject** . A monitor delegate may be specified for observing the progress of the method. 
<br />

<table class="dtTABLE" id="table2" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="WIDTH: 50%" />
            <col span="1" style="WIDTH: 50%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Overload List</th>
            <th colspan="1" rowspan="1">
							Description</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[WriteXml(System.Xml.XmlReader, XmlOptions)](dcsIAdgObjectClassWriteXmlMethod1.html) 
</td>
            <td colspan="1" rowspan="1">

Produces an XML document fragment representing the **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[ WriteXml(System.Xml.XmlReader, XmlOptions, XmlInfoEventHandler)](dcsIAdgObjectClassWriteXmlMethod2.html) 
</td>
            <td colspan="1" rowspan="1">

Produces an XML document fragment representing the **IAdgObject** providing a delegate parameter for monitoring the method's progress.
</td>
          </tr>
</table>

See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [IAdgObject Class Members](dcsIAdgObjectMembers.html)
      <br />
      [AdgFactory.ReadXml Method](dcsAdgFactoryClassReadXmlMethods.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

