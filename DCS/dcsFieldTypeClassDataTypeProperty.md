---
title: FieldType.DataType Property

Id: dcsFieldTypeClassDataTypeProperty
TocParent: dcsFieldTypeProperties
TocOrder: 1

keywords: DataType property
keywords: FieldType.DataType property
keywords: enumerations [DCS 16.0 DataTypes, used by
keywords: DataTypes enumeration, used by
keywords: fields, data type returned for
keywords: data types, return for field
keywords: how to, return data type of field

---

The data type for this field. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public DataTypes DataType { get; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property DataType As [DataTypes](dcsDataTypesEnumeration.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp DataType Type(DataTypes) Access(*Public)<br />   BegGet** 
      </pre>

Property Value

Integer. Returns the data type of this field given as one of the values of [DataTypes](dcsDataTypesEnumeration.html). 
Remarks

Valid field data types are defined by the <span> **DataTypes** </span> enumeration.
Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html)

**Assembly:** ASNA DataGate Providers

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FieldType Class](dcsFieldTypeClass.html)
      <br />
      [FieldType Class Members](dcsFieldTypeMembers.html)
      <br />
      [DataTypes Enumeration](dcsDataTypesEnumeration.html)
      <br />
      [ASNA.DataGate.Common Namespaces](dcsDataGateCommonNamespace.html)

