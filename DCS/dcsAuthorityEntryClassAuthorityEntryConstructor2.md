---
title: AuthorityEntry(string)

Id: dcsAuthorityEntryClassAuthorityEntryConstructor2
TocParent: dcsAuthorityEntryClassAuthorityEntryConstructors
TocOrder: 1

---

<span>Creates a new instance of <span> **AuthorityEntry** </span> with all fields except **Username** initialized to default values</span>. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public AuthorityEntry(
   string username
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub AuthorityEntry( _
   ByVal username As String
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegConstructor AuthorityEntry Access(*Public)
   DclSrParm username Type(*String)** 
      </pre>

Parameters

<dl>
        <dt>
 *username* 
        </dt>
        <dd>

**String** . A non-group profile name. See the [ UserName](dcsAuthorityEntryClassUsernameField.html) field.
</dd>
</dl>

Exceptions

None.
Remarks

Only use this constructor when *username* is a single user profile (rather than a group profile) since [ IsGroupAccount](dcsAuthorityEntryClassUsernameField.html) is initialized **False** . The **Username** field is initialized with *username* .

This constructor initializes the [ AuthorityType](dcsAuthorityEntryClassAuthorityTypeField.html) field to **Use** .
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
      [UserName Field](dcsAuthorityEntryClassUsernameField.html)
      <br />
      [AuthorityType Field](dcsAuthorityEntryClassAuthorityTypeField.html)
      <br />
      [IsGroupAccount Field](dcsAuthorityEntryClassUsernameField.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

