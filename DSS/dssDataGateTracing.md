---
title: DataGate&#174; Engine Tracing

Id: dssDataGateTracing
TocParent: Welcome
TocOrder: 45

---

<table>
			    <tr>

			       <td><span class="OH_MultiViewContainerPanelDhtmlTable"> DataGate&#174; 16.0 for SQL Server Reference Guide
				   </span><br />
				   </td>
			    </tr>
</table>

# DataGate&#174; Engine Tracing

## Introduction
All release versions of the DataGate&#174; Server Engine for Windows (dgServer.exe) are capable of producing output log files containing potentially useful information for ASNA development and support. After configuring the registry of the machine running DataGate&#174; Server as instructed below, and then restarting the DataGate&#174; Service, trace output will be collected into one or more text files. These instructions include modifications to the Windows system registry; only follow them if you have been directed by ASNA support personnel to do so.

Tracing can result in extremely large text files.
<div>
Tracing is controlled by a few values found under a particular Windows registry key. Because dgServer.exe is a 32-bit application, the key's location (in tools such as Regedit.exe) depends on whether it is running on the 32-bit or 64-bit Windows platform:

**32-bit Windows: <br />HKLM\Software\ASNA\Acceler8-DB\CurrentVersion\AdbTrace** 

**64-bit Windows: <br />HKLM\Software\Wow6432Node\ASNA\Acceler8-DB\CurrentVersion\AdbTrace** 

The values under this key specify the location of trace output files, the kind of information included in the output, and other parameters for customizing output in certain scenarios. Except for values specified as "Optional" below, each value is required to successfully initiate tracing.

#### REGZ: TraceFile (Required)
This string specifies the full path of the file produced by dgServer.exe to contain database output. The directory containing the file must exist and be accessible to the user that dgServer.exe runs as (usually, the Local System account, which usually has access to all file locations). If the file already exists, trace output is appended to the end of the file; otherwise dgServer.exe creates the file. 

#### REGSZ: TraceLevel (Required)
This string should contain a decimal integer number in the range 1 through 7 (inclusive). The binary form of this value consists of three bits, each of which controls the type of information contained in the trace. If bit 0 is set (e.g., values 1, 3, 5 or 7), then "API"-level output is produced. If bit 1 is set (e.g., values 2, 3, 6, or 7), "Function"-level output is produced. If bit 2 is set (e.g., values 4, 5, 6, or 7), "Line"-level output is produced. Generally, unless instructed otherwise by ASNA support, TraceLevel should be set to 7 to insure all types of output are included in the trace.

#### REGSZ: TraceFlush (Optional)
Specifies whether output should be "flushed" after each write to the file. If the value is "Y", the operating system will delay the execution of a DataGate&#174; job while the current line of trace output is written to the file. This should only be set to "Y" when recommended by ASNA support. Any other value for TraceFlush will disable the option.

#### REGSZ: TraceFileLineLimit (Optional)
When this value is not present, all trace output is directed to the single file specified by TraceFile. When this value is set, trace output may consist of several files, all of which contain no more than the number of lines specified by the value. This is useful when trace output is very large, to restrict the size of the log by dividing it into several files. Files produced will be named according to the availability of the specific file name. Thus, if TraceFile is set to "c:\mydir\mylog.txt" and TraceFileLineLimit is set, tracing will produce a file named "c:\mydir\mylogXXXX.txt", where XXXX is a 4-digit number. For example, suppose "c:\mydir" is initially empty. 

When tracing begins, the first trace output will be found in "c:\mydir\mylog0000.txt". After the specified number of lines have been added to the file, it is closed and a second file, "c:\mydir\mylog0001.txt" is opened for tracing output. Trace files created this way are never overwritten or appended. If a file exists with the name specified by the sequence, the next file in the sequence is tried. If TraceFileLineLimit is not a number in the range 1000-2147483647, the line limit is set to 1000 lines. 

#### REGSZ: TraceLineDuplicationRatio (Optional)
This value may be used to produce lossy compression of the trace data as it is generated. When a trace log line is generated (whether this value is set or not), a simple comparison with the preceding log line is performed, and if the two lines are equal, no trace is produced and a line counter is incremented. A subsequent unequal comparison of a later log line results in an output line noting the number of duplicate lines counted, prior to the new line. Note that no log data is lost (non-lossy compression), since only duplicate lines are skipped. <br /><br /> If this registry value contains a number between 50 and 100, the line comparison algorithm is modified as follows. If X of the first Y ordered characters in the current and preceding lines are the same value, and the shorter of the two lines has Y characters, then the lines are considered "duplicate" if the ratio X/Y is greater than or equal to the value of TraceLineDuplicationRatio divided by 100. If this value is not set or contains a value other than in the range 50-100, the default value of the ratio is 100. A useful value for this is usually something like 90, to help remove repetitive data access logs, for example.
