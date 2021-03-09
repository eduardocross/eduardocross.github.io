---
title: FileAdapter.ResetPrintAttr Method

Id: dcsFileAdapterClassResetPrintAttrMethod
TocParent: dcsFileAdapterMethods
TocOrder: 24

keywords: ResetPrintAttr method
keywords: FileAdapter.ResetPrintAttr method
keywords: printer jobs, starting
keywords: printer jobs, stopping
keywords: printer jobs, reset device attributes
keywords: how to, reset print job device attributes

---

Complete the current printer job, change device-related parameters associated with the open print file, then start a new printer job.
<pre> **[C#]** 
 Public void ResetPrintAttr (
   string docName,
   ASNA.DataGate.Providers.PrintDevAttr attr
)

      </pre>
      <pre> **[Visual Basic]** 
 Overloads Public Sub ResetPrintAttr ( _
   ByVal docName As String _
   ByVal attr As [ASNA.DataGate.Providers.PrintDevAttr](dcsPrintDevAttrClass.html)
)

      </pre>
      <pre class="prettyprint"> **[Visual RPG]** 
BegSr ResetPrintAttr Access(*Public)
  DclSrParm docName Type(string)
  DclSrParm attr Type(ASNA.DataGate.Providers.PrintDevAttr)
      </pre>

Parameters

<dl>
        <dt>
 *docName* 
        </dt>
        <dd>Name of the next printer job. </dd>
        <dt>
 *attr* 
        </dt>
        <dd>[ASNA.DataGate.Providers.PrintDevAttr](dcsPrintDevAttrClass.html). 
								Sets the device-related attributes for the next printer job.</dd>
</dl>
      <br />

Exceptions

<br />

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <th colspan="1" rowspan="1">
							Exception Type
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NullReferenceException
</td>
            <td colspan="1" rowspan="1">

FileAdapter [open](dcsFileAdapterClassOpenMethod.html) method has not been called (file is not open).
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

<table class="dtTABLE" id="table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
          <tr valign="top">
            <th colspan="1" rowspan="1">
							Value of dgException.Error
						</th>
            <th colspan="1" rowspan="1">
							Condition
						</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEaINVFTOP
</td>
            <td colspan="1" rowspan="1">

This method is only valid when used with print files.
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEmFILENOTOPEN
</td>
            <td colspan="1" rowspan="1">

This method can only be used with open print files.
</td>
          </tr>
</table>

Remarks

**ResetPrintAttr** completes the printer job associated with the open print file and begins a new printer job with new printer job properties as specified by the ***docName*** and ***attr*** parameters. The [ForceEOD](dcsFileAdapterClassForceEODMethod.html) method provides similar printer job functionality for print files but does not change the job name or device attributes. 

The ** *attr* ** parameter refers to an instance of [ ASNA.DataGate.Providers.PrintDevAttr](dcsPrintDevAttrClass.html) object specified when the file is opened. For example, the program’s print operation can print several documents using one setting for margins (set via the **PrintFileOpenAttr.DevAttr** property), then change the margins before printing the next set of documents (via the **ResetPrintAttr** method).

The ** *docName* ** parameter allows you to associate a new name with the new printer job. This name can be used by the operating system to identify a job in a printer queue. If ** *docName* ** is null (Nothing in VB, *Nothing in AVR), the next printer job will have the same name as the current printer job.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FileAdapter Class](dcsFileAdapterClass.html)
      <br />
      [FileAdapter Class Members](dcsFileAdapterMembers.html)
      <br />
      [ForceEOD Method](dcsFileAdapterClassForceEODMethod.html)
      <br />
      [ASNA.DataGate.Providers.PrintDevAttr Class](dcsPrintDevAttrClass.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

