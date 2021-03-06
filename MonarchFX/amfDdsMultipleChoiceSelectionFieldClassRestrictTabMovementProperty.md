---
title: RestrictTabMovement Property

Id: amfDdsMultipleChoiceSelectionFieldClassRestrictTabMovementProperty
TocParent: amfDdsMultipleChoiceSelectionFieldClassPropertiesMain
TocOrder: 30

keywords: MultipleChoiceSelectionField RestrictTabMovement
keywords: RestrictTabMovement

---

This property is not yet fully implemented. At time of writing it preserves the RSTCSR keyword but does not effect .NET behavior.

Sets whether or not to restrict tab movement within the selection field. This preserves the RSTSCR keyword.

#### Syntax
<pre class="prettyprint"> **BegProp RestrictTabMovement Access(*Public) Type(*boolean) Modifier(*Overrides)
   BegGet;  BegSet** </pre>

#### Property Values
Boolean that determines whether to restrict tab movement within the selection field. This preserves the RSTSCR keyword. Defaults to <code>False</code>.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsMultipleChoiceSelectionField Class](amfDdsMultipleChoiceSelectionFieldClass.html) <br clear="none" />[ SingleChoiceSelectionField Class Members](amfDdsMultipleChoiceSelectionFieldClassMembers.html)<br clear="none" />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
