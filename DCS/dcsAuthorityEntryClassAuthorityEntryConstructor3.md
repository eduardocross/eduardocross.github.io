---
title: AuthorityEntry(string,AuthorityTypes)

Id: dcsAuthorityEntryClassAuthorityEntryConstructor3
TocParent: dcsAuthorityEntryClassAuthorityEntryConstructors
TocOrder: 2

keywords: AuthorityTypes enumeration, used by
keywords: enumerations [DCS 16.0 AuthorityTypes, used by

---

<span>Creates a new instance of <span> **AuthorityEntry** </span> specifying a single-user profile and corresponding authorization types</span>.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public AuthorityEntry(
   string username
   [AuthorityTypes](dcsAuthorityTypesEnumeration.html) authorityType
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub AuthorityEntry( _
   ByVal username As string _
   ByVal authorityType As [AuthorityTypes](dcsAuthorityTypesEnumeration.html)** 
 **)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc AuthorityEntry Access(*Public)
   DclSrParm username Type (*string)
   DclSrParm authorityType Type([AuthorityTypes](dcsAuthorityTypesEnumeration.html))** 
      </pre>

Parameters

<dl>
        <dt>
 *username* 
        </dt>
        <dd>

**String** . A non-group profile name. See the [ UserName](dcsAuthorityEntryClassUsernameField.html) property.
</dd>
        <dt>
 *authorityType* 
        </dt>
        <dd>

[AuthorityTypes](dcsAuthorityTypesEnumeration.html). A combination of the bit values of **AuthorityTypes** expresssing authorized capabilities.
</dd>
</dl>

Exceptions

None.
Remarks

Only use this constructor when *username* is a single-user profile (rather than a group profile) since [ IsGroupAccount](dcsAuthorityEntryClassUsernameField.html) is initialized **False** . The [ UserName](dcsAuthorityEntryClassUsernameField.html) property is initialized with *username* . The [ AuthorityType](dcsAuthorityEntryClassAuthorityTypeField.html) field is initialized with *authorityType.* 
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
      [UserName Property](dcsAuthorityEntryClassUsernameField.html)
      <br />
      [IsGroupAccount Field](dcsAuthorityEntryClassUsernameField.html)
      <br />
      [AuthorityTypes Enumeration](dcsAuthorityTypesEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

