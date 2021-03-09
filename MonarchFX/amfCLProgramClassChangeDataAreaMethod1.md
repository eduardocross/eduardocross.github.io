---
title: CLProgram.ChangeDataArea(string,integer,integer,string)

Id: amfCLProgramClassChangeDataAreaMethod1
TocParent: amfCLProgramClassChangeDataAreaMethods
TocOrder: 10

---

Changes the values of the current data area associated with the program.

#### Syntax
<pre class="syntax"> **BegSr ChangeDataArea Access(*Protected) Type(Void)
   DclSrParm *dataArea*  Type(*String)
   DclSrParm *start*  Type(*Integer)
   DclSrParm *length*  Type(*Integer)
   DclSrParm *newValue*  Type(*String)** 
      </pre>

#### Parameters
<dl>
        <dt>
          <code> *dataArea* </code>
        </dt>
        <dd>

String. The path to the data area to change.
</dd>
        <dt>
          <code> *start* </code>
        </dt>
        <dd>

Integer. The starting point within the *dataArea.* 
</dd>
        <dt>
          <code> *length* </code>
        </dt>
        <dd>

Integer. The length of the data area to be changed.
</dd>
        <dt>
          <code> *newValue* </code>
        </dt>
        <dd>

String. The new data area values for the substitution variables in the *dataArea* . The format of each variable must be defined in the CL program parameters.
</dd>
</dl>

#### Remarks
This method changes values within the *dataArea* , as specified by the *start* position and *length* , replaced with *newValue,* but does not change the other attributes.
<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
<dl><dt>
        [CLProgram
        Class](amfCLProgramClass.html)
        <br clear="none" />
        [
        CLProgram Class Members](amfCLProgramClassMembers.html)
        <br clear="none" />
        [ASNA.Monarch
        Namespace](amfMonarchNamespace.html)
      </dt></dl>

