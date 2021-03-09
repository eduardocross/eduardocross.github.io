---
title: AdgDataSet.GetFormatIndex Method

Id: dcsAdgDataSetClassGetFormatIndexMethod
TocParent: dcsAdgDataSetMethods
TocOrder: 3

keywords: GetFormatIndex method
keywords: AdgDataSet.GetFormatIndex method
keywords: database files, identify format of
keywords: files, identify format of
keywords: file formats, obtain format index from name
keywords: format indexes, obtain for file from format name
keywords: file format index from format names

---

Returns an integer identifying a DataGate file format.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public int GetFormatIndex(
   string strFormat
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function GetFormatIndex( _
   ByVal strFormat As String _
) As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc GetFormatIndex Access(*Public) Type(*Integer) Len(4)
   DclSrParm strFormat Type(*String)** 
      </pre>

Parameters

<dl>
        <dt>
 *strFormat* 
        </dt>
        <dd>String identifying a file format in the **AdgDataSet** .</dd>
</dl>

Exceptions

None.
Remarks

In **AdgDataSet,** DataTables corresponding to DataGate file formats are identified in two ways:

1. by format name, ([ GetFormatName](dcsAdgDataSetClassGetFormatNameMethod.html)) 
					and
2. by integer index.

<p> **GetFormatIndex** provides a way to obtain the integer index, given a format name. **GetFormatIndex** does not validate the *strFormat* parameter. If *strFormat* names a format that does not exist in the **AdgDataSet** , the method returns an invalid format index value equal to the current value of the [ Formats](dcsAdgDataSetClassFormatsProperty.html) property.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [AdgDataSet Class Members](dcsAdgDataSetMembers.html)
      <br />
      [Formats Property](dcsAdgDataSetClassFormatsProperty.html)
      <br />
      [GetFormatName Method](dcsAdgDataSetClassGetFormatNameMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

