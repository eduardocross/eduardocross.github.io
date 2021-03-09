---
title: DdsDecRange Class

Id: amfDdsDecRangeClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 232

keywords: DdsDecRange class, about DdsDecRange class
keywords: classes [ASNA.Monarch.WebDspF], DdsDecRange class
keywords: field controls, decimal control

---

**DdsDecRange** creates a control that allows users to select a range of numerical options.

For a list of all members of this type, see [ DdsDecRange Members](amfDdsDecRangeClassMembers.html).

#### Applicable Products:
**Monarch, Wings, Mobile RPG** 
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
    [ASNA.Monarch.WebDspF.DdsField](amfDdsFieldClass.html)      
        [ASNA.Monarch.WebDspF.DdsDataField](amfDdsDataFieldClass.html)
 **ASNA.Monarch.WebDspF.DdsDecRange** </pre>

#### Syntax
<pre class="prettyprint"> **Public class DdsDecRange Inherits DdsDataField** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
An instance of **DdsDecRange** represents a user-input text box or dropdown box that allows decimal fields.

The default style for a DdsDecRange is **Textbox** . The initial default of a DdsDecRange is to display as a Textbox that accepts any decimal values from the user. However, use the [ Values](amfDdsDataFieldClassValuesProperty.html) property to enter the valid values that the application can accept from the user. If the user may not know what the values mean, also use the [ ValuesText](amfDdsDataFieldClassValuesTextProperty.html) property to indicate text for each of the entries in the **Values** property. However, for the entries in **Values** and/or the **ValuesText** to display for the user, use the [ ValuesStyle](amfDdsDataFieldClassValuesStyleProperty.html) property to specify whether just the **Values** or the ValuesText displays, or whether you want **both** of them to display in a drop-down box. ** *Please note that this also applies to Multi-line textboxes.* ** 
<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ DdsDecRange Class Members](amfDdsDecRangeClassMembers.html) 
<!-- last one -->

