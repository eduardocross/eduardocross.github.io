---
title: AdgDataSet.Initialize Method

Id: dcsAdgDataSetClassInitializeMethod
TocParent: dcsAdgDataSetMethods
TocOrder: 6

keywords: Initialize method
keywords: AdgDataSet.Initialize method
keywords: initialize, AdgDataSet class

---

Initialize an instance of **AdgDataSet** .
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public abstract void Initialize();** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public MustOverride Sub Initialize()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Initialize Access(*Public) Modifier(*MustOverride)** 
      </pre>

Remarks

**Initialize** is implemented by classes that inherit **AdgDataSet.** The method is called from the [ AdgDataSet Constructors](dcsAdgDataSetClassConstructorsMain.html) to initialize the object.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [AdgDataSet Class](dcsAdgDataSetClass.html)
      <br />
      [AdgDataSet Class Members](dcsAdgDataSetMembers.html)
      <br />
      [AdgDataSet Class Constructors](dcsAdgDataSetClassConstructorsMain.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

