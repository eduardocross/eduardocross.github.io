---
title: DdsSubfile Members

Id: amfDdsSubfileClassMembers
TocParent: amfDdsSubfileClass
TocOrder: 5

keywords: DdsSubfile class
keywords: DdsSubfile class, all members
keywords: ASNA.Monarch.WebDspF.DdsSubfile class
keywords: members [ASNA.Monarch.WebDspF], DdsSubfile class

---

      [DdsSubfile
      Overview](amfDdsSubfileClass.html)

This document lists the members of the DdsSubfile class. It does not include properties inherited from System.Web.UI.WebControls.WebControl and System.Web.UI.WebControls.Panel, nor those inherited from the base classes. See [DdsSubfile Class Properties](amfDdsSubfileClassPropertiesMain.html) for a list that includes inherited properties.

#### Constructors
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="20%" /><col width="70%" />
          </colgroup>
          <tr><th>Method</th>
              <th>Description</th>
          </tr>
          <tr valign="top">
            <td><img alt="public method" src="../Images/Methods.bmp" />
              [
              DdsSubfile](amfDdsSubfileClassConstructors.html)
            </td>
            <td>Creates a new instance of a

 **DdsSubfile** .</td>
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
            format name to be used by the compiler. (Inherited from
            DdsRecord.)</td>
          </tr>
          <tr>
            <td><img alt="public property" src="../Images/property.bmp" />
              [
              AttnKeys](amfDdsRecordClassAttnKeysProperty.html)
            </td>
            <td>Gets or sets the keys the
            user can press, the message to be displayed, and the
            response indicators to turn on. No input data is
            transmitted from the Browser. (Inherited from
            DdsRecord.)</td>
          </tr>
          <tr>
            <td style="height: 52px">![](Images/property.bmp)
              [
              ChangeInd](amfDdsRecordClassChangeIndProperty.html)
            </td>
            <td style="height: 52px">Gets or sets the response
            indicator to set *ON when this record changes.
            (Inherited from DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [CommandKeyInd](amfDdsRecordClassCommandKeyIndProperty.html)</td>
            <td>Gets or sets the response
            indicator to set 'on' when the user presses any command
            key other than "enter". (Inherited from
            DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [CursorField](amfDdsRecordClassCursorFieldProperty.html)</td>
            <td>Gets or sets the field
            name receiving the name of the field where
            the cursor is located. (Inherited from DdsRecord.)</td>
          </tr>
                     <tr>
            <td>![](Images/property.bmp) [CursorLocation](amfDdsRecordClassCursorLocationProperty.html)</td>
            <td>Gets or sets where on the page
            the cursor is currently located. (Inherited from DdsRecord.)</td>
          </tr>

          <tr>
            <td>![](Images/property.bmp) [CursorRecord](amfDdsRecordClassCursorRecordProperty.html)</td>
            <td>Gets or sets the field
            name receiving the name of the record where
            the cursor is located. (Inherited from DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              DataOnly](amfDdsSubfileClassDataOnlyProperty.html)
            </td>
            <td>Gets or sets a boolean
            value indicating whether the subfile has data only and
            the subfile contents are not to be rendered to the
            browser. The default is 
 **False** .</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) DroppedRowHeight</td>
            <td>Deprecated.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              EraseFormats](amfDdsRecordClassEraseFormatsProperty.html)
            </td>
            <td>Gets or sets an instance of

 **ASNA.Monarch.WebDspF.EraseProperty**  specifying
            which records are to be erased from the display when
            this record is written. (Inherited from
            DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              FuncKeys](amfDdsRecordClassFuncKeysProperty.html)
            </td>
            <td>Gets or sets the keys
            the user can press, the message to be displayed, and
            the response indicators to turn on. Input data is
            transmitted from the browser. (Inherited from
            DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              NextChanged](amfDdsSubfileClassNextChangedProperty.html)
            </td>
            <td>Gets or sets a string
            containing *False or *True indicating if the record has
            changed and whether READC will read the record.
            (SFLNXTCHG)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              ReturnData](amfDdsRecordClassReturnDataProperty.html)
            </td>
            <td>Gets or sets the boolean
            value specifying whether to return the same data that
            was returned on the previous input operation sent to
            this record format (RTNDATA). The default is 
 **False** . (Inherited from
            DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [RowsCssClasses](amfDdsSubfileClassRowsCssClassesProperty.html)</td>
            <td>Gets or sets a string
            containing a space or comma separated list of css
            classes to use for alternating rows.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) SflDropKey</td>
            <td>Deprecated. See SubfileControl class [SflDropKey](amfDdsSubfileControlClassSflDropKeyProperty.html) property.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) SflFoldKey</td>
            <td>Deprecated. See SubfileControl class [SflFoldKey](amfDdsSubfileControlClassSflFoldKeyProperty.html) property.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) SubfileDrop</td>
            <td>Deprecated.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) SubfileFold</td>
            <td>Deprecated.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) SubfileMode</td>
            <td>Deprecated.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              UseSubfilePaging](amfDdsSubfileClassUseSubfilePagingProperty.html)
            </td>
            <td>Gets or sets a boolean
            value indicating if subfile paging is used. The
            default is 
 **False** .</td>
          </tr>
			<tr>
				<td>![](Images/property.bmp)[VirtualRowCol](amfDdsSubfileClassVirtualRowColProperty.html)
				</td>
				<td>Gets or sets a Row, Column value for the upper-Left corner of the Subfile screen area, as defined by DDS.
				</td>
			</tr>
			<tr>
				<td>![](Images/property.bmp)[VirtualWidth](amfDdsSubfileClassVirtualWidthProperty.html)
				</td>
				<td>Gets or sets and integet value for the horizontal positions occupied by fields in a subfile record (as described by DDS).
				</td> 
			</tr>
			<tr>
				<td>![](Images/property.bmp)[VirtualRowsPerRecord](amfDdsSubfileClassVirtualRowsPerRecordProperty.html)
				</td>
				<td>Gets or sets an integer value for the vertical positions occupied by fields in a subfile record (as described by DDS).
				</td>
			</tr>
          <tr>
            <td>![](Images/property.bmp)
              [Window](amfDdsRecordClassWindowProperty.html)
            </td>
            <td>Gets or sets a boolean
            value indicating if this DdsRecord control is a window.
            The default is 
 **False** . (Inherited from
            DdsRecord.)</td>
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
            <td>![](Images/property.bmp)
              [
              WindowHeight](amfDdsRecordClassWindowHeightProperty.html)
            </td>
            <td>Gets or sets the height of
            the window in pixels. (Inherited from DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              WindowLeft](amfDdsRecordClassWindowLeftProperty.html)
            </td>
            <td>Gets or sets the
            x-coordinate of the windows left edge in pixels.
            (Inherited from DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              WindowLeftField](amfDdsRecordClassWindowLeftFieldProperty.html)
            </td>
            <td>Gets or sets the name of
            the field containing the x-coordinate of the windows
            left edge in pixels. (Inherited from DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              WindowTitle](amfDdsRecordClassWindowTitleProperty.html)
            </td>
            <td>Gets or sets the text to
            use as the window title (WDWTITLE). (Inherited from
            DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              WindowTitleField](amfDdsRecordClassWindowTitleFieldProperty.html)
            </td>
            <td>Gets or sets the name of
            the field containing the text to use as the window
            title (WDWTITLE). (Inherited from DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              WindowTop](amfDdsRecordClassWindowTopProperty.html)
            </td>
            <td>Gets or sets the top
            position of the window in pixels. (Inherited from
            DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              WindowTopField](amfDdsRecordClassWindowTopFieldProperty.html)
            </td>
            <td>Gets or sets the name of
            the field containing the top edge of the window in
            pixels. (Inherited from DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              WindowWidth](amfDdsRecordClassWindowWidthProperty.html)
            </td>
            <td>Gets or sets the width of
            the window in pixels. (Inherited from DdsRecord.)</td>
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
            <td><img alt="public method" src="../Images/Methods.bmp" />
              [
              GetConditionedValue](amfDdsSubfileClassGetConditionedValueMethod.html)
            </td>
            <td>Returns a string containing
            the conditional values for a specific field.</td>
          </tr>
          <tr>
            <td><img alt="public method" src="../Images/Methods.bmp" />
              [
              IsNotFalse](amfDdsSubfileClassIsNotFalseMethod.html)
            </td>
            <td>Returns 
 **True**  if the condition for the fieldID is not
            false.</td>
          </tr>
          <tr>
            <td><img alt="public method" src="../Images/Methods.bmp" />
              [IsTrue](amfDdsSubfileClassIsTrueMethod.html)
            </td>
            <td>Returns 
 **True**  if the condition for the fieldID is
            true.</td>
          </tr>
          <tr>
            <td><img alt="public method" src="../Images/Methods.bmp" />
              [
              ReadBrowser](amfDdsSubfileClassReadBrowserMethod.html)
            </td>
            <td>Reads the browser.</td>
          </tr>
          <tr>
            <td><img alt="public method" src="../Images/Methods.bmp" />
              [
              ResetDataOnly](amfDdsSubfileClassResetDataOnlyMethod.html)
            </td>
            <td>Resets the 
 **DataOnly**  property to the default value
            (*False).</td>
          </tr>
          <tr>
            <td><img alt="public method" src="../Images/Methods.bmp" />
              [
              ResetNextChanged](amfDdsSubfileClassResetNextChangedMethod.html)
            </td>
            <td>Resets the 
 **NextChanged**  property to the default
            value (*False).</td>
          </tr>
</table>

#### See Also
[DdsSubfile
      Class](amfDdsSubfileClass.html)
      <br />
      [
      ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)

