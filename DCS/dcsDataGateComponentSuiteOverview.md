---
title: ASNA DataGate Component Suite for Visual Studio .NET

Id: dcsDataGateComponentSuiteOverview
TocParent: dcsIntroductionMain
TocOrder: 0

keywords: overview, DataGate Component Suite
keywords: DataGate Component Suite
keywords: DataGate Component Suite, overview

---

The ASNA DataGate Component Suite for Visual Studio .NET assembly provides managed-code access to data and objects residing in DataGate for IBM i and DataGate for Windows (formerly, Acceler8DB) databases. Leveraging the strength of the .NET Framework, DCS for Visual Studio 2019 programs can be created using any .NET development language, including ASNA Visual RPG, Visual Basic, C#, and others. Data access mechanisms in DCS for Visual Studio 2019 support and enhance the System.Data namespace, including the DataSet model, while maintaining traditional DataGate record-level characteristics.

For the first time, DCS for Visual Studio 2019 provides all of the same interfaces used by the Visual RPG compiler. The same powerful database engine used by Visual RPG is fully under your control for use in any .NET language. Visual RPG for .NET remains the language of choice for creating programs that access DataGate databases. However, with DCS for .NET, Visual Basic programmers and others can access data with nearly the same efficiency. Likewise, Visual RPG programmers will appreciate DCS for its object management capabilities.

Many common database application functions are facilitated by DCS for Visual Studio 2019, including the following:

- Retrieve, display, and update data with a record-level access paradigm.
- Print a report using a DataGate OLE print file.
- Call a stored procedure on the database server.
- Determine if a file’s format has changed prior to opening.
- Compose database network connection parameters on-the-fly.

All of these tasks and more can be accomplished with the help of a few DCS objects.
<br />

<table class="dtTABLE" id="table3" style="border-spacing: 0px" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Task
						</th>
            <th colspan="1" rowspan="1">
							Object
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[File/data access](dcsUsingtheFileAdapterClass.html) 
</td>
            <td colspan="1" rowspan="1">

[ASNA.DataGate.Client.FileAdapter](dcsFileAdapterClass.html) and [ASNA.DataGate.Client.AdgDataSet](dcsAdgDataSetClass.html) classes provide the core functionality. [AdgDataSet](dcsAdgDataSetClass.html) inherits <span>System.Data.DataSet</span> and its rich ADO.NET utility.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[Manage database connections ](dcsManagingDatabaseConnectionsMain.html) 
</td>
            <td colspan="1" rowspan="1">

The [ASNA.DataGate.Client.AdgConnection](dcsAdgConnectionClass.html) and [ASNA.DataGate.Providers.SourceProfile](dcsSourceProfileClass.html) classes manage database connections and connection parameters including DataGate database names and transaction processing.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

[Stored procedure call ](dcsCallingStoredProcedures.html) 
</td>
            <td colspan="1" rowspan="1">
							Functionality provided by:
- [ASNA.DataGate.Client.As400Program](dcsAs400ProgramClass.html)
- [ASNA.DataGate.DataLink.ProgParm](dcsProgParmClass.html)
- [ASNA.DataGate.DataLink.ProgParmType](dcsProgParmTypeClass.html)

</td>
          </tr>
</table>

<br />

