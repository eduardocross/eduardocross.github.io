---
title: DdsSubfileControl Members

Id: amfddsSubfileControlClassMembers
TocParent: amfddsSubfileControlClass
TocOrder: 5

keywords: DdsSubfileControl class
keywords: DdsSubfileControl class, all members
keywords: ASNA.Monarch.WebDspF.DdsSubfileControl class
keywords: members [ASNA.Monarch.WebDspF], DdsSubfileControl class

---

[ DdsSubfileControl Overview](amfddsSubfileControlClass.html) 

This document lists the members of the DdsSubfileControl class. It does not include properties inherited from System.Web.UI.WebControls.WebControl and System.Web.UI.WebControls.Panel, nor those inherited from the base classes. See [DdsSubfileControl Class Properties](amfDdsSubfileControlClassPropertiesMain.html) for a list that includes inherited properties.

#### Constructors
<table class="mytable" cellspacing="0" cellpadding="4" width="90%">
          <colgroup><col width="30%" /><col width="70%" />
          </colgroup>
          <tr><th>Method</th>
              <th>Description</th>
          </tr>
          <tr valign="top">
            <td><img alt="public method" src="Images/Methods.bmp" />
              [
              DdsSubfileControl](amfDdsSubfileControlClassConstructors.html)
            </td>
            <td>Creates a new instance of a

 **DdsSubfileControl** .</td>
          </tr>
