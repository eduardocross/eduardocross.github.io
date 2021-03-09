---
title: StructureType Class

Id: dcsStructureTypeClass
TocParent: dcsASNADataGateDataLinkClasses
TocOrder: 2

keywords: StructureType class
keywords: StructureType class, about StructureType class
keywords: classes [DCS 16.0 StructureType class
keywords: parameters, structured data types class
keywords: program parameters, structured data types class

---

Define the data types of members of a structured iSeries program parameter. 

For a list of all members of this type, see [StructureType Members](dcsStructureTypeMembers.html).

[ASNA.DataGate.DataLink](dcsDataGateClientNamespace.html) <br /> ASNA.DataGate.DataLink.<span>StructureType</span>
<pre class="syntax" >
        <span>&lt;Serializable&gt;</span>
 **Public Class StructureType** 
      </pre>

Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
Remarks

iSeries programs can be defined to accept parameters in the form of data structures. These can be modeled in DCS using the **StructureType** class. The members of the data structure described with **StructureType** are composed of contained [ProgParmType](dcsProgParmTypeClass.html) and/or **StructureType** objects.

As with simple parameter types, structured types may be described to be scalar or vector parameters. Vectors are single-dimension arrays or "multiple-occurrence" types.

The only public method of **StructureType** is its [ constructor](dcsStructureTypeConstructorsMain.html). The array of objects passed to the constructor contains an ordered list of the **ProgParmType** and/or **StructureType** objects which describe the structure. 
Requirements

**Namespace:** [ASNA.DataGate.DataLink](dcsDataGateDataLinkNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [StructureType Members](dcsStructureTypeMembers.html)
      <br />
      [ProgParmType Class](dcsProgParmTypeClass.html)
      <br />
      [ASNA.DataGate.DataLink Namespace](dcsDataGateDataLinkNamespace.html)
      <br />
      [Calling Stored Procedures](dcsCallingStoredProcedures.html)

