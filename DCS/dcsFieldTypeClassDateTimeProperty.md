---
title: FieldType.DateTime Property

Id: dcsFieldTypeClassDateTimeProperty
TocParent: dcsFieldTypeProperties
TocOrder: 2

keywords: DateTime property
keywords: FieldType.DateTime property
keywords: enumerations [DCS 16.0 DateTimeFormat, used by
keywords: DateTimeFormat enumeration, used by
keywords: fields, date/time format length
keywords: date/time format of field
keywords: how to, determine date/time format of field

---

The date and time format of the field. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public DateTimeFormat DateTime { get; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property DateTime As [DateTimeFormat](dcsDateTimeFormatEnumeration.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp DateTime Type(DateTimeFormat) Access(*Public)<br />   BegGet** 
      </pre>

Property Value

[DateTimeFormat](dcsDateTimeFormatEnumeration.html). Returns the number of bytes in this field given as one of the values of **DateTimeFormat** . 
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
      [DateTimeFormat Enumeration](dcsDateTimeFormatEnumeration.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

