---
title: FileAdapter.FormatRequested Property

Id: dcsFileAdapterClassFormatRequestedProperty
TocParent: dcsFileAdapterProperties
TocOrder: 7

keywords: FormatRequested property
keywords: FileAdapter.FormatRequested property
keywords: multiformat files, format index of most recent
keywords: file formats, index of most recent
keywords: file format index of most recent
keywords: files, format index of most recent
keywords: database files, format index of most recent

---

Reflects the most recent format specified in a [ SetFormat](dcsFileAdapterClassSetFormatMethod.html) or [ResetFormat](dcsFileAdapterClassResetFormatMethod.html) method call.
<pre>
        <span class="lang">[C#]</span>
 **Public int FormatRequested { get; }** 
      </pre>
      <pre>
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property FormatRequested As Integer** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp FormatRequested Access(*Public) Type(*Integer4)
   BegGet** 
      </pre>

Property Value

**Int32** . A zero-relative format index of a format in the file represented by **FileAdapter** or the value -1. 
Remarks

When a format is specified as a "requested" format in **FileAdapter** (via the **SetFormat** method), DCS uses this property to make note of that information. 

When the user program invokes **ResetFormat** , the value of **FormatRequested** is set to -1. 
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
      [SetFormat Method](dcsFileAdapterClassSetFormatMethod.html)
      <br />
      [ResetFormat Method](dcsFileAdapterClassResetFormatMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

