---
title: DdsMessagePanel Class

Id: amfDdsMessagePanelClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 270

keywords: FormatNotFoundException
keywords: EmptyFormatException
keywords: ExternalFieldException
keywords: DdsMessagePanel class, about DdsMessagePanel class
keywords: classes [ASNA.Monarch.WebDspF], DdsMessagePanel class

---

The **DdsMessagePanel** class defines a panel that can be used to display messages (instead of **DdsFile** ) when [ DdsFile](amfDdsFileClass.html) messages are hidden ( [ DisplayErrorMessages](amfDdsFileClassDisplayErrorMessagesProperty.html) property is False).

For a list of all members of this type, see [ DdsMessagePanel Members](amfDdsMessagePanelClassMembers.html).

#### Applicable Products:
**Monarch, Wings, Mobile RPG** 
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
 **ASNA.Monarch.WebDspF.DdsMessagePanel** </pre>

#### Syntax
<pre class="prettyprint"> **Public class DdsMessagePanel Inherits System.Web.UI.WebControls.Panel** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.
<!--mine -->

#### Exceptions
The following exceptions may be encountered when the message panel is rendered.
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="50%" /><col width="50%" />
          </colgroup>
          <tr><th>Value</th>
           <th>Condition</th>
          </tr>
          <tr>
            <td>EmptyFormatException</td>
            <td>Display file format is
            empty.</td>
          </tr>
          <tr>
            <td>ExternalFieldException</td>
            <td>Requested field does not
            belong to the display file format.</td>
          </tr>
          <tr>
            <td>            FormatNotFoundException</td>
            <td>Display file format was not
            found.</td>
          </tr>
</table>

<!-- -->

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
<dl>
        <dd>[
        ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
        <dd>[
        DdsMessagePanel Class Members](amfDdsMessagePanelClassMembers.html)</dd>
</dl>

