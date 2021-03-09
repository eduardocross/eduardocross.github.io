---
title: IAdgObject.OwnerIsGroup Property

Id: dcsIAdgObjectClassOwnerIsGroupProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 11

keywords: OwnerIsGroup property
keywords: IAdgObject.OwnerIsGroup property
keywords: how to, determine if database object owner is single or group profile
keywords: database objects, identify single or group profile owner
keywords: owner names, identify single or group user profile

---

**OwnerIsGroup** specifies [ Owner](dcsIAdgObjectClassOwnerProperty.html) is a group account when **True** .
<pre>        <span class="lang">[C#]</span>
 **Public bool OwnerIsGroup { get; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public ReadOnly Property OwnerIsGroup As boolean** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp OwnerIsGroup Access(*Public) Type(*boolean) Len(45)
   BegGet** 
      </pre>

Property Value <p> **Boolean** . ReadOnly. **True** if [ Owner](dcsIAdgObjectClassOwnerProperty.html) names a group profile, otherwise **False** . 
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

The path name specified when the **IAdgObject** instance was created does not reference an existing database object, or the property is not available for this object type.
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

dgEgNONSECUREDB
</td>
            <td colspan="1" rowspan="1">

The property value is unavailable because the database does not have the user security feature.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEgNOAUTHLOCK
</td>
            <td colspan="1" rowspan="1">

The user of the session does not have "management" authority to the existing database object represented by **IAdgObject** .
</td>
          </tr>
</table>

Remarks

Database object may be owned by a user or group profile. **OwnerIsGroup** , when **True** , indicates that **Owner** is a group profile.

Depending upon the database provider, **IAdgObject** queries for security attributes, such as **OwnerIsGroup** , only once in the lifetime of the **IAdgObject** instance. If attributes change after the query, the change will not be reflected in the property values of the **IAdgObject** .
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [Owner Property](dcsIAdgObjectClassOwnerProperty.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

