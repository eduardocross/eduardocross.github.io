---
title: DatabaseName.Deserialize Method

Id: dcsDatabaseNameClassDeserializeMethod
TocParent: dcsDatabaseNameMethods
TocOrder: 0

keywords: Deserialize method
keywords: DatabaseName.Deserialize method
keywords: database files, deserialize library objects from
keywords: database file members, deserialize from database
keywords: how to, deserialize database file objects
keywords: deserialize database

---

**Deserialize** reads the XML text and generates a SourceProfile object from its XML representation.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public static SourceProfile Deserialize( ,
   string tag ,
   string serSp
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub Deserialize(_ 
   ByVal tag As String_ 
   ByVal serSp As String_
) As SourceProfile** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc Deserialize Access(*Public) Type(SourceProfile)
   DclSrParm tag   Type(*String)
   DclSrParm serSp Type (*String)** 
      </pre>

Parameters

<dl>
        <dt>
 *tag* 
        </dt>
        <dd>Pending. </dd>
        <dt>
 *serSp* 
        </dt>
        <dd>String. The serialized database connection XML text file.
							</dd>
</dl>

Returns

ASNA.DataGate.Providers.SourceProfile.
Requirements

**Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [DatabaseName Class](dcsDatabaseNameClass.html)
      <br />
      [DatabaseName Class Members](dcsDatabaseNameMembers.html)
      <br />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

