---
title: AccessResult Enumeration

Id: dcsAccessResultEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 1

keywords: AccessResult enumeration
keywords: enumerations [DCS 16.0 AccessResult
keywords: finding records
keywords: OK enumeration member
keywords: NotFound enumeration member

---

Defines modes on whether a record was found.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum AccessResult;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Enum AccessResult** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum AccessResult Access(*Public)** 
      </pre>

Remarks

The <span> **AccessResult** </span> enumeration is used as a parameter by the [ BeginTransaction](dcsAdgConnectionClassBeginTransactionMethodMain.html) and [ BeginAutoTransaction](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html) methods of the [AdgConnection](dcsAdgConnectionClass.html) class.
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="center" span="1" width="12%" style="FONT-WEIGHT: bold" />
            <col span="1" width="60%" />
            <col align="center" span="1" width="10%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Member</th>
            <th colspan="1" rowspan="1">
							Description</th>
            <th colspan="1" rowspan="1">
							Value</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

OK
</td>
            <td colspan="1" rowspan="1">

Indicates that the next (or prior) sequential record was found to contain the given key (specified by Key and Keycount), and so the record was read.
</td>
            <td colspan="1" rowspan="1">

0
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NotFound
</td>
            <td colspan="1" rowspan="1">

Indicates that the next (or prior) record did not match the key, and thus no record was read by the method.
</td>
            <td colspan="1" rowspan="1">

1
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)

<strong >Platforms:</strong> Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      <span>
        [AdgConnection Class](dcsAdgConnectionClass.html)
      </span>
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

