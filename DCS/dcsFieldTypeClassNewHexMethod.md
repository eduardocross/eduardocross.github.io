---
title: FieldType.NewHex Method

Id: dcsFieldTypeClassNewHexMethod
TocParent: dcsFieldTypeMethods
TocOrder: 6

keywords: NewHex method
keywords: FieldType.NewHex method
keywords: fields, hexadecimal
keywords: hexadecimal field defined
keywords: how to, define hexadecimal field

---

Creates a new hexadecimal data [ FieldType](dcsFieldTypeClass.html).
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public static FieldType NewHex(<br />   int length<br />);**  </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Shared Function NewHex( _<br />   ByVal length As Integer _<br />) As [FieldType](dcsFieldTypeClass.html)**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc NewHex Type(FieldType) Access(*Public) Shared(*Yes)<br />   DclSrParm length Type(*Integer) Len(4)** 
      </pre>

Parameters

<dl>
        <dt>
 *length* 
        </dt>
        <dd>Integer.  The length of the field in bytes.
					</dd>
</dl>

Remarks

**NewHex** constructs a **FieldType** object that represents a DataGate hexadecimal field. Hexadecimal fields are fixed-width, "uninterpreted" byte vectors designed to contain binary data. Neither the data provider nor DCS perform any data translation or formatting for hexadecimal fields. A hexadecimal field is defined only in terms of its size.

DCS restricts manipulation of hexadecimal field data to byte arrays only. The object value returned by DCS as the value of a hexadecimal field (in methods such as [As400Program.ParmToObject](dcsAs400ProgramClassParmToObjectMethodMain.html)) will always be an array of **System.Byte** value types. Likewise, DCS will only accept byte arrays for setting the value of hexadecimal fields.
Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html)

<span> **Assembly:** ASNA DataGate Client</span> 

<span /> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FieldType Class](dcsFieldTypeClass.html)
      <br />
      [FieldType Class Members](dcsFieldTypeMembers.html)
      <br />
      [As400Program.ParmToObject](dcsAs400ProgramClassParmToObjectMethodMain.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

