---
title: AdgConnection.Open Method

Id: dcsAdgConnectionClassOpenMethod
TocParent: dcsAdgConnectionMethodsMain
TocOrder: 9

keywords: Open method
keywords: AdgConnection.Open method

keywords: open database connection
keywords: database connections, open
keywords: how to, open database connection

---

Opens a database connection with the settings specified by the provider-specific [SourceProfile](dcsSourceProfileClass.html) class. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public void Open();** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub Open()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Open Access(*Public)** 
      </pre>

Exceptions

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

SourceProfile specifies a connection to a database provider which implements ASNA license enforcement and the provider’s trial license period has expired. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsPCODE 
</td>
            <td colspan="1" rowspan="1">

SourceProfile specifies a connection to a database provider which implements ASNA license enforcement and the provider’s license evidence is missing or invalid. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsNOLICSRVR, dgEsLMMUTEX, dgEsLMSYNCDQD, dgEsLMSTART, dgEsLMPID 
</td>
            <td colspan="1" rowspan="1">

SourceProfile specifies a connection to a database provider which implements ASNA license enforcement and the license management provider could not be contacted. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEsAS400ERROR 
</td>
            <td colspan="1" rowspan="1">

The database server encountered a system error, which may include a user authentication problem. Details are available via the <span>SystemError</span> and <span>Text</span> fields of [dgException](dcsdgExceptionClass.html). 
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

SourceProfile specifies a connection that is to query the user for authentication information and the user cancelled the query. 
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEINTERNAL 
</td>
            <td colspan="1" rowspan="1">

The <span>AdgConnection</span> object is already in the <span>Open</span> state, or an internal system error occurred. 
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

This method is used to transition an **AdgConnection** object to the Open state. If successful, a new database connection is established. The characteristics of the new connection may be specified by prior assignment of the [ SourceProfile](dcsAdgConnectionClassSourceProfileProperty.html) property, or by specifying a registered database name or **SourceProfile** object in the [ AdgConnection constructor](dcsAdgConnectionConstructorsMain.html).
Examples

<pre>
        <span class="lang">
 **[C#]** 
        </span>
  try
  {
      AdgConnection dataBase = new AdgConnection("*Public/DG NET IBM i");
      dataBase.Open();
  }
  catch(dgException e)
  {
      System.Windows.Forms.MessageBox.Show(e.Message, "Error establishing connection to database.");
  }</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Try
      Dim dataBase As New AdgConnection("*Public/DG NET IBM i")
      dataBase.Open()
  Catch e As dgException
      MsgBox(e.Message, MsgBoxStyle.Exclamation, "Error establishing connection to database.")
  End Try</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  Try
      DclFld dataBase Type(AdgConnection)
      dataBase = *New AdgConnection("*Public/DG NET IBM i")
      dataBase.Open()
  Catch e Type(dgException)
      MsgBox e.Message "Error establishing connection to database."); 
  EndTry</pre>

Requirements

<span> **Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro</span> 
See Also

<dl />
      [AdgConnection Class](dcsAdgConnectionClass.html)
      <br />
      [AdgConnection Class Members](dcsAdgConnectionMembers.html)
      <br />
      [State Property](dcsAdgConnectionClassStateProperty.html)
      <br />
      [SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

