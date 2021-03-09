---
title: IAdgObject.Unlock Method

Id: dcsIAdgObjectClassUnlockMethod
TocParent: dcsIAdgObjectMethods
TocOrder: 10

keywords: Unlock method
keywords: IAdgObject.Unlock method
keywords: ShareTypes enumeration, used by
keywords: enumerations [DCS 16.0 ShareTypes, used by
keywords: database connections, unlock when closing
keywords: connection resources, unlock when disposing
keywords: how to, remove database object lock restrictions
keywords: how to, unlock database object lock restrictions
keywords: database objects, unlock restrictions
keywords: lock restrictions, re-set for database objects
keywords: unlock restrictions, re-set for database objects
keywords: lock facitities, re-set restrictions for database objects

---

**Unlock** reverses the effects of a previously successful [Lock](dcsIAdgObjectClassLockMethod.html) method call.
<pre>        <span class="lang">[C#]</span>
 **Public void IAdgObject Unlock(<br />    [ShareTypes](dcsShareTypesEnumeration.html) ShareType ,<br />);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Sub Unlock(_<br />   ByVal ShareType As [ShareTypes](dcsShareTypesEnumeration.html) _<br />) As IAdgObject** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Unlock Access(*Public) Type (IAdgObject)
   DclSrParm ShareType Type([ShareTypes](dcsShareTypesEnumeration.html))** 
      </pre>

Parameters

<dl>
        <dt>
 *ShareType* 
        </dt>
        <dd>
[ShareTypes](dcsShareTypesEnumeration.html). The type of lock to be released.
</dd>
</dl>

Exceptions

<table class="dtTABLE" id="Table2" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="20%" style="FONT-WEIGHT: bold" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Exception Type</th>
            <th colspan="1" rowspan="1">
							Condition</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NullReferenceException 
</td>
            <td colspan="1" rowspan="1">

The [AdgConnection](dcsAdgConnectionClass.html) reference or path name string used to create the **IAdgObject** instance were null. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgException 
</td>
            <td colspan="1" rowspan="1">

See table below. 
</td>
          </tr>
</table>

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.

<table class="dtTABLE" id="Table3" cellspacing="0"> <colgroup span="1"> <col align="middles" span="1" width="20%" style="FONT-WEIGHT: bold" /> <col span="1" width="70%" /> </colgroup> <tr> <th colspan="1" rowspan="1"> Value of dgException.Error </th> <th colspan="1" rowspan="1"> Condition </th> </tr> <tr> <td colspan="1" rowspan="1"> <p>dgEmNOLOCK 
</td>
            <td colspan="1" rowspan="1">

The lock specified by *ShareType* was not previously granted by the **Lock** method or the lock has been otherwise removed (see Remarks below). 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOTFND 
</td>
            <td colspan="1" rowspan="1">

The database object the **IAdgObject** represents does not exist or is unavailable. 
</td>
          </tr>
</table>

Remarks

The [Lock](dcsIAdgObjectClassLockMethod.html) and **Unlock** methods engage the database's object locking facilities allowing programs to enforce some degree of data coherency in a multiprocessing system. The target of these methods is the pre-existing database object corresponding to **IAdgObject** . The details of object locking are dependent upon the database provider, but **Lock** and **Unlock** allow selective control of one of a set of "share types", as given by *ShareType* .

Generally, when an object lock is granted with a successful call to the **Lock** method, the lock remains in effect until <u>one</u> of the following occurs: 

1. The lock is removed with a successful call to **Unlock.**
2. The database session ends (the **AdgConnection**  object associated 
					with **IAdgObject** 
				is closed or disposed).
3. A database administrator forcibly removes the lock.

Note that a granted lock is not automatically removed when the **IAdgObject** is disposed, unless this results in the auto-disposal of the associated **AdgConnection** object. Programs should explicitly remove granted locks with the **Unlock** method prior to disposing of an **IAdgObject** instance. 
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [Lock Method](dcsIAdgObjectClassLockMethod.html)
      <br />
      [ShareTypes Enumeration](dcsShareTypesEnumeration.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

