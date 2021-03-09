---
title: DdsSubfile.IsNotFalse Method

Id: amfDdsSubfileClassIsNotFalseMethod
TocParent: amfDdsSubfileClassMethods
TocOrder: 30

keywords: DdsSubfile.IsNotFalse method
keywords: IsNotFalse method
keywords: how to, test conditional value for subfile field
keywords: conditioning expressions, testing for subfile fields
keywords: subfiles, conditional field expression test
keywords: subfile fields, conditional expression test
keywords: subfile records, conditional field expression test
keywords: web controls, conditional field expression test
keywords: subfile usage, conditional field expression test

---

This method returns **True** if the condition for the fieldID is not false.

#### Syntax
<pre class="prettyprint"> **BegFunc IsNotFalse Access(*Public) Type(*Boolean) Modifier(*Overrides)
   DclSrParm *fieldID*  Type(*string)
   DclSrParm *condition*  Type(*string)** </pre>

#### Parameters
<dl>
        <dt>
 *fieldID* 
        </dt>
        <dd>String containing the ID for the field to
        evaluate.</dd>
        <dt>
 *condition* 
        </dt>
        <dd>String containing the condition to evaluate.</dd>
</dl>

#### Return Value
**True** if the *condition* for the *fieldID* is not false; otherwise **False** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsSubfile Class](amfDdsSubfileClass.html) <br /> [ DdsSubfile Class Members](amfDdsSubfileClassMembers.html) <br /> [ ConditionalValue Class](amfConditionalValueClass.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
