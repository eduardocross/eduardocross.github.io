---
title: FieldType.NewTime Method

Id: dcsFieldTypeClassNewTimeMethod
TocParent: dcsFieldTypeMethods
TocOrder: 9

keywords: NewTime method
keywords: FieldType.NewTime method
keywords: enumerations [DCS 16.0 DateTimeFormat, used by
keywords: DateTimeFormat enumeration, used by
keywords: fields, time
keywords: time field defined
keywords: how to, define time field

---

Creates a new time [ FieldType](dcsFieldTypeClass.html).
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public static FieldType NewTime(<br />   DateTimeFormat fmt<br />);**  </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Shared Function NewTime( _<br />   ByVal fmt As [DateTimeFormat](dcsDateTimeFormatEnumeration.html)       _<br />) As [FieldType](dcsFieldTypeClass.html)**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc NewTime Type(FieldType) Access(*Public) Shared(*Yes)<br />   DclSrParm fmt Type(DateTimeFormat) Len(4)** 
      </pre>
      <pre />

Parameters

<dl>
        <dt>
 *fmt* 
        </dt>
        <dd>
          [DateTimeFormat](dcsDateTimeFormatEnumeration.html). The format of 
						the time field.</dd>
</dl>

Exceptions

**System.ArgumentException** . Thrown if *fmt* is **YMD** , **MDY** , **DMY** , or **JUL** .
Remarks

**NewTime** constructs a **FieldType** that represents a DataGate time field. Time fields contain 24-hour clock time data in a variety of formats, as specified by fmt (see [ DateTimeFormat](dcsDateTimeFormatEnumeration.html) for details). The storage size of a time field is 8 bytes. 

The value of *fmt* may not be **YMD** , **MDY** , **DMY** , or **JUL** .

Note that internally, DCS manipulates date, time, and timestamp fields as **System.DateTime** value types. The object value returned by DCS as the value of a date, time, or timestamp field (in methods such as [ As400Program.ParmToObject](dcsAs400ProgramClassParmToObjectMethodMain.html)) will be converted from a value of DateTime. Likewise, DCS will only accept values that can be accurately converted to DateTime values, for setting the value of date, time, or timestamp fields.
Examples

<pre>
   <span class="lang"> **[C#]** 
        </span>
  /* Use the already initialized As400OProgram "timeProg" to set the
   * value of a DateTime variable. This program accepts a time data 
            type
   * whose time format is ISO as its sole parameter, which it does not
   * read but uses to return data. */

  ProgParmType as400Time = new ProgParmType("TimeISO", 0, 
            FieldType.NewTime(DateTimeFormat.ISO));
  ProgParm timeParm = new ProgParm(as400Time, DataDirection.Output);
  timeProg.AppendParm(timeParm);

  timeProg.Execute();

  DateTime currentTime;
  currentTime = Convert.ToDateTime(timeProg.ParmToObject(timeParm, 
            Type.GetType("System.DateTime"), 0));
  /* IMPORTANT NOTE: The time and date data types do not return all the 
            information
   * which a .NET DateTime can contain. Specifically, if you specify a 
            parm as a NewTime,
   * the data portion of the returned DateTime will be set to MinValue- 
            time format *USA
   * will zero out the seconds as well. The same will happen to the 
            time portion of a
   * variable if its IBM i parm was set to be a NewDate. */</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Use the already initialized As400OProgram "timeProg" to set the
  ' value of a DateTime variable. This program accepts a time data type
  ' whose time format is ISO as its sole parameter, which it does not
  ' read but uses to return data.

  Dim as400Time As New ProgParmType("TimeISO", 0, 
            FieldType.NewTime(DateTimeFormat.ISO))
  Dim timeParm As New ProgParm(as400Time, DataDirection.Output)
  timeProg.AppendParm(timeParm)

  timeProg.Execute()

  Dim currentTime As DateTime
  currentTime = Convert.ToDateTime(timeProg.ParmToObject(timeParm, 
            Type.GetType("System.DateTime"), 0))
  ' IMPORTANT NOTE: The time and date data types do not return all the 
            information
  ' which a .NET DateTime can contain. SpecIfically, If you specIfy a parm 
            as a NewTime,
  ' the data portion of the returned DateTime will be set to MinValue- time 
            format *USA
  ' will zero out the seconds as well. The same will happen to the time 
            portion of a
  ' variable If its IBM i parm was set to be a NewDate. </pre>

Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html)

<span> **Assembly:** ASNA DataGate Client</span> 

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [FieldType Class](dcsFieldTypeClass.html)
      <br />
      [FieldType Class Members](dcsFieldTypeMembers.html)
      <br />
      [DateTimeFormat Enumeration](dcsDateTimeFormatEnumeration.html)
      <br />
      [As400Program.ParmToObject](dcsAs400ProgramClassParmToObjectMethodMain.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

