---
title: SourceProfile.GetNames Method

Id: dcsSourceProfileClassGetNamesMethod
TocParent: dcsSourceProfileMethodsMain
TocOrder: 3

keywords: GetNames method
keywords: SourceProfile.GetNames method
keywords: Windows registry, database names retrieved from
keywords: registered database names, retrieved
keywords: database connections, registry names retrieved
keywords: connections, database names currently registered retrieved
keywords: how to, retrieve current registered database names

---

## <span style="font-color:red">Deprecated</span>
Replaced by [DatabaseName.GetNames](DCSDataBaseNameClassGetNamesMethod.html)

Returns the currently registered database names available for use in a program.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public static string[] GetNames(<br />   bool publicDbs<br />);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Shared GetName( _
   ByVal publicDbs As Boolean _
 ) As String()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc GetNames Type(*String) Rank(1) Access(*Public) Shared(*Yes)
   DclSrParm publicDbs Type(*Boolean)** 
      </pre>

Parameters

<dl>
        <dt>
 *publicDbs* 
        </dt>
        <dd>The public database.
					</dd>
</dl>

Returns

String. The currently registered database names available for use in a program.
Examples 

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  /* This code will fill a combo box with all of the available database
   * names. */
  foreach(string name in SourceProfile.GetNames(true)) /* Get *PUBLIC 
            databases. */
      cbDbName.Items.Add(name); /* NOTE: The names 
            appear without the "*PUBLIC/" prefix. */
  foreach(string name in SourceProfile.GetNames(false)) /* Get non public 
            databases. */
      cbDbName.Items.Add(name);</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' This code will fill a combo box with all of the available database
  ' names.
  For Each name As String In SourceProfile.GetNames(True) ' Get *PUBLIC 
            databases.
      cbDbName.Items.Add(name) ' ' NOTE: The names 
            appear without the "*PUBLIC/" prefix.
  Next
  For Each name As String In SourceProfile.GetNames(False) ' Get non public 
            databases.
      cbDbName.Items.Add(name)
  Next</pre>

Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span> 
See Also

<dl />
      <span>
        [SourceProfile Class](dcsSourceProfileClass.html) <br />[
						SourceProfile Class Members](dcsSourceProfileMembers.html)<br />[
						Register Method](dcsSourceProfileClassRegisterMethod.html)<br />[Unregister 
						Method](dcsSourceProfileClassUnregisterMethod.html)<br />[ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)</span>  

