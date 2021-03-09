---
title: ProgParmType(string, integer, FieldType)

Id: dcsProgParmTypeClassProgParmTypeConstructor
TocParent: dcsProgParmTypeConstructorsMain
TocOrder: 0

---

Defines the data type of a simple iSeries program parameter.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public ProgParmType(<br />   string name,<br />   int cElems,<br />   FieldType type<br />)**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public Sub New( _<br />   ByVal name As String, _<br />   ByVal cElems As Integer, _<br />   ByVal type As [ASNA.DataGate.Common.FieldType](dcsFieldTypeClass.html)<br />)**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegConstructor Access(*Public)<br />   DclSrParm name Type(*String)<br />   DclSrParm cElems Type(*Integer) Len(4)<br />   DclSrParm type Type(FieldType)** 
      </pre>

Parameters

<dl>
        <dt>
 *name* 
        </dt>
        <dd>String.  Optional name to identify the **ProgParmType**  object 
						in the [As400Program](dcsAs400ProgramClass.html) parameter list. 
						 If not required, specify an empty string or null.  </dd>
        <dt>
 *cElems*  
							</dt>
        <dd>Integer.  The number of elements in a single-dimension array.  If the **ProgParmType**  describes a scalar parameter type, specify 0 </dd>
        <dt>
 *type*  
									</dt>
        <dd>
          [ASNA.DataGate.Common.FieldType](dcsFieldTypeClass.html).  The 
										database provider-specific object type of the parameter.
									</dd>
</dl>

Remarks

**ProgParmType** constructs simple parameter types. 

- *name* allows the **ProgParmType** to be assigned an application-specific name for use in identifying a parameter or structured type member in the **As400Program** object’s parameter list.
- *cElems* specifies the length of a multiple-occurrence (single-dimension array) parameter.
- If the type is a non-array parameter, specify 0 for *cElems* .

In terms of the internal definition of parameters in DCS, a multiple-occurrence parameter of one element is indistinguishable from a non-array parameter.

The database object type of the parameter is given by *type* . Generally, the value of *type* is obtained using one of the"New" static methods of the [FieldType](dcsFieldTypeClass.html) class, such as [FieldType.NewPacked](dcsFieldTypeClassNewPackedMethod.html) for packed decimal types. **ProgParmType** treats *type* as a read-only object; thus a single instance of **FieldType** may be referenced by multiple instances of **ProgParmType** .

To construct a parameter list procedurally using the parameter classes, construct instances of **ProgParmType** and/or [ StructureType](dcsStructureTypeClass.html); then, append instances of [ ProgParm](dcsProgParmClass.html) (referencing the corresponding **ProgParmType** or **StructureType** ) to the **As400Program** object.
Requirements

**Namespace:** [ASNA.DataGate.DataLink](dcsDataGateDataLinkNamespace.html) 

<span> **Assembly:** ASNA DataGate DataLink</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span>
See Also

<dl />
      [ProgParmType Class](dcsProgParmTypeClass.html)
      <br />
      [ProgParm Class](dcsProgParmClass.html) 
				<br />[StructureType Class](dcsStructureTypeClass.html)<br />
				[As400Program Class](dcsAs400ProgramClass.html)<br />
				[AppendParm Method](dcsAs400ProgramClassAppendParmMethod.html)<br />
				[AppendParms Method](dcsAs400ProgramClassAppendParmsMethod.html)<br />
				[ParmToObject Method](dcsAs400ProgramClassParmToObjectMethodMain.html)<br />
				[FieldType Class](dcsFieldTypeClass.html)<br />
				[NewPacked Method](dcsFieldTypeClassNewPackedMethod.html)<br />
				[ASNA.DataGate.DataLink Namespace](dcsDataGateDataLinkNamespace.html)<br />
				[Calling Stored Procedures](dcsCallingStoredProcedures.html)

