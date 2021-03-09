---
title: AdgConnection.Clone Method

Id: dcsAdgConnectionClassCloneMethod
TocParent: dcsAdgConnectionMethodsMain
TocOrder: 2

keywords: Clone method
keywords: AdgConnection.Clone method
keywords: database files, connection copied 
keywords: files, database connection established
keywords: copy database connection
keywords: how to, copy database connection
keywords: database connections, copied

---

Returns a copy of the **AdgConnection** object. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public virtual new object Clone();** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Overridable NotOverridable Clone() As Object** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc Clone Access(*Public) Type(*Object) Modifier(*Overridable)** 
      </pre>

Returns

An instance of [AdgConnection](dcsAdgConnectionClass.html).
Exceptions

[DgException](dcsdgExceptionClass.html) may be thrown by this method, but only if the copied object is in the Open [ state](dcsAdgConnectionClassStateProperty.html) (thus causing the [Open ](dcsAdgConnectionClassOpenMethod.html) method to be called on the copy).

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" x-use-null-cells="x-use-null-cells" style="border-spacing: 0px;     x-cell-content-align: Top" cellspacing="0">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Value of
							<br />
							dgException.Error
						</th>
            <th colspan="1" rowspan="1">

Condition
</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsTRLEXP
</td>
            <td colspan="1" rowspan="1">

SourceProfile specifies a connection to a database provider which implements ASNA license enforcement, and the provider’s trial license period has expired. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPCODE
</td>
            <td colspan="1" rowspan="1">

SourceProfile specifies a connection to a database provider which implements ASNA license enforcement, and the provider’s license evidence is missing or invalid.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsNOLICSRVR, dgEsLMMUTEX, dgEsLMSYNCDQD, dgEsLMSTART, dgEsLMPID
</td>
            <td colspan="1" rowspan="1">

SourceProfile specifies a connection to a database provider which implements ASNA license enforcement, and the license management provider could not be contacted.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEiDG8START
</td>
            <td colspan="1" rowspan="1">

SourceProfile specifies a connection to an IBM i database provider, and the provider has encountered difficulty in starting a job for the connection. Refer to job logs for user profile for details.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsAS400ERROR
</td>
            <td colspan="1" rowspan="1">

The database server encountered a system error, which may include a user authentication problem. Details are available via the SystemError and Text fields of dgException.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEOLDSERVER
</td>
            <td colspan="1" rowspan="1">

SourceProfile specifies a connection to a release of a database provider that does not support the DataGate client assembly. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmCANCEL
</td>
            <td colspan="1" rowspan="1">

SourceProfile specifies a connection that is to query the user for authentication information, and the user cancelled the query.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINTERNAL
</td>
            <td colspan="1" rowspan="1">

The AdgConnection object is already in the Open state, or an internal system error occurred.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINVPLATFORM
</td>
            <td colspan="1" rowspan="1">

SourceProfile specifies a database provider that is currently not supported by the DataGate client assembly, therefore a connection cannot be opened.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsMTSTRLEXP
</td>
            <td colspan="1" rowspan="1">

The DataGate client assembly’s trial license for web application use has expired.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsMTSPCODE, dgEsMTSPRCCNT
</td>
            <td colspan="1" rowspan="1">

The DataGate client assembly is not currently licensed for use in a web application on this machine.
</td>
          </tr>
</table>

Remarks

This method returns a copy of the **AdgConnection** object. If successful, the copy’s [ SourceProfile](dcsAdgConnectionClassSourceProfileProperty.html) property will reference the same **SourceProfile** object contained in the **SourceProfile** property of the copied object. If the copied object is in the Open **state** , the [ Open](dcsAdgConnectionClassOpenMethod.html) method is invoked on the copy, providing a new database connection.

Note that a database connection cannot be shared between two instances of **AdgConnection** .
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  AdgConnection Cx;
  Cx = new AdgConnection("ASNA Local DB");
  Cx.Open();</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Dim Cx As AdgConnection
  Cx = New AdgConnection("ASNA Local DB")
  Cx.Open()</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  Dclfld Name(Cx) Type(AdgConnection)
  Cx = *New AdgConnection("ASNA Local DB")
  Cx.Open()</pre>

Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      <span>
        [AdgConnection Class](dcsAdgConnectionClass.html)
        <br />
        [AdgConnection Class Members](dcsAdgConnectionMembers.html)
        <br />
        [Open Method](dcsAdgConnectionClassOpenMethod.html)
        <br />
        [SourceProfile Property](dcsAdgConnectionClassSourceProfileProperty.html)
        <br />
        [State Property](dcsAdgConnectionClassStateProperty.html)
        <br />
        [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)
      </span>

<br />

