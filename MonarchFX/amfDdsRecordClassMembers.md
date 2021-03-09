---
title: DdsRecord Members

Id: amfDdsRecordClassMembers
TocParent: amfDdsRecordClass
TocOrder: 5

keywords: DdsRecord class
keywords: DdsRecord class, all members
keywords: ASNA.Monarch.WebDspF.DdsRecord class
keywords: members [ASNA.Monarch.WebDspF], DdsRecord class

---

[DdsRecord Overview](amfDdsRecordClass.html) 

This member's page does not include members inherited from System.Web.UI.WebControls.WebControl or System.Web.UI.WebControls.Panel. See [DdsRecord Class Properties](amfDdsRecordClassPropertiesMain.html) for a listing of additional methods that are inherited by this class.

#### Constructors
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="20%" /><col width="70%" />
          </colgroup>
          <tr><th>Method</th>
              <th>Description</th>
          </tr>
          <tr valign="top">
            <td><img alt="public method" src="../Images/Methods.bmp" width="16" height="16" border="0" /> 
            [
            DdsRecord](amfDdsRecordClassConstructors.html)</td>
            <td>Creates a new instance of a       
 **DdsRecord**  object.</td>
          </tr>
</table>

#### Public Methods
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
          <col width="20%" />
          <col width="70%" />
          </colgroup>
          <tr><th>Method</th>
          <th>Description</th>
          </tr>
          <tr>
            <td><img alt="public methods" src="../Images/Methods.bmp" width="16" height="16" border="0" /> [CollectResponseIndicators](amfDdsRecordClassCollectResponseIndicatorsMethod.html)</td>
            <td>Collects an array
            containing the response indicators for the record.</td>
          </tr>
          <tr>
            <td><img alt="public methods" src="../Images/Methods.bmp" width="16" height="16" border="0" /> [GetDdsFile](amfDdsRecordClassGetDdsFileMethod.html)</td>
            <td>Returns an instance of a 
            [
            DdsFile](amfDdsFileClass.html) object for the 
 **DdsRecord** .</td>
          </tr>
          <tr>
            <td style="height: 29px"><img alt="public methods" src="../Images/Methods.bmp" width="16" height="16" border="0" /> [GetResultIndicator](amfDdsRecordClassGetResultIndicatorMethod.html)</td>
            <td style="height: 29px">Returns the integer value
            for the result indicator specified.</td>
          </tr>
          <tr>
            <td><img alt="public methods" src="../Images/Methods.bmp" width="16" height="16" border="0" /> [IsAidKeyInEffect](amfDdsRecordClassIsAidKeyInEffectMethods.html)</td>
            <td>Overloaded. Returns a
            boolean value indicating if the specific key or
            indicator is in effect. If in effect, the
            resulting indicator or resulting indicator and text are
            also returned.</td>
          </tr>
          <tr>
            <td><img alt="public methods" src="../Images/Methods.bmp" width="16" height="16" border="0" />
            [
            IsNotFalse](amfDdsRecordClassIsNotFalseMethods.html)</td>
            <td>Overloaded. Returns 
 **true**  if the condition or the condition
            for a specific field is not false.</td>
          </tr>
          <tr>
            <td><img alt="public methods" src="../Images/Methods.bmp" width="16" height="16" border="0" /> [IsTrue](amfDdsRecordClassIsTrueMethods.html)</td>
            <td>Overloaded. Returns 
 **true**  if the condition or the condition
            for a specific field is true.</td>
          </tr>
          <tr>
            <td><img alt="public methods" src="../Images/Methods.bmp" width="16" height="16" border="0" /> [ReadBrowser](amfDdsRecordClassReadBrowserMethod.html)</td>
            <td>Reads the browser.</td>
          </tr>
          <tr>
            <td><img alt="public methods" src="../Images/Methods.bmp" width="16" height="16" border="0" /> [WasAidKeyInEffect](amfDdsRecordClassWasAidKeyInEffectMethods.html)</td>
            <td>Overloaded. Returns a
            boolean value indicating if the specific key or
            indicator expression was in effect for the
            DdsRecord.  If in effect, the resulting indicator
            or resulting indicator and text are
            also returned.</td>
          </tr>
</table>

