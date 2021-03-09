---
title: IAdgObject.Schema Property

Id: dcsIAdgObjectClassSchemaProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 14

keywords: Schema property
keywords: IAdgObject.Schema property
keywords: XML schema, validate fragments for database objects
keywords: database objects, XML documents, validate against schema fragments
keywords: XML [DCS 16.0 documents, validate fragments against schema
keywords: XML [DCS 16.0 documents, establish adherence to schema
keywords: XML [DCS 16.0 schema, validate XML document to
keywords: how to, validate XML document against schema

---

**Schema** is the XML schema collection DCS uses to validate XML document fragments describing **IAdgObject** instances and the database objects they represent.
<pre>        <span class="lang">[C#]</span>
 **Public System.Xml.Schema.XmlSchemaCollection Schema { get }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property Schema As System.Xml.Schema.XmlSchemaCollection** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Schema Access(*Public) Type(System.Xml.Schema.XmlSchemaCollection)
   BegGet** 
      </pre>

Property Value

**System.Xml.Schema.XmlSchemaCollection** . The DataGate XML object description schema. 
Remarks

**IAdgObject** instances can be persisted to and from XML documents (see also [AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethods.html) and [IAdgObject.WriteXml](dcsIAdgObjectClassWriteXmlMethods.html)). The **Schema** property references the static collection of XML schema to which these XML documents must adhere. User programs, such as utilities or development tools, may use **Schema** to pre-validate such documents. Note that **AdgFactory.ReadXml** uses **Schema** to validate its XML stream input unless [ XmlOptions.DontValidate](dcsXmlOptionsEnumeration.html) is specified.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [WriteXml Methods](dcsIAdgObjectClassWriteXmlMethods.html)
      <br />
      [AdgFactory.ReadXml Methods](dcsAdgFactoryClassReadXmlMethods.html)
      <br />
      [XmlOptions Enumeration](dcsXmlOptionsEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

