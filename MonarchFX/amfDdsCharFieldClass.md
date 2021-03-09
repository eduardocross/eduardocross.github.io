---
title: DdsCharField Class

Id: amfDdsCharFieldClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 160

keywords: DdsCharField class, about DdsCharField class
keywords: classes [ASNA.Monarch.WebDspF], DdsCharField class

---

**DdsCharField** is a derived class that further defines a character field and can be displayed as a text box, dropdown box, or a checkbox.

For a list of all members of this type, see [ DdsCharField Members](amfDdsCharFieldClassMembers.html).

#### Applicable Products:
**Monarch, Wings, Mobile RPG** 
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
    [ASNA.Monarch.WebDspF.DdsField](amfDdsFieldClass.html)
    [ASNA.Monarch.WebDspF.DdsDataField](amfDdsDataFieldClass.html)
 **ASNA.Monarch.WebDspF.DdsCharField** </pre>

#### Syntax
<pre class="syntax"> **public class DdsCharField: Inherits DdsDataField** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
An instance of **DdsCharField** represents a text box, dropdown box, or checkbox. The DdsCharField control has a CssClass called **DdsCharField** . See [More about Style Sheets](../../../../../../MonarchFX/_HTML/amfMoreAboutStyleSheets.html) for additional information.

The default style for a **DdsCharField** is a **Textbox** that accepts any values from the user. Use the [ Values](amfDdsDataFieldClassValuesProperty.html) property to enter the valid values that the application can accept from the user. If the user may not know what the values mean, also use the [ ValuesText](../../../../../../MonarchFX/_HTML/amfDdsDataFieldClassValuesTextProperty.html) property to indicate text for each of the entries in the **Values** property. However, for the entries in **Values** and/or the **ValuesText** to display for the user, use the [ ValuesStyle](../../../../../../MonarchFX/_HTML/amfDdsDataFieldClassValuesStyleProperty.html) property to specify whether just the **Values** or the **ValuesText** displays or whether you want **both** to display in a drop-down box. ** *Please note that this also applies to Multi-line textboxes.* ** 

When the field is set to display as a **Checkbox** , you will need to know what the valid values for the field are and determine the accepted values when the Checkbox is checked or unchecked. To do this, specify entries in the [ DefaultValue](../../../../../../MonarchFX/_HTML/amfDdsCharFieldClassDefaultValueProperty.html), [ CheckedValue](../../../../../../MonarchFX/_HTML/amfDdsCharFieldClassCheckedValueProperty.html) or [ UnCheckedValue](../../../../../../MonarchFX/_HTML/amfDdsCharFieldClassUncheckedValueProperty.html) properties.
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro
<!-- end -->

#### See Also
<dl>
        <dd>
		[
        ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
        <dd>
		[
        DdsCharField Members](amfDdsCharFieldClassMembers.html)</dd>
</dl>

