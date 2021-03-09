---
title: DdsFile Class

Id: amfDdsFileClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 250

keywords: DdsFile class, about DdsFile class
keywords: classes [ASNA.Monarch.WebDspF], DdsFile class
keywords: attention keys, abouts
keywords: attention keys, container class
keywords: function keys, about
keywords: function keys, container class

---

The **DdsFile** class is the container object responsible for enabling and processing function keys. It decides which function keys to draw on the form. When the user selects a function key, the appropriate indicators are turned on. The DdsFile control is displayed as a key banner. If a function key is not enabled, the function keys in the banner are grayed out.

For a list of all members of this type, see [DdsFile Members](amfDdsFileClassMembers.html).

#### Applicable Products:
**Monarch, Wings, Mobile RPG** 
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
 **ASNA.Monarch.WebDspF.DdsFile** </pre>

#### Syntax
<pre class="prettyprint"> **public class DdsFile Inherits System.Web.UI.Control** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
**DdsFile** has four important properties [ AttnKeys](amfDdsFileClassAttnKeysProperty.html), [ FuncKeys](amfDdsFileClassFuncKeysProperty.html), [ EnterText](amfDdsFileClassEnterTextProperty.html), and [ ResetText](amfDdsFileClassResetTextProperty.html).

The **AttnKeys** property controls which keys the user can press, the message to be displayed, and the response indicators to turn on. The attention key settings are in a semicolon( **;** ) separated list of function key, 'text', and response **:** option indicators.
<pre>     For example: 
        F10 'Finished' 07 : !99;F4 'Skip' *NONE : 09;</pre>

This property is mainly used to control processing within the application to control flow within the form since NO input data is transmitted from the browser.

The **FuncKeys** property contains all function key settings in a semicolon( **;** ) separated list of function key, 'text' and response **:** option indicators.
<pre>     For example: 
        F3 'Add' 07 : !99;F4 'Delete' *NONE : 09;</pre>

This property is mainly used to control processing between applications since input data is transmitted from the browser.

The **EnterText** and **ResetText** properties allow text labels to be established for the Enter and Reset keys respectively as there is no mechanism to provide text because these keys cannot be 'enabled' by a record format (or file).

Refer to [ Web.config Considerations](amfconWebConfigConsiderations.html) for more information on how to establish labels for function keys for foreign language applications.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br clear="none" /> [DdsFile Class Members](amfDdsFileClassMembers.html) <br clear="none" /> [ Web.config Considerations](amfconWebConfigConsiderations.html) 
