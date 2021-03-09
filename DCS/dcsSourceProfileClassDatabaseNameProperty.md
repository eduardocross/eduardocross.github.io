---
title: SourceProfile.DatabaseName Property

Id: dcsSourceProfileClassDatabaseNameProperty
TocParent: dcsSourceProfilePropertiesMain
TocOrder: 0

keywords: DatabaseName property
keywords: SourceProfile.DatabaseName property
keywords: database names, for set of connection parameters
keywords: Windows registry, database name for connection retrieved
keywords: registered database names, retrieved for connection
keywords: database connections, registry names retrieved for connection
keywords: connections, database name currently registered
keywords: how to, retrieve database name of connection

---

The database name (or identifier) of this set of connection parameters.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string DatabaseName { get; }**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property DatabaseName As String**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp DatabaseName Type(*String) Access(*Public)<br />   BegGet** 
      </pre>

Property Value

String. Read-only. Returns the parameter passed to the **SourceProfile** [constructor](dcsSourceProfileConstructorsMain.html) which created this object. If this **SourceProfile** was instantiated by other means, the value is an empty string.
Examples 

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  /* This code displays all of the *PUBLIC database
   * names, along with their descriptive text, to the list view
   * "lvDbNames" whose view is set to "View.Details". */
  ListViewItem newItem;
  SourceProfile currentProfile;
  foreach(string name in SourceProfile.GetNames(true))
  {
      currentProfile = new SourceProfile(name);
      newItem = new ListViewItem(currentProfile.DatabaseName);
      newItem.SubItems.Add(currentProfile.Text);
      lvDbNames.Items.Add(newItem);
  }</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' This code displays all of the *PUBLIC database
  ' names, along with their descriptive text, to the listview
  ' "lvDbNames" whose view is set to "View.Details". 
  Dim newItem As ListViewItem
  Dim currentProfile As SourceProfile
  For Each name As String In SourceProfile.GetNames(True)
      currentProfile = New SourceProfile(name)
      newItem = New ListViewItem(currentProfile.DatabaseName)
      newItem.SubItems.Add(currentProfile.Text)
      lvDbNames.Items.Add(newItem)
  Next
</pre>

Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span> 
See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html) <br />
	  [SourceProfile Class Members](dcsSourceProfileMembers.html)<br />
	  [SourceProfile Class Constructors](dcsSourceProfileConstructorsMain.html)<br />
	  [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

