---
title: DatabaseName.Unregister Method

Id: dcsDatabaseNameClassUnregisterMethod
TocParent: dcsDatabaseNameMethods
TocOrder: 7

keywords: Unregister method
keywords: DatabaseName.Unregister method
keywords: Windows registry, Unregister database names
keywords: database names, create and update registry
keywords: Unregistered database names, create and update
keywords: connections, database named Unregistered
keywords: database connections, registry database name created or updated
keywords: how to, update Unregistered name of database
keywords: how to, create Unregistered name of database

---

Deletes a registered database name from the system registry. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public void Unregister(
   String dbName
);** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Shared Unregister( _
   ByVal dbName As String _
) As void** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Unregister Type(*Void) Access(*Public)
   DclSrParm dbName Type (String)** 
      </pre>

Parameters

<dl>
        <dt>
 *dbName* 
        </dt>
        <dd>
 **String** . The name of the database. </dd>
</dl>

#### Requirements
**Namespace: [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html)** 

**Assembly:** ASNA DataGate Client 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [DatabaseName Class](dcsDatabaseNameClass.html)
      <br />
      [DatabaseName Class Members](dcsDatabaseNameMembers.html)
      <br />
      [UnUnregister Method](dcsDatabaseNameClassUnUnregisterMethod.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

