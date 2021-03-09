---
title: WaitOptions Enumeration

Id: dcsWaitOptionsEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 32

keywords: Default enumeration member
keywords: Definite enumeration member
keywords: Immediate enumeration member
keywords: Indefinite enumeration member
keywords: WaitOptions enumeration
keywords: enumerations [DCS 16.0 WaitOptions

---

<span> **WaitOptions** </span> defines values for directing the [Lock](dcsIAdgObjectClassLockMethod.html) method when the requested lock cannot be immediately granted.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum WaitOptions;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Enum WaitOptions** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum WaitOptions Access(*Public)** 
      </pre>

Remarks

**WaitOptions** is a parameter of the **IAdgObject.Lock** method. The parameter defines how the "lock unavailable" condition is handled by **Lock** . If the lock requested is not available (due to a conflicting resource allocation), the **WaitOptions** value directs **Lock** to either wait for the lock to become available (indefinitely, or for some number of seconds), or to throw an exception. The table below lists the values of **WaitOptions** and their effect on **Lock** .
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <col align="middles" span="1" width="20%" style="FONT-WEIGHT: bold" />
          <col span="1" width="70%" />
          <col align="middles" span="1" width="10%" />
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

Default
</td>
            <td colspan="1" rowspan="1">

The condition is handled in the default manner, dependent upon the database system configuration. Generally, a system is configured to either throw an exception immediately, wait some number of seconds for the lock to become available, or wait indefinitely for the lock to become available.
</td>
            <td colspan="1" rowspan="1">

0
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Immediate
</td>
            <td colspan="1" rowspan="1">

An exception is thrown immediately to signal the condition. See **IAdgObject.Lock** for details.
</td>
            <td colspan="1" rowspan="1">

1
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Definite
</td>
            <td colspan="1" rowspan="1">

**Lock** will block for no more than the number of seconds specified by its *WaitTime* parameter. If the lock becomes available before the timer expires, the database will grant the lock, and **Lock** will return without error. If the timer expires before the lock is granted, **Lock** will throw an exception to signal the condition. See **IAdgObject.Lock** for details.
</td>
            <td colspan="1" rowspan="1">

2
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Indefinite
</td>
            <td colspan="1" rowspan="1">

**Lock** will block indefinitely, until the database grants the requested lock.
</td>
            <td colspan="1" rowspan="1">

3
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [IAdgObject.Lock Method](dcsIAdgObjectClassLockMethod.html) <br />
	  [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

