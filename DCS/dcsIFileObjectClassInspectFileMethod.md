---
title: IFileObject.InspectFile Method

Id: dcsIFileObjectClassInspectFileMethod
TocParent: dcsIFileObjectMethods
TocOrder: 2

keywords: InspectFile method, IFileObject class
keywords: InspectFile method
keywords: IFileObject.InspectFile method

---

InspectFile is reserved for internal use by DCS and should not be invoked by user programs .
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void InspectFile(<br />[InspectFileParts](dcsInspectFilePartsEnumeration.html) parts,<br />[InspectFileOutput](dcsInspectFileOutputEnumeration.html) output, <br />   out int ErrorCount,
   [AdgObserver](dcsAdgObserverDelegate.html) observer
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub InspectFile(_
   ByVal parts As [InspectFileParts](dcsInspectFilePartsEnumeration.html)_      
   ByVal output As [InspectFileOutput](dcsInspectFileOutputEnumeration.html)_<br />   ByVal ErrorCount As Integer_<br />   ByVal observer As [AdgObserver](dcsAdgObserverDelegate.html)<br /> ) As Void** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc InspectFile Access(*Public) Type(Void)<br />   DclSrParm parts Type([InspectFileParts](dcsInspectFilePartsEnumeration.html))<br />   DclSrParm output Type([InspectFileOutput](dcsInspectFileOutputEnumeration.html))<br />   DclSrParm ErrorCount Type(*Integer)<br />   DclSrParm observer Type([AdgObserver](dcsAdgObserverDelegate.html))** 
      </pre>

Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span><b class="le" style="FONT-WEIGHT: bold">Platforms: </b>Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [IFileObject Class](dcsIFileObjectClass.html)
      <br />
      [IFileObject Members](dcsIFileObjectMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

