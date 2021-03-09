---
title: FileAdapter.CurrentFormatIndex Property

Id: dcsFileAdapterClassCurrentFormatIndexProperty
TocParent: dcsFileAdapterProperties
TocOrder: 2

keywords: CurrentFormatIndex property
keywords: FileAdapter.CurrentFormatIndex property
keywords: database files, index for current record format
keywords: files, index for current record format
keywords: records, index for record format
keywords: index for record format
keywords: how to, get index for record format

---

An integer containing the index for the record format of the record most recently accessed by the **FileAdapter** . 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public int CurrentFormatIndex { get; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property CurrentFormatIndex As Integer** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp CurrentFormatIndex Type(*Integer) Len(4)
   BegGet** 
      </pre>

Property Value

Integer. Returns an integer containing the index for the current record format. 
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [
					FileAdapter Members](dcsFileAdapterMembers.html)
      <br />
      [ASNA.DataGate.Client 
					Namespace](dcsDataGateClientNamespace.html)

