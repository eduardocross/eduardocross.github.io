---
title: FileOpenAttr.OptimalBlockingFactor Field

Id: dcsFileOpenAttrClassOptimalBlockingFactorField
TocParent: dcsFileOpenAttrFields
TocOrder: 1

keywords: OptimalBlockingFactor field
keywords: FileOpenAttr.OptimalBlockingFactor field
keywords: network blocking factor, calculate
keywords: how to, calculate network blocking factor
keywords: database files, network blocking factor calculated
keywords: files, network blocking factor calculated

---

This constant, when assigned to the **BlockingFactor** property, requests that DataGate calculate the best-fit size of the network blocking record buffer.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **Public static int OptimalBlockingFactor**  </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **public Property OptimalBlockingFactor As Integer**  </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp OptimalBlockingFactor Type(*Integer) Access(*Public)** 
      </pre>

Field
 Value

Integer. A constant value to set the [ BlockingFactor](dcsFileOpenAttrClassBlockingFactorProperty.html) property.
Remarks

This constant, when assigned to the **BlockingFactor** property, requests that DataGate calculate the best-fit size of the network blocking record buffer, using factors such as record length and network packet size. In most cases, this yields the best network blocking performance.
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1");
  dbFile.AccessMode = AccessMode.Read;
  /* Automatically calculates the best blocking factor. */
  dbFile.OpenAttributes.BlockingFactor = FileOpenAttr.OptimalBlockingFactor;
  AdgDataSet ds = null;
  dbFile.OpenNewAdgDataSet(out ds);</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1", "CMMASTERL1")
  dbFile.AccessMode = AccessMode.Read
  ' Automatically calculates the best blocking factor. 
  dbFile.OpenAttributes.BlockingFactor = FileOpenAttr.OptimalBlockingFactor
  Dim ds As AdgDataSet = Nothing
  dbFile.OpenNewAdgDataSet(ds)
</pre>

Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileOpenAttr Class](dcsFileOpenAttrClass.html)
      <br />
      [FileOpenAttr Class Members](dcsFileOpenAttrClassMembers.html)
      <br />
      [BlockingFactor Property](dcsFileOpenAttrClassBlockingFactorProperty.html)
      <br />
      [ASNA.DataGate.Providers 
					Namespace](dcsDataGateProvidersNamespace.html)

