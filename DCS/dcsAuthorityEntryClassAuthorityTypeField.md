---
title: AuthorityEntry.AuthorityType Field

Id: dcsAuthorityEntryClassAuthorityTypeField
TocParent: dcsAuthorityEntryFields
TocOrder: 0

keywords: AuthorityType field
keywords: AuthorityEntry.AuthorityType field
keywords: AuthorityTypes enumeration, used by
keywords: enumerations [DCS 16.0 AuthorityTypes, used by
keywords: how to, establish database access and limitations
keywords: database objects, authorities access and limitations established
keywords: authorities, access and limitations established for database

---

**AuthorityType** defines the access capabilities and limitations for this authorization entry.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public [AuthorityTypes](dcsAuthorityTypesEnumeration.html) AuthorityType** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Shared Property AuthorityType As [AuthorityTypes](dcsAuthorityTypesEnumeration.html)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **DclFld Name(AuthorityType) Type([AuthorityTypes](dcsAuthorityTypesEnumeration.html)) Access(*Public) Shared(*Yes)** 
      </pre>

Field
 Value

[AuthorityTypes](dcsAuthorityTypesEnumeration.html). A value denoting access capabilities and limitation. This value may be a bit-combination of **AuthorityTypes** enumeration.
Remarks

**AuthorityType** is a combination of the bit values of the **AuthorityTypes** enumeration, describing the "access capabilities" portion of the AuthorityEntry. For example, if **AuthorityType** is equal to the **Exclude** value, AuthorityEntry indicates that [ UserName](dcsAuthorityEntryClassUsernameField.html) has no access capability to the database object **AuthorityEntry** is associated with. 
Requirements

**Namespace:** [ ASNA.DataGate.Client](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AuthorityEntry Class](dcsAuthorityEntryClass.html)
      <br />
      [AuthorityEntry Class Members](dcsAuthorityEntryMembers.html)
      <br />
      [UserName Field](dcsAuthorityEntryClassUsernameField.html)
      <br />
      [AuthorityTypes Enumeration](dcsAuthorityTypesEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

