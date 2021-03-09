---
title: IPrintProperties.GetValue Method

Id: dcsIPrintPropertiesClassGetValueMethod
TocParent: dcsIPrintPropertiesMethods
TocOrder: 2

keywords: GetValue method
keywords: IPrintProperties.GetValue method
keywords: print controls, format fields, property value returned
keywords: print controls, run time properties accessed
keywords: print files, accessing print control property values

---

Access a print control property value.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public object GetValue(
   fieldName string,
   propName string,
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **public sub GetValue(_
  ByVal fieldName As string _<br />  ByVal  propName As string _
) As Object** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr GetValue Type(Object) Access(*Public)
   DclSrParm fieldName Type(*string)
   DclSrParm propName Type(*string)** 
        </pre>

Parameters

<dl>
        <dt>
 *fieldName* 
        </dt>
        <dd>
 **String** .  The field in the format represented by **IPrintProperties**  associated 
						with the print control. </dd>
        <dt>
 *propName* 
        </dt>
        <dd>
 **String** .  The property name of the print control to obtain 
								the value of.
							</dd>
</dl>

Return Value

**Object** . The value of the specified property.
Exceptions

<table class="dtTABLE" id="table2" style="border-spacing: 0px; x-cell-content-align: Top" cellspacing="0" x-use-null-cells="x-use-null-cells">
          <colgroup span="1">
            <col span="1" style="FONT-WEIGHT: bold; WIDTH: 20%" />
            <col span="1" style="WIDTH: 70%" />
          </colgroup>
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

</td> <td colspan="1" rowspan="1"> <p>The property specified by *propName* cannot be found for the control of the field specified by *fieldName* .
</td>
          </tr>
          <tr>
            <td colspan="1" rowspan="1">

NullReferenceException
</td>
            <td colspan="1" rowspan="1">

*fieldName* or *propName* is a null reference.
</td>
          </tr>
</table>

Remarks

Print controls associated with format fields have run-time properties that can be accessed with **GetValue** . **IPrintProperties** refers to the format containing the field with associated print control, *fieldName* refers to the field, and *propName* is the name of a property of the control. The value returned is a generic object reference.

Since print controls may be implemented as COM-based unmanaged objects, this method may invoke .NET interoperability functions to obtain a so-called "runtime callable wrapper" for such controls. The user should be aware of the constraints of .NET interoperability in terms of performance and security when using this method.

As a convenience, **GetValue** performs a simple conversion for certain OLE class types representing image data. If the value of the requested property is one of the following types from the "stdole" namespace:

- **StdPicture**
- **Picture**
- **IPicture**

Then DCS uses .NET framework classes to convert the value to the **System.Drawing.Image** type. The **Image** class is somewhat more useful for .NET programs and objects of the type are readily convertible to one of the OLE interop types if necessary. 
Requirements

<span> **Namespace:** [ ASNA.DataGate.Providers](dcsDataGateProvidersNamespace.html) </span> 

<span> **Assembly:** ASNA DataGate Client</span> 

<span> **Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10</span> 
See Also

<dl />
      [IPrintProperties Class](dcsIPrintPropertiesClass.html)
      <br />
      <br />
      [ASNA.DataGate.Providers Namespace](dcsDataGateProvidersNamespace.html)

