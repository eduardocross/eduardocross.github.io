---
title: ProgParmClass

Id: dcsProgParmClass
TocParent: dcsASNADataGateDataLinkClasses
TocOrder: 0

keywords: classes [DCS 16.0 ProgParm class
keywords: ProgParm class
keywords: ProgParm class, about ProgParm class
keywords: program parameters, about ProgParm
keywords: parameters, about ProgParm

---

A representation of an iSeries program parameter for use with [ As400Program](dcsAs400ProgramClass.html).

For a list of all members of this type, see [ProgParm Members](dcsProgParmMembers.html).

[ASNA.DataGate.DataLink](dcsDataGateDataLinkNamespace.html) <br /> ASNA.DataGate.DataLink.<span>ProgParm</span>
<pre class="syntax" >
        <span>&lt;Serializable&gt;</span>
 **Public Class ProgParm** 
      </pre>

Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
Remarks

DCS provides **ProgParm** to represent iSeries program parameters in your .NET program. Program parameters have three distinct components: 

1. a description of the data (metadata)
2. the data itself; the parameter value
3. the "input/output" orientation of the parameter

**ProgParm** objects reference an instance of [ProgParmType](dcsProgParmTypeClass.html) or [StructureType](dcsStructureTypeClass.html). The **As400Program** object references a list of **ProgParm** objects representing the ordered list of program parameters passed to the program. **ProgParm** objects are used to access the data associated with a particular parameter.

To construct a parameter list procedurally using the parameter classes, construct instances of **ProgParmType** and/or **StructureType** ; then append instances of **ProgParm** (referencing the corresponding **ProgParmType** or **StructureType** ) to the **As400Program** object. 

The constructors of **ProgParm** allow you to specify the metadata and input/output orientation of the parameter. The [ ObjectToParm](dcsAs400ProgramClassObjectToParmMethodMain.html) and [ParmToObject ](dcsAs400ProgramClassParmToObjectMethodMain.html)methods of **As400Program** allow you to specify and retrieve, respectively, the values of parameters represented by **ProgParm** .
Requirements

**Namespace:** [ASNA.DataGate.DataLink](dcsDataGateDataLinkNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [ProgParm Members](dcsProgParmMembers.html)
      <br />
      [As400Program Class](dcsAs400ProgramClass.html)
      <br />
      [ObjectToParm Method](dcsAs400ProgramClassObjectToParmMethodMain.html)
      <br />
      [ParmToObject Method](dcsAs400ProgramClassParmToObjectMethodMain.html)
      <br />
      [ProgParmType Class](dcsProgParmTypeClass.html)
      <br />
      [StructureType Class](dcsStructureTypeClass.html)
      <br />
      [ASNA.DataGate.DataLink Namespace](dcsDataGateDataLinkNamespace.html)
      <br />
      [Calling Stored Procedures](dcsCallingStoredProcedures.html)

