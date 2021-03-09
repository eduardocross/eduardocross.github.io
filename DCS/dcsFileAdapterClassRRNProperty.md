---
title: FileAdapter.RRN Property

Id: dcsFileAdapterClassRRNProperty
TocParent: dcsFileAdapterProperties
TocOrder: 11

keywords: RRN property
keywords: FileAdapter.RRN property
keywords: database files, RRN of open file member
keywords: files, RRN of open file member
keywords: RRN, of current opened file member
keywords: relative record numbers, of current opened file member

---

The relative record number of the member of the currently-opened file. 
<pre>        <span class="lang">[C#]</span>
 **Public long RRN { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property RRN As Long** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp RRN Type(*Integer) Len(8) Access(*Public)
   BegGet** 
      </pre>

Property Value

Integer. Returns a long integer containing the relative record number of the member of the currently-opened file.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Class Members](dcsFileAdapterMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

