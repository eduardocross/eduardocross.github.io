---
title: DatabaseName.GetSourceProfiles Method

Id: dcsDatabaseNameClassGetSourceProfilesMethod
TocParent: dcsDatabaseNameMethods
TocOrder: 3

keywords: GetSourceProfiles method
keywords: DatabaseName.GetSourceProfiles method

---

Returns an array of [SourceProfile](dcsSourceProfileClass.html) objects currently registered for the database.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public static SourceProfile[] GetSourceProfiles(
   bool publicDbs
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Shared GetSourceProfiles( _
   ByVal publicDbs As Boolean _
) As [SourceProfile](dcsSourceProfileClass.html)[]** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc GetSourceProfiles Type(SourceProfile) Rank(1) Access(*Public) Shared(*Yes)
   DclSrParm publicDbs Type(*Boolean)** 
      </pre>

Parameters

<dl>
        <dt>
 *publicDbs* 
        </dt>
        <dd>
 **Boolean** . **True**  if this is a public 
						database.
					</dd>
</dl>

Returns

[SourceProfile](dcsSourceProfileClass.html) array of objects.
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

