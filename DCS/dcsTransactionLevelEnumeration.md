---
title: TransactionLevel Enumeration

Id: dcsTransactionLevelEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 31

keywords: High enumeration member
keywords: Low enumeration member
keywords: Medium enumeration member
keywords: Serial enumeration member
keywords: TransactionLevel enumeration
keywords: enumerations [DCS 16.0 TransactionLevel
keywords: transactions, lock level constants
keywords: transaction lock level constants
keywords: database transactions, lock level constants

---

The **TransactionLevel** enumerated constant defines values for the [ TransactionLevel](dcsIAdgTransactionClassTransactionLevelProperty.html) property of [IAdgTransaction](dcsIAdgTransactionClass.html).
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum TransactionLevel;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Enum TransactionLevel** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum TransactionLevel Access(*Public)** 
      </pre>

Remarks

A parameter of type **TransactionLevel** may be specified by certain overloads of the [ AdgConnection.BeginAutoTransaction](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html) and [ AdgConnection.BeginTransaction](dcsAdgConnectionClassBeginTransactionMethodMain.html) methods to create an instance of **IAdgTransaction** with the **TransactionLevel** property initialized to the specified value. 

A value of this type may be used by **IAdgTransaction** and database providers to prioritize transaction contexts.

For the System i database provider, the value of the **TransactionLevel** property translates to the value of the "LCKLVL" parameter of the "STRCMTCTL" command used to begin a transaction context. Please consult the iSeries database documentation for details. The following table summarizes the translation. 
Members

<table class="dtTABLE" id="Table3" cellspacing="0" width="50%">
          <colgroup span="1">
            <col align="middles" span="1" width="10%" style="FONT-WEIGHT: bold" />
            <col span="1" width="25%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
								Member</th>
            <th colspan="1" rowspan="1">
								iSeries STRCMTCTL LCKLVL</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Low
</td>
            <td colspan="1" rowspan="1">

*CHG
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Medium
</td>
            <td colspan="1" rowspan="1">

*CS
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

High
</td>
            <td colspan="1" rowspan="1">

*ALL
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Serial
</td>
            <td colspan="1" rowspan="1">

*ALL
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [BeginTransaction 
					Method](dcsAdgConnectionClassBeginTransactionMethodMain.html)
      <br />
      [BeginAutoTransaction 
					Method](dcsAdgConnectionClassBeginAutoTransactionMethodMain.html)
      <br />
      [IAdgTransaction Class](dcsIAdgTransactionClass.html)
      <br />
      [TransactionLevel 
					Property](dcsIAdgTransactionClassTransactionLevelProperty.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

