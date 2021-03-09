---
title: FileOpenAttr.InhibitWrites Property

Id: dcsFileOpenAttrClassInhibitWriteProperty
TocParent: dcsFileOpenAttrProperties
TocOrder: 3

keywords: how to, enable write access to database files
keywords: how to, disable write access to database files during testing
keywords: database files, write-access enabled
keywords: database files, write-access disabled
keywords: files, write-access enabled
keywords: files, write-access disabled
keywords: write-access enabled
keywords: write-access disabled
keywords: InhibitWrites property
keywords: FileOpenAttr.InhibitWrites property

---

Specify write-access enabling on the open file.
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **Public bool InhibitWrite { get; set; }**  </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Property InhibitWrite As Boolean**  </pre>
      <pre class="prettyprint">        <span class="lang">[Visual RPG]</span>
 **BegProp InhibitWrites Type(*Boolean) Access(*Public)<br />   BegGet, BegSet** 
      </pre>

Property Value

Boolean. If **true** , write access operations are silently disabled.
Remarks

This property can be used for application development and testing purposes to disable write operations (add, update, delete) on the open database file. When disabled, write operations are allowed (subject to the access mode specified when opening the file), but are effectively "no-ops" in regard to their effect on the database.

When the value of **InhibitWrites** is **False** or not specified, write operations are enabled on the open file.

<span> **InhibitWrites** </span> is a feature of the database provider and may not be available for all providers.
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
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

