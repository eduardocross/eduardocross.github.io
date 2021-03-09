---
title: SourceProfile.InitialLibl Property

Id: dcsSourceProfileClassInitialLiblProperty
TocParent: dcsSourceProfilePropertiesMain
TocOrder: 1

keywords: InitialLibl property
keywords: SourceProfile.InitialLibl property
keywords: initial library list, getting
keywords: get initial library list
keywords: database files, get initial library list

---

Gets and sets the current database’s initial library list. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string[] InitialLibl { get; set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Property InitialLibl As String()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp InitialLibl Type(*String) Rank(1) Access(*Public)** 
      </pre>

Property Value

[ SourceProfile](dcsSourceProfileClass.html). (get/set)
Remarks

Gets or sets the initial library list for this database.
Examples

<pre class="prettyprint">
        <span class="lang">
 **[C#]** 
        </span>
  /* This code will update the database name "SalesDB" to include
   * "IMPORTS" in its library list. */
  SourceProfile sp = new SourceProfile("SalesDB");
  string[] newList = new string[sp.InitialLibl.Length + 1];
  int i;
  for (i = 0; i &lt; sp.InitialLibl.Length; i ++)
  {
      newList[i] = sp.InitialLibl[i];
  }
  newList[i] = "IMPORTS";
  sp.InitialLibl = newList;
  sp.Register();</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' This code will update the database name "SalesDB" to include
  ' "IMPORTS" in its library list. 
  Dim sp As New SourceProfile("SalesDB")
  Dim newList(sp.InitialLibl.Length) As String
  Dim i As Integer
  For i = 0 To sp.InitialLibl.Length - 1
      newList(i) = sp.InitialLibl(i)
  Next i
  newList(i) = "IMPORTS"
  sp.InitialLibl = newList
  sp.Register()</pre>

Requirements

**Namespace:** [ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html)

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span> 
See Also

<dl />
      [SourceProfile Class](dcsSourceProfileClass.html) <br />
      [SourceProfile Class Members](dcsSourceProfileMembers.html)<br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

