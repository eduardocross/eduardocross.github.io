---
title: ChoiceControlField Property

Id: amfDdsSelectionFieldChoiceClassChoiceControlFieldProperty
TocParent: amfDdsSelectionFieldChoiceClassPropertiesMain

keywords: SelectionFieldChoice ChoiceControlField
keywords: Choice Text

---

Name of a hidden field that contains the input behavior's control value.

#### Syntax
<pre class="prettyprint"> **BegProp ChoiceControlField Access(*Public) Type(*string) Modifier(*Overrides)
   BegGet;  BegSet** </pre>

#### Property Values
String that defines a hidden field that contains the input behavior's control value. Defaults to <code>(Empty)</code>.
<table>
	<tr><th>Control  Value</th><th>Meaning on Output</th><th>Meaning on Input</th></tr>
	<tr><td>0</td><td>Available</td><td>Unselected</td></tr>
	<tr><td>1</td><td>Selected</td><td>Selected</td></tr>
	<tr><td>2,3,4</td><td>Unavailable</td><td>Unavailable</td></tr>
</table>

**Note &#8211;** on IBM i, the values 2, 3 and 4 define when the cursor can or cannot be positioned. This does not apply to Web Browsers. 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSelectionFieldChoice Class](amfDdsSelectionFieldChoiceClass.html) <br clear="none" />[ DdsSelectionFieldChoice Class Members](amfDdsSelectionFieldChoiceClassMembers.html)<br clear="none" />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
