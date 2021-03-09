---
title: DdsField.ErrorMessageId Property

Id: amfDdsFieldClassErrorMessageIdProperty
TocParent: amfDdsFieldClassProperties
TocOrder: 40

keywords: Web server controls [ASNA.Monarch], setting field error message ids
keywords: how to, set field control error message ids
keywords: how to, get field control error message ids
keywords: CssClass property, _Error appended
keywords: CSS, _Error appended
keywords: cascading style sheets, _Error appended
keywords: _Error
keywords: display files, setting field control error message ids
keywords: display files, getting field control error message ids
keywords: web controls, setting field control error message ids
keywords: web controls, getting field control error message ids
keywords: field controls, error message ids
keywords: indicator expressions, field control error message ids
keywords: conditioning expressions, field control error message ids
keywords: ErrorMessageId property
keywords: ErrorMessageID Property Editor, setting values
keywords: DdsField.ErrorMessageId property

---

Gets or sets the conditions that control the error message for the field when a message file is used.

#### Syntax
<pre class="prettyprint"> **BegProp ErrorMessageId Access(*Public) Type([ErrMsgIdProperty](amfErrMsgIdPropertyClass.html))
   BegGet;  BegSet** </pre>

#### Property Values
**ErrMsgIdProperty** object containing the conditional property values for the field when a message file is used.

#### Remarks
To set the **ErrorMessageId** property, click on the right hand side of the property window, and the **ErrorMessageId Property Editor** window will display as shown below.

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
        used to condition the ERRMSGID keyword. After the display
        of the error message, this indicator is set *OFF. However,
        if the response indicator is also specified on another
        keyword, the on/off setting is based on the results of that
        function.
- *DataField* : Optionally enter the field name that
        contains one or more substitution values used as data
        fields within the predefined message. The substitution
        values take the place of the substitution variables defined
        in the message text when the message initially defined.
        This field must exist in the record format and defined as
        *Char.

In the example below, if *IN31 is *ON, myMsgId31 in myMsgFile will be displayed for DataField CSRFLD and *IN98 will be set *ON. See [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) and [ Monarch Web Control Indicator Expression Tester](amfMonarchWebControlIndicatorExpressionTester.html) for more information on setting the conditional indicators and testing your expressions.

![](Images/ErrorMessageId.jpg) 

**Runtime Considerations for DdsCharField and DdsDecField:** 

When the control's [ ErrorMessage](amfDdsFieldClassErrorMessageProperty.html) or **ErrorMessageId** properties condition expression evaluates to TRUE at runtime, Monarch Framework appends "_Error" to the control's CssClass property. For example, if the CssClass property is "DdsCharField", then at runtime, the control's generated HTML class attribute would be **class="DdsCharField_Error"** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsField Class](amfDdsFieldClass.html) <br clear="none" /> [ Derived classes](amfDdsFieldClassDerivedClasses.html) <br clear="none" /> [ ErrMsgIdProperty Class](amfErrMsgIdPropertyClass.html) <br clear="none" /> [ Conditional Properties Overview](amfconConditionalPropertiesOverview.html) <br clear="none" /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html) 
