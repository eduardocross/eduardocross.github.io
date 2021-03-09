---
title: FieldType.Precision Property

Id: dcsFieldTypeClassPrecisionProperty
TocParent: dcsFieldTypeProperties
TocOrder: 4

keywords: Precision property
keywords: FieldType.Precision property
keywords: decimal fields, maximum number of digits
keywords: fields, maximum number of digits for decimals
keywords: maximum number of digits in decimal field
keywords: how to, define maximum number of digits in decimal field
keywords: number of, maximum digits in decimal field

---

The maximum number of digits for decimal fields. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public int Precision { get; }**  </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property Precision As Integer**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Precision Type(*Integer) Len(4) Access(*Public)<br />   BegGet** 
      </pre>

Property Value

Integer. Returns the maximum number of digits for decimal fields.
Remarks

Use the **Precision** property to determine the maximum number of digits used to represent values for a numeric **FieldType** object. 
Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html)

<span> **Assembly:** ASNA DataGate Client</span> 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FieldType Class](dcsFieldTypeClass.html)
      <br />
      [FieldType Class Members](dcsFieldTypeMembers.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

