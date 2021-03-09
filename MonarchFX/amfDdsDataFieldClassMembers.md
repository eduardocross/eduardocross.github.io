---
title: DdsDataField Members

Id: amfDdsDataFieldClassMembers
TocParent: amfDdsDataFieldClass
TocOrder: 5

keywords: DdsDataField class
keywords: DdsDataField class, all members
keywords: members [ASNA.Monarch.WebDspF], DdsDataField class

---

[ DdsDataField Overview](amfDdsDataFieldClass.html) 

#### Constructors
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="30%" />
          <col width="70%" />
          </colgroup>
          <tr><th>Method</th>
  <th>Description</th>
          </tr>

          <tr>
<td><img  alt="public method" src="../Images/Methods.bmp" width="16" border="0" />  [DdsDataField](amfDdsDataFieldClassConstructors.html)</td>
          <td>Instances of this class cannot be created directly; they can only be created as base class instances of the [derived classes](amfDdsDataFieldDerivedClasses.html).</td>
          </tr>
</table>

<br />

#### Public Properties
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
           <col width="30%" />
           <col width="70%" />
          </colgroup>
          <tr><th>Property</th>
          <th>Description</th>
          </tr>
          <tr>
<td><img  height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" />  [  Alias](amfDdsDataFieldClassAliasProperty.html)</td>
 <td>Gets or sets an alternate field name for the field.</td>
          </tr>
          <tr><td><img  height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [AutoPostBack](amfDdsDataFieldClassAutoPostBackProperty.html)</td>
 <td>Gets or sets a boolean value that if true, causes the control to generate a post back to the server when the field is output-only.</td>
          </tr>
          <tr><td><img  height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [AutoPostBackKey](amfDdsDataFieldClassAutoPostBackKeyProperty.html)</td>
 <td>Gets or sets the aidkey to return to the server when **AutoPostBack**  is True.</td>
          </tr>
          <tr><td>![public property" src="../Images/property.bmp" width="16" border="0](../Images/property.bmp" />  [ChangeInd](amfDdsDataFieldClassChangeIndProperty.html)</td>
 <td>Gets or sets the response indicator to set 'on' when this field changes.</td>
          </tr>
          <tr>
<td><img  height="16)  [  Compare](amfDdsDataFieldClassCompareProperty.html)</td>
 <td>Gets or sets the relational operator and value used to validate user data input.</td>
          </tr>
		<tr>
            <td>![](Images/property.bmp)[
              MandatoryEnter](amfDdsDataFieldClassMandatoryEnterProperty.html)
            </td>
            <td>Determines whether the field must have a value entered into it for operations to continue.</td>
          </tr>
		  <tr>
            <td>![](Images/property.bmp)[
              MandatoryFill](amfDdsDataFieldClassMandatoryFillProperty.html)
            </td>
            <td>Determines whether a character must be entered each position in the field.</td>
          </tr>
          <tr><td>![](Images/property.bmp)  [MessageId](amfDdsDataFieldClassMessageIdProperty.html)</td>
 <td>Gets or sets the conditional value that controls the messages to be associated with this field when a message file is used.</td>
          </tr>
          <tr><td>![](Images/property.bmp)  [PositionCursor](amfDdsDataFieldClassPositionCursorProperty.html)</td>
 <td>Gets or sets a string containing the position cursor attribute value for the **DdsDataField** .</td>
          </tr>
          <tr><td>![](Images/property.bmp) [Protect](amfDdsDataFieldClassProtectProperty.html)</td>
 <td>Gets or sets the *RPG indicator*  expression that, when evaluated, determines if the field is output-only(read-only).</td>
          </tr>
          <tr><td>![](Images/property.bmp) [SubmitValue](amfDdsDataFieldClassSubmitValueProperty.html)</td>
 <td>Gets or sets a value for the field that when selected, is treated the same as if the user had entered this value and pressed&lt;enter&gt;.</td>
          </tr>
          <tr><td>![](Images/property.bmp) [Text](amfDdsDataFieldClassTextProperty.html)</td>
 <td>Gets or sets the value (in string form) of the field.</td>
          </tr>
          <tr><td>![](Images/property.bmp) [Usage](amfDdsDataFieldClassUsageProperty.html)</td>
 <td>Gets or sets how the field is used, output, input, both (input and output),or hidden.</td>
          </tr>
          <tr><td>![](Images/property.bmp) [Values](amfDdsDataFieldClassValuesProperty.html)</td>
 <td>Gets or sets the list of valid values that can be input into this field.</td>
          </tr>
          <tr><td>![](Images/property.bmp) [ValuesStyle](amfDdsDataFieldClassValuesStyleProperty.html)</td>
 <td>Gets or sets the control style used to specify if the field is TextBox or Dropdown with text, values, or both.</td>
          </tr>
          <tr><td>![](Images/property.bmp) [ValuesText](amfDdsDataFieldClassValuesTextProperty.html)</td>
 <td>Gets or sets a list of text to be shown when using the dropdown **ValuesStyle** .</td>
          </tr>
          <tr><td>![](Images/property.bmp) [VirtualRowCol](amfDdsDataFieldClassVirtualRowColProperty.html)</td>
 <td>Gets or sets the row and column that this field is reported on in the Displayfile.</td>
          </tr>
</table>

#### Public Methods
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
          <col width="30%" />
          <col width="70%" />
          </colgroup>
          <tr><th>Method</th>
          <th>Description</th>
          </tr>
          <tr>
<td><img alt="public method" src="../Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" border="0" />  [  LoadPostData](amfDdsDataFieldClassLoadPostDataMethods.html)</td>
 <td>Overloaded. Processes postback data for an ASP.NET server control and returns **True**  if the server control's state changed as a result of the postback; otherwise **False** .</td>
          </tr>
          <tr><td><img alt="public method" src="../Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" border="0" />  [  ParseValues](amfDdsDataFieldClassParseValuesMethod.html)</td>
 <td>Parses the values to be displayed when the field is of type dropdown.</td>
          </tr>
          <tr>
<td><img alt="public method" src="../Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" border="0" />  [  RaisePostDataChangedEvent](amfDdsDataFieldClassRaisePostDataChangedEventMethod.html)</td>
 <td>Signals the server control object to notify the ASP.NET application that the state of the control has changed.</td>
          </tr>
          <tr>
<td><img alt="public method" src="../Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" border="0" />  [  RenderBeginTag](amfDdsDataFieldClassRenderBeginTagMethod.html)</td>
 <td>Renders the HTML opening tag of the control into the specified *writer* .</td>
          </tr>
          <tr>
<td><img alt="public method" src="../Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" border="0" />  [  RenderEndTag](amfDdsDataFieldClassRenderEndTagMethod.html)</td>
 <td>Renders the HTML closing tag of the control into the specified *writer* .</td>
          </tr>
          <tr>
<td><img alt="public method" src="../Images/Methods.bmp" style="WIDTH:16px; HEIGHT:16px" width="16" border="0" />  [  ResetMessageId](amfDdsDataFieldClassResetMessageIdMethod.html)</td>
 <td>Resets the [MessageId](amfDdsDataFieldClassMessageIdProperty.html) property.</td>
          </tr>
</table>

#### See Also
<dl>
        <dd>[DdsDataField
      Class](amfDdsDataFieldClass.html)</dd>
        <dd>[
      MsgIdProperty Class](amfMsgIdPropertyClass.html)</dd>
       <dd>[
      Derived Classes](amfDdsDataFieldDerivedClasses.html) </dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
</dl>

