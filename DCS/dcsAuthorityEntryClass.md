---
title: AuthorityEntry Class

Id: dcsAuthorityEntryClass
TocParent: dcsASNADataGateClientClasses
TocOrder: 6

keywords: classes [DCS 16.0 AuthorityEntry class
keywords: AuthorityEntry class
keywords: AuthorityEntry class, about AuthorityEntry class
keywords: authorities, about AuthorityEntry class

---

The <span> **AuthorityEntry** </span> class describes a user or group authorization to a database object. For a list of all members, see [AuthorityEntry Members](dcsAuthorityEntryMembers.html). 

[ASNA.DataGate.Client](dcsDataGateClientNamespace.html) <br /> **ASNA.DataGate.Client.<span>AuthorityEntry</span>** 
<pre class="prettyprint">
        <span class="lang">[Prototype in C#]</span>
public class AuthorityEntry :</pre>

Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
Remarks

<span style="FONT-WEIGHT: bold">AuthorityEntry</span> describes a user or group authorization to a database directory, member, or file. An instance of **AuthorityEntry** is usually one of a collection of authority descriptors for the database object, such as provided by the [AuthorityEntries](dcsIAdgObjectClassAuthorityEntriesProperty.html) property of [IAdgObject](dcsIAdgObjectClass.html).

[AuthorityEntry](dcsAuthorityEntryClassAuthorityEntryConstructors.html) constructors create a single authority descriptor. [ AuthorityType](dcsAuthorityEntryClassAuthorityTypeField.html) establishes the access capabilitities and limitations (add, change, exclude, management, etc.). [ UserName](dcsAuthorityEntryClassUsernameField.html) establishes the user or group profile name associated with the access authority. [IsGroupAccount](dcsAuthorityEntryClassUsernameField.html) indicates if the **Username** is a user or group profile.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AuthorityEntry Class Members](dcsAuthorityEntryMembers.html)
      <br />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [IAdgObject.AuthorityEntries 
					Property](dcsIAdgObjectClassAuthorityEntriesProperty.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

