---
title: AuthorityEntry.Username Field

Id: dcsAuthorityEntryClassUsernameField
TocParent: dcsAuthorityEntryFields
TocOrder: 2

keywords: AuthorityEntry.Username field
keywords: Username field
keywords: how to, establish database authority user or group profile name
keywords: user profile names, establish for database authorities
keywords: group profile names, establish for database authorities
keywords: authorities, profile name established for database

---

**UserName** is the name of the group or user profile whose access capabilities are defined by this [AuthorityEntry](dcsAuthorityEntryClass.html).
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string Username** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Property Username As string** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **DclFld Name(Username) Type(*string) Access(*Public) Shared(*Yes)** 
      </pre>

Field
 Value

String. A user or group profile name known to the database provider.
Remarks

An **AuthorityEntry** instance describes an authorization for exactly one profile name specified by **Username** . This may name a single-user profile known to the database provider, such as the user profile for the session (see also [SourceProfile.User](dcsSourceProfileClassUserProperty.html)). It may otherwise name a group profile or profile class as defined by the database provider (for example, "*PUBLIC", typically found in IBM i databases) The distinction between group and user profile names in **AuthorityEntry** is given by the [IsGroupAccount](dcsAuthorityEntryClassUsernameField.html) field.

Many database providers honor the string "*Current", which is a generic specification for the user profile associated with the current session. When this is used for the value of **Username** , **IsGroupProfile** should be **False** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AuthorityEntry Class](dcsAuthorityEntryClass.html)
      <br />
      [IsGroupAccount Field](dcsAuthorityEntryClassUsernameField.html)
      <br />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [User Property](dcsSourceProfileClassUserProperty.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