</table>

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
            <td><img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [ActualMode](amfDdsSubfileControlClassActualModeProperty.html)</td>
            <td>Gets the subfile drop or
            fold state of the subfile control.</td>
          </tr>
          <tr>
            <td style="height: 30px"><img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [Alias](amfDdsRecordClassAliasProperty.html)</td>
            <td style="height: 30px">Gets or sets an alternate
            format name to be used by the compiler. (Inherited from
            DdsRecord.)</td>
          </tr>
          <tr>
            <td><img alt="public property" src="Images/property.bmp" />
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
            <td style="height: 28px">![public property" src="Images/property.bmp" width="16" border="0](Images/property.bmp" />
              [
              ChangeInd](amfDdsDataFieldClassChangeIndProperty.html)
            </td>
            <td style="height: 28px">Gets or sets the response
            indicator to set "on" when this record changes.
            (Inherited from DdsDataField.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              ClearRecords](amfddsSubfileControlClassClearRecordsProperty.html)
            </td>
            <td>Gets or sets a string value
            containing an indicator expression (condition) that
            when evaluated indicates 
 **True** , clears the data of the detail
            records (SFLCLR).</td>
          </tr>
          <tr><td>![](Images/property.bmp)
          	[ClickSetsCurrentRecord](amfDdsSubfileControlClassClickSetsCurrentRecordProperty.html)
			</td>
			<td>Gets or sets a boolean that determines if the mouse click is handled to update the selection state.
				Note: If set to false and CueCurrentRecord is true, when changing rows using the keyboard
				TAB key, the "current record" CSS style will be applied.
			</td>
		   </tr>
           <tr>
            <td>![](Images/property.bmp) [CommandKeyInd](amfDdsRecordClassCommandKeyIndProperty.html)</td>
            <td>Gets or sets the response
            indicator to set "on" when the user presses any command
            key other than "enter". (Inherited from
            DdsRecord.)</td>
          </tr>
          <tr>
			<td>![](Images/property.bmp) [CueCurrentRecord](amfDdsSubfileControlClassCueCurrentRecordProperty.html)
			</td>
			<td>Gets or sets a boolean value that determines if any of the two CSS styles should be applied when mouse 
				click event fires.
			</td>
		</tr>
          <tr>
            <td style="height: 52px">![](Images/property.bmp) [CursorField](amfDdsRecordClassCursorFieldProperty.html)</td>
            <td style="height: 52px">Gets or sets the field
            name that contains the name of the field
            where the cursor is located. (Inherited from
            DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [CursorRecord](amfDdsRecordClassCursorRecordProperty.html)</td>
            <td>Gets or sets the field
            name that contains the name of the record
            where the cursor is located. (Inherited from
            DdsRecord.)</td>
          </tr>
          <tr>
			<td>![](Images/property.bmp)
				[DblClickTargetField](amfDdsSubfileControlClassDblClickTargetFieldProperty.html)
			</td>
			<td>Gets or sets the string value for the name of the field to be modified when double-click is detected.
			</td>
		</tr>
		<tr>
			<td style="height: 73px">![](Images/property.bmp)
			[DblClickTargetValue](amfDdsSubfileControlClassDblClickTargetValueProperty.html)
			</td>
			<td style="height: 73px">Gets or sets the string value that the target field is to be set to. (Requires the DblClickTargetField 
				to contain a valid field name, of fields in the corresponding record).							
			</td>
		  </tr>
		  <tr>
			<td>![](Images/property.bmp)
			[DblClickKey](amfDdsSubfileControlClassDblClickKeyProperty.html)
			</td>
			<td>If this optional string value is not empty, the Key will be "pushed" (and the Page will be 
				submitted).						
			</td>
		  </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              DisplayFields](amfddsSubfileControlClassDisplayFieldsProperty.html)
            </td>
            <td>Gets or sets a string value
            containing an indicator expression (condition) that
            when evaluated indicates 
 **True** , causes the fields in the format
            to display (SFLDSPCTL).</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              DisplayRecords](amfddsSubfileControlClassDisplayRecordsProperty.html)
            </td>
            <td>Gets or sets a string value
            containing an indicator expression (condition), that
            when evaluated indicates 
 **True** , causes the records in the
            subfile to display (SFLDSP).</td>
          </tr>
          <tr>
            <td style="height: 73px">![](Images/property.bmp)
              [
              EraseFormats](amfDdsFieldClassErrorMessageProperty.html)
            </td>
            <td style="height: 73px">Gets or sets an instance of

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
            <td>Gets or sets the keys the
            user can press, the message to be displayed, and the
            response indicators to turn on. Input data is
            transmitted from the browser. (Inherited from
            DdsRecord.)</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              InitializeRecords](amfddsSubfileControlClassInitializeRecordsProperty.html)
            </td>
            <td>Gets or sets a string value
            containing an indicator expression that when turned on
            (*True), all of the records in the Subfile are
            initialized (SFLINZ).</td>
          </tr>
		  <tr>
            <td>![](Images/property.bmp)
              [
              InitNotActive](amfDdsSubfileClassInitNotActiveProperty.html)
            </td>
            <td>Boolean that sets whether added records will be active (treated as part of the subfile) before 
			their records are written to or changed.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              ProgramQ](amfddsSubfileControlClassProgramQProperty.html)
            </td>
            <td>Gets or sets the name of
            the field containing the name of the program queue used
            to build a message subfile (SFLPGMQ). Use the special
            value *PGM to specify the program using this
            subfile.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              ProgramQLen](amfddsSubfileControlClassProgramQLenProperty.html)
            </td>
            <td>Gets or sets the length of
            the 
            [
            ProgramQ](amfddsSubfileControlClassProgramQProperty.html) property field.</td>
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
            <td style="height: 52px"><img height="16) [SflDropKey](amfDdsSubfileControlClassSflDropKeyProperty.html)</td>
            <td style="height: 52px">Gets or sets the function
            key to press to switch between
            a truncated and folded display of the
            subfile record.</td>
          </tr>
          <tr>
            <td><img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [SflFoldKey](amfDdsSubfileControlClassSflFoldKeyProperty.html)</td>
            <td>Gets or sets the function
            key to press to switch between
            a folded and truncated display of the subfile
            record.</td>
          </tr>
          <tr>
            <td><img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [SflMode](amfDdsSubfileControlClassSflModeProperty.html)</td>
            <td>Gets or sets the name
            of the field in which the state of the subfile will be
            contained.</td>
          </tr>
          <tr>
            <td>![public property" src="Images/property.bmp" width="16" border="0](Images/property.bmp" /> [ShowRecordAtTop](amfDdsSubfileControlClassShowRecordAtTopProperty.html)</td>
            <td>Gets or sets a boolean
            value to indicate if the record number, contained
            in the hidden field in the 
 **ShowRecordField**  property, is
            displayed as the first record on the page. This is the
            equivalent to the SFLRCDNBR keyword *TOP.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [ShowRecordField](amfDdsSubfileControlClassShowRecordFieldProperty.html)</td>
            <td>Gets or sets the name
            of a hidden field containing the record
            number of the subfile record whose page is to be
            displayed. (SFLRCDNBR).</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [ShowRecordWithCursor](amfDdsSubfileControlClassShowRecordWithCursorProperty.html)</td>
            <td>Gets or sets a boolean
            value to indicate if the cursor is to be positioned in
            the record number, contained in the hidden field
            in the 
 **ShowRecordField**  property. This is
            equivalent to the SFLRCDNBR keyword CURSOR.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [SubfileCursorRecord](amfDdsSubfileControlClassSubfileCursorRecordProperty.html)</td>
            <td>Gets or sets the field name
            receiving the number of the subfile record where the
            cursor was positioned (SFLCSRRRN).</td>
          </tr>
          <tr>
            <td><img height="16) [SubfileDrop](amfDdsSubfileControlClassSubfileDropProperty.html)</td>
            <td>Gets or sets a set of
            conditional indicators that determine when
            the display of the subfile records is in truncated
            form.</td>
          </tr>
          <tr>
            <td><img height="16" alt="public property" src="Images/property.bmp" width="16" border="0" /> [SubfileFold](amfDdsSubfileControlClassSubfileFoldProperty.html)</td>
            <td>Gets or sets a set of
            conditional indicators that determine when
            the display of the subfile records is in folded
            form.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [SubfileEnd](amfDdsSubfileControlClassSubfileEndProperty.html)</td>
            <td>Gets or sets an indicator
            expression that when evaluated indicates whether 
 **SubfileEndTextOn** (True) or 
 **SubfileEndTextOff** (False) will be
            used (SFLEND).</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [SubfileEndTextOff](amfDdsSubfileControlClassSubFileEndTextOffProperty.html)</td>
            <td>Gets or sets a string
            containing the text to display in the lower right
            display location occupied by the subfile when the 
 **SubfileEnd**  condition
            evaluates False.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp) [SubfileEndTextOn](amfDdsSubfileControlClassSubFileEndTextOnProperty.html)</td>
            <td>Gets or sets a string
            containing the text to display in the lower right
            display location occupied by the subfile when the 
 **SubfileEnd**  condition
            evaluates True.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              SubfileMessage](amfddsSubfileControlClassSubfileMessageProperty.html)
            </td>
            <td>Gets or sets the conditions
            that control the error messages for the record.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              SubfileMessageId](amfddsSubfileControlClassSubfileMessageIdProperty.html)
            </td>
            <td>Gets or sets the conditions
            that control the error messages for the record
            when a message file is used.</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              SubfilePage](amfddsSubfileControlClassSubfilePageProperty.html)
            </td>
            <td>Gets or sets the number of
            records in the Subfile to be displayed at the same time
            (SFLPAG).</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              SubfileSize](amfddsSubfileControlClassSubfileSizeProperty.html)
            </td>
            <td>Gets or sets the number of
            records in the Subfile (SFLSIZ).</td>
          </tr>
          <tr>
            <td>![](Images/property.bmp)
              [
              SubfileStyle](amfddsSubfileControlClassSubfileStyleProperty.html)
            </td>
            <td>Gets or sets the style of
            the Subfile from a member of the 
            [
            SubfileStyles](amfSubfileStylesEnumeration.html) enumeration that specifies the HTML
            element used for the subfile data: Classic,
            Checkboxes, DropDown, ListBox, and RadioButton.</td>
          </tr>
          <tr>
			 <td>![](Images/property.bmp)
			 [VerticalScrollBar](amfDdsSubfileControlClassVerticalScrollBarProperty.html)
			 </td>
			 <td>Gets or sets a boolean value indicating whether a vertical scrollbar shows to the right of the subfile.<br/>
				 Note: This increases the subfile width by 19 pixels.</td>				
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
            <td>![](Images/property.bmp)
            [
            WindowFeatures](amfDdsRecordClassWindowFeaturesProperty.html)</td>
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
          <colgroup><col width="30%" /><col width="70%" />
          </colgroup>
          <tr><th>Method</th>
            <th>Description</th>
          </tr>
          <tr>
            <td><img alt="public method" src="Images/Methods.bmp" />
              [
              ResetSubfileMessage](amfDdsSubfileControlClassResetSubfileMessageMethod.html)
            </td>
            <td>Resets the 
            [
            SubfileMessage](amfddsSubfileControlClassSubfileMessageProperty.html) property to default values.</td>
          </tr>
          <tr>
            <td><img alt="public method" src="Images/Methods.bmp" />
              [
              ResetSubfileMessageId](amfDdsSubfileControlClassResetSubfileMessageIdMethod.html)
            </td>
            <td>Resets the 
            [
            SubfileMessageId](amfddsSubfileControlClassSubfileMessageIdProperty.html) property to default values.</td>
          </tr>
</table>

#### See Also
[ DdsSubfileControl Class](amfddsSubfileControlClass.html) <br /> [ ASNA.Monarch.WebDspF Namespace](amfWebDspFNamespace.html)
