---
title: RepairOptions Enumeration

Id: dcsRepairOptionsEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 28

keywords: None enumeration member
keywords: Verbose enumeration member
keywords: KeepFile enumeration member
keywords: ForceRebuild enumeration member
keywords: RepairOptions enumeration
keywords: enumerations [DCS 16.0 RepairOptions
keywords: repair database files in library, options
keywords: database libraries, repair database files, options
keywords: database files, repair files in library, options
keywords: how to, repair database files in library, options
keywords: how to, invoke automatic diagnostic and repair function for library files, options
keywords: database files, repairing single file, options
keywords: repair single database file, options
keywords: how to, repair database file, options
keywords: how to, invoke automatic diagnostic and repair function for a file, options

---

<span> **RepairOptions** </span> specifies optional ancillary functions for the [ IDirectory.RepairObjects](dcsIDirectoryClassRepairObjectsMethod.html) and [ IFileObject.RepairFile](dcsIFileObjectClassRepairFileMethod.html) methods. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **[Flags]<br /> public enum RepairOptions;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **&lt;FlagsAttribute&gt;<br />Public Enum RepairOptions** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum RepairOptions Access(*Public) Attributes(Flags)** 
      </pre>

Remarks

The values of this enumeration can be combined to specify more than one option. Please see **IDirectory.RepairObjects** and **IFileObject.RepairFile** for more information regarding file repair functions. 

The following table details each value and its corresponding repair function. 
Members

<br />

<table class="dtTABLE" id="Table3" cellspacing="0">
            <tr>
              <th>			Member</th>
              <th>			Description</th>
              <th>			Value</th>
            </tr>
            <tr>
              <td>

None
</td>
              <td>
                No optional functions.  Only the default primary automated 
											diagnostic/repair facilities are engaged.
              </td>
              <td>

0
</td>
            </tr>
            <tr>
              <td>

Verbose
</td>
              <td>

Generate detailed debugging and tracing messages encountered via the AdgObserver delegate.
</td>
              <td>

1
</td>
            </tr>
            <tr>
              <td>

KeepFile
</td>
              <td>

Prior to repair, a copy of the original unrepaired grove file is made. The name of the copy is changed to terminate with the extension .old (instead of .grv). The copy resides in the same directory as the repaired grove file.
</td>
              <td>

2
</td>
            </tr>
            <tr>
              <td>

ForceRebuild
</td>
              <td>

The file is subjected to repair procedures regardless of the outcome of the automated diagnostic test. If this is not specified, the file is only "repaired" if diagnostic tests reveal a flaw.
</td>
              <td>

4
</td>
            </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
        [IDirectory.RepairObjects Method](dcsIDirectoryClassRepairObjectsMethod.html)
        <br />
        [IFileObject.RepairFile Method](dcsIFileObjectClassRepairFileMethod.html)
        <br />
        [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

