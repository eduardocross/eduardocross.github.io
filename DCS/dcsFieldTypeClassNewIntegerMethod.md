---
title: FieldType.NewInteger Method

Id: dcsFieldTypeClassNewIntegerMethod
TocParent: dcsFieldTypeMethods
TocOrder: 7

keywords: NewInteger method
keywords: FieldType.NewInteger method
keywords: fields, value limit for integer
keywords: fields, integer
keywords: integer field defined
keywords: how to, define integer field

---

Creates a new integer [ FieldType](dcsFieldTypeClass.html).
<pre class="prettyprint">       <span class="lang">[C#]</span>
 **public static FieldType NewInteger(<br />   int length<br />);**  </pre>
      <pre class="prettyprint">       <span class="lang">[Visual Basic] </span>
 **Public Shared Function NewInteger( _<br />   ByVal length As Integer _<br />) As [FieldType](dcsFieldTypeClass.html)**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc NewInteger Type(FieldType) Access(*Public) Shared(*Yes)<br />   DclSrParm length Type(*Integer) Len(4)** 
      </pre>

Parameters

<dl>
        <dt>
 *length* 
        </dt>
        <dd>Integer.  The length of the field in bytes, either 2 or 4.
					</dd>
</dl>

Exceptions

**System.ArgumentException** . Thrown if *length* is not equal to 2 or 4.
Remarks

**NewInteger** constructs a **FieldType** object that represents a DataGate integer field. Integer fields contain integer numeric data stored in unsigned binary format in 2 or 4 bytes. The upper limit of 2-byte integer field values is 65535 and the upper limit of 4-byte integer field values is 4294967295.
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

