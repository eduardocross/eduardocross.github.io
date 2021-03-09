---
title: DdsSubfileControl.DisplayFields Property

Id: amfddsSubfileControlClassDisplayFieldsProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 20

keywords: DisplayFields property
keywords: DdsSubfileControl.DisplayFields property
keywords: subfiles, controlling fields display
keywords: subfile fields, displaying
keywords: subfile records, displaying
keywords: displaying, fields
keywords: user fields, displaying
keywords: how to, control display of subfile fields
keywords: conditioning expressions, controlling subfile control field display
keywords: indicator expressions, controlling subfile control field display
keywords: SFLDSPCTL

---

Gets or sets a string value containing an indicator expression (condition) that when evaluated indicates **True** , causes the fields in the format to display (SFLDSPCTL).

#### Syntax
<pre class="prettyprint"> **BegProp DisplayFields Access(*Public) Type(*String)
   BegGet: BegSet** </pre>

#### Property Values
String. A string value containing an indicator expression or the special value ***True** or ***False** . When the condition evaluates **True** , the fields in the format are displayed. For example setting this property to "03 &amp; !90" means that if *IN03 is *ON and *IN90 is *OFF (condition is true), the fields in the format will display.

#### Remarks
The **DisplayFields** property works similar to the **SFLDSPCTL** keyword so that your program displays fields in the subfile control record format when your program sends an output operation to the subfile control record format. If you do not use an option indicator with this keyword, such as **!90** , the subfile control record is displayed on every output operation to the subfile control record format.

**Note** : **DisplayFields** must be in effect when the subfile is displayed for an input operation to the subfile control record to be valid, even if there are no displayable fields in the subfile control record format. If **DisplayFields** is not in effect for an input operation, the runtime error, "Invalid input attempt on format" will be issued.

To set this property at design-time, click on the right of the **DisplayFields** property and enter the indicator expression.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
