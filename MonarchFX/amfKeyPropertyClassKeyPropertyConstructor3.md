---
title: KeyProperty(String, String)

Id: amfKeyPropertyClassKeyPropertyConstructor3
TocParent: amfKeyPropertyClassConstructors
TocOrder: 30

---

This method constructs a new instance of a **KeyProperty** object with indicator expression and text values established.

#### Syntax
<pre class="prettyprint"> **BegConstructor KeyProperty Access(*Public)
  DclSrParm *indicatorExpressionString*  Type(*String)
  DclSrParm *text*  Type (*String)** </pre>

#### Parameters
<dl>
        <dt>
 *indicatorExpressionString* 
        </dt>
        <dd>String containing an indicator expression in the form 
 *'Fkey text ind'*  where 
 *Fkey*  is the function key, 
 *text*  is text associated with the function
        key, and 
 *ind*  is a response option indicator
        expression.  For example, "F3 Add 07:!99".</dd>
        <dt>
 *text* 
        </dt>
        <dd>String containing additional text.</dd>
</dl>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[KeyProperty Class](amfKeyPropertyClass.html) <br /> [ KeyProperty Class Members](amfKeyPropertyClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
