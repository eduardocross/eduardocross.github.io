---
title: DdsField.ErrorMessage Property

Id: amfDdsFieldClassErrorMessageProperty
TocParent: amfDdsFieldClassProperties
TocOrder: 30

keywords: Web server controls [ASNA.Monarch], setting field control error messages
keywords: CssClass property, _Error appended
keywords: _Error
keywords: CSS, _Error appended
keywords: cascading style sheets, _Error appended
keywords: how to, set field control error messages
keywords: how to, get field control error messages
keywords: display files, setting field control error messages
keywords: display files, getting field control error messages
keywords: web controls, setting field control error messages
keywords: web controls, getting field control error messages
keywords: field controls, error messages
keywords: indicator expressions, field control error messages
keywords: conditioning expressions, field control error messages
keywords: ErrorMessage property
keywords: ErrorMessage Property Editor, setting values
keywords: DdsField.ErrorMessage property

---

Gets or sets the conditions that control the error message for the field.

#### Syntax
<pre class="prettyprint"> **BegProp ErrorMessage Access(*Public) Type([ErrMsgProperty](amfErrMsgPropertyClass.html))
   BegGet;  BegSet** </pre>

#### Property Values
**ErrMsgProperty** object containing the conditional values controlling the error message for the field.

#### Remarks
To set the **ErrorMessage** property, click on the right hand side of the property window and the **ErrorMessage Property Editor** window will display as shown below.

Enter the message as the *Value* and the indicator expression ( *Condition* ) under which the message will be displayed. For example, a *Value* of "Re-enter your selection" and a *Condition* of 30 meaning the message you entered will be displayed when *IN30 is **True** . See [Conditional Properties Overview](amfconConditionalPropertiesOverview.html) and [ Monarch Web Control Indicator Expression Tester](amfMonarchWebControlIndicatorExpressionTester.html) for more information on setting the conditional indicators and testing your expressions.

Note:

DDS **ERRMSG** keyword allows specifying a response-indicator using the following format: ERRMSG('message-text' [response-indicator]), where [response-indicator] is an optional numeric indicator from 01 to 99. Monarch migrates **ERRMSG** as a property called **ErrorMessage** where the message-text *is not* quoted and the optional response-indicator is separated by blank space. The format used is the following: ErrorMessage='message-text [response-indicator] : conditional-indicator-expression'. For example, 30 (at position 7 and 8) and ERRMSG('Re-enter your selection') keyword, where the error message is conditioned on option indicator 30, and no response indicator is specified, would be migrated as ErrorMessage='Re-enter your selection : 30'. If the 'message-text' happens to end in a word that *looks like* an option indicator; for example 'Re-enter selection for Customer 07', then, instead of migrating the keyword as ErrorMessage='Re-enter selection for Customer 07 : 30' which the runtime would confuse 07 as a response indicator, it is necessary to resolve the ambiguity and migrate the keyword as ErrorMessage='Re-enter selection for Customer 07. : 30', thus eliminating the possibility of 07 to be confused with response indicator 07 - notice the dot appended at the end of the message-text -.

<img id="IMG1" src="Images/zzErrorMessagePropertyEditor.jpg" /> 

**Runtime Considerations for DdsCharField and DdsDecField:** 

When the control's **ErrorMessage** or [ ErrorMessageId](amfDdsFieldClassErrorMessageIdProperty.html) properties condition expression evaluates to TRUE at runtime, Monarch Framework appends "_Error" to the control's CssClass property. For example, if the CssClass property is "DdsCharField", then at runtime, the control's generated HTML class attribute would be **class="DdsCharField_Error"** .

#### Requirements
**Namespace:** [ASNA.Monarch.WebDspF](amfWebDspFNamespace.html)

**Assembly:** ASNA.Monarch.WebDspF.DLL

**Platforms:** Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, Windows 7, Windows 8 Pro, Windows 10 Pro

#### See Also
[DdsField Class](amfDdsFieldClass.html) <br clear="none" /> [ Derived classes](amfDdsFieldClassDerivedClasses.html) <br clear="none" /> [ ErrMsgProperty Class](amfErrMsgPropertyClass.html) <br clear="none" /> [ Conditional Properties Overview](amfconConditionalPropertiesOverview.html) <br clear="none" /> [ Monarch Web Control Indicator Expression Tester](amfMonarchWebControlIndicatorExpressionTester.html) <br clear="none" />[ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
