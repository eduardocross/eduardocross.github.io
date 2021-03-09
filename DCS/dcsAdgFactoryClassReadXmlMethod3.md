---
title: ReadXml(AdgConnection, string, AdgObjectTypes, string, System.Xml.XmlReader, XmlOptions)

Id: dcsAdgFactoryClassReadXmlMethod3
TocParent: dcsAdgFactoryClassReadXmlMethods
TocOrder: 2

keywords: AdgObjectTypes enumeration, used by
keywords: XmlOptions enumeration, used by
keywords: enumerations [DCS for VS 2005], AdgObjectTypes, used by
keywords: enumerations [DCS for VS 2005], XmlOptions, used by

---

This **ReadXml** method returns an instance of an [IAdgObject](dcsIAdgObjectClass.html) (representing a file, library, or member) from an XML document stream. Optionally, **ReadXml** creates a new database object or a hierarchy of database objects.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public static IAdgObject ReadXml(
   [AdgConnection](dcsAdgConnectionClass.html) cn ,
   string containerPath ,
   [AdgObjectTypes](dcsAdgObjectTypesEnumeration.html) docObjectType ,    
   string docObjectNewName ,    
   System.Xml.XmlReader reader ,
   [XmlOptions](dcsXmlOptionsEnumeration.html) options
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub ReadXml( _
   ByVal cn As [AdgConnection](dcsAdgConnectionClass.html) _<br />   ByVal containerPath As string _
   ByVal docObjectType As <a ref="dcsAdgObjectTypesEnumeration.htm">AdgObjectTypes</a> _
   ByVal docObjectNewName As string _
   ByVal reader As System.Xml.XmlReader _
   ByVal options As [XmlOptions](dcsXmlOptionsEnumeration.html)
   ) As IAdgObject** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr ReadXml Access(*Public) Type(IAdgObject)
   DclSrParm cn Type([AdgConnection](dcsAdgConnectionClass.html))
   DclSrParm containerPath Type(*string)
   DclSrParm docObjectType Type([AdgObjectTypes](dcsAdgObjectTypesEnumeration.html))
   DclSrParm docObjectNewName Type(*string)
   DclSrParm reader Type(System.Xml.XmlReader)
   DclSrParm options Type([XmlOptions](dcsXmlOptionsEnumeration.html))** 
      </pre>

Parameters

<dl>
        <dt>
 *cn* 
        </dt>
        <dd>

An instance of the [AdgConnection](dcsAdgConnectionClass.html) class representing a database connection to the server.
</dd>
        <dt>
 *containerPath* 
        </dt>
        <dd>

String. The pathname of a pre-existing database object container for the [ IAdgObject](dcsIAdgObjectClass.html) to be created by this method.
</dd>
        <dt>
 *docObjectType* 
        </dt>
        <dd>

[AdgObjectTypes](dcsAdgObjectTypesEnumeration.html). Used to specify the database object type to be created. This value is used to validate the XML description of the database object.
</dd>
        <dt>
 *docObjectNewName* 
        </dt>
        <dd>

String containing the new name of the database object.
</dd>
        <dt>
 *reader* 
        </dt>
        <dd>

**System.Xml.XmlReader** . The input stream positioned at the beginning of the XML description of the database object **.** 
</dd>
        <dt>
 *options* 
        </dt>
        <dd>

[XmlOptions](dcsXmlOptionsEnumeration.html). Input options for interpreting the XML description and creating the IAdgObject. Valid values are defined by the **XmlOptions** Enumeration.
</dd>
</dl>

Returns

A new instance of **IAdgObject** . The underlying type of the **IAdgObject** instance is determined by the value of the *docObjectType* parameter, as given in the following table: 
<table class="dtTABLE" id="Table4" style="border-spacing: 0px; x-cell-content-align: Top" height="0" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" valign="top" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value of *docObjectType* </th>
            <th colspan="1" rowspan="1">
							Type of **IAdgObject**  returned by **ReadXml** </th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Directory 
</td>
            <td colspan="1" rowspan="1">

[IDirectory](dcsIDirectoryClass.html) 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

File
</td>
            <td colspan="1" rowspan="1">

[IFileObject](dcsIFileObjectClass.html) 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Member
</td>
            <td colspan="1" rowspan="1">

[IMember](dcsIMemberClass.html) 
</td>
          </tr>
</table>

Exceptions

<table class="dtTABLE" id="Table2" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" style="FONT-WEIGHT: bold" width="30%" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							ExceptionType</th>
            <th colspan="1" rowspan="1">
							Condition</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NullReferenceException 
</td>
            <td colspan="1" rowspan="1">

The *cn* and/or *containerPath* parameters are null references. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

XmlSchemaException
</td>
            <td colspan="1" rowspan="1">

An error occurred validating the DataGate XML schema.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

XmlException
</td>
            <td colspan="1" rowspan="1">

An error occurred validating or loading the supplied XML document fragment.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgException 
</td>
            <td colspan="1" rowspan="1">

See table below. 
</td>
          </tr>
</table>

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" style="FONT-WEIGHT: bold" width="20%" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Member</th>
            <th colspan="1" rowspan="1">
							Description</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG 
</td>
            <td colspan="1" rowspan="1">

**ReadXml** is not supported for the supplied value of *docObjectType* . 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgErBADSRC
</td>
            <td colspan="1" rowspan="1">

An attempt to create a logical database file failed because no valid base files were specified in the file definition. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINVSQLOP 
</td>
            <td colspan="1" rowspan="1">

The **AdgConnection** specified is a connection to an SQL Server database provider, and DCS currently does not support the **IAdgObject** interface for the type specified by *docObjectType* for those providers. 
</td>
          </tr>
</table>

<br />

Remarks

[IAdgObject](dcsIAdgObjectClass.html) instances can be persisted to and from XML documents (see also [IAdgObject.WriteXml](dcsIAdgObjectClassWriteXmlMethods.html)). **ReadXml** interprets such an XML document, and if valid, returns a new **IAdgObject** instance. 

Additionally, **ReadXml** can create a hierarchy of **IAdgObject** instances. For example, the XML document may describe a database library and its contents. **ReadXml** will return an **IAdgObject** which is an instance of **IDirectory** for such a document. Further, **ReadXml** can read this document such that the returned **IDirectory** 's [Enumerate](dcsIDirectoryClassEnumerateMethod.html) method would access **IAdgObject** instances (describing objects in the library) concurrently created in the **ReadXml** call. Another option (specified by the bit-set value of *options* ) directs **ReadXml** to create the new database objects (in the database specified by *cn* ) as the **IAdgObjects** are created from the XML stream. Other bits in *options* allow the creation of contained **IAdgObjects** to be discriminated by object type (see [ XmlOptions](dcsXmlOptionsEnumeration.html)).

When **ReadXml** successfully returns an **IAdgObject** instance, the instance's [ToString](dcsIAdgObjectClassToStringMethod.html) method will return a path name consisting of the name of the database object (described in the XML document) appended to the value of *containerPath* . 

The value of *docObjectType* must match the object type given in the document, or a validation error will occur. 

The state of *reader* should be such that the next content node to be read describes the **IAdgObject** instance to be created. Intervening non-content nodes, if any, are ignored. *reader* may reference a document containing multiple, top-level elements describing **IAdgObjects** , but only the first occurrence will be used to create the returned **IAdgObject** . Note however that the top-level element read may define an object container (such as a library or file), and embed elements describing objects it contains. **ReadXml** can also process and create **IAdgObject** instances for these contained objects (see **XmlOptions** ).

For large XML documents, **ReadXml** may create many objects. In this case, consider using the overloaded version of [ ReadXml](dcsAdgFactoryClassReadXmlMethod4.html) which defines the [XmlInfoEventHandler](dcsXmlInfoEventHandlerDelegate.html) parameter, to monitor the method's progress. 
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> Pro
See Also

<dl />
      [AdgFactory Class](dcsAdgFactoryClass.html)
      <br />
      [ReadXml Methods](dcsAdgFactoryClassReadXmlMethods.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [WriteXml Method](dcsIAdgObjectClassWriteXmlMethods.html)
      <br />
      [ToString Method](dcsIAdgObjectClassToStringMethod.html)
      <br />
      [IDirectory Class](dcsIDirectoryClass.html)
      <br />
      [Enumerate Method](dcsIDirectoryClassEnumerateMethod.html)
      <br />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [IMember Class](dcsIMemberClass.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [AdgObjectTypes Enumeration](dcsAdgObjectTypesEnumeration.html)
      <br />
      [XmlOptions Enumeration](dcsXmlOptionsEnumeration.html)
      <br />
      [XmlInfoEventHandler Delegate](dcsXmlInfoEventHandlerDelegate.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

