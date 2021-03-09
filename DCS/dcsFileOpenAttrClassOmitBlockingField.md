---
title: FileOpenAttr.OmitBlocking Field

Id: dcsFileOpenAttrClassOmitBlockingField
TocParent: dcsFileOpenAttrFields
TocOrder: 0

keywords: OmitBlocking field
keywords: FileOpenAttr.OmitBlocking field

keywords: network blocking factor, default
keywords: how to, network blocking factor default
keywords: database files, network blocking factor default
keywords: files, network blocking factor default

---

This constant, when assigned to the [ BlockingFactor](dcsFileOpenAttrClassBlockingFactorProperty.html) property, causes DataGate to omit the record blocking feature in the [FileAdapter.Open](dcsFileAdapterClassOpenMethod.html) method. This is the default value of the **BlockingFactor** property.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **Public static int OmitBlocking** 
      </pre>
      <pre class="prettyprint">       <span class="lang">[Visual Basic] </span>
 **Public Property OmitBlocking As Integer** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **DclFld Name(OmitBlocking) Type(*Integer) Access(*Public)** 
      </pre>

Field
 Value

Integer. A constant value to set the **BlockingFactor** property.
Remarks

Two special values are recognized for the **BlockingFactor** property. [OptimalBlockingFactor](dcsFileOpenAttrClassOptimalBlockingFactorField.html) tells DataGate to calculate the best-fit size of the record buffer, using factors such as record length and network packet size. In most cases, **OptimalBlockingFactor** will yield the best network blocking performance. **OmitBlocking** is the default value of **BlockingFactor** signifying that all record blocking features will be omitted.
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span> AdgConnection db = new AdgConnection("*Public/DG
  NET Local"); FileAdapter dbFile = new FileAdapter(db,
  "*Libl/CMASTNEWL1", "CMMASTERL1"); dbFile.AccessMode
  = AccessMode.Read; /* Omits record blocking feature. */
  dbFile.OpenAttributes.BlockingFactor = FileOpenAttr.OmitBlocking;
  AdgDataSet ds = null;
  dbFile.OpenNewAdgDataSet(out ds);</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span> Dim db As New AdgConnection("*Public/DG NET
  Local") Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEWL1",
  "CMMASTERL1") dbFile.AccessMode =
  AccessMode.Read ' Automatically omits record blocking feature. 
  dbFile.OpenAttributes.BlockingFactor = FileOpenAttr.OmitBlocking
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
      [OptimalBlockingFactor 
					Field](dcsFileOpenAttrClassOptimalBlockingFactorField.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [Open Method](dcsFileAdapterClassOpenMethod.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

