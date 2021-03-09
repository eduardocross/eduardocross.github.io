---
title: FileOpenAttr.WaitForFile Property

Id: dcsFileOpenAttrClassWaitForFileProperty
TocParent: dcsFileOpenAttrProperties
TocOrder: 6

keywords: WaitForFile property
keywords: FileOpenAttr.WaitForFile property
keywords: database files, wait time for access to
keywords: files, wait time for access to
keywords: time, wait for file access
keywords: how to, wait for file access

---

Time, in seconds, that a process will wait to access a file.
<pre>        <span class="lang">[C#]</span>
 **Public int WaitForFile { get; set; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Property WaitForFile As Integer** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp WaitForFile Type(*Integer) Len(4) Access(*Public)<br />   BegGet, BegSet** 
      </pre>

Property Value

Integer. Returns or sets the amount of time (in seconds) that a process will wait to access a file.
Remarks

The timeout specified with <span> **WaitForFile** </span> applies to the [FileAdapter](dcsFileAdapterClass.html) open methods. If the resources required for opening the file, including access mode and sharing request, are not immediately available, the database provider will block the operation for a time period not exceeding the number of seconds specified in <span> **WaitForFile** </span>. If the resources become available during this period, the file will be opened. Otherwise, an exception will be thrown.

When set, <span> **WaitForFile** </span> overrides any default specified when the file was created. **WaitForFile** is a feature of the database provider and may not be available for all providers.

**Implementation on the IBM i:** The [ShareType](dcsFileOpenAttrClassShareTypesProperty.html) property is supported via the ALCOBJ command. When specified with **WaitForFile** , the ALCOBJ command is passed the value of **WaitForFile** in the WAIT parameter. The valid values for this parameter are 0 (indicating no wait), and 30-32767 (indicating that the program should wait that number of seconds for the command to time-out). DCS will accept any valid integer value for the **WaitForFile** command. DataGate for IBM i will translate the value, such that any value less than 1 is specified as WAIT(0). Also, any value greater than 0 and less than 31 is specified as WAIT(30). Finally, any value greater than 32767 is specified as WAIT(32767).
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
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

