---
title: FieldType.NewDate Method

Id: dcsFieldTypeClassNewDateMethod
TocParent: dcsFieldTypeMethods
TocOrder: 2

keywords: NewDate method
keywords: FieldType.NewDate method
keywords: enumerations [DCS 16.0 DateTimeFormat, used by
keywords: DateTimeFormat enumeration, used by
keywords: fields, date
keywords: date field defined
keywords: how to, define date field

---

Creates a new date [ FieldType](dcsFieldTypeClass.html).
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public static FieldType NewDate(<br />   DateTimeFormat fmt<br />);**  </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Shared Function NewDate( _<br />   ByVal fmt As [DateTimeFormat](dcsDateTimeFormatEnumeration.html)       _<br />) As [FieldType](dcsFieldTypeClass.html)**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc NewDate Type(FieldType) Access(*Public) Shared(*Yes)
   DclSrParm fmt Type(DateTimeFormat) Len(4)** 
      </pre>

Parameters

<dl>
        <dt>
 *fmt* 
        </dt>
        <dd>
          [DateTimeFormat](dcsDateTimeFormatEnumeration.html).  The format 
						of the date field.</dd>
</dl>

Exceptions

System.ArgumentException.  Thrown if *fmt*  is **DateTimeFormat.HMS** .

Remarks

**NewDate** constructs a **FieldType** that represents a DataGate date field. Date fields contain calendar date data in a variety of formats, as specified by *fmt* . The storage size of a date field is 6 to 10 bytes, dependent upon the format (see [ DateTimeFormat](dcsDateTimeFormatEnumeration.html) for details).

The value of *fmt* may be any value of **DateTimeFormat** , except for **HMS** .

Note that internally, DCS manipulates date, time, and timestamp fields as **System.DateTime** value types. The object value returned by DCS as the value of a date, time, or timestamp field (in methods such as [ As400Program.ParmToObject](dcsAs400ProgramClassParmToObjectMethodMain.html)) will be converted from a value of **DateTime** . Likewise, DCS will only accept values which can be accurately converted to **DateTime** values, for setting the value of date, time, or timestamp fields.
Examples

<pre> <span class="lang"> **[C#]** </span>
  /* Create a parms list to pass to a pre-initialized As400Program object.
   * We want to pass one date with time format *USA and another with time
   * format *ISO. Other time formats are available in the DateTimeFormat
   * enumeration as well. */
  DateTime DateUSA = System.DateTime.Now;
  DateTime DateISO = System.DateTime.Now;

  ProgParmType type1 = new ProgParmType("DateUSA", 0, FieldType.NewDate(DateTimeFormat.USA));
  ProgParmType type2 = new ProgParmType("DateISO", 0, FieldType.NewDate(DateTimeFormat.ISO));
  ProgParm parm1 = new ProgParm(type1, DataDirection.InputOutput);
  ProgParm parm2 = new ProgParm(type2, DataDirection.InputOutput);

  prog.AppendParm(parm1);
  prog.AppendParm(parm2);

  /* In the lines below, we assign the IBM i program parameters
   * values from our .NET variables. */
  prog.ObjectToParm(parm1, DateUSA, 0);
  prog.ObjectToParm(parm1, DateISO, 0);

  /* Call the program. */
  prog.Execute();

  /* The parameters can be bidirectional and thus return data as well. 
   * To use that data, we assign the values of the parameters back to our
   * .NET variables. */
  DateUSA = Convert.ToDateTime(prog.ParmToObject(parm1, DateUSA.GetType(), 0));
  DateISO = Convert.ToDateTime(prog.ParmToObject(parm2, DateUSA.GetType(), 0));
  /* IMPORTANT NOTE: The time and date data types do not return all the information
   * which a .NET DateTime can contain. Specifically, if you specify a parm as a NewTime,
   * the data portion of the returned DateTime will be set to MinValue. The same will
   * happen to the time portion of a variable if its IBM i parm was set to be a NewDate. */</pre>

  <pre><span class="lang"> **[Visual Basic]** </span>
  ' Create a parms list to pass to a pre-initialized As400Program object.
  ' We want to pass one date with time format *USA and another with time
  ' format *ISO. Other time formats are available in the DateTimeFormat
  ' enumeration as well. 
  Dim DateUSA As DateTime = System.DateTime.Now
  Dim DateISO As DateTime = System.DateTime.Now

  Dim type1 As New ProgParmType("DateUSA", 0, FieldType.NewDate(DateTimeFormat.USA))
  Dim type2 As New ProgParmType("DateISO", 0, FieldType.NewDate(DateTimeFormat.ISO))
  Dim parm1 As New ProgParm(type1, DataDirection.InputOutput)
  Dim parm2 As New ProgParm(type2, DataDirection.InputOutput)

  prog.AppendParm(parm1)
  prog.AppendParm(parm2)

  ' In the lines below, we assign the IBM i program parameters
  ' values from our .NET variables. 
  prog.ObjectToParm(parm1, DateUSA, 0)
  prog.ObjectToParm(parm1, DateISO, 0)

  ' Call the program. 
  prog.Execute()

  ' The parameters can be bidirectional and thus return data as well. 
  ' To use that data, we assign the values of the parameters back to our
  ' .NET variables. 
  DateUSA = Convert.ToDateTime(prog.ParmToObject(parm1, DateUSA.GetType(), 0))
  DateISO = Convert.ToDateTime(prog.ParmToObject(parm2, DateUSA.GetType(), 0))
  ' IMPORTANT NOTE: The time and date data types do not return all the information
  ' which a .NET DateTime can contain. Specifically, if you specify a parm as a NewTime,
  ' the data portion of the returned DateTime will be set to MinValue. The same will
  ' happen to the time portion of a variable if its IBM i parm was set to be a NewDate. </pre>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html)

<span> **Assembly:** ASNA DataGate Client</span>

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />[FieldType Class](dcsFieldTypeClass.html)<br />[FieldType Class Members](dcsFieldTypeMembers.html)<br />[DateTimeFormat Enumeration](dcsDateTimeFormatEnumeration.html)<br />[As400Program.ParmToObject](dcsAs400ProgramClassParmToObjectMethodMain.html)
 <br />[ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