#### Public Properties
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup>
           <col width="20%" />
           <col width="70%" />
          </colgroup>
          <tr><th>Property</th>
          <th>Description</th>
          </tr>
          <tr>
            <td><img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [Alias](amfDdsRecordClassAliasProperty.html)</td>
            <td>Gets or sets an alternate
            format name to be used by the compiler.</td>
          </tr>
          <tr>
            <td><img height="16" alt="public property" src="../Images/property.bmp" width="16" border="0" /> [AttnKeys](amfDdsRecordClassAttnKeysProperty.html)</td>
            <td>Gets or sets the keys the
            user can press, the message to be displayed, and the
            response indicators to turn on. No input data is
            transmitted from the Browser.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [ChangeInd](amfDdsRecordClassChangeIndProperty.html)</td>
            <td>Gets or sets the response
            indicator to set 'on' when this record changes.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [CommandKeyInd](amfDdsRecordClassCommandKeyIndProperty.html)</td>
            <td>Gets or sets the response
            indicator to set 'on' when the user presses any command
            key other than "enter".</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [CursorField](amfDdsRecordClassCursorFieldProperty.html)</td>
            <td>Gets or sets the field
            name receiving the name of the field where
            the cursor is located.</td>
          </tr>
           <tr>
            <td>![](Images/property.bmp) [CursorLocation](amfDdsRecordClassCursorLocationProperty.html)</td>
            <td>Gets or sets where on the page
            the cursor is currently located.</td>
          </tr>

          <tr>
            <td>![](Images/property.bmp) [CursorRecord](amfDdsRecordClassCursorRecordProperty.html)</td>
            <td>Gets or sets the field
            name receiving the name of the record where
            the cursor is located.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [EraseFormats](amfDdsRecordClassEraseFormatsProperty.html)</td>
            <td>Gets or sets an instance of

 **ASNA.Monarch.WebDspF.EraseProperty**  specifying
            which record formats are to be erased from the display
            when this record is written.</td>
          </tr>
           <tr>
            <td>![](Images/property.bmp) [FooterBarControlID](amfDdsRecordClassFoooterBarControlIDProperty.html)</td>
            <td>Gets or sets a string identifying the [DdsBar](amfDdsBarClass.html) control to be used as a footer in a mobile application.</td>
          </tr>

          <tr>
            <td>![](Images/property.bmp) [FuncKeys](amfDdsRecordClassFuncKeysProperty.html)</td>
            <td>Gets or sets the keys the
            user can press, the message to be displayed, and the
            response indicators to turn on. Input data is
            transmitted from the browser.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [NavigationBarControlID](amfDdsRecordClassNavigationBarControlIDProperty.html)</td>
            <td>Gets or sets a string identifying the [DdsBar](amfDdsBarClass.html) control to be used as a top navigation bar in a mobile application.</td>
          </tr>
		   <tr>
                <td>
                    ![](Images/property.bmp)
                    [
                        Protect
                    ](amfDdsRecordClassProtectProperty.html)
                </td>
                <td>
                    Sets whether all input-capable fields already on the display file are made output-only (protected).
                </td>
            </tr>
          <tr>
            <td>![](Images/property.bmp) [ReturnData](amfDdsRecordClassReturnDataProperty.html)</td>
            <td>Gets or sets the boolean
            value specifying whether to return the same data that
            was returned on the previous input operation sent to
            this record format (RTNDATA). The default is 
 **False** .</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [Window](amfDdsRecordClassWindowProperty.html)</td>
            <td>Gets or sets a boolean
            value indicating if the record is displayed as a popup
            window. The default is 
 **False** .</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [WindowFeatures](amfDdsRecordClassWindowFeaturesProperty.html)</td>
            <td>Gets or sets a value
            specifying the features of the windows ornaments for
            the dialog box used as parameters to the
            ShowModalDialog of IE, which control some of the
            features of the pop-up windows.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [WindowHeight](amfDdsRecordClassWindowHeightProperty.html)</td>
            <td>Gets or sets the height of
            the window in pixels.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [WindowLeft](amfDdsRecordClassWindowLeftProperty.html)</td>
            <td>Gets or sets the
            x-coordinate of the windows left edge in pixels.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [WindowLeftField](amfDdsRecordClassWindowLeftFieldProperty.html)</td>
            <td>Gets or sets the name of
            the field containing the x-coordinate of the windows
            left edge in pixels.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [WindowTitle](amfDdsRecordClassWindowTitleProperty.html)</td>
            <td>Gets or sets the text to
            use as the window title (WDWTITLE).</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [WindowTitleField](amfDdsRecordClassWindowTitleFieldProperty.html)</td>
            <td>Gets or sets the name of
            the field containing the text to use as the window
            title (WDWTITLE).</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [WindowTop](amfDdsRecordClassWindowTopProperty.html)</td>
            <td>Gets or sets the top
            position of the window in pixels.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [WindowStyle](amfDdsRecordClassWindowStyleProperty.html)</td>
            <td>Gets or sets the Window
            Pop-up implementation style.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [WindowTopField](amfDdsRecordClassWindowTopFieldProperty.html)</td>
            <td>Gets or sets the name of
            the field containing the top edge of the window in
            pixels.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [WindowWidth](amfDdsRecordClassWindowWidthProperty.html)</td>
            <td>Gets or sets the width of
            the window in pixels.</td>
          </tr>
</table>

#### See Also
[DdsRecord
      Class](amfDdsRecordClass.html)
      <br />
      [DdsFile Class](amfDdsFileClass.html)
      <br />
      [
      ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)

