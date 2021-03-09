---
title: dgException Class

Id: dcsdgExceptionClass
TocParent: dcsASNADataGateCommonClasses
TocOrder: 0

keywords: classes [DCS 16.0 dgException class
keywords: dgException class
keywords: dgException class, about dgException class

---

The exception that is thrown by DCS to indicate procedural conditions, including errors.

For a list of all members of this type, see [ dgException Members](dcsdgExceptionClassMembers.html).

[ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) <br /> ASNA.DataGate.Common.dgException
<pre class="prettyprint">System.Exception
   ASNA.DataGate.Common.dgException
&lt;Serializable&gt;
Public Class <span>dgException</span></pre>

Thread Safety

Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
Remarks

Exceptions specific to the DataGate provider being accessed by DCS are communicated through <span> **dgException** </span>. Most often, these exceptions are in the form of a condition identifier (provided by the [ Error](dcsdgExceptionClassErrorField.html) field) and a text message (provided by the [ Message](dcsdgExceptionClassMessageProperty.html) property).

The [ErrorClass](dcsdgExceptionClassErrorClassField.html) field classifies the condition identifier as one of the categories given by the <span>dgErrorClass</span> enumeration. The [SystemError](dcsdgExceptionClassSystemErrorField.html) field contains a provider-dependent exception identifier for certain exceptions. Likewise, the [Text](dcsDisconnectingfromaDatabase.html) field may contain text messages given by the underlying database for the exception.

DCS throws other exceptions besides <span> **dgException** </span>. Please see the documentation for the particular DCS object or method call for a description of the exceptions thrown.

**dgException** inherits from <span>System.Exception</span>, which provides many useful functions for diagnosing and reporting bugs in your code and DCS.
Requirements

**Namespace:** [ASNA.DataGate.Common](dcsDataGateCommonNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [dgException Members](dcsdgExceptionClassMembers.html)
      <br />
      [ASNA DataGate Common Namespace](dcsDataGateCommonNamespace.html)
      <br />

