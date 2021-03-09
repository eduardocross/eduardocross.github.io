---
title: DdsSelection Field Choice Collection Editor

Id: amfUnderChoicesList
TocParent: amfConWidgetSupport
TocOrder: 10

keywords: ASNA Widget Controls
keywords: Choice Data Storage
keywords: DdsSelection Field Choice Storage
keywords: DdsSingleChoiceSelectionField Choice Dialog
keywords: Choice List Editor
keywords: Choice Collection Editor

---

<table>
			    <tr>
			      <td>
				   <span class="OH_MultiViewContainerPanelDhtmlTable">ASNA Monarch&#174; Framework 10.0
				   </span></td>
			    </tr>
</table>

# DdsSelectionField Choice Collection Editor

### Choice Collection
The functional portions of each SelectionField are the choices that make them up. The specifics of each choice are set through this Collection Editor. 

![](Images/ColumnCollectionEditor.png)
<br/>

The Choice Collection Editor has two panes:

- The left pane &#8212; contains a dynamic list of each choice included in the table.
- The right pane &#8212; displays the properties of the choice currently selected in the left pane.

The left pane has only four buttons associated with it:

- **Add**  &#8212; Adds a new choice with a generic name to the bottom of the collection.
- **Remove**  &#8212; Removes the selected choice from the collction.
- **Up Arrow**  &#8212; Shifts the selected choice up one rank in the collection.
- **Down Arrow**  &#8212; Shifts the selected choice down one rank in the collection.

The right pane contains multiple headings, each with associated properties

- Accessibility
					<ul>
					<li> *AccessKey*  &#8212; Gets or sets a key used to access the  control.
- *TabIndex*  &#8211; Sets the Tab Index for this control.

</li>
				<li>Appearance

- *BackColor*  &#8212; Sets the background color for this control.
- *BorderColor*  &#8212; Sets the border color for this control.
- *BorderStyle*  &#8212; Sets the border style for this control.
- *BorderWidth*  &#8212; Sets the border width for this control.
- *CssClass*  &#8212; Sets a CSS class to apply to the choice, useful for setting colors or transparency.
- *Font*  &#8212; Sets the font for this control.
- *ForeColor*  &#8212; Sets the font color for this control.

</li>
								<li>Behavior

- *ClientID*  &#8212; Sets the algorithm used to determine the ClientID Property. (Inherited from ASP.NET 
			WebControl.)
- *Enabled*  &#8212; Sets whether the control is enabled.
- *EnableTheming*  &#8212;Determines whether themes apply to this control.
- *EnableViewState*  &#8212; Determines whether the server control persists its view state, and the view state of any child controls it contains, to the requesting client.
- *SkinID*  &#8212; Gets or sets the skin to use on the control.
- *ToolTip*  &#8212; Sets the tooltip text for this control.
- *ValidateRequestMode*  &#8212; Sets a value that indicates whether the control checks client input from the browser for potentially dangerous values.
- *ViewStateMode*  &#8212; Used to change the result behavior of setting the EnableViewState of a page or a control to true.
- *VirtualRowCol*  &#8212; Sets the row and column that this field is reported on in the Display file.
- *Visible*  &#8212; Sets whether the control  is visible to the users.
- *VisibleCondition*  &#8212; Contains a conditional indicator expression that determines whether the column is visible.

</li>
					<li>Behaviour

- *AttnKey*  &#8212; Sets an AidKey to be pushed when this choice is selected.
- *ChoiceControlField*  &#8212;IBMi field associated with the choice.
- *ChoiceNumber*  &#8212; (Required) An ID number for this choice.
- *ChoiceText*  &#8212; String that appears in the field for the choice. Default: (Empty).
- *ChoiceTextField*  &#8212; Sets an IBM i fieldname that contains the text for the choice. Default: (Empty).
- *FuncKey*  &#8212; Sets the Function Key to call when the choice is selected.
- *SpaceBefore*  &#8212; Sets the space before the choice.

</li>
				<li>Layout

- Height &#8212; Sets the height of the choice.
- Width &#8212; Sets the width of the choice.

</li>

			</ul>

**Note** &#8212; The AttnKey and FuncKey properties are not present in SingleChoiceSelectionField and MultipleChoiceSelectionField.

Clicking **Okay** will save any changes made to the choice collection. Clicking **Close** will close the dialog without saving. 
