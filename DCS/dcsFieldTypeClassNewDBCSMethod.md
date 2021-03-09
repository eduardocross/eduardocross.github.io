---
title: FieldType.NewDBCS Method

Id: dcsFieldTypeClassNewDBCSMethod
TocParent: dcsFieldTypeMethods
TocOrder: 3

keywords: double byte fields
keywords: NewDBCS method
keywords: FieldType.NewDBCS method
keywords: fields, double byte
keywords: double byte field defined
keywords: how to, define double byte field type
keywords: enumerations [DCS 16.0 DbcsFormat, used by
keywords: DbcsFormat enumeration, used by

---

Creates a new fixed-width double-byte character [FieldType](dcsFieldTypeClass.html).
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public static FieldType NewDBCS(<br />   int length,<br />   DbcsFormat fmt<br />);** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Shared Function NewDBCS( _<br />   ByVal length As Integer _<br />   ByVal fmt As [DbcsFormat](dcsDbcsFormatEnumeration.html)<br />) As [FieldType](dcsFieldTypeClass.html)**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc NewDBCS Type(FieldType) Access(*Public) Shared(*Yes)<br />   DclSrParm length Type(*Integer) Len(4)
   DclSrParm fmt Type(DbcsFormat)** 
      </pre>

Parameters

<dl>
        <dt>
 *length* 
        </dt>
        <dd>Integer.  The length of the field in double-byte characters. </dd>
        <dt>
 *fmt* 
        </dt>
        <dd>
          [DbcsFormat](dcsDbcsFormatEnumeration.html).  The format of the 
								double-byte character **FieldType** .
							</dd>
</dl>

Exceptions

System.ArgumentException. Thrown if *fmt* is **DbcsFormat.None** .
Remarks

**NewDBCS** constructs a **FieldType** that represents a DataGate character field composed of double-byte characters. DBCS fields contain double-byte character data in a fixed-width format. The storage size of a DBCS field is dependent upon the format but each double-byte character stored occupies 2 bytes of storage. 
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
      [DbcsFormat Enumeration](dcsDbcsFormatEnumeration.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

