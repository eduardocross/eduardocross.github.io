---
title: DdsButton.TextField Property

Id: amfDdsButtonClassTextFieldProperty
TocParent: amfDdsButtonClassProperties
TocOrder: 83

keywords: TextField property
keywords: DdsButton.TextField property

---

Defines the name of a record field used to report the data for the Text .

#### Syntax
<pre class="prettyprint"> **BegProp TextField Access(*Public) Type(*String)
   BegGet;  BegSet** </pre>

#### Property Values
String. Sets the name of the record field used to report the Text. Requires [DdsButton.TextFieldLength](amfDdsButtonClassTextFieldLengthProperty.html).

#### Remarks
This sets a CharField in an IBM i record to draw the data for the text from. It must be used with [TextFieldLength](amfDdsButtonClassTextFieldLengthProperty.html) in order to avoid throwing an error. This property is very useful if the Text is likely to be changed or updated frequently, or if it will be used in multiple places throughout the site. Overrides [Text](amfDdsButtonClassTextProperty.html).

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsButton Description](amfUnderstandingButtons.html)<br /> [ DdsButton Class](amfDdsButtonClass.html) <br /> [ DdsButton Class Members](amfDdsButtonClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
