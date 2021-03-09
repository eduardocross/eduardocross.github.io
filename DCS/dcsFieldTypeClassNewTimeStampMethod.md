---
title: FieldType.NewTimeStamp Method

Id: dcsFieldTypeClassNewTimeStampMethod
TocParent: dcsFieldTypeMethods
TocOrder: 10

keywords: NewTimeStamp method
keywords: FieldType.NewTimeStamp method
keywords: fields, timestamp
keywords: timestamp field defined
keywords: how to, define timestamp field

---

Creates a new timestamp [ FieldType](dcsFieldTypeClass.html).
<pre class="prettyprint">        <span class="lang">[C#]</span>
 **public static FieldType NewTimeStamp();**  </pre>
      <pre class="prettyprint">        <span class="lang">[Visual Basic] </span>
 **Public Shared Function NewTimeStamp() As [FieldType](dcsFieldTypeClass.html)**  </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc NewTimeStamp Type(FieldType) Access(*Public) Shared(*Yes)** 
      </pre>

Remarks

**NewTimeStamp** constructs a **FieldType** which represents a DataGate timestamp field. Timestamp fields contain calendar date and 24-hour clock time data denoting a specific instant in time. The storage size of a timestamp field is 26 bytes.

**Note** : Internally, DCS manipulates date, time, and timestamp fields as **System.DateTime** value types. The object value returned by DCS as the value of a date, time, or timestamp field (in methods such as [As400Program.ParmToObject](dcsAs400ProgramClassParmToObjectMethodMain.html)) will be converted from a value of DateTime. Likewise, DCS will only accept values which can be accurately converted to DateTime values, for setting the value of date, time, or timestamp fields.
Examples

<pre>        <span class="lang">
 **[C#]** 
        </span>
  /* Use the already initialized As400OProgram "timeProg" to set the
   * value of a DateTime variable. This program accepts a timestamp data type
   * whose time format is ISO as its sole parameter, which it does not
   * read but uses to return data. */

  ProgParmType as400Time = new ProgParmType("TimeISO", 0, FieldType.NewTimestamp());
  ProgParm timeParm = new ProgParm(as400Time, DataDirection.Output);
  timeProg.AppendParm(timeParm);

  timeProg.Execute();

  DateTime currentTime;
  currentTime = Convert.ToDateTime(timeProg.ParmToObject(timeParm, Type.GetType("System.DateTime"), 0));
  /* Unlike the IBM i FieldType NewTime or NewDate, NewTimeStamp contains both date and time
   * values. */</pre>
      <pre>        <span class="lang">
 **[Visual Basic]** 
        </span>
  ' Use the already initialized As400OProgram "timeProg" to set the
  ' value of a DateTime variable. This program accepts a timestamp data type
  ' whose time format is ISO as its sole parameter, which it does not
  ' read but uses to return data. 

  Dim as400Time As New ProgParmType("TimeISO", 0, FieldType.NewTimestamp())
  Dim timeParm As New ProgParm(as400Time, DataDirection.Output)
  timeProg.AppendParm(timeParm)

  timeProg.Execute()

  Dim currentTime As DateTime
  currentTime = Convert.ToDateTime(timeProg.ParmToObject(timeParm, Type.GetType("System.DateTime"), 0))
  ' Unlike the IBM i FieldType NewTime or NewDate, NewTimeStamp contains both date and time
  ' values. </pre>

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
      [As400Program.ParmToObject](dcsAs400ProgramClassParmToObjectMethodMain.html)
      <br />
      [ASNA.DataGate.Common Namespace](dcsDataGateCommonNamespace.html)

