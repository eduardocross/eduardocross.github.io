---
title: AdgConnection(SourceProfile)

Id: dcsAdgConnectionClassAdgConnectionMethod1
TocParent: dcsAdgConnectionConstructorsMain
TocOrder: 0

---

Constructs an [AdgConnection](dcsAdgConnectionClass.html) instance from the initial values of the [ SourceProfile](dcsAdgConnectionClassSourceProfileProperty.html) containing the properties of the database connection.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public AdgConnection(
   [SourceProfile](dcsSourceProfileClass.html) sp
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Sub New( _
   ByVal sp As [SourceProfile](dcsSourceProfileClass.html)
)** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegConstructor Access(*Public)
      DclSrParm sp Type([SourceProfile](dcsSourceProfileClass.html))** 
      </pre>
      <br />

Parameters

<dl>
        <dt />
</dl>

*sp* 
<dl>
        <dd>

The **SourceProfile** object ([SourceProfile](dcsSourceProfileClass.html)) containing the properties of the database connection.
</dd>
</dl>

Exceptions

[ASNA.DataGate.Common.dgException](dcsdgExceptionClass.html) is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the dgException.Error property.
<br />

<table class="dtTABLE" id="Table5" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
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
            <td colspan="1" rowspan="1" style="height: 68px">

dgEdbNODBNAME
</td>
            <td colspan="1" rowspan="1" style="height: 68px">

The value specified by the *dbName* parameter is an empty string, or does not refer to a valid registered database name.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgENOTSECURE
</td>
            <td colspan="1" rowspan="1">

A password was not found for a database name registered to use password authentication.
</td>
          </tr>
</table>

Remarks

An **AdgConnection** object is constructed by specifying an initial value for the [SourceProfile](dcsAdgConnectionClassSourceProfileProperty.html) property, which is subsequently used by the [ Open](dcsAdgConnectionClassOpenMethod.html) method to connect to a particular database server. The properties of **SourceProfile** specify the database connection parameters.

The *sp* parameter is used to construct a new **SourceProfile** instance, using the [SourceProfile(string)](dcsSourceProfileClassSourceProfileConstructor2.html) constructor. This **SourceProfile** object is then assigned to the **AdgConnection** object’s **SourceProfile** property.
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
      [SourceProfile Method](dcsAdgConnectionClassSourceProfileProperty.html)
      <br />
      [Open Method](dcsAdgConnectionClassOpenMethod.html)
      <br />
      [ASNA.DataGate.Providers.SourceProfile Class](dcsSourceProfileClass.html)
      <br />
      [SourceProfile 
					Constructor](dcsSourceProfileClassSourceProfileConstructor2.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

