---
title: DependentTypes Enumeration

Id: dcsDependentTypesEnumeration
TocParent: dcsDataGateCommonEnumerations
TocOrder: 10

keywords: enumerations [DCS 16.0 DependentTypes
keywords: DependentTypes enumeration
keywords: Base enumeration member
keywords: Reference enumeration member
keywords: Join enumeration member

---

<span> **DependentTypes** </span> defines values specifying a dependent object's relationship to a base file. 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public enum DependentTypes;** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Enum DependentTypes** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegEnum DependentTypes Access(*Public)** 
      </pre>

Remarks

**DependentTypes** indicates the relationship a dependent database object shares with its base. The [Dependent](dcsDependentClass.html) class defines a read-only property ([DependentType](dcsDependentClassDependentTypeProperty.html)) indicating such a relationship, along with other details defining the dependent object. The types of dependent relationships are given in the Members section below.

Note that support for the values of this enumeration is database provider-dependent. Not all database providers support dependent object information and not all values of **DependentTypes** are currently implemented.
Members

<table class="dtTABLE" id="Table3" cellspacing="0">
          <colgroup span="1">
            <col align="middles" span="1" width="8%" style="FONT-WEIGHT: bold" />
            <col span="1" width="40%" />
            <col span="1" width="5%" />
          </colgroup>
          <tr>
            <th colspan="1" rowspan="1">
							Member</th>
            <th colspan="1" rowspan="1">
							Description</th>
            <th colspan="1" rowspan="1">
							Value</th>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Base
</td>
            <td colspan="1" rowspan="1">

The dependent object defines the depended-on object as a logical base. The objects may be members or files.
</td>
            <td colspan="1" rowspan="1">

0
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Reference
</td>
            <td colspan="1" rowspan="1">

This value is reserved for future use. 
</td>
            <td colspan="1" rowspan="1">

1
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

Join
</td>
            <td colspan="1" rowspan="1">

The dependent object defines a join including the depended-on object. The dependent is a logical join file and the depended-on object is a physical file.
</td>
            <td colspan="1" rowspan="1">

2
</td>
          </tr>
</table>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10

**Assembly:** ASNA DataGate Client (in ASNA.DataGate.Client.dll)
See Also

<dl />
      [Dependent Class](dcsDependentClass.html)
      <br />
      [DependentType Property](dcsDependentClassDependentTypeProperty.html) <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

