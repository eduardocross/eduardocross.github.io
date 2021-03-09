---
title: AuthorityEntry(string, AuthorityTypes, boolean)

Id: dcsAuthorityEntryClassAuthorityEntryConstructor4
TocParent: dcsAuthorityEntryClassAuthorityEntryConstructors
TocOrder: 3

keywords: AuthorityTypes enumeration, used by
keywords: enumerations [DCS 16.0 AuthorityTypes, used by

---

<span>Creates a new instance of <span> **AuthorityEntry** </span> specifying a profile, its corresponding authorization types, and the profile type</span>.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public AuthorityEntry(
   string username
   [AuthorityTypes](dcsAuthorityTypesEnumeration.html) authorityType
   bool isGroupAccount
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub AuthorityEntry ( _
   ByVal username As string _<br />   ByVal authorityType As [AuthorityTypes](dcsAuthorityTypesEnumeration.html)
   ByVal isGroupAccount As boolean** 
   )</pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegConstructor AuthorityEntry Access(*Public)
   DclSrParm username Type (*string)
   DclSrParm authorityType Type([AuthorityTypes](dcsAuthorityTypesEnumeration.html))<br />   DclSrParm isGroupAccount Type(*boolean)** 
      </pre>

Parameters

<dl>
        <dt>
 *username* 
        </dt>
        <dd>

**String** . The user to group profile name. See the [ UserName](dcsAuthorityEntryClassUsernameField.html) field.
</dd>
        <dt>
 *authorityType* 
        </dt>
        <dd>

[AuthorityTypes](dcsAuthorityTypesEnumeration.html). A combination of the bit values of **AuthorityTypes** expresssing authorized capabilities.
</dd>
        <dt>
 *isGroupAccount* 
        </dt>
        <dd>

**Boolean** . Set this to **False** if *username* is a single user profile, or **True** if *username* is a group profile. See **Username** .
</dd>
</dl>

Exceptions

None.
Remarks

This constructor provides parameters for initializing all of the fields of **AuthorityEntry** . The [UserName](dcsAuthorityEntryClassUsernameField.html) field is set to *username* , the [AuthorityType](dcsAuthorityEntryClassAuthorityTypeField.html) field is set to *authorityType* , and the [ IsGroupAccount](dcsAuthorityEntryClassUsernameField.html) field is set to *isGroupAccount* .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AuthorityEntry Class](dcsAuthorityEntryClass.html)
      <br />
      [AuthorityEntry Class Members](dcsAuthorityEntryMembers.html)
      <br />
      [AuthorityType Field](dcsAuthorityEntryClassAuthorityTypeField.html)
      <br />
      [IsGroupAccount Field](dcsAuthorityEntryClassUsernameField.html)
      <br />
      [UserName Field](dcsAuthorityEntryClassUsernameField.html)
      <br />
      [AuthorityTypes Enumeration](dcsAuthorityTypesEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

