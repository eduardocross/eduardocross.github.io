---
title: WebDisplayFile Class

Id: amfWebDisplayFileClass
TocParent: amfMonarchNamespaceClasses
TocOrder: 240

keywords: WebDisplayFile class
keywords: WebDisplayFile class, about WebDisplayFile class
keywords: classes [ASNA.Monarch], WebDisplayFile class

---

The **WebDisplayFile** class provides for form control for program web device, program, and job.

For a list of all members of this type, see [ WebDisplayFile Members](amfWebDisplayFileClassMembers.html).
<!--mine -->

#### Inheritance Hierarchy
<pre>[ ASNA.Monarch](amfMonarchNamespace.html)
 **ASNA.Monarch.WebDisplayFile**       </pre>

#### Syntax
<pre class="prettyprint"> **public class WebDisplayFile Inherits System.Object**       </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
A display file is composed of one or more formats, each defining a template of what is to be shown in a segment of the screen. Each format may contain input and/or output fields and constants as well as directives on how to display each of these elements and the interaction of this format with other formats present on the screen.

DDS is the primary means of defining a display file. Each element on a display file might be conditioned with an indicator, as part of a write operation an array of boolean indicators must be provided enabling the display file engine to determine whether to display conditioned elements.

With each format definition a list of AID keys (i.e.: function keys) available to the user is specified. As part of each entry in the list, a caption is provided and the index of the indicator array to "turn on" if the user does indeed press that key.
<!-- -->

#### Requirements
<table class="dttable" cellspacing="0" cellpadding="4" width="60%">
           <colgroup>
            <col width="15%" style="font-weight:bold" />
            <col width="85%" />
          </colgroup>
          <tr>
            <td>Namespace:</td>
            <td>[ASNA.Monarch](amfMonarchNamespace.html)</td>
          </tr>
          <tr>
            <td>Assembly:</td>
            <td>ASNA.VisualRPG.Runtime.DLL</td>
          </tr>
         <tr>
            <td>Platforms:</td>
            <td> Windows Server 2012, Windows Server 2012 R2, Windows Server 2016,  Windows 7, Windows 8 Pro, Windows 10 Pro</td>
         </tr>
</table>

<!-- end -->

#### See Also
[ASNA.Monarch Namespace](amfMonarchNamespace.html) <br /> [ WebDisplayFile Class Members](amfWebDisplayFileClassMembers.html)
