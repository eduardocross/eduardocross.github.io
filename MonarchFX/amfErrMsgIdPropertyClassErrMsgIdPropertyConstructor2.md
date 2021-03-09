---
title: ErrMsgIdProperty Constructor(String)

Id: amfErrMsgIdPropertyClassErrMsgIdPropertyConstructor2
TocParent: amfErrMsgIdPropertyClassConstructors
TocOrder: 20

---

This method constructs a new instance of an **ErrMsgIdProperty** object with values established.

#### Syntax
<pre class="prettyprint"> **BegConstructor ErrMsgIdProperty Access(*Public)
  DclSrParm *propString*  Type(*String)** </pre>

#### Parameters
<dl>
        <dt>
 *propString* 
        </dt>
        <dd>String containing an array of value/conditions error
        messages using a message file.</dd>
</dl>

#### Remarks
***propString*** contains an array, each array element contains:

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
- *Data Definitions* : Optionally field name that
        contains one or more substitution values used as data
        fields within the predefined message. The substitution
        values take the place of the substitution variables defined
        in the message text when the message was initially defined.
        The field must exist in the record format and defined as
        *Char.

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ ErrMsgIdProperty Class](amfErrMsgIdPropertyClass.html) <br clear="none" /> [ ErrMsgIdProperty Class Members](amfErrMsgIdPropertyClassMembers.html) <br clear="none" /> [ DdsField.ErrMsgId Property Class](amfDdsFieldClassErrorMessageIdProperty.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
