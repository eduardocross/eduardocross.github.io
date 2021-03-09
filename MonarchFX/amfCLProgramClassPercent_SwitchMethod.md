---
title: CLProgram.Percent_Switch Method

Id: amfCLProgramClassPercent_SwitchMethod
TocParent: amfCLProgramClassMethods
TocOrder: 160

keywords: Percent_Switch method
keywords: CLProgram.Percent_Switch method
keywords: sws
keywords: sws, checking settings
keywords: job switches, checking settings
keywords: how to, determine job switch settings

---

This method compares a bit-mask against the current job switch ( *sws* ) settings and returns a value of '1' if the comparison is equal, otherwise, '0'.

#### Syntax
<pre class="syntax"> **BegFunc Percent_Switch Access(*Protected) Type(*String) 
   DclSrParm *mask*  Type(*String) Len(8)**       </pre>

#### Parameters
<dl>
        <dt>
          <code> *mask* </code>
        </dt>
        <dd>

String. The mask showing the job switches that are to be compared and the on/off test value. Each position within the mask corresponds with a job switch i.e. position 1 compared to switch 1. Values for each position within the mask are:

- <code>0</code> - Check job switch for a 0 (off).
- <code>1</code> - Check job switch for a 1 (on).
- <code>X</code> - Do not check this switch.

</dd>
</dl>

#### Return Value
String. A value of '1' if the comparison of every switch is the same, otherwise, the result is '0'.
<!-- start -->

#### Requirements
**Namespace:** [ASNA.Monarch](amfMonarchNamespace.html)

**Assembly:** ASNA.VisualRPG.Runtime.DLL 

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->      

#### See Also
[CLProgram Class](amfCLProgramClass.html) <br clear="none" /> [ CLProgram Class Members](amfCLProgramClassMembers.html) <br clear="none" /> [ASNA.Monarch Namespace](amfMonarchNamespace.html) 
