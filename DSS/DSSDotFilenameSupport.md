---
title: Filenames Including Periods

Id: DSSDotFilenameSupport
TocParent: DSSOperation
TocOrder: 60

keywords: ASNA DataGate
keywords: ASNA DataGate&#174; for SQL Server
keywords: DSS
keywords: Period filenames
keywords: Filenames including periods 
keywords: Filenames with .

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">[
				   ASNA DataGate&#174; for SQL Server Reference Manual
				   ](Welcome.html)</span></td>
			    </tr>
</table>

# Filenames Including "."

---

<br />

**<span style='font-size:10.0pt;font-family:Arial'>Contents</span>** 

<span style='font-size:9.0pt;font-family:Arial;'>Object Names with '.'</span> 

<span style='font-size:9.0pt;font-family:Arial'>Limited Support for DataGate&#174; Objects with '.''</span> 

<span style='font-size:9.0pt;font-family:Arial;'>Object Names with '.' and SQL Server 'Schema'</span> 

<span style='font-size:9.0pt;font-family:Arial;'>Specify '.' Mapping and Syntax with dgserver.exe</span> 

<span style='font-size:9.0pt;font-family:Arial;'>Specify the Desired Syntax using the Registry</span> 

<span style='font-size:9.0pt;font-family:Arial;'>Unsupported '.' Access</span> 

### Object Names with '.'
Although SQL Server permits object names that contain '.', two significant problems arise when using such names in DataGate&#174; for SQL Server (DSS). First, SQL Server uses '.' as a separator character when an object's owner, database, and/or server are explicitly part of the object name, e.g., "<code>myserver.mydatabase.me.myobject</code>", or "<code>me.myobject</code>". This release resolves this problem as detailed below (see Object Names with '.' and SQL Server 'Schema'). The second problem arises from a bug in the SQL Server access API used by DSS, <code>OLEDB</code>. <code>OLEDB</code> does not support using names with '.' in its rowset update API. Thus, DataGate&#174; cannot generally support them either. However, this release includes support for a workaround that may suffice in some application scenarios. 

### Limited Support for DataGate&#174; Object Names with '.' 
DataGate&#174; can be configured to use an alternate character for specifying DataGate&#174; object names containing '.' to SQL Server. For example, a DataGate&#174; file may be named "<code>my.file</code>". When using the configuration to replace '.' with, say, '_', the underlying SQL Server table would be named "<code>my_file</code>". In this configuration, all DSS interface calls to SQL Server will specify <code>my_file</code> instead of <code>my.file</code>. To a DataGate&#174; user, it appears that object names may contain '.'. 

There are limits the user must be aware of when using this support: 1) All object names containing the replacement characters will be exposed to DataGate&#174; users as objects names containing '.' instead. For example, a DataGate&#174; Studio user might find a file named "<code>new.file</code>" in a DSS library, and subsequently try to create a new file named "<code>new_file</code>" in the same library. In this case, DSS will return a "duplicate object" error, because SQL Server already has an object named "<code>new_file</code>" (mapped to DataGate&#174; as "<code>new.file</code>"). Similarly, rename and delete operations can be problematic. 2) This support is not the default DSS behavior; all new DSS deployments will need to be configured to use the support. 3) When using SQL Server "schema" as part of a DataGate&#174; object name, a particular path name syntax is required (as outlined in the next section) when using this support.

### Object Names with '.' and SQL Server 'Schema'
In previous releases, DSS reserved '.' as a separator when specifying the "schema" (owner name) of an object (physical file, logical file, index), e.g., 
<pre>/libname/schemaname.file</pre>

Since this conflicts with the use of '.' in DataGate&#174; object names, the syntax is now deprecated, and only available when DSS is started with a special registry value, as mentioned below. The new syntax allows an object to use '.' in an object name, and specify the schema as a prefix with brackets, e.g.,
<pre>/libname/[schemaname]my.file</pre>

The new syntax is used by default when installing and starting DSS. Since existing applications may be dependent on the old syntax, DSS will modally support either syntax. DSS chooses which syntax to use once, at the time the DataGate&#174; Service is started, and will use the indicated syntax for all client/server database connections until the service is stopped. The syntax to use is indicated by a registry key value as detailed below. If no value is found in the registry, the new syntax is used by default. Note that DSS cannot simultaneously support both the old syntax and '.' in object names.

### Specify '.' Mapping and Syntax with dgserver.exe 
dgserver.exe is the command-line installer for the DataGate&#174; Service, which handles DSS server requests from clients. <code>dgserver.exe </code>is usually invoked by the DataGate&#174; Server installer, but may also be used by a command-line user. dgserver.exe accepts several optional parameters (invoke '<code>dgserver.exe -?</code>' to see a list), but requires either '<code>-i</code>' or '<code>-u</code>' to install or uninstall, respectively, the DataGate&#174; Service. 

You may specify the '<code>-s</code>' parameter with '<code>-i</code>', indicating that DSS will use the deprecated syntax. Likewise, omitting '<code>-s</code>' when '<code>-i</code>' is specified indicates that DSS will use the new syntax.

To have dgserver.exe to configure a '.' mapping character as part of the installation, you may specify the '<code>-k</code>' parameter. '<code>-k</code>' is used to specify arbitrary named values to be added to the installation, and so it is expected to be immediately followed by two other command line parameters: the name, and the value. In this case, the name is "DSS Object Name Dot Substitution", and the value should be a valid SQL Server object name character other than '.', for example "_". In this case the entire command could be given as 
<pre>dgServer.exe -i -k "DSS Object Name Dot Substitution" "_"</pre>

Note that the use of quotes to specify the name "DSS Object Name Dot Substitution" is critical; otherwise the Windows command line shell will interpret the space-delimited words as separate parameters. Also note that DSS gives this specification more weight than the '<code>-s</code>' parameter. If '<code>-s</code>' were added to the above command, DSS would ignore the '<code>-s</code>' and use the new syntax with the specified object name mapping.

### Specify the Desired Syntax Using the Registry
When the dgserver.exe command-line tool mentioned previously is invoked, the installer simply creates the proper Windows Registry key value(s) to specify the desired configuration. The key values are then referenced by DSS when the service starts. The key values may also be edited with the Windows Registry Editor (regedit.exe). The key and values are: 
<pre>[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\DataGate&#174; Server]
"Use Old Schema Syntax"=dword:0
"DSS Object Name Dot Substitution"="_"</pre>

The <code>DWORD</code> value of "Use Old Schema Syntax", if present, may be either '1' or '0'. If the value is '<code>0</code>', not present, or "DSS Object Name Dot Substitution" has a value other than ".", DSS will use the new syntax when started. If the value is '<code>1</code>' and "DSS Object Name Dot Substitution" is not present or set to ".", DSS will use the old syntax.

### Unsupported '.' Access
Since this release uses the new schema syntax by default, many DataGate&#174; functions involving objects with '.' in the name may "just work" against a DSS deployment so configured, even without the "DSS Object Name Dot Substitution" key. Such functions include read-only record access, and many others. However, there are certain operations, such as a record update, that will produce errors and/or undefined behavior unless the mapping workaround is configured. Therefore, ASNA can only provide official support for '.' in object names against DSS configured to use the mapping configuration option. 
