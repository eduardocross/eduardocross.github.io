---
title: SourceProfile.Unregister Method

Id: dcsSourceProfileClassUnregisterMethod
TocParent: dcsSourceProfileMethodsMain
TocOrder: 7

keywords: Unregister method
keywords: SourceProfile.Unregister method
keywords: Windows registry, delete database names from
keywords: database names, delete from registry
keywords: registered database names, delete
keywords: database connections, registry database name deleted
keywords: connections, database name registry delete
keywords: how to, delete database name from registry

---

## <span style="font-color:red">Deprecated</span>
Deprecated by [DatabaseName.Unregister](DCSDataBaseNameClassUnregisterMethod.html)

Deletes a registered database name from the system registry.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public static void Unregister(<br />   string dbName<br />);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Shared Sub Unregister( _<br />   ByVal dbName As String _<br />)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Unregister Access(*Public) Shared(*Yes)<br />   DclSrParm dbName Type(*String)** 
      </pre>

Parameters

<dl>
        <dd />
        <dt>
 *dbName* 
        </dt>
        <dd>	A string identifying the registered database name to delete.
						</dd>
</dl>

Exceptions

None.
Examples 

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  /* Open up and unregistered the database profile "Worthless Db". */
  try
  {
      SourceProfile.Unregister("Worthless Db");
  }
  catch(dgException)
  {
      MessageBox.Show("\"Worthless DB\" is not a 
            registered database profile.",
          "Could not unregister.");
      return;
  }</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Open up and unregistered the database profile "Worthless Db".
  Try
      SourceProfile.Unregister("Worthless Db")
  Catch dgEx As dgException
      MsgBox("""Worthless DB"" is not a registered 
            database profile.", _
      MsgBoxStyle.Critical, "Could not unregister.")
      Return
  End Try</pre>

Requirements

**Namespace: [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html)** 

**Assembly:** ASNA DataGate Client 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016,Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html) <br />
	  [SourceProfile Class Members](dcsSourceProfileMembers.html) <br />
	  [Register Method](dcsSourceProfileClassRegisterMethod.html)<br />
	  [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

