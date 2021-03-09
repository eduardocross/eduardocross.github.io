---
title: FieldType.ByteLength Property

Id: dcsFieldTypeClassByteLengthProperty
TocParent: dcsFieldTypeProperties
TocOrder: 0

keywords: ByteLength property
keywords: FieldType.ByteLength property
keywords: fields, length of in bytes
keywords: field length in bytes
keywords: how to, return field length

---

The length of the field in bytes.<span />
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public int ByteLength { get; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property ByteLength As Integer** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp ByteLength Type(*Integer) Len(4) Access(*Public)<br />   BegGet** 
      </pre>

Property Value

Integer. Returns the number of bytes in this field. 
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
      [ASNA.DataGate.Common Namespace](dcsASNADataGateCommonClasses.html)

