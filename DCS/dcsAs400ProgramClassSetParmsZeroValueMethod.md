---
title: As400Program.SetParmsZeroValue Method

Id: dcsAs400ProgramClassSetParmsZeroValueMethod
TocParent: dcsAs400ProgramMethodsMain
TocOrder: 7

keywords: SetParmsZeroValue method
keywords: As400Program.SetParmsZeroValue method
keywords: parameter lists, set program parameter list to zeroes
keywords: program parameters, set parameter list to zeroes
keywords: parameters, set program parameter list to zeroes
keywords: how to, set program parameter list to zeroes

---

Sets all parameters in the parameter list to default 'zero' values.
<pre class="prettyprint">
        <span class="lang">[C#]</span>
 **public SetParmsZeroValue(
);** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual Basic] </span>
 **Public Function SetParmsZeroValue( )** 
      </pre>
      <pre class="prettyprint">
        <span class="lang">[Visual RPG]</span>
 **BegFunc SetParmsZeroValue Access(*Public)** 
      </pre>

Remarks

Use **SetParmsZeroValue** when a program has a large number of input parameters but only a few must be set explicitly for the server program to run effectively. **SetParmsZeroValue** does not remove parameters from the parameter list.
Requirements

**Namespace:** [ASNA.DataGate.Client](dcsDataGateClientNamespace.html) 

**Assembly:** ASNA DataGate Client

**Platforms:** Windows Server 2008 R2, Windows Server 2012, Windows 7, Windows 8 Pro, Windows 8.1 Pro, Windows 10
See Also

<dl />
      [As400Program Class](dcsAs400ProgramClass.html)
      <br />
      [
					As400Program Class Members](dcsAs400ProgramMembers.html)
      <br />
      [ASNA.DataGate.Client 
					Namespace](dcsDataGateClientNamespace.html)

