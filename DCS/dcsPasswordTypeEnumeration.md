---
title: PasswordType Enumeration

Id: dcsPasswordTypeEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 20

keywords: enumerations [DCS 16.0 PasswordType
keywords: PasswordType enumeration
keywords: Legacy enumeration member
keywords: SecurePassPhrase enumeration member

---

The <span> **PasswordType** </span> enumerated constant defines values indicating a particular authentication scheme or password security mode. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public enum PasswordType;** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Enum PasswordType** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegEnum PasswordType Access(*Public)** 
      </pre>

Remarks

Database providers may define special authentication schemes for initiating sessions. The values of this enumeration are assigned to the [ SourceProfile.PasswordType](dcsSourceProfileClassPasswordTypeProperty.html) property to provide a way to specify that a [ SourceProfile](dcsSourceProfileClass.html) object uses a particular authentication scheme or password security mode. 
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col span="1" width="15%" style="FONT-WEIGHT: bold" />
            <col span="1" width="60%" />
            <col span="1" width="10%" />
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

SecurePassPhrase
</td>
            <td colspan="1" rowspan="1">

The password has no special properties and can be specified as a string of any characters (of any length). Note that although DCS permits the password to be an arbitrary string, the database provider may enforce restrictions when the session is authenticated.
</td>
            <td colspan="1" rowspan="1">

1
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Legacy 
</td>
            <td colspan="1" rowspan="1">

The password can be no longer than 31 characters in length. Further, the password supports the iSeries V4R5 authentication scheme (and V5R1 or later with the QPWDLVL system value set to 0 or 1), and Acceler8DB/DataGate database names created with legacy clients. When using this value to authenticate iSeries sessions, passwords are converted to uppercase and truncated to a length of exactly 10 characters. 
</td>
            <td colspan="1" rowspan="1">

0 
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)
      <br />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [Password Property](dcsSourceProfileClassPasswordProperty.html)

