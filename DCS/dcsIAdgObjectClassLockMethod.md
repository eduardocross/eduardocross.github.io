---
title: IAdgObject.Lock Method

Id: dcsIAdgObjectClassLockMethod
TocParent: dcsIAdgObjectMethods
TocOrder: 3

keywords: Lock method
keywords: IAdgObject.Lock method
keywords: WaitOptions enumeration, used by
keywords: ShareTypes enumeration, used by
keywords: enumerations [DCS 16.0 WaitOptions, used by
keywords: enumerations [DCS 16.0 ShareTypes, used by
keywords: how to, set database object lock restrictions
keywords: database objects, set lock restrictions
keywords: lock restrictions, set for database objects

---

**Lock** engages the database provider's object locking facility to set a lock restricting access to the database object corresponding to **IAdgObject** .
<pre>        <span class="lang">[C#]</span>
 **Public void IAdgObject Lock(
   [ShareTypes](dcsShareTypesEnumeration.html) ShareType ,
   [WaitOptions](dcsWaitOptionsEnumeration.html) WaitOption ,
   Short WaitTime
);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Sub Lock(
   ByVal ShareType As [ShareTypes](dcsShareTypesEnumeration.html) _
   ByVal WaitOption As [WaitOptions](dcsWaitOptionsEnumeration.html) _
   ByVal WaitTime As short
) As IAdgObject** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Lock Access(*Public) Type (IAdgObject)
   DclSrParm ShareType Type([ShareTypes](dcsShareTypesEnumeration.html))
   DclSrParm WaitOption Type([WaitOptions](dcsWaitOptionsEnumeration.html))
   DclSrParm WaitTime Type(short)** 
      </pre>

Parameters

<dl>
        <dt>
 *ShareType* 
        </dt>
        <dd>
[ShareTypes](dcsShareTypesEnumeration.html). The type of lock to be set. 
</dd>
        <dt>
 *WaitOption* 
        </dt>
        <dd>
[WaitOptions](dcsWaitOptionsEnumeration.html). Specifies how **Lock** reacts when the requested lock is not immediately available.
</dd>
        <dt>
 *WaitTime* 
        </dt>
        <dd>
**System.Short** . The time in seconds to wait for a held lock to become available, subject to *WaitOption* .
</dd>
</dl>

Exceptions

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col span="1" valign="top" style="FONT-WEIGHT: bold" width="20%" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							ExceptionType</th>
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

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the <span>dgException.Error</span> property.
<br />

<table class="dtTABLE" id="Table2" cellspacing="0">
          <colgroup span="1">
            <col span="1" valign="top" style="FONT-WEIGHT: bold" width="20%" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value of dgException.Error</th>
            <th colspan="1" rowspan="1">
							Condition</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBUSYOBJ
</td>
            <td colspan="1" rowspan="1">

The lock specified by *ShareType* was not granted due to the lock being held by another session (see Remarks below).
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

The **Lock** and [ Unlock](dcsIAdgObjectClassUnlockMethod.html) methods engage the database's object locking facilities allowing programs to enforce some degree of data coherency in a multiprocessing system. The target of these methods is the pre-existing database object corresponding to **IAdgObject** . The details of object locking are dependent upon the database provider, but **Lock** and **Unlock** allow selective control of one of a set of "share types", as given by *ShareType* . 

Generally, when an object lock is granted with a successful call to the **Lock** method, the lock remains in effect until <u>one</u> of the following occurs: 

1. The lock is removed with a successful call to **Unlock.**
2. The database session ends (the [AdgConnection](dcsAdgConnectionClass.html) object associated with **IAdgObject** is closed or disposed).
3. A database administrator forcibly removes the lock.

Note that a granted lock is not automatically removed when the **IAdgObject** is disposed, unless this results in the auto-disposal of the associated **AdgConnection** object. Programs should explicitly remove granted locks with the **Unlock** method prior to disposing of an **IAdgObject** instance.

When the database cannot immediately grant a requested lock, **Lock** responds as indicated by *WaitOption* . This parameter directs **Lock** to either wait (indefinitely, or for *WaitTime* seconds) for the lock to become available, or to immediately throw an exception. &amp; **Default** for *WaitOption* specifies the databases's default response. 

Ultimately, if a lock cannot be granted, **Lock** throws **dgException** with the **Error** property set to **dgEmBUSYOBJ.** 

*WaitTime* is ignored if *WaitOption* has any value other than **Definite** . 
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [Unlock Method](dcsIAdgObjectClassUnlockMethod.html)
      <br />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [WaitOptions Enumeration](dcsWaitOptionsEnumeration.html)
      <br />
      [ShareTypes Enumeration](dcsShareTypesEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

