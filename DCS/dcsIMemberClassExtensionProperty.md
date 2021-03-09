---
title: IMember.Extension Property

Id: dcsIMemberClassExtensionProperty
TocParent: dcsIMemberProperties
TocOrder: 2

keywords: Extension property
keywords: IMember.Extension property
keywords: data types, identify type contained in database source file members
keywords: database file members, source data type set or returned
keywords: how to, set/return source data type for database file member

---

A string typically identifying the type of data contained in database source file members.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public string Extension { get; set; }** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Property Extension As String ()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Extension Access(*Public) Type(*String)
   BegGet** 
      </pre>

Property Value

**String** . A well-known character sequence identifying a type of source file data. The string may be empty or no greater than **ASNA.DataGate.Common.Constants.ExtensionSize** in length.
Exceptions

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Exception Type
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgException 
</td>
            <td colspan="1" rowspan="1">

The values is being set or is being accessed for the first time, requiring a database provider operation. See table below. 
</td>
          </tr>
</table>

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the <span>dgException.Error</span> property.
<br />

<table class="dtTABLE" id="table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
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

One or both of the following conditions exist:

- The value of **Extension** is being set, but the value provided is a null reference.
- The path name referenced by this **IMember** instance does not locate a valid database object.

</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmINV400OP 
</td>
            <td colspan="1" rowspan="1">

The value of **Extension** is being set but the database provider does not support the changing of database member object's extension. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmMNOTFND
</td>
            <td colspan="1" rowspan="1">

The path name referenced by this **IMember** instance may locate a valid database object but the object is not a member.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBUSYOBJ
</td>
            <td colspan="1" rowspan="1">

The value of Extension is being set but the database provider could not obtain the following locks:

- "Shared read" on the member object's parent file.
- "Exclusive read" on the member object.

</td>
          </tr>
</table>

Remarks

Use the **Extension** property to determine the type of data contained by the existing database source file member represented by **IMember** . The string denoting a member's type is generally an application - and/or user-defined keyword (e.g., "PRTF" stands for "print file source" on the iSeries). A member without a data type is denoted by an empty string value for **Extension** . 

When a value is assigned to **Extension** , DCS updates the database member to use the given value as its new extension. Likewise, if the user program has not assigned a value to the property, DCS queries the database provider to obtain the value from the existing database member. The value obtained from the database provider is cached and returned on each successive access of **Extension** , until either the user program assigns a new value to **Extension** or the **IMember** instance is disposed.

Note that when assigning a value to **Extension** , DCS does not permit the value to be greater than **ASNA.DataGate.Common.Constants.ExtensionSize** in length and silently truncates the provided value to that length. 
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IMember Class](dcsIMemberClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

