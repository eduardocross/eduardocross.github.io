---
title: InspectFileParts Enumeration

Id: dcsInspectFilePartsEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 16

keywords: InspectFileParts enumeration
keywords: enumerations [DCS 16.0 InspectFileParts

---

<span> **InspectFileParts** </span> defines values used internally by DCS . 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum InspectFileParts;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum InspectFileParts** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum InspectFileParts Access(*Public)** 
      </pre>

Remarks

**InspectFileParts** defines values only used by the reserved method **IFileObject.InspectFile.** This method should not be invoked by user programs. 
Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

