---
title: IAdgObject.Text Property

Id: dcsIAdgObjectClassTextProperty
TocParent: dcsIAdgObjectProperties
TocOrder: 17

keywords: Text property
keywords: IAdgObject.Text property
keywords: text description/comments of database objects
keywords: database objects, set text description/comments of
keywords: database objects, return text description/comments of
keywords: how to, set text description/comments of database objects

---

**Text** is the textual description or comments associated with a database object.
<pre>        <span class="lang">[C#]</span>
 **Public string Text { get; set; }** 
      </pre>
      <pre>        <span class="lang">[Visual Basic] </span>
 **Public Property Text As String** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegProp Text Access(*Public) Type(*String) Len(45)
   BegGet** 
      </pre>

Property Value

**String** . Returns or sets the textural description or comments associated with the database object. 
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

The value being set is a null reference. 
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

<table class="dtTABLE" id="Table3" cellspacing="0"> <colgroup span="1"> <col align="Middles" span="1" style="FONT-WEIGHT: bold" width="30%" /> <col span="1" width="70%" /> </colgroup> <tr> <th colspan="1" rowspan="1"> Value of dgException.Error </th> <th colspan="1" rowspan="1"> Condition </th> </tr> <tr> <td colspan="1" rowspan="1"> <p>dgEsAS400ERROR 
</td>
            <td colspan="1" rowspan="1">

The database provider encountered a system-level error. Details provided in the **dgException.Message** property. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmNOOBJAUTH
</td>
            <td colspan="1" rowspan="1">

When setting the value of the text area of an existing database object represented by **IAdgObject** , the user of the session does not have the required "management" authority to the object.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmBUSYOBJ 
</td>
            <td colspan="1" rowspan="1">

When setting the value of the text area of an existing database object represented by **IAdgObject** , some database providers attempt to obtain an exclusive-read lock on the database object represented by **IAdgObject** . This exception indicates that the lock could not be obtained. 
</td>
          </tr>
</table>

Remarks

Database objects may be decorated with a "text area" - a single string of the user's choice associated with the object - ostensibly describing the object. For existing database objects, **Text** is the value of the text area of the object. Setting the value of **Text** will change the text area of an existing object with the supplied value.

For new database objects, the text area of the new object will be set with the value of **Text** at the time [ Create](dcsIAdgObjectClassCreateMethod.html) is called (initially, an empty string).

Note that the text area may not be supported by all database providers and string length may be limited.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [IAdgObject Class](dcsIAdgObjectClass.html)
      <br />
      [Create Method](dcsIAdgObjectClassCreateMethod.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

