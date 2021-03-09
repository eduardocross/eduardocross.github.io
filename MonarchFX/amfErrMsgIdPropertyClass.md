---
title: ErrMsgIdProperty Class

Id: amfErrMsgIdPropertyClass
TocParent: amfWebDspFClassLibraryMain
TocOrder: 370

keywords: ErrMsgIdProperty class, about ErrMsgIdProperty
keywords: classes [ASNA.Monarch.WebDspF], ErrMsgIdProperty class
keywords: ErrorMessageID Property Editor, container

---

The <span> **ErrMsgIdProperty** </span> is a derived class that is a container for the [ ErrorMessageId](amfDdsFieldClassErrorMessageIdProperty.html) Property Editor and [ SubfileMessageId](amfddsSubfileControlClassSubfileMessageIdProperty.html) Property Editor values.

For a list of all members of this type, see [ ErrMsgIdProperty Members](amfErrMsgIdPropertyClassMembers.html).
<!--mine -->

#### Inheritance Hierarchy
<pre>[ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)
    [ASNA.Monarch.WebDspF.ConditionalProperty](amfConditionalPropertyClass.html)
 **ASNA.Monarch.WebDspF.ErrMsgIdProperty** </pre>      

#### Syntax
<pre class="prettyprint"> **Public class ErrMsgIdProperty Inherits ConditionalProperty** </pre>

#### Thread Safety
Any public static (Shared) members of this type are safe for multithreaded operations. Any instance members are not guaranteed to be thread safe.

#### Remarks
An instance of <span> **ErrMsgIdProperty** </span> represents a collection of messages by ID's for a control that is set when the **ErrorMessageId** or **SubfileMessageId** properties are set.

Each array element contains:

- *Condition* : An indicator expression under which the
        message will be displayed. Text cannot be specified.
- *Message ID:*  The message identifier for the
        message.
- *Message File* : The library (optional) and message
        file name as [library/]messagefile.
- *Response Indicator:*  Optionally response indicator
        that will be set *ON. If the response indicator is entered,
        it should be the same as the option indicator used to
        condition the ERRMSGID keyword.
- *Data Field Definitions* : Optionally field name that
        contains one or more substitution values used as data
        fields within the predefined message. The substitution
        values take the place of the substitution variables defined
        in the message text when the message was initially defined.
        The field must exist in the record format and defined as
        *Char.

![](Images/zzErrorMessageIdPropertyEditor.jpg) 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) <br clear="none" /> [ ErrMsgIdProperty Members](amfErrMsgIdPropertyClassMembers.html) <br clear="none" /> [ ConditionalProperty Class](amfConditionalPropertyClass.html) <br clear="none" /> [ DdsField.ErrorMessageId Property](amfDdsFieldClassErrorMessageIdProperty.html) 
