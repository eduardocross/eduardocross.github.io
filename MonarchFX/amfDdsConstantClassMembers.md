---
title: DdsConstant Members

Id: amfDdsConstantClassMembers
TocParent: amfDdsConstantClass
TocOrder: 5

keywords: DdsConstant class
keywords: DdsConstant class, all members
keywords: members [ASNA.Monarch.WebDspF], DdsConstant class

---

This topic contains a listing of the constructors, properties, and methods of the [DdsConstant Class](amfDdsConstantClass.html).

This member's page does not include inherited properties, methods, or fields. See [DdsConstant Class Properties](amfDdsConstantClassPropertiesMain.html) for a full listing of additional members that are inherited by this class.

#### Constructors
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Method</th>
            <th>Description</th>
          </tr>

          <tr>
            <td>![](../Images/Methods.bmp" />
              [
              DdsConstant](amfDdsConstantClassConstructors.html)
            </td>
            <td>This method constructs a
            new instance of a 
 **DdsConstant**  object.</td>
          </tr>
</table>

<br />

#### Public Properties
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Property</th>
            <th>Description</th>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [Color](amfDdsFieldClassColorProperty.html)
            </td>
            <td>Gets or sets the
            conditional values that control the color of the
            field.  (Inherited from DdsField.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              Comment](amfDdsFieldClassCommentProperty.html)
            </td>
            <td>Gets or sets a comment
            associated with the field.  (Inherited from
            DdsField.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              ErrorMessage](amfDdsFieldClassErrorMessageProperty.html)
            </td>
            <td>Gets or sets the conditions
            that control the error messages for the field. 
            (Inherited from DdsField.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              ErrorMessageId](amfDdsFieldClassErrorMessageIdProperty.html)
            </td>
            <td>Gets or sets the conditions
            that control the error message for the field when a
            message file is used.  (Inherited from
            DdsField.)</td>
          </tr>
		  <tr>
		  <td>![](Images/property.bmp)
		   [InvertFontColor](amfDdsFieldClassInvertFontColorProperty.html)</td>
		   <td>Inverts the font and background color of the text.</td>
		   </tr>
          <tr>
			<td>
				![](Images/property.bmp) [MsgConFile](amfDdsConstantClassMsgConFileProperty.html)
				</td>
			<td>Gets or sets the **Name**  of the Message File, without the **amfx**  
			extension.
				</td>
		</tr>
		<tr>
			<td>
				![](..\Images\property.bmp) [MsgConID](amfDdsConstantClassMsgConIdProperty.html)
				</td>
			<td>Gets or sets the Message-ID specifying the text to use as the value of the constant field. 				</td>
		</tr>
		<tr>
			<td>![](..\Images\property.bmp) [MsgConLength](amfDdsConstantClassMsgConLengthProperty.html)

						</td>
						<td>Gets or sets the maximum number of characters to copy from the message. Note: This property is different from the Web control's inherited **Length**  property.
						</td>
					</tr>
          <tr>
            <td>![public methods](../Images/property.bmp)
              [Text](amfDdsConstantClassTextProperty.html)
            </td>
            <td>Gets or sets a string
            containing either a constant to display, or the special
            value *DATE, *TIME, *USER or *SYSNAME.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              Visible](amfDdsFieldClassVisibleProperty.html)
            </td>
            <td>Gets or sets a boolean
            value that indicates whether a field is visible
            and rendered on the page.  (Inherited from
            DdsField.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              VisibleCondition](amfDdsFieldClassVisibleConditionProperty.html)
            </td>
            <td>Gets or sets the 
 *RPG indicator*  expression that, when
            evaluated, determines if the field 
            should be visible. (Inherited
            from DdsField.)</td>
          </tr>
</table>

#### Public Methods
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
            <col width="30%" />
            <col width="70%" />
          </colgroup>
          <tr>
            <th>Method</th>
            <th>Description</th>
          </tr>
          <tr>
            <td>![](Images/Methods.bmp)[
              EncodedLiteral](amfDdsConstantClassEncodedLiteralMethod.html)
            </td>
            <td>Takes a string value and
            encodes it to a valid XML element. "&lt;", "&gt;", and
            "&amp;" become "&amp;lt;" "&amp;gt;", and "&amp;amp"
            respectively. Consecutive spaces (after the first) are
            replaced with "&amp;nbsp;".</td>
          </tr>
          <tr>
            <td>![public methods](../Images/Methods.bmp)[
              EncodedNonBlank](amfDdsConstantClassEncodedNonBlankMethod.html)
            </td>
            <td>Takes a string value and
            encodes it to a valid XML element. "&lt;", "&gt;", and
            "&amp;" become "&amp;lt;" "&amp;gt;", and "&amp;amp"
            respectively.</td>
          </tr>
          <tr>
            <td>![public methods](../Images/Methods.bmp)[
              ResetText](amfDdsConstantClassResetTextMethod.html)
            </td>
            <td>Resets the 
 **Text**  property to default values.</td>
          </tr>
		  <tr>
		  <td><img src="../Images/property.bmp)
		   [Underline](amfDdsFieldClassUnderlineProperty.html)</td>
		   <td>Applies an underline to the text, and implements the DSPATR:UL keyword. (Inherited from DdsField.)</td>
		   </tr>
</table>

#### See Also
<dl>
        <dd>[DdsConstant Class](amfDdsConstantClass.html)</dd>
        <dd>[ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)</dd>
</dl>

