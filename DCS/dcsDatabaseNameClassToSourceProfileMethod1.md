---
title: DatabaseName.ToSourceProfile(String)

Id: dcsDatabaseNameClassToSourceProfileMethod1
TocParent: dcsDatabaseNameClassToSourceProfileMethods
TocOrder: 0

---

Converts the named database into a SourceProfile object.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public static SourceProfile ToSourceProfile( ,
   string dbName
);** 
      </pre>

<pre class="prettyprint">        [Visual Basic] **Public Sub ToSourceProfile(_ 
   ByVal dbName As String_
) As SourceProfile** 
      </pre>

      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc ToSourceProfile Access(*Public) Type(SourceProfile)
   DclSrParm dbName Type (*String)** 
      </pre>

Parameters

<dl>
        <dt>
 *dbName* 
        </dt>
        <dd>
 **String** . The name of the database. </dd>
</dl>

Returns

[ASNA.DataGate.Providers.SourceProfile](dcsSourceProfileClass.html) <br /> 
Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [DatabaseName Class](dcsDatabaseNameClass.html)
      <br />
      [DatabaseName Class Members](dcsDatabaseNameMembers.html)
      <br />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

