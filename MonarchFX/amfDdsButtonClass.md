---
title: DdsButton Class

Id: amfDdsButtonClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 150

keywords: DdsButton class, about DdsButton class
keywords: classes [ASNA.Monarch.WebDspF], DdsButton class
keywords: Web server controls, button

---

The **DdsButton** is a class that defines a single 'button' control for a corresponding attention key or function key defined in [ DdsRecord](amfDdsRecordClass.html).

For a list of all members of this type, see [DdsButton Members](amfDdsButtonClassMembers.html).

For a short explanation of this class in use, see the [DdsButton Description](amfUnderstandingButtons.html).

#### Applicable Products:
**Monarch, Wings, Mobile RPG** 
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
 **ASNA.Monarch.WebDspF.DdsButton**       </pre>

#### Syntax
<pre class="syntax"> **public class DdsButton Inherits System.Web.UI.WebControls.WebControl** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
An instance of **DdsButton** represents a single button control that can be placed anywhere on the form with the characteristics of the corresponding attention key or functions key setting defined in <a> **DdsRecord** </a>.

The [ AidKey](amfDdsButtonClassAidKeyProperty.html) property is set to a function key defined in [ DdsRecord.FuncKeys](amfDdsRecordClassFuncKeysProperty.html) containing the text and response indicators from the property that corresponds to the **aidKey** value specified. The [ FieldName](amfDdsButtonClassFieldNameProperty.html) property is used for the name of the field the button is emulating.

For example, the **FuncKeys** property for the containing **DdsRecord** contains ** *F4 'PROMPT' 04;F6 'ADD' 06 : !30;F11 'Delete' 11 : !30;F12 'Cancel' 12* ;** . If the **AidKey** property for the **DdsButton** is set to **F12** , the **getStringFromKey** method would return ** *'Cancel 12'* ** , where ***Cancel*** is used as the text for the button, and ** *12* ** is the response indicator turned on when the input data is transmitted from the browser.

Four styles can be used to control how a **DdsButton** will appear on the web page. The [ ButtonStyle](amfDdsButtonClassButtonStyleProperty.html) property is used for this purpose as follows.

- Use ButtonStyle 
 **Link**  to create a hyperlink-style button on the
        Web page. This control has the same appearance as a 
 **Hyperlink**  but has
        the functionality of a Button.
- Use ButtonStyle **Icon**  to choose a mobile-friendly 
		  icon from the ASNA.urated selection.
- Use ButtonStyle 
 **Image**  to specify an image as a
        clickable button on the web page. This appears as an
        image but has the same functionality as a Button. The

        [
        Image](amfDdsButtonClassImageProperty.html) property will contain the path to this image
        used.
- Use ButtonStyle 
 **Button**  to create a standard button with
        that functionality. The 
        [
        Text](amfDdsButtonClassTextProperty.html) property contains the value to be displayed for the
        button.

Additionally, you can use the [ OnMouseOverImage](amfDdsButtonClassOnMouseOverImageProperty.html) property to specify an image that can be displayed when the user rolls the mouse over the button when the ButtonStyle is Image. When set, this property is used instead of the **ToolTip** property. Position can be set with the [ VirtualRowCol](amfDdsButtonClassVirtualRowColProperty.html) property.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ DdsButton Members](amfDdsButtonClassMembers.html) <br />[DdsButton Description](amfUnderstandingButtons.html)<br /> [Overview of Aid Keys](amfconOverviewofAidKeys.html) 
