---
title: DatabaseName.ToSourceProfile(string, bool, bool, bool)

Id: dcsDatabaseNameClassToSourceProfileMethod4
TocParent: dcsDatabaseNameClassToSourceProfileMethods
TocOrder: 1

---

Named SourceProfile optionally constructed from a registered database name. If constructing from registered database name, optionally throw exception if duplicate IDs are discovered in the registry and DataGate.config. 
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public static SourceProfile ToSourceProfile( ,
   string dbName
   bool bFromSecStorage
   bool bDetectDuplicates
   bool bClassic
);** 
      </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Sub ToSourceProfile(_ 
   ByVal dbName As String_
   ByVal bFromSecStorage As Boolean
   ByVal bDetectDuplicates
   ByVal bClassic
) As SourceProfile** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc ToSourceProfile Access(*Public) Type(SourceProfile)
   DclSrParm dbName Type (*String)
   DclSrParm bFromSecStorage Type (*Boolean)
   DclSrParm bDetectDuplicates Type (*Boolean)
   DclSrParm bClassic Type (*Boolean)** 
      </pre>

Parameters

<dl>
        <dt>
 *dbName* 
        </dt>
        <dd>
 **String** . The name of the database.  </dd>
        <dt>
 *bFromSecStorage* 
        </dt>
        <dd>
 **Boolean.**  If True to attempt to read a "classic" 
        database name from the Windows Registry, if dbName is not found in the
        DataGate config file.  This is the default behavior of the overloads of this
        method which do not specify this parameter. If "False" ignore the 
        database names in the Windows registry.
</dd>
		<dt>
 *bDetectDuplicates* 
        </dt>
        <dd>
 **Boolean.**   If True, and database names exist for the value given by the dbName 
       parameter in both the registry and in DataGate configuration files, an exception is thrown. 
       Ignored if <code>bFromSecStorage</code> is False.
</dd>
		<dt>
 *bClassic* 
        </dt>
        <dd>
 **Boolean.**   The value of this parameter has no effect unless
        <code>bFromSecStorage</code> is true.  In that case, only attempt to read the database 
		name specified by <code>dbName</code> from the Windows Registry, and ignore the 
		database names in the DataGate config file.
</dd>
</dl>

Returns

If <code>bFromSecStorage</code> is true, a SourceProfile instance read from the DataGate configuration file is returned, if it exists there, unless <code>bClassic</code> is true. Otherwise, a SourceProfile instance read from from the Windows Registry is returned, if it is found. If the value of <code>bFromSecStorage</code> is false, a default instance of SourceProfile is returned, with its DatabaseName property set to the value of the <code>dbName</code> parameter. 

[ASNA.DataGate.Providers.SourceProfile](dcsSourceProfileClass.html) <br /> 
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

