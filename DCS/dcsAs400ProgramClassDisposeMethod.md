---
title: As400Program.Dispose Method

Id: dcsAs400ProgramClassDisposeMethod
TocParent: dcsAs400ProgramMethodsMain
TocOrder: 2

keywords: releasing IBM i program system resources
keywords: Dispose method
keywords: As400Program.Dispose method

---

Release unmanaged resources associated with **As400Program** . 
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public virtual new void Dispose** ();</pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Overridable NotOverridable Sub Dispose()** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegSr Dispose Access(*Public) Modifier(*Overridable)** 
      </pre>

Exceptions

None.
Remarks

The **As400Program** class implements the <span>IDisposable</span> interface. Currently **As400Program** does not directly use unmanaged resources therefore this implementation of <span> **Dispose** </span> has no effect.

This method is provided for future enhancements. To maintain compatibility with future DCS releases, it is recommended that you call the **Dispose** method when your program’s use of **As400Program** is complete (prior to finalization).
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [As400Program Class](dcsAs400ProgramClass.html)
      <br />
      [As400Program Class Members](dcsAs400ProgramMembers.html)
      <br />
      [ASNA.DataGate.Client Namespace](dcsDataGateClientNamespace.html)

