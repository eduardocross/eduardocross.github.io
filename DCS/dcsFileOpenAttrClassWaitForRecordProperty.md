---
title: FileOpenAttr.WaitForRecord Property

Id: dscFileOpenAttrClassWaitForRecordProperty
TocParent: dcsFileOpenAttrProperties
TocOrder: 7

keywords: WaitForRecord property
keywords: FileOpenAttr.WaitForRecord property
keywords: records, wait time to access
keywords: database files, wait time for record access
keywords: files, wait time for access to record
keywords: time, wait for record access
keywords: how to, wait for record access

---

Time, in seconds, that a process will wait for access to a record.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **Public int WaitForRecord { get; set; }** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Property WaitForRecord As Integer** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp WaitForRecord Type(*Integer) Len(4) Access(*Public)<br />   BegGet, BegSet** 
      </pre>

Property Value

Integer. Returns or sets the amount of time (in seconds) that a process will wait to access a record.
Remarks

The timeout specified with <span> **WaitForRecord** </span> applies to the [FileAdapter](dcsFileAdapterClass.html) access methods. If a record cannot be accessed, due to outstanding lock requests (including commitment control) for accessing that record, the database provider will block the operation for a time period not exceeding the number of seconds specified in **WaitForRecord** . If the record becomes available during this period, the operation will unblock. Otherwise, an exception will be thrown.

When set, <span> **WaitForRecord** </span> overrides any default specified when the file was created. <span> **WaitForRecord** </span> is a feature of the database provider, and may not be available for all providers.

Implementation on the IBM i: The [ShareType](dcsFileOpenAttrClassShareTypesProperty.html) property is supported via the ALCOBJ command. When specified with [ WaitForFile](dcsFileOpenAttrClassWaitForFileProperty.html) the ALCOBJ command is passed the value of **WaitForFile** in the WAIT parameter. The valid values for this parameter are 0 (indicating no wait), and 30-32767 (indicating that the program should wait that number of seconds for the command to time-out). DCS will accept any valid integer value for the **WaitForFile** command. DataGate for IBM i will translate the value, such that any value less than 1 is specified as WAIT(0). Also, any value greater than 0 and less than 31 is specified as WAIT(30). Finally, any value greater than 32767 is specified as WAIT(32767).
Examples 

<pre>        <span class="lang">
 **[C#]** 
        </span>
  /* Opens a record which will spend no time waiting for a record
   * if that record is locked. */
  AdgConnection db = new AdgConnection("*Public/DG NET Local");
  FileAdapter dbFile = new FileAdapter(db, "*Libl/CMASTNEW", "CMMASTER");
  dbFile.AccessMode = AccessMode.Delete;
  dbFile.OpenAttributes.WaitForRecord = 0;
  AdgDataSet myDS = null;
  dbFile.OpenNewAdgDataSet(out myDS);
</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Opens a record which will spend no time waiting For a record
  ' If that record is locked. 
  Dim db As New AdgConnection("*Public/DG NET Local")
  Dim dbFile As New FileAdapter(db, "*Libl/CMASTNEW", "CMMASTER")
  dbFile.AccessMode = AccessMode.Delete
  dbFile.OpenAttributes.WaitForRecord = 0
  Dim myDS As AdgDataSet = Nothing
  dbFile.OpenNewAdgDataSet(myDS)</pre>

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
      [ShareType Property](dcsFileOpenAttrClassShareTypesProperty.html)
      <br />
      [WaitForFile Property](dcsFileOpenAttrClassWaitForFileProperty.html)
      <br />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

