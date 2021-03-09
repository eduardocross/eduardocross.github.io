---
title: FieldType.Dbcs Property

Id: dcsFieldTypeClassDbcsProperty
TocParent: dcsFieldTypeProperties
TocOrder: 3

keywords: Dbcs property
keywords: FieldType.Dbcs property
keywords: enumerations [DCS 16.0 DbcsFormat, used by
keywords: DbcsFormat enumeration, used by
keywords: fields, double byte length
keywords: double byte field length
keywords: how to, return double byte field length

---

The length of the field in bytes. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public DbcsFormat Dbcs { get; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property Dbcs As [DbcsFormat](dcsDbcsFormatEnumeration.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Dbcs Type(DbcsFormat) Access(*Public)<br />   BegGet** 
      </pre>

Property Value

Integer. Returns the number of bytes in this field given as one of the values of [ DbcsFormat](dcsDbcsFormatEnumeration.html). 
Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html)

<span> **Assembly:** ASNA DataGate Providers</span> 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FieldType Class](dcsFieldTypeClass.html)
      <br />
      [FieldType Class Members](dcsFieldTypeMembers.html)
      <br />
      [DbcsFormat Enumeration](dcsDbcsFormatEnumeration.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

