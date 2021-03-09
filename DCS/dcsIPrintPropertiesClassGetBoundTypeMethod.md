---
title: IPrintProperties.GetBoundType Method

Id: dcsIPrintPropertiesClassGetBoundTypeMethod
TocParent: dcsIPrintPropertiesMethods
TocOrder: 0

keywords: GetBoundType method
keywords: IPrintProperties.GetBoundType method
keywords: how to, determine CLR type of print control object for print format field
keywords: print controls, format fields, return CLR type of control object
keywords: print controls, return CLR type of for format field
keywords: print files, return CLR type of print control object for format field

---

<span> **GetBoundType** </span> returns the CLR type of a print control associated with a field.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public System.Type GetBoundType(
   fieldName string,
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public sub GetBoundType(_<br />   ByVal fieldName As string_
) As System.Type** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr GetBoundType Type(System.Type) Access(*Public)
   DclSrParm fieldName Type(*string)** 
 </pre>

Parameters

<dl>
        <dt>
 *fieldName* 
        </dt>
        <dd>
 **String** .  The field in the format represented by **IPrintProperties** 
						to obtain the control type for.
					</dd>
</dl>

Return Value

**System.Type** . This object reveals the CLR type of a print control. 
Exceptions

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" />
          <col span="1" style="WIDTH: 70%" />
          <tr>
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

*fieldName* is a null reference.
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

ASNA.DataGate.Common.dgException is thrown to signal normal procedural conditions, in addition to error conditions. The following table summarizes these conditions, and the corresponding value of the <span>dgException.Error</span> property.

<table class="dtTABLE" id="table3" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells"> <col span="1" style="FONT-WEIGHT: bold; WIDTH: 30%" /> <col span="1" style="WIDTH: 70%" /> <tr> <th colspan="1" rowspan="1"> Value of dgException.Error </th> <th colspan="1" rowspan="1"> Condition </th> </tr> <tr> <td colspan="1" rowspan="1"> <p>dgEcFLDNOTFND
</td>
            <td colspan="1" rowspan="1">

No print control object is associated with this **IPrintProperties** instance for *fieldName* .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

dgEpLIBNOTFND
</td>
            <td colspan="1" rowspan="1">

The file is an OLE print file, but the print control for the field could not be found. This may be due to an installation issue with the associated control library.
</td>
          </tr>
</table>

Remarks

Print controls associated with format fields are rendered by **IPrintProperties** as common language runtime (CLR) objects. **GetBoundType** provides a way of determining the CLR type of print control objects, without obtaining an object reference to the control. To obtain a reference to the control object itself, use [ GetTypedObject](dcsIPrintPropertiesClassGetTypedObjectMethod.html).

If no print control object is associated with *fieldName* , an exception is raised. Otherwise, an instance of **System.Type** is returned, which represents the metadata of the control object.

Since print controls may be implemented as COM-based unmanaged objects, this method may invoke .NET interoperability functions to obtain a so-called "runtime callable wrapper" for such controls. The user should be aware of the constraints of .NET interoperability in terms of performance and security when using this method. 
Requirements

<span> **Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span> 
See 
Also

<span>[IPrintProperties Class](dcsIPrintPropertiesClass.html) <br /> [GetTypedObject Method](dcsIPrintPropertiesClassGetTypedObjectMethod.html) <br /> [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html) </span> 
