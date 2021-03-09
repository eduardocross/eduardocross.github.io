---
title: DdsSubfileControl.SubfileMessageId Property

Id: amfddsSubfileControlClassSubfileMessageIdProperty
TocParent: amfddsSubfileControlClassPropertiesMain
TocOrder: 210

keywords: SubfileMessageId property
keywords: DdsSubfileControl.SubfileMessageId property
keywords: SubfileMessageID Property Editor, setting values
keywords: conditioning expressions, controlling subfile control messages
keywords: indicator expressions, controlling subfile control messages
keywords: message files, file name
keywords: error message file name
keywords: error messages, file name
keywords: message files, display conditions
keywords: error messages, display condition
keywords: error message display condition
keywords: message files, message id
keywords: error messages, id
keywords: error message id
keywords: message files, response indicators
keywords: error messages, response indicators
keywords: error message response indicators
keywords: message files, data field
keywords: error messages, data field
keywords: error message data field
keywords: how to, set error message objects
keywords: how to, get error message objects
keywords: subfiles, message id
keywords: subfile records, setting message id
keywords: subfile records, getting message id
keywords: subfile controls, setting message id
keywords: subfile controls, getting message id
keywords: web controls, message id

---

Gets or sets a new instance of an [ ErrMsgIdProperty](amfErrMsgIdPropertyClass.html) object that identifies a message ID number to be associated with this control.

#### Syntax
<pre class="prettyprint"> **BegProp SubfileMessageId Access(*Public) Type([ErrMsgIdProperty](amfErrMsgIdPropertyClass.html))
   BegGet;  BegSet** </pre>

#### Property Values
**ErrMsgIdProperty** object containing the values shown below.

#### Remarks
To set this property at design-time, click on the right of the **SubfileMessageId** property and the **SubfileMessageId Property Editor** will display as shown below. Enter the condition, message Id, message file, response indicators, and data field information. 

- *Condition* : Enter the indicator expression under
        which the message will be displayed. Text cannot be
        specified.
- *MsgID:*  Enter the message identifier for the message
        to be displayed.
- *MsgFile* : Enter the library (optional) and message
        file name as [library/]messagefile.
- *ResponseInd:*  Optionally enter the response
        indicator that will be set *ON. If the response indicator
        is entered, it should be the same as the option indicator
        used to condition the MSGID keyword. After the display of
        the message, this indicator is set *OFF. However, if the
        response indicator is also specified on another keyword,
        the on/off setting is based on the results of that
        function.
- *DataField* : Optionally enter the field name that
        contains one or more substitution values used as data
        fields within the predefined message. The substitution
        values take the place of the substitution variables defined
        in the message text when the message initially defined.
        This field must exist in the record format and defined as
        *Char.

In the example below, if *IN31 is *ON, myMsgId31 in myMsgFile will be displayed for DataField CSRFLD and *IN98 will be set *ON.

![](Images/zzSubfileControlSubfileMessageId.JPG) 

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ DdsSubfileControl Class Members](amfddsSubfileControlClassMembers.html) <br /> [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) <br />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)<br />[ ErrMsgIdProperty Class](amfErrMsgIdPropertyClass.html) 
