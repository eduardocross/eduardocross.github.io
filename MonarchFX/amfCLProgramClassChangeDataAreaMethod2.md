---
title: CLProgram.ChangeDataArea(string, string)

Id: amfCLProgramClassChangeDataAreaMethod2
TocParent: amfCLProgramClassChangeDataAreaMethods
TocOrder: 20

---

Changes the values of the current data area to be associated with the program.

#### Syntax
<pre class="syntax"> **BegSr ChangeDataArea Access(*Protected) Type(Void)
   DclSrParm *dataArea*  Type(*String)
   DclSrParm *newValue*  Type(*String)**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *dataArea* </code>
        </dt>
        <dd>

String. The path to the data area to change.
</dd>
        <dt>
          <code> *newValue* </code>
        </dt>
        <dd>

String. The new data area values for the substitution variables in the dataArea. The format of each variable must be defined in the CL program parameters.
</dd>
</dl>

#### Remarks
This method changes the values of the *dataArea* but does not change the other attributes.
<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
