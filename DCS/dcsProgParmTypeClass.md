---
title: ProgParmType Class

Id: dcsProgParmTypeClass
TocParent: dcsASNADataGateDataLinkClasses
TocOrder: 1

keywords: classes [DCS 16.0 ProgParmType class
keywords: ProgParmType class
keywords: ProgParmType class, about ProgParmType class
keywords: fields, about fields as program parameters
keywords: program parameters, simple data types class
keywords: parameters, simple data types class

---

Defines the data type of a simple iSeries program parameter.

For a list of all members of this type, see [ProgParmType Members](dcsProgParmTypeMembers.html).

[ASNA.DataGate.DataLink](dcsDataGateDataLinkNamespace.html) <br /> ASNA.DataGate.DataLink.<span>ProgParmType</span>
<pre class="syntax" >
        <span>&lt;Serializable&gt;</span>
 **Public Class ProgParmType** 
      </pre>

Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
Remarks

**ProgParmType** wraps a [ASNA.DataGate.Common.FieldType](dcsFieldTypeClass.html) object to describe the data type of an iSeries program parameter. The data type may be described to be a scalar or vector. Additionally, you may associate a string identifier with the program parameter. For complex parameter types composed of combinations of scalars, arrays, and embedded complex types, define program parameters with [StructureType](dcsStructureTypeClass.html) objects.

The only public method of **ProgParmType** is its [ constructor](dcsProgParmTypeConstructorsMain.html). The **FieldType** object contained by **ProgParmType** provides most of the information for the parameter type description. **FieldType** is used internally by DCS to manipulate many database objects, including program parameters and file fields.

The optional name associated with a **ProgParmType** object may be used by parameter manipulation methods such as [ As400Program.ObjectToParm](dcsAs400ProgramClassObjectToParmMethodMain.html).
Requirements

**Namespace:** [ASNA.DataGate.DataLink](dcsDataGateDataLinkNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [ProgParmType Members](dcsProgParmTypeMembers.html)
      <br />
      [As400Program Class](dcsAs400ProgramClass.html)
      <br />
      [ObjectToParm Method](dcsAs400ProgramClassObjectToParmMethodMain.html)
      <br />
      [FieldType Class](dcsFieldTypeClass.html)
      <br />
      [ProgParm Class](dcsProgParmClass.html)
      <br />
      [StructureType Class](dcsStructureTypeClass.html)
      <br />
      [ASNA DataGate DataLink Namespace](dcsDataGateDataLinkNamespace.html)
      <br />
      [Calling Stored Procedures](dcsCallingStoredProcedures.html)

