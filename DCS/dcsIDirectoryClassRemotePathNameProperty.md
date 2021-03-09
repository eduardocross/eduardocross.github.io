---
title: IDirectory.RemotePathName Property

Id: dcsIDirectoryClassRemotePathNameProperty
TocParent: dcsIDirectoryProperties
TocOrder: 1

keywords: RemotePathName property
keywords: IDirectory.RemotePathName property 
keywords: remote path names, return for database library directory
keywords: remote path names, Acceler8DB compatibility
keywords: database libraries, return full path name of directory
keywords: how to, return full path name of directory for database library

---

**RemotePathName** is the full path name of a directory associated with the library represented by **IDirectory** , if any.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string RemotePathName{ get; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property RemotePathName As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp RemotePathName Access(*Public)Type (IDirectory)<br />       DclSrParm remotePathName Type(*String) Len(45)
    BegGet** 
      </pre>

Property Value <p> **String** . Returns the full path of a directory associated with the library, or an empty string. 
Remarks

This property is provided for compatibility with legacy Acceler8DB database systems. Only Windows-based "datalink" database providers support this property. See also [ AttachRemoteDirectory](dcsIDirectoryClassAttachRemoteDirectoryMethod.html).
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IDirectory Class](dcsIDirectoryClass.html)
      <br />
      [IDirectory Class Members](dcsIDirectoryMembers.html)
      <br />
      [AttachRemoteDirectory 
					Method](dcsIDirectoryClassAttachRemoteDirectoryMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

