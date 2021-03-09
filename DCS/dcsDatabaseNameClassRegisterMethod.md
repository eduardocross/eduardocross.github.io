---
title: DatabaseName.Register Method

Id: dcsDatabaseNameClassRegisterMethod
TocParent: dcsDatabaseNameMethods
TocOrder: 4

keywords: Register method
keywords: DatabaseName.Register method
keywords: Windows registry, register database names
keywords: database names, create and update registry
keywords: registered database names, create and update
keywords: connections, database named registered
keywords: database connections, registry database name created or updated
keywords: how to, update registered name of database
keywords: how to, create registered name of database

---

Saves the contents of the **SourceProfile** object to the system registry as a database name. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public static SourceProfile Register(
   SourceProfile sp
   String dbName
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Shared Register( _
   ByVal sp As [SourceProfile](dcsSourceProfileClass.html) _
   ByVal dbName As String _
) As SourceProfile** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc Register Type(SourceProfile) Access(*Public)
   DclSrParm sp Type(SourceProfile)
   DclSrParm dbName Type (String)** 
      </pre>

Parameters

<dl>
        <dt>
 *sp* 
        </dt>
        <dd>
 **SourceProfile** object to be registered. </dd>
        <dt>
 *dbName* 
        </dt>
        <dd>
 **String** . The name of the database name to 
									delete. </dd>
</dl>

Returns

[SourceProfile](dcsSourceProfileClass.html).

#### Requirements
**Namespace: [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html)** 

**Assembly:** ASNA DataGate Client 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro 
See Also

<dl />
      [DatabaseName Class](dcsDatabaseNameClass.html)
      <br />
      [DatabaseName Class Members](dcsDatabaseNameMembers.html)
      <br />
      [Unregister Method](dcsDatabaseNameClassUnregisterMethod.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

