---
title: FieldType.NewBinary Method

Id: dcsFieldTypeClassNewBinaryMethod
TocParent: dcsFieldTypeMethods
TocOrder: 0

keywords: NewBinary method
keywords: FieldType.NewBinary method
keywords: fields, binary
keywords: binary field defined
keywords: how to, define binary fields

---

Creates a new binary decimal [ FieldType](dcsFieldTypeClass.html).
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public static FieldType NewBinary(<br />  int prec,<br />  int scale<br />);** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Shared Function NewBinary( _<br />  ByVal prec As Integer, _<br />  ByVal scale As Integer _<br />) As [FieldType](dcsFieldTypeClass.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc NewBinary Type(FieldType) Access(*Public) Shared(*Yes)
   DclSrParm prec Type(*Integer) Len(4)
   DclSrParm scale Type(*Integer) Len(4)** 
      </pre>

Parameters

<dl>
        <dt>
 *prec* 
        </dt>
        <dd>Integer.  The maximum number of digits for decimal fields. </dd>
        <dt>
 *scale* 
        </dt>
        <dd>Integer.  The maximum number of digits to the right of the decimal point.
							</dd>
</dl>

Exceptions

**System.ArgumentException** . Thrown if *scale* is greater than *prec* or if *prec* is greater than 9. 
Remarks

<span> **NewBinary** </span> constructs a **FieldType** that represents a traditional DataGate binary field. Binary fields contain decimal numerical data in a simple integer format. In storage, binary fields may occupy 2 or 4 bytes depending upon the desired decimal precision.

The largest decimal precision allowed for binary fields is 9. If *prec* is greater than 4, the binary field will occupy 4 bytes in storage; otherwise, it is a 2-byte field.
Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html)

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FieldType Class](dcsFieldTypeClass.html)
      <br />
      [FieldType Class Members](dcsFieldTypeMembers.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

