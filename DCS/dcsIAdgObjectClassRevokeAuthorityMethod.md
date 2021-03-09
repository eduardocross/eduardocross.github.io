---
title: IAdgObject.RevokeAuthority Method

Id: dcsIAdgObjectClassRevokeAuthorityMethod
TocParent: dcsIAdgObjectMethods
TocOrder: 8

keywords: RevokeAuthority method
keywords: IAdgObject.RevokeAuthority method
keywords: AuthorityTypes enumeration, used by
keywords: enumerations [DCS 16.0 AuthorityTypes, used by
keywords: how to, re-set user authorities to a database object
keywords: user authorities, re-set access to a database object
keywords: database objects, re-set user authorities
keywords: authorities, re-set database access for a specific user
keywords: how to, revoke previously granted or denied authority to a database object
keywords: revoke authorities previously granted or denied to a database object

---

**RevokeAuthority** removes a previously granted or denied user authorization to a database object.
<pre>        <span class="lang">[C#]</span>
 **Public void IAdgObject RevokeAuthority(
   string userName
   [AuthorityTypes](dcsAuthorityTypesEnumeration.html) authorityType
);** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Sub RevokeAuthority( _
   ByVal userName As string _<br />   ByVal authorityType As [AuthorityTypes](dcsAuthorityTypesEnumeration.html)**  **) As IAdgObject** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr RevokeAuthority Access(*Public) Type(IAdgObject)** 
 **DclSrParm userName Type (*string)
   DclSrParm authorityType Type([AuthorityTypes](dcsAuthorityTypesEnumeration.html))** 
      </pre>

Parameters

<dl>
        <dt>
 *userName* 
        </dt>
        <dd>

**String** . The name of the user whose authority is being revoked.
</dd>
        <dt>
 *authorityType* 
        </dt>
        <dd>

[AuthorityTypes](dcsAuthorityTypesEnumeration.html). The authority being revoked for the user and [IAdgObject](dcsIAdgObjectClass.html).
</dd>
</dl>

Exceptions

<table class="dtTABLE" id="Table2" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" style="FONT-WEIGHT: bold" width="30%" />
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

The [AdgConnection](dcsAdgConnectionClass.html) or path name specified when the **IAdgObject** instance was created is null. 
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
<br />

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" style="FONT-WEIGHT: bold" width="20%" />
            <col span="1" width="70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value of dgException.Error
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVARG 
</td>
            <td colspan="1" rowspan="1">

The path name specified when the **IAdgObject** instance was created does not reference an existing database object, or *userName* is an empty string. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgENOTIMPL 
</td>
            <td colspan="1" rowspan="1">

This method is unavailable from the current database provider. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNONSECUREDB
</td>
            <td colspan="1" rowspan="1">

The method is unavailable because the database does not have the user security feature.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOAUTHLOCK
</td>
            <td colspan="1" rowspan="1">

The method is unavailable because the database provider could not allocate the pertinent security records.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsAS400ERROR
</td>
            <td colspan="1" rowspan="1">

The database provider encountered a system-level error. Details provided in the **dgException.Message** property.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINV400OP
</td>
            <td colspan="1" rowspan="1">

The database provider does not support this method for the object type represented by **IAdgObject** .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExDENIED
</td>
            <td colspan="1" rowspan="1">

Access to the method was denied by the database provider's "exit point" security support.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExINVLIC
</td>
            <td colspan="1" rowspan="1">

The database provider's "exit point" security support encountered an exit point validation routine for the method, but the license for this support is invalid or not found.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgExMISSING 
</td>
            <td colspan="1" rowspan="1">

The database provider's "exit point" security support discovered a registration for an exit point validation routine for the method, but the validation routine itself was not found. 
</td>
          </tr>
</table>

Remarks

A user's authority to the database object represented by **IAdgObject** can be manipulated with **RevokeAuthority** and [ GrantAuthority](dcsIAdgObjectClassGrantAuthorityMethod.html). The methods' *authorityType* parameters describe the authorization being granted or revoked. **AuthorityTypes** includes a broad range of authorizations which enable or disable various kinds of database object access.

The revoked authorization applies only to the specified user, *userName* .

Some database providers may not support all authorization types. 
Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [GrantAuthority Method](dcsIAdgObjectClassGrantAuthorityMethod.html)
      <br />
      [AuthorityTypes Enumeration](dcsAuthorityTypesEnumeration.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

