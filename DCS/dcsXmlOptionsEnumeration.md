---
title: XmlOptions Enumeration

Id: dcsXmlOptionsEnumeration
TocParent: dcsDataGateClientEnumerations
TocOrder: 4

keywords: Default enumeration member
keywords: WithData enumeration member
keywords: WithMembers enumeration member
keywords: WithPhysicalFiles enumeration member
keywords: WithLogicalFile enumeration member
keywords: WithOlePrintFiles enumeration member
keywords: WithFiles enumeration member
keywords: WithDirectories enumeration member
keywords: WithSubObjects enumeration member
keywords: CreateObject enumeration member
keywords: RetainObjectTree enumeration member
keywords: IgnoreDuplicates enumeration member
keywords: DontValidate enumeration member
keywords: RelativeBasePaths enumeration member
keywords: XmlOptions enumeration
keywords: enumerations [DCS 16.0 XmlOptions
keywords: XML [DCS 16.0 database files, create options
keywords: XML [DCS 16.0 database libraries, create options
keywords: XML [DCS 16.0 database objects, create options
keywords: XML [DCS 16.0 database file members, create options
keywords: XML [DCS 16.0 XML options constants
keywords: database files, create from XML document, create options
keywords: database file members, create from XML document, create options
keywords: database libraries, create from XML document, create options

---

The **XmlOptions** enumeration defines bit-flag values directing the [ AdgFactory.ReadXml](dcsAdgFactoryClassReadXmlMethod2.html) and [IAdgObject.WriteXml](dcsIAdgObjectClassWriteXmlMethod2.html) methods. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **[Flags]public enum XmlOptions;** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **&lt;Flags&gt; Public Enum XmlOptions** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegEnum XmlOptions Access(*Public) Attributes(Flags)** 
      </pre>

Remarks

**XmlOptions** defines verbs directing the operation of the **AdgFactory.ReadXml** and **IAdgObject.WriteXml** methods. The table below lists each value, and its effect on the methods. The enumeration is defined with the **System.FlagsAttribute** , so its values can be combined to create a composite value. See **ReadXml** and **WriteXml** for more information. 
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="15%" style="FONT-WEIGHT: bold" />
            <col span="1" width="42%" />
            <col align="middles" span="1" width="42%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value</th>
            <th colspan="1" rowspan="1">
							ReadXml</th>
            <th colspan="1" rowspan="1">
							WriteXml</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Default
</td>
            <td colspan="1" rowspan="1">

Only create the [IAdgObject](dcsIAdgObjectClass.html) corresponding to the document element. Disregard descriptions of contained objects if any, and do not create a new database object. Validate the schema of the document against the value of the [IAdgObject.Schema](dcsIAdgObjectClassSchemaProperty.html) property. 
</td>
            <td colspan="1" rowspan="1">

Create the XML document fragment describing the **IAdgObject** only. Disregard objects contained by the **IAdgObject** , if any. Base object paths are given as absolute paths. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

WithData
</td>
            <td colspan="1" rowspan="1">

This is a reserved value and should not be used.
</td>
            <td colspan="1" rowspan="1">

This is a reserved value and should not be used
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

WithMembers 
</td>
            <td colspan="1" rowspan="1">

Create [IMember](dcsIMemberClass.html) objects specified in the document. If the document element does not define a member, then only members contained by [IFileObject](dcsIFileObjectClass.html) instances also created by the call to ReadXml are created.<br /> The *CreateObject* , *RetainObjectTree* , and *IgnoreDuplicates* values also apply to the created **IMember** object. 
</td>
            <td colspan="1" rowspan="1">

Create the XML document fragment and include database members contained by the **IAdgObject** . If any file objects are described in XML, then those files' members will be described as well. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

WithPhysicalFiles 
</td>
            <td colspan="1" rowspan="1">

Create **IFileObject** objects specified in the document as physical files. If the document element does not define a physical file, then only physical files contained by [IDirectory](dcsIDirectoryClass.html) instances also created by the call to ReadXml are created. The *CreateObject* , *RetainObjectTree* , and *IgnoreDuplicates* values also apply to the created **IFileObject** object. 
</td>
            <td colspan="1" rowspan="1">

Create the XML document fragment and include database physical files contained by the **IAdgObject** . If any library objects are described in XML, then physical files contained in those libraries will be described as well. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

WithLogicalFile 
</td>
            <td colspan="1" rowspan="1">

Create **IFileObject** objects specified in the document as logical files. If the document element does not define a logical file, then only logical files contained by **IDirectory** instances also created by the call to ReadXml are created. The *CreateObject* , *RetainObjectTree* , and *IgnoreDuplicates* values also apply to the created **IFileObject** object. 
</td>
            <td colspan="1" rowspan="1">

Create the XML document fragment and include database logical files contained by the **IAdgObject** . If any library objects are described in XML, then logical files contained in those libraries will be described as well. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

WithOlePrintFiles 
</td>
            <td colspan="1" rowspan="1">

Create **IFileObject** objects specified in the document as OLE print files. If the document element does not define an OLE print file, then only OLE print files contained by **IDirectory** instances also created by the call to ReadXml are created. The *CreateObject* , *RetainObjectTree* , and *IgnoreDuplicates* values also apply to the created **IFileObject** object. 
</td>
            <td colspan="1" rowspan="1">

Create the XML document fragment and include database OLE print files contained by the **IAdgObject** . If any library objects are described in XML, then OLE print files contained in those libraries will be described as well. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

WithFiles 
</td>
            <td colspan="1" rowspan="1">

This composite value combines the effects of the *WithPhysicalFiles* , *WithLogicalFiles* , and *WithOlePrintFiles* values. 
</td>
            <td colspan="1" rowspan="1">

This composite value combines the effects of the *WithPhysicalFiles* , *WithLogicalFiles* , and *WithOlePrintFiles* values. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

WithDirectories 
</td>
            <td colspan="1" rowspan="1">

Create **IDirectory** objects specified in the document. The document element must specify a library element, or this option is ignored. Any libraries specified in the document as contained by **IDirectory** objects created by this call to ReadXml are also created. The *CreateObject* , *RetainObjectTree* , and *IgnoreDuplicates* values also apply to the created **IDirectory** object. 
</td>
            <td colspan="1" rowspan="1">

Create the XML document fragment and include database libraries contained by the **IAdgObject** . If any library objects are described in XML then libraries contained in those libraries will be described as well. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

WithSubObjects 
</td>
            <td colspan="1" rowspan="1">

This composite value combines the effects of *WithMembers* , *WithPhysicalFiles* , *WithLogicalFiles* , *WithOlePrintFiles* , and *WithDirectories* files. 
</td>
            <td colspan="1" rowspan="1">

This composite value combines the effects of *WithMembers* , *WithPhysicalFiles* , *WithLogicalFiles* , *WithOlePrintFiles* , and *WithDirectories* files. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

CreateObject 
</td>
            <td colspan="1" rowspan="1">

Upon successful creation of **IAdgObject** instances in this call to ReadXml, call the [IAdgObject.Create](dcsIAdgObjectClassCreateMethod.html) method to create a database object. **IAdgObjects** and the underlying database objects are created in the order they occur in the XML document. 
</td>
            <td colspan="1" rowspan="1">

This option does not apply to WriteXml. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

RetainObjectTree 
</td>
            <td colspan="1" rowspan="1">

If the document specifies container objects (libraries or files), instances of **IAdgObject** contained are retained as references in the containing **IAdgObject's** enumeration facilities. If this is not specified, contained **IAdgObject** instances may be created temporarily by ReadXml (e.g., for use with the *CreateObject* facility), but they are not otherwise retained for use outside of ReadXml. 
</td>
            <td colspan="1" rowspan="1">

This option does not apply to WriteXml. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

IgnoreDuplicates 
</td>
            <td colspan="1" rowspan="1">

Only valid if specified with the *CreateObject* value, this allows ReadXml to ignore "duplicate object" errors returned by the database when attempting to use **IAdgObject** . **Create** to create the objects. If this is not specified, ReadXml will stop processing when a duplicate object is encountered. 
</td>
            <td colspan="1" rowspan="1">

This option does not apply to WriteXml. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

DontValidate 
</td>
            <td colspan="1" rowspan="1">

Read, but don't validate the XML document. This option should only be used when the document is known to be valid from a previous call to ReadXml. If not specified, ReadXml will wrap the passed XmlReader in an XmlValidatingReader to validate the document as it is read. 
</td>
            <td colspan="1" rowspan="1">

This option does not apply to WriteXml. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

RelativeBasePaths 
</td>
            <td colspan="1" rowspan="1">

This option does not apply to ReadXml. 
</td>
            <td colspan="1" rowspan="1">

Write base paths in base object descriptions as relative to the **IAdgObject** root - the **IAdgObject** upon which the WriteXml method was invoked. That is, if the prefix of a base path is the path of the **IAdgObject** root, the prefix is removed in the base object description, allowing a degree of portability for the base path. See the Remarks section of the WriteXml and ReadXml methods for more details. 
</td>
          </tr>
</table>

<br />

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [AdgFactory Class](dcsAdgFactoryClass.html)
      <br />
      [ReadXml Methods](dcsAdgFactoryClassReadXmlMethods.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [WriteXml Methods](dcsIAdgObjectClassWriteXmlMethods.html)
      <br />
      [Schema Property](dcsIAdgObjectClassSchemaProperty.html)
      <br />
      [Create Method](dcsIAdgObjectClassCreateMethod.html)
      <br />
      [IMember Class](dcsIMemberClass.html)
      <br />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [IDirectory Class](dcsIDirectoryClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

