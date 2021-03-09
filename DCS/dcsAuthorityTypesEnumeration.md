---
title: AuthorityTypes Enumeration

Id: dcsAuthorityTypesEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 4

keywords: enumerations [DCS 16.0 AuthorityTypes
keywords: AuthorityTypes enumeration
keywords: Exclude enumeration member
keywords: Read enumeration member
keywords: Add enumeration member
keywords: Update enumeration member
keywords: Delete enumeration member
keywords: Execute enumeration member
keywords: Operational enumeration member
keywords: Change enumeration member
keywords: Use enumeration member
keywords: Existence enumeration member
keywords: Alter enumeration member
keywords: Management enumeration member
keywords: All enumeration member

---

The <span> **AuthorityTypes** </span> enumerated constant defines values that specify the types of object access authority users may be assigned. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum AuthorityTypes;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Enum AuthorityTypes** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum AuthorityTypes Access(*Public)** 
      </pre>

Remarks

**AuthorityTypes** is defined as a parameter of the [ GrantAuthority](dcsIAdgObjectClassGrantAuthorityMethod.html) and [RevokeAuthority](dcsIAdgObjectClassRevokeAuthorityMethod.html) methods of [IAdgObject](dcsIAdgObjectClass.html). The parameter's value denotes the authorization that a user is being granted or denied, in regard to the the database object represented by **IAdgObject** . **AuthorityTypes** is defined with the **System.FlagsAttribute** so its values can be combined to form specialized authority values. Some of combinations are pre-defined, such as **Change** and **All** . The following table summarizes the values of **AuthorityTypes** . 
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col span="1" width="10%" style="FONT-WEIGHT: bold" />
            <col span="1" width="50%" />
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

Exclude
</td>
            <td colspan="1" rowspan="1">

No authorizations have been assigned to the user. This value denotes the absence of any of the other authorizations which may be granted or denied.
</td>
            <td colspan="1" rowspan="1">

0
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Read
</td>
            <td colspan="1" rowspan="1">

The user may access the contents of the object.
</td>
            <td colspan="1" rowspan="1">

1
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Add
</td>
            <td colspan="1" rowspan="1">

The user may add entries to the database object.
</td>
            <td colspan="1" rowspan="1">

2
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Update
</td>
            <td colspan="1" rowspan="1">

The user may change the content of existing entries in the object.
</td>
            <td colspan="1" rowspan="1">

4
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Delete
</td>
            <td colspan="1" rowspan="1">

The user may remove entries from the object.
</td>
            <td colspan="1" rowspan="1">

8
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Execute
</td>
            <td colspan="1" rowspan="1">

The user may search a library object. 
</td>
            <td colspan="1" rowspan="1">

16
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Operational
</td>
            <td colspan="1" rowspan="1">

The user may look at the object's attributes and use the object as specified by the data authorities the user has to the object. 
</td>
            <td colspan="1" rowspan="1">

32
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Change
</td>
            <td colspan="1" rowspan="1">

The user has a combination of Add, Update, Delete, and Operational authority to the object. 
</td>
            <td colspan="1" rowspan="1">

46
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Use
</td>
            <td colspan="1" rowspan="1">

The user has a combination of Read, Execute, and Operational authority to the object.
</td>
            <td colspan="1" rowspan="1">

49
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Existence
</td>
            <td colspan="1" rowspan="1">

The user may control the object's existence and ownership.
</td>
            <td colspan="1" rowspan="1">

64
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Alter
</td>
            <td colspan="1" rowspan="1">

The user may change the attributes of the object.
</td>
            <td colspan="1" rowspan="1">

128
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Management
</td>
            <td colspan="1" rowspan="1">

The user may specify security, move or rename the object, or add members to a database file.
</td>
            <td colspan="1" rowspan="1">

256
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

All
</td>
            <td colspan="1" rowspan="1">

The user has "all authority" to the database object. This value is a combination of all other authorization values.
</td>
            <td colspan="1" rowspan="1">

511
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [GrantAuthority Method](dcsIAdgObjectClassGrantAuthorityMethod.html)
      <br />
      [RevokeAuthority Method](dcsIAdgObjectClassRevokeAuthorityMethod.html) <br />
	  [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

