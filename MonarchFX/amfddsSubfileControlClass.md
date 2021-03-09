---
title: DdsSubfileControl Class

Id: amfddsSubfileControlClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 320

keywords: DdsSubfileControl class, about DdsSubfileControl class
keywords: classes [ASNA.Monarch.WebDspF], DdsSubFileControl class
keywords: message files, avoiding crowded messages
keywords: how to, avoid crowded message display

---

The **DdsSubfileControl** class is an extension of a **DdsRecord** and is both the controller and container of a subfile.

For a list of all members of this type, see [ DdsSubfileControl Members](amfddsSubfileControlClassMembers.html).

#### Applicable Products:
**Monarch, Wings** 
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
    [ASNA.Monarch.WebDspF.DdsRecord](amfDdsRecordClass.html)
 **ASNA.Monarch.WebDspF.DdsSubfileControl** </pre>

#### Syntax
<pre class="prettyprint"> **public class DdsSubfileControl Inherits DdsRecord** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
An instance of **DdsSubfileControl** represents an extension of a DdsRecord. A subfile is typically rendered in a classic tabular format with each record in the subfile providing the data for a row and field shown as a column. It is possible to render a subfile records as a sequence of checkboxes, radio buttons, in a drop-down box or a list box. The [ SubfileStyle](amfddsSubfileControlClassSubfileStyleProperty.html) property determines the widget(s) to use for rendering the subfile.

**Crowded Messages in a Message Subfile** 

Sometimes when multiple messages appear on a message subfile, a vertical scroll bar appears on the right hand side of the subfile area taking just enough real-state to force the browser to add a horizontal scroll bar to the span. If the subfile control specified that only a single line was to be shown at a time, the scroll bars effectively take all the space available for the subfile, making it impossible for the user to read the messages.

In the Error Message Subfile, there are three elements involved:

- Subfile Record Format Control
- Subfile Record Format
- Message Character Field.

#### Example
In the following example, these are three id's: MSGCTL, MSGSFL, and MSGSFL_ZMSGKY.

All of these controls should have the adequate dimensions to allow for multiple messages to display comfortably. As you can see from the "HTML" sample, the **MSGSFL_ZMSGKY** (DdsCharField) has a **Width** of 656 pixels, but **MSGCTL** (DdsSubfileControl) and **MSGSFL** (DdsSubfile) are only 574 pixels wide. You should set them all the same width and that being as large as the space taken by the longest message you expect (measured in pixels). You can also set your subfile page to be more than one on MSGCTL and then the user could see multiple messages at a time. Finally, setting the SubfilePage property to 0 avoids the vertical scroll bar altogether and displays all records on the screen. Refer the [ DdsSubfileControl Members](amfddsSubfileControlClassMembers.html) for more information on specific property setting for controlling the display of messages.
<pre class="example">
              <span style="color:blue">&lt; mdf:DdsSubfileControl id ="MSGCTL" <span style="COLOR: red">runat</span>="server" <span style="COLOR: red">style</span>="<span style="COLOR: red">POSITION</span>: relative"
                <span style="COLOR: red">Alias</span>="MSGCTL" <span style="COLOR: red">CssClass</span>="DdsRecord" <span style="COLOR: red">ms_positioning</span>="GridLayout" <span style="COLOR: red">Width</span>="574px" <span style="COLOR: red">Height</span>="20"
                <span style="COLOR: red">ProgramQ</span>="ZPGMQ" <span style="COLOR: red">DisplayFields</span>="49" <span style="COLOR: red">DisplayRecords</span>="49"          
                <span style="COLOR: red">InitializeRecords</span>="49" <span style="COLOR: red">SubfilePage</span>="1" <span style="COLOR: red">SubfileSize</span>="50"&gt;
      &lt;<span style="COLOR: maroon">mdf:DdsSubfile</span><span style="COLOR: red">id</span>="MSGSFL" <span style="COLOR: red">style</span>="<span style="COLOR: red">LEFT</span>: 0px; <span style="COLOR: red">WIDTH</span>: 665px; <span style="COLOR: red">POSITION</span>: absolute; <span style="COLOR: red">TOP</span>: 0px;
                HEIGHT: 32px" <span style="COLOR: red">runat</span>="server" <span style="COLOR: red">ms_positioning</span>="GridLayout"
                <span style="COLOR: red">Height</span>="20" <span style="COLOR: red">Width</span>="574px" <span style="COLOR: red">CssClass</span>="DdsRecord" <span style="COLOR: red">Alias</span>="MSGSFL"&gt;
         &lt;<span style="COLOR: maroon">mdf:DdsCharField</span><span style="COLOR: red">id</span>="MSGSFL_ZMSGKY" <span style="COLOR: red">style</span>="<span style="COLOR: red">LEFT</span>: 8px; <span style="COLOR: red">POSITION</span>: absolute; <span style="COLOR: red">TOP</span>: 4px"   
                <span style="COLOR: red">runat</span>="server" <span style="COLOR: red">Height</span>="28px" <span style="COLOR: red">Width</span>="656px" <span style="COLOR: red">CssClass</span>="DdsSflMsgField"           
                <span style="COLOR: red">Length</span>="76" <span style="COLOR: red">Usage</span>="OutputOnly"&gt;
         &lt;/<span style="COLOR: maroon">mdf:DdsCharField</span>&gt;
      &lt;/<span style="COLOR: maroon">mdf:DdsSubfile</span>&gt;
&lt;/<span style="COLOR: maroon">mdf:DdsSubfileControl</span>&gt;</span></pre>

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) 
