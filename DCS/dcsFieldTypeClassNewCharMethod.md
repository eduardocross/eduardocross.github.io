---
title: FieldType.NewChar Method

Id: dcsFieldTypeClassNewCharMethod
TocParent: dcsFieldTypeMethods
TocOrder: 1

keywords: NewChar method
keywords: FieldType.NewChar method
keywords: fields, character
keywords: character field type defined
keywords: how to, define character field

---

Creates a new fixed-width character [ FieldType](dcsFieldTypeClass.html).
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public static FieldType NewChar(<br />  int length<br />);** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Shared Function NewChar( _<br />  ByVal length As Integer _<br /><br />) As [FieldType](dcsFieldTypeClass.html)**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc NewChar Type(FieldType) Access(*Public) Shared(*Yes)<br />   DclSrParm length Type(*Integer) Len(4)** 
      </pre>

Parameters

<dl>
        <dt>
 *length* 
        </dt>
        <dd>Integer.  The length of the field in single-byte characters.</dd>
</dl>

Exceptions

None.
Remarks

**NewChar** constructs a **FieldType** that represents a traditional DataGate character field. Character fields contain single-byte character data in a fixed-width format. 
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

