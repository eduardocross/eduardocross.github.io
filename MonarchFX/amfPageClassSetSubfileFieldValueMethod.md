---
title: Page.SetSubfileFieldValue Method

Id: amfPageClassSetSubfileFieldValueMethod
TocParent: amfPageClassMethodsMain
TocOrder: 99

keywords: SetSubfileFieldValue method
keywords: Page.SetSubfileFieldValue method

---

Sets the value of a subfile field.

#### Syntax
<pre class="prettyprint"> **SetSubfileFieldValue(FormatName, FieldName, RRN, Object newValue)** </pre>

*FormatName* is the name of the format as visible to the RPG program; not case sensitive. *FeildName* is the name of the feild as visible to the RPG program; not case sensitive. *RRN* is the Relative Record Number of the Subfile as visible to the RPG program; can be set to any valid integer of 1 or greater. *NewValue* is the value that the field will take.

#### Return Value
**Object** . Sets the value of the subfile field specified by FormatName, FieldName, and RRN. The object will be in whatever format the Field held. Any casting must be done with additional methods.

#### Exceptions
None.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
<dl>
        <dd>[Page Class](amfPageClass.html)</dd>
		<dd>[Page Class Methods](amfPageClassMethodsMain.html)</dd>
        <dd>[Page Class Members](amfPageClassMembers.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
</dl>

