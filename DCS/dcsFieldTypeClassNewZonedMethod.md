---
title: FieldType.NewZoned Method

Id: dcsFieldTypeClassNewZonedMethod
TocParent: dcsFieldTypeMethods
TocOrder: 11

keywords: NewZoned method
keywords: FieldType.NewZoned method
keywords: fields, zoned decimal
keywords: fields, zoned decimal size limit
keywords: zoned decimal field defined
keywords: how to, define zoned decimal field

---

Creates a new zoned decimal [ FieldType](dcsFieldTypeClass.html).
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public static FieldType NewZoned(<br />   int prec,<br />   int scale<br />)**  </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Shared Function NewZoned( _<br />   ByVal prec As Integer, _<br />   ByVal scale As Integer<br />) As [FieldType](dcsFieldTypeClass.html)**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc NewZoned Type(FieldType) Access(*Public) Shared(*Yes)<br />   DclSrParm prec Type(*Integer) Len(4)<br />   DclSrParm scale Type(*Integer) Len(4)** 
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

System.ArgumentException. Thrown if *scale* is greater than *prec* .
Remarks

**NewZoned** constructs a **FieldType** object that represents a DataGate zoned decimal field. Zoned decimal fields contain signed decimal numeric data formatted in the traditional zoned decimal format. In this format, each decimal digit is contained in a byte of storage. The rightmost byte of a zoned decimal field contains the least significant digit and a sign (+/-) indicator. Thus, the amount of storage in bytes required for a zoned decimal field is the precision of the field. 

The maximum precision of a zoned decimal field is data provider dependent. On the IBM i platform, zoned decimal fields may have up to 16 digits. 
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

