---
title: ILibraryList.UserConfig Property

Id: dcsILibraryListClassUserConfigProperty
TocParent: dcsILibraryListProperties
TocOrder: 3

keywords: UserConfig property
keywords: ILibraryList.UserConfig property
keywords: directories, setting user portion of available directories in the library list
keywords: directories, getting user portion of available directories in the library list
keywords: library lists, setting user portion of available directories in
keywords: library lists, getting user portion of available directories in
keywords: how to, set user portion of available directories in the library list
keywords: how to, get user portion of available directories in the library list

---

**UserConfig** sets or returns a string array containing a list of the user portion of the available directories in the library list represented by **ILibraryList** . 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string[] UserConfig { get;  set}** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Property UserConfig As String()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp UserConfig Type(*string) Access(*Public) Rank(1)
     BegGet;  BegSet** 
      </pre>

Property Value

**String array** . A string array containing a list of the user portion of the available directories in the library list represented by **ILibraryList** .
Remarks

Use [SystemConfig](dcsILibraryListClassSystemConfigProperty.html) property to set and return the system and user portion of the available library list.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [ILibraryList Class](dcsILibraryListClass.html)
      <br />
      [ILibraryList Class Members](dcsILibraryListMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

